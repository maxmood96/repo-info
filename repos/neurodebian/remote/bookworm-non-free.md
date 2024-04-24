## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:78d4242758abcd384f9cca19221e833dc778147a319c55ce997d7f61a8bc16e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bookworm-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:193070e0b61d57c19dbca51bcbd117ca60edadb54b22e0570b693a583b2867c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61314654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8bf6ad4ff0926c9ff35d4161a510be4889ca485eb3b41c87ea81d4b4fd65367`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:34 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
# Wed, 10 Apr 2024 01:50:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 09:51:48 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:51:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 10 Apr 2024 09:51:50 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 10 Apr 2024 09:51:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:51:58 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c087f86e121d55f4598e753f728ac2801dbe7e8199f2cd2cf2dc83bc988efc54`  
		Last Modified: Wed, 10 Apr 2024 09:53:25 GMT  
		Size: 11.5 MB (11463870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c369d6247952f21971956ccaf88bf54ba2e71d315602b3183283d2d040a396`  
		Last Modified: Wed, 10 Apr 2024 09:53:24 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb996df433ecf304998a1b8375abbbcb6bb3675aff13b0c1e24d8f8df5089f26`  
		Last Modified: Wed, 10 Apr 2024 09:53:24 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db057033acc071cce8a542b473b2338f27f8ceb75d8f5a22222ccd42298c6d8`  
		Last Modified: Wed, 10 Apr 2024 09:53:24 GMT  
		Size: 288.0 KB (287980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcf88b6e1b2d26448e99250d4adcdbd76b4aaf8841edce63b9b0f93817cbb21`  
		Last Modified: Wed, 10 Apr 2024 09:53:33 GMT  
		Size: 428.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:91337a1e94def592bbd01d137c15beec06f770224a7e4e9916021ac4807c8bee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61335703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c4ce701f20e6ed13ecd243e1db2046bbfda06bb0838d4af3ce89407cc28f9f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:41:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:41:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 24 Apr 2024 04:41:27 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 24 Apr 2024 04:41:30 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:41:32 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc25b7b4f0f0785407b52c5ab62c03c68b16d48dbff6f85628b50a8d5a783d0`  
		Last Modified: Wed, 24 Apr 2024 04:42:57 GMT  
		Size: 11.4 MB (11429751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3e19eb2c60eedda2f4cf1976f0c806b310292a7d55e3b1ea15f8cf76d6ba2f`  
		Last Modified: Wed, 24 Apr 2024 04:42:56 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759585282845c3252db14d8ddcc2c4e2bf59648949ad6c9625a6afad359e0120`  
		Last Modified: Wed, 24 Apr 2024 04:42:56 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd085a612fc52502e17d38291e29478c6f400c15e4685dcc925cd3a9e8894833`  
		Last Modified: Wed, 24 Apr 2024 04:42:57 GMT  
		Size: 290.2 KB (290167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78819c7f738132280c3305dbdd627bf20b4edb2a9e149e3d73a85d826f5f5c84`  
		Last Modified: Wed, 24 Apr 2024 04:43:10 GMT  
		Size: 430.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:f21d2a2c52896cec8a69d3dc10c93c6c968e9f56549952f76a86f2e580095aa2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62761866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a01d8364920a2d50bd720b72856ddedd63634184e1e4603b9df00479321dbef`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:56:58 GMT
ADD file:790f7a239f36cc7d8fd7fba66cd64aaff5f743c1c06e080820f865bae8f4a8c1 in / 
# Wed, 10 Apr 2024 00:56:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:23:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:23:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 10 Apr 2024 07:23:42 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 10 Apr 2024 07:23:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:23:51 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:417ba0ba1bcbb46434cbd64273ffc8edbe2c1921e58094e580e87c3b8e518701`  
		Last Modified: Wed, 10 Apr 2024 01:01:38 GMT  
		Size: 50.6 MB (50587234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16eee48bd91b78b72210da4efa0fdcdc5e71fb772596cd8c0572336b1af8524`  
		Last Modified: Wed, 10 Apr 2024 07:25:16 GMT  
		Size: 11.9 MB (11883988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8527804a98939baaadec8983fdae4ab5ce88aa38dbc3fd98b78784b8adf96f`  
		Last Modified: Wed, 10 Apr 2024 07:25:14 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501cf72b2080e40e991ec5c9aa98d3348e202aa424b986a2e0677e824d2ed8b5`  
		Last Modified: Wed, 10 Apr 2024 07:25:14 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2a12e51afe8bf6ee26dfa29de12a2bfdb63e53df2d3b1a18bf795e95cbfd1c`  
		Last Modified: Wed, 10 Apr 2024 07:25:14 GMT  
		Size: 288.2 KB (288202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc6b13c79af4260e1e39014af8e2ab2fd06ce9b0f16e73635d2eabac48e32a4`  
		Last Modified: Wed, 10 Apr 2024 07:25:32 GMT  
		Size: 429.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
