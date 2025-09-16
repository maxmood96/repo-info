## `buildpack-deps:plucky`

```console
$ docker pull buildpack-deps@sha256:ad595e41ef90eaebc49652af873ae105d983bff1949c95fe197f837bc1269693
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
$ docker pull buildpack-deps@sha256:f7f0cdc5bfe1183f5bdaf4871c0970617a1ecda86c87da43d3fba066277083b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.3 MB (308326174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f1f1d96dd71ea699801da7fae8de2b7d836d023b58f356988464df600c2ef9`
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
ADD file:d17f4a4666630f8b9d15b4dc3923b653110adbab5c7c5d0bd03975e1894a7a36 in / 
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
	-	`sha256:a54a536f5c04d9395dbeed64c1972fe7c7df89f5374561b8718bebbfe644fd94`  
		Last Modified: Wed, 10 Sep 2025 15:57:46 GMT  
		Size: 29.7 MB (29715598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b97812ff0ce0ff49ad436d22bb765dc0c078ca9b006fea6b1c05ccb51df32b`  
		Last Modified: Mon, 15 Sep 2025 22:12:34 GMT  
		Size: 20.2 MB (20155362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf48aa6b9536a40dede0911aadcf30219099f98ef3110e93ec66966f1fe3d90`  
		Last Modified: Mon, 15 Sep 2025 23:14:09 GMT  
		Size: 49.4 MB (49414738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d409e83e099d4de5aace938047d5234510139774fb1ae2d5d875b9dc7aed725`  
		Last Modified: Tue, 16 Sep 2025 00:14:38 GMT  
		Size: 209.0 MB (209040476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4363ac553bd6cd997b5a84108ee49f46dac6c92499ea52db5c96e5143bc7bcde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11975606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856f394fa0fe00b1a33cf3fad8ce2d2bdef7daa211a92f602124841d0369e021`

```dockerfile
```

-	Layers:
	-	`sha256:b8c65c19ac6eb0d5e9c368a7727688b7c5f3003379ee4c0b21f04b75e8b55963`  
		Last Modified: Tue, 16 Sep 2025 01:20:06 GMT  
		Size: 12.0 MB (11965417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aff59e92d3775c938b6bbac5588fcb859c4dd8f397c8a0c93cb103bbea207372`  
		Last Modified: Tue, 16 Sep 2025 01:20:07 GMT  
		Size: 10.2 KB (10189 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:89bcc690bfbe775e784864e4930d06e09abbc732ffe70522dfae50453a8c3a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255424499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4bcc63f810d87edc556b5e5df70476ef6c0e7bb3c5890bb991981ac6e8d4e5`
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
ADD file:10114ef0b2a9754f23d7fb435ea61b94bb321445f7265266c66bf4ff069986da in / 
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
	-	`sha256:cbb4155e6c1b850eb4480b08de2a9e6acb90dd08837756bc1647f535d025f8b4`  
		Last Modified: Mon, 15 Sep 2025 21:09:59 GMT  
		Size: 26.8 MB (26843807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec71301aecd896f276835da86ce14239083f765a1e273818df6ebc7eead691a5`  
		Last Modified: Mon, 15 Sep 2025 22:09:57 GMT  
		Size: 17.9 MB (17869049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7e4faff9e63402482c522f896062b775823dec4a4570a8d923179be27343c8`  
		Last Modified: Mon, 15 Sep 2025 23:14:08 GMT  
		Size: 50.3 MB (50283599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2382bbfcbe334d789f65763d336f392bebc26d59063da9c941a7ddbf77ed415f`  
		Last Modified: Tue, 16 Sep 2025 00:14:37 GMT  
		Size: 160.4 MB (160428044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d7c391d076c526d6d406f0e0e13e6ae6485b9741a3e9bcba65f086955c6cff90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11728171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781604f28308b9b684919a1547d9baaed9e76abfd959fb8dce0f0f6cd1bdb7b0`

```dockerfile
```

-	Layers:
	-	`sha256:094839aed09272dc609a01b2a8ce2056882fbf5294fd52dd9e1b03b0e357613d`  
		Last Modified: Tue, 16 Sep 2025 01:20:17 GMT  
		Size: 11.7 MB (11717918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93667496b1004423e362de783d3d08978aee6674b208f8ed749115c24cbc9f01`  
		Last Modified: Tue, 16 Sep 2025 01:20:18 GMT  
		Size: 10.3 KB (10253 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6888a9f0d88f1b255a7cf7ca76f320b0cbf77db3eb4ee7e83baffc9b7bc4401f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288738260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8126d4059e71d97a1fb18b5339ee4905cdeb4c020378064067818125fb3ebf94`
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
ADD file:1d0db44377aa33c495de438dd435408b4391cf11e887ef1a542a8ab49275c67c in / 
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
	-	`sha256:47429ff9cdd3006afbf0a7a02f144b5a7444e546614a97a12fd567f7a4e3afdb`  
		Last Modified: Wed, 10 Sep 2025 15:57:53 GMT  
		Size: 28.3 MB (28305856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10315f775138ab7163eef3727c6dab9223b7bcb7a298fa6c0bfbded2ea9618ac`  
		Last Modified: Mon, 15 Sep 2025 22:11:59 GMT  
		Size: 19.2 MB (19157502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f424115f422524d8669feeae705a3eb75b88f27a52e5374250b57f1b9d36d2`  
		Last Modified: Tue, 16 Sep 2025 00:13:14 GMT  
		Size: 47.1 MB (47129681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f9469477e8c0e1a2fe85f13c6c2124457fd6107ea8089774ad26a2dbb548a1`  
		Last Modified: Tue, 16 Sep 2025 00:14:40 GMT  
		Size: 194.1 MB (194145221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b0fb8aa316168fc6a9999ae775c2dbfe2405ccb947d062d1c9b2969a2a3553db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12038942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:593b573b0efdd59074ce655019a8babd078edf1b9c287c0efea24c186845ef58`

```dockerfile
```

-	Layers:
	-	`sha256:cd8b11f9b28fa55c97c9d14167c98ce79601caab642afb18711f98412bec61b6`  
		Last Modified: Tue, 16 Sep 2025 01:20:27 GMT  
		Size: 12.0 MB (12028673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e78d3f588fc574c33bf611c4efaa29dae446100adadcf47fcf0df46448e69a7`  
		Last Modified: Tue, 16 Sep 2025 01:20:29 GMT  
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
		Last Modified: Sun, 17 Aug 2025 07:11:16 GMT  
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
$ docker pull buildpack-deps@sha256:d20ab355473dae1a44d9728599195723ac80770a2d82524f92a65d2ee8e0dcc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.2 MB (398243879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b44150bbaef11e523b8b4658c7d33ebaf9307832e9e0a67d9494667403edf3d`
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
ADD file:6deeb8ad1cf6cbcbaeadf271398b84360ae1aa44c52589c5a25061070904d259 in / 
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
	-	`sha256:4dbb31f8610f9a26c0e0287f94383b3fdd5b82ca5cff6fb36074b179a1a762ea`  
		Last Modified: Mon, 18 Aug 2025 06:51:45 GMT  
		Size: 29.7 MB (29736585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e174fc97d5309e505875653aa9c1975ab84d1b6475850d214ebef84c966dbb8`  
		Last Modified: Mon, 18 Aug 2025 20:07:27 GMT  
		Size: 19.9 MB (19891636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a542fcd16befe20d20f03c94c1d6fb003cb3c6b88da348b633d1e794d099e004`  
		Last Modified: Mon, 18 Aug 2025 23:53:44 GMT  
		Size: 55.3 MB (55253019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16aaf81c6e1e7016143a1b73c477d4ad6930f5e42355d8043f5b08a94e13bb9a`  
		Last Modified: Fri, 22 Aug 2025 18:10:30 GMT  
		Size: 293.4 MB (293362639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:67eb2877639dd370a9bd08bad8d5b8dccd3bd18bbb0858ecd2e2d615800338cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12013250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8114da212e41d242dede95b57ef5f6f2b296c1776edfcce46069c3462ce80ad8`

```dockerfile
```

-	Layers:
	-	`sha256:2e3b6e65a705dc98a0f43475aa533915470f1ca5286683d9fb95a37151c2a32a`  
		Last Modified: Fri, 22 Aug 2025 04:19:56 GMT  
		Size: 12.0 MB (12003029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fe4d15d80e361614cbf8d58a9ea2344ddb823313ba5e19c88b2dd8e727ff599`  
		Last Modified: Fri, 22 Aug 2025 04:19:57 GMT  
		Size: 10.2 KB (10221 bytes)  
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
