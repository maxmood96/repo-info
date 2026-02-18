## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:83561ed416c5007baf6d10d065bb576996dd8bf52251e468acdd1de3c68bedd0
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
$ docker pull buildpack-deps@sha256:b5d747d293f20f6ce256eec1536d4a7f0466f7270039b1075c60f9f44401e9a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.1 MB (276101252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a832c38de1623abd17e2c769125031dd3bd94763d94c7df002e1ea036034e52`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 17 Feb 2026 21:16:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Feb 2026 21:48:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c8a6fb9740c3884e8704c3750f8ea0885ea49dcd0559b6345527766060a8d5`  
		Last Modified: Tue, 17 Feb 2026 20:12:03 GMT  
		Size: 13.6 MB (13627740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdac0592bf7abf5eca2187635c12f3b17e221c70870780e63d851bf19971904`  
		Last Modified: Tue, 17 Feb 2026 21:16:35 GMT  
		Size: 45.3 MB (45334710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ef649e58734e4b6394dc203c84adda0582264e0b7c5cc1ab3b093198b30229`  
		Last Modified: Tue, 17 Feb 2026 21:49:02 GMT  
		Size: 187.4 MB (187411191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:08061239f27485adc3c512bec8f3ac677977e6fc99755266c11a015a5d07c254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11743864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d68408c484e7bf723faeeca58f2d9151062487391bc1819c85bf9c6977abc27`

```dockerfile
```

-	Layers:
	-	`sha256:ba71feb03aa71fe78d3fde874af232282a6178217918c6d298c634deed2cb38e`  
		Last Modified: Tue, 17 Feb 2026 21:48:57 GMT  
		Size: 11.7 MB (11733723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47245686e52cc372bbafac7401a99213e5b141dd24b48f0480e4474676c87877`  
		Last Modified: Tue, 17 Feb 2026 21:48:57 GMT  
		Size: 10.1 KB (10141 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:134ebb86d7256fae1295a30e8b5171e61f4b50bb6e693a7d0a971a9050609be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.2 MB (238168580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99ce1f0ef2af95a8df08391348a7db07ce56c53bf5730cbdbdc2bc14143ada6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:51:23 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:51:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:51:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:51:24 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:51:27 GMT
ADD file:9633092e110ed5475e9e31841bcc6e288ca09c116e102d75694089f384f549b3 in / 
# Tue, 10 Feb 2026 16:51:28 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 17 Feb 2026 21:15:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Feb 2026 21:43:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:dd135084b7c993802b7c1ba97d192c201727ddf710812c361d5441cb729f5c20`  
		Last Modified: Tue, 10 Feb 2026 17:41:49 GMT  
		Size: 26.9 MB (26855457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86066a2c0cee319af3a1fc2959296da0853a5a25ac26fbf28428bea5a43b759`  
		Last Modified: Tue, 17 Feb 2026 20:11:26 GMT  
		Size: 12.8 MB (12785431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185437dab8e6448d6b1c6faead84fa77e5dce81c90e97e924a5cdd7730e0adc5`  
		Last Modified: Tue, 17 Feb 2026 21:16:01 GMT  
		Size: 48.9 MB (48866627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc2763d4966881a1d5d7112f3b765af5c1ccae5080fd5a84fb33d6311579536`  
		Last Modified: Tue, 17 Feb 2026 21:43:43 GMT  
		Size: 149.7 MB (149661065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:320388bc984abb49feb4e21858b2fb29376c1f30f7589c0990d880656be2a7ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11069608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:361f0cd43002a4541eae4bc023caa871f6fb2f81ccead976c25937fe8aa868be`

```dockerfile
```

-	Layers:
	-	`sha256:776d8f5c878762074b772fa069c123a36c5bcb79c2e6debbcc3755daffbc587e`  
		Last Modified: Tue, 17 Feb 2026 21:43:39 GMT  
		Size: 11.1 MB (11059404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b635cee867b349edb3078ddf3705378712b743b9dd93a751ecb61dcc008305d`  
		Last Modified: Tue, 17 Feb 2026 21:43:38 GMT  
		Size: 10.2 KB (10204 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d120f5b924618007bdaa2062a5cb6b229c3b4a59a07b3a8f3187b3e2b164ff7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265533713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0769efbef8276447b5f06d45bee6bfc7b6832b75eb99da7a1c725b95a57c6708`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 17 Feb 2026 21:16:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Feb 2026 21:47:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bda92f4d7534c4a38c86466cb58329d22d7c6ac91c27502ec994aeb6522d57`  
		Last Modified: Tue, 17 Feb 2026 20:11:47 GMT  
		Size: 13.5 MB (13462064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3561d00c2984fff5f0b19d42b750943f4109a740bc06eb4addae06668f956cbd`  
		Last Modified: Tue, 17 Feb 2026 21:16:14 GMT  
		Size: 45.3 MB (45272365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f002a6e98463985f932384c4eb1a3d784fd98d64fc54d948a99699bdd6f5dc9`  
		Last Modified: Tue, 17 Feb 2026 21:48:31 GMT  
		Size: 177.9 MB (177934164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e91c16047d38c06262f4c0f8aad62f787b9b4740c24c941b62efa6a7db02e39f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11293409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d5d6bb77cbb3026e0c736755f0750aa5f64896f04407289b735b7723b0a1f57`

```dockerfile
```

-	Layers:
	-	`sha256:841c7346eb985ca8284f3c26a61821ed447cc3a4ebfc4e881c4a63bbf4a544dd`  
		Last Modified: Tue, 17 Feb 2026 21:48:28 GMT  
		Size: 11.3 MB (11283188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6e61cab04a217cd8991427310c1bd9606ab48537e8307662272af03e25a53f6`  
		Last Modified: Tue, 17 Feb 2026 21:48:28 GMT  
		Size: 10.2 KB (10221 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:55181b8eeb2eceb244e3b80f8fc70c2c6ba20e30cc90f7fb75f4c78c5b002956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.8 MB (291788626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8323d99b2c9d532a8d9e9998de744e2ded759a9dfae73286fbb103261c9e4a25`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:10:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 17 Feb 2026 21:43:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 18 Feb 2026 00:20:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca93a66bdf3fa40b5c5ab2fa85f68e7a3ea39b2c49a65eefe83983c813fe050`  
		Last Modified: Tue, 17 Feb 2026 20:11:14 GMT  
		Size: 16.0 MB (15956288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482e92da14e48cff422152d5a995808a826a26b53a4abdf34ab18c4e4cc1095d`  
		Last Modified: Tue, 17 Feb 2026 21:44:20 GMT  
		Size: 50.5 MB (50452715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2889ee8e8acebd658032dc49df664547f003c9bd900f0c6553ae42d02668cea`  
		Last Modified: Wed, 18 Feb 2026 00:21:28 GMT  
		Size: 191.1 MB (191072717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a44e582ff0b690fd40f26775bfb5aca5be2f2c21b86545bca832e5e4d4d1a463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11240798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0975db933a906fee9cacc05f80f37893072c82f7fdca9fd0649bad65bb86a5f5`

```dockerfile
```

-	Layers:
	-	`sha256:1ed0282a7c0cda27b73e092cdb0ab42a14910ead64ca7ade2fdede761ab1d617`  
		Last Modified: Wed, 18 Feb 2026 00:21:24 GMT  
		Size: 11.2 MB (11230625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fb704314ff0089200d9fd4e1634d0af75f7b6436c06cde296503bd454b377ce`  
		Last Modified: Wed, 18 Feb 2026 00:21:23 GMT  
		Size: 10.2 KB (10173 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:fd3d0326f9afcb631284d9a013ed5ffc8e0638b1cb514e286d7657409c9f2db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330446115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2080a4b44fe51ea95ad38bcf4ed19f77ce08d821adcf3b905d42c178f182c42b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jan 2026 06:14:56 GMT
ARG RELEASE
# Tue, 13 Jan 2026 06:14:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 06:14:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 06:14:58 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 06:15:46 GMT
ADD file:8d0655de001e92042901c645c76202ac355acb6fa186561e7344a0829ffd983d in / 
# Tue, 13 Jan 2026 06:15:51 GMT
CMD ["/bin/bash"]
# Mon, 19 Jan 2026 18:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 20 Jan 2026 14:41:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 22 Jan 2026 05:56:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f151392858868452ec0f1f8d2947624e8dcdecf23bce587cfbd7c38a3264f9df`  
		Last Modified: Tue, 13 Jan 2026 06:36:06 GMT  
		Size: 31.0 MB (30953090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92aa37a63720515321479a1b97dc2892cdbe1fe7821a8e0975eaba80f062c279`  
		Last Modified: Mon, 19 Jan 2026 18:06:28 GMT  
		Size: 14.3 MB (14330939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dafa63c982ccb6c692e1e05cfd12ed9263e9ecf6d93e52b51783e4d8dd6ae0f`  
		Last Modified: Tue, 20 Jan 2026 14:44:02 GMT  
		Size: 53.9 MB (53875613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36210f70da4605504cba8c997c5e2642a1df25d6cb68c0ebe626944fd5a96bb7`  
		Last Modified: Thu, 22 Jan 2026 06:07:10 GMT  
		Size: 231.3 MB (231286473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f9e792f3c3964ddfe84714c7a41d47fd2cf52cf168ad4b156e8078b5044ecb6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11233935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e0d9c6d11daf0a0da985122ada0baaf9848d511cb5094a54013627792ccdbd`

```dockerfile
```

-	Layers:
	-	`sha256:784549636393bb3f0a4a42cff0c6baa9c49bcbe551c5d8863508c27da74400b3`  
		Last Modified: Thu, 22 Jan 2026 06:06:37 GMT  
		Size: 11.2 MB (11223762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:237cc5b0a6081177871a64d8502c68ded0322efe9e37de3ca58a16c68f0ff496`  
		Last Modified: Thu, 22 Jan 2026 06:06:34 GMT  
		Size: 10.2 KB (10173 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:248b8c9349a0d7320b9685fdfc10061afb0eef6bde55f81cf2fca4caf5bb9039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.5 MB (254494898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd60bd6939dec38ceada183fee87d58e38144e22438c6c21bd3765fb059ccbd1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:51 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:51 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:52 GMT
ADD file:be1799101a7a15f881e3aebea1e86fa6a156760dc7688b1affe179e948814a3b in / 
# Tue, 10 Feb 2026 16:50:52 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:10:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 17 Feb 2026 21:15:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Feb 2026 22:24:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8b6ba492713239cba0554ce53d24405e1285684fa64bcfb05df4af8037ba5836`  
		Last Modified: Tue, 10 Feb 2026 17:42:12 GMT  
		Size: 29.9 MB (29909784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791303199d68c9f312a5d0bfd906c93cc0e8d90e0628258a53b896296dbca649`  
		Last Modified: Tue, 17 Feb 2026 20:10:50 GMT  
		Size: 14.9 MB (14941388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2473e66ee8f78bb53bdcffed2627b2c45253885826fe33f99d8de8bdff1a3b`  
		Last Modified: Tue, 17 Feb 2026 21:15:43 GMT  
		Size: 46.7 MB (46745247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e379d2ee1007dc1051e30eda58e5f986b6d5493bb9146acef023d60f06519d8`  
		Last Modified: Tue, 17 Feb 2026 22:26:12 GMT  
		Size: 162.9 MB (162898479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:352075e6c65885229b973c24c7a7b86e05b65ab05c8fcf3de9c8d7b5c3f66e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11084601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0bcc261be28775f3b480d0bd26d57cf5c48a055e30eda820e7ea37e5abd4b9`

```dockerfile
```

-	Layers:
	-	`sha256:d21360a4b7530378557913eabd4c6b01d8f25883281ad41af975cd878d324101`  
		Last Modified: Tue, 17 Feb 2026 22:26:09 GMT  
		Size: 11.1 MB (11074460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3e357c93160a2919901f6aa65758b98f0f3ef82ef0d1674e1e41a8c6e98dd15`  
		Last Modified: Tue, 17 Feb 2026 22:26:09 GMT  
		Size: 10.1 KB (10141 bytes)  
		MIME: application/vnd.in-toto+json
