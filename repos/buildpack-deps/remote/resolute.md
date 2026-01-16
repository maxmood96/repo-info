## `buildpack-deps:resolute`

```console
$ docker pull buildpack-deps@sha256:c125bf04cbd7bca0c81f16480c4a84744c6efb5d582d0672b48f07d745145e73
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
$ docker pull buildpack-deps@sha256:76d60c02eea8d0bffe9116312b486d7d62cf47b860f703c0fc54941e4f6e5d24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.6 MB (227562699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc8a119a2d3715c5b2625400b49cbf5ff20e4f192d2b341398b89318aceb3e1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 06 Jan 2026 16:12:47 GMT
ARG RELEASE
# Tue, 06 Jan 2026 16:12:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 06 Jan 2026 16:12:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 06 Jan 2026 16:12:47 GMT
LABEL org.opencontainers.image.version=26.04
# Tue, 06 Jan 2026 16:12:52 GMT
ADD file:2badcd83b204d640ccedc4ace52673007514f420a84bd8c139cdf292ab0fd3e4 in / 
# Tue, 06 Jan 2026 16:12:53 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:07:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 15 Jan 2026 22:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 15 Jan 2026 23:28:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a9ee0a3989db9dc297303b58491eba6d69952baa6b2827fc54ee64ce18e07032`  
		Last Modified: Thu, 15 Jan 2026 21:43:51 GMT  
		Size: 31.2 MB (31161903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afba882eabc4fb690fa94f15129818fcf2958502ce348f72e1f4978f4fb0a975`  
		Last Modified: Thu, 15 Jan 2026 22:08:16 GMT  
		Size: 17.8 MB (17784528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e787e849e38a2c06b825e1d0dc7a2ac35b36e530488241b0cd53030551589a46`  
		Last Modified: Thu, 15 Jan 2026 22:35:30 GMT  
		Size: 50.7 MB (50699858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c60a3745aea0029daeac7dc9464a0a54de49ff5a90c0e01daa6645af99d12e8`  
		Last Modified: Thu, 15 Jan 2026 23:29:01 GMT  
		Size: 127.9 MB (127916410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:980716e8637414ba224406a03157de07f5432a1682ed642dd0ecbc042ed5fe72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11430784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82fa41577aa4f2af7517af4575470fc0e0248461c507d109c8c3cd8d158a3fab`

```dockerfile
```

-	Layers:
	-	`sha256:0df0eb80c9c69a19ce24e85da7206c23c83b6e1f8a7122aed54ca9996ac1e639`  
		Last Modified: Fri, 16 Jan 2026 02:21:23 GMT  
		Size: 11.4 MB (11420560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70e8a21dc38d39102ebdff5ece344e381566611febed05347ace3b290db2aa65`  
		Last Modified: Fri, 16 Jan 2026 02:21:24 GMT  
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
$ docker pull buildpack-deps@sha256:82ce5450420248246ebd8463f4e883daaf88dd5ba382a803b009f7e5d545df29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.6 MB (241575223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c043265394b231cd35e3f2e63493f0fc50124fdbec848736c2b26126f3651023`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 06 Jan 2026 16:12:54 GMT
ARG RELEASE
# Tue, 06 Jan 2026 16:12:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 06 Jan 2026 16:12:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 06 Jan 2026 16:12:54 GMT
LABEL org.opencontainers.image.version=26.04
# Tue, 06 Jan 2026 16:12:55 GMT
ADD file:9266e4011fb5ad8a3df9e390fc8165ed1fd44560192a8470907993912a77df90 in / 
# Tue, 06 Jan 2026 16:12:55 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:06:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 15 Jan 2026 22:46:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 15 Jan 2026 23:34:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f779d014bea281c13f5bd15e791164db36f27117b06bcc6a0832c49e20ca6c3f`  
		Last Modified: Thu, 15 Jan 2026 21:56:50 GMT  
		Size: 33.4 MB (33397954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66829f85ee6a4ac10cb285e12e8d836204a87759cfb752c0e2b65010651a3b0f`  
		Last Modified: Thu, 15 Jan 2026 22:06:49 GMT  
		Size: 19.9 MB (19947648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00ffb09829df0d3df34b27f7b2ec620dde52eb10796d930fa7f7a852d0ed178`  
		Last Modified: Thu, 15 Jan 2026 22:47:24 GMT  
		Size: 49.0 MB (49048827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb9bf8b30164b2679272d12502f081a0a0a0b4a9c65b4b9172bf619397046c5`  
		Last Modified: Thu, 15 Jan 2026 23:36:59 GMT  
		Size: 139.2 MB (139180794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:83007234cc1538df42015e21c188462f10d89976951c35c932fce7c2e8a0c8a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11464717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4304bcbf9bdbf833f5159eddf7ed22c8ddfd42dc14fe72164e5c65070f79a163`

```dockerfile
```

-	Layers:
	-	`sha256:8c40a5082b2435bff849fc7b3d0f631fdc2d3d34802fa3f6dbe2501744821319`  
		Last Modified: Fri, 16 Jan 2026 02:21:58 GMT  
		Size: 11.5 MB (11454557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76b848637ee36ea5fc1f5a6332da887545e53b7311c10d3cc1530f064a783dd8`  
		Last Modified: Fri, 16 Jan 2026 02:21:59 GMT  
		Size: 10.2 KB (10160 bytes)  
		MIME: application/vnd.in-toto+json
