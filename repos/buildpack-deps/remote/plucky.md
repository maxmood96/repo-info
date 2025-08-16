## `buildpack-deps:plucky`

```console
$ docker pull buildpack-deps@sha256:60309c18f0fb8aeefce1a56fcd8362bbb0f0ba48b5f10072e453faf1d7436629
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

### `buildpack-deps:plucky` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:bca8b94c2e6db3696ac63ed244820ddbe54d7a1fe19c50a196afdb9f83223224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308218041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4275cb87080fc280cedb5cf9647883d4f1603a318cfe3b54c8a663a3410f1705`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:0b62dcb33fe378845a262fa61527f246a452317a171d84377cd6915b5d44c281 in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:df3646a507d2b3b1b0bde6e6a491ee8926b6961e71b422b45b15dec9c6e2bc9e`  
		Last Modified: Sat, 02 Aug 2025 10:46:49 GMT  
		Size: 29.7 MB (29713909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa5ad9b9943c0e22e19439eab0c771d59c80537fc66eadd9af4a89a5c8b167b`  
		Last Modified: Sat, 16 Aug 2025 00:49:31 GMT  
		Size: 20.2 MB (20155127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c58e347bc287aa01e2babe592875e3c6c1ec2a120c6e2ec056debc7e78b9b56`  
		Last Modified: Sat, 16 Aug 2025 01:08:48 GMT  
		Size: 49.4 MB (49415404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f8d6cfe20237deb8a1bdb875ee3d83859a600e1132beb4052d10e190f27131`  
		Last Modified: Sat, 16 Aug 2025 02:10:11 GMT  
		Size: 208.9 MB (208933601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:93181a0761697108f43c34d1e85becc0935c5283547ba0710aca340b087b2cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11975590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ffbcf647e85951cb2e68454ebf7a3ee4c8f3e55062d8c70b8c805835bb2484f`

```dockerfile
```

-	Layers:
	-	`sha256:7790b1a208ab09e9575df7492ba25c76ff647cf22c3792c1098be8c3edc6e6b0`  
		Last Modified: Sat, 16 Aug 2025 04:19:25 GMT  
		Size: 12.0 MB (11965401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4c5354df56b5d75c868e2aff42322be866d3d2d2f1677b3368950c634813b74`  
		Last Modified: Sat, 16 Aug 2025 04:19:26 GMT  
		Size: 10.2 KB (10189 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e8a6c39d3febccb5a9f5f067f9bda964027ca54eb1406bcf2a9db622240d5c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255092668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c008fca2ff77107e7f3baf1c74efaf01ace93c5fb3e1881fc52c06a9fc3f930e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:ac993f8361d52080de798fe91ca382cf3c467ff71bc71600bbdaa585a1bd89e2 in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:51cd15c2b408ab8a834ca6023a771252ece14de5c8ed593748e2cd27e7ba9092`  
		Last Modified: Wed, 16 Jul 2025 03:43:37 GMT  
		Size: 26.8 MB (26843329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e00e1ee9b88439f885d74c1785459e997940c0a063728b9e12f626fc5f975bc`  
		Last Modified: Wed, 16 Jul 2025 07:30:07 GMT  
		Size: 17.9 MB (17866319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd5be0c18fcc231fa210a38f2bb00f94aca22d0203686cd9053220c70a1e89c`  
		Last Modified: Wed, 16 Jul 2025 09:00:46 GMT  
		Size: 50.4 MB (50363433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02160a5fb8a412689fec2eada4d6c9d925439ed4de6dc269d5d08f348992df0c`  
		Last Modified: Thu, 07 Aug 2025 05:35:09 GMT  
		Size: 160.0 MB (160019587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e500320f110125e305182f04d72eec600e71e83f6b427942f550d02569024998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11727998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad47f8b1746e291f59d1f21774a5bfaecbd1147b21114a6a35e40ad2364ba1e`

```dockerfile
```

-	Layers:
	-	`sha256:f540e1d71642f988153bded6a37514eff2fcd7f51acb2f73d56c743e8d4d0c93`  
		Last Modified: Wed, 16 Jul 2025 10:20:09 GMT  
		Size: 11.7 MB (11717750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8c5e05a5cbb55d7f5f8a5d6704499f5927d6241af61e594f0c061812fcd4782`  
		Last Modified: Wed, 16 Jul 2025 10:20:10 GMT  
		Size: 10.2 KB (10248 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:68a09a644bd3723b3658f2adf779fbc17e436eec5d5ec18d6d00bd6323948cda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.8 MB (288831095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2396777210e1adf10ce27e4b4998e18adf0c895b9c33d9a1ab09b45ea866f79`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:74b87afd48f111047bf713b8cf20d092443090c5c4f1b03dcd0722ddd1aa5d5f in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a74c143acce9afb47a82de9bb1f61fd6893a6383504aff0859c0f58738f12195`  
		Last Modified: Wed, 16 Jul 2025 05:59:46 GMT  
		Size: 28.3 MB (28299661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4421b809b182abd87dea29f51671e1762d97df2182c32ede6a90986394b2d5e1`  
		Last Modified: Wed, 16 Jul 2025 09:41:56 GMT  
		Size: 19.2 MB (19155576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231c6170e4086deb5df42629ea6c5f78b6d1e02ddde6b4c61109912fe4de4d29`  
		Last Modified: Wed, 16 Jul 2025 14:31:27 GMT  
		Size: 47.2 MB (47163655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b1310a1c8cec171c2de90c2b24862bb749f9a42d81700a0eccaa97ac867094`  
		Last Modified: Wed, 16 Jul 2025 23:56:21 GMT  
		Size: 194.2 MB (194212203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5d2ef103e8ad2a9d3de5020fa30a9def7995606da5b018a65db82f6afbca79d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12038773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64700866f1ccda18015a45ec08050a038000dbb548044a41ecbbea0cd4819efe`

```dockerfile
```

-	Layers:
	-	`sha256:02145965e9dfdbe9b51d9984c4148c68e2031ce1571c842f1f6dc56009ce78e6`  
		Last Modified: Wed, 16 Jul 2025 19:19:52 GMT  
		Size: 12.0 MB (12028505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9fb7b0d5e6fd63eb461dbcf897f8bdde98b5ec711e2dddfe689e1770155fb0f`  
		Last Modified: Wed, 16 Jul 2025 19:19:53 GMT  
		Size: 10.3 KB (10268 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a3e56802439f390a2a0237c78b6452c55177cddfcaee30a980a4ff62f014bc6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.5 MB (311535854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4476311ce446ae2c7f5311511c54e95192d9838c26b04f73de616a343dbda950`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:16f6fede728adf38126b61ca02d4b0c1db312e097bfc28d2add38bf1e35aea5f in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9050d7b66e4df73becb02e146013883ca8e8b432d324566dd56f658fc5d9f081`  
		Last Modified: Wed, 16 Jul 2025 01:40:21 GMT  
		Size: 32.9 MB (32937695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4700582777440d737c5d52b148c8ac90a518903a8fccb9b879f43d11f9b29d`  
		Last Modified: Wed, 16 Jul 2025 05:21:08 GMT  
		Size: 21.6 MB (21581386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bdce12a3e3796b20f054a5c41677d32d50fda57fc11f41afda4bd96c5df186b`  
		Last Modified: Wed, 16 Jul 2025 08:59:48 GMT  
		Size: 52.6 MB (52626938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc25dc355f2f2ba8d3b17000cc459032c3f3377e29e449f116b3775b975e11cc`  
		Last Modified: Thu, 07 Aug 2025 05:36:19 GMT  
		Size: 204.4 MB (204389835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a036f1145acd0732ab5ca410617e24b8b1d2bf0b21a863de628737bdff6d00fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11956736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d40abe5c197edf93824473931ac91a330ea36c4f696a1353bfd1026737f45ec`

```dockerfile
```

-	Layers:
	-	`sha256:0b82174afa917460340db17ea2a0e24b9e056cfd3b3a98753d4b26d16567f08e`  
		Last Modified: Wed, 16 Jul 2025 13:20:10 GMT  
		Size: 11.9 MB (11946515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19659c6c5fcdef292921575d21b3d531d9dd6a54ccbe8a6902c11a29ab87a1c0`  
		Last Modified: Wed, 16 Jul 2025 13:20:11 GMT  
		Size: 10.2 KB (10221 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:9f8637daab651005709b924f74da8c348a7de71566dccb6db3aa88c77e0b7382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.3 MB (398283588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9cbfa59cc0509536b39dff94332197c28dee17d5a8b3e800c429d3c87e9245`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:a13c0f71b63dde34d50b20e9c0f907b4ff0149f6defb35873bd5c775dc6608f0 in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e37cdc611bf317b30fafd3638be9680c6eafc009b0f9f982d8e6a8bd269d932b`  
		Last Modified: Fri, 18 Jul 2025 13:58:52 GMT  
		Size: 29.7 MB (29736805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14aa98380567c4c984802c325f8915c9a9af6c2d9a7e4d9e6b681e6d78148bc`  
		Last Modified: Sun, 20 Jul 2025 04:00:51 GMT  
		Size: 19.9 MB (19889957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a265d02e438e9c43ad14e4e69f7128dc1f1ad4cd8a0450af5a79b31f7d595b4e`  
		Last Modified: Sun, 20 Jul 2025 10:19:33 GMT  
		Size: 55.3 MB (55305216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a038d5d81f852adb9c5eb9443cd85a2d94f468001d1d04f4c364e7d65f07ac4`  
		Last Modified: Mon, 21 Jul 2025 15:23:02 GMT  
		Size: 293.4 MB (293351610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e711c9a431f848b9fcf16ab12be0ab5947e5f8f7b678cfbbb1ae47eff0cb56b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12013081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f687dacc57fd5d58b3460c8039636dc63c8f2ff93131ac9bfff524f08549653`

```dockerfile
```

-	Layers:
	-	`sha256:3f2c15396fd7416cb95eb7f3f83f05969f4bce883676e204ebece51bfc6553a0`  
		Last Modified: Sun, 20 Jul 2025 16:20:06 GMT  
		Size: 12.0 MB (12002861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6e0f7d8d4a843ed07b9578fccd201e532999339616eb35b2bd0aa8b48d5a04e`  
		Last Modified: Sun, 20 Jul 2025 16:20:06 GMT  
		Size: 10.2 KB (10220 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3c7882234507a7ba14637bd4d1da2786c294e70c5a2bc7cdbe35d7ee1110049c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274702865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7396eaf3e98b54fcbafca8cd44c24faa0cc29b239f4bafe9959907dd7cee7d03`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:4835f515da64e68a0d9668d8db154aae5a5e48af77b309894fc71ff41f645e45 in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1e9b7604476ec6328c322f5f4eee245a30844798202ad272f83b77424e3b1974`  
		Last Modified: Wed, 16 Jul 2025 05:19:56 GMT  
		Size: 28.6 MB (28569319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a7ff3817d970c11f86de16193d7f589f9b11c36eb0cab8624b4977956c86f0`  
		Last Modified: Wed, 16 Jul 2025 08:46:46 GMT  
		Size: 21.6 MB (21555165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7530d657a8e702b3949a81002f2c7bd24061e9cf41f71347f876afce2c76e61`  
		Last Modified: Wed, 16 Jul 2025 10:33:47 GMT  
		Size: 48.7 MB (48676352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307af14c68cb9cf1d21e1098013e575828d552ee47437f58efd6642fc4cb60f7`  
		Last Modified: Thu, 07 Aug 2025 05:37:34 GMT  
		Size: 175.9 MB (175902029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6c262e9660d59b83ac12cdb979428754110f1372b5cba413ab58caa154a13b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11761476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76fd0ef86b8f15554d2c1b42083e974b9a39f32795df3bda47ddde65d6a6dee1`

```dockerfile
```

-	Layers:
	-	`sha256:89d5541074364de54d14269c6ef5817c3080350766cb53df0759b87ca64b5106`  
		Last Modified: Wed, 16 Jul 2025 13:20:26 GMT  
		Size: 11.8 MB (11751287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1608e7441c8e19429f33e77ead04810bf8cbfb1e24e11a9211a32f717a37b7f`  
		Last Modified: Wed, 16 Jul 2025 13:20:26 GMT  
		Size: 10.2 KB (10189 bytes)  
		MIME: application/vnd.in-toto+json
