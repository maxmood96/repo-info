## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:be4532d018b913b5d1a04d38788746ab5bfabe38ced126e42a64800da40289f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:1d9050ccc0475e9e9e6f5fc7a30926a1c501b2ce4b2c42e8c3b2ac7b1f468371
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64646531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72f492e5a61e2c8f114ba5e6663b837cc3fd012a765558599aa79d3c3211fdbe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:52:30 GMT
ADD file:7fec587617b78a81cacf7bfcdeac3b9e90b4135c4c242e80b5ea34f57d221168 in / 
# Wed, 10 Apr 2024 01:52:31 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 09:52:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:52:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 10 Apr 2024 09:52:14 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 10 Apr 2024 09:52:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:52:22 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:9c331a6d36afda0d91938277ed86b71e85bfb5904bb0efa434e13d0991817c34`  
		Last Modified: Wed, 10 Apr 2024 01:58:18 GMT  
		Size: 51.7 MB (51735884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48816c7fdc58b5956b3735ba4d3470ae4cc5fbd22e6d0320c17edf67a9b43f2b`  
		Last Modified: Wed, 10 Apr 2024 09:53:42 GMT  
		Size: 12.6 MB (12620360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcecbdee07372936cc82a1cf33920062b6a3a5ee3ae0b83eb54a2e9ce751a246`  
		Last Modified: Wed, 10 Apr 2024 09:53:41 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227243aca8967f39447f2235c4aadff5afc623f7b5dabcbac120cd90bf91f10b`  
		Last Modified: Wed, 10 Apr 2024 09:53:41 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e7a93ed117f5fd6d6b3f3b9193fe217252f5d40417ae70de64ceb120198460`  
		Last Modified: Wed, 10 Apr 2024 09:53:41 GMT  
		Size: 287.9 KB (287884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b62e423e895e3d2effc1fa9709528ddd4953e1c5371460c6017cff244c00bc`  
		Last Modified: Wed, 10 Apr 2024 09:53:49 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e33d516cdc361be2c1983630f4a425106b7428bbae0317b5a69a5ae6e28b71a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (65028691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c635c6680667b6158f737c57d0fd89ae7c703969321ad8b7b4e44dd790f22ed`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:41:31 GMT
ADD file:69ea41e74fa7a7601d1adbbdf992359f0c16c551447466cb4aaeac1914dc2377 in / 
# Wed, 10 Apr 2024 00:41:32 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:24:52 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:24:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 10 Apr 2024 07:24:53 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 10 Apr 2024 07:24:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:25:02 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:de2b6ae488daf95901751cee985416dfee51a36f7f9f15e60031279618e00a20`  
		Last Modified: Wed, 10 Apr 2024 00:46:49 GMT  
		Size: 52.1 MB (52136998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d3314e63373ea49d2747bbacfd86de539736d0ffd0bedb258a47825bec40fc`  
		Last Modified: Wed, 10 Apr 2024 07:26:21 GMT  
		Size: 12.6 MB (12600701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd79efd98f63f526acdcacf17861110f1469da8409683c6a86aca38ef692188`  
		Last Modified: Wed, 10 Apr 2024 07:26:20 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16fb0712dca88ceb3b40da1dfa46101e51680921e074b4e0e2c52d91ca134834`  
		Last Modified: Wed, 10 Apr 2024 07:26:20 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a7fd5f19f3cc1e174533a1b004cdf8eb36b373ccbd88b399d929068ba09561`  
		Last Modified: Wed, 10 Apr 2024 07:26:20 GMT  
		Size: 288.6 KB (288588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6089719930832275528eff840f3a481c202ca94ccf07850361a9332d02248626`  
		Last Modified: Wed, 10 Apr 2024 07:26:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:7d720fce2bfbba32832cc2bf799dd698e43bb233d4a37c2cd4d197b0cb4193b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (65963609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f46f2052a62716fe2561cd94f0df4bc0d16574b334e2a01e5d8736e1808ac0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:58:52 GMT
ADD file:e239896f7b5e011b6d0233f2b19722dd4ed9b477a41df953ada860d9292309a9 in / 
# Wed, 10 Apr 2024 00:58:53 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:24:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:24:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 10 Apr 2024 07:24:09 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 10 Apr 2024 07:24:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:24:17 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:aa1551ec75fa2e9c2e1970c5f0cf8c95e50b19638484e38cd439a1ae005100e7`  
		Last Modified: Wed, 10 Apr 2024 01:05:22 GMT  
		Size: 52.5 MB (52545296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679fd105449905a0a94707b3cba942d456bf9fe38526a79f7b341be509fb6708`  
		Last Modified: Wed, 10 Apr 2024 07:25:43 GMT  
		Size: 13.1 MB (13128155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2827d9b3036a22fee78ea17382d6ba1f730c8c763ef24312843fcaf186c8cc69`  
		Last Modified: Wed, 10 Apr 2024 07:25:40 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc53f67a234b9e433bd5bc4d7b7c4fe1e787931568ce54d0eb27900e207d2095`  
		Last Modified: Wed, 10 Apr 2024 07:25:40 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068b92b06f0afc1e120d97fe37e9366d8729e90600f03c95d7ccdbca3a3fd8b8`  
		Last Modified: Wed, 10 Apr 2024 07:25:40 GMT  
		Size: 287.8 KB (287757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a446d0e0f4843ac41fcb1c976e2e429b405f2dc9841ac6c22095f1b59139e6`  
		Last Modified: Wed, 10 Apr 2024 07:25:50 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
