## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:6fc68118810ba802a76712f55deef44533d455c3c9030e116e6db6264a54fbfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
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
$ docker pull buildpack-deps@sha256:4a8c2141db6cdfc0f5ad185c9adf1ff7832e858f941bcbc7700ea739d5be19a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344563712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77b122b42bf51251ba013be3241f93d29207f7bd3edfc3369abcf5a3f70900d3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:46:33 GMT
ADD file:168af20819ee8d7bc6ca3fd35873fe0b65f567f6fc4763ae2fed655e04826ef6 in / 
# Tue, 02 May 2023 23:46:33 GMT
CMD ["bash"]
# Wed, 03 May 2023 19:56:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 19:56:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 19:57:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:879480f6969a02afb639ba9b35bc2df992fec064538a2e8af5e14cf6b6fbeac3`  
		Last Modified: Tue, 02 May 2023 23:49:26 GMT  
		Size: 49.3 MB (49299247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd0eff3468a08b4cdf12f032ff78080b7173e0fe025644e187e4ce067d8cec4`  
		Last Modified: Wed, 03 May 2023 20:12:04 GMT  
		Size: 20.2 MB (20242385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa4b98d8b24de05dde098374b8e4720da9febf2a711f42a5ab448f355d63ef2`  
		Last Modified: Wed, 03 May 2023 20:12:21 GMT  
		Size: 64.1 MB (64104353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d4a4591553a674af4ef1154265f88858142bef461b8f90d557c575bf541563`  
		Last Modified: Wed, 03 May 2023 20:12:54 GMT  
		Size: 210.9 MB (210917727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ad3061da1212449a59b43d847a36d5e5b7e837fb8f42356739f86ecc7902775b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.3 MB (312288099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09050fbcbba8e87c5c73b838649be2ab48399875e17bbda63b1f22aa1e844aaf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 22:48:29 GMT
ADD file:1ecd266ebf23430d2ea2417b92ebee6029d940fbe99297183c4f811e24fdffb7 in / 
# Tue, 02 May 2023 22:48:32 GMT
CMD ["bash"]
# Tue, 02 May 2023 22:54:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 22:55:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 22:57:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cbca433c216350213a8b219e118cb55f422acfc53f49c76c44e044b42a5c0aa6`  
		Last Modified: Tue, 02 May 2023 22:50:27 GMT  
		Size: 47.2 MB (47167199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66d6e362e78baa664a585ad9ce74e92a9cd5b5324a686fbee141b57914ff008`  
		Last Modified: Tue, 02 May 2023 23:02:51 GMT  
		Size: 19.3 MB (19333871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7473034563d35f714ff8a45d3cffb6212ffecfb9c56b62a5ec6362567926f5`  
		Last Modified: Tue, 02 May 2023 23:03:11 GMT  
		Size: 61.5 MB (61548113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c829dc10de7fc2162995e0aa311c5250185e2983dc07a575bb6fbd623f4fd0c`  
		Last Modified: Tue, 02 May 2023 23:03:46 GMT  
		Size: 184.2 MB (184238916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:44edf8f678302510c459b3a9c3cd953b4b4f1f9f9379eaedfd47efd34ee2322f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.2 MB (304194726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68cfbdb2a81af057ea1a70140227c4197f31f0be7f707a48ddb28a3db0792b2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:10 GMT
ADD file:aa1c08333544c05fc5317d775ee99af7479c6fa5f35b74652f6126a7a5099958 in / 
# Tue, 11 Apr 2023 23:59:11 GMT
CMD ["bash"]
# Tue, 02 May 2023 22:57:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 22:58:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:00:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:81b1dd69f2a38ad14b0919ab9c395aafeb137158539ab6531ac5743690a0ebb7`  
		Last Modified: Wed, 12 Apr 2023 00:02:26 GMT  
		Size: 45.9 MB (45883114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc728032b22ec228489b2369f28a34e938fe54c39f4225a5368b0cc8da4e2e8`  
		Last Modified: Tue, 02 May 2023 23:34:21 GMT  
		Size: 18.6 MB (18602071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94a58ca5ea9331f28cd3dc05bb9d4a096adbe07cb2b9dc5b999ef426d1a51e5`  
		Last Modified: Tue, 02 May 2023 23:34:44 GMT  
		Size: 59.2 MB (59248070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720df57ab935b154eb0db730d28c635895f9229edb8792bb1ae2d9509a5fa26b`  
		Last Modified: Tue, 02 May 2023 23:35:28 GMT  
		Size: 180.5 MB (180461471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:41e78c1d81b534a5d4c9df2987dbeb5c9d47b8c1e858b35aa364a2df76b5cccc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.7 MB (335695600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2354f944dc0655ed6169c48f42201ae1660a29026a78dc34c65073d1508a2214`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:22:25 GMT
ADD file:1af23b8894efa507a47bf873cf69ecaa5ea13b618cae85b8c46125af6399b4fb in / 
# Wed, 03 May 2023 00:22:26 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:19:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:19:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:20:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:15c964cdaf05fdeddcf9bddd79eba05f71f2859fee9c193ba5d19a237f7fb92e`  
		Last Modified: Wed, 03 May 2023 00:25:01 GMT  
		Size: 49.3 MB (49345335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd2bfca96f059705a95bd29801b5c141a373826be0a739310df1a330c3a4134`  
		Last Modified: Wed, 03 May 2023 17:36:08 GMT  
		Size: 20.0 MB (20039445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778cd36edb73016f3ce8597f8a5ef1f79eb887ddec7f86d5b9accd80346edb15`  
		Last Modified: Wed, 03 May 2023 17:36:22 GMT  
		Size: 64.0 MB (63982020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e4ae666f1462af10fe15c06958b2e979fb104dfad6428c1cf8408bfa25d52f8`  
		Last Modified: Wed, 03 May 2023 17:36:50 GMT  
		Size: 202.3 MB (202328800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:df17c62fa74fe7be652661feb4e910b630a494edb48cca4cbdd2d086e8509bf0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.7 MB (353689778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1659417ac8936abfe4f12cde518b2232f6a6a20a09a709c9c602ebc310ea62a6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:38:30 GMT
ADD file:7718865253a3489583d40f8c7a7beede0c20cebbab68bb3e97ad2e84082afcb7 in / 
# Wed, 12 Apr 2023 00:38:30 GMT
CMD ["bash"]
# Tue, 02 May 2023 23:38:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:39:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:41:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a4ce9e81f634822e5166ef3eef875a4140795ac18afe0391433d72c7865bf67b`  
		Last Modified: Wed, 12 Apr 2023 00:41:43 GMT  
		Size: 50.3 MB (50317977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b53a8ccb81ed2e84af88da981d1e4dc7ac411f271a4e8a7f3122eb7715b96a8a`  
		Last Modified: Tue, 02 May 2023 23:53:39 GMT  
		Size: 20.8 MB (20819554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adaab9e9b74f7059f308d197924d72cb7b9630fdb08961bae1044f9e9a1dab60`  
		Last Modified: Tue, 02 May 2023 23:54:01 GMT  
		Size: 66.0 MB (65960854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0de03155290d7939b0c70714e934e8b67692fe9331d683aee54e5f16e56937`  
		Last Modified: Tue, 02 May 2023 23:54:48 GMT  
		Size: 216.6 MB (216591393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:6cf9bc801d943e49588bd4f8f9a3e146565301c13b162980acd3bc636493b17f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328363586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa82721571fa0a4bc6991369588465e9f8a1ece6c9e2739153e25dbdca82271`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:08:16 GMT
ADD file:6a525220124da7146a3c356cc57678f3b8d7c6e9299febaaebd5b5a005f1325c in / 
# Wed, 12 Apr 2023 00:08:21 GMT
CMD ["bash"]
# Tue, 02 May 2023 23:08:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:10:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:17:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b6bdb9410f81554043d19e5ae83249eaa10ffe038db54932946c7d9eaccc8b96`  
		Last Modified: Wed, 12 Apr 2023 00:15:35 GMT  
		Size: 49.3 MB (49299322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d31f3eabe7fc60bb418c1f16a58905f2b69b1006f3c39c64cb0010b7ef8b92`  
		Last Modified: Tue, 02 May 2023 23:35:56 GMT  
		Size: 19.6 MB (19555025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ffb429bc95d286b0317eae289b0c001399e7c388e936d016df785b157abf902`  
		Last Modified: Tue, 02 May 2023 23:36:46 GMT  
		Size: 62.9 MB (62939831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91426807255ed15d325140417f52b60b65f7f625be380803164f87a4cfd175bf`  
		Last Modified: Tue, 02 May 2023 23:38:53 GMT  
		Size: 196.6 MB (196569408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a3e1ab1ceed101797bf7da8ec33e1c3dfb1cbc8c705d0daab577db6afd56e504
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.5 MB (366471871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2198fd60691d927ac02caa46589850b3d74e83e7f24df3f6859919942e7af383`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:07:22 GMT
ADD file:b747fc06f7ee1d3e19fc9cf3aa83e6ab4caa056a72d230caf616e67849bfe112 in / 
# Wed, 12 Apr 2023 00:07:25 GMT
CMD ["bash"]
# Tue, 02 May 2023 23:17:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:18:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:23:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8314f03b76ec928732612641a4f8420e3c4c25719b48503230bf6c03979aeb2e`  
		Last Modified: Wed, 12 Apr 2023 00:11:50 GMT  
		Size: 53.3 MB (53299984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c68dac52e65bcdd27d7d79356306767e30e234ee8c68a7d70f07c6cfb448d5b`  
		Last Modified: Wed, 03 May 2023 00:11:13 GMT  
		Size: 21.6 MB (21579638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1d95ac0c246fe46bf2c9a6bf4f2994b4bfa6a31424e34f5d0fff8b8f85dc5b`  
		Last Modified: Wed, 03 May 2023 00:11:40 GMT  
		Size: 69.6 MB (69558686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690804e853943a7df1c107dfa3280cf6afd592a0b8c44c6ce12bf84ead9a884d`  
		Last Modified: Wed, 03 May 2023 00:12:40 GMT  
		Size: 222.0 MB (222033563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:994d3db211a48bed77df6b8747618f78b70c07f570a7e52e5a1063889ac325df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.6 MB (319597689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb4c49624a5ce704b1caf51355317daafa3bf9711e2a71863c516e3c09dc086d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:19 GMT
ADD file:5d2b35b45a0f23e2f2e93f9c311eb34a92e4591ea27979236d801e512d44cb85 in / 
# Tue, 11 Apr 2023 23:59:31 GMT
CMD ["bash"]
# Wed, 03 May 2023 03:05:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 03:06:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 03:07:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8a09cd2374da8355612e7d4c91d55107a3f089816ae52b2c91b9e08e6a895ab1`  
		Last Modified: Wed, 12 Apr 2023 00:04:39 GMT  
		Size: 47.7 MB (47670407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2923010ed47ed4a1aef7c5ba63bde7a5e752417572d5233c833ab2a793a7852d`  
		Last Modified: Wed, 03 May 2023 03:33:07 GMT  
		Size: 19.7 MB (19733881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb415e6385094977215a7cef468d3e6ed5ac5239dc3f96cff46024956339c54`  
		Last Modified: Wed, 03 May 2023 03:33:20 GMT  
		Size: 63.1 MB (63101264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab98378e0e35e904cb3f57bc44bfb14b8b2e31d929cfbea415cf1d89370026c4`  
		Last Modified: Wed, 03 May 2023 03:33:48 GMT  
		Size: 189.1 MB (189092137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
