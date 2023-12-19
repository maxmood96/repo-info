## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:1e854c9fa6458cf2800f14c2b9808601e4d8c1a13774b293820e86fbfea45712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:8bf257824aefa8385ad61f019be968c3ad774b46de888ffc6a0289f589144be0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65213680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b299f8fa9025b01fda6c1a485c3d1d8ae5587c500753eb30e0d3fb7912b860e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:23:12 GMT
ADD file:67c1d3c6f8f2705b6f6d6b4762836596ce976447eae7be0ec98e100a9231ebce in / 
# Tue, 21 Nov 2023 05:23:12 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:03:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:03:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 21 Nov 2023 09:03:03 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 21 Nov 2023 09:03:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:03:12 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:5af5a460cbb647bf09bd5ad2cdefd21714ccd512b0a7fba09506cd06308c9d18`  
		Last Modified: Tue, 21 Nov 2023 05:28:47 GMT  
		Size: 52.1 MB (52122268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5637e2505f3efe6a087f0f58c43c8fa65c0d83fd30901d7560db79c143a89afe`  
		Last Modified: Tue, 21 Nov 2023 09:04:40 GMT  
		Size: 12.8 MB (12802830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5bd83037a1745411887e11ab89e62bb031e2361c3db34862b23ca31dee441e1`  
		Last Modified: Tue, 21 Nov 2023 09:04:38 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837ae61a5f7f79b1d181aaba6974a82f53dcc648a239770ffeef958fdfb6a5fb`  
		Last Modified: Tue, 21 Nov 2023 09:04:38 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536170650855aec71462bc8423f1f5c9bb8c63968ba94830b610238d565d624c`  
		Last Modified: Tue, 21 Nov 2023 09:04:38 GMT  
		Size: 286.2 KB (286177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e2248e03a81aac3ef875d327ae662c63d1e610cff26c081cb48860b88ee6b82`  
		Last Modified: Tue, 21 Nov 2023 09:04:48 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:82cd99d15d3a48ea5f267295680e9de1fcc372bf0fe088b57df45b9978ab6dfb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64142492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c971a0a9a9e11e50fbb65fc492626dcec8c326556acb8dcdd888eb23e19e65`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:42:13 GMT
ADD file:b95bf5556d43a8a1d79a2dbf26ab8a4a912869d65cc1b76a372ca80259a65b7b in / 
# Tue, 19 Dec 2023 01:42:14 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:06:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:06:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 19 Dec 2023 03:06:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 19 Dec 2023 03:06:46 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:06:49 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:2f38ee39d2143cc6781c8d40b267519e59c558f7902df442f2e5ecfcefb01689`  
		Last Modified: Tue, 19 Dec 2023 01:47:24 GMT  
		Size: 49.7 MB (49689786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e289d2bd50130a54f42a5188139efd22f1e4f872bf3d2ea9ee64df6bbe8a2d`  
		Last Modified: Tue, 19 Dec 2023 03:08:14 GMT  
		Size: 14.2 MB (14163608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6592770f5ba6afac48334ec1e5b9f57d99a6972ab6ea31b37e445e6ed7836a81`  
		Last Modified: Tue, 19 Dec 2023 03:08:12 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b92ab013a67f046cd17d84ea7ab3e4f6eedba968eef8b8e56083974801edbb4`  
		Last Modified: Tue, 19 Dec 2023 03:08:12 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c053063e1b60822a02be21a864c0d45e978a421c861555ff8a276300ea58b7`  
		Last Modified: Tue, 19 Dec 2023 03:08:12 GMT  
		Size: 286.7 KB (286688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69a478f4b8b4d7f1802cbc5ebb6db8b13e757c1605ab3b55293ff8f58465165`  
		Last Modified: Tue, 19 Dec 2023 03:08:22 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:94976f90e5fa87a0ed44333f409cfeeab6a7ba07db6eb883d1489cc084e394c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65577648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6efd9e9e6b90b99f7d877031cc657ed13ef8a42e944e21227291ec87c9f2833f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:40:47 GMT
ADD file:736d4b14c103f5161855a9c14b05565523005af03b61bcfb3d6bfaddee9431f3 in / 
# Tue, 19 Dec 2023 01:40:47 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:51:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:51:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 19 Dec 2023 03:51:55 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 19 Dec 2023 03:52:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:52:06 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:567001fd97421e53b722a950bba83f44d7635056bc895f0b4f77b68d779fc15e`  
		Last Modified: Tue, 19 Dec 2023 01:46:59 GMT  
		Size: 50.6 MB (50559243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf0d5db5fdec42c82bcc5337d39f7bf6b089a42b3787d180eedd48aaf4d4a2bb`  
		Last Modified: Tue, 19 Dec 2023 03:53:24 GMT  
		Size: 14.7 MB (14729998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f9aec2cefffd0c64a74a6846300482dea9046c877c1c1559aae5523f25d8610`  
		Last Modified: Tue, 19 Dec 2023 03:53:21 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58ce81bf04c62ba5934917b776534fb6478af6e9325c3ee241a2345c0d800d5`  
		Last Modified: Tue, 19 Dec 2023 03:53:21 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00decda9d198acc08dcefd5412a863c2625149c3aca917edadf313f6696f075`  
		Last Modified: Tue, 19 Dec 2023 03:53:21 GMT  
		Size: 286.0 KB (285999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e688bdf943114a5f9eb7b38d60a3aedc84797466a58af2a005c848c05173c0`  
		Last Modified: Tue, 19 Dec 2023 03:53:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
