## `buildpack-deps:resolute`

```console
$ docker pull buildpack-deps@sha256:e554d27eda550a8412e18e6b28bb694c6ceaa93659b902bfe32428750360b31e
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

### `buildpack-deps:resolute` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:24934bdd84ae27ea8079a8caf401f6101628d04efb0479cfcbf9c35f2a8e0ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.1 MB (272088838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a44de7886dd5fa3103aed34bb77b7bb9621c1fde0b1d83188dd90b7b917682d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 30 Nov 2025 03:28:38 GMT
ARG RELEASE
# Sun, 30 Nov 2025 03:28:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 30 Nov 2025 03:28:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 30 Nov 2025 03:28:38 GMT
LABEL org.opencontainers.image.version=26.04
# Sun, 30 Nov 2025 03:28:41 GMT
ADD file:55d8d7c2a599eebdadf029d609185a93b70e5c572fbf864d8e1dea8ca32c7e8a in / 
# Sun, 30 Nov 2025 03:28:41 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 22:11:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 02 Dec 2025 23:11:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 03 Dec 2025 00:13:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ab1cebba4171ff5f2efb3092f20bb54ba4f8853e67ae7ba36b66c426fd17d4b4`  
		Last Modified: Tue, 02 Dec 2025 21:29:21 GMT  
		Size: 33.8 MB (33763754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db10505684265b8f15b7389af79a333e81deff06c492e0c86a76684ac37bc564`  
		Last Modified: Tue, 02 Dec 2025 22:11:39 GMT  
		Size: 19.4 MB (19408148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecad741edb8a7bfc0a31060fb84a145b290196acbec4e0ab37b15a7ef2e8d5c6`  
		Last Modified: Tue, 02 Dec 2025 23:11:32 GMT  
		Size: 48.1 MB (48097579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d6905c4a47bd3cefadbee2701ca88cc4c7f97135c536a043e47cf092386748`  
		Last Modified: Wed, 03 Dec 2025 03:26:14 GMT  
		Size: 170.8 MB (170819357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a8c4636f36ebc79d8aebead262b39d92f44d20b2f4254301c07eb0803db4c359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11680402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a96884610fbacae9c80486b9b65a2cce0839ccd014ae0abcd2e5543e650087b`

```dockerfile
```

-	Layers:
	-	`sha256:8a2a02c4dd78ea64eb60f24970317a5194541bb50cd2ccb3de009b144bf8d397`  
		Last Modified: Wed, 03 Dec 2025 02:20:11 GMT  
		Size: 11.7 MB (11670242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08d835ceec22a522665ab6f52b231c351bddfd36405eefcc55228a0de6200ed5`  
		Last Modified: Wed, 03 Dec 2025 02:20:13 GMT  
		Size: 10.2 KB (10160 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2f88b49bfc8798221681535326fb83d626076b976c44b5c047259a6cdc39c97e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.3 MB (225269492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee0729a0a653aa5f2e2d0f6a818f3f16b2be83eb47047b94f16495a680c7ed1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 30 Nov 2025 03:30:55 GMT
ARG RELEASE
# Sun, 30 Nov 2025 03:30:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 30 Nov 2025 03:30:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 30 Nov 2025 03:30:55 GMT
LABEL org.opencontainers.image.version=26.04
# Sun, 30 Nov 2025 03:31:00 GMT
ADD file:9003dc9541ce76045dd67f0ad2d95c2697e3b7155bc6abaa06ebbf38b78aa407 in / 
# Sun, 30 Nov 2025 03:31:00 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 22:11:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 02 Dec 2025 23:11:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 03 Dec 2025 00:12:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cd71ce16db91fba8d9cd0435979699051c3f118fd7c402d7cbdc6eb32d240426`  
		Last Modified: Tue, 02 Dec 2025 21:30:00 GMT  
		Size: 31.1 MB (31147436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148d15adde59bf29b7e8735e2ca69fe70d44a2559de9882a34bf8c8ed08114a7`  
		Last Modified: Tue, 02 Dec 2025 22:11:34 GMT  
		Size: 17.8 MB (17756410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1a9c5eb4062359ec001f06df08977ad317de1969c45cac1858b9e39fe7e85a`  
		Last Modified: Tue, 02 Dec 2025 23:12:20 GMT  
		Size: 50.6 MB (50591212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34798eb588de9f70c06c2a6fcf5e14c8e76b75803b4a6fd8b51036aaa4c9101d`  
		Last Modified: Wed, 03 Dec 2025 00:13:18 GMT  
		Size: 125.8 MB (125774434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:05b3f05b00f84d26488258155e62312dc1aa75de977d740a8b8453200ea5878a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11421372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:240d7d7b8a9e753e306e3bacd38bf60c3bce84f9440b391749524a48a3af345c`

```dockerfile
```

-	Layers:
	-	`sha256:dc705388acdb61a2ef032bdc6daa2531a611431f1a13f6313a5f4d784e6bff34`  
		Last Modified: Wed, 03 Dec 2025 02:20:22 GMT  
		Size: 11.4 MB (11411148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fed1c7f3627c88e13a1294d6b3d33e2d50eb8b774737b522c170d5bd3440993`  
		Last Modified: Wed, 03 Dec 2025 02:21:07 GMT  
		Size: 10.2 KB (10224 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3f27faf1521e146885f6aaa67f964bc265bd255b8088f12b223eb2f826236ac2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.5 MB (260462153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59864b3040cd5fe9b0b09c216033a91cab55684a002ebb5d49c29a41ce920b5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 30 Nov 2025 03:30:15 GMT
ARG RELEASE
# Sun, 30 Nov 2025 03:30:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 30 Nov 2025 03:30:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 30 Nov 2025 03:30:16 GMT
LABEL org.opencontainers.image.version=26.04
# Sun, 30 Nov 2025 03:30:19 GMT
ADD file:980aeef211cdc1dc441eea6aa6e600765d2ad909294a70a9dfc54b86b8acb82c in / 
# Sun, 30 Nov 2025 03:30:19 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 22:11:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 02 Dec 2025 23:10:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 03 Dec 2025 00:12:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a3b546ef13e5307a10c1657c5a408cce9d7fd8da967afbb8383018e2b2c2a8ed`  
		Last Modified: Tue, 02 Dec 2025 21:29:59 GMT  
		Size: 33.3 MB (33301426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67396e94407424cf9bf12089c47b3de0191e9811df778f7c7d577a0ce4e2d3fa`  
		Last Modified: Tue, 02 Dec 2025 22:11:49 GMT  
		Size: 19.0 MB (18963975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcefd35480496c60d20e52391d3cc2b8e99b310df00d219ea34f600f9ab8573a`  
		Last Modified: Tue, 02 Dec 2025 23:11:21 GMT  
		Size: 47.7 MB (47730732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c2f68a2b1bd2eb85f5cedddcdf58dc7f5ce331bcbbf68eb8edb938b5953f8c`  
		Last Modified: Wed, 03 Dec 2025 03:26:08 GMT  
		Size: 160.5 MB (160466020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8810b530e30416741f47bb7e8c98ca2224737744d0af9d0040a6af50ffadacfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11734658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7a2857282f9818f10fa974994a56a157da7cafee7ada4190e275451c8991e5`

```dockerfile
```

-	Layers:
	-	`sha256:283731a9ed4cbc7915e2688e755b056a2da355ed76255e1e2bbb6578eac4fef1`  
		Last Modified: Wed, 03 Dec 2025 02:21:17 GMT  
		Size: 11.7 MB (11724418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f39d2b3b538159f9f8db066ac12520e1d3174b530b1a8b8c5eb8c8e21383173c`  
		Last Modified: Wed, 03 Dec 2025 02:21:18 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:082697f274ee0d06e18eda1a982c20511353a37143d84e9039065ae88ea4d549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.6 MB (288574039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a66b9718360cbeb368d0f1140dd77fe6c4bd64a1da373ca5523fe327ed1d5b2a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Nov 2025 16:28:00 GMT
ARG RELEASE
# Mon, 03 Nov 2025 16:28:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Nov 2025 16:28:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Nov 2025 16:28:00 GMT
LABEL org.opencontainers.image.version=26.04
# Mon, 03 Nov 2025 16:28:04 GMT
ADD file:9dc48ed376a5f94217dece483aa159c1e9252d86454df2922631eb0d8e28f33f in / 
# Mon, 03 Nov 2025 16:28:04 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:02:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Fri, 14 Nov 2025 08:03:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 14 Nov 2025 14:25:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b8a7d2071217601e99b42fdc9fbf0f11b498ca9a077822716cc8b2c60912ef80`  
		Last Modified: Thu, 13 Nov 2025 23:04:03 GMT  
		Size: 39.7 MB (39663384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136f99d9e4921d1d5ec73699767f26acccc59c2f03cb3c2902fd8897e7af4545`  
		Last Modified: Fri, 14 Nov 2025 02:03:05 GMT  
		Size: 20.8 MB (20787622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca1c166775b82d33750156d6c084bfa5ea195c09bca4014f1aa368ef94e5c8e`  
		Last Modified: Fri, 14 Nov 2025 08:04:26 GMT  
		Size: 53.7 MB (53676009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fae2ff2c6b73b9696106ee1de2a9c38d208bf65d85f3cc0beaf20baf6c0fdb`  
		Last Modified: Fri, 14 Nov 2025 23:45:19 GMT  
		Size: 174.4 MB (174447024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bbed1b8ab5ac30e0ed4625570dac6844cbf5f76257eade72508049c487edcc36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11660216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a744c1ad7ad49333dd4b4fef4facd0ec8f1c78682b86e75cdb6b0d6bda5c3f37`

```dockerfile
```

-	Layers:
	-	`sha256:8aa5312ffbd5f5701811dcc9daf20b9a099879ae8c0d722e82415e415f3078ec`  
		Last Modified: Fri, 14 Nov 2025 17:20:00 GMT  
		Size: 11.7 MB (11650024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6d86b1dbf9904b4fa50b778cafba45f9922a0a33ec3ea4b640671b31935d04f`  
		Last Modified: Fri, 14 Nov 2025 17:20:01 GMT  
		Size: 10.2 KB (10192 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1b70c85d8fd803661cdb801993ae5b99addd30331e51269359e58f564aa9af37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (240011724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1274c841bfd8a24ddec38634b466f4bccffdb83ee69e17e44acf3f91e2938ce8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 30 Nov 2025 03:41:55 GMT
ARG RELEASE
# Sun, 30 Nov 2025 03:41:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 30 Nov 2025 03:41:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 30 Nov 2025 03:41:55 GMT
LABEL org.opencontainers.image.version=26.04
# Sun, 30 Nov 2025 03:41:57 GMT
ADD file:f463f77192f170ee64673f5278f91bdada45dc922d8fd7d4131d154fe01a4fec in / 
# Sun, 30 Nov 2025 03:41:57 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 22:11:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 02 Dec 2025 23:10:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 03 Dec 2025 00:13:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cf3c1d5ff4ce09e68a22f9e6e4bbc83188de5c366e0945d8cc5e8dc699355c91`  
		Last Modified: Tue, 02 Dec 2025 21:28:26 GMT  
		Size: 33.4 MB (33395368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31df4f0b4855de3fe403ca5d6b658f6b8866dffa556bc1fe856875a56977e649`  
		Last Modified: Tue, 02 Dec 2025 22:12:00 GMT  
		Size: 19.9 MB (19867529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13c1b2aaafeb245c9cf5096ea5239ce001ce8766f974bd2ace2c71a24ffa0cb`  
		Last Modified: Tue, 02 Dec 2025 23:11:34 GMT  
		Size: 49.0 MB (48971153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4882feb94229f802b3b834edc15c94dfc6a5e9130673b316fdb41b41957ddd`  
		Last Modified: Wed, 03 Dec 2025 03:26:04 GMT  
		Size: 137.8 MB (137777674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b6072934dc3c547c164f028fa1b9beb426d6c33c0e07439cb597d37c7d8999f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11455302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616888d78ac3210bf6872ff94696e40ae4aaa6671a2b914b41403239d7c20179`

```dockerfile
```

-	Layers:
	-	`sha256:fae8c9aeaba80f102ef31bdf08c3f3d5e8af038eec70a8c1929290aaa48fe80b`  
		Last Modified: Wed, 03 Dec 2025 02:21:37 GMT  
		Size: 11.4 MB (11445143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27819223754a50abd86614493d2693361e3799178062f3286c697c0d13d6ab31`  
		Last Modified: Wed, 03 Dec 2025 02:21:38 GMT  
		Size: 10.2 KB (10159 bytes)  
		MIME: application/vnd.in-toto+json
