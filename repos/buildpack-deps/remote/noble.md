## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:0e3ce7ba5d5a213fdf1ad193f10eb72dc560290f9e3758ecc0a19d9d9eab492f
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
$ docker pull buildpack-deps@sha256:569ab536a9dae4e9d247cabcec51df400121e7a84fd4e1c609dfe83222f120d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274749554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f961b2915beb08026b6b137c490bd6c4c510a6e7fe8597062ff5859defb68f`
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
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
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
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1521653fda6cd0a5792ccce948424ec895da66a78dd341dd761cf5d863079a6c`  
		Last Modified: Tue, 03 Jun 2025 13:39:06 GMT  
		Size: 13.6 MB (13621261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbcab7b82fcbccfbf0a9487149491a20ab8e4066e46b6e6b12ac9f4ec1a5e632`  
		Last Modified: Tue, 03 Jun 2025 13:39:08 GMT  
		Size: 45.3 MB (45308313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9e873383b3b7f91dc3c37bc75dd970f677bb91f88bc1792e8ecd8507341432`  
		Last Modified: Tue, 03 Jun 2025 13:39:15 GMT  
		Size: 186.1 MB (186104643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:30fd4d7234e5dd2a6d12d251ff01226dae57ff31d21929e6cc9e291a93eb4e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11450395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1800245d81401dd25ad8bb4368ce1d386cd655f72dc9cab1105c6b570425a2`

```dockerfile
```

-	Layers:
	-	`sha256:373cf7fef4683ab30462012b7dbc2e1200637bbdb65e3f6d09678b407804dd01`  
		Last Modified: Tue, 03 Jun 2025 06:12:14 GMT  
		Size: 11.4 MB (11440211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79df4ecfdd8fcbc806d38425b2aee8be9497fb78c5eef581fbaca7b2a8383972`  
		Last Modified: Tue, 03 Jun 2025 06:12:14 GMT  
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
		Last Modified: Tue, 03 Jun 2025 04:16:36 GMT  
		Size: 12.8 MB (12780568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc7ee5bd9c76349491b1d6eb575462fcbf5da5b8524ca927456bb287c669459`  
		Last Modified: Tue, 03 Jun 2025 05:12:27 GMT  
		Size: 48.9 MB (48866974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590a66c8d0efe987d0727a9c4977f7cde6870ec1934e8350bb2a7fcea7decb0c`  
		Last Modified: Tue, 03 Jun 2025 06:17:12 GMT  
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
		Last Modified: Tue, 03 Jun 2025 06:17:09 GMT  
		Size: 10.8 MB (10785035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0a43b313ca6ef7d3543e5a0f9ed318112d5f2cacae1574b0eaa87cba014444f`  
		Last Modified: Tue, 03 Jun 2025 06:17:08 GMT  
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
		Last Modified: Tue, 03 Jun 2025 04:17:41 GMT  
		Size: 13.5 MB (13456235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759b17809d1c47c854abc09c29619c5c3e1ecc066ba58350e83935a74d8b2f18`  
		Last Modified: Tue, 03 Jun 2025 06:47:26 GMT  
		Size: 45.3 MB (45337861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3461c485614044dbf5989b4c65d9e3bcd4fd0b492929c313376bb25f8d71be`  
		Last Modified: Tue, 03 Jun 2025 11:38:46 GMT  
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
		Last Modified: Tue, 03 Jun 2025 11:38:43 GMT  
		Size: 11.0 MB (11008817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3eb5bca715dc87b6d23629b58b604192c206580a44289000af761e03e09035d`  
		Last Modified: Tue, 03 Jun 2025 11:38:42 GMT  
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
		Last Modified: Tue, 03 Jun 2025 04:17:18 GMT  
		Size: 16.0 MB (15954183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8164017b162a84441c445117a482b3279cfe5281941001cae73acc870be8f689`  
		Last Modified: Tue, 03 Jun 2025 06:31:02 GMT  
		Size: 50.4 MB (50437375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347d8913ce982d4430262844f781a7d5df0880b2f487c26071a98babc2b83781`  
		Last Modified: Tue, 03 Jun 2025 10:17:57 GMT  
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
		Last Modified: Tue, 03 Jun 2025 10:17:51 GMT  
		Size: 11.0 MB (10956226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1950a4de0e880640e619ea3727afed3b0f1ced0e3d3aaf7ec3172e6f08a27df`  
		Last Modified: Tue, 03 Jun 2025 10:17:50 GMT  
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
		Last Modified: Tue, 03 Jun 2025 04:20:54 GMT  
		Size: 14.3 MB (14327998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0dc15b68fdc69e46f38c05f839bcd5a0103364875b543486932c8110c33ae5`  
		Last Modified: Tue, 03 Jun 2025 06:50:42 GMT  
		Size: 53.9 MB (53862201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996a1f412fa7a99539f63fa73bf1320a32063d5a505802d5b91db346f2ab4bac`  
		Last Modified: Tue, 03 Jun 2025 12:31:39 GMT  
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
		Last Modified: Tue, 03 Jun 2025 12:31:09 GMT  
		Size: 10.9 MB (10949495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:826aef09920b23b205d93708e7de3a03deaebb63db74d4d318954e9ee6b68388`  
		Last Modified: Tue, 03 Jun 2025 12:31:07 GMT  
		Size: 10.2 KB (10215 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:52d571f0517cc486b3aa0e2b7ec1f46729aa17771ccfbe582ea5ab71559a92a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.1 MB (253097233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7bc5ce03db956e483bca4c40eddf828f760ef552bbe1fb8ab0e2ad4aebe7d5d`
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
ADD file:b6b8557b3fef6c06eb943ce735f649cf7033ab3925e70e6b43901f1f29b4d5e9 in / 
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
	-	`sha256:7fa55ab2f467363da0197dee4a8e5af9e7ba7ef5686c6f0951bc509c387b765c`  
		Last Modified: Tue, 03 Jun 2025 13:31:43 GMT  
		Size: 29.9 MB (29930056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de52c2fdeab987f45f86ba773c7a796e45606740580a41f52ad841cf7937f80`  
		Last Modified: Tue, 03 Jun 2025 04:16:39 GMT  
		Size: 14.9 MB (14937985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a419ab9a4b62e5fe13ab2f0ca43ddbbcccbe7da113416be348882575840fa555`  
		Last Modified: Tue, 03 Jun 2025 05:16:47 GMT  
		Size: 46.7 MB (46738663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027a6dad7359b0a89c4824f888d46f6a94499f3b6928e95b26562b419e7e624b`  
		Last Modified: Tue, 03 Jun 2025 06:59:38 GMT  
		Size: 161.5 MB (161490529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5072e699410dd43ea33bc3b3fde4bdf82542b3ca1a5a7a08e49903a4f76d2304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8fadd722ee723b8c45a41daf795f3bda7f68033f283ec34bd5ddf4fea5bb371`

```dockerfile
```

-	Layers:
	-	`sha256:ab334dba74c99b003d3aa049d5ee2c50689048e5cdce1c5e9e88dd80851804a8`  
		Last Modified: Tue, 03 Jun 2025 06:59:35 GMT  
		Size: 10.8 MB (10800115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9bbbd95b922821f4b7423665066df1a2a31d5a9a34242e8a8561d0c9b5b8a2f`  
		Last Modified: Tue, 03 Jun 2025 06:59:35 GMT  
		Size: 10.2 KB (10184 bytes)  
		MIME: application/vnd.in-toto+json
