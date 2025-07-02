## `buildpack-deps:jammy`

```console
$ docker pull buildpack-deps@sha256:2dc0637787906095ab5fa95181947c358ccdd4728eae9425439657bddce90c19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:jammy` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5d4011b61505d673a5350c9f2ad53747ea92d9d0491082932d364afd6958f82b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.0 MB (249046275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3cc43003aeef75235ad5392fd52e005118705e2721cadad8722be062033206`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678e87101798c1c992d7c441a146a64a4a76a20702382a0e0ad72a873e291446`  
		Last Modified: Wed, 02 Jul 2025 03:09:59 GMT  
		Size: 7.1 MB (7103261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a1aa76818dce63f07dd58dd5d43f128f03c6e179946ade2073fc935ecfd682`  
		Last Modified: Wed, 02 Jul 2025 04:11:46 GMT  
		Size: 39.5 MB (39485981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e869816fab3c2d9c5f91c219b2a3dd7f517ff81251a7f6ad17ec0593e3d0a1`  
		Last Modified: Wed, 02 Jul 2025 07:21:22 GMT  
		Size: 172.9 MB (172921347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0f2d4a4458d62bbca2e380eac4150684c0f08c1a7ca69edf857c4d6e0c563821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11849589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfed42c3d5d803a5f5c43faea9d1b7317fd66c600787a3d1ea1fddb13a9e0b38`

```dockerfile
```

-	Layers:
	-	`sha256:b299ac9832063d5a633eb540d4bcf8c87876a763bd498f5653c03d14b54753d3`  
		Last Modified: Wed, 02 Jul 2025 07:19:23 GMT  
		Size: 11.8 MB (11839386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2171e1db7eabed5a642736b6544a8201282ea7331ac8ec935b6122abfa356a53`  
		Last Modified: Wed, 02 Jul 2025 07:19:24 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0ecaf0b6a4863c60e6e5fbfa16401b54cb5c40780fda83b92f8c4ed3a1075de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.3 MB (216272175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23c665a5f02f996dfcab2429f6f7bee3cad34482478e9c2c06cb8ef2918d840`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:ae409b4c753aab53fbf5e46b332d29d614f9ed31f53ec79d39ec3fbf2d659151 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:446fe3fba694631d6dbb9bee9d2a2a5c22c79cba078007ea85d822fb4083a291`  
		Last Modified: Wed, 02 Jul 2025 09:16:19 GMT  
		Size: 26.6 MB (26642498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44793a28e493f85253cf4a362d676e8f72bc75cc19d68d009cf83da67ba00b18`  
		Last Modified: Wed, 02 Jul 2025 10:20:37 GMT  
		Size: 7.0 MB (7007547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7985036e44b083c2805969377e41fadbd2c507b1230b2f71ed066da3d08edaa`  
		Last Modified: Wed, 02 Jul 2025 11:10:11 GMT  
		Size: 42.3 MB (42250104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a467ac1d4361359a083b1e0251ec09e3958b484fb37827d0d5f7f11700784b`  
		Last Modified: Wed, 02 Jul 2025 13:32:19 GMT  
		Size: 140.4 MB (140372026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c0291643c7d178050fa6819964bc612f7cd56a1221e27920d85f7fb8d0bb88cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11638874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d6e4d9a6bddb0168317978042d271e99f4b4544c99b97ccb3599e7ed8d3582`

```dockerfile
```

-	Layers:
	-	`sha256:c256d59ce0e34d4c65710b41e965ef629e8cac8dfb471fdd9098b92ab1f77327`  
		Last Modified: Wed, 02 Jul 2025 13:19:27 GMT  
		Size: 11.6 MB (11628611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b418c1761b745315ed2e9a97a9b2bc368f787d98acff29aa7fc7861acc5620e`  
		Last Modified: Wed, 02 Jul 2025 13:19:28 GMT  
		Size: 10.3 KB (10263 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6497a7f91965c3ef0572cbf2b63fd78485319e5890ba42739143af3c213dcc3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240175722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10b1f5ea084cbea09dfaadd4dc8e3cae7fe29142497bd81f952068043a37399d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44131f96e79008ec3b856a988d4d1fc58f4660f7ca12f41dfc747b162fe5ac2b`  
		Last Modified: Wed, 02 Jul 2025 04:18:53 GMT  
		Size: 7.0 MB (7049144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75659a4f0d38b8a15e802e7c5cddf95ad4371c4d4c4360e9c8fc87b7ad6f3f10`  
		Last Modified: Wed, 02 Jul 2025 07:36:17 GMT  
		Size: 39.4 MB (39380645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78acd7149489fab19a434a6be9337a442489ffeebbab99fe999a2b2ef9744dca`  
		Last Modified: Wed, 02 Jul 2025 16:43:59 GMT  
		Size: 166.4 MB (166386661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e6c6f7097a5eb48a9b0c8294c1c238634386c9f33d7b67efcb34bc14760c9a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11845336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83be9c4e3cf3b450bbe49482b3b3ebaddf1c29bb8b323c437ebffceccd69037c`

```dockerfile
```

-	Layers:
	-	`sha256:d8fe60e7c66122ec56da9cda94d173cfc9811678bfdac611a74708b596f3ab32`  
		Last Modified: Wed, 02 Jul 2025 16:19:34 GMT  
		Size: 11.8 MB (11835053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9dc31cfe9e39ae6b683da2608be51fe3e19af4d00247834b5f1fcdec15fcb2e`  
		Last Modified: Wed, 02 Jul 2025 16:19:35 GMT  
		Size: 10.3 KB (10283 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8b7ca80686c4406df33eadf6f05189bd76a553f4a422ee1eaa99e679f096c11c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269782279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5aeeeae16fa864a6999b2c1c0373f4c6932b948840cf49f87af215987aa13e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa2f9318738f3e4745fb8820b87dd05a41b99285bed1820fc6d1741f50edfd6`  
		Last Modified: Wed, 02 Jul 2025 03:09:58 GMT  
		Size: 8.2 MB (8181165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfd2a5f4efcf40a954b3ffecb64526e1b4b9dba6c19488754a9bb57b5ef9e90`  
		Last Modified: Wed, 02 Jul 2025 05:09:09 GMT  
		Size: 43.8 MB (43766786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98b3471c3dd58a33041822b9a4d270b67327b0b447f0bca6d114bc88055c624`  
		Last Modified: Wed, 02 Jul 2025 14:26:34 GMT  
		Size: 183.4 MB (183391707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f77e8dee8430f06b12c48bee0168cde0e327b4bc384904fb512a3cdc3f75ed64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11808986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47e6a43679e14ddd51c5d72d2071f5e95b0cffc51f3d5b9d71d52bf22776fbf`

```dockerfile
```

-	Layers:
	-	`sha256:24346582c8f31c675e4923f854b493d10dd36ab8447a12add60be7379b5fdfaa`  
		Last Modified: Wed, 02 Jul 2025 16:19:43 GMT  
		Size: 11.8 MB (11798751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c69f97962a028d6664717bf0583c4db723ad1975423f3740f4edc2f6ba5b4d1`  
		Last Modified: Wed, 02 Jul 2025 16:19:43 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:ba2f23ad6ba5604c91b2d8d881cedc20c543938c77acc1b5107d426b161e2582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274240485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d3e4dee54020a6c34556d7430a1ec74f4f051408d162d93a3d009d4f7397e5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:0ded5e5d9800a3ca1fc6792130ca0e401e0261a23680af38f712027491983279 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:dd93a8b5e7738819eda172cffad1b4d261aaf297806a57d80d1554e15f7f974c`  
		Last Modified: Wed, 02 Jul 2025 01:15:23 GMT  
		Size: 27.0 MB (27041006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b1bda053366ed50c1b86a21bf7cb4fbc00d26d03ec2e958c6018096098af67d`  
		Last Modified: Wed, 02 Jul 2025 03:11:43 GMT  
		Size: 7.1 MB (7116147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65a835443a6dae65841e6a022353da8bbef5344693459fd79d37f5cab1d17cd`  
		Last Modified: Wed, 02 Jul 2025 06:23:08 GMT  
		Size: 42.3 MB (42303013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7908829086e02665b3cb905261dd84786eeb2f9b581ccdd2f0d4ac93e109f03`  
		Last Modified: Wed, 02 Jul 2025 13:06:02 GMT  
		Size: 197.8 MB (197780319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:175a0496324dba563c7e346ed416f5a05407b2543c7f081d2ec9493bd977f9fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11789990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004a88a05f0e506231dca145884a9dbcb36472ca8807436579f266a1899ac12f`

```dockerfile
```

-	Layers:
	-	`sha256:b1733cae741f16295d07491d2d29fba0fdc7fa3d7ff449314b15594d766512fa`  
		Last Modified: Wed, 02 Jul 2025 10:19:44 GMT  
		Size: 11.8 MB (11779755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db9e5079627d2d8b99015b8ca8d24f8fc5e14ecbfff3768b100cae0a19cfb5c8`  
		Last Modified: Wed, 02 Jul 2025 10:19:44 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c21661e9c853d3299ae434a9134e9b6a3d3262c3442413a2e3474731740550c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (223018304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e756361ceaf57210557c4c2b132676b68dc8db15b20bf7f45ac145d41dda23`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:dad9a012cce363ba4f28e2a6f3efa82869330e872362e4867be1bd507ed8963a in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8d24804db3a6eaf32ea752d2dd82fb21273e4e2494ca124217c93f38bc823ca5`  
		Last Modified: Wed, 02 Jul 2025 03:43:01 GMT  
		Size: 28.0 MB (28002175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bdee4a43a9907ec4877c229f815931c1f4c005f17fb7d5bb41d54c28390815a`  
		Last Modified: Wed, 02 Jul 2025 04:11:58 GMT  
		Size: 7.0 MB (7014175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b2fb90aff9aa834bf3f9bc9e88ea2f6ae42d37f950666624e6bb57f7ca47bb`  
		Last Modified: Wed, 02 Jul 2025 05:18:51 GMT  
		Size: 39.4 MB (39421678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe995d8a301d985f4d6e19ef9faf3ee5685bec05b42f6a03b872f206db4140f`  
		Last Modified: Wed, 02 Jul 2025 13:06:03 GMT  
		Size: 148.6 MB (148580276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bc951b888c55085e7f867c5d56e31a041c3c607c6723fff6d6760456d7c4eed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11663478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f1220dbfc602b85cfd0c4ba9a23325b39886ec7fada742cc25d249183c0c628`

```dockerfile
```

-	Layers:
	-	`sha256:94816457570f4b133b32b09a329706dc489d7449bb2c0a803e2e618e3762c374`  
		Last Modified: Wed, 02 Jul 2025 10:19:52 GMT  
		Size: 11.7 MB (11653275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4a42b439a36dd014e24f51d40abb6c45628f58a8ce4a75520046db4b4b0e64c`  
		Last Modified: Wed, 02 Jul 2025 10:19:52 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json
