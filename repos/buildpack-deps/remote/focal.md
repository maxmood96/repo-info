## `buildpack-deps:focal`

```console
$ docker pull buildpack-deps@sha256:e08c02e1b2e93aaf286f79a8ac22e2408a11f6d07f019726513a1fb908df9db9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:focal` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:43d3c37b0b77687dac2c85f36cc78a8d7ba9d75699df4a15837516767442e88d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245767248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28d3054fd40eb8bac73c86d57a0840bb78a6f10e352fb09aead9f07e2fa02613`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:00:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:00:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:03:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:63e9bbe323274e77e58d77c6ab6802d247458f784222fbb07a2556d6ec74ee05`  
		Last Modified: Sat, 17 Feb 2024 02:07:52 GMT  
		Size: 28.6 MB (28584317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85a62b2979b092f4c9b7a13eb5a5bf3d6639092b1e3200a93e448ce02a751a7`  
		Last Modified: Wed, 06 Mar 2024 04:14:22 GMT  
		Size: 11.1 MB (11131163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b4d70c07f54619a9053b20d9a7e6bdb6166b2c0fc92ac0d16c2fd1cd08e3c8a`  
		Last Modified: Wed, 06 Mar 2024 04:14:41 GMT  
		Size: 60.9 MB (60905037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786495634ea9b39ce8af363dc672e02cf79588e0ad80bcb2a1e8973f4a188ebc`  
		Last Modified: Wed, 06 Mar 2024 04:15:09 GMT  
		Size: 145.1 MB (145146731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:10b37574baeaa2ffca16861be219ec66a0fbc2c0bde9296bdd71b26ba9a1e994
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (212024419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babf5a42015560ee03688d95bf4505562e6d4635fd18553d1a7a61993eb0220f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:40 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:52:51 GMT
ADD file:d5544f56cf9b2897ccff2833db59b6aa51af25a2aa34f4e000e12396d6b18f30 in / 
# Wed, 10 Apr 2024 18:52:52 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 02:15:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:15:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:17:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:415e9bbd0769b29f08b5782353a86f2e8e29ba55d4d4d1e7fe999652679005c5`  
		Last Modified: Tue, 16 Apr 2024 01:53:17 GMT  
		Size: 24.6 MB (24602624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb5e0f9a8123efc9edf4ed4a3a071bda75e2e0678a53d646c8e6c0b3ff6df70`  
		Last Modified: Tue, 16 Apr 2024 02:31:55 GMT  
		Size: 9.6 MB (9604241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe0762329df1909a1314fc970b65988a47ae49a3d6eb8bace711b09364313eb`  
		Last Modified: Tue, 16 Apr 2024 02:32:13 GMT  
		Size: 55.9 MB (55867415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a2bf1952767aaad32e467fac989f475006f869982d4a123f51e8935062b0e9`  
		Last Modified: Tue, 16 Apr 2024 02:32:39 GMT  
		Size: 122.0 MB (121950139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:982651ec5ccd639e43b545d4e20fd6c3b78acb745cd05f0baf2fa452b29fe0d2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (236046537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538d75eba8e8234c343621c5f6dd3a8aa2ad03f408a90ef799e51723029e57c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 01:50:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 01:51:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 01:55:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7688b82426696e44f961201d38c484dd5279eb88689c7eadb2100dd075e697f8`  
		Last Modified: Fri, 12 Apr 2024 07:29:54 GMT  
		Size: 27.2 MB (27204984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f9e24831b35659f11dda56ed6229046a1aa11ed7d76373cb21a01b415fc51a`  
		Last Modified: Tue, 16 Apr 2024 02:10:29 GMT  
		Size: 11.0 MB (10982960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d94608895359e7ebf7493231f818b215ada755a377c25d53dd41663616f2db`  
		Last Modified: Tue, 16 Apr 2024 02:10:47 GMT  
		Size: 61.0 MB (61048754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6558c02328f955bc619a713487360b291faee25655d680ccac9538c209fec57`  
		Last Modified: Tue, 16 Apr 2024 02:11:10 GMT  
		Size: 136.8 MB (136809839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:96bb2f8f2527fc3efebaca509e5f9cd2f1bceb793ff98312e57c1cff59eb2f42
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.5 MB (269527313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:833353366305082a68720d6ac0c74263ff046584cf1531b47e11e646132436a6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:04:56 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:04:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:04:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:04:56 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:04:59 GMT
ADD file:8efe37e124c3eb7c9e2b3ba1f33a019526490b9a49cbe8997abf72caf6bb7ece in / 
# Wed, 10 Apr 2024 19:04:59 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 02:57:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:05:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0c372adcddc32347cef56486050a9e3f15243cd4c6b2ef3b7de6d5d6f7bf9ef1`  
		Last Modified: Tue, 16 Apr 2024 02:49:17 GMT  
		Size: 33.3 MB (33315676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04712a59991e1b0784ad92727b7b6d6432a880ab5579b91ef637a0b3bb9a543f`  
		Last Modified: Tue, 16 Apr 2024 03:30:35 GMT  
		Size: 12.9 MB (12940665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3905c6570c57c33c32c7daea87d229ca9938b6522c9ff4819d25f56d45e2b289`  
		Last Modified: Tue, 16 Apr 2024 03:30:56 GMT  
		Size: 69.6 MB (69639882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60208895a163e9d4db4e67403f714d7d994c81eae73c72ac3036e02780e45434`  
		Last Modified: Tue, 16 Apr 2024 03:31:30 GMT  
		Size: 153.6 MB (153631090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:56f1b0e44973413035240e964584235a8e484e72049c19045538e7ca17124f0b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226578050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcb499ffba05ef5739dd98152e73295b1afbb9cc1473100b1cc0ded84e538fc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:51:34 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:51:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:51:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:51:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:51:38 GMT
ADD file:c91b061ad49bce1f6e2860bfe87ed2e94cc280b915289f041d2dd5ce3ef385ad in / 
# Wed, 10 Apr 2024 18:51:38 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 01:20:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 01:21:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 01:23:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d94fd945c36b3b9c768528b528e1b8e7d49b0c692243295ec499726809202c4e`  
		Last Modified: Tue, 16 Apr 2024 01:36:12 GMT  
		Size: 27.0 MB (27013490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea19c9f54da460d7cbfd01dc0e5e3b36dc8a0d80e21af8ecbed7f77edfe6352`  
		Last Modified: Tue, 16 Apr 2024 01:36:10 GMT  
		Size: 10.7 MB (10689984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bc8d13e1b2fb25e841a0aa68e79beee843b75348e8d56f1fc20400353084d8`  
		Last Modified: Tue, 16 Apr 2024 01:36:29 GMT  
		Size: 60.3 MB (60317983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7260fdade369a2c0ad704ea62defa0083ddce6c9b0c7c30ad11b9cd89d2a99c`  
		Last Modified: Tue, 16 Apr 2024 01:36:54 GMT  
		Size: 128.6 MB (128556593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
