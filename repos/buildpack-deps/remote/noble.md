## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:33720f48dc2813d3587095d6293c14aa8518d646acc8867920747bbeec793d9f
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
$ docker pull buildpack-deps@sha256:f7d0b46fb0bfdd108a3ee9c39aa641bcb706387b52740b5ffbb0d24ef06ae360
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 MB (279595111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d194d1899bcef2cddaa91e9c500662fda2fdd9bd2efa273dc4888907f6f324`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:00 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:02 GMT
ADD file:ac9d5a9d5b9b1217a6b26f1069a16bc48fa9c2ed76f3eaf28a8e643ae2058d11 in / 
# Mon, 29 Apr 2024 16:38:03 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 23:36:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 22 May 2024 23:37:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 22 May 2024 23:40:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:683717517814a7e5abc1086ac638706a33e20d12621de123d0d4041d703a8736`  
		Last Modified: Thu, 02 May 2024 00:53:54 GMT  
		Size: 29.7 MB (29702452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a3fa374d78d6bc1d2cab1e56e050fad206b983d08dd4d05ce017af22c2bb25`  
		Last Modified: Wed, 22 May 2024 23:41:29 GMT  
		Size: 14.4 MB (14441188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad31eb17b1c35f2639c2ad85926af055e59d35a801e6a53297275981850f09e`  
		Last Modified: Wed, 22 May 2024 23:41:45 GMT  
		Size: 45.4 MB (45435931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9df4ea0675fc5718fd2a59df49c891ac217c0bcb24f1bfc7571e3eb6378436f`  
		Last Modified: Wed, 22 May 2024 23:42:21 GMT  
		Size: 190.0 MB (190015540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1d37137547549d646fd57c80777473ef45ae08123b5ac09fbf5c4fde3067832f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (239981834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ece3e854961aad2be5695cc18d54a9e4b7f8cc59e34f8d8fa83a93434b92b81`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:10:38 GMT
ARG RELEASE
# Thu, 30 May 2024 06:10:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:10:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:10:39 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:10:57 GMT
ADD file:d80eadd0437b975b8658cf30a5fbcfeeeaeb7189648e9d358fbe8d3605b11c50 in / 
# Thu, 30 May 2024 06:10:58 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:46:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 03:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 03:50:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6076354c2bb3f763be2bb71ab68ee2ac3135a0463546e9db3cdce8e4c4aa1d89`  
		Last Modified: Wed, 05 Jun 2024 03:54:33 GMT  
		Size: 27.0 MB (26958335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1733b899cc4621ee2b6ef63859316cd9ea6c5a74e9e1e6750a442033b12a34a`  
		Last Modified: Wed, 05 Jun 2024 03:54:31 GMT  
		Size: 13.5 MB (13492414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991c8d02626362e73446fe59044c18a39c72b337463c7d3893055fa2f243d418`  
		Last Modified: Wed, 05 Jun 2024 03:54:49 GMT  
		Size: 49.0 MB (49014700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f34590d25db915d57bedf55001f29ec4ebdfb48c7ea83504b8482e68e45c0ba`  
		Last Modified: Wed, 05 Jun 2024 03:55:18 GMT  
		Size: 150.5 MB (150516385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:06a7da3942ae13f33acfaf2e1e971486e4db867b30859056b50937a86ca41119
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270690232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09f81a7bd245c75bcb733c13a8bb936d7672752eb17bf190f3b815ac48f144d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:39:55 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:39:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:39:58 GMT
ADD file:d1bd5209fbd828a2a6f6ad537f0eb77154890b9445411715281122300f5bb21e in / 
# Mon, 29 Apr 2024 16:39:58 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 23:20:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 22 May 2024 23:21:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 22 May 2024 23:26:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ca6fd4ca81e04c073f1c2caac4de56748f56d5ff8b6eb9e1c781888109e50383`  
		Last Modified: Thu, 02 May 2024 02:33:15 GMT  
		Size: 29.0 MB (29038670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2afb81653918fa9a91fa586df7601ad7b3319bbca1de65beb077f68feedada9`  
		Last Modified: Wed, 22 May 2024 23:27:43 GMT  
		Size: 14.3 MB (14272172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb103266013103b27f23e5331700e3f47c0d81dfb6cc077477879bc345690da4`  
		Last Modified: Wed, 22 May 2024 23:27:57 GMT  
		Size: 45.4 MB (45399239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deef20cbde7690a803ad57c8c9c8cf19e6544e2612e5c52094c20d92303d0e9d`  
		Last Modified: Wed, 22 May 2024 23:28:25 GMT  
		Size: 182.0 MB (181980151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9619e7c9339fe5bdb325c8d01555ce2746158470af37a237ff1e3cf8b202a949
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.1 MB (299075645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbdc7c63c45b23130d981ac8d546c3afcdaed68df9000044e7e2a5c7708517c7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:03:19 GMT
ARG RELEASE
# Thu, 30 May 2024 06:03:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:03:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:03:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:03:22 GMT
ADD file:3d2d3a18d4f4a1567fc0564572f74e0601522492c4d8ca8614999dda64995e61 in / 
# Thu, 30 May 2024 06:03:22 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:40:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 03:41:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 03:46:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bfc0d112768e1e28c0c23d62efaae836e46b237aa988781b18fb80319506dab6`  
		Last Modified: Wed, 05 Jun 2024 03:50:27 GMT  
		Size: 34.6 MB (34579185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3b2a4dc63f1fc6fc82666c25e81039ff2658d2b0cda97654d305a96000de59`  
		Last Modified: Wed, 05 Jun 2024 03:50:23 GMT  
		Size: 17.0 MB (17037196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a2f6408ac8504d2696bad50727125bba3b8fcbd3f4cdb16db364d82f071b65`  
		Last Modified: Wed, 05 Jun 2024 03:50:44 GMT  
		Size: 50.7 MB (50707829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b25879c4fdce10703def064e54c010daf1b8184181400403c00faa9efd17e96`  
		Last Modified: Wed, 05 Jun 2024 03:51:22 GMT  
		Size: 196.8 MB (196751435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:dddd9fe0920094e9fa26ae39d8dfc7d4bc5125416bdf0e36d08a7ebbd36d9e77
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.1 MB (262135650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46582e245ff1dd4d81eb347b044e99e2f37966f0581b541e144665050b053d63`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 May 2024 06:02:59 GMT
ARG RELEASE
# Thu, 30 May 2024 06:02:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:02:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:02:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:03:02 GMT
ADD file:86f095e5ef79ee7d8fd4d38b4387a592e42b8c601012de015a295a8d2e2bca0c in / 
# Thu, 30 May 2024 06:03:02 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:30:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 03:31:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 05 Jun 2024 03:33:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:28663a99b4d51febbb131a7863581d31dc096c94d48d6a44ff0e85e38d0a6642`  
		Last Modified: Wed, 05 Jun 2024 03:37:11 GMT  
		Size: 29.8 MB (29787181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2243161fa5e13054dad01d197157a6aec0198db427b3a3a9dfcabce754b42691`  
		Last Modified: Wed, 05 Jun 2024 03:37:08 GMT  
		Size: 15.9 MB (15888579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d620b15b28615214d0c65c6af1f9e67a03ef2f4b497937d254d6730cbfab1d8`  
		Last Modified: Wed, 05 Jun 2024 03:37:23 GMT  
		Size: 47.1 MB (47119774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2cc128cc05544c139bf7bea282e63242ff37d44a9bb2ae723d3ca4960faf099`  
		Last Modified: Wed, 05 Jun 2024 03:37:50 GMT  
		Size: 169.3 MB (169340116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
