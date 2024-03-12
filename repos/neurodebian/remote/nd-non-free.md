## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:4e0819a5697a0eeafe84bd9f59337edbfcc3d53173704d7b8483e2857d503b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:b340a79d2a341c91db8c6a77475e62ba570526cdf7b52a1e0d2ad10500ebc231
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64365886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee32da5375780054b4a90751eb1f7198b49f0ffaa1c71365797c72a5007664d4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:01 GMT
ADD file:d669b75a7533bca38f2c301c256ebdfa35812b13652db86b8742a30e6856fd74 in / 
# Tue, 13 Feb 2024 00:39:01 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 11:26:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 11:26:56 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 13 Feb 2024 11:26:57 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 13 Feb 2024 11:27:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 11:27:06 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:b49777280093cb58e1e93044ad56b006d1fb67107f14896ae3fd237faac8d485`  
		Last Modified: Tue, 13 Feb 2024 00:44:56 GMT  
		Size: 52.3 MB (52336486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2fb79b4bfc9a9b9bc98aacf93eb694ea7d81d7144f42b9f294e4e95e783d1d`  
		Last Modified: Tue, 13 Feb 2024 11:28:30 GMT  
		Size: 11.7 MB (11740332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd1d20f6aa2686e64bc73f8298e8ec534036d891c88437552ca541ba61456c8`  
		Last Modified: Tue, 13 Feb 2024 11:28:28 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4657c66cb5f7dbc54c6de898a2a898a046845ec208fb7138f15ee2dea84e8b`  
		Last Modified: Tue, 13 Feb 2024 11:28:29 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e883645c227cf89a583f421a0604968dbd09497c690cdce0fc5d6592c33004`  
		Last Modified: Tue, 13 Feb 2024 11:28:29 GMT  
		Size: 286.7 KB (286669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e9766816b60586f0f1a687e1c1d0477ecf77da3f604dcac532507c704d1980`  
		Last Modified: Tue, 13 Feb 2024 11:28:38 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c55ddfbe0a72708842c7d92502388da10feb80fed43af033c1c9d14c492daf8a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64216244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:181108166e3164f97ec775e88d68fc3831a3fdeaaa8a48b5f506669ce93a2d92`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:42:26 GMT
ADD file:88085ab115a08b9d412def1f9fea5d59c60a8e26965f72639d8199179230cb86 in / 
# Tue, 13 Feb 2024 00:42:26 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:28:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:28:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 13 Feb 2024 02:28:20 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 13 Feb 2024 02:28:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:28:28 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:84e6541c14eb2246826ed0d079d915b03d190721bc05675c66f459f0cc97e40b`  
		Last Modified: Tue, 13 Feb 2024 00:47:37 GMT  
		Size: 52.2 MB (52195661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530d9fa27a5b36a7cb59316d7fe526dc5b251bea1a9f86c165075aa6fe54092f`  
		Last Modified: Tue, 13 Feb 2024 02:29:50 GMT  
		Size: 11.7 MB (11731160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80f670ddc162c044ae19dcb1808e1a0347e7fa4e9baa69b117caae4f075024f`  
		Last Modified: Tue, 13 Feb 2024 02:29:49 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dbbe655aff736d787cd9cb88478fb9c3773d0e7f10b679bbb85e5c46a939396`  
		Last Modified: Tue, 13 Feb 2024 02:29:49 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8305489ee84dc4b7567d41f89b89fd2f4ab7f144aea32d30e8d18605056090`  
		Last Modified: Tue, 13 Feb 2024 02:29:49 GMT  
		Size: 287.0 KB (287029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942506cdb77ed4a33b1d04d2419d2a98667fa841cc522764221f923951a1c6dd`  
		Last Modified: Tue, 13 Feb 2024 02:29:58 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:bc216070c880333bfcdc05b8a9b900f16460c23835c193ae5a8a9aeccd5a9f22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65659479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d024877dea71a1536a756aec7d627eb19781ba70c10c8978d1276368d49ca7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:40 GMT
ADD file:383595e3854ec7f22e8d333af3b6c0a5019c955f674a09a7c4bf1426ec9a661d in / 
# Tue, 12 Mar 2024 00:59:40 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:37:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:37:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 12 Mar 2024 01:37:19 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 12 Mar 2024 01:37:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:37:31 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:8c85e8b663e835053744f416ba1ea5847d00b7b5cb5dac4003e16ea78fe851b3`  
		Last Modified: Tue, 12 Mar 2024 01:05:55 GMT  
		Size: 52.3 MB (52250465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd7555a20337a05fd7e07b812be4ec859e409d73e940c618b561d51894d43da`  
		Last Modified: Tue, 12 Mar 2024 01:38:44 GMT  
		Size: 13.1 MB (13119089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346f3c41ccbd57b4aa7ee1a6225a1cd6555f9f42e5ce75c9bd8d278c46f63ddb`  
		Last Modified: Tue, 12 Mar 2024 01:38:42 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517da467f152240640a6ae7b9254e7561f696ff1f2b536882ad18e40711d55a6`  
		Last Modified: Tue, 12 Mar 2024 01:38:42 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085187cab94862ed8a7c58d99f66ce66633c6c4587e7c29559663e39680df4b6`  
		Last Modified: Tue, 12 Mar 2024 01:38:43 GMT  
		Size: 287.5 KB (287522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde8e83a8fd2b793f050542a82c4eb67f1b57ccc24c12079062f8e3d46a8f275`  
		Last Modified: Tue, 12 Mar 2024 01:38:52 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
