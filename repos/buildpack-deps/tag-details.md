<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `buildpack-deps`

-	[`buildpack-deps:18.04`](#buildpack-deps1804)
-	[`buildpack-deps:18.04-curl`](#buildpack-deps1804-curl)
-	[`buildpack-deps:18.04-scm`](#buildpack-deps1804-scm)
-	[`buildpack-deps:20.04`](#buildpack-deps2004)
-	[`buildpack-deps:20.04-curl`](#buildpack-deps2004-curl)
-	[`buildpack-deps:20.04-scm`](#buildpack-deps2004-scm)
-	[`buildpack-deps:22.04`](#buildpack-deps2204)
-	[`buildpack-deps:22.04-curl`](#buildpack-deps2204-curl)
-	[`buildpack-deps:22.04-scm`](#buildpack-deps2204-scm)
-	[`buildpack-deps:22.10`](#buildpack-deps2210)
-	[`buildpack-deps:22.10-curl`](#buildpack-deps2210-curl)
-	[`buildpack-deps:22.10-scm`](#buildpack-deps2210-scm)
-	[`buildpack-deps:23.04`](#buildpack-deps2304)
-	[`buildpack-deps:23.04-curl`](#buildpack-deps2304-curl)
-	[`buildpack-deps:23.04-scm`](#buildpack-deps2304-scm)
-	[`buildpack-deps:bionic`](#buildpack-depsbionic)
-	[`buildpack-deps:bionic-curl`](#buildpack-depsbionic-curl)
-	[`buildpack-deps:bionic-scm`](#buildpack-depsbionic-scm)
-	[`buildpack-deps:bookworm`](#buildpack-depsbookworm)
-	[`buildpack-deps:bookworm-curl`](#buildpack-depsbookworm-curl)
-	[`buildpack-deps:bookworm-scm`](#buildpack-depsbookworm-scm)
-	[`buildpack-deps:bullseye`](#buildpack-depsbullseye)
-	[`buildpack-deps:bullseye-curl`](#buildpack-depsbullseye-curl)
-	[`buildpack-deps:bullseye-scm`](#buildpack-depsbullseye-scm)
-	[`buildpack-deps:buster`](#buildpack-depsbuster)
-	[`buildpack-deps:buster-curl`](#buildpack-depsbuster-curl)
-	[`buildpack-deps:buster-scm`](#buildpack-depsbuster-scm)
-	[`buildpack-deps:curl`](#buildpack-depscurl)
-	[`buildpack-deps:focal`](#buildpack-depsfocal)
-	[`buildpack-deps:focal-curl`](#buildpack-depsfocal-curl)
-	[`buildpack-deps:focal-scm`](#buildpack-depsfocal-scm)
-	[`buildpack-deps:jammy`](#buildpack-depsjammy)
-	[`buildpack-deps:jammy-curl`](#buildpack-depsjammy-curl)
-	[`buildpack-deps:jammy-scm`](#buildpack-depsjammy-scm)
-	[`buildpack-deps:kinetic`](#buildpack-depskinetic)
-	[`buildpack-deps:kinetic-curl`](#buildpack-depskinetic-curl)
-	[`buildpack-deps:kinetic-scm`](#buildpack-depskinetic-scm)
-	[`buildpack-deps:latest`](#buildpack-depslatest)
-	[`buildpack-deps:lunar`](#buildpack-depslunar)
-	[`buildpack-deps:lunar-curl`](#buildpack-depslunar-curl)
-	[`buildpack-deps:lunar-scm`](#buildpack-depslunar-scm)
-	[`buildpack-deps:oldstable`](#buildpack-depsoldstable)
-	[`buildpack-deps:oldstable-curl`](#buildpack-depsoldstable-curl)
-	[`buildpack-deps:oldstable-scm`](#buildpack-depsoldstable-scm)
-	[`buildpack-deps:scm`](#buildpack-depsscm)
-	[`buildpack-deps:sid`](#buildpack-depssid)
-	[`buildpack-deps:sid-curl`](#buildpack-depssid-curl)
-	[`buildpack-deps:sid-scm`](#buildpack-depssid-scm)
-	[`buildpack-deps:stable`](#buildpack-depsstable)
-	[`buildpack-deps:stable-curl`](#buildpack-depsstable-curl)
-	[`buildpack-deps:stable-scm`](#buildpack-depsstable-scm)
-	[`buildpack-deps:testing`](#buildpack-depstesting)
-	[`buildpack-deps:testing-curl`](#buildpack-depstesting-curl)
-	[`buildpack-deps:testing-scm`](#buildpack-depstesting-scm)
-	[`buildpack-deps:unstable`](#buildpack-depsunstable)
-	[`buildpack-deps:unstable-curl`](#buildpack-depsunstable-curl)
-	[`buildpack-deps:unstable-scm`](#buildpack-depsunstable-scm)

## `buildpack-deps:18.04`

```console
$ docker pull buildpack-deps@sha256:fb154449c96034e2ac28a113cfbc31b7da0e4a21387c397dec6b1deec6d89d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:18.04` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b1da6a5f500b67fa28bbae2b90a8e9da4def283d1fb918b1d4db0c9cd86ec183
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 MB (221417037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeecfa359fe257650879cc03de2c96ee1ab252d40eaf9467a855893ac7df28f5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:22:42 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:22:44 GMT
ADD file:4560926e076acae6b8396a9f1e760eee0f53e22e90ce8554dda57f1103547795 in / 
# Wed, 08 Mar 2023 03:22:44 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:21:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:21:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 05:22:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:24:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cd150c608fee7837e3a5b28be5c7b540eaf4efa27b3b755d55326470691ce2df`  
		Last Modified: Sun, 12 Mar 2023 07:24:55 GMT  
		Size: 26.7 MB (26710746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c78e6dac9cec3c01ca7687f8e0a53a4b5e9b04f4910729279be4204ce5360e`  
		Last Modified: Thu, 16 Mar 2023 05:41:29 GMT  
		Size: 6.6 MB (6617364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b18b892afad36455b3ae75f0ab2c1bc45822e03069f2667faa4bede3825be5`  
		Last Modified: Thu, 16 Mar 2023 05:41:28 GMT  
		Size: 3.0 MB (3026128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c57462ca1fd8565d56aa476a7fa497011a11c6f761194b368d2c722e146b20`  
		Last Modified: Thu, 16 Mar 2023 05:41:43 GMT  
		Size: 45.5 MB (45514749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f391d58903094b86c56fd169ec96c398321c3ccab4f8893113f4de938d003a`  
		Last Modified: Thu, 16 Mar 2023 05:42:10 GMT  
		Size: 139.5 MB (139548050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:18.04` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1f740f07a329775404244fd36ca65500a61ecd79c38851ee6ce6408443fa9779
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189581013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb26767826b27bb17bc813102a23903c31d4ea475f341486310a77dd6e54d766`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:27:01 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:27:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:27:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:27:01 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:27:08 GMT
ADD file:21d7947367fe1aa8cc668c943d11c4841b0ead14b9103ef46fb8db8084603a75 in / 
# Wed, 08 Mar 2023 03:27:09 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:44:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:45:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 03:45:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:47:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9fb42489e9f507aa183ef669baec25f94b8c4c22159a4ccc23a1977cedd0d1fa`  
		Last Modified: Thu, 16 Mar 2023 03:39:03 GMT  
		Size: 22.3 MB (22305374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2b71966fc2f22e1375423fb61221ed137cf5e7e8d202bfa403292ba600daab`  
		Last Modified: Thu, 16 Mar 2023 04:07:46 GMT  
		Size: 5.7 MB (5681012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebcf04b4bbda07472ffbb83ab11cb71b6ff2c6bef9749979a8a3981f285c0f53`  
		Last Modified: Thu, 16 Mar 2023 04:07:46 GMT  
		Size: 2.6 MB (2586979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3058bdcdd1b82bda414133ce433d46f98b5f56911e44f00ff6bd1de1c0a6caba`  
		Last Modified: Thu, 16 Mar 2023 04:08:04 GMT  
		Size: 40.7 MB (40713543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d88abc5604e52bcee192566d8fae426f1031f855abd4229bd8c43feeb2648d`  
		Last Modified: Thu, 16 Mar 2023 04:08:30 GMT  
		Size: 118.3 MB (118294105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:18.04` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2c9e464ea859a1b832272828463904e3f9c04bdebf0e7aa9cdc4c6c48481c85e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (206011203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b97289739597eaf439933630ebefa90822ac12cd90c8157a55e7b3f32763f4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:25:33 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:25:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:25:35 GMT
ADD file:5f229d85bac2e85aa7ce97b2168fc61bd401d0151e8940a12d244356f984e65f in / 
# Wed, 08 Mar 2023 03:25:35 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:58:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:58:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 03:59:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:02:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c21a0233221a76e66b6c10d2445f591bd28eb0773e6cb539474d6dca9ea0b594`  
		Last Modified: Sun, 12 Mar 2023 07:27:31 GMT  
		Size: 23.7 MB (23734706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc06fc1cf8ad0140062ec53dbc631cea853ddb72d7c0b353edd743b1dca4ceb`  
		Last Modified: Thu, 16 Mar 2023 04:21:50 GMT  
		Size: 6.1 MB (6057809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33d0b4e623a1829e474acf7b4d21109a9f27c7d8c8bf12f163ffe645eed93ec`  
		Last Modified: Thu, 16 Mar 2023 04:21:49 GMT  
		Size: 2.8 MB (2790695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37de71f159d52bbc91be8b71a2d8862f89e2c137ac5d4e17c923aaa4fa5aa30`  
		Last Modified: Thu, 16 Mar 2023 04:22:03 GMT  
		Size: 43.3 MB (43311869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc13acad8ae8946317f508f7e0eda6de200ca13831f7433e58942f2466c21473`  
		Last Modified: Thu, 16 Mar 2023 04:22:25 GMT  
		Size: 130.1 MB (130116124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:18.04` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d189ba12fe145c64ea06852f5de7d0ab170ab04daca4c5effd4a4705cabb888e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 MB (218710648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc3d7329f212c3056b20a7f0084491a4e3d07e63c6848a789189f5137e2d75d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:13:19 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:13:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:13:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:13:19 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:13:21 GMT
ADD file:6cf3e34995c6c44762ed692b86a0442d981e9a69fa4288960047e505d75c0223 in / 
# Wed, 08 Mar 2023 03:13:22 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:56:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:56:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 01:57:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:00:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c58af8b772f2ca9c63db81d620e48946c13c027ecd7ab2d9062d010ca2ed11f3`  
		Last Modified: Thu, 16 Mar 2023 01:54:42 GMT  
		Size: 27.2 MB (27164610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1df9a7dbeea70a625098ba195b5c6a6046e010992d4b2616b74e5efca85ff0`  
		Last Modified: Thu, 16 Mar 2023 02:02:18 GMT  
		Size: 6.9 MB (6907798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9c7488bcb45de5faeb1bc3f4a19015817de4a09d3c762c619d48aa2855322e`  
		Last Modified: Thu, 16 Mar 2023 02:02:17 GMT  
		Size: 3.3 MB (3255693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54663dad9d7f237e7f0a0a533af683ae66d66098cdd57ea8f90fde4dd8897ffb`  
		Last Modified: Thu, 16 Mar 2023 02:02:38 GMT  
		Size: 47.1 MB (47095486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5e9e49852091a0f82ca614c93efb7802ff6bbabc0da2e14b9606920c072cb6`  
		Last Modified: Thu, 16 Mar 2023 02:03:15 GMT  
		Size: 134.3 MB (134287061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:18.04` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:093d533487c60b2c92363199f07f041884638f879f09c20c9aa303e056b1267c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246441203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dcd83e221d1f7aaec4fdcb03d7776c2eadf8d9cf89c85eaba5ab7f7793f25ed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:13:23 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:13:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:13:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:13:23 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:13:26 GMT
ADD file:5ea8615c09f693252cb9d45458421679f82f84d315200a7611165869195b3a69 in / 
# Wed, 08 Mar 2023 03:13:26 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:07:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:07:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 03:08:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:14:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1c668e1b654ae9320eeecdef5ebc0faea219f3828f6cd3a05983984863b60058`  
		Last Modified: Thu, 16 Mar 2023 01:43:01 GMT  
		Size: 30.4 MB (30441944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e5cf4c1f014d5508f129bb3d2e36a3448b5d92b400a35d3051160723af42b4`  
		Last Modified: Thu, 16 Mar 2023 03:47:41 GMT  
		Size: 7.0 MB (7036943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a259ed8117f57e3f76e8e31ddb857f6d36e8f1ac8131d38a456833aa7e0c20`  
		Last Modified: Thu, 16 Mar 2023 03:47:40 GMT  
		Size: 3.7 MB (3740612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409f528497ffaa0bc9ae78b8139359ddd38315caf439a39a670aaed487c6c06d`  
		Last Modified: Thu, 16 Mar 2023 03:48:07 GMT  
		Size: 53.7 MB (53736792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22095eabcbee3060dd218f09d76cf296a873b1a36d1d4f86794d105fe7e5ec5f`  
		Last Modified: Thu, 16 Mar 2023 03:48:53 GMT  
		Size: 151.5 MB (151484912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:18.04` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0c8e0a8e8c0a624863dcfee0278ed624183fd34de9612945d2db9d6842c229d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.8 MB (205782934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8557c42f5d0087a913e9c89b40998da81a7d55355bad38d52f6b3f7699f2681b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:23:29 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:23:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:23:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:23:29 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:23:31 GMT
ADD file:a6309e462d28398152cb726a11615118d79858da963b8c614772b87d87465967 in / 
# Wed, 08 Mar 2023 03:23:31 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:43:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:43:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 01:44:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:46:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3a2279f06ab19f0d57823e69b999f54a344e28bd9f955b4db9a5875c0caa543a`  
		Last Modified: Thu, 16 Mar 2023 02:01:03 GMT  
		Size: 25.4 MB (25370993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb37be097f66ed2ca5a62bf5e79eee23cbae99ae37fa4214bd021813206a4896`  
		Last Modified: Thu, 16 Mar 2023 02:01:00 GMT  
		Size: 6.3 MB (6310585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffee9aa0246535c2e55658c3cb0a6996668f7a403a4b960a9fdbcd4d42847f3`  
		Last Modified: Thu, 16 Mar 2023 02:00:59 GMT  
		Size: 3.0 MB (2976589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc2dd868684ceaf83a27108c1b52ca7a6e8f3b0168ad780911abc88235bfb03`  
		Last Modified: Thu, 16 Mar 2023 02:01:18 GMT  
		Size: 45.0 MB (45040946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df620083a573baec7672a8d7b904f0c02ababd741e0ace4108dda4b119901ee2`  
		Last Modified: Thu, 16 Mar 2023 02:01:42 GMT  
		Size: 126.1 MB (126083821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:18.04-curl`

```console
$ docker pull buildpack-deps@sha256:3fd8a96d4a8804a8424ff1593c4b2858231aa0c710e83e5c826fab6724f4037f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:18.04-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:edc4ef3195e1d82ba936e48a088384a87de4ef1e079743cf63a8590eb9a20bfd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36354238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c36747240a25171490608a4897f503021ceb197cb460e20444ca7089a2453ea7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:22:42 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:22:44 GMT
ADD file:4560926e076acae6b8396a9f1e760eee0f53e22e90ce8554dda57f1103547795 in / 
# Wed, 08 Mar 2023 03:22:44 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:21:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:21:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:cd150c608fee7837e3a5b28be5c7b540eaf4efa27b3b755d55326470691ce2df`  
		Last Modified: Sun, 12 Mar 2023 07:24:55 GMT  
		Size: 26.7 MB (26710746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c78e6dac9cec3c01ca7687f8e0a53a4b5e9b04f4910729279be4204ce5360e`  
		Last Modified: Thu, 16 Mar 2023 05:41:29 GMT  
		Size: 6.6 MB (6617364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b18b892afad36455b3ae75f0ab2c1bc45822e03069f2667faa4bede3825be5`  
		Last Modified: Thu, 16 Mar 2023 05:41:28 GMT  
		Size: 3.0 MB (3026128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:18.04-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:37305f1fffd9b6e8b98b050b702e595498870f5d0cf8cbc4d2e30cdcc7b2177a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30573365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45de6bc525f3e1c8327e7663ff847e537821bb211ca5fe282aa4fe66f79c36f8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:27:01 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:27:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:27:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:27:01 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:27:08 GMT
ADD file:21d7947367fe1aa8cc668c943d11c4841b0ead14b9103ef46fb8db8084603a75 in / 
# Wed, 08 Mar 2023 03:27:09 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:44:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:45:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:9fb42489e9f507aa183ef669baec25f94b8c4c22159a4ccc23a1977cedd0d1fa`  
		Last Modified: Thu, 16 Mar 2023 03:39:03 GMT  
		Size: 22.3 MB (22305374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2b71966fc2f22e1375423fb61221ed137cf5e7e8d202bfa403292ba600daab`  
		Last Modified: Thu, 16 Mar 2023 04:07:46 GMT  
		Size: 5.7 MB (5681012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebcf04b4bbda07472ffbb83ab11cb71b6ff2c6bef9749979a8a3981f285c0f53`  
		Last Modified: Thu, 16 Mar 2023 04:07:46 GMT  
		Size: 2.6 MB (2586979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:18.04-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bbaa8d87e02533fb9f0e332551bec711913649f23f663cb20c4c47c5323680f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32583210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3656a9cc190e6da3224283797ac375e158b4a022d1d5a3d2bb49d9dac0b85124`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:25:33 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:25:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:25:35 GMT
ADD file:5f229d85bac2e85aa7ce97b2168fc61bd401d0151e8940a12d244356f984e65f in / 
# Wed, 08 Mar 2023 03:25:35 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:58:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:58:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:c21a0233221a76e66b6c10d2445f591bd28eb0773e6cb539474d6dca9ea0b594`  
		Last Modified: Sun, 12 Mar 2023 07:27:31 GMT  
		Size: 23.7 MB (23734706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc06fc1cf8ad0140062ec53dbc631cea853ddb72d7c0b353edd743b1dca4ceb`  
		Last Modified: Thu, 16 Mar 2023 04:21:50 GMT  
		Size: 6.1 MB (6057809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33d0b4e623a1829e474acf7b4d21109a9f27c7d8c8bf12f163ffe645eed93ec`  
		Last Modified: Thu, 16 Mar 2023 04:21:49 GMT  
		Size: 2.8 MB (2790695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:18.04-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c88613067a38450529dace018781fd35548bed5b209c241a5262b458b0e48a52
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37328101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e48e7492b46c775c749e6d5febf5731b1aeface4bf187ab7edb99482a1e0f64`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:13:19 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:13:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:13:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:13:19 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:13:21 GMT
ADD file:6cf3e34995c6c44762ed692b86a0442d981e9a69fa4288960047e505d75c0223 in / 
# Wed, 08 Mar 2023 03:13:22 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:56:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:56:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:c58af8b772f2ca9c63db81d620e48946c13c027ecd7ab2d9062d010ca2ed11f3`  
		Last Modified: Thu, 16 Mar 2023 01:54:42 GMT  
		Size: 27.2 MB (27164610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1df9a7dbeea70a625098ba195b5c6a6046e010992d4b2616b74e5efca85ff0`  
		Last Modified: Thu, 16 Mar 2023 02:02:18 GMT  
		Size: 6.9 MB (6907798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9c7488bcb45de5faeb1bc3f4a19015817de4a09d3c762c619d48aa2855322e`  
		Last Modified: Thu, 16 Mar 2023 02:02:17 GMT  
		Size: 3.3 MB (3255693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:18.04-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:93af7cd2c9b2348c3885ca9fad668d06a219296d9c2032725a0d3de25878e908
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41219499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1588570491594531960cec00e2bb87f2fb1b48f878dc4d6bd888024f30e1de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:13:23 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:13:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:13:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:13:23 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:13:26 GMT
ADD file:5ea8615c09f693252cb9d45458421679f82f84d315200a7611165869195b3a69 in / 
# Wed, 08 Mar 2023 03:13:26 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:07:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:07:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:1c668e1b654ae9320eeecdef5ebc0faea219f3828f6cd3a05983984863b60058`  
		Last Modified: Thu, 16 Mar 2023 01:43:01 GMT  
		Size: 30.4 MB (30441944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e5cf4c1f014d5508f129bb3d2e36a3448b5d92b400a35d3051160723af42b4`  
		Last Modified: Thu, 16 Mar 2023 03:47:41 GMT  
		Size: 7.0 MB (7036943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a259ed8117f57e3f76e8e31ddb857f6d36e8f1ac8131d38a456833aa7e0c20`  
		Last Modified: Thu, 16 Mar 2023 03:47:40 GMT  
		Size: 3.7 MB (3740612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:18.04-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:20ebcda199381e882997d1cb49046a4a86cf2a4d85ec17a0d4cf03c2342dee11
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34658167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f626e5ed1171f12e2d4e06623f35558e748ecc2010eb93c132ab27524b2b55b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:23:29 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:23:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:23:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:23:29 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:23:31 GMT
ADD file:a6309e462d28398152cb726a11615118d79858da963b8c614772b87d87465967 in / 
# Wed, 08 Mar 2023 03:23:31 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:43:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:43:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3a2279f06ab19f0d57823e69b999f54a344e28bd9f955b4db9a5875c0caa543a`  
		Last Modified: Thu, 16 Mar 2023 02:01:03 GMT  
		Size: 25.4 MB (25370993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb37be097f66ed2ca5a62bf5e79eee23cbae99ae37fa4214bd021813206a4896`  
		Last Modified: Thu, 16 Mar 2023 02:01:00 GMT  
		Size: 6.3 MB (6310585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffee9aa0246535c2e55658c3cb0a6996668f7a403a4b960a9fdbcd4d42847f3`  
		Last Modified: Thu, 16 Mar 2023 02:00:59 GMT  
		Size: 3.0 MB (2976589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:18.04-scm`

```console
$ docker pull buildpack-deps@sha256:341aade2e27224f02ffa8406356d222ae812b4b877d9cae398a6f1c9c8aa1fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:18.04-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c5ed4186cca291cb15e4a3ec07c8f72214eecb664ab6000d21de81b4ef3c22eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81868987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee72242d4f5e40206fc21b1eda028beb28d7d73857bfdba0cc421a166b05b081`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:22:42 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:22:44 GMT
ADD file:4560926e076acae6b8396a9f1e760eee0f53e22e90ce8554dda57f1103547795 in / 
# Wed, 08 Mar 2023 03:22:44 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:21:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:21:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 05:22:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cd150c608fee7837e3a5b28be5c7b540eaf4efa27b3b755d55326470691ce2df`  
		Last Modified: Sun, 12 Mar 2023 07:24:55 GMT  
		Size: 26.7 MB (26710746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c78e6dac9cec3c01ca7687f8e0a53a4b5e9b04f4910729279be4204ce5360e`  
		Last Modified: Thu, 16 Mar 2023 05:41:29 GMT  
		Size: 6.6 MB (6617364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b18b892afad36455b3ae75f0ab2c1bc45822e03069f2667faa4bede3825be5`  
		Last Modified: Thu, 16 Mar 2023 05:41:28 GMT  
		Size: 3.0 MB (3026128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c57462ca1fd8565d56aa476a7fa497011a11c6f761194b368d2c722e146b20`  
		Last Modified: Thu, 16 Mar 2023 05:41:43 GMT  
		Size: 45.5 MB (45514749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:18.04-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1f9d5b0d3c5fb26bbcb17109b65208ac2a36d7a6a4253289e090c1e39fbe1744
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71286908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf91a3d86cf7e62586cfa021d5d042c3f8ad4473ddc03742ce5fe9199395303a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:27:01 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:27:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:27:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:27:01 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:27:08 GMT
ADD file:21d7947367fe1aa8cc668c943d11c4841b0ead14b9103ef46fb8db8084603a75 in / 
# Wed, 08 Mar 2023 03:27:09 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:44:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:45:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 03:45:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9fb42489e9f507aa183ef669baec25f94b8c4c22159a4ccc23a1977cedd0d1fa`  
		Last Modified: Thu, 16 Mar 2023 03:39:03 GMT  
		Size: 22.3 MB (22305374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2b71966fc2f22e1375423fb61221ed137cf5e7e8d202bfa403292ba600daab`  
		Last Modified: Thu, 16 Mar 2023 04:07:46 GMT  
		Size: 5.7 MB (5681012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebcf04b4bbda07472ffbb83ab11cb71b6ff2c6bef9749979a8a3981f285c0f53`  
		Last Modified: Thu, 16 Mar 2023 04:07:46 GMT  
		Size: 2.6 MB (2586979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3058bdcdd1b82bda414133ce433d46f98b5f56911e44f00ff6bd1de1c0a6caba`  
		Last Modified: Thu, 16 Mar 2023 04:08:04 GMT  
		Size: 40.7 MB (40713543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:18.04-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:127e2166fb2409edd8d8b5261a115a0e2aec1641f2bc70769b51e60924fda8eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75895079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c55e4c16477e8e6ec9875fa4a0fc1eb3184b34403fb222976e5a361d5ab3466`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:25:33 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:25:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:25:35 GMT
ADD file:5f229d85bac2e85aa7ce97b2168fc61bd401d0151e8940a12d244356f984e65f in / 
# Wed, 08 Mar 2023 03:25:35 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:58:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:58:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 03:59:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c21a0233221a76e66b6c10d2445f591bd28eb0773e6cb539474d6dca9ea0b594`  
		Last Modified: Sun, 12 Mar 2023 07:27:31 GMT  
		Size: 23.7 MB (23734706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc06fc1cf8ad0140062ec53dbc631cea853ddb72d7c0b353edd743b1dca4ceb`  
		Last Modified: Thu, 16 Mar 2023 04:21:50 GMT  
		Size: 6.1 MB (6057809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33d0b4e623a1829e474acf7b4d21109a9f27c7d8c8bf12f163ffe645eed93ec`  
		Last Modified: Thu, 16 Mar 2023 04:21:49 GMT  
		Size: 2.8 MB (2790695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37de71f159d52bbc91be8b71a2d8862f89e2c137ac5d4e17c923aaa4fa5aa30`  
		Last Modified: Thu, 16 Mar 2023 04:22:03 GMT  
		Size: 43.3 MB (43311869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:18.04-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:06347734d5e392a96f4432d6290610b9761773fe58a4467957bb5ac5c104e085
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84423587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea41bed709b37c2011e131b1f224971e01f761e9a8b0c487987ca43d939e5062`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:13:19 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:13:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:13:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:13:19 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:13:21 GMT
ADD file:6cf3e34995c6c44762ed692b86a0442d981e9a69fa4288960047e505d75c0223 in / 
# Wed, 08 Mar 2023 03:13:22 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:56:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:56:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 01:57:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c58af8b772f2ca9c63db81d620e48946c13c027ecd7ab2d9062d010ca2ed11f3`  
		Last Modified: Thu, 16 Mar 2023 01:54:42 GMT  
		Size: 27.2 MB (27164610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1df9a7dbeea70a625098ba195b5c6a6046e010992d4b2616b74e5efca85ff0`  
		Last Modified: Thu, 16 Mar 2023 02:02:18 GMT  
		Size: 6.9 MB (6907798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9c7488bcb45de5faeb1bc3f4a19015817de4a09d3c762c619d48aa2855322e`  
		Last Modified: Thu, 16 Mar 2023 02:02:17 GMT  
		Size: 3.3 MB (3255693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54663dad9d7f237e7f0a0a533af683ae66d66098cdd57ea8f90fde4dd8897ffb`  
		Last Modified: Thu, 16 Mar 2023 02:02:38 GMT  
		Size: 47.1 MB (47095486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:18.04-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:47ffaea8984e18680bf34023dc84dbbc005a5c50b47cb92e9221be8e55ce28a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (94956291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e8cb730f01b5b2426648fed56c18477b531abea23c6d47db1eacc88079b2ab4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:13:23 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:13:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:13:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:13:23 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:13:26 GMT
ADD file:5ea8615c09f693252cb9d45458421679f82f84d315200a7611165869195b3a69 in / 
# Wed, 08 Mar 2023 03:13:26 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:07:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:07:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 03:08:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1c668e1b654ae9320eeecdef5ebc0faea219f3828f6cd3a05983984863b60058`  
		Last Modified: Thu, 16 Mar 2023 01:43:01 GMT  
		Size: 30.4 MB (30441944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e5cf4c1f014d5508f129bb3d2e36a3448b5d92b400a35d3051160723af42b4`  
		Last Modified: Thu, 16 Mar 2023 03:47:41 GMT  
		Size: 7.0 MB (7036943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a259ed8117f57e3f76e8e31ddb857f6d36e8f1ac8131d38a456833aa7e0c20`  
		Last Modified: Thu, 16 Mar 2023 03:47:40 GMT  
		Size: 3.7 MB (3740612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409f528497ffaa0bc9ae78b8139359ddd38315caf439a39a670aaed487c6c06d`  
		Last Modified: Thu, 16 Mar 2023 03:48:07 GMT  
		Size: 53.7 MB (53736792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:18.04-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3e5c483b07d9d0b5a4f4dbb989320ab32f2ccc83e8b565759f680a7659b1961c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79699113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d8b61386e03e4309345be55e3dd943e007820aadcbcc64fb24e1524fea86052`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:23:29 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:23:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:23:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:23:29 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:23:31 GMT
ADD file:a6309e462d28398152cb726a11615118d79858da963b8c614772b87d87465967 in / 
# Wed, 08 Mar 2023 03:23:31 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:43:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:43:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 01:44:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3a2279f06ab19f0d57823e69b999f54a344e28bd9f955b4db9a5875c0caa543a`  
		Last Modified: Thu, 16 Mar 2023 02:01:03 GMT  
		Size: 25.4 MB (25370993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb37be097f66ed2ca5a62bf5e79eee23cbae99ae37fa4214bd021813206a4896`  
		Last Modified: Thu, 16 Mar 2023 02:01:00 GMT  
		Size: 6.3 MB (6310585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffee9aa0246535c2e55658c3cb0a6996668f7a403a4b960a9fdbcd4d42847f3`  
		Last Modified: Thu, 16 Mar 2023 02:00:59 GMT  
		Size: 3.0 MB (2976589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc2dd868684ceaf83a27108c1b52ca7a6e8f3b0168ad780911abc88235bfb03`  
		Last Modified: Thu, 16 Mar 2023 02:01:18 GMT  
		Size: 45.0 MB (45040946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:20.04`

```console
$ docker pull buildpack-deps@sha256:838634b0a7daabf564f087e7f9b5818c7b3ae9312cc42908e8fd7fd4317cd638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:20.04` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:dd5e6240f9fcbcbe0f6f1a3405b40d0ab6e82fbe91909deaa1212cc65b48f1da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245783085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37352ea462c043f4e445123486977b7b52534da3dd5e19c44166e8f46f245097`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:23:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:23:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:24:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:25:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb9a1000294d18d6dc41a0282435b987380b7f0b46c7f3dc891087e1a473ce2`  
		Last Modified: Tue, 18 Apr 2023 01:34:39 GMT  
		Size: 7.7 MB (7744253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986bdd8de236de34e3a40a899fbcd02bedbc9de7f3b6ced517c2fa4149ab0fdd`  
		Last Modified: Tue, 18 Apr 2023 01:34:38 GMT  
		Size: 3.6 MB (3627203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a87a85bf796c479f3384f9845bbb9da0e19847e85730eef87d5e68561f7c9d`  
		Last Modified: Tue, 18 Apr 2023 01:34:59 GMT  
		Size: 60.7 MB (60745533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c05a097a1be622d326505e77f9094db55692396eeea49cabc0f2d782e8c4dd`  
		Last Modified: Tue, 18 Apr 2023 01:35:27 GMT  
		Size: 145.1 MB (145087533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:10cc7efff129069f31d402ddacdbf482a876e5419831f90619e7e6b457f80e55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.8 MB (211791715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c67b859cc6a4bbe955c191558f0017a32648ececc20276b3da75e1f2563a037`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:47 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:20:50 GMT
ADD file:0da456bd328984fcedf5367b46a38da6ca4b43061baf6d1283380962cddc7481 in / 
# Thu, 13 Apr 2023 13:20:50 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:34:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:34:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:35:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:38:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e68c91cb250f35160f683afa80c3ada46f06948ded46a188be490ea3afff08f5`  
		Last Modified: Fri, 14 Apr 2023 09:34:28 GMT  
		Size: 24.6 MB (24586976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029732d3be1a924e821f7cd01afe768f39d85e2d484ace5bcceab5fbc250c347`  
		Last Modified: Tue, 18 Apr 2023 01:49:22 GMT  
		Size: 6.7 MB (6729180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df6a23fdc52b8fc5a75f036a53f4c9f7a7e07c603fe5a73ba891f8dee1a7505`  
		Last Modified: Tue, 18 Apr 2023 01:49:21 GMT  
		Size: 3.1 MB (3104419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21583b635c301612839572600eb97628067e10e4fd4af5803b399abbcbfc8054`  
		Last Modified: Tue, 18 Apr 2023 01:49:41 GMT  
		Size: 55.4 MB (55443791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49765b1a78a05ff3d4d223bda34a4d9e7223b0de368ac54afe942a68f60b9e29`  
		Last Modified: Tue, 18 Apr 2023 01:50:07 GMT  
		Size: 121.9 MB (121927349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f49b29319819b63c4b870e6272eddc5c21fbefb46d5e0b521909247ce724e230
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (235991114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9d124be76c767ac4c947fc3428ac1d7b0af211d5140cbe2f0390bc20ea03aa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:20:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:20:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:20:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:23:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2378679266ac5157323158b6e52e7a884e559db5217037e57992e47a1667d525`  
		Last Modified: Fri, 14 Apr 2023 07:39:20 GMT  
		Size: 27.2 MB (27196396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fee697311c4e091f41acde237da003390953c6ecc286d893292b2dcd0c76821`  
		Last Modified: Tue, 18 Apr 2023 01:34:33 GMT  
		Size: 7.6 MB (7604657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c60e27a0516909c7200fcf3394a9e6e0d0e593249f51b70b05db3952b66592`  
		Last Modified: Tue, 18 Apr 2023 01:34:32 GMT  
		Size: 3.6 MB (3617029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d5ef789db5e2842d73302eede7f6b7a692bd35f3ee908d4039d7853bf8157a`  
		Last Modified: Tue, 18 Apr 2023 01:34:47 GMT  
		Size: 60.8 MB (60807001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f147652501c7415f8b33749fd53610b03fad71aeb32c9307e0c1e93049148db6`  
		Last Modified: Tue, 18 Apr 2023 01:35:09 GMT  
		Size: 136.8 MB (136766031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0d5ca5035ccb90aa7f7888823fe1abfbcced3b7ac57b01d5885eae7f5fd0915e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269620396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da4a2917c479ad5c831ac7b1e22ffbfdb4017dfd4c56d11a4268714434557735`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:36:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:36:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 00:38:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:44:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d276072145993a42aed3e2b3e8cd26b6e08aab266d9c9d792ee89b26150681da`  
		Last Modified: Fri, 14 Apr 2023 09:36:00 GMT  
		Size: 33.3 MB (33300980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:923459354bb7c8ed9378009c3b9bfafa2c71db0dd9434ff6f28fa8559018a9fe`  
		Last Modified: Tue, 18 Apr 2023 01:01:27 GMT  
		Size: 8.7 MB (8694604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14eb66e0ca52c6c0e9019cd99e5a7d12708b5fcf95d917cf1dcd06a56b91160`  
		Last Modified: Tue, 18 Apr 2023 01:01:26 GMT  
		Size: 4.5 MB (4486817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e714fae693c74669418568b2a270066a28e7e561eae1ff8896650c09e925c0e0`  
		Last Modified: Tue, 18 Apr 2023 01:02:00 GMT  
		Size: 69.6 MB (69551759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cbfcddd95021b74ec467c8940e3dbdb2a5bddcfd554c99e9d4cd2908cd48db`  
		Last Modified: Tue, 18 Apr 2023 01:02:48 GMT  
		Size: 153.6 MB (153586236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ea1d4fe41029219e24238984342752c22186d78c9a76b177751136beee29eb8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226382412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e38d59d083edfdf8d44ec3f0d15c7e9bab6a63149c98e6ecafb7ece063c1252`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:35 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:37 GMT
ADD file:44c66c03ba0afcc05de1b2078f83e8bfe04706b31491fcd3fdd93cfc88d5f06c in / 
# Thu, 13 Apr 2023 13:09:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:01:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:02:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:02:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:05:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f11b609b1d63f2d37c0e3789823e7a7e62a078bddca7c46da8602655989c62d9`  
		Last Modified: Fri, 14 Apr 2023 09:38:39 GMT  
		Size: 27.0 MB (27016370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfd953572ac96bfce6706f45014f76e59e53b096cdc8eba22ffc73112fa0b3c`  
		Last Modified: Tue, 18 Apr 2023 01:13:21 GMT  
		Size: 7.4 MB (7383689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc90d577c47f7094dda274dbf62b36e812018f84c10844be7715d198c95ddfef`  
		Last Modified: Tue, 18 Apr 2023 01:13:21 GMT  
		Size: 3.5 MB (3542231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a73d2f132bb961264ac78079104aeb71d832e93e48e8bc52edc4cb58ed80e5`  
		Last Modified: Tue, 18 Apr 2023 01:13:38 GMT  
		Size: 60.0 MB (60018552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de07e3fe4a067ed0ec9ea6ffefdaf899a92a5a3700af3a79b09f15d87b7ccf21`  
		Last Modified: Tue, 18 Apr 2023 01:14:01 GMT  
		Size: 128.4 MB (128421570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:20.04-curl`

```console
$ docker pull buildpack-deps@sha256:e5bf5d43f727c6d007d5ff3da4ab2be4d551ca8fb14acb958b7b2319fe0aa144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:20.04-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5d167aefeaa2fb9ce79039758c2e7e6f56edf1a89ce8bc448e2f0cefe70f016b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.0 MB (39950019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d29726e1d46db52e0feed2033aa867e7f1bafe790a3630d26ce848a63d201a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:23:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:23:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb9a1000294d18d6dc41a0282435b987380b7f0b46c7f3dc891087e1a473ce2`  
		Last Modified: Tue, 18 Apr 2023 01:34:39 GMT  
		Size: 7.7 MB (7744253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986bdd8de236de34e3a40a899fbcd02bedbc9de7f3b6ced517c2fa4149ab0fdd`  
		Last Modified: Tue, 18 Apr 2023 01:34:38 GMT  
		Size: 3.6 MB (3627203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0628a7d571d19fc024ba47f0d48d0d5abce1c8cf9fcaf8e47656b7530a9c568f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34420575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa87f794e80c6034ad4c3e37878afcbdfab9a85127f85cd589b076509cc57c7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:47 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:20:50 GMT
ADD file:0da456bd328984fcedf5367b46a38da6ca4b43061baf6d1283380962cddc7481 in / 
# Thu, 13 Apr 2023 13:20:50 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:34:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:34:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:e68c91cb250f35160f683afa80c3ada46f06948ded46a188be490ea3afff08f5`  
		Last Modified: Fri, 14 Apr 2023 09:34:28 GMT  
		Size: 24.6 MB (24586976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029732d3be1a924e821f7cd01afe768f39d85e2d484ace5bcceab5fbc250c347`  
		Last Modified: Tue, 18 Apr 2023 01:49:22 GMT  
		Size: 6.7 MB (6729180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df6a23fdc52b8fc5a75f036a53f4c9f7a7e07c603fe5a73ba891f8dee1a7505`  
		Last Modified: Tue, 18 Apr 2023 01:49:21 GMT  
		Size: 3.1 MB (3104419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a5a09365e7a798606f12145b1a2aa619dcf85ac37d76bf3a1a265f4ec322b82a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.4 MB (38418082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1203810cbe5d7ab8ee42998962ed79b73f595e7c95742f93e279128030402c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:20:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:20:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2378679266ac5157323158b6e52e7a884e559db5217037e57992e47a1667d525`  
		Last Modified: Fri, 14 Apr 2023 07:39:20 GMT  
		Size: 27.2 MB (27196396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fee697311c4e091f41acde237da003390953c6ecc286d893292b2dcd0c76821`  
		Last Modified: Tue, 18 Apr 2023 01:34:33 GMT  
		Size: 7.6 MB (7604657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c60e27a0516909c7200fcf3394a9e6e0d0e593249f51b70b05db3952b66592`  
		Last Modified: Tue, 18 Apr 2023 01:34:32 GMT  
		Size: 3.6 MB (3617029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9a7c1ca644dbaeb4e9f71191e1d38e9fb4e701776f81ffd32f8e15bd3488dc63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46482401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d0cac502d4a1f06f6436f63ca94d88152c8e4b92b64470e43375be4510e382e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:36:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:36:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d276072145993a42aed3e2b3e8cd26b6e08aab266d9c9d792ee89b26150681da`  
		Last Modified: Fri, 14 Apr 2023 09:36:00 GMT  
		Size: 33.3 MB (33300980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:923459354bb7c8ed9378009c3b9bfafa2c71db0dd9434ff6f28fa8559018a9fe`  
		Last Modified: Tue, 18 Apr 2023 01:01:27 GMT  
		Size: 8.7 MB (8694604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14eb66e0ca52c6c0e9019cd99e5a7d12708b5fcf95d917cf1dcd06a56b91160`  
		Last Modified: Tue, 18 Apr 2023 01:01:26 GMT  
		Size: 4.5 MB (4486817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b1e9c44d6382be519684eb9baeafa3d3987d5fbb96b18f184e460fe8cd2b2523
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37942290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b37a689a24b79a714a9ba3d143e6ee344a23c224ab53f56218912ef410c4d81a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:35 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:37 GMT
ADD file:44c66c03ba0afcc05de1b2078f83e8bfe04706b31491fcd3fdd93cfc88d5f06c in / 
# Thu, 13 Apr 2023 13:09:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:01:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:02:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:f11b609b1d63f2d37c0e3789823e7a7e62a078bddca7c46da8602655989c62d9`  
		Last Modified: Fri, 14 Apr 2023 09:38:39 GMT  
		Size: 27.0 MB (27016370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfd953572ac96bfce6706f45014f76e59e53b096cdc8eba22ffc73112fa0b3c`  
		Last Modified: Tue, 18 Apr 2023 01:13:21 GMT  
		Size: 7.4 MB (7383689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc90d577c47f7094dda274dbf62b36e812018f84c10844be7715d198c95ddfef`  
		Last Modified: Tue, 18 Apr 2023 01:13:21 GMT  
		Size: 3.5 MB (3542231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:20.04-scm`

```console
$ docker pull buildpack-deps@sha256:77cd090edcf9a80bdc1593875fec276b9707bc4b20033d9b94305e56e49704c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:20.04-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:47b489d185fb17e3e4f0fc2a7284c506770fb797f36984482679b4d8501adc3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100695552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d95dd14a8d4f56fe1a512f3b3e0fe9b5991c977d0e07e35a715ecb1be3d6457`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:23:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:23:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:24:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb9a1000294d18d6dc41a0282435b987380b7f0b46c7f3dc891087e1a473ce2`  
		Last Modified: Tue, 18 Apr 2023 01:34:39 GMT  
		Size: 7.7 MB (7744253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986bdd8de236de34e3a40a899fbcd02bedbc9de7f3b6ced517c2fa4149ab0fdd`  
		Last Modified: Tue, 18 Apr 2023 01:34:38 GMT  
		Size: 3.6 MB (3627203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a87a85bf796c479f3384f9845bbb9da0e19847e85730eef87d5e68561f7c9d`  
		Last Modified: Tue, 18 Apr 2023 01:34:59 GMT  
		Size: 60.7 MB (60745533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9bc5ce508a49cf286377f106cb4e3fa3244acedd048a885383a8a848cfa61298
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.9 MB (89864366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14e666bff045b0d2159f0f22babec61e9c232b43bce2bfed15f4a37485c646c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:47 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:20:50 GMT
ADD file:0da456bd328984fcedf5367b46a38da6ca4b43061baf6d1283380962cddc7481 in / 
# Thu, 13 Apr 2023 13:20:50 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:34:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:34:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:35:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e68c91cb250f35160f683afa80c3ada46f06948ded46a188be490ea3afff08f5`  
		Last Modified: Fri, 14 Apr 2023 09:34:28 GMT  
		Size: 24.6 MB (24586976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029732d3be1a924e821f7cd01afe768f39d85e2d484ace5bcceab5fbc250c347`  
		Last Modified: Tue, 18 Apr 2023 01:49:22 GMT  
		Size: 6.7 MB (6729180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df6a23fdc52b8fc5a75f036a53f4c9f7a7e07c603fe5a73ba891f8dee1a7505`  
		Last Modified: Tue, 18 Apr 2023 01:49:21 GMT  
		Size: 3.1 MB (3104419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21583b635c301612839572600eb97628067e10e4fd4af5803b399abbcbfc8054`  
		Last Modified: Tue, 18 Apr 2023 01:49:41 GMT  
		Size: 55.4 MB (55443791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:098a12c340df6609717509b4709d479d9a1dc023641ff15c5723cfdbb4acf8b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99225083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d851cc464e9adf44ba6942b3bae4e4a50116b410a00b63c7048d7e9d79a2ff5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:20:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:20:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:20:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2378679266ac5157323158b6e52e7a884e559db5217037e57992e47a1667d525`  
		Last Modified: Fri, 14 Apr 2023 07:39:20 GMT  
		Size: 27.2 MB (27196396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fee697311c4e091f41acde237da003390953c6ecc286d893292b2dcd0c76821`  
		Last Modified: Tue, 18 Apr 2023 01:34:33 GMT  
		Size: 7.6 MB (7604657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c60e27a0516909c7200fcf3394a9e6e0d0e593249f51b70b05db3952b66592`  
		Last Modified: Tue, 18 Apr 2023 01:34:32 GMT  
		Size: 3.6 MB (3617029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d5ef789db5e2842d73302eede7f6b7a692bd35f3ee908d4039d7853bf8157a`  
		Last Modified: Tue, 18 Apr 2023 01:34:47 GMT  
		Size: 60.8 MB (60807001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:65ea078073458f501b145217e5ae0912024a6c3050c7fdfdb16c43f7167d7a5e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (116034160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49f7ad1554b25d8c56d16aeaaf445fac6e83b41fdbf9d30033f714ee0d2df88e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:36:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:36:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 00:38:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d276072145993a42aed3e2b3e8cd26b6e08aab266d9c9d792ee89b26150681da`  
		Last Modified: Fri, 14 Apr 2023 09:36:00 GMT  
		Size: 33.3 MB (33300980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:923459354bb7c8ed9378009c3b9bfafa2c71db0dd9434ff6f28fa8559018a9fe`  
		Last Modified: Tue, 18 Apr 2023 01:01:27 GMT  
		Size: 8.7 MB (8694604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14eb66e0ca52c6c0e9019cd99e5a7d12708b5fcf95d917cf1dcd06a56b91160`  
		Last Modified: Tue, 18 Apr 2023 01:01:26 GMT  
		Size: 4.5 MB (4486817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e714fae693c74669418568b2a270066a28e7e561eae1ff8896650c09e925c0e0`  
		Last Modified: Tue, 18 Apr 2023 01:02:00 GMT  
		Size: 69.6 MB (69551759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:20.04-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b49083c62ebe88b5f10ca6d6083a9c3a50544dedd323efcdd669678b796dfb89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (97960842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d473b3b8e44fa7c52afbd1368b9356f6d7fbfac2b9d6dffcd8d1054b1edf6f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:35 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:37 GMT
ADD file:44c66c03ba0afcc05de1b2078f83e8bfe04706b31491fcd3fdd93cfc88d5f06c in / 
# Thu, 13 Apr 2023 13:09:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:01:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:02:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:02:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f11b609b1d63f2d37c0e3789823e7a7e62a078bddca7c46da8602655989c62d9`  
		Last Modified: Fri, 14 Apr 2023 09:38:39 GMT  
		Size: 27.0 MB (27016370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfd953572ac96bfce6706f45014f76e59e53b096cdc8eba22ffc73112fa0b3c`  
		Last Modified: Tue, 18 Apr 2023 01:13:21 GMT  
		Size: 7.4 MB (7383689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc90d577c47f7094dda274dbf62b36e812018f84c10844be7715d198c95ddfef`  
		Last Modified: Tue, 18 Apr 2023 01:13:21 GMT  
		Size: 3.5 MB (3542231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a73d2f132bb961264ac78079104aeb71d832e93e48e8bc52edc4cb58ed80e5`  
		Last Modified: Tue, 18 Apr 2023 01:13:38 GMT  
		Size: 60.0 MB (60018552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:22.04`

```console
$ docker pull buildpack-deps@sha256:fe20c1a1fa7749ce93af04e56c2a46297e6b236eeddbdb8fd780ec58784c121a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:22.04` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c7af89fe20e8b370fa3d84c23f5dbb048e01cfd38fbc12c1e02232c1a84af80f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.0 MB (250022556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375da4bb35d8bd52aa3070617888fd8aea7a8aec9a99774cdd1df6a8a87cd5ca`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:29:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:29:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 05:29:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:32:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7490ba7e16ba382ca21015280e2ee6dad31879a1f043029e350a8e429770f36`  
		Last Modified: Thu, 16 Mar 2023 05:43:15 GMT  
		Size: 3.8 MB (3788671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eeb23ea57c359eecf9e21c40ddb69f738e9121008fd4956d733ba66d3b7eb38`  
		Last Modified: Thu, 16 Mar 2023 05:43:15 GMT  
		Size: 3.6 MB (3561600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6c00a0ea05e6a2089233e7238bbed0ffbf7b2655f03195967e2083ee623899`  
		Last Modified: Thu, 16 Mar 2023 05:43:30 GMT  
		Size: 39.4 MB (39352910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa902bb14f17725bbd311e77e44da0ef803e68e0965c5f95635eb83f288b5d4`  
		Last Modified: Thu, 16 Mar 2023 05:44:00 GMT  
		Size: 172.9 MB (172889412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:548a747004a966f5fe24d920b0b67a7e2f63d2f84ee8a998d73573f3534d291c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.7 MB (216673703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2805f8c5309daa5cfffe1813e3cf819142f1ed5ef4f8e6be329cbcad71c2d30`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:31:41 GMT
ADD file:e9c3ac290fb81ae2e78de99052d776396ee3aff05e1a66fd2dccb01d7de9bb45 in / 
# Wed, 08 Mar 2023 04:31:42 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:51:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:51:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 03:52:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:55:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cba1fa3bcdf4f746dcf5b8f86874cee4a6eff75dd5c5cd29e4c912574b12a1c6`  
		Last Modified: Thu, 09 Mar 2023 04:41:14 GMT  
		Size: 27.0 MB (27025397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff3d54aa809ca004a01d3a10bf7017a1fb216f185fd9d0f210f1bc9512298c1`  
		Last Modified: Thu, 16 Mar 2023 04:09:39 GMT  
		Size: 3.5 MB (3540124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caec72904127d7cb95dfd39a3f311865b026d929e1440427ec21122be6e15db3`  
		Last Modified: Thu, 16 Mar 2023 04:09:39 GMT  
		Size: 3.7 MB (3714418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b259dc20995aa828e48008def151ea3da6891615621976f66dc6b63fdbda38a`  
		Last Modified: Thu, 16 Mar 2023 04:09:57 GMT  
		Size: 41.9 MB (41908320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d21e83a1a0d8dfe0c0f53e1f8d51356e226e68eb9de5b136253db03ceac4e7`  
		Last Modified: Thu, 16 Mar 2023 04:10:26 GMT  
		Size: 140.5 MB (140485444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bc8bb348a53f7d9f3e309b375c7fd76b56a0c48f89c849a9c6ade599cdc8180a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 MB (241329007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ffb8e18683ff48d54f07c675683997a40a1555dde02c54147d8d9d48aa756df`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:32:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:32:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:32:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:32:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:32:40 GMT
ADD file:79b36308bc382d9cae7197b4cecc21430f4e8f3e8bec3547d0f00bcff7681e60 in / 
# Wed, 08 Mar 2023 04:32:41 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 04:07:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:08:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 04:08:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:11:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b2ddfd337773edbf5766dce2fdbeef139ba8c42724e29eda157c84e9f97f1bce`  
		Last Modified: Wed, 08 Mar 2023 12:37:24 GMT  
		Size: 28.4 MB (28387554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aef66b301cbfe4ff1bb09357ccf381140239a236438d27a992d076491a3a066`  
		Last Modified: Thu, 16 Mar 2023 04:23:23 GMT  
		Size: 3.8 MB (3760501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693278d975de74bdcb529fd46771b1335b9501b8f479a3c8128b69375f7945a8`  
		Last Modified: Thu, 16 Mar 2023 04:23:23 GMT  
		Size: 3.5 MB (3536190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bfc2e7bfd914b57fdeae1d187ca7a12534443f9e2a6142287dab73c0296ade8`  
		Last Modified: Thu, 16 Mar 2023 04:23:36 GMT  
		Size: 39.2 MB (39243621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2292b558961f2b5d5b6555b004730bdf51c7012b78b0a9474df76b1674aaa26`  
		Last Modified: Thu, 16 Mar 2023 04:24:01 GMT  
		Size: 166.4 MB (166401141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d098228e71918993c4063a767b2eef4e86f48651116a36ecd3b3faa15276d498
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271846871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55eaa1527dc94604178ceeb1d0dd71d0ef94cf7213d605391668aa27d2fb142e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:16 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:20 GMT
ADD file:d7434a52d8d8aa6288e788f6fe7e156f0e11bf9b8275efaf70aab0bfc4d919cf in / 
# Wed, 08 Mar 2023 04:39:20 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:23:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:23:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 03:24:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:29:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:deffc758660db3b0ee7a1f211d720633f06f27ab1e4c31db4caf8c27f4a80eeb`  
		Last Modified: Thu, 16 Mar 2023 02:22:27 GMT  
		Size: 35.7 MB (35711728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda6a81b65d142865ef5dbb2df2e98c084dc995272e55f804a36f283c6f9cc0a`  
		Last Modified: Thu, 16 Mar 2023 03:50:35 GMT  
		Size: 4.3 MB (4262063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ead6720a64b98a3aff60731463b608c0b67ecd6e1da5fdea16027f2602fed35`  
		Last Modified: Thu, 16 Mar 2023 03:50:35 GMT  
		Size: 4.2 MB (4234751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d902f277ddd72c79a705e87198d386aa6f00888bd94535ac236140f709bbdce`  
		Last Modified: Thu, 16 Mar 2023 03:50:57 GMT  
		Size: 43.8 MB (43768451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e52f20a783e0f77850e23839602213aca9d779491820b6b87d582377010ff1`  
		Last Modified: Thu, 16 Mar 2023 03:51:51 GMT  
		Size: 183.9 MB (183869878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d8f68fa9506203d2ae62c96ff52ca734da392b0abdf6fb87d0b095d32da75234
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.7 MB (223696064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:027fabc11727fa0a1d019f1c51338d85905a5113cdc2c03b8c1fbb1f2a852c17`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:24 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:26 GMT
ADD file:630f9865d3d4fd4294d45cac7cbaea83fb549c2e563de454348da964d19fbbba in / 
# Wed, 08 Mar 2023 04:39:26 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:49:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:49:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 01:50:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:52:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2c7366af510b72cc0b3456fb93cfa0bfc76f7d383db5cb315967e7b1ce2e0c42`  
		Last Modified: Thu, 16 Mar 2023 02:02:40 GMT  
		Size: 28.6 MB (28647599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfb18fcfcf98f525d6770606600d80d5413262ce3575995b49064988c1bd147`  
		Last Modified: Thu, 16 Mar 2023 02:02:37 GMT  
		Size: 3.8 MB (3792844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072af6d5dacbd70c88a5e91a5627fe4a95af544c4db1b250a263452128dc9cab`  
		Last Modified: Thu, 16 Mar 2023 02:02:37 GMT  
		Size: 3.5 MB (3472886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b80aecb29fcddae2ca64d4c31faa682b41b3206400c727d5eec25c7d83c8630`  
		Last Modified: Thu, 16 Mar 2023 02:02:54 GMT  
		Size: 39.3 MB (39284857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:277c8fbd8d44bf1475a44df6398ba9159c13423417cffb98f23824dca61b4a1d`  
		Last Modified: Thu, 16 Mar 2023 02:03:19 GMT  
		Size: 148.5 MB (148497878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:22.04-curl`

```console
$ docker pull buildpack-deps@sha256:1950ad34a10c685de875a9d2f586a239612590e033635f7ca3b07cd333c35d88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:22.04-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e1f00c6daf4cd328bbef9c52e6c60f18a47e5b716ef5a5d78542c90635025d20
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 MB (37780234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb7e40d800141c3758097d639c8f71da7d755a34a9ce59dabba14aac2a540ee`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:29:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:29:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7490ba7e16ba382ca21015280e2ee6dad31879a1f043029e350a8e429770f36`  
		Last Modified: Thu, 16 Mar 2023 05:43:15 GMT  
		Size: 3.8 MB (3788671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eeb23ea57c359eecf9e21c40ddb69f738e9121008fd4956d733ba66d3b7eb38`  
		Last Modified: Thu, 16 Mar 2023 05:43:15 GMT  
		Size: 3.6 MB (3561600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d14e02d71154d77fa15e8fe99c09399a29cf9cd6a168b06bf6cfdc6cbdd98960
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34279939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831a4c6176514fb8d4452ddac355efa1a3da26e98087da273d6c3bcc34ba38e1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:31:41 GMT
ADD file:e9c3ac290fb81ae2e78de99052d776396ee3aff05e1a66fd2dccb01d7de9bb45 in / 
# Wed, 08 Mar 2023 04:31:42 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:51:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:51:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:cba1fa3bcdf4f746dcf5b8f86874cee4a6eff75dd5c5cd29e4c912574b12a1c6`  
		Last Modified: Thu, 09 Mar 2023 04:41:14 GMT  
		Size: 27.0 MB (27025397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff3d54aa809ca004a01d3a10bf7017a1fb216f185fd9d0f210f1bc9512298c1`  
		Last Modified: Thu, 16 Mar 2023 04:09:39 GMT  
		Size: 3.5 MB (3540124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caec72904127d7cb95dfd39a3f311865b026d929e1440427ec21122be6e15db3`  
		Last Modified: Thu, 16 Mar 2023 04:09:39 GMT  
		Size: 3.7 MB (3714418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:fa825f78772b21eb6d058d2d80e48ded564c870a66ec077b8219225d6f515c2c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35684245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd233dec7831ce72a921837b590af2d1f8f8d87f1b119fae78edba2ea730316`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:32:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:32:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:32:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:32:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:32:40 GMT
ADD file:79b36308bc382d9cae7197b4cecc21430f4e8f3e8bec3547d0f00bcff7681e60 in / 
# Wed, 08 Mar 2023 04:32:41 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 04:07:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:08:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b2ddfd337773edbf5766dce2fdbeef139ba8c42724e29eda157c84e9f97f1bce`  
		Last Modified: Wed, 08 Mar 2023 12:37:24 GMT  
		Size: 28.4 MB (28387554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aef66b301cbfe4ff1bb09357ccf381140239a236438d27a992d076491a3a066`  
		Last Modified: Thu, 16 Mar 2023 04:23:23 GMT  
		Size: 3.8 MB (3760501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693278d975de74bdcb529fd46771b1335b9501b8f479a3c8128b69375f7945a8`  
		Last Modified: Thu, 16 Mar 2023 04:23:23 GMT  
		Size: 3.5 MB (3536190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:057ed8d3115324cc3a7cbde4dad9bc42768a3cfeeb98aa5a2342d57a704ea2b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44208542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d825634c6ab1942263dbe9f71d6b27d39b833fb4013c32ad433760b35351762d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:16 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:20 GMT
ADD file:d7434a52d8d8aa6288e788f6fe7e156f0e11bf9b8275efaf70aab0bfc4d919cf in / 
# Wed, 08 Mar 2023 04:39:20 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:23:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:23:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:deffc758660db3b0ee7a1f211d720633f06f27ab1e4c31db4caf8c27f4a80eeb`  
		Last Modified: Thu, 16 Mar 2023 02:22:27 GMT  
		Size: 35.7 MB (35711728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda6a81b65d142865ef5dbb2df2e98c084dc995272e55f804a36f283c6f9cc0a`  
		Last Modified: Thu, 16 Mar 2023 03:50:35 GMT  
		Size: 4.3 MB (4262063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ead6720a64b98a3aff60731463b608c0b67ecd6e1da5fdea16027f2602fed35`  
		Last Modified: Thu, 16 Mar 2023 03:50:35 GMT  
		Size: 4.2 MB (4234751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b22525cdcb82e2ef5355054b43872f265a7e983b5de76a9606921cde9d74b610
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 MB (35913329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a514140debee8dd2b4218d8d1975fc7b1e4623707f2083cffa6cdbd3f7e11228`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:24 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:26 GMT
ADD file:630f9865d3d4fd4294d45cac7cbaea83fb549c2e563de454348da964d19fbbba in / 
# Wed, 08 Mar 2023 04:39:26 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:49:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:49:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2c7366af510b72cc0b3456fb93cfa0bfc76f7d383db5cb315967e7b1ce2e0c42`  
		Last Modified: Thu, 16 Mar 2023 02:02:40 GMT  
		Size: 28.6 MB (28647599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfb18fcfcf98f525d6770606600d80d5413262ce3575995b49064988c1bd147`  
		Last Modified: Thu, 16 Mar 2023 02:02:37 GMT  
		Size: 3.8 MB (3792844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072af6d5dacbd70c88a5e91a5627fe4a95af544c4db1b250a263452128dc9cab`  
		Last Modified: Thu, 16 Mar 2023 02:02:37 GMT  
		Size: 3.5 MB (3472886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:22.04-scm`

```console
$ docker pull buildpack-deps@sha256:79b0f9319ebb640493eaf8539641f9fc67a08f10ec5fc2f8a7d9a447fd786055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:22.04-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f34fd3d1a17609e88da35bc2a959ddd09a4cff838e251132a6a4551b7f710a8e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77133144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9805e59e9e583a30a563cbac116296ba8acf152f10fabcbecc2d3f99f8b6ab`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:29:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:29:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 05:29:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7490ba7e16ba382ca21015280e2ee6dad31879a1f043029e350a8e429770f36`  
		Last Modified: Thu, 16 Mar 2023 05:43:15 GMT  
		Size: 3.8 MB (3788671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eeb23ea57c359eecf9e21c40ddb69f738e9121008fd4956d733ba66d3b7eb38`  
		Last Modified: Thu, 16 Mar 2023 05:43:15 GMT  
		Size: 3.6 MB (3561600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6c00a0ea05e6a2089233e7238bbed0ffbf7b2655f03195967e2083ee623899`  
		Last Modified: Thu, 16 Mar 2023 05:43:30 GMT  
		Size: 39.4 MB (39352910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8249c9a5f7475ad02f242ade08a27052609481d8cd35ae4089fa7ecb14295c45
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76188259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7c6edcb5acd77a3e2b70af5afcda9bef5dcb2ee9c21e24297ee96426322b6e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:31:41 GMT
ADD file:e9c3ac290fb81ae2e78de99052d776396ee3aff05e1a66fd2dccb01d7de9bb45 in / 
# Wed, 08 Mar 2023 04:31:42 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:51:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:51:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 03:52:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cba1fa3bcdf4f746dcf5b8f86874cee4a6eff75dd5c5cd29e4c912574b12a1c6`  
		Last Modified: Thu, 09 Mar 2023 04:41:14 GMT  
		Size: 27.0 MB (27025397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff3d54aa809ca004a01d3a10bf7017a1fb216f185fd9d0f210f1bc9512298c1`  
		Last Modified: Thu, 16 Mar 2023 04:09:39 GMT  
		Size: 3.5 MB (3540124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caec72904127d7cb95dfd39a3f311865b026d929e1440427ec21122be6e15db3`  
		Last Modified: Thu, 16 Mar 2023 04:09:39 GMT  
		Size: 3.7 MB (3714418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b259dc20995aa828e48008def151ea3da6891615621976f66dc6b63fdbda38a`  
		Last Modified: Thu, 16 Mar 2023 04:09:57 GMT  
		Size: 41.9 MB (41908320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6857aefe9fc47abf0d2d28e21e046b63e6be875de53f2b1fd49dea88192e4560
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74927866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca9591d5aa5d0b25f21dfa798fa26b330206f083d8ca36701124b4a875b6c2c4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:32:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:32:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:32:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:32:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:32:40 GMT
ADD file:79b36308bc382d9cae7197b4cecc21430f4e8f3e8bec3547d0f00bcff7681e60 in / 
# Wed, 08 Mar 2023 04:32:41 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 04:07:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:08:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 04:08:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b2ddfd337773edbf5766dce2fdbeef139ba8c42724e29eda157c84e9f97f1bce`  
		Last Modified: Wed, 08 Mar 2023 12:37:24 GMT  
		Size: 28.4 MB (28387554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aef66b301cbfe4ff1bb09357ccf381140239a236438d27a992d076491a3a066`  
		Last Modified: Thu, 16 Mar 2023 04:23:23 GMT  
		Size: 3.8 MB (3760501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693278d975de74bdcb529fd46771b1335b9501b8f479a3c8128b69375f7945a8`  
		Last Modified: Thu, 16 Mar 2023 04:23:23 GMT  
		Size: 3.5 MB (3536190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bfc2e7bfd914b57fdeae1d187ca7a12534443f9e2a6142287dab73c0296ade8`  
		Last Modified: Thu, 16 Mar 2023 04:23:36 GMT  
		Size: 39.2 MB (39243621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d8da9e38d3c74aa25f5da85d9e692795099198656dfb38ba3058d5cc1c3284d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 MB (87976993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a899652169ee26f65829047e0799b9409330896911f49369b3b425b1315c02b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:16 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:20 GMT
ADD file:d7434a52d8d8aa6288e788f6fe7e156f0e11bf9b8275efaf70aab0bfc4d919cf in / 
# Wed, 08 Mar 2023 04:39:20 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:23:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:23:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 03:24:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:deffc758660db3b0ee7a1f211d720633f06f27ab1e4c31db4caf8c27f4a80eeb`  
		Last Modified: Thu, 16 Mar 2023 02:22:27 GMT  
		Size: 35.7 MB (35711728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda6a81b65d142865ef5dbb2df2e98c084dc995272e55f804a36f283c6f9cc0a`  
		Last Modified: Thu, 16 Mar 2023 03:50:35 GMT  
		Size: 4.3 MB (4262063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ead6720a64b98a3aff60731463b608c0b67ecd6e1da5fdea16027f2602fed35`  
		Last Modified: Thu, 16 Mar 2023 03:50:35 GMT  
		Size: 4.2 MB (4234751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d902f277ddd72c79a705e87198d386aa6f00888bd94535ac236140f709bbdce`  
		Last Modified: Thu, 16 Mar 2023 03:50:57 GMT  
		Size: 43.8 MB (43768451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.04-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9b906aa81cc60290a664f0ff6bcb0f491cac7dd31f6cc7fbb73f4f2823d84ca0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75198186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:accf40ea7a4019526a1b76f2c48458f738926fa6bb6f285ca24c9c03b98771ed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:24 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:26 GMT
ADD file:630f9865d3d4fd4294d45cac7cbaea83fb549c2e563de454348da964d19fbbba in / 
# Wed, 08 Mar 2023 04:39:26 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:49:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:49:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 01:50:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2c7366af510b72cc0b3456fb93cfa0bfc76f7d383db5cb315967e7b1ce2e0c42`  
		Last Modified: Thu, 16 Mar 2023 02:02:40 GMT  
		Size: 28.6 MB (28647599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfb18fcfcf98f525d6770606600d80d5413262ce3575995b49064988c1bd147`  
		Last Modified: Thu, 16 Mar 2023 02:02:37 GMT  
		Size: 3.8 MB (3792844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072af6d5dacbd70c88a5e91a5627fe4a95af544c4db1b250a263452128dc9cab`  
		Last Modified: Thu, 16 Mar 2023 02:02:37 GMT  
		Size: 3.5 MB (3472886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b80aecb29fcddae2ca64d4c31faa682b41b3206400c727d5eec25c7d83c8630`  
		Last Modified: Thu, 16 Mar 2023 02:02:54 GMT  
		Size: 39.3 MB (39284857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:22.10`

```console
$ docker pull buildpack-deps@sha256:1de863c96612a1ba170ad856067a4785d1c48157c2a20b86a0fa43d66099ac20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:22.10` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:47a4169bc938bbd93194b81c05ebde3ce8761cfb50f556bc891e8d3127139a9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.8 MB (258757659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa2be6aefd392ae2d26ec97c171529a285f6e7ad875a5b19149f0121627a521d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:03:38 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:03:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:03:39 GMT
ADD file:ba742ddbebcc8282f5094275969bfb2ff4b2973e385c198b6897bea2a9cb4b85 in / 
# Thu, 13 Apr 2023 13:03:39 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:26:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:26:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:27:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:30:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:318b284d262b8726296dca98d01be71ddfad412c987a7ecec4db3278eef82188`  
		Last Modified: Fri, 14 Apr 2023 09:51:30 GMT  
		Size: 27.5 MB (27482065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a21382eec6e41b44d6c1e3ab5faaf936e33dfa42e25ce3b71ba5bee3dc3352`  
		Last Modified: Tue, 18 Apr 2023 01:35:37 GMT  
		Size: 6.8 MB (6774413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72965a2f51dc0d93d80a13692ed731534afdf361dfbabdd2da5b4ff69faeab0b`  
		Last Modified: Tue, 18 Apr 2023 01:35:36 GMT  
		Size: 3.6 MB (3635395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e29d10ebe6980c4a950b493f7124babae9418113f9b240e5bd9d4eacfb7162`  
		Last Modified: Tue, 18 Apr 2023 01:35:53 GMT  
		Size: 39.7 MB (39739228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6054ae3e51fffb85a5c75e32dfddc8412f3afafeb95561d3259bdbce227ad5f5`  
		Last Modified: Tue, 18 Apr 2023 01:36:24 GMT  
		Size: 181.1 MB (181126558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.10` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:035179436aed59c0c83db5632b9f6dbb7e8670ca49b317e341118be400ba4324
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221883309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af7580b578b34f3ffbcfa3fb65851e9ba09187d501c8e45611bba3c8586aee6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:51 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:52 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:10:01 GMT
ADD file:7c943de57b75e515f072a13706b12ee97f17d22a120991f8effbc0615c544253 in / 
# Thu, 13 Apr 2023 13:10:02 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:39:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:40:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:44:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f98d8e30b5bcedb55e832c340c4accb90ea3b5319d99dd02667d1ae133fe0f01`  
		Last Modified: Fri, 14 Apr 2023 09:55:43 GMT  
		Size: 25.9 MB (25891251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d51b5e66e30d2da337764807887bf782dbee472da4c68d5d639f11675c2b227`  
		Last Modified: Tue, 18 Apr 2023 01:50:18 GMT  
		Size: 5.9 MB (5947326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ebf5377710c036b1bad928498ea4e024c30e8f182174cd7a1a5a982218e210`  
		Last Modified: Tue, 18 Apr 2023 01:50:17 GMT  
		Size: 3.8 MB (3801747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7d2e4eec630d9a9b5faa00fb07be6af7f2c4e2a54c97ea8cc1822bbb2447c8`  
		Last Modified: Tue, 18 Apr 2023 01:50:35 GMT  
		Size: 42.6 MB (42613117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a37aaa3caa5861bbeba27ff23967333f6181d66435f89cade2586a061ba7af`  
		Last Modified: Tue, 18 Apr 2023 01:51:03 GMT  
		Size: 143.6 MB (143629868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.10` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f15bbe544c8596ce66173fc4e4e595cdad287cd19b75b0ecb90a17207003bf28
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246726292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e9ba4ebb965e3b2baafaec5093d051d5c0ac17fa0db69a7eba6757db44402e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:37 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:37 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:20:38 GMT
ADD file:8b5c9a166ff42d52b423d188428558ea2bf225c42aeb3de339514e6ad9fdd504 in / 
# Thu, 13 Apr 2023 13:20:39 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:24:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:24:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:25:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:29:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:479b8cd2e9c97aa9b4eb9d8070207c8b64f471b3ec6bb582c7b09dacb55735a2`  
		Last Modified: Fri, 14 Apr 2023 09:53:52 GMT  
		Size: 26.7 MB (26702173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a211e249366d1e9c621cfbb98a45087c7ca76b4539f9bc7d9068b701a8054585`  
		Last Modified: Tue, 18 Apr 2023 01:35:19 GMT  
		Size: 6.6 MB (6604111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd99e3413cacb724e75738256d7ae34f43ccb93122964be0ea699ffcc780ae6d`  
		Last Modified: Tue, 18 Apr 2023 01:35:19 GMT  
		Size: 3.6 MB (3603384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee999b3c3995eddaf919a60db441654b53a3390af8730f1b0a438577ec230068`  
		Last Modified: Tue, 18 Apr 2023 01:35:35 GMT  
		Size: 39.5 MB (39512803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c32c97453084fb79cd6834efc8143004eb54df5b273f0ee5de88d2e2ca20c3`  
		Last Modified: Tue, 18 Apr 2023 01:36:00 GMT  
		Size: 170.3 MB (170303821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.10` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d7f5050ebc5dd34d23a84c1079856e93173b6d6b70fd3c9f40520a44a65b4e70
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281324046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369d2dd6eb5633076e9b5ea2f1fc56834446018606b3738c523d5f9dadae0947`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:21:42 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:21:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:21:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:21:43 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:21:45 GMT
ADD file:2f24914c3a2e66342aa7cf589af143b01a1cd7532c92c4263d251fb826b8b810 in / 
# Thu, 13 Apr 2023 13:21:46 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:45:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:46:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 00:47:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:53:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3b2b861f7bcaef2d589c1d8518a14da93644aafdcc9bfc5554895ed342bc341c`  
		Last Modified: Fri, 14 Apr 2023 09:57:14 GMT  
		Size: 32.1 MB (32098609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978ddb6b21e3fea6c8cb5970d8cd307a6ec15ef6b639b994cfdebe9384ef6e24`  
		Last Modified: Tue, 18 Apr 2023 01:03:02 GMT  
		Size: 7.8 MB (7751781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54556acf1bc962b10d66a29a9198cf3876dbc10be5d5899d89ee4ee01770250e`  
		Last Modified: Tue, 18 Apr 2023 01:03:01 GMT  
		Size: 4.4 MB (4362837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4db88fb9e9071e75f6c65177600cda26da9887d2574f51858808a6973fb9252`  
		Last Modified: Tue, 18 Apr 2023 01:03:29 GMT  
		Size: 44.1 MB (44147073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d215be67ce556d3fdbd64f14d10e6426bf36fb6035ba527939c1614d3d8dade0`  
		Last Modified: Tue, 18 Apr 2023 01:04:25 GMT  
		Size: 193.0 MB (192963746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.10` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:addc2e3ff7a25e8fae18b569593daa21e377dd047158af082341ca3d5249c9b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228647799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebe59ba4464149ed91005f254898908afda7a4d0ad989503cc2415bef2a1847`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:08:08 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:08:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:08:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:08:08 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:08:09 GMT
ADD file:df5733230d0258ecd0cbdcc7c2075865bc335200f2cafee8dacccfd082710b96 in / 
# Thu, 13 Apr 2023 13:08:10 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:05:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:06:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:06:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:08:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c450971bf0fd92eac91caf0b3126482e5fecadead22e59da08f9661a4b4f03be`  
		Last Modified: Fri, 14 Apr 2023 10:00:19 GMT  
		Size: 26.0 MB (26029287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded2cd498871df7ac556305ff379ade5376ed441cad7f51cf98b4867ac750d39`  
		Last Modified: Tue, 18 Apr 2023 01:14:11 GMT  
		Size: 6.5 MB (6467769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5cee9d25bba89e9b965d2fee1419c9d544d12c148be50fd20849d7f808bde1`  
		Last Modified: Tue, 18 Apr 2023 01:14:10 GMT  
		Size: 3.6 MB (3625375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36304f69d4e520034a19fbb9f1da633dd4722e9cdc720512923f71d850cc07d5`  
		Last Modified: Tue, 18 Apr 2023 01:14:24 GMT  
		Size: 39.6 MB (39564578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a4c7f51941a2d297df128b432e31b25677e7e42ba0d57b82603461c4244e87`  
		Last Modified: Tue, 18 Apr 2023 01:14:48 GMT  
		Size: 153.0 MB (152960790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:22.10-curl`

```console
$ docker pull buildpack-deps@sha256:070458606dbc997307494bb256f2e0b9f5e9ceed956f38d8ad1951239e6e7015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:22.10-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e2baef48d968cfb8eaa239e989fe2f8fa6dc82e8cdb6992d928a7af7e7b97698
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37891873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b717cacdac4c1a10af86a1162d9c8fd0db43b12a5aa661a257dad5328881196`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:03:38 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:03:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:03:39 GMT
ADD file:ba742ddbebcc8282f5094275969bfb2ff4b2973e385c198b6897bea2a9cb4b85 in / 
# Thu, 13 Apr 2023 13:03:39 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:26:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:26:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:318b284d262b8726296dca98d01be71ddfad412c987a7ecec4db3278eef82188`  
		Last Modified: Fri, 14 Apr 2023 09:51:30 GMT  
		Size: 27.5 MB (27482065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a21382eec6e41b44d6c1e3ab5faaf936e33dfa42e25ce3b71ba5bee3dc3352`  
		Last Modified: Tue, 18 Apr 2023 01:35:37 GMT  
		Size: 6.8 MB (6774413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72965a2f51dc0d93d80a13692ed731534afdf361dfbabdd2da5b4ff69faeab0b`  
		Last Modified: Tue, 18 Apr 2023 01:35:36 GMT  
		Size: 3.6 MB (3635395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.10-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c855f3091d5cd8f298812ef20659893606ad3decf412e045c3baf00844f4c0f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 MB (35640324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93ceadf349fadae92f8b50df62219bf931bb7754516e96a10c2fb6c7d6c89221`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:51 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:52 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:10:01 GMT
ADD file:7c943de57b75e515f072a13706b12ee97f17d22a120991f8effbc0615c544253 in / 
# Thu, 13 Apr 2023 13:10:02 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:39:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:f98d8e30b5bcedb55e832c340c4accb90ea3b5319d99dd02667d1ae133fe0f01`  
		Last Modified: Fri, 14 Apr 2023 09:55:43 GMT  
		Size: 25.9 MB (25891251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d51b5e66e30d2da337764807887bf782dbee472da4c68d5d639f11675c2b227`  
		Last Modified: Tue, 18 Apr 2023 01:50:18 GMT  
		Size: 5.9 MB (5947326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ebf5377710c036b1bad928498ea4e024c30e8f182174cd7a1a5a982218e210`  
		Last Modified: Tue, 18 Apr 2023 01:50:17 GMT  
		Size: 3.8 MB (3801747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.10-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3c54974fca8d55cc2aae0bf59aaf13d1492ee8fab8fc7afc6758ca10a9901bc7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36909668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8f78b7034cdd7b9e8c7a44a1c482fb47fc143533f941369a3d0387c98fd411`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:37 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:37 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:20:38 GMT
ADD file:8b5c9a166ff42d52b423d188428558ea2bf225c42aeb3de339514e6ad9fdd504 in / 
# Thu, 13 Apr 2023 13:20:39 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:24:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:24:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:479b8cd2e9c97aa9b4eb9d8070207c8b64f471b3ec6bb582c7b09dacb55735a2`  
		Last Modified: Fri, 14 Apr 2023 09:53:52 GMT  
		Size: 26.7 MB (26702173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a211e249366d1e9c621cfbb98a45087c7ca76b4539f9bc7d9068b701a8054585`  
		Last Modified: Tue, 18 Apr 2023 01:35:19 GMT  
		Size: 6.6 MB (6604111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd99e3413cacb724e75738256d7ae34f43ccb93122964be0ea699ffcc780ae6d`  
		Last Modified: Tue, 18 Apr 2023 01:35:19 GMT  
		Size: 3.6 MB (3603384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.10-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a173db92e12ea4bc7ab8861dc75b1d01163b4169bf587bcbdf056ceceef84f9b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44213227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa7da5a02e3ed5cc84aef25afdec00f9462f210848b3903b605466dcbf679da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:21:42 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:21:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:21:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:21:43 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:21:45 GMT
ADD file:2f24914c3a2e66342aa7cf589af143b01a1cd7532c92c4263d251fb826b8b810 in / 
# Thu, 13 Apr 2023 13:21:46 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:45:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:46:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3b2b861f7bcaef2d589c1d8518a14da93644aafdcc9bfc5554895ed342bc341c`  
		Last Modified: Fri, 14 Apr 2023 09:57:14 GMT  
		Size: 32.1 MB (32098609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978ddb6b21e3fea6c8cb5970d8cd307a6ec15ef6b639b994cfdebe9384ef6e24`  
		Last Modified: Tue, 18 Apr 2023 01:03:02 GMT  
		Size: 7.8 MB (7751781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54556acf1bc962b10d66a29a9198cf3876dbc10be5d5899d89ee4ee01770250e`  
		Last Modified: Tue, 18 Apr 2023 01:03:01 GMT  
		Size: 4.4 MB (4362837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.10-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a9a30abdb96a71c9bfe40e06305587f2453f48e6826253c2346f68c867918c49
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36122431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d179c68254fd9641c116296236caf4426c7b9a75a4eef7ff30749528c41b419`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:08:08 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:08:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:08:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:08:08 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:08:09 GMT
ADD file:df5733230d0258ecd0cbdcc7c2075865bc335200f2cafee8dacccfd082710b96 in / 
# Thu, 13 Apr 2023 13:08:10 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:05:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:06:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:c450971bf0fd92eac91caf0b3126482e5fecadead22e59da08f9661a4b4f03be`  
		Last Modified: Fri, 14 Apr 2023 10:00:19 GMT  
		Size: 26.0 MB (26029287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded2cd498871df7ac556305ff379ade5376ed441cad7f51cf98b4867ac750d39`  
		Last Modified: Tue, 18 Apr 2023 01:14:11 GMT  
		Size: 6.5 MB (6467769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5cee9d25bba89e9b965d2fee1419c9d544d12c148be50fd20849d7f808bde1`  
		Last Modified: Tue, 18 Apr 2023 01:14:10 GMT  
		Size: 3.6 MB (3625375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:22.10-scm`

```console
$ docker pull buildpack-deps@sha256:9121f3d8acb4f1325a22fc4e4ee0f6fa0942195663d4177200cb4a93170f0d3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:22.10-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:6cefb88899f6601cbdc537665bce2f7653e8668d18af7822325c5686361be75c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77631101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba075d897f5e029a7aca18b815d2b01d1c74b1ba28a99b4f2956c3f74e46aed6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:03:38 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:03:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:03:39 GMT
ADD file:ba742ddbebcc8282f5094275969bfb2ff4b2973e385c198b6897bea2a9cb4b85 in / 
# Thu, 13 Apr 2023 13:03:39 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:26:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:26:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:27:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:318b284d262b8726296dca98d01be71ddfad412c987a7ecec4db3278eef82188`  
		Last Modified: Fri, 14 Apr 2023 09:51:30 GMT  
		Size: 27.5 MB (27482065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a21382eec6e41b44d6c1e3ab5faaf936e33dfa42e25ce3b71ba5bee3dc3352`  
		Last Modified: Tue, 18 Apr 2023 01:35:37 GMT  
		Size: 6.8 MB (6774413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72965a2f51dc0d93d80a13692ed731534afdf361dfbabdd2da5b4ff69faeab0b`  
		Last Modified: Tue, 18 Apr 2023 01:35:36 GMT  
		Size: 3.6 MB (3635395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e29d10ebe6980c4a950b493f7124babae9418113f9b240e5bd9d4eacfb7162`  
		Last Modified: Tue, 18 Apr 2023 01:35:53 GMT  
		Size: 39.7 MB (39739228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.10-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:67774d150a60cdea71df4fa5c89c73e76fdb497221591402019183488e37a818
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78253441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5be701f11a06844f2e3d9caf98e515b72b789382e8713d49d572ec08d3583316`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:51 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:52 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:10:01 GMT
ADD file:7c943de57b75e515f072a13706b12ee97f17d22a120991f8effbc0615c544253 in / 
# Thu, 13 Apr 2023 13:10:02 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:39:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:40:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f98d8e30b5bcedb55e832c340c4accb90ea3b5319d99dd02667d1ae133fe0f01`  
		Last Modified: Fri, 14 Apr 2023 09:55:43 GMT  
		Size: 25.9 MB (25891251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d51b5e66e30d2da337764807887bf782dbee472da4c68d5d639f11675c2b227`  
		Last Modified: Tue, 18 Apr 2023 01:50:18 GMT  
		Size: 5.9 MB (5947326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ebf5377710c036b1bad928498ea4e024c30e8f182174cd7a1a5a982218e210`  
		Last Modified: Tue, 18 Apr 2023 01:50:17 GMT  
		Size: 3.8 MB (3801747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7d2e4eec630d9a9b5faa00fb07be6af7f2c4e2a54c97ea8cc1822bbb2447c8`  
		Last Modified: Tue, 18 Apr 2023 01:50:35 GMT  
		Size: 42.6 MB (42613117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.10-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:87bda58def49dc9de7b321934e261d639446fbd2f0e7b72e39629f25cf6d2406
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76422471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b214eb7217e5d32bda0460644803e68d09cd216aae2a1b6df4aaacdad4a79e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:37 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:37 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:20:38 GMT
ADD file:8b5c9a166ff42d52b423d188428558ea2bf225c42aeb3de339514e6ad9fdd504 in / 
# Thu, 13 Apr 2023 13:20:39 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:24:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:24:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:25:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:479b8cd2e9c97aa9b4eb9d8070207c8b64f471b3ec6bb582c7b09dacb55735a2`  
		Last Modified: Fri, 14 Apr 2023 09:53:52 GMT  
		Size: 26.7 MB (26702173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a211e249366d1e9c621cfbb98a45087c7ca76b4539f9bc7d9068b701a8054585`  
		Last Modified: Tue, 18 Apr 2023 01:35:19 GMT  
		Size: 6.6 MB (6604111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd99e3413cacb724e75738256d7ae34f43ccb93122964be0ea699ffcc780ae6d`  
		Last Modified: Tue, 18 Apr 2023 01:35:19 GMT  
		Size: 3.6 MB (3603384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee999b3c3995eddaf919a60db441654b53a3390af8730f1b0a438577ec230068`  
		Last Modified: Tue, 18 Apr 2023 01:35:35 GMT  
		Size: 39.5 MB (39512803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.10-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8950cc9fc07e29fd9573ee916ff1e1e20a87ce63a3ce582471e7e7068d50417c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88360300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed0a57ba28d358bb99ed050b777f48faba8b19a18596c84507171a953dd5c76b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:21:42 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:21:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:21:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:21:43 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:21:45 GMT
ADD file:2f24914c3a2e66342aa7cf589af143b01a1cd7532c92c4263d251fb826b8b810 in / 
# Thu, 13 Apr 2023 13:21:46 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:45:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:46:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 00:47:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3b2b861f7bcaef2d589c1d8518a14da93644aafdcc9bfc5554895ed342bc341c`  
		Last Modified: Fri, 14 Apr 2023 09:57:14 GMT  
		Size: 32.1 MB (32098609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978ddb6b21e3fea6c8cb5970d8cd307a6ec15ef6b639b994cfdebe9384ef6e24`  
		Last Modified: Tue, 18 Apr 2023 01:03:02 GMT  
		Size: 7.8 MB (7751781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54556acf1bc962b10d66a29a9198cf3876dbc10be5d5899d89ee4ee01770250e`  
		Last Modified: Tue, 18 Apr 2023 01:03:01 GMT  
		Size: 4.4 MB (4362837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4db88fb9e9071e75f6c65177600cda26da9887d2574f51858808a6973fb9252`  
		Last Modified: Tue, 18 Apr 2023 01:03:29 GMT  
		Size: 44.1 MB (44147073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:22.10-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:99ca92b8905a1d95dfc35c299d441b4a1858d2538f1694510683b0320824beb9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75687009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637c9d75ac5352b4cbf7abcd1bf489b99d3901a9d7e6c435d32b9b2e5c820806`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:08:08 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:08:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:08:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:08:08 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:08:09 GMT
ADD file:df5733230d0258ecd0cbdcc7c2075865bc335200f2cafee8dacccfd082710b96 in / 
# Thu, 13 Apr 2023 13:08:10 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:05:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:06:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:06:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c450971bf0fd92eac91caf0b3126482e5fecadead22e59da08f9661a4b4f03be`  
		Last Modified: Fri, 14 Apr 2023 10:00:19 GMT  
		Size: 26.0 MB (26029287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded2cd498871df7ac556305ff379ade5376ed441cad7f51cf98b4867ac750d39`  
		Last Modified: Tue, 18 Apr 2023 01:14:11 GMT  
		Size: 6.5 MB (6467769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5cee9d25bba89e9b965d2fee1419c9d544d12c148be50fd20849d7f808bde1`  
		Last Modified: Tue, 18 Apr 2023 01:14:10 GMT  
		Size: 3.6 MB (3625375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36304f69d4e520034a19fbb9f1da633dd4722e9cdc720512923f71d850cc07d5`  
		Last Modified: Tue, 18 Apr 2023 01:14:24 GMT  
		Size: 39.6 MB (39564578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:23.04`

```console
$ docker pull buildpack-deps@sha256:8f30aeb6da27a92876d75b655895a20d8e7b78315a226232fd7ae946beec400d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:23.04` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c040bdb4d1eccb9d60dd883c8659fbf36a70b95230aec411f7752a8c9df7547c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.0 MB (263988698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ea1fdc55d3ba2d46c3a45c9262a09a41439e31a6d6370f6f97f83cc0f34fcc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:51:04 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:51:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:51:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:51:04 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:51:05 GMT
ADD file:0974d2aeef46c39070cbf74e10bf8644b9753060809b3c7100126a1bcb448f12 in / 
# Sat, 15 Apr 2023 04:51:06 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:30:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:31:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:31:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:34:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:43bb70e8bba148f5c5a4d50f8a5204951f795a069a2cd25b2e37ebafdd10afc7`  
		Last Modified: Tue, 18 Apr 2023 01:36:35 GMT  
		Size: 27.6 MB (27604045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d673d8abcf3e237b47c181613058fc86a03ce40e22cfa4a288287dffe5ef25d3`  
		Last Modified: Tue, 18 Apr 2023 01:36:33 GMT  
		Size: 6.4 MB (6382657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc90ad50e915047a562094b5a7813b9e3f81bb7782373cfac2a9fcbf7a5574a`  
		Last Modified: Tue, 18 Apr 2023 01:36:32 GMT  
		Size: 3.7 MB (3693225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbab6c6decb3beeb560234f8c7d7751604b70f7509abcff1a13111b80ae018a4`  
		Last Modified: Tue, 18 Apr 2023 01:36:50 GMT  
		Size: 44.3 MB (44256643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e5d1d102ea25927cc8832edc34d8152aab70036d9a4f916f543ede88760c4e`  
		Last Modified: Tue, 18 Apr 2023 01:37:22 GMT  
		Size: 182.1 MB (182052128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.04` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:000d7e40e49f456e833154c2d71353f3bddb12a02e2b0ba882978f93f9c6c56e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228579351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a1cef0b8f1ba77af697fcca31c23ab0d1ae072e54d4ed84cbc4a2c454709101`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:38:02 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:38:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:38:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:38:02 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:38:05 GMT
ADD file:9f0981aade24310bb7a4c492e6ec76e24f146f4efd6782ddba79ece3b8afe7b5 in / 
# Sat, 15 Apr 2023 04:38:05 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:44:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:45:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:45:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:48:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cc0ec898907bfe3505695fd5ae23b4cf5d6d180fdb036e767c23cc35a2abc39b`  
		Last Modified: Tue, 18 Apr 2023 01:51:15 GMT  
		Size: 25.4 MB (25437825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3711420f6b1b87fa85e1e1dde561aa26c9e0143e968d0ba9f6f98811b9e290`  
		Last Modified: Tue, 18 Apr 2023 01:51:12 GMT  
		Size: 5.5 MB (5545810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e741069d31363bff0e76178d15c895dcacd68407a20ce1c27f0a73ee511e61d8`  
		Last Modified: Tue, 18 Apr 2023 01:51:12 GMT  
		Size: 3.8 MB (3847237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4988e98a76edb96dc5fee90cb5d45db9378a4ba15f49647a098e4a4c4b888c77`  
		Last Modified: Tue, 18 Apr 2023 01:51:31 GMT  
		Size: 48.3 MB (48294473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892ba47d241faa5d135b9966167a61c95aad80e94b334d0b7ec63041f64fda43`  
		Last Modified: Tue, 18 Apr 2023 01:51:59 GMT  
		Size: 145.5 MB (145454006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.04` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7eb8a34ef8517f80859dc448e809c9c9078e6b8dacf23a6750cd0eae459b9487
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254284885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a583d5b43c43b667581b05b79463eba4d8cf6b9295ec519f94633ce5f61562a1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:41:09 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:41:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:41:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:41:10 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:41:17 GMT
ADD file:0a45cfb0f66cc6191e34ca0d42987f4ee1f86f70c5ee9a29ec3e353ceea7ce51 in / 
# Sat, 15 Apr 2023 04:41:18 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:29:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:30:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:30:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:33:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cc6919ddce2a233f58cc3e7dbe578e059849f4571e49c4a84c7c981f17a89835`  
		Last Modified: Tue, 18 Apr 2023 01:36:11 GMT  
		Size: 27.0 MB (27018561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9dfffa12a1f77a99f18745a89a98d7c560b403d259aaabb2ea7e8099aba267`  
		Last Modified: Tue, 18 Apr 2023 01:36:08 GMT  
		Size: 6.2 MB (6217841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b46934c541eaff8b64481ad9212943b45e46655b2e916d0a2a1edf56c835075`  
		Last Modified: Tue, 18 Apr 2023 01:36:09 GMT  
		Size: 3.7 MB (3653186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff58527001798506a9dc32ce859a3d047cc557aa033359f185d2451be24cf5b`  
		Last Modified: Tue, 18 Apr 2023 01:36:24 GMT  
		Size: 44.1 MB (44077916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55eb81a3584d1feea46abd6869b71852c54408ee766a0895b86d4915752208de`  
		Last Modified: Tue, 18 Apr 2023 01:36:49 GMT  
		Size: 173.3 MB (173317381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.04` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5090fa89cb4d665c6b029976d4d929e424390503a1f35135e12612c86f8d073e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.5 MB (288502540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29bf47b159469fa22c03c0456e2d2221865676486fbf95b847453b413e41ca0a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:51:08 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:51:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:51:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:51:09 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:51:11 GMT
ADD file:57838c4589ddbfb3bfb239d9d6749a36f0d7201d8788fa4293dfe9ad93308e40 in / 
# Sat, 15 Apr 2023 04:51:12 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:54:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:54:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 00:55:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:00:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fcabd7528fca87cc5a63f487865487cc2f6832df71a8c871f40b369f4f0f945d`  
		Last Modified: Tue, 18 Apr 2023 01:04:41 GMT  
		Size: 32.0 MB (31996733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd02da4adaf96b5e8dea2c0a2846b3cda00cb99c8a2af6a5da9996399bdab78`  
		Last Modified: Tue, 18 Apr 2023 01:04:36 GMT  
		Size: 7.4 MB (7364592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6bd36dd881e6a900302ba6370fbb475b14bf1dd9e35dc4209f84fb8c5065fb`  
		Last Modified: Tue, 18 Apr 2023 01:04:35 GMT  
		Size: 4.4 MB (4413806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11b8a0da4d0a3c624fb719be6321b9020894b77b2028fb6352c38403a1a77e6`  
		Last Modified: Tue, 18 Apr 2023 01:05:04 GMT  
		Size: 48.9 MB (48945236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1c1f4dc0b62d9d13e02a7d9066e7642d3a6440780c8ff95db3ba050af43976`  
		Last Modified: Tue, 18 Apr 2023 01:06:01 GMT  
		Size: 195.8 MB (195782173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.04` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:51c88a6dfccf081c6f31980cfce4183a66f188868648a9d6382e802317134227
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235447894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3f0864f3aba4bc5def98d2e8129dfbc7c9b623b4f64aa2d42cee71bc56f8a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:52:00 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:52:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:52:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:52:00 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:52:02 GMT
ADD file:fbea81511df0975bdcf894e5be93dc02670d76233449f6221b0a6752e6178646 in / 
# Sat, 15 Apr 2023 04:52:02 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:09:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:09:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:10:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:12:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:92338e21c9dcc2f2402a20239390e6f35f1a8beaa9ebf17ca317ce011b1cef40`  
		Last Modified: Tue, 18 Apr 2023 01:14:57 GMT  
		Size: 26.2 MB (26236111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1665ec17c4182267692bd75dd16a85d9e658f0f52656651e35f3c6856edf38f`  
		Last Modified: Tue, 18 Apr 2023 01:14:54 GMT  
		Size: 6.1 MB (6066022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435dc1ff769b0f8daba446a3386907dc4fe1be7df7f69e61b212baf2fb17ce18`  
		Last Modified: Tue, 18 Apr 2023 01:14:54 GMT  
		Size: 3.7 MB (3678419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af9b4b3cd888e49ca9b73654104bd6dafd3b084b47dbe8b9aa070a6fec27c58`  
		Last Modified: Tue, 18 Apr 2023 01:15:08 GMT  
		Size: 44.1 MB (44087604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8dfd448b2176a355c388f14e3c38c9a20244ab8c4a8f63df88fbe70b2f6630`  
		Last Modified: Tue, 18 Apr 2023 01:15:33 GMT  
		Size: 155.4 MB (155379738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:23.04-curl`

```console
$ docker pull buildpack-deps@sha256:a86b9ddf8bc507fe7814dfa053c530c7f3bdbf26759d272a6b0e92974ed084ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:23.04-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f309034a3bcb45ac60629303e126db07403cdb2a7e01389ac326498f0b2f3368
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37679927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220173d47bb64c458e18cdfea3dafd604370b15d4b684bcdc8d12c24f3e20246`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:51:04 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:51:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:51:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:51:04 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:51:05 GMT
ADD file:0974d2aeef46c39070cbf74e10bf8644b9753060809b3c7100126a1bcb448f12 in / 
# Sat, 15 Apr 2023 04:51:06 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:30:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:31:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:43bb70e8bba148f5c5a4d50f8a5204951f795a069a2cd25b2e37ebafdd10afc7`  
		Last Modified: Tue, 18 Apr 2023 01:36:35 GMT  
		Size: 27.6 MB (27604045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d673d8abcf3e237b47c181613058fc86a03ce40e22cfa4a288287dffe5ef25d3`  
		Last Modified: Tue, 18 Apr 2023 01:36:33 GMT  
		Size: 6.4 MB (6382657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc90ad50e915047a562094b5a7813b9e3f81bb7782373cfac2a9fcbf7a5574a`  
		Last Modified: Tue, 18 Apr 2023 01:36:32 GMT  
		Size: 3.7 MB (3693225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.04-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0db04bad5c5ec2a78f7cfa3f1b642bf737c44fdde8915d5423aa6b7ba7c65eb8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34830872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bd0ffae1c99ddc27c3872ac1d526dd3ccb5341b161b0518994bc0f8dd1b48a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:38:02 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:38:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:38:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:38:02 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:38:05 GMT
ADD file:9f0981aade24310bb7a4c492e6ec76e24f146f4efd6782ddba79ece3b8afe7b5 in / 
# Sat, 15 Apr 2023 04:38:05 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:44:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:45:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:cc0ec898907bfe3505695fd5ae23b4cf5d6d180fdb036e767c23cc35a2abc39b`  
		Last Modified: Tue, 18 Apr 2023 01:51:15 GMT  
		Size: 25.4 MB (25437825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3711420f6b1b87fa85e1e1dde561aa26c9e0143e968d0ba9f6f98811b9e290`  
		Last Modified: Tue, 18 Apr 2023 01:51:12 GMT  
		Size: 5.5 MB (5545810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e741069d31363bff0e76178d15c895dcacd68407a20ce1c27f0a73ee511e61d8`  
		Last Modified: Tue, 18 Apr 2023 01:51:12 GMT  
		Size: 3.8 MB (3847237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.04-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4e87da995eca42edb48757bdf7d1057b205ff73cd3e340a45187725b3b7a281a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36889588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3faa679b0465766abf4614a65c625b5d7e241b2071dd2e53956428742d68e1b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:41:09 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:41:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:41:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:41:10 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:41:17 GMT
ADD file:0a45cfb0f66cc6191e34ca0d42987f4ee1f86f70c5ee9a29ec3e353ceea7ce51 in / 
# Sat, 15 Apr 2023 04:41:18 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:29:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:30:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:cc6919ddce2a233f58cc3e7dbe578e059849f4571e49c4a84c7c981f17a89835`  
		Last Modified: Tue, 18 Apr 2023 01:36:11 GMT  
		Size: 27.0 MB (27018561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9dfffa12a1f77a99f18745a89a98d7c560b403d259aaabb2ea7e8099aba267`  
		Last Modified: Tue, 18 Apr 2023 01:36:08 GMT  
		Size: 6.2 MB (6217841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b46934c541eaff8b64481ad9212943b45e46655b2e916d0a2a1edf56c835075`  
		Last Modified: Tue, 18 Apr 2023 01:36:09 GMT  
		Size: 3.7 MB (3653186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.04-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f7f929427c910be5fe858e0f968e85d6e70d2d7168e8aae85e37ec03557f8c8a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43775131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d87006cf7cfef2979a32c9ffb816c8d07b7da92dcd2d041cd3bec310ce664690`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:51:08 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:51:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:51:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:51:09 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:51:11 GMT
ADD file:57838c4589ddbfb3bfb239d9d6749a36f0d7201d8788fa4293dfe9ad93308e40 in / 
# Sat, 15 Apr 2023 04:51:12 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:54:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:54:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:fcabd7528fca87cc5a63f487865487cc2f6832df71a8c871f40b369f4f0f945d`  
		Last Modified: Tue, 18 Apr 2023 01:04:41 GMT  
		Size: 32.0 MB (31996733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd02da4adaf96b5e8dea2c0a2846b3cda00cb99c8a2af6a5da9996399bdab78`  
		Last Modified: Tue, 18 Apr 2023 01:04:36 GMT  
		Size: 7.4 MB (7364592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6bd36dd881e6a900302ba6370fbb475b14bf1dd9e35dc4209f84fb8c5065fb`  
		Last Modified: Tue, 18 Apr 2023 01:04:35 GMT  
		Size: 4.4 MB (4413806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.04-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d1fe860c8e5b73d01ef34d19528360fb22471301f44f5d0983c10986da138bf6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35980552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e48719fe1a6ff3a99da9dcc66662d1f07f131663406f8df5491a5218fa013e4b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:52:00 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:52:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:52:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:52:00 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:52:02 GMT
ADD file:fbea81511df0975bdcf894e5be93dc02670d76233449f6221b0a6752e6178646 in / 
# Sat, 15 Apr 2023 04:52:02 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:09:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:09:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:92338e21c9dcc2f2402a20239390e6f35f1a8beaa9ebf17ca317ce011b1cef40`  
		Last Modified: Tue, 18 Apr 2023 01:14:57 GMT  
		Size: 26.2 MB (26236111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1665ec17c4182267692bd75dd16a85d9e658f0f52656651e35f3c6856edf38f`  
		Last Modified: Tue, 18 Apr 2023 01:14:54 GMT  
		Size: 6.1 MB (6066022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435dc1ff769b0f8daba446a3386907dc4fe1be7df7f69e61b212baf2fb17ce18`  
		Last Modified: Tue, 18 Apr 2023 01:14:54 GMT  
		Size: 3.7 MB (3678419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:23.04-scm`

```console
$ docker pull buildpack-deps@sha256:101eaaa881d244e5b86427bd2ea3986745db049d51b2efbcbe0f1d5408efa51e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:23.04-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:bbccbf35da61832e131a695eb66a451648c9fe24207019c396fcd9cdaf261c59
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81936570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2a3771bec692bafa9bf6b6d10c70540d0db0e39ed2f951458ba86af7f7e7c4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:51:04 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:51:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:51:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:51:04 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:51:05 GMT
ADD file:0974d2aeef46c39070cbf74e10bf8644b9753060809b3c7100126a1bcb448f12 in / 
# Sat, 15 Apr 2023 04:51:06 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:30:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:31:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:31:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:43bb70e8bba148f5c5a4d50f8a5204951f795a069a2cd25b2e37ebafdd10afc7`  
		Last Modified: Tue, 18 Apr 2023 01:36:35 GMT  
		Size: 27.6 MB (27604045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d673d8abcf3e237b47c181613058fc86a03ce40e22cfa4a288287dffe5ef25d3`  
		Last Modified: Tue, 18 Apr 2023 01:36:33 GMT  
		Size: 6.4 MB (6382657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc90ad50e915047a562094b5a7813b9e3f81bb7782373cfac2a9fcbf7a5574a`  
		Last Modified: Tue, 18 Apr 2023 01:36:32 GMT  
		Size: 3.7 MB (3693225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbab6c6decb3beeb560234f8c7d7751604b70f7509abcff1a13111b80ae018a4`  
		Last Modified: Tue, 18 Apr 2023 01:36:50 GMT  
		Size: 44.3 MB (44256643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.04-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8a9c907da4326f88024491a3da9762d29aa85c9ae4614dc8dbd65046f9d57918
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83125345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b8ef037b71f435f2efdf17ffe0b410ad38b4e58304c29569f0b121b7228e12`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:38:02 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:38:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:38:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:38:02 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:38:05 GMT
ADD file:9f0981aade24310bb7a4c492e6ec76e24f146f4efd6782ddba79ece3b8afe7b5 in / 
# Sat, 15 Apr 2023 04:38:05 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:44:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:45:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:45:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cc0ec898907bfe3505695fd5ae23b4cf5d6d180fdb036e767c23cc35a2abc39b`  
		Last Modified: Tue, 18 Apr 2023 01:51:15 GMT  
		Size: 25.4 MB (25437825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3711420f6b1b87fa85e1e1dde561aa26c9e0143e968d0ba9f6f98811b9e290`  
		Last Modified: Tue, 18 Apr 2023 01:51:12 GMT  
		Size: 5.5 MB (5545810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e741069d31363bff0e76178d15c895dcacd68407a20ce1c27f0a73ee511e61d8`  
		Last Modified: Tue, 18 Apr 2023 01:51:12 GMT  
		Size: 3.8 MB (3847237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4988e98a76edb96dc5fee90cb5d45db9378a4ba15f49647a098e4a4c4b888c77`  
		Last Modified: Tue, 18 Apr 2023 01:51:31 GMT  
		Size: 48.3 MB (48294473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.04-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ee060cbb2825a0e5c6d2c37a0f28eb460681bbc14451be3d563d3549f7365bfc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (80967504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2a9bce91e466eaf8d5721d6d72082a18ece9524f992f0fde72b08ce01455a6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:41:09 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:41:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:41:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:41:10 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:41:17 GMT
ADD file:0a45cfb0f66cc6191e34ca0d42987f4ee1f86f70c5ee9a29ec3e353ceea7ce51 in / 
# Sat, 15 Apr 2023 04:41:18 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:29:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:30:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:30:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cc6919ddce2a233f58cc3e7dbe578e059849f4571e49c4a84c7c981f17a89835`  
		Last Modified: Tue, 18 Apr 2023 01:36:11 GMT  
		Size: 27.0 MB (27018561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9dfffa12a1f77a99f18745a89a98d7c560b403d259aaabb2ea7e8099aba267`  
		Last Modified: Tue, 18 Apr 2023 01:36:08 GMT  
		Size: 6.2 MB (6217841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b46934c541eaff8b64481ad9212943b45e46655b2e916d0a2a1edf56c835075`  
		Last Modified: Tue, 18 Apr 2023 01:36:09 GMT  
		Size: 3.7 MB (3653186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff58527001798506a9dc32ce859a3d047cc557aa033359f185d2451be24cf5b`  
		Last Modified: Tue, 18 Apr 2023 01:36:24 GMT  
		Size: 44.1 MB (44077916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.04-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1fd6a50b6a6df0aaae7eecf4f25a23d66698a56a420fceac58859c82334c373c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92720367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2680105e7ba022355f1f320347591ffcaa718b8d1c7fb525bcbaa2bd1de940`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:51:08 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:51:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:51:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:51:09 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:51:11 GMT
ADD file:57838c4589ddbfb3bfb239d9d6749a36f0d7201d8788fa4293dfe9ad93308e40 in / 
# Sat, 15 Apr 2023 04:51:12 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:54:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:54:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 00:55:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fcabd7528fca87cc5a63f487865487cc2f6832df71a8c871f40b369f4f0f945d`  
		Last Modified: Tue, 18 Apr 2023 01:04:41 GMT  
		Size: 32.0 MB (31996733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd02da4adaf96b5e8dea2c0a2846b3cda00cb99c8a2af6a5da9996399bdab78`  
		Last Modified: Tue, 18 Apr 2023 01:04:36 GMT  
		Size: 7.4 MB (7364592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6bd36dd881e6a900302ba6370fbb475b14bf1dd9e35dc4209f84fb8c5065fb`  
		Last Modified: Tue, 18 Apr 2023 01:04:35 GMT  
		Size: 4.4 MB (4413806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11b8a0da4d0a3c624fb719be6321b9020894b77b2028fb6352c38403a1a77e6`  
		Last Modified: Tue, 18 Apr 2023 01:05:04 GMT  
		Size: 48.9 MB (48945236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:23.04-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:712fd37daa58220b07ef60020b33ade10599163dc40e476600099c7058b75bd8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80068156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dc83d080597d0511ef668ef12d04f8965d989d28c0896a33c9d5b0b3c59593`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:52:00 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:52:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:52:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:52:00 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:52:02 GMT
ADD file:fbea81511df0975bdcf894e5be93dc02670d76233449f6221b0a6752e6178646 in / 
# Sat, 15 Apr 2023 04:52:02 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:09:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:09:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:10:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:92338e21c9dcc2f2402a20239390e6f35f1a8beaa9ebf17ca317ce011b1cef40`  
		Last Modified: Tue, 18 Apr 2023 01:14:57 GMT  
		Size: 26.2 MB (26236111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1665ec17c4182267692bd75dd16a85d9e658f0f52656651e35f3c6856edf38f`  
		Last Modified: Tue, 18 Apr 2023 01:14:54 GMT  
		Size: 6.1 MB (6066022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435dc1ff769b0f8daba446a3386907dc4fe1be7df7f69e61b212baf2fb17ce18`  
		Last Modified: Tue, 18 Apr 2023 01:14:54 GMT  
		Size: 3.7 MB (3678419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af9b4b3cd888e49ca9b73654104bd6dafd3b084b47dbe8b9aa070a6fec27c58`  
		Last Modified: Tue, 18 Apr 2023 01:15:08 GMT  
		Size: 44.1 MB (44087604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bionic`

```console
$ docker pull buildpack-deps@sha256:fb154449c96034e2ac28a113cfbc31b7da0e4a21387c397dec6b1deec6d89d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bionic` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b1da6a5f500b67fa28bbae2b90a8e9da4def283d1fb918b1d4db0c9cd86ec183
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 MB (221417037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeecfa359fe257650879cc03de2c96ee1ab252d40eaf9467a855893ac7df28f5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:22:42 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:22:44 GMT
ADD file:4560926e076acae6b8396a9f1e760eee0f53e22e90ce8554dda57f1103547795 in / 
# Wed, 08 Mar 2023 03:22:44 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:21:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:21:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 05:22:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:24:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cd150c608fee7837e3a5b28be5c7b540eaf4efa27b3b755d55326470691ce2df`  
		Last Modified: Sun, 12 Mar 2023 07:24:55 GMT  
		Size: 26.7 MB (26710746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c78e6dac9cec3c01ca7687f8e0a53a4b5e9b04f4910729279be4204ce5360e`  
		Last Modified: Thu, 16 Mar 2023 05:41:29 GMT  
		Size: 6.6 MB (6617364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b18b892afad36455b3ae75f0ab2c1bc45822e03069f2667faa4bede3825be5`  
		Last Modified: Thu, 16 Mar 2023 05:41:28 GMT  
		Size: 3.0 MB (3026128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c57462ca1fd8565d56aa476a7fa497011a11c6f761194b368d2c722e146b20`  
		Last Modified: Thu, 16 Mar 2023 05:41:43 GMT  
		Size: 45.5 MB (45514749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f391d58903094b86c56fd169ec96c398321c3ccab4f8893113f4de938d003a`  
		Last Modified: Thu, 16 Mar 2023 05:42:10 GMT  
		Size: 139.5 MB (139548050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1f740f07a329775404244fd36ca65500a61ecd79c38851ee6ce6408443fa9779
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189581013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb26767826b27bb17bc813102a23903c31d4ea475f341486310a77dd6e54d766`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:27:01 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:27:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:27:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:27:01 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:27:08 GMT
ADD file:21d7947367fe1aa8cc668c943d11c4841b0ead14b9103ef46fb8db8084603a75 in / 
# Wed, 08 Mar 2023 03:27:09 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:44:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:45:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 03:45:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:47:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9fb42489e9f507aa183ef669baec25f94b8c4c22159a4ccc23a1977cedd0d1fa`  
		Last Modified: Thu, 16 Mar 2023 03:39:03 GMT  
		Size: 22.3 MB (22305374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2b71966fc2f22e1375423fb61221ed137cf5e7e8d202bfa403292ba600daab`  
		Last Modified: Thu, 16 Mar 2023 04:07:46 GMT  
		Size: 5.7 MB (5681012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebcf04b4bbda07472ffbb83ab11cb71b6ff2c6bef9749979a8a3981f285c0f53`  
		Last Modified: Thu, 16 Mar 2023 04:07:46 GMT  
		Size: 2.6 MB (2586979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3058bdcdd1b82bda414133ce433d46f98b5f56911e44f00ff6bd1de1c0a6caba`  
		Last Modified: Thu, 16 Mar 2023 04:08:04 GMT  
		Size: 40.7 MB (40713543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d88abc5604e52bcee192566d8fae426f1031f855abd4229bd8c43feeb2648d`  
		Last Modified: Thu, 16 Mar 2023 04:08:30 GMT  
		Size: 118.3 MB (118294105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2c9e464ea859a1b832272828463904e3f9c04bdebf0e7aa9cdc4c6c48481c85e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (206011203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b97289739597eaf439933630ebefa90822ac12cd90c8157a55e7b3f32763f4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:25:33 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:25:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:25:35 GMT
ADD file:5f229d85bac2e85aa7ce97b2168fc61bd401d0151e8940a12d244356f984e65f in / 
# Wed, 08 Mar 2023 03:25:35 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:58:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:58:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 03:59:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:02:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c21a0233221a76e66b6c10d2445f591bd28eb0773e6cb539474d6dca9ea0b594`  
		Last Modified: Sun, 12 Mar 2023 07:27:31 GMT  
		Size: 23.7 MB (23734706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc06fc1cf8ad0140062ec53dbc631cea853ddb72d7c0b353edd743b1dca4ceb`  
		Last Modified: Thu, 16 Mar 2023 04:21:50 GMT  
		Size: 6.1 MB (6057809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33d0b4e623a1829e474acf7b4d21109a9f27c7d8c8bf12f163ffe645eed93ec`  
		Last Modified: Thu, 16 Mar 2023 04:21:49 GMT  
		Size: 2.8 MB (2790695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37de71f159d52bbc91be8b71a2d8862f89e2c137ac5d4e17c923aaa4fa5aa30`  
		Last Modified: Thu, 16 Mar 2023 04:22:03 GMT  
		Size: 43.3 MB (43311869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc13acad8ae8946317f508f7e0eda6de200ca13831f7433e58942f2466c21473`  
		Last Modified: Thu, 16 Mar 2023 04:22:25 GMT  
		Size: 130.1 MB (130116124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d189ba12fe145c64ea06852f5de7d0ab170ab04daca4c5effd4a4705cabb888e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 MB (218710648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc3d7329f212c3056b20a7f0084491a4e3d07e63c6848a789189f5137e2d75d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:13:19 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:13:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:13:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:13:19 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:13:21 GMT
ADD file:6cf3e34995c6c44762ed692b86a0442d981e9a69fa4288960047e505d75c0223 in / 
# Wed, 08 Mar 2023 03:13:22 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:56:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:56:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 01:57:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:00:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c58af8b772f2ca9c63db81d620e48946c13c027ecd7ab2d9062d010ca2ed11f3`  
		Last Modified: Thu, 16 Mar 2023 01:54:42 GMT  
		Size: 27.2 MB (27164610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1df9a7dbeea70a625098ba195b5c6a6046e010992d4b2616b74e5efca85ff0`  
		Last Modified: Thu, 16 Mar 2023 02:02:18 GMT  
		Size: 6.9 MB (6907798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9c7488bcb45de5faeb1bc3f4a19015817de4a09d3c762c619d48aa2855322e`  
		Last Modified: Thu, 16 Mar 2023 02:02:17 GMT  
		Size: 3.3 MB (3255693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54663dad9d7f237e7f0a0a533af683ae66d66098cdd57ea8f90fde4dd8897ffb`  
		Last Modified: Thu, 16 Mar 2023 02:02:38 GMT  
		Size: 47.1 MB (47095486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5e9e49852091a0f82ca614c93efb7802ff6bbabc0da2e14b9606920c072cb6`  
		Last Modified: Thu, 16 Mar 2023 02:03:15 GMT  
		Size: 134.3 MB (134287061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:093d533487c60b2c92363199f07f041884638f879f09c20c9aa303e056b1267c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246441203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dcd83e221d1f7aaec4fdcb03d7776c2eadf8d9cf89c85eaba5ab7f7793f25ed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:13:23 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:13:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:13:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:13:23 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:13:26 GMT
ADD file:5ea8615c09f693252cb9d45458421679f82f84d315200a7611165869195b3a69 in / 
# Wed, 08 Mar 2023 03:13:26 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:07:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:07:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 03:08:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:14:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1c668e1b654ae9320eeecdef5ebc0faea219f3828f6cd3a05983984863b60058`  
		Last Modified: Thu, 16 Mar 2023 01:43:01 GMT  
		Size: 30.4 MB (30441944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e5cf4c1f014d5508f129bb3d2e36a3448b5d92b400a35d3051160723af42b4`  
		Last Modified: Thu, 16 Mar 2023 03:47:41 GMT  
		Size: 7.0 MB (7036943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a259ed8117f57e3f76e8e31ddb857f6d36e8f1ac8131d38a456833aa7e0c20`  
		Last Modified: Thu, 16 Mar 2023 03:47:40 GMT  
		Size: 3.7 MB (3740612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409f528497ffaa0bc9ae78b8139359ddd38315caf439a39a670aaed487c6c06d`  
		Last Modified: Thu, 16 Mar 2023 03:48:07 GMT  
		Size: 53.7 MB (53736792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22095eabcbee3060dd218f09d76cf296a873b1a36d1d4f86794d105fe7e5ec5f`  
		Last Modified: Thu, 16 Mar 2023 03:48:53 GMT  
		Size: 151.5 MB (151484912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0c8e0a8e8c0a624863dcfee0278ed624183fd34de9612945d2db9d6842c229d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.8 MB (205782934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8557c42f5d0087a913e9c89b40998da81a7d55355bad38d52f6b3f7699f2681b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:23:29 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:23:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:23:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:23:29 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:23:31 GMT
ADD file:a6309e462d28398152cb726a11615118d79858da963b8c614772b87d87465967 in / 
# Wed, 08 Mar 2023 03:23:31 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:43:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:43:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 01:44:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:46:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3a2279f06ab19f0d57823e69b999f54a344e28bd9f955b4db9a5875c0caa543a`  
		Last Modified: Thu, 16 Mar 2023 02:01:03 GMT  
		Size: 25.4 MB (25370993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb37be097f66ed2ca5a62bf5e79eee23cbae99ae37fa4214bd021813206a4896`  
		Last Modified: Thu, 16 Mar 2023 02:01:00 GMT  
		Size: 6.3 MB (6310585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffee9aa0246535c2e55658c3cb0a6996668f7a403a4b960a9fdbcd4d42847f3`  
		Last Modified: Thu, 16 Mar 2023 02:00:59 GMT  
		Size: 3.0 MB (2976589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc2dd868684ceaf83a27108c1b52ca7a6e8f3b0168ad780911abc88235bfb03`  
		Last Modified: Thu, 16 Mar 2023 02:01:18 GMT  
		Size: 45.0 MB (45040946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df620083a573baec7672a8d7b904f0c02ababd741e0ace4108dda4b119901ee2`  
		Last Modified: Thu, 16 Mar 2023 02:01:42 GMT  
		Size: 126.1 MB (126083821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bionic-curl`

```console
$ docker pull buildpack-deps@sha256:3fd8a96d4a8804a8424ff1593c4b2858231aa0c710e83e5c826fab6724f4037f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bionic-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:edc4ef3195e1d82ba936e48a088384a87de4ef1e079743cf63a8590eb9a20bfd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36354238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c36747240a25171490608a4897f503021ceb197cb460e20444ca7089a2453ea7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:22:42 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:22:44 GMT
ADD file:4560926e076acae6b8396a9f1e760eee0f53e22e90ce8554dda57f1103547795 in / 
# Wed, 08 Mar 2023 03:22:44 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:21:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:21:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:cd150c608fee7837e3a5b28be5c7b540eaf4efa27b3b755d55326470691ce2df`  
		Last Modified: Sun, 12 Mar 2023 07:24:55 GMT  
		Size: 26.7 MB (26710746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c78e6dac9cec3c01ca7687f8e0a53a4b5e9b04f4910729279be4204ce5360e`  
		Last Modified: Thu, 16 Mar 2023 05:41:29 GMT  
		Size: 6.6 MB (6617364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b18b892afad36455b3ae75f0ab2c1bc45822e03069f2667faa4bede3825be5`  
		Last Modified: Thu, 16 Mar 2023 05:41:28 GMT  
		Size: 3.0 MB (3026128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:37305f1fffd9b6e8b98b050b702e595498870f5d0cf8cbc4d2e30cdcc7b2177a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30573365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45de6bc525f3e1c8327e7663ff847e537821bb211ca5fe282aa4fe66f79c36f8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:27:01 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:27:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:27:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:27:01 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:27:08 GMT
ADD file:21d7947367fe1aa8cc668c943d11c4841b0ead14b9103ef46fb8db8084603a75 in / 
# Wed, 08 Mar 2023 03:27:09 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:44:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:45:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:9fb42489e9f507aa183ef669baec25f94b8c4c22159a4ccc23a1977cedd0d1fa`  
		Last Modified: Thu, 16 Mar 2023 03:39:03 GMT  
		Size: 22.3 MB (22305374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2b71966fc2f22e1375423fb61221ed137cf5e7e8d202bfa403292ba600daab`  
		Last Modified: Thu, 16 Mar 2023 04:07:46 GMT  
		Size: 5.7 MB (5681012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebcf04b4bbda07472ffbb83ab11cb71b6ff2c6bef9749979a8a3981f285c0f53`  
		Last Modified: Thu, 16 Mar 2023 04:07:46 GMT  
		Size: 2.6 MB (2586979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bbaa8d87e02533fb9f0e332551bec711913649f23f663cb20c4c47c5323680f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32583210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3656a9cc190e6da3224283797ac375e158b4a022d1d5a3d2bb49d9dac0b85124`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:25:33 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:25:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:25:35 GMT
ADD file:5f229d85bac2e85aa7ce97b2168fc61bd401d0151e8940a12d244356f984e65f in / 
# Wed, 08 Mar 2023 03:25:35 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:58:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:58:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:c21a0233221a76e66b6c10d2445f591bd28eb0773e6cb539474d6dca9ea0b594`  
		Last Modified: Sun, 12 Mar 2023 07:27:31 GMT  
		Size: 23.7 MB (23734706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc06fc1cf8ad0140062ec53dbc631cea853ddb72d7c0b353edd743b1dca4ceb`  
		Last Modified: Thu, 16 Mar 2023 04:21:50 GMT  
		Size: 6.1 MB (6057809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33d0b4e623a1829e474acf7b4d21109a9f27c7d8c8bf12f163ffe645eed93ec`  
		Last Modified: Thu, 16 Mar 2023 04:21:49 GMT  
		Size: 2.8 MB (2790695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c88613067a38450529dace018781fd35548bed5b209c241a5262b458b0e48a52
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37328101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e48e7492b46c775c749e6d5febf5731b1aeface4bf187ab7edb99482a1e0f64`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:13:19 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:13:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:13:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:13:19 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:13:21 GMT
ADD file:6cf3e34995c6c44762ed692b86a0442d981e9a69fa4288960047e505d75c0223 in / 
# Wed, 08 Mar 2023 03:13:22 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:56:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:56:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:c58af8b772f2ca9c63db81d620e48946c13c027ecd7ab2d9062d010ca2ed11f3`  
		Last Modified: Thu, 16 Mar 2023 01:54:42 GMT  
		Size: 27.2 MB (27164610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1df9a7dbeea70a625098ba195b5c6a6046e010992d4b2616b74e5efca85ff0`  
		Last Modified: Thu, 16 Mar 2023 02:02:18 GMT  
		Size: 6.9 MB (6907798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9c7488bcb45de5faeb1bc3f4a19015817de4a09d3c762c619d48aa2855322e`  
		Last Modified: Thu, 16 Mar 2023 02:02:17 GMT  
		Size: 3.3 MB (3255693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:93af7cd2c9b2348c3885ca9fad668d06a219296d9c2032725a0d3de25878e908
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41219499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1588570491594531960cec00e2bb87f2fb1b48f878dc4d6bd888024f30e1de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:13:23 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:13:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:13:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:13:23 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:13:26 GMT
ADD file:5ea8615c09f693252cb9d45458421679f82f84d315200a7611165869195b3a69 in / 
# Wed, 08 Mar 2023 03:13:26 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:07:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:07:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:1c668e1b654ae9320eeecdef5ebc0faea219f3828f6cd3a05983984863b60058`  
		Last Modified: Thu, 16 Mar 2023 01:43:01 GMT  
		Size: 30.4 MB (30441944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e5cf4c1f014d5508f129bb3d2e36a3448b5d92b400a35d3051160723af42b4`  
		Last Modified: Thu, 16 Mar 2023 03:47:41 GMT  
		Size: 7.0 MB (7036943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a259ed8117f57e3f76e8e31ddb857f6d36e8f1ac8131d38a456833aa7e0c20`  
		Last Modified: Thu, 16 Mar 2023 03:47:40 GMT  
		Size: 3.7 MB (3740612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:20ebcda199381e882997d1cb49046a4a86cf2a4d85ec17a0d4cf03c2342dee11
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34658167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f626e5ed1171f12e2d4e06623f35558e748ecc2010eb93c132ab27524b2b55b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:23:29 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:23:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:23:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:23:29 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:23:31 GMT
ADD file:a6309e462d28398152cb726a11615118d79858da963b8c614772b87d87465967 in / 
# Wed, 08 Mar 2023 03:23:31 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:43:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:43:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3a2279f06ab19f0d57823e69b999f54a344e28bd9f955b4db9a5875c0caa543a`  
		Last Modified: Thu, 16 Mar 2023 02:01:03 GMT  
		Size: 25.4 MB (25370993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb37be097f66ed2ca5a62bf5e79eee23cbae99ae37fa4214bd021813206a4896`  
		Last Modified: Thu, 16 Mar 2023 02:01:00 GMT  
		Size: 6.3 MB (6310585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffee9aa0246535c2e55658c3cb0a6996668f7a403a4b960a9fdbcd4d42847f3`  
		Last Modified: Thu, 16 Mar 2023 02:00:59 GMT  
		Size: 3.0 MB (2976589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bionic-scm`

```console
$ docker pull buildpack-deps@sha256:341aade2e27224f02ffa8406356d222ae812b4b877d9cae398a6f1c9c8aa1fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bionic-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c5ed4186cca291cb15e4a3ec07c8f72214eecb664ab6000d21de81b4ef3c22eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81868987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee72242d4f5e40206fc21b1eda028beb28d7d73857bfdba0cc421a166b05b081`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:22:42 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:22:44 GMT
ADD file:4560926e076acae6b8396a9f1e760eee0f53e22e90ce8554dda57f1103547795 in / 
# Wed, 08 Mar 2023 03:22:44 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:21:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:21:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 05:22:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cd150c608fee7837e3a5b28be5c7b540eaf4efa27b3b755d55326470691ce2df`  
		Last Modified: Sun, 12 Mar 2023 07:24:55 GMT  
		Size: 26.7 MB (26710746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c78e6dac9cec3c01ca7687f8e0a53a4b5e9b04f4910729279be4204ce5360e`  
		Last Modified: Thu, 16 Mar 2023 05:41:29 GMT  
		Size: 6.6 MB (6617364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b18b892afad36455b3ae75f0ab2c1bc45822e03069f2667faa4bede3825be5`  
		Last Modified: Thu, 16 Mar 2023 05:41:28 GMT  
		Size: 3.0 MB (3026128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c57462ca1fd8565d56aa476a7fa497011a11c6f761194b368d2c722e146b20`  
		Last Modified: Thu, 16 Mar 2023 05:41:43 GMT  
		Size: 45.5 MB (45514749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1f9d5b0d3c5fb26bbcb17109b65208ac2a36d7a6a4253289e090c1e39fbe1744
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71286908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf91a3d86cf7e62586cfa021d5d042c3f8ad4473ddc03742ce5fe9199395303a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:27:01 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:27:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:27:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:27:01 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:27:08 GMT
ADD file:21d7947367fe1aa8cc668c943d11c4841b0ead14b9103ef46fb8db8084603a75 in / 
# Wed, 08 Mar 2023 03:27:09 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:44:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:45:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 03:45:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9fb42489e9f507aa183ef669baec25f94b8c4c22159a4ccc23a1977cedd0d1fa`  
		Last Modified: Thu, 16 Mar 2023 03:39:03 GMT  
		Size: 22.3 MB (22305374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2b71966fc2f22e1375423fb61221ed137cf5e7e8d202bfa403292ba600daab`  
		Last Modified: Thu, 16 Mar 2023 04:07:46 GMT  
		Size: 5.7 MB (5681012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebcf04b4bbda07472ffbb83ab11cb71b6ff2c6bef9749979a8a3981f285c0f53`  
		Last Modified: Thu, 16 Mar 2023 04:07:46 GMT  
		Size: 2.6 MB (2586979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3058bdcdd1b82bda414133ce433d46f98b5f56911e44f00ff6bd1de1c0a6caba`  
		Last Modified: Thu, 16 Mar 2023 04:08:04 GMT  
		Size: 40.7 MB (40713543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:127e2166fb2409edd8d8b5261a115a0e2aec1641f2bc70769b51e60924fda8eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75895079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c55e4c16477e8e6ec9875fa4a0fc1eb3184b34403fb222976e5a361d5ab3466`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:25:33 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:25:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:25:35 GMT
ADD file:5f229d85bac2e85aa7ce97b2168fc61bd401d0151e8940a12d244356f984e65f in / 
# Wed, 08 Mar 2023 03:25:35 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:58:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:58:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 03:59:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c21a0233221a76e66b6c10d2445f591bd28eb0773e6cb539474d6dca9ea0b594`  
		Last Modified: Sun, 12 Mar 2023 07:27:31 GMT  
		Size: 23.7 MB (23734706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc06fc1cf8ad0140062ec53dbc631cea853ddb72d7c0b353edd743b1dca4ceb`  
		Last Modified: Thu, 16 Mar 2023 04:21:50 GMT  
		Size: 6.1 MB (6057809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33d0b4e623a1829e474acf7b4d21109a9f27c7d8c8bf12f163ffe645eed93ec`  
		Last Modified: Thu, 16 Mar 2023 04:21:49 GMT  
		Size: 2.8 MB (2790695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37de71f159d52bbc91be8b71a2d8862f89e2c137ac5d4e17c923aaa4fa5aa30`  
		Last Modified: Thu, 16 Mar 2023 04:22:03 GMT  
		Size: 43.3 MB (43311869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:06347734d5e392a96f4432d6290610b9761773fe58a4467957bb5ac5c104e085
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84423587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea41bed709b37c2011e131b1f224971e01f761e9a8b0c487987ca43d939e5062`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:13:19 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:13:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:13:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:13:19 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:13:21 GMT
ADD file:6cf3e34995c6c44762ed692b86a0442d981e9a69fa4288960047e505d75c0223 in / 
# Wed, 08 Mar 2023 03:13:22 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:56:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:56:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 01:57:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c58af8b772f2ca9c63db81d620e48946c13c027ecd7ab2d9062d010ca2ed11f3`  
		Last Modified: Thu, 16 Mar 2023 01:54:42 GMT  
		Size: 27.2 MB (27164610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1df9a7dbeea70a625098ba195b5c6a6046e010992d4b2616b74e5efca85ff0`  
		Last Modified: Thu, 16 Mar 2023 02:02:18 GMT  
		Size: 6.9 MB (6907798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9c7488bcb45de5faeb1bc3f4a19015817de4a09d3c762c619d48aa2855322e`  
		Last Modified: Thu, 16 Mar 2023 02:02:17 GMT  
		Size: 3.3 MB (3255693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54663dad9d7f237e7f0a0a533af683ae66d66098cdd57ea8f90fde4dd8897ffb`  
		Last Modified: Thu, 16 Mar 2023 02:02:38 GMT  
		Size: 47.1 MB (47095486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:47ffaea8984e18680bf34023dc84dbbc005a5c50b47cb92e9221be8e55ce28a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (94956291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e8cb730f01b5b2426648fed56c18477b531abea23c6d47db1eacc88079b2ab4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:13:23 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:13:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:13:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:13:23 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:13:26 GMT
ADD file:5ea8615c09f693252cb9d45458421679f82f84d315200a7611165869195b3a69 in / 
# Wed, 08 Mar 2023 03:13:26 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:07:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:07:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 03:08:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1c668e1b654ae9320eeecdef5ebc0faea219f3828f6cd3a05983984863b60058`  
		Last Modified: Thu, 16 Mar 2023 01:43:01 GMT  
		Size: 30.4 MB (30441944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e5cf4c1f014d5508f129bb3d2e36a3448b5d92b400a35d3051160723af42b4`  
		Last Modified: Thu, 16 Mar 2023 03:47:41 GMT  
		Size: 7.0 MB (7036943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a259ed8117f57e3f76e8e31ddb857f6d36e8f1ac8131d38a456833aa7e0c20`  
		Last Modified: Thu, 16 Mar 2023 03:47:40 GMT  
		Size: 3.7 MB (3740612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409f528497ffaa0bc9ae78b8139359ddd38315caf439a39a670aaed487c6c06d`  
		Last Modified: Thu, 16 Mar 2023 03:48:07 GMT  
		Size: 53.7 MB (53736792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3e5c483b07d9d0b5a4f4dbb989320ab32f2ccc83e8b565759f680a7659b1961c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79699113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d8b61386e03e4309345be55e3dd943e007820aadcbcc64fb24e1524fea86052`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:23:29 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:23:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:23:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:23:29 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:23:31 GMT
ADD file:a6309e462d28398152cb726a11615118d79858da963b8c614772b87d87465967 in / 
# Wed, 08 Mar 2023 03:23:31 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:43:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:43:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 01:44:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3a2279f06ab19f0d57823e69b999f54a344e28bd9f955b4db9a5875c0caa543a`  
		Last Modified: Thu, 16 Mar 2023 02:01:03 GMT  
		Size: 25.4 MB (25370993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb37be097f66ed2ca5a62bf5e79eee23cbae99ae37fa4214bd021813206a4896`  
		Last Modified: Thu, 16 Mar 2023 02:01:00 GMT  
		Size: 6.3 MB (6310585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffee9aa0246535c2e55658c3cb0a6996668f7a403a4b960a9fdbcd4d42847f3`  
		Last Modified: Thu, 16 Mar 2023 02:00:59 GMT  
		Size: 3.0 MB (2976589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc2dd868684ceaf83a27108c1b52ca7a6e8f3b0168ad780911abc88235bfb03`  
		Last Modified: Thu, 16 Mar 2023 02:01:18 GMT  
		Size: 45.0 MB (45040946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bookworm`

```console
$ docker pull buildpack-deps@sha256:f95b9908ce0e8045cd9bd8a2fe52392ff1cbe65f1656d5a78931ecdc23feb7eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bookworm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d2831f26a1be4155a536403a4091c9fa3578d932016713ad45c204a54ef9bbe0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.9 MB (345874026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8740ff589a8566528392543b04f5042041d597aebdf89a8351ad91a78b3c798`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:35 GMT
ADD file:1cb6c660a2e3ea14b2a11bb8b80f53920c3da423a0ad7004391bfab4db4d0177 in / 
# Wed, 12 Apr 2023 00:19:36 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:48:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:49:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 07:49:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:50:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cc556c281183180fae02d57fa6fb60ed0a99d9040936278743dc4022bfb0c686`  
		Last Modified: Wed, 12 Apr 2023 00:22:48 GMT  
		Size: 49.3 MB (49292938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8022b43d7c31d74c341d297cf10031ff0c51f596473a0c1945ee83a841094638`  
		Last Modified: Wed, 12 Apr 2023 07:56:29 GMT  
		Size: 9.1 MB (9083160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db75f726ec67539c4823cb16851963ebe5838a853b0e769fd662020fad918781`  
		Last Modified: Wed, 12 Apr 2023 07:56:29 GMT  
		Size: 11.4 MB (11422437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8a9e299258b84de99d6d739eb84b5b1632005f9c7723f2dd9e209fb1a8aaa3`  
		Last Modified: Wed, 12 Apr 2023 07:56:46 GMT  
		Size: 64.1 MB (64097699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5269c0251f891649bf20972368b34411b22208df54ce5c4b1b9eb649793edbb`  
		Last Modified: Wed, 12 Apr 2023 07:57:20 GMT  
		Size: 212.0 MB (211977792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ca3000a5c2c81e15247951e66c081c65117913ded0f177159d6c15adf29997c5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.6 MB (314581039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7816bfe042349b0c7c87b9c180f83b2294e7e688a27afa564c62ce1bbbe48fa1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:48:19 GMT
ADD file:df1103dce44baa95c92287ab5016f36d5cc45c6062116ebf5273f7e79a00915c in / 
# Wed, 12 Apr 2023 00:48:20 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:11:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:11:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:12:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:15:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:795c0ca2726dffdb0e5ef6ffa341d17ec672d5915011f1a93a05e8c95a4779ae`  
		Last Modified: Wed, 12 Apr 2023 00:50:12 GMT  
		Size: 48.1 MB (48110879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e70c1a23fdf0fd320a61a2506f0ca4a391a319de8403734e4af8d678a6081fc`  
		Last Modified: Wed, 12 Apr 2023 01:20:09 GMT  
		Size: 8.5 MB (8523001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27111cd5fb1057675f2e0b269790dc264d344d6e4b7ad92ff941f90a496167b`  
		Last Modified: Wed, 12 Apr 2023 01:20:09 GMT  
		Size: 11.1 MB (11065924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ed8d7f4b0f78246beda91a51ddbc4ab368fe6f04bb2432498c3f5a76cbc010`  
		Last Modified: Wed, 12 Apr 2023 01:20:30 GMT  
		Size: 61.5 MB (61541287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e7bffea89dcea5595c3a9d4dcd9ae2c5876dacb4265050ed658554b4d6da420`  
		Last Modified: Wed, 12 Apr 2023 01:21:06 GMT  
		Size: 185.3 MB (185339948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a95980932c697cd75fe78313b6c518454ecebe4a2a0e247d9f1e6210eb31e041
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.9 MB (299884114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f23b6bbc84faa85b393ae1cdc942b366a444b75550e6e70cffe1fa7b80024b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:10 GMT
ADD file:aa1c08333544c05fc5317d775ee99af7479c6fa5f35b74652f6126a7a5099958 in / 
# Tue, 11 Apr 2023 23:59:11 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:32:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:32:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:32:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:35:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:81b1dd69f2a38ad14b0919ab9c395aafeb137158539ab6531ac5743690a0ebb7`  
		Last Modified: Wed, 12 Apr 2023 00:02:26 GMT  
		Size: 45.9 MB (45883114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f399f5abf6c810daac72b311feda8726e38c0c228183ccf5d0da4de0b8ec79f4`  
		Last Modified: Wed, 12 Apr 2023 09:43:59 GMT  
		Size: 8.2 MB (8169132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3453014a13bae733f0a1d38594c31a25841303277602f61394efaff085c42288`  
		Last Modified: Wed, 12 Apr 2023 09:43:59 GMT  
		Size: 10.7 MB (10690179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1d5c89a8ad9820582b69420d902dbb04e78a440ab16e42dd52a5778aea37e4`  
		Last Modified: Wed, 12 Apr 2023 09:44:19 GMT  
		Size: 59.2 MB (59247424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac4f8fdeee401c8aa14952b7737a316db27f53eb8c98736aeefa5111187e4c5`  
		Last Modified: Wed, 12 Apr 2023 09:44:56 GMT  
		Size: 175.9 MB (175894265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:93e13c1041833e26336a9a4362a935021cb140f05c425f7cda66b1d288da141d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.0 MB (337000447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4817e1bdddcea21ae977e3e5b270332950842257559a3ae2efe4a18f83f1110e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:27 GMT
ADD file:efed18ef2a003bff7e64e7049455216e51876402083581032c35085328e416f6 in / 
# Wed, 12 Apr 2023 00:39:28 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:04:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:04:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:04:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:06:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0f987ce91d920ae0a705ed6c9824f1bbbfa282defb8986614030eb8e2bc0b4e`  
		Last Modified: Wed, 12 Apr 2023 00:41:45 GMT  
		Size: 49.3 MB (49345365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e6a618ee06e99ebfbb7809c1cc4902cb717d294243f3765f170fd1c8eaf94a`  
		Last Modified: Wed, 12 Apr 2023 01:12:23 GMT  
		Size: 8.9 MB (8915044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59c3f19470d2fd9e1407a7ddcbac3c316a999a143865347f221db18517e0838`  
		Last Modified: Wed, 12 Apr 2023 01:12:24 GMT  
		Size: 11.4 MB (11389565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b373ae05bf678c385bace283c65197a2bbc2a334c528ed7b58a01d93131de585`  
		Last Modified: Wed, 12 Apr 2023 01:12:39 GMT  
		Size: 64.0 MB (63974624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a4f590cd785a4e380e2e92cca3c7b2d82be15d89bb52da582994cc39d9bdd5`  
		Last Modified: Wed, 12 Apr 2023 01:13:07 GMT  
		Size: 203.4 MB (203375849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:34c578f8d193ff514ac530b8922a3055877b2d87cc4e289f31e765c7450ed112
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.4 MB (348376060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7d23d91b6b9538e488de01d18982225f2c00d113996363a9198e3a7dc32c14`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:38:30 GMT
ADD file:7718865253a3489583d40f8c7a7beede0c20cebbab68bb3e97ad2e84082afcb7 in / 
# Wed, 12 Apr 2023 00:38:30 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:02:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:02:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:03:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:05:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a4ce9e81f634822e5166ef3eef875a4140795ac18afe0391433d72c7865bf67b`  
		Last Modified: Wed, 12 Apr 2023 00:41:43 GMT  
		Size: 50.3 MB (50317977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e54183fe5cb0866f886a93c0d098d38e649286a2b516b64d9658dd40f5d74b`  
		Last Modified: Wed, 12 Apr 2023 01:13:34 GMT  
		Size: 9.3 MB (9264042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76896a8c48193a86329dc809066c177aedc76d55811eb32ca7c80c1ab06f66f1`  
		Last Modified: Wed, 12 Apr 2023 01:13:34 GMT  
		Size: 11.8 MB (11827045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba7e1ed0df9a2a8a6501d91360cea22ab988653bf057d73c44ecb41e49f6151`  
		Last Modified: Wed, 12 Apr 2023 01:13:56 GMT  
		Size: 66.0 MB (65960427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4551baecfb99d1499518d7ef04818e3c6d649ec19322e320b452af6855389592`  
		Last Modified: Wed, 12 Apr 2023 01:14:43 GMT  
		Size: 211.0 MB (211006569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:23311ac289d337013971c368b465b0986aaed3f32cdbb0a775d92e4772069c65
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.4 MB (322418858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40969785f199073c1927d0b7134dd5fac42485fedf7eeacac9d143b89abac0ef`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:08:16 GMT
ADD file:6a525220124da7146a3c356cc57678f3b8d7c6e9299febaaebd5b5a005f1325c in / 
# Wed, 12 Apr 2023 00:08:21 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 10:49:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 10:50:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 10:52:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 10:59:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b6bdb9410f81554043d19e5ae83249eaa10ffe038db54932946c7d9eaccc8b96`  
		Last Modified: Wed, 12 Apr 2023 00:15:35 GMT  
		Size: 49.3 MB (49299322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71852747f2b9b21534b53c60a706551ff2aae26334aec4b70c4920fe9fb4f8c`  
		Last Modified: Wed, 12 Apr 2023 11:17:26 GMT  
		Size: 8.4 MB (8442270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb9aa6963a60e7aad5662c525f6bbd5202ae82472a684135f6111f1f7d3318e`  
		Last Modified: Wed, 12 Apr 2023 11:17:26 GMT  
		Size: 11.2 MB (11177314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324e348066ac545280d6c0f59d4c327df571da3bc37b52136ddfcb88f5e93d87`  
		Last Modified: Wed, 12 Apr 2023 11:18:17 GMT  
		Size: 62.9 MB (62939755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0043323f2473139490f98ebdaec70e638f66c8d9c516af7709dfde6cee5dc31`  
		Last Modified: Wed, 12 Apr 2023 11:20:20 GMT  
		Size: 190.6 MB (190560197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0209217507f6f357a8082281a14e968862d9d1681ccf30ff783642fad4ec9f85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.9 MB (359860373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb042a9f5f9e7c0af296066c675f6d6e2628f8c26edb13164760d5bd193064b5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:07:22 GMT
ADD file:b747fc06f7ee1d3e19fc9cf3aa83e6ab4caa056a72d230caf616e67849bfe112 in / 
# Wed, 12 Apr 2023 00:07:25 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:24:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:25:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:26:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:31:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8314f03b76ec928732612641a4f8420e3c4c25719b48503230bf6c03979aeb2e`  
		Last Modified: Wed, 12 Apr 2023 00:11:50 GMT  
		Size: 53.3 MB (53299984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823af2d3550f6b52577dc50d69a272726b10382b4fae65d06e3b7196165e42d5`  
		Last Modified: Wed, 12 Apr 2023 09:43:31 GMT  
		Size: 9.7 MB (9663796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f73dc4aed694f9f90cd285bb10ed1d4652e9e29ca42e3ae9b7e2148cb39b812`  
		Last Modified: Wed, 12 Apr 2023 09:43:31 GMT  
		Size: 12.2 MB (12184513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1002e389de5d993e4a73f7cf4311d2ac394084c1570912d013506d78ea334895`  
		Last Modified: Wed, 12 Apr 2023 09:43:59 GMT  
		Size: 69.6 MB (69558417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7bbfd7ef8d272f24c3ac1b3965ec076e9d3cecb875f224158e1384609161ad7`  
		Last Modified: Wed, 12 Apr 2023 09:45:01 GMT  
		Size: 215.2 MB (215153663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f3ab35ffe09db7e9be153f5725015386c28800e98cb51a46e7c57187d5a0e602
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.8 MB (314808227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7150ecfe845b425b67f772c301e8610bfca04fb6c670705d638bd01b5dd34bb1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:19 GMT
ADD file:5d2b35b45a0f23e2f2e93f9c311eb34a92e4591ea27979236d801e512d44cb85 in / 
# Tue, 11 Apr 2023 23:59:31 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:24:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:24:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 00:25:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:26:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8a09cd2374da8355612e7d4c91d55107a3f089816ae52b2c91b9e08e6a895ab1`  
		Last Modified: Wed, 12 Apr 2023 00:04:39 GMT  
		Size: 47.7 MB (47670407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d047361c12b2aeb253b1923b053dcc960101b3b3348af8f15f95f7fda2b89e4`  
		Last Modified: Wed, 12 Apr 2023 00:32:00 GMT  
		Size: 8.7 MB (8713846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a462d218c24c21390b32ace449f4f47a57624b858dc05a37c31cb7f6e21c41`  
		Last Modified: Wed, 12 Apr 2023 00:32:00 GMT  
		Size: 11.3 MB (11288081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628da1a495c0341f28b24cb228c4984d7d8a718059c95991d67739f4a4602e4b`  
		Last Modified: Wed, 12 Apr 2023 00:32:14 GMT  
		Size: 63.1 MB (63101451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e16abe3590f67fe9ba9faa6530081d422098a3dabb4fd1cb81b378a88316bf`  
		Last Modified: Wed, 12 Apr 2023 00:32:42 GMT  
		Size: 184.0 MB (184034442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:33e2a1a1bc1160b1cec89c4ba8b9b95ab439c6d5c554bd5fd41889a695a77f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bookworm-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:6a036620bf66ab7f03f891595654eae2995b8a08bb32443b8e130fa87c26c2b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69798535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95348693c13cd4b3237dba422f5d46f3c7b727c7c451791d70fb9f93a80800b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:35 GMT
ADD file:1cb6c660a2e3ea14b2a11bb8b80f53920c3da423a0ad7004391bfab4db4d0177 in / 
# Wed, 12 Apr 2023 00:19:36 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:48:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:49:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:cc556c281183180fae02d57fa6fb60ed0a99d9040936278743dc4022bfb0c686`  
		Last Modified: Wed, 12 Apr 2023 00:22:48 GMT  
		Size: 49.3 MB (49292938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8022b43d7c31d74c341d297cf10031ff0c51f596473a0c1945ee83a841094638`  
		Last Modified: Wed, 12 Apr 2023 07:56:29 GMT  
		Size: 9.1 MB (9083160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db75f726ec67539c4823cb16851963ebe5838a853b0e769fd662020fad918781`  
		Last Modified: Wed, 12 Apr 2023 07:56:29 GMT  
		Size: 11.4 MB (11422437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:66ba8371e61af6282fc38b6060f0c069dfedce71185d25e520e1124503a36408
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67699804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc6c4cd7610510c3dbf367553fdb3b3d67108a1c4f5fef96d4fccbb8635f2db`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:48:19 GMT
ADD file:df1103dce44baa95c92287ab5016f36d5cc45c6062116ebf5273f7e79a00915c in / 
# Wed, 12 Apr 2023 00:48:20 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:11:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:11:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:795c0ca2726dffdb0e5ef6ffa341d17ec672d5915011f1a93a05e8c95a4779ae`  
		Last Modified: Wed, 12 Apr 2023 00:50:12 GMT  
		Size: 48.1 MB (48110879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e70c1a23fdf0fd320a61a2506f0ca4a391a319de8403734e4af8d678a6081fc`  
		Last Modified: Wed, 12 Apr 2023 01:20:09 GMT  
		Size: 8.5 MB (8523001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27111cd5fb1057675f2e0b269790dc264d344d6e4b7ad92ff941f90a496167b`  
		Last Modified: Wed, 12 Apr 2023 01:20:09 GMT  
		Size: 11.1 MB (11065924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b289f68e3841fe69e7989c97ee56cf9d1fd5e6c40aeee876b5ed49d24196349f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64742425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb40b9cc3e34bc48896c67a00695947a3ba4c4f9994a7add99e9ef2f171754d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:10 GMT
ADD file:aa1c08333544c05fc5317d775ee99af7479c6fa5f35b74652f6126a7a5099958 in / 
# Tue, 11 Apr 2023 23:59:11 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:32:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:32:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:81b1dd69f2a38ad14b0919ab9c395aafeb137158539ab6531ac5743690a0ebb7`  
		Last Modified: Wed, 12 Apr 2023 00:02:26 GMT  
		Size: 45.9 MB (45883114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f399f5abf6c810daac72b311feda8726e38c0c228183ccf5d0da4de0b8ec79f4`  
		Last Modified: Wed, 12 Apr 2023 09:43:59 GMT  
		Size: 8.2 MB (8169132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3453014a13bae733f0a1d38594c31a25841303277602f61394efaff085c42288`  
		Last Modified: Wed, 12 Apr 2023 09:43:59 GMT  
		Size: 10.7 MB (10690179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:03a892b4f8141b6f3f3c1d36591ec20f5abf8e7db913d6b06bef0195f59ada5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69649974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c5127fd80af5e1e2f2405e7610f8464a9e99f288f6b5e5afce4df2eb1aa624`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:27 GMT
ADD file:efed18ef2a003bff7e64e7049455216e51876402083581032c35085328e416f6 in / 
# Wed, 12 Apr 2023 00:39:28 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:04:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:04:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b0f987ce91d920ae0a705ed6c9824f1bbbfa282defb8986614030eb8e2bc0b4e`  
		Last Modified: Wed, 12 Apr 2023 00:41:45 GMT  
		Size: 49.3 MB (49345365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e6a618ee06e99ebfbb7809c1cc4902cb717d294243f3765f170fd1c8eaf94a`  
		Last Modified: Wed, 12 Apr 2023 01:12:23 GMT  
		Size: 8.9 MB (8915044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59c3f19470d2fd9e1407a7ddcbac3c316a999a143865347f221db18517e0838`  
		Last Modified: Wed, 12 Apr 2023 01:12:24 GMT  
		Size: 11.4 MB (11389565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b43a148c9da49809e8efcfafdef9c412da433e7735208795c69a14047f003874
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71409064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e15fc1cc8869eaa3b3492c5ebdad339d1c464b7630edf0a5e01a6fd94f6f3be`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:38:30 GMT
ADD file:7718865253a3489583d40f8c7a7beede0c20cebbab68bb3e97ad2e84082afcb7 in / 
# Wed, 12 Apr 2023 00:38:30 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:02:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:02:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a4ce9e81f634822e5166ef3eef875a4140795ac18afe0391433d72c7865bf67b`  
		Last Modified: Wed, 12 Apr 2023 00:41:43 GMT  
		Size: 50.3 MB (50317977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e54183fe5cb0866f886a93c0d098d38e649286a2b516b64d9658dd40f5d74b`  
		Last Modified: Wed, 12 Apr 2023 01:13:34 GMT  
		Size: 9.3 MB (9264042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76896a8c48193a86329dc809066c177aedc76d55811eb32ca7c80c1ab06f66f1`  
		Last Modified: Wed, 12 Apr 2023 01:13:34 GMT  
		Size: 11.8 MB (11827045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:3afc2ecbb80ef88ab70eb6ad01b612cc86b9eb46cd591f35f29128b222ca942e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68918906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb594595ebffc0ba011ef2f95469fdfdc4776f79e192ac3a4122772b6b04ca30`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:08:16 GMT
ADD file:6a525220124da7146a3c356cc57678f3b8d7c6e9299febaaebd5b5a005f1325c in / 
# Wed, 12 Apr 2023 00:08:21 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 10:49:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 10:50:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b6bdb9410f81554043d19e5ae83249eaa10ffe038db54932946c7d9eaccc8b96`  
		Last Modified: Wed, 12 Apr 2023 00:15:35 GMT  
		Size: 49.3 MB (49299322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71852747f2b9b21534b53c60a706551ff2aae26334aec4b70c4920fe9fb4f8c`  
		Last Modified: Wed, 12 Apr 2023 11:17:26 GMT  
		Size: 8.4 MB (8442270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb9aa6963a60e7aad5662c525f6bbd5202ae82472a684135f6111f1f7d3318e`  
		Last Modified: Wed, 12 Apr 2023 11:17:26 GMT  
		Size: 11.2 MB (11177314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5e2e84459ecb32db9fabb5e93567cedf5076f979a0d89d1ba558d1b2edebd39e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75148293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:321fa2f7d47d7fb1798f5396badb74ddbb7bb63d6ff179ee9938a659c3966ed4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:07:22 GMT
ADD file:b747fc06f7ee1d3e19fc9cf3aa83e6ab4caa056a72d230caf616e67849bfe112 in / 
# Wed, 12 Apr 2023 00:07:25 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:24:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:25:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8314f03b76ec928732612641a4f8420e3c4c25719b48503230bf6c03979aeb2e`  
		Last Modified: Wed, 12 Apr 2023 00:11:50 GMT  
		Size: 53.3 MB (53299984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823af2d3550f6b52577dc50d69a272726b10382b4fae65d06e3b7196165e42d5`  
		Last Modified: Wed, 12 Apr 2023 09:43:31 GMT  
		Size: 9.7 MB (9663796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f73dc4aed694f9f90cd285bb10ed1d4652e9e29ca42e3ae9b7e2148cb39b812`  
		Last Modified: Wed, 12 Apr 2023 09:43:31 GMT  
		Size: 12.2 MB (12184513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:377be7d5891b37466c736b399c0beb5ac9fdccf106bbee4e802cd0c0200a985e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67672334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75da5ea476406e76c74e365fa869cd83bc1a1cbbd23ef34d20b56b9cf7624b2c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:19 GMT
ADD file:5d2b35b45a0f23e2f2e93f9c311eb34a92e4591ea27979236d801e512d44cb85 in / 
# Tue, 11 Apr 2023 23:59:31 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:24:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:24:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8a09cd2374da8355612e7d4c91d55107a3f089816ae52b2c91b9e08e6a895ab1`  
		Last Modified: Wed, 12 Apr 2023 00:04:39 GMT  
		Size: 47.7 MB (47670407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d047361c12b2aeb253b1923b053dcc960101b3b3348af8f15f95f7fda2b89e4`  
		Last Modified: Wed, 12 Apr 2023 00:32:00 GMT  
		Size: 8.7 MB (8713846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a462d218c24c21390b32ace449f4f47a57624b858dc05a37c31cb7f6e21c41`  
		Last Modified: Wed, 12 Apr 2023 00:32:00 GMT  
		Size: 11.3 MB (11288081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:b3ac5bae610464bfbd16f2433b21b14f01c8cc1061332166a29f88ec39ba07fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bookworm-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9ed3be818675099491b2a9c5066bbd63d5283caa5f3b77d978ea95ecb43f2d61
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133896234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba56358263d5c537ab77ee622af1e53f4ab231c655f7637aa7739d9b469a80da`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:35 GMT
ADD file:1cb6c660a2e3ea14b2a11bb8b80f53920c3da423a0ad7004391bfab4db4d0177 in / 
# Wed, 12 Apr 2023 00:19:36 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:48:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:49:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 07:49:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cc556c281183180fae02d57fa6fb60ed0a99d9040936278743dc4022bfb0c686`  
		Last Modified: Wed, 12 Apr 2023 00:22:48 GMT  
		Size: 49.3 MB (49292938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8022b43d7c31d74c341d297cf10031ff0c51f596473a0c1945ee83a841094638`  
		Last Modified: Wed, 12 Apr 2023 07:56:29 GMT  
		Size: 9.1 MB (9083160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db75f726ec67539c4823cb16851963ebe5838a853b0e769fd662020fad918781`  
		Last Modified: Wed, 12 Apr 2023 07:56:29 GMT  
		Size: 11.4 MB (11422437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8a9e299258b84de99d6d739eb84b5b1632005f9c7723f2dd9e209fb1a8aaa3`  
		Last Modified: Wed, 12 Apr 2023 07:56:46 GMT  
		Size: 64.1 MB (64097699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:344b53de882fcda7c2d453195595144a3c69b6e842ee71d13d6da33ab28ecc50
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129241091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5754c39ab542288953f32e05c79772f7f299ee5ef462be8bd98f34a5d5ae07f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:48:19 GMT
ADD file:df1103dce44baa95c92287ab5016f36d5cc45c6062116ebf5273f7e79a00915c in / 
# Wed, 12 Apr 2023 00:48:20 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:11:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:11:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:12:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:795c0ca2726dffdb0e5ef6ffa341d17ec672d5915011f1a93a05e8c95a4779ae`  
		Last Modified: Wed, 12 Apr 2023 00:50:12 GMT  
		Size: 48.1 MB (48110879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e70c1a23fdf0fd320a61a2506f0ca4a391a319de8403734e4af8d678a6081fc`  
		Last Modified: Wed, 12 Apr 2023 01:20:09 GMT  
		Size: 8.5 MB (8523001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27111cd5fb1057675f2e0b269790dc264d344d6e4b7ad92ff941f90a496167b`  
		Last Modified: Wed, 12 Apr 2023 01:20:09 GMT  
		Size: 11.1 MB (11065924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ed8d7f4b0f78246beda91a51ddbc4ab368fe6f04bb2432498c3f5a76cbc010`  
		Last Modified: Wed, 12 Apr 2023 01:20:30 GMT  
		Size: 61.5 MB (61541287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b598cfea4a2fdd4babbe11e7f9770817e72eb9f2af57e7f8c34b858af1d56d2e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (123989849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411c875b6d761c0534bb297279832abe2d22d60dd23cd2e13d5d061f524a4799`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:10 GMT
ADD file:aa1c08333544c05fc5317d775ee99af7479c6fa5f35b74652f6126a7a5099958 in / 
# Tue, 11 Apr 2023 23:59:11 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:32:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:32:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:32:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:81b1dd69f2a38ad14b0919ab9c395aafeb137158539ab6531ac5743690a0ebb7`  
		Last Modified: Wed, 12 Apr 2023 00:02:26 GMT  
		Size: 45.9 MB (45883114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f399f5abf6c810daac72b311feda8726e38c0c228183ccf5d0da4de0b8ec79f4`  
		Last Modified: Wed, 12 Apr 2023 09:43:59 GMT  
		Size: 8.2 MB (8169132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3453014a13bae733f0a1d38594c31a25841303277602f61394efaff085c42288`  
		Last Modified: Wed, 12 Apr 2023 09:43:59 GMT  
		Size: 10.7 MB (10690179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1d5c89a8ad9820582b69420d902dbb04e78a440ab16e42dd52a5778aea37e4`  
		Last Modified: Wed, 12 Apr 2023 09:44:19 GMT  
		Size: 59.2 MB (59247424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:14fe92b486d2fa872ed5792948ef263bf382710d96156521bba91db6409d8adf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133624598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f0946fdc4f05c98259e0c4a796a7215b79fdfac56393722a52de699ef3ad2c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:27 GMT
ADD file:efed18ef2a003bff7e64e7049455216e51876402083581032c35085328e416f6 in / 
# Wed, 12 Apr 2023 00:39:28 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:04:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:04:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:04:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0f987ce91d920ae0a705ed6c9824f1bbbfa282defb8986614030eb8e2bc0b4e`  
		Last Modified: Wed, 12 Apr 2023 00:41:45 GMT  
		Size: 49.3 MB (49345365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e6a618ee06e99ebfbb7809c1cc4902cb717d294243f3765f170fd1c8eaf94a`  
		Last Modified: Wed, 12 Apr 2023 01:12:23 GMT  
		Size: 8.9 MB (8915044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59c3f19470d2fd9e1407a7ddcbac3c316a999a143865347f221db18517e0838`  
		Last Modified: Wed, 12 Apr 2023 01:12:24 GMT  
		Size: 11.4 MB (11389565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b373ae05bf678c385bace283c65197a2bbc2a334c528ed7b58a01d93131de585`  
		Last Modified: Wed, 12 Apr 2023 01:12:39 GMT  
		Size: 64.0 MB (63974624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:1b7217dd58c62e94d4df1bd3fe5e75114d9fdb3da6a3d8338c1e2534008bffce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.4 MB (137369491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed8865cd6ac62a089861253f45fe5c6131b992aa6d88dd85645089c3f5ada23`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:38:30 GMT
ADD file:7718865253a3489583d40f8c7a7beede0c20cebbab68bb3e97ad2e84082afcb7 in / 
# Wed, 12 Apr 2023 00:38:30 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:02:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:02:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:03:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a4ce9e81f634822e5166ef3eef875a4140795ac18afe0391433d72c7865bf67b`  
		Last Modified: Wed, 12 Apr 2023 00:41:43 GMT  
		Size: 50.3 MB (50317977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e54183fe5cb0866f886a93c0d098d38e649286a2b516b64d9658dd40f5d74b`  
		Last Modified: Wed, 12 Apr 2023 01:13:34 GMT  
		Size: 9.3 MB (9264042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76896a8c48193a86329dc809066c177aedc76d55811eb32ca7c80c1ab06f66f1`  
		Last Modified: Wed, 12 Apr 2023 01:13:34 GMT  
		Size: 11.8 MB (11827045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba7e1ed0df9a2a8a6501d91360cea22ab988653bf057d73c44ecb41e49f6151`  
		Last Modified: Wed, 12 Apr 2023 01:13:56 GMT  
		Size: 66.0 MB (65960427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:77882a60b3dac839278148546ac1b5ae49c0b862dc34eb47c9b961189f54aa62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131858661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b1707593870d644bad6ee88adb0d34d3d057b27f135eb3c00dae5700d6ce01`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:08:16 GMT
ADD file:6a525220124da7146a3c356cc57678f3b8d7c6e9299febaaebd5b5a005f1325c in / 
# Wed, 12 Apr 2023 00:08:21 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 10:49:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 10:50:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 10:52:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b6bdb9410f81554043d19e5ae83249eaa10ffe038db54932946c7d9eaccc8b96`  
		Last Modified: Wed, 12 Apr 2023 00:15:35 GMT  
		Size: 49.3 MB (49299322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71852747f2b9b21534b53c60a706551ff2aae26334aec4b70c4920fe9fb4f8c`  
		Last Modified: Wed, 12 Apr 2023 11:17:26 GMT  
		Size: 8.4 MB (8442270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb9aa6963a60e7aad5662c525f6bbd5202ae82472a684135f6111f1f7d3318e`  
		Last Modified: Wed, 12 Apr 2023 11:17:26 GMT  
		Size: 11.2 MB (11177314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324e348066ac545280d6c0f59d4c327df571da3bc37b52136ddfcb88f5e93d87`  
		Last Modified: Wed, 12 Apr 2023 11:18:17 GMT  
		Size: 62.9 MB (62939755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ff9ad1cd6f756acfad0e6713004c604f421a818881a59a65cdf72c3ac1f32b42
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144706710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d4f37092672a6f4eee455d949bb5dc19844135bb11f8290db298507672facf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:07:22 GMT
ADD file:b747fc06f7ee1d3e19fc9cf3aa83e6ab4caa056a72d230caf616e67849bfe112 in / 
# Wed, 12 Apr 2023 00:07:25 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:24:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:25:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:26:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8314f03b76ec928732612641a4f8420e3c4c25719b48503230bf6c03979aeb2e`  
		Last Modified: Wed, 12 Apr 2023 00:11:50 GMT  
		Size: 53.3 MB (53299984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823af2d3550f6b52577dc50d69a272726b10382b4fae65d06e3b7196165e42d5`  
		Last Modified: Wed, 12 Apr 2023 09:43:31 GMT  
		Size: 9.7 MB (9663796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f73dc4aed694f9f90cd285bb10ed1d4652e9e29ca42e3ae9b7e2148cb39b812`  
		Last Modified: Wed, 12 Apr 2023 09:43:31 GMT  
		Size: 12.2 MB (12184513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1002e389de5d993e4a73f7cf4311d2ac394084c1570912d013506d78ea334895`  
		Last Modified: Wed, 12 Apr 2023 09:43:59 GMT  
		Size: 69.6 MB (69558417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f1a6a91892b66c97ca28c0d4aa10b5706ce5d49d91fcfb33f33d04a191068ce7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 MB (130773785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1798d2a8c091800a97b7795b2e2f35680f165f0a95d7f44b12965f19623788f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:19 GMT
ADD file:5d2b35b45a0f23e2f2e93f9c311eb34a92e4591ea27979236d801e512d44cb85 in / 
# Tue, 11 Apr 2023 23:59:31 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:24:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:24:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 00:25:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8a09cd2374da8355612e7d4c91d55107a3f089816ae52b2c91b9e08e6a895ab1`  
		Last Modified: Wed, 12 Apr 2023 00:04:39 GMT  
		Size: 47.7 MB (47670407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d047361c12b2aeb253b1923b053dcc960101b3b3348af8f15f95f7fda2b89e4`  
		Last Modified: Wed, 12 Apr 2023 00:32:00 GMT  
		Size: 8.7 MB (8713846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a462d218c24c21390b32ace449f4f47a57624b858dc05a37c31cb7f6e21c41`  
		Last Modified: Wed, 12 Apr 2023 00:32:00 GMT  
		Size: 11.3 MB (11288081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628da1a495c0341f28b24cb228c4984d7d8a718059c95991d67739f4a4602e4b`  
		Last Modified: Wed, 12 Apr 2023 00:32:14 GMT  
		Size: 63.1 MB (63101451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bullseye`

```console
$ docker pull buildpack-deps@sha256:695fd9e1f58574422eece085006690b3110abb0d304260024d40775b95c6056e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bullseye` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4156d4c78d3e29a9aa11a5528a08847352e66895bb0a75cec05f4d43752fb8f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.5 MB (322492485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09bd8b383fcae8260115c949f68a3ccbe1df72567c4e1ad6f53b72329c1c5e1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:55 GMT
ADD file:f2d012660f882f319a5878a3f9ce285f488b8f90fad49ad238541cf72089e035 in / 
# Wed, 12 Apr 2023 00:19:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:50:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:51:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 07:51:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:52:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0248cf3e63c73d0e496a67807d056ca41d5e968b61087e8eca2cf4b9b4d7b99`  
		Last Modified: Wed, 12 Apr 2023 00:23:20 GMT  
		Size: 55.1 MB (55052736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127e97b4daf784e08840a21765f0d4f251192ef2994d0e4a253490f81e63955b`  
		Last Modified: Wed, 12 Apr 2023 07:57:29 GMT  
		Size: 5.2 MB (5166696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0336c50c9f6942b660e433b1086238eec37057c34b14c4e3b28bd7bf05bd84ba`  
		Last Modified: Wed, 12 Apr 2023 07:57:29 GMT  
		Size: 10.9 MB (10876749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b89f3c7f7da8adf032a33a75d1b659cee33179ecb88ea0ba75e4fc58ebe63a6`  
		Last Modified: Wed, 12 Apr 2023 07:57:46 GMT  
		Size: 54.6 MB (54584801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d62772179761f8fddfaed03ed2bdf7078b103b193d18d79a9b49364830d56cf`  
		Last Modified: Wed, 12 Apr 2023 07:58:19 GMT  
		Size: 196.8 MB (196811503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:5307e4d5147eb64f430d2a521eee4a5504ed8c4a0d7d98aa81c28190c2c963d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.6 MB (295551904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62bc4c385631ea22e58568f3c02e7102b4f9f8f5a1ebb96d7e82bf8764dbecae`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:48:34 GMT
ADD file:ae13a4cbeb20b92ec29dd7409de47a964fe373bdde2a4e8880b5a4d9dc64171e in / 
# Wed, 12 Apr 2023 00:48:35 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:15:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:15:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:16:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:17:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:86cb8d774eca43d428d6a35506c172ba62358d2d5ec90c886e3b38b297f93b20`  
		Last Modified: Wed, 12 Apr 2023 00:50:46 GMT  
		Size: 52.6 MB (52555175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49db155cdf8645f599affcbbbc75eb928b0a9d010c4ac54afcfa9d7e4fa85e0`  
		Last Modified: Wed, 12 Apr 2023 01:21:15 GMT  
		Size: 5.1 MB (5072827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8936087cbd048148575fda58348506149db80a2699e99ae2042086628c0e5a38`  
		Last Modified: Wed, 12 Apr 2023 01:21:16 GMT  
		Size: 10.6 MB (10573853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0bf11569c39ee4f3d8515112046a55f14f39e54c6f0ea26271033c090f77d2`  
		Last Modified: Wed, 12 Apr 2023 01:21:35 GMT  
		Size: 52.3 MB (52340617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:622390f39404d88752f248bc2136a55baca97d5324d43689204df0157d284282`  
		Last Modified: Wed, 12 Apr 2023 01:22:13 GMT  
		Size: 175.0 MB (175009432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:14544dda30d13c761bb7bfb4d7fdffb2d3abd01a303373a2bcb846940b12680d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (283013417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f5b3339637b4c0d3912ef6cd818266179b085a40521f419e38c9546b616ee3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:35 GMT
ADD file:75c57df33c95251a80549b7949853df282a42bc4e5f19176764907a54b74caa9 in / 
# Tue, 11 Apr 2023 23:59:36 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:35:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:35:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:37:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4feff9b88735325634445419eaaec2ed47500b63027cfd2de34b8bc6d55ee85c`  
		Last Modified: Wed, 12 Apr 2023 00:02:57 GMT  
		Size: 50.2 MB (50216882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5f77534be142d18fb6441aad5ebb0a6b1fbd1128fee964f14c772d3f48978f`  
		Last Modified: Wed, 12 Apr 2023 09:45:07 GMT  
		Size: 4.9 MB (4934569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0797973d3ff4c7bfddd6439ceacd815ea867f868a8c75686d5b80ee1a3eca322`  
		Last Modified: Wed, 12 Apr 2023 09:45:08 GMT  
		Size: 10.2 MB (10217876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cff4fab8e209a4a8ef903baadd1f4839687988e57cef0235a447c0198ddfab`  
		Last Modified: Wed, 12 Apr 2023 09:45:28 GMT  
		Size: 50.4 MB (50355731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c442c38966496f089bcee5c78d8e7321764a2a679fd64f1070215e5f24b6d872`  
		Last Modified: Wed, 12 Apr 2023 09:46:04 GMT  
		Size: 167.3 MB (167288359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e7277cb741804ffe9213d32a419f6738ef4494fbd33db9326b55282dfbc1dd6b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314135667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c57708eddbf78525fe399f52d71e35653f6c3298641025d07fcc3323777584`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:42 GMT
ADD file:dd3d4e5fe819950e7d01b44a29dbd790438cd722ba76198910e2597448ab0c6f in / 
# Wed, 12 Apr 2023 00:39:43 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:06:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:06:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:07:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:08:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dc80b8cdbfd36cb20231d807a50d704945d1df4da8f6e23197ccfcb629970491`  
		Last Modified: Wed, 12 Apr 2023 00:42:14 GMT  
		Size: 53.7 MB (53705529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5884e7f2c8c61aa845de4902fc29639b58861ae6c2d80bafe82082c0456c0740`  
		Last Modified: Wed, 12 Apr 2023 01:13:17 GMT  
		Size: 5.2 MB (5152752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b792b01ed3c8dc1488cd8aac41ab7d49bb17f3fa22b2e6c846078cec81a1c00`  
		Last Modified: Wed, 12 Apr 2023 01:13:17 GMT  
		Size: 10.9 MB (10873655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f993d5b17f32f4b8a535c25e182e5d8412625beee450e513ca57036e8fdd6dc`  
		Last Modified: Wed, 12 Apr 2023 01:13:34 GMT  
		Size: 54.7 MB (54676038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26edf98ece5babdb6b65e76738cef2c2d05e7075161753d3ba95cd84480d211`  
		Last Modified: Wed, 12 Apr 2023 01:14:02 GMT  
		Size: 189.7 MB (189727693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ff274b300c58e39b8abdacecdee25d47651abe32a696616b92656ca392bd5d21
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.2 MB (328223380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5eee57e4ddbeaa9219392349db2bc711541f424d58a97b4a86ad5bd768ff773`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:38:51 GMT
ADD file:4da7e6af0782b21849e5f6385de3589ac5b8d81d173721f9990d32da754df2cb in / 
# Wed, 12 Apr 2023 00:38:51 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:05:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:05:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:06:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:07:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b2bef40925391866903279768b0ae1e8233ef6a1aae64509a922f4aa96fe42a6`  
		Last Modified: Wed, 12 Apr 2023 00:42:19 GMT  
		Size: 56.0 MB (56032818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37ccf9a5e34ba2345ce265a9a11c93ee254e1f3616dfd1c1deda6e2f7d614c8`  
		Last Modified: Wed, 12 Apr 2023 01:14:53 GMT  
		Size: 5.3 MB (5293626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4988d5e4328f031f6884a7351766aa8a2806c9cdca38d354477fc537eaa4911f`  
		Last Modified: Wed, 12 Apr 2023 01:14:54 GMT  
		Size: 11.2 MB (11249875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660a2befd486d43a308dd1561f57efeafe1f13defd6439d34aeb5efec783ee3d`  
		Last Modified: Wed, 12 Apr 2023 01:15:17 GMT  
		Size: 55.9 MB (55922746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f09985282f12d05c5724bcbb0481a94f66820112bafc34a1d990dfdf74a52fc`  
		Last Modified: Wed, 12 Apr 2023 01:16:02 GMT  
		Size: 199.7 MB (199724315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:733073a5e45e28ac1efdd031f70eb14ea95adc6350a95cd5eec6e4289ad5726c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301296282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb9d52fa12ccd33943e746e02c6d998737105a5b221ed73b5860e5137600578`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:09:26 GMT
ADD file:5d2c839055739fe92d64098c09607e7ec9123101d15f837c54f3688755af0c23 in / 
# Wed, 12 Apr 2023 00:09:31 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 11:00:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 11:00:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 11:02:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 11:08:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80243e355b05bee53c6acc45ace2cde4f7495dafe9f3f8d7d299ed51d04928d2`  
		Last Modified: Wed, 12 Apr 2023 00:16:48 GMT  
		Size: 53.3 MB (53272023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed6aed7903d464c3c421335c8a4b93f11e64b669c7eab532e87e5945fd185e2`  
		Last Modified: Wed, 12 Apr 2023 11:20:32 GMT  
		Size: 5.1 MB (5127336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af3f0065ba2217f3ef903c35f7e644bd2222c1630a96ac62477510cedfa848`  
		Last Modified: Wed, 12 Apr 2023 11:20:34 GMT  
		Size: 10.7 MB (10662154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81fa7bf218e18cc100c89241735ff424465ba8caca78835fdadafcd212de62f`  
		Last Modified: Wed, 12 Apr 2023 11:21:19 GMT  
		Size: 53.3 MB (53306535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f17002a316d921b7e863e4fa717c4354ebce8cf57671d9a2bf8f34dec378d8c`  
		Last Modified: Wed, 12 Apr 2023 11:23:14 GMT  
		Size: 178.9 MB (178928234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5b39e218d6f9e9f7c2241165c5f3ff812622a74d175997245e60615626e2508a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.0 MB (330997339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b69805860c4cc4b90cbcdadb6ab37298c1d198c92781fef2c1ca29f434eae34b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:07:58 GMT
ADD file:c3c2a10473ddaa3d8a30ca99b19ad3599d0e60d826c4e0315bdb7463352ebc09 in / 
# Wed, 12 Apr 2023 00:08:02 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:31:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:32:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:33:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:36:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2d3ffdd4610a019889b845cc82b3d956ad85cca78ad4bff2d5e5522bd02c17e7`  
		Last Modified: Wed, 12 Apr 2023 00:12:37 GMT  
		Size: 58.9 MB (58926600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00772c18aacd8e2ae167f5f94b2e86c7b77fd3f7790dc5e6754e48fcce1ff484`  
		Last Modified: Wed, 12 Apr 2023 09:45:12 GMT  
		Size: 5.4 MB (5415380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1877fd565f7c580ab3b8fd343d19de69c9c3334787d6a3c93c9c21fe08ea32a`  
		Last Modified: Wed, 12 Apr 2023 09:45:13 GMT  
		Size: 11.6 MB (11629984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a24a9774fce2d157b32633fbd68d6d4777632ca49b0a35d2e9be9a2455d88b`  
		Last Modified: Wed, 12 Apr 2023 09:45:40 GMT  
		Size: 58.9 MB (58865366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d134f385b05ace42f019d92548a9dd6708f9ae2ee3269131645b4ff67b2463`  
		Last Modified: Wed, 12 Apr 2023 09:46:38 GMT  
		Size: 196.2 MB (196160009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:478709c66fdeffea827bb22297605067d97172933185294b18da02b3b071e7a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296079415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62811c5341c95a39adc789318a1ba301b0fae01b6b77e3b4a63a1693c43fa76d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:00:25 GMT
ADD file:ab4e28724d04724a57e0f5bbe299d3361103f05ad1978dc3bfef243c1f9d6476 in / 
# Wed, 12 Apr 2023 00:00:38 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:26:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:26:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 00:27:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:28:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:042263756d7dc47bf98a243871107aa3a2b41acda91d104d8b4e148749a43dda`  
		Last Modified: Wed, 12 Apr 2023 00:05:03 GMT  
		Size: 53.3 MB (53286682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2973b8c98f9da7833ab9cd69185dd958a8939a30136cdcfedb66ce775db358ee`  
		Last Modified: Wed, 12 Apr 2023 00:32:48 GMT  
		Size: 5.1 MB (5149313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f740d13ac612bf8b6489559a7945ec1439fee2d5eba455ab0db047cd3f30a9a`  
		Last Modified: Wed, 12 Apr 2023 00:32:49 GMT  
		Size: 10.8 MB (10766104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c0067783f401b099adca196dce9e464e66236e49faba106e2f04ac73a90df7`  
		Last Modified: Wed, 12 Apr 2023 00:33:02 GMT  
		Size: 54.1 MB (54061843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1b5accdd9fd68a290692e1a0a3d853312f236ae0463540b5fdd97d598cc7a6`  
		Last Modified: Wed, 12 Apr 2023 00:33:28 GMT  
		Size: 172.8 MB (172815473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:b77ca637508f0f6f5d834c57f2e6af153c2ce4a48afb439b5fb469529360a951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bullseye-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:acd62d4d9773006a9d0acddc08a4cbf7637d1c975e67459b52a7dc093bdfc271
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71096181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af19f7b630d3d79df60c6a9ae3051940c35c240094ef6e54f4f7843577467896`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:55 GMT
ADD file:f2d012660f882f319a5878a3f9ce285f488b8f90fad49ad238541cf72089e035 in / 
# Wed, 12 Apr 2023 00:19:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:50:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:51:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b0248cf3e63c73d0e496a67807d056ca41d5e968b61087e8eca2cf4b9b4d7b99`  
		Last Modified: Wed, 12 Apr 2023 00:23:20 GMT  
		Size: 55.1 MB (55052736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127e97b4daf784e08840a21765f0d4f251192ef2994d0e4a253490f81e63955b`  
		Last Modified: Wed, 12 Apr 2023 07:57:29 GMT  
		Size: 5.2 MB (5166696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0336c50c9f6942b660e433b1086238eec37057c34b14c4e3b28bd7bf05bd84ba`  
		Last Modified: Wed, 12 Apr 2023 07:57:29 GMT  
		Size: 10.9 MB (10876749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:03091d90e79cf371dee743c2a8537556060a22246a5c1a68d53f63e201715f4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68201855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39fd3f1fac0693a3efcdf720af9216deb72c54ed024f9c8edfa061944f26d405`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:48:34 GMT
ADD file:ae13a4cbeb20b92ec29dd7409de47a964fe373bdde2a4e8880b5a4d9dc64171e in / 
# Wed, 12 Apr 2023 00:48:35 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:15:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:15:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:86cb8d774eca43d428d6a35506c172ba62358d2d5ec90c886e3b38b297f93b20`  
		Last Modified: Wed, 12 Apr 2023 00:50:46 GMT  
		Size: 52.6 MB (52555175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49db155cdf8645f599affcbbbc75eb928b0a9d010c4ac54afcfa9d7e4fa85e0`  
		Last Modified: Wed, 12 Apr 2023 01:21:15 GMT  
		Size: 5.1 MB (5072827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8936087cbd048148575fda58348506149db80a2699e99ae2042086628c0e5a38`  
		Last Modified: Wed, 12 Apr 2023 01:21:16 GMT  
		Size: 10.6 MB (10573853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a8434b10032012c2760d715f731aa184a425b42164650c42161de37dd78702cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65369327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475e074940bc42bc670d7bf9b9fb35f58ef5e44c093fb372fa6b177c75f785cc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:35 GMT
ADD file:75c57df33c95251a80549b7949853df282a42bc4e5f19176764907a54b74caa9 in / 
# Tue, 11 Apr 2023 23:59:36 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:35:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:4feff9b88735325634445419eaaec2ed47500b63027cfd2de34b8bc6d55ee85c`  
		Last Modified: Wed, 12 Apr 2023 00:02:57 GMT  
		Size: 50.2 MB (50216882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5f77534be142d18fb6441aad5ebb0a6b1fbd1128fee964f14c772d3f48978f`  
		Last Modified: Wed, 12 Apr 2023 09:45:07 GMT  
		Size: 4.9 MB (4934569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0797973d3ff4c7bfddd6439ceacd815ea867f868a8c75686d5b80ee1a3eca322`  
		Last Modified: Wed, 12 Apr 2023 09:45:08 GMT  
		Size: 10.2 MB (10217876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a5537c32568d575a5a3bb0f96138a7cf42dc7d590729308b1ed7538fbdd433e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69731936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0130b5aae27ce4286f62ae8a2e5324e811b8d862aa0aea6923a7b461615ccf17`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:42 GMT
ADD file:dd3d4e5fe819950e7d01b44a29dbd790438cd722ba76198910e2597448ab0c6f in / 
# Wed, 12 Apr 2023 00:39:43 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:06:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:06:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:dc80b8cdbfd36cb20231d807a50d704945d1df4da8f6e23197ccfcb629970491`  
		Last Modified: Wed, 12 Apr 2023 00:42:14 GMT  
		Size: 53.7 MB (53705529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5884e7f2c8c61aa845de4902fc29639b58861ae6c2d80bafe82082c0456c0740`  
		Last Modified: Wed, 12 Apr 2023 01:13:17 GMT  
		Size: 5.2 MB (5152752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b792b01ed3c8dc1488cd8aac41ab7d49bb17f3fa22b2e6c846078cec81a1c00`  
		Last Modified: Wed, 12 Apr 2023 01:13:17 GMT  
		Size: 10.9 MB (10873655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:39321899797ed2861f1e87a3547e2e911faa2ce033098728aa240b793dd8232b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72576319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1535cd25f9ea155765a6cae9f83a5e50a533888ddb926700a119b7e91a0a0f1b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:38:51 GMT
ADD file:4da7e6af0782b21849e5f6385de3589ac5b8d81d173721f9990d32da754df2cb in / 
# Wed, 12 Apr 2023 00:38:51 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:05:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:05:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b2bef40925391866903279768b0ae1e8233ef6a1aae64509a922f4aa96fe42a6`  
		Last Modified: Wed, 12 Apr 2023 00:42:19 GMT  
		Size: 56.0 MB (56032818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37ccf9a5e34ba2345ce265a9a11c93ee254e1f3616dfd1c1deda6e2f7d614c8`  
		Last Modified: Wed, 12 Apr 2023 01:14:53 GMT  
		Size: 5.3 MB (5293626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4988d5e4328f031f6884a7351766aa8a2806c9cdca38d354477fc537eaa4911f`  
		Last Modified: Wed, 12 Apr 2023 01:14:54 GMT  
		Size: 11.2 MB (11249875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:66e9ab47759b918c5d7fec7837bf41e0032b99600e25a33827f94b51355e46e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69061513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6925f09cbf336d4383b178072c72886c41699bb1743ff950dfc483a88c39a928`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:09:26 GMT
ADD file:5d2c839055739fe92d64098c09607e7ec9123101d15f837c54f3688755af0c23 in / 
# Wed, 12 Apr 2023 00:09:31 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 11:00:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 11:00:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:80243e355b05bee53c6acc45ace2cde4f7495dafe9f3f8d7d299ed51d04928d2`  
		Last Modified: Wed, 12 Apr 2023 00:16:48 GMT  
		Size: 53.3 MB (53272023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed6aed7903d464c3c421335c8a4b93f11e64b669c7eab532e87e5945fd185e2`  
		Last Modified: Wed, 12 Apr 2023 11:20:32 GMT  
		Size: 5.1 MB (5127336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af3f0065ba2217f3ef903c35f7e644bd2222c1630a96ac62477510cedfa848`  
		Last Modified: Wed, 12 Apr 2023 11:20:34 GMT  
		Size: 10.7 MB (10662154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d2bf2a378307a21bf35bbc234fd0768bf348c2aa8d28c3ee065b4248dcbfa2d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (75971964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17ee001184461420ef6a9dcaa8006e2702365c6fb83c1ea64e12ef337924ac12`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:07:58 GMT
ADD file:c3c2a10473ddaa3d8a30ca99b19ad3599d0e60d826c4e0315bdb7463352ebc09 in / 
# Wed, 12 Apr 2023 00:08:02 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:31:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:32:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2d3ffdd4610a019889b845cc82b3d956ad85cca78ad4bff2d5e5522bd02c17e7`  
		Last Modified: Wed, 12 Apr 2023 00:12:37 GMT  
		Size: 58.9 MB (58926600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00772c18aacd8e2ae167f5f94b2e86c7b77fd3f7790dc5e6754e48fcce1ff484`  
		Last Modified: Wed, 12 Apr 2023 09:45:12 GMT  
		Size: 5.4 MB (5415380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1877fd565f7c580ab3b8fd343d19de69c9c3334787d6a3c93c9c21fe08ea32a`  
		Last Modified: Wed, 12 Apr 2023 09:45:13 GMT  
		Size: 11.6 MB (11629984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5726b9b13d1328b42898380f57612273babbfe94f7918919e3553ca203957c96
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69202099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d3f520b42352a1bbcb04c9c67c162e7870ac7063005e1cbfb804dea99188dc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:00:25 GMT
ADD file:ab4e28724d04724a57e0f5bbe299d3361103f05ad1978dc3bfef243c1f9d6476 in / 
# Wed, 12 Apr 2023 00:00:38 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:26:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:26:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:042263756d7dc47bf98a243871107aa3a2b41acda91d104d8b4e148749a43dda`  
		Last Modified: Wed, 12 Apr 2023 00:05:03 GMT  
		Size: 53.3 MB (53286682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2973b8c98f9da7833ab9cd69185dd958a8939a30136cdcfedb66ce775db358ee`  
		Last Modified: Wed, 12 Apr 2023 00:32:48 GMT  
		Size: 5.1 MB (5149313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f740d13ac612bf8b6489559a7945ec1439fee2d5eba455ab0db047cd3f30a9a`  
		Last Modified: Wed, 12 Apr 2023 00:32:49 GMT  
		Size: 10.8 MB (10766104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:2a03804b71d9d4c346239c8af9c9c11774ec58200bbb20c33039aeefaa07f868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bullseye-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:22e8a94a63b1cf94bc6e69418b975d41cb9ca48640b8b3a48002eb9c65039abb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125680982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8cd24e709af1ad98665077ad3ae2b89451839cb3a36350db232d6ce523d0d60`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:55 GMT
ADD file:f2d012660f882f319a5878a3f9ce285f488b8f90fad49ad238541cf72089e035 in / 
# Wed, 12 Apr 2023 00:19:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:50:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:51:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 07:51:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0248cf3e63c73d0e496a67807d056ca41d5e968b61087e8eca2cf4b9b4d7b99`  
		Last Modified: Wed, 12 Apr 2023 00:23:20 GMT  
		Size: 55.1 MB (55052736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127e97b4daf784e08840a21765f0d4f251192ef2994d0e4a253490f81e63955b`  
		Last Modified: Wed, 12 Apr 2023 07:57:29 GMT  
		Size: 5.2 MB (5166696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0336c50c9f6942b660e433b1086238eec37057c34b14c4e3b28bd7bf05bd84ba`  
		Last Modified: Wed, 12 Apr 2023 07:57:29 GMT  
		Size: 10.9 MB (10876749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b89f3c7f7da8adf032a33a75d1b659cee33179ecb88ea0ba75e4fc58ebe63a6`  
		Last Modified: Wed, 12 Apr 2023 07:57:46 GMT  
		Size: 54.6 MB (54584801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ea05ef84678632f8c536876f2c7f5fc619fc524fc4b7dea24106ccb4b55809a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.5 MB (120542472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640f06156014acf4823a54fa99d9d265ad6efe6eda17f48174918044c3a2ea19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:48:34 GMT
ADD file:ae13a4cbeb20b92ec29dd7409de47a964fe373bdde2a4e8880b5a4d9dc64171e in / 
# Wed, 12 Apr 2023 00:48:35 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:15:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:15:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:16:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:86cb8d774eca43d428d6a35506c172ba62358d2d5ec90c886e3b38b297f93b20`  
		Last Modified: Wed, 12 Apr 2023 00:50:46 GMT  
		Size: 52.6 MB (52555175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49db155cdf8645f599affcbbbc75eb928b0a9d010c4ac54afcfa9d7e4fa85e0`  
		Last Modified: Wed, 12 Apr 2023 01:21:15 GMT  
		Size: 5.1 MB (5072827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8936087cbd048148575fda58348506149db80a2699e99ae2042086628c0e5a38`  
		Last Modified: Wed, 12 Apr 2023 01:21:16 GMT  
		Size: 10.6 MB (10573853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0bf11569c39ee4f3d8515112046a55f14f39e54c6f0ea26271033c090f77d2`  
		Last Modified: Wed, 12 Apr 2023 01:21:35 GMT  
		Size: 52.3 MB (52340617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:bca4866a43bc982429c365a3c9eae150e257f6e85a758fa3d39d843b62e8f5a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115725058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb174836486b1bffbdfcbbc82c0c81dfa80fde95c26ad135982dde37aba1e99`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:35 GMT
ADD file:75c57df33c95251a80549b7949853df282a42bc4e5f19176764907a54b74caa9 in / 
# Tue, 11 Apr 2023 23:59:36 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:35:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:35:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4feff9b88735325634445419eaaec2ed47500b63027cfd2de34b8bc6d55ee85c`  
		Last Modified: Wed, 12 Apr 2023 00:02:57 GMT  
		Size: 50.2 MB (50216882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5f77534be142d18fb6441aad5ebb0a6b1fbd1128fee964f14c772d3f48978f`  
		Last Modified: Wed, 12 Apr 2023 09:45:07 GMT  
		Size: 4.9 MB (4934569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0797973d3ff4c7bfddd6439ceacd815ea867f868a8c75686d5b80ee1a3eca322`  
		Last Modified: Wed, 12 Apr 2023 09:45:08 GMT  
		Size: 10.2 MB (10217876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cff4fab8e209a4a8ef903baadd1f4839687988e57cef0235a447c0198ddfab`  
		Last Modified: Wed, 12 Apr 2023 09:45:28 GMT  
		Size: 50.4 MB (50355731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8932a28128c9d2abaed3ae68d2641c6738ab07bf083ca8886920e13ce37bbce3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124407974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7143247bb9728129c637c315a5d5529383d57dfbf55c6999d1479a6f6dee2b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:42 GMT
ADD file:dd3d4e5fe819950e7d01b44a29dbd790438cd722ba76198910e2597448ab0c6f in / 
# Wed, 12 Apr 2023 00:39:43 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:06:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:06:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:07:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dc80b8cdbfd36cb20231d807a50d704945d1df4da8f6e23197ccfcb629970491`  
		Last Modified: Wed, 12 Apr 2023 00:42:14 GMT  
		Size: 53.7 MB (53705529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5884e7f2c8c61aa845de4902fc29639b58861ae6c2d80bafe82082c0456c0740`  
		Last Modified: Wed, 12 Apr 2023 01:13:17 GMT  
		Size: 5.2 MB (5152752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b792b01ed3c8dc1488cd8aac41ab7d49bb17f3fa22b2e6c846078cec81a1c00`  
		Last Modified: Wed, 12 Apr 2023 01:13:17 GMT  
		Size: 10.9 MB (10873655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f993d5b17f32f4b8a535c25e182e5d8412625beee450e513ca57036e8fdd6dc`  
		Last Modified: Wed, 12 Apr 2023 01:13:34 GMT  
		Size: 54.7 MB (54676038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2af50719cfc3c1165d1e75a99045d98388d375c4dcf2cafd5526a78d50080eab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128499065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7863e942eeec226faacc53f695802b0b24e7dd766b5e4a9498a0d7c62e92c702`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:38:51 GMT
ADD file:4da7e6af0782b21849e5f6385de3589ac5b8d81d173721f9990d32da754df2cb in / 
# Wed, 12 Apr 2023 00:38:51 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:05:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:05:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:06:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b2bef40925391866903279768b0ae1e8233ef6a1aae64509a922f4aa96fe42a6`  
		Last Modified: Wed, 12 Apr 2023 00:42:19 GMT  
		Size: 56.0 MB (56032818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37ccf9a5e34ba2345ce265a9a11c93ee254e1f3616dfd1c1deda6e2f7d614c8`  
		Last Modified: Wed, 12 Apr 2023 01:14:53 GMT  
		Size: 5.3 MB (5293626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4988d5e4328f031f6884a7351766aa8a2806c9cdca38d354477fc537eaa4911f`  
		Last Modified: Wed, 12 Apr 2023 01:14:54 GMT  
		Size: 11.2 MB (11249875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660a2befd486d43a308dd1561f57efeafe1f13defd6439d34aeb5efec783ee3d`  
		Last Modified: Wed, 12 Apr 2023 01:15:17 GMT  
		Size: 55.9 MB (55922746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:cae0c78b86d9818b2acfb8edab82633baa924d1c55cf73f682790afe23194474
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122368048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e2e60633ae43426dc3b6ad6b6c990668c1e5a30f73bfab6f97a660d5d16ef9d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:09:26 GMT
ADD file:5d2c839055739fe92d64098c09607e7ec9123101d15f837c54f3688755af0c23 in / 
# Wed, 12 Apr 2023 00:09:31 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 11:00:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 11:00:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 11:02:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80243e355b05bee53c6acc45ace2cde4f7495dafe9f3f8d7d299ed51d04928d2`  
		Last Modified: Wed, 12 Apr 2023 00:16:48 GMT  
		Size: 53.3 MB (53272023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed6aed7903d464c3c421335c8a4b93f11e64b669c7eab532e87e5945fd185e2`  
		Last Modified: Wed, 12 Apr 2023 11:20:32 GMT  
		Size: 5.1 MB (5127336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af3f0065ba2217f3ef903c35f7e644bd2222c1630a96ac62477510cedfa848`  
		Last Modified: Wed, 12 Apr 2023 11:20:34 GMT  
		Size: 10.7 MB (10662154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81fa7bf218e18cc100c89241735ff424465ba8caca78835fdadafcd212de62f`  
		Last Modified: Wed, 12 Apr 2023 11:21:19 GMT  
		Size: 53.3 MB (53306535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a328c66040a29e932ae7b1d267bd4b11602af4f3cf8bf7a959c2ab0b2c7b2541
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134837330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1795d723a8d4b32e096f6732a2e5a3c212e5f6bb12ad9bb5c0e5dd1b4257eba`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:07:58 GMT
ADD file:c3c2a10473ddaa3d8a30ca99b19ad3599d0e60d826c4e0315bdb7463352ebc09 in / 
# Wed, 12 Apr 2023 00:08:02 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:31:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:32:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:33:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2d3ffdd4610a019889b845cc82b3d956ad85cca78ad4bff2d5e5522bd02c17e7`  
		Last Modified: Wed, 12 Apr 2023 00:12:37 GMT  
		Size: 58.9 MB (58926600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00772c18aacd8e2ae167f5f94b2e86c7b77fd3f7790dc5e6754e48fcce1ff484`  
		Last Modified: Wed, 12 Apr 2023 09:45:12 GMT  
		Size: 5.4 MB (5415380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1877fd565f7c580ab3b8fd343d19de69c9c3334787d6a3c93c9c21fe08ea32a`  
		Last Modified: Wed, 12 Apr 2023 09:45:13 GMT  
		Size: 11.6 MB (11629984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a24a9774fce2d157b32633fbd68d6d4777632ca49b0a35d2e9be9a2455d88b`  
		Last Modified: Wed, 12 Apr 2023 09:45:40 GMT  
		Size: 58.9 MB (58865366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:dfe7b376859cc874a19230408e2042b1d984722eca290ce8cced0e27c6bdc7bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123263942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0184582450f7852885e4f2a6aaf51c5ec9ce0ff2ce9cd9b877a945b87bfd33c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:00:25 GMT
ADD file:ab4e28724d04724a57e0f5bbe299d3361103f05ad1978dc3bfef243c1f9d6476 in / 
# Wed, 12 Apr 2023 00:00:38 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:26:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:26:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 00:27:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:042263756d7dc47bf98a243871107aa3a2b41acda91d104d8b4e148749a43dda`  
		Last Modified: Wed, 12 Apr 2023 00:05:03 GMT  
		Size: 53.3 MB (53286682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2973b8c98f9da7833ab9cd69185dd958a8939a30136cdcfedb66ce775db358ee`  
		Last Modified: Wed, 12 Apr 2023 00:32:48 GMT  
		Size: 5.1 MB (5149313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f740d13ac612bf8b6489559a7945ec1439fee2d5eba455ab0db047cd3f30a9a`  
		Last Modified: Wed, 12 Apr 2023 00:32:49 GMT  
		Size: 10.8 MB (10766104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c0067783f401b099adca196dce9e464e66236e49faba106e2f04ac73a90df7`  
		Last Modified: Wed, 12 Apr 2023 00:33:02 GMT  
		Size: 54.1 MB (54061843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:buster`

```console
$ docker pull buildpack-deps@sha256:5c2114d327b0e2a38de4e3dcf5fa304e4da23264a1e77643632d0a25325d7e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:buster` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2ea103832a6fac73696522edc50dc0aa8c41a2073edb2d29685224196ed046e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.0 MB (312037541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:055f98e5c72e14d3f944a8a2f131602966cfd07c563d5884eddb16a00be4c875`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:15 GMT
ADD file:40953ed6e6f96703b2e0c13288437c2aaf8b3df33dbc423686290cbe0e595a5e in / 
# Wed, 12 Apr 2023 00:20:15 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:52:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 07:53:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:54:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2ff1d7c41c74a25258bfa6f0b8adb0a727f84518f55f65ca845ebc747976c408`  
		Last Modified: Wed, 12 Apr 2023 00:24:01 GMT  
		Size: 50.4 MB (50448726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b253aeafeaa7e0671bb60008df01de101a38a045ff7bc656e3b0fbfc7c05cca5`  
		Last Modified: Wed, 12 Apr 2023 07:58:30 GMT  
		Size: 7.9 MB (7863355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2201bd995cccf12851a50820de03d34a17011dcbb9ac9fdf3a50c952cbb131`  
		Last Modified: Wed, 12 Apr 2023 07:58:30 GMT  
		Size: 10.0 MB (10001452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de76e268b103d05fa8960e0f77951ff54b912b63429c34f5d6adfd09f5f9ee2`  
		Last Modified: Wed, 12 Apr 2023 07:58:44 GMT  
		Size: 51.9 MB (51876420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a8df5894511ce28a05e2925a75e8a4acbd0634c39ad734fdfba8e23d1b1569`  
		Last Modified: Wed, 12 Apr 2023 07:59:14 GMT  
		Size: 191.8 MB (191847588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:410344bd121264c1e44e6ff6404552757b78c17737dcb22a19f6ae20ba31f66d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.9 MB (277871836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd6300ad40c10f96fede2bdeedc551685aa3053dd2376792263ee1faf0f6f679`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:53 GMT
ADD file:3f6ca36ec4fbf50ab85c907c089dbb0618c73393c07a5841b922145b17795552 in / 
# Tue, 11 Apr 2023 23:59:54 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:37:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:37:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:37:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:39:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:166ef90dbaeab03f451f526d325c57795001e25f10c984c334a82d174b3c554b`  
		Last Modified: Wed, 12 Apr 2023 00:03:36 GMT  
		Size: 45.9 MB (45916201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84460c1688b734c8075a939aae674e32cf7240a0d3a2fa0602a9a9fd472ffe1e`  
		Last Modified: Wed, 12 Apr 2023 09:46:16 GMT  
		Size: 7.2 MB (7153935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed4779654861d62e5bc31eea7bacd2c7bbfdb617dd9dc01e2afd24a4baedf7f`  
		Last Modified: Wed, 12 Apr 2023 09:46:17 GMT  
		Size: 9.3 MB (9348985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6bfe04b18e678bcacb84dd292223f32a76d4837c22ccd16465318f6c1429f21`  
		Last Modified: Wed, 12 Apr 2023 09:46:34 GMT  
		Size: 47.4 MB (47395508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc69a47db99b12842846092749a24bc3d2701f5e6b46467a6eb56e1d19ed48a3`  
		Last Modified: Wed, 12 Apr 2023 09:47:09 GMT  
		Size: 168.1 MB (168057207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5e8e3f3212dcc5c0e3442e591cffe69a01891021308eca92c8b3bc2803c31459
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.6 MB (302601726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0303fb5950d191d02ab39565ca367ca55dc2b108c9b7ba4d645ed85d1a074d1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:55 GMT
ADD file:93facc669dd63b37fb5dde18f3b3a1cb5621aa396e1960ea85facdd1c619a3f0 in / 
# Wed, 12 Apr 2023 00:39:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:08:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:08:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:08:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:10:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b4910c31031a0301ea4f8b7155269014925aeb17c71b869dea3ff907ba294b55`  
		Last Modified: Wed, 12 Apr 2023 00:42:52 GMT  
		Size: 49.2 MB (49238632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208fd617b499747daceba851b67da426c285d1e306b316a193f06968123f49da`  
		Last Modified: Wed, 12 Apr 2023 01:14:12 GMT  
		Size: 7.7 MB (7732136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efadebfda1423d1b70a0e991e9ff8bb2e3fe0b08d55562359a004c265fc7c86`  
		Last Modified: Wed, 12 Apr 2023 01:14:12 GMT  
		Size: 10.0 MB (10003581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe7e7c438113f5e58417f97e7eb0a755b17ee63eebd85a7c3b86a2aad4c993e`  
		Last Modified: Wed, 12 Apr 2023 01:14:27 GMT  
		Size: 52.2 MB (52191713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33997ebd7335eb6f55d98725b5fb8e4899166098d6db119cd6f6bc7055ffa858`  
		Last Modified: Wed, 12 Apr 2023 01:14:51 GMT  
		Size: 183.4 MB (183435664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; 386

```console
$ docker pull buildpack-deps@sha256:76a9d8ac8ca52b47077a29022657b9bdc9facd485bf6f6bc8c7115ed9915e020
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.5 MB (321464682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb3655fb3b861afdfc5e7da86468a57acd97ab2b796815bf255141ce4e9ec42c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:11 GMT
ADD file:8299e58c7e43af1f3b9fdb9bd37e3f37cf619a97ef1b87d60ca66860d646d526 in / 
# Wed, 12 Apr 2023 00:39:11 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:08:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:08:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:08:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:11:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2d15e1c2a3da7d675c2513d7ceab1d0f33ced9a82bed63d9a11ce71f1218d232`  
		Last Modified: Wed, 12 Apr 2023 00:43:07 GMT  
		Size: 51.2 MB (51206167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af123d7f5c8b1197b6040820195efacf1a57299baf71416c7a63281566cdc199`  
		Last Modified: Wed, 12 Apr 2023 01:16:15 GMT  
		Size: 8.0 MB (8034011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3af175eda8706326ac898703f9aafb47e7e08ec08318794c6838efa8f3d3bc`  
		Last Modified: Wed, 12 Apr 2023 01:16:15 GMT  
		Size: 10.3 MB (10345678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9cbd6d7217bf920da02e590f88fbfb42fb3162969840a3b17eb25c762247c04`  
		Last Modified: Wed, 12 Apr 2023 01:16:35 GMT  
		Size: 53.5 MB (53471080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d0a6f1efbd6131f1ae888ea393318f9d32a3e8ad8b8c97207c3a5b7a3ed9bc`  
		Last Modified: Wed, 12 Apr 2023 01:17:17 GMT  
		Size: 198.4 MB (198407746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:buster-curl`

```console
$ docker pull buildpack-deps@sha256:aced785a2513d8727060141156b30a8a3081d95054e1196da909d83c1c6d1203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:buster-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7f26d8de0d9b1472f4b76a591461f81e28dd4469eed96b3bb172a93adde9779f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68313533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212d47455d74a1b460742fc95270dd155e5dccb7f8cf98d1b0166a911a42e56f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:15 GMT
ADD file:40953ed6e6f96703b2e0c13288437c2aaf8b3df33dbc423686290cbe0e595a5e in / 
# Wed, 12 Apr 2023 00:20:15 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:52:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2ff1d7c41c74a25258bfa6f0b8adb0a727f84518f55f65ca845ebc747976c408`  
		Last Modified: Wed, 12 Apr 2023 00:24:01 GMT  
		Size: 50.4 MB (50448726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b253aeafeaa7e0671bb60008df01de101a38a045ff7bc656e3b0fbfc7c05cca5`  
		Last Modified: Wed, 12 Apr 2023 07:58:30 GMT  
		Size: 7.9 MB (7863355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2201bd995cccf12851a50820de03d34a17011dcbb9ac9fdf3a50c952cbb131`  
		Last Modified: Wed, 12 Apr 2023 07:58:30 GMT  
		Size: 10.0 MB (10001452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:076bc54af0ee3f4cc5de008a85e1e66f5f01d819b9bdf9ed313c1c1b88928e78
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62419121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79aebda5e687723c136aae0676cad834f015f5bb039f4857700bf9dba626b13f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:53 GMT
ADD file:3f6ca36ec4fbf50ab85c907c089dbb0618c73393c07a5841b922145b17795552 in / 
# Tue, 11 Apr 2023 23:59:54 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:37:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:37:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:166ef90dbaeab03f451f526d325c57795001e25f10c984c334a82d174b3c554b`  
		Last Modified: Wed, 12 Apr 2023 00:03:36 GMT  
		Size: 45.9 MB (45916201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84460c1688b734c8075a939aae674e32cf7240a0d3a2fa0602a9a9fd472ffe1e`  
		Last Modified: Wed, 12 Apr 2023 09:46:16 GMT  
		Size: 7.2 MB (7153935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed4779654861d62e5bc31eea7bacd2c7bbfdb617dd9dc01e2afd24a4baedf7f`  
		Last Modified: Wed, 12 Apr 2023 09:46:17 GMT  
		Size: 9.3 MB (9348985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f4f9c875a9f7cdaa332594325c8c868d26a05ef018355a11554c8b1b5657b625
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (66974349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25cefdb01c939d204ba6d7c49b6053a29c8ad035592de81e899acd889fd70fc2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:55 GMT
ADD file:93facc669dd63b37fb5dde18f3b3a1cb5621aa396e1960ea85facdd1c619a3f0 in / 
# Wed, 12 Apr 2023 00:39:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:08:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:08:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b4910c31031a0301ea4f8b7155269014925aeb17c71b869dea3ff907ba294b55`  
		Last Modified: Wed, 12 Apr 2023 00:42:52 GMT  
		Size: 49.2 MB (49238632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208fd617b499747daceba851b67da426c285d1e306b316a193f06968123f49da`  
		Last Modified: Wed, 12 Apr 2023 01:14:12 GMT  
		Size: 7.7 MB (7732136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efadebfda1423d1b70a0e991e9ff8bb2e3fe0b08d55562359a004c265fc7c86`  
		Last Modified: Wed, 12 Apr 2023 01:14:12 GMT  
		Size: 10.0 MB (10003581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:da84dcb1542b8a34ef0e6ebd7f50eeb5da1bf9f8c87c221b3d3a2bd81c81de56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69585856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256da6b06a3adecebaf9bba1b763d651016b84bfec4ad7bc9dbe24e15f37894a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:11 GMT
ADD file:8299e58c7e43af1f3b9fdb9bd37e3f37cf619a97ef1b87d60ca66860d646d526 in / 
# Wed, 12 Apr 2023 00:39:11 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:08:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:08:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2d15e1c2a3da7d675c2513d7ceab1d0f33ced9a82bed63d9a11ce71f1218d232`  
		Last Modified: Wed, 12 Apr 2023 00:43:07 GMT  
		Size: 51.2 MB (51206167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af123d7f5c8b1197b6040820195efacf1a57299baf71416c7a63281566cdc199`  
		Last Modified: Wed, 12 Apr 2023 01:16:15 GMT  
		Size: 8.0 MB (8034011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3af175eda8706326ac898703f9aafb47e7e08ec08318794c6838efa8f3d3bc`  
		Last Modified: Wed, 12 Apr 2023 01:16:15 GMT  
		Size: 10.3 MB (10345678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:buster-scm`

```console
$ docker pull buildpack-deps@sha256:08c41fe7825eae00e1c06c4f80dec886cf1d2ddb59aa9c22db15f4b323e97bdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:buster-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0559dadbf61570961c0fad2acef618449ab55dc06360900e44639acdfc52d29b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120189953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ba89d7351401c33e1d4f3e124b255947cc4bf33b68236db9d8985829c0c1420`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:15 GMT
ADD file:40953ed6e6f96703b2e0c13288437c2aaf8b3df33dbc423686290cbe0e595a5e in / 
# Wed, 12 Apr 2023 00:20:15 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:52:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 07:53:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2ff1d7c41c74a25258bfa6f0b8adb0a727f84518f55f65ca845ebc747976c408`  
		Last Modified: Wed, 12 Apr 2023 00:24:01 GMT  
		Size: 50.4 MB (50448726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b253aeafeaa7e0671bb60008df01de101a38a045ff7bc656e3b0fbfc7c05cca5`  
		Last Modified: Wed, 12 Apr 2023 07:58:30 GMT  
		Size: 7.9 MB (7863355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2201bd995cccf12851a50820de03d34a17011dcbb9ac9fdf3a50c952cbb131`  
		Last Modified: Wed, 12 Apr 2023 07:58:30 GMT  
		Size: 10.0 MB (10001452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de76e268b103d05fa8960e0f77951ff54b912b63429c34f5d6adfd09f5f9ee2`  
		Last Modified: Wed, 12 Apr 2023 07:58:44 GMT  
		Size: 51.9 MB (51876420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d925de6f72cf2aa2ab02bdd4c3d06adb08d6466494a4e8bef5bc734e3a607fb4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109814629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d111674b4fe94e19007fc403fdd31abbba530618ab7e280ec871ab5d045784`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:53 GMT
ADD file:3f6ca36ec4fbf50ab85c907c089dbb0618c73393c07a5841b922145b17795552 in / 
# Tue, 11 Apr 2023 23:59:54 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:37:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:37:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:37:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:166ef90dbaeab03f451f526d325c57795001e25f10c984c334a82d174b3c554b`  
		Last Modified: Wed, 12 Apr 2023 00:03:36 GMT  
		Size: 45.9 MB (45916201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84460c1688b734c8075a939aae674e32cf7240a0d3a2fa0602a9a9fd472ffe1e`  
		Last Modified: Wed, 12 Apr 2023 09:46:16 GMT  
		Size: 7.2 MB (7153935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed4779654861d62e5bc31eea7bacd2c7bbfdb617dd9dc01e2afd24a4baedf7f`  
		Last Modified: Wed, 12 Apr 2023 09:46:17 GMT  
		Size: 9.3 MB (9348985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6bfe04b18e678bcacb84dd292223f32a76d4837c22ccd16465318f6c1429f21`  
		Last Modified: Wed, 12 Apr 2023 09:46:34 GMT  
		Size: 47.4 MB (47395508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:96e03d67380daeace99ddc589fb25df608d86e8a2d78ef9d4635323c7774934b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119166062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2ed8743d8648e388b28b2c5274b320ccc3352bca03a56d3d0b65c133c5acf9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:55 GMT
ADD file:93facc669dd63b37fb5dde18f3b3a1cb5621aa396e1960ea85facdd1c619a3f0 in / 
# Wed, 12 Apr 2023 00:39:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:08:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:08:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:08:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b4910c31031a0301ea4f8b7155269014925aeb17c71b869dea3ff907ba294b55`  
		Last Modified: Wed, 12 Apr 2023 00:42:52 GMT  
		Size: 49.2 MB (49238632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208fd617b499747daceba851b67da426c285d1e306b316a193f06968123f49da`  
		Last Modified: Wed, 12 Apr 2023 01:14:12 GMT  
		Size: 7.7 MB (7732136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efadebfda1423d1b70a0e991e9ff8bb2e3fe0b08d55562359a004c265fc7c86`  
		Last Modified: Wed, 12 Apr 2023 01:14:12 GMT  
		Size: 10.0 MB (10003581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe7e7c438113f5e58417f97e7eb0a755b17ee63eebd85a7c3b86a2aad4c993e`  
		Last Modified: Wed, 12 Apr 2023 01:14:27 GMT  
		Size: 52.2 MB (52191713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0e2e0b3634ba26d3880a8dad7170dc329234f18b5b9b38e0bd3c4637cbe27ace
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123056936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67dfa6883f98d7b82d1d95b560a9f118e646738acef237ff47081baf6ed84941`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:11 GMT
ADD file:8299e58c7e43af1f3b9fdb9bd37e3f37cf619a97ef1b87d60ca66860d646d526 in / 
# Wed, 12 Apr 2023 00:39:11 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:08:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:08:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:08:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2d15e1c2a3da7d675c2513d7ceab1d0f33ced9a82bed63d9a11ce71f1218d232`  
		Last Modified: Wed, 12 Apr 2023 00:43:07 GMT  
		Size: 51.2 MB (51206167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af123d7f5c8b1197b6040820195efacf1a57299baf71416c7a63281566cdc199`  
		Last Modified: Wed, 12 Apr 2023 01:16:15 GMT  
		Size: 8.0 MB (8034011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3af175eda8706326ac898703f9aafb47e7e08ec08318794c6838efa8f3d3bc`  
		Last Modified: Wed, 12 Apr 2023 01:16:15 GMT  
		Size: 10.3 MB (10345678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9cbd6d7217bf920da02e590f88fbfb42fb3162969840a3b17eb25c762247c04`  
		Last Modified: Wed, 12 Apr 2023 01:16:35 GMT  
		Size: 53.5 MB (53471080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:curl`

```console
$ docker pull buildpack-deps@sha256:b77ca637508f0f6f5d834c57f2e6af153c2ce4a48afb439b5fb469529360a951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:acd62d4d9773006a9d0acddc08a4cbf7637d1c975e67459b52a7dc093bdfc271
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71096181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af19f7b630d3d79df60c6a9ae3051940c35c240094ef6e54f4f7843577467896`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:55 GMT
ADD file:f2d012660f882f319a5878a3f9ce285f488b8f90fad49ad238541cf72089e035 in / 
# Wed, 12 Apr 2023 00:19:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:50:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:51:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b0248cf3e63c73d0e496a67807d056ca41d5e968b61087e8eca2cf4b9b4d7b99`  
		Last Modified: Wed, 12 Apr 2023 00:23:20 GMT  
		Size: 55.1 MB (55052736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127e97b4daf784e08840a21765f0d4f251192ef2994d0e4a253490f81e63955b`  
		Last Modified: Wed, 12 Apr 2023 07:57:29 GMT  
		Size: 5.2 MB (5166696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0336c50c9f6942b660e433b1086238eec37057c34b14c4e3b28bd7bf05bd84ba`  
		Last Modified: Wed, 12 Apr 2023 07:57:29 GMT  
		Size: 10.9 MB (10876749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:03091d90e79cf371dee743c2a8537556060a22246a5c1a68d53f63e201715f4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68201855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39fd3f1fac0693a3efcdf720af9216deb72c54ed024f9c8edfa061944f26d405`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:48:34 GMT
ADD file:ae13a4cbeb20b92ec29dd7409de47a964fe373bdde2a4e8880b5a4d9dc64171e in / 
# Wed, 12 Apr 2023 00:48:35 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:15:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:15:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:86cb8d774eca43d428d6a35506c172ba62358d2d5ec90c886e3b38b297f93b20`  
		Last Modified: Wed, 12 Apr 2023 00:50:46 GMT  
		Size: 52.6 MB (52555175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49db155cdf8645f599affcbbbc75eb928b0a9d010c4ac54afcfa9d7e4fa85e0`  
		Last Modified: Wed, 12 Apr 2023 01:21:15 GMT  
		Size: 5.1 MB (5072827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8936087cbd048148575fda58348506149db80a2699e99ae2042086628c0e5a38`  
		Last Modified: Wed, 12 Apr 2023 01:21:16 GMT  
		Size: 10.6 MB (10573853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a8434b10032012c2760d715f731aa184a425b42164650c42161de37dd78702cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65369327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475e074940bc42bc670d7bf9b9fb35f58ef5e44c093fb372fa6b177c75f785cc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:35 GMT
ADD file:75c57df33c95251a80549b7949853df282a42bc4e5f19176764907a54b74caa9 in / 
# Tue, 11 Apr 2023 23:59:36 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:35:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:4feff9b88735325634445419eaaec2ed47500b63027cfd2de34b8bc6d55ee85c`  
		Last Modified: Wed, 12 Apr 2023 00:02:57 GMT  
		Size: 50.2 MB (50216882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5f77534be142d18fb6441aad5ebb0a6b1fbd1128fee964f14c772d3f48978f`  
		Last Modified: Wed, 12 Apr 2023 09:45:07 GMT  
		Size: 4.9 MB (4934569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0797973d3ff4c7bfddd6439ceacd815ea867f868a8c75686d5b80ee1a3eca322`  
		Last Modified: Wed, 12 Apr 2023 09:45:08 GMT  
		Size: 10.2 MB (10217876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a5537c32568d575a5a3bb0f96138a7cf42dc7d590729308b1ed7538fbdd433e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69731936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0130b5aae27ce4286f62ae8a2e5324e811b8d862aa0aea6923a7b461615ccf17`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:42 GMT
ADD file:dd3d4e5fe819950e7d01b44a29dbd790438cd722ba76198910e2597448ab0c6f in / 
# Wed, 12 Apr 2023 00:39:43 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:06:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:06:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:dc80b8cdbfd36cb20231d807a50d704945d1df4da8f6e23197ccfcb629970491`  
		Last Modified: Wed, 12 Apr 2023 00:42:14 GMT  
		Size: 53.7 MB (53705529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5884e7f2c8c61aa845de4902fc29639b58861ae6c2d80bafe82082c0456c0740`  
		Last Modified: Wed, 12 Apr 2023 01:13:17 GMT  
		Size: 5.2 MB (5152752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b792b01ed3c8dc1488cd8aac41ab7d49bb17f3fa22b2e6c846078cec81a1c00`  
		Last Modified: Wed, 12 Apr 2023 01:13:17 GMT  
		Size: 10.9 MB (10873655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:39321899797ed2861f1e87a3547e2e911faa2ce033098728aa240b793dd8232b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72576319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1535cd25f9ea155765a6cae9f83a5e50a533888ddb926700a119b7e91a0a0f1b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:38:51 GMT
ADD file:4da7e6af0782b21849e5f6385de3589ac5b8d81d173721f9990d32da754df2cb in / 
# Wed, 12 Apr 2023 00:38:51 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:05:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:05:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b2bef40925391866903279768b0ae1e8233ef6a1aae64509a922f4aa96fe42a6`  
		Last Modified: Wed, 12 Apr 2023 00:42:19 GMT  
		Size: 56.0 MB (56032818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37ccf9a5e34ba2345ce265a9a11c93ee254e1f3616dfd1c1deda6e2f7d614c8`  
		Last Modified: Wed, 12 Apr 2023 01:14:53 GMT  
		Size: 5.3 MB (5293626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4988d5e4328f031f6884a7351766aa8a2806c9cdca38d354477fc537eaa4911f`  
		Last Modified: Wed, 12 Apr 2023 01:14:54 GMT  
		Size: 11.2 MB (11249875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:66e9ab47759b918c5d7fec7837bf41e0032b99600e25a33827f94b51355e46e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69061513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6925f09cbf336d4383b178072c72886c41699bb1743ff950dfc483a88c39a928`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:09:26 GMT
ADD file:5d2c839055739fe92d64098c09607e7ec9123101d15f837c54f3688755af0c23 in / 
# Wed, 12 Apr 2023 00:09:31 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 11:00:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 11:00:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:80243e355b05bee53c6acc45ace2cde4f7495dafe9f3f8d7d299ed51d04928d2`  
		Last Modified: Wed, 12 Apr 2023 00:16:48 GMT  
		Size: 53.3 MB (53272023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed6aed7903d464c3c421335c8a4b93f11e64b669c7eab532e87e5945fd185e2`  
		Last Modified: Wed, 12 Apr 2023 11:20:32 GMT  
		Size: 5.1 MB (5127336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af3f0065ba2217f3ef903c35f7e644bd2222c1630a96ac62477510cedfa848`  
		Last Modified: Wed, 12 Apr 2023 11:20:34 GMT  
		Size: 10.7 MB (10662154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d2bf2a378307a21bf35bbc234fd0768bf348c2aa8d28c3ee065b4248dcbfa2d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (75971964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17ee001184461420ef6a9dcaa8006e2702365c6fb83c1ea64e12ef337924ac12`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:07:58 GMT
ADD file:c3c2a10473ddaa3d8a30ca99b19ad3599d0e60d826c4e0315bdb7463352ebc09 in / 
# Wed, 12 Apr 2023 00:08:02 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:31:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:32:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2d3ffdd4610a019889b845cc82b3d956ad85cca78ad4bff2d5e5522bd02c17e7`  
		Last Modified: Wed, 12 Apr 2023 00:12:37 GMT  
		Size: 58.9 MB (58926600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00772c18aacd8e2ae167f5f94b2e86c7b77fd3f7790dc5e6754e48fcce1ff484`  
		Last Modified: Wed, 12 Apr 2023 09:45:12 GMT  
		Size: 5.4 MB (5415380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1877fd565f7c580ab3b8fd343d19de69c9c3334787d6a3c93c9c21fe08ea32a`  
		Last Modified: Wed, 12 Apr 2023 09:45:13 GMT  
		Size: 11.6 MB (11629984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5726b9b13d1328b42898380f57612273babbfe94f7918919e3553ca203957c96
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69202099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d3f520b42352a1bbcb04c9c67c162e7870ac7063005e1cbfb804dea99188dc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:00:25 GMT
ADD file:ab4e28724d04724a57e0f5bbe299d3361103f05ad1978dc3bfef243c1f9d6476 in / 
# Wed, 12 Apr 2023 00:00:38 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:26:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:26:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:042263756d7dc47bf98a243871107aa3a2b41acda91d104d8b4e148749a43dda`  
		Last Modified: Wed, 12 Apr 2023 00:05:03 GMT  
		Size: 53.3 MB (53286682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2973b8c98f9da7833ab9cd69185dd958a8939a30136cdcfedb66ce775db358ee`  
		Last Modified: Wed, 12 Apr 2023 00:32:48 GMT  
		Size: 5.1 MB (5149313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f740d13ac612bf8b6489559a7945ec1439fee2d5eba455ab0db047cd3f30a9a`  
		Last Modified: Wed, 12 Apr 2023 00:32:49 GMT  
		Size: 10.8 MB (10766104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:focal`

```console
$ docker pull buildpack-deps@sha256:838634b0a7daabf564f087e7f9b5818c7b3ae9312cc42908e8fd7fd4317cd638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:focal` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:dd5e6240f9fcbcbe0f6f1a3405b40d0ab6e82fbe91909deaa1212cc65b48f1da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245783085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37352ea462c043f4e445123486977b7b52534da3dd5e19c44166e8f46f245097`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:23:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:23:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:24:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:25:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb9a1000294d18d6dc41a0282435b987380b7f0b46c7f3dc891087e1a473ce2`  
		Last Modified: Tue, 18 Apr 2023 01:34:39 GMT  
		Size: 7.7 MB (7744253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986bdd8de236de34e3a40a899fbcd02bedbc9de7f3b6ced517c2fa4149ab0fdd`  
		Last Modified: Tue, 18 Apr 2023 01:34:38 GMT  
		Size: 3.6 MB (3627203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a87a85bf796c479f3384f9845bbb9da0e19847e85730eef87d5e68561f7c9d`  
		Last Modified: Tue, 18 Apr 2023 01:34:59 GMT  
		Size: 60.7 MB (60745533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c05a097a1be622d326505e77f9094db55692396eeea49cabc0f2d782e8c4dd`  
		Last Modified: Tue, 18 Apr 2023 01:35:27 GMT  
		Size: 145.1 MB (145087533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:10cc7efff129069f31d402ddacdbf482a876e5419831f90619e7e6b457f80e55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.8 MB (211791715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c67b859cc6a4bbe955c191558f0017a32648ececc20276b3da75e1f2563a037`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:47 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:20:50 GMT
ADD file:0da456bd328984fcedf5367b46a38da6ca4b43061baf6d1283380962cddc7481 in / 
# Thu, 13 Apr 2023 13:20:50 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:34:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:34:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:35:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:38:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e68c91cb250f35160f683afa80c3ada46f06948ded46a188be490ea3afff08f5`  
		Last Modified: Fri, 14 Apr 2023 09:34:28 GMT  
		Size: 24.6 MB (24586976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029732d3be1a924e821f7cd01afe768f39d85e2d484ace5bcceab5fbc250c347`  
		Last Modified: Tue, 18 Apr 2023 01:49:22 GMT  
		Size: 6.7 MB (6729180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df6a23fdc52b8fc5a75f036a53f4c9f7a7e07c603fe5a73ba891f8dee1a7505`  
		Last Modified: Tue, 18 Apr 2023 01:49:21 GMT  
		Size: 3.1 MB (3104419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21583b635c301612839572600eb97628067e10e4fd4af5803b399abbcbfc8054`  
		Last Modified: Tue, 18 Apr 2023 01:49:41 GMT  
		Size: 55.4 MB (55443791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49765b1a78a05ff3d4d223bda34a4d9e7223b0de368ac54afe942a68f60b9e29`  
		Last Modified: Tue, 18 Apr 2023 01:50:07 GMT  
		Size: 121.9 MB (121927349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f49b29319819b63c4b870e6272eddc5c21fbefb46d5e0b521909247ce724e230
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (235991114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9d124be76c767ac4c947fc3428ac1d7b0af211d5140cbe2f0390bc20ea03aa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:20:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:20:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:20:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:23:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2378679266ac5157323158b6e52e7a884e559db5217037e57992e47a1667d525`  
		Last Modified: Fri, 14 Apr 2023 07:39:20 GMT  
		Size: 27.2 MB (27196396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fee697311c4e091f41acde237da003390953c6ecc286d893292b2dcd0c76821`  
		Last Modified: Tue, 18 Apr 2023 01:34:33 GMT  
		Size: 7.6 MB (7604657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c60e27a0516909c7200fcf3394a9e6e0d0e593249f51b70b05db3952b66592`  
		Last Modified: Tue, 18 Apr 2023 01:34:32 GMT  
		Size: 3.6 MB (3617029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d5ef789db5e2842d73302eede7f6b7a692bd35f3ee908d4039d7853bf8157a`  
		Last Modified: Tue, 18 Apr 2023 01:34:47 GMT  
		Size: 60.8 MB (60807001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f147652501c7415f8b33749fd53610b03fad71aeb32c9307e0c1e93049148db6`  
		Last Modified: Tue, 18 Apr 2023 01:35:09 GMT  
		Size: 136.8 MB (136766031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0d5ca5035ccb90aa7f7888823fe1abfbcced3b7ac57b01d5885eae7f5fd0915e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269620396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da4a2917c479ad5c831ac7b1e22ffbfdb4017dfd4c56d11a4268714434557735`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:36:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:36:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 00:38:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:44:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d276072145993a42aed3e2b3e8cd26b6e08aab266d9c9d792ee89b26150681da`  
		Last Modified: Fri, 14 Apr 2023 09:36:00 GMT  
		Size: 33.3 MB (33300980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:923459354bb7c8ed9378009c3b9bfafa2c71db0dd9434ff6f28fa8559018a9fe`  
		Last Modified: Tue, 18 Apr 2023 01:01:27 GMT  
		Size: 8.7 MB (8694604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14eb66e0ca52c6c0e9019cd99e5a7d12708b5fcf95d917cf1dcd06a56b91160`  
		Last Modified: Tue, 18 Apr 2023 01:01:26 GMT  
		Size: 4.5 MB (4486817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e714fae693c74669418568b2a270066a28e7e561eae1ff8896650c09e925c0e0`  
		Last Modified: Tue, 18 Apr 2023 01:02:00 GMT  
		Size: 69.6 MB (69551759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cbfcddd95021b74ec467c8940e3dbdb2a5bddcfd554c99e9d4cd2908cd48db`  
		Last Modified: Tue, 18 Apr 2023 01:02:48 GMT  
		Size: 153.6 MB (153586236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ea1d4fe41029219e24238984342752c22186d78c9a76b177751136beee29eb8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226382412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e38d59d083edfdf8d44ec3f0d15c7e9bab6a63149c98e6ecafb7ece063c1252`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:35 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:37 GMT
ADD file:44c66c03ba0afcc05de1b2078f83e8bfe04706b31491fcd3fdd93cfc88d5f06c in / 
# Thu, 13 Apr 2023 13:09:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:01:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:02:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:02:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:05:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f11b609b1d63f2d37c0e3789823e7a7e62a078bddca7c46da8602655989c62d9`  
		Last Modified: Fri, 14 Apr 2023 09:38:39 GMT  
		Size: 27.0 MB (27016370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfd953572ac96bfce6706f45014f76e59e53b096cdc8eba22ffc73112fa0b3c`  
		Last Modified: Tue, 18 Apr 2023 01:13:21 GMT  
		Size: 7.4 MB (7383689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc90d577c47f7094dda274dbf62b36e812018f84c10844be7715d198c95ddfef`  
		Last Modified: Tue, 18 Apr 2023 01:13:21 GMT  
		Size: 3.5 MB (3542231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a73d2f132bb961264ac78079104aeb71d832e93e48e8bc52edc4cb58ed80e5`  
		Last Modified: Tue, 18 Apr 2023 01:13:38 GMT  
		Size: 60.0 MB (60018552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de07e3fe4a067ed0ec9ea6ffefdaf899a92a5a3700af3a79b09f15d87b7ccf21`  
		Last Modified: Tue, 18 Apr 2023 01:14:01 GMT  
		Size: 128.4 MB (128421570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:focal-curl`

```console
$ docker pull buildpack-deps@sha256:e5bf5d43f727c6d007d5ff3da4ab2be4d551ca8fb14acb958b7b2319fe0aa144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:focal-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5d167aefeaa2fb9ce79039758c2e7e6f56edf1a89ce8bc448e2f0cefe70f016b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.0 MB (39950019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d29726e1d46db52e0feed2033aa867e7f1bafe790a3630d26ce848a63d201a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:23:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:23:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb9a1000294d18d6dc41a0282435b987380b7f0b46c7f3dc891087e1a473ce2`  
		Last Modified: Tue, 18 Apr 2023 01:34:39 GMT  
		Size: 7.7 MB (7744253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986bdd8de236de34e3a40a899fbcd02bedbc9de7f3b6ced517c2fa4149ab0fdd`  
		Last Modified: Tue, 18 Apr 2023 01:34:38 GMT  
		Size: 3.6 MB (3627203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0628a7d571d19fc024ba47f0d48d0d5abce1c8cf9fcaf8e47656b7530a9c568f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34420575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa87f794e80c6034ad4c3e37878afcbdfab9a85127f85cd589b076509cc57c7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:47 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:20:50 GMT
ADD file:0da456bd328984fcedf5367b46a38da6ca4b43061baf6d1283380962cddc7481 in / 
# Thu, 13 Apr 2023 13:20:50 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:34:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:34:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:e68c91cb250f35160f683afa80c3ada46f06948ded46a188be490ea3afff08f5`  
		Last Modified: Fri, 14 Apr 2023 09:34:28 GMT  
		Size: 24.6 MB (24586976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029732d3be1a924e821f7cd01afe768f39d85e2d484ace5bcceab5fbc250c347`  
		Last Modified: Tue, 18 Apr 2023 01:49:22 GMT  
		Size: 6.7 MB (6729180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df6a23fdc52b8fc5a75f036a53f4c9f7a7e07c603fe5a73ba891f8dee1a7505`  
		Last Modified: Tue, 18 Apr 2023 01:49:21 GMT  
		Size: 3.1 MB (3104419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a5a09365e7a798606f12145b1a2aa619dcf85ac37d76bf3a1a265f4ec322b82a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.4 MB (38418082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1203810cbe5d7ab8ee42998962ed79b73f595e7c95742f93e279128030402c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:20:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:20:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2378679266ac5157323158b6e52e7a884e559db5217037e57992e47a1667d525`  
		Last Modified: Fri, 14 Apr 2023 07:39:20 GMT  
		Size: 27.2 MB (27196396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fee697311c4e091f41acde237da003390953c6ecc286d893292b2dcd0c76821`  
		Last Modified: Tue, 18 Apr 2023 01:34:33 GMT  
		Size: 7.6 MB (7604657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c60e27a0516909c7200fcf3394a9e6e0d0e593249f51b70b05db3952b66592`  
		Last Modified: Tue, 18 Apr 2023 01:34:32 GMT  
		Size: 3.6 MB (3617029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9a7c1ca644dbaeb4e9f71191e1d38e9fb4e701776f81ffd32f8e15bd3488dc63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46482401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d0cac502d4a1f06f6436f63ca94d88152c8e4b92b64470e43375be4510e382e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:36:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:36:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d276072145993a42aed3e2b3e8cd26b6e08aab266d9c9d792ee89b26150681da`  
		Last Modified: Fri, 14 Apr 2023 09:36:00 GMT  
		Size: 33.3 MB (33300980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:923459354bb7c8ed9378009c3b9bfafa2c71db0dd9434ff6f28fa8559018a9fe`  
		Last Modified: Tue, 18 Apr 2023 01:01:27 GMT  
		Size: 8.7 MB (8694604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14eb66e0ca52c6c0e9019cd99e5a7d12708b5fcf95d917cf1dcd06a56b91160`  
		Last Modified: Tue, 18 Apr 2023 01:01:26 GMT  
		Size: 4.5 MB (4486817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b1e9c44d6382be519684eb9baeafa3d3987d5fbb96b18f184e460fe8cd2b2523
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37942290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b37a689a24b79a714a9ba3d143e6ee344a23c224ab53f56218912ef410c4d81a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:35 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:37 GMT
ADD file:44c66c03ba0afcc05de1b2078f83e8bfe04706b31491fcd3fdd93cfc88d5f06c in / 
# Thu, 13 Apr 2023 13:09:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:01:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:02:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:f11b609b1d63f2d37c0e3789823e7a7e62a078bddca7c46da8602655989c62d9`  
		Last Modified: Fri, 14 Apr 2023 09:38:39 GMT  
		Size: 27.0 MB (27016370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfd953572ac96bfce6706f45014f76e59e53b096cdc8eba22ffc73112fa0b3c`  
		Last Modified: Tue, 18 Apr 2023 01:13:21 GMT  
		Size: 7.4 MB (7383689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc90d577c47f7094dda274dbf62b36e812018f84c10844be7715d198c95ddfef`  
		Last Modified: Tue, 18 Apr 2023 01:13:21 GMT  
		Size: 3.5 MB (3542231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:focal-scm`

```console
$ docker pull buildpack-deps@sha256:77cd090edcf9a80bdc1593875fec276b9707bc4b20033d9b94305e56e49704c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:focal-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:47b489d185fb17e3e4f0fc2a7284c506770fb797f36984482679b4d8501adc3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100695552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d95dd14a8d4f56fe1a512f3b3e0fe9b5991c977d0e07e35a715ecb1be3d6457`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:23:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:23:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:24:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb9a1000294d18d6dc41a0282435b987380b7f0b46c7f3dc891087e1a473ce2`  
		Last Modified: Tue, 18 Apr 2023 01:34:39 GMT  
		Size: 7.7 MB (7744253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986bdd8de236de34e3a40a899fbcd02bedbc9de7f3b6ced517c2fa4149ab0fdd`  
		Last Modified: Tue, 18 Apr 2023 01:34:38 GMT  
		Size: 3.6 MB (3627203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a87a85bf796c479f3384f9845bbb9da0e19847e85730eef87d5e68561f7c9d`  
		Last Modified: Tue, 18 Apr 2023 01:34:59 GMT  
		Size: 60.7 MB (60745533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9bc5ce508a49cf286377f106cb4e3fa3244acedd048a885383a8a848cfa61298
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.9 MB (89864366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14e666bff045b0d2159f0f22babec61e9c232b43bce2bfed15f4a37485c646c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:47 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:20:50 GMT
ADD file:0da456bd328984fcedf5367b46a38da6ca4b43061baf6d1283380962cddc7481 in / 
# Thu, 13 Apr 2023 13:20:50 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:34:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:34:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:35:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e68c91cb250f35160f683afa80c3ada46f06948ded46a188be490ea3afff08f5`  
		Last Modified: Fri, 14 Apr 2023 09:34:28 GMT  
		Size: 24.6 MB (24586976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029732d3be1a924e821f7cd01afe768f39d85e2d484ace5bcceab5fbc250c347`  
		Last Modified: Tue, 18 Apr 2023 01:49:22 GMT  
		Size: 6.7 MB (6729180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df6a23fdc52b8fc5a75f036a53f4c9f7a7e07c603fe5a73ba891f8dee1a7505`  
		Last Modified: Tue, 18 Apr 2023 01:49:21 GMT  
		Size: 3.1 MB (3104419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21583b635c301612839572600eb97628067e10e4fd4af5803b399abbcbfc8054`  
		Last Modified: Tue, 18 Apr 2023 01:49:41 GMT  
		Size: 55.4 MB (55443791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:098a12c340df6609717509b4709d479d9a1dc023641ff15c5723cfdbb4acf8b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99225083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d851cc464e9adf44ba6942b3bae4e4a50116b410a00b63c7048d7e9d79a2ff5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:20:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:20:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:20:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2378679266ac5157323158b6e52e7a884e559db5217037e57992e47a1667d525`  
		Last Modified: Fri, 14 Apr 2023 07:39:20 GMT  
		Size: 27.2 MB (27196396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fee697311c4e091f41acde237da003390953c6ecc286d893292b2dcd0c76821`  
		Last Modified: Tue, 18 Apr 2023 01:34:33 GMT  
		Size: 7.6 MB (7604657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c60e27a0516909c7200fcf3394a9e6e0d0e593249f51b70b05db3952b66592`  
		Last Modified: Tue, 18 Apr 2023 01:34:32 GMT  
		Size: 3.6 MB (3617029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d5ef789db5e2842d73302eede7f6b7a692bd35f3ee908d4039d7853bf8157a`  
		Last Modified: Tue, 18 Apr 2023 01:34:47 GMT  
		Size: 60.8 MB (60807001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:65ea078073458f501b145217e5ae0912024a6c3050c7fdfdb16c43f7167d7a5e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (116034160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49f7ad1554b25d8c56d16aeaaf445fac6e83b41fdbf9d30033f714ee0d2df88e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:36:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:36:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 00:38:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d276072145993a42aed3e2b3e8cd26b6e08aab266d9c9d792ee89b26150681da`  
		Last Modified: Fri, 14 Apr 2023 09:36:00 GMT  
		Size: 33.3 MB (33300980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:923459354bb7c8ed9378009c3b9bfafa2c71db0dd9434ff6f28fa8559018a9fe`  
		Last Modified: Tue, 18 Apr 2023 01:01:27 GMT  
		Size: 8.7 MB (8694604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14eb66e0ca52c6c0e9019cd99e5a7d12708b5fcf95d917cf1dcd06a56b91160`  
		Last Modified: Tue, 18 Apr 2023 01:01:26 GMT  
		Size: 4.5 MB (4486817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e714fae693c74669418568b2a270066a28e7e561eae1ff8896650c09e925c0e0`  
		Last Modified: Tue, 18 Apr 2023 01:02:00 GMT  
		Size: 69.6 MB (69551759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b49083c62ebe88b5f10ca6d6083a9c3a50544dedd323efcdd669678b796dfb89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (97960842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d473b3b8e44fa7c52afbd1368b9356f6d7fbfac2b9d6dffcd8d1054b1edf6f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:35 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:37 GMT
ADD file:44c66c03ba0afcc05de1b2078f83e8bfe04706b31491fcd3fdd93cfc88d5f06c in / 
# Thu, 13 Apr 2023 13:09:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:01:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:02:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:02:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f11b609b1d63f2d37c0e3789823e7a7e62a078bddca7c46da8602655989c62d9`  
		Last Modified: Fri, 14 Apr 2023 09:38:39 GMT  
		Size: 27.0 MB (27016370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfd953572ac96bfce6706f45014f76e59e53b096cdc8eba22ffc73112fa0b3c`  
		Last Modified: Tue, 18 Apr 2023 01:13:21 GMT  
		Size: 7.4 MB (7383689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc90d577c47f7094dda274dbf62b36e812018f84c10844be7715d198c95ddfef`  
		Last Modified: Tue, 18 Apr 2023 01:13:21 GMT  
		Size: 3.5 MB (3542231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a73d2f132bb961264ac78079104aeb71d832e93e48e8bc52edc4cb58ed80e5`  
		Last Modified: Tue, 18 Apr 2023 01:13:38 GMT  
		Size: 60.0 MB (60018552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:jammy`

```console
$ docker pull buildpack-deps@sha256:fe20c1a1fa7749ce93af04e56c2a46297e6b236eeddbdb8fd780ec58784c121a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:jammy` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c7af89fe20e8b370fa3d84c23f5dbb048e01cfd38fbc12c1e02232c1a84af80f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.0 MB (250022556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375da4bb35d8bd52aa3070617888fd8aea7a8aec9a99774cdd1df6a8a87cd5ca`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:29:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:29:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 05:29:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:32:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7490ba7e16ba382ca21015280e2ee6dad31879a1f043029e350a8e429770f36`  
		Last Modified: Thu, 16 Mar 2023 05:43:15 GMT  
		Size: 3.8 MB (3788671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eeb23ea57c359eecf9e21c40ddb69f738e9121008fd4956d733ba66d3b7eb38`  
		Last Modified: Thu, 16 Mar 2023 05:43:15 GMT  
		Size: 3.6 MB (3561600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6c00a0ea05e6a2089233e7238bbed0ffbf7b2655f03195967e2083ee623899`  
		Last Modified: Thu, 16 Mar 2023 05:43:30 GMT  
		Size: 39.4 MB (39352910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa902bb14f17725bbd311e77e44da0ef803e68e0965c5f95635eb83f288b5d4`  
		Last Modified: Thu, 16 Mar 2023 05:44:00 GMT  
		Size: 172.9 MB (172889412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:548a747004a966f5fe24d920b0b67a7e2f63d2f84ee8a998d73573f3534d291c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.7 MB (216673703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2805f8c5309daa5cfffe1813e3cf819142f1ed5ef4f8e6be329cbcad71c2d30`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:31:41 GMT
ADD file:e9c3ac290fb81ae2e78de99052d776396ee3aff05e1a66fd2dccb01d7de9bb45 in / 
# Wed, 08 Mar 2023 04:31:42 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:51:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:51:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 03:52:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:55:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cba1fa3bcdf4f746dcf5b8f86874cee4a6eff75dd5c5cd29e4c912574b12a1c6`  
		Last Modified: Thu, 09 Mar 2023 04:41:14 GMT  
		Size: 27.0 MB (27025397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff3d54aa809ca004a01d3a10bf7017a1fb216f185fd9d0f210f1bc9512298c1`  
		Last Modified: Thu, 16 Mar 2023 04:09:39 GMT  
		Size: 3.5 MB (3540124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caec72904127d7cb95dfd39a3f311865b026d929e1440427ec21122be6e15db3`  
		Last Modified: Thu, 16 Mar 2023 04:09:39 GMT  
		Size: 3.7 MB (3714418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b259dc20995aa828e48008def151ea3da6891615621976f66dc6b63fdbda38a`  
		Last Modified: Thu, 16 Mar 2023 04:09:57 GMT  
		Size: 41.9 MB (41908320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d21e83a1a0d8dfe0c0f53e1f8d51356e226e68eb9de5b136253db03ceac4e7`  
		Last Modified: Thu, 16 Mar 2023 04:10:26 GMT  
		Size: 140.5 MB (140485444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bc8bb348a53f7d9f3e309b375c7fd76b56a0c48f89c849a9c6ade599cdc8180a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 MB (241329007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ffb8e18683ff48d54f07c675683997a40a1555dde02c54147d8d9d48aa756df`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:32:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:32:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:32:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:32:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:32:40 GMT
ADD file:79b36308bc382d9cae7197b4cecc21430f4e8f3e8bec3547d0f00bcff7681e60 in / 
# Wed, 08 Mar 2023 04:32:41 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 04:07:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:08:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 04:08:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:11:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b2ddfd337773edbf5766dce2fdbeef139ba8c42724e29eda157c84e9f97f1bce`  
		Last Modified: Wed, 08 Mar 2023 12:37:24 GMT  
		Size: 28.4 MB (28387554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aef66b301cbfe4ff1bb09357ccf381140239a236438d27a992d076491a3a066`  
		Last Modified: Thu, 16 Mar 2023 04:23:23 GMT  
		Size: 3.8 MB (3760501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693278d975de74bdcb529fd46771b1335b9501b8f479a3c8128b69375f7945a8`  
		Last Modified: Thu, 16 Mar 2023 04:23:23 GMT  
		Size: 3.5 MB (3536190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bfc2e7bfd914b57fdeae1d187ca7a12534443f9e2a6142287dab73c0296ade8`  
		Last Modified: Thu, 16 Mar 2023 04:23:36 GMT  
		Size: 39.2 MB (39243621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2292b558961f2b5d5b6555b004730bdf51c7012b78b0a9474df76b1674aaa26`  
		Last Modified: Thu, 16 Mar 2023 04:24:01 GMT  
		Size: 166.4 MB (166401141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d098228e71918993c4063a767b2eef4e86f48651116a36ecd3b3faa15276d498
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271846871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55eaa1527dc94604178ceeb1d0dd71d0ef94cf7213d605391668aa27d2fb142e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:16 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:20 GMT
ADD file:d7434a52d8d8aa6288e788f6fe7e156f0e11bf9b8275efaf70aab0bfc4d919cf in / 
# Wed, 08 Mar 2023 04:39:20 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:23:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:23:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 03:24:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:29:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:deffc758660db3b0ee7a1f211d720633f06f27ab1e4c31db4caf8c27f4a80eeb`  
		Last Modified: Thu, 16 Mar 2023 02:22:27 GMT  
		Size: 35.7 MB (35711728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda6a81b65d142865ef5dbb2df2e98c084dc995272e55f804a36f283c6f9cc0a`  
		Last Modified: Thu, 16 Mar 2023 03:50:35 GMT  
		Size: 4.3 MB (4262063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ead6720a64b98a3aff60731463b608c0b67ecd6e1da5fdea16027f2602fed35`  
		Last Modified: Thu, 16 Mar 2023 03:50:35 GMT  
		Size: 4.2 MB (4234751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d902f277ddd72c79a705e87198d386aa6f00888bd94535ac236140f709bbdce`  
		Last Modified: Thu, 16 Mar 2023 03:50:57 GMT  
		Size: 43.8 MB (43768451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e52f20a783e0f77850e23839602213aca9d779491820b6b87d582377010ff1`  
		Last Modified: Thu, 16 Mar 2023 03:51:51 GMT  
		Size: 183.9 MB (183869878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d8f68fa9506203d2ae62c96ff52ca734da392b0abdf6fb87d0b095d32da75234
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.7 MB (223696064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:027fabc11727fa0a1d019f1c51338d85905a5113cdc2c03b8c1fbb1f2a852c17`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:24 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:26 GMT
ADD file:630f9865d3d4fd4294d45cac7cbaea83fb549c2e563de454348da964d19fbbba in / 
# Wed, 08 Mar 2023 04:39:26 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:49:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:49:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 01:50:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:52:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2c7366af510b72cc0b3456fb93cfa0bfc76f7d383db5cb315967e7b1ce2e0c42`  
		Last Modified: Thu, 16 Mar 2023 02:02:40 GMT  
		Size: 28.6 MB (28647599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfb18fcfcf98f525d6770606600d80d5413262ce3575995b49064988c1bd147`  
		Last Modified: Thu, 16 Mar 2023 02:02:37 GMT  
		Size: 3.8 MB (3792844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072af6d5dacbd70c88a5e91a5627fe4a95af544c4db1b250a263452128dc9cab`  
		Last Modified: Thu, 16 Mar 2023 02:02:37 GMT  
		Size: 3.5 MB (3472886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b80aecb29fcddae2ca64d4c31faa682b41b3206400c727d5eec25c7d83c8630`  
		Last Modified: Thu, 16 Mar 2023 02:02:54 GMT  
		Size: 39.3 MB (39284857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:277c8fbd8d44bf1475a44df6398ba9159c13423417cffb98f23824dca61b4a1d`  
		Last Modified: Thu, 16 Mar 2023 02:03:19 GMT  
		Size: 148.5 MB (148497878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:jammy-curl`

```console
$ docker pull buildpack-deps@sha256:1950ad34a10c685de875a9d2f586a239612590e033635f7ca3b07cd333c35d88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:jammy-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e1f00c6daf4cd328bbef9c52e6c60f18a47e5b716ef5a5d78542c90635025d20
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 MB (37780234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb7e40d800141c3758097d639c8f71da7d755a34a9ce59dabba14aac2a540ee`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:29:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:29:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7490ba7e16ba382ca21015280e2ee6dad31879a1f043029e350a8e429770f36`  
		Last Modified: Thu, 16 Mar 2023 05:43:15 GMT  
		Size: 3.8 MB (3788671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eeb23ea57c359eecf9e21c40ddb69f738e9121008fd4956d733ba66d3b7eb38`  
		Last Modified: Thu, 16 Mar 2023 05:43:15 GMT  
		Size: 3.6 MB (3561600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d14e02d71154d77fa15e8fe99c09399a29cf9cd6a168b06bf6cfdc6cbdd98960
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34279939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831a4c6176514fb8d4452ddac355efa1a3da26e98087da273d6c3bcc34ba38e1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:31:41 GMT
ADD file:e9c3ac290fb81ae2e78de99052d776396ee3aff05e1a66fd2dccb01d7de9bb45 in / 
# Wed, 08 Mar 2023 04:31:42 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:51:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:51:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:cba1fa3bcdf4f746dcf5b8f86874cee4a6eff75dd5c5cd29e4c912574b12a1c6`  
		Last Modified: Thu, 09 Mar 2023 04:41:14 GMT  
		Size: 27.0 MB (27025397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff3d54aa809ca004a01d3a10bf7017a1fb216f185fd9d0f210f1bc9512298c1`  
		Last Modified: Thu, 16 Mar 2023 04:09:39 GMT  
		Size: 3.5 MB (3540124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caec72904127d7cb95dfd39a3f311865b026d929e1440427ec21122be6e15db3`  
		Last Modified: Thu, 16 Mar 2023 04:09:39 GMT  
		Size: 3.7 MB (3714418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:fa825f78772b21eb6d058d2d80e48ded564c870a66ec077b8219225d6f515c2c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35684245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd233dec7831ce72a921837b590af2d1f8f8d87f1b119fae78edba2ea730316`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:32:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:32:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:32:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:32:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:32:40 GMT
ADD file:79b36308bc382d9cae7197b4cecc21430f4e8f3e8bec3547d0f00bcff7681e60 in / 
# Wed, 08 Mar 2023 04:32:41 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 04:07:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:08:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b2ddfd337773edbf5766dce2fdbeef139ba8c42724e29eda157c84e9f97f1bce`  
		Last Modified: Wed, 08 Mar 2023 12:37:24 GMT  
		Size: 28.4 MB (28387554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aef66b301cbfe4ff1bb09357ccf381140239a236438d27a992d076491a3a066`  
		Last Modified: Thu, 16 Mar 2023 04:23:23 GMT  
		Size: 3.8 MB (3760501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693278d975de74bdcb529fd46771b1335b9501b8f479a3c8128b69375f7945a8`  
		Last Modified: Thu, 16 Mar 2023 04:23:23 GMT  
		Size: 3.5 MB (3536190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:057ed8d3115324cc3a7cbde4dad9bc42768a3cfeeb98aa5a2342d57a704ea2b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44208542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d825634c6ab1942263dbe9f71d6b27d39b833fb4013c32ad433760b35351762d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:16 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:20 GMT
ADD file:d7434a52d8d8aa6288e788f6fe7e156f0e11bf9b8275efaf70aab0bfc4d919cf in / 
# Wed, 08 Mar 2023 04:39:20 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:23:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:23:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:deffc758660db3b0ee7a1f211d720633f06f27ab1e4c31db4caf8c27f4a80eeb`  
		Last Modified: Thu, 16 Mar 2023 02:22:27 GMT  
		Size: 35.7 MB (35711728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda6a81b65d142865ef5dbb2df2e98c084dc995272e55f804a36f283c6f9cc0a`  
		Last Modified: Thu, 16 Mar 2023 03:50:35 GMT  
		Size: 4.3 MB (4262063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ead6720a64b98a3aff60731463b608c0b67ecd6e1da5fdea16027f2602fed35`  
		Last Modified: Thu, 16 Mar 2023 03:50:35 GMT  
		Size: 4.2 MB (4234751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b22525cdcb82e2ef5355054b43872f265a7e983b5de76a9606921cde9d74b610
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 MB (35913329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a514140debee8dd2b4218d8d1975fc7b1e4623707f2083cffa6cdbd3f7e11228`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:24 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:26 GMT
ADD file:630f9865d3d4fd4294d45cac7cbaea83fb549c2e563de454348da964d19fbbba in / 
# Wed, 08 Mar 2023 04:39:26 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:49:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:49:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2c7366af510b72cc0b3456fb93cfa0bfc76f7d383db5cb315967e7b1ce2e0c42`  
		Last Modified: Thu, 16 Mar 2023 02:02:40 GMT  
		Size: 28.6 MB (28647599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfb18fcfcf98f525d6770606600d80d5413262ce3575995b49064988c1bd147`  
		Last Modified: Thu, 16 Mar 2023 02:02:37 GMT  
		Size: 3.8 MB (3792844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072af6d5dacbd70c88a5e91a5627fe4a95af544c4db1b250a263452128dc9cab`  
		Last Modified: Thu, 16 Mar 2023 02:02:37 GMT  
		Size: 3.5 MB (3472886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:jammy-scm`

```console
$ docker pull buildpack-deps@sha256:79b0f9319ebb640493eaf8539641f9fc67a08f10ec5fc2f8a7d9a447fd786055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:jammy-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f34fd3d1a17609e88da35bc2a959ddd09a4cff838e251132a6a4551b7f710a8e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77133144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9805e59e9e583a30a563cbac116296ba8acf152f10fabcbecc2d3f99f8b6ab`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 05:29:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 05:29:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 05:29:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7490ba7e16ba382ca21015280e2ee6dad31879a1f043029e350a8e429770f36`  
		Last Modified: Thu, 16 Mar 2023 05:43:15 GMT  
		Size: 3.8 MB (3788671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eeb23ea57c359eecf9e21c40ddb69f738e9121008fd4956d733ba66d3b7eb38`  
		Last Modified: Thu, 16 Mar 2023 05:43:15 GMT  
		Size: 3.6 MB (3561600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6c00a0ea05e6a2089233e7238bbed0ffbf7b2655f03195967e2083ee623899`  
		Last Modified: Thu, 16 Mar 2023 05:43:30 GMT  
		Size: 39.4 MB (39352910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8249c9a5f7475ad02f242ade08a27052609481d8cd35ae4089fa7ecb14295c45
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76188259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7c6edcb5acd77a3e2b70af5afcda9bef5dcb2ee9c21e24297ee96426322b6e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:31:41 GMT
ADD file:e9c3ac290fb81ae2e78de99052d776396ee3aff05e1a66fd2dccb01d7de9bb45 in / 
# Wed, 08 Mar 2023 04:31:42 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:51:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:51:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 03:52:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cba1fa3bcdf4f746dcf5b8f86874cee4a6eff75dd5c5cd29e4c912574b12a1c6`  
		Last Modified: Thu, 09 Mar 2023 04:41:14 GMT  
		Size: 27.0 MB (27025397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff3d54aa809ca004a01d3a10bf7017a1fb216f185fd9d0f210f1bc9512298c1`  
		Last Modified: Thu, 16 Mar 2023 04:09:39 GMT  
		Size: 3.5 MB (3540124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caec72904127d7cb95dfd39a3f311865b026d929e1440427ec21122be6e15db3`  
		Last Modified: Thu, 16 Mar 2023 04:09:39 GMT  
		Size: 3.7 MB (3714418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b259dc20995aa828e48008def151ea3da6891615621976f66dc6b63fdbda38a`  
		Last Modified: Thu, 16 Mar 2023 04:09:57 GMT  
		Size: 41.9 MB (41908320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6857aefe9fc47abf0d2d28e21e046b63e6be875de53f2b1fd49dea88192e4560
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74927866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca9591d5aa5d0b25f21dfa798fa26b330206f083d8ca36701124b4a875b6c2c4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:32:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:32:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:32:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:32:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:32:40 GMT
ADD file:79b36308bc382d9cae7197b4cecc21430f4e8f3e8bec3547d0f00bcff7681e60 in / 
# Wed, 08 Mar 2023 04:32:41 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 04:07:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:08:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 04:08:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b2ddfd337773edbf5766dce2fdbeef139ba8c42724e29eda157c84e9f97f1bce`  
		Last Modified: Wed, 08 Mar 2023 12:37:24 GMT  
		Size: 28.4 MB (28387554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aef66b301cbfe4ff1bb09357ccf381140239a236438d27a992d076491a3a066`  
		Last Modified: Thu, 16 Mar 2023 04:23:23 GMT  
		Size: 3.8 MB (3760501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693278d975de74bdcb529fd46771b1335b9501b8f479a3c8128b69375f7945a8`  
		Last Modified: Thu, 16 Mar 2023 04:23:23 GMT  
		Size: 3.5 MB (3536190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bfc2e7bfd914b57fdeae1d187ca7a12534443f9e2a6142287dab73c0296ade8`  
		Last Modified: Thu, 16 Mar 2023 04:23:36 GMT  
		Size: 39.2 MB (39243621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d8da9e38d3c74aa25f5da85d9e692795099198656dfb38ba3058d5cc1c3284d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 MB (87976993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a899652169ee26f65829047e0799b9409330896911f49369b3b425b1315c02b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:16 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:20 GMT
ADD file:d7434a52d8d8aa6288e788f6fe7e156f0e11bf9b8275efaf70aab0bfc4d919cf in / 
# Wed, 08 Mar 2023 04:39:20 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:23:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:23:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 03:24:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:deffc758660db3b0ee7a1f211d720633f06f27ab1e4c31db4caf8c27f4a80eeb`  
		Last Modified: Thu, 16 Mar 2023 02:22:27 GMT  
		Size: 35.7 MB (35711728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda6a81b65d142865ef5dbb2df2e98c084dc995272e55f804a36f283c6f9cc0a`  
		Last Modified: Thu, 16 Mar 2023 03:50:35 GMT  
		Size: 4.3 MB (4262063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ead6720a64b98a3aff60731463b608c0b67ecd6e1da5fdea16027f2602fed35`  
		Last Modified: Thu, 16 Mar 2023 03:50:35 GMT  
		Size: 4.2 MB (4234751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d902f277ddd72c79a705e87198d386aa6f00888bd94535ac236140f709bbdce`  
		Last Modified: Thu, 16 Mar 2023 03:50:57 GMT  
		Size: 43.8 MB (43768451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9b906aa81cc60290a664f0ff6bcb0f491cac7dd31f6cc7fbb73f4f2823d84ca0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75198186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:accf40ea7a4019526a1b76f2c48458f738926fa6bb6f285ca24c9c03b98771ed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:24 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:26 GMT
ADD file:630f9865d3d4fd4294d45cac7cbaea83fb549c2e563de454348da964d19fbbba in / 
# Wed, 08 Mar 2023 04:39:26 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:49:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:49:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Mar 2023 01:50:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2c7366af510b72cc0b3456fb93cfa0bfc76f7d383db5cb315967e7b1ce2e0c42`  
		Last Modified: Thu, 16 Mar 2023 02:02:40 GMT  
		Size: 28.6 MB (28647599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfb18fcfcf98f525d6770606600d80d5413262ce3575995b49064988c1bd147`  
		Last Modified: Thu, 16 Mar 2023 02:02:37 GMT  
		Size: 3.8 MB (3792844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072af6d5dacbd70c88a5e91a5627fe4a95af544c4db1b250a263452128dc9cab`  
		Last Modified: Thu, 16 Mar 2023 02:02:37 GMT  
		Size: 3.5 MB (3472886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b80aecb29fcddae2ca64d4c31faa682b41b3206400c727d5eec25c7d83c8630`  
		Last Modified: Thu, 16 Mar 2023 02:02:54 GMT  
		Size: 39.3 MB (39284857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:kinetic`

```console
$ docker pull buildpack-deps@sha256:1de863c96612a1ba170ad856067a4785d1c48157c2a20b86a0fa43d66099ac20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:kinetic` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:47a4169bc938bbd93194b81c05ebde3ce8761cfb50f556bc891e8d3127139a9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.8 MB (258757659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa2be6aefd392ae2d26ec97c171529a285f6e7ad875a5b19149f0121627a521d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:03:38 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:03:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:03:39 GMT
ADD file:ba742ddbebcc8282f5094275969bfb2ff4b2973e385c198b6897bea2a9cb4b85 in / 
# Thu, 13 Apr 2023 13:03:39 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:26:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:26:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:27:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:30:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:318b284d262b8726296dca98d01be71ddfad412c987a7ecec4db3278eef82188`  
		Last Modified: Fri, 14 Apr 2023 09:51:30 GMT  
		Size: 27.5 MB (27482065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a21382eec6e41b44d6c1e3ab5faaf936e33dfa42e25ce3b71ba5bee3dc3352`  
		Last Modified: Tue, 18 Apr 2023 01:35:37 GMT  
		Size: 6.8 MB (6774413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72965a2f51dc0d93d80a13692ed731534afdf361dfbabdd2da5b4ff69faeab0b`  
		Last Modified: Tue, 18 Apr 2023 01:35:36 GMT  
		Size: 3.6 MB (3635395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e29d10ebe6980c4a950b493f7124babae9418113f9b240e5bd9d4eacfb7162`  
		Last Modified: Tue, 18 Apr 2023 01:35:53 GMT  
		Size: 39.7 MB (39739228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6054ae3e51fffb85a5c75e32dfddc8412f3afafeb95561d3259bdbce227ad5f5`  
		Last Modified: Tue, 18 Apr 2023 01:36:24 GMT  
		Size: 181.1 MB (181126558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:035179436aed59c0c83db5632b9f6dbb7e8670ca49b317e341118be400ba4324
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221883309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af7580b578b34f3ffbcfa3fb65851e9ba09187d501c8e45611bba3c8586aee6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:51 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:52 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:10:01 GMT
ADD file:7c943de57b75e515f072a13706b12ee97f17d22a120991f8effbc0615c544253 in / 
# Thu, 13 Apr 2023 13:10:02 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:39:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:40:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:44:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f98d8e30b5bcedb55e832c340c4accb90ea3b5319d99dd02667d1ae133fe0f01`  
		Last Modified: Fri, 14 Apr 2023 09:55:43 GMT  
		Size: 25.9 MB (25891251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d51b5e66e30d2da337764807887bf782dbee472da4c68d5d639f11675c2b227`  
		Last Modified: Tue, 18 Apr 2023 01:50:18 GMT  
		Size: 5.9 MB (5947326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ebf5377710c036b1bad928498ea4e024c30e8f182174cd7a1a5a982218e210`  
		Last Modified: Tue, 18 Apr 2023 01:50:17 GMT  
		Size: 3.8 MB (3801747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7d2e4eec630d9a9b5faa00fb07be6af7f2c4e2a54c97ea8cc1822bbb2447c8`  
		Last Modified: Tue, 18 Apr 2023 01:50:35 GMT  
		Size: 42.6 MB (42613117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a37aaa3caa5861bbeba27ff23967333f6181d66435f89cade2586a061ba7af`  
		Last Modified: Tue, 18 Apr 2023 01:51:03 GMT  
		Size: 143.6 MB (143629868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f15bbe544c8596ce66173fc4e4e595cdad287cd19b75b0ecb90a17207003bf28
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246726292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e9ba4ebb965e3b2baafaec5093d051d5c0ac17fa0db69a7eba6757db44402e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:37 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:37 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:20:38 GMT
ADD file:8b5c9a166ff42d52b423d188428558ea2bf225c42aeb3de339514e6ad9fdd504 in / 
# Thu, 13 Apr 2023 13:20:39 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:24:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:24:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:25:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:29:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:479b8cd2e9c97aa9b4eb9d8070207c8b64f471b3ec6bb582c7b09dacb55735a2`  
		Last Modified: Fri, 14 Apr 2023 09:53:52 GMT  
		Size: 26.7 MB (26702173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a211e249366d1e9c621cfbb98a45087c7ca76b4539f9bc7d9068b701a8054585`  
		Last Modified: Tue, 18 Apr 2023 01:35:19 GMT  
		Size: 6.6 MB (6604111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd99e3413cacb724e75738256d7ae34f43ccb93122964be0ea699ffcc780ae6d`  
		Last Modified: Tue, 18 Apr 2023 01:35:19 GMT  
		Size: 3.6 MB (3603384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee999b3c3995eddaf919a60db441654b53a3390af8730f1b0a438577ec230068`  
		Last Modified: Tue, 18 Apr 2023 01:35:35 GMT  
		Size: 39.5 MB (39512803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c32c97453084fb79cd6834efc8143004eb54df5b273f0ee5de88d2e2ca20c3`  
		Last Modified: Tue, 18 Apr 2023 01:36:00 GMT  
		Size: 170.3 MB (170303821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d7f5050ebc5dd34d23a84c1079856e93173b6d6b70fd3c9f40520a44a65b4e70
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281324046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369d2dd6eb5633076e9b5ea2f1fc56834446018606b3738c523d5f9dadae0947`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:21:42 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:21:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:21:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:21:43 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:21:45 GMT
ADD file:2f24914c3a2e66342aa7cf589af143b01a1cd7532c92c4263d251fb826b8b810 in / 
# Thu, 13 Apr 2023 13:21:46 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:45:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:46:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 00:47:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:53:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3b2b861f7bcaef2d589c1d8518a14da93644aafdcc9bfc5554895ed342bc341c`  
		Last Modified: Fri, 14 Apr 2023 09:57:14 GMT  
		Size: 32.1 MB (32098609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978ddb6b21e3fea6c8cb5970d8cd307a6ec15ef6b639b994cfdebe9384ef6e24`  
		Last Modified: Tue, 18 Apr 2023 01:03:02 GMT  
		Size: 7.8 MB (7751781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54556acf1bc962b10d66a29a9198cf3876dbc10be5d5899d89ee4ee01770250e`  
		Last Modified: Tue, 18 Apr 2023 01:03:01 GMT  
		Size: 4.4 MB (4362837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4db88fb9e9071e75f6c65177600cda26da9887d2574f51858808a6973fb9252`  
		Last Modified: Tue, 18 Apr 2023 01:03:29 GMT  
		Size: 44.1 MB (44147073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d215be67ce556d3fdbd64f14d10e6426bf36fb6035ba527939c1614d3d8dade0`  
		Last Modified: Tue, 18 Apr 2023 01:04:25 GMT  
		Size: 193.0 MB (192963746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:addc2e3ff7a25e8fae18b569593daa21e377dd047158af082341ca3d5249c9b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228647799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebe59ba4464149ed91005f254898908afda7a4d0ad989503cc2415bef2a1847`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:08:08 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:08:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:08:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:08:08 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:08:09 GMT
ADD file:df5733230d0258ecd0cbdcc7c2075865bc335200f2cafee8dacccfd082710b96 in / 
# Thu, 13 Apr 2023 13:08:10 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:05:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:06:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:06:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:08:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c450971bf0fd92eac91caf0b3126482e5fecadead22e59da08f9661a4b4f03be`  
		Last Modified: Fri, 14 Apr 2023 10:00:19 GMT  
		Size: 26.0 MB (26029287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded2cd498871df7ac556305ff379ade5376ed441cad7f51cf98b4867ac750d39`  
		Last Modified: Tue, 18 Apr 2023 01:14:11 GMT  
		Size: 6.5 MB (6467769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5cee9d25bba89e9b965d2fee1419c9d544d12c148be50fd20849d7f808bde1`  
		Last Modified: Tue, 18 Apr 2023 01:14:10 GMT  
		Size: 3.6 MB (3625375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36304f69d4e520034a19fbb9f1da633dd4722e9cdc720512923f71d850cc07d5`  
		Last Modified: Tue, 18 Apr 2023 01:14:24 GMT  
		Size: 39.6 MB (39564578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a4c7f51941a2d297df128b432e31b25677e7e42ba0d57b82603461c4244e87`  
		Last Modified: Tue, 18 Apr 2023 01:14:48 GMT  
		Size: 153.0 MB (152960790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:kinetic-curl`

```console
$ docker pull buildpack-deps@sha256:070458606dbc997307494bb256f2e0b9f5e9ceed956f38d8ad1951239e6e7015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:kinetic-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e2baef48d968cfb8eaa239e989fe2f8fa6dc82e8cdb6992d928a7af7e7b97698
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37891873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b717cacdac4c1a10af86a1162d9c8fd0db43b12a5aa661a257dad5328881196`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:03:38 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:03:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:03:39 GMT
ADD file:ba742ddbebcc8282f5094275969bfb2ff4b2973e385c198b6897bea2a9cb4b85 in / 
# Thu, 13 Apr 2023 13:03:39 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:26:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:26:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:318b284d262b8726296dca98d01be71ddfad412c987a7ecec4db3278eef82188`  
		Last Modified: Fri, 14 Apr 2023 09:51:30 GMT  
		Size: 27.5 MB (27482065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a21382eec6e41b44d6c1e3ab5faaf936e33dfa42e25ce3b71ba5bee3dc3352`  
		Last Modified: Tue, 18 Apr 2023 01:35:37 GMT  
		Size: 6.8 MB (6774413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72965a2f51dc0d93d80a13692ed731534afdf361dfbabdd2da5b4ff69faeab0b`  
		Last Modified: Tue, 18 Apr 2023 01:35:36 GMT  
		Size: 3.6 MB (3635395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c855f3091d5cd8f298812ef20659893606ad3decf412e045c3baf00844f4c0f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 MB (35640324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93ceadf349fadae92f8b50df62219bf931bb7754516e96a10c2fb6c7d6c89221`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:51 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:52 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:10:01 GMT
ADD file:7c943de57b75e515f072a13706b12ee97f17d22a120991f8effbc0615c544253 in / 
# Thu, 13 Apr 2023 13:10:02 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:39:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:f98d8e30b5bcedb55e832c340c4accb90ea3b5319d99dd02667d1ae133fe0f01`  
		Last Modified: Fri, 14 Apr 2023 09:55:43 GMT  
		Size: 25.9 MB (25891251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d51b5e66e30d2da337764807887bf782dbee472da4c68d5d639f11675c2b227`  
		Last Modified: Tue, 18 Apr 2023 01:50:18 GMT  
		Size: 5.9 MB (5947326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ebf5377710c036b1bad928498ea4e024c30e8f182174cd7a1a5a982218e210`  
		Last Modified: Tue, 18 Apr 2023 01:50:17 GMT  
		Size: 3.8 MB (3801747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3c54974fca8d55cc2aae0bf59aaf13d1492ee8fab8fc7afc6758ca10a9901bc7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36909668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8f78b7034cdd7b9e8c7a44a1c482fb47fc143533f941369a3d0387c98fd411`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:37 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:37 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:20:38 GMT
ADD file:8b5c9a166ff42d52b423d188428558ea2bf225c42aeb3de339514e6ad9fdd504 in / 
# Thu, 13 Apr 2023 13:20:39 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:24:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:24:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:479b8cd2e9c97aa9b4eb9d8070207c8b64f471b3ec6bb582c7b09dacb55735a2`  
		Last Modified: Fri, 14 Apr 2023 09:53:52 GMT  
		Size: 26.7 MB (26702173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a211e249366d1e9c621cfbb98a45087c7ca76b4539f9bc7d9068b701a8054585`  
		Last Modified: Tue, 18 Apr 2023 01:35:19 GMT  
		Size: 6.6 MB (6604111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd99e3413cacb724e75738256d7ae34f43ccb93122964be0ea699ffcc780ae6d`  
		Last Modified: Tue, 18 Apr 2023 01:35:19 GMT  
		Size: 3.6 MB (3603384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a173db92e12ea4bc7ab8861dc75b1d01163b4169bf587bcbdf056ceceef84f9b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44213227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa7da5a02e3ed5cc84aef25afdec00f9462f210848b3903b605466dcbf679da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:21:42 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:21:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:21:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:21:43 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:21:45 GMT
ADD file:2f24914c3a2e66342aa7cf589af143b01a1cd7532c92c4263d251fb826b8b810 in / 
# Thu, 13 Apr 2023 13:21:46 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:45:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:46:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3b2b861f7bcaef2d589c1d8518a14da93644aafdcc9bfc5554895ed342bc341c`  
		Last Modified: Fri, 14 Apr 2023 09:57:14 GMT  
		Size: 32.1 MB (32098609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978ddb6b21e3fea6c8cb5970d8cd307a6ec15ef6b639b994cfdebe9384ef6e24`  
		Last Modified: Tue, 18 Apr 2023 01:03:02 GMT  
		Size: 7.8 MB (7751781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54556acf1bc962b10d66a29a9198cf3876dbc10be5d5899d89ee4ee01770250e`  
		Last Modified: Tue, 18 Apr 2023 01:03:01 GMT  
		Size: 4.4 MB (4362837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a9a30abdb96a71c9bfe40e06305587f2453f48e6826253c2346f68c867918c49
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36122431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d179c68254fd9641c116296236caf4426c7b9a75a4eef7ff30749528c41b419`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:08:08 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:08:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:08:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:08:08 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:08:09 GMT
ADD file:df5733230d0258ecd0cbdcc7c2075865bc335200f2cafee8dacccfd082710b96 in / 
# Thu, 13 Apr 2023 13:08:10 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:05:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:06:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:c450971bf0fd92eac91caf0b3126482e5fecadead22e59da08f9661a4b4f03be`  
		Last Modified: Fri, 14 Apr 2023 10:00:19 GMT  
		Size: 26.0 MB (26029287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded2cd498871df7ac556305ff379ade5376ed441cad7f51cf98b4867ac750d39`  
		Last Modified: Tue, 18 Apr 2023 01:14:11 GMT  
		Size: 6.5 MB (6467769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5cee9d25bba89e9b965d2fee1419c9d544d12c148be50fd20849d7f808bde1`  
		Last Modified: Tue, 18 Apr 2023 01:14:10 GMT  
		Size: 3.6 MB (3625375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:kinetic-scm`

```console
$ docker pull buildpack-deps@sha256:9121f3d8acb4f1325a22fc4e4ee0f6fa0942195663d4177200cb4a93170f0d3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:kinetic-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:6cefb88899f6601cbdc537665bce2f7653e8668d18af7822325c5686361be75c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77631101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba075d897f5e029a7aca18b815d2b01d1c74b1ba28a99b4f2956c3f74e46aed6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:03:38 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:03:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:03:39 GMT
ADD file:ba742ddbebcc8282f5094275969bfb2ff4b2973e385c198b6897bea2a9cb4b85 in / 
# Thu, 13 Apr 2023 13:03:39 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:26:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:26:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:27:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:318b284d262b8726296dca98d01be71ddfad412c987a7ecec4db3278eef82188`  
		Last Modified: Fri, 14 Apr 2023 09:51:30 GMT  
		Size: 27.5 MB (27482065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a21382eec6e41b44d6c1e3ab5faaf936e33dfa42e25ce3b71ba5bee3dc3352`  
		Last Modified: Tue, 18 Apr 2023 01:35:37 GMT  
		Size: 6.8 MB (6774413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72965a2f51dc0d93d80a13692ed731534afdf361dfbabdd2da5b4ff69faeab0b`  
		Last Modified: Tue, 18 Apr 2023 01:35:36 GMT  
		Size: 3.6 MB (3635395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e29d10ebe6980c4a950b493f7124babae9418113f9b240e5bd9d4eacfb7162`  
		Last Modified: Tue, 18 Apr 2023 01:35:53 GMT  
		Size: 39.7 MB (39739228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:67774d150a60cdea71df4fa5c89c73e76fdb497221591402019183488e37a818
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78253441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5be701f11a06844f2e3d9caf98e515b72b789382e8713d49d572ec08d3583316`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:51 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:52 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:10:01 GMT
ADD file:7c943de57b75e515f072a13706b12ee97f17d22a120991f8effbc0615c544253 in / 
# Thu, 13 Apr 2023 13:10:02 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:39:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:40:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f98d8e30b5bcedb55e832c340c4accb90ea3b5319d99dd02667d1ae133fe0f01`  
		Last Modified: Fri, 14 Apr 2023 09:55:43 GMT  
		Size: 25.9 MB (25891251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d51b5e66e30d2da337764807887bf782dbee472da4c68d5d639f11675c2b227`  
		Last Modified: Tue, 18 Apr 2023 01:50:18 GMT  
		Size: 5.9 MB (5947326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ebf5377710c036b1bad928498ea4e024c30e8f182174cd7a1a5a982218e210`  
		Last Modified: Tue, 18 Apr 2023 01:50:17 GMT  
		Size: 3.8 MB (3801747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7d2e4eec630d9a9b5faa00fb07be6af7f2c4e2a54c97ea8cc1822bbb2447c8`  
		Last Modified: Tue, 18 Apr 2023 01:50:35 GMT  
		Size: 42.6 MB (42613117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:87bda58def49dc9de7b321934e261d639446fbd2f0e7b72e39629f25cf6d2406
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76422471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b214eb7217e5d32bda0460644803e68d09cd216aae2a1b6df4aaacdad4a79e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:37 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:37 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:20:38 GMT
ADD file:8b5c9a166ff42d52b423d188428558ea2bf225c42aeb3de339514e6ad9fdd504 in / 
# Thu, 13 Apr 2023 13:20:39 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:24:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:24:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:25:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:479b8cd2e9c97aa9b4eb9d8070207c8b64f471b3ec6bb582c7b09dacb55735a2`  
		Last Modified: Fri, 14 Apr 2023 09:53:52 GMT  
		Size: 26.7 MB (26702173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a211e249366d1e9c621cfbb98a45087c7ca76b4539f9bc7d9068b701a8054585`  
		Last Modified: Tue, 18 Apr 2023 01:35:19 GMT  
		Size: 6.6 MB (6604111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd99e3413cacb724e75738256d7ae34f43ccb93122964be0ea699ffcc780ae6d`  
		Last Modified: Tue, 18 Apr 2023 01:35:19 GMT  
		Size: 3.6 MB (3603384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee999b3c3995eddaf919a60db441654b53a3390af8730f1b0a438577ec230068`  
		Last Modified: Tue, 18 Apr 2023 01:35:35 GMT  
		Size: 39.5 MB (39512803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8950cc9fc07e29fd9573ee916ff1e1e20a87ce63a3ce582471e7e7068d50417c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88360300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed0a57ba28d358bb99ed050b777f48faba8b19a18596c84507171a953dd5c76b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:21:42 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:21:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:21:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:21:43 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:21:45 GMT
ADD file:2f24914c3a2e66342aa7cf589af143b01a1cd7532c92c4263d251fb826b8b810 in / 
# Thu, 13 Apr 2023 13:21:46 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:45:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:46:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 00:47:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3b2b861f7bcaef2d589c1d8518a14da93644aafdcc9bfc5554895ed342bc341c`  
		Last Modified: Fri, 14 Apr 2023 09:57:14 GMT  
		Size: 32.1 MB (32098609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978ddb6b21e3fea6c8cb5970d8cd307a6ec15ef6b639b994cfdebe9384ef6e24`  
		Last Modified: Tue, 18 Apr 2023 01:03:02 GMT  
		Size: 7.8 MB (7751781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54556acf1bc962b10d66a29a9198cf3876dbc10be5d5899d89ee4ee01770250e`  
		Last Modified: Tue, 18 Apr 2023 01:03:01 GMT  
		Size: 4.4 MB (4362837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4db88fb9e9071e75f6c65177600cda26da9887d2574f51858808a6973fb9252`  
		Last Modified: Tue, 18 Apr 2023 01:03:29 GMT  
		Size: 44.1 MB (44147073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:99ca92b8905a1d95dfc35c299d441b4a1858d2538f1694510683b0320824beb9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75687009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637c9d75ac5352b4cbf7abcd1bf489b99d3901a9d7e6c435d32b9b2e5c820806`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:08:08 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:08:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:08:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:08:08 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:08:09 GMT
ADD file:df5733230d0258ecd0cbdcc7c2075865bc335200f2cafee8dacccfd082710b96 in / 
# Thu, 13 Apr 2023 13:08:10 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:05:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:06:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:06:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c450971bf0fd92eac91caf0b3126482e5fecadead22e59da08f9661a4b4f03be`  
		Last Modified: Fri, 14 Apr 2023 10:00:19 GMT  
		Size: 26.0 MB (26029287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded2cd498871df7ac556305ff379ade5376ed441cad7f51cf98b4867ac750d39`  
		Last Modified: Tue, 18 Apr 2023 01:14:11 GMT  
		Size: 6.5 MB (6467769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5cee9d25bba89e9b965d2fee1419c9d544d12c148be50fd20849d7f808bde1`  
		Last Modified: Tue, 18 Apr 2023 01:14:10 GMT  
		Size: 3.6 MB (3625375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36304f69d4e520034a19fbb9f1da633dd4722e9cdc720512923f71d850cc07d5`  
		Last Modified: Tue, 18 Apr 2023 01:14:24 GMT  
		Size: 39.6 MB (39564578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:latest`

```console
$ docker pull buildpack-deps@sha256:695fd9e1f58574422eece085006690b3110abb0d304260024d40775b95c6056e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:latest` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4156d4c78d3e29a9aa11a5528a08847352e66895bb0a75cec05f4d43752fb8f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.5 MB (322492485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09bd8b383fcae8260115c949f68a3ccbe1df72567c4e1ad6f53b72329c1c5e1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:55 GMT
ADD file:f2d012660f882f319a5878a3f9ce285f488b8f90fad49ad238541cf72089e035 in / 
# Wed, 12 Apr 2023 00:19:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:50:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:51:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 07:51:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:52:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0248cf3e63c73d0e496a67807d056ca41d5e968b61087e8eca2cf4b9b4d7b99`  
		Last Modified: Wed, 12 Apr 2023 00:23:20 GMT  
		Size: 55.1 MB (55052736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127e97b4daf784e08840a21765f0d4f251192ef2994d0e4a253490f81e63955b`  
		Last Modified: Wed, 12 Apr 2023 07:57:29 GMT  
		Size: 5.2 MB (5166696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0336c50c9f6942b660e433b1086238eec37057c34b14c4e3b28bd7bf05bd84ba`  
		Last Modified: Wed, 12 Apr 2023 07:57:29 GMT  
		Size: 10.9 MB (10876749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b89f3c7f7da8adf032a33a75d1b659cee33179ecb88ea0ba75e4fc58ebe63a6`  
		Last Modified: Wed, 12 Apr 2023 07:57:46 GMT  
		Size: 54.6 MB (54584801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d62772179761f8fddfaed03ed2bdf7078b103b193d18d79a9b49364830d56cf`  
		Last Modified: Wed, 12 Apr 2023 07:58:19 GMT  
		Size: 196.8 MB (196811503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:5307e4d5147eb64f430d2a521eee4a5504ed8c4a0d7d98aa81c28190c2c963d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.6 MB (295551904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62bc4c385631ea22e58568f3c02e7102b4f9f8f5a1ebb96d7e82bf8764dbecae`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:48:34 GMT
ADD file:ae13a4cbeb20b92ec29dd7409de47a964fe373bdde2a4e8880b5a4d9dc64171e in / 
# Wed, 12 Apr 2023 00:48:35 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:15:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:15:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:16:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:17:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:86cb8d774eca43d428d6a35506c172ba62358d2d5ec90c886e3b38b297f93b20`  
		Last Modified: Wed, 12 Apr 2023 00:50:46 GMT  
		Size: 52.6 MB (52555175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49db155cdf8645f599affcbbbc75eb928b0a9d010c4ac54afcfa9d7e4fa85e0`  
		Last Modified: Wed, 12 Apr 2023 01:21:15 GMT  
		Size: 5.1 MB (5072827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8936087cbd048148575fda58348506149db80a2699e99ae2042086628c0e5a38`  
		Last Modified: Wed, 12 Apr 2023 01:21:16 GMT  
		Size: 10.6 MB (10573853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0bf11569c39ee4f3d8515112046a55f14f39e54c6f0ea26271033c090f77d2`  
		Last Modified: Wed, 12 Apr 2023 01:21:35 GMT  
		Size: 52.3 MB (52340617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:622390f39404d88752f248bc2136a55baca97d5324d43689204df0157d284282`  
		Last Modified: Wed, 12 Apr 2023 01:22:13 GMT  
		Size: 175.0 MB (175009432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:14544dda30d13c761bb7bfb4d7fdffb2d3abd01a303373a2bcb846940b12680d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (283013417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f5b3339637b4c0d3912ef6cd818266179b085a40521f419e38c9546b616ee3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:35 GMT
ADD file:75c57df33c95251a80549b7949853df282a42bc4e5f19176764907a54b74caa9 in / 
# Tue, 11 Apr 2023 23:59:36 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:35:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:35:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:37:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4feff9b88735325634445419eaaec2ed47500b63027cfd2de34b8bc6d55ee85c`  
		Last Modified: Wed, 12 Apr 2023 00:02:57 GMT  
		Size: 50.2 MB (50216882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5f77534be142d18fb6441aad5ebb0a6b1fbd1128fee964f14c772d3f48978f`  
		Last Modified: Wed, 12 Apr 2023 09:45:07 GMT  
		Size: 4.9 MB (4934569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0797973d3ff4c7bfddd6439ceacd815ea867f868a8c75686d5b80ee1a3eca322`  
		Last Modified: Wed, 12 Apr 2023 09:45:08 GMT  
		Size: 10.2 MB (10217876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cff4fab8e209a4a8ef903baadd1f4839687988e57cef0235a447c0198ddfab`  
		Last Modified: Wed, 12 Apr 2023 09:45:28 GMT  
		Size: 50.4 MB (50355731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c442c38966496f089bcee5c78d8e7321764a2a679fd64f1070215e5f24b6d872`  
		Last Modified: Wed, 12 Apr 2023 09:46:04 GMT  
		Size: 167.3 MB (167288359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e7277cb741804ffe9213d32a419f6738ef4494fbd33db9326b55282dfbc1dd6b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314135667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c57708eddbf78525fe399f52d71e35653f6c3298641025d07fcc3323777584`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:42 GMT
ADD file:dd3d4e5fe819950e7d01b44a29dbd790438cd722ba76198910e2597448ab0c6f in / 
# Wed, 12 Apr 2023 00:39:43 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:06:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:06:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:07:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:08:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dc80b8cdbfd36cb20231d807a50d704945d1df4da8f6e23197ccfcb629970491`  
		Last Modified: Wed, 12 Apr 2023 00:42:14 GMT  
		Size: 53.7 MB (53705529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5884e7f2c8c61aa845de4902fc29639b58861ae6c2d80bafe82082c0456c0740`  
		Last Modified: Wed, 12 Apr 2023 01:13:17 GMT  
		Size: 5.2 MB (5152752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b792b01ed3c8dc1488cd8aac41ab7d49bb17f3fa22b2e6c846078cec81a1c00`  
		Last Modified: Wed, 12 Apr 2023 01:13:17 GMT  
		Size: 10.9 MB (10873655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f993d5b17f32f4b8a535c25e182e5d8412625beee450e513ca57036e8fdd6dc`  
		Last Modified: Wed, 12 Apr 2023 01:13:34 GMT  
		Size: 54.7 MB (54676038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26edf98ece5babdb6b65e76738cef2c2d05e7075161753d3ba95cd84480d211`  
		Last Modified: Wed, 12 Apr 2023 01:14:02 GMT  
		Size: 189.7 MB (189727693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ff274b300c58e39b8abdacecdee25d47651abe32a696616b92656ca392bd5d21
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.2 MB (328223380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5eee57e4ddbeaa9219392349db2bc711541f424d58a97b4a86ad5bd768ff773`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:38:51 GMT
ADD file:4da7e6af0782b21849e5f6385de3589ac5b8d81d173721f9990d32da754df2cb in / 
# Wed, 12 Apr 2023 00:38:51 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:05:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:05:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:06:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:07:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b2bef40925391866903279768b0ae1e8233ef6a1aae64509a922f4aa96fe42a6`  
		Last Modified: Wed, 12 Apr 2023 00:42:19 GMT  
		Size: 56.0 MB (56032818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37ccf9a5e34ba2345ce265a9a11c93ee254e1f3616dfd1c1deda6e2f7d614c8`  
		Last Modified: Wed, 12 Apr 2023 01:14:53 GMT  
		Size: 5.3 MB (5293626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4988d5e4328f031f6884a7351766aa8a2806c9cdca38d354477fc537eaa4911f`  
		Last Modified: Wed, 12 Apr 2023 01:14:54 GMT  
		Size: 11.2 MB (11249875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660a2befd486d43a308dd1561f57efeafe1f13defd6439d34aeb5efec783ee3d`  
		Last Modified: Wed, 12 Apr 2023 01:15:17 GMT  
		Size: 55.9 MB (55922746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f09985282f12d05c5724bcbb0481a94f66820112bafc34a1d990dfdf74a52fc`  
		Last Modified: Wed, 12 Apr 2023 01:16:02 GMT  
		Size: 199.7 MB (199724315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:733073a5e45e28ac1efdd031f70eb14ea95adc6350a95cd5eec6e4289ad5726c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301296282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb9d52fa12ccd33943e746e02c6d998737105a5b221ed73b5860e5137600578`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:09:26 GMT
ADD file:5d2c839055739fe92d64098c09607e7ec9123101d15f837c54f3688755af0c23 in / 
# Wed, 12 Apr 2023 00:09:31 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 11:00:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 11:00:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 11:02:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 11:08:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80243e355b05bee53c6acc45ace2cde4f7495dafe9f3f8d7d299ed51d04928d2`  
		Last Modified: Wed, 12 Apr 2023 00:16:48 GMT  
		Size: 53.3 MB (53272023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed6aed7903d464c3c421335c8a4b93f11e64b669c7eab532e87e5945fd185e2`  
		Last Modified: Wed, 12 Apr 2023 11:20:32 GMT  
		Size: 5.1 MB (5127336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af3f0065ba2217f3ef903c35f7e644bd2222c1630a96ac62477510cedfa848`  
		Last Modified: Wed, 12 Apr 2023 11:20:34 GMT  
		Size: 10.7 MB (10662154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81fa7bf218e18cc100c89241735ff424465ba8caca78835fdadafcd212de62f`  
		Last Modified: Wed, 12 Apr 2023 11:21:19 GMT  
		Size: 53.3 MB (53306535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f17002a316d921b7e863e4fa717c4354ebce8cf57671d9a2bf8f34dec378d8c`  
		Last Modified: Wed, 12 Apr 2023 11:23:14 GMT  
		Size: 178.9 MB (178928234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5b39e218d6f9e9f7c2241165c5f3ff812622a74d175997245e60615626e2508a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.0 MB (330997339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b69805860c4cc4b90cbcdadb6ab37298c1d198c92781fef2c1ca29f434eae34b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:07:58 GMT
ADD file:c3c2a10473ddaa3d8a30ca99b19ad3599d0e60d826c4e0315bdb7463352ebc09 in / 
# Wed, 12 Apr 2023 00:08:02 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:31:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:32:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:33:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:36:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2d3ffdd4610a019889b845cc82b3d956ad85cca78ad4bff2d5e5522bd02c17e7`  
		Last Modified: Wed, 12 Apr 2023 00:12:37 GMT  
		Size: 58.9 MB (58926600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00772c18aacd8e2ae167f5f94b2e86c7b77fd3f7790dc5e6754e48fcce1ff484`  
		Last Modified: Wed, 12 Apr 2023 09:45:12 GMT  
		Size: 5.4 MB (5415380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1877fd565f7c580ab3b8fd343d19de69c9c3334787d6a3c93c9c21fe08ea32a`  
		Last Modified: Wed, 12 Apr 2023 09:45:13 GMT  
		Size: 11.6 MB (11629984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a24a9774fce2d157b32633fbd68d6d4777632ca49b0a35d2e9be9a2455d88b`  
		Last Modified: Wed, 12 Apr 2023 09:45:40 GMT  
		Size: 58.9 MB (58865366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d134f385b05ace42f019d92548a9dd6708f9ae2ee3269131645b4ff67b2463`  
		Last Modified: Wed, 12 Apr 2023 09:46:38 GMT  
		Size: 196.2 MB (196160009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:478709c66fdeffea827bb22297605067d97172933185294b18da02b3b071e7a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296079415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62811c5341c95a39adc789318a1ba301b0fae01b6b77e3b4a63a1693c43fa76d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:00:25 GMT
ADD file:ab4e28724d04724a57e0f5bbe299d3361103f05ad1978dc3bfef243c1f9d6476 in / 
# Wed, 12 Apr 2023 00:00:38 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:26:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:26:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 00:27:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:28:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:042263756d7dc47bf98a243871107aa3a2b41acda91d104d8b4e148749a43dda`  
		Last Modified: Wed, 12 Apr 2023 00:05:03 GMT  
		Size: 53.3 MB (53286682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2973b8c98f9da7833ab9cd69185dd958a8939a30136cdcfedb66ce775db358ee`  
		Last Modified: Wed, 12 Apr 2023 00:32:48 GMT  
		Size: 5.1 MB (5149313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f740d13ac612bf8b6489559a7945ec1439fee2d5eba455ab0db047cd3f30a9a`  
		Last Modified: Wed, 12 Apr 2023 00:32:49 GMT  
		Size: 10.8 MB (10766104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c0067783f401b099adca196dce9e464e66236e49faba106e2f04ac73a90df7`  
		Last Modified: Wed, 12 Apr 2023 00:33:02 GMT  
		Size: 54.1 MB (54061843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1b5accdd9fd68a290692e1a0a3d853312f236ae0463540b5fdd97d598cc7a6`  
		Last Modified: Wed, 12 Apr 2023 00:33:28 GMT  
		Size: 172.8 MB (172815473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:lunar`

```console
$ docker pull buildpack-deps@sha256:8f30aeb6da27a92876d75b655895a20d8e7b78315a226232fd7ae946beec400d
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
$ docker pull buildpack-deps@sha256:c040bdb4d1eccb9d60dd883c8659fbf36a70b95230aec411f7752a8c9df7547c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.0 MB (263988698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ea1fdc55d3ba2d46c3a45c9262a09a41439e31a6d6370f6f97f83cc0f34fcc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:51:04 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:51:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:51:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:51:04 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:51:05 GMT
ADD file:0974d2aeef46c39070cbf74e10bf8644b9753060809b3c7100126a1bcb448f12 in / 
# Sat, 15 Apr 2023 04:51:06 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:30:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:31:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:31:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:34:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:43bb70e8bba148f5c5a4d50f8a5204951f795a069a2cd25b2e37ebafdd10afc7`  
		Last Modified: Tue, 18 Apr 2023 01:36:35 GMT  
		Size: 27.6 MB (27604045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d673d8abcf3e237b47c181613058fc86a03ce40e22cfa4a288287dffe5ef25d3`  
		Last Modified: Tue, 18 Apr 2023 01:36:33 GMT  
		Size: 6.4 MB (6382657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc90ad50e915047a562094b5a7813b9e3f81bb7782373cfac2a9fcbf7a5574a`  
		Last Modified: Tue, 18 Apr 2023 01:36:32 GMT  
		Size: 3.7 MB (3693225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbab6c6decb3beeb560234f8c7d7751604b70f7509abcff1a13111b80ae018a4`  
		Last Modified: Tue, 18 Apr 2023 01:36:50 GMT  
		Size: 44.3 MB (44256643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e5d1d102ea25927cc8832edc34d8152aab70036d9a4f916f543ede88760c4e`  
		Last Modified: Tue, 18 Apr 2023 01:37:22 GMT  
		Size: 182.1 MB (182052128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:000d7e40e49f456e833154c2d71353f3bddb12a02e2b0ba882978f93f9c6c56e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228579351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a1cef0b8f1ba77af697fcca31c23ab0d1ae072e54d4ed84cbc4a2c454709101`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:38:02 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:38:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:38:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:38:02 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:38:05 GMT
ADD file:9f0981aade24310bb7a4c492e6ec76e24f146f4efd6782ddba79ece3b8afe7b5 in / 
# Sat, 15 Apr 2023 04:38:05 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:44:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:45:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:45:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:48:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cc0ec898907bfe3505695fd5ae23b4cf5d6d180fdb036e767c23cc35a2abc39b`  
		Last Modified: Tue, 18 Apr 2023 01:51:15 GMT  
		Size: 25.4 MB (25437825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3711420f6b1b87fa85e1e1dde561aa26c9e0143e968d0ba9f6f98811b9e290`  
		Last Modified: Tue, 18 Apr 2023 01:51:12 GMT  
		Size: 5.5 MB (5545810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e741069d31363bff0e76178d15c895dcacd68407a20ce1c27f0a73ee511e61d8`  
		Last Modified: Tue, 18 Apr 2023 01:51:12 GMT  
		Size: 3.8 MB (3847237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4988e98a76edb96dc5fee90cb5d45db9378a4ba15f49647a098e4a4c4b888c77`  
		Last Modified: Tue, 18 Apr 2023 01:51:31 GMT  
		Size: 48.3 MB (48294473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892ba47d241faa5d135b9966167a61c95aad80e94b334d0b7ec63041f64fda43`  
		Last Modified: Tue, 18 Apr 2023 01:51:59 GMT  
		Size: 145.5 MB (145454006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7eb8a34ef8517f80859dc448e809c9c9078e6b8dacf23a6750cd0eae459b9487
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254284885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a583d5b43c43b667581b05b79463eba4d8cf6b9295ec519f94633ce5f61562a1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:41:09 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:41:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:41:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:41:10 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:41:17 GMT
ADD file:0a45cfb0f66cc6191e34ca0d42987f4ee1f86f70c5ee9a29ec3e353ceea7ce51 in / 
# Sat, 15 Apr 2023 04:41:18 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:29:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:30:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:30:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:33:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cc6919ddce2a233f58cc3e7dbe578e059849f4571e49c4a84c7c981f17a89835`  
		Last Modified: Tue, 18 Apr 2023 01:36:11 GMT  
		Size: 27.0 MB (27018561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9dfffa12a1f77a99f18745a89a98d7c560b403d259aaabb2ea7e8099aba267`  
		Last Modified: Tue, 18 Apr 2023 01:36:08 GMT  
		Size: 6.2 MB (6217841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b46934c541eaff8b64481ad9212943b45e46655b2e916d0a2a1edf56c835075`  
		Last Modified: Tue, 18 Apr 2023 01:36:09 GMT  
		Size: 3.7 MB (3653186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff58527001798506a9dc32ce859a3d047cc557aa033359f185d2451be24cf5b`  
		Last Modified: Tue, 18 Apr 2023 01:36:24 GMT  
		Size: 44.1 MB (44077916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55eb81a3584d1feea46abd6869b71852c54408ee766a0895b86d4915752208de`  
		Last Modified: Tue, 18 Apr 2023 01:36:49 GMT  
		Size: 173.3 MB (173317381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5090fa89cb4d665c6b029976d4d929e424390503a1f35135e12612c86f8d073e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.5 MB (288502540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29bf47b159469fa22c03c0456e2d2221865676486fbf95b847453b413e41ca0a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:51:08 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:51:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:51:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:51:09 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:51:11 GMT
ADD file:57838c4589ddbfb3bfb239d9d6749a36f0d7201d8788fa4293dfe9ad93308e40 in / 
# Sat, 15 Apr 2023 04:51:12 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:54:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:54:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 00:55:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:00:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fcabd7528fca87cc5a63f487865487cc2f6832df71a8c871f40b369f4f0f945d`  
		Last Modified: Tue, 18 Apr 2023 01:04:41 GMT  
		Size: 32.0 MB (31996733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd02da4adaf96b5e8dea2c0a2846b3cda00cb99c8a2af6a5da9996399bdab78`  
		Last Modified: Tue, 18 Apr 2023 01:04:36 GMT  
		Size: 7.4 MB (7364592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6bd36dd881e6a900302ba6370fbb475b14bf1dd9e35dc4209f84fb8c5065fb`  
		Last Modified: Tue, 18 Apr 2023 01:04:35 GMT  
		Size: 4.4 MB (4413806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11b8a0da4d0a3c624fb719be6321b9020894b77b2028fb6352c38403a1a77e6`  
		Last Modified: Tue, 18 Apr 2023 01:05:04 GMT  
		Size: 48.9 MB (48945236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1c1f4dc0b62d9d13e02a7d9066e7642d3a6440780c8ff95db3ba050af43976`  
		Last Modified: Tue, 18 Apr 2023 01:06:01 GMT  
		Size: 195.8 MB (195782173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:51c88a6dfccf081c6f31980cfce4183a66f188868648a9d6382e802317134227
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235447894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3f0864f3aba4bc5def98d2e8129dfbc7c9b623b4f64aa2d42cee71bc56f8a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:52:00 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:52:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:52:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:52:00 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:52:02 GMT
ADD file:fbea81511df0975bdcf894e5be93dc02670d76233449f6221b0a6752e6178646 in / 
# Sat, 15 Apr 2023 04:52:02 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:09:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:09:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:10:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:12:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:92338e21c9dcc2f2402a20239390e6f35f1a8beaa9ebf17ca317ce011b1cef40`  
		Last Modified: Tue, 18 Apr 2023 01:14:57 GMT  
		Size: 26.2 MB (26236111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1665ec17c4182267692bd75dd16a85d9e658f0f52656651e35f3c6856edf38f`  
		Last Modified: Tue, 18 Apr 2023 01:14:54 GMT  
		Size: 6.1 MB (6066022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435dc1ff769b0f8daba446a3386907dc4fe1be7df7f69e61b212baf2fb17ce18`  
		Last Modified: Tue, 18 Apr 2023 01:14:54 GMT  
		Size: 3.7 MB (3678419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af9b4b3cd888e49ca9b73654104bd6dafd3b084b47dbe8b9aa070a6fec27c58`  
		Last Modified: Tue, 18 Apr 2023 01:15:08 GMT  
		Size: 44.1 MB (44087604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8dfd448b2176a355c388f14e3c38c9a20244ab8c4a8f63df88fbe70b2f6630`  
		Last Modified: Tue, 18 Apr 2023 01:15:33 GMT  
		Size: 155.4 MB (155379738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:lunar-curl`

```console
$ docker pull buildpack-deps@sha256:a86b9ddf8bc507fe7814dfa053c530c7f3bdbf26759d272a6b0e92974ed084ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:lunar-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f309034a3bcb45ac60629303e126db07403cdb2a7e01389ac326498f0b2f3368
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37679927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220173d47bb64c458e18cdfea3dafd604370b15d4b684bcdc8d12c24f3e20246`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:51:04 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:51:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:51:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:51:04 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:51:05 GMT
ADD file:0974d2aeef46c39070cbf74e10bf8644b9753060809b3c7100126a1bcb448f12 in / 
# Sat, 15 Apr 2023 04:51:06 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:30:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:31:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:43bb70e8bba148f5c5a4d50f8a5204951f795a069a2cd25b2e37ebafdd10afc7`  
		Last Modified: Tue, 18 Apr 2023 01:36:35 GMT  
		Size: 27.6 MB (27604045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d673d8abcf3e237b47c181613058fc86a03ce40e22cfa4a288287dffe5ef25d3`  
		Last Modified: Tue, 18 Apr 2023 01:36:33 GMT  
		Size: 6.4 MB (6382657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc90ad50e915047a562094b5a7813b9e3f81bb7782373cfac2a9fcbf7a5574a`  
		Last Modified: Tue, 18 Apr 2023 01:36:32 GMT  
		Size: 3.7 MB (3693225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0db04bad5c5ec2a78f7cfa3f1b642bf737c44fdde8915d5423aa6b7ba7c65eb8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34830872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bd0ffae1c99ddc27c3872ac1d526dd3ccb5341b161b0518994bc0f8dd1b48a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:38:02 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:38:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:38:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:38:02 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:38:05 GMT
ADD file:9f0981aade24310bb7a4c492e6ec76e24f146f4efd6782ddba79ece3b8afe7b5 in / 
# Sat, 15 Apr 2023 04:38:05 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:44:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:45:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:cc0ec898907bfe3505695fd5ae23b4cf5d6d180fdb036e767c23cc35a2abc39b`  
		Last Modified: Tue, 18 Apr 2023 01:51:15 GMT  
		Size: 25.4 MB (25437825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3711420f6b1b87fa85e1e1dde561aa26c9e0143e968d0ba9f6f98811b9e290`  
		Last Modified: Tue, 18 Apr 2023 01:51:12 GMT  
		Size: 5.5 MB (5545810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e741069d31363bff0e76178d15c895dcacd68407a20ce1c27f0a73ee511e61d8`  
		Last Modified: Tue, 18 Apr 2023 01:51:12 GMT  
		Size: 3.8 MB (3847237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4e87da995eca42edb48757bdf7d1057b205ff73cd3e340a45187725b3b7a281a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36889588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3faa679b0465766abf4614a65c625b5d7e241b2071dd2e53956428742d68e1b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:41:09 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:41:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:41:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:41:10 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:41:17 GMT
ADD file:0a45cfb0f66cc6191e34ca0d42987f4ee1f86f70c5ee9a29ec3e353ceea7ce51 in / 
# Sat, 15 Apr 2023 04:41:18 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:29:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:30:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:cc6919ddce2a233f58cc3e7dbe578e059849f4571e49c4a84c7c981f17a89835`  
		Last Modified: Tue, 18 Apr 2023 01:36:11 GMT  
		Size: 27.0 MB (27018561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9dfffa12a1f77a99f18745a89a98d7c560b403d259aaabb2ea7e8099aba267`  
		Last Modified: Tue, 18 Apr 2023 01:36:08 GMT  
		Size: 6.2 MB (6217841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b46934c541eaff8b64481ad9212943b45e46655b2e916d0a2a1edf56c835075`  
		Last Modified: Tue, 18 Apr 2023 01:36:09 GMT  
		Size: 3.7 MB (3653186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f7f929427c910be5fe858e0f968e85d6e70d2d7168e8aae85e37ec03557f8c8a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43775131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d87006cf7cfef2979a32c9ffb816c8d07b7da92dcd2d041cd3bec310ce664690`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:51:08 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:51:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:51:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:51:09 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:51:11 GMT
ADD file:57838c4589ddbfb3bfb239d9d6749a36f0d7201d8788fa4293dfe9ad93308e40 in / 
# Sat, 15 Apr 2023 04:51:12 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:54:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:54:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:fcabd7528fca87cc5a63f487865487cc2f6832df71a8c871f40b369f4f0f945d`  
		Last Modified: Tue, 18 Apr 2023 01:04:41 GMT  
		Size: 32.0 MB (31996733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd02da4adaf96b5e8dea2c0a2846b3cda00cb99c8a2af6a5da9996399bdab78`  
		Last Modified: Tue, 18 Apr 2023 01:04:36 GMT  
		Size: 7.4 MB (7364592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6bd36dd881e6a900302ba6370fbb475b14bf1dd9e35dc4209f84fb8c5065fb`  
		Last Modified: Tue, 18 Apr 2023 01:04:35 GMT  
		Size: 4.4 MB (4413806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d1fe860c8e5b73d01ef34d19528360fb22471301f44f5d0983c10986da138bf6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35980552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e48719fe1a6ff3a99da9dcc66662d1f07f131663406f8df5491a5218fa013e4b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:52:00 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:52:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:52:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:52:00 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:52:02 GMT
ADD file:fbea81511df0975bdcf894e5be93dc02670d76233449f6221b0a6752e6178646 in / 
# Sat, 15 Apr 2023 04:52:02 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:09:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:09:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:92338e21c9dcc2f2402a20239390e6f35f1a8beaa9ebf17ca317ce011b1cef40`  
		Last Modified: Tue, 18 Apr 2023 01:14:57 GMT  
		Size: 26.2 MB (26236111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1665ec17c4182267692bd75dd16a85d9e658f0f52656651e35f3c6856edf38f`  
		Last Modified: Tue, 18 Apr 2023 01:14:54 GMT  
		Size: 6.1 MB (6066022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435dc1ff769b0f8daba446a3386907dc4fe1be7df7f69e61b212baf2fb17ce18`  
		Last Modified: Tue, 18 Apr 2023 01:14:54 GMT  
		Size: 3.7 MB (3678419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:lunar-scm`

```console
$ docker pull buildpack-deps@sha256:101eaaa881d244e5b86427bd2ea3986745db049d51b2efbcbe0f1d5408efa51e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:lunar-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:bbccbf35da61832e131a695eb66a451648c9fe24207019c396fcd9cdaf261c59
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81936570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2a3771bec692bafa9bf6b6d10c70540d0db0e39ed2f951458ba86af7f7e7c4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:51:04 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:51:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:51:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:51:04 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:51:05 GMT
ADD file:0974d2aeef46c39070cbf74e10bf8644b9753060809b3c7100126a1bcb448f12 in / 
# Sat, 15 Apr 2023 04:51:06 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:30:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:31:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:31:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:43bb70e8bba148f5c5a4d50f8a5204951f795a069a2cd25b2e37ebafdd10afc7`  
		Last Modified: Tue, 18 Apr 2023 01:36:35 GMT  
		Size: 27.6 MB (27604045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d673d8abcf3e237b47c181613058fc86a03ce40e22cfa4a288287dffe5ef25d3`  
		Last Modified: Tue, 18 Apr 2023 01:36:33 GMT  
		Size: 6.4 MB (6382657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc90ad50e915047a562094b5a7813b9e3f81bb7782373cfac2a9fcbf7a5574a`  
		Last Modified: Tue, 18 Apr 2023 01:36:32 GMT  
		Size: 3.7 MB (3693225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbab6c6decb3beeb560234f8c7d7751604b70f7509abcff1a13111b80ae018a4`  
		Last Modified: Tue, 18 Apr 2023 01:36:50 GMT  
		Size: 44.3 MB (44256643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8a9c907da4326f88024491a3da9762d29aa85c9ae4614dc8dbd65046f9d57918
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83125345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b8ef037b71f435f2efdf17ffe0b410ad38b4e58304c29569f0b121b7228e12`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:38:02 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:38:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:38:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:38:02 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:38:05 GMT
ADD file:9f0981aade24310bb7a4c492e6ec76e24f146f4efd6782ddba79ece3b8afe7b5 in / 
# Sat, 15 Apr 2023 04:38:05 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:44:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:45:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:45:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cc0ec898907bfe3505695fd5ae23b4cf5d6d180fdb036e767c23cc35a2abc39b`  
		Last Modified: Tue, 18 Apr 2023 01:51:15 GMT  
		Size: 25.4 MB (25437825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3711420f6b1b87fa85e1e1dde561aa26c9e0143e968d0ba9f6f98811b9e290`  
		Last Modified: Tue, 18 Apr 2023 01:51:12 GMT  
		Size: 5.5 MB (5545810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e741069d31363bff0e76178d15c895dcacd68407a20ce1c27f0a73ee511e61d8`  
		Last Modified: Tue, 18 Apr 2023 01:51:12 GMT  
		Size: 3.8 MB (3847237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4988e98a76edb96dc5fee90cb5d45db9378a4ba15f49647a098e4a4c4b888c77`  
		Last Modified: Tue, 18 Apr 2023 01:51:31 GMT  
		Size: 48.3 MB (48294473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ee060cbb2825a0e5c6d2c37a0f28eb460681bbc14451be3d563d3549f7365bfc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (80967504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2a9bce91e466eaf8d5721d6d72082a18ece9524f992f0fde72b08ce01455a6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:41:09 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:41:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:41:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:41:10 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:41:17 GMT
ADD file:0a45cfb0f66cc6191e34ca0d42987f4ee1f86f70c5ee9a29ec3e353ceea7ce51 in / 
# Sat, 15 Apr 2023 04:41:18 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:29:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:30:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:30:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cc6919ddce2a233f58cc3e7dbe578e059849f4571e49c4a84c7c981f17a89835`  
		Last Modified: Tue, 18 Apr 2023 01:36:11 GMT  
		Size: 27.0 MB (27018561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9dfffa12a1f77a99f18745a89a98d7c560b403d259aaabb2ea7e8099aba267`  
		Last Modified: Tue, 18 Apr 2023 01:36:08 GMT  
		Size: 6.2 MB (6217841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b46934c541eaff8b64481ad9212943b45e46655b2e916d0a2a1edf56c835075`  
		Last Modified: Tue, 18 Apr 2023 01:36:09 GMT  
		Size: 3.7 MB (3653186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff58527001798506a9dc32ce859a3d047cc557aa033359f185d2451be24cf5b`  
		Last Modified: Tue, 18 Apr 2023 01:36:24 GMT  
		Size: 44.1 MB (44077916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1fd6a50b6a6df0aaae7eecf4f25a23d66698a56a420fceac58859c82334c373c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92720367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2680105e7ba022355f1f320347591ffcaa718b8d1c7fb525bcbaa2bd1de940`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:51:08 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:51:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:51:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:51:09 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:51:11 GMT
ADD file:57838c4589ddbfb3bfb239d9d6749a36f0d7201d8788fa4293dfe9ad93308e40 in / 
# Sat, 15 Apr 2023 04:51:12 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:54:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:54:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 00:55:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fcabd7528fca87cc5a63f487865487cc2f6832df71a8c871f40b369f4f0f945d`  
		Last Modified: Tue, 18 Apr 2023 01:04:41 GMT  
		Size: 32.0 MB (31996733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd02da4adaf96b5e8dea2c0a2846b3cda00cb99c8a2af6a5da9996399bdab78`  
		Last Modified: Tue, 18 Apr 2023 01:04:36 GMT  
		Size: 7.4 MB (7364592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6bd36dd881e6a900302ba6370fbb475b14bf1dd9e35dc4209f84fb8c5065fb`  
		Last Modified: Tue, 18 Apr 2023 01:04:35 GMT  
		Size: 4.4 MB (4413806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11b8a0da4d0a3c624fb719be6321b9020894b77b2028fb6352c38403a1a77e6`  
		Last Modified: Tue, 18 Apr 2023 01:05:04 GMT  
		Size: 48.9 MB (48945236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:712fd37daa58220b07ef60020b33ade10599163dc40e476600099c7058b75bd8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80068156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dc83d080597d0511ef668ef12d04f8965d989d28c0896a33c9d5b0b3c59593`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:52:00 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:52:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:52:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:52:00 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:52:02 GMT
ADD file:fbea81511df0975bdcf894e5be93dc02670d76233449f6221b0a6752e6178646 in / 
# Sat, 15 Apr 2023 04:52:02 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:09:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:09:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:10:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:92338e21c9dcc2f2402a20239390e6f35f1a8beaa9ebf17ca317ce011b1cef40`  
		Last Modified: Tue, 18 Apr 2023 01:14:57 GMT  
		Size: 26.2 MB (26236111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1665ec17c4182267692bd75dd16a85d9e658f0f52656651e35f3c6856edf38f`  
		Last Modified: Tue, 18 Apr 2023 01:14:54 GMT  
		Size: 6.1 MB (6066022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435dc1ff769b0f8daba446a3386907dc4fe1be7df7f69e61b212baf2fb17ce18`  
		Last Modified: Tue, 18 Apr 2023 01:14:54 GMT  
		Size: 3.7 MB (3678419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af9b4b3cd888e49ca9b73654104bd6dafd3b084b47dbe8b9aa070a6fec27c58`  
		Last Modified: Tue, 18 Apr 2023 01:15:08 GMT  
		Size: 44.1 MB (44087604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldstable`

```console
$ docker pull buildpack-deps@sha256:5c2114d327b0e2a38de4e3dcf5fa304e4da23264a1e77643632d0a25325d7e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2ea103832a6fac73696522edc50dc0aa8c41a2073edb2d29685224196ed046e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.0 MB (312037541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:055f98e5c72e14d3f944a8a2f131602966cfd07c563d5884eddb16a00be4c875`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:15 GMT
ADD file:40953ed6e6f96703b2e0c13288437c2aaf8b3df33dbc423686290cbe0e595a5e in / 
# Wed, 12 Apr 2023 00:20:15 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:52:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 07:53:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:54:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2ff1d7c41c74a25258bfa6f0b8adb0a727f84518f55f65ca845ebc747976c408`  
		Last Modified: Wed, 12 Apr 2023 00:24:01 GMT  
		Size: 50.4 MB (50448726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b253aeafeaa7e0671bb60008df01de101a38a045ff7bc656e3b0fbfc7c05cca5`  
		Last Modified: Wed, 12 Apr 2023 07:58:30 GMT  
		Size: 7.9 MB (7863355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2201bd995cccf12851a50820de03d34a17011dcbb9ac9fdf3a50c952cbb131`  
		Last Modified: Wed, 12 Apr 2023 07:58:30 GMT  
		Size: 10.0 MB (10001452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de76e268b103d05fa8960e0f77951ff54b912b63429c34f5d6adfd09f5f9ee2`  
		Last Modified: Wed, 12 Apr 2023 07:58:44 GMT  
		Size: 51.9 MB (51876420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a8df5894511ce28a05e2925a75e8a4acbd0634c39ad734fdfba8e23d1b1569`  
		Last Modified: Wed, 12 Apr 2023 07:59:14 GMT  
		Size: 191.8 MB (191847588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:410344bd121264c1e44e6ff6404552757b78c17737dcb22a19f6ae20ba31f66d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.9 MB (277871836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd6300ad40c10f96fede2bdeedc551685aa3053dd2376792263ee1faf0f6f679`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:53 GMT
ADD file:3f6ca36ec4fbf50ab85c907c089dbb0618c73393c07a5841b922145b17795552 in / 
# Tue, 11 Apr 2023 23:59:54 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:37:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:37:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:37:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:39:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:166ef90dbaeab03f451f526d325c57795001e25f10c984c334a82d174b3c554b`  
		Last Modified: Wed, 12 Apr 2023 00:03:36 GMT  
		Size: 45.9 MB (45916201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84460c1688b734c8075a939aae674e32cf7240a0d3a2fa0602a9a9fd472ffe1e`  
		Last Modified: Wed, 12 Apr 2023 09:46:16 GMT  
		Size: 7.2 MB (7153935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed4779654861d62e5bc31eea7bacd2c7bbfdb617dd9dc01e2afd24a4baedf7f`  
		Last Modified: Wed, 12 Apr 2023 09:46:17 GMT  
		Size: 9.3 MB (9348985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6bfe04b18e678bcacb84dd292223f32a76d4837c22ccd16465318f6c1429f21`  
		Last Modified: Wed, 12 Apr 2023 09:46:34 GMT  
		Size: 47.4 MB (47395508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc69a47db99b12842846092749a24bc3d2701f5e6b46467a6eb56e1d19ed48a3`  
		Last Modified: Wed, 12 Apr 2023 09:47:09 GMT  
		Size: 168.1 MB (168057207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5e8e3f3212dcc5c0e3442e591cffe69a01891021308eca92c8b3bc2803c31459
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.6 MB (302601726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0303fb5950d191d02ab39565ca367ca55dc2b108c9b7ba4d645ed85d1a074d1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:55 GMT
ADD file:93facc669dd63b37fb5dde18f3b3a1cb5621aa396e1960ea85facdd1c619a3f0 in / 
# Wed, 12 Apr 2023 00:39:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:08:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:08:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:08:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:10:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b4910c31031a0301ea4f8b7155269014925aeb17c71b869dea3ff907ba294b55`  
		Last Modified: Wed, 12 Apr 2023 00:42:52 GMT  
		Size: 49.2 MB (49238632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208fd617b499747daceba851b67da426c285d1e306b316a193f06968123f49da`  
		Last Modified: Wed, 12 Apr 2023 01:14:12 GMT  
		Size: 7.7 MB (7732136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efadebfda1423d1b70a0e991e9ff8bb2e3fe0b08d55562359a004c265fc7c86`  
		Last Modified: Wed, 12 Apr 2023 01:14:12 GMT  
		Size: 10.0 MB (10003581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe7e7c438113f5e58417f97e7eb0a755b17ee63eebd85a7c3b86a2aad4c993e`  
		Last Modified: Wed, 12 Apr 2023 01:14:27 GMT  
		Size: 52.2 MB (52191713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33997ebd7335eb6f55d98725b5fb8e4899166098d6db119cd6f6bc7055ffa858`  
		Last Modified: Wed, 12 Apr 2023 01:14:51 GMT  
		Size: 183.4 MB (183435664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:76a9d8ac8ca52b47077a29022657b9bdc9facd485bf6f6bc8c7115ed9915e020
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.5 MB (321464682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb3655fb3b861afdfc5e7da86468a57acd97ab2b796815bf255141ce4e9ec42c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:11 GMT
ADD file:8299e58c7e43af1f3b9fdb9bd37e3f37cf619a97ef1b87d60ca66860d646d526 in / 
# Wed, 12 Apr 2023 00:39:11 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:08:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:08:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:08:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:11:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2d15e1c2a3da7d675c2513d7ceab1d0f33ced9a82bed63d9a11ce71f1218d232`  
		Last Modified: Wed, 12 Apr 2023 00:43:07 GMT  
		Size: 51.2 MB (51206167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af123d7f5c8b1197b6040820195efacf1a57299baf71416c7a63281566cdc199`  
		Last Modified: Wed, 12 Apr 2023 01:16:15 GMT  
		Size: 8.0 MB (8034011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3af175eda8706326ac898703f9aafb47e7e08ec08318794c6838efa8f3d3bc`  
		Last Modified: Wed, 12 Apr 2023 01:16:15 GMT  
		Size: 10.3 MB (10345678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9cbd6d7217bf920da02e590f88fbfb42fb3162969840a3b17eb25c762247c04`  
		Last Modified: Wed, 12 Apr 2023 01:16:35 GMT  
		Size: 53.5 MB (53471080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d0a6f1efbd6131f1ae888ea393318f9d32a3e8ad8b8c97207c3a5b7a3ed9bc`  
		Last Modified: Wed, 12 Apr 2023 01:17:17 GMT  
		Size: 198.4 MB (198407746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:aced785a2513d8727060141156b30a8a3081d95054e1196da909d83c1c6d1203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7f26d8de0d9b1472f4b76a591461f81e28dd4469eed96b3bb172a93adde9779f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68313533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212d47455d74a1b460742fc95270dd155e5dccb7f8cf98d1b0166a911a42e56f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:15 GMT
ADD file:40953ed6e6f96703b2e0c13288437c2aaf8b3df33dbc423686290cbe0e595a5e in / 
# Wed, 12 Apr 2023 00:20:15 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:52:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2ff1d7c41c74a25258bfa6f0b8adb0a727f84518f55f65ca845ebc747976c408`  
		Last Modified: Wed, 12 Apr 2023 00:24:01 GMT  
		Size: 50.4 MB (50448726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b253aeafeaa7e0671bb60008df01de101a38a045ff7bc656e3b0fbfc7c05cca5`  
		Last Modified: Wed, 12 Apr 2023 07:58:30 GMT  
		Size: 7.9 MB (7863355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2201bd995cccf12851a50820de03d34a17011dcbb9ac9fdf3a50c952cbb131`  
		Last Modified: Wed, 12 Apr 2023 07:58:30 GMT  
		Size: 10.0 MB (10001452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:076bc54af0ee3f4cc5de008a85e1e66f5f01d819b9bdf9ed313c1c1b88928e78
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62419121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79aebda5e687723c136aae0676cad834f015f5bb039f4857700bf9dba626b13f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:53 GMT
ADD file:3f6ca36ec4fbf50ab85c907c089dbb0618c73393c07a5841b922145b17795552 in / 
# Tue, 11 Apr 2023 23:59:54 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:37:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:37:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:166ef90dbaeab03f451f526d325c57795001e25f10c984c334a82d174b3c554b`  
		Last Modified: Wed, 12 Apr 2023 00:03:36 GMT  
		Size: 45.9 MB (45916201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84460c1688b734c8075a939aae674e32cf7240a0d3a2fa0602a9a9fd472ffe1e`  
		Last Modified: Wed, 12 Apr 2023 09:46:16 GMT  
		Size: 7.2 MB (7153935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed4779654861d62e5bc31eea7bacd2c7bbfdb617dd9dc01e2afd24a4baedf7f`  
		Last Modified: Wed, 12 Apr 2023 09:46:17 GMT  
		Size: 9.3 MB (9348985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f4f9c875a9f7cdaa332594325c8c868d26a05ef018355a11554c8b1b5657b625
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (66974349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25cefdb01c939d204ba6d7c49b6053a29c8ad035592de81e899acd889fd70fc2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:55 GMT
ADD file:93facc669dd63b37fb5dde18f3b3a1cb5621aa396e1960ea85facdd1c619a3f0 in / 
# Wed, 12 Apr 2023 00:39:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:08:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:08:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b4910c31031a0301ea4f8b7155269014925aeb17c71b869dea3ff907ba294b55`  
		Last Modified: Wed, 12 Apr 2023 00:42:52 GMT  
		Size: 49.2 MB (49238632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208fd617b499747daceba851b67da426c285d1e306b316a193f06968123f49da`  
		Last Modified: Wed, 12 Apr 2023 01:14:12 GMT  
		Size: 7.7 MB (7732136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efadebfda1423d1b70a0e991e9ff8bb2e3fe0b08d55562359a004c265fc7c86`  
		Last Modified: Wed, 12 Apr 2023 01:14:12 GMT  
		Size: 10.0 MB (10003581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:da84dcb1542b8a34ef0e6ebd7f50eeb5da1bf9f8c87c221b3d3a2bd81c81de56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69585856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256da6b06a3adecebaf9bba1b763d651016b84bfec4ad7bc9dbe24e15f37894a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:11 GMT
ADD file:8299e58c7e43af1f3b9fdb9bd37e3f37cf619a97ef1b87d60ca66860d646d526 in / 
# Wed, 12 Apr 2023 00:39:11 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:08:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:08:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2d15e1c2a3da7d675c2513d7ceab1d0f33ced9a82bed63d9a11ce71f1218d232`  
		Last Modified: Wed, 12 Apr 2023 00:43:07 GMT  
		Size: 51.2 MB (51206167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af123d7f5c8b1197b6040820195efacf1a57299baf71416c7a63281566cdc199`  
		Last Modified: Wed, 12 Apr 2023 01:16:15 GMT  
		Size: 8.0 MB (8034011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3af175eda8706326ac898703f9aafb47e7e08ec08318794c6838efa8f3d3bc`  
		Last Modified: Wed, 12 Apr 2023 01:16:15 GMT  
		Size: 10.3 MB (10345678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:08c41fe7825eae00e1c06c4f80dec886cf1d2ddb59aa9c22db15f4b323e97bdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0559dadbf61570961c0fad2acef618449ab55dc06360900e44639acdfc52d29b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120189953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ba89d7351401c33e1d4f3e124b255947cc4bf33b68236db9d8985829c0c1420`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:15 GMT
ADD file:40953ed6e6f96703b2e0c13288437c2aaf8b3df33dbc423686290cbe0e595a5e in / 
# Wed, 12 Apr 2023 00:20:15 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:52:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 07:53:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2ff1d7c41c74a25258bfa6f0b8adb0a727f84518f55f65ca845ebc747976c408`  
		Last Modified: Wed, 12 Apr 2023 00:24:01 GMT  
		Size: 50.4 MB (50448726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b253aeafeaa7e0671bb60008df01de101a38a045ff7bc656e3b0fbfc7c05cca5`  
		Last Modified: Wed, 12 Apr 2023 07:58:30 GMT  
		Size: 7.9 MB (7863355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2201bd995cccf12851a50820de03d34a17011dcbb9ac9fdf3a50c952cbb131`  
		Last Modified: Wed, 12 Apr 2023 07:58:30 GMT  
		Size: 10.0 MB (10001452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de76e268b103d05fa8960e0f77951ff54b912b63429c34f5d6adfd09f5f9ee2`  
		Last Modified: Wed, 12 Apr 2023 07:58:44 GMT  
		Size: 51.9 MB (51876420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d925de6f72cf2aa2ab02bdd4c3d06adb08d6466494a4e8bef5bc734e3a607fb4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109814629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d111674b4fe94e19007fc403fdd31abbba530618ab7e280ec871ab5d045784`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:53 GMT
ADD file:3f6ca36ec4fbf50ab85c907c089dbb0618c73393c07a5841b922145b17795552 in / 
# Tue, 11 Apr 2023 23:59:54 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:37:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:37:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:37:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:166ef90dbaeab03f451f526d325c57795001e25f10c984c334a82d174b3c554b`  
		Last Modified: Wed, 12 Apr 2023 00:03:36 GMT  
		Size: 45.9 MB (45916201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84460c1688b734c8075a939aae674e32cf7240a0d3a2fa0602a9a9fd472ffe1e`  
		Last Modified: Wed, 12 Apr 2023 09:46:16 GMT  
		Size: 7.2 MB (7153935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed4779654861d62e5bc31eea7bacd2c7bbfdb617dd9dc01e2afd24a4baedf7f`  
		Last Modified: Wed, 12 Apr 2023 09:46:17 GMT  
		Size: 9.3 MB (9348985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6bfe04b18e678bcacb84dd292223f32a76d4837c22ccd16465318f6c1429f21`  
		Last Modified: Wed, 12 Apr 2023 09:46:34 GMT  
		Size: 47.4 MB (47395508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:96e03d67380daeace99ddc589fb25df608d86e8a2d78ef9d4635323c7774934b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119166062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2ed8743d8648e388b28b2c5274b320ccc3352bca03a56d3d0b65c133c5acf9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:55 GMT
ADD file:93facc669dd63b37fb5dde18f3b3a1cb5621aa396e1960ea85facdd1c619a3f0 in / 
# Wed, 12 Apr 2023 00:39:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:08:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:08:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:08:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b4910c31031a0301ea4f8b7155269014925aeb17c71b869dea3ff907ba294b55`  
		Last Modified: Wed, 12 Apr 2023 00:42:52 GMT  
		Size: 49.2 MB (49238632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208fd617b499747daceba851b67da426c285d1e306b316a193f06968123f49da`  
		Last Modified: Wed, 12 Apr 2023 01:14:12 GMT  
		Size: 7.7 MB (7732136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efadebfda1423d1b70a0e991e9ff8bb2e3fe0b08d55562359a004c265fc7c86`  
		Last Modified: Wed, 12 Apr 2023 01:14:12 GMT  
		Size: 10.0 MB (10003581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe7e7c438113f5e58417f97e7eb0a755b17ee63eebd85a7c3b86a2aad4c993e`  
		Last Modified: Wed, 12 Apr 2023 01:14:27 GMT  
		Size: 52.2 MB (52191713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0e2e0b3634ba26d3880a8dad7170dc329234f18b5b9b38e0bd3c4637cbe27ace
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123056936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67dfa6883f98d7b82d1d95b560a9f118e646738acef237ff47081baf6ed84941`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:11 GMT
ADD file:8299e58c7e43af1f3b9fdb9bd37e3f37cf619a97ef1b87d60ca66860d646d526 in / 
# Wed, 12 Apr 2023 00:39:11 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:08:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:08:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:08:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2d15e1c2a3da7d675c2513d7ceab1d0f33ced9a82bed63d9a11ce71f1218d232`  
		Last Modified: Wed, 12 Apr 2023 00:43:07 GMT  
		Size: 51.2 MB (51206167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af123d7f5c8b1197b6040820195efacf1a57299baf71416c7a63281566cdc199`  
		Last Modified: Wed, 12 Apr 2023 01:16:15 GMT  
		Size: 8.0 MB (8034011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3af175eda8706326ac898703f9aafb47e7e08ec08318794c6838efa8f3d3bc`  
		Last Modified: Wed, 12 Apr 2023 01:16:15 GMT  
		Size: 10.3 MB (10345678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9cbd6d7217bf920da02e590f88fbfb42fb3162969840a3b17eb25c762247c04`  
		Last Modified: Wed, 12 Apr 2023 01:16:35 GMT  
		Size: 53.5 MB (53471080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:scm`

```console
$ docker pull buildpack-deps@sha256:2a03804b71d9d4c346239c8af9c9c11774ec58200bbb20c33039aeefaa07f868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:22e8a94a63b1cf94bc6e69418b975d41cb9ca48640b8b3a48002eb9c65039abb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125680982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8cd24e709af1ad98665077ad3ae2b89451839cb3a36350db232d6ce523d0d60`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:55 GMT
ADD file:f2d012660f882f319a5878a3f9ce285f488b8f90fad49ad238541cf72089e035 in / 
# Wed, 12 Apr 2023 00:19:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:50:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:51:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 07:51:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0248cf3e63c73d0e496a67807d056ca41d5e968b61087e8eca2cf4b9b4d7b99`  
		Last Modified: Wed, 12 Apr 2023 00:23:20 GMT  
		Size: 55.1 MB (55052736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127e97b4daf784e08840a21765f0d4f251192ef2994d0e4a253490f81e63955b`  
		Last Modified: Wed, 12 Apr 2023 07:57:29 GMT  
		Size: 5.2 MB (5166696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0336c50c9f6942b660e433b1086238eec37057c34b14c4e3b28bd7bf05bd84ba`  
		Last Modified: Wed, 12 Apr 2023 07:57:29 GMT  
		Size: 10.9 MB (10876749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b89f3c7f7da8adf032a33a75d1b659cee33179ecb88ea0ba75e4fc58ebe63a6`  
		Last Modified: Wed, 12 Apr 2023 07:57:46 GMT  
		Size: 54.6 MB (54584801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ea05ef84678632f8c536876f2c7f5fc619fc524fc4b7dea24106ccb4b55809a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.5 MB (120542472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640f06156014acf4823a54fa99d9d265ad6efe6eda17f48174918044c3a2ea19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:48:34 GMT
ADD file:ae13a4cbeb20b92ec29dd7409de47a964fe373bdde2a4e8880b5a4d9dc64171e in / 
# Wed, 12 Apr 2023 00:48:35 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:15:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:15:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:16:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:86cb8d774eca43d428d6a35506c172ba62358d2d5ec90c886e3b38b297f93b20`  
		Last Modified: Wed, 12 Apr 2023 00:50:46 GMT  
		Size: 52.6 MB (52555175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49db155cdf8645f599affcbbbc75eb928b0a9d010c4ac54afcfa9d7e4fa85e0`  
		Last Modified: Wed, 12 Apr 2023 01:21:15 GMT  
		Size: 5.1 MB (5072827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8936087cbd048148575fda58348506149db80a2699e99ae2042086628c0e5a38`  
		Last Modified: Wed, 12 Apr 2023 01:21:16 GMT  
		Size: 10.6 MB (10573853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0bf11569c39ee4f3d8515112046a55f14f39e54c6f0ea26271033c090f77d2`  
		Last Modified: Wed, 12 Apr 2023 01:21:35 GMT  
		Size: 52.3 MB (52340617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:bca4866a43bc982429c365a3c9eae150e257f6e85a758fa3d39d843b62e8f5a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115725058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb174836486b1bffbdfcbbc82c0c81dfa80fde95c26ad135982dde37aba1e99`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:35 GMT
ADD file:75c57df33c95251a80549b7949853df282a42bc4e5f19176764907a54b74caa9 in / 
# Tue, 11 Apr 2023 23:59:36 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:35:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:35:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4feff9b88735325634445419eaaec2ed47500b63027cfd2de34b8bc6d55ee85c`  
		Last Modified: Wed, 12 Apr 2023 00:02:57 GMT  
		Size: 50.2 MB (50216882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5f77534be142d18fb6441aad5ebb0a6b1fbd1128fee964f14c772d3f48978f`  
		Last Modified: Wed, 12 Apr 2023 09:45:07 GMT  
		Size: 4.9 MB (4934569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0797973d3ff4c7bfddd6439ceacd815ea867f868a8c75686d5b80ee1a3eca322`  
		Last Modified: Wed, 12 Apr 2023 09:45:08 GMT  
		Size: 10.2 MB (10217876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cff4fab8e209a4a8ef903baadd1f4839687988e57cef0235a447c0198ddfab`  
		Last Modified: Wed, 12 Apr 2023 09:45:28 GMT  
		Size: 50.4 MB (50355731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8932a28128c9d2abaed3ae68d2641c6738ab07bf083ca8886920e13ce37bbce3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124407974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7143247bb9728129c637c315a5d5529383d57dfbf55c6999d1479a6f6dee2b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:42 GMT
ADD file:dd3d4e5fe819950e7d01b44a29dbd790438cd722ba76198910e2597448ab0c6f in / 
# Wed, 12 Apr 2023 00:39:43 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:06:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:06:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:07:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dc80b8cdbfd36cb20231d807a50d704945d1df4da8f6e23197ccfcb629970491`  
		Last Modified: Wed, 12 Apr 2023 00:42:14 GMT  
		Size: 53.7 MB (53705529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5884e7f2c8c61aa845de4902fc29639b58861ae6c2d80bafe82082c0456c0740`  
		Last Modified: Wed, 12 Apr 2023 01:13:17 GMT  
		Size: 5.2 MB (5152752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b792b01ed3c8dc1488cd8aac41ab7d49bb17f3fa22b2e6c846078cec81a1c00`  
		Last Modified: Wed, 12 Apr 2023 01:13:17 GMT  
		Size: 10.9 MB (10873655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f993d5b17f32f4b8a535c25e182e5d8412625beee450e513ca57036e8fdd6dc`  
		Last Modified: Wed, 12 Apr 2023 01:13:34 GMT  
		Size: 54.7 MB (54676038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2af50719cfc3c1165d1e75a99045d98388d375c4dcf2cafd5526a78d50080eab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128499065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7863e942eeec226faacc53f695802b0b24e7dd766b5e4a9498a0d7c62e92c702`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:38:51 GMT
ADD file:4da7e6af0782b21849e5f6385de3589ac5b8d81d173721f9990d32da754df2cb in / 
# Wed, 12 Apr 2023 00:38:51 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:05:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:05:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:06:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b2bef40925391866903279768b0ae1e8233ef6a1aae64509a922f4aa96fe42a6`  
		Last Modified: Wed, 12 Apr 2023 00:42:19 GMT  
		Size: 56.0 MB (56032818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37ccf9a5e34ba2345ce265a9a11c93ee254e1f3616dfd1c1deda6e2f7d614c8`  
		Last Modified: Wed, 12 Apr 2023 01:14:53 GMT  
		Size: 5.3 MB (5293626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4988d5e4328f031f6884a7351766aa8a2806c9cdca38d354477fc537eaa4911f`  
		Last Modified: Wed, 12 Apr 2023 01:14:54 GMT  
		Size: 11.2 MB (11249875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660a2befd486d43a308dd1561f57efeafe1f13defd6439d34aeb5efec783ee3d`  
		Last Modified: Wed, 12 Apr 2023 01:15:17 GMT  
		Size: 55.9 MB (55922746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:cae0c78b86d9818b2acfb8edab82633baa924d1c55cf73f682790afe23194474
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122368048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e2e60633ae43426dc3b6ad6b6c990668c1e5a30f73bfab6f97a660d5d16ef9d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:09:26 GMT
ADD file:5d2c839055739fe92d64098c09607e7ec9123101d15f837c54f3688755af0c23 in / 
# Wed, 12 Apr 2023 00:09:31 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 11:00:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 11:00:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 11:02:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80243e355b05bee53c6acc45ace2cde4f7495dafe9f3f8d7d299ed51d04928d2`  
		Last Modified: Wed, 12 Apr 2023 00:16:48 GMT  
		Size: 53.3 MB (53272023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed6aed7903d464c3c421335c8a4b93f11e64b669c7eab532e87e5945fd185e2`  
		Last Modified: Wed, 12 Apr 2023 11:20:32 GMT  
		Size: 5.1 MB (5127336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af3f0065ba2217f3ef903c35f7e644bd2222c1630a96ac62477510cedfa848`  
		Last Modified: Wed, 12 Apr 2023 11:20:34 GMT  
		Size: 10.7 MB (10662154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81fa7bf218e18cc100c89241735ff424465ba8caca78835fdadafcd212de62f`  
		Last Modified: Wed, 12 Apr 2023 11:21:19 GMT  
		Size: 53.3 MB (53306535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a328c66040a29e932ae7b1d267bd4b11602af4f3cf8bf7a959c2ab0b2c7b2541
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134837330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1795d723a8d4b32e096f6732a2e5a3c212e5f6bb12ad9bb5c0e5dd1b4257eba`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:07:58 GMT
ADD file:c3c2a10473ddaa3d8a30ca99b19ad3599d0e60d826c4e0315bdb7463352ebc09 in / 
# Wed, 12 Apr 2023 00:08:02 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:31:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:32:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:33:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2d3ffdd4610a019889b845cc82b3d956ad85cca78ad4bff2d5e5522bd02c17e7`  
		Last Modified: Wed, 12 Apr 2023 00:12:37 GMT  
		Size: 58.9 MB (58926600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00772c18aacd8e2ae167f5f94b2e86c7b77fd3f7790dc5e6754e48fcce1ff484`  
		Last Modified: Wed, 12 Apr 2023 09:45:12 GMT  
		Size: 5.4 MB (5415380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1877fd565f7c580ab3b8fd343d19de69c9c3334787d6a3c93c9c21fe08ea32a`  
		Last Modified: Wed, 12 Apr 2023 09:45:13 GMT  
		Size: 11.6 MB (11629984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a24a9774fce2d157b32633fbd68d6d4777632ca49b0a35d2e9be9a2455d88b`  
		Last Modified: Wed, 12 Apr 2023 09:45:40 GMT  
		Size: 58.9 MB (58865366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:dfe7b376859cc874a19230408e2042b1d984722eca290ce8cced0e27c6bdc7bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123263942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0184582450f7852885e4f2a6aaf51c5ec9ce0ff2ce9cd9b877a945b87bfd33c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:00:25 GMT
ADD file:ab4e28724d04724a57e0f5bbe299d3361103f05ad1978dc3bfef243c1f9d6476 in / 
# Wed, 12 Apr 2023 00:00:38 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:26:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:26:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 00:27:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:042263756d7dc47bf98a243871107aa3a2b41acda91d104d8b4e148749a43dda`  
		Last Modified: Wed, 12 Apr 2023 00:05:03 GMT  
		Size: 53.3 MB (53286682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2973b8c98f9da7833ab9cd69185dd958a8939a30136cdcfedb66ce775db358ee`  
		Last Modified: Wed, 12 Apr 2023 00:32:48 GMT  
		Size: 5.1 MB (5149313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f740d13ac612bf8b6489559a7945ec1439fee2d5eba455ab0db047cd3f30a9a`  
		Last Modified: Wed, 12 Apr 2023 00:32:49 GMT  
		Size: 10.8 MB (10766104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c0067783f401b099adca196dce9e464e66236e49faba106e2f04ac73a90df7`  
		Last Modified: Wed, 12 Apr 2023 00:33:02 GMT  
		Size: 54.1 MB (54061843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:e9c192dccaeb2e1fdedf36d2dbcf10f6398bf85c6f7e932390752212375b989f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:sid` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:1cb95d972e0a2c28195432ae6f0b584389e01e1938354a98b61c2d0e4c79f44f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (350981822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9133db89f5b5ae7caee0f8cca02226caaa3b22832a67d2a4bfc68f2ca38dfccf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:55 GMT
ADD file:0936f6fccda991ba27a7f73ca61c23a436b7ca417e504b66d5a68f2283e1e81d in / 
# Wed, 12 Apr 2023 00:20:55 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:54:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:54:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 07:54:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:55:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:003dca91ec623536e08abc4e1bb2849836a84c44f82e24b97fd5423162a4d46e`  
		Last Modified: Wed, 12 Apr 2023 00:25:13 GMT  
		Size: 49.3 MB (49287652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f0b6179599c75a087e6850c42ef248d973e29a6898ed99c9bccdae08d2cd2`  
		Last Modified: Wed, 12 Apr 2023 07:59:24 GMT  
		Size: 9.1 MB (9082764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f184ca8dda7ed83dd9d21d6c880d4e15976f35814156a0a67df81423067f4b8`  
		Last Modified: Wed, 12 Apr 2023 07:59:24 GMT  
		Size: 11.4 MB (11422423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76159e5040abc54c8e269f5e87ba68551c98fa9a6a06c9d7af5eae5f9f3ee57b`  
		Last Modified: Wed, 12 Apr 2023 07:59:41 GMT  
		Size: 64.3 MB (64257071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108d0b8f8755100dc81501ff3e762f953171a4a1230223973781ad90f85c1a53`  
		Last Modified: Wed, 12 Apr 2023 08:00:14 GMT  
		Size: 216.9 MB (216931912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7c5689a7aafd87d157899f6caf4601d66e8e391aef6483970f37553b5a868314
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.5 MB (318503660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:321ba3c06205c499df306cc1b5cfded148321e0a03dea6b3028714995c1f7d03`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:48:48 GMT
ADD file:b02c911309a1b69d235b76dab369d523653c62374b0173ee9f1b65017607f9d6 in / 
# Wed, 12 Apr 2023 00:48:48 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:18:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:18:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:19:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8699c4859220eb7e4f2a5ae13e4dd5f9143cb7144e2a02a3eb381a79416524bf`  
		Last Modified: Wed, 12 Apr 2023 00:51:27 GMT  
		Size: 48.1 MB (48109671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b565bf44c40ab65f5193c4fbfd752809f50e95e2c4b2397728f42419979d7c`  
		Last Modified: Wed, 12 Apr 2023 01:22:25 GMT  
		Size: 8.5 MB (8522810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8db076a21199a98e758a14876a91c9a890bb606e6d9d483862bcb73bc5cfbb`  
		Last Modified: Wed, 12 Apr 2023 01:22:25 GMT  
		Size: 11.1 MB (11065853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466720607b58ed4036916fa9d7cb2e82a3ca95f0e5ec8e2ef908744cd3e409ec`  
		Last Modified: Wed, 12 Apr 2023 01:22:44 GMT  
		Size: 61.7 MB (61667229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df42d9b3dd685881fab45c09a19f6d1505f1612856e8b0acca62c90e5aa6457`  
		Last Modified: Wed, 12 Apr 2023 01:23:20 GMT  
		Size: 189.1 MB (189138097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:30e30ff4573c461ff2d568b1512825ef8adb8715ab6aed2656fa60ddd8018427
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.6 MB (303626296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6871b7f96f3c0576d00b1c9f421e3518c6bb2ef2dbcac9568a5daad019b0acff`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:00:33 GMT
ADD file:f8bcd71f10e7adad706b3a1685fd5c4844e3ebde65bdf9a7c004d7b9dd3520d7 in / 
# Wed, 12 Apr 2023 00:00:34 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:40:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:40:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:40:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:42:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7b0aac501774f41dc4e46815077e011ed06b86d9469c6ca28755965123669423`  
		Last Modified: Wed, 12 Apr 2023 00:04:46 GMT  
		Size: 45.9 MB (45890234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78f03ccdd59b1aad6c28d38c86bc934c8e0a1da27d7a0be742b455933d23138`  
		Last Modified: Wed, 12 Apr 2023 09:47:20 GMT  
		Size: 8.2 MB (8168595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da6afe7624e90c309b1a605bad2994526027d5e48a341ffc3ea92eb706041f2`  
		Last Modified: Wed, 12 Apr 2023 09:47:20 GMT  
		Size: 10.7 MB (10690111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59c0245364868d7a1a6302c947f5a93b4058f6e740cfb6fdb6e5bb49709f683`  
		Last Modified: Wed, 12 Apr 2023 09:47:40 GMT  
		Size: 59.4 MB (59375149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a55ffccb5d27da5f28faad7acfd1221f109589677e83ec5d087ad21a4cd46b`  
		Last Modified: Wed, 12 Apr 2023 09:48:18 GMT  
		Size: 179.5 MB (179502207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ddc7753bdf44aa12263963bdb9942af3b69f4ed4dad7430d1a9eecabd6381d97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.1 MB (342096356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e722281a223374a931912368ece55c74201c7f46e39795b84006341333ddb0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:40:21 GMT
ADD file:2784bc6dba1e1dbea293e074ebf51fa7d89cb5545ea63ba2ed75b74d067387d4 in / 
# Wed, 12 Apr 2023 00:40:22 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:10:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:10:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:10:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:11:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:43d214f7ab3ca35a0c9ed4d8cdf62b36248aba2fa1bbac4ecd64e82ba2520b70`  
		Last Modified: Wed, 12 Apr 2023 00:43:58 GMT  
		Size: 49.3 MB (49327656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99d9e5d2b2df062d16ffea4a022a4c09ce904fb96ec3fa4712a1d936593ae2a`  
		Last Modified: Wed, 12 Apr 2023 01:15:01 GMT  
		Size: 8.9 MB (8915031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd2b1a4cab3b4ac2bb4a7e9aaaa60ce806e3c49a8726f7baf5a10ba5e0e89fb`  
		Last Modified: Wed, 12 Apr 2023 01:15:01 GMT  
		Size: 11.4 MB (11389544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff14914c0381e1889d1db49b1b39da80ae3a347cf1af048e2ae0eb42aec87a12`  
		Last Modified: Wed, 12 Apr 2023 01:15:17 GMT  
		Size: 64.2 MB (64154048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f54a27824f720f86861a2776e1cc4e2f54563a9d0f0b56d1a6ec034866e3f8`  
		Last Modified: Wed, 12 Apr 2023 01:15:45 GMT  
		Size: 208.3 MB (208310077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:413efb8fbcbb35e21e9437afbee83ae1bdcf365d62cc1261952b77c46884fede
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.0 MB (352984444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e361eb5030e9416d576bb6456af5b6f82090e0ffcde0ac62558e2c5fa198c1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:51 GMT
ADD file:31710a830769b5e1f2612e1cd05380f677714bf52f61a54adbc7424087fd1378 in / 
# Wed, 12 Apr 2023 00:39:52 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:11:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:11:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:11:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:13:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:35e4af56b8bda58bf958814bc36c8e3a9a1d719c8582c0f33d7d69cc5b416211`  
		Last Modified: Wed, 12 Apr 2023 00:44:24 GMT  
		Size: 50.3 MB (50310899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145bb18c860aae65312434f79bce9d784a4824ef455202efca0f687a388037fe`  
		Last Modified: Wed, 12 Apr 2023 01:17:27 GMT  
		Size: 9.3 MB (9263774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2063c41d1dff24f54b6a7d8edde21610fe37e02b35ed369be0ccf9f64cdc43fe`  
		Last Modified: Wed, 12 Apr 2023 01:17:27 GMT  
		Size: 11.8 MB (11827096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3196dd70f259df7354dba37d732f79f68e602883ec8838b2cfcd0515de5c5c`  
		Last Modified: Wed, 12 Apr 2023 01:17:49 GMT  
		Size: 66.1 MB (66127351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc32f4359c6fe3187a1f8bab45e405139e65a8f45a4858a27e1059dd58842672`  
		Last Modified: Wed, 12 Apr 2023 01:18:36 GMT  
		Size: 215.5 MB (215455324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:885466e182139f809db3510356d10b81b0a078489b1d592c6173599161d05814
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.6 MB (327567207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5442a8ca6a5ce365db78cf474da8a69c9fcf55de9a1fe952e7df516f2f47cbe0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:10:29 GMT
ADD file:60b5ce2a691448a1aab43387ba9337b8cc193a2cbb2a01ac71f5f0cb083415ff in / 
# Wed, 12 Apr 2023 00:10:34 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 11:09:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 11:09:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 11:11:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 11:16:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:45f3dc30e8865982b1af34a4bd64597aea34350dd1bf817342cb2901014ff9a2`  
		Last Modified: Wed, 12 Apr 2023 00:18:10 GMT  
		Size: 49.3 MB (49296248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0311647062c4d77b089dceb0e1175eb800c6718e8093eee8f3b7f766f3ca545c`  
		Last Modified: Wed, 12 Apr 2023 11:23:31 GMT  
		Size: 8.4 MB (8441995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad4d6630c6fc30725f01ed1da37d38070bf8059059638cd3afdce16cabec21a7`  
		Last Modified: Wed, 12 Apr 2023 11:23:31 GMT  
		Size: 11.2 MB (11177398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f0e5f6f719dbccb2bc36692548601c776d9eebffd01feb704ac9cb58945a04`  
		Last Modified: Wed, 12 Apr 2023 11:24:21 GMT  
		Size: 63.1 MB (63101303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e65d58860ee0d917719ee8b76f31e6cc2d8c69a45c47febab4ef6badb11ce38`  
		Last Modified: Wed, 12 Apr 2023 11:26:26 GMT  
		Size: 195.6 MB (195550263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1587d433361a947d6b38a4b0800e685a14cb87316b8d23a379afaed6801a222b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.7 MB (365706334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eceff9414624c6f92e4e22e9d4c2dbacc8e477ce90ef9c2c94a6ff5a6b6e384d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:08:41 GMT
ADD file:8700846eefa6ef0670106ef8055671479d597d057ee34d1d248dbefa5977753b in / 
# Wed, 12 Apr 2023 00:08:44 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:37:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:37:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:38:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:42:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1c14c235d79599f644d6f952e975871669fe8a00e0434e5d26966f11cfb3820b`  
		Last Modified: Wed, 12 Apr 2023 00:13:39 GMT  
		Size: 53.3 MB (53291710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140d550f01a3ea4465718eae23deed53e8c34f53813fb05c7fbbd6718d137b67`  
		Last Modified: Wed, 12 Apr 2023 09:46:52 GMT  
		Size: 9.7 MB (9663547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450886794424f907ac99ffb3d1748b6d36f1ae455fbb553503d88898905d6d36`  
		Last Modified: Wed, 12 Apr 2023 09:46:52 GMT  
		Size: 12.2 MB (12184648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf2504e8cddf5044ea9695b547b876a5177d803d452f5e4e0d8050845be707d`  
		Last Modified: Wed, 12 Apr 2023 09:47:19 GMT  
		Size: 69.7 MB (69742173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cadf35097d9f51dc61a0506497f5b08804ea65f918143f059285ebe1685ced5`  
		Last Modified: Wed, 12 Apr 2023 09:48:20 GMT  
		Size: 220.8 MB (220824256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:b9c02baf674d938d6af39d2f681786407b07e39dcc6c0ef663bbfa3027bb41f6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.0 MB (361040206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcff52053934b6b9001b1f614aafda9141bd8e31a4b2680e51f8d44353d4a4ed`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:09:05 GMT
ADD file:b8c0cf42f791d92283c2c47cf2ed446fb98a7cde685c9b923c89cadb86ddad31 in / 
# Wed, 12 Apr 2023 00:09:07 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:31:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:32:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 00:35:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:43:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6178d7c3b8603b1579d72ad9f5bda8fd22627feccccd498dad946eddfe96d27a`  
		Last Modified: Wed, 12 Apr 2023 00:12:25 GMT  
		Size: 45.5 MB (45494949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd056fe810f7c94134b5c26af6939949c18bfa4868dbc9f81ea8d7a25a0daf4c`  
		Last Modified: Wed, 12 Apr 2023 00:44:01 GMT  
		Size: 8.1 MB (8117374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f8d5394c046224d62d5170fd151d4339e0f5131b1503bf3eafecefe1ec7a10`  
		Last Modified: Wed, 12 Apr 2023 00:44:01 GMT  
		Size: 10.8 MB (10794055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc0c6cc5fb9f28304c05335b3e21ed5e3cce359b94731f04cc903938689ebc19`  
		Last Modified: Wed, 12 Apr 2023 00:45:23 GMT  
		Size: 59.7 MB (59741177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16f9d49dc3af209b4bcf7ce13172c2a5a76516c0d39580db79da7b27eaf387f`  
		Last Modified: Wed, 12 Apr 2023 00:50:51 GMT  
		Size: 236.9 MB (236892651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9287c8095d9220df2f988981ac641e97e22f861d9bd87aa2a19a9e6cf396a687
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.0 MB (319011191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914264ef0379c6c6c2f67b9eb3fd0e99ffc0016a3f81cb006225180ad93d3a77`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:01:19 GMT
ADD file:0593fbca11f3d4a9b2b916ee99bb70651af04ea1275262f12e9b0e5c07e81f0e in / 
# Wed, 12 Apr 2023 00:01:29 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:28:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:28:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 00:28:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:29:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1844a6b5cc32e25703d3a6ac2115866157b1f856d7463d0dca8443fea51061f1`  
		Last Modified: Wed, 12 Apr 2023 00:05:31 GMT  
		Size: 47.7 MB (47665068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f306dc6c45f3e2637390b46a2dce7fb061bb8be6ae7c72c47bba97d84b99d256`  
		Last Modified: Wed, 12 Apr 2023 00:33:37 GMT  
		Size: 8.7 MB (8713548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7676682574fe22f1cac8016a4f36ad54898c4313e0609a7e88e75e035e32444b`  
		Last Modified: Wed, 12 Apr 2023 00:33:36 GMT  
		Size: 11.3 MB (11288124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de3f9748f029581dd4821ad6e7d4da7ab4a31600128a2411dda2639c9b92fe58`  
		Last Modified: Wed, 12 Apr 2023 00:33:51 GMT  
		Size: 63.3 MB (63260422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81adcc7796eb9dd6b2ccee5b41b08f31d903a15caab787b2edc99367e1c15497`  
		Last Modified: Wed, 12 Apr 2023 00:34:19 GMT  
		Size: 188.1 MB (188084029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:f8cb8daba973c30f3ebe59cc75c94f38d1352e658bf22265d425182d2e509f78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:162b0f4bf898e2f30f86c124dae307c51fcefaf8e30eba8f3d0538d5b88b1533
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69792839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:895c4767319db895fdd9034df03472e20114f0f8c5ae8c9ce85f116db05635b8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:55 GMT
ADD file:0936f6fccda991ba27a7f73ca61c23a436b7ca417e504b66d5a68f2283e1e81d in / 
# Wed, 12 Apr 2023 00:20:55 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:54:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:54:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:003dca91ec623536e08abc4e1bb2849836a84c44f82e24b97fd5423162a4d46e`  
		Last Modified: Wed, 12 Apr 2023 00:25:13 GMT  
		Size: 49.3 MB (49287652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f0b6179599c75a087e6850c42ef248d973e29a6898ed99c9bccdae08d2cd2`  
		Last Modified: Wed, 12 Apr 2023 07:59:24 GMT  
		Size: 9.1 MB (9082764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f184ca8dda7ed83dd9d21d6c880d4e15976f35814156a0a67df81423067f4b8`  
		Last Modified: Wed, 12 Apr 2023 07:59:24 GMT  
		Size: 11.4 MB (11422423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:8b516bb4199218b93e0828691cca7924741a8012ef412cd89ec797180b9ad014
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67698334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9438faefdd9540401ef284f3ce81a1c9c2829d48e27358bfaecfb65aedfa6e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:48:48 GMT
ADD file:b02c911309a1b69d235b76dab369d523653c62374b0173ee9f1b65017607f9d6 in / 
# Wed, 12 Apr 2023 00:48:48 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:18:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8699c4859220eb7e4f2a5ae13e4dd5f9143cb7144e2a02a3eb381a79416524bf`  
		Last Modified: Wed, 12 Apr 2023 00:51:27 GMT  
		Size: 48.1 MB (48109671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b565bf44c40ab65f5193c4fbfd752809f50e95e2c4b2397728f42419979d7c`  
		Last Modified: Wed, 12 Apr 2023 01:22:25 GMT  
		Size: 8.5 MB (8522810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8db076a21199a98e758a14876a91c9a890bb606e6d9d483862bcb73bc5cfbb`  
		Last Modified: Wed, 12 Apr 2023 01:22:25 GMT  
		Size: 11.1 MB (11065853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a1e3bbf1c55a5464c86a292f106703c74891fbfa001f613d40d655e93bd9bede
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64748940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9173a08df38173e6306894fae0aa76e6f71dd6c980d9610d7cc52026a4ece2e7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:00:33 GMT
ADD file:f8bcd71f10e7adad706b3a1685fd5c4844e3ebde65bdf9a7c004d7b9dd3520d7 in / 
# Wed, 12 Apr 2023 00:00:34 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:40:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:40:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:7b0aac501774f41dc4e46815077e011ed06b86d9469c6ca28755965123669423`  
		Last Modified: Wed, 12 Apr 2023 00:04:46 GMT  
		Size: 45.9 MB (45890234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78f03ccdd59b1aad6c28d38c86bc934c8e0a1da27d7a0be742b455933d23138`  
		Last Modified: Wed, 12 Apr 2023 09:47:20 GMT  
		Size: 8.2 MB (8168595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da6afe7624e90c309b1a605bad2994526027d5e48a341ffc3ea92eb706041f2`  
		Last Modified: Wed, 12 Apr 2023 09:47:20 GMT  
		Size: 10.7 MB (10690111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c3e4535c3a32e860c9cdcb87e33d91d91a05de0caebac0e396b682b23449f890
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69632231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59a19733f90d03e40a3a26aa25904ff3dd15a57aa3bc07c4723ab3a166147dc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:40:21 GMT
ADD file:2784bc6dba1e1dbea293e074ebf51fa7d89cb5545ea63ba2ed75b74d067387d4 in / 
# Wed, 12 Apr 2023 00:40:22 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:10:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:10:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:43d214f7ab3ca35a0c9ed4d8cdf62b36248aba2fa1bbac4ecd64e82ba2520b70`  
		Last Modified: Wed, 12 Apr 2023 00:43:58 GMT  
		Size: 49.3 MB (49327656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99d9e5d2b2df062d16ffea4a022a4c09ce904fb96ec3fa4712a1d936593ae2a`  
		Last Modified: Wed, 12 Apr 2023 01:15:01 GMT  
		Size: 8.9 MB (8915031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd2b1a4cab3b4ac2bb4a7e9aaaa60ce806e3c49a8726f7baf5a10ba5e0e89fb`  
		Last Modified: Wed, 12 Apr 2023 01:15:01 GMT  
		Size: 11.4 MB (11389544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7fd624c3066dfa1ca3da4f7665c730788104cdc2cb90f94fe839582a1a20bff9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71401769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10d2d9289ea8eef61411b36e3c5358bc3e57f93d19422a12cdce3b5d7d7e922d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:51 GMT
ADD file:31710a830769b5e1f2612e1cd05380f677714bf52f61a54adbc7424087fd1378 in / 
# Wed, 12 Apr 2023 00:39:52 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:11:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:11:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:35e4af56b8bda58bf958814bc36c8e3a9a1d719c8582c0f33d7d69cc5b416211`  
		Last Modified: Wed, 12 Apr 2023 00:44:24 GMT  
		Size: 50.3 MB (50310899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145bb18c860aae65312434f79bce9d784a4824ef455202efca0f687a388037fe`  
		Last Modified: Wed, 12 Apr 2023 01:17:27 GMT  
		Size: 9.3 MB (9263774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2063c41d1dff24f54b6a7d8edde21610fe37e02b35ed369be0ccf9f64cdc43fe`  
		Last Modified: Wed, 12 Apr 2023 01:17:27 GMT  
		Size: 11.8 MB (11827096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:628533752353ab5e8a3f84261cb7c6e11db611d071e8d45ea918ba12085f4c61
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68915641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d997660f9947209900669cfd7ee82e565be22d4bce90cf6ee7ddc2b5ae238304`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:10:29 GMT
ADD file:60b5ce2a691448a1aab43387ba9337b8cc193a2cbb2a01ac71f5f0cb083415ff in / 
# Wed, 12 Apr 2023 00:10:34 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 11:09:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 11:09:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:45f3dc30e8865982b1af34a4bd64597aea34350dd1bf817342cb2901014ff9a2`  
		Last Modified: Wed, 12 Apr 2023 00:18:10 GMT  
		Size: 49.3 MB (49296248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0311647062c4d77b089dceb0e1175eb800c6718e8093eee8f3b7f766f3ca545c`  
		Last Modified: Wed, 12 Apr 2023 11:23:31 GMT  
		Size: 8.4 MB (8441995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad4d6630c6fc30725f01ed1da37d38070bf8059059638cd3afdce16cabec21a7`  
		Last Modified: Wed, 12 Apr 2023 11:23:31 GMT  
		Size: 11.2 MB (11177398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d3deb81ed361a658e6300eef9c948a9e31cb0c6fba12d79abc858df84a2113a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75139905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8d4b5ad4e2fe62ee02f64ca2b0eaa429bec6abebf8d5b731058ffd2e8f32d76`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:08:41 GMT
ADD file:8700846eefa6ef0670106ef8055671479d597d057ee34d1d248dbefa5977753b in / 
# Wed, 12 Apr 2023 00:08:44 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:37:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:37:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:1c14c235d79599f644d6f952e975871669fe8a00e0434e5d26966f11cfb3820b`  
		Last Modified: Wed, 12 Apr 2023 00:13:39 GMT  
		Size: 53.3 MB (53291710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140d550f01a3ea4465718eae23deed53e8c34f53813fb05c7fbbd6718d137b67`  
		Last Modified: Wed, 12 Apr 2023 09:46:52 GMT  
		Size: 9.7 MB (9663547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450886794424f907ac99ffb3d1748b6d36f1ae455fbb553503d88898905d6d36`  
		Last Modified: Wed, 12 Apr 2023 09:46:52 GMT  
		Size: 12.2 MB (12184648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:b6ecdf5c65f021e05c80106a2cc8a598f2fb062039c62b358a2a42fc40f3d4d8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64406378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfc1ea8528f7edf3edcdff9fd62663fec45eaf492953562405ce7f8504695160`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:09:05 GMT
ADD file:b8c0cf42f791d92283c2c47cf2ed446fb98a7cde685c9b923c89cadb86ddad31 in / 
# Wed, 12 Apr 2023 00:09:07 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:31:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:32:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:6178d7c3b8603b1579d72ad9f5bda8fd22627feccccd498dad946eddfe96d27a`  
		Last Modified: Wed, 12 Apr 2023 00:12:25 GMT  
		Size: 45.5 MB (45494949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd056fe810f7c94134b5c26af6939949c18bfa4868dbc9f81ea8d7a25a0daf4c`  
		Last Modified: Wed, 12 Apr 2023 00:44:01 GMT  
		Size: 8.1 MB (8117374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f8d5394c046224d62d5170fd151d4339e0f5131b1503bf3eafecefe1ec7a10`  
		Last Modified: Wed, 12 Apr 2023 00:44:01 GMT  
		Size: 10.8 MB (10794055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2a32ff0d5208b6ad040a9cb58b776824b3c95030e002745b9128549a0e88a98e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67666740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d98184dbb030d39270ec3b57dcd40af7dc1cb4c8755f6afe805779ab651c12`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:01:19 GMT
ADD file:0593fbca11f3d4a9b2b916ee99bb70651af04ea1275262f12e9b0e5c07e81f0e in / 
# Wed, 12 Apr 2023 00:01:29 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:28:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:28:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:1844a6b5cc32e25703d3a6ac2115866157b1f856d7463d0dca8443fea51061f1`  
		Last Modified: Wed, 12 Apr 2023 00:05:31 GMT  
		Size: 47.7 MB (47665068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f306dc6c45f3e2637390b46a2dce7fb061bb8be6ae7c72c47bba97d84b99d256`  
		Last Modified: Wed, 12 Apr 2023 00:33:37 GMT  
		Size: 8.7 MB (8713548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7676682574fe22f1cac8016a4f36ad54898c4313e0609a7e88e75e035e32444b`  
		Last Modified: Wed, 12 Apr 2023 00:33:36 GMT  
		Size: 11.3 MB (11288124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:ab9b4b0c7793beb83665883122683e2f0f6d28df1c5857c6e90413b1a333a8a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:sid-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d9f6278d7e0c871b5bcdc327298a29c7c00a8a0504891c4ad2631c374b75a01c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134049910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd617366d1cce33570b6dcf04f7eac2404f89e0bece798cb7e973cbd704f667`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:55 GMT
ADD file:0936f6fccda991ba27a7f73ca61c23a436b7ca417e504b66d5a68f2283e1e81d in / 
# Wed, 12 Apr 2023 00:20:55 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:54:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:54:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 07:54:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:003dca91ec623536e08abc4e1bb2849836a84c44f82e24b97fd5423162a4d46e`  
		Last Modified: Wed, 12 Apr 2023 00:25:13 GMT  
		Size: 49.3 MB (49287652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f0b6179599c75a087e6850c42ef248d973e29a6898ed99c9bccdae08d2cd2`  
		Last Modified: Wed, 12 Apr 2023 07:59:24 GMT  
		Size: 9.1 MB (9082764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f184ca8dda7ed83dd9d21d6c880d4e15976f35814156a0a67df81423067f4b8`  
		Last Modified: Wed, 12 Apr 2023 07:59:24 GMT  
		Size: 11.4 MB (11422423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76159e5040abc54c8e269f5e87ba68551c98fa9a6a06c9d7af5eae5f9f3ee57b`  
		Last Modified: Wed, 12 Apr 2023 07:59:41 GMT  
		Size: 64.3 MB (64257071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c0b4a3eae58bd274c266cb60478e79df6446cb058ebcb7beec816064f9c69b75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129365563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b15a5f5bf525f6d5ed1af6bc9d3b44768864d1199c3f26e961d670e918851d7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:48:48 GMT
ADD file:b02c911309a1b69d235b76dab369d523653c62374b0173ee9f1b65017607f9d6 in / 
# Wed, 12 Apr 2023 00:48:48 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:18:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:18:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8699c4859220eb7e4f2a5ae13e4dd5f9143cb7144e2a02a3eb381a79416524bf`  
		Last Modified: Wed, 12 Apr 2023 00:51:27 GMT  
		Size: 48.1 MB (48109671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b565bf44c40ab65f5193c4fbfd752809f50e95e2c4b2397728f42419979d7c`  
		Last Modified: Wed, 12 Apr 2023 01:22:25 GMT  
		Size: 8.5 MB (8522810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8db076a21199a98e758a14876a91c9a890bb606e6d9d483862bcb73bc5cfbb`  
		Last Modified: Wed, 12 Apr 2023 01:22:25 GMT  
		Size: 11.1 MB (11065853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466720607b58ed4036916fa9d7cb2e82a3ca95f0e5ec8e2ef908744cd3e409ec`  
		Last Modified: Wed, 12 Apr 2023 01:22:44 GMT  
		Size: 61.7 MB (61667229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4625cae1cb86a704920cb5e233396ab0915f8f8aea6c2991bf83dc37494e5707
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 MB (124124089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a34df020edfcb54003832698a6fd1b0d2df01b8d86feaa47193d84801d022ab7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:00:33 GMT
ADD file:f8bcd71f10e7adad706b3a1685fd5c4844e3ebde65bdf9a7c004d7b9dd3520d7 in / 
# Wed, 12 Apr 2023 00:00:34 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:40:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:40:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:40:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7b0aac501774f41dc4e46815077e011ed06b86d9469c6ca28755965123669423`  
		Last Modified: Wed, 12 Apr 2023 00:04:46 GMT  
		Size: 45.9 MB (45890234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78f03ccdd59b1aad6c28d38c86bc934c8e0a1da27d7a0be742b455933d23138`  
		Last Modified: Wed, 12 Apr 2023 09:47:20 GMT  
		Size: 8.2 MB (8168595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da6afe7624e90c309b1a605bad2994526027d5e48a341ffc3ea92eb706041f2`  
		Last Modified: Wed, 12 Apr 2023 09:47:20 GMT  
		Size: 10.7 MB (10690111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59c0245364868d7a1a6302c947f5a93b4058f6e740cfb6fdb6e5bb49709f683`  
		Last Modified: Wed, 12 Apr 2023 09:47:40 GMT  
		Size: 59.4 MB (59375149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:909145f5f8b9a67acd7be2b62e379fe6c15950dee01727de50e4cc961c962502
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133786279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c7d9c27ae042d56e7ca69c21a7a5a690294d166c8196d78574264d9160d8957`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:40:21 GMT
ADD file:2784bc6dba1e1dbea293e074ebf51fa7d89cb5545ea63ba2ed75b74d067387d4 in / 
# Wed, 12 Apr 2023 00:40:22 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:10:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:10:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:10:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:43d214f7ab3ca35a0c9ed4d8cdf62b36248aba2fa1bbac4ecd64e82ba2520b70`  
		Last Modified: Wed, 12 Apr 2023 00:43:58 GMT  
		Size: 49.3 MB (49327656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99d9e5d2b2df062d16ffea4a022a4c09ce904fb96ec3fa4712a1d936593ae2a`  
		Last Modified: Wed, 12 Apr 2023 01:15:01 GMT  
		Size: 8.9 MB (8915031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd2b1a4cab3b4ac2bb4a7e9aaaa60ce806e3c49a8726f7baf5a10ba5e0e89fb`  
		Last Modified: Wed, 12 Apr 2023 01:15:01 GMT  
		Size: 11.4 MB (11389544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff14914c0381e1889d1db49b1b39da80ae3a347cf1af048e2ae0eb42aec87a12`  
		Last Modified: Wed, 12 Apr 2023 01:15:17 GMT  
		Size: 64.2 MB (64154048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:8e5134589fb0e6d388a1a4741142104956636747431cf809398cd58520b6da78
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137529120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc693ca7c37b5ced8d79a021265f81c4cecbc277909bb33bb103fd1302a0b37`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:51 GMT
ADD file:31710a830769b5e1f2612e1cd05380f677714bf52f61a54adbc7424087fd1378 in / 
# Wed, 12 Apr 2023 00:39:52 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:11:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:11:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:11:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:35e4af56b8bda58bf958814bc36c8e3a9a1d719c8582c0f33d7d69cc5b416211`  
		Last Modified: Wed, 12 Apr 2023 00:44:24 GMT  
		Size: 50.3 MB (50310899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145bb18c860aae65312434f79bce9d784a4824ef455202efca0f687a388037fe`  
		Last Modified: Wed, 12 Apr 2023 01:17:27 GMT  
		Size: 9.3 MB (9263774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2063c41d1dff24f54b6a7d8edde21610fe37e02b35ed369be0ccf9f64cdc43fe`  
		Last Modified: Wed, 12 Apr 2023 01:17:27 GMT  
		Size: 11.8 MB (11827096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3196dd70f259df7354dba37d732f79f68e602883ec8838b2cfcd0515de5c5c`  
		Last Modified: Wed, 12 Apr 2023 01:17:49 GMT  
		Size: 66.1 MB (66127351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:14ec2fad7148b576e923bf9b355b0735a20034441088f6ed8ba3d942adafc96f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132016944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20304a399e5ecc0f6c31f60f0cfc8c882574dba660ad45ace353b0f7c64b2af8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:10:29 GMT
ADD file:60b5ce2a691448a1aab43387ba9337b8cc193a2cbb2a01ac71f5f0cb083415ff in / 
# Wed, 12 Apr 2023 00:10:34 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 11:09:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 11:09:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 11:11:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:45f3dc30e8865982b1af34a4bd64597aea34350dd1bf817342cb2901014ff9a2`  
		Last Modified: Wed, 12 Apr 2023 00:18:10 GMT  
		Size: 49.3 MB (49296248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0311647062c4d77b089dceb0e1175eb800c6718e8093eee8f3b7f766f3ca545c`  
		Last Modified: Wed, 12 Apr 2023 11:23:31 GMT  
		Size: 8.4 MB (8441995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad4d6630c6fc30725f01ed1da37d38070bf8059059638cd3afdce16cabec21a7`  
		Last Modified: Wed, 12 Apr 2023 11:23:31 GMT  
		Size: 11.2 MB (11177398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f0e5f6f719dbccb2bc36692548601c776d9eebffd01feb704ac9cb58945a04`  
		Last Modified: Wed, 12 Apr 2023 11:24:21 GMT  
		Size: 63.1 MB (63101303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8135b2f23a71e776729d178ad2c044b029e434a6d8851c6db2bcf9c99af46c83
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.9 MB (144882078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1217c66cbb148d338fc6383d0543b5e72c22f88e67d1ad1e01886b46dfed4a7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:08:41 GMT
ADD file:8700846eefa6ef0670106ef8055671479d597d057ee34d1d248dbefa5977753b in / 
# Wed, 12 Apr 2023 00:08:44 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:37:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:37:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:38:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1c14c235d79599f644d6f952e975871669fe8a00e0434e5d26966f11cfb3820b`  
		Last Modified: Wed, 12 Apr 2023 00:13:39 GMT  
		Size: 53.3 MB (53291710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140d550f01a3ea4465718eae23deed53e8c34f53813fb05c7fbbd6718d137b67`  
		Last Modified: Wed, 12 Apr 2023 09:46:52 GMT  
		Size: 9.7 MB (9663547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450886794424f907ac99ffb3d1748b6d36f1ae455fbb553503d88898905d6d36`  
		Last Modified: Wed, 12 Apr 2023 09:46:52 GMT  
		Size: 12.2 MB (12184648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf2504e8cddf5044ea9695b547b876a5177d803d452f5e4e0d8050845be707d`  
		Last Modified: Wed, 12 Apr 2023 09:47:19 GMT  
		Size: 69.7 MB (69742173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:bcd300a4e07d706f2fd9f306c4c32864622137e94ae3c3c4670ea905ee0beff3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 MB (124147555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397d717b57a8049a3da1ad949d9ed38c1e6d2518bf8f6c629c18545c03f04445`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:09:05 GMT
ADD file:b8c0cf42f791d92283c2c47cf2ed446fb98a7cde685c9b923c89cadb86ddad31 in / 
# Wed, 12 Apr 2023 00:09:07 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:31:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:32:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 00:35:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6178d7c3b8603b1579d72ad9f5bda8fd22627feccccd498dad946eddfe96d27a`  
		Last Modified: Wed, 12 Apr 2023 00:12:25 GMT  
		Size: 45.5 MB (45494949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd056fe810f7c94134b5c26af6939949c18bfa4868dbc9f81ea8d7a25a0daf4c`  
		Last Modified: Wed, 12 Apr 2023 00:44:01 GMT  
		Size: 8.1 MB (8117374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f8d5394c046224d62d5170fd151d4339e0f5131b1503bf3eafecefe1ec7a10`  
		Last Modified: Wed, 12 Apr 2023 00:44:01 GMT  
		Size: 10.8 MB (10794055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc0c6cc5fb9f28304c05335b3e21ed5e3cce359b94731f04cc903938689ebc19`  
		Last Modified: Wed, 12 Apr 2023 00:45:23 GMT  
		Size: 59.7 MB (59741177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ab7bb732a3d488865f2b887c55fbefc2e0041d528429e377f1f5ee84b43bda25
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130927162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dba9e0d63f399d18f4d3f0cd3f58b4eee0e1d16c71d855c9f9b0bd4e250d67b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:01:19 GMT
ADD file:0593fbca11f3d4a9b2b916ee99bb70651af04ea1275262f12e9b0e5c07e81f0e in / 
# Wed, 12 Apr 2023 00:01:29 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:28:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:28:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 00:28:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1844a6b5cc32e25703d3a6ac2115866157b1f856d7463d0dca8443fea51061f1`  
		Last Modified: Wed, 12 Apr 2023 00:05:31 GMT  
		Size: 47.7 MB (47665068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f306dc6c45f3e2637390b46a2dce7fb061bb8be6ae7c72c47bba97d84b99d256`  
		Last Modified: Wed, 12 Apr 2023 00:33:37 GMT  
		Size: 8.7 MB (8713548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7676682574fe22f1cac8016a4f36ad54898c4313e0609a7e88e75e035e32444b`  
		Last Modified: Wed, 12 Apr 2023 00:33:36 GMT  
		Size: 11.3 MB (11288124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de3f9748f029581dd4821ad6e7d4da7ab4a31600128a2411dda2639c9b92fe58`  
		Last Modified: Wed, 12 Apr 2023 00:33:51 GMT  
		Size: 63.3 MB (63260422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:stable`

```console
$ docker pull buildpack-deps@sha256:695fd9e1f58574422eece085006690b3110abb0d304260024d40775b95c6056e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:stable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4156d4c78d3e29a9aa11a5528a08847352e66895bb0a75cec05f4d43752fb8f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.5 MB (322492485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09bd8b383fcae8260115c949f68a3ccbe1df72567c4e1ad6f53b72329c1c5e1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:55 GMT
ADD file:f2d012660f882f319a5878a3f9ce285f488b8f90fad49ad238541cf72089e035 in / 
# Wed, 12 Apr 2023 00:19:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:50:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:51:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 07:51:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:52:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0248cf3e63c73d0e496a67807d056ca41d5e968b61087e8eca2cf4b9b4d7b99`  
		Last Modified: Wed, 12 Apr 2023 00:23:20 GMT  
		Size: 55.1 MB (55052736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127e97b4daf784e08840a21765f0d4f251192ef2994d0e4a253490f81e63955b`  
		Last Modified: Wed, 12 Apr 2023 07:57:29 GMT  
		Size: 5.2 MB (5166696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0336c50c9f6942b660e433b1086238eec37057c34b14c4e3b28bd7bf05bd84ba`  
		Last Modified: Wed, 12 Apr 2023 07:57:29 GMT  
		Size: 10.9 MB (10876749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b89f3c7f7da8adf032a33a75d1b659cee33179ecb88ea0ba75e4fc58ebe63a6`  
		Last Modified: Wed, 12 Apr 2023 07:57:46 GMT  
		Size: 54.6 MB (54584801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d62772179761f8fddfaed03ed2bdf7078b103b193d18d79a9b49364830d56cf`  
		Last Modified: Wed, 12 Apr 2023 07:58:19 GMT  
		Size: 196.8 MB (196811503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:5307e4d5147eb64f430d2a521eee4a5504ed8c4a0d7d98aa81c28190c2c963d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.6 MB (295551904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62bc4c385631ea22e58568f3c02e7102b4f9f8f5a1ebb96d7e82bf8764dbecae`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:48:34 GMT
ADD file:ae13a4cbeb20b92ec29dd7409de47a964fe373bdde2a4e8880b5a4d9dc64171e in / 
# Wed, 12 Apr 2023 00:48:35 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:15:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:15:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:16:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:17:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:86cb8d774eca43d428d6a35506c172ba62358d2d5ec90c886e3b38b297f93b20`  
		Last Modified: Wed, 12 Apr 2023 00:50:46 GMT  
		Size: 52.6 MB (52555175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49db155cdf8645f599affcbbbc75eb928b0a9d010c4ac54afcfa9d7e4fa85e0`  
		Last Modified: Wed, 12 Apr 2023 01:21:15 GMT  
		Size: 5.1 MB (5072827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8936087cbd048148575fda58348506149db80a2699e99ae2042086628c0e5a38`  
		Last Modified: Wed, 12 Apr 2023 01:21:16 GMT  
		Size: 10.6 MB (10573853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0bf11569c39ee4f3d8515112046a55f14f39e54c6f0ea26271033c090f77d2`  
		Last Modified: Wed, 12 Apr 2023 01:21:35 GMT  
		Size: 52.3 MB (52340617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:622390f39404d88752f248bc2136a55baca97d5324d43689204df0157d284282`  
		Last Modified: Wed, 12 Apr 2023 01:22:13 GMT  
		Size: 175.0 MB (175009432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:14544dda30d13c761bb7bfb4d7fdffb2d3abd01a303373a2bcb846940b12680d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (283013417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f5b3339637b4c0d3912ef6cd818266179b085a40521f419e38c9546b616ee3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:35 GMT
ADD file:75c57df33c95251a80549b7949853df282a42bc4e5f19176764907a54b74caa9 in / 
# Tue, 11 Apr 2023 23:59:36 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:35:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:35:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:37:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4feff9b88735325634445419eaaec2ed47500b63027cfd2de34b8bc6d55ee85c`  
		Last Modified: Wed, 12 Apr 2023 00:02:57 GMT  
		Size: 50.2 MB (50216882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5f77534be142d18fb6441aad5ebb0a6b1fbd1128fee964f14c772d3f48978f`  
		Last Modified: Wed, 12 Apr 2023 09:45:07 GMT  
		Size: 4.9 MB (4934569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0797973d3ff4c7bfddd6439ceacd815ea867f868a8c75686d5b80ee1a3eca322`  
		Last Modified: Wed, 12 Apr 2023 09:45:08 GMT  
		Size: 10.2 MB (10217876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cff4fab8e209a4a8ef903baadd1f4839687988e57cef0235a447c0198ddfab`  
		Last Modified: Wed, 12 Apr 2023 09:45:28 GMT  
		Size: 50.4 MB (50355731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c442c38966496f089bcee5c78d8e7321764a2a679fd64f1070215e5f24b6d872`  
		Last Modified: Wed, 12 Apr 2023 09:46:04 GMT  
		Size: 167.3 MB (167288359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e7277cb741804ffe9213d32a419f6738ef4494fbd33db9326b55282dfbc1dd6b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314135667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c57708eddbf78525fe399f52d71e35653f6c3298641025d07fcc3323777584`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:42 GMT
ADD file:dd3d4e5fe819950e7d01b44a29dbd790438cd722ba76198910e2597448ab0c6f in / 
# Wed, 12 Apr 2023 00:39:43 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:06:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:06:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:07:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:08:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dc80b8cdbfd36cb20231d807a50d704945d1df4da8f6e23197ccfcb629970491`  
		Last Modified: Wed, 12 Apr 2023 00:42:14 GMT  
		Size: 53.7 MB (53705529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5884e7f2c8c61aa845de4902fc29639b58861ae6c2d80bafe82082c0456c0740`  
		Last Modified: Wed, 12 Apr 2023 01:13:17 GMT  
		Size: 5.2 MB (5152752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b792b01ed3c8dc1488cd8aac41ab7d49bb17f3fa22b2e6c846078cec81a1c00`  
		Last Modified: Wed, 12 Apr 2023 01:13:17 GMT  
		Size: 10.9 MB (10873655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f993d5b17f32f4b8a535c25e182e5d8412625beee450e513ca57036e8fdd6dc`  
		Last Modified: Wed, 12 Apr 2023 01:13:34 GMT  
		Size: 54.7 MB (54676038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26edf98ece5babdb6b65e76738cef2c2d05e7075161753d3ba95cd84480d211`  
		Last Modified: Wed, 12 Apr 2023 01:14:02 GMT  
		Size: 189.7 MB (189727693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ff274b300c58e39b8abdacecdee25d47651abe32a696616b92656ca392bd5d21
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.2 MB (328223380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5eee57e4ddbeaa9219392349db2bc711541f424d58a97b4a86ad5bd768ff773`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:38:51 GMT
ADD file:4da7e6af0782b21849e5f6385de3589ac5b8d81d173721f9990d32da754df2cb in / 
# Wed, 12 Apr 2023 00:38:51 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:05:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:05:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:06:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:07:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b2bef40925391866903279768b0ae1e8233ef6a1aae64509a922f4aa96fe42a6`  
		Last Modified: Wed, 12 Apr 2023 00:42:19 GMT  
		Size: 56.0 MB (56032818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37ccf9a5e34ba2345ce265a9a11c93ee254e1f3616dfd1c1deda6e2f7d614c8`  
		Last Modified: Wed, 12 Apr 2023 01:14:53 GMT  
		Size: 5.3 MB (5293626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4988d5e4328f031f6884a7351766aa8a2806c9cdca38d354477fc537eaa4911f`  
		Last Modified: Wed, 12 Apr 2023 01:14:54 GMT  
		Size: 11.2 MB (11249875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660a2befd486d43a308dd1561f57efeafe1f13defd6439d34aeb5efec783ee3d`  
		Last Modified: Wed, 12 Apr 2023 01:15:17 GMT  
		Size: 55.9 MB (55922746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f09985282f12d05c5724bcbb0481a94f66820112bafc34a1d990dfdf74a52fc`  
		Last Modified: Wed, 12 Apr 2023 01:16:02 GMT  
		Size: 199.7 MB (199724315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:733073a5e45e28ac1efdd031f70eb14ea95adc6350a95cd5eec6e4289ad5726c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301296282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb9d52fa12ccd33943e746e02c6d998737105a5b221ed73b5860e5137600578`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:09:26 GMT
ADD file:5d2c839055739fe92d64098c09607e7ec9123101d15f837c54f3688755af0c23 in / 
# Wed, 12 Apr 2023 00:09:31 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 11:00:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 11:00:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 11:02:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 11:08:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80243e355b05bee53c6acc45ace2cde4f7495dafe9f3f8d7d299ed51d04928d2`  
		Last Modified: Wed, 12 Apr 2023 00:16:48 GMT  
		Size: 53.3 MB (53272023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed6aed7903d464c3c421335c8a4b93f11e64b669c7eab532e87e5945fd185e2`  
		Last Modified: Wed, 12 Apr 2023 11:20:32 GMT  
		Size: 5.1 MB (5127336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af3f0065ba2217f3ef903c35f7e644bd2222c1630a96ac62477510cedfa848`  
		Last Modified: Wed, 12 Apr 2023 11:20:34 GMT  
		Size: 10.7 MB (10662154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81fa7bf218e18cc100c89241735ff424465ba8caca78835fdadafcd212de62f`  
		Last Modified: Wed, 12 Apr 2023 11:21:19 GMT  
		Size: 53.3 MB (53306535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f17002a316d921b7e863e4fa717c4354ebce8cf57671d9a2bf8f34dec378d8c`  
		Last Modified: Wed, 12 Apr 2023 11:23:14 GMT  
		Size: 178.9 MB (178928234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5b39e218d6f9e9f7c2241165c5f3ff812622a74d175997245e60615626e2508a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.0 MB (330997339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b69805860c4cc4b90cbcdadb6ab37298c1d198c92781fef2c1ca29f434eae34b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:07:58 GMT
ADD file:c3c2a10473ddaa3d8a30ca99b19ad3599d0e60d826c4e0315bdb7463352ebc09 in / 
# Wed, 12 Apr 2023 00:08:02 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:31:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:32:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:33:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:36:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2d3ffdd4610a019889b845cc82b3d956ad85cca78ad4bff2d5e5522bd02c17e7`  
		Last Modified: Wed, 12 Apr 2023 00:12:37 GMT  
		Size: 58.9 MB (58926600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00772c18aacd8e2ae167f5f94b2e86c7b77fd3f7790dc5e6754e48fcce1ff484`  
		Last Modified: Wed, 12 Apr 2023 09:45:12 GMT  
		Size: 5.4 MB (5415380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1877fd565f7c580ab3b8fd343d19de69c9c3334787d6a3c93c9c21fe08ea32a`  
		Last Modified: Wed, 12 Apr 2023 09:45:13 GMT  
		Size: 11.6 MB (11629984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a24a9774fce2d157b32633fbd68d6d4777632ca49b0a35d2e9be9a2455d88b`  
		Last Modified: Wed, 12 Apr 2023 09:45:40 GMT  
		Size: 58.9 MB (58865366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d134f385b05ace42f019d92548a9dd6708f9ae2ee3269131645b4ff67b2463`  
		Last Modified: Wed, 12 Apr 2023 09:46:38 GMT  
		Size: 196.2 MB (196160009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:478709c66fdeffea827bb22297605067d97172933185294b18da02b3b071e7a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296079415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62811c5341c95a39adc789318a1ba301b0fae01b6b77e3b4a63a1693c43fa76d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:00:25 GMT
ADD file:ab4e28724d04724a57e0f5bbe299d3361103f05ad1978dc3bfef243c1f9d6476 in / 
# Wed, 12 Apr 2023 00:00:38 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:26:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:26:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 00:27:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:28:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:042263756d7dc47bf98a243871107aa3a2b41acda91d104d8b4e148749a43dda`  
		Last Modified: Wed, 12 Apr 2023 00:05:03 GMT  
		Size: 53.3 MB (53286682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2973b8c98f9da7833ab9cd69185dd958a8939a30136cdcfedb66ce775db358ee`  
		Last Modified: Wed, 12 Apr 2023 00:32:48 GMT  
		Size: 5.1 MB (5149313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f740d13ac612bf8b6489559a7945ec1439fee2d5eba455ab0db047cd3f30a9a`  
		Last Modified: Wed, 12 Apr 2023 00:32:49 GMT  
		Size: 10.8 MB (10766104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c0067783f401b099adca196dce9e464e66236e49faba106e2f04ac73a90df7`  
		Last Modified: Wed, 12 Apr 2023 00:33:02 GMT  
		Size: 54.1 MB (54061843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1b5accdd9fd68a290692e1a0a3d853312f236ae0463540b5fdd97d598cc7a6`  
		Last Modified: Wed, 12 Apr 2023 00:33:28 GMT  
		Size: 172.8 MB (172815473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:b77ca637508f0f6f5d834c57f2e6af153c2ce4a48afb439b5fb469529360a951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:stable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:acd62d4d9773006a9d0acddc08a4cbf7637d1c975e67459b52a7dc093bdfc271
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71096181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af19f7b630d3d79df60c6a9ae3051940c35c240094ef6e54f4f7843577467896`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:55 GMT
ADD file:f2d012660f882f319a5878a3f9ce285f488b8f90fad49ad238541cf72089e035 in / 
# Wed, 12 Apr 2023 00:19:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:50:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:51:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b0248cf3e63c73d0e496a67807d056ca41d5e968b61087e8eca2cf4b9b4d7b99`  
		Last Modified: Wed, 12 Apr 2023 00:23:20 GMT  
		Size: 55.1 MB (55052736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127e97b4daf784e08840a21765f0d4f251192ef2994d0e4a253490f81e63955b`  
		Last Modified: Wed, 12 Apr 2023 07:57:29 GMT  
		Size: 5.2 MB (5166696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0336c50c9f6942b660e433b1086238eec37057c34b14c4e3b28bd7bf05bd84ba`  
		Last Modified: Wed, 12 Apr 2023 07:57:29 GMT  
		Size: 10.9 MB (10876749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:03091d90e79cf371dee743c2a8537556060a22246a5c1a68d53f63e201715f4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68201855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39fd3f1fac0693a3efcdf720af9216deb72c54ed024f9c8edfa061944f26d405`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:48:34 GMT
ADD file:ae13a4cbeb20b92ec29dd7409de47a964fe373bdde2a4e8880b5a4d9dc64171e in / 
# Wed, 12 Apr 2023 00:48:35 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:15:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:15:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:86cb8d774eca43d428d6a35506c172ba62358d2d5ec90c886e3b38b297f93b20`  
		Last Modified: Wed, 12 Apr 2023 00:50:46 GMT  
		Size: 52.6 MB (52555175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49db155cdf8645f599affcbbbc75eb928b0a9d010c4ac54afcfa9d7e4fa85e0`  
		Last Modified: Wed, 12 Apr 2023 01:21:15 GMT  
		Size: 5.1 MB (5072827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8936087cbd048148575fda58348506149db80a2699e99ae2042086628c0e5a38`  
		Last Modified: Wed, 12 Apr 2023 01:21:16 GMT  
		Size: 10.6 MB (10573853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a8434b10032012c2760d715f731aa184a425b42164650c42161de37dd78702cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65369327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475e074940bc42bc670d7bf9b9fb35f58ef5e44c093fb372fa6b177c75f785cc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:35 GMT
ADD file:75c57df33c95251a80549b7949853df282a42bc4e5f19176764907a54b74caa9 in / 
# Tue, 11 Apr 2023 23:59:36 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:35:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:4feff9b88735325634445419eaaec2ed47500b63027cfd2de34b8bc6d55ee85c`  
		Last Modified: Wed, 12 Apr 2023 00:02:57 GMT  
		Size: 50.2 MB (50216882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5f77534be142d18fb6441aad5ebb0a6b1fbd1128fee964f14c772d3f48978f`  
		Last Modified: Wed, 12 Apr 2023 09:45:07 GMT  
		Size: 4.9 MB (4934569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0797973d3ff4c7bfddd6439ceacd815ea867f868a8c75686d5b80ee1a3eca322`  
		Last Modified: Wed, 12 Apr 2023 09:45:08 GMT  
		Size: 10.2 MB (10217876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a5537c32568d575a5a3bb0f96138a7cf42dc7d590729308b1ed7538fbdd433e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69731936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0130b5aae27ce4286f62ae8a2e5324e811b8d862aa0aea6923a7b461615ccf17`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:42 GMT
ADD file:dd3d4e5fe819950e7d01b44a29dbd790438cd722ba76198910e2597448ab0c6f in / 
# Wed, 12 Apr 2023 00:39:43 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:06:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:06:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:dc80b8cdbfd36cb20231d807a50d704945d1df4da8f6e23197ccfcb629970491`  
		Last Modified: Wed, 12 Apr 2023 00:42:14 GMT  
		Size: 53.7 MB (53705529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5884e7f2c8c61aa845de4902fc29639b58861ae6c2d80bafe82082c0456c0740`  
		Last Modified: Wed, 12 Apr 2023 01:13:17 GMT  
		Size: 5.2 MB (5152752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b792b01ed3c8dc1488cd8aac41ab7d49bb17f3fa22b2e6c846078cec81a1c00`  
		Last Modified: Wed, 12 Apr 2023 01:13:17 GMT  
		Size: 10.9 MB (10873655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:39321899797ed2861f1e87a3547e2e911faa2ce033098728aa240b793dd8232b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72576319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1535cd25f9ea155765a6cae9f83a5e50a533888ddb926700a119b7e91a0a0f1b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:38:51 GMT
ADD file:4da7e6af0782b21849e5f6385de3589ac5b8d81d173721f9990d32da754df2cb in / 
# Wed, 12 Apr 2023 00:38:51 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:05:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:05:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b2bef40925391866903279768b0ae1e8233ef6a1aae64509a922f4aa96fe42a6`  
		Last Modified: Wed, 12 Apr 2023 00:42:19 GMT  
		Size: 56.0 MB (56032818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37ccf9a5e34ba2345ce265a9a11c93ee254e1f3616dfd1c1deda6e2f7d614c8`  
		Last Modified: Wed, 12 Apr 2023 01:14:53 GMT  
		Size: 5.3 MB (5293626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4988d5e4328f031f6884a7351766aa8a2806c9cdca38d354477fc537eaa4911f`  
		Last Modified: Wed, 12 Apr 2023 01:14:54 GMT  
		Size: 11.2 MB (11249875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:66e9ab47759b918c5d7fec7837bf41e0032b99600e25a33827f94b51355e46e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69061513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6925f09cbf336d4383b178072c72886c41699bb1743ff950dfc483a88c39a928`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:09:26 GMT
ADD file:5d2c839055739fe92d64098c09607e7ec9123101d15f837c54f3688755af0c23 in / 
# Wed, 12 Apr 2023 00:09:31 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 11:00:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 11:00:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:80243e355b05bee53c6acc45ace2cde4f7495dafe9f3f8d7d299ed51d04928d2`  
		Last Modified: Wed, 12 Apr 2023 00:16:48 GMT  
		Size: 53.3 MB (53272023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed6aed7903d464c3c421335c8a4b93f11e64b669c7eab532e87e5945fd185e2`  
		Last Modified: Wed, 12 Apr 2023 11:20:32 GMT  
		Size: 5.1 MB (5127336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af3f0065ba2217f3ef903c35f7e644bd2222c1630a96ac62477510cedfa848`  
		Last Modified: Wed, 12 Apr 2023 11:20:34 GMT  
		Size: 10.7 MB (10662154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d2bf2a378307a21bf35bbc234fd0768bf348c2aa8d28c3ee065b4248dcbfa2d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (75971964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17ee001184461420ef6a9dcaa8006e2702365c6fb83c1ea64e12ef337924ac12`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:07:58 GMT
ADD file:c3c2a10473ddaa3d8a30ca99b19ad3599d0e60d826c4e0315bdb7463352ebc09 in / 
# Wed, 12 Apr 2023 00:08:02 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:31:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:32:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2d3ffdd4610a019889b845cc82b3d956ad85cca78ad4bff2d5e5522bd02c17e7`  
		Last Modified: Wed, 12 Apr 2023 00:12:37 GMT  
		Size: 58.9 MB (58926600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00772c18aacd8e2ae167f5f94b2e86c7b77fd3f7790dc5e6754e48fcce1ff484`  
		Last Modified: Wed, 12 Apr 2023 09:45:12 GMT  
		Size: 5.4 MB (5415380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1877fd565f7c580ab3b8fd343d19de69c9c3334787d6a3c93c9c21fe08ea32a`  
		Last Modified: Wed, 12 Apr 2023 09:45:13 GMT  
		Size: 11.6 MB (11629984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5726b9b13d1328b42898380f57612273babbfe94f7918919e3553ca203957c96
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69202099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d3f520b42352a1bbcb04c9c67c162e7870ac7063005e1cbfb804dea99188dc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:00:25 GMT
ADD file:ab4e28724d04724a57e0f5bbe299d3361103f05ad1978dc3bfef243c1f9d6476 in / 
# Wed, 12 Apr 2023 00:00:38 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:26:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:26:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:042263756d7dc47bf98a243871107aa3a2b41acda91d104d8b4e148749a43dda`  
		Last Modified: Wed, 12 Apr 2023 00:05:03 GMT  
		Size: 53.3 MB (53286682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2973b8c98f9da7833ab9cd69185dd958a8939a30136cdcfedb66ce775db358ee`  
		Last Modified: Wed, 12 Apr 2023 00:32:48 GMT  
		Size: 5.1 MB (5149313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f740d13ac612bf8b6489559a7945ec1439fee2d5eba455ab0db047cd3f30a9a`  
		Last Modified: Wed, 12 Apr 2023 00:32:49 GMT  
		Size: 10.8 MB (10766104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:stable-scm`

```console
$ docker pull buildpack-deps@sha256:2a03804b71d9d4c346239c8af9c9c11774ec58200bbb20c33039aeefaa07f868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:stable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:22e8a94a63b1cf94bc6e69418b975d41cb9ca48640b8b3a48002eb9c65039abb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125680982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8cd24e709af1ad98665077ad3ae2b89451839cb3a36350db232d6ce523d0d60`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:55 GMT
ADD file:f2d012660f882f319a5878a3f9ce285f488b8f90fad49ad238541cf72089e035 in / 
# Wed, 12 Apr 2023 00:19:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:50:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:51:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 07:51:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0248cf3e63c73d0e496a67807d056ca41d5e968b61087e8eca2cf4b9b4d7b99`  
		Last Modified: Wed, 12 Apr 2023 00:23:20 GMT  
		Size: 55.1 MB (55052736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127e97b4daf784e08840a21765f0d4f251192ef2994d0e4a253490f81e63955b`  
		Last Modified: Wed, 12 Apr 2023 07:57:29 GMT  
		Size: 5.2 MB (5166696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0336c50c9f6942b660e433b1086238eec37057c34b14c4e3b28bd7bf05bd84ba`  
		Last Modified: Wed, 12 Apr 2023 07:57:29 GMT  
		Size: 10.9 MB (10876749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b89f3c7f7da8adf032a33a75d1b659cee33179ecb88ea0ba75e4fc58ebe63a6`  
		Last Modified: Wed, 12 Apr 2023 07:57:46 GMT  
		Size: 54.6 MB (54584801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ea05ef84678632f8c536876f2c7f5fc619fc524fc4b7dea24106ccb4b55809a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.5 MB (120542472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640f06156014acf4823a54fa99d9d265ad6efe6eda17f48174918044c3a2ea19`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:48:34 GMT
ADD file:ae13a4cbeb20b92ec29dd7409de47a964fe373bdde2a4e8880b5a4d9dc64171e in / 
# Wed, 12 Apr 2023 00:48:35 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:15:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:15:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:16:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:86cb8d774eca43d428d6a35506c172ba62358d2d5ec90c886e3b38b297f93b20`  
		Last Modified: Wed, 12 Apr 2023 00:50:46 GMT  
		Size: 52.6 MB (52555175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49db155cdf8645f599affcbbbc75eb928b0a9d010c4ac54afcfa9d7e4fa85e0`  
		Last Modified: Wed, 12 Apr 2023 01:21:15 GMT  
		Size: 5.1 MB (5072827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8936087cbd048148575fda58348506149db80a2699e99ae2042086628c0e5a38`  
		Last Modified: Wed, 12 Apr 2023 01:21:16 GMT  
		Size: 10.6 MB (10573853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0bf11569c39ee4f3d8515112046a55f14f39e54c6f0ea26271033c090f77d2`  
		Last Modified: Wed, 12 Apr 2023 01:21:35 GMT  
		Size: 52.3 MB (52340617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:bca4866a43bc982429c365a3c9eae150e257f6e85a758fa3d39d843b62e8f5a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115725058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb174836486b1bffbdfcbbc82c0c81dfa80fde95c26ad135982dde37aba1e99`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:35 GMT
ADD file:75c57df33c95251a80549b7949853df282a42bc4e5f19176764907a54b74caa9 in / 
# Tue, 11 Apr 2023 23:59:36 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:35:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:35:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4feff9b88735325634445419eaaec2ed47500b63027cfd2de34b8bc6d55ee85c`  
		Last Modified: Wed, 12 Apr 2023 00:02:57 GMT  
		Size: 50.2 MB (50216882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5f77534be142d18fb6441aad5ebb0a6b1fbd1128fee964f14c772d3f48978f`  
		Last Modified: Wed, 12 Apr 2023 09:45:07 GMT  
		Size: 4.9 MB (4934569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0797973d3ff4c7bfddd6439ceacd815ea867f868a8c75686d5b80ee1a3eca322`  
		Last Modified: Wed, 12 Apr 2023 09:45:08 GMT  
		Size: 10.2 MB (10217876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cff4fab8e209a4a8ef903baadd1f4839687988e57cef0235a447c0198ddfab`  
		Last Modified: Wed, 12 Apr 2023 09:45:28 GMT  
		Size: 50.4 MB (50355731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8932a28128c9d2abaed3ae68d2641c6738ab07bf083ca8886920e13ce37bbce3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124407974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7143247bb9728129c637c315a5d5529383d57dfbf55c6999d1479a6f6dee2b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:42 GMT
ADD file:dd3d4e5fe819950e7d01b44a29dbd790438cd722ba76198910e2597448ab0c6f in / 
# Wed, 12 Apr 2023 00:39:43 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:06:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:06:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:07:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dc80b8cdbfd36cb20231d807a50d704945d1df4da8f6e23197ccfcb629970491`  
		Last Modified: Wed, 12 Apr 2023 00:42:14 GMT  
		Size: 53.7 MB (53705529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5884e7f2c8c61aa845de4902fc29639b58861ae6c2d80bafe82082c0456c0740`  
		Last Modified: Wed, 12 Apr 2023 01:13:17 GMT  
		Size: 5.2 MB (5152752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b792b01ed3c8dc1488cd8aac41ab7d49bb17f3fa22b2e6c846078cec81a1c00`  
		Last Modified: Wed, 12 Apr 2023 01:13:17 GMT  
		Size: 10.9 MB (10873655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f993d5b17f32f4b8a535c25e182e5d8412625beee450e513ca57036e8fdd6dc`  
		Last Modified: Wed, 12 Apr 2023 01:13:34 GMT  
		Size: 54.7 MB (54676038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2af50719cfc3c1165d1e75a99045d98388d375c4dcf2cafd5526a78d50080eab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128499065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7863e942eeec226faacc53f695802b0b24e7dd766b5e4a9498a0d7c62e92c702`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:38:51 GMT
ADD file:4da7e6af0782b21849e5f6385de3589ac5b8d81d173721f9990d32da754df2cb in / 
# Wed, 12 Apr 2023 00:38:51 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:05:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:05:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:06:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b2bef40925391866903279768b0ae1e8233ef6a1aae64509a922f4aa96fe42a6`  
		Last Modified: Wed, 12 Apr 2023 00:42:19 GMT  
		Size: 56.0 MB (56032818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37ccf9a5e34ba2345ce265a9a11c93ee254e1f3616dfd1c1deda6e2f7d614c8`  
		Last Modified: Wed, 12 Apr 2023 01:14:53 GMT  
		Size: 5.3 MB (5293626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4988d5e4328f031f6884a7351766aa8a2806c9cdca38d354477fc537eaa4911f`  
		Last Modified: Wed, 12 Apr 2023 01:14:54 GMT  
		Size: 11.2 MB (11249875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660a2befd486d43a308dd1561f57efeafe1f13defd6439d34aeb5efec783ee3d`  
		Last Modified: Wed, 12 Apr 2023 01:15:17 GMT  
		Size: 55.9 MB (55922746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:cae0c78b86d9818b2acfb8edab82633baa924d1c55cf73f682790afe23194474
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122368048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e2e60633ae43426dc3b6ad6b6c990668c1e5a30f73bfab6f97a660d5d16ef9d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:09:26 GMT
ADD file:5d2c839055739fe92d64098c09607e7ec9123101d15f837c54f3688755af0c23 in / 
# Wed, 12 Apr 2023 00:09:31 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 11:00:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 11:00:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 11:02:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80243e355b05bee53c6acc45ace2cde4f7495dafe9f3f8d7d299ed51d04928d2`  
		Last Modified: Wed, 12 Apr 2023 00:16:48 GMT  
		Size: 53.3 MB (53272023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed6aed7903d464c3c421335c8a4b93f11e64b669c7eab532e87e5945fd185e2`  
		Last Modified: Wed, 12 Apr 2023 11:20:32 GMT  
		Size: 5.1 MB (5127336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af3f0065ba2217f3ef903c35f7e644bd2222c1630a96ac62477510cedfa848`  
		Last Modified: Wed, 12 Apr 2023 11:20:34 GMT  
		Size: 10.7 MB (10662154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81fa7bf218e18cc100c89241735ff424465ba8caca78835fdadafcd212de62f`  
		Last Modified: Wed, 12 Apr 2023 11:21:19 GMT  
		Size: 53.3 MB (53306535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a328c66040a29e932ae7b1d267bd4b11602af4f3cf8bf7a959c2ab0b2c7b2541
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134837330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1795d723a8d4b32e096f6732a2e5a3c212e5f6bb12ad9bb5c0e5dd1b4257eba`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:07:58 GMT
ADD file:c3c2a10473ddaa3d8a30ca99b19ad3599d0e60d826c4e0315bdb7463352ebc09 in / 
# Wed, 12 Apr 2023 00:08:02 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:31:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:32:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:33:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2d3ffdd4610a019889b845cc82b3d956ad85cca78ad4bff2d5e5522bd02c17e7`  
		Last Modified: Wed, 12 Apr 2023 00:12:37 GMT  
		Size: 58.9 MB (58926600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00772c18aacd8e2ae167f5f94b2e86c7b77fd3f7790dc5e6754e48fcce1ff484`  
		Last Modified: Wed, 12 Apr 2023 09:45:12 GMT  
		Size: 5.4 MB (5415380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1877fd565f7c580ab3b8fd343d19de69c9c3334787d6a3c93c9c21fe08ea32a`  
		Last Modified: Wed, 12 Apr 2023 09:45:13 GMT  
		Size: 11.6 MB (11629984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a24a9774fce2d157b32633fbd68d6d4777632ca49b0a35d2e9be9a2455d88b`  
		Last Modified: Wed, 12 Apr 2023 09:45:40 GMT  
		Size: 58.9 MB (58865366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:dfe7b376859cc874a19230408e2042b1d984722eca290ce8cced0e27c6bdc7bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123263942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0184582450f7852885e4f2a6aaf51c5ec9ce0ff2ce9cd9b877a945b87bfd33c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:00:25 GMT
ADD file:ab4e28724d04724a57e0f5bbe299d3361103f05ad1978dc3bfef243c1f9d6476 in / 
# Wed, 12 Apr 2023 00:00:38 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:26:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:26:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 00:27:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:042263756d7dc47bf98a243871107aa3a2b41acda91d104d8b4e148749a43dda`  
		Last Modified: Wed, 12 Apr 2023 00:05:03 GMT  
		Size: 53.3 MB (53286682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2973b8c98f9da7833ab9cd69185dd958a8939a30136cdcfedb66ce775db358ee`  
		Last Modified: Wed, 12 Apr 2023 00:32:48 GMT  
		Size: 5.1 MB (5149313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f740d13ac612bf8b6489559a7945ec1439fee2d5eba455ab0db047cd3f30a9a`  
		Last Modified: Wed, 12 Apr 2023 00:32:49 GMT  
		Size: 10.8 MB (10766104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c0067783f401b099adca196dce9e464e66236e49faba106e2f04ac73a90df7`  
		Last Modified: Wed, 12 Apr 2023 00:33:02 GMT  
		Size: 54.1 MB (54061843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:f95b9908ce0e8045cd9bd8a2fe52392ff1cbe65f1656d5a78931ecdc23feb7eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d2831f26a1be4155a536403a4091c9fa3578d932016713ad45c204a54ef9bbe0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.9 MB (345874026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8740ff589a8566528392543b04f5042041d597aebdf89a8351ad91a78b3c798`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:35 GMT
ADD file:1cb6c660a2e3ea14b2a11bb8b80f53920c3da423a0ad7004391bfab4db4d0177 in / 
# Wed, 12 Apr 2023 00:19:36 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:48:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:49:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 07:49:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:50:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cc556c281183180fae02d57fa6fb60ed0a99d9040936278743dc4022bfb0c686`  
		Last Modified: Wed, 12 Apr 2023 00:22:48 GMT  
		Size: 49.3 MB (49292938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8022b43d7c31d74c341d297cf10031ff0c51f596473a0c1945ee83a841094638`  
		Last Modified: Wed, 12 Apr 2023 07:56:29 GMT  
		Size: 9.1 MB (9083160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db75f726ec67539c4823cb16851963ebe5838a853b0e769fd662020fad918781`  
		Last Modified: Wed, 12 Apr 2023 07:56:29 GMT  
		Size: 11.4 MB (11422437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8a9e299258b84de99d6d739eb84b5b1632005f9c7723f2dd9e209fb1a8aaa3`  
		Last Modified: Wed, 12 Apr 2023 07:56:46 GMT  
		Size: 64.1 MB (64097699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5269c0251f891649bf20972368b34411b22208df54ce5c4b1b9eb649793edbb`  
		Last Modified: Wed, 12 Apr 2023 07:57:20 GMT  
		Size: 212.0 MB (211977792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ca3000a5c2c81e15247951e66c081c65117913ded0f177159d6c15adf29997c5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.6 MB (314581039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7816bfe042349b0c7c87b9c180f83b2294e7e688a27afa564c62ce1bbbe48fa1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:48:19 GMT
ADD file:df1103dce44baa95c92287ab5016f36d5cc45c6062116ebf5273f7e79a00915c in / 
# Wed, 12 Apr 2023 00:48:20 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:11:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:11:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:12:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:15:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:795c0ca2726dffdb0e5ef6ffa341d17ec672d5915011f1a93a05e8c95a4779ae`  
		Last Modified: Wed, 12 Apr 2023 00:50:12 GMT  
		Size: 48.1 MB (48110879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e70c1a23fdf0fd320a61a2506f0ca4a391a319de8403734e4af8d678a6081fc`  
		Last Modified: Wed, 12 Apr 2023 01:20:09 GMT  
		Size: 8.5 MB (8523001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27111cd5fb1057675f2e0b269790dc264d344d6e4b7ad92ff941f90a496167b`  
		Last Modified: Wed, 12 Apr 2023 01:20:09 GMT  
		Size: 11.1 MB (11065924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ed8d7f4b0f78246beda91a51ddbc4ab368fe6f04bb2432498c3f5a76cbc010`  
		Last Modified: Wed, 12 Apr 2023 01:20:30 GMT  
		Size: 61.5 MB (61541287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e7bffea89dcea5595c3a9d4dcd9ae2c5876dacb4265050ed658554b4d6da420`  
		Last Modified: Wed, 12 Apr 2023 01:21:06 GMT  
		Size: 185.3 MB (185339948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a95980932c697cd75fe78313b6c518454ecebe4a2a0e247d9f1e6210eb31e041
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.9 MB (299884114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f23b6bbc84faa85b393ae1cdc942b366a444b75550e6e70cffe1fa7b80024b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:10 GMT
ADD file:aa1c08333544c05fc5317d775ee99af7479c6fa5f35b74652f6126a7a5099958 in / 
# Tue, 11 Apr 2023 23:59:11 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:32:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:32:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:32:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:35:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:81b1dd69f2a38ad14b0919ab9c395aafeb137158539ab6531ac5743690a0ebb7`  
		Last Modified: Wed, 12 Apr 2023 00:02:26 GMT  
		Size: 45.9 MB (45883114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f399f5abf6c810daac72b311feda8726e38c0c228183ccf5d0da4de0b8ec79f4`  
		Last Modified: Wed, 12 Apr 2023 09:43:59 GMT  
		Size: 8.2 MB (8169132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3453014a13bae733f0a1d38594c31a25841303277602f61394efaff085c42288`  
		Last Modified: Wed, 12 Apr 2023 09:43:59 GMT  
		Size: 10.7 MB (10690179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1d5c89a8ad9820582b69420d902dbb04e78a440ab16e42dd52a5778aea37e4`  
		Last Modified: Wed, 12 Apr 2023 09:44:19 GMT  
		Size: 59.2 MB (59247424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac4f8fdeee401c8aa14952b7737a316db27f53eb8c98736aeefa5111187e4c5`  
		Last Modified: Wed, 12 Apr 2023 09:44:56 GMT  
		Size: 175.9 MB (175894265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:93e13c1041833e26336a9a4362a935021cb140f05c425f7cda66b1d288da141d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.0 MB (337000447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4817e1bdddcea21ae977e3e5b270332950842257559a3ae2efe4a18f83f1110e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:27 GMT
ADD file:efed18ef2a003bff7e64e7049455216e51876402083581032c35085328e416f6 in / 
# Wed, 12 Apr 2023 00:39:28 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:04:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:04:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:04:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:06:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0f987ce91d920ae0a705ed6c9824f1bbbfa282defb8986614030eb8e2bc0b4e`  
		Last Modified: Wed, 12 Apr 2023 00:41:45 GMT  
		Size: 49.3 MB (49345365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e6a618ee06e99ebfbb7809c1cc4902cb717d294243f3765f170fd1c8eaf94a`  
		Last Modified: Wed, 12 Apr 2023 01:12:23 GMT  
		Size: 8.9 MB (8915044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59c3f19470d2fd9e1407a7ddcbac3c316a999a143865347f221db18517e0838`  
		Last Modified: Wed, 12 Apr 2023 01:12:24 GMT  
		Size: 11.4 MB (11389565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b373ae05bf678c385bace283c65197a2bbc2a334c528ed7b58a01d93131de585`  
		Last Modified: Wed, 12 Apr 2023 01:12:39 GMT  
		Size: 64.0 MB (63974624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a4f590cd785a4e380e2e92cca3c7b2d82be15d89bb52da582994cc39d9bdd5`  
		Last Modified: Wed, 12 Apr 2023 01:13:07 GMT  
		Size: 203.4 MB (203375849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:34c578f8d193ff514ac530b8922a3055877b2d87cc4e289f31e765c7450ed112
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.4 MB (348376060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7d23d91b6b9538e488de01d18982225f2c00d113996363a9198e3a7dc32c14`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:38:30 GMT
ADD file:7718865253a3489583d40f8c7a7beede0c20cebbab68bb3e97ad2e84082afcb7 in / 
# Wed, 12 Apr 2023 00:38:30 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:02:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:02:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:03:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:05:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a4ce9e81f634822e5166ef3eef875a4140795ac18afe0391433d72c7865bf67b`  
		Last Modified: Wed, 12 Apr 2023 00:41:43 GMT  
		Size: 50.3 MB (50317977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e54183fe5cb0866f886a93c0d098d38e649286a2b516b64d9658dd40f5d74b`  
		Last Modified: Wed, 12 Apr 2023 01:13:34 GMT  
		Size: 9.3 MB (9264042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76896a8c48193a86329dc809066c177aedc76d55811eb32ca7c80c1ab06f66f1`  
		Last Modified: Wed, 12 Apr 2023 01:13:34 GMT  
		Size: 11.8 MB (11827045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba7e1ed0df9a2a8a6501d91360cea22ab988653bf057d73c44ecb41e49f6151`  
		Last Modified: Wed, 12 Apr 2023 01:13:56 GMT  
		Size: 66.0 MB (65960427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4551baecfb99d1499518d7ef04818e3c6d649ec19322e320b452af6855389592`  
		Last Modified: Wed, 12 Apr 2023 01:14:43 GMT  
		Size: 211.0 MB (211006569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:23311ac289d337013971c368b465b0986aaed3f32cdbb0a775d92e4772069c65
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.4 MB (322418858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40969785f199073c1927d0b7134dd5fac42485fedf7eeacac9d143b89abac0ef`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:08:16 GMT
ADD file:6a525220124da7146a3c356cc57678f3b8d7c6e9299febaaebd5b5a005f1325c in / 
# Wed, 12 Apr 2023 00:08:21 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 10:49:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 10:50:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 10:52:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 10:59:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b6bdb9410f81554043d19e5ae83249eaa10ffe038db54932946c7d9eaccc8b96`  
		Last Modified: Wed, 12 Apr 2023 00:15:35 GMT  
		Size: 49.3 MB (49299322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71852747f2b9b21534b53c60a706551ff2aae26334aec4b70c4920fe9fb4f8c`  
		Last Modified: Wed, 12 Apr 2023 11:17:26 GMT  
		Size: 8.4 MB (8442270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb9aa6963a60e7aad5662c525f6bbd5202ae82472a684135f6111f1f7d3318e`  
		Last Modified: Wed, 12 Apr 2023 11:17:26 GMT  
		Size: 11.2 MB (11177314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324e348066ac545280d6c0f59d4c327df571da3bc37b52136ddfcb88f5e93d87`  
		Last Modified: Wed, 12 Apr 2023 11:18:17 GMT  
		Size: 62.9 MB (62939755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0043323f2473139490f98ebdaec70e638f66c8d9c516af7709dfde6cee5dc31`  
		Last Modified: Wed, 12 Apr 2023 11:20:20 GMT  
		Size: 190.6 MB (190560197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0209217507f6f357a8082281a14e968862d9d1681ccf30ff783642fad4ec9f85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.9 MB (359860373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb042a9f5f9e7c0af296066c675f6d6e2628f8c26edb13164760d5bd193064b5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:07:22 GMT
ADD file:b747fc06f7ee1d3e19fc9cf3aa83e6ab4caa056a72d230caf616e67849bfe112 in / 
# Wed, 12 Apr 2023 00:07:25 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:24:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:25:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:26:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:31:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8314f03b76ec928732612641a4f8420e3c4c25719b48503230bf6c03979aeb2e`  
		Last Modified: Wed, 12 Apr 2023 00:11:50 GMT  
		Size: 53.3 MB (53299984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823af2d3550f6b52577dc50d69a272726b10382b4fae65d06e3b7196165e42d5`  
		Last Modified: Wed, 12 Apr 2023 09:43:31 GMT  
		Size: 9.7 MB (9663796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f73dc4aed694f9f90cd285bb10ed1d4652e9e29ca42e3ae9b7e2148cb39b812`  
		Last Modified: Wed, 12 Apr 2023 09:43:31 GMT  
		Size: 12.2 MB (12184513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1002e389de5d993e4a73f7cf4311d2ac394084c1570912d013506d78ea334895`  
		Last Modified: Wed, 12 Apr 2023 09:43:59 GMT  
		Size: 69.6 MB (69558417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7bbfd7ef8d272f24c3ac1b3965ec076e9d3cecb875f224158e1384609161ad7`  
		Last Modified: Wed, 12 Apr 2023 09:45:01 GMT  
		Size: 215.2 MB (215153663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f3ab35ffe09db7e9be153f5725015386c28800e98cb51a46e7c57187d5a0e602
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.8 MB (314808227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7150ecfe845b425b67f772c301e8610bfca04fb6c670705d638bd01b5dd34bb1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:19 GMT
ADD file:5d2b35b45a0f23e2f2e93f9c311eb34a92e4591ea27979236d801e512d44cb85 in / 
# Tue, 11 Apr 2023 23:59:31 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:24:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:24:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 00:25:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:26:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8a09cd2374da8355612e7d4c91d55107a3f089816ae52b2c91b9e08e6a895ab1`  
		Last Modified: Wed, 12 Apr 2023 00:04:39 GMT  
		Size: 47.7 MB (47670407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d047361c12b2aeb253b1923b053dcc960101b3b3348af8f15f95f7fda2b89e4`  
		Last Modified: Wed, 12 Apr 2023 00:32:00 GMT  
		Size: 8.7 MB (8713846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a462d218c24c21390b32ace449f4f47a57624b858dc05a37c31cb7f6e21c41`  
		Last Modified: Wed, 12 Apr 2023 00:32:00 GMT  
		Size: 11.3 MB (11288081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628da1a495c0341f28b24cb228c4984d7d8a718059c95991d67739f4a4602e4b`  
		Last Modified: Wed, 12 Apr 2023 00:32:14 GMT  
		Size: 63.1 MB (63101451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e16abe3590f67fe9ba9faa6530081d422098a3dabb4fd1cb81b378a88316bf`  
		Last Modified: Wed, 12 Apr 2023 00:32:42 GMT  
		Size: 184.0 MB (184034442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:33e2a1a1bc1160b1cec89c4ba8b9b95ab439c6d5c554bd5fd41889a695a77f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:6a036620bf66ab7f03f891595654eae2995b8a08bb32443b8e130fa87c26c2b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69798535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95348693c13cd4b3237dba422f5d46f3c7b727c7c451791d70fb9f93a80800b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:35 GMT
ADD file:1cb6c660a2e3ea14b2a11bb8b80f53920c3da423a0ad7004391bfab4db4d0177 in / 
# Wed, 12 Apr 2023 00:19:36 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:48:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:49:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:cc556c281183180fae02d57fa6fb60ed0a99d9040936278743dc4022bfb0c686`  
		Last Modified: Wed, 12 Apr 2023 00:22:48 GMT  
		Size: 49.3 MB (49292938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8022b43d7c31d74c341d297cf10031ff0c51f596473a0c1945ee83a841094638`  
		Last Modified: Wed, 12 Apr 2023 07:56:29 GMT  
		Size: 9.1 MB (9083160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db75f726ec67539c4823cb16851963ebe5838a853b0e769fd662020fad918781`  
		Last Modified: Wed, 12 Apr 2023 07:56:29 GMT  
		Size: 11.4 MB (11422437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:66ba8371e61af6282fc38b6060f0c069dfedce71185d25e520e1124503a36408
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67699804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc6c4cd7610510c3dbf367553fdb3b3d67108a1c4f5fef96d4fccbb8635f2db`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:48:19 GMT
ADD file:df1103dce44baa95c92287ab5016f36d5cc45c6062116ebf5273f7e79a00915c in / 
# Wed, 12 Apr 2023 00:48:20 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:11:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:11:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:795c0ca2726dffdb0e5ef6ffa341d17ec672d5915011f1a93a05e8c95a4779ae`  
		Last Modified: Wed, 12 Apr 2023 00:50:12 GMT  
		Size: 48.1 MB (48110879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e70c1a23fdf0fd320a61a2506f0ca4a391a319de8403734e4af8d678a6081fc`  
		Last Modified: Wed, 12 Apr 2023 01:20:09 GMT  
		Size: 8.5 MB (8523001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27111cd5fb1057675f2e0b269790dc264d344d6e4b7ad92ff941f90a496167b`  
		Last Modified: Wed, 12 Apr 2023 01:20:09 GMT  
		Size: 11.1 MB (11065924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b289f68e3841fe69e7989c97ee56cf9d1fd5e6c40aeee876b5ed49d24196349f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64742425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb40b9cc3e34bc48896c67a00695947a3ba4c4f9994a7add99e9ef2f171754d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:10 GMT
ADD file:aa1c08333544c05fc5317d775ee99af7479c6fa5f35b74652f6126a7a5099958 in / 
# Tue, 11 Apr 2023 23:59:11 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:32:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:32:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:81b1dd69f2a38ad14b0919ab9c395aafeb137158539ab6531ac5743690a0ebb7`  
		Last Modified: Wed, 12 Apr 2023 00:02:26 GMT  
		Size: 45.9 MB (45883114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f399f5abf6c810daac72b311feda8726e38c0c228183ccf5d0da4de0b8ec79f4`  
		Last Modified: Wed, 12 Apr 2023 09:43:59 GMT  
		Size: 8.2 MB (8169132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3453014a13bae733f0a1d38594c31a25841303277602f61394efaff085c42288`  
		Last Modified: Wed, 12 Apr 2023 09:43:59 GMT  
		Size: 10.7 MB (10690179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:03a892b4f8141b6f3f3c1d36591ec20f5abf8e7db913d6b06bef0195f59ada5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69649974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c5127fd80af5e1e2f2405e7610f8464a9e99f288f6b5e5afce4df2eb1aa624`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:27 GMT
ADD file:efed18ef2a003bff7e64e7049455216e51876402083581032c35085328e416f6 in / 
# Wed, 12 Apr 2023 00:39:28 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:04:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:04:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b0f987ce91d920ae0a705ed6c9824f1bbbfa282defb8986614030eb8e2bc0b4e`  
		Last Modified: Wed, 12 Apr 2023 00:41:45 GMT  
		Size: 49.3 MB (49345365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e6a618ee06e99ebfbb7809c1cc4902cb717d294243f3765f170fd1c8eaf94a`  
		Last Modified: Wed, 12 Apr 2023 01:12:23 GMT  
		Size: 8.9 MB (8915044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59c3f19470d2fd9e1407a7ddcbac3c316a999a143865347f221db18517e0838`  
		Last Modified: Wed, 12 Apr 2023 01:12:24 GMT  
		Size: 11.4 MB (11389565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b43a148c9da49809e8efcfafdef9c412da433e7735208795c69a14047f003874
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71409064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e15fc1cc8869eaa3b3492c5ebdad339d1c464b7630edf0a5e01a6fd94f6f3be`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:38:30 GMT
ADD file:7718865253a3489583d40f8c7a7beede0c20cebbab68bb3e97ad2e84082afcb7 in / 
# Wed, 12 Apr 2023 00:38:30 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:02:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:02:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a4ce9e81f634822e5166ef3eef875a4140795ac18afe0391433d72c7865bf67b`  
		Last Modified: Wed, 12 Apr 2023 00:41:43 GMT  
		Size: 50.3 MB (50317977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e54183fe5cb0866f886a93c0d098d38e649286a2b516b64d9658dd40f5d74b`  
		Last Modified: Wed, 12 Apr 2023 01:13:34 GMT  
		Size: 9.3 MB (9264042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76896a8c48193a86329dc809066c177aedc76d55811eb32ca7c80c1ab06f66f1`  
		Last Modified: Wed, 12 Apr 2023 01:13:34 GMT  
		Size: 11.8 MB (11827045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:3afc2ecbb80ef88ab70eb6ad01b612cc86b9eb46cd591f35f29128b222ca942e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68918906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb594595ebffc0ba011ef2f95469fdfdc4776f79e192ac3a4122772b6b04ca30`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:08:16 GMT
ADD file:6a525220124da7146a3c356cc57678f3b8d7c6e9299febaaebd5b5a005f1325c in / 
# Wed, 12 Apr 2023 00:08:21 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 10:49:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 10:50:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b6bdb9410f81554043d19e5ae83249eaa10ffe038db54932946c7d9eaccc8b96`  
		Last Modified: Wed, 12 Apr 2023 00:15:35 GMT  
		Size: 49.3 MB (49299322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71852747f2b9b21534b53c60a706551ff2aae26334aec4b70c4920fe9fb4f8c`  
		Last Modified: Wed, 12 Apr 2023 11:17:26 GMT  
		Size: 8.4 MB (8442270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb9aa6963a60e7aad5662c525f6bbd5202ae82472a684135f6111f1f7d3318e`  
		Last Modified: Wed, 12 Apr 2023 11:17:26 GMT  
		Size: 11.2 MB (11177314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5e2e84459ecb32db9fabb5e93567cedf5076f979a0d89d1ba558d1b2edebd39e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75148293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:321fa2f7d47d7fb1798f5396badb74ddbb7bb63d6ff179ee9938a659c3966ed4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:07:22 GMT
ADD file:b747fc06f7ee1d3e19fc9cf3aa83e6ab4caa056a72d230caf616e67849bfe112 in / 
# Wed, 12 Apr 2023 00:07:25 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:24:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:25:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8314f03b76ec928732612641a4f8420e3c4c25719b48503230bf6c03979aeb2e`  
		Last Modified: Wed, 12 Apr 2023 00:11:50 GMT  
		Size: 53.3 MB (53299984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823af2d3550f6b52577dc50d69a272726b10382b4fae65d06e3b7196165e42d5`  
		Last Modified: Wed, 12 Apr 2023 09:43:31 GMT  
		Size: 9.7 MB (9663796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f73dc4aed694f9f90cd285bb10ed1d4652e9e29ca42e3ae9b7e2148cb39b812`  
		Last Modified: Wed, 12 Apr 2023 09:43:31 GMT  
		Size: 12.2 MB (12184513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:377be7d5891b37466c736b399c0beb5ac9fdccf106bbee4e802cd0c0200a985e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67672334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75da5ea476406e76c74e365fa869cd83bc1a1cbbd23ef34d20b56b9cf7624b2c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:19 GMT
ADD file:5d2b35b45a0f23e2f2e93f9c311eb34a92e4591ea27979236d801e512d44cb85 in / 
# Tue, 11 Apr 2023 23:59:31 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:24:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:24:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8a09cd2374da8355612e7d4c91d55107a3f089816ae52b2c91b9e08e6a895ab1`  
		Last Modified: Wed, 12 Apr 2023 00:04:39 GMT  
		Size: 47.7 MB (47670407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d047361c12b2aeb253b1923b053dcc960101b3b3348af8f15f95f7fda2b89e4`  
		Last Modified: Wed, 12 Apr 2023 00:32:00 GMT  
		Size: 8.7 MB (8713846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a462d218c24c21390b32ace449f4f47a57624b858dc05a37c31cb7f6e21c41`  
		Last Modified: Wed, 12 Apr 2023 00:32:00 GMT  
		Size: 11.3 MB (11288081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:b3ac5bae610464bfbd16f2433b21b14f01c8cc1061332166a29f88ec39ba07fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9ed3be818675099491b2a9c5066bbd63d5283caa5f3b77d978ea95ecb43f2d61
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133896234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba56358263d5c537ab77ee622af1e53f4ab231c655f7637aa7739d9b469a80da`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:35 GMT
ADD file:1cb6c660a2e3ea14b2a11bb8b80f53920c3da423a0ad7004391bfab4db4d0177 in / 
# Wed, 12 Apr 2023 00:19:36 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:48:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:49:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 07:49:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cc556c281183180fae02d57fa6fb60ed0a99d9040936278743dc4022bfb0c686`  
		Last Modified: Wed, 12 Apr 2023 00:22:48 GMT  
		Size: 49.3 MB (49292938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8022b43d7c31d74c341d297cf10031ff0c51f596473a0c1945ee83a841094638`  
		Last Modified: Wed, 12 Apr 2023 07:56:29 GMT  
		Size: 9.1 MB (9083160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db75f726ec67539c4823cb16851963ebe5838a853b0e769fd662020fad918781`  
		Last Modified: Wed, 12 Apr 2023 07:56:29 GMT  
		Size: 11.4 MB (11422437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8a9e299258b84de99d6d739eb84b5b1632005f9c7723f2dd9e209fb1a8aaa3`  
		Last Modified: Wed, 12 Apr 2023 07:56:46 GMT  
		Size: 64.1 MB (64097699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:344b53de882fcda7c2d453195595144a3c69b6e842ee71d13d6da33ab28ecc50
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129241091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5754c39ab542288953f32e05c79772f7f299ee5ef462be8bd98f34a5d5ae07f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:48:19 GMT
ADD file:df1103dce44baa95c92287ab5016f36d5cc45c6062116ebf5273f7e79a00915c in / 
# Wed, 12 Apr 2023 00:48:20 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:11:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:11:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:12:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:795c0ca2726dffdb0e5ef6ffa341d17ec672d5915011f1a93a05e8c95a4779ae`  
		Last Modified: Wed, 12 Apr 2023 00:50:12 GMT  
		Size: 48.1 MB (48110879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e70c1a23fdf0fd320a61a2506f0ca4a391a319de8403734e4af8d678a6081fc`  
		Last Modified: Wed, 12 Apr 2023 01:20:09 GMT  
		Size: 8.5 MB (8523001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27111cd5fb1057675f2e0b269790dc264d344d6e4b7ad92ff941f90a496167b`  
		Last Modified: Wed, 12 Apr 2023 01:20:09 GMT  
		Size: 11.1 MB (11065924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ed8d7f4b0f78246beda91a51ddbc4ab368fe6f04bb2432498c3f5a76cbc010`  
		Last Modified: Wed, 12 Apr 2023 01:20:30 GMT  
		Size: 61.5 MB (61541287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b598cfea4a2fdd4babbe11e7f9770817e72eb9f2af57e7f8c34b858af1d56d2e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (123989849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411c875b6d761c0534bb297279832abe2d22d60dd23cd2e13d5d061f524a4799`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:10 GMT
ADD file:aa1c08333544c05fc5317d775ee99af7479c6fa5f35b74652f6126a7a5099958 in / 
# Tue, 11 Apr 2023 23:59:11 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:32:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:32:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:32:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:81b1dd69f2a38ad14b0919ab9c395aafeb137158539ab6531ac5743690a0ebb7`  
		Last Modified: Wed, 12 Apr 2023 00:02:26 GMT  
		Size: 45.9 MB (45883114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f399f5abf6c810daac72b311feda8726e38c0c228183ccf5d0da4de0b8ec79f4`  
		Last Modified: Wed, 12 Apr 2023 09:43:59 GMT  
		Size: 8.2 MB (8169132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3453014a13bae733f0a1d38594c31a25841303277602f61394efaff085c42288`  
		Last Modified: Wed, 12 Apr 2023 09:43:59 GMT  
		Size: 10.7 MB (10690179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1d5c89a8ad9820582b69420d902dbb04e78a440ab16e42dd52a5778aea37e4`  
		Last Modified: Wed, 12 Apr 2023 09:44:19 GMT  
		Size: 59.2 MB (59247424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:14fe92b486d2fa872ed5792948ef263bf382710d96156521bba91db6409d8adf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133624598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f0946fdc4f05c98259e0c4a796a7215b79fdfac56393722a52de699ef3ad2c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:27 GMT
ADD file:efed18ef2a003bff7e64e7049455216e51876402083581032c35085328e416f6 in / 
# Wed, 12 Apr 2023 00:39:28 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:04:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:04:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:04:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0f987ce91d920ae0a705ed6c9824f1bbbfa282defb8986614030eb8e2bc0b4e`  
		Last Modified: Wed, 12 Apr 2023 00:41:45 GMT  
		Size: 49.3 MB (49345365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e6a618ee06e99ebfbb7809c1cc4902cb717d294243f3765f170fd1c8eaf94a`  
		Last Modified: Wed, 12 Apr 2023 01:12:23 GMT  
		Size: 8.9 MB (8915044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59c3f19470d2fd9e1407a7ddcbac3c316a999a143865347f221db18517e0838`  
		Last Modified: Wed, 12 Apr 2023 01:12:24 GMT  
		Size: 11.4 MB (11389565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b373ae05bf678c385bace283c65197a2bbc2a334c528ed7b58a01d93131de585`  
		Last Modified: Wed, 12 Apr 2023 01:12:39 GMT  
		Size: 64.0 MB (63974624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:1b7217dd58c62e94d4df1bd3fe5e75114d9fdb3da6a3d8338c1e2534008bffce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.4 MB (137369491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed8865cd6ac62a089861253f45fe5c6131b992aa6d88dd85645089c3f5ada23`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:38:30 GMT
ADD file:7718865253a3489583d40f8c7a7beede0c20cebbab68bb3e97ad2e84082afcb7 in / 
# Wed, 12 Apr 2023 00:38:30 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:02:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:02:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:03:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a4ce9e81f634822e5166ef3eef875a4140795ac18afe0391433d72c7865bf67b`  
		Last Modified: Wed, 12 Apr 2023 00:41:43 GMT  
		Size: 50.3 MB (50317977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e54183fe5cb0866f886a93c0d098d38e649286a2b516b64d9658dd40f5d74b`  
		Last Modified: Wed, 12 Apr 2023 01:13:34 GMT  
		Size: 9.3 MB (9264042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76896a8c48193a86329dc809066c177aedc76d55811eb32ca7c80c1ab06f66f1`  
		Last Modified: Wed, 12 Apr 2023 01:13:34 GMT  
		Size: 11.8 MB (11827045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba7e1ed0df9a2a8a6501d91360cea22ab988653bf057d73c44ecb41e49f6151`  
		Last Modified: Wed, 12 Apr 2023 01:13:56 GMT  
		Size: 66.0 MB (65960427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:77882a60b3dac839278148546ac1b5ae49c0b862dc34eb47c9b961189f54aa62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131858661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b1707593870d644bad6ee88adb0d34d3d057b27f135eb3c00dae5700d6ce01`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:08:16 GMT
ADD file:6a525220124da7146a3c356cc57678f3b8d7c6e9299febaaebd5b5a005f1325c in / 
# Wed, 12 Apr 2023 00:08:21 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 10:49:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 10:50:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 10:52:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b6bdb9410f81554043d19e5ae83249eaa10ffe038db54932946c7d9eaccc8b96`  
		Last Modified: Wed, 12 Apr 2023 00:15:35 GMT  
		Size: 49.3 MB (49299322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71852747f2b9b21534b53c60a706551ff2aae26334aec4b70c4920fe9fb4f8c`  
		Last Modified: Wed, 12 Apr 2023 11:17:26 GMT  
		Size: 8.4 MB (8442270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb9aa6963a60e7aad5662c525f6bbd5202ae82472a684135f6111f1f7d3318e`  
		Last Modified: Wed, 12 Apr 2023 11:17:26 GMT  
		Size: 11.2 MB (11177314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324e348066ac545280d6c0f59d4c327df571da3bc37b52136ddfcb88f5e93d87`  
		Last Modified: Wed, 12 Apr 2023 11:18:17 GMT  
		Size: 62.9 MB (62939755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ff9ad1cd6f756acfad0e6713004c604f421a818881a59a65cdf72c3ac1f32b42
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144706710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d4f37092672a6f4eee455d949bb5dc19844135bb11f8290db298507672facf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:07:22 GMT
ADD file:b747fc06f7ee1d3e19fc9cf3aa83e6ab4caa056a72d230caf616e67849bfe112 in / 
# Wed, 12 Apr 2023 00:07:25 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:24:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:25:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:26:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8314f03b76ec928732612641a4f8420e3c4c25719b48503230bf6c03979aeb2e`  
		Last Modified: Wed, 12 Apr 2023 00:11:50 GMT  
		Size: 53.3 MB (53299984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823af2d3550f6b52577dc50d69a272726b10382b4fae65d06e3b7196165e42d5`  
		Last Modified: Wed, 12 Apr 2023 09:43:31 GMT  
		Size: 9.7 MB (9663796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f73dc4aed694f9f90cd285bb10ed1d4652e9e29ca42e3ae9b7e2148cb39b812`  
		Last Modified: Wed, 12 Apr 2023 09:43:31 GMT  
		Size: 12.2 MB (12184513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1002e389de5d993e4a73f7cf4311d2ac394084c1570912d013506d78ea334895`  
		Last Modified: Wed, 12 Apr 2023 09:43:59 GMT  
		Size: 69.6 MB (69558417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f1a6a91892b66c97ca28c0d4aa10b5706ce5d49d91fcfb33f33d04a191068ce7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 MB (130773785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1798d2a8c091800a97b7795b2e2f35680f165f0a95d7f44b12965f19623788f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:19 GMT
ADD file:5d2b35b45a0f23e2f2e93f9c311eb34a92e4591ea27979236d801e512d44cb85 in / 
# Tue, 11 Apr 2023 23:59:31 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:24:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:24:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 00:25:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8a09cd2374da8355612e7d4c91d55107a3f089816ae52b2c91b9e08e6a895ab1`  
		Last Modified: Wed, 12 Apr 2023 00:04:39 GMT  
		Size: 47.7 MB (47670407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d047361c12b2aeb253b1923b053dcc960101b3b3348af8f15f95f7fda2b89e4`  
		Last Modified: Wed, 12 Apr 2023 00:32:00 GMT  
		Size: 8.7 MB (8713846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a462d218c24c21390b32ace449f4f47a57624b858dc05a37c31cb7f6e21c41`  
		Last Modified: Wed, 12 Apr 2023 00:32:00 GMT  
		Size: 11.3 MB (11288081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628da1a495c0341f28b24cb228c4984d7d8a718059c95991d67739f4a4602e4b`  
		Last Modified: Wed, 12 Apr 2023 00:32:14 GMT  
		Size: 63.1 MB (63101451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:e9c192dccaeb2e1fdedf36d2dbcf10f6398bf85c6f7e932390752212375b989f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:unstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:1cb95d972e0a2c28195432ae6f0b584389e01e1938354a98b61c2d0e4c79f44f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (350981822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9133db89f5b5ae7caee0f8cca02226caaa3b22832a67d2a4bfc68f2ca38dfccf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:55 GMT
ADD file:0936f6fccda991ba27a7f73ca61c23a436b7ca417e504b66d5a68f2283e1e81d in / 
# Wed, 12 Apr 2023 00:20:55 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:54:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:54:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 07:54:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:55:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:003dca91ec623536e08abc4e1bb2849836a84c44f82e24b97fd5423162a4d46e`  
		Last Modified: Wed, 12 Apr 2023 00:25:13 GMT  
		Size: 49.3 MB (49287652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f0b6179599c75a087e6850c42ef248d973e29a6898ed99c9bccdae08d2cd2`  
		Last Modified: Wed, 12 Apr 2023 07:59:24 GMT  
		Size: 9.1 MB (9082764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f184ca8dda7ed83dd9d21d6c880d4e15976f35814156a0a67df81423067f4b8`  
		Last Modified: Wed, 12 Apr 2023 07:59:24 GMT  
		Size: 11.4 MB (11422423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76159e5040abc54c8e269f5e87ba68551c98fa9a6a06c9d7af5eae5f9f3ee57b`  
		Last Modified: Wed, 12 Apr 2023 07:59:41 GMT  
		Size: 64.3 MB (64257071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108d0b8f8755100dc81501ff3e762f953171a4a1230223973781ad90f85c1a53`  
		Last Modified: Wed, 12 Apr 2023 08:00:14 GMT  
		Size: 216.9 MB (216931912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7c5689a7aafd87d157899f6caf4601d66e8e391aef6483970f37553b5a868314
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.5 MB (318503660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:321ba3c06205c499df306cc1b5cfded148321e0a03dea6b3028714995c1f7d03`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:48:48 GMT
ADD file:b02c911309a1b69d235b76dab369d523653c62374b0173ee9f1b65017607f9d6 in / 
# Wed, 12 Apr 2023 00:48:48 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:18:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:18:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:19:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8699c4859220eb7e4f2a5ae13e4dd5f9143cb7144e2a02a3eb381a79416524bf`  
		Last Modified: Wed, 12 Apr 2023 00:51:27 GMT  
		Size: 48.1 MB (48109671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b565bf44c40ab65f5193c4fbfd752809f50e95e2c4b2397728f42419979d7c`  
		Last Modified: Wed, 12 Apr 2023 01:22:25 GMT  
		Size: 8.5 MB (8522810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8db076a21199a98e758a14876a91c9a890bb606e6d9d483862bcb73bc5cfbb`  
		Last Modified: Wed, 12 Apr 2023 01:22:25 GMT  
		Size: 11.1 MB (11065853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466720607b58ed4036916fa9d7cb2e82a3ca95f0e5ec8e2ef908744cd3e409ec`  
		Last Modified: Wed, 12 Apr 2023 01:22:44 GMT  
		Size: 61.7 MB (61667229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df42d9b3dd685881fab45c09a19f6d1505f1612856e8b0acca62c90e5aa6457`  
		Last Modified: Wed, 12 Apr 2023 01:23:20 GMT  
		Size: 189.1 MB (189138097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:30e30ff4573c461ff2d568b1512825ef8adb8715ab6aed2656fa60ddd8018427
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.6 MB (303626296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6871b7f96f3c0576d00b1c9f421e3518c6bb2ef2dbcac9568a5daad019b0acff`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:00:33 GMT
ADD file:f8bcd71f10e7adad706b3a1685fd5c4844e3ebde65bdf9a7c004d7b9dd3520d7 in / 
# Wed, 12 Apr 2023 00:00:34 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:40:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:40:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:40:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:42:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7b0aac501774f41dc4e46815077e011ed06b86d9469c6ca28755965123669423`  
		Last Modified: Wed, 12 Apr 2023 00:04:46 GMT  
		Size: 45.9 MB (45890234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78f03ccdd59b1aad6c28d38c86bc934c8e0a1da27d7a0be742b455933d23138`  
		Last Modified: Wed, 12 Apr 2023 09:47:20 GMT  
		Size: 8.2 MB (8168595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da6afe7624e90c309b1a605bad2994526027d5e48a341ffc3ea92eb706041f2`  
		Last Modified: Wed, 12 Apr 2023 09:47:20 GMT  
		Size: 10.7 MB (10690111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59c0245364868d7a1a6302c947f5a93b4058f6e740cfb6fdb6e5bb49709f683`  
		Last Modified: Wed, 12 Apr 2023 09:47:40 GMT  
		Size: 59.4 MB (59375149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a55ffccb5d27da5f28faad7acfd1221f109589677e83ec5d087ad21a4cd46b`  
		Last Modified: Wed, 12 Apr 2023 09:48:18 GMT  
		Size: 179.5 MB (179502207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ddc7753bdf44aa12263963bdb9942af3b69f4ed4dad7430d1a9eecabd6381d97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.1 MB (342096356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e722281a223374a931912368ece55c74201c7f46e39795b84006341333ddb0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:40:21 GMT
ADD file:2784bc6dba1e1dbea293e074ebf51fa7d89cb5545ea63ba2ed75b74d067387d4 in / 
# Wed, 12 Apr 2023 00:40:22 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:10:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:10:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:10:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:11:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:43d214f7ab3ca35a0c9ed4d8cdf62b36248aba2fa1bbac4ecd64e82ba2520b70`  
		Last Modified: Wed, 12 Apr 2023 00:43:58 GMT  
		Size: 49.3 MB (49327656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99d9e5d2b2df062d16ffea4a022a4c09ce904fb96ec3fa4712a1d936593ae2a`  
		Last Modified: Wed, 12 Apr 2023 01:15:01 GMT  
		Size: 8.9 MB (8915031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd2b1a4cab3b4ac2bb4a7e9aaaa60ce806e3c49a8726f7baf5a10ba5e0e89fb`  
		Last Modified: Wed, 12 Apr 2023 01:15:01 GMT  
		Size: 11.4 MB (11389544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff14914c0381e1889d1db49b1b39da80ae3a347cf1af048e2ae0eb42aec87a12`  
		Last Modified: Wed, 12 Apr 2023 01:15:17 GMT  
		Size: 64.2 MB (64154048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f54a27824f720f86861a2776e1cc4e2f54563a9d0f0b56d1a6ec034866e3f8`  
		Last Modified: Wed, 12 Apr 2023 01:15:45 GMT  
		Size: 208.3 MB (208310077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:413efb8fbcbb35e21e9437afbee83ae1bdcf365d62cc1261952b77c46884fede
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.0 MB (352984444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e361eb5030e9416d576bb6456af5b6f82090e0ffcde0ac62558e2c5fa198c1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:51 GMT
ADD file:31710a830769b5e1f2612e1cd05380f677714bf52f61a54adbc7424087fd1378 in / 
# Wed, 12 Apr 2023 00:39:52 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:11:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:11:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:11:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:13:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:35e4af56b8bda58bf958814bc36c8e3a9a1d719c8582c0f33d7d69cc5b416211`  
		Last Modified: Wed, 12 Apr 2023 00:44:24 GMT  
		Size: 50.3 MB (50310899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145bb18c860aae65312434f79bce9d784a4824ef455202efca0f687a388037fe`  
		Last Modified: Wed, 12 Apr 2023 01:17:27 GMT  
		Size: 9.3 MB (9263774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2063c41d1dff24f54b6a7d8edde21610fe37e02b35ed369be0ccf9f64cdc43fe`  
		Last Modified: Wed, 12 Apr 2023 01:17:27 GMT  
		Size: 11.8 MB (11827096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3196dd70f259df7354dba37d732f79f68e602883ec8838b2cfcd0515de5c5c`  
		Last Modified: Wed, 12 Apr 2023 01:17:49 GMT  
		Size: 66.1 MB (66127351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc32f4359c6fe3187a1f8bab45e405139e65a8f45a4858a27e1059dd58842672`  
		Last Modified: Wed, 12 Apr 2023 01:18:36 GMT  
		Size: 215.5 MB (215455324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:885466e182139f809db3510356d10b81b0a078489b1d592c6173599161d05814
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.6 MB (327567207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5442a8ca6a5ce365db78cf474da8a69c9fcf55de9a1fe952e7df516f2f47cbe0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:10:29 GMT
ADD file:60b5ce2a691448a1aab43387ba9337b8cc193a2cbb2a01ac71f5f0cb083415ff in / 
# Wed, 12 Apr 2023 00:10:34 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 11:09:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 11:09:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 11:11:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 11:16:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:45f3dc30e8865982b1af34a4bd64597aea34350dd1bf817342cb2901014ff9a2`  
		Last Modified: Wed, 12 Apr 2023 00:18:10 GMT  
		Size: 49.3 MB (49296248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0311647062c4d77b089dceb0e1175eb800c6718e8093eee8f3b7f766f3ca545c`  
		Last Modified: Wed, 12 Apr 2023 11:23:31 GMT  
		Size: 8.4 MB (8441995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad4d6630c6fc30725f01ed1da37d38070bf8059059638cd3afdce16cabec21a7`  
		Last Modified: Wed, 12 Apr 2023 11:23:31 GMT  
		Size: 11.2 MB (11177398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f0e5f6f719dbccb2bc36692548601c776d9eebffd01feb704ac9cb58945a04`  
		Last Modified: Wed, 12 Apr 2023 11:24:21 GMT  
		Size: 63.1 MB (63101303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e65d58860ee0d917719ee8b76f31e6cc2d8c69a45c47febab4ef6badb11ce38`  
		Last Modified: Wed, 12 Apr 2023 11:26:26 GMT  
		Size: 195.6 MB (195550263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1587d433361a947d6b38a4b0800e685a14cb87316b8d23a379afaed6801a222b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.7 MB (365706334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eceff9414624c6f92e4e22e9d4c2dbacc8e477ce90ef9c2c94a6ff5a6b6e384d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:08:41 GMT
ADD file:8700846eefa6ef0670106ef8055671479d597d057ee34d1d248dbefa5977753b in / 
# Wed, 12 Apr 2023 00:08:44 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:37:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:37:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:38:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:42:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1c14c235d79599f644d6f952e975871669fe8a00e0434e5d26966f11cfb3820b`  
		Last Modified: Wed, 12 Apr 2023 00:13:39 GMT  
		Size: 53.3 MB (53291710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140d550f01a3ea4465718eae23deed53e8c34f53813fb05c7fbbd6718d137b67`  
		Last Modified: Wed, 12 Apr 2023 09:46:52 GMT  
		Size: 9.7 MB (9663547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450886794424f907ac99ffb3d1748b6d36f1ae455fbb553503d88898905d6d36`  
		Last Modified: Wed, 12 Apr 2023 09:46:52 GMT  
		Size: 12.2 MB (12184648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf2504e8cddf5044ea9695b547b876a5177d803d452f5e4e0d8050845be707d`  
		Last Modified: Wed, 12 Apr 2023 09:47:19 GMT  
		Size: 69.7 MB (69742173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cadf35097d9f51dc61a0506497f5b08804ea65f918143f059285ebe1685ced5`  
		Last Modified: Wed, 12 Apr 2023 09:48:20 GMT  
		Size: 220.8 MB (220824256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:b9c02baf674d938d6af39d2f681786407b07e39dcc6c0ef663bbfa3027bb41f6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.0 MB (361040206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcff52053934b6b9001b1f614aafda9141bd8e31a4b2680e51f8d44353d4a4ed`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:09:05 GMT
ADD file:b8c0cf42f791d92283c2c47cf2ed446fb98a7cde685c9b923c89cadb86ddad31 in / 
# Wed, 12 Apr 2023 00:09:07 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:31:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:32:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 00:35:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:43:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6178d7c3b8603b1579d72ad9f5bda8fd22627feccccd498dad946eddfe96d27a`  
		Last Modified: Wed, 12 Apr 2023 00:12:25 GMT  
		Size: 45.5 MB (45494949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd056fe810f7c94134b5c26af6939949c18bfa4868dbc9f81ea8d7a25a0daf4c`  
		Last Modified: Wed, 12 Apr 2023 00:44:01 GMT  
		Size: 8.1 MB (8117374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f8d5394c046224d62d5170fd151d4339e0f5131b1503bf3eafecefe1ec7a10`  
		Last Modified: Wed, 12 Apr 2023 00:44:01 GMT  
		Size: 10.8 MB (10794055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc0c6cc5fb9f28304c05335b3e21ed5e3cce359b94731f04cc903938689ebc19`  
		Last Modified: Wed, 12 Apr 2023 00:45:23 GMT  
		Size: 59.7 MB (59741177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16f9d49dc3af209b4bcf7ce13172c2a5a76516c0d39580db79da7b27eaf387f`  
		Last Modified: Wed, 12 Apr 2023 00:50:51 GMT  
		Size: 236.9 MB (236892651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9287c8095d9220df2f988981ac641e97e22f861d9bd87aa2a19a9e6cf396a687
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.0 MB (319011191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914264ef0379c6c6c2f67b9eb3fd0e99ffc0016a3f81cb006225180ad93d3a77`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:01:19 GMT
ADD file:0593fbca11f3d4a9b2b916ee99bb70651af04ea1275262f12e9b0e5c07e81f0e in / 
# Wed, 12 Apr 2023 00:01:29 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:28:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:28:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 00:28:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:29:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1844a6b5cc32e25703d3a6ac2115866157b1f856d7463d0dca8443fea51061f1`  
		Last Modified: Wed, 12 Apr 2023 00:05:31 GMT  
		Size: 47.7 MB (47665068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f306dc6c45f3e2637390b46a2dce7fb061bb8be6ae7c72c47bba97d84b99d256`  
		Last Modified: Wed, 12 Apr 2023 00:33:37 GMT  
		Size: 8.7 MB (8713548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7676682574fe22f1cac8016a4f36ad54898c4313e0609a7e88e75e035e32444b`  
		Last Modified: Wed, 12 Apr 2023 00:33:36 GMT  
		Size: 11.3 MB (11288124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de3f9748f029581dd4821ad6e7d4da7ab4a31600128a2411dda2639c9b92fe58`  
		Last Modified: Wed, 12 Apr 2023 00:33:51 GMT  
		Size: 63.3 MB (63260422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81adcc7796eb9dd6b2ccee5b41b08f31d903a15caab787b2edc99367e1c15497`  
		Last Modified: Wed, 12 Apr 2023 00:34:19 GMT  
		Size: 188.1 MB (188084029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:f8cb8daba973c30f3ebe59cc75c94f38d1352e658bf22265d425182d2e509f78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:162b0f4bf898e2f30f86c124dae307c51fcefaf8e30eba8f3d0538d5b88b1533
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69792839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:895c4767319db895fdd9034df03472e20114f0f8c5ae8c9ce85f116db05635b8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:55 GMT
ADD file:0936f6fccda991ba27a7f73ca61c23a436b7ca417e504b66d5a68f2283e1e81d in / 
# Wed, 12 Apr 2023 00:20:55 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:54:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:54:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:003dca91ec623536e08abc4e1bb2849836a84c44f82e24b97fd5423162a4d46e`  
		Last Modified: Wed, 12 Apr 2023 00:25:13 GMT  
		Size: 49.3 MB (49287652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f0b6179599c75a087e6850c42ef248d973e29a6898ed99c9bccdae08d2cd2`  
		Last Modified: Wed, 12 Apr 2023 07:59:24 GMT  
		Size: 9.1 MB (9082764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f184ca8dda7ed83dd9d21d6c880d4e15976f35814156a0a67df81423067f4b8`  
		Last Modified: Wed, 12 Apr 2023 07:59:24 GMT  
		Size: 11.4 MB (11422423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:8b516bb4199218b93e0828691cca7924741a8012ef412cd89ec797180b9ad014
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67698334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9438faefdd9540401ef284f3ce81a1c9c2829d48e27358bfaecfb65aedfa6e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:48:48 GMT
ADD file:b02c911309a1b69d235b76dab369d523653c62374b0173ee9f1b65017607f9d6 in / 
# Wed, 12 Apr 2023 00:48:48 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:18:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8699c4859220eb7e4f2a5ae13e4dd5f9143cb7144e2a02a3eb381a79416524bf`  
		Last Modified: Wed, 12 Apr 2023 00:51:27 GMT  
		Size: 48.1 MB (48109671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b565bf44c40ab65f5193c4fbfd752809f50e95e2c4b2397728f42419979d7c`  
		Last Modified: Wed, 12 Apr 2023 01:22:25 GMT  
		Size: 8.5 MB (8522810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8db076a21199a98e758a14876a91c9a890bb606e6d9d483862bcb73bc5cfbb`  
		Last Modified: Wed, 12 Apr 2023 01:22:25 GMT  
		Size: 11.1 MB (11065853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a1e3bbf1c55a5464c86a292f106703c74891fbfa001f613d40d655e93bd9bede
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64748940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9173a08df38173e6306894fae0aa76e6f71dd6c980d9610d7cc52026a4ece2e7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:00:33 GMT
ADD file:f8bcd71f10e7adad706b3a1685fd5c4844e3ebde65bdf9a7c004d7b9dd3520d7 in / 
# Wed, 12 Apr 2023 00:00:34 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:40:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:40:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:7b0aac501774f41dc4e46815077e011ed06b86d9469c6ca28755965123669423`  
		Last Modified: Wed, 12 Apr 2023 00:04:46 GMT  
		Size: 45.9 MB (45890234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78f03ccdd59b1aad6c28d38c86bc934c8e0a1da27d7a0be742b455933d23138`  
		Last Modified: Wed, 12 Apr 2023 09:47:20 GMT  
		Size: 8.2 MB (8168595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da6afe7624e90c309b1a605bad2994526027d5e48a341ffc3ea92eb706041f2`  
		Last Modified: Wed, 12 Apr 2023 09:47:20 GMT  
		Size: 10.7 MB (10690111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c3e4535c3a32e860c9cdcb87e33d91d91a05de0caebac0e396b682b23449f890
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69632231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59a19733f90d03e40a3a26aa25904ff3dd15a57aa3bc07c4723ab3a166147dc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:40:21 GMT
ADD file:2784bc6dba1e1dbea293e074ebf51fa7d89cb5545ea63ba2ed75b74d067387d4 in / 
# Wed, 12 Apr 2023 00:40:22 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:10:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:10:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:43d214f7ab3ca35a0c9ed4d8cdf62b36248aba2fa1bbac4ecd64e82ba2520b70`  
		Last Modified: Wed, 12 Apr 2023 00:43:58 GMT  
		Size: 49.3 MB (49327656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99d9e5d2b2df062d16ffea4a022a4c09ce904fb96ec3fa4712a1d936593ae2a`  
		Last Modified: Wed, 12 Apr 2023 01:15:01 GMT  
		Size: 8.9 MB (8915031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd2b1a4cab3b4ac2bb4a7e9aaaa60ce806e3c49a8726f7baf5a10ba5e0e89fb`  
		Last Modified: Wed, 12 Apr 2023 01:15:01 GMT  
		Size: 11.4 MB (11389544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7fd624c3066dfa1ca3da4f7665c730788104cdc2cb90f94fe839582a1a20bff9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71401769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10d2d9289ea8eef61411b36e3c5358bc3e57f93d19422a12cdce3b5d7d7e922d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:51 GMT
ADD file:31710a830769b5e1f2612e1cd05380f677714bf52f61a54adbc7424087fd1378 in / 
# Wed, 12 Apr 2023 00:39:52 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:11:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:11:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:35e4af56b8bda58bf958814bc36c8e3a9a1d719c8582c0f33d7d69cc5b416211`  
		Last Modified: Wed, 12 Apr 2023 00:44:24 GMT  
		Size: 50.3 MB (50310899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145bb18c860aae65312434f79bce9d784a4824ef455202efca0f687a388037fe`  
		Last Modified: Wed, 12 Apr 2023 01:17:27 GMT  
		Size: 9.3 MB (9263774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2063c41d1dff24f54b6a7d8edde21610fe37e02b35ed369be0ccf9f64cdc43fe`  
		Last Modified: Wed, 12 Apr 2023 01:17:27 GMT  
		Size: 11.8 MB (11827096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:628533752353ab5e8a3f84261cb7c6e11db611d071e8d45ea918ba12085f4c61
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68915641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d997660f9947209900669cfd7ee82e565be22d4bce90cf6ee7ddc2b5ae238304`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:10:29 GMT
ADD file:60b5ce2a691448a1aab43387ba9337b8cc193a2cbb2a01ac71f5f0cb083415ff in / 
# Wed, 12 Apr 2023 00:10:34 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 11:09:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 11:09:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:45f3dc30e8865982b1af34a4bd64597aea34350dd1bf817342cb2901014ff9a2`  
		Last Modified: Wed, 12 Apr 2023 00:18:10 GMT  
		Size: 49.3 MB (49296248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0311647062c4d77b089dceb0e1175eb800c6718e8093eee8f3b7f766f3ca545c`  
		Last Modified: Wed, 12 Apr 2023 11:23:31 GMT  
		Size: 8.4 MB (8441995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad4d6630c6fc30725f01ed1da37d38070bf8059059638cd3afdce16cabec21a7`  
		Last Modified: Wed, 12 Apr 2023 11:23:31 GMT  
		Size: 11.2 MB (11177398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d3deb81ed361a658e6300eef9c948a9e31cb0c6fba12d79abc858df84a2113a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75139905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8d4b5ad4e2fe62ee02f64ca2b0eaa429bec6abebf8d5b731058ffd2e8f32d76`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:08:41 GMT
ADD file:8700846eefa6ef0670106ef8055671479d597d057ee34d1d248dbefa5977753b in / 
# Wed, 12 Apr 2023 00:08:44 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:37:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:37:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:1c14c235d79599f644d6f952e975871669fe8a00e0434e5d26966f11cfb3820b`  
		Last Modified: Wed, 12 Apr 2023 00:13:39 GMT  
		Size: 53.3 MB (53291710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140d550f01a3ea4465718eae23deed53e8c34f53813fb05c7fbbd6718d137b67`  
		Last Modified: Wed, 12 Apr 2023 09:46:52 GMT  
		Size: 9.7 MB (9663547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450886794424f907ac99ffb3d1748b6d36f1ae455fbb553503d88898905d6d36`  
		Last Modified: Wed, 12 Apr 2023 09:46:52 GMT  
		Size: 12.2 MB (12184648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:b6ecdf5c65f021e05c80106a2cc8a598f2fb062039c62b358a2a42fc40f3d4d8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64406378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfc1ea8528f7edf3edcdff9fd62663fec45eaf492953562405ce7f8504695160`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:09:05 GMT
ADD file:b8c0cf42f791d92283c2c47cf2ed446fb98a7cde685c9b923c89cadb86ddad31 in / 
# Wed, 12 Apr 2023 00:09:07 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:31:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:32:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:6178d7c3b8603b1579d72ad9f5bda8fd22627feccccd498dad946eddfe96d27a`  
		Last Modified: Wed, 12 Apr 2023 00:12:25 GMT  
		Size: 45.5 MB (45494949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd056fe810f7c94134b5c26af6939949c18bfa4868dbc9f81ea8d7a25a0daf4c`  
		Last Modified: Wed, 12 Apr 2023 00:44:01 GMT  
		Size: 8.1 MB (8117374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f8d5394c046224d62d5170fd151d4339e0f5131b1503bf3eafecefe1ec7a10`  
		Last Modified: Wed, 12 Apr 2023 00:44:01 GMT  
		Size: 10.8 MB (10794055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2a32ff0d5208b6ad040a9cb58b776824b3c95030e002745b9128549a0e88a98e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67666740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d98184dbb030d39270ec3b57dcd40af7dc1cb4c8755f6afe805779ab651c12`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:01:19 GMT
ADD file:0593fbca11f3d4a9b2b916ee99bb70651af04ea1275262f12e9b0e5c07e81f0e in / 
# Wed, 12 Apr 2023 00:01:29 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:28:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:28:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:1844a6b5cc32e25703d3a6ac2115866157b1f856d7463d0dca8443fea51061f1`  
		Last Modified: Wed, 12 Apr 2023 00:05:31 GMT  
		Size: 47.7 MB (47665068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f306dc6c45f3e2637390b46a2dce7fb061bb8be6ae7c72c47bba97d84b99d256`  
		Last Modified: Wed, 12 Apr 2023 00:33:37 GMT  
		Size: 8.7 MB (8713548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7676682574fe22f1cac8016a4f36ad54898c4313e0609a7e88e75e035e32444b`  
		Last Modified: Wed, 12 Apr 2023 00:33:36 GMT  
		Size: 11.3 MB (11288124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:ab9b4b0c7793beb83665883122683e2f0f6d28df1c5857c6e90413b1a333a8a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:unstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d9f6278d7e0c871b5bcdc327298a29c7c00a8a0504891c4ad2631c374b75a01c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134049910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd617366d1cce33570b6dcf04f7eac2404f89e0bece798cb7e973cbd704f667`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:55 GMT
ADD file:0936f6fccda991ba27a7f73ca61c23a436b7ca417e504b66d5a68f2283e1e81d in / 
# Wed, 12 Apr 2023 00:20:55 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 07:54:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 07:54:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 07:54:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:003dca91ec623536e08abc4e1bb2849836a84c44f82e24b97fd5423162a4d46e`  
		Last Modified: Wed, 12 Apr 2023 00:25:13 GMT  
		Size: 49.3 MB (49287652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f0b6179599c75a087e6850c42ef248d973e29a6898ed99c9bccdae08d2cd2`  
		Last Modified: Wed, 12 Apr 2023 07:59:24 GMT  
		Size: 9.1 MB (9082764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f184ca8dda7ed83dd9d21d6c880d4e15976f35814156a0a67df81423067f4b8`  
		Last Modified: Wed, 12 Apr 2023 07:59:24 GMT  
		Size: 11.4 MB (11422423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76159e5040abc54c8e269f5e87ba68551c98fa9a6a06c9d7af5eae5f9f3ee57b`  
		Last Modified: Wed, 12 Apr 2023 07:59:41 GMT  
		Size: 64.3 MB (64257071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c0b4a3eae58bd274c266cb60478e79df6446cb058ebcb7beec816064f9c69b75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129365563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b15a5f5bf525f6d5ed1af6bc9d3b44768864d1199c3f26e961d670e918851d7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:48:48 GMT
ADD file:b02c911309a1b69d235b76dab369d523653c62374b0173ee9f1b65017607f9d6 in / 
# Wed, 12 Apr 2023 00:48:48 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:18:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:18:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8699c4859220eb7e4f2a5ae13e4dd5f9143cb7144e2a02a3eb381a79416524bf`  
		Last Modified: Wed, 12 Apr 2023 00:51:27 GMT  
		Size: 48.1 MB (48109671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b565bf44c40ab65f5193c4fbfd752809f50e95e2c4b2397728f42419979d7c`  
		Last Modified: Wed, 12 Apr 2023 01:22:25 GMT  
		Size: 8.5 MB (8522810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8db076a21199a98e758a14876a91c9a890bb606e6d9d483862bcb73bc5cfbb`  
		Last Modified: Wed, 12 Apr 2023 01:22:25 GMT  
		Size: 11.1 MB (11065853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466720607b58ed4036916fa9d7cb2e82a3ca95f0e5ec8e2ef908744cd3e409ec`  
		Last Modified: Wed, 12 Apr 2023 01:22:44 GMT  
		Size: 61.7 MB (61667229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4625cae1cb86a704920cb5e233396ab0915f8f8aea6c2991bf83dc37494e5707
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 MB (124124089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a34df020edfcb54003832698a6fd1b0d2df01b8d86feaa47193d84801d022ab7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:00:33 GMT
ADD file:f8bcd71f10e7adad706b3a1685fd5c4844e3ebde65bdf9a7c004d7b9dd3520d7 in / 
# Wed, 12 Apr 2023 00:00:34 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:40:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:40:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:40:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7b0aac501774f41dc4e46815077e011ed06b86d9469c6ca28755965123669423`  
		Last Modified: Wed, 12 Apr 2023 00:04:46 GMT  
		Size: 45.9 MB (45890234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78f03ccdd59b1aad6c28d38c86bc934c8e0a1da27d7a0be742b455933d23138`  
		Last Modified: Wed, 12 Apr 2023 09:47:20 GMT  
		Size: 8.2 MB (8168595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da6afe7624e90c309b1a605bad2994526027d5e48a341ffc3ea92eb706041f2`  
		Last Modified: Wed, 12 Apr 2023 09:47:20 GMT  
		Size: 10.7 MB (10690111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59c0245364868d7a1a6302c947f5a93b4058f6e740cfb6fdb6e5bb49709f683`  
		Last Modified: Wed, 12 Apr 2023 09:47:40 GMT  
		Size: 59.4 MB (59375149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:909145f5f8b9a67acd7be2b62e379fe6c15950dee01727de50e4cc961c962502
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133786279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c7d9c27ae042d56e7ca69c21a7a5a690294d166c8196d78574264d9160d8957`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:40:21 GMT
ADD file:2784bc6dba1e1dbea293e074ebf51fa7d89cb5545ea63ba2ed75b74d067387d4 in / 
# Wed, 12 Apr 2023 00:40:22 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:10:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:10:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:10:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:43d214f7ab3ca35a0c9ed4d8cdf62b36248aba2fa1bbac4ecd64e82ba2520b70`  
		Last Modified: Wed, 12 Apr 2023 00:43:58 GMT  
		Size: 49.3 MB (49327656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99d9e5d2b2df062d16ffea4a022a4c09ce904fb96ec3fa4712a1d936593ae2a`  
		Last Modified: Wed, 12 Apr 2023 01:15:01 GMT  
		Size: 8.9 MB (8915031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd2b1a4cab3b4ac2bb4a7e9aaaa60ce806e3c49a8726f7baf5a10ba5e0e89fb`  
		Last Modified: Wed, 12 Apr 2023 01:15:01 GMT  
		Size: 11.4 MB (11389544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff14914c0381e1889d1db49b1b39da80ae3a347cf1af048e2ae0eb42aec87a12`  
		Last Modified: Wed, 12 Apr 2023 01:15:17 GMT  
		Size: 64.2 MB (64154048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:8e5134589fb0e6d388a1a4741142104956636747431cf809398cd58520b6da78
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137529120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc693ca7c37b5ced8d79a021265f81c4cecbc277909bb33bb103fd1302a0b37`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:51 GMT
ADD file:31710a830769b5e1f2612e1cd05380f677714bf52f61a54adbc7424087fd1378 in / 
# Wed, 12 Apr 2023 00:39:52 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:11:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:11:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:11:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:35e4af56b8bda58bf958814bc36c8e3a9a1d719c8582c0f33d7d69cc5b416211`  
		Last Modified: Wed, 12 Apr 2023 00:44:24 GMT  
		Size: 50.3 MB (50310899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145bb18c860aae65312434f79bce9d784a4824ef455202efca0f687a388037fe`  
		Last Modified: Wed, 12 Apr 2023 01:17:27 GMT  
		Size: 9.3 MB (9263774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2063c41d1dff24f54b6a7d8edde21610fe37e02b35ed369be0ccf9f64cdc43fe`  
		Last Modified: Wed, 12 Apr 2023 01:17:27 GMT  
		Size: 11.8 MB (11827096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3196dd70f259df7354dba37d732f79f68e602883ec8838b2cfcd0515de5c5c`  
		Last Modified: Wed, 12 Apr 2023 01:17:49 GMT  
		Size: 66.1 MB (66127351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:14ec2fad7148b576e923bf9b355b0735a20034441088f6ed8ba3d942adafc96f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132016944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20304a399e5ecc0f6c31f60f0cfc8c882574dba660ad45ace353b0f7c64b2af8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:10:29 GMT
ADD file:60b5ce2a691448a1aab43387ba9337b8cc193a2cbb2a01ac71f5f0cb083415ff in / 
# Wed, 12 Apr 2023 00:10:34 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 11:09:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 11:09:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 11:11:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:45f3dc30e8865982b1af34a4bd64597aea34350dd1bf817342cb2901014ff9a2`  
		Last Modified: Wed, 12 Apr 2023 00:18:10 GMT  
		Size: 49.3 MB (49296248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0311647062c4d77b089dceb0e1175eb800c6718e8093eee8f3b7f766f3ca545c`  
		Last Modified: Wed, 12 Apr 2023 11:23:31 GMT  
		Size: 8.4 MB (8441995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad4d6630c6fc30725f01ed1da37d38070bf8059059638cd3afdce16cabec21a7`  
		Last Modified: Wed, 12 Apr 2023 11:23:31 GMT  
		Size: 11.2 MB (11177398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f0e5f6f719dbccb2bc36692548601c776d9eebffd01feb704ac9cb58945a04`  
		Last Modified: Wed, 12 Apr 2023 11:24:21 GMT  
		Size: 63.1 MB (63101303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8135b2f23a71e776729d178ad2c044b029e434a6d8851c6db2bcf9c99af46c83
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.9 MB (144882078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1217c66cbb148d338fc6383d0543b5e72c22f88e67d1ad1e01886b46dfed4a7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:08:41 GMT
ADD file:8700846eefa6ef0670106ef8055671479d597d057ee34d1d248dbefa5977753b in / 
# Wed, 12 Apr 2023 00:08:44 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:37:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:37:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:38:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1c14c235d79599f644d6f952e975871669fe8a00e0434e5d26966f11cfb3820b`  
		Last Modified: Wed, 12 Apr 2023 00:13:39 GMT  
		Size: 53.3 MB (53291710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140d550f01a3ea4465718eae23deed53e8c34f53813fb05c7fbbd6718d137b67`  
		Last Modified: Wed, 12 Apr 2023 09:46:52 GMT  
		Size: 9.7 MB (9663547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450886794424f907ac99ffb3d1748b6d36f1ae455fbb553503d88898905d6d36`  
		Last Modified: Wed, 12 Apr 2023 09:46:52 GMT  
		Size: 12.2 MB (12184648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf2504e8cddf5044ea9695b547b876a5177d803d452f5e4e0d8050845be707d`  
		Last Modified: Wed, 12 Apr 2023 09:47:19 GMT  
		Size: 69.7 MB (69742173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:bcd300a4e07d706f2fd9f306c4c32864622137e94ae3c3c4670ea905ee0beff3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 MB (124147555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397d717b57a8049a3da1ad949d9ed38c1e6d2518bf8f6c629c18545c03f04445`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:09:05 GMT
ADD file:b8c0cf42f791d92283c2c47cf2ed446fb98a7cde685c9b923c89cadb86ddad31 in / 
# Wed, 12 Apr 2023 00:09:07 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:31:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:32:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 00:35:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6178d7c3b8603b1579d72ad9f5bda8fd22627feccccd498dad946eddfe96d27a`  
		Last Modified: Wed, 12 Apr 2023 00:12:25 GMT  
		Size: 45.5 MB (45494949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd056fe810f7c94134b5c26af6939949c18bfa4868dbc9f81ea8d7a25a0daf4c`  
		Last Modified: Wed, 12 Apr 2023 00:44:01 GMT  
		Size: 8.1 MB (8117374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f8d5394c046224d62d5170fd151d4339e0f5131b1503bf3eafecefe1ec7a10`  
		Last Modified: Wed, 12 Apr 2023 00:44:01 GMT  
		Size: 10.8 MB (10794055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc0c6cc5fb9f28304c05335b3e21ed5e3cce359b94731f04cc903938689ebc19`  
		Last Modified: Wed, 12 Apr 2023 00:45:23 GMT  
		Size: 59.7 MB (59741177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ab7bb732a3d488865f2b887c55fbefc2e0041d528429e377f1f5ee84b43bda25
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130927162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dba9e0d63f399d18f4d3f0cd3f58b4eee0e1d16c71d855c9f9b0bd4e250d67b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:01:19 GMT
ADD file:0593fbca11f3d4a9b2b916ee99bb70651af04ea1275262f12e9b0e5c07e81f0e in / 
# Wed, 12 Apr 2023 00:01:29 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:28:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 00:28:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 00:28:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1844a6b5cc32e25703d3a6ac2115866157b1f856d7463d0dca8443fea51061f1`  
		Last Modified: Wed, 12 Apr 2023 00:05:31 GMT  
		Size: 47.7 MB (47665068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f306dc6c45f3e2637390b46a2dce7fb061bb8be6ae7c72c47bba97d84b99d256`  
		Last Modified: Wed, 12 Apr 2023 00:33:37 GMT  
		Size: 8.7 MB (8713548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7676682574fe22f1cac8016a4f36ad54898c4313e0609a7e88e75e035e32444b`  
		Last Modified: Wed, 12 Apr 2023 00:33:36 GMT  
		Size: 11.3 MB (11288124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de3f9748f029581dd4821ad6e7d4da7ab4a31600128a2411dda2639c9b92fe58`  
		Last Modified: Wed, 12 Apr 2023 00:33:51 GMT  
		Size: 63.3 MB (63260422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
