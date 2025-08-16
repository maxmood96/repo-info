## `buildpack-deps:plucky`

```console
$ docker pull buildpack-deps@sha256:d2735edb6ee2caf02b6f124f4742a79532f5d1e284e300c1c45acf356667bee0
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
$ docker pull buildpack-deps@sha256:5a51daec4d6b069f783a650d645e885a5233a36ff5ebfc6ae4a0e141cbef73d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255056237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266811889ca22503f66f8e3ad171443bd1456415511d879c7292707356238c70`
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
ADD file:40484c65b4dcca549c6a747c24b1002288b4ab2fd10533c84f127f05671c8369 in / 
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
	-	`sha256:643a2486ef3b8a74980bf7d40e2e5df32ede4686496e21ea7df2e3962c382f7a`  
		Last Modified: Sat, 16 Aug 2025 01:48:32 GMT  
		Size: 26.8 MB (26843859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1800cfd42ef8e1d2f5e5f40ba8e788b4d1a8bc53001cea31e8b1f59f8a89a7`  
		Last Modified: Sat, 16 Aug 2025 02:08:54 GMT  
		Size: 17.9 MB (17868367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2cb83f5402a61c8600c08d4a8e7e9dac61c34e44872f3c62b88a7b58610ef33`  
		Last Modified: Sat, 16 Aug 2025 03:08:35 GMT  
		Size: 50.3 MB (50277519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9815b03d2760613f5487fb1251915b7a4e8da4ccf568dda46883b36921b31aef`  
		Last Modified: Sat, 16 Aug 2025 04:11:29 GMT  
		Size: 160.1 MB (160066492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f24492c72662dd1c1988ae6fb3a67b2b0965ca01de206e5f6247c0fccb1555f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11728151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ff9dcaad642e1d6add5e57d6d3e24535197b9846f7ff28679392a5b8a429d1`

```dockerfile
```

-	Layers:
	-	`sha256:e3731c0d5c5a91c93e142402215c4559151ae2c29ca52fe63c81f453a0974ea9`  
		Last Modified: Sat, 16 Aug 2025 07:19:38 GMT  
		Size: 11.7 MB (11717902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d21655959227aef0dd43185854b8bf8f69839ca12efb77292fa0bd6f99e781ff`  
		Last Modified: Sat, 16 Aug 2025 07:19:39 GMT  
		Size: 10.2 KB (10249 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9e3d1eee8a25f9949ce70ab183fe6aeb7b2749bb0d9e4fec7bd0e35ced2e5db5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.8 MB (288762508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c9bf2b2a2e764bdecabc6a070efa43788746fb5c15fe5bc9be0307ec3ab925`
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
ADD file:d2716c4e2900235ac3cbe59b5ceb4d150c5d8640609a7e714f73597fac5926a0 in / 
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
	-	`sha256:48a6fe0456113b96785d9a1aa522254b504a40e53b8d74195c44e4fdf52b25f3`  
		Last Modified: Sun, 03 Aug 2025 12:06:38 GMT  
		Size: 28.3 MB (28298459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256cce6f0cda1e8b174db959b4349a70248e021fa76ee7a5af885fa065edfba8`  
		Last Modified: Sat, 16 Aug 2025 02:09:07 GMT  
		Size: 19.2 MB (19156760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4132b3bf5e02c4ba2f9854b1104fed50ff9272a4ece06b80e983918548aa8f`  
		Last Modified: Sat, 16 Aug 2025 03:08:52 GMT  
		Size: 47.1 MB (47131939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3eb94ebd08205dfaf61f99e6c1630cba681fc58296a1748d74739b92a7f0f72`  
		Last Modified: Sat, 16 Aug 2025 17:17:16 GMT  
		Size: 194.2 MB (194175350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:da9f975a42fe733e5e69d24580567e5dbf43fd538f7e80610516a0d9b0313bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12038926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06cc979eafc7d7a768404ce9c899d06cd9870b9195c0b5cd8019d99ec77fd2e6`

```dockerfile
```

-	Layers:
	-	`sha256:33b08ad22ed0e19921388c8b3ab58dcd21763a45ec6c6a2ab6dd853ca2ea2e2c`  
		Last Modified: Sat, 16 Aug 2025 07:19:48 GMT  
		Size: 12.0 MB (12028657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdd305bbd9d786e7743b6b5411fca2603048b3cbcd4a1fde30e8136a08ef2e7b`  
		Last Modified: Sat, 16 Aug 2025 07:19:49 GMT  
		Size: 10.3 KB (10269 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:fbf2134def9132cb917bc68eb33b0afc64247032a8f3d95f363995580b613141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.5 MB (311466158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72378dd1779b65d7403189780d2b1391f77bb75cb88a016b52147f396605cea7`
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
ADD file:a8eb7da2a1ca7797c073828f60b756f90268770883895115685fd3d94a242d2d in / 
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
	-	`sha256:1daa9f9107ec702f1bb8c0adeb8503c3284800cb0ab71220cc003eecca7ad0c3`  
		Last Modified: Sat, 16 Aug 2025 01:51:59 GMT  
		Size: 32.9 MB (32937635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95de13ff493371ae39ab76633e8a083b008b87c0a55de33bd66993adee6f516e`  
		Last Modified: Sat, 16 Aug 2025 02:13:42 GMT  
		Size: 21.6 MB (21583537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c731ab940030e8aef661328e75f9be9edf4effeb6ecb06ae5972e4bf0d5543f`  
		Last Modified: Sat, 16 Aug 2025 03:08:58 GMT  
		Size: 52.5 MB (52541256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8063129a9ff20c89a0cb324582b7094e80e24a0edca9b2066f6a54832e3cb82f`  
		Last Modified: Sat, 16 Aug 2025 04:12:50 GMT  
		Size: 204.4 MB (204403730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7f89683f4ec031aa70564deb616ff03016754f8501e6e67393e0487060b8d798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11956888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa7878bd74bf774d91ab265682a59983f36fee898017c6bf1a949e4f8def824`

```dockerfile
```

-	Layers:
	-	`sha256:38d1b5d007ed0ffd67ec150909e1b32b943f96496259a61e2919ada778c25feb`  
		Last Modified: Sat, 16 Aug 2025 07:19:58 GMT  
		Size: 11.9 MB (11946667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0c0a2c7a358c6ec0064868bbd1626a5242ab625703154787d616a2ab5d0e580`  
		Last Modified: Sat, 16 Aug 2025 07:19:59 GMT  
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
$ docker pull buildpack-deps@sha256:2ea0b9ae9ada4a8fe26130b55d136d41aa48b5d0b3a054865fb17670504af8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.8 MB (274770115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825920c4bc4cb33d6803c0f21518a4654fac69f87655852d424623a2f08283ac`
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
ADD file:dbfd8a48b57e266f38c953769b4c851820b26a22244748f6a7b74a7afa784b9d in / 
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
	-	`sha256:47c0d49428a531c3d8e5ed6ba4d57558d20b656fda4fcf9e372c9472510b2065`  
		Last Modified: Sat, 16 Aug 2025 04:58:35 GMT  
		Size: 28.6 MB (28570291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ce6693ceeeb6ed38d301eeb4e76d18ee20c3f2b0017462cbe50af032cbb605`  
		Last Modified: Sat, 16 Aug 2025 05:11:52 GMT  
		Size: 21.6 MB (21557152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72d86cc05bc5e5ac1edfed81111a0bbdedf1d57fbf672715708580289e5b2d7`  
		Last Modified: Sat, 16 Aug 2025 06:08:44 GMT  
		Size: 48.6 MB (48641357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9101435abe1bf001676ee07033c5e1ea97ab5ec7afd5d48efbf4d5915f77894`  
		Last Modified: Sat, 16 Aug 2025 08:07:16 GMT  
		Size: 176.0 MB (176001315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a1fa830bfcd9a4b590a1f26d0c150fcbb8fc042755b11cd05c7415d8d5fa05f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11761628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ab01c8f861a64afbae2cd9ed6711895dc9a9a5299f8592c04280123096005c`

```dockerfile
```

-	Layers:
	-	`sha256:fd4b4e4e8fe8f6a44c1570004c41c6d422a4b069894c1e61a74fa3f2394e3053`  
		Last Modified: Sat, 16 Aug 2025 10:20:05 GMT  
		Size: 11.8 MB (11751439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25409bc58dbfc2c3cd884bc6016b111ab386717fdff5ef3ffaf1c2f57fe5e53c`  
		Last Modified: Sat, 16 Aug 2025 10:20:06 GMT  
		Size: 10.2 KB (10189 bytes)  
		MIME: application/vnd.in-toto+json
