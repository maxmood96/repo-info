## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:79dd72e52b84ec52c11bd24af2cd9caead0e0436b8224f0527257b3ac2df6566
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
$ docker pull buildpack-deps@sha256:b453c8cd367cd4cce43dca346a2bf74039e51900afd54078a805ab90d0250dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.8 MB (274812458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f6e4a388f8fe7d2eca12baee3ad68b037d4305fa6bb4356b568a736ce5f63da`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4da1c38cd39a1dd115e9a6c26965a439c65b03d482b5fa7a24467582eadd75`  
		Last Modified: Thu, 09 Oct 2025 21:31:21 GMT  
		Size: 13.6 MB (13625081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf06f1df562fcf4f04a84ed229e7bef8b2385ff7761d3b16236ff11be8f0eb1`  
		Last Modified: Thu, 09 Oct 2025 22:13:38 GMT  
		Size: 45.3 MB (45334192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd1db563ce3e44ed7c128b3ebf86c3cdde2dde527d852546746056a425155db`  
		Last Modified: Fri, 10 Oct 2025 04:30:10 GMT  
		Size: 186.1 MB (186130038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:159c45debe69743323e2cb732ae17eb69ac6f8390dc63c68c2035cb469721515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11742963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f43b2382b52ab2eab685b87191b296727038a67efcf40bdc210dfa9daa29e0`

```dockerfile
```

-	Layers:
	-	`sha256:3d538bf1288dc9fd8cf58e20ad2872b4797a1a9ebcdb5735799d2409f410b912`  
		Last Modified: Fri, 10 Oct 2025 04:19:33 GMT  
		Size: 11.7 MB (11732779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2dd0f137561613c7147c5bf4811cffce2eee4e7ee835f67380e223a77e6b1d1`  
		Last Modified: Fri, 10 Oct 2025 04:19:34 GMT  
		Size: 10.2 KB (10184 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a5b91976f0faa07753065590f9f35f554127e4329e8f00dfca696c2872b53881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236869849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2bbc601d9aaf8a3cfd7300c0fb4a3eb94dc4367ef62b317a5fef70ecea32253`
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
ADD file:1ccdd7fca45ec88ba0ddda07e5e5acb6b40ddcb3023e0cbc04ffffdf4e30fb0a in / 
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
	-	`sha256:4afa85c5883c0db62b02025c149edaaa237af5ba25ea48039e875a802d465ac7`  
		Last Modified: Wed, 01 Oct 2025 18:03:16 GMT  
		Size: 26.9 MB (26851732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022ffe8d142b8dd5e375cb3bbf3b7f0d742fcf24654020fe40ada08aa8d2bfe4`  
		Last Modified: Thu, 09 Oct 2025 21:08:02 GMT  
		Size: 12.8 MB (12784406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6168ce6859325b4e6307d2e5462c00745a7afa8be1928d087849949ffeff2cb`  
		Last Modified: Thu, 09 Oct 2025 21:17:41 GMT  
		Size: 48.9 MB (48865669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02a1b94f51e799e4f6beea5087f854aea8f13b33dbfcc8198a39f3121057e75`  
		Last Modified: Mon, 13 Oct 2025 08:38:53 GMT  
		Size: 148.4 MB (148368042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2c5301d2b38a5bfb1d321ab2917e3b12474afa4f2ddb89ec8e1882472961d14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11068728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4556ade9e1d91595927c152dbd12f35f8db9e64264b128fdef07337cfd206296`

```dockerfile
```

-	Layers:
	-	`sha256:3120b08d63a2df29f7a17c55fb2972ee0dc6177f412fbee8238dff64f69f63e2`  
		Last Modified: Fri, 10 Oct 2025 01:19:30 GMT  
		Size: 11.1 MB (11058480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c579be95667b55b3182de9cd211140ad81cfe4c1e9005fcbbbf5a22948c1c572`  
		Last Modified: Fri, 10 Oct 2025 01:19:31 GMT  
		Size: 10.2 KB (10248 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c1b303df7c84e691dcc1555149da6a5cedb5e5bbbb25f306ccb05606b99b9bc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.3 MB (264302347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098e418b44107a41bd716d1b5f124f890d30d8b52c70bac3c6ad9b567dc3fab6`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cd70ea204ed4db7ba47a601ca9a11c75a0084d32a61213dd88df48189d57b7`  
		Last Modified: Thu, 09 Oct 2025 21:09:03 GMT  
		Size: 13.5 MB (13460697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d49dfd9b0c2e4777e0eb65d385c4fbe4ac4f35cb1096d5ae1801095edc9d20`  
		Last Modified: Thu, 09 Oct 2025 21:32:19 GMT  
		Size: 45.3 MB (45274515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab30ffe71753ab558a70420a0bd96c1effd3889c1f79335b3b3fea12ee8e538`  
		Last Modified: Fri, 10 Oct 2025 09:01:40 GMT  
		Size: 176.7 MB (176705423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2cfd0412c8a88593d2a9d4cd31483037012fe2b116631750f0403194db47acc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11292512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1a9e5cb2d05f801c55ce43706a198cd009122ea136c35bcee3ccace1b9257bc`

```dockerfile
```

-	Layers:
	-	`sha256:b1658fd0b0762daff4c07c270239af36c9723994fa5d8d8616ff9ec77ac94552`  
		Last Modified: Fri, 10 Oct 2025 04:19:47 GMT  
		Size: 11.3 MB (11282248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b53abe1f0dc4d43269f64062eacadf6be1fbdbfa885614eddf150f474298695`  
		Last Modified: Fri, 10 Oct 2025 04:19:48 GMT  
		Size: 10.3 KB (10264 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:898c5c16b7da7ee9776b644112a5009a33e913636ce4bb35898b08820c5ebfbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290373466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8585150d37542edee5a586357bf1efbae974943fa318cb2c5d04c0b73040fd4`
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
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
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
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff2c43d036e8b55e943cd93e0bc732e1fdb6b9a5f8fec89a5e868148e6bf1fb`  
		Last Modified: Thu, 09 Oct 2025 21:09:03 GMT  
		Size: 16.0 MB (15953193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0519421d01f87184f984ce44c220694d718f4d07feb1a3dc151316502799631`  
		Last Modified: Thu, 09 Oct 2025 23:05:04 GMT  
		Size: 50.4 MB (50405554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c89d544e84a380e3f90b734727514736197e836c245fd9c1dab736a4165f76`  
		Last Modified: Wed, 05 Nov 2025 18:59:45 GMT  
		Size: 189.7 MB (189711194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6d878aca2d51bb8319edfb7e0ebba537b1e0dfcac5a66355ccf92b3988b6c82e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11239901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd9714538cb7949ba2c4857665384f7b6eb29361dc603614c61840bad95cff9`

```dockerfile
```

-	Layers:
	-	`sha256:3d9352b88ba536b4e70314182977808ab38a5d9f2ae08c19e564324829acbfd2`  
		Last Modified: Fri, 10 Oct 2025 10:19:40 GMT  
		Size: 11.2 MB (11229685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c099107f78e95a92d6748c2b4e164600380c0fddb6b6284e520b6ace606ddff`  
		Last Modified: Fri, 10 Oct 2025 10:19:41 GMT  
		Size: 10.2 KB (10216 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:40fef8e9081f89208a380798a81a4461e835c6852ae7a4f118d470f713570889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330409770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8d8ce41f697890135098ad9a24a37b5bc041d310a2674528f8d51a56e998e6d`
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
ADD file:857dc87fbafae31881cff8c69aed267a033f5df226dd351ee89de918ad5678ce in / 
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
	-	`sha256:ff47a256ba51b80e9880bc96be4ac2f094c47e0fcd7eec71bab85787cfa54b8b`  
		Last Modified: Mon, 13 Oct 2025 04:10:18 GMT  
		Size: 31.0 MB (30951381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfbce957852ea37a1a2c784ab77650af27478b8247917467797949fa28f5220`  
		Last Modified: Wed, 15 Oct 2025 03:32:31 GMT  
		Size: 14.3 MB (14331055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81914e0814a78a62c0685917a2edcd042fc3ef4760ffdfb24ef42ebc31626ff`  
		Last Modified: Wed, 15 Oct 2025 22:40:47 GMT  
		Size: 53.9 MB (53876629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea92763762ff5d4992dcb15589bfa611066078e2043c5820c1abf6ce57dd180`  
		Last Modified: Thu, 16 Oct 2025 10:51:14 GMT  
		Size: 231.3 MB (231250705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:814fa492ea4b8930caeaa0e729b4718a1b9798331bff20fc9597d8a1332a9045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11233142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8206bdd3509cc0257f1ba8b7e1a5e48a8987a37e226bb379d711cd5c81fb70b`

```dockerfile
```

-	Layers:
	-	`sha256:0c2c3fd2e0f874d9dd6e50207d7dc632e93d69eb15265baba46fb7a248fabc42`  
		Last Modified: Thu, 16 Oct 2025 13:19:49 GMT  
		Size: 11.2 MB (11222926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9365ba7e886fa9005bcf87d18f9825a5121f7d48ca49a17651fbd8acc0d7a9a`  
		Last Modified: Thu, 16 Oct 2025 13:19:50 GMT  
		Size: 10.2 KB (10216 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:fc03bde07af3683e4651694e57cdebe14518c7155990a4686f96fafc0f47a583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.2 MB (253184640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f3a90a6d5906e99749d86eb9f2ced1c4d4b41163cf854ea7a89feb73df69a4`
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
ADD file:1c921a1d937949898d3d4ba499ce8d41425fe6dd2c8fdbcddd0070f2699f05b2 in / 
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
	-	`sha256:67735b72a65d308a2c2c9505d0d6e8419b7f2654a16cbd56963d88e01202d507`  
		Last Modified: Wed, 01 Oct 2025 15:43:10 GMT  
		Size: 29.9 MB (29906151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcae3965c70c7cb3a760d4160161a0695e258329f001c8a190e4c43e7741035`  
		Last Modified: Thu, 09 Oct 2025 21:09:01 GMT  
		Size: 14.9 MB (14938071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dae70b370244b74d48002094af6772c75d26b87a7e01ac35ca230e7d276ca0`  
		Last Modified: Thu, 09 Oct 2025 22:20:06 GMT  
		Size: 46.8 MB (46813759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a080befa18d95ed0fab83d3490831490fb9fba885fbb61f62b5c84299e542f9d`  
		Last Modified: Fri, 10 Oct 2025 04:20:01 GMT  
		Size: 161.5 MB (161526659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2a71fafb4742f6d21b68eb707ee718471736f9ae5e6f2c17c3ffde1db2d6b2bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11083716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab2e5314134a00e57cdb0a44259b71f651ae6fcd3c0c85aa1d6b567d28709f3`

```dockerfile
```

-	Layers:
	-	`sha256:340e26fe61bd5fd26febb8b09dc5548984ca351eb8e03420b18a6c77fd3e3e83`  
		Last Modified: Fri, 10 Oct 2025 04:20:05 GMT  
		Size: 11.1 MB (11073532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a98fb95f25025756c9aea13f52febef7c7d3fd019b88f3fb77e33d7f4cb23829`  
		Last Modified: Fri, 10 Oct 2025 04:20:06 GMT  
		Size: 10.2 KB (10184 bytes)  
		MIME: application/vnd.in-toto+json
