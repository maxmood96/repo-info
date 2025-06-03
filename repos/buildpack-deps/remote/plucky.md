## `buildpack-deps:plucky`

```console
$ docker pull buildpack-deps@sha256:3a45816906be70316a08610d7200b5c37f008225d49b39229a343170a447f897
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
$ docker pull buildpack-deps@sha256:e67ade807dea0faadc16b08c2335b307b5ed5748d10f5240c1d36d95f54de7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308162272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e4c642761b3da6c3445e997e033f673e53cbcd7674665236013b4cd8315206f`
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
ADD file:29dc686fc057e53a681b8c03992e78dd0e0a51bf8a236cc3521a22c47f5a664c in / 
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
	-	`sha256:ceec33bc4ecc35f481014971dfd0bef0975e4c683b671de114d18f717809fdca`  
		Last Modified: Tue, 03 Jun 2025 13:31:12 GMT  
		Size: 29.7 MB (29705751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0550cdcb61b6424407d4e35266180693a8e2f5ef79da9fb59c3b1ddaaa0caa8c`  
		Last Modified: Tue, 03 Jun 2025 14:20:00 GMT  
		Size: 20.2 MB (20152326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db4449b6b81bf5c64b178e751a4c9768f50c9ae29e561f816a113f2a10d8f853`  
		Last Modified: Tue, 03 Jun 2025 14:20:01 GMT  
		Size: 49.4 MB (49361757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ba46cfe967ef2bffdeda0d01260c3d93625850abed1f10ec721b31b7195433`  
		Last Modified: Tue, 03 Jun 2025 14:20:13 GMT  
		Size: 208.9 MB (208942438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b47e57252b242dab9ee01d59af0b7d2de6b48b5a17aec250ae0db03f040f9921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11693846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbad1bb71fc15438ac8813ce479a5334ae974978ba2247f8d681bf5f70f8526b`

```dockerfile
```

-	Layers:
	-	`sha256:e3a3360a24ae27825ed0b023f6671d971cb61dbfcde9a90f68ea260b5bdaa954`  
		Last Modified: Tue, 03 Jun 2025 06:13:04 GMT  
		Size: 11.7 MB (11683657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce5bbdc9007748323ed53739b47ba4e4020df5fb311de6e7182d55f94254edb5`  
		Last Modified: Tue, 03 Jun 2025 06:13:04 GMT  
		Size: 10.2 KB (10189 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9f348a0d841eb41a4ad440676471949c41dac8a124c8ba4a7cf248fee9fd709e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.9 MB (254911799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc2cb8c768c443126308fa3313cc360217ddb2b306ef6fd2ea343309e3b3da3f`
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
ADD file:d6879d0c0fa28bd1837e6dbafdfb1a3f4954b30c82228ec457f3534084b1b06c in / 
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
	-	`sha256:beb95769af35adb742af688d03f5edaac2080fd1544a9debb2a242d0a4f83f3a`  
		Last Modified: Fri, 23 May 2025 20:00:12 GMT  
		Size: 26.7 MB (26744711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33a63434c954882953b5d658928b56d67b6af1e7f05181f9724f04bd6215482`  
		Last Modified: Tue, 03 Jun 2025 04:18:59 GMT  
		Size: 17.9 MB (17863778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40283a6b3701254e50fb1d57a197a4238779b267e309108c6271072c59fa5b03`  
		Last Modified: Tue, 03 Jun 2025 05:14:35 GMT  
		Size: 50.3 MB (50291001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccca9b105dfe6111ccc63b9ec2ac4b7466c29a04ec86a7466673e934e92c8dec`  
		Last Modified: Tue, 03 Jun 2025 06:24:54 GMT  
		Size: 160.0 MB (160012309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ee4f1420addc0945e552a175a58f9220bbf4db49303c28bd166c512795df64ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11446386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b45ab42e6e570cf1210a097c324361411623f080fa92099332f143297bea579`

```dockerfile
```

-	Layers:
	-	`sha256:b8a45f532ad285885dbecd8180d52f1a4682028b8bf91fd17ea84c673dd1df05`  
		Last Modified: Tue, 03 Jun 2025 06:24:50 GMT  
		Size: 11.4 MB (11436137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d05af2a2233281510e6698ede2a1d28477b78d02d9a07d915918b20050a47eea`  
		Last Modified: Tue, 03 Jun 2025 06:24:50 GMT  
		Size: 10.2 KB (10249 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:fb438b979d29afd43604daa265281d8f1e6dec6a7e850a95068f1a040ceed19b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288718004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39ff748ec100be2654bf75b94d22e16cd72cb5c5ca88ba4bc011d2f55a99889`
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
ADD file:69566c238e02d3d509c1c7043bbfec00fb61739dc83b7d0aae8b0ae65e212969 in / 
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
	-	`sha256:7d9f0f10f351a33173394e673a1712955d12f1533cfa6efcbbfe5b9f243ec4ac`  
		Last Modified: Tue, 03 Jun 2025 13:49:11 GMT  
		Size: 28.3 MB (28256177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd31d13b21fb543ad35891a01647ccde88b51562a2ced6d124b09518d92dc31`  
		Last Modified: Tue, 03 Jun 2025 04:20:10 GMT  
		Size: 19.2 MB (19151561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33404833a315b5a43c1444c81214ccdd6142e55c351795f8535774479e087cb6`  
		Last Modified: Tue, 03 Jun 2025 06:49:21 GMT  
		Size: 47.2 MB (47193537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ed268a77acdfc1679901969477c703a37baee42e922582513b7207d296ea33`  
		Last Modified: Tue, 03 Jun 2025 11:46:07 GMT  
		Size: 194.1 MB (194116729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dc1734f4f4ffd289fc25fd579e799de7cee5e5b68f47313abdd16ee9d7174e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11757175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33cfe5b6267c1227fb4487eed27bdd74591e4b9c6b73901b120c2f70e77e0d22`

```dockerfile
```

-	Layers:
	-	`sha256:eaf0a338c3357844a51cd490949dd97d2385733497e29facf8be76f0b8b63b81`  
		Last Modified: Tue, 03 Jun 2025 11:46:02 GMT  
		Size: 11.7 MB (11746906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83736a59ab35215a61c4da752c6fc927da9b8d9731907f5be481aadf351a7008`  
		Last Modified: Tue, 03 Jun 2025 11:46:02 GMT  
		Size: 10.3 KB (10269 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:aa529d64a26463a2e3d6a8ec35390b168a379c74dba66589a3e1b5ef4750327d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.5 MB (311513442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9795c68a12125a84ed542eb225ec7281faff43acca1730ed4b0779ecda86c0de`
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
ADD file:cda37fe24274d4de5d4c3fc4886aefbad3f40443b4e91f57028a7577b742d264 in / 
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
	-	`sha256:e87250c63325ea7d2be55bf09a946f77b9abd9b4493fa3899f34e621de51cd51`  
		Last Modified: Fri, 23 May 2025 20:00:19 GMT  
		Size: 32.9 MB (32930743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06c94083c16bbd7aacd8020c570715224c5f67a1059694131841333ffe84d12`  
		Last Modified: Tue, 03 Jun 2025 04:19:40 GMT  
		Size: 21.6 MB (21579680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d65d915ccdc91645aabba219b68467bee4daf2637d2024e2476c72fe413f0b`  
		Last Modified: Tue, 03 Jun 2025 06:34:37 GMT  
		Size: 52.6 MB (52615400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8973bcc8132ce10d0c61b741afe2d067322b76354e0bdf47a1fd3eb3b41c2fba`  
		Last Modified: Tue, 03 Jun 2025 10:28:31 GMT  
		Size: 204.4 MB (204387619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d0aafc9e4ff090d7c6919b4d13fb0af3340c19fbbec17edf96a2e622c8557242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11675109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2e44c0ee3bce2163578f93a9fc510164182a43c7884c2fbd9779efab1a6bb2`

```dockerfile
```

-	Layers:
	-	`sha256:bd69778dee71d05533cc2f0eb248cdc0ba0ad4118b7d8f023b28402b044cd560`  
		Last Modified: Tue, 03 Jun 2025 10:28:27 GMT  
		Size: 11.7 MB (11664888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fb652f41df099fad2b823b4c87411a77b3e4801036f942aa73c0ce62206340e`  
		Last Modified: Tue, 03 Jun 2025 10:28:26 GMT  
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
$ docker pull buildpack-deps@sha256:d598a4de41ee9815204f65a01799e4f215e782836fbbe6b30d3af75c732a54df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274653583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b4e72fef52b479c6873b2e9a8efdfc27db46f14d23e6f611059f18ca419f2fd`
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
ADD file:f4cf53c93b512451b6135ae8d690cc56703aa0b63ad01beca88b2ac68598596c in / 
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
	-	`sha256:1c99586607cc0eb79096bece5f19d764d8f7b01451aa36df68f188900c9f0a46`  
		Last Modified: Fri, 23 May 2025 20:00:33 GMT  
		Size: 28.5 MB (28547574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feaeb09c8304d0b85a488269c9ff3dfabd51ec24de81796614b926dda7a0fac8`  
		Last Modified: Tue, 03 Jun 2025 04:18:11 GMT  
		Size: 21.6 MB (21552885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43393f50c9188d163cfff89f0ddba3d9e020bebf5745b91c70e2d02b26452bd`  
		Last Modified: Tue, 03 Jun 2025 05:18:48 GMT  
		Size: 48.7 MB (48652135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a527c4098103cbdb47105f83cb45ee0dd4d5f4422f5b0814cef740726b70f12e`  
		Last Modified: Tue, 03 Jun 2025 07:04:57 GMT  
		Size: 175.9 MB (175900989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f48ea12c456f0a85860ab5c7c64aa09ace8111f8384d7b6904408f54d4bfa00d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11479891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3fc6f8207b1caae6bce549f6bed1721bdd89e31201b607396871faf7da40db`

```dockerfile
```

-	Layers:
	-	`sha256:e83bf35bed89278ab0cdb9218e3e13b9fe7a743ff550007cc0ac211cf94fd8bc`  
		Last Modified: Tue, 03 Jun 2025 07:04:54 GMT  
		Size: 11.5 MB (11469702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b42b1a79a8340cf84156e62633ff2bd258dc9944195850a1e5a3ca7e25c92b36`  
		Last Modified: Tue, 03 Jun 2025 07:04:54 GMT  
		Size: 10.2 KB (10189 bytes)  
		MIME: application/vnd.in-toto+json
