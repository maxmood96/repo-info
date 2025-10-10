## `buildpack-deps:questing`

```console
$ docker pull buildpack-deps@sha256:f7ee38f6ebff2ea90743ada41dba740613b7c4118c27dd96bc6cea0c06852530
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:questing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a0f46ba170767ece4f8b148e1760c37eb92ac21f6c2a15264190ab08146c8436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.1 MB (721137954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ba8062115e2afb7722923063ba6d4cb68510a95b7b6921b1f242f4416fdb43`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:3e1fc6c64a64de6123cd187bfc3549ceab9f37ceca8ba0d0e9addbc07a5d53c8 in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:21a6916525526a79befc4836ff7c3c0e74713ee310d255c8da8f58b9a151659d`  
		Last Modified: Mon, 01 Sep 2025 22:59:17 GMT  
		Size: 29.9 MB (29867188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e224a77ce8b9fd8b90f0b4539e5eb08bc23c4e2886afe48cd36db172a7d2959f`  
		Last Modified: Mon, 01 Sep 2025 23:08:41 GMT  
		Size: 18.9 MB (18931646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5882be4ee48f16cd22475acd3bd5968b81e7faaad2ed80bb1914300f3925b0`  
		Last Modified: Tue, 02 Sep 2025 00:12:14 GMT  
		Size: 48.4 MB (48350551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3f386cf3e715845e723299bf17a1030f43b388a6d42c2673cd7dac8fc62978`  
		Last Modified: Tue, 02 Sep 2025 06:26:49 GMT  
		Size: 624.0 MB (623988569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:738a8cfdb1e3c96abc63ad2b82e172277c4c1cff82eea2177d94526fbf6ec53e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12028511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae9241fc47e784087b9bd895406faad201ab3de8f0bcfa72e5e7f0ee745c2fe`

```dockerfile
```

-	Layers:
	-	`sha256:bb4f46c3369928d88023bd390fd5cb3450e3488a033a1af77e44b881d011ecd2`  
		Last Modified: Tue, 02 Sep 2025 04:20:13 GMT  
		Size: 12.0 MB (12018308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2a3553bbaa275d33e698be346c60ac12b3d6b3fd82d452f1c0f9d61fcf9b419`  
		Last Modified: Tue, 02 Sep 2025 04:20:14 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1669864506c986b84134962c59d9c205e449ab7430a2420e21714389ee5a7905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.2 MB (225221215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de12f1728df4df60f9dd9d1fbf91587458069b875235512d6cee435914b8a331`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:8bbeb482f2b247bef1627efb419885c5e995c29ac97454dfbe51dfc4ecf549d2 in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2d9a0dc3298847c4f5e3ffc1427dcb99ebe4c8fbb1c040628256b603b41f715b`  
		Last Modified: Thu, 09 Oct 2025 21:05:13 GMT  
		Size: 31.8 MB (31837227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5789843bac3bfe60c050b74177d6bdef81818507b015abb59a7fdba7199764e2`  
		Last Modified: Thu, 09 Oct 2025 21:08:26 GMT  
		Size: 17.3 MB (17313855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002109b64c318f0cddb99550d76900ca955f79ff25683a2f5e00126fe7346c26`  
		Last Modified: Thu, 09 Oct 2025 21:18:06 GMT  
		Size: 50.6 MB (50563068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f4147480bbf3de322aea9c28cbee57e79248892c8367c8e283eaa9625f5a06`  
		Last Modified: Thu, 09 Oct 2025 22:15:43 GMT  
		Size: 125.5 MB (125507065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3f367196b0165bc5b06fbc09d181fdddbbd37484f70260e5ed86c504a55c9632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11460187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e16bd7de0fb15d59b67c4b6b7a879cfcec1ac252dfdecac468b5da9de57e53d6`

```dockerfile
```

-	Layers:
	-	`sha256:f30c4118a8aa27f273917d84a22adf8472ac84d59eabff2398a2aaede29ad134`  
		Last Modified: Fri, 10 Oct 2025 01:20:10 GMT  
		Size: 11.4 MB (11449921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d90be72f12008b7325a83ed2a17fc7afd1ee3ad37343c0c4f10dc8d1d91f8964`  
		Last Modified: Fri, 10 Oct 2025 01:20:12 GMT  
		Size: 10.3 KB (10266 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1dee248069c73878592ca9c2813b498c8577eba15b49f9c28529064b3dc683c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.0 MB (719973448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:761239a3c285508ebcea9cfdfed7ab6e13946af22e4314116bf3691acedff25d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:19248c5112de8819af31f1004ee6a9219793a6df0d44a4fc6cc1be08e39db7ee in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7d6568191452cbdd8c0679323e9a94d03a75b9163e71cb4bd79ef11a7ee6864d`  
		Last Modified: Mon, 01 Sep 2025 23:13:40 GMT  
		Size: 29.4 MB (29434129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3bd093703175385b11e9b309ef9f6c7f0a33cb398834dc17a287ea617cac67`  
		Last Modified: Tue, 02 Sep 2025 18:34:11 GMT  
		Size: 18.5 MB (18454215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a998257116262cff14f4f45dab37a436e6e43c88aaa707500cb6ba034c0365`  
		Last Modified: Tue, 02 Sep 2025 03:47:44 GMT  
		Size: 48.1 MB (48062869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71eb5d26d995f5b48cf370c7427085ddc2ca8145e877cc3d6213f2554542fb9`  
		Last Modified: Tue, 02 Sep 2025 18:35:43 GMT  
		Size: 624.0 MB (624022235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fa6355d195ac28707514214b750187b748bac15ace5da8ca6699fdc0e6555666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12082886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e926ee418175a474bb59f07896fe5da3fabfd75a2ad68ff4cec166241f08f10a`

```dockerfile
```

-	Layers:
	-	`sha256:9a9edc9c099d83fb99e9b9cf60156073ce495f4896b16e790cf203b72f891859`  
		Last Modified: Tue, 02 Sep 2025 10:20:01 GMT  
		Size: 12.1 MB (12072603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98fda4b431967cf0d610454b3d6b2a1a1785cf51cfe85cf42a5bb7bbb08b7c3d`  
		Last Modified: Tue, 02 Sep 2025 10:20:02 GMT  
		Size: 10.3 KB (10283 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:74888ac8501f6bc772af24896dfcb4662bb5285e245de26a8fce5323f6d6080c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.1 MB (668125984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:947815e4d59c84614bc06c79a168e6a9c1ee1b4126b520041d8fd586850733cc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:49e4ea796fe843e65e0d5fb09f0a6555704c063422825381bdb201d4843cfe12 in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3c8ebe2b438b5cc9c96e61725caa750ed639e2764eaf8da3c5a76f2580c4259d`  
		Last Modified: Mon, 01 Sep 2025 23:52:51 GMT  
		Size: 34.5 MB (34480208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e0c9c0bc001baae6754cacd7396757d44d020b3a3ba6c5ec0a0d0f7224f934`  
		Last Modified: Sat, 04 Oct 2025 09:21:23 GMT  
		Size: 20.9 MB (20860809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e39d9a0fb42af6b523f27db319d34fe787d04f59d17372e4c487e8f8f51a33`  
		Last Modified: Tue, 02 Sep 2025 05:26:52 GMT  
		Size: 53.7 MB (53663473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a8ca2816d24def2efb1ed8e37364c5521c07d545b5acb743ffedb4ae075e84`  
		Last Modified: Sat, 04 Oct 2025 09:34:30 GMT  
		Size: 559.1 MB (559121494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:59807bfdd20ba2a5d6ca8615eab07c3f9449599dd46e541488e396515eef182c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12001676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01502885389899170ee55c4128edf01acdb11bd1c612fe4ec3583ec6346b12f8`

```dockerfile
```

-	Layers:
	-	`sha256:94bfb153808ee6696c11ab96c10fd2a3de6abce90efce1b48892e7ad723247fe`  
		Last Modified: Tue, 02 Sep 2025 10:20:18 GMT  
		Size: 12.0 MB (11991441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a715f002f84fba89a0c8cf51db0028e458aa0bbf1e0a0c00e442f6d188f8bf20`  
		Last Modified: Tue, 02 Sep 2025 10:20:19 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1e5b67e19fbc4cc7241a36b7efd3c3aab3bc56fdb03a776e77ac09c4ba2fb51e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.9 MB (617912621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c527434683aad1a3c0ed8f1cf176b44388ca2fc43c15ef86d3e9fb813756703e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:516af95a32cb0f359ae2fcbf9660395ec3a5a108f92c89ef32596ebc62c72a72 in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:750ad3720277eb112055a37a3c157bf6501faed8f33fbc6c22b30be0455266a2`  
		Last Modified: Mon, 01 Sep 2025 23:00:47 GMT  
		Size: 29.7 MB (29674908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e979693de6fad3a4fad4b978eff915f773a6bfdecfb5c2436a5bf6586e0b71b2`  
		Last Modified: Tue, 02 Sep 2025 01:20:29 GMT  
		Size: 21.0 MB (20956802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40615dff064cb8a1f03f35315e386e6c3412e2691c38301270897509fdfd63a2`  
		Last Modified: Tue, 02 Sep 2025 00:20:22 GMT  
		Size: 49.0 MB (49047270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6423c57bf057572f47f252c7ea178ec31849ede758fec3dccbd91eba1ecc55ec`  
		Last Modified: Tue, 02 Sep 2025 18:35:30 GMT  
		Size: 518.2 MB (518233641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:de4bc682638a5a97cc0fc0e2e0698997b4ead3ea73168ade917f373a9a348392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11803923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba202ef3d0b0d38ebb696bc13070b2c4b094957ac4fc702535973dff8920fd29`

```dockerfile
```

-	Layers:
	-	`sha256:0ad3ddb2aa1d995315d4c3b58daa646e54d059e98ec9945e1b649bdddd60eab3`  
		Last Modified: Tue, 02 Sep 2025 04:20:55 GMT  
		Size: 11.8 MB (11793720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acb15cdb6fafd03be0dd207358c87816e06be4ff1149f82a1a3271d107f4d13a`  
		Last Modified: Tue, 02 Sep 2025 04:20:56 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json
