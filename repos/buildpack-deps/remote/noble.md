## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:5242dcb771eb171714f3892436bc9a9cb534a4b6d7481e10ca7ea62a3ed84b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:noble` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:333917f6aa55aaa103d0b78bbb3743bda393e7d317bbcd3b1deb0f8b72031234
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.9 MB (323857558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01879effe0ec199729157e81f7d45cd0a74546be873c66d59fa0a688098b10f6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:51:33 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:51:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:51:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:51:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:51:35 GMT
ADD file:5fdfd910138ea9c55567565b4159698866331e2e19eacecb4cc9d14a337e4e72 in / 
# Mon, 12 Feb 2024 04:51:35 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 03:34:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 03:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 03:38:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f97f48cbc0b07925817eb987f4aad620bb8746b88171a7a78a9eb70c056a1f16`  
		Last Modified: Fri, 16 Feb 2024 03:40:13 GMT  
		Size: 30.4 MB (30383550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43159cd89f554b8b5218ce69e51f6de33a8670c302dbb8da0845c7ccabc7862b`  
		Last Modified: Fri, 16 Feb 2024 03:40:11 GMT  
		Size: 13.7 MB (13726943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf161ff7600e7b7c16f6ede46503033c3e73c9937f61e69002cd9d251df0d55d`  
		Last Modified: Fri, 16 Feb 2024 03:40:29 GMT  
		Size: 48.1 MB (48138649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70b23ce13f84812ac6df1bc6603b609b4098273dd0ead57baadb72855d6221e`  
		Last Modified: Fri, 16 Feb 2024 03:41:09 GMT  
		Size: 231.6 MB (231608416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fa0bb130944677fedf59a198ccb7adaa49f87ffa5ad3972acac42b8586258b44
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.2 MB (276226502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba87b96a8fa9144b6aba6687ad2685b46eb6993268141e6bc72a3d3e37ec5495`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:22:39 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:22:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:22:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:22:39 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:22:42 GMT
ADD file:1a0a51108f4f8e0b235f7272452d282ea13f08d47f16682fe7692f82c4257d18 in / 
# Sat, 27 Jan 2024 16:22:42 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:04:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:05:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:08:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ac0f5659d9dfd5db0bb4d4c61abc9180fe37bd866eee19911008c648d692a0c4`  
		Last Modified: Fri, 02 Feb 2024 00:12:28 GMT  
		Size: 27.6 MB (27601561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecef6eb383bc18ee41099cc94d04bbad13554a3011ca70d490e046952db78372`  
		Last Modified: Fri, 02 Feb 2024 00:12:25 GMT  
		Size: 13.0 MB (13032633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23569f813ab6f239b230aecd3b3f680f19a5269e8d75eac5b6d08abd958163a8`  
		Last Modified: Fri, 02 Feb 2024 00:12:44 GMT  
		Size: 49.6 MB (49588838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1ed75b166e905752a38b944cb766ce6506c1a4818a659a1aa29515dd527221`  
		Last Modified: Fri, 02 Feb 2024 00:13:19 GMT  
		Size: 186.0 MB (186003470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3eb16e62a071ad7d3fbfb73ff07a3b096b1c2c571d070f55b85d58845aab17e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310487016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b7904e60519f5b1814dc03ad696849afbcf4f3d3f4067def614e910e5d0c0ad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:52:06 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:52:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:52:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:52:07 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:52:09 GMT
ADD file:3ba739169a5d008e9474d4e0f02a874840e759fe8dd36ae68a5ccd1040648941 in / 
# Mon, 12 Feb 2024 04:52:09 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 04:43:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 04:44:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 04:48:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5ddf3e3c3a3f4a7084396c5fea9e867258a287407252e406f4a47f9c57c7e768`  
		Last Modified: Fri, 16 Feb 2024 04:50:22 GMT  
		Size: 29.6 MB (29634636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a510494515f4fe176171eb81a58eb13a7d968c4fd55af5da54ea2b1236d850`  
		Last Modified: Fri, 16 Feb 2024 04:50:20 GMT  
		Size: 13.5 MB (13520137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9e7554008f9b077a355c6245831eea73ea7b69335b673b117960e3985c652e`  
		Last Modified: Fri, 16 Feb 2024 04:50:36 GMT  
		Size: 48.2 MB (48184820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f65f1329b9a04f2040322eb6419b9f931ac6ee4a673b814acd7de474c173abf`  
		Last Modified: Fri, 16 Feb 2024 04:51:08 GMT  
		Size: 219.1 MB (219147423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:09a3d9ffff8cb8fdd1181b970e6046cca6735a0d5b0933ab4d6045e0c2af885c
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340724194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83974ad154d44a698b0ba4385d07ef05492680f6befddac8e570e401d04c518c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Feb 2024 04:54:47 GMT
ARG RELEASE
# Mon, 12 Feb 2024 04:54:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Feb 2024 04:54:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Feb 2024 04:54:47 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 12 Feb 2024 04:54:50 GMT
ADD file:52a2f480522705b01ec516237a34993e5cb661cbb9082d50ffeb08b7f467770b in / 
# Mon, 12 Feb 2024 04:54:51 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 04:03:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 04:05:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 04:11:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2f99e65953eb4c26f66aa6a038cad2127b130e0857531898f0345de4a7c7c967`  
		Last Modified: Fri, 16 Feb 2024 04:14:18 GMT  
		Size: 35.2 MB (35220719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85838c27b62b5d20ff7b908b2b786d1db23180ebd001f5af468413763f01c9c0`  
		Last Modified: Fri, 16 Feb 2024 04:14:12 GMT  
		Size: 16.0 MB (16037692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5962258c49518f24fa86ea6b63115900e0009f9793322227c39a561cacb6ace3`  
		Last Modified: Fri, 16 Feb 2024 04:14:38 GMT  
		Size: 53.6 MB (53572182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760e1a5aaa7d979936307c88cefa9024fdd1430b8041cf9ce8e9725e565fdac0`  
		Last Modified: Fri, 16 Feb 2024 04:15:24 GMT  
		Size: 235.9 MB (235893601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:22ba22df087f3d536bb0160362250138599e72dd805fe47efaa3cdc9fdd3a2eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302078922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef314acfdcd07bfec6ee6997dd3fe06950037a6a65cb86356bf49db81315235`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:15:37 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:15:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:15:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:15:37 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:15:39 GMT
ADD file:7dd6a1a2ef765af3feba0e026e0d3c5c0d1793c106b572fe316a5265d8f715b6 in / 
# Sat, 27 Jan 2024 16:15:39 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:24:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:26:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 01:29:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:613ff254a56e5e32a5cef69ec3d0423f8c34e54c150269e6d7b755b5d2aa8515`  
		Last Modified: Fri, 02 Feb 2024 01:35:43 GMT  
		Size: 30.3 MB (30319501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeecfce9669b97c510f67dd6aa25593fbd474c1d056f87af305f67daca9644de`  
		Last Modified: Fri, 02 Feb 2024 01:35:41 GMT  
		Size: 14.9 MB (14928513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850e1ed4384dfa6da051412846b24fc4182a18620863cd54092878378deef24d`  
		Last Modified: Fri, 02 Feb 2024 01:35:55 GMT  
		Size: 46.9 MB (46863566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f00c13f803446bd9774a13fd2849578bf70c1892b6e4afc4fe0056f8a85639eb`  
		Last Modified: Fri, 02 Feb 2024 01:36:27 GMT  
		Size: 210.0 MB (209967342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
