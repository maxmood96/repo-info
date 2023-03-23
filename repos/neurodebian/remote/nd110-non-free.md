## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:0aa37de092be864b3018db13b87ea51aaa51eac8d566ccbec31c0e1efdfefed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:397850dd721f2d70f2666b6034e38902616f1811810b36c57856e53a045e9260
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66671135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:570f9463ec5d93718c4ef20e1a5a0bb21677e80bc18d56c0e717c38e26c8b4c7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:45 GMT
ADD file:513c5d5e501279c21a05c1d8b66e5f0b02ee4b27f0b928706d92fd9ce11c1be6 in / 
# Wed, 01 Mar 2023 04:09:46 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 16:44:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:44:27 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 16:44:27 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 16:44:31 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:44:36 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:32fb02163b6bb519a30f909008e852354dae10bdfd6b34190dbdfe8f15403ea0`  
		Last Modified: Wed, 01 Mar 2023 04:13:58 GMT  
		Size: 55.0 MB (55045922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df5c007abfc5f3715238ab710d360a822c834f28faed9cc547746652dab22cd`  
		Last Modified: Wed, 01 Mar 2023 16:46:18 GMT  
		Size: 11.3 MB (11310897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1cdb53401388a02c1e5e17fc1dc83ec52e7997dd6b127fd9ad6bb3de19e52c`  
		Last Modified: Wed, 01 Mar 2023 16:46:17 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e51668d450029487fb5a4fb332c296d6948851c0d406c5b319d2998c6f4c2cc`  
		Last Modified: Wed, 01 Mar 2023 16:46:17 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db904d97aba2ef6f2e3a672e36e3569f2a042d58a5f50ca4a25604196db49bf4`  
		Last Modified: Wed, 01 Mar 2023 16:46:17 GMT  
		Size: 311.9 KB (311939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a90083e3034d3bc1b9cd93ac980645679a1506f873cd25e8759b770d6a61461`  
		Last Modified: Wed, 01 Mar 2023 16:46:29 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:295ddab89857cef0356935333a55df2ba7b26c6b53d402b293ff3f5c27e953d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65330164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f273b679fbf05cd298c531d890064262b449d3d7ac94283da3408f650ac4bfc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:02 GMT
ADD file:70d18f9eea4e4fbdb941e66490ccb7233e182fe7ded1185de91c7d55580dd13e in / 
# Thu, 23 Mar 2023 00:45:02 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 09:30:29 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:30:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 23 Mar 2023 09:30:30 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 23 Mar 2023 09:30:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:30:37 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:8022b074731d9ecee7f4fba79b993920973811dda168bbc08636f18523b90122`  
		Last Modified: Thu, 23 Mar 2023 00:47:46 GMT  
		Size: 53.7 MB (53703099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1073198b78bb3e7b1ce4370609ffa5310772b90829b03034acf5ff27fc5f6fbc`  
		Last Modified: Thu, 23 Mar 2023 09:31:48 GMT  
		Size: 11.3 MB (11312879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b494f8a0906f457066670c42f89edf0123014152733ca71c0b65dc7862cbfbf`  
		Last Modified: Thu, 23 Mar 2023 09:31:47 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8d72de2ce242bb047e2e0892ff659ce549fe3be331a3354e2760f601b48107`  
		Last Modified: Thu, 23 Mar 2023 09:31:46 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5987ef310f1e22a1071117070fc246f525fcab178073b74dfac7696582cbab`  
		Last Modified: Thu, 23 Mar 2023 09:31:47 GMT  
		Size: 311.8 KB (311812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013b84876434546224a0b3486b5afd43e5f2e02d867d6595aa8aea5dab4980ff`  
		Last Modified: Thu, 23 Mar 2023 09:31:57 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:17342a3cac539237ebbf3decf4a3d0fb62f2aea056d47801e5993ac452c7476e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68050126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82edc11129ce5d91a4c497d06338acbe0e6389aceababdb7bf378a6e525b74d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:39:01 GMT
ADD file:881e5812ed9664defe9745d26894a268ec27de907c9a615a5204bbb5e8e94262 in / 
# Wed, 01 Mar 2023 01:39:02 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:02:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 14:02:16 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 14:02:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:02:24 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:0a0c64c8f15c57499fa240b509d736a6e6b861478b11e52aadbc9551cfd10638`  
		Last Modified: Wed, 01 Mar 2023 01:44:12 GMT  
		Size: 56.0 MB (56028076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d58d45583f5f2bd82e8920458aa2cb48aed0e0d6f50ba44efb0923aa2c314ec`  
		Last Modified: Wed, 01 Mar 2023 14:04:23 GMT  
		Size: 11.7 MB (11707911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2ae0795989f1dd3adfa210230afec831ec4381bc92649f1a062f811a34ae70`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137c174eec1820823e69dd86b30989a7e2d0bcba2d2c59e49f95ffa14e54aaa8`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e50021c3c5964822b03b7f16a663a1ede8aa633768ab9c5f10ba67aa7a4f9cb`  
		Last Modified: Wed, 01 Mar 2023 14:04:21 GMT  
		Size: 311.8 KB (311766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ce7ee0211d218f2689625e321e91c6f45179a898f5b3baa1dc337e06185a96`  
		Last Modified: Wed, 01 Mar 2023 14:04:35 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
