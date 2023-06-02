## `buildpack-deps:lunar`

```console
$ docker pull buildpack-deps@sha256:906da9046aa70234a1c25c11c8f1a83e7f78a77a7bfda86f48eadfbb16e6c241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:lunar` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8a55ef42557b825d674a0f12878f480c9b74ac9acd1b0a46f33afa00d71a6d82
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 MB (268177303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3c2439ee2f86bb326c795fe540a0e948010326ac956a00dfb340c27768c7e5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 May 2023 09:16:59 GMT
ARG RELEASE
# Tue, 23 May 2023 09:16:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 May 2023 09:16:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 May 2023 09:16:59 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 23 May 2023 09:17:01 GMT
ADD file:6591237a72178b71d79f687b816ad23237fbef0bc3ec42332369d9e7bdaa04e4 in / 
# Tue, 23 May 2023 09:17:01 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 00:42:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:43:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:45:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9e4ea5938a80fb79461962ff5189dfe6a9611db20e7fd777d48e9c1fb890dd7d`  
		Last Modified: Fri, 02 Jun 2023 00:50:42 GMT  
		Size: 27.6 MB (27604778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c71826d6ef94eb72f39ead11e9bf5bffebf6621de6a623a7219ccbe084e7a9`  
		Last Modified: Fri, 02 Jun 2023 00:50:40 GMT  
		Size: 13.7 MB (13743419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b272b87751d403529d61b4fa7a58440e4c95528eb9ff983882453e8e7d2591`  
		Last Modified: Fri, 02 Jun 2023 00:50:57 GMT  
		Size: 44.3 MB (44346555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73dce92a4b1f87e0594c54aa422dd905c1c616ac4db9095159c1100752d990fe`  
		Last Modified: Fri, 02 Jun 2023 00:51:28 GMT  
		Size: 182.5 MB (182482551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:87d923f02b7142e2a78c0fa57fcee8555ca92d330e67de3e788393c29178a11f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.6 MB (232593143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a61166c3400c2dca20a5d8765812cb9f638090e8f8f1062c12a42d7025741d2d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 May 2023 08:33:12 GMT
ARG RELEASE
# Tue, 23 May 2023 08:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 May 2023 08:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 May 2023 08:33:12 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 23 May 2023 08:33:16 GMT
ADD file:eff76586a1ef817ec09adc4b06a3656dccdfa9eaa17e0580677ed3315d37067b in / 
# Tue, 23 May 2023 08:33:16 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:47:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:48:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:51:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e86bb05c5dbd58b5e8389e535f7991f8471422d2de083b44e2acfa1487cad3c1`  
		Last Modified: Thu, 01 Jun 2023 23:56:17 GMT  
		Size: 25.4 MB (25439673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8da934754d2097069a43e26adff9e2c241ab6b06b4448327d31f266b517a59`  
		Last Modified: Thu, 01 Jun 2023 23:56:16 GMT  
		Size: 12.7 MB (12663559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cafdfe4d281381f0fa72659c7125eaab81f01378af04c3b6d53411d71a39b04`  
		Last Modified: Thu, 01 Jun 2023 23:56:33 GMT  
		Size: 48.7 MB (48692331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234d75b0aa1c89b54f45a66c838a9e5edad70e8697c8bd558fce15c31bb3fe50`  
		Last Modified: Thu, 01 Jun 2023 23:57:01 GMT  
		Size: 145.8 MB (145797580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:132615ea1627542395bde3e487f6746ba57da78dceaf85b8775828105088d26e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.3 MB (258282349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d4edb7c30b26c2a7238114ab45fadf696648daa47647d9e58f1f9eaf24f097`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 May 2023 08:33:45 GMT
ARG RELEASE
# Tue, 23 May 2023 08:33:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 May 2023 08:33:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 May 2023 08:33:45 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 23 May 2023 08:33:47 GMT
ADD file:b2902a85ba60d642b00f2d7d7e4f56825749dca527e2d8d5e64d854c76ed28f0 in / 
# Tue, 23 May 2023 08:33:47 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:56:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:57:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:00:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:799351a2e050dcbccac2616755ae9631d97278ecebbd4db013e40b3a849439c5`  
		Last Modified: Fri, 02 Jun 2023 00:05:52 GMT  
		Size: 27.0 MB (27017966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f53223904f9116e3fca0e8c45abe0ddd4a8c43584afe7ad09b9406e2d26a91`  
		Last Modified: Fri, 02 Jun 2023 00:05:49 GMT  
		Size: 13.3 MB (13331051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8e19cbae0e39a2642e58e9a773ece1aac1b0cac4eb9eec6c8fd81b765ad2dd`  
		Last Modified: Fri, 02 Jun 2023 00:06:05 GMT  
		Size: 44.2 MB (44194052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2ac513a62a22e5c10ab763fe08d5825e5cb5ffcc5f64a6c53041e4cc9ad1a3`  
		Last Modified: Fri, 02 Jun 2023 00:06:30 GMT  
		Size: 173.7 MB (173739280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:cf70981edef6c48524b615c7b0039c55fc9303af3012d96e65accff7b3bb3502
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.2 MB (293195611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da7b226dc7c4322e8dd2f7839a97019df71a150a17df08d30d3afad9a1665c54`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 May 2023 08:36:49 GMT
ARG RELEASE
# Tue, 23 May 2023 08:36:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 May 2023 08:36:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 May 2023 08:36:50 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 23 May 2023 08:36:52 GMT
ADD file:d76035fa745d219f333adeb90e6eedc3b563dca64aa80c2fbe88d7389ba798d2 in / 
# Tue, 23 May 2023 08:36:53 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 00:07:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:08:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:14:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:949f734ad643dc041d0099be4f14b5d487e88ee4a4715547d536c0fb34f3d2a5`  
		Last Modified: Fri, 02 Jun 2023 00:24:59 GMT  
		Size: 32.0 MB (31997157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94c6acbf105653fae1ce0dd770ebaecddb43ed456d1efec703ab88302a258e5`  
		Last Modified: Fri, 02 Jun 2023 00:24:57 GMT  
		Size: 15.8 MB (15840641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2543924bc730178b71560bbf215eab51af39beb08abc751cf0ceb20febacfa11`  
		Last Modified: Fri, 02 Jun 2023 00:25:21 GMT  
		Size: 49.0 MB (49043911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd9df09f091a7526cff5b069ee1f9ffe4f78b76eb7854d921c55d9452abddef`  
		Last Modified: Fri, 02 Jun 2023 00:26:17 GMT  
		Size: 196.3 MB (196313902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d73f71c4332c4ebe7ac0b770fb62aea4cc353446e6b8a68348e153c785fa9c63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240262718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be99f41f3b2f99bc79b377d5852a8e0ec3e33e4a863089586b78e6dca150418a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 May 2023 08:34:39 GMT
ARG RELEASE
# Tue, 23 May 2023 08:34:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 May 2023 08:34:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 May 2023 08:34:39 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 23 May 2023 08:34:41 GMT
ADD file:390d5b6c76bd6ae4f2901362d9a308f7dc4fa9a83574ec3952e867bc951c1552 in / 
# Tue, 23 May 2023 08:34:41 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:12:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:12:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:14:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fd80ecb7763a9e3fbf3b7c2b815d337acc04e6d1a42898eee903ca05160f9419`  
		Last Modified: Thu, 01 Jun 2023 23:19:54 GMT  
		Size: 26.2 MB (26236512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05916a9cc39edfb88d065692b72105e6d80b81387a04f196cce1b55eabc17c66`  
		Last Modified: Thu, 01 Jun 2023 23:19:53 GMT  
		Size: 14.0 MB (14003969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbda1a8e864725727f7e49613e295b1cab05586208b442e983a8de1d47289016`  
		Last Modified: Thu, 01 Jun 2023 23:20:06 GMT  
		Size: 44.2 MB (44223082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e28774b21e8b497c22d6141760ecd30c10ef54ce4e663e3b6adfb1de9044504`  
		Last Modified: Thu, 01 Jun 2023 23:20:31 GMT  
		Size: 155.8 MB (155799155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
