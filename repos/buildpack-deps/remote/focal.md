## `buildpack-deps:focal`

```console
$ docker pull buildpack-deps@sha256:2de32588f72f63229c83e3f08529cc15db231b2d95412ab4c30ad49d7cd99591
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

### `buildpack-deps:focal` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:40237ab74606fa355747b8320c7ea04bdfa33506d1bd27fd96d412d5e7e79bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244580116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7f9f4291dee0554fd9250ace2aa69b0fdb23746d675a9fe7ac6ca4dfddded97`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7577a2ab12ee9be5df3b0c322f8c7e4cb7d72c7826b239c5a9581720d332213b`  
		Last Modified: Wed, 09 Apr 2025 01:45:55 GMT  
		Size: 11.2 MB (11150331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c877c591199a05136cbe615838a58a7f442fd6f8ab6f1220d44832d7d85f20`  
		Last Modified: Wed, 09 Apr 2025 02:12:02 GMT  
		Size: 60.9 MB (60945274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec59412da6cf45ab9e51d160d0581ceb16aaba2b62336320ea803478b8e7ec0a`  
		Last Modified: Wed, 09 Apr 2025 03:12:03 GMT  
		Size: 145.0 MB (144974117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:focal` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:52fc601d3dd8affe2f5418518b99b1cbd1504494573810c19a0199f4414f1d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12271655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a71bc1c0274000a86e3f200ae04fd1d85c6c1cbfe6f9cc044868eaf5b5dcd25`

```dockerfile
```

-	Layers:
	-	`sha256:bfc81b03a88bd756c28be527160fb386ad93d47dd041438fbe8aad4dce378c95`  
		Last Modified: Wed, 09 Apr 2025 03:12:00 GMT  
		Size: 12.3 MB (12261450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a58cfe61629422fa68cbc2c3251d08b9710f07b909cf0f66a15426593fb7da09`  
		Last Modified: Wed, 09 Apr 2025 03:11:59 GMT  
		Size: 10.2 KB (10205 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:focal` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e303e1b2446f649d83139b176c57e51cf84833273e143f0719ce175361d229ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210900777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38bd94ad4ec2a558f1dc9052293172c7eaf4041ae15b5607a997bd41ac16a783`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:bd50d86208ba682c6f55f52b7ec95adbfb2e247d9dfff47b9c3871d27a7b0d19 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:12c22ff1560db33ab4235fc5b1744509b7c274b95beb2a7ba7b6671705fcef6e`  
		Last Modified: Tue, 08 Apr 2025 11:48:35 GMT  
		Size: 23.6 MB (23624063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da7e36a763f959e9959a67d83a9318d563b85525cd5898dd19774da499cb0a5`  
		Last Modified: Wed, 09 Apr 2025 11:32:37 GMT  
		Size: 9.6 MB (9620939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df8cfc1c5d2280abe333b6e3ae8d6c857a34aec7fca5b6203efa3d9438d09a0`  
		Last Modified: Wed, 09 Apr 2025 12:17:38 GMT  
		Size: 55.9 MB (55878359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00ff032036807b3c904280e2acbf14eb042da6867092572943fd61d2dba3090`  
		Last Modified: Wed, 09 Apr 2025 13:15:27 GMT  
		Size: 121.8 MB (121777416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:focal` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a4372f1636750fe89babd62d6a2ba1066b497d70314aeff949fac7052e1b5e34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12087540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d545c40b182ec0fc3c4e6fdfd01704d846c68de7538dc6243af05c2f1a58e9e`

```dockerfile
```

-	Layers:
	-	`sha256:782dd4e7f1abc24bd3f059b1a4423581b9eb9172b5231b5c76699833de5a79ad`  
		Last Modified: Wed, 09 Apr 2025 13:15:25 GMT  
		Size: 12.1 MB (12077277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d63a02c213f47113fefb22648a1464c794a5cbd82ee7d3ad2495a74f72c78945`  
		Last Modified: Wed, 09 Apr 2025 13:15:24 GMT  
		Size: 10.3 KB (10263 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:focal` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a25455522d1e9d512b16e21bca820fabc9fa1e8bb600cfe361a078bf038a3dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.7 MB (234653317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511e513fcb7919c2a2a14e081a8ad758f62b793a02dcf907f19bd5334482094a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03900f2fdf5974424bfd298551b0e62da0045dd4710d9615492752026efcb4f5`  
		Last Modified: Wed, 09 Apr 2025 06:08:33 GMT  
		Size: 11.0 MB (10990957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efdcfee37ba889d2ad71993cf205f4b2dc389a010af39dbdb021d9dbe7eb43c`  
		Last Modified: Wed, 09 Apr 2025 13:57:07 GMT  
		Size: 61.0 MB (61043214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d4c58a6b4c37847e25951dfcc678eea2036942c4d38e71fc30ae667ac3d9c0`  
		Last Modified: Thu, 10 Apr 2025 00:18:30 GMT  
		Size: 136.6 MB (136641485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:focal` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:096c6a17f811b05875fdcba9d8231737705b07ba1fbde5bb928f98e92da930eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12276175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9370d4c7d52e8cb0697163e2fa37f7a450cf07c9981e9645a20f5233ec5dbb7a`

```dockerfile
```

-	Layers:
	-	`sha256:3a031e7f25a33607f54626a0144f7de9ccd40f9117f283da1fc5d7d8949266ba`  
		Last Modified: Thu, 10 Apr 2025 00:18:27 GMT  
		Size: 12.3 MB (12265890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:571af1d3e0ab129013a9fb0dedf8a2b6b4aaf8574d174497179fbfeff5ac47bc`  
		Last Modified: Thu, 10 Apr 2025 00:18:26 GMT  
		Size: 10.3 KB (10285 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:focal` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:567ed8b58edf586e270e38c76633fb88fec88485cd9d26be9b08f954625b58d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 MB (268173043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f458e69daa74f21f62dff9526c0a729d7b57bb86ac7da77666255b111619973a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:d85970cec61787609e3854cb76ce16d54fe420b254cf48fc9ed9ed678717ff28 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:92d54367a68b4f03400315732acb4290d88bb06f8fe1414fd823f93402bec922`  
		Last Modified: Tue, 08 Apr 2025 11:48:44 GMT  
		Size: 32.1 MB (32076946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbe8b02ff52733b6c9023254a29940996cd72195264668a2791dcfbd8d98610`  
		Last Modified: Wed, 09 Apr 2025 04:26:54 GMT  
		Size: 13.0 MB (12963091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a47c8098863d5f0589ae9f6a551c0ff5ca0ca9faf3385f60c211a8c0999d57a`  
		Last Modified: Wed, 09 Apr 2025 07:34:19 GMT  
		Size: 69.7 MB (69680780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4253b6a4ca2adb08dcc662a8f1cdd08f9073e8a2c886d8655ec34423b5c0a74e`  
		Last Modified: Wed, 09 Apr 2025 13:24:29 GMT  
		Size: 153.5 MB (153452226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:focal` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3395737b2f25a4453c1eade5bdefb9049c817d9167d9d3b9894993088c9d7b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12244186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6400a7fb05076345a0007cea5e8d84bf90b13a33f84343394f268bf649ee6c`

```dockerfile
```

-	Layers:
	-	`sha256:bac59377690afe7e9fca3f5ce2b3865dc898754dae9ddc04eb13e77b5222d3c2`  
		Last Modified: Wed, 09 Apr 2025 13:24:16 GMT  
		Size: 12.2 MB (12233950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5176aa4000aff16fedeac93ef87ba7fff5b1ba8a1bd6ba9240c7c7fd3464e22`  
		Last Modified: Wed, 09 Apr 2025 13:24:15 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:focal` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:27e7579fd75f8d3c688ec536af77cba1006a288078005b421a30a6a11cd7b395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.8 MB (225797428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f904f089f6733c628e5de524d875e09e88d55f7f62446e509a14692616707440`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:82f0132f510f24adc12d74491187647b94a14baa7a57fd22a67a5c3767541496 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b35596e17e863edd4c594d026a60e36f73cc6a076370f55a24732114fd25ff68`  
		Last Modified: Tue, 08 Apr 2025 11:48:56 GMT  
		Size: 26.4 MB (26368190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4495dc22cf93325906d3dc47401597dbe3f0e5d18ba19d26285034bdf0c41a02`  
		Last Modified: Wed, 09 Apr 2025 04:10:51 GMT  
		Size: 10.7 MB (10702249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6fe3eec205cfbc7c8ab84f500e3b8710bf1bbea0a0750d4c476d2160c50c2f`  
		Last Modified: Wed, 09 Apr 2025 07:07:21 GMT  
		Size: 60.3 MB (60346452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1451138ae428c812f5c9630a06a566fc5a984021aa5efeedfbd09ecea4cc620`  
		Last Modified: Wed, 09 Apr 2025 10:22:10 GMT  
		Size: 128.4 MB (128380537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:focal` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:30c7664245969828397555157bde4c714547c4d25401dfd42fb3333c9304eccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12108134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e596998d123103d4f921a226398a465988594a5c398b297cd0fb59e45bce600d`

```dockerfile
```

-	Layers:
	-	`sha256:44851f3e86a455d26ef2e15abe4f10dfeb683891478cb91d027065775e9f1ef2`  
		Last Modified: Wed, 09 Apr 2025 10:22:06 GMT  
		Size: 12.1 MB (12097929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc0eb3299ac6c64fecfecc6e7dc24e270e586243b0a1c4bad4d3d70d72c5eb6e`  
		Last Modified: Wed, 09 Apr 2025 10:22:06 GMT  
		Size: 10.2 KB (10205 bytes)  
		MIME: application/vnd.in-toto+json
