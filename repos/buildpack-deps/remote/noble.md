## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:dc1392fc256c152b26b6be30b403a336aa73a464692c5e77944e909b21a85ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:noble` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d576c9d3d2623a662f9147eafcf3d305cab76ea3b2f2811803b7a6ddcc5e6185
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.4 MB (282350393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f5a0bf20163c749546f28feb8c6ea9c5e425f7005702c1c9895d04ae3a6ea23`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:01 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:03 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Tue, 27 Aug 2024 15:55:03 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:44:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 00:45:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 00:47:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:32b824d45c6101d459f5d3c13ab8658b6f79713f3bd64e363d3f6bc98faf5d6d`  
		Last Modified: Tue, 27 Aug 2024 21:43:22 GMT  
		Size: 30.6 MB (30611547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dcdb77dd1cbe00fb13e2a010b7052722035edb06195ac08b57d796617423fef`  
		Last Modified: Tue, 17 Sep 2024 00:51:57 GMT  
		Size: 16.0 MB (16017088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345b5509344fd379350000c7ff7136f4bb9e0907683154a35e01c343d3aaa268`  
		Last Modified: Tue, 17 Sep 2024 00:52:12 GMT  
		Size: 45.5 MB (45477387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51503dd6ffc660c3a5cdfe4907a3f2bb56c131b33c0049777a99c9547d4d33e3`  
		Last Modified: Tue, 17 Sep 2024 00:52:49 GMT  
		Size: 190.2 MB (190244371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7c8158415bfcc472b648151a318932f4cfe044041229bfcc0e1fda10f886e064
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.0 MB (241997040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1dfe2c00f04abf01ce6bafd5fcdf18ba0b4511afa6852b985dbab56398c74d7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:10 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:14 GMT
ADD file:0efc83f80e5e3a9125a702063e487f836d2e0ff9a88f4d0330897d15e445d415 in / 
# Tue, 27 Aug 2024 15:55:14 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:32:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:33:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:36:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3662f20bd36fe3ab5035e3d6d75d4a5a27e32e29abe306052959223600a1522c`  
		Last Modified: Tue, 17 Sep 2024 01:24:15 GMT  
		Size: 27.7 MB (27731977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3107c13260c7e80b038cd95e226c8f255f72cffa548c84603487e7c9533cec`  
		Last Modified: Tue, 17 Sep 2024 01:42:43 GMT  
		Size: 14.6 MB (14560557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b2411b9846cffe86b78ccc0ca0886e65974eebdb17ef941fd0ca8d1eac5aec`  
		Last Modified: Tue, 17 Sep 2024 01:42:59 GMT  
		Size: 49.0 MB (49027219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36b2f4a9e68f9e10270485abad7f4c1e7ec8abeaacfc1ba0fcf30408d609375`  
		Last Modified: Tue, 17 Sep 2024 01:43:26 GMT  
		Size: 150.7 MB (150677287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0e8de3ad24dac6c6cac494b4814e26aef75b307d664b6b2686340d9275cc9028
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.4 MB (271386929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:258dd1dedbe32e7e1ece435c11db9077d0b9a7afcc0b020f4a760a4d2e608478`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:55 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:58 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Mon, 16 Sep 2024 06:23:59 GMT
CMD ["/bin/bash"]
# Wed, 02 Oct 2024 01:07:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:08:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 02 Oct 2024 01:11:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:43cc87cb0cd1fc1c0b6c8670fa2a07f84e6af2cd95bce48b7909b42cca8e5fc1`  
		Last Modified: Fri, 20 Sep 2024 15:05:59 GMT  
		Size: 30.0 MB (29952705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64851f27095916d4936043f696b80bafea7c2e553dcec89f4e806debc7ab7bd1`  
		Last Modified: Wed, 02 Oct 2024 01:18:10 GMT  
		Size: 13.5 MB (13452843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6108651e89a3a91252dddfdeef0ab0fb469fb24f4de592a5944ffec8fb73f0`  
		Last Modified: Wed, 02 Oct 2024 01:18:24 GMT  
		Size: 45.8 MB (45769072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c427e7a315343f68b951b898d838e339e728f26647e6f21415d0406eb721ab29`  
		Last Modified: Wed, 02 Oct 2024 01:18:49 GMT  
		Size: 182.2 MB (182212309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f66db98810f9414a05224f51a825d0fbb520cbf715adcfdb591df4ddda0f3762
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301420056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b56948e3c3a192f7459b0053798fb59c67fcceadccd8d8fe23ee0c53c3e2c2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:56:25 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:56:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:56:28 GMT
ADD file:c70c2393dc0404f71d25ae70ab08b5aa65e46753a6169cfd4f5554c942cc0218 in / 
# Tue, 27 Aug 2024 15:56:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:40:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 00:41:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 00:45:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5d340ed979f83f097fa56590781e2ea4e2d63a50fc75b5e5bc616f845d2e2f80`  
		Last Modified: Tue, 17 Sep 2024 00:53:16 GMT  
		Size: 35.5 MB (35518179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a6e8308dad143a201e728cbfbe6acc7e5b19c74a93209f434931aab40b968f`  
		Last Modified: Tue, 17 Sep 2024 00:53:12 GMT  
		Size: 18.6 MB (18618158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c162e72cd72ec90c41417f91a23cfce5a2b5820e5406899302bfea8ba48237b`  
		Last Modified: Tue, 17 Sep 2024 00:53:33 GMT  
		Size: 50.6 MB (50641952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae8b3d9da5a3b09573aa1743c12128740b6a301436f0d3ba2435ecdef70d9898`  
		Last Modified: Tue, 17 Sep 2024 00:54:10 GMT  
		Size: 196.6 MB (196641767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:963e4ae4e1c3226c12e980267912197fb63345626660613ef58b811c4f68f4b8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.4 MB (332417808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5d16f2a6f41210556fc201c48c67a5f511c7a9bc76cf06d5407ea3b198ea1b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 16:13:45 GMT
ARG RELEASE
# Tue, 27 Aug 2024 16:13:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 16:13:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 16:13:46 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 16:14:17 GMT
ADD file:93d9ee7cf8a421a6d4ab56202ff743dbe7e87beb3d3c9bc1cebb49cf8e1ae4a7 in / 
# Tue, 27 Aug 2024 16:14:20 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 02:10:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 02:13:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 02:19:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7f1cd38a0bd0947977b4bf53d67dbf81507e47c66eadbe86a6ef2edc5df9c038`  
		Last Modified: Tue, 17 Sep 2024 02:36:49 GMT  
		Size: 31.9 MB (31945085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70795db72e869829e9393a7a9859b7d6989d7ba34b48de302c65628b7b96ca5e`  
		Last Modified: Tue, 17 Sep 2024 02:36:39 GMT  
		Size: 16.4 MB (16427708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31ff4b62acbc4050fdf30112f7c0382ff10d99ecdd5fc869c02c029d9a9c27f`  
		Last Modified: Tue, 17 Sep 2024 02:37:51 GMT  
		Size: 53.9 MB (53938921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719620108ad09e130bfae61573bb9a6d67dd3fba2631d277f5c686f678d0247b`  
		Last Modified: Tue, 17 Sep 2024 02:42:18 GMT  
		Size: 230.1 MB (230106094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3ee15b8da1fe9d0464f8361abe248664974bf58e7b2c30af91163c16c5c11ecf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.1 MB (264103990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7fba033f71ab0b7b0282d6e61e7ca416b5fb0948d5b78ae1eb0cfd43c7fbef`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:05 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:08 GMT
ADD file:55ce2834630c73439274688061a6b2ad0d6952c2435dc51250026e14f139275d in / 
# Tue, 27 Aug 2024 15:55:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:21:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:22:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:24:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1ebdf4a84a853f3e1fae6f15bd5f734d2925697002b9b26792d25b2080fac7e6`  
		Last Modified: Tue, 17 Sep 2024 01:29:05 GMT  
		Size: 30.7 MB (30665390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58735d40f4b71b662b627ba6ba6d829f33372bcf38616c587e8193ff9f05294`  
		Last Modified: Tue, 17 Sep 2024 01:29:04 GMT  
		Size: 17.1 MB (17068874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:054f4588e2fa050fc15cddee8730098abc2d2c3a235c7296c6d7d50c4a7b4a36`  
		Last Modified: Tue, 17 Sep 2024 01:29:17 GMT  
		Size: 47.1 MB (47062470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f0c1001912d6749947e8b3ceda12389dbbe49519dcf8a58eeed2137e009fa0`  
		Last Modified: Tue, 17 Sep 2024 01:29:43 GMT  
		Size: 169.3 MB (169307256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
