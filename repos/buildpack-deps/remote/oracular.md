## `buildpack-deps:oracular`

```console
$ docker pull buildpack-deps@sha256:b08deb0d33d7f80992b25716c4fac0662387ea504455b28b26f1033220fe7096
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
$ docker pull buildpack-deps@sha256:f2d468863910d62e7330375fd0395f4ad0779ec27a3ee0b00c49b0ea6b23afcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.2 MB (286231930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b5a46626d0cc438768876575effe13f925efd7379f00d0400c7b3741369191`
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
ADD file:08360137caccff53ccad4b814b2e19f27aa9fe2a71175550a7f6b13fe243924d in / 
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
	-	`sha256:31734b193a814b7d6f96f0d11a89c942ca61ac79d819105323c548bf31f98613`  
		Last Modified: Wed, 20 Nov 2024 04:18:12 GMT  
		Size: 30.6 MB (30601312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb3a0dc114c54fd18d42d481f5d85eb84000d5cd297bd2f753d1290eb36719c`  
		Last Modified: Tue, 03 Dec 2024 02:29:09 GMT  
		Size: 15.4 MB (15374140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64ddd91578315b54cf47f01baf6ea302d702c1bc46efefdcad51af4f6a7812b`  
		Last Modified: Tue, 03 Dec 2024 03:17:12 GMT  
		Size: 46.5 MB (46491318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4065e49aa231bcf1f2eedf5b60edcdd89df6863377a6110a492b6bb6c2daf66`  
		Last Modified: Tue, 03 Dec 2024 04:32:09 GMT  
		Size: 193.8 MB (193765160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c5312bff979618340f2d1556c3453421e1e55f873bf4efe7ddc7d25705766245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11369581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8527a70c975c34f4def1074b8ee7f1aabf34798e8772d52d20aedd7f33eeda4f`

```dockerfile
```

-	Layers:
	-	`sha256:c5b9641e0dec7e5403d1612f3ae20c9d246f99bf083b7747bf196a3cfd9f730b`  
		Last Modified: Tue, 03 Dec 2024 04:32:07 GMT  
		Size: 11.4 MB (11359378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07ec353f310cb5323bbb08e4760de895cdc7de806f12f1ba46515611d0372297`  
		Last Modified: Tue, 03 Dec 2024 04:32:06 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5e6c535541d799fcadbade99bcad57a32135142047242193e8c6c420b1aa93e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 MB (248408833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9875927388483d1bb47a79ad5e415dfed6a83a9f1b688632c124b47324a667c5`
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
ADD file:5cf848783aed3abcaefd540a7a70f443ef2bead6c50d01e0a72cd1aa6f542081 in / 
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
	-	`sha256:c553618cfeea14cb253bd7777b2e3299019b3065e1cb073744b43353379582a7`  
		Last Modified: Wed, 20 Nov 2024 04:18:39 GMT  
		Size: 27.5 MB (27546971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a00677e72221e7026f8e6b0ed5b47e7316c84195a5d85d7c2cf005d741e670`  
		Last Modified: Tue, 03 Dec 2024 07:40:05 GMT  
		Size: 14.1 MB (14060900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c52f0d85713a2f01f551bbf8afba0de5917d8a73a492b3fca6575c2696d83eb`  
		Last Modified: Tue, 03 Dec 2024 17:21:00 GMT  
		Size: 49.5 MB (49462929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a1ade74a0a0a3cb322d91a5b98afa058c0268e2ceebea121af375e348bed51`  
		Last Modified: Tue, 03 Dec 2024 20:20:38 GMT  
		Size: 157.3 MB (157338033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c9b4c62d6c5815bea5eb2dd0d5b3c2d844959ccd8f09eab126117f4c48a373a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11149176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5650dba2bfa8ac954879544aa3ba225de09a50747a66b3d7deb6b194e3a56d`

```dockerfile
```

-	Layers:
	-	`sha256:998154eeaa3b2c9daa4fa63ce0763edc00fe6c7a8960cf03ff43f5137b32c574`  
		Last Modified: Tue, 03 Dec 2024 20:20:35 GMT  
		Size: 11.1 MB (11138913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:065d062a0d03124977ef15b202544942d5dcd3547f37a77db3a62bb85fa307b8`  
		Last Modified: Tue, 03 Dec 2024 20:20:34 GMT  
		Size: 10.3 KB (10263 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:42e5d1c5d818a085ca5eb3e65007a5613672626901be13287e2eb8977e12cbb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.9 MB (279937838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d17ee958e00a1a6edf4a25addf51b7d7cbe299dba12ade1e5849aa5e006b1f1`
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
ADD file:11edc0b5b8a0810c86ff8de1ece47e84856118afa9f296152b12c0bdabf33154 in / 
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
	-	`sha256:6d229850a7784435237486a1406ffb5a4f0a4ac3b993928d18b30ad6853c6845`  
		Last Modified: Wed, 20 Nov 2024 04:18:26 GMT  
		Size: 30.3 MB (30284785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c08bcb2cbebb6d9db3a5ad2c52e975d21aa32088786303f6c521a0bb1f93f0`  
		Size: 15.1 MB (15147474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be5c9e4ce5805ad177f3aba8a70b5f1255051eb50b349f3819d9ee550186986`  
		Last Modified: Tue, 03 Dec 2024 11:54:23 GMT  
		Size: 46.4 MB (46423354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f144299644d986372fc7ab74c3e363056d5b1e93d2c8b4c856cb8d36c2a238d`  
		Last Modified: Tue, 03 Dec 2024 16:33:41 GMT  
		Size: 188.1 MB (188082225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a454f0ce4fefaaaf46eb66f48c64c50fb9f2005aad6a461386bf2369f9787302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11446009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73565036103c3e95c080e8ac4cd9db7e4f3901ca503409000edab5a9833aa071`

```dockerfile
```

-	Layers:
	-	`sha256:d9331ccd4adb34076f9c1de43104541397d3f4cad61b4f3912f2f5926f05f390`  
		Last Modified: Tue, 03 Dec 2024 16:33:37 GMT  
		Size: 11.4 MB (11435726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a806f212f7a6ab953efafd515e1def1e01f226f4883138d23f91068b4ae8cdcc`  
		Last Modified: Tue, 03 Dec 2024 16:33:37 GMT  
		Size: 10.3 KB (10283 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:07f2d3407c4086803bd20bacc23257dd31fd4031c8e86b5fb5c3620df1b3d0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301587069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7e09496b7805c1cef26d55c8f0982819a893d10d3d489717c57ffae9df60b9`
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
ADD file:c92b611280c7d224d58f2a2a7dfdc19380dda99a38e10495643ec0b43d2f3cac in / 
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
	-	`sha256:2039ab37391bfea5163cf2545fcb585344c981096040149e81aec9301f35f97b`  
		Last Modified: Wed, 20 Nov 2024 04:18:53 GMT  
		Size: 35.1 MB (35063190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335ed3d865eafcfc72459a536871a40009d4a399d947a0418657fd44f442c19d`  
		Last Modified: Tue, 03 Dec 2024 04:41:29 GMT  
		Size: 17.2 MB (17249971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19dd08a4345b11dbad4e6464f658a55387f7b1317148b558d997474d998e8fe5`  
		Last Modified: Tue, 03 Dec 2024 09:48:00 GMT  
		Size: 51.8 MB (51759651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1e7838794de9de838af4f642fa9a2c7787fc250fe2e6ea745400b6b118189b`  
		Last Modified: Tue, 03 Dec 2024 16:33:24 GMT  
		Size: 197.5 MB (197514257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a639d44639e78ee7c6cd1b7d424ba1c4d797a91d6c804122fb85a0d4e7fd4696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11361895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896d60018831607d6cf171e3307e4738e1ca84613d5375a7c6513eb779e8d90e`

```dockerfile
```

-	Layers:
	-	`sha256:1245cc6f4d67addb23dc7ac9e404400d3a787b5fa977037662ca4247d44923dc`  
		Last Modified: Tue, 03 Dec 2024 16:33:20 GMT  
		Size: 11.4 MB (11351660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76663542be6a991f1c7a41dca7b3cd4aab48b5c7bdb938e0deaade848e7b5561`  
		Last Modified: Tue, 03 Dec 2024 16:33:19 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8d5a7f2f0db10b545763695bb927af0842ee2cfba1caefe2966992777d27afb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.2 MB (378202631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c665ea6044af20b4b12d2b65300f30d5b7695ba2bc0e5cf82b306177f50003f`
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
ADD file:76a233bff3b463f93cb832f44963527276c1cd491cd0a75c9c5d2eac75da2380 in / 
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
	-	`sha256:9d51f6335bdd76dd9dcfd4d3eaa2272acccc262c17300716acd3ffb0ec5f5846`  
		Last Modified: Wed, 20 Nov 2024 04:19:07 GMT  
		Size: 31.8 MB (31787958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48e90448070e192152f471d2c8fd1cfc67ec60c6cb742a212ead9de030d94d6`  
		Last Modified: Tue, 03 Dec 2024 06:47:45 GMT  
		Size: 15.9 MB (15890462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4180e9749ee9c2cd33764d68a8a49f4513db415bcf81e499f6bd3b0b7312f056`  
		Last Modified: Tue, 03 Dec 2024 09:56:53 GMT  
		Size: 54.6 MB (54615995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d229559deb983f34d263c1186e731a20b3d9db40451b4063f3de51f6fc326219`  
		Last Modified: Tue, 03 Dec 2024 11:31:19 GMT  
		Size: 275.9 MB (275908216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4e00820dd6ff6beb8effa14dc6357c1c4e04d951a758caacf793ec7dd2b33fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11417908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:664c2c34bd590b1f1e97e2d7910c02c94c1aeca1d6b7bba8fc435b595c252143`

```dockerfile
```

-	Layers:
	-	`sha256:d75666c5ed1b37cd483e2f968e564cfb994c3b7cb8acfabb93f8b56c5b7bb8d5`  
		Last Modified: Tue, 03 Dec 2024 11:30:44 GMT  
		Size: 11.4 MB (11407673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00bd0cdc0851b621344bcdeb7d234bb1dd772ad6c7004714a0e5ee05418e0d98`  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6f95adf3a52b8a9b79ba8f14c9b9ceddd5c0d7e858dddfc5423b476ef0221492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265507437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fcdc2270c2fb7756c24dfddace9096deec97390161569734095a649c3603a4e`
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
ADD file:d8a0fd6e6a1b5571de35cb60b4e05523a0290523534ad63464fdf47dfbe0b041 in / 
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
	-	`sha256:8ccad27fc3ed57037242d8c7dde5d5ce195749a63f65f7d9a663f7b822c4429a`  
		Last Modified: Wed, 20 Nov 2024 04:19:18 GMT  
		Size: 30.8 MB (30775034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d6a6da1657d09f717e7f94493d3e0563278583e47322d423316da636b93135`  
		Last Modified: Tue, 03 Dec 2024 04:11:01 GMT  
		Size: 16.9 MB (16937481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae51c456fa63fca49c43c89a34927e42baace55350a312e11092478ffa7894cf`  
		Last Modified: Tue, 03 Dec 2024 07:58:31 GMT  
		Size: 47.8 MB (47774022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9602e6e79d8a9afdd7c8691bf80181cc5be4942308ba620ef74fe70421e13ce3`  
		Last Modified: Tue, 03 Dec 2024 10:59:07 GMT  
		Size: 170.0 MB (170020900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c6c0e1f425fdb1d84c16cbbe7a6878cd2598f37f3526144365efe934b8b8a0be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11168896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb66150459757f9898298255cd0cb66c204688a4cf85ae139b5689db0254223`

```dockerfile
```

-	Layers:
	-	`sha256:7d36c1b3ced50159e6fdb1185db60346dc278bb5afe7507c3174f447100ae1e0`  
		Size: 11.2 MB (11158693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0de5e93240ee180a47ee52972d2c014e4e8cd4da6ee12024db5bd71f405d3966`  
		Last Modified: Tue, 03 Dec 2024 10:59:03 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json
