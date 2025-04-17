## `buildpack-deps:plucky`

```console
$ docker pull buildpack-deps@sha256:f3a19ad22a7cca54cfaeb12d3c255e72b5197da58924b819aa4d38cc4f540000
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
		Last Modified: Tue, 15 Apr 2025 21:45:08 GMT  
		Size: 29.7 MB (29710720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f757c9c78154a5f72abeb34fccd9ae44a8f5af313fc815debcf1f79b961ceb3`  
		Last Modified: Thu, 17 Apr 2025 19:07:38 GMT  
		Size: 20.1 MB (20131316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad5724474da3f6989ea92f5122b47e0db09df68332efd5cbdfb4cedb6b6bc41`  
		Last Modified: Thu, 17 Apr 2025 20:07:56 GMT  
		Size: 49.4 MB (49362604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c27c7152907b58ba77c7144a0287812d77c36e47c9c4da8b17b425c73219de`  
		Last Modified: Thu, 17 Apr 2025 21:08:28 GMT  
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
		Last Modified: Tue, 15 Apr 2025 21:45:21 GMT  
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
		Last Modified: Tue, 15 Apr 2025 21:45:15 GMT  
		Size: 28.3 MB (28261176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86243b610edc9d6c1e787d92fd82404a07dc7df1137da6257f05b9a0e0e6b99`  
		Last Modified: Thu, 17 Apr 2025 19:08:33 GMT  
		Size: 19.1 MB (19130209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ec985f2342cf4d978e41a17055220791aa792de162145255f27519e5e65e49`  
		Last Modified: Thu, 17 Apr 2025 20:08:23 GMT  
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
		Last Modified: Tue, 15 Apr 2025 21:45:28 GMT  
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
$ docker pull buildpack-deps@sha256:4d273694cbb0454416b169c9bd46a1fdeb0d19e260efa79e524d0af25fc6be73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.2 MB (402151373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff07e9668856fc25b18d808d97e75f4003c5b2c45be1575496081496208f8ac9`
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
ADD file:e1ade0e6cf3587e52fd2e150b2140bd7286f1ee2e92d7688f7a8e9295f045099 in / 
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
	-	`sha256:e94e661d55750b27c664c062defe70e7670822fb9e808139123296023b7710c3`  
		Last Modified: Wed, 02 Apr 2025 05:20:27 GMT  
		Size: 29.7 MB (29709622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b558e2c1a19e40220bf31e3d0070d8d63c7e158ae6110e51725275b330f1f1`  
		Last Modified: Wed, 09 Apr 2025 05:25:36 GMT  
		Size: 22.7 MB (22683100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5588567711623060e35aa3c33f50330a44b11c077bb51e996901fd513a90742b`  
		Last Modified: Wed, 09 Apr 2025 08:52:37 GMT  
		Size: 55.3 MB (55307041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db43e38ff91a18e807761ce614e8fbb96bf3197476ebc6a45db2b097a3c2c269`  
		Last Modified: Wed, 09 Apr 2025 11:47:00 GMT  
		Size: 294.5 MB (294451610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1bd8235244174cdbea0b936eda3b851d0445438622795314cd76a4352d6e4bbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11624591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d6ad498ae1f008096a917741e9d459fd0565e914a006684d3035e7a120c48a6`

```dockerfile
```

-	Layers:
	-	`sha256:5951be9c80bb71a057879500552329588d08c5fd53a97ca6c042b4c533c617a4`  
		Last Modified: Wed, 09 Apr 2025 11:46:21 GMT  
		Size: 11.6 MB (11614371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30dec5f94896e37d3876a47154d8da683c261c90c551d0525470037a6ed1f92d`  
		Last Modified: Wed, 09 Apr 2025 11:46:19 GMT  
		Size: 10.2 KB (10220 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1b1a56b64f4bc7afd8b49897b953233eb6df0060f133af6de8f7d10c12d5e40e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278638196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0483c96fb24409746fb482ad28f7508afdd82ca26894eb4245bb6ca6301d9d8`
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
ADD file:3187e5e8dafde316503f01473967b5018998dede98c27020e30f819899f6f60d in / 
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
	-	`sha256:0da16fa1ee9f8c39405683939ed3b583090ca47b5e4b8aad0a1993291bc12217`  
		Last Modified: Wed, 02 Apr 2025 05:20:34 GMT  
		Size: 28.5 MB (28538092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48d924dd8dd7d642c1ddf208f8b6cd8d159007414bde5bf9a8ba8d05ba940bd`  
		Last Modified: Wed, 09 Apr 2025 04:14:20 GMT  
		Size: 24.1 MB (24137884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7839b7b40dbb37516cc2befb4e4f946dcb071a33eb50544455d69b681c5de000`  
		Last Modified: Wed, 09 Apr 2025 07:11:39 GMT  
		Size: 48.6 MB (48640084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5e95063c09de60a723126209a57b46e535aa05e3fd032f52ec19b84f14fac7`  
		Last Modified: Wed, 09 Apr 2025 10:49:08 GMT  
		Size: 177.3 MB (177322136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2d81105a23610b2a978c4d6c3171677f2a49c5a1d09f7f9c6b51c27ed0259cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11374760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54949e5e4eacffb45ea30424b7e92464e2a4209fd689238457553e8f43d3b69`

```dockerfile
```

-	Layers:
	-	`sha256:e55a2b03cd6f37703a162c52d296dd51dc1e57e24d70bc10e0309f6bf50cdad6`  
		Last Modified: Wed, 09 Apr 2025 10:49:04 GMT  
		Size: 11.4 MB (11364571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5429899e0fafff07031ff3972c7d91f3b20aec9991e853957acf5fca5f90269`  
		Last Modified: Wed, 09 Apr 2025 10:49:04 GMT  
		Size: 10.2 KB (10189 bytes)  
		MIME: application/vnd.in-toto+json
