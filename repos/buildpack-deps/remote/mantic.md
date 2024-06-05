## `buildpack-deps:mantic`

```console
$ docker pull buildpack-deps@sha256:97beb8a09bcac3ec6292dae7baa6dad76458d8225dc779fa3e11e630bab69723
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
$ docker pull buildpack-deps@sha256:15959ae0ea998982c4f9020b571c183a74b8ecd6173975dadf221a7b1172f8cf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.5 MB (246497968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac5fadc348a3fa3c9c0ead1dc43b82d56a7d9bf9c632203e12e1787cd66406e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:35:52 GMT
ARG RELEASE
# Thu, 30 May 2024 04:35:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:35:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:35:52 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:35:58 GMT
ADD file:5aa23d80e542b577797d50ebc7e42a4293a8387e071f3acf47dd1c4232e3463b in / 
# Thu, 30 May 2024 04:35:59 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:41:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:42:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:45:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8a04cad1e2168093eb69d36324c57c8d5a592597dc124473e47a7734b4ac780d`  
		Last Modified: Wed, 05 Jun 2024 03:53:36 GMT  
		Size: 25.7 MB (25688648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be993b7551c91005764db4f62ec9285d2322d78dbed6f84b24965e75ba4bb29d`  
		Last Modified: Wed, 05 Jun 2024 03:53:33 GMT  
		Size: 9.2 MB (9152175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76642a0d8c917f8b4762138fba3c9de67689f5a5e5de9b64d3f6f72b20f70709`  
		Last Modified: Wed, 05 Jun 2024 03:53:52 GMT  
		Size: 48.9 MB (48942204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8865e47fb8518fbe3850de6b634b5678c01dd50ca46ea099fda5505a3460b2f`  
		Last Modified: Wed, 05 Jun 2024 03:54:21 GMT  
		Size: 162.7 MB (162714941 bytes)  
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
$ docker pull buildpack-deps@sha256:c5518ee43966f4d3aadc3036aed440186d365ac1c31e3537dd3873c9a702b57e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.8 MB (293830944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f909253f1cb306f8cc9d72a734c9aa127c4f96619e546a80603402f14165c71`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:40:57 GMT
ARG RELEASE
# Thu, 30 May 2024 04:40:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:40:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:40:57 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:41:01 GMT
ADD file:95d00e4368890732f9068173852e581f3c88514b2457d11d24ac4d2505a594d7 in / 
# Thu, 30 May 2024 04:41:01 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:34:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:39:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1db7b14ff19434de4b9e4762b8b845a87a0d56130bdee33d4a49f233abb62c9b`  
		Last Modified: Wed, 05 Jun 2024 03:49:19 GMT  
		Size: 32.4 MB (32350668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e104d2d8f80f552c85787a29c9846d9ccc245d14399c5c14a1b07feae431275`  
		Last Modified: Wed, 05 Jun 2024 03:49:14 GMT  
		Size: 11.6 MB (11585778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cb7ced059bf2a43a1fe9d833ce19fe75a8eaf293da574dd45c14836e77cdf4`  
		Last Modified: Wed, 05 Jun 2024 03:49:35 GMT  
		Size: 49.6 MB (49618077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a7ee833f24770d2de6172bc5a24ff710d08064d7ed5d5c58cc56080e319e1f`  
		Last Modified: Wed, 05 Jun 2024 03:50:12 GMT  
		Size: 200.3 MB (200276421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8be834fc55e85de04be1a4be2b720b896375063e368195c5c61df37086dec2b0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259174294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5daafee1e2949c467e190a77fefda1291dc30bfc1d91720ac40807974b783772`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 04:40:53 GMT
ARG RELEASE
# Thu, 30 May 2024 04:40:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 04:40:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 04:40:53 GMT
LABEL org.opencontainers.image.version=23.10
# Thu, 30 May 2024 04:40:56 GMT
ADD file:69a1fef8aa0fa78f89ddebfe6ce2c6931d9d6df07b9ed9ebe3f9bebe04eed7f2 in / 
# Thu, 30 May 2024 04:40:56 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:26:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:27:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:29:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eee394775ffd8c11d94a145d72ab3ed77cb072ed5a12669c7ac4615a277e23a9`  
		Last Modified: Wed, 05 Jun 2024 03:36:21 GMT  
		Size: 27.9 MB (27891404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d74c9a6e2d4a8987c978732b98b406a9f7977e0c8dc80bd843a38a97029cea`  
		Last Modified: Wed, 05 Jun 2024 03:36:18 GMT  
		Size: 9.8 MB (9759019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8180965f353999389ac9a5a3880e73af3fe29a168b55d1e7cf69c49184ef1d`  
		Last Modified: Wed, 05 Jun 2024 03:36:33 GMT  
		Size: 46.0 MB (46047739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c6c8bf19011470468580af2c58176f51e586eef8ee879c216bc083a94efa7e`  
		Last Modified: Wed, 05 Jun 2024 03:37:00 GMT  
		Size: 175.5 MB (175476132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
