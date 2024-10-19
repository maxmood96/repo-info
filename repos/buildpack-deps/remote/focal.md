## `buildpack-deps:focal`

```console
$ docker pull buildpack-deps@sha256:16c8ccb9a9ee899900267a9d981999b01006d3ed892b23916fef75a7671cb56a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:focal` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:ee54563d3336ac7f3c376662be0735333f0859b8cdd8ef4e2f5eab7de3d5e936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244516542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547baaa4a2e93c2a23bf004443f3d933e4dc70ac89856c1e7c914c091832cf87`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c439405a1dd88c17c6ae4e1c05d5c4a282f8957203f506a1d3b8c0b018b66b3`  
		Last Modified: Sat, 19 Oct 2024 02:06:13 GMT  
		Size: 11.1 MB (11147032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841fed924c2a2b74fd07c670509feadf6fc8830b3356a2ad22a1066d9c45c02d`  
		Last Modified: Sat, 19 Oct 2024 02:52:27 GMT  
		Size: 60.9 MB (60925550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cacc106c739550fd7621a1d278bdf3aa771e4c8f58721002b6f8649a68efde`  
		Last Modified: Sat, 19 Oct 2024 03:53:22 GMT  
		Size: 144.9 MB (144932900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:focal` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:10d5ec4689716563ebaa051df0a345ce725d398439aa848ce7b085f0e780bb9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12289578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7752ea622fce61ec1985ddd51d16d5de58848de3045dc12da492a2940f8318a2`

```dockerfile
```

-	Layers:
	-	`sha256:8c82922d7ed03225c05653afc2c2926c740c832136083b7b77c59aca67cc9265`  
		Last Modified: Sat, 19 Oct 2024 03:53:20 GMT  
		Size: 12.3 MB (12279374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79fc481476bd9710b015115f3ec2d0b79c613673fa5e6c9902fb043e8f866b74`  
		Last Modified: Sat, 19 Oct 2024 03:53:20 GMT  
		Size: 10.2 KB (10204 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:focal` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:88b014d36a585fc80c03c18e81db498ea6a2cc8fe63f6b7970d50988fec1b4e9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212086395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86181f7988f85f5bb0e8890430b79aeffb7e6799ea4f8b6d4d8b724c70807692`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:34 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:34 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:36 GMT
ADD file:f76c848564adfa0c782654cd9423feee0ffacccd95abfe3e4e696203d5e61fbf in / 
# Fri, 11 Oct 2024 03:38:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:17:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 01:18:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 01:22:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7474977cdbc1bb838c947dfdfa420a17f877727196fdf929b5bbfb57ddc59d1e`  
		Last Modified: Wed, 16 Oct 2024 01:27:36 GMT  
		Size: 24.6 MB (24600743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf94ef511a5b70086da0dbde4b10efbb6a0a474eca153a011c1115ac2c3f095`  
		Last Modified: Wed, 16 Oct 2024 01:27:35 GMT  
		Size: 9.6 MB (9621768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85418fe461856e419c5868f0e9e1f96a4ed78b150102e641b5fe7857f36a3313`  
		Last Modified: Wed, 16 Oct 2024 01:27:55 GMT  
		Size: 55.9 MB (55883691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cca2489adff278a53195ce381982f82039209fff1b3e492c207cbd9ec073277`  
		Last Modified: Wed, 16 Oct 2024 01:28:21 GMT  
		Size: 122.0 MB (121980193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:495b6b4d58f94e94d1f22015d0d249c9649095a7d063b32c736fb2c916e42eef
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236095150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:496889ddbe9850404c3f52ea7b95ad2db7ab56a92d8207750b740ac4cb3f4b3f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:21:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 01:22:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 01:24:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:963ceec6c2ca13b343a25d3157e3e30ffa80fc297ad5e3f78d8f43087427b2d3`  
		Last Modified: Sat, 12 Oct 2024 07:30:30 GMT  
		Size: 27.2 MB (27204259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a26dece8dd0e19868776e664f1845a9814a1f9f8561192d9ab9bb201f219e88`  
		Last Modified: Wed, 16 Oct 2024 01:29:52 GMT  
		Size: 11.0 MB (10993345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39f9d5b8d7b30e36de2e9aeed0f6ae96330e08473b8c9f609ca57f6740ef24e`  
		Last Modified: Wed, 16 Oct 2024 01:30:06 GMT  
		Size: 61.1 MB (61064176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25fc637cf2bf691076a7a288a69201040457239da81e7cfa38e752d8622d5e25`  
		Last Modified: Wed, 16 Oct 2024 01:30:27 GMT  
		Size: 136.8 MB (136833370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4c0550be955c837b134542411a398204029bf53e6f9e0d51f27dcb45967c7ed9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269572199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06cc7ca3bc451a92d9dfefa590dfafe32c7d5c7bab50dc881759093991b06d91`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:35 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:38 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Fri, 11 Oct 2024 03:38:39 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:50:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 01:51:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Oct 2024 01:55:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d534431b5b1c76e43335aa792bdca680eb5ebbeaeea07c6eeae4aa9d2cb8e841`  
		Last Modified: Wed, 16 Oct 2024 01:44:06 GMT  
		Size: 33.3 MB (33315666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5ceded1fb62333ad13f625f4b106d80d9b82c064bbf2410811567d29993427`  
		Last Modified: Wed, 16 Oct 2024 02:01:05 GMT  
		Size: 13.0 MB (12963181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cea2472a450c114a5052b42d3fc38c28fdfc12a3ef4b6aae683f81aa37195d`  
		Last Modified: Wed, 16 Oct 2024 02:01:25 GMT  
		Size: 69.7 MB (69663815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b651cb541d90efde7531c763c124c010c282b207cdf55a59cd980b277c39b96`  
		Last Modified: Wed, 16 Oct 2024 02:01:57 GMT  
		Size: 153.6 MB (153629537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:78234a5a1dc90d47e4c99ba0dc51825f68de33f2ce7d33ee21849f4706fe74f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.8 MB (225760717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ac61a5e7ed525ed26aa28473663586e05df887b6ee5b12788ca94c5cfdbd32f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:e3e9bad1c3576edf8ddea2dd7af2ed8ecac1ad0b15d714dd9c51f679d44d13b6 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f6b14778eb4fed5cbb0bd80eea19d48526571f3b2dfa0196faf63f42fdb8c6c2`  
		Last Modified: Fri, 11 Oct 2024 04:41:53 GMT  
		Size: 26.4 MB (26365979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178338141fcd63fb07a3b3174480acba6d71f4005370e73b64d2d0aa4c75dd76`  
		Last Modified: Sat, 19 Oct 2024 03:49:50 GMT  
		Size: 10.7 MB (10704103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848ffcc86defea840ce0480def4a0552dc82be2b64b587e49f72509940010a27`  
		Last Modified: Sat, 19 Oct 2024 05:10:43 GMT  
		Size: 60.4 MB (60355097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb26afbf296e69771173336d5e5b1a3d04b47a55e49a9044de1331f73fbe922a`  
		Last Modified: Sat, 19 Oct 2024 06:55:39 GMT  
		Size: 128.3 MB (128335538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:focal` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d0d954ba3a57a572f5ba18ae37b08a116b3604463dc304933b5af60df5b9de8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12125870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752abc34e6cceae583c78429c3395ceb1addbaec18966dbfd5c5a24331ce8111`

```dockerfile
```

-	Layers:
	-	`sha256:5f0c3a664f674e453ad5b29ae0a2eea27950019ac3f535cc546009db161f939b`  
		Last Modified: Sat, 19 Oct 2024 06:55:38 GMT  
		Size: 12.1 MB (12115665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0066639bb9117f720d9cd195f96f19ee4a1ffff0f87443b655ba184d55d31412`  
		Last Modified: Sat, 19 Oct 2024 06:55:37 GMT  
		Size: 10.2 KB (10205 bytes)  
		MIME: application/vnd.in-toto+json
