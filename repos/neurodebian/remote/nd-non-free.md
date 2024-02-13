## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:efbe0862758a79c08418e148ebfd7d0f3130b767a2f0d2e1b29b2498b8f68add
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
$ docker pull neurodebian@sha256:072e02bd813aaf1c04480dc6616aa7a5d462330e0b8377a05bf39efd1fdf6b93
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65613859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643855a7f641e39abf852cf662d329317eba1d22bd5c6ed939269612d338d968`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:38 GMT
ADD file:4189b090bbf8678fcabd8dabb56450346892e68ce7343823f5a1de966a7cfba7 in / 
# Tue, 13 Feb 2024 00:40:38 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:52:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:52:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 13 Feb 2024 04:52:26 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 13 Feb 2024 04:52:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:52:37 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:986c70cdc0585f2b2041c18972cf24b00e1384bf0ae25efa4ed418df60c27f39`  
		Last Modified: Tue, 13 Feb 2024 00:47:09 GMT  
		Size: 53.2 MB (53166067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5ff05424983947d416460daea0beed52a01a3b9970b770c1167bc20aab7d58`  
		Last Modified: Tue, 13 Feb 2024 04:53:51 GMT  
		Size: 12.2 MB (12158920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb908d4224d5bd21959b0d22148bfb1ea7ce87a9c93e9730d26866e50dcac7c`  
		Last Modified: Tue, 13 Feb 2024 04:53:49 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b572f36ad7071a0c86ca82b412fbf974b419b567747af5beb97de04248175c`  
		Last Modified: Tue, 13 Feb 2024 04:53:49 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b369a74ab6bd1f00455c5f2416facd7c2cdfe2899849a79197778eb95b1ff03e`  
		Last Modified: Tue, 13 Feb 2024 04:53:49 GMT  
		Size: 286.5 KB (286473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab59594423f9e7097c19cf64324ac2c33ce55608463ebfdcc1d34e82618bc43`  
		Last Modified: Tue, 13 Feb 2024 04:53:59 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
