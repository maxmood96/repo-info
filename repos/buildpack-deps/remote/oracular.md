## `buildpack-deps:oracular`

```console
$ docker pull buildpack-deps@sha256:5cd1b41a09a6ba9e6a743f0cae2da4bb1210040766984b246b3b72b8cc79f445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:oracular` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:1f39714b7552ebbe1d80a542a4e764ec7fff0eeb5ff155e5305c836b8e1bde6f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.6 MB (293595121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd75f501048aea4153cf8a32016424ad5641c82b7450e1e602fabfc68f972d7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:56:52 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:56:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:56:52 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:56:54 GMT
ADD file:34960976e9fa0e0fb13074c6911c3f1ec7b0f3060a3e974a7990f112b21dfd8e in / 
# Wed, 18 Sep 2024 03:56:55 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 02:06:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 02:07:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 02:10:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:99f7bc2f0cd993797d13d7044e31040d2683667c94a87ee94efee8e7da42349d`  
		Last Modified: Wed, 02 Oct 2024 02:12:45 GMT  
		Size: 35.0 MB (35047708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b498f0285ec09f980863c82881d08a2c237772c9ac274cb04f01dc19283d56d6`  
		Last Modified: Wed, 02 Oct 2024 02:12:44 GMT  
		Size: 18.0 MB (18003571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ba6e5f3d90cff89eeec5ed07e205cd2b78e8e111454ee7cfcdf300bfd6122d`  
		Last Modified: Wed, 02 Oct 2024 02:12:59 GMT  
		Size: 46.5 MB (46504774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b191893e4ede174d5397194694c3780fcc1122cf4a6798dc746a28b5b8090ee`  
		Last Modified: Wed, 02 Oct 2024 02:13:35 GMT  
		Size: 194.0 MB (194039068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2085016390fa315d8ae35cb1d0896be3d5d902f2c7b553376d3e9a259df11c33
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.3 MB (257295116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b4c9ee67c97324ae0cba8cbe153b91c3452c4a67125059a3e3636c350f9aa9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:58:56 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:58:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:58:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:58:56 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:58:59 GMT
ADD file:b20509e33aca34c58565d5c38befc8f0446b34a5cbb409d03147aab392e5bb95 in / 
# Wed, 18 Sep 2024 03:58:59 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:38:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:39:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:42:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5d91f41aedf3f489d22d95042355ed6b7e565293529f4f7855d9950ced504eac`  
		Last Modified: Wed, 02 Oct 2024 01:44:44 GMT  
		Size: 34.2 MB (34209783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666d2b222a4f9de5bbbc224ebc8a06919774057f356ad3684ec337a3e1d8d5b3`  
		Last Modified: Wed, 02 Oct 2024 01:44:41 GMT  
		Size: 16.0 MB (16003899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabf4c374ea7ab02bd9e1c077c3f4295612de66efa2c54b41fef14db04e0aead`  
		Last Modified: Wed, 02 Oct 2024 01:44:59 GMT  
		Size: 49.5 MB (49478102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a543e4a77995b18667e3ce720c44d3f0e07160a7e910559184a9dd7fe0bb9484`  
		Last Modified: Wed, 02 Oct 2024 01:45:28 GMT  
		Size: 157.6 MB (157603332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9080b3fa5c7e031077d09cd1aa67f9d05d99a53aed134674352053088aa37937
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.7 MB (287690780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a835fd6185ddf21f8309db2fbf6d7b6eececcda785fc939aa3f1dbf5a9fb2ad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:58:05 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:58:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:58:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:58:05 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:58:07 GMT
ADD file:cd1dbd2cf0195cc6d4674a585350e1a69fa96a310f6fcb1779824f40d9dad7bc in / 
# Wed, 18 Sep 2024 03:58:07 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:12:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:13:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:16:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:72b0311f761c1205ff38132f7ac025264668a60de0df6534b9df12be50456e88`  
		Last Modified: Wed, 02 Oct 2024 01:19:01 GMT  
		Size: 34.9 MB (34865505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c979bceba7fb77a741cad6add3eca7d109f0cf2e792a5c57571d7064a3f03c71`  
		Last Modified: Wed, 02 Oct 2024 01:18:59 GMT  
		Size: 18.1 MB (18135893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbeccf52d0c7d95f1cd621b4538c19cfff5867e52d01d5a00f759a459ea28999`  
		Last Modified: Wed, 02 Oct 2024 01:19:14 GMT  
		Size: 46.4 MB (46434300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925c4202924345a21194a077f853b64ce8ee8e676a6e91001d61fbc28dad6ba0`  
		Last Modified: Wed, 02 Oct 2024 01:19:40 GMT  
		Size: 188.3 MB (188255082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1d2786b9534cd8ff21466912c2ae42c51e750cf7793219433622506e44175cdb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.4 MB (309380326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92bc9f5ab72cde0cb37715560656f77831a32ee257219f9c207b0ee8a3062492`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:58:02 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:58:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:58:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:58:02 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:58:06 GMT
ADD file:06706071c1ca331eeb46804ea489d12de04ca8396c988aa1af4d825df23c914f in / 
# Wed, 18 Sep 2024 03:58:07 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:49:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:50:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:53:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c0f97a4c53879ae9596685c5148411bf1641cf2669742e2cee166f7f64c53a58`  
		Last Modified: Wed, 02 Oct 2024 01:56:52 GMT  
		Size: 39.7 MB (39734765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bedcd74e68335e2c9fe642408c79f74b5df03e0a2884bdc5f4644390b075c6`  
		Last Modified: Wed, 02 Oct 2024 01:56:48 GMT  
		Size: 20.2 MB (20164867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09f090381214fba1abf5d6db78c3189b6ac1fc85765a40e6be5d83b7160a433`  
		Last Modified: Wed, 02 Oct 2024 01:57:09 GMT  
		Size: 51.8 MB (51772787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce954ce4c7e576b190694854b8f4ad4e44769c2ab96b6082ebb32f9a11300207`  
		Last Modified: Wed, 02 Oct 2024 01:57:47 GMT  
		Size: 197.7 MB (197707907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:b8de50a98489d37d99d315cf2bb8771efdb7cf7fea091eef922c49b4161fa536
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.0 MB (389023176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8032fabfec89a24ffed66b5a643c9ac7eff935f42ee7bfd8aed16d3f6a77156`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 04:00:09 GMT
ARG RELEASE
# Fri, 13 Sep 2024 04:00:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 04:00:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 04:00:09 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 04:00:42 GMT
ADD file:fe1b6caff13e4673435edd0393d6a3f32627418ddd1d4f581d953510f87f8aa9 in / 
# Fri, 13 Sep 2024 04:00:44 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 02:21:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 02:23:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 02:30:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:adf60c3ca2ea943019774faf982dba804d10a64bd1a899c7b02591ef2bacbd23`  
		Last Modified: Tue, 17 Sep 2024 02:42:56 GMT  
		Size: 38.5 MB (38532888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d94ca004400cea4a3b19ceb645b60b2f4123c2ce8d0e9a3e087262598d72363`  
		Last Modified: Tue, 17 Sep 2024 02:42:44 GMT  
		Size: 15.8 MB (15825384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10db76789a2225592ba3f2c14ad9b00436b5d8aa72d91ad76d779dbdb33026fb`  
		Last Modified: Tue, 17 Sep 2024 02:43:56 GMT  
		Size: 55.0 MB (54968797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41f993555922f589e5a2ccb58922282904a47cf97af5b42a198c162bfb51304`  
		Last Modified: Tue, 17 Sep 2024 02:49:11 GMT  
		Size: 279.7 MB (279696107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c1b94bfaa2e56c7aeaff52679ff4779a169746a2e6cbb4def3d569a168e7f1f4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271908522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543c8cdf61067f50de3da9ea6a9ca70cb685f31fc28f2c8d4858b1aebc73e8ad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:57:27 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:57:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:57:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:57:27 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:57:28 GMT
ADD file:e41c6d9ae5268de87153f5edfcf09d55f5acd46b261a676b5cdd694b2af56a03 in / 
# Wed, 18 Sep 2024 03:57:28 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:35:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:36:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:38:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1102db7038079f87ec003c3def579ef89f3b072fdf2b6bfd0548fa36007abe8e`  
		Last Modified: Wed, 02 Oct 2024 01:40:19 GMT  
		Size: 34.6 MB (34600471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5d6e54a4c0cd66c7247eca1290a229ee261c7fafb8f9c53eb08ded7414fc84`  
		Last Modified: Wed, 02 Oct 2024 01:40:17 GMT  
		Size: 19.2 MB (19245230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f66afb7703de047378bbcd7202a18143aa8936962a5cb32c6625771ab85206`  
		Last Modified: Wed, 02 Oct 2024 01:40:31 GMT  
		Size: 47.9 MB (47891767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38f9b9a4e4d09843427eb68bed83f636b885ed208222043fe011670735db076`  
		Last Modified: Wed, 02 Oct 2024 01:40:58 GMT  
		Size: 170.2 MB (170171054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
