## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:4ea684055c35645685e8aed0e3c01478fec16fd5ffca0f9a39f0e596edc0ed50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd120-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:8e832b29196db0f32af55eda6ef202b9f4b697690e13c8ddb78ff2230d35b154
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64670889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c057e56d52e96c4c40faea2abb608948144d4234b4023acd2c846fc23125086`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 00:20:15 GMT
ADD file:7507edfdf016128615e9ba278d471fd6d27c96436e543786b691c93b6f94b56b in / 
# Tue, 23 Aug 2022 00:20:16 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 03:55:54 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 03:55:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 23 Aug 2022 03:55:56 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 23 Aug 2022 03:55:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 03:56:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:5e784af754e1c7855decd29b818520a98b5b539515cd7c199c5dbceb6cc4a45f`  
		Last Modified: Tue, 23 Aug 2022 00:23:57 GMT  
		Size: 52.7 MB (52725730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650c798b6bdd1512fe63c6cf25cc09780086b64703ad0bc4208790384f464363`  
		Last Modified: Tue, 23 Aug 2022 03:57:58 GMT  
		Size: 11.7 MB (11650437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c927b815f82cc37ed61292156716f9fffd225fc2cc423508787a104d35b4dc`  
		Last Modified: Tue, 23 Aug 2022 03:57:56 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3fffa8e969c190aadb7263dc443f80fde51e18ad3b19e797cfc97b05b69940`  
		Last Modified: Tue, 23 Aug 2022 03:57:56 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca479e17c89ef83eefe0368d4c0efc753811049db26c00d5210dd776cc7ba069`  
		Last Modified: Tue, 23 Aug 2022 03:57:56 GMT  
		Size: 292.3 KB (292348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a89ced0cec2c05752478822c2ef56c88dc4576dceb06e84590537f004ba6452`  
		Last Modified: Tue, 23 Aug 2022 03:58:07 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:613019438494951252b0c12cecd0e620c00d13c83fbdd75a944b0fd33584b60e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64662007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d4036d940849434d03949dbb2d47f1a8b20d1ae235bb9365546b0bde8e38d5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 01:51:53 GMT
ADD file:f94a576f262c4fcf5112164145c04850c826787b299878e7e126754d1211a51c in / 
# Tue, 23 Aug 2022 01:51:53 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 04:41:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 04:41:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 23 Aug 2022 04:41:27 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 23 Aug 2022 04:41:31 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 04:41:39 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:7dd208a8a7339c037c691e6ace1cd3f94803ee4c17a3211b9ccadf01d1ff2ca9`  
		Last Modified: Tue, 23 Aug 2022 01:56:50 GMT  
		Size: 53.1 MB (53117563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a006b5263649e771e4ee55bd5d94edb00d6f14e74d51a2277e6269ffa0ca683a`  
		Last Modified: Tue, 23 Aug 2022 04:44:32 GMT  
		Size: 11.4 MB (11445143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccdc42b7fbf708ecbe63cdb5b74d5200ba729bc6136ffaa477e4e87b5248bbad`  
		Last Modified: Tue, 23 Aug 2022 04:44:30 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981c85701c833c8b5beb94b468806214b762887f6a5bca3596afffc113d1fb34`  
		Last Modified: Tue, 23 Aug 2022 04:44:30 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd92d83ced9119e462aa83ffcf9c4836e0d852c4e8a92ba87b54c26512eb81a`  
		Last Modified: Tue, 23 Aug 2022 04:44:30 GMT  
		Size: 97.0 KB (96952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093a3ca5f38d519788cd9affb6c7b0bff71751d10b12e90fb92a291cd4a2bc06`  
		Last Modified: Tue, 23 Aug 2022 04:44:42 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:dcab9250ea1c2d1c5dafdf4bf158ea86856d45ce1d9844d9f749594e9a9ec0ac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (65953171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f551bfedb0e03a0e0b335b674b898c65dd08f7475d54f130f09d44aa92edfd3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:38:40 GMT
ADD file:f331e5b0e8626bfcbb682d701943586f63db1ff65d9add0d94759ecaeb8c8269 in / 
# Tue, 02 Aug 2022 00:38:41 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 16:19:54 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 16:19:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 02 Aug 2022 16:19:56 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 02 Aug 2022 16:20:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 16:20:06 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:f78c3dc38f418186e278713175ef4cfc4bc70d85867d3597da89d03b5b956170`  
		Last Modified: Tue, 02 Aug 2022 00:43:55 GMT  
		Size: 54.0 MB (53974067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae8c66b4bb8cadf4b53644ccd234088106515eb05365f06331b37d3bc5eb099`  
		Last Modified: Tue, 02 Aug 2022 16:22:18 GMT  
		Size: 11.9 MB (11879913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bde24dd5326f2de30597d887c86597ef038a904e5dd0900a9d07c4662867ff4`  
		Last Modified: Tue, 02 Aug 2022 16:22:16 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0ab6157a1370156c19d5abf99e97f661c9e34b852d02789efe28253fbc45d0`  
		Last Modified: Tue, 02 Aug 2022 16:22:17 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415b8ec7e6730b1e84a05a158f37b694c42ddf99177223214958b8848f205c42`  
		Last Modified: Tue, 02 Aug 2022 16:22:17 GMT  
		Size: 96.8 KB (96842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dfb68ac818e8338ef3401f599abe51a6f30439a03cd7bf0f913eac22f90a6a8`  
		Last Modified: Tue, 02 Aug 2022 16:22:29 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
