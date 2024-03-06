## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:c39d69d10d0140c4c4bf04d1efea4fe2854fa91ff1ff38c0828f32bd9b9e404d
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
$ docker pull buildpack-deps@sha256:259dd02ae96f2d1babcf2983e064912b0e3b659930fc6be79a8522535248e9d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.7 MB (318695257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7c40ab633dffd0bfaf07763af95a466147808ffc85bc8c9eb79fb712220c04`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:22:40 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:22:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:22:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:22:40 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:22:42 GMT
ADD file:93f7775e4e5ce50f9e61bbd8f651e279ddd3add435e095c503b909e3da650623 in / 
# Sun, 25 Feb 2024 04:22:42 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:10:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:10:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:13:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80edb1aaf132005ee2bb2f811872efbbbf0cb9b8ec36897c5849798408c7047b`  
		Last Modified: Wed, 06 Mar 2024 04:17:28 GMT  
		Size: 30.6 MB (30551664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed6aec9cb3192e03ad86531dfe44b7ee4ba8d368c7d645de6cccf2c8dffd0942`  
		Last Modified: Wed, 06 Mar 2024 04:17:25 GMT  
		Size: 13.5 MB (13455900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8382e640dd0ca6f92e2593a14d2863e9b909da9090d0f355787601b074e7e19c`  
		Last Modified: Wed, 06 Mar 2024 04:17:44 GMT  
		Size: 45.7 MB (45743931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4adea66a5a529e25830935a61441a370c0563b30d99ea2da7a49e53bf8108fe9`  
		Last Modified: Wed, 06 Mar 2024 04:18:24 GMT  
		Size: 228.9 MB (228943762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8ba0e14a02d5e19dcb27e9e14af9939b30f7878fb599510a1f00d51db45e47c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.2 MB (273230848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576daa73dca6305c7ad39ca45a2e5b80acdeddc0fb2197af8d139a7a5fb538e3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:29:12 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:29:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:29:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:29:13 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:29:15 GMT
ADD file:23f3bed4668146daee4397de493e7552ac025df8df189085e9e494a96fa0c387 in / 
# Sun, 25 Feb 2024 04:29:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:04:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:05:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:08:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c45e0810ab1c7fc30d716f075d506d33fd67be1ee3c90239200d7ce6b1030bfe`  
		Last Modified: Wed, 06 Mar 2024 03:13:33 GMT  
		Size: 27.7 MB (27731114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20942a9851c4aab23d43b8f866570d29f4316a78b3da8425e34c056c008745c`  
		Last Modified: Wed, 06 Mar 2024 03:13:29 GMT  
		Size: 12.6 MB (12602765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f349b2b4241ab3d83537ee61a9cad53d88310fbb5248f6e04b49a1285e9aba79`  
		Last Modified: Wed, 06 Mar 2024 03:13:51 GMT  
		Size: 49.8 MB (49761194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e01583a141e97ef5a0aec445ed9f7e14e941b8b3e37745c1e36c3109b96554`  
		Last Modified: Wed, 06 Mar 2024 03:14:32 GMT  
		Size: 183.1 MB (183135775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:45ebb68136dfda231c4d3a51c9527ad2063b899981d8d6438edc8cb96f417dd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305425921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71d15e3ee41e130ebf4284b61a5e0347bffcb935d8c2be0e9fac98e091c91b5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:11 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:12 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:17 GMT
ADD file:d70383c2066380d512b8d983092c0ca9faeb5eea2890bca883d43f049d7ae8fc in / 
# Sun, 25 Feb 2024 04:24:17 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:45:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:45:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:48:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:29440aefa520893bd718db0f6410e6e526dff0029d9bae385123a40bdfaac005`  
		Last Modified: Wed, 06 Mar 2024 03:52:21 GMT  
		Size: 29.9 MB (29875465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87f3d34b3b4ec03b04a5b27194ca3da88544ac3dba2211387389425c0ac8648`  
		Last Modified: Wed, 06 Mar 2024 03:52:18 GMT  
		Size: 13.3 MB (13271020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9974eadb59c4c8a7258a03bdd5d5182c454d60c821a9dd902e3c04eb031390`  
		Last Modified: Wed, 06 Mar 2024 03:52:35 GMT  
		Size: 45.8 MB (45805608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca642e4c3164d875c8a8e31782bb31faf2f4b630867d243eecba4e0ee7953bf4`  
		Last Modified: Wed, 06 Mar 2024 03:53:05 GMT  
		Size: 216.5 MB (216473828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:baf0bf3926067d244a5c186b6b0029a1b09ed610cc3e37331ba14cd48e9d5ff7
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.8 MB (335846262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9481a6c3ca7d56bb183ace9f2a0e456ae608916c120ca6224e2675325199e3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:08 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:09 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:12 GMT
ADD file:4a02618d84dcab4bbb05f776869d999a8c26745e9e74e185ff8cc5dd1adef67a in / 
# Sun, 25 Feb 2024 04:24:12 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:44:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:50:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:948c41f680a2c1a00eb8d31747ec9f9bf3450ef13555dd70b044362577b93e63`  
		Last Modified: Wed, 06 Mar 2024 02:55:19 GMT  
		Size: 35.7 MB (35655105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22da2fade9ea6248ac088068db05e59c62ffb846b88d481b80df6a1d935846a`  
		Last Modified: Wed, 06 Mar 2024 02:55:14 GMT  
		Size: 15.8 MB (15759946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6aadf819f0aa05de123e377fd7bdc60300c1a6221aa1b4e955c92679e6771c`  
		Last Modified: Wed, 06 Mar 2024 02:55:46 GMT  
		Size: 51.1 MB (51052412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881ddf165df7bb2420e4acab24b0465182f8afbef4c4f87365c28ac2fb58bd85`  
		Last Modified: Wed, 06 Mar 2024 02:56:32 GMT  
		Size: 233.4 MB (233378799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c6d1af75975c131519bbc8eeef86a9312c981a838d2fcfc00dccfdd4a7f99141
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.9 MB (301888562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def7e5ea62cb995f9b4683cfad978dd3e5956d619fb317798e5bca90d3796de1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:24:11 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:24:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:24:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:24:11 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:24:13 GMT
ADD file:d14045ce9e07df2d8f9bd72b1fde177ac65891154b19a19ffa7fa03960fdbe94 in / 
# Sun, 25 Feb 2024 04:24:13 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:39:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:41:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:44:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba672c08b1f1d80da8328ffbb8c068ddda49ba41754c6df92773d5b97a619b3e`  
		Last Modified: Wed, 06 Mar 2024 04:48:40 GMT  
		Size: 30.6 MB (30645649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0f5ec95c792756ff5c9429755f7929e89d3cc0e3f161036e78e61e0d0d3344`  
		Last Modified: Wed, 06 Mar 2024 04:48:38 GMT  
		Size: 14.8 MB (14821611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1671ccd52fd4caa5e52f088375d19d5cc86ba163b0350c95ff464ebb872668a3`  
		Last Modified: Wed, 06 Mar 2024 04:48:54 GMT  
		Size: 47.3 MB (47346503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74fd1b8866a23f60ebd429fa73528999c0080ab66d901f8ef47e7450888952ae`  
		Last Modified: Wed, 06 Mar 2024 04:49:26 GMT  
		Size: 209.1 MB (209074799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
