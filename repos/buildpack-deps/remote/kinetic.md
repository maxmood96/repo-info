## `buildpack-deps:kinetic`

```console
$ docker pull buildpack-deps@sha256:c6601b926e80085d6dccb999262c23c0a428bd0e7ad37ead519a6b803ba53fe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:kinetic` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0b34490510c29fa74353ade9e5d90182d82346a3246992c1ae54ee125ccb8ed4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262660283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1957599663a9fb73a6c45227894308eee2990917cb02b30a6fa23a66f56f5b74`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:23:07 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:23:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:23:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:23:07 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 28 Jun 2023 08:23:09 GMT
ADD file:50094673f74cf3945ac21e23bb84d41d3516bc1ac90ebf7f17379288c33c17b2 in / 
# Wed, 28 Jun 2023 08:23:09 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 03:43:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:44:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:46:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e4ae0f456d5b5ed53c0d0f67cd1948207060810837f2b15dcdf5bd97bbceb300`  
		Last Modified: Tue, 04 Jul 2023 03:56:47 GMT  
		Size: 27.5 MB (27488903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f7fd2e9f809d0b31bf96fde0b09fb68493e5499b9a4dae5f3dfc0a0ed0b7ce`  
		Last Modified: Tue, 04 Jul 2023 03:56:46 GMT  
		Size: 14.2 MB (14189206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e60069d839c80c438523487b52eb9073ef4a8fd32af5b8a6dfe8480792c8a57`  
		Last Modified: Tue, 04 Jul 2023 03:57:02 GMT  
		Size: 39.8 MB (39825912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fbc9753f2da447aadff4044bd763bb11c8f004fa9ab7cccc88048ddacb264aa`  
		Last Modified: Tue, 04 Jul 2023 03:57:35 GMT  
		Size: 181.2 MB (181156262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f78e0e5d6707a04956b352cf8fb6883cb9ce87a31fa7befcfb88144d5a452357
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.6 MB (225624695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3685089673bda68c20b3c886018604ff1e74c04bdd8989f7fca96ba999fab182`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:50:23 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:50:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:50:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:50:23 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 28 Jun 2023 08:50:29 GMT
ADD file:1c3ce20a4b19d1c7779aa47e9799d2887ac4d142bb495eb0bdca08ff1c8fd106 in / 
# Wed, 28 Jun 2023 08:50:30 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 06:09:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:09:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:12:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b2a8550df843bc39f9334e8b8d8524b0e0abe390674577c839e53aa1c6afb06`  
		Last Modified: Tue, 04 Jul 2023 06:24:17 GMT  
		Size: 25.9 MB (25912764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eef66710f99af0d044d772f07b2eaf0c9da9559b1b10f9da05b104e86fb12a7`  
		Last Modified: Tue, 04 Jul 2023 06:24:15 GMT  
		Size: 13.1 MB (13141364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f28d29b0c8e6083c797c1ed79183346245421c696c0b8365d1b4027561dc13e`  
		Last Modified: Tue, 04 Jul 2023 06:24:34 GMT  
		Size: 42.9 MB (42939065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f417099045b65e1689b25195d9a5ca52532043778ba15ae89200da7da00efea`  
		Last Modified: Tue, 04 Jul 2023 06:25:06 GMT  
		Size: 143.6 MB (143631502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:fe77e6e21c64105552429c5273332cc2e769d79bfbf74c26a92cb9cbec3d2d7a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 MB (250423813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b20fadd9a6936babea6d9dafc67064e118c913a7342ca0cfd0a522d03de2fd4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:16:50 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:16:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:16:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:16:51 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 28 Jun 2023 09:16:58 GMT
ADD file:a41ad4058e77a6f1ee9800af03cf13403d5d844e876246ba55c4ceb2106b6d5f in / 
# Wed, 28 Jun 2023 09:16:59 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 06:11:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:12:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:15:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c5528eed9908e3645e0eff6666ba300d135b6ff9801f5ae1cc49bb06a3f29fcf`  
		Last Modified: Tue, 04 Jul 2023 06:25:40 GMT  
		Size: 26.7 MB (26730941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8785a3c2b399ffc53927bd8e5eea56d2819ea053d0d78910ae32f88d2f9ec680`  
		Last Modified: Tue, 04 Jul 2023 06:25:37 GMT  
		Size: 13.7 MB (13727615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af381f44d3219c7eab50c1af5c7bf36233fa1a694569f8a29e1be2e7d55cd37`  
		Last Modified: Tue, 04 Jul 2023 06:25:53 GMT  
		Size: 39.6 MB (39636653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1160a4dcea08cb2cc3585710f41a7615c6d7bc8668f20d79b85391142f1910b`  
		Last Modified: Tue, 04 Jul 2023 06:26:18 GMT  
		Size: 170.3 MB (170328604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:015d6829eda0af44d4186f2cf2c0b6726a23f5b9574881a0b21e75e419f6f601
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285537534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41cee9ff03f244bfd65fcb2ce00a37aa729796de6aee6a06366fecbcef36eb6c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:04:09 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:04:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:04:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:04:09 GMT
LABEL org.opencontainers.image.version=22.10
# Wed, 28 Jun 2023 09:04:12 GMT
ADD file:8c5e727842a7ff4d34b93a1ee45f14532c9b03594ad53400240e6f0f4b99b390 in / 
# Wed, 28 Jun 2023 09:04:12 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 04:09:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:10:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:19:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c4c2a73576db8e1d5b385d67fe412db5e6cd146167f6c5fa6153b87f17abfc3d`  
		Last Modified: Tue, 04 Jul 2023 04:44:10 GMT  
		Size: 32.1 MB (32102426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297facc34b9d65726d36999c1b9378836014f1dbb15725b2be4359b50bec9d21`  
		Last Modified: Tue, 04 Jul 2023 04:44:07 GMT  
		Size: 16.2 MB (16234063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9cb9fc38b5a1da1252223c33aa1381def6fb94284f39b6c1d6025d92bf99478`  
		Last Modified: Tue, 04 Jul 2023 04:44:34 GMT  
		Size: 44.2 MB (44231612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd62a63c22d9416c3b46dccf9da4cb3234f7549206282332be98c282450d9c7d`  
		Last Modified: Tue, 04 Jul 2023 04:45:31 GMT  
		Size: 193.0 MB (192969433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b122cbd93966173e324bed10b46003a1499a6fa1f099086cb4514d10db4dd748
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233062462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2471e1864b14d7637a2a024b934f1ef936d7f8d40a147e9141f5da52deafe111`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:10:49 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:10:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:10:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:10:49 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 05 Jun 2023 17:10:51 GMT
ADD file:2390e4c5ac4f862cf5fb266c70962a01f271fa692b74af886f18911482025825 in / 
# Mon, 05 Jun 2023 17:10:51 GMT
CMD ["/bin/bash"]
# Sat, 17 Jun 2023 09:50:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 17 Jun 2023 09:50:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 17 Jun 2023 09:52:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:45d37589c642f2585803ed2ba24d2b897920c885c7a913bb399e12a2410d5503`  
		Last Modified: Sat, 17 Jun 2023 10:01:25 GMT  
		Size: 26.0 MB (26034488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10ce8336984e795efd05d14a13611a92ef77b199d749859036bd37fbbf18040`  
		Last Modified: Sat, 17 Jun 2023 10:01:24 GMT  
		Size: 14.3 MB (14344562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f89ec5257613dfb7e6ac3731cf008ae93397126d7d27b80d7d9e63428331cd`  
		Last Modified: Sat, 17 Jun 2023 10:01:38 GMT  
		Size: 39.7 MB (39678007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5e09768f30946e642c4ccc2ba209f76e0f517c84c6302d60380391c1fb4c86`  
		Last Modified: Sat, 17 Jun 2023 10:02:02 GMT  
		Size: 153.0 MB (153005405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
