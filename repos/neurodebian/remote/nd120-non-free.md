## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:e824689fd765e6636fd053b8640c6c796089ca812aedeae435886e5b5368b67e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd120-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:bd5355676c5af8e531fbb1f95cb73c50e8aded59a5bbd628ba410ab609d423a7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (65014415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54479f492559d1e663f6669b2c7233f7cdea30f616c8fcdfe326d874ebec17a7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:03 GMT
ADD file:ca5a5911d0951e5c75f1790eb644a6fd41dcb9712fa2af0fb6d3a537a72e6ad8 in / 
# Tue, 04 Oct 2022 23:26:04 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 04:38:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:38:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 05 Oct 2022 04:38:32 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 05 Oct 2022 04:38:36 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:38:42 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:6674a3ae4f8f54c2f747bad2069e50ce00e352d650887729310d984cebecea22`  
		Last Modified: Tue, 04 Oct 2022 23:29:50 GMT  
		Size: 53.0 MB (52962415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2316c52551cab9cc0ad9166bc77e216033702e8aaabffc0abcfb89f136d8c76`  
		Last Modified: Wed, 05 Oct 2022 04:41:29 GMT  
		Size: 11.8 MB (11764299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe69058d31d6cd9481204bc8bf1336732437d0660a1d75e5f65767c22a94bb9`  
		Last Modified: Wed, 05 Oct 2022 04:41:27 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87205a6c66a4f8e9f0acef27904269125540931696cbeef7b33f8df121ac2edd`  
		Last Modified: Wed, 05 Oct 2022 04:41:27 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8368ed01254e7fabcaccc37943c9d4b1b860ee0375ed75e45c834a9c52ade31`  
		Last Modified: Wed, 05 Oct 2022 04:41:28 GMT  
		Size: 285.3 KB (285329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ca0c4df391b41681b1f4c8259b14ac54ae55eaca35fa4729063e3b06d85119`  
		Last Modified: Wed, 05 Oct 2022 04:41:37 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9fb15b3ee57c8ecf0c6fad7fbc5ce41d2124d2363d6d2532d4c74192ed6f5e4d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64610704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a146677dea1903a8763fe0202bdc02ac58275e1db107f7d1a45d48d360d56b1a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:00 GMT
ADD file:269c8bec4871d84b9133706a2f391209619d53c0bfa56121c740757cf5798fcb in / 
# Tue, 04 Oct 2022 23:44:02 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:59:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:59:18 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 05 Oct 2022 03:59:19 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 05 Oct 2022 03:59:23 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:59:30 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:2debf9e7f23054c81a936da9b01c5db9f72a55d4810f7bf0e5641bd1748d90b7`  
		Last Modified: Tue, 04 Oct 2022 23:49:11 GMT  
		Size: 53.0 MB (52980389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0ef51f5528c6564ff374a45d9cb4c4c6eaf535c3565cbb4ba763bc55b22343`  
		Last Modified: Wed, 05 Oct 2022 04:03:24 GMT  
		Size: 11.5 MB (11531064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469c79e490be5fc87427c713b2cff0a58e2d249f09613ea11f6d6a02ed9e62f7`  
		Last Modified: Wed, 05 Oct 2022 04:03:22 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52a22ac0a033238596c38df2f9af0747aa62ed9470c2a82f61ed8978d6ccc5f`  
		Last Modified: Wed, 05 Oct 2022 04:03:23 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8bc59e065b02635051c28a8a2b68751fbdc3486f83ce39b848da35674d67b13`  
		Last Modified: Wed, 05 Oct 2022 04:03:23 GMT  
		Size: 96.9 KB (96904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86addfd21f29a2b3cc2f2d4caa2e71233a7f3263674e19b65321fcf5e03cc560`  
		Last Modified: Wed, 05 Oct 2022 04:03:36 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:a0419b3921c4500ce8017f99b534dd4c66e6641fdd63cf8d17d36a607b17dead
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (66022979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee04776b466810c25260cd640d93dd96840d94e5bf91857e004aa6b5f454b5c6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:38:57 GMT
ADD file:2a0c743e373aeed6462c2f3ae8a138fb0e240e935ad7ca5bf008aa3efd3673a0 in / 
# Tue, 04 Oct 2022 23:38:58 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 02:15:35 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:15:37 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 05 Oct 2022 02:15:38 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 05 Oct 2022 02:15:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:15:50 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:c68776dad61a299b8e65d1a6a02e376b8ed2e9b241bd753bf6c35d497055ecdf`  
		Last Modified: Tue, 04 Oct 2022 23:44:23 GMT  
		Size: 53.9 MB (53932827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b23a7101cec8d64ddc2337801957f17d5366b0725dfb359c4a75a69d6a5e59b`  
		Last Modified: Wed, 05 Oct 2022 02:17:53 GMT  
		Size: 12.0 MB (11990988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bc6ea3e1edb50b087a2d132755dd424f332df905fd3ca53fc106283fa89192`  
		Last Modified: Wed, 05 Oct 2022 02:17:51 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f7492185dc14c52e2b31a59607eac615a02bb456adcdd05c611ea2b460da27`  
		Last Modified: Wed, 05 Oct 2022 02:17:51 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:156209dfa890bcc23c8e351f1f08baad61399ccb713ea04a5f81e3d9a8d3760a`  
		Last Modified: Wed, 05 Oct 2022 02:17:51 GMT  
		Size: 96.8 KB (96816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e038e92cc95c6ee9d08edbfccb0fd01d6cc3153d445b6ea5717491f57216b426`  
		Last Modified: Wed, 05 Oct 2022 02:18:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
