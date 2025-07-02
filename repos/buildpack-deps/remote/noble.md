## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:7269390c7e40473c18888f60cfcacbb0052497b4320670e52b97f10fe9b2a01a
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

### `buildpack-deps:noble` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:34fab391b3bf397f2e2ffb73e412df80525c518a5f2cf621770e8f1f47b0e165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.8 MB (274780183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143b7ed0d58c725fa3eec25fa8559e1989d778e29d3ff1f2cf68fa84a36458db`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fdbabbfc2d2357c11d06b94c29d86f9283ba38506222a230cfe31c410f7d61`  
		Last Modified: Wed, 02 Jul 2025 03:09:59 GMT  
		Size: 13.6 MB (13621201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743668f722e37fbf61a19f14a10a6cd8fa02930295eba1e6fcc7c625738ad375`  
		Last Modified: Wed, 02 Jul 2025 04:11:45 GMT  
		Size: 45.4 MB (45390189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184b4ec820cc5490740596b28d53f38347424538e09d40552bfd41196d4c9b5d`  
		Last Modified: Wed, 02 Jul 2025 07:24:47 GMT  
		Size: 186.1 MB (186050427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b6e3057410ae8114efadf7913f22f99e922c8fed5b1e6fbc74993a54de36541c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11742859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709204f2432b934c38c823b90f827cf088c0060af50ffb77eccbee33cc17b2bb`

```dockerfile
```

-	Layers:
	-	`sha256:b69279f35f390baf628b27852c1f5bb958089d68a072edb6a0093b48595495f3`  
		Last Modified: Wed, 02 Jul 2025 07:19:43 GMT  
		Size: 11.7 MB (11732675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5e2362f4ffad27066dae1c939466f83a400f849e44a57b26688c6e6ed26f3e6`  
		Last Modified: Wed, 02 Jul 2025 07:19:44 GMT  
		Size: 10.2 KB (10184 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:682047d0c8d4d57d8e9da39251839cf50df7c8982fcfc19d51c09ddf6187f86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.8 MB (236837347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8481514418108a862b7bd15c64e16135f8b3d71823713529a4df66ca83e18b63`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:f5b71e3353c1f92a265c88e163d98b6fc00235db4d001763328933c4838f3576 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:76393e3f1626a318c4984c6e6d91f17fe6888451b277b6cc175eab3a1032ebf5`  
		Last Modified: Tue, 03 Jun 2025 13:33:19 GMT  
		Size: 26.8 MB (26842221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca74547492ebc6726e0a1ef9887a16bf144497b7eff9f2f4d1b9b96fd524d65`  
		Last Modified: Tue, 03 Jun 2025 17:00:56 GMT  
		Size: 12.8 MB (12780568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc7ee5bd9c76349491b1d6eb575462fcbf5da5b8524ca927456bb287c669459`  
		Last Modified: Tue, 03 Jun 2025 17:00:57 GMT  
		Size: 48.9 MB (48866974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590a66c8d0efe987d0727a9c4977f7cde6870ec1934e8350bb2a7fcea7decb0c`  
		Last Modified: Tue, 03 Jun 2025 17:01:05 GMT  
		Size: 148.3 MB (148347584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:49838b92e6a6b0504a448e0b90e31405ee54f0e2080d5f5c7b3389c5313931b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10795279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26e559cc8b923528864f37a28a1443d1a8d27a5a809491d6bddd0d4da432106`

```dockerfile
```

-	Layers:
	-	`sha256:0ed819bf1860fbe3e3e8338c6c0a19c82921abb52d9f0d7150d1f58b5fe18c7f`  
		Last Modified: Tue, 03 Jun 2025 17:31:12 GMT  
		Size: 10.8 MB (10785035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0a43b313ca6ef7d3543e5a0f9ed318112d5f2cacae1574b0eaa87cba014444f`  
		Last Modified: Tue, 03 Jun 2025 17:31:14 GMT  
		Size: 10.2 KB (10244 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ea47b561682f4750e3ad502f2300e55a21be88091fda138a59fa3ba1ea41b5ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.3 MB (264294654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb698cd5ae514fec03a1f8d991f3b9ff81db33d243bcb0fa0a55e2b5653510e9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b69317717db81c94bb0365bd720346e2a43a6b03173cf89d340cc19a993286`  
		Last Modified: Tue, 03 Jun 2025 17:01:02 GMT  
		Size: 13.5 MB (13456235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759b17809d1c47c854abc09c29619c5c3e1ecc066ba58350e83935a74d8b2f18`  
		Last Modified: Tue, 03 Jun 2025 17:01:01 GMT  
		Size: 45.3 MB (45337861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3461c485614044dbf5989b4c65d9e3bcd4fd0b492929c313376bb25f8d71be`  
		Last Modified: Tue, 03 Jun 2025 17:01:08 GMT  
		Size: 176.6 MB (176648659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:14878cafee78e256f96cc859a0191979f57c473e429153a102f4a2c2d2f84832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11019081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d22fc5a7536de9adda8f1ad861600fe47a16389c47f232aa99fae1870617f4ee`

```dockerfile
```

-	Layers:
	-	`sha256:17c51ddae6f34acefb00575c24b08cf1cea0af03e5ed6580354f23ab758d41e5`  
		Last Modified: Tue, 03 Jun 2025 17:31:16 GMT  
		Size: 11.0 MB (11008817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3eb5bca715dc87b6d23629b58b604192c206580a44289000af761e03e09035d`  
		Last Modified: Tue, 03 Jun 2025 17:31:20 GMT  
		Size: 10.3 KB (10264 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d3dcfa613902b29d2002b1b9ca74c7099b3d43922a35214f84e22dcb20528c1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.3 MB (290315013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9d736ab39fcec862b0449bd23c0661332f63987ab136a75aff86834f56edce7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:5b5c63079c35f826dfba60892de9b0b4108ed6547a12101193a481b991b1add9 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9f6c4197b204ad8fd01f03e4a049c781a2075478303fbfa660f581b019365dab`  
		Last Modified: Tue, 03 Jun 2025 13:31:13 GMT  
		Size: 34.3 MB (34325210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b8bfbc006efc56c6755ed0088bc7e2319e113b78600a3ddbd68b5426fba260`  
		Last Modified: Tue, 03 Jun 2025 17:31:27 GMT  
		Size: 16.0 MB (15954183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8164017b162a84441c445117a482b3279cfe5281941001cae73acc870be8f689`  
		Last Modified: Tue, 03 Jun 2025 17:31:43 GMT  
		Size: 50.4 MB (50437375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347d8913ce982d4430262844f781a7d5df0880b2f487c26071a98babc2b83781`  
		Last Modified: Tue, 03 Jun 2025 17:32:05 GMT  
		Size: 189.6 MB (189598245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:13da83f1ac2340b348b15ba78e46d1a9f1c8962d972c80d17f5d47751a106db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (10966442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032099d7feb41ddb9fef1be7b0de397ebb82d4501130305061e48f78ba8372d1`

```dockerfile
```

-	Layers:
	-	`sha256:98b9c68633cd60f2b913a6627ce66b561d4895bb11f446cfb8ee12698e7ea9fa`  
		Last Modified: Tue, 03 Jun 2025 17:31:26 GMT  
		Size: 11.0 MB (10956226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1950a4de0e880640e619ea3727afed3b0f1ced0e3d3aaf7ec3172e6f08a27df`  
		Last Modified: Tue, 03 Jun 2025 17:31:29 GMT  
		Size: 10.2 KB (10216 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:c89fd2b6329b3006fa863a9b862a0e914ee7bcad2c81ee4bc3dffa7f33bdb34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.3 MB (330276615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4d6cc34e98c3627fa3cac6a079104b6e576281eb7f51a37200af29bf979b2f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:f68263cf915d0f5d61ab9caa83da511fc9ef55d936429cb8fb542906fc38a8fa in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4ac2db62b9f8401057b5c4ebae4764d70573ec599f6a1f0b5dc2c4491ed8e39a`  
		Last Modified: Tue, 03 Jun 2025 13:37:40 GMT  
		Size: 30.9 MB (30947484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f34a9ec93701ff69dabbd7cfb519ee4f1c3aea72d284f88712f56d2d510da2`  
		Last Modified: Tue, 03 Jun 2025 17:31:41 GMT  
		Size: 14.3 MB (14327998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0dc15b68fdc69e46f38c05f839bcd5a0103364875b543486932c8110c33ae5`  
		Last Modified: Tue, 03 Jun 2025 17:31:59 GMT  
		Size: 53.9 MB (53862201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996a1f412fa7a99539f63fa73bf1320a32063d5a505802d5b91db346f2ab4bac`  
		Last Modified: Tue, 03 Jun 2025 17:32:08 GMT  
		Size: 231.1 MB (231138932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:528388a858b0137fe8a813e82151bd94b424d5c5c29ac9e421611603aefea1e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (10959710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b1b7e5b846121469af8470ca455a0db639c51b0a22773aa4dfcbc482c59eeb`

```dockerfile
```

-	Layers:
	-	`sha256:d860cc0629763f0457ec08edc2d7f30acb5683f29ceda8eade149a824bff539d`  
		Last Modified: Tue, 03 Jun 2025 17:31:37 GMT  
		Size: 10.9 MB (10949495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:826aef09920b23b205d93708e7de3a03deaebb63db74d4d318954e9ee6b68388`  
		Last Modified: Tue, 03 Jun 2025 17:31:44 GMT  
		Size: 10.2 KB (10215 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:65a44e671aee0e6fca69fc35f7740c5907cfba493ea63ef0473844987d0e65d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.1 MB (253104204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b4b7c9224218c6ae4eb5ca7ea4caae47e28957a19fa7e764ee04710a035683`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:80b0b0c2a08a762cf6a520d8428a5c769c29e72f4a51630adb2231f2816c50c4 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:30d64ca13d9d94eb48bf3fece3e38a4e60931d72f1a8c633dec981e43a0515a4`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 29.9 MB (29925630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0a7472d36ac954b6ad8ae016bc95c96fed55c2a6dff7a2277fb2905ea71cd5`  
		Last Modified: Wed, 02 Jul 2025 04:13:00 GMT  
		Size: 14.9 MB (14938086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006872a7d3dfbb370d9b9ad9f173b1cff4ec2ed138890295c7fcf7af3bc38370`  
		Last Modified: Wed, 02 Jul 2025 05:18:26 GMT  
		Size: 46.8 MB (46774728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452c4650af949af617d8d515922edc1973c72bca84c1235c17ee31a9678ca7a2`  
		Last Modified: Wed, 02 Jul 2025 07:11:02 GMT  
		Size: 161.5 MB (161465760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0e8370689e47843ae5edbbc30d4795137f9179723b87b4519517bde12c5e6b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11083612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1406b3ff0da34d9ce3484e190db7c5e355e04da156cd3616a853d82511bcce2b`

```dockerfile
```

-	Layers:
	-	`sha256:18ac6e78b53ee38b0357de4859b17cc69a06edff53b26807da23a4ca0410e4ad`  
		Last Modified: Wed, 02 Jul 2025 10:20:08 GMT  
		Size: 11.1 MB (11073428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f8d69c94ae7d6c122392ebcfb23734769356afec3e121c737f30d99de7de04c`  
		Last Modified: Wed, 02 Jul 2025 10:20:09 GMT  
		Size: 10.2 KB (10184 bytes)  
		MIME: application/vnd.in-toto+json
