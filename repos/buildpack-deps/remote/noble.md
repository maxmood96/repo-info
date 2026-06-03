## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:4618aa79a611f1a729f8a3fcef7ea3771b6cc4dacb41b15f8d333756dd2c13b6
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
$ docker pull buildpack-deps@sha256:e1fdd564fbd7f385b670fee2bc4064de9b7c419c025719efea986e968235c40d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.4 MB (274376347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3779a67248ce5df9b77c8eebc4993bdcf967727b2a9dc2550ea5038d3d837c0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:11:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 02 Jun 2026 09:12:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 02 Jun 2026 10:13:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450086accc6bf61159108eda83fd8a98ffb3d28b7b751cdd690a270df67a3fd1`  
		Last Modified: Tue, 02 Jun 2026 08:11:15 GMT  
		Size: 13.6 MB (13631676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a4502a619876b8a7826e9c38e999c517f266ca04e89c208a5583056e6bfaf1`  
		Last Modified: Tue, 02 Jun 2026 09:13:09 GMT  
		Size: 45.4 MB (45424662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9b81c8fb083ddd92246b1e447243e4d02ff27b83d98e97f5e708a380f4540c`  
		Last Modified: Tue, 02 Jun 2026 10:13:48 GMT  
		Size: 185.6 MB (185587204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:12ca1af918855b8c75f6e4ff7a476a9a6a6a3d7f95dcbb15cba4143dcdd261c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11733728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f199a1e96900af777b9e4e0843c88f9d8376f901af7bb8ea7e5b6bc36bbb920`

```dockerfile
```

-	Layers:
	-	`sha256:078b7d8ca178a44f63c77f3a11aab988c7c3ecce408df5e7d4ef2655f7c4bac3`  
		Last Modified: Tue, 02 Jun 2026 10:13:44 GMT  
		Size: 11.7 MB (11723587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b239a9b9eda7b52c91c5f4c59d1f7441f80124ee1dd9292cd93eabe02c4fad52`  
		Last Modified: Tue, 02 Jun 2026 10:13:43 GMT  
		Size: 10.1 KB (10141 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8b3b4815522d499040ac492065bda314716a3ff32bea44ebb9b272848109ce4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.6 MB (236584961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7c4ebe861ac2ad2da4b2da2287e82a0c5c274e40ea22c2bbe13eb0da275adb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 May 2026 01:36:59 GMT
ARG RELEASE
# Wed, 20 May 2026 01:36:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:36:59 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:02 GMT
ADD file:6d117ff682b1d31146902ad551197b012e75561d62d92d029219fcbf5c493c35 in / 
# Wed, 20 May 2026 01:37:02 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:09:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 02 Jun 2026 09:13:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 02 Jun 2026 10:14:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a2dede8d0e9ca179460cb274dab10c5c4b741cf1544b130df872809a4467e3e4`  
		Last Modified: Wed, 20 May 2026 02:15:37 GMT  
		Size: 26.9 MB (26859709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b118b4a0c6ca2ad4f0b7d3f4e7f824e209e719825c9725ce8c175f943f51da2e`  
		Last Modified: Tue, 02 Jun 2026 08:09:35 GMT  
		Size: 12.8 MB (12788925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86f8d7e733608db1d7c68cf03f7e3309fd2fff04c29d71ea92c207bcfff41dc`  
		Last Modified: Tue, 02 Jun 2026 09:13:37 GMT  
		Size: 48.9 MB (48938247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b573621e920887cdc0c5779eba4d3e91e5acd8a38dc5d8e6fa980eadde401fbd`  
		Last Modified: Tue, 02 Jun 2026 10:14:31 GMT  
		Size: 148.0 MB (147998080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d879a607f71cfed175757b1ec43d81693807e6de77603e1254215b3d6ef9bd5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11059429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c7f81794a4c351cf480392d70d796202ab9389005b0e3b28d68dcf31556575b`

```dockerfile
```

-	Layers:
	-	`sha256:7e3fdad3db74ab2a2602fa4f7d98646089266ce899605fb5b324971689c305d5`  
		Last Modified: Tue, 02 Jun 2026 10:14:28 GMT  
		Size: 11.0 MB (11049224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cc69af0acdb900d8a4e4413fd2d4286c4e40f71f357d2309edcf2db9e1896bc`  
		Last Modified: Tue, 02 Jun 2026 10:14:27 GMT  
		Size: 10.2 KB (10205 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:724585c5cb7c24802ddd06e138679fcdb7538ee08927ddabb498f9823b8ab5f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.8 MB (263841564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff16c77c3254f1f0be28768c31118b911f9496a1704a3af9b3747042fa32493`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:11:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 02 Jun 2026 09:12:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 02 Jun 2026 10:12:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b224b62323017769a142e9665ce9c8ea5728f289ccf479c861e9809bad5d8376`  
		Last Modified: Tue, 02 Jun 2026 08:11:26 GMT  
		Size: 13.5 MB (13466558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e08eafc6c229e820cd66a3b4e4d2fa50aa50bb9bc990e4456e2368cb77f6a7`  
		Last Modified: Tue, 02 Jun 2026 09:12:43 GMT  
		Size: 45.3 MB (45306900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823fabd7e84639cae4d814f89ec099ad6cfecbd79385d734ee4e9dbe498fe1d6`  
		Last Modified: Tue, 02 Jun 2026 10:13:30 GMT  
		Size: 176.2 MB (176191700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:046587b02046256392f616ce3a209fc4cfd53cf5ec758430900e48b88a3af3c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11283235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75424914b038a795f0fd8633c0a76547165c0000e5b00a82db79705fa15f23ca`

```dockerfile
```

-	Layers:
	-	`sha256:8c5a76b3c25e9d5991544ab27ad53ed8d04c6e8d947a6224e6b14398f070d109`  
		Last Modified: Tue, 02 Jun 2026 10:13:27 GMT  
		Size: 11.3 MB (11273014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2a503e605bf0f4faf9b6e08c30dbadb2525ed949709fa4cb739b85826680dd7`  
		Last Modified: Tue, 02 Jun 2026 10:13:27 GMT  
		Size: 10.2 KB (10221 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1e2370d34ac0a38376798090346f84f4366ec9c99448f90e405804796dc7a0ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289655427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f4e1b68be7adeed817ddd1abe4f1b4a8b471dc929179b59cc315387a92fc8a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:10:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 02 Jun 2026 09:12:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 02 Jun 2026 10:42:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187aeb2a9889fd701a0c7ee32834f3636fe8324b6c4bdb83baad19d7d389c281`  
		Last Modified: Tue, 02 Jun 2026 08:10:22 GMT  
		Size: 16.0 MB (15961906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4062997331ce0a95193beeeeffabe9870d8b52791710c25c92449b6c22aad75b`  
		Last Modified: Tue, 02 Jun 2026 09:13:08 GMT  
		Size: 50.4 MB (50388905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8c016169262bcef135864da54e10316a19438fb1f24f52d8a48a17b6160098`  
		Last Modified: Tue, 02 Jun 2026 10:43:15 GMT  
		Size: 189.0 MB (188990517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4cbd5d161e361fd0dd167b66dda4aaf31e2dd213fba5404f246f7512adeca132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11230606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6e3313c1c5b2735074c36892c53dca37b568b94779ccb5023f9f79c37a5c5b`

```dockerfile
```

-	Layers:
	-	`sha256:bf5459e49c7abccf5906b6f967f27fbd1488cb84f4132a4da4c5aff3229c5c13`  
		Last Modified: Tue, 02 Jun 2026 10:43:11 GMT  
		Size: 11.2 MB (11220433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7cf0fb15c19cb252ccfabaae714109bf19af0634b57b2c9b1a815dd824fc6d4`  
		Last Modified: Tue, 02 Jun 2026 10:43:11 GMT  
		Size: 10.2 KB (10173 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:5b78aad1757a9eae0805452f058292706e74d2e6a4b23bf822424d07459cb666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.2 MB (330230654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344fa36bca24520a3d65cf2454f9a15361cd8a975b414d164f1ceb011d4eb14f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 May 2026 02:06:08 GMT
ARG RELEASE
# Wed, 20 May 2026 02:06:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 02:06:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 02:06:59 GMT
ADD file:f1fd7ee282731834f2f36b17e9b538e569ade4ce8b89924b635551ff3a45c706 in / 
# Wed, 20 May 2026 02:07:03 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 18:04:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 02 Jun 2026 23:08:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 03 Jun 2026 02:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:924f9a731915e06f77b3487378ddf9426f8422fa1d96461bef1d0e0a35c36743`  
		Last Modified: Wed, 20 May 2026 02:15:52 GMT  
		Size: 31.0 MB (30965919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6165c45f7d3fe380ace51e4cc852195290eee963df6a38f7a335b47ef781490`  
		Last Modified: Tue, 02 Jun 2026 18:05:26 GMT  
		Size: 14.3 MB (14337475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d29f8b733601a7bdffb1d722ee43961e11975ae214b5596abc73a36270c020`  
		Last Modified: Tue, 02 Jun 2026 23:10:46 GMT  
		Size: 53.8 MB (53849669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0679d340aa625c48f933d4a6dc4fe288e9dca23a0cd13c3b8440cafb5a5810d`  
		Last Modified: Wed, 03 Jun 2026 02:52:59 GMT  
		Size: 231.1 MB (231077591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:36d8fab2d39f43f2574eb3a8a90a5e20ea0844c8aa164f65806638c13d9dc484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11223843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d261f2a26ef0a8be84683cd7534edd21a5938427b016abe17afd4e5ce068e1e5`

```dockerfile
```

-	Layers:
	-	`sha256:07cdf340bc8af2c36cb7cc68fa4ce65afdb147dc4811ecee89d68d3df9e008b4`  
		Last Modified: Wed, 03 Jun 2026 02:52:27 GMT  
		Size: 11.2 MB (11213670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90b8c53956cc8956a2632a9a8064dd95e2e49cbb338bff330e89831cf2927c73`  
		Last Modified: Wed, 03 Jun 2026 02:52:23 GMT  
		Size: 10.2 KB (10173 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:703621ee3f105276c97223345f581b9f3b80489d3ff9a9facd247a6aadc55b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.6 MB (252601375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d2f8a84f080f8889a8594d5d85c25fdb4a4002a073418522437b27b0632398`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:09 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:11 GMT
ADD file:b574b1e436c2db4e4d66f69c75e47a9aebf0da1ad375147eb2c0b7ff76c6ab7e in / 
# Wed, 20 May 2026 01:37:11 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:10:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 02 Jun 2026 09:12:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 02 Jun 2026 10:12:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c8ebd0a624851e8502e41ee64db2b6a45537554969784d82ebbc91c905cbc2ef`  
		Last Modified: Wed, 20 May 2026 02:16:00 GMT  
		Size: 29.9 MB (29912835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591d53e14180df305f0fe02c9303d41b73a2de4393458677c78c708d80d4d6eb`  
		Last Modified: Tue, 02 Jun 2026 08:10:13 GMT  
		Size: 14.9 MB (14944603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3cb41df27dfa7f083e1e5f3ac67744db7ef082b8f8a3dc3c7dff9d63fe0281a`  
		Last Modified: Tue, 02 Jun 2026 09:12:26 GMT  
		Size: 46.8 MB (46809270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae9bdcd49b85309e7dc13f35e1d21aa8ecc50112586174d9e7024553881fc7c`  
		Last Modified: Tue, 02 Jun 2026 10:13:07 GMT  
		Size: 160.9 MB (160934667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2369653ac7935ba5f483a0acbccac85bb1245990cc351fbf617e71071ad28320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11074429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cceb4479053ce7404f9beeafe53b304abb762906863b77aa8089b01d0e70f4d`

```dockerfile
```

-	Layers:
	-	`sha256:8aed67352e0998b5266a7e50c6d9bd40b50d4f8a0d07443bc4fd3cad61a053c4`  
		Last Modified: Tue, 02 Jun 2026 10:13:04 GMT  
		Size: 11.1 MB (11064288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:082fb6aa879201089805efa0c91a2f690b2b9fe7f8c1c6d46011103611f036cd`  
		Last Modified: Tue, 02 Jun 2026 10:13:04 GMT  
		Size: 10.1 KB (10141 bytes)  
		MIME: application/vnd.in-toto+json
