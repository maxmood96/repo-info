## `buildpack-deps:oracular`

```console
$ docker pull buildpack-deps@sha256:7fa266be3c61c156d7dd51db5478495dd0621bf520277eea36b263ffe8494c6f
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

### `buildpack-deps:oracular` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:36f6f13366ee1e22864439f1bcb06150c8d4920339720d4c960701efb1cda171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.0 MB (286955795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6368b3dc3d42516b229c8ed9f84959b5a68afa17d62b6754948de24b3433d74`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:764959978f9fe798d77bf581ad10e612d454a82cfa4151c252f99dfba77930a3 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:440a90d6b31c594198d5c8b7f0cdefd617cd095c8cccb6efe3152af757db0f83`  
		Last Modified: Thu, 08 May 2025 17:05:29 GMT  
		Size: 30.6 MB (30647018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5caf06dc4ca048294638d860fdbe31b52df91fba85cc982ec96d4cfae787323f`  
		Last Modified: Thu, 08 May 2025 17:35:20 GMT  
		Size: 15.6 MB (15563441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f2791f340319af4abd181ca8dbaafcbeac7b2dc1efc999fc9a565cc4e5ebd8`  
		Last Modified: Thu, 08 May 2025 17:35:23 GMT  
		Size: 46.6 MB (46637373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca67ced6594610ad7af78544c80bf8f87c1b5fea929ab49c9e378fc08711b0f`  
		Last Modified: Wed, 09 Apr 2025 03:11:51 GMT  
		Size: 194.1 MB (194107963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6d0872c3496986d404281bb4b2264eaca4da034659b654f57789f4e4270663f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11352571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:297bff578d18511ce1bfa1b2e55f6190b367eed1f9c04013588f7c960e2d8d6b`

```dockerfile
```

-	Layers:
	-	`sha256:7cfd6b44268f50b8b6894bfbb611975508aa2d7904179cb13653653c2c7ff865`  
		Last Modified: Wed, 09 Apr 2025 03:11:48 GMT  
		Size: 11.3 MB (11342368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef75cf4c79698a89089d78eddaaf5111b0b3fe258b4ca04d79d016560ce1f3d`  
		Last Modified: Wed, 09 Apr 2025 03:11:48 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:85f3a4fa317d3b5ec0abe5ea98139370488e6e06851f30b2d302024fb06a24f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.0 MB (248982550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2f0db3dbff8b06b06de283b4477cc9c71405853e372d47b5e804957e564942`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:f13ab66af81cfdff78a6c942b3d1f102b5a17f8c923dfff8d28e2403245adf4c in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:090aa4b9a734ba6bec570aa125b6ad0489dc536d5cdd28a669b8bdd0a0cf0b7a`  
		Last Modified: Fri, 21 Mar 2025 09:40:57 GMT  
		Size: 27.6 MB (27554319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95637e503528dcbfe1fdb44aef45d4820550ec4b33d60a6ac713d5b873a3d752`  
		Last Modified: Wed, 09 Apr 2025 11:35:56 GMT  
		Size: 14.3 MB (14303290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dd76adb0395e9e97fae2b6b75e8fbf122e60f7c76228b01116cf3edbfe2632`  
		Last Modified: Wed, 09 Apr 2025 12:21:05 GMT  
		Size: 49.5 MB (49455502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f75d00cc9b1183419b7e7890aa09e139e010d59f229ccc8d12440abbfebc0e`  
		Last Modified: Wed, 09 Apr 2025 13:27:27 GMT  
		Size: 157.7 MB (157669439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:28834f5b6023318b18a155b4369b933b7886593ffc32e8fe78b80f0730f18093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11132489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429bf8d1dd510696e6c3d0a88cd7feb4f98680a082f356eb4bffd09c0e372c6e`

```dockerfile
```

-	Layers:
	-	`sha256:9a7dc3e01aa329b28b60a1c4e4284cab60a7d3d13e73e0450c612bbae561b58c`  
		Last Modified: Wed, 09 Apr 2025 13:27:23 GMT  
		Size: 11.1 MB (11122227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eae949c2849d3a7d73614e47e4b40e6c2b8d65faf95d03ddb7c16c10d400da6`  
		Last Modified: Wed, 09 Apr 2025 13:27:22 GMT  
		Size: 10.3 KB (10262 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d66e21c163272bbc1a84f3083baba15063cb494c03bacf58724ce9ddd851c506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280563201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1570bd4689ea6184c7bdde8552c456d77ae777422e73e988dc4a79a3a65cb9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:458f2262832f9254682efb663e94ed73cf9f068bc4799f5a25ffb533a869ed44 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3d825962f62a727b0760fe9a4f96a67a09a0d2a8077e99007e7681149f2ab3fd`  
		Last Modified: Thu, 08 May 2025 17:10:33 GMT  
		Size: 30.3 MB (30320224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eacb0abd365e7ac96a553eb11a8b04ca8a62c023926633845107e9e215227a7`  
		Last Modified: Wed, 09 Apr 2025 06:11:20 GMT  
		Size: 15.3 MB (15330068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28478c451efafdd58825833b7a96ab18f7d12cc4d2cf5871b329ac70bc3074e5`  
		Last Modified: Wed, 09 Apr 2025 14:00:14 GMT  
		Size: 46.5 MB (46534730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e4ac0edbe0b1bf373a838ed269c9224b4e44d69dfded6f05134683d137bc95`  
		Last Modified: Wed, 09 Apr 2025 18:26:22 GMT  
		Size: 188.4 MB (188378179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e085c6ef282908fd44c5e8e2c062c49a41016186a1226c6050272d2b785114a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11428912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541b6f66c08970aa2ca22c9f2f3f28641aa7754e957b4e46fab99ca6b381804f`

```dockerfile
```

-	Layers:
	-	`sha256:cddb8653758f5b78d7a915707cffb429f08e15976bb6097944ae84c1e104b23b`  
		Last Modified: Wed, 09 Apr 2025 18:26:18 GMT  
		Size: 11.4 MB (11418629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a41cfe2e4ab977b85c3e2b4937b588f702c731979807a89acde4752097b631ae`  
		Last Modified: Wed, 09 Apr 2025 18:26:17 GMT  
		Size: 10.3 KB (10283 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f90d501fe401ad938fe71a1bc80687a8e1b19bb12bbb85200c2a48aeedc2041c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302253805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66528d11ea66362687924c82cf524ef4102cffe6c860149033bd7b687c41e8eb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:1b338c439eae4a20ee7d1b84db98f2f0664cd0c53c3843407f28a1b33a48c0ae in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8617c693189c511af931ec6b7aa3573654d8d3d3274b061f881929dc7e9e831e`  
		Last Modified: Fri, 21 Mar 2025 09:41:03 GMT  
		Size: 35.1 MB (35116459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eca3df5efb1d2a7a155d29563d34a4cc59b77f1356adfd169ce229390b6bd91`  
		Last Modified: Wed, 09 Apr 2025 04:30:59 GMT  
		Size: 17.5 MB (17490417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fdbf25494c1d33658a8d848c137015fdf810bc230f9fa986642899a607aab15`  
		Last Modified: Wed, 09 Apr 2025 07:39:13 GMT  
		Size: 51.8 MB (51818048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c732b52206caeeae18937373be417f9071c7502917174bb680d74b867d9307`  
		Last Modified: Wed, 09 Apr 2025 13:41:21 GMT  
		Size: 197.8 MB (197828881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4121f8709350df1f0b3018e36879888c4814127a77b462a5ca1d7e4a80c00478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11344939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6cb192cb4d53082754c17b55d321439c82600cb3bcb3bcb30ddd0b392c9542`

```dockerfile
```

-	Layers:
	-	`sha256:5c234cedcbb845b6053bd306e97a4ac27427092e43bcd3b89dbbc4842402e8d0`  
		Last Modified: Wed, 09 Apr 2025 13:41:16 GMT  
		Size: 11.3 MB (11334706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62473be04f1c9f1f92c2169536875d423e597d308d44476846c8ff6ece4a25d5`  
		Last Modified: Wed, 09 Apr 2025 13:41:15 GMT  
		Size: 10.2 KB (10233 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:7a07c45844ca69f5a6b3e46f2c4ff9cec65c99a359c3db0d720a94e349541b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.0 MB (378982155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4dfb95fc0deffdff66b2b4625e8b16257435515597c48ea7d29572794c3bf67`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:e17f3a566611e6e6aaf40f0cf67dace1148c4e227e136a582732abd5470cc4bb in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:17143e5c2a0de46dd660097f35b7d1c381a1cfd489bea2cdd1a596a3e3b08cda`  
		Last Modified: Fri, 21 Mar 2025 09:41:10 GMT  
		Size: 31.8 MB (31808054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f1c68219c9767213bddad50e7129bda08a3407ab786d2bb7b5a54df5e760ea`  
		Last Modified: Wed, 09 Apr 2025 05:21:45 GMT  
		Size: 16.2 MB (16187400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff1351043fedb7e8229fe0f7f54e7d9a6728f389ecd49c4378c8f4a18d98c04`  
		Last Modified: Wed, 09 Apr 2025 08:46:47 GMT  
		Size: 54.6 MB (54603679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c63de24acdbd03cbc02a42295bbdb4b8d76a4a21a7feb144a1c9467108b1062`  
		Last Modified: Wed, 09 Apr 2025 11:24:08 GMT  
		Size: 276.4 MB (276383022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:76b3f8610f614164c04bd03042ae03b0f5f4ebdc653384bf723afe8306ff4961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11400817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcaa0c60af0f9f202e1ce8713ea7360ab69262f5ed3af5d97d0131a5859ee8d0`

```dockerfile
```

-	Layers:
	-	`sha256:55dc3f41832622fe3e0fa5d8245762f0e708442c29c2352c29e729573ef22ddc`  
		Last Modified: Wed, 09 Apr 2025 11:23:32 GMT  
		Size: 11.4 MB (11390582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12e75181ba371400030cc90cc4288850be4885bc37fd9f9e078bd76b355b072c`  
		Last Modified: Wed, 09 Apr 2025 11:23:30 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b197d483308d9597b0e4e0218998041c48dbcf24c0a9ec780c82a64ab2c3210e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266300887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca464153f74d05eca7f93f5fc14a0bcb26623e105746e2040f27a91a706fd96`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:6836ca55f6c19fc0e06d3dc978a72aa71953f87a5bd8cbddc3ed081700c03924 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d97194ac694365d185a619f35f2e6568110c20c3adf2a9504567854113756237`  
		Last Modified: Fri, 21 Mar 2025 09:41:16 GMT  
		Size: 30.8 MB (30807587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6dd0f373b4fd69149d2e82b840da266bbef643b2959efd2fd5c3339bf6327c8`  
		Last Modified: Wed, 09 Apr 2025 04:13:25 GMT  
		Size: 17.1 MB (17133933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9317ef61611edda8e8ee6e896ffd5dae97da282073fac53c5c33b08abb4dfc07`  
		Last Modified: Wed, 09 Apr 2025 07:10:33 GMT  
		Size: 48.1 MB (48073577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d28aef641e955eb66bc334c849a6c0949d01095d164e83d0bb1d35fcc19bed`  
		Last Modified: Wed, 09 Apr 2025 10:42:01 GMT  
		Size: 170.3 MB (170285790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ba42182f44600a588abae19583c26a8d547f96908c55cfaeae640c7f1d8e3a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11152130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc182b2fd8f72009b7077fea2668d3991545b54f7dab8aebb9cfbd228c7d1bee`

```dockerfile
```

-	Layers:
	-	`sha256:3d2d278bd6b2fcf9b72992a92a1faabf5f46767eab03856d9f94fd9aebf50624`  
		Last Modified: Wed, 09 Apr 2025 10:41:59 GMT  
		Size: 11.1 MB (11141927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0c08cf4ec1ff64ae9d65460ee342e6c995a7c4ef4e1289b003f7c05a080bb9b`  
		Last Modified: Wed, 09 Apr 2025 10:41:58 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json
