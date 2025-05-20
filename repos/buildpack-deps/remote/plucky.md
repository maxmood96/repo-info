## `buildpack-deps:plucky`

```console
$ docker pull buildpack-deps@sha256:ddfebe2a9be137c92eeba035ace683de46217c66eb06df7b29c13f405115f9f0
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
$ docker pull buildpack-deps@sha256:31d6d8320e43f856f4bbfebcf625586f36a2ccf8184a7728540f17276ac598d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.1 MB (308055429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad372e8e19546cbc3a42051273e0e182e7ae8eaa6f8a1f7155f22eee700f01f`
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
ADD file:980bb2d70ee1d803d3c9180ebef258c9795083efbff9e9b7eaab4ae2ea044632 in / 
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
	-	`sha256:1b3c8f62d074f218ad1cd11a4c801f7d6b73b93db485e1c170d6182a19604852`  
		Last Modified: Thu, 08 May 2025 17:06:23 GMT  
		Size: 29.7 MB (29710720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f757c9c78154a5f72abeb34fccd9ae44a8f5af313fc815debcf1f79b961ceb3`  
		Last Modified: Fri, 09 May 2025 04:11:46 GMT  
		Size: 20.1 MB (20131316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad5724474da3f6989ea92f5122b47e0db09df68332efd5cbdfb4cedb6b6bc41`  
		Last Modified: Fri, 09 May 2025 04:11:49 GMT  
		Size: 49.4 MB (49362604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c27c7152907b58ba77c7144a0287812d77c36e47c9c4da8b17b425c73219de`  
		Last Modified: Fri, 09 May 2025 04:12:04 GMT  
		Size: 208.9 MB (208850789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:359bbe0c76729031f2afc6d61554d5a29a6ec80b5d2ca199f0525b2936e83da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11587187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af613a127a660e756ff9ebb1556811bfcb9694215f9f2c4f67fc5b3dd76b7a2`

```dockerfile
```

-	Layers:
	-	`sha256:540a5255c02b853644fcbb2854c459cc268259c7ba38302d26664bbd4d258b28`  
		Last Modified: Thu, 17 Apr 2025 21:08:25 GMT  
		Size: 11.6 MB (11576998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1713d1dae8322ca19d3a0752184bb8ecc7c71bf3d3c1bb71dc171d6ff6eb3cf0`  
		Last Modified: Thu, 17 Apr 2025 21:08:25 GMT  
		Size: 10.2 KB (10189 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b54f1379cecfa32a96881e9593f8ceef4c45127f9e8467434270fb6d5a808fed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.8 MB (254829997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e49ed9c4ddf0453922d6a31be93f1cdbfb23d8e34a9f2b4e2cc9f4ff776e104`
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
ADD file:fb0f94fccc5217831c9326a88f9d43753e6977b91ade49b0b852f1e4ef22ea73 in / 
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
	-	`sha256:86d463765a1ef9e0563fb0c3823561d371da6b7f687151958aeb7efcbc80addb`  
		Last Modified: Thu, 08 May 2025 18:12:29 GMT  
		Size: 26.7 MB (26733303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab87d6883b32267ffea1009a181926e75ec6cf0ff7b79cffc076fa4735dc92d`  
		Last Modified: Thu, 17 Apr 2025 19:08:00 GMT  
		Size: 17.8 MB (17843153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f906d8462ce8ce7f0f00d9a66c6be0c4b7dfce05b4b038770d4f78ea76a60b`  
		Last Modified: Thu, 17 Apr 2025 20:08:05 GMT  
		Size: 50.3 MB (50292313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c886492d4d0e27cbe27749e69ede92ab14e9bd1aa1e973f704e0e91fc027870`  
		Last Modified: Thu, 17 Apr 2025 21:11:52 GMT  
		Size: 160.0 MB (159961228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:61cd980c1a9b65bbd046f624f08009488118e62b634819c46b8577a347212715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11342047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e03cd07761a7a0b90250cd834d74ad526e42d4a77a56ddc24ceef14690de317`

```dockerfile
```

-	Layers:
	-	`sha256:3b8af903c8748ea687d11b64f5a0d06f6227ec20734860e38969fcb6e0e99f1e`  
		Last Modified: Thu, 17 Apr 2025 21:11:48 GMT  
		Size: 11.3 MB (11331798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d9b52de1993410b3bedf703290d1292a79a866a274e25099889738dfd44a24a`  
		Last Modified: Thu, 17 Apr 2025 21:11:48 GMT  
		Size: 10.2 KB (10249 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1a1fba0f22e068e25c550b618f93c95086c4e5b1f638e9bcd1e417fca6c98afa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.6 MB (288586184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53d03cb0b20be569d329f133b1fd15374df50a90e091ede31ba8d0be5d7d36dc`
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
ADD file:569b1b24c0a1612eb4d548884c87952b053cad17ead534d91b34f74bf31bd2e3 in / 
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
	-	`sha256:36dff27e34eb6a337ae036fbb86e7b073ae0e8f1dc5d7e705423c419a175f092`  
		Last Modified: Thu, 08 May 2025 17:09:24 GMT  
		Size: 28.3 MB (28261176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86243b610edc9d6c1e787d92fd82404a07dc7df1137da6257f05b9a0e0e6b99`  
		Last Modified: Tue, 20 May 2025 02:03:03 GMT  
		Size: 19.1 MB (19130209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ec985f2342cf4d978e41a17055220791aa792de162145255f27519e5e65e49`  
		Last Modified: Tue, 20 May 2025 02:03:07 GMT  
		Size: 47.1 MB (47128620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc8dd77978254a6e7fcada91fed2aeb2f6490f95e60f646ea1eed8c81889c5b`  
		Last Modified: Thu, 17 Apr 2025 21:11:42 GMT  
		Size: 194.1 MB (194066179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:352a9bbe53458707cb2aa2db3e11adc5e00f5f9d3ffb68f0d91257db412046ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11651096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7d947a49611c1d6fa8c056dbb447516881729193a90ee091ee7e2e43bf2ece9`

```dockerfile
```

-	Layers:
	-	`sha256:31ab2f8b87eebc84d810fa695d7297916e5748ad8ffe7ef1e6ec92c935713f41`  
		Last Modified: Thu, 17 Apr 2025 21:11:38 GMT  
		Size: 11.6 MB (11640827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0a2ad9781158f908c4222b4e0c4095de52857719d0e4f2c5051d7a5354b212f`  
		Last Modified: Thu, 17 Apr 2025 21:11:38 GMT  
		Size: 10.3 KB (10269 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8ac85f9ed0c486098bc083ad8dfe3eb4f592892a81cd6cb31dc67b3d8b7278df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.4 MB (311356158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f33055808e45cc58f0334552559bf73ce6d61861cbe7addc780da28c94df01`
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
ADD file:7beeb672215e04d6c96e9a0d60bbea564ba541da31facc36a320d045fdcef6d2 in / 
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
	-	`sha256:2731a3c5c15f5006b875bcf4a527fb9cc63904021559cd358c160c91018fe816`  
		Last Modified: Thu, 08 May 2025 18:11:42 GMT  
		Size: 32.9 MB (32912546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2beb87237962b8380a9e374cf35ac02c42ab0b99ccf115150e657e391e2bb0`  
		Last Modified: Thu, 17 Apr 2025 19:08:48 GMT  
		Size: 21.6 MB (21558484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43095d756cc2c24de6c5a2f0801e91256998daf7396c041eca5c561ce2ae022d`  
		Last Modified: Thu, 17 Apr 2025 20:08:50 GMT  
		Size: 52.6 MB (52561529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a676d850fd126bbab81a0ab8c6d5091397c61e2e49b9fa906fa5aeb46f5fcac3`  
		Last Modified: Thu, 17 Apr 2025 21:13:50 GMT  
		Size: 204.3 MB (204323599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e8135cf152bc107ef2ea11c28cbcfb213e4bb22c6874f2afed0658852dc71295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11568718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3918670f5979cac0d100ff8381d6d21606d86c81350168bc5b9a25ad2c88afce`

```dockerfile
```

-	Layers:
	-	`sha256:cab4d07b4992fc7ed4bceb56e7348fc7ed52b341368873c866f1e1fa096f32e0`  
		Last Modified: Thu, 17 Apr 2025 21:13:45 GMT  
		Size: 11.6 MB (11558497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6592afbea9389180ff2614d7ef98c26963eb3e16cc11f3bbdd29c11f3474fd6`  
		Last Modified: Thu, 17 Apr 2025 21:13:44 GMT  
		Size: 10.2 KB (10221 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:dac76d82d53eb75fcba2eadcda6bdeccbd9a3304f46d5cf82cd30202e16fa9e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.9 MB (397929585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d394c091e45350d6297f7f0a8b2e69faec568d5408bf2f6020f1dd6afaf55c`
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
ADD file:3ed52cbbe2433c5dc12dbb7e732f2e889444782966bb4bca420af94f96515440 in / 
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
	-	`sha256:df4fa7894ea6fec34e9613aa41ce12d39e86174106bbc5e006a59c24f83a40a8`  
		Last Modified: Fri, 09 May 2025 05:11:01 GMT  
		Size: 29.7 MB (29711418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a28ce9969a80966c4d110ac26c6b9b392674b7c0ac90ca28268a9e5904c34c`  
		Last Modified: Fri, 18 Apr 2025 00:10:23 GMT  
		Size: 19.9 MB (19866811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d7ee2e5f97e1e0ab0102b96377a6a0d40ab2e76725ff1a7984fcbaa50fcaea`  
		Last Modified: Fri, 18 Apr 2025 01:12:49 GMT  
		Size: 55.2 MB (55228758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0390c7cec7cfc6619eeab671778e222fccc6d0822caf5bbe7f4df18c83bed0`  
		Last Modified: Fri, 18 Apr 2025 02:27:33 GMT  
		Size: 293.1 MB (293122598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:35ed243cc537f326e68185e1bef10158d2fdd3427910ad97884a8e49ff932f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11625384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59144bae36ed2ecb389e513170ad6189139f45bcdeb68e5ed21556d9842406ef`

```dockerfile
```

-	Layers:
	-	`sha256:9182b6b320d48baf521b88cd5cb59fc99e95e865d968db94f174575215849560`  
		Last Modified: Fri, 18 Apr 2025 02:26:55 GMT  
		Size: 11.6 MB (11615163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:077fc9da5707e0c506cc313179ff7f57f3bce2134ba93eb4765849cc543d0ca6`  
		Last Modified: Fri, 18 Apr 2025 02:26:53 GMT  
		Size: 10.2 KB (10221 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ac242baa3a4583c6b8e44550303b5e6892ff9466a95f368a36d5b56eaef6866d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274599799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c691d96fd30c5b21c6b35cecf59e71339b8c7173ad027397910d1d3c44f093a7`
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
ADD file:5ca4f47f61e345e345a04e385f59c0dbae96e3d9a3847eff9ec82735a92e05db in / 
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
	-	`sha256:1ec0a0fdff98ebea942fb34978c3e1893fee1092e8d0044b8d82301576686072`  
		Last Modified: Thu, 08 May 2025 18:11:38 GMT  
		Size: 28.5 MB (28540061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3273adb8720fb64f547b9a6d1a7ffd6d1330c51daf6ed393cfa037b238d8de1d`  
		Last Modified: Thu, 17 Apr 2025 20:08:26 GMT  
		Size: 21.5 MB (21532525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c56448db369931ce4d54211993030fc2e3bdde1f6d1ddcbb1e3d20d09c941b1`  
		Last Modified: Thu, 17 Apr 2025 21:09:13 GMT  
		Size: 48.6 MB (48649513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1edccf98926c27b50b293c1aedd6e483095fdc410cd6f6c8abb6a58ab640f776`  
		Last Modified: Thu, 17 Apr 2025 22:12:51 GMT  
		Size: 175.9 MB (175877700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d93e02f54009dfb351b913cc8d591fb9dad7787345d0ee84bdac36b2e9ec4ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11375552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3cddd6382a7c28c820fceacee0a582cb8bdbc29715cb82d18877b9bb51d865`

```dockerfile
```

-	Layers:
	-	`sha256:ae2a08f1801071d699435d1e6f49f1301b37286fd5a638819febfc8150b93aed`  
		Last Modified: Thu, 17 Apr 2025 22:12:46 GMT  
		Size: 11.4 MB (11365363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4af654c60d43ef031bf2302a3cfc2435efaf2ff9c9c6b5c70f910bda3913b440`  
		Last Modified: Thu, 17 Apr 2025 22:12:46 GMT  
		Size: 10.2 KB (10189 bytes)  
		MIME: application/vnd.in-toto+json
