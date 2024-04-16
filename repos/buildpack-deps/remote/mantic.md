## `buildpack-deps:mantic`

```console
$ docker pull buildpack-deps@sha256:0755ecbdd2ce0a0efc72bd61544ddffc6d6ec3750f80cafb95704b37a48990ab
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
$ docker pull buildpack-deps@sha256:f918d4428aa964953d5aff1d5bab0b82c372f9d3d38a2d12b77458d37c3ca34a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279780099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:641f1e177d185a2b62526fb65c672b0fac9bbfd5897ebd1aaf0eb1e1d8b13450`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:35:50 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:35:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:35:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:35:50 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:35:51 GMT
ADD file:fb2da00b24905f9231165c1a3f037a78a00c19ca26c375a018728838dfeb82d2 in / 
# Fri, 16 Feb 2024 09:35:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:06:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:06:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:09:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:83b8dadc4df3fdb50c87e452b3f9cfea60d51607db61aca9a1062c27c65ad0e2`  
		Last Modified: Tue, 05 Mar 2024 21:36:44 GMT  
		Size: 28.0 MB (28035167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb317c53627269ca09e9abcb9ab5a7700fe4050abfa54ef20c935f8a020b0d4`  
		Last Modified: Wed, 06 Mar 2024 04:16:23 GMT  
		Size: 9.9 MB (9910875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b21ae994c2a096a3b04d9c7a1755c60179f67ca190f61936d6da7e1729ee588`  
		Last Modified: Wed, 06 Mar 2024 04:16:41 GMT  
		Size: 44.8 MB (44763285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a90bca93d1e62f99fd8cc0756b7bee297e054ae196104b9fdc912a38ff8fe2b`  
		Last Modified: Wed, 06 Mar 2024 04:17:15 GMT  
		Size: 197.1 MB (197070772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5289f79ac531efb8ad33bd0b0b6292dc4e2f62c9ce303580430f92ceeba1f221
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246446751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e4c6acfd8c70545c484652739cb0d03b4027ea23f793b63b1e6b189a815dff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 10:00:27 GMT
ARG RELEASE
# Fri, 16 Feb 2024 10:00:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 10:00:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 10:00:27 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 10:00:32 GMT
ADD file:a8ad044c0716add39fcee624f55c4ca977480f572c190628fd0dcd180478ffe1 in / 
# Fri, 16 Feb 2024 10:00:32 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:58:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:59:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:03:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:490b22d657a9bee69801f742987cf2202ef1facc1143749c551c75e40cb2b8fd`  
		Last Modified: Wed, 06 Mar 2024 03:12:23 GMT  
		Size: 25.7 MB (25683605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d74dd7838268a90e7e95de52c8608c15817df4a837c3718e184968aa8632638`  
		Last Modified: Wed, 06 Mar 2024 03:12:19 GMT  
		Size: 9.2 MB (9153237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9155ba03212deb920e05dc77749cc267b5b6fcdc16bda27f00864d27e0607886`  
		Last Modified: Wed, 06 Mar 2024 03:12:42 GMT  
		Size: 49.0 MB (48950883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5181be50d83864dec48e37287e8806806c68c94293ef26ba5d9653a7ff9a4b7b`  
		Last Modified: Wed, 06 Mar 2024 03:13:17 GMT  
		Size: 162.7 MB (162659026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:731cd983d3ce69d4c3675d6785c277e077bdf72ddc5656a646c81f189e9e53df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (271963020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd68da85d5538251384ff0fdc2aedec7071fa8ab5fc95818c5f5ab10f6720f7f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:51:12 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:51:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:51:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:51:12 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:51:14 GMT
ADD file:26243ab96da01a7d087b1c824a80d95c015b3c87952acd0ff162515d17c19a31 in / 
# Fri, 12 Apr 2024 15:51:14 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 02:00:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:01:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:04:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:14dec08930ea65c3dbde0e38ed54f079d9cc601f7e9429870443eb6f5c127ecd`  
		Last Modified: Tue, 16 Apr 2024 02:12:13 GMT  
		Size: 27.4 MB (27378355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48b671c7c275cde8e73a26074b9763487010e57526a55b3e22e3bc0da54ec6b`  
		Last Modified: Tue, 16 Apr 2024 02:12:10 GMT  
		Size: 9.7 MB (9664437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6855e3956a9a4d92d9a1298b6fe89998168da253af783ba53efa35c4403235bd`  
		Last Modified: Tue, 16 Apr 2024 02:12:26 GMT  
		Size: 44.7 MB (44677506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44488ca64d68e744c93e18124ae16efba2553d1b3bd7344de4f0650a80d0f2e`  
		Last Modified: Tue, 16 Apr 2024 02:12:53 GMT  
		Size: 190.2 MB (190242722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ab7b2acc2516219c4ef73f4b519ca6601deef8c0a12945ec8150420b6b56bcd9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293684369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ffcb209559ecddada302e968d75fcc80963af851b66bb76f1f3c712f1bb074`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 09:36:48 GMT
ARG RELEASE
# Fri, 16 Feb 2024 09:36:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 09:36:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 09:36:48 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 16 Feb 2024 09:36:52 GMT
ADD file:cb1f81d9c266883aed50b7de079d58a9f6d90401d2d7ccf3aa7f9c5ad5eec617 in / 
# Fri, 16 Feb 2024 09:36:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:35:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:36:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:42:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:214a4d0fe457c3d67700d559db1bef30e158af48faba534bfe016fdb2e3b2662`  
		Last Modified: Wed, 06 Mar 2024 02:54:03 GMT  
		Size: 32.3 MB (32348067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa0dda02c37214de423eb7444d8a4123495e723c785f46d9699f2c2c60c0586`  
		Last Modified: Wed, 06 Mar 2024 02:53:56 GMT  
		Size: 11.6 MB (11585045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa179ccd4d1ba32381ba7b18ea7a19fe2a7be5021377e619dcd5ea87d94344d0`  
		Last Modified: Wed, 06 Mar 2024 02:54:21 GMT  
		Size: 49.6 MB (49556847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24aba2c716f2fa40ca775335da4d638dd85043cc5ed23691c0e7ff819d6012f4`  
		Last Modified: Wed, 06 Mar 2024 02:55:01 GMT  
		Size: 200.2 MB (200194410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b0bb4be8e9694b1643f291f8dc14c2ec77a94fe63e7c34d645270681d5056626
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258357386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51802e8a43b0c61410f61911274b3a306cb32543bb003147a42f0ad5989b3fce`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:51:31 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:51:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:51:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:51:31 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:51:33 GMT
ADD file:13a7b46379c7483a76105798c32aac56ed459dca7ef015d973b0e1d68d9b7812 in / 
# Fri, 12 Apr 2024 15:51:33 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 01:28:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 01:28:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 01:31:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c38167d4d3684f5f8ee90b7adc5372841c98bba0d9aa208819985d030733dcfe`  
		Last Modified: Tue, 16 Apr 2024 01:37:51 GMT  
		Size: 27.9 MB (27890477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15768582f995f80e1c5766c7d3c9f5c2a98ef818cd780593cc4ec8e4abebc68`  
		Last Modified: Tue, 16 Apr 2024 01:37:49 GMT  
		Size: 9.8 MB (9758725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8626ab716cf334ee2c2065efea9a5208a1ca02fec3d802f60e7c3307826539`  
		Last Modified: Tue, 16 Apr 2024 01:38:05 GMT  
		Size: 45.3 MB (45253789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b56139bd19e7ca4356199686daeef8a1ff38afe98729b44ed774ab26bc8078c1`  
		Last Modified: Tue, 16 Apr 2024 01:38:33 GMT  
		Size: 175.5 MB (175454395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
