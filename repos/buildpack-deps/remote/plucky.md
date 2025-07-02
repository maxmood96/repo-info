## `buildpack-deps:plucky`

```console
$ docker pull buildpack-deps@sha256:354161addbb4523bb0fca44b9b74642df66d8f052f06cb8b95226122af41cda7
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
$ docker pull buildpack-deps@sha256:3058263cad85b0601572860ca98a1083ebe8abf78558a10fd2884c5a9c8e7c6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308203544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb2e1500c50a1e52396e3a78ce1fee388a64b28f5f5b2680de761416fbee5d7c`
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
ADD file:0eaca8af04f137f2866a51aed71cb0d60a5a9483bab5dace0b797eb156bf8181 in / 
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
	-	`sha256:03c83456f76b8d3372f50dc65e1d9e37069a275d343928676618ba69375be326`  
		Last Modified: Fri, 20 Jun 2025 13:04:27 GMT  
		Size: 29.7 MB (29707855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c2978e07515c3b36a9e013517d5d0fdb1336f1e5f279fcc992ab204e90af30`  
		Last Modified: Wed, 02 Jul 2025 03:09:59 GMT  
		Size: 20.2 MB (20153078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797e0893e17797c98a316aba7f7b08eb1b3c05fa694f2f281b7fb2c4b8b065e8`  
		Last Modified: Wed, 02 Jul 2025 05:11:15 GMT  
		Size: 49.4 MB (49441540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728ca7b57daf25a8a61ebbb1f58de169382e57094c1c95a2f12c3759d70d6c98`  
		Last Modified: Wed, 02 Jul 2025 10:59:54 GMT  
		Size: 208.9 MB (208901071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4f358f279fcb7be6c519fc070becc99eb96c775d7a4d72f4fe1d47a68e4b8aa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11975234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f3565bdc2256f6e4309613284bd00d1538112341dc9f2315f36151afadd990`

```dockerfile
```

-	Layers:
	-	`sha256:19a4622f440b489f4d505b64e669f9ab470480c6077680943a83f8a1432b329f`  
		Last Modified: Wed, 02 Jul 2025 07:20:26 GMT  
		Size: 12.0 MB (11965045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf1331636b31970bd6a797542bc6b8a96c49bd809599d37171d1e10bfc8180cf`  
		Last Modified: Wed, 02 Jul 2025 07:20:27 GMT  
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
		Last Modified: Tue, 03 Jun 2025 15:49:03 GMT  
		Size: 26.7 MB (26744711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33a63434c954882953b5d658928b56d67b6af1e7f05181f9724f04bd6215482`  
		Last Modified: Wed, 11 Jun 2025 12:40:55 GMT  
		Size: 17.9 MB (17863778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40283a6b3701254e50fb1d57a197a4238779b267e309108c6271072c59fa5b03`  
		Last Modified: Wed, 11 Jun 2025 12:32:05 GMT  
		Size: 50.3 MB (50291001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccca9b105dfe6111ccc63b9ec2ac4b7466c29a04ec86a7466673e934e92c8dec`  
		Last Modified: Wed, 11 Jun 2025 12:28:09 GMT  
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
		Last Modified: Tue, 03 Jun 2025 16:19:50 GMT  
		Size: 11.4 MB (11436137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d05af2a2233281510e6698ede2a1d28477b78d02d9a07d915918b20050a47eea`  
		Last Modified: Tue, 03 Jun 2025 16:19:51 GMT  
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
		Last Modified: Fri, 06 Jun 2025 17:54:26 GMT  
		Size: 19.2 MB (19151561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33404833a315b5a43c1444c81214ccdd6142e55c351795f8535774479e087cb6`  
		Last Modified: Fri, 06 Jun 2025 17:54:32 GMT  
		Size: 47.2 MB (47193537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ed268a77acdfc1679901969477c703a37baee42e922582513b7207d296ea33`  
		Last Modified: Fri, 06 Jun 2025 17:54:44 GMT  
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
		Last Modified: Tue, 03 Jun 2025 16:20:00 GMT  
		Size: 11.7 MB (11746906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83736a59ab35215a61c4da752c6fc927da9b8d9731907f5be481aadf351a7008`  
		Last Modified: Tue, 03 Jun 2025 16:20:00 GMT  
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
		Last Modified: Tue, 03 Jun 2025 15:49:04 GMT  
		Size: 32.9 MB (32930743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06c94083c16bbd7aacd8020c570715224c5f67a1059694131841333ffe84d12`  
		Last Modified: Wed, 04 Jun 2025 11:29:30 GMT  
		Size: 21.6 MB (21579680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d65d915ccdc91645aabba219b68467bee4daf2637d2024e2476c72fe413f0b`  
		Last Modified: Wed, 04 Jun 2025 11:29:51 GMT  
		Size: 52.6 MB (52615400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8973bcc8132ce10d0c61b741afe2d067322b76354e0bdf47a1fd3eb3b41c2fba`  
		Last Modified: Wed, 11 Jun 2025 12:23:35 GMT  
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
		Last Modified: Tue, 03 Jun 2025 16:20:09 GMT  
		Size: 11.7 MB (11664888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fb652f41df099fad2b823b4c87411a77b3e4801036f942aa73c0ce62206340e`  
		Last Modified: Tue, 03 Jun 2025 16:20:10 GMT  
		Size: 10.2 KB (10221 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:79c0dcc7cad5c469844e96ae84862af302152d71628680a74a02a03a0244aa06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.1 MB (398147470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94399de7bca13767e8a8d260fa4e8b56418f90af9997af36e82816714ed1f48d`
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
ADD file:c49bd76120e14b8b9162a3d1121cdf875a3d564e276b9f4ca958ab6539abd18b in / 
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
	-	`sha256:a1b727d8aae617aa5491ea5a16fbbe00714b12ddd4035d39d00167040babe630`  
		Last Modified: Tue, 03 Jun 2025 16:56:03 GMT  
		Size: 29.7 MB (29736274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c289b4d47c7acf94afbc11299bd9a8acfc809ebfc9614bf0d9d55878e3c933`  
		Last Modified: Wed, 04 Jun 2025 11:30:24 GMT  
		Size: 19.9 MB (19888048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041bab769fde9af465bf0f8205fe976dcb138ab77f163aa7ad0fc5ece41b9932`  
		Last Modified: Wed, 04 Jun 2025 11:30:42 GMT  
		Size: 55.3 MB (55313775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7df389ac2384fa74cf5ac62c0f1204c0e2b82c541a7363d48e7450faaa0c9ac`  
		Last Modified: Wed, 04 Jun 2025 11:31:29 GMT  
		Size: 293.2 MB (293209373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:582841c602196872718e0e9f14f67acde27d734c94b2eb747ef4397da77a99c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11731483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06ebed009c9334a051d9db482a11b1cc63fbe9c3b34e1c70373f3c3bc1ef8681`

```dockerfile
```

-	Layers:
	-	`sha256:18dfe5ef8cf6ab86106939860ff64998db5b30be462ce895ae3b65cadc313895`  
		Last Modified: Tue, 03 Jun 2025 16:20:20 GMT  
		Size: 11.7 MB (11721262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a6746bafd9e5a9cb6d8566b36fbf8e292195ff8225722aa9f62773208211c18`  
		Last Modified: Tue, 03 Jun 2025 16:20:21 GMT  
		Size: 10.2 KB (10221 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:eddc18f9d2e9363ec2652d69853c697d0c7d7f5c97a7ecbf94858ed4dbfa3364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274729464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10931dbbf7a3c6d69f08ab0872a508c84e23cd916a2cfbdf5e56a37a02c0b18c`
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
ADD file:65c3a17ff08c38e485d0568f4f81d1da9836ed770a2520181c054658bb406a70 in / 
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
	-	`sha256:8d2faba794696654b8419836f3eb5351940dfc517452f2b22b94fd93a86787cd`  
		Last Modified: Wed, 02 Jul 2025 03:45:47 GMT  
		Size: 28.5 MB (28549841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0178a6e17bae3ec6d2f5a9dfedfcef603db4f51fd66d1823b0b0ee74433626`  
		Last Modified: Wed, 02 Jul 2025 04:13:48 GMT  
		Size: 21.6 MB (21553717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6253d2a81a2a83edc5f04fdca1b31e72c9fd0d30d375ceef0386e642e48a5f76`  
		Last Modified: Wed, 02 Jul 2025 05:19:09 GMT  
		Size: 48.7 MB (48698463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f5aed737ac7b69bd93e380b9b706b95588c1a0b1a96cc81ce482672d5a504a`  
		Last Modified: Wed, 02 Jul 2025 07:15:58 GMT  
		Size: 175.9 MB (175927443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:27116d9a9739947d4879deb22548f56f99d9bad88cb159a2f72fc506ea81f0ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11761272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e7c15a21db3e4a7eabb7cfb3ad16a01a886d067adb3970133dda86720b96bc`

```dockerfile
```

-	Layers:
	-	`sha256:666f3a78d50e4253c8976c6690d43f63e6fad56024843796c88a5697be6ccbcd`  
		Last Modified: Wed, 02 Jul 2025 10:20:33 GMT  
		Size: 11.8 MB (11751083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c2a2a32efe3c3c8078aa47d634279a913f6bc7182379b8c1f8abd5c0d0a02f5`  
		Last Modified: Wed, 02 Jul 2025 10:20:34 GMT  
		Size: 10.2 KB (10189 bytes)  
		MIME: application/vnd.in-toto+json
