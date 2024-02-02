## `buildpack-deps:focal`

```console
$ docker pull buildpack-deps@sha256:d1ef0088e5f7297d40b4a6e4e85f19ed45afca0c1eef50a298acf4b5c34abe70
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
$ docker pull buildpack-deps@sha256:ea9b8e0f79aea918edd8670e1faa166973535e5378adda8b648066c02949dd64
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246414818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ff53dba2ff548bba6d1586e7d8a0010822da590cfd6fd6102d7a683af0e5cd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:13:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 01:39:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 01:42:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcef08e556c11a34b8d8fb3480bb58c85880c44c9dbb4c7a24548fcd7bd436b6`  
		Last Modified: Sat, 16 Dec 2023 11:19:10 GMT  
		Size: 11.1 MB (11129595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1c216d731daa0988a1cc7878764acfaf7c52a2181601dfb6386930facdce08`  
		Last Modified: Wed, 17 Jan 2024 02:05:11 GMT  
		Size: 60.9 MB (60905172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce23f4f67a4e39c1cc056d0705787d07d7fe9db6c3d13c55ec8f09f5656fff5`  
		Last Modified: Wed, 17 Jan 2024 02:05:39 GMT  
		Size: 145.8 MB (145796027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:06bbef973feb92fd645256eccf79d4ad83b2493d1308ea6fbf33b93175f2e28d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (211983832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6baa604c8db1d66316eb9ef3725889845c2fe68d2f5deb855a0ba4a9712ab9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:02:57 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:02:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:03:00 GMT
ADD file:06dcbc8a8b50c1189965851d9f1a29fe046ec9589e6e850865a8608d0a59ad50 in / 
# Tue, 23 Jan 2024 13:03:00 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 23:50:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 23:51:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 23:54:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:93eb4c358a70eb4dc4f48209013d08987bf6c1a559df5adba7fc713ba9fc0bf7`  
		Last Modified: Thu, 25 Jan 2024 21:04:32 GMT  
		Size: 24.6 MB (24602341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44b202c69953fc401f61bc6b1baee27abf4816c8580b13ed3f520ffa63cc29b`  
		Last Modified: Fri, 02 Feb 2024 00:09:29 GMT  
		Size: 9.6 MB (9606042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996dff6ef7bf273a917daf5f26fdf3ce2a3437a1b88a12d438339cad825fc1a9`  
		Last Modified: Fri, 02 Feb 2024 00:09:47 GMT  
		Size: 55.8 MB (55824821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5faf7a65783ebc0fc71fce330a35048ccfe09acb142df1bcb3449c51e4cc02`  
		Last Modified: Fri, 02 Feb 2024 00:10:15 GMT  
		Size: 122.0 MB (121950628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c8e19ff404d986ed70c9a37728378491351545b1f63dc600b52b67cc7fc56020
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (235999243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c3577f0f40635ec54c63ace74aa03b9382b74bf2815447d7297fbc2da3158b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:49:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:50:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:53:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:beb9e0b551f10db0eea20b2fc47ad9cb3a7f0f338845eeb162a82fec32843b1a`  
		Last Modified: Wed, 24 Jan 2024 18:44:36 GMT  
		Size: 27.2 MB (27205060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6679ad14e1203644b9acf842ad02c1eb97402c388d955eca7e37c7edb4a24ba9`  
		Last Modified: Fri, 02 Feb 2024 01:07:59 GMT  
		Size: 11.0 MB (10985306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb28a40b969d9c86cd7dfd800a5a944b208ada3cd9f8bdef6303362dc2e51a1`  
		Last Modified: Fri, 02 Feb 2024 01:08:15 GMT  
		Size: 61.0 MB (61012320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df8ce900192481f0da30214cf0dbf57e840b8842dc245f68513f6afd79e3157`  
		Last Modified: Fri, 02 Feb 2024 01:08:40 GMT  
		Size: 136.8 MB (136796557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9d039d78d35643cabe5b2df1832eb9d609fab64344c8d88ea7e8097f4ae67ab8
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.5 MB (269529129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c18eda4f812d2fd63ac182480c6a65f39915667de6ffa1ebba948988d9cade`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 12:54:35 GMT
ARG RELEASE
# Tue, 23 Jan 2024 12:54:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 12:54:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 12:54:35 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 12:54:38 GMT
ADD file:96f44a86185939ee5de23552dc064d300ba16f7f31dc2d5ea1081d99cb0ecc9f in / 
# Tue, 23 Jan 2024 12:54:39 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:58:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:00:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:05:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:235f35baf74b5944d6dbafa8498b4e2ba58703a9be506a8a9008f01bb6d54cff`  
		Last Modified: Fri, 02 Feb 2024 01:44:37 GMT  
		Size: 33.3 MB (33316035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b958220f1a42c95910cc6699db54892ac8d4332c6d038f58f4eccc0c35c1683e`  
		Last Modified: Fri, 02 Feb 2024 02:32:11 GMT  
		Size: 12.9 MB (12941345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c2154c6f7dea8a1736513627d712be0826012c99ae1779a8fc56e36ec1656f`  
		Last Modified: Fri, 02 Feb 2024 02:32:32 GMT  
		Size: 69.7 MB (69653324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e15e3a2cd5f3a2c53f73d28f854d26d6cce5cf8909a67aa711941c4e12f89d`  
		Last Modified: Fri, 02 Feb 2024 02:33:08 GMT  
		Size: 153.6 MB (153618425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ce25d4b95513e23adef005c7fd9686de47217809ddee0313e8cce3f0fdcaa2a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226574839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d505195f4353a80806333a66e0853c2c57162ae0f1dab9d7a40034596c00e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:36 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:36 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:38 GMT
ADD file:9688c7fb864a2f858b61b1962f9c2236540bc2d74ee75df78412ca5655b0c9da in / 
# Tue, 23 Jan 2024 13:01:39 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:04:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:06:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:09:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a682f62754950fac591750632706a670049f0e9f7ee2bcc2b26407d9c264ed76`  
		Last Modified: Fri, 02 Feb 2024 01:33:16 GMT  
		Size: 27.0 MB (27016265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c18276081750da11b1262393e76e48599e609d7e11bf29d57d0729f853cdce`  
		Last Modified: Fri, 02 Feb 2024 01:33:14 GMT  
		Size: 10.7 MB (10692261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ddc6215f51639b9e751c9ce21a6eafd69dfe8cb324818572b591e3eae0d4fd`  
		Last Modified: Fri, 02 Feb 2024 01:33:32 GMT  
		Size: 60.3 MB (60315331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84689abf9543da36ae4ac6e39a52cbc52c219425fe0252a7eb0d2f78b652c9c4`  
		Last Modified: Fri, 02 Feb 2024 01:33:54 GMT  
		Size: 128.6 MB (128550982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
