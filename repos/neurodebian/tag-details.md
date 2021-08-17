<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neurodebian`

-	[`neurodebian:bionic`](#neurodebianbionic)
-	[`neurodebian:bionic-non-free`](#neurodebianbionic-non-free)
-	[`neurodebian:bullseye`](#neurodebianbullseye)
-	[`neurodebian:bullseye-non-free`](#neurodebianbullseye-non-free)
-	[`neurodebian:buster`](#neurodebianbuster)
-	[`neurodebian:buster-non-free`](#neurodebianbuster-non-free)
-	[`neurodebian:focal`](#neurodebianfocal)
-	[`neurodebian:focal-non-free`](#neurodebianfocal-non-free)
-	[`neurodebian:hirsute`](#neurodebianhirsute)
-	[`neurodebian:hirsute-non-free`](#neurodebianhirsute-non-free)
-	[`neurodebian:latest`](#neurodebianlatest)
-	[`neurodebian:nd`](#neurodebiannd)
-	[`neurodebian:nd-non-free`](#neurodebiannd-non-free)
-	[`neurodebian:nd100`](#neurodebiannd100)
-	[`neurodebian:nd100-non-free`](#neurodebiannd100-non-free)
-	[`neurodebian:nd110`](#neurodebiannd110)
-	[`neurodebian:nd110-non-free`](#neurodebiannd110-non-free)
-	[`neurodebian:nd16.04`](#neurodebiannd1604)
-	[`neurodebian:nd16.04-non-free`](#neurodebiannd1604-non-free)
-	[`neurodebian:nd18.04`](#neurodebiannd1804)
-	[`neurodebian:nd18.04-non-free`](#neurodebiannd1804-non-free)
-	[`neurodebian:nd20.04`](#neurodebiannd2004)
-	[`neurodebian:nd20.04-non-free`](#neurodebiannd2004-non-free)
-	[`neurodebian:nd21.04`](#neurodebiannd2104)
-	[`neurodebian:nd21.04-non-free`](#neurodebiannd2104-non-free)
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
$ docker pull neurodebian@sha256:40592492b9cae174140033219405eccf96213f0a66ea8747b12a463622edc8dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:bionic` - linux; amd64

