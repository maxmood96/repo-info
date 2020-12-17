## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:e388489756836c3604d65e26151ea1e96895e2f2aff2228321fab78702b3b65c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5bf0a8ab539a3061a177f582f83bdf81716c93e9e8e358594b1fa383d37945eb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.6 MB (473577214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf40329d2a502d3632fa0677a3849e8588de21636fafc34ab4e7b544478008f4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:05:18 GMT
ADD file:ec1a9a704ae13b142c48069368561119760ccdf3d65d854c426d0dc9c39e60fb in / 
# Fri, 11 Dec 2020 02:05:18 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 16:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 16:55:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 16:56:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 16:57:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e4991c356405721fc787980835bdbf5c529ae12379346a771feb34407c522bd6`  
		Last Modified: Fri, 11 Dec 2020 02:11:29 GMT  
		Size: 53.1 MB (53113553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31d9601ffb01bb76b4b0f063798a4d1ee0fd755c12d07c76aebee06efabb9ba`  
		Last Modified: Thu, 17 Dec 2020 17:23:45 GMT  
		Size: 7.9 MB (7908261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bba58616c17ab814aac1a7b782186b5ce1114f80b807ec7635a3895fecec549`  
		Last Modified: Thu, 17 Dec 2020 17:23:46 GMT  
		Size: 10.6 MB (10648148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4e78a0ed9f63a0a28e8e8e899d253ff1658a5536db81e8636b4fe46a4dc490`  
		Last Modified: Thu, 17 Dec 2020 17:24:13 GMT  
		Size: 53.8 MB (53849812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362f2ecb577bfb822fd0936355d49b56df36cd774d1da27cff5164edb77c1a2e`  
		Last Modified: Thu, 17 Dec 2020 17:25:45 GMT  
		Size: 348.1 MB (348057440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7d3ecbecf21eb100c12f8f48821458f5303c11d2a9ffcb80db3fefaec58268c8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **458.5 MB (458485542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a1003251b6e94429098945737a514f7f3fbd72168215a650dffb08e9bd752c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:03:07 GMT
ADD file:8b9117df3f1a986438250b725bc8ec117cf1caba2e6953cf9a870edbcda4c565 in / 
# Fri, 11 Dec 2020 02:03:10 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 01:48:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 01:49:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 01:50:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 01:53:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:69233e69b29a579de45732361ee762ae02ccbe96b0f2a09fc2a48a802a25b265`  
		Last Modified: Fri, 11 Dec 2020 02:13:31 GMT  
		Size: 51.1 MB (51053259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f37df2f9cd5b84770356fa5f939540352df527e8614387e2efb5526fb6ba3a`  
		Last Modified: Thu, 17 Dec 2020 02:10:26 GMT  
		Size: 7.5 MB (7461139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b0c8aa368faca2325c1ba58e6f5cab5bd150dfbee94b95963c35d62581f86b`  
		Last Modified: Thu, 17 Dec 2020 02:10:27 GMT  
		Size: 10.3 MB (10335182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212eef771074abcec8b78a98ac45bbf906c1c19db951d76d98bc559350707cab`  
		Last Modified: Thu, 17 Dec 2020 02:11:17 GMT  
		Size: 51.5 MB (51532447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8936ae1d45ad9e899049d38dcf9eb796704e0a17c7d71f1c008a0c6ed0194b69`  
		Last Modified: Thu, 17 Dec 2020 02:13:48 GMT  
		Size: 338.1 MB (338103515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c96d3b14903065ef1a806daced609099cc99555f6b23c9d72fbb92a9e32aefb5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.1 MB (432092381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a5d9c792bdba9592b938db1c30f75fe35d76b90068c0223b498f565c4e4390`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:22:18 GMT
ADD file:f1ca2b90268fd790612e08e0e01b5ea1b63749dbec2ebb79b37a6168e5e82815 in / 
# Fri, 11 Dec 2020 02:22:20 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 08:11:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 08:11:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 08:12:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 08:15:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3354b3972c3003db2792ea643d0250983d6938232305c0bd0b2f3f8ee458c9ca`  
		Last Modified: Fri, 11 Dec 2020 02:32:03 GMT  
		Size: 48.7 MB (48731592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baab97db610a1c905a0eebb8e725d651de6230d65856718b02a7b163ec6be47d`  
		Last Modified: Thu, 17 Dec 2020 08:50:10 GMT  
		Size: 7.2 MB (7201642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28db3c64e92e3b49294d9851fd87b5a747ba682105ffa349b1b91e08f977d2a7`  
		Last Modified: Thu, 17 Dec 2020 08:50:10 GMT  
		Size: 10.0 MB (9974261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdba5ff0958089b4a9eb1ac55908b6ad830216260bd4f77573aca9e88494657e`  
		Last Modified: Thu, 17 Dec 2020 08:50:34 GMT  
		Size: 49.6 MB (49588839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd9223cddc6fd044d29a6eb1e7a095df51fd9c8dc99a9e1d6c953db02b15fbfd`  
		Last Modified: Thu, 17 Dec 2020 08:52:13 GMT  
		Size: 316.6 MB (316596047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7efb4645c06b0553629a6c8c241b0342f2e998de644c79e86dd0b90207627410
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.6 MB (464624488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b74f6b43f76fc5afc99422e47418a79bc4a9fcfc598088fb46071b4478c1d1d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:44:38 GMT
ADD file:8b5c11cc7a49f4bcd4f99db7d2c343338d9930a8254ed6527ec04ee8f41446d1 in / 
# Fri, 11 Dec 2020 02:44:40 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 10:01:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 10:02:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 10:03:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 10:05:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:452eaeaea0dc38e36d92c42c3301a9bf90cd1779fdbe05d762ba387c5823b66d`  
		Last Modified: Fri, 11 Dec 2020 02:51:52 GMT  
		Size: 52.0 MB (51961868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0d52d53c53e183980fe740fce73a7c89f32b4adea4989c49be8a76c2999c75`  
		Last Modified: Thu, 17 Dec 2020 10:36:06 GMT  
		Size: 7.8 MB (7769932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd2421bac8b34a287e63b8037ea012d6d3cc94f585a8661e2c6ac8b3b643cf6`  
		Last Modified: Thu, 17 Dec 2020 10:36:06 GMT  
		Size: 10.7 MB (10653916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b747c34e3bd0d2dd82a55e6d50f5f15bddf4acd3c3a008ffcb20ac74c983fe`  
		Last Modified: Thu, 17 Dec 2020 10:36:33 GMT  
		Size: 54.0 MB (53971214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d088b9e1ead7a25c9d17bceed3b30b5a590bdc7668a45bb92031b9b6469e88`  
		Last Modified: Thu, 17 Dec 2020 10:38:02 GMT  
		Size: 340.3 MB (340267558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:325d23ffdb7414599f6ac964476c3c1bdf11811fbee52cd473af0e74cc37538c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.1 MB (335111425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b83e1843dd69df65aa3c6b374f5f180e6654728ace2ee23c00a5887548c9e31`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:02:21 GMT
ADD file:b10b66385eba9f330914811c1ea9830c75a7d222442b3076a102c918588f96cc in / 
# Fri, 11 Dec 2020 02:02:22 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 08:06:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 08:06:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 08:06:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 08:08:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5cec9c367337182f351780e9e280bde357c303f0ca43358fc7dcbe63a9420fb1`  
		Last Modified: Fri, 11 Dec 2020 02:08:35 GMT  
		Size: 54.2 MB (54157004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bfed47518c0a507801e5cbe565f2d9072a66d37097eb93c108be072d452bcc7`  
		Last Modified: Thu, 17 Dec 2020 08:22:55 GMT  
		Size: 8.1 MB (8082025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c73ad66a61af03c90dfc68fd0342e7c31aede5c056cec3bb18195e6c3af97ff`  
		Last Modified: Thu, 17 Dec 2020 08:22:55 GMT  
		Size: 11.0 MB (11031118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b17636990e83105666693f7637b7aeb56bbcfc13e62b0eac8d8e8a78c158b8`  
		Last Modified: Thu, 17 Dec 2020 08:23:33 GMT  
		Size: 55.1 MB (55144761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93bce259fdca42d889bac8a282a3f05d40d562e9d840ce71381d67156e623e21`  
		Last Modified: Thu, 17 Dec 2020 08:25:10 GMT  
		Size: 206.7 MB (206696517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:33be7804b208706e2d1cfd5ec555dc8796f8ab9ecb0116690b38f14bb87fb92c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.8 MB (307800086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad889d3e2cf1006aa61b20f1bbc75137e05e4eb3da19196287cca7fdee16917`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:02:20 GMT
ADD file:1c9d3b0dae65df3d925c78ab44bc00642c930f3deef925694dc0c1a3213de35a in / 
# Fri, 11 Dec 2020 02:02:21 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 02:07:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 02:08:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 02:08:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 02:11:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ede4ac036d71d6e9539de8a220d9f79c46f7c9cb9bf53f8498188327ec302195`  
		Last Modified: Fri, 11 Dec 2020 02:08:06 GMT  
		Size: 51.8 MB (51829610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6b5a1437a4f1692906f39eec85d6b3bb70a1f4164e324e1d9a001d903c7e87`  
		Last Modified: Thu, 17 Dec 2020 02:20:48 GMT  
		Size: 7.4 MB (7428942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c3593042d91d6e96d4f41313ca6efcc8a059da9d708b31e0f3dc5ebd823ccc`  
		Last Modified: Thu, 17 Dec 2020 02:20:50 GMT  
		Size: 10.7 MB (10656677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ceb1263972938cd1bc3132438877816eb79dd7894295e23b3a307805917fd3f`  
		Last Modified: Thu, 17 Dec 2020 02:21:44 GMT  
		Size: 52.6 MB (52583429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f35e046700922385d21428b9eccc2b7a23cc42eac338eb5c764d15a1cb170d6`  
		Last Modified: Thu, 17 Dec 2020 02:23:56 GMT  
		Size: 185.3 MB (185301428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0b2b21bd2f597465c03101c62646325ba64499ec6f02f0ed8ea57fce10034cd6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **471.4 MB (471371421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03b47d0cee4c98be6ea83641ecda0b90b1a7a1c12bd9396d295ac288619595e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 03:31:53 GMT
ADD file:9583240ab6aa83a5f964dedeba18905486e879b1839d8329fc20f91cfccdd8d1 in / 
# Fri, 11 Dec 2020 03:32:06 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 11:15:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 11:17:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 11:20:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 11:32:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:018083dcdb1846644d37fb03ece4c9beb51dcb25f9851d01fc02f63c6fb143cc`  
		Last Modified: Fri, 11 Dec 2020 03:40:16 GMT  
		Size: 57.1 MB (57079148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0f8189a228fc57571454349d96c296688da37380e9b69091c6bee4d5f29315`  
		Last Modified: Thu, 17 Dec 2020 13:31:15 GMT  
		Size: 8.4 MB (8363474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765c21425572bad2d7f45674f0aca68f65a0064c986d32df2a8bfa1a71486b9f`  
		Last Modified: Thu, 17 Dec 2020 13:31:15 GMT  
		Size: 11.4 MB (11421266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b746c36884ebbc3753c6b143c63c5253980af55ae64b0699e6254c39ef8cac`  
		Last Modified: Thu, 17 Dec 2020 13:32:37 GMT  
		Size: 58.1 MB (58121475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42418b22b1d1f07d78a5b2361984048835818c9ef994dcb308995e0bc5a95654`  
		Last Modified: Thu, 17 Dec 2020 13:36:57 GMT  
		Size: 336.4 MB (336386058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:04d172a167bd9f62b93baf88e4dd279c31c713dd2c54ed050cf1ebacb0b98226
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.5 MB (431536231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aecaccf0e2f2f59b5eb754a4e6345f1ef7c130fed3ec48cfee7ecb39db19857`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:11:03 GMT
ADD file:74a0f68651d74636caec45b24b97289c444300a4e20ead2e9dd4ecad9a89b149 in / 
# Fri, 11 Dec 2020 02:11:10 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 11:07:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 11:07:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 11:08:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 11:11:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8c1102ca26cfeafe4e6f6b885fc1f8b1c19daafd157e556c9eb528d215f3ec2a`  
		Last Modified: Fri, 11 Dec 2020 02:16:10 GMT  
		Size: 51.7 MB (51656809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12f7e9486693eeeb90ca681816ec85fe5b3711fecfa8135127df223787ae321`  
		Last Modified: Thu, 17 Dec 2020 11:45:01 GMT  
		Size: 7.6 MB (7583470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3570bdaa2dbab5cd55b00748ab7c276c7f1644555be788bccaa538f9ee606a6`  
		Last Modified: Thu, 17 Dec 2020 11:45:01 GMT  
		Size: 10.5 MB (10525427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07678dfd6cd3af2aa29333f3da97482a64670de63bcfb4f2a8331a63a7555ddd`  
		Last Modified: Thu, 17 Dec 2020 11:45:18 GMT  
		Size: 53.3 MB (53325030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15d298bf4b9f51b97aeb82302cb786daa146b78bb37f63512befb103990dc80`  
		Last Modified: Thu, 17 Dec 2020 11:46:08 GMT  
		Size: 308.4 MB (308445495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
