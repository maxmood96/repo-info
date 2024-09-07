## `buildpack-deps:oracular`

```console
$ docker pull buildpack-deps@sha256:fa25bd08eaf16e017c2287dddcda254c509e8cac396a4c5a9352dcd3b586b0b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:oracular` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:53a3af67688dca3357dc3c61750adf28f8538254864c06acb3896e346d69fd23
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.1 MB (298126965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51675e700651d03dddab91d364cd70e1336f1991beadfb035c88b781a000539`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:38:38 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:38:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:38:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:38:38 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:38:40 GMT
ADD file:3e58023fe8ae84c8f4bc55aad37fe164a2311db70a6b417b82d3cc05f257c264 in / 
# Sun, 11 Aug 2024 15:38:40 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 04:22:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 04:23:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 04:26:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d99a07f5fc56ba5a74c9ef03e39c6d21ec548275b38ca100d2282ac50dba5b88`  
		Last Modified: Mon, 19 Aug 2024 09:38:59 GMT  
		Size: 31.2 MB (31215904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee87e67aeac71b57f34617bcbcbfb48b4526a877864b276d6cfac92c28332fe7`  
		Last Modified: Sat, 07 Sep 2024 04:27:23 GMT  
		Size: 18.2 MB (18164652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055335bda5b48b9b7f5bf248f1a6cda9c73710f1621ec8e7795dfa323f2e016d`  
		Last Modified: Sat, 07 Sep 2024 04:27:39 GMT  
		Size: 46.9 MB (46852775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee09a1f0595ea00a56bf60089efe3547f7c5b9e6ab94e3fec96f1d6ec2225dce`  
		Last Modified: Sat, 07 Sep 2024 04:28:12 GMT  
		Size: 201.9 MB (201893634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f5303ef2025d662e9f49e96d8f9a65496c6464611d6c26f02271de44cca99f03
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.9 MB (258946084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcbed6e56952a127479fa7e8f064c4286d6698794d76d534c349ec0cddc6e92b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:38:54 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:38:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:38:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:38:54 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:38:58 GMT
ADD file:4a74176688f6256cc90d758b02955eb55de176831a5890c949712ad4b2991476 in / 
# Sun, 11 Aug 2024 15:38:58 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 01:59:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 02:00:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 02:04:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ba000785763e277141f722f9cc6aebee15ac21572de15075a6407026d2ceab7c`  
		Last Modified: Sat, 07 Sep 2024 02:05:11 GMT  
		Size: 28.2 MB (28151027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693d4bfd023e08a42b470cb0b43c766b88b85f7f30fb5b43fa0219943ce2a3c9`  
		Last Modified: Sat, 07 Sep 2024 02:05:08 GMT  
		Size: 16.2 MB (16231437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff511081b01199e4b9bb12d45bce6d56e4cd79db917542973d713b209bc166e`  
		Last Modified: Sat, 07 Sep 2024 02:05:26 GMT  
		Size: 49.8 MB (49799754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33cf6986399844487d0a4441f3c73bd0d75f4f01a51d238f23d20b323d9123ff`  
		Last Modified: Sat, 07 Sep 2024 02:05:57 GMT  
		Size: 164.8 MB (164763866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a6e1914b35a42dc8a1e3d3c3c7b2e39ff7bd08fd344e441940ade2c25aba9741
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.0 MB (292039463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8069aca49b11ddfab5419df6d0a322999fca568e6f3cb68fe4d5f48a9a806d9b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:38:41 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:38:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:38:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:38:41 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:38:43 GMT
ADD file:1ad5462522bfc6d8b07f9d64ddf868aa9145c44d7e36ac7489e07719bc0f9c50 in / 
# Sun, 11 Aug 2024 15:38:43 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 04:20:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 04:20:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 04:24:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:dc0f8ac147f52f41cac91af40556dcda467531813bfbe1899f174f25d02e853c`  
		Last Modified: Tue, 20 Aug 2024 05:04:56 GMT  
		Size: 31.0 MB (31036287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12168fbcdb069935dfac3395cf822dcc16837e5f6b7f9c66bb10e5975d6ac3ea`  
		Last Modified: Sat, 07 Sep 2024 04:25:43 GMT  
		Size: 18.3 MB (18294539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3024e10b71baa355a2df6e0d250585dc206f2c9ea54534441463dc57467b4b44`  
		Last Modified: Sat, 07 Sep 2024 04:25:59 GMT  
		Size: 46.8 MB (46802301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951062e5b2fd6d80a940e440cd74d8a39d9ff7b11defbf672b243f6fe4612d08`  
		Last Modified: Sat, 07 Sep 2024 04:26:26 GMT  
		Size: 195.9 MB (195906336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c9649827163d60b6e8a1f61b1252872e212351892e53bc2a01a277e0efabdc49
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316117234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a5dddb4b63f18e6b6fec2cf320e166504a6d8fd6c2f4f975a9e8f89b14f0c3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:39:31 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:39:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:39:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:39:31 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:39:34 GMT
ADD file:c995bac66bc8ed18a9e5e7591143905810e18f366ac82dd51470210c97712108 in / 
# Sun, 11 Aug 2024 15:39:34 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 05:58:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 05:59:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 06:05:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e5263b57d12e15968f82be92102a4bc2eec746bcdb5e8f52265768241e5d8ad7`  
		Last Modified: Sat, 07 Sep 2024 06:06:12 GMT  
		Size: 36.1 MB (36122058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ba2db1b506c462e2b35c8a62eeb6cb6de7fba291c922a3627ba9ee572d5d40`  
		Last Modified: Sat, 07 Sep 2024 06:06:08 GMT  
		Size: 20.4 MB (20371527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314fe13ab777163606b9145019d08931bba0381111e334bc7a164f67a035ed73`  
		Last Modified: Sat, 07 Sep 2024 06:06:31 GMT  
		Size: 52.2 MB (52185743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed4c027cd6ebb8fffc10d99f831ea2742f2251c37b83d72e34dce5596fe5c50`  
		Last Modified: Sat, 07 Sep 2024 06:07:10 GMT  
		Size: 207.4 MB (207437906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f013b5d281ec472e3bec9d5008e19e377beefacb2c9c6d60ebfd05630d5b6790
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.1 MB (276051969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9215737453d0c0471a03c64c6bf94d12f7df48d6501e1531b132e45a0c0176f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:38:23 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:38:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:38:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:38:23 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:38:25 GMT
ADD file:1afe7006fc30d35d19a6fd7338d9bdf3312fb2e5d9c617c709d1a2edc626d881 in / 
# Sun, 11 Aug 2024 15:38:25 GMT
CMD ["/bin/bash"]
# Sat, 07 Sep 2024 01:51:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 01:52:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 07 Sep 2024 01:55:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:29e8b1ec75570fb19b7a0386180396a0e815ede57a87574c2ad028bfecdd6918`  
		Last Modified: Sat, 07 Sep 2024 01:56:24 GMT  
		Size: 31.1 MB (31132029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70745f7dad6d5386030f49f2426f299968336739bcbcf9ae2b8462560b4a9943`  
		Last Modified: Sat, 07 Sep 2024 01:56:23 GMT  
		Size: 19.4 MB (19412068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008cf182f449632ffe2a4d63ef9fa22ab66fd95d2c395d89ba25703628dae55b`  
		Last Modified: Sat, 07 Sep 2024 01:56:36 GMT  
		Size: 48.3 MB (48256989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e91c618697b775b83b66d93e2814a7040b5e3340d5be35ed7c381a24ad9e448`  
		Last Modified: Sat, 07 Sep 2024 01:57:02 GMT  
		Size: 177.3 MB (177250883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
