## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:b65b6ab45d97cb5217ba744761956caf03c4ffe719f9d91d0f681c97767c171f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:noble` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0765be84cb4a511e15fd7bd919c62ae67beaa529e84285cc3437bcbf5a1076b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.6 MB (313559493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ad6790e4469155aa753919f1ded78ddfab2ef5ba8aac5501484b4575a28089`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 07:59:58 GMT
ARG RELEASE
# Thu, 21 Dec 2023 07:59:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 07:59:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 07:59:58 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 08:00:00 GMT
ADD file:a0ba91d32217ea2536915535ff91264b55534a6ec7ff3d6ae86c586ba16b04e5 in / 
# Thu, 21 Dec 2023 08:00:01 GMT
CMD ["/bin/bash"]
# Thu, 04 Jan 2024 20:33:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 01:53:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 01:56:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e6e962016133a2e69bf8bb72544b211445633f148627c656908805f0ca1e2a14`  
		Last Modified: Tue, 02 Jan 2024 21:20:35 GMT  
		Size: 30.4 MB (30350118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eab6a772f8ed88e9b2ee72076bfd4fb0e94a8febad8182dcac2722aae4058e9`  
		Last Modified: Thu, 04 Jan 2024 20:38:23 GMT  
		Size: 13.7 MB (13719056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7599ddef79c8c9a66cd4f40b174c9ac5724bc3fcbaf13bdc706636285942a53`  
		Last Modified: Wed, 17 Jan 2024 02:08:29 GMT  
		Size: 46.0 MB (45953591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb5e5cfb36065e12453f96cad4a73f4251559fb9d4ff30c09bac5160908eaeb`  
		Last Modified: Wed, 17 Jan 2024 02:09:07 GMT  
		Size: 223.5 MB (223536728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e811ec208c2b8251790e1cbe760b3c02a6245d1c418bb0c50803036f4d442935
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.5 MB (270519637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d11b13f0aea87b2986b2d1a3c60aab7b35d205aa6cc900fd9b072427031229e2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 08:15:34 GMT
ARG RELEASE
# Thu, 21 Dec 2023 08:15:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 08:15:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 08:15:35 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 08:15:37 GMT
ADD file:e7d60066a3b63b2e3fe37105c61c5e46691f4f567804e5eca5a9006ceed5d139 in / 
# Thu, 21 Dec 2023 08:15:37 GMT
CMD ["/bin/bash"]
# Thu, 04 Jan 2024 20:17:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 02:14:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 02:17:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5b1fdfccfb097e3ea8369bc634c0a794c7f5dfa00a944deeff4a97c9496acd7f`  
		Last Modified: Thu, 04 Jan 2024 20:24:32 GMT  
		Size: 25.8 MB (25769091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7239c158ae97251c79c79b045912b146acfff69748a2146ac66091ac11d3a817`  
		Last Modified: Thu, 04 Jan 2024 20:24:29 GMT  
		Size: 14.6 MB (14621580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b5a3653290438533a6e25c0661e212a2f6e7a8757b18df319541e20188a0e5`  
		Last Modified: Wed, 17 Jan 2024 02:29:11 GMT  
		Size: 50.1 MB (50091765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a163e6271ade96eb72f1f822e130bd6fd7a7f4034343757a8aeea0f1a5b4da9`  
		Last Modified: Wed, 17 Jan 2024 02:29:56 GMT  
		Size: 180.0 MB (180037201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:27824d4737679dc889c9f05221d17d5a26057e108e2d329aba169a11a5482dd5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 MB (298013578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17be8a8cab848a41fd8edd75bae2b85ff6218e695b966ac291e47cf5deafd38b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 08:07:26 GMT
ARG RELEASE
# Thu, 21 Dec 2023 08:07:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 08:07:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 08:07:26 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 08:07:30 GMT
ADD file:747b926a2c5db1bde721d5f2e6cc257e61f094098f4ec5109ca37f7ec202e15f in / 
# Thu, 21 Dec 2023 08:07:31 GMT
CMD ["/bin/bash"]
# Thu, 04 Jan 2024 21:02:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 02:48:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 02:51:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:894886ead4cb9562f49271af0159d0a1ca3cd047fe095546a95b2547503278bc`  
		Last Modified: Thu, 04 Jan 2024 21:08:18 GMT  
		Size: 27.4 MB (27440272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad4c764df2e8f81f9fa5b16b3c9e87d20f8f97148504bbf60a3eb3b51fc5d07`  
		Last Modified: Thu, 04 Jan 2024 21:08:16 GMT  
		Size: 15.5 MB (15513863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae3ebef7d3c1616351532aa160c17b0911557b386f40db28b80fa777f1e64d7`  
		Last Modified: Wed, 17 Jan 2024 03:10:22 GMT  
		Size: 46.0 MB (45975955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f9a5338a599646dea63be51609349922394f004590892024f179c8de9bdabd`  
		Last Modified: Wed, 17 Jan 2024 03:11:01 GMT  
		Size: 209.1 MB (209083488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8e7e90b0fc6cc2d78c3a8c32c3dd23d80a605a7b51096e854eefd6250cdd7401
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.3 MB (327273931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8b5726822f9c84c46833ba201075a7d701208a3856038a79f712539fe5e47e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 07:46:19 GMT
ARG RELEASE
# Thu, 21 Dec 2023 07:46:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 07:46:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 07:46:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 07:46:22 GMT
ADD file:83a18fa01ec4574671ff01727c2059a3f114915594312ad939999fb6266c8b85 in / 
# Thu, 21 Dec 2023 07:46:23 GMT
CMD ["/bin/bash"]
# Thu, 04 Jan 2024 20:30:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 03:18:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 03:23:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f7ae3c70a47814103cc56d7659dc773a9caf5ce8df4d8324b88d9b5043e063d4`  
		Last Modified: Thu, 04 Jan 2024 20:38:35 GMT  
		Size: 32.4 MB (32405112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a6c7c9e8ceb49b67e3dbdacee3d70552db6ae83ceaea6d637dab7c45794b13`  
		Last Modified: Thu, 04 Jan 2024 20:38:28 GMT  
		Size: 18.5 MB (18547889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c7e7ec224c4fb551cbfccdcb2e9f922b97b63a7e37bcc2e802140b0fb681de`  
		Last Modified: Wed, 17 Jan 2024 03:33:16 GMT  
		Size: 51.2 MB (51193679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51252675d663f8720b62a3e98bed435e44ea173173476f57e6604dae4751db74`  
		Last Modified: Wed, 17 Jan 2024 03:34:01 GMT  
		Size: 225.1 MB (225127251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e005e4677bff5ee1112d0310428d64a4959f3f07746910eeb67c30f195c2c6d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 MB (291147667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c781042dc5ee40cc58449e3420a8f89882ea25c0e6c6e1754c388e91e564e2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Dec 2023 08:03:37 GMT
ARG RELEASE
# Thu, 21 Dec 2023 08:03:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 21 Dec 2023 08:03:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 21 Dec 2023 08:03:37 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 21 Dec 2023 08:03:39 GMT
ADD file:6d95854b18c392a40cc9d516bfc1a0bcd815c49b996995d35c13d1ff02d92b8b in / 
# Thu, 21 Dec 2023 08:03:39 GMT
CMD ["/bin/bash"]
# Thu, 04 Jan 2024 20:45:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 03:58:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 04:01:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0eb0ee1ee32a505c711b23ae33e7ecc888899622d95c7e982ef82dbb529c5d8`  
		Last Modified: Thu, 04 Jan 2024 20:50:14 GMT  
		Size: 28.2 MB (28174524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02199b1c3761965bf141c9010678515a9c50e39cc89d2a830d1dd5d17aa25bc2`  
		Last Modified: Thu, 04 Jan 2024 20:50:13 GMT  
		Size: 16.6 MB (16609480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485bb0479022ae70b4d5d036ab8cd2a74bdb0cdf2ce41f139a8f33c3c3062fe1`  
		Last Modified: Wed, 17 Jan 2024 04:09:32 GMT  
		Size: 47.5 MB (47466650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a964a9c9929f0234620bf2dd4effe60e6d9f99cc5772e627b8e1a32f683e7b1`  
		Last Modified: Wed, 17 Jan 2024 04:10:03 GMT  
		Size: 198.9 MB (198897013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
