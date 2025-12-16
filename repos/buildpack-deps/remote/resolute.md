## `buildpack-deps:resolute`

```console
$ docker pull buildpack-deps@sha256:81f7db856e84c53db8768844c0881a1abb2e683bacdb9e08b891249f3faf2eb0
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
$ docker pull buildpack-deps@sha256:3a203067fe9166b3f95356c2a23fe071f5edc61438ddc0c9c1bb53773cc2d86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.3 MB (273275266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bae33081928ff4dc7c571f36d4d215ea4b0f0ffd7586b7e2162b224e95864e5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 08 Dec 2025 03:12:22 GMT
ARG RELEASE
# Mon, 08 Dec 2025 03:12:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 08 Dec 2025 03:12:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 08 Dec 2025 03:12:22 GMT
LABEL org.opencontainers.image.version=26.04
# Mon, 08 Dec 2025 03:12:24 GMT
ADD file:20d5e915d0d393fcb7e648f66e92f60aae8aa4008ec9f474084335d6b517afe4 in / 
# Mon, 08 Dec 2025 03:12:25 GMT
CMD ["/bin/bash"]
# Mon, 15 Dec 2025 20:11:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 15 Dec 2025 21:10:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Dec 2025 21:16:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1930ad95e8edfa40a67fed625a6b952de1df4b24c225dd737adb00346824f4ac`  
		Last Modified: Mon, 15 Dec 2025 20:02:05 GMT  
		Size: 33.7 MB (33742427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc032e9d150edca71ca527020eb733586080f7bda49bec4c3582b3f374be743`  
		Last Modified: Mon, 15 Dec 2025 20:11:39 GMT  
		Size: 19.4 MB (19428885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34e03e630d58ec8ee7cf7211a1e391f98a0ccd100cc5f40ec4beb6f17291111`  
		Last Modified: Mon, 15 Dec 2025 21:10:50 GMT  
		Size: 48.6 MB (48553742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649e6b3ca56eb0233fae185b4fe8c863db18aaf9824e54d20ec9afc5f1a96555`  
		Last Modified: Tue, 16 Dec 2025 01:34:24 GMT  
		Size: 171.6 MB (171550212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:722f2d40aec8fa312bb85a77d33a9a3b74f919ed2ad4e2c4887c25222915fece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11684808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3941b2b65f35bc11c744dfcfa84b7f2ec16f8b1540806323789d77edc87df65`

```dockerfile
```

-	Layers:
	-	`sha256:35e6f76ea2eefb3c5385f7afea23c260a2b55c5138300ba8f058fb9a37022ce9`  
		Last Modified: Mon, 15 Dec 2025 23:19:45 GMT  
		Size: 11.7 MB (11674649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcd746617058f714eb36e860853bac5c0d3f77c0e5f14a12f8683dbf2e52b2b0`  
		Last Modified: Mon, 15 Dec 2025 23:19:46 GMT  
		Size: 10.2 KB (10159 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e5f5607b62be37d5a504948447b4ff87f33b0e65bbaf61db0174c661c1e3d294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.9 MB (226889804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7be03514923eb3d0373fd20bd8f39f5818459526791b206ff8cfaa4c5911c79`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 08 Dec 2025 03:13:34 GMT
ARG RELEASE
# Mon, 08 Dec 2025 03:13:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 08 Dec 2025 03:13:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 08 Dec 2025 03:13:34 GMT
LABEL org.opencontainers.image.version=26.04
# Mon, 08 Dec 2025 03:13:39 GMT
ADD file:b61e9f94116cf2f68a6415698661ee2b700e7d672508b7326845bcf886232f85 in / 
# Mon, 08 Dec 2025 03:13:39 GMT
CMD ["/bin/bash"]
# Mon, 15 Dec 2025 20:10:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 15 Dec 2025 21:10:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Dec 2025 21:19:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2bf29d7486c7e629372c92e4748c184d88f0e4e34b33e49f296e9c9c32039dec`  
		Last Modified: Mon, 15 Dec 2025 20:00:53 GMT  
		Size: 31.2 MB (31156573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df541f37757c7ee3123bb95436fe3a3bf9cac7e92450e3a3a87b55d80bf8aee`  
		Last Modified: Mon, 15 Dec 2025 20:10:55 GMT  
		Size: 17.7 MB (17745313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae46f09dc50163ba4eec305ba6b855deff0220e28d3b3422e7a56d10557f4029`  
		Last Modified: Mon, 15 Dec 2025 21:10:42 GMT  
		Size: 51.0 MB (51049819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1945bd0ec101817eef2b4e982b5d555931b607abb3bf3d73d1ad8fa9cf6451f7`  
		Last Modified: Mon, 15 Dec 2025 21:20:20 GMT  
		Size: 126.9 MB (126938099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d9d42534ae3a3ddbb90510af1754fda9487a181e0b76b0b82945b50a62f9cbd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11425769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6216dac96d3a5ef87d2c689abe2e249f9c9110de67d5985138cad5c2f876d1fa`

```dockerfile
```

-	Layers:
	-	`sha256:011d18b188ffaab75a65511948b3d83c07a2c73cbc4bacf9d9c0958620655430`  
		Last Modified: Mon, 15 Dec 2025 23:19:57 GMT  
		Size: 11.4 MB (11415545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a45a012d11e4f9dd159064eeefac8f166cf9eb9721f2702784df50e9cc63e12`  
		Last Modified: Mon, 15 Dec 2025 23:19:58 GMT  
		Size: 10.2 KB (10224 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:390af2688648cbd80a4471818961db3395c7b6f0909831cfe766e9f2647c5094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.2 MB (262220020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37bc030931e53451489aef30badecaf57d5f9072810d70a6a9dfff784e76533f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 08 Dec 2025 03:13:36 GMT
ARG RELEASE
# Mon, 08 Dec 2025 03:13:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 08 Dec 2025 03:13:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 08 Dec 2025 03:13:37 GMT
LABEL org.opencontainers.image.version=26.04
# Mon, 08 Dec 2025 03:13:40 GMT
ADD file:880dc0c9ea14ee504f2d3c0432440022eb7cb1d8e051e9c517689f394260958d in / 
# Mon, 08 Dec 2025 03:13:40 GMT
CMD ["/bin/bash"]
# Mon, 15 Dec 2025 20:10:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 15 Dec 2025 21:10:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Dec 2025 21:16:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0196ed0ac4ca95d4c74a0629deb6468dc9b8d3f3bbe0834d244c1ef7c9bdd8b3`  
		Last Modified: Mon, 15 Dec 2025 20:01:51 GMT  
		Size: 33.3 MB (33300910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40970ea46a6648d5c0acf6872b257eeae96e2929f52e0a4991f153cd5c126ccb`  
		Last Modified: Mon, 15 Dec 2025 20:10:54 GMT  
		Size: 19.0 MB (18953427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d06c4b4a1abaa456ef1a4e4a8a431922173ff3082858910d3b60740353a6d1`  
		Last Modified: Mon, 15 Dec 2025 21:11:09 GMT  
		Size: 48.2 MB (48213000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae046f76d4b7e97969340d0fcc335cc15ae1300a90a546722baf6c684438efb`  
		Last Modified: Tue, 16 Dec 2025 01:34:28 GMT  
		Size: 161.8 MB (161752683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b3c0ff995054a5fce4176079a78bb8fd5ed20b4e9452cc661827b41cecc925ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11739063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2db095ddc469f30d327fe9e53caf428c4d0ffab481c58b6bd442dfdd2464f68`

```dockerfile
```

-	Layers:
	-	`sha256:e600982d8888fa68802fa1a873e10ab21fd7be0898b9dfd374f7be1734e73ee5`  
		Last Modified: Mon, 15 Dec 2025 23:20:08 GMT  
		Size: 11.7 MB (11728823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d576587efeb507daefe22438a752c04f9c2245d2c16f7a00d726d7be6e9d4781`  
		Last Modified: Mon, 15 Dec 2025 23:20:09 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:02c1f867b26e64852d42bea29b6183fd5aa7e28bfc1509fb79f3e36c249d86e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.1 MB (283126713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bd11e16515a03adae9cb1a5bec0d7a150688374b0131e1c898b28e2a14fce0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 08 Dec 2025 03:13:14 GMT
ARG RELEASE
# Mon, 08 Dec 2025 03:13:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 08 Dec 2025 03:13:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 08 Dec 2025 03:13:14 GMT
LABEL org.opencontainers.image.version=26.04
# Mon, 08 Dec 2025 03:13:20 GMT
ADD file:1ba64fcb8425d92e42a4dcd6299abe7ca1abca89c8ada8bca11d7804b715a1b7 in / 
# Mon, 08 Dec 2025 03:13:21 GMT
CMD ["/bin/bash"]
# Mon, 15 Dec 2025 20:10:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 15 Dec 2025 21:10:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Dec 2025 21:21:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:99d2753c6e5d3b5e655cfd1b57108083b422a46cfe597843b023a4e2c7c000bd`  
		Last Modified: Mon, 15 Dec 2025 20:01:29 GMT  
		Size: 38.8 MB (38808598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e9c4708e4fcc9ce73471d9e3d813efeee0cfcd5a8afd3b763ae4d5927a0d5c`  
		Last Modified: Mon, 15 Dec 2025 20:11:35 GMT  
		Size: 21.9 MB (21906882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90b16e5bd388001855f31a9018a7801bc4713e3ed4803e64c0e957a08a7ff85`  
		Last Modified: Mon, 15 Dec 2025 21:11:32 GMT  
		Size: 54.2 MB (54201880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3789d0dbfe128bd8133b025e4e63b9876fafaf6faf0769489b6e03459942534c`  
		Last Modified: Mon, 15 Dec 2025 21:23:20 GMT  
		Size: 168.2 MB (168209353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3e828e54613614b51fd77357c29d150cce7ea87d95153ee300bf1bb06c3f916f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11656594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6adeba69584bc16e9e3ed95dcc13c2aee25dae41faf65969117ad703dca1127`

```dockerfile
```

-	Layers:
	-	`sha256:6a19697b61d69fdfc076ed8c74493ac01626d782090f9cb51a06c305da207521`  
		Last Modified: Mon, 15 Dec 2025 23:20:21 GMT  
		Size: 11.6 MB (11646403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15895dfd358bd29046ef735de45fc1494a5f1d648c7901437d12ad184b963b8d`  
		Last Modified: Mon, 15 Dec 2025 23:20:22 GMT  
		Size: 10.2 KB (10191 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0b64fcf138289ca2f1ff56c488190a484d3397f028fa16ae95c69e22c97899d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 MB (242051691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dfabfd8a08145725bccffe322da86220d8bd732eb6c0d9bab58166474811b9f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 08 Dec 2025 03:12:49 GMT
ARG RELEASE
# Mon, 08 Dec 2025 03:12:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 08 Dec 2025 03:12:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 08 Dec 2025 03:12:49 GMT
LABEL org.opencontainers.image.version=26.04
# Mon, 08 Dec 2025 03:12:51 GMT
ADD file:9d8d73794e21475bdd8f856aa959b4a2af7fda40f696897caf099eefd5628d0b in / 
# Mon, 08 Dec 2025 03:12:51 GMT
CMD ["/bin/bash"]
# Mon, 15 Dec 2025 20:10:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 15 Dec 2025 21:10:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Dec 2025 21:17:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9a53a9f36e89cb17b371244f4700e0e70e68c792d70ffa6f555d0497c602d741`  
		Last Modified: Mon, 15 Dec 2025 19:59:57 GMT  
		Size: 33.4 MB (33395288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32929a90664eb992dfded2cfe05892d67b8b30f3ec5f2a61699955dd20048079`  
		Last Modified: Mon, 15 Dec 2025 20:10:56 GMT  
		Size: 19.9 MB (19882916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d63b6cc2121582b69aaa364c4666d8667029a1d6a0a63422f73b702d28d3d8c`  
		Last Modified: Mon, 15 Dec 2025 21:11:09 GMT  
		Size: 49.4 MB (49415769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2cd0757b68321bab666dbcd922bce0d787fe24573205f0f646b7ad1b6fb60b`  
		Last Modified: Tue, 16 Dec 2025 01:34:18 GMT  
		Size: 139.4 MB (139357718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2c183b94bf028f424060a4694e0358693ef1979e36cd130cf9c39f5a55f4e6dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11459702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2e0320b7fb2389f7664974069d9b89479af95fec0733f55004379b7d9325a8`

```dockerfile
```

-	Layers:
	-	`sha256:d3db7272a584639ea872500af7b04f5a7f503c9473de181b86df7feaa7f362dd`  
		Last Modified: Mon, 15 Dec 2025 23:20:35 GMT  
		Size: 11.4 MB (11449542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e025a81d454c073b766feac4cc869017cf71029b13d96c9c4a1d1c74cc315785`  
		Last Modified: Mon, 15 Dec 2025 23:20:36 GMT  
		Size: 10.2 KB (10160 bytes)  
		MIME: application/vnd.in-toto+json
