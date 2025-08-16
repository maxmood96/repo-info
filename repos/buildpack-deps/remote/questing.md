## `buildpack-deps:questing`

```console
$ docker pull buildpack-deps@sha256:1ed58972f0cc9693629c2ccbf0eecb30654771b11b9edbd075736b152371a92a
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
		Last Modified: Sat, 16 Aug 2025 09:06:44 GMT  
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
$ docker pull buildpack-deps@sha256:85feaf7ffe2f5b2db5d7587a05e91ceab16c40e1b3314ae39d98a36fcad7f453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.7 MB (624743840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f57885fa0612929dc464fcb4871a3e1f9cdf98df32edeeb3d74b8d0b47c76b`
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
ADD file:6cceeaa1e4c04b40ea2fa59915877179d13dfe75963b2bf5af2d179b7651fcab in / 
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
	-	`sha256:5fdf70baf2d69a62d712c5290da1eadd264d65ac840f33b44cab7084448ac925`  
		Last Modified: Sat, 16 Aug 2025 01:48:56 GMT  
		Size: 27.8 MB (27766578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f5f8859e7c63a9c160d8e856742d21c1c5cd88e9979620c98d02e7400a78d1`  
		Last Modified: Sat, 16 Aug 2025 02:09:43 GMT  
		Size: 17.3 MB (17259103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b0ed35808f1a066354a407ef01e08a829b491ab11dc1374245f9a9fe35239f`  
		Last Modified: Sat, 16 Aug 2025 03:09:34 GMT  
		Size: 50.4 MB (50357700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff13b59c3ae36d2fb457e6f8ff606bc844cfea8a0a3cc697ac7412c2725ac3b`  
		Last Modified: Sat, 16 Aug 2025 17:56:49 GMT  
		Size: 529.4 MB (529360459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9ff4daa3ee2073edbecaa633c4d6c6caa206230733fbb939e89213644b316ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11774239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:181b524dc8261076630f2d2a3a05444492a00bdbd4ab577474771cac5c0bbeda`

```dockerfile
```

-	Layers:
	-	`sha256:17a13dcb410ba1b064ef1900d3b5a9650d95267ac9c9a1c7d8cb53f1be587048`  
		Last Modified: Sat, 16 Aug 2025 07:19:57 GMT  
		Size: 11.8 MB (11763976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40a11d588f61f6a265bb29e873ee73394792e63ac3e7bb032c7d90f188448b25`  
		Last Modified: Sat, 16 Aug 2025 07:19:58 GMT  
		Size: 10.3 KB (10263 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a11e414e43f76eeab2aa82c2760c1fc517854c5278973b5acb47081396072662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.0 MB (715955378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a3ec8e821a4e379ea84a4e50359d55a372ee2b2317fc4040f2fc3d89a8d62a`
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
ADD file:b572189ec957414802fcdd31718df41b6aa37b1788b72c0b4276113a05ca3847 in / 
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
	-	`sha256:7e1303c7d3dea2855daef53d0a8f3ec020cf348b429dc95ae8653a86d0d8b8ed`  
		Last Modified: Sat, 16 Aug 2025 01:38:38 GMT  
		Size: 29.3 MB (29310925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a97eb8f278e435c853098d1ffa029d384d7ea69f796411aa8cddffc825cdaae`  
		Last Modified: Sat, 16 Aug 2025 02:09:42 GMT  
		Size: 18.4 MB (18384161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd834fb11e0a39629f2517d7a2504b48ab7ea76e3adbed4e69a2970486f0d7c`  
		Last Modified: Sat, 16 Aug 2025 03:09:59 GMT  
		Size: 47.3 MB (47319573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3d09396eb4abd0d523c19267eca28d8d90f50a625922d8f9c86cdd01256027`  
		Last Modified: Sat, 16 Aug 2025 05:08:14 GMT  
		Size: 620.9 MB (620940719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2b72e09682eddbe7a2730257b5ba329d0fab57c295be342f65719c5017047089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12086675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39cae4920c53a073a03b3544beaf0d5cfbaaeb27656969bdf5c3c2137a06e50a`

```dockerfile
```

-	Layers:
	-	`sha256:35a6beb96522075ac4754cc7d1b5a1ba9f3595458a74ec931eea93f495b1aa9d`  
		Last Modified: Sat, 16 Aug 2025 07:20:07 GMT  
		Size: 12.1 MB (12076392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7c823c197ca285b5d0efc18bae7cffa495a1540c39313301a18e6a5cb1a18e3`  
		Last Modified: Sat, 16 Aug 2025 07:20:08 GMT  
		Size: 10.3 KB (10283 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e68c82e1726159ffff4fed8f7e683370983ab038b550949c26ca2dd2c3a7649a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.5 MB (668523553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad52c95d917716a8b504dd812a99e2895f76224b34142f412a36a6f28e67b1d`
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
ADD file:9ee944b262d08273ebeed7c7e10331931448ce12dbbf68a399e8c06bef0d9b1b in / 
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
	-	`sha256:c17919b40786dbdd1b0e57e5e0f6254429096c2a4edd2c2d1abb619a9860b100`  
		Last Modified: Sat, 16 Aug 2025 01:52:43 GMT  
		Size: 34.2 MB (34171496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cee2a7f9203ea1c35edf02b23466082a11ceb072dbbb218de698867c4cd518`  
		Last Modified: Sat, 16 Aug 2025 02:14:52 GMT  
		Size: 20.7 MB (20745793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166e6e139026a2451641d9dd89313b21889f2928a9873bae1650f841fb688f4f`  
		Last Modified: Sat, 16 Aug 2025 03:10:37 GMT  
		Size: 52.9 MB (52949959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b0067d9cccd80fed08c984151d08c95c62d09982b775718502b4dff736e34b`  
		Last Modified: Sat, 16 Aug 2025 04:20:15 GMT  
		Size: 560.7 MB (560656305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ac8fda28d4492186d23fb18d3077388586cab398d58afa8a0626076233e233bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12005453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5b97974b88ed7f1dd1290103e3304848620ec05dd89f47a97fa33dbb349ad72`

```dockerfile
```

-	Layers:
	-	`sha256:82760ba534049b38f440cd2637614b5c48717b370c8124fa5603a6ff7464434f`  
		Last Modified: Sat, 16 Aug 2025 07:20:17 GMT  
		Size: 12.0 MB (11995218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09eaae4b87cb7c03f85ce93722c41cf3525c6019b6d8487260f13ece6ec28a28`  
		Last Modified: Sat, 16 Aug 2025 07:20:18 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a65a2141037df469a7acfc71b9799f86ebfa09a14f9a597fb477d849af2c5664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.8 MB (618804707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f6b5964064aa9153b91c4a7ae7cc5af228f703ac4148bbbcc871a6d356e3cd1`
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
ADD file:5d7fc1c7ab0341c0edd5218b95f2477fe713c704c0bfd784afe2ecc5f63cbe37 in / 
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
	-	`sha256:3d323ed134b3da3f8123622d5cd2d3cec4a1c728577e76ebc6912f3735a9864b`  
		Last Modified: Sat, 16 Aug 2025 04:58:48 GMT  
		Size: 29.7 MB (29651850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28c69c954dcf306c929945b1d30400512da9d95a60defbb5ae061ed32651efa`  
		Last Modified: Sat, 16 Aug 2025 05:12:35 GMT  
		Size: 20.9 MB (20949164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ece2a3cf86e85414183f79d9f7d1e6a9dbaebe0b93e05f6abedcc3de4b81557`  
		Last Modified: Sat, 16 Aug 2025 06:09:35 GMT  
		Size: 48.9 MB (48902947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f9989ed0f2878badd12fdc1de222ac13b795cf040c688cddbe19804e85ee99`  
		Last Modified: Sat, 16 Aug 2025 07:15:43 GMT  
		Size: 519.3 MB (519300746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f2ca0c2db460684cd44b979d154aa18c212367ba3ecea2e2bf24842c3068a66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11807712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec6f2a6ee49520e4cdc0826b530d5f7afc45e324662d7ed66ae4db5f0e41c81`

```dockerfile
```

-	Layers:
	-	`sha256:feebdca26bd1c7de8fcaa0ee75ab13e084ad839bf9143a7fb1093e67e837919f`  
		Last Modified: Sat, 16 Aug 2025 10:20:14 GMT  
		Size: 11.8 MB (11797509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1628602b656d6417c98c6529f065276891be217d5ef4816e49e4caa4a840617c`  
		Last Modified: Sat, 16 Aug 2025 10:20:15 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json