```console
$ docker pull neurodebian@sha256:451d9dafb1761cdf796aaa3f9bd0d6d18783769193b9c3b762e794486c4d07ce
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31765376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714338cfdd48d5d70e55de7cd452321932c3a1cbf7ed5b9dfa712720c07eb328`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:30 GMT
ADD file:e729fb032bd2f7cde20fb343da0cd358447e8b23028422c123944e8d0be660fa in / 
# Mon, 26 Jul 2021 21:21:31 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:13:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:13:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 27 Jul 2021 00:13:32 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 27 Jul 2021 00:13:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:feac5306138255e28a9862d3f3d29025d0a4d0648855afe1acd6131af07138ac`  
		Last Modified: Mon, 26 Jul 2021 21:22:52 GMT  
		Size: 26.7 MB (26709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e938ab6c3a5cf1c29298043d3d5c68195eec69585541aa9a6bb749be67881c51`  
		Last Modified: Tue, 27 Jul 2021 00:17:12 GMT  
		Size: 4.8 MB (4813118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7870bda0883ce8d4f86ede7a7881a3366d112673fe11cc38223ef4510228bf53`  
		Last Modified: Tue, 27 Jul 2021 00:17:11 GMT  
		Size: 3.2 KB (3154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9662eb146b3a44cd5c3251fd7622e852c35e6c4b810c3685b04f29d89a9bd731`  
		Last Modified: Tue, 27 Jul 2021 00:17:11 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2653b42c5af817f901660031c386465e53297b18053e5d8a6a62280b13a4f5d2`  
		Last Modified: Tue, 27 Jul 2021 00:17:11 GMT  
		Size: 239.8 KB (239821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bionic-non-free`

```console
$ docker pull neurodebian@sha256:799ea3936e5f9184b1d8828590ac89c4dbdbe23719d234046e9f69b30415877d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:bionic-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:293f8209bf213ba2b9ce8fd4c487adad9b6af8c0a26b1dc871f766d08d029fed
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31765632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa69c51ac01c99497165137e1317c5447591d002600924d32828605f04224f44`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:30 GMT
ADD file:e729fb032bd2f7cde20fb343da0cd358447e8b23028422c123944e8d0be660fa in / 
# Mon, 26 Jul 2021 21:21:31 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:13:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:13:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 27 Jul 2021 00:13:32 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 27 Jul 2021 00:13:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:13:43 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:feac5306138255e28a9862d3f3d29025d0a4d0648855afe1acd6131af07138ac`  
		Last Modified: Mon, 26 Jul 2021 21:22:52 GMT  
		Size: 26.7 MB (26709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e938ab6c3a5cf1c29298043d3d5c68195eec69585541aa9a6bb749be67881c51`  
		Last Modified: Tue, 27 Jul 2021 00:17:12 GMT  
		Size: 4.8 MB (4813118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7870bda0883ce8d4f86ede7a7881a3366d112673fe11cc38223ef4510228bf53`  
		Last Modified: Tue, 27 Jul 2021 00:17:11 GMT  
		Size: 3.2 KB (3154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9662eb146b3a44cd5c3251fd7622e852c35e6c4b810c3685b04f29d89a9bd731`  
		Last Modified: Tue, 27 Jul 2021 00:17:11 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2653b42c5af817f901660031c386465e53297b18053e5d8a6a62280b13a4f5d2`  
		Last Modified: Tue, 27 Jul 2021 00:17:11 GMT  
		Size: 239.8 KB (239821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0e41b964cb330ae3f324759621ac01ea88e9e576bad4e242ad8d109a91ff71`  
		Last Modified: Tue, 27 Jul 2021 00:17:24 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:b7db7f885625f2280e7e18dfc30f6b58a72b0d8c78ffff453e62959a2bb9dfbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:dca66f4d80bcf66851ec3bd735051b1eb5bccdb84b47f7af1143704cfb7de550
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66537692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae37d11fe00597c1adf723dc0c1cb0205aa7c3918365e2537f1cfc8bdd1b88d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:26 GMT
ADD file:a528c112b566e7f129178dadedfa421b0c5b870997c4628327967850e54b915c in / 
# Tue, 17 Aug 2021 01:23:26 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:42:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:42:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 17 Aug 2021 11:42:19 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 17 Aug 2021 11:42:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4c25b3090c2685271afcffc2a4db73f15ab11a0124bfcde6085c934a4e6f4a51`  
		Last Modified: Tue, 17 Aug 2021 01:29:06 GMT  
		Size: 54.9 MB (54915004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7980c5f3aa1b56b00a43522300773b7b46a2893e5ef57cf76a2f95c78169172b`  
		Last Modified: Tue, 17 Aug 2021 11:44:34 GMT  
		Size: 11.3 MB (11309469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c33da905ad58fa70e2dcc7f460afaf846405f6c2d9ee4627ac4289b9173569`  
		Last Modified: Tue, 17 Aug 2021 11:44:33 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7649419684ebbeb22f83ef1d9d3d09879e0fbbce13e9c5c7c2227b02b2e1c4`  
		Last Modified: Tue, 17 Aug 2021 11:44:32 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13d735f3c9625d83e34655ad9d3908af64dcb9467c99804b73e390b190624fb`  
		Last Modified: Tue, 17 Aug 2021 11:44:33 GMT  
		Size: 311.2 KB (311203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:f37abdaf5a71138ff6b5e522cbc8e3d44c7ea9e491660f7fa782191f1b907a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:5e2b0a80760bc955ad06fd67b984170e99fe0fbd73091329293fd17b267b4c39
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66538058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6013efa885925229f770e7b1a7ee691323ee2450d8b34379a477160fd20e9e2c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:26 GMT
ADD file:a528c112b566e7f129178dadedfa421b0c5b870997c4628327967850e54b915c in / 
# Tue, 17 Aug 2021 01:23:26 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:42:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:42:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 17 Aug 2021 11:42:19 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 17 Aug 2021 11:42:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:42:33 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:4c25b3090c2685271afcffc2a4db73f15ab11a0124bfcde6085c934a4e6f4a51`  
		Last Modified: Tue, 17 Aug 2021 01:29:06 GMT  
		Size: 54.9 MB (54915004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7980c5f3aa1b56b00a43522300773b7b46a2893e5ef57cf76a2f95c78169172b`  
		Last Modified: Tue, 17 Aug 2021 11:44:34 GMT  
		Size: 11.3 MB (11309469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c33da905ad58fa70e2dcc7f460afaf846405f6c2d9ee4627ac4289b9173569`  
		Last Modified: Tue, 17 Aug 2021 11:44:33 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7649419684ebbeb22f83ef1d9d3d09879e0fbbce13e9c5c7c2227b02b2e1c4`  
		Last Modified: Tue, 17 Aug 2021 11:44:32 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13d735f3c9625d83e34655ad9d3908af64dcb9467c99804b73e390b190624fb`  
		Last Modified: Tue, 17 Aug 2021 11:44:33 GMT  
		Size: 311.2 KB (311203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc7e4c6ee174344223cdf91d4360d44f13994916c77d9a96d19756a9098e670`  
		Last Modified: Tue, 17 Aug 2021 11:44:44 GMT  
		Size: 366.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:buster`

```console
$ docker pull neurodebian@sha256:a144b854a1621f41890fb850fcb3ecab3378cc45162f4a936acba101147d0b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:buster` - linux; amd64

```console
$ docker pull neurodebian@sha256:08dd24a69418fbc228741fd08c46107ba30c6ad2d3d62de9ccdea2b8f75482b7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61241052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae7a7397e2890ec4e92b72a56c6030c96679ad523ff0ccc278aad0e307392ef7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:41:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:41:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 17 Aug 2021 11:41:45 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 17 Aug 2021 11:41:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec371be32636521f27bad15f42934bb1189f1f408cbe19471ac6372862924d1`  
		Last Modified: Tue, 17 Aug 2021 11:44:09 GMT  
		Size: 10.5 MB (10500040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99d5763b996b375cdcf31e9831e332f51a3298c56790cb567a11070da5da5a0`  
		Last Modified: Tue, 17 Aug 2021 11:44:07 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308144ecaf23b11e838899244248ce7bc70d6912ad831de7fada3630f0c0b59`  
		Last Modified: Tue, 17 Aug 2021 11:44:07 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2078e085ecc552d76ef0a184b32d682163684a6eaa033ddf9202290bda3c8ea`  
		Last Modified: Tue, 17 Aug 2021 11:44:07 GMT  
		Size: 302.8 KB (302799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:buster-non-free`

```console
$ docker pull neurodebian@sha256:46d4ff0665db7f115a9f18d83aed21a69fbab671f290ae95b4f4e4132518842c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:buster-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:bef51b302becfa096c68984712136aa1f61a955b7ee09a62e025348daa7c6d47
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61241418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6a8a1942392fd5336fbbf0d6ce711a2cbcf599ed6b397b0e79c0714408d7878`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:41:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:41:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 17 Aug 2021 11:41:45 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 17 Aug 2021 11:41:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:41:58 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec371be32636521f27bad15f42934bb1189f1f408cbe19471ac6372862924d1`  
		Last Modified: Tue, 17 Aug 2021 11:44:09 GMT  
		Size: 10.5 MB (10500040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99d5763b996b375cdcf31e9831e332f51a3298c56790cb567a11070da5da5a0`  
		Last Modified: Tue, 17 Aug 2021 11:44:07 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308144ecaf23b11e838899244248ce7bc70d6912ad831de7fada3630f0c0b59`  
		Last Modified: Tue, 17 Aug 2021 11:44:07 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2078e085ecc552d76ef0a184b32d682163684a6eaa033ddf9202290bda3c8ea`  
		Last Modified: Tue, 17 Aug 2021 11:44:07 GMT  
		Size: 302.8 KB (302799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1746f0cf4c2f09051bcb143c8041cfc5033c4d13c9b22a573e8a729923cdf6a0`  
		Last Modified: Tue, 17 Aug 2021 11:44:20 GMT  
		Size: 366.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:focal`

```console
$ docker pull neurodebian@sha256:dfe56cdfbaba469a68a34265558fe3653d29ce4bf4f8873582b2284631cb9401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:d4c6391daea504d855fe42504ebfc6d07f1653badc4724040f50a8b75744d114
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34296820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f97ff2718a58ec8de130e3d73fba84de56aa226494ae818cf58063dd9e33b5a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:13:54 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:13:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 27 Jul 2021 00:13:56 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 27 Jul 2021 00:14:00 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870d1e2acc9261e5c3a40b500f5959e6394d09583b3467f279e6b40fa9ed0faa`  
		Last Modified: Tue, 27 Jul 2021 00:17:36 GMT  
		Size: 5.5 MB (5488799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f682b7475d2896a202cbcefb58ae71d2bf958761ac8068be9ae2f58c0a012bb6`  
		Last Modified: Tue, 27 Jul 2021 00:17:34 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5c473424a3f78f98ed3c2f554c0d343e02cb12efc7f6d2e1b591f43756d58f`  
		Last Modified: Tue, 27 Jul 2021 00:17:34 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8f546e25b59926a75cc53a386fc97e72f3893848614566fda6e2fa026b7dd1`  
		Last Modified: Tue, 27 Jul 2021 00:17:34 GMT  
		Size: 238.1 KB (238065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:focal-non-free`

```console
$ docker pull neurodebian@sha256:51e50f2fef713c938fd8f0e9b621f18446b5ee9fb9d2d6140a61a8d6f2054e07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:focal-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:08c3a5fbff55830503f374ff412b3aecba1f0d3923b11cbd00c6d307885ac878
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34297075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9818eb64c7a6c42e291d4257c8c876f5ec06c640580ae2167c2696a0f268a1e0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:13:54 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:13:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 27 Jul 2021 00:13:56 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 27 Jul 2021 00:14:00 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:14:05 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870d1e2acc9261e5c3a40b500f5959e6394d09583b3467f279e6b40fa9ed0faa`  
		Last Modified: Tue, 27 Jul 2021 00:17:36 GMT  
		Size: 5.5 MB (5488799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f682b7475d2896a202cbcefb58ae71d2bf958761ac8068be9ae2f58c0a012bb6`  
		Last Modified: Tue, 27 Jul 2021 00:17:34 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5c473424a3f78f98ed3c2f554c0d343e02cb12efc7f6d2e1b591f43756d58f`  
		Last Modified: Tue, 27 Jul 2021 00:17:34 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8f546e25b59926a75cc53a386fc97e72f3893848614566fda6e2fa026b7dd1`  
		Last Modified: Tue, 27 Jul 2021 00:17:34 GMT  
		Size: 238.1 KB (238065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5b9bcdfe52b5bc32583670eccca7273dc04e6ed5fe25571d3d3843785ce7e2`  
		Last Modified: Tue, 27 Jul 2021 00:17:46 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:hirsute`

```console
$ docker pull neurodebian@sha256:7385a5023129b01a4b02ed9229e193d33810441449993c9f0f82d258cd47143b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:hirsute` - linux; amd64

```console
$ docker pull neurodebian@sha256:bff1efcd9743c627506e21e0d1dc5f455ff4963b1c5168a812ec623c3cb9d3dd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37686774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c59636c0452ae01455d116c48f4ac2ebfc4e6058b46a920090363ca3d157695f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:54 GMT
ADD file:6ae44786caae9af1c6b70dc9cc244e7d4e06fffc0696f68877527d69aa3fc735 in / 
# Mon, 26 Jul 2021 21:21:54 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:15:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:15:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 27 Jul 2021 00:15:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian hirsute main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel hirsute main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 27 Jul 2021 00:15:38 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4451f5c7eb7af74432585f5ebfbeb01bbfc87ec4a74dc93703bdd89330559cd1`  
		Last Modified: Mon, 26 Jul 2021 21:23:44 GMT  
		Size: 31.8 MB (31837572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d56df5ecf752059653014e714bae6507778c2fd9f6c3f864fdeb0f11be5318b`  
		Last Modified: Tue, 27 Jul 2021 00:18:24 GMT  
		Size: 5.6 MB (5597737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e7d996b67eeee2532d9643e28004d43fba9c80c19ac98f2b5378cc7fd200041`  
		Last Modified: Tue, 27 Jul 2021 00:18:23 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35723c871426551f5e5c91aa3caf285e3fbdd3819e9baba7432cc48fa90afc25`  
		Last Modified: Tue, 27 Jul 2021 00:18:23 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df43dcede292226ffbef4971d7b79425f61a336e7bf892f24f89f0cde937e57`  
		Last Modified: Tue, 27 Jul 2021 00:18:23 GMT  
		Size: 249.5 KB (249455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:hirsute-non-free`

```console
$ docker pull neurodebian@sha256:dc1891c2764c95560eb7a56f32d5422ce7067031afe7915a82db5233d60bfe40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:hirsute-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:a255713afcc6cc708ac499c0b89e5bd2d9623c2d5f38b83c8964a323ea4b0030
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37687033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9445c97ade590117897e42cddf4822b60f20bd87239e97e4bbd859e27dc8608e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:54 GMT
ADD file:6ae44786caae9af1c6b70dc9cc244e7d4e06fffc0696f68877527d69aa3fc735 in / 
# Mon, 26 Jul 2021 21:21:54 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:15:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:15:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 27 Jul 2021 00:15:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian hirsute main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel hirsute main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 27 Jul 2021 00:15:38 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:15:45 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:4451f5c7eb7af74432585f5ebfbeb01bbfc87ec4a74dc93703bdd89330559cd1`  
		Last Modified: Mon, 26 Jul 2021 21:23:44 GMT  
		Size: 31.8 MB (31837572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d56df5ecf752059653014e714bae6507778c2fd9f6c3f864fdeb0f11be5318b`  
		Last Modified: Tue, 27 Jul 2021 00:18:24 GMT  
		Size: 5.6 MB (5597737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e7d996b67eeee2532d9643e28004d43fba9c80c19ac98f2b5378cc7fd200041`  
		Last Modified: Tue, 27 Jul 2021 00:18:23 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35723c871426551f5e5c91aa3caf285e3fbdd3819e9baba7432cc48fa90afc25`  
		Last Modified: Tue, 27 Jul 2021 00:18:23 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df43dcede292226ffbef4971d7b79425f61a336e7bf892f24f89f0cde937e57`  
		Last Modified: Tue, 27 Jul 2021 00:18:23 GMT  
		Size: 249.5 KB (249455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dafb5cb912e6be0079cd434fc4fb0c83d60571d2b29cca69b8bb32cfb2babb3`  
		Last Modified: Tue, 27 Jul 2021 00:18:34 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:a144b854a1621f41890fb850fcb3ecab3378cc45162f4a936acba101147d0b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:latest` - linux; amd64

```console
$ docker pull neurodebian@sha256:08dd24a69418fbc228741fd08c46107ba30c6ad2d3d62de9ccdea2b8f75482b7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61241052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae7a7397e2890ec4e92b72a56c6030c96679ad523ff0ccc278aad0e307392ef7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:41:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:41:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 17 Aug 2021 11:41:45 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 17 Aug 2021 11:41:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec371be32636521f27bad15f42934bb1189f1f408cbe19471ac6372862924d1`  
		Last Modified: Tue, 17 Aug 2021 11:44:09 GMT  
		Size: 10.5 MB (10500040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99d5763b996b375cdcf31e9831e332f51a3298c56790cb567a11070da5da5a0`  
		Last Modified: Tue, 17 Aug 2021 11:44:07 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308144ecaf23b11e838899244248ce7bc70d6912ad831de7fada3630f0c0b59`  
		Last Modified: Tue, 17 Aug 2021 11:44:07 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2078e085ecc552d76ef0a184b32d682163684a6eaa033ddf9202290bda3c8ea`  
		Last Modified: Tue, 17 Aug 2021 11:44:07 GMT  
		Size: 302.8 KB (302799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:eb53c2b1b9269695e52d90c075a9eccfde83bb8aa2f73713f0f85c38aabd9c51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd` - linux; amd64

```console
$ docker pull neurodebian@sha256:2a62e113e5893316ef7f83654b81fc95b5a5848d0fc54dcc139e514699732c9f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.6 MB (66553807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f54735921ebcd8fe81d80a77df0b70e093d11d8961d87c18b90972ee1eca273`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:25:06 GMT
ADD file:3052ec53a19fa26baad5d50e4d2867be2cc386ae62195d8dbb9d90d0b904c464 in / 
# Tue, 17 Aug 2021 01:25:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:42:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:42:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 17 Aug 2021 11:42:46 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 17 Aug 2021 11:42:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a6952a6bd46e0eaa2c0e7e851a45f288b3dc080472a9249e48c74b3fb7551fcc`  
		Last Modified: Tue, 17 Aug 2021 01:31:55 GMT  
		Size: 54.9 MB (54930846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410ec36aee1a8f201f9c0031cd0f05202d26dd1d1436a96bf9c25d7e16cd6409`  
		Last Modified: Tue, 17 Aug 2021 11:44:56 GMT  
		Size: 11.3 MB (11309853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511f77571d0ebc200d836bb589cbdbc218a43528b6107216fb05ac08b051e861`  
		Last Modified: Tue, 17 Aug 2021 11:44:55 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb24c8352006baecfb22a1adb719cc0dd9979fc96bd6e659b84d5e08367516a4`  
		Last Modified: Tue, 17 Aug 2021 11:44:57 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3017795095606b9588affb41bc71fcda9f48a651b50d1e21b632ed47564d944c`  
		Last Modified: Tue, 17 Aug 2021 11:44:55 GMT  
		Size: 311.1 KB (311099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:80a7a7c1946118af7d7021ff098f4b1181c437cf6078393ef71116bb7b4a1353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:7e888b386ccd79eed3cc5c45d9c4e74665cbcd61c69317984194ea9b143c2686
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.6 MB (66554123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44cc3785a6cdb16a17d84956f49da466b06e6a126197a0a9ae26eb68582e92ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:25:06 GMT
ADD file:3052ec53a19fa26baad5d50e4d2867be2cc386ae62195d8dbb9d90d0b904c464 in / 
# Tue, 17 Aug 2021 01:25:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:42:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:42:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 17 Aug 2021 11:42:46 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 17 Aug 2021 11:42:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:42:56 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:a6952a6bd46e0eaa2c0e7e851a45f288b3dc080472a9249e48c74b3fb7551fcc`  
		Last Modified: Tue, 17 Aug 2021 01:31:55 GMT  
		Size: 54.9 MB (54930846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410ec36aee1a8f201f9c0031cd0f05202d26dd1d1436a96bf9c25d7e16cd6409`  
		Last Modified: Tue, 17 Aug 2021 11:44:56 GMT  
		Size: 11.3 MB (11309853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511f77571d0ebc200d836bb589cbdbc218a43528b6107216fb05ac08b051e861`  
		Last Modified: Tue, 17 Aug 2021 11:44:55 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb24c8352006baecfb22a1adb719cc0dd9979fc96bd6e659b84d5e08367516a4`  
		Last Modified: Tue, 17 Aug 2021 11:44:57 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3017795095606b9588affb41bc71fcda9f48a651b50d1e21b632ed47564d944c`  
		Last Modified: Tue, 17 Aug 2021 11:44:55 GMT  
		Size: 311.1 KB (311099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1f96b4ea8e389a530c0f176604c77f640d48f27ed379dd42b0624d42999787`  
		Last Modified: Tue, 17 Aug 2021 11:45:08 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd100`

```console
$ docker pull neurodebian@sha256:a144b854a1621f41890fb850fcb3ecab3378cc45162f4a936acba101147d0b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd100` - linux; amd64

```console
$ docker pull neurodebian@sha256:08dd24a69418fbc228741fd08c46107ba30c6ad2d3d62de9ccdea2b8f75482b7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61241052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae7a7397e2890ec4e92b72a56c6030c96679ad523ff0ccc278aad0e307392ef7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:41:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:41:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 17 Aug 2021 11:41:45 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 17 Aug 2021 11:41:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec371be32636521f27bad15f42934bb1189f1f408cbe19471ac6372862924d1`  
		Last Modified: Tue, 17 Aug 2021 11:44:09 GMT  
		Size: 10.5 MB (10500040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99d5763b996b375cdcf31e9831e332f51a3298c56790cb567a11070da5da5a0`  
		Last Modified: Tue, 17 Aug 2021 11:44:07 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308144ecaf23b11e838899244248ce7bc70d6912ad831de7fada3630f0c0b59`  
		Last Modified: Tue, 17 Aug 2021 11:44:07 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2078e085ecc552d76ef0a184b32d682163684a6eaa033ddf9202290bda3c8ea`  
		Last Modified: Tue, 17 Aug 2021 11:44:07 GMT  
		Size: 302.8 KB (302799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd100-non-free`

```console
$ docker pull neurodebian@sha256:46d4ff0665db7f115a9f18d83aed21a69fbab671f290ae95b4f4e4132518842c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd100-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:bef51b302becfa096c68984712136aa1f61a955b7ee09a62e025348daa7c6d47
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61241418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6a8a1942392fd5336fbbf0d6ce711a2cbcf599ed6b397b0e79c0714408d7878`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:41:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:41:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 17 Aug 2021 11:41:45 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 17 Aug 2021 11:41:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:41:58 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec371be32636521f27bad15f42934bb1189f1f408cbe19471ac6372862924d1`  
		Last Modified: Tue, 17 Aug 2021 11:44:09 GMT  
		Size: 10.5 MB (10500040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99d5763b996b375cdcf31e9831e332f51a3298c56790cb567a11070da5da5a0`  
		Last Modified: Tue, 17 Aug 2021 11:44:07 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308144ecaf23b11e838899244248ce7bc70d6912ad831de7fada3630f0c0b59`  
		Last Modified: Tue, 17 Aug 2021 11:44:07 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2078e085ecc552d76ef0a184b32d682163684a6eaa033ddf9202290bda3c8ea`  
		Last Modified: Tue, 17 Aug 2021 11:44:07 GMT  
		Size: 302.8 KB (302799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1746f0cf4c2f09051bcb143c8041cfc5033c4d13c9b22a573e8a729923cdf6a0`  
		Last Modified: Tue, 17 Aug 2021 11:44:20 GMT  
		Size: 366.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:b7db7f885625f2280e7e18dfc30f6b58a72b0d8c78ffff453e62959a2bb9dfbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd110` - linux; amd64

```console
$ docker pull neurodebian@sha256:dca66f4d80bcf66851ec3bd735051b1eb5bccdb84b47f7af1143704cfb7de550
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66537692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae37d11fe00597c1adf723dc0c1cb0205aa7c3918365e2537f1cfc8bdd1b88d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:26 GMT
ADD file:a528c112b566e7f129178dadedfa421b0c5b870997c4628327967850e54b915c in / 
# Tue, 17 Aug 2021 01:23:26 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:42:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:42:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 17 Aug 2021 11:42:19 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 17 Aug 2021 11:42:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4c25b3090c2685271afcffc2a4db73f15ab11a0124bfcde6085c934a4e6f4a51`  
		Last Modified: Tue, 17 Aug 2021 01:29:06 GMT  
		Size: 54.9 MB (54915004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7980c5f3aa1b56b00a43522300773b7b46a2893e5ef57cf76a2f95c78169172b`  
		Last Modified: Tue, 17 Aug 2021 11:44:34 GMT  
		Size: 11.3 MB (11309469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c33da905ad58fa70e2dcc7f460afaf846405f6c2d9ee4627ac4289b9173569`  
		Last Modified: Tue, 17 Aug 2021 11:44:33 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7649419684ebbeb22f83ef1d9d3d09879e0fbbce13e9c5c7c2227b02b2e1c4`  
		Last Modified: Tue, 17 Aug 2021 11:44:32 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13d735f3c9625d83e34655ad9d3908af64dcb9467c99804b73e390b190624fb`  
		Last Modified: Tue, 17 Aug 2021 11:44:33 GMT  
		Size: 311.2 KB (311203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:f37abdaf5a71138ff6b5e522cbc8e3d44c7ea9e491660f7fa782191f1b907a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:5e2b0a80760bc955ad06fd67b984170e99fe0fbd73091329293fd17b267b4c39
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66538058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6013efa885925229f770e7b1a7ee691323ee2450d8b34379a477160fd20e9e2c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:26 GMT
ADD file:a528c112b566e7f129178dadedfa421b0c5b870997c4628327967850e54b915c in / 
# Tue, 17 Aug 2021 01:23:26 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:42:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:42:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 17 Aug 2021 11:42:19 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 17 Aug 2021 11:42:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:42:33 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:4c25b3090c2685271afcffc2a4db73f15ab11a0124bfcde6085c934a4e6f4a51`  
		Last Modified: Tue, 17 Aug 2021 01:29:06 GMT  
		Size: 54.9 MB (54915004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7980c5f3aa1b56b00a43522300773b7b46a2893e5ef57cf76a2f95c78169172b`  
		Last Modified: Tue, 17 Aug 2021 11:44:34 GMT  
		Size: 11.3 MB (11309469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c33da905ad58fa70e2dcc7f460afaf846405f6c2d9ee4627ac4289b9173569`  
		Last Modified: Tue, 17 Aug 2021 11:44:33 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7649419684ebbeb22f83ef1d9d3d09879e0fbbce13e9c5c7c2227b02b2e1c4`  
		Last Modified: Tue, 17 Aug 2021 11:44:32 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13d735f3c9625d83e34655ad9d3908af64dcb9467c99804b73e390b190624fb`  
		Last Modified: Tue, 17 Aug 2021 11:44:33 GMT  
		Size: 311.2 KB (311203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc7e4c6ee174344223cdf91d4360d44f13994916c77d9a96d19756a9098e670`  
		Last Modified: Tue, 17 Aug 2021 11:44:44 GMT  
		Size: 366.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd16.04`

```console
$ docker pull neurodebian@sha256:43b573d833942d586f9a7d4a1c3f1ca209077a20b2a90c26cb02b0fa61b03156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd16.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:3160d9542153b47caf8d069cbc0db22d1638ad4adbd353f1259c21355f99b6ea
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46729660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f1bda86cb8ade0c529bcb17fda696383d42d0188167b4119599fb18acdbab3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:22:15 GMT
ADD file:a94a87e268e99c78143fae5148bd1200bf0da90c0e7f42bd8c168bb205ccb105 in / 
# Mon, 26 Jul 2021 21:22:16 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 26 Jul 2021 21:22:17 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 21:22:17 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 26 Jul 2021 21:22:18 GMT
CMD ["/bin/bash"]
# Tue, 27 Jul 2021 00:13:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:13:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 27 Jul 2021 00:13:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian xenial main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel xenial main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 27 Jul 2021 00:13:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:52818491084148fa3469964bbcc3576686018a3b16b2e29be0407565c4c80b44`  
		Last Modified: Thu, 22 Jul 2021 16:25:00 GMT  
		Size: 46.5 MB (46497362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9df81d603d28f2a294b2f11b4f60d07b5b833b2ad7d6659a3f59b10cff2696`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636d9303bf663657be8e6796d720913bb985b5343da7949749ae1e72b54a88d8`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672b5bdcef61237567b311ad3d349f5eae18ba839ce2b204858a3083437a0a59`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e7416d41f03136eeac7efb16c3fd8a6589880fff5bda819b3a1e6066c41fef7`  
		Last Modified: Tue, 27 Jul 2021 00:16:47 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bd79c96d093dd72ba4bbd9c6352b1fb0f299189cdc0d6388c894f24eec8714`  
		Last Modified: Tue, 27 Jul 2021 00:16:48 GMT  
		Size: 3.2 KB (3155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb360a6236175933715f7da41d199cb387954378bed350ccbcccc94565dfefe`  
		Last Modified: Tue, 27 Jul 2021 00:16:47 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0bfb7b9c9a2ce4ec8233a80b6131f224640f54ca2b6af5dcde3f11b71f315d4`  
		Last Modified: Tue, 27 Jul 2021 00:16:47 GMT  
		Size: 227.2 KB (227170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd16.04-non-free`

```console
$ docker pull neurodebian@sha256:822e4ac31d3f0aadb858981a3ee4ece7f5d77edb5fb8f6b81efb166e3be2699a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd16.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:62ea27a9925c741937b8763cdb75ecd8c3dfbca34503701c7eb16b37f277c439
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46729916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21bb46914f12361be318974e8b6196f2a48122d7c2eaa4d987cd4c9f60d09626`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:22:15 GMT
ADD file:a94a87e268e99c78143fae5148bd1200bf0da90c0e7f42bd8c168bb205ccb105 in / 
# Mon, 26 Jul 2021 21:22:16 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 26 Jul 2021 21:22:17 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 21:22:17 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 26 Jul 2021 21:22:18 GMT
CMD ["/bin/bash"]
# Tue, 27 Jul 2021 00:13:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:13:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 27 Jul 2021 00:13:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian xenial main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel xenial main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 27 Jul 2021 00:13:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:13:19 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:52818491084148fa3469964bbcc3576686018a3b16b2e29be0407565c4c80b44`  
		Last Modified: Thu, 22 Jul 2021 16:25:00 GMT  
		Size: 46.5 MB (46497362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9df81d603d28f2a294b2f11b4f60d07b5b833b2ad7d6659a3f59b10cff2696`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636d9303bf663657be8e6796d720913bb985b5343da7949749ae1e72b54a88d8`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672b5bdcef61237567b311ad3d349f5eae18ba839ce2b204858a3083437a0a59`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e7416d41f03136eeac7efb16c3fd8a6589880fff5bda819b3a1e6066c41fef7`  
		Last Modified: Tue, 27 Jul 2021 00:16:47 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bd79c96d093dd72ba4bbd9c6352b1fb0f299189cdc0d6388c894f24eec8714`  
		Last Modified: Tue, 27 Jul 2021 00:16:48 GMT  
		Size: 3.2 KB (3155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb360a6236175933715f7da41d199cb387954378bed350ccbcccc94565dfefe`  
		Last Modified: Tue, 27 Jul 2021 00:16:47 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0bfb7b9c9a2ce4ec8233a80b6131f224640f54ca2b6af5dcde3f11b71f315d4`  
		Last Modified: Tue, 27 Jul 2021 00:16:47 GMT  
		Size: 227.2 KB (227170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787a536fe6fc734fba11687bdfb5bf9d581534aadb3907eb628b70239dff16e4`  
		Last Modified: Tue, 27 Jul 2021 00:17:00 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd18.04`

```console
$ docker pull neurodebian@sha256:40592492b9cae174140033219405eccf96213f0a66ea8747b12a463622edc8dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd18.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:451d9dafb1761cdf796aaa3f9bd0d6d18783769193b9c3b762e794486c4d07ce
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31765376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714338cfdd48d5d70e55de7cd452321932c3a1cbf7ed5b9dfa712720c07eb328`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:30 GMT
ADD file:e729fb032bd2f7cde20fb343da0cd358447e8b23028422c123944e8d0be660fa in / 
# Mon, 26 Jul 2021 21:21:31 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:13:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:13:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 27 Jul 2021 00:13:32 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 27 Jul 2021 00:13:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:feac5306138255e28a9862d3f3d29025d0a4d0648855afe1acd6131af07138ac`  
		Last Modified: Mon, 26 Jul 2021 21:22:52 GMT  
		Size: 26.7 MB (26709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e938ab6c3a5cf1c29298043d3d5c68195eec69585541aa9a6bb749be67881c51`  
		Last Modified: Tue, 27 Jul 2021 00:17:12 GMT  
		Size: 4.8 MB (4813118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7870bda0883ce8d4f86ede7a7881a3366d112673fe11cc38223ef4510228bf53`  
		Last Modified: Tue, 27 Jul 2021 00:17:11 GMT  
		Size: 3.2 KB (3154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9662eb146b3a44cd5c3251fd7622e852c35e6c4b810c3685b04f29d89a9bd731`  
		Last Modified: Tue, 27 Jul 2021 00:17:11 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2653b42c5af817f901660031c386465e53297b18053e5d8a6a62280b13a4f5d2`  
		Last Modified: Tue, 27 Jul 2021 00:17:11 GMT  
		Size: 239.8 KB (239821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd18.04-non-free`

```console
$ docker pull neurodebian@sha256:799ea3936e5f9184b1d8828590ac89c4dbdbe23719d234046e9f69b30415877d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd18.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:293f8209bf213ba2b9ce8fd4c487adad9b6af8c0a26b1dc871f766d08d029fed
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31765632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa69c51ac01c99497165137e1317c5447591d002600924d32828605f04224f44`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:30 GMT
ADD file:e729fb032bd2f7cde20fb343da0cd358447e8b23028422c123944e8d0be660fa in / 
# Mon, 26 Jul 2021 21:21:31 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:13:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:13:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 27 Jul 2021 00:13:32 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bionic main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bionic main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 27 Jul 2021 00:13:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:13:43 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:feac5306138255e28a9862d3f3d29025d0a4d0648855afe1acd6131af07138ac`  
		Last Modified: Mon, 26 Jul 2021 21:22:52 GMT  
		Size: 26.7 MB (26709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e938ab6c3a5cf1c29298043d3d5c68195eec69585541aa9a6bb749be67881c51`  
		Last Modified: Tue, 27 Jul 2021 00:17:12 GMT  
		Size: 4.8 MB (4813118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7870bda0883ce8d4f86ede7a7881a3366d112673fe11cc38223ef4510228bf53`  
		Last Modified: Tue, 27 Jul 2021 00:17:11 GMT  
		Size: 3.2 KB (3154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9662eb146b3a44cd5c3251fd7622e852c35e6c4b810c3685b04f29d89a9bd731`  
		Last Modified: Tue, 27 Jul 2021 00:17:11 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2653b42c5af817f901660031c386465e53297b18053e5d8a6a62280b13a4f5d2`  
		Last Modified: Tue, 27 Jul 2021 00:17:11 GMT  
		Size: 239.8 KB (239821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0e41b964cb330ae3f324759621ac01ea88e9e576bad4e242ad8d109a91ff71`  
		Last Modified: Tue, 27 Jul 2021 00:17:24 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd20.04`

```console
$ docker pull neurodebian@sha256:dfe56cdfbaba469a68a34265558fe3653d29ce4bf4f8873582b2284631cb9401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd20.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:d4c6391daea504d855fe42504ebfc6d07f1653badc4724040f50a8b75744d114
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34296820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f97ff2718a58ec8de130e3d73fba84de56aa226494ae818cf58063dd9e33b5a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:13:54 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:13:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 27 Jul 2021 00:13:56 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 27 Jul 2021 00:14:00 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870d1e2acc9261e5c3a40b500f5959e6394d09583b3467f279e6b40fa9ed0faa`  
		Last Modified: Tue, 27 Jul 2021 00:17:36 GMT  
		Size: 5.5 MB (5488799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f682b7475d2896a202cbcefb58ae71d2bf958761ac8068be9ae2f58c0a012bb6`  
		Last Modified: Tue, 27 Jul 2021 00:17:34 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5c473424a3f78f98ed3c2f554c0d343e02cb12efc7f6d2e1b591f43756d58f`  
		Last Modified: Tue, 27 Jul 2021 00:17:34 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8f546e25b59926a75cc53a386fc97e72f3893848614566fda6e2fa026b7dd1`  
		Last Modified: Tue, 27 Jul 2021 00:17:34 GMT  
		Size: 238.1 KB (238065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd20.04-non-free`

```console
$ docker pull neurodebian@sha256:51e50f2fef713c938fd8f0e9b621f18446b5ee9fb9d2d6140a61a8d6f2054e07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd20.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:08c3a5fbff55830503f374ff412b3aecba1f0d3923b11cbd00c6d307885ac878
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34297075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9818eb64c7a6c42e291d4257c8c876f5ec06c640580ae2167c2696a0f268a1e0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:13:54 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:13:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 27 Jul 2021 00:13:56 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 27 Jul 2021 00:14:00 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:14:05 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870d1e2acc9261e5c3a40b500f5959e6394d09583b3467f279e6b40fa9ed0faa`  
		Last Modified: Tue, 27 Jul 2021 00:17:36 GMT  
		Size: 5.5 MB (5488799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f682b7475d2896a202cbcefb58ae71d2bf958761ac8068be9ae2f58c0a012bb6`  
		Last Modified: Tue, 27 Jul 2021 00:17:34 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5c473424a3f78f98ed3c2f554c0d343e02cb12efc7f6d2e1b591f43756d58f`  
		Last Modified: Tue, 27 Jul 2021 00:17:34 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8f546e25b59926a75cc53a386fc97e72f3893848614566fda6e2fa026b7dd1`  
		Last Modified: Tue, 27 Jul 2021 00:17:34 GMT  
		Size: 238.1 KB (238065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5b9bcdfe52b5bc32583670eccca7273dc04e6ed5fe25571d3d3843785ce7e2`  
		Last Modified: Tue, 27 Jul 2021 00:17:46 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd21.04`

```console
$ docker pull neurodebian@sha256:7385a5023129b01a4b02ed9229e193d33810441449993c9f0f82d258cd47143b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd21.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:bff1efcd9743c627506e21e0d1dc5f455ff4963b1c5168a812ec623c3cb9d3dd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37686774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c59636c0452ae01455d116c48f4ac2ebfc4e6058b46a920090363ca3d157695f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:54 GMT
ADD file:6ae44786caae9af1c6b70dc9cc244e7d4e06fffc0696f68877527d69aa3fc735 in / 
# Mon, 26 Jul 2021 21:21:54 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:15:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:15:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 27 Jul 2021 00:15:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian hirsute main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel hirsute main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 27 Jul 2021 00:15:38 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4451f5c7eb7af74432585f5ebfbeb01bbfc87ec4a74dc93703bdd89330559cd1`  
		Last Modified: Mon, 26 Jul 2021 21:23:44 GMT  
		Size: 31.8 MB (31837572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d56df5ecf752059653014e714bae6507778c2fd9f6c3f864fdeb0f11be5318b`  
		Last Modified: Tue, 27 Jul 2021 00:18:24 GMT  
		Size: 5.6 MB (5597737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e7d996b67eeee2532d9643e28004d43fba9c80c19ac98f2b5378cc7fd200041`  
		Last Modified: Tue, 27 Jul 2021 00:18:23 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35723c871426551f5e5c91aa3caf285e3fbdd3819e9baba7432cc48fa90afc25`  
		Last Modified: Tue, 27 Jul 2021 00:18:23 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df43dcede292226ffbef4971d7b79425f61a336e7bf892f24f89f0cde937e57`  
		Last Modified: Tue, 27 Jul 2021 00:18:23 GMT  
		Size: 249.5 KB (249455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd21.04-non-free`

```console
$ docker pull neurodebian@sha256:dc1891c2764c95560eb7a56f32d5422ce7067031afe7915a82db5233d60bfe40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd21.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:a255713afcc6cc708ac499c0b89e5bd2d9623c2d5f38b83c8964a323ea4b0030
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37687033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9445c97ade590117897e42cddf4822b60f20bd87239e97e4bbd859e27dc8608e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:54 GMT
ADD file:6ae44786caae9af1c6b70dc9cc244e7d4e06fffc0696f68877527d69aa3fc735 in / 
# Mon, 26 Jul 2021 21:21:54 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:15:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:15:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 27 Jul 2021 00:15:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian hirsute main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel hirsute main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 27 Jul 2021 00:15:38 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:15:45 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:4451f5c7eb7af74432585f5ebfbeb01bbfc87ec4a74dc93703bdd89330559cd1`  
		Last Modified: Mon, 26 Jul 2021 21:23:44 GMT  
		Size: 31.8 MB (31837572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d56df5ecf752059653014e714bae6507778c2fd9f6c3f864fdeb0f11be5318b`  
		Last Modified: Tue, 27 Jul 2021 00:18:24 GMT  
		Size: 5.6 MB (5597737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e7d996b67eeee2532d9643e28004d43fba9c80c19ac98f2b5378cc7fd200041`  
		Last Modified: Tue, 27 Jul 2021 00:18:23 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35723c871426551f5e5c91aa3caf285e3fbdd3819e9baba7432cc48fa90afc25`  
		Last Modified: Tue, 27 Jul 2021 00:18:23 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df43dcede292226ffbef4971d7b79425f61a336e7bf892f24f89f0cde937e57`  
		Last Modified: Tue, 27 Jul 2021 00:18:23 GMT  
		Size: 249.5 KB (249455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dafb5cb912e6be0079cd434fc4fb0c83d60571d2b29cca69b8bb32cfb2babb3`  
		Last Modified: Tue, 27 Jul 2021 00:18:34 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd90`

```console
$ docker pull neurodebian@sha256:bd6ed680ec87f09d2f7d938c3a3cfb9a9830c8ca70c48066f18cd4f2e49d65d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd90` - linux; amd64

```console
$ docker pull neurodebian@sha256:80a21d864cafb2cc871224998949aafc5e01fe82f654751984f95716aa1d8178
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52247307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf30cb4f6f16df85b68edd6f5a292439879dfaa2514414fcf416693a6ba92ba`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:25:56 GMT
ADD file:0d0aa1ebd07b0f301aaf1077d1e9f2e9be1859510dd8535e143571b347a2a379 in / 
# Tue, 17 Aug 2021 01:25:56 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:41:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:41:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 17 Aug 2021 11:41:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 17 Aug 2021 11:41:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eb18d230e067c240479c6a3f842e7f9d4ff1088e3072d0a3245829c4e356623f`  
		Last Modified: Tue, 17 Aug 2021 01:33:03 GMT  
		Size: 45.4 MB (45379966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74da9bd3ea387bd8f0c1d956c5f13bc59105ab662f4faa816279a810b0e41035`  
		Last Modified: Tue, 17 Aug 2021 11:43:48 GMT  
		Size: 6.6 MB (6571669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ee3441efbe03819d8184474dc717251fb4974110beca925e6149a15a671513`  
		Last Modified: Tue, 17 Aug 2021 11:43:47 GMT  
		Size: 3.2 KB (3156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f8b5792a9dd26b558e699eebf1dbf350b5962108aba91c8e39b2fc3f0be09f`  
		Last Modified: Tue, 17 Aug 2021 11:43:47 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c2b3622754909c2f66abc9b9350ef378d4e0ef9023df1d36ca71d77447da0b`  
		Last Modified: Tue, 17 Aug 2021 11:43:47 GMT  
		Size: 292.3 KB (292270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:nd90-non-free`

```console
$ docker pull neurodebian@sha256:f8d33e8702c1fd370a34334135d75b5bc88c9b2a215cf0eddc88370cd77323d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:nd90-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:17259e9962b7d067be1067ac841d3e477b1b17ae621196a71f7e81cdd2241f12
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52247674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ec2ca9e9ae74dd07e6d0edffcae867b93166ceba2277589742c3b8ffa0ce7b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:25:56 GMT
ADD file:0d0aa1ebd07b0f301aaf1077d1e9f2e9be1859510dd8535e143571b347a2a379 in / 
# Tue, 17 Aug 2021 01:25:56 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:41:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:41:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 17 Aug 2021 11:41:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 17 Aug 2021 11:41:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:41:24 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:eb18d230e067c240479c6a3f842e7f9d4ff1088e3072d0a3245829c4e356623f`  
		Last Modified: Tue, 17 Aug 2021 01:33:03 GMT  
		Size: 45.4 MB (45379966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74da9bd3ea387bd8f0c1d956c5f13bc59105ab662f4faa816279a810b0e41035`  
		Last Modified: Tue, 17 Aug 2021 11:43:48 GMT  
		Size: 6.6 MB (6571669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ee3441efbe03819d8184474dc717251fb4974110beca925e6149a15a671513`  
		Last Modified: Tue, 17 Aug 2021 11:43:47 GMT  
		Size: 3.2 KB (3156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f8b5792a9dd26b558e699eebf1dbf350b5962108aba91c8e39b2fc3f0be09f`  
		Last Modified: Tue, 17 Aug 2021 11:43:47 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c2b3622754909c2f66abc9b9350ef378d4e0ef9023df1d36ca71d77447da0b`  
		Last Modified: Tue, 17 Aug 2021 11:43:47 GMT  
		Size: 292.3 KB (292270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4503ff964929647a79980a1703d4825513e72476336a03949c8edc1a8d33f86d`  
		Last Modified: Tue, 17 Aug 2021 11:43:58 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:46d4ff0665db7f115a9f18d83aed21a69fbab671f290ae95b4f4e4132518842c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:bef51b302becfa096c68984712136aa1f61a955b7ee09a62e025348daa7c6d47
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61241418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6a8a1942392fd5336fbbf0d6ce711a2cbcf599ed6b397b0e79c0714408d7878`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:41:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:41:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 17 Aug 2021 11:41:45 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 17 Aug 2021 11:41:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:41:58 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec371be32636521f27bad15f42934bb1189f1f408cbe19471ac6372862924d1`  
		Last Modified: Tue, 17 Aug 2021 11:44:09 GMT  
		Size: 10.5 MB (10500040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99d5763b996b375cdcf31e9831e332f51a3298c56790cb567a11070da5da5a0`  
		Last Modified: Tue, 17 Aug 2021 11:44:07 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308144ecaf23b11e838899244248ce7bc70d6912ad831de7fada3630f0c0b59`  
		Last Modified: Tue, 17 Aug 2021 11:44:07 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2078e085ecc552d76ef0a184b32d682163684a6eaa033ddf9202290bda3c8ea`  
		Last Modified: Tue, 17 Aug 2021 11:44:07 GMT  
		Size: 302.8 KB (302799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1746f0cf4c2f09051bcb143c8041cfc5033c4d13c9b22a573e8a729923cdf6a0`  
		Last Modified: Tue, 17 Aug 2021 11:44:20 GMT  
		Size: 366.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:eb53c2b1b9269695e52d90c075a9eccfde83bb8aa2f73713f0f85c38aabd9c51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:2a62e113e5893316ef7f83654b81fc95b5a5848d0fc54dcc139e514699732c9f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.6 MB (66553807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f54735921ebcd8fe81d80a77df0b70e093d11d8961d87c18b90972ee1eca273`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:25:06 GMT
ADD file:3052ec53a19fa26baad5d50e4d2867be2cc386ae62195d8dbb9d90d0b904c464 in / 
# Tue, 17 Aug 2021 01:25:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:42:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:42:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 17 Aug 2021 11:42:46 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 17 Aug 2021 11:42:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a6952a6bd46e0eaa2c0e7e851a45f288b3dc080472a9249e48c74b3fb7551fcc`  
		Last Modified: Tue, 17 Aug 2021 01:31:55 GMT  
		Size: 54.9 MB (54930846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410ec36aee1a8f201f9c0031cd0f05202d26dd1d1436a96bf9c25d7e16cd6409`  
		Last Modified: Tue, 17 Aug 2021 11:44:56 GMT  
		Size: 11.3 MB (11309853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511f77571d0ebc200d836bb589cbdbc218a43528b6107216fb05ac08b051e861`  
		Last Modified: Tue, 17 Aug 2021 11:44:55 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb24c8352006baecfb22a1adb719cc0dd9979fc96bd6e659b84d5e08367516a4`  
		Last Modified: Tue, 17 Aug 2021 11:44:57 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3017795095606b9588affb41bc71fcda9f48a651b50d1e21b632ed47564d944c`  
		Last Modified: Tue, 17 Aug 2021 11:44:55 GMT  
		Size: 311.1 KB (311099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:80a7a7c1946118af7d7021ff098f4b1181c437cf6078393ef71116bb7b4a1353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:7e888b386ccd79eed3cc5c45d9c4e74665cbcd61c69317984194ea9b143c2686
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.6 MB (66554123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44cc3785a6cdb16a17d84956f49da466b06e6a126197a0a9ae26eb68582e92ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:25:06 GMT
ADD file:3052ec53a19fa26baad5d50e4d2867be2cc386ae62195d8dbb9d90d0b904c464 in / 
# Tue, 17 Aug 2021 01:25:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:42:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:42:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 17 Aug 2021 11:42:46 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 17 Aug 2021 11:42:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:42:56 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:a6952a6bd46e0eaa2c0e7e851a45f288b3dc080472a9249e48c74b3fb7551fcc`  
		Last Modified: Tue, 17 Aug 2021 01:31:55 GMT  
		Size: 54.9 MB (54930846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410ec36aee1a8f201f9c0031cd0f05202d26dd1d1436a96bf9c25d7e16cd6409`  
		Last Modified: Tue, 17 Aug 2021 11:44:56 GMT  
		Size: 11.3 MB (11309853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511f77571d0ebc200d836bb589cbdbc218a43528b6107216fb05ac08b051e861`  
		Last Modified: Tue, 17 Aug 2021 11:44:55 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb24c8352006baecfb22a1adb719cc0dd9979fc96bd6e659b84d5e08367516a4`  
		Last Modified: Tue, 17 Aug 2021 11:44:57 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3017795095606b9588affb41bc71fcda9f48a651b50d1e21b632ed47564d944c`  
		Last Modified: Tue, 17 Aug 2021 11:44:55 GMT  
		Size: 311.1 KB (311099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1f96b4ea8e389a530c0f176604c77f640d48f27ed379dd42b0624d42999787`  
		Last Modified: Tue, 17 Aug 2021 11:45:08 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:stretch`

```console
$ docker pull neurodebian@sha256:bd6ed680ec87f09d2f7d938c3a3cfb9a9830c8ca70c48066f18cd4f2e49d65d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:stretch` - linux; amd64

```console
$ docker pull neurodebian@sha256:80a21d864cafb2cc871224998949aafc5e01fe82f654751984f95716aa1d8178
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52247307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf30cb4f6f16df85b68edd6f5a292439879dfaa2514414fcf416693a6ba92ba`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:25:56 GMT
ADD file:0d0aa1ebd07b0f301aaf1077d1e9f2e9be1859510dd8535e143571b347a2a379 in / 
# Tue, 17 Aug 2021 01:25:56 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:41:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:41:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 17 Aug 2021 11:41:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 17 Aug 2021 11:41:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eb18d230e067c240479c6a3f842e7f9d4ff1088e3072d0a3245829c4e356623f`  
		Last Modified: Tue, 17 Aug 2021 01:33:03 GMT  
		Size: 45.4 MB (45379966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74da9bd3ea387bd8f0c1d956c5f13bc59105ab662f4faa816279a810b0e41035`  
		Last Modified: Tue, 17 Aug 2021 11:43:48 GMT  
		Size: 6.6 MB (6571669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ee3441efbe03819d8184474dc717251fb4974110beca925e6149a15a671513`  
		Last Modified: Tue, 17 Aug 2021 11:43:47 GMT  
		Size: 3.2 KB (3156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f8b5792a9dd26b558e699eebf1dbf350b5962108aba91c8e39b2fc3f0be09f`  
		Last Modified: Tue, 17 Aug 2021 11:43:47 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c2b3622754909c2f66abc9b9350ef378d4e0ef9023df1d36ca71d77447da0b`  
		Last Modified: Tue, 17 Aug 2021 11:43:47 GMT  
		Size: 292.3 KB (292270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:stretch-non-free`

```console
$ docker pull neurodebian@sha256:f8d33e8702c1fd370a34334135d75b5bc88c9b2a215cf0eddc88370cd77323d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:stretch-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:17259e9962b7d067be1067ac841d3e477b1b17ae621196a71f7e81cdd2241f12
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52247674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ec2ca9e9ae74dd07e6d0edffcae867b93166ceba2277589742c3b8ffa0ce7b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:25:56 GMT
ADD file:0d0aa1ebd07b0f301aaf1077d1e9f2e9be1859510dd8535e143571b347a2a379 in / 
# Tue, 17 Aug 2021 01:25:56 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:41:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:41:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 17 Aug 2021 11:41:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian stretch main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel stretch main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 17 Aug 2021 11:41:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:41:24 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:eb18d230e067c240479c6a3f842e7f9d4ff1088e3072d0a3245829c4e356623f`  
		Last Modified: Tue, 17 Aug 2021 01:33:03 GMT  
		Size: 45.4 MB (45379966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74da9bd3ea387bd8f0c1d956c5f13bc59105ab662f4faa816279a810b0e41035`  
		Last Modified: Tue, 17 Aug 2021 11:43:48 GMT  
		Size: 6.6 MB (6571669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ee3441efbe03819d8184474dc717251fb4974110beca925e6149a15a671513`  
		Last Modified: Tue, 17 Aug 2021 11:43:47 GMT  
		Size: 3.2 KB (3156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f8b5792a9dd26b558e699eebf1dbf350b5962108aba91c8e39b2fc3f0be09f`  
		Last Modified: Tue, 17 Aug 2021 11:43:47 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c2b3622754909c2f66abc9b9350ef378d4e0ef9023df1d36ca71d77447da0b`  
		Last Modified: Tue, 17 Aug 2021 11:43:47 GMT  
		Size: 292.3 KB (292270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4503ff964929647a79980a1703d4825513e72476336a03949c8edc1a8d33f86d`  
		Last Modified: Tue, 17 Aug 2021 11:43:58 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:xenial`

```console
$ docker pull neurodebian@sha256:43b573d833942d586f9a7d4a1c3f1ca209077a20b2a90c26cb02b0fa61b03156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:xenial` - linux; amd64

```console
$ docker pull neurodebian@sha256:3160d9542153b47caf8d069cbc0db22d1638ad4adbd353f1259c21355f99b6ea
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46729660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f1bda86cb8ade0c529bcb17fda696383d42d0188167b4119599fb18acdbab3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:22:15 GMT
ADD file:a94a87e268e99c78143fae5148bd1200bf0da90c0e7f42bd8c168bb205ccb105 in / 
# Mon, 26 Jul 2021 21:22:16 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 26 Jul 2021 21:22:17 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 21:22:17 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 26 Jul 2021 21:22:18 GMT
CMD ["/bin/bash"]
# Tue, 27 Jul 2021 00:13:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:13:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 27 Jul 2021 00:13:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian xenial main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel xenial main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 27 Jul 2021 00:13:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:52818491084148fa3469964bbcc3576686018a3b16b2e29be0407565c4c80b44`  
		Last Modified: Thu, 22 Jul 2021 16:25:00 GMT  
		Size: 46.5 MB (46497362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9df81d603d28f2a294b2f11b4f60d07b5b833b2ad7d6659a3f59b10cff2696`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636d9303bf663657be8e6796d720913bb985b5343da7949749ae1e72b54a88d8`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672b5bdcef61237567b311ad3d349f5eae18ba839ce2b204858a3083437a0a59`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e7416d41f03136eeac7efb16c3fd8a6589880fff5bda819b3a1e6066c41fef7`  
		Last Modified: Tue, 27 Jul 2021 00:16:47 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bd79c96d093dd72ba4bbd9c6352b1fb0f299189cdc0d6388c894f24eec8714`  
		Last Modified: Tue, 27 Jul 2021 00:16:48 GMT  
		Size: 3.2 KB (3155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb360a6236175933715f7da41d199cb387954378bed350ccbcccc94565dfefe`  
		Last Modified: Tue, 27 Jul 2021 00:16:47 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0bfb7b9c9a2ce4ec8233a80b6131f224640f54ca2b6af5dcde3f11b71f315d4`  
		Last Modified: Tue, 27 Jul 2021 00:16:47 GMT  
		Size: 227.2 KB (227170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neurodebian:xenial-non-free`

```console
$ docker pull neurodebian@sha256:822e4ac31d3f0aadb858981a3ee4ece7f5d77edb5fb8f6b81efb166e3be2699a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neurodebian:xenial-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:62ea27a9925c741937b8763cdb75ecd8c3dfbca34503701c7eb16b37f277c439
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46729916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21bb46914f12361be318974e8b6196f2a48122d7c2eaa4d987cd4c9f60d09626`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:22:15 GMT
ADD file:a94a87e268e99c78143fae5148bd1200bf0da90c0e7f42bd8c168bb205ccb105 in / 
# Mon, 26 Jul 2021 21:22:16 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 26 Jul 2021 21:22:17 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 21:22:17 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 26 Jul 2021 21:22:18 GMT
CMD ["/bin/bash"]
# Tue, 27 Jul 2021 00:13:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:13:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 27 Jul 2021 00:13:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian xenial main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel xenial main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 27 Jul 2021 00:13:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:13:19 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:52818491084148fa3469964bbcc3576686018a3b16b2e29be0407565c4c80b44`  
		Last Modified: Thu, 22 Jul 2021 16:25:00 GMT  
		Size: 46.5 MB (46497362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9df81d603d28f2a294b2f11b4f60d07b5b833b2ad7d6659a3f59b10cff2696`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636d9303bf663657be8e6796d720913bb985b5343da7949749ae1e72b54a88d8`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672b5bdcef61237567b311ad3d349f5eae18ba839ce2b204858a3083437a0a59`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e7416d41f03136eeac7efb16c3fd8a6589880fff5bda819b3a1e6066c41fef7`  
		Last Modified: Tue, 27 Jul 2021 00:16:47 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bd79c96d093dd72ba4bbd9c6352b1fb0f299189cdc0d6388c894f24eec8714`  
		Last Modified: Tue, 27 Jul 2021 00:16:48 GMT  
		Size: 3.2 KB (3155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb360a6236175933715f7da41d199cb387954378bed350ccbcccc94565dfefe`  
		Last Modified: Tue, 27 Jul 2021 00:16:47 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0bfb7b9c9a2ce4ec8233a80b6131f224640f54ca2b6af5dcde3f11b71f315d4`  
		Last Modified: Tue, 27 Jul 2021 00:16:47 GMT  
		Size: 227.2 KB (227170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787a536fe6fc734fba11687bdfb5bf9d581534aadb3907eb628b70239dff16e4`  
		Last Modified: Tue, 27 Jul 2021 00:17:00 GMT  
		Size: 256.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
