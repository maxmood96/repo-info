## `buildpack-deps:jammy`

```console
$ docker pull buildpack-deps@sha256:76e113d59a5d4146de0e2233916140926bdb44cf3a01351c0df7aca2677a068d
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
$ docker pull buildpack-deps@sha256:8f0b51cf67027f286da802d987879ca207ea71c01717cbbcd81854344e1fe73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250647818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06095c83152cdf2da8c059f2884b35363fea1929bab49200f632d250671eeef4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:32:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:19:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd31ed89fd7d59ba427c9f431e17b158ade8eb04083b8b256c587fc6521fb6b`  
		Last Modified: Tue, 17 Mar 2026 01:15:21 GMT  
		Size: 7.1 MB (7105152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075740e987dc00eb4d143d9ae323d2cc63723a346886c2ff4f364ceeef4cb514`  
		Last Modified: Tue, 17 Mar 2026 02:32:53 GMT  
		Size: 39.5 MB (39487897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c68cbba844d479bb3cd3a52e14eefdfa7c13d04cf7207c0df1435b1fee30abf`  
		Last Modified: Tue, 17 Mar 2026 03:20:12 GMT  
		Size: 174.5 MB (174516249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dd43a24be7636f8153b3d8f00e91a8800d5372eb77eec3a104974be638145290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11852168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba64796fc647a25a124ea5cb957e358d552b657dfca490e5b8620a84e625b320`

```dockerfile
```

-	Layers:
	-	`sha256:d4dfa76c3f7d1347bae43cfe44c7823fe5f4f984d128ddfc21790a77542626e5`  
		Last Modified: Tue, 17 Mar 2026 03:20:07 GMT  
		Size: 11.8 MB (11842010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb884bab453f70110c1bd43c7998e657a1f16123427971ace13f26a7ceb1806c`  
		Last Modified: Tue, 17 Mar 2026 03:20:06 GMT  
		Size: 10.2 KB (10158 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7fd629067f74d411cda0637cb562ee5e38cd1dcc6a12a299d85822cdf1d87432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.8 MB (217821275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f27ff147f1bfc1e5ef0af7422cb6aca48760c8bfd81bb2f84d41fc8465f10b0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:32:59 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:32:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:32:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:00 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:04 GMT
ADD file:f12ba0d4c2b96568c5eaebe951355983398ad22bb0ad2b3a1a93ae2c24d13555 in / 
# Tue, 24 Feb 2026 07:33:04 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:17:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:17:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d411674a4afc7be17053720e1c67deb36aff030c844d1520a78ec3bea5895fbb`  
		Last Modified: Tue, 24 Feb 2026 08:07:57 GMT  
		Size: 26.6 MB (26647217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f10ddf28b37730bf44a2bcc60b1f3b94591cf93dc2d0f8c09aed80a257459f`  
		Last Modified: Tue, 17 Mar 2026 01:15:16 GMT  
		Size: 7.0 MB (7009277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f099f59b2365bca7b3c9fb761a585e9fee4eefc234dd21e8677091b101c94360`  
		Last Modified: Tue, 17 Mar 2026 02:17:24 GMT  
		Size: 42.3 MB (42269398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989d1c36126737039d2344168c7211196f29c44dbf65191d1093a05c1af3a960`  
		Last Modified: Tue, 17 Mar 2026 03:18:23 GMT  
		Size: 141.9 MB (141895383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2140b7e356e4ee0054f50227dd026bc002ecd15fabe8249af0842d9f04f45d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11641443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d026ac3b97eab46dae0530e09c42d765f0a5b1382677e2372f3e0c1f079c469`

```dockerfile
```

-	Layers:
	-	`sha256:1f45c13c4c7272c895aceca0c28fc6ba9d88a6caee10fb3cfcbf59dc7b9e0642`  
		Last Modified: Tue, 17 Mar 2026 03:18:20 GMT  
		Size: 11.6 MB (11631219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5996a1945df00020debceda8a1ec6173de4c4ec069989b50e15424f077fd1a3`  
		Last Modified: Tue, 17 Mar 2026 03:18:19 GMT  
		Size: 10.2 KB (10224 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7eebc607e22084899bd008fa1c4ebf0278ab1049df9500ef96b28ffcc262d312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241922920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d559123489c9196f0653159d366be747d57d2b57f5576817d566db43ecdcbf4e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:37:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:22:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6485dc332a06408f602b0cdb9b519fb93ef48ddb953b0ca66a482c8afa276f5e`  
		Last Modified: Tue, 17 Mar 2026 01:15:34 GMT  
		Size: 7.1 MB (7059209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5613c92be07518a2207635fd4933f858a67625df2826c58a29582a86f333aeba`  
		Last Modified: Tue, 17 Mar 2026 02:37:20 GMT  
		Size: 39.4 MB (39411378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4c3d5c2a14d6607ea1804c86d228a4184d6716c1f091ee4b3e68f053e9a90f`  
		Last Modified: Tue, 17 Mar 2026 03:23:08 GMT  
		Size: 168.1 MB (168063308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6a4cd7caabbd0fae6325c75c40b8f86fc6da650eed87ccb3a562b38e60f128ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11847917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d108a608e44bf4048ffe200a91f696c3785400cfacc7e8125f7bd7d46ca25524`

```dockerfile
```

-	Layers:
	-	`sha256:3e456bb41252806d45f85a63f10c863be96aac5bce0522411b2f393f3b1feb49`  
		Last Modified: Tue, 17 Mar 2026 03:23:05 GMT  
		Size: 11.8 MB (11837677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cb1193412ddc3e10358ac0994c43c05d8f8819ae8d7371a40caeec31528c287`  
		Last Modified: Tue, 17 Mar 2026 03:23:05 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8f525b54d26ce41443fdf346d1a70cfa1df38c554e575a8f67e2936e2a8cb65e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.6 MB (271624947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63f808173a39970b88e5e7e6aa84f3c7935039356265b6d767d4667586596295`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:34:11 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:34:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:34:16 GMT
ADD file:8cdc5dcac981a23986a941c048f55a86d8ba46328e91ad30db9af43286781c61 in / 
# Tue, 24 Feb 2026 07:34:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 08:26:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 10:22:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 19:06:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:31e4dc9ee1718c21d378c7cdb3929e157eabf4d70fe4bbe2e6b8ec5289e836dc`  
		Last Modified: Tue, 24 Feb 2026 08:08:05 GMT  
		Size: 34.5 MB (34453448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce3a8acb89c2623912d6125678bb29c4a7f2e207f6e77e26bb6abce76585d23`  
		Last Modified: Tue, 17 Mar 2026 08:26:53 GMT  
		Size: 8.2 MB (8184428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1985ce43823ffd73c71d0c8f81fbbf854ebffd4e2943cbdf935d0e19f696702f`  
		Last Modified: Tue, 17 Mar 2026 10:22:37 GMT  
		Size: 43.8 MB (43776073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0e7bcac69ee07c3efeebabf0723dfb295d41c421617dabfb122e6dba69ff86`  
		Last Modified: Tue, 17 Mar 2026 19:07:51 GMT  
		Size: 185.2 MB (185210998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6a228f9c0af65218b99df1357ca8a23f554611c20cf97708b685ef23d5cc87ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11811567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a51d44dc9a4f6ecf20ea008309f64f551c9c681709a0320a72c58f2ca2cc06`

```dockerfile
```

-	Layers:
	-	`sha256:4959d88ce47aec6dd22c1b1bf11ae02034643057d9b54727dd6cd29e2fd084c8`  
		Last Modified: Tue, 17 Mar 2026 19:07:47 GMT  
		Size: 11.8 MB (11801375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e58cd84debfd67c1b98d6d00b0b12dd394620ac80e0bc74e3f71b2d849fe83c`  
		Last Modified: Tue, 17 Mar 2026 19:07:46 GMT  
		Size: 10.2 KB (10192 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:37ede1cb347fa7dca94e5942a501188f8e7d8a97dee96233621a1657275f4b4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.9 MB (275927809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda3704198e8639d24819177d49cf1deb3170eaee281c2f6cc43a9460535cd16`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:58:19 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:58:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:58:20 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:59:01 GMT
ADD file:fe9bc101b444ec167a91ca8e26679867fc3481650b0a57dfbc71041252c52df3 in / 
# Tue, 24 Feb 2026 07:59:06 GMT
CMD ["/bin/bash"]
# Sat, 21 Mar 2026 03:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Mar 2026 15:06:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Mar 2026 20:13:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c32e08022022bb708d1470956136113ea37119623075e5019f555d270f225be6`  
		Last Modified: Tue, 24 Feb 2026 08:08:12 GMT  
		Size: 27.0 MB (27045961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064f5d3ba01514a8f2923c2d44171c1cae4e8eeb6cda3193e3b8b567ce709f7a`  
		Last Modified: Sat, 21 Mar 2026 03:04:18 GMT  
		Size: 7.1 MB (7117456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07873d88f3e6ca12c311302e484c39f7c2814698f630485c1d15a3628a2b24f`  
		Last Modified: Sat, 21 Mar 2026 15:08:25 GMT  
		Size: 42.3 MB (42308372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da446d839f93b03774adf439342ed71474797aee31bfc80b83254c0115dec9ce`  
		Last Modified: Sun, 22 Mar 2026 20:22:43 GMT  
		Size: 199.5 MB (199456020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8c28032e5b6a454c1add61bcc5f2fce52bc3e39a070184b9aa9d4da8ab9e5a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11792551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c01ed93bdd28efae20f29cc8c5e409b81670707d10e3cc60ba9c993dc961136`

```dockerfile
```

-	Layers:
	-	`sha256:3466b8098b2239a90860e06d3e5b56d8fea956969b1c794f53bafec0d488e43f`  
		Last Modified: Sun, 22 Mar 2026 20:22:16 GMT  
		Size: 11.8 MB (11782359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a316089711d5cce1a0cace72b8b866a339ac65decffd19a5cf80a52e07b1c4a0`  
		Last Modified: Sun, 22 Mar 2026 20:22:13 GMT  
		Size: 10.2 KB (10192 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4345ad8e23c0cb9080b57f6f194029cc47c0e7b2ec1c40595351d24a376824a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.7 MB (224657001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935b5efe9e2e5fe040c585f77ceb05882ccaa8a5b1fd640f976da53225df21b0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:34 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:35 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:36 GMT
ADD file:03057d2fc9102d77c6c1ba39821174f9277c7aeb8de5358b12c437097e81cdb8 in / 
# Tue, 24 Feb 2026 07:33:36 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:19:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:22:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 11:59:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b108e2a3f64e047295acfb714c51eedfbd4912d55d53e8bbbad5c2ac52fdf289`  
		Last Modified: Tue, 24 Feb 2026 08:08:19 GMT  
		Size: 28.0 MB (28007102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2dee707e7ee901389a7d7012845d60c86c0f8b7b2c73c8a41b180a2d5814ff`  
		Last Modified: Tue, 17 Mar 2026 02:19:59 GMT  
		Size: 7.0 MB (7017051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d2899039a596d80cb747cead57f28fd899213e332ba43b8f8703006814d83c`  
		Last Modified: Tue, 17 Mar 2026 03:23:19 GMT  
		Size: 39.4 MB (39414737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81535ab9e22e8942c4e61c05c25e456e0f2eaebb47e9b6f1e045d54f8cf5c78`  
		Last Modified: Tue, 17 Mar 2026 12:00:26 GMT  
		Size: 150.2 MB (150218111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e5b18140ea24466cba2e6829fcf6ef89ea9891951829ca53d2077bb001e17af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11666047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b9aefb4ca3d9b12e3b19e8466b44749d45782bf17ed256ed17e0500b3a9a79`

```dockerfile
```

-	Layers:
	-	`sha256:6ca41f7f7a36214a45a498bc601710aad4a119b1871368d3e3772dacdb0c053f`  
		Last Modified: Tue, 17 Mar 2026 12:00:24 GMT  
		Size: 11.7 MB (11655887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:181446854ec6b71e43c56a5b4984a96a9cea454a67c39bf902830bc993406e8a`  
		Last Modified: Tue, 17 Mar 2026 12:00:23 GMT  
		Size: 10.2 KB (10160 bytes)  
		MIME: application/vnd.in-toto+json
