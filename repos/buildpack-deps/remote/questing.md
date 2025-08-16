## `buildpack-deps:questing`

```console
$ docker pull buildpack-deps@sha256:0401841c42ea8f01076e651402000c50836291f4d81bd98c45ef10fd369ce2fe
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
$ docker pull buildpack-deps@sha256:46dcf56347f47805aa8e2cd664057df4a851142b5d8a93dae5347ab6bf12537e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **714.6 MB (714608299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3f02d0b0b7c7b8c990cd8870e385abe3beeabc4d1311c8cd9bbaf3ec15215c`
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
ADD file:a74a840d4eedf15a85cf6d55ff2e2efce2562bb735481008b7b05feab3e31a41 in / 
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
	-	`sha256:17bdd67b6aa5856e02c1b36cec4ec29df1dacb071c5f6279c9aea0a311ee1058`  
		Last Modified: Sat, 16 Aug 2025 00:41:51 GMT  
		Size: 29.7 MB (29740502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be79c5851a446b3b5b175c8d0ac3f08bbee9078a0b4863c6e57fefddd86b32c0`  
		Last Modified: Sat, 16 Aug 2025 00:49:30 GMT  
		Size: 18.9 MB (18862801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837b1c4b03ec273ca0621a1a2eee5af08d62b0e1a1b7d7d4784d47d5b54b769b`  
		Last Modified: Sat, 16 Aug 2025 01:08:49 GMT  
		Size: 47.6 MB (47585971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615fdd64e43ff7f2cc548a3ff5c550f4772213252077d3c488c3710555c7c666`  
		Last Modified: Sat, 16 Aug 2025 02:10:22 GMT  
		Size: 618.4 MB (618419025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:eacdfcc7787fef9f034a3c8443ee2d8eb3215c9e46a322d9ab2107a9c4fc95f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12032305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf0fcc982b69d3ed3aefba09dbd6d97283cec22bcbb1bdecbd40da1ac39135f`

```dockerfile
```

-	Layers:
	-	`sha256:471cf02a14c6de6e31066fd01bd800160daa8b58b26d5e08cf30ab8f59607c26`  
		Last Modified: Sat, 16 Aug 2025 04:19:51 GMT  
		Size: 12.0 MB (12022102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bebc55a3b8f55d60a2c700fa606076c38f44832c47d1eaeafda75a68581ed1f`  
		Last Modified: Sat, 16 Aug 2025 04:19:51 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d52c8c74697eb03419f26f3ce7fce1f28ae6f40f531815f412dd6034de015301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.1 MB (633079395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6a5d16879fb3300dd6c4e0b031b052eeff1c4ee7012e1081a7b46c9b2c7e57`
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
ADD file:9eed1b2293ee9b1a3f538aceaac3ea32a998f61f054dad9cd5a407828bc5e7fa in / 
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
	-	`sha256:0d7bc1e0094544c65656ef653b3c67a22bb857cf01de93e24e36a5b8bd9c6839`  
		Last Modified: Tue, 12 Aug 2025 17:03:09 GMT  
		Size: 27.7 MB (27736612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d602962dce0a4ffd02b7128b627e79af88041418e069c243e79a489d2c76cc9a`  
		Last Modified: Tue, 12 Aug 2025 17:24:45 GMT  
		Size: 17.3 MB (17259013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af33432f0724121e962e4b411da290ccc76a6b8c0919ab48a491d6134ccb2b7`  
		Last Modified: Wed, 13 Aug 2025 17:21:43 GMT  
		Size: 52.5 MB (52535352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958f24c9a66fa92ff8c4e603fe28448f35ff37bef0e9b4eb979d10565957d42b`  
		Last Modified: Wed, 13 Aug 2025 17:22:15 GMT  
		Size: 535.5 MB (535548418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1dbf9882366c9486aeb7f03dacb8e6c5ff8835b895b8d01e902f6951de53df08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11771501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eda36ff706e93cc3279cc10815e5453cbb53f1b6e107c1dddcb10fbe21ba2c7`

```dockerfile
```

-	Layers:
	-	`sha256:ec5439feee469094395876addf529d64d9f6b81d02d148922fc676cd69735957`  
		Last Modified: Tue, 12 Aug 2025 19:20:46 GMT  
		Size: 11.8 MB (11761238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d69f4839a4dfdc111b76c8404b4e8a68802ecb78a79891ce18ee0aba0bbb84c`  
		Last Modified: Tue, 12 Aug 2025 19:20:47 GMT  
		Size: 10.3 KB (10263 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cfe13239a9125897c613b1b5bdb9d411daa00b0b7913ecd3151cb36dcd22ead9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **725.0 MB (724991350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61fb1e8badedf1f9f034c632916c7613106ffeb120ea1b490be192b7412d63d2`
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
ADD file:ec3f48e621d9128ce28e8aec63d50c4c4eefc59528b99116bbc3032f4279f5ee in / 
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
	-	`sha256:c6f3bc6961ab41704f6454c7be252d2be9e9153165b095e56dea5e0112de7753`  
		Last Modified: Tue, 12 Aug 2025 17:03:14 GMT  
		Size: 29.3 MB (29314444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47763b1514857655ffbc66a9fedccd790dec27127100e6dbf9ae3a5fdc7b6d8`  
		Last Modified: Wed, 13 Aug 2025 17:21:13 GMT  
		Size: 18.4 MB (18384151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628b6434ea47d356ba7c65e3f77d6bb7f6f2d54d59b3b4d635243a46a8e69e3e`  
		Last Modified: Tue, 12 Aug 2025 22:16:19 GMT  
		Size: 49.8 MB (49778583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc10cf72c70a869a8e64cebe473c76ebd46448c4b53207928cd187a4de1a8c6`  
		Last Modified: Wed, 13 Aug 2025 17:22:04 GMT  
		Size: 627.5 MB (627514172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:82f24bc375a62ccc2f75e2331bb87f4ac6da083b7ecd2567c2fa3290a3b57d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12083939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10d9d270266112eeab6be67be5f85e85e2a012c429971849ac2c7a7cbc949abe`

```dockerfile
```

-	Layers:
	-	`sha256:cbac1b6c15865d652c5a2fb3d850d20c547f5b3ab1591ece007c9491a8fa0195`  
		Last Modified: Wed, 13 Aug 2025 07:21:04 GMT  
		Size: 12.1 MB (12073656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f63d2b7756e7bf6f7f32d0c650ea99051c8dccab4499d2f6933ed0c4a5e668bf`  
		Last Modified: Wed, 13 Aug 2025 07:21:04 GMT  
		Size: 10.3 KB (10283 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f141f725d5d067825386ebed72bb4bdb47a485f29a841e9e167e9b884662b3c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.5 MB (678496867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7fb4b0fc73a4657110ad457994998585ff957bc656ec97d523c0327cf114491`
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
ADD file:566d1fae557135e37d75df659c267bd6a62cf94b1fcfe7e157578d9270ef463a in / 
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
	-	`sha256:0b1109ae8bd2c2ee8f31117236bd09c15587a8d6ba7a611f16c4200c2bb761de`  
		Last Modified: Tue, 12 Aug 2025 17:15:59 GMT  
		Size: 34.1 MB (34111991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eca0501624351fb3456fb0392bb33c5140287cc91e607e55eed9b0d1cd8846d`  
		Last Modified: Tue, 12 Aug 2025 17:27:55 GMT  
		Size: 20.7 MB (20745823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a06657384bb754cb4b3846f3caa8a12bcc375aff96c2b369a2a25369b0d022`  
		Last Modified: Tue, 12 Aug 2025 23:18:47 GMT  
		Size: 55.7 MB (55704378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ce8d46f7a1acad18f796ca3d95c5c56117960e5cd3ba0170ec4adcec8dd087`  
		Last Modified: Wed, 13 Aug 2025 12:34:13 GMT  
		Size: 567.9 MB (567934675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0359dda2eb73457656b2647622a067ce8c4f33a9cb59bc2b4a527daa13668ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12000276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a927f3e5fe567150b36b8bd68de2c65dd8eae5b319471281bbbadbf7ffa8e6`

```dockerfile
```

-	Layers:
	-	`sha256:fc08021117faa54b4e3c9b5bae9f819b75757cd842e438604568aef9f0dfca7e`  
		Last Modified: Wed, 13 Aug 2025 13:20:03 GMT  
		Size: 12.0 MB (11990041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:148fc667a4891e8b151a95154f0cc6ad10fbfbc505e256cae4a384b6bf71814d`  
		Last Modified: Wed, 13 Aug 2025 13:20:04 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2c0d10ce6c03ca3642dc92d17b7930a0392d9a83e04f22d428b7f965e4f5be34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.1 MB (627133137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ac21f308f7e330094c7737cffe988d2ba092164fce2f0b3cb3b620312c65f7`
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
ADD file:2ad5f91fe5edd35a8a0cb6ec99904a35771f2b8a0819b888cca27bd2b8edc998 in / 
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
	-	`sha256:c765da7735337fafbed911e71485d7f0505e50d1941beb7fa962494422b6b9be`  
		Last Modified: Tue, 12 Aug 2025 17:03:53 GMT  
		Size: 29.6 MB (29618719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b53c981ca1715af0d0448a048d0a4642c6a7becf08354f007f4e1da1b9569b0`  
		Last Modified: Tue, 12 Aug 2025 20:19:20 GMT  
		Size: 20.9 MB (20949219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b53944a72c5140ac1e0979538c80a60692cb4b9b098e1921d41485efb62ee5`  
		Last Modified: Tue, 12 Aug 2025 18:44:14 GMT  
		Size: 51.5 MB (51546811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24daf8916cc251079043ed6b939949fe37c835dd083044b0386971a971198aa`  
		Last Modified: Tue, 12 Aug 2025 21:08:58 GMT  
		Size: 525.0 MB (525018388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:908cb9401d8e9eb1ea92a298a15267e34e74976191e2d4c460c1c1051db5d262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11804978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ceec716e967fa1f92e056b487beed98b3ff1c77427252721f34d5bb305ddf6`

```dockerfile
```

-	Layers:
	-	`sha256:23f81e245c061f8506c0e79b93ff0b25916a6ebbecdd988489a8d365807bf0eb`  
		Last Modified: Tue, 12 Aug 2025 22:20:36 GMT  
		Size: 11.8 MB (11794775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb2c466b3f724eb1ec0bf59e6889dfd1eafbed7a81df7882e7f64f40b46afdcc`  
		Last Modified: Tue, 12 Aug 2025 22:20:37 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json
