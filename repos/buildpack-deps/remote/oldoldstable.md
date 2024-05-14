## `buildpack-deps:oldoldstable`

```console
$ docker pull buildpack-deps@sha256:7e86cd95a38a9581e5698e61592c7ce5ce09267bae83eaf98d8ef81e3bccce29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldoldstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7f6c766d2340071d06e69ddab69dde8f348118050930de690cd448c4d66da1cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312095112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d19d1123dc98839be934851144435b5375e3c1c28cc877de748cf1cc3ecf3250`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:28:36 GMT
ADD file:9062f3516bb9d149bc29e8f3ee94806152277d05a3f2ee0ba7bc2040d8bfc8d5 in / 
# Tue, 14 May 2024 01:28:37 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:57:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:57:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:59:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:673c873103ec067ad3ce1763a9ed20efd4591771bc605ceede174e83eb25ee0d`  
		Last Modified: Tue, 14 May 2024 01:33:29 GMT  
		Size: 50.7 MB (50656909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44f61bacd5268a0f7dbd851e763d6ee101c21d0af21e649584357d4443cd709`  
		Last Modified: Tue, 14 May 2024 03:06:14 GMT  
		Size: 17.6 MB (17586437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e7d6cb6a5235443faadc8d241ebb270739fd828ca9f0b78c63a1e7f36f8405`  
		Last Modified: Tue, 14 May 2024 03:06:29 GMT  
		Size: 51.9 MB (51894320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79bc40752dd2cf0f18dcf07e73c1c85269734230ce7b22f18f4a4d120f54e608`  
		Last Modified: Tue, 14 May 2024 03:07:00 GMT  
		Size: 192.0 MB (191957446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fd45bff6eb237ad90e784e14ec06049261d4365c528dde1834a579d2c03c5e34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.9 MB (277927151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57d1e87724e2dde2424db300f85e44d2d955b8967394cbcc691585a1fb9ca1f8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:09:12 GMT
ADD file:a05edfdd56e92b1814d8e812ef81e814accd29893888392076dbc26b33b5ae41 in / 
# Tue, 14 May 2024 01:09:13 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:39:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:39:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:41:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:66d6e1b7bddcb1c893c2c3e9b1ac8f5fca7c047037ed836079c97c9a917cd989`  
		Last Modified: Tue, 14 May 2024 01:13:47 GMT  
		Size: 46.1 MB (46129793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e36c6c43e23d017283e609c78ad3425681f38a7cec50832f329aebf9f45a45`  
		Last Modified: Tue, 14 May 2024 01:49:06 GMT  
		Size: 16.2 MB (16217024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780d070dbdc44447a3c019b1076d14827afec1e3d9f53f0941c341dde2f5b674`  
		Last Modified: Tue, 14 May 2024 01:49:23 GMT  
		Size: 47.4 MB (47410306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeab1a68b064abb317c5afc7a68fdc8b46b5c9f37a1fad3e3d9664777a761c11`  
		Last Modified: Tue, 14 May 2024 01:49:55 GMT  
		Size: 168.2 MB (168170028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d157bf1470311d32cc604b0e010ba59e4960c589bd98de96768a4c1adefa711f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.7 MB (302674958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ded790d0b118beef12ba72b235b7995264e49bd3c5b6f45304b64d76c0cb9f5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:40:02 GMT
ADD file:da8c3a2d966487a4e1bc0646a771d18df585d75dc24f095a1aaa762ce0841747 in / 
# Tue, 14 May 2024 00:40:02 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:47:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:47:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:48:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0a8090f4fec79fd213192f5f5c31c70546878a20b6c7ca023ff9001fb788f828`  
		Last Modified: Tue, 14 May 2024 00:43:49 GMT  
		Size: 49.5 MB (49453094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e540eb6c9fa042a5d3f1166ea6b4d3806d751dcc600baff113c7e2b711719d`  
		Last Modified: Tue, 14 May 2024 01:54:42 GMT  
		Size: 17.5 MB (17456998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334249e7f4554ad45c3998bd6a23aa8d7ecc535422903784fb251e6345d36f9a`  
		Last Modified: Tue, 14 May 2024 01:54:57 GMT  
		Size: 52.2 MB (52230498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019b2124bd151541dda5ef935a2883293321b124587270f4c0c28495c25a1ca4`  
		Last Modified: Tue, 14 May 2024 01:55:22 GMT  
		Size: 183.5 MB (183534368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:58a54df267489446037d570f72d8bda8e3e0d5f428fe1ebeff88aa70eff3108d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.5 MB (321501958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1535153c37f63f8995d6256760094273ed7097096a2cdb760b505208edbb966`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:47:45 GMT
ADD file:5e59addfe8663b7c16cce40874c2a3c8601e20e80f5a0897c86b64ba463c10e9 in / 
# Tue, 14 May 2024 00:47:45 GMT
CMD ["bash"]
# Tue, 14 May 2024 09:05:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 09:05:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 09:07:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1a892f56e4b10aaecbb51b3219d90bd0d8a1e955acd0624a6ef27ed086ba168c`  
		Last Modified: Tue, 14 May 2024 00:53:06 GMT  
		Size: 51.4 MB (51419713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df672f2f18886bf928d6070d3311b71a33f94ce9708b67ade8e00ea0ec6cf25c`  
		Last Modified: Tue, 14 May 2024 09:15:53 GMT  
		Size: 18.1 MB (18098325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20019971ec9aacb9b7c64eb51f32f35360675176e10007625a27813b8a8cd124`  
		Last Modified: Tue, 14 May 2024 09:16:13 GMT  
		Size: 53.5 MB (53491794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a3d64f2a6cfb08d0e101f8b79c83a6035104799f3de7058346a363aa6a09f3`  
		Last Modified: Tue, 14 May 2024 09:16:59 GMT  
		Size: 198.5 MB (198492126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
