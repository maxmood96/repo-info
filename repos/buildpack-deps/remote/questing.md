## `buildpack-deps:questing`

```console
$ docker pull buildpack-deps@sha256:642e7e6022be5ef28fec24caa6e1e4c8f8c29ceea3eb5cbfe3719f6586eb74a4
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
$ docker pull buildpack-deps@sha256:138df11114ceb636b188f81ca4201cf15ac579e03a31c1ec330cd8f1bcffb56d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.0 MB (273047330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32bba209b8a19e6a871e495d3c4153345cf5b913ec9f99aff92901831e48c3b3`
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
ADD file:7992b30df2d5e1a9868a357037fee7a935fb600c535045c3dae00a6d2da0ffea in / 
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
	-	`sha256:9b965cd3592863b7a60b38bfeed24007834fdaf4994cb2c642c14d872f7ba0d9`  
		Last Modified: Thu, 09 Oct 2025 21:06:04 GMT  
		Size: 34.5 MB (34453346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7576d1bb6bbc5cda3456d256501881b6fe33fdd86baf9d81e296b44b4629ac72`  
		Last Modified: Thu, 09 Oct 2025 21:09:12 GMT  
		Size: 18.9 MB (18935913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01b2a607449ed42f8af633598423c355d043948545b440f818a3041f97a9533`  
		Last Modified: Thu, 09 Oct 2025 22:13:55 GMT  
		Size: 48.3 MB (48274512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a12a90845480dc0abdf738eb1a24df77d2104cae240c2aaba2e4b288ddba54`  
		Last Modified: Fri, 10 Oct 2025 03:31:51 GMT  
		Size: 171.4 MB (171383559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:17816f2f423d432b0c1d2e6612967019175e0f1dd7f0805bbd0208d64c8cc400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11718587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d655dba257c5097c496ca3b1f090286cf58d72d38cd45b66475f8e5a32aae0b`

```dockerfile
```

-	Layers:
	-	`sha256:91e3ec89c2862ed18e31a0769fbb4ecdde6a7a357e0daf90fb0631e0d34ebc28`  
		Last Modified: Fri, 10 Oct 2025 04:19:50 GMT  
		Size: 11.7 MB (11708385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21c553dbc66590ff8fc0b278a9f22aa575073508dfebc3183eaa3ed78be24882`  
		Last Modified: Fri, 10 Oct 2025 04:19:51 GMT  
		Size: 10.2 KB (10202 bytes)  
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
$ docker pull buildpack-deps@sha256:f879fb61719622f5f59242bf5f0785b96305a0016795cafe715b868762e0296d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261381684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adbed856e2bc3aeaba0a5f3d36a94e820538c5232d04c11832e685b5b6a5999a`
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
ADD file:8ccca3821827ab9c5998bd942e103c70878335f75be5b71b28f3fbe104f6c658 in / 
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
	-	`sha256:4d90657552ac1b6284508877841188af829f382e60eeb51a71e7aa12b4a521b8`  
		Last Modified: Thu, 09 Oct 2025 21:05:33 GMT  
		Size: 34.1 MB (34071074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae8e65d481c24454a1936d3603010aecc1bac389df893175bccd3d0809a7506`  
		Last Modified: Thu, 09 Oct 2025 21:09:35 GMT  
		Size: 18.5 MB (18494427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f27663259df5fc48d274b5c5cee2aa50d96334d72713156abc98f7fd8d3b81`  
		Last Modified: Thu, 09 Oct 2025 21:32:26 GMT  
		Size: 47.9 MB (47923769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e6b0ce92272c3cb0da7e982e1d6706806dcdae03254fc2425125baef61ccf8`  
		Last Modified: Thu, 09 Oct 2025 22:16:09 GMT  
		Size: 160.9 MB (160892414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f1026c6cf282e04bd3ccb18f081d79824d7b12067fdca8b1292cc4e9899dbeaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11772843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d48299973443533dee1d91795490a81032aed195cad87d382a5b665ce3c36c6`

```dockerfile
```

-	Layers:
	-	`sha256:49f6b79d0710d585e961fd030657f5d2d7e2f4679cfd143321dcdd35c6c15b9c`  
		Last Modified: Fri, 10 Oct 2025 04:20:08 GMT  
		Size: 11.8 MB (11762561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dac4ee9cd74f10b69c714d724f7c5bc52a8948ffaac60178b3b4716a78f68eba`  
		Last Modified: Fri, 10 Oct 2025 04:20:09 GMT  
		Size: 10.3 KB (10282 bytes)  
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
