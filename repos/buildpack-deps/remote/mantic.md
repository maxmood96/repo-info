## `buildpack-deps:mantic`

```console
$ docker pull buildpack-deps@sha256:51eb9bd00fe32022584e4276ca2cb5dfcf2b6c1c976b6bbc3b460e39af800895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:mantic` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f3e24648ef154885cea361d8b52c2e1985772d844acee52834f53a7b890a660b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279847530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804500f8c179d8acd90b7a8ac182045dd16d1a2a8852e33f39f2ca8d75bb8a07`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:02:03 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:02:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:02:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:02:03 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 29 Apr 2024 16:02:05 GMT
ADD file:870c43eadc01423c5bc11fc4422ee10b05cae0f50c997f8e380e0ed25c6c0b11 in / 
# Mon, 29 Apr 2024 16:02:05 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:02:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:03:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:06:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8496cd0ea1eee2817b0144b138e4851ca29d675473addef86c4d5838b98b10e0`  
		Last Modified: Tue, 30 Apr 2024 03:34:40 GMT  
		Size: 28.0 MB (28037242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90001033f98f32d73d26d33545975169f4a8186beac4819ea4fde58f38f27815`  
		Last Modified: Thu, 02 May 2024 02:13:27 GMT  
		Size: 9.9 MB (9911781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d673a81eea47677f1c20cd613c42d148d058da96220692d2550e23112c34d7`  
		Last Modified: Thu, 02 May 2024 02:13:44 GMT  
		Size: 44.8 MB (44768343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4707b0e737051f716e2f28a20fb735b02d0039f7410b285382c64f5768e886`  
		Last Modified: Thu, 02 May 2024 02:14:17 GMT  
		Size: 197.1 MB (197130164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3ca3e5113b7e6f0f04020de4f7a6a18a7582b7a2960af44497fea12115bb5cc0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.5 MB (246510618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb15e530f5c107eee84dc5eedaeed5c20c33d943d7eae04e81da24a4f37505a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:05:53 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:05:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:05:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:05:53 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 29 Apr 2024 16:05:59 GMT
ADD file:36a9fb96170feb2e8bb6dfda0793b5f7069593502c61024a6ed3d84eb01afdaf in / 
# Mon, 29 Apr 2024 16:05:59 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:57:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:58:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:02:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c14f7cb79524b2adc26e658f09be736a2820a009c0cf783b8204bd8f44ff6dd1`  
		Last Modified: Thu, 02 May 2024 02:11:20 GMT  
		Size: 25.7 MB (25687736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891e062e56c3529de217cc9c1b86c28a85a8a887411ef56e0566d3b280203ff0`  
		Last Modified: Thu, 02 May 2024 02:11:17 GMT  
		Size: 9.2 MB (9152040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922394cec4336bec66ccf4cdc7027a9c41f90dcc87336a1ea3fae1ca7dd15295`  
		Last Modified: Thu, 02 May 2024 02:11:36 GMT  
		Size: 49.0 MB (48950463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aec45b68680584fce0c0c2f6a272f6d1cb44d067216db665c61cc1983905e8a`  
		Last Modified: Thu, 02 May 2024 02:12:06 GMT  
		Size: 162.7 MB (162720379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:60ae123f83a4d99c45d7ade2bf96bddaaf5423579e2a767d40c0721ebaf9256c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (271970370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ba88a9a8ef565c742aed51af53a476920cf6dec6e05143a78dc9f5803671f7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 15:59:01 GMT
ARG RELEASE
# Mon, 29 Apr 2024 15:59:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 15:59:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 15:59:01 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 29 Apr 2024 15:59:07 GMT
ADD file:0766b52edac59a701a3c97d7372ee928210e45e682fc997b4e7f869a2136ff7a in / 
# Mon, 29 Apr 2024 15:59:07 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 03:19:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:20:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:24:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:de30cfcb0b3c8185bc9bf88dc253529aa2f988dce372173b61c766339c7d4045`  
		Last Modified: Tue, 30 Apr 2024 03:38:06 GMT  
		Size: 27.4 MB (27380844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db73c434226caddcf2d26fded83051afc5a676600e1a811e0c60301447972450`  
		Last Modified: Thu, 02 May 2024 03:32:49 GMT  
		Size: 9.7 MB (9666068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be4c27558f1ae84b9ea479f94cc05da2332db46eb7f5f592143a723012da835`  
		Last Modified: Thu, 02 May 2024 03:33:04 GMT  
		Size: 44.7 MB (44678929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593b20f4867463461e1ab708c0b9c0dc0ef77d253a694af279e3950ea2f7a17e`  
		Last Modified: Thu, 02 May 2024 03:33:31 GMT  
		Size: 190.2 MB (190244529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4f60f4bb49bdb5c44e7fbb18dfdd59d408ff7e5259d2e8475d837504f7aef4ee
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.8 MB (293761183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9661e1cd15d13f9830de908c609c268d7519c56dfd0176b2a60a7244da8c6d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:04:17 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:04:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:04:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:04:17 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 29 Apr 2024 16:04:20 GMT
ADD file:3eff778e5407e167e169212e204258e93e6574103bc6286f120fa1e790582498 in / 
# Mon, 29 Apr 2024 16:04:20 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:11:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:13:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:20:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1532b783baec83835efe31b4c05c574cf39a1e1e98d7628702e186198cf0ee6d`  
		Last Modified: Thu, 02 May 2024 02:32:33 GMT  
		Size: 32.4 MB (32350607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d677821ac7ae97f0fa4ec3f5603bc76de57322ccedcc962b6e6f80d05d963c8c`  
		Last Modified: Thu, 02 May 2024 02:32:26 GMT  
		Size: 11.6 MB (11585962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00acf8b3c751d3b8dca105ecc98b21874e712adc45ccc949a1ecccedcc7def18`  
		Last Modified: Thu, 02 May 2024 02:32:50 GMT  
		Size: 49.6 MB (49561852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:312276fba7dd2624d0a1a149ed351173a3c3ab23705f809d399d1d89ac2f0ada`  
		Last Modified: Thu, 02 May 2024 02:33:28 GMT  
		Size: 200.3 MB (200262762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9b7495b48b0d48025f09d498d616d85a6d2444f43496ceb97d60ecb548ed7aa0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258360349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d75f1763aee9261cfb542daaa68c084826f2379c33264c46bb2480565a3586b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 15:49:35 GMT
ARG RELEASE
# Mon, 29 Apr 2024 15:49:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 15:49:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 15:49:35 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 29 Apr 2024 15:49:37 GMT
ADD file:76b6235c926b9bd628f27161f73913d479e584c2035eb7185806b814f4e96e14 in / 
# Mon, 29 Apr 2024 15:49:38 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:23:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:24:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:27:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ae85e9169f00cfaac0525494fb8251c5f790089a9748fdbd34e5fec105e50fbe`  
		Last Modified: Thu, 02 May 2024 01:34:50 GMT  
		Size: 27.9 MB (27890933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e372ff38d547ce6c08db910602c662578b312dc24c86593738f583360e0613`  
		Last Modified: Thu, 02 May 2024 01:34:48 GMT  
		Size: 9.8 MB (9759011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f4cdf7791a613f05e9e4b51edd04a313f26fbe67c95bfbe74d9d933253a492`  
		Last Modified: Thu, 02 May 2024 01:35:03 GMT  
		Size: 45.3 MB (45254411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec5f70a60cda378edc68ae96c3a26b34f3237057c5fb7ff7d927208ad251cb0`  
		Last Modified: Thu, 02 May 2024 01:35:30 GMT  
		Size: 175.5 MB (175455994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
