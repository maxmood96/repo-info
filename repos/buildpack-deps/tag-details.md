<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `buildpack-deps`

-	[`buildpack-deps:20.04`](#buildpack-deps2004)
-	[`buildpack-deps:20.04-curl`](#buildpack-deps2004-curl)
-	[`buildpack-deps:20.04-scm`](#buildpack-deps2004-scm)
-	[`buildpack-deps:22.04`](#buildpack-deps2204)
-	[`buildpack-deps:22.04-curl`](#buildpack-deps2204-curl)
-	[`buildpack-deps:22.04-scm`](#buildpack-deps2204-scm)
-	[`buildpack-deps:24.04`](#buildpack-deps2404)
-	[`buildpack-deps:24.04-curl`](#buildpack-deps2404-curl)
-	[`buildpack-deps:24.04-scm`](#buildpack-deps2404-scm)
-	[`buildpack-deps:24.10`](#buildpack-deps2410)
-	[`buildpack-deps:24.10-curl`](#buildpack-deps2410-curl)
-	[`buildpack-deps:24.10-scm`](#buildpack-deps2410-scm)
-	[`buildpack-deps:bookworm`](#buildpack-depsbookworm)
-	[`buildpack-deps:bookworm-curl`](#buildpack-depsbookworm-curl)
-	[`buildpack-deps:bookworm-scm`](#buildpack-depsbookworm-scm)
-	[`buildpack-deps:bullseye`](#buildpack-depsbullseye)
-	[`buildpack-deps:bullseye-curl`](#buildpack-depsbullseye-curl)
-	[`buildpack-deps:bullseye-scm`](#buildpack-depsbullseye-scm)
-	[`buildpack-deps:curl`](#buildpack-depscurl)
-	[`buildpack-deps:focal`](#buildpack-depsfocal)
-	[`buildpack-deps:focal-curl`](#buildpack-depsfocal-curl)
-	[`buildpack-deps:focal-scm`](#buildpack-depsfocal-scm)
-	[`buildpack-deps:jammy`](#buildpack-depsjammy)
-	[`buildpack-deps:jammy-curl`](#buildpack-depsjammy-curl)
-	[`buildpack-deps:jammy-scm`](#buildpack-depsjammy-scm)
-	[`buildpack-deps:latest`](#buildpack-depslatest)
-	[`buildpack-deps:noble`](#buildpack-depsnoble)
-	[`buildpack-deps:noble-curl`](#buildpack-depsnoble-curl)
-	[`buildpack-deps:noble-scm`](#buildpack-depsnoble-scm)
-	[`buildpack-deps:oldstable`](#buildpack-depsoldstable)
-	[`buildpack-deps:oldstable-curl`](#buildpack-depsoldstable-curl)
-	[`buildpack-deps:oldstable-scm`](#buildpack-depsoldstable-scm)
-	[`buildpack-deps:oracular`](#buildpack-depsoracular)
-	[`buildpack-deps:oracular-curl`](#buildpack-depsoracular-curl)
-	[`buildpack-deps:oracular-scm`](#buildpack-depsoracular-scm)
-	[`buildpack-deps:scm`](#buildpack-depsscm)
-	[`buildpack-deps:sid`](#buildpack-depssid)
-	[`buildpack-deps:sid-curl`](#buildpack-depssid-curl)
-	[`buildpack-deps:sid-scm`](#buildpack-depssid-scm)
-	[`buildpack-deps:stable`](#buildpack-depsstable)
-	[`buildpack-deps:stable-curl`](#buildpack-depsstable-curl)
-	[`buildpack-deps:stable-scm`](#buildpack-depsstable-scm)
-	[`buildpack-deps:testing`](#buildpack-depstesting)
-	[`buildpack-deps:testing-curl`](#buildpack-depstesting-curl)
-	[`buildpack-deps:testing-scm`](#buildpack-depstesting-scm)
-	[`buildpack-deps:trixie`](#buildpack-depstrixie)
-	[`buildpack-deps:trixie-curl`](#buildpack-depstrixie-curl)
-	[`buildpack-deps:trixie-scm`](#buildpack-depstrixie-scm)
-	[`buildpack-deps:unstable`](#buildpack-depsunstable)
-	[`buildpack-deps:unstable-curl`](#buildpack-depsunstable-curl)
-	[`buildpack-deps:unstable-scm`](#buildpack-depsunstable-scm)

## `buildpack-deps:20.04`

```console
$ docker pull buildpack-deps@sha256:1a40dd9495bc10ecfa6b69e15a1da148b54c00ab0f1b24adc2f26881947ab0f2
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

### `buildpack-deps:20.04` - linux; amd64

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

### `buildpack-deps:20.04` - unknown; unknown

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

### `buildpack-deps:20.04` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:40083431ca62c9c4dc7354235efc7e8a272de74d3cad4ffe2efd08ecd5029363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210863816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:874eb12226c1dad0ceed95327494dc99847c16fe906f23654b5d83dba771022c`
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
ADD file:f76c848564adfa0c782654cd9423feee0ffacccd95abfe3e4e696203d5e61fbf in / 
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
	-	`sha256:10b337d353b3ceaf6823ab2d8696989401feed741b22eb313c8a0cd378762d39`  
		Last Modified: Fri, 11 Oct 2024 04:41:36 GMT  
		Size: 23.6 MB (23620412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961fa3ee3eee16522e395458be87f5269ec5b27ec4fcb4d916faeb1068afaba7`  
		Last Modified: Sat, 19 Oct 2024 06:42:29 GMT  
		Size: 9.6 MB (9620727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a338f01587f18e017e42cf3dfc75e5bd303749299cb0e64ea2a2a0865922d2`  
		Last Modified: Sat, 19 Oct 2024 08:17:06 GMT  
		Size: 55.9 MB (55881822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483891405091050bef8215a64be70ff765bb19eee55901429b24ee283116d3b7`  
		Last Modified: Sat, 19 Oct 2024 10:31:06 GMT  
		Size: 121.7 MB (121740855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:20.04` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:93efc80be5ecab52a464d9fe7ee867901486937a09303516dfaefe6856243530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12105240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc243d6b55f7a192331109744e9df94b733026d4e2e155b63e40f6f0260451c`

```dockerfile
```

-	Layers:
	-	`sha256:a3dfa5079336624661fb047c1126818aed138720d84626c43c7747288cdc7e20`  
		Last Modified: Sat, 19 Oct 2024 10:31:03 GMT  
		Size: 12.1 MB (12094977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e0a3efb0dd55efc5a6fa32017808ac86585ba4027123cba07c6d7a58dc3cd9e`  
		Last Modified: Sat, 19 Oct 2024 10:31:03 GMT  
		Size: 10.3 KB (10263 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:20.04` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d4c044d8e0f1effba941cff238b571cfeb2e4a19ef48e834457abf6cdc14e429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234622538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec51c60e90612793ad7dd898106f7378adf3b78ee245ebece43e8a95fedc228`
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
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a902a6ffa3ee5a0c3f67d06b1a3bb3611210a02b2f2878ae8c1ba1419d989ce1`  
		Last Modified: Sat, 19 Oct 2024 05:21:18 GMT  
		Size: 11.0 MB (10992039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974843836b66b5df8f55da9465dfaca000af6e2d0abe0b8f6cf9013fb718f2c3`  
		Last Modified: Sat, 19 Oct 2024 06:23:32 GMT  
		Size: 61.1 MB (61058312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa0b091012b7f1d636c962fb0be5c5cc11429d7830d5e6b97c54b6d42ef9e875`  
		Last Modified: Sat, 19 Oct 2024 12:40:50 GMT  
		Size: 136.6 MB (136598359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:20.04` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:081e8fe779a686657480a819933b8e270cc9d4a9ed0057fea740342d5b1f93d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12294104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741bd60f669b009e3e0a4062ca49f681e688e44817deffa24b9007acdbd2d06b`

```dockerfile
```

-	Layers:
	-	`sha256:5a19cb8bb2ddaa8e4f7f6306c58bc420202117bf5f4953c8266fc40becfde627`  
		Last Modified: Sat, 19 Oct 2024 12:40:48 GMT  
		Size: 12.3 MB (12283819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8c2a0daf3e80482a28ac6ff19751369ba0d8a59de020a210728c4c86666bbf3`  
		Last Modified: Sat, 19 Oct 2024 12:40:47 GMT  
		Size: 10.3 KB (10285 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:20.04` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ee2a5a58c33e111cce242e157196083fad8519580932bafb9f60fc1c7d30b42f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.1 MB (268105351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3117badda098ded0d13268050fc8f6f7a49dc25190131f2ce1a2f161da37e01d`
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
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
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
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e03dda56aeda86639422183ec93ff76ae68820943e9c534c079867713065a4`  
		Last Modified: Sat, 19 Oct 2024 04:11:36 GMT  
		Size: 13.0 MB (12961183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3475eebae315fac14d1638f5f55a0781ae70edd29e02e2525f0f7f09c1dc89ad`  
		Last Modified: Sat, 19 Oct 2024 05:26:29 GMT  
		Size: 69.7 MB (69663215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e33a43aa68ef75c0c7f240422932e3091598ee81550af17d6083e9a5023cb5`  
		Last Modified: Sat, 19 Oct 2024 13:55:28 GMT  
		Size: 153.4 MB (153404447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:20.04` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c611eff47846c518010eca80d80d699ba66b52f8c53f95ece158a4ea61414de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12262058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd084947b42c1e302e6ec2e560ca6f80266cafe8f3d7aeab6bfade07cbcec2e0`

```dockerfile
```

-	Layers:
	-	`sha256:d51c35d85c5aeff236489fab5d3e8a4884636f3d091cea2a6eafedca79a9c924`  
		Last Modified: Sat, 19 Oct 2024 13:55:24 GMT  
		Size: 12.3 MB (12251821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbe51e9d84b971b16202ed46c5eac6475dcfae44ad6bf132ddc4f5014dc023aa`  
		Last Modified: Sat, 19 Oct 2024 13:55:24 GMT  
		Size: 10.2 KB (10237 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:20.04` - linux; s390x

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

### `buildpack-deps:20.04` - unknown; unknown

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

## `buildpack-deps:20.04-curl`

```console
$ docker pull buildpack-deps@sha256:4da6b2ff6ddf2c4364d0236b0a6fee455f768788ece240518c756ff7d4b06a8c
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

### `buildpack-deps:20.04-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0422293bc781517a1205b2ba6dff7ba236217c9327f8af92e264ba52f93484b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38658092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90edfc157d0d40a2b2be22d1471c22b1abd30fce2d83cc55b4f3927fd7a3f52a`
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

### `buildpack-deps:20.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:116a19e525bb1d8197b26528a2b5ef7fedd9b8d08d42e8f0a74b5f58b28976fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3060155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef3471432bdf86cd7eed5ee88b82b6d4f8bfa3b8b7fdcce6c6319530cd28365`

```dockerfile
```

-	Layers:
	-	`sha256:304c699502debcf5c70a97fb9fb35a4238f59c74a383b028c33d0138d0244daa`  
		Last Modified: Sat, 19 Oct 2024 02:06:13 GMT  
		Size: 3.1 MB (3053230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0ad0bc1951b5669a88f7481c27f808527008c18d6b05fcf4e25e2ac39fadc42`  
		Last Modified: Sat, 19 Oct 2024 02:06:13 GMT  
		Size: 6.9 KB (6925 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:20.04-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0fdf25a37e79618b2acc9d2ffc3b5a1bd46effc5727538657c57796d88900e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 MB (33241139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7921c1e13d1125fcc881dee683609e7270392d779373f4b9fbddc619310ac41f`
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
ADD file:f76c848564adfa0c782654cd9423feee0ffacccd95abfe3e4e696203d5e61fbf in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:10b337d353b3ceaf6823ab2d8696989401feed741b22eb313c8a0cd378762d39`  
		Last Modified: Fri, 11 Oct 2024 04:41:36 GMT  
		Size: 23.6 MB (23620412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961fa3ee3eee16522e395458be87f5269ec5b27ec4fcb4d916faeb1068afaba7`  
		Last Modified: Sat, 19 Oct 2024 06:42:29 GMT  
		Size: 9.6 MB (9620727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:20.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:94a31eb3318b611219d30a7394399d37e3208fcd20b753ee6afab05d21c37424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3062470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c57bae5f7f4ebbacc3f176472d95468cc7f460acc61b103e42637be1d2f6bdb`

```dockerfile
```

-	Layers:
	-	`sha256:7c2ec0cb6889c0b75216697a3f1ce6e08b6d61ffbb3a957ab4bfb07b47fe8bb9`  
		Last Modified: Sat, 19 Oct 2024 06:42:28 GMT  
		Size: 3.1 MB (3055486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c797b5ccbd5650ce46791a1edf2868f666be13330d6821a02488a65487ca39bd`  
		Last Modified: Sat, 19 Oct 2024 06:42:28 GMT  
		Size: 7.0 KB (6984 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:20.04-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9d491d90c508287b19fbdd3b93681f83acebbef4632d594cb41d9ebf722f3e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36965867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44cef15a32fbc51f174b3570e4b8be2e24c07a196b0466fc546b6e5fe1d74c02`
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
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a902a6ffa3ee5a0c3f67d06b1a3bb3611210a02b2f2878ae8c1ba1419d989ce1`  
		Last Modified: Sat, 19 Oct 2024 05:21:18 GMT  
		Size: 11.0 MB (10992039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:20.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ecaa54a4ed8a3abf2a0edd2e615be9a8e18fdb4eb9bc0b91d0afb8d2c4926720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3060481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7add9cc6fef9939e1897cc36b8fe6321415b509c213759804a5480ab813bba2`

```dockerfile
```

-	Layers:
	-	`sha256:b992674687c31519661dd0d849a6ad5bb284cd8612dff3f15d0b802fe207fd72`  
		Last Modified: Sat, 19 Oct 2024 05:21:17 GMT  
		Size: 3.1 MB (3053476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d1ca8e8e16915ab9608c16690a682d2d645bd137d2fbc137b9329b2bb15901e`  
		Last Modified: Sat, 19 Oct 2024 05:21:17 GMT  
		Size: 7.0 KB (7005 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:20.04-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9810120f0cd96478e176022922fd783e953c80d776219d0319c2ae20c9813916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45037689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96261e974791e765a0357ae79f5e219bb3cd323acab789ba9da04094be5a8c5`
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
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e03dda56aeda86639422183ec93ff76ae68820943e9c534c079867713065a4`  
		Last Modified: Sat, 19 Oct 2024 04:11:36 GMT  
		Size: 13.0 MB (12961183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:20.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c64242d8de1d7656fc9862aa1d77468227bf5bf5c630ef1bc407704a9d977e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51db9f907e8c6d21692c40ac2aa42d785ec63653e6c18cbad0ae4e8f7682939f`

```dockerfile
```

-	Layers:
	-	`sha256:9fb29c41083da621d5ef8abe6da2303447585e7fb9d9e85676cf0583d168977e`  
		Last Modified: Sat, 19 Oct 2024 04:11:36 GMT  
		Size: 3.1 MB (3057665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd60afd512ca4047963ff916bc36024a260432f1f636a594eb480fa5cce35737`  
		Last Modified: Sat, 19 Oct 2024 04:11:35 GMT  
		Size: 7.0 KB (6957 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:20.04-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:c8428cf20044f6bc7409d9e28f1f66af5a3e7da17b81a9e33554bad3cb05a08a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.1 MB (33108292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2542a60b19a8a9a3b537e38fea15b2986fd1acdda726099843dd377022fbb1ad`
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
ADD file:f99ddac77e3940392223df513cab07fbc1fbae5269b21e7c49c63c99a7e47b14 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cdd35cb9ddeba9facdedc5a699ecb5f7e1e084b8cdfda59220bfd27ee7a2023a`  
		Last Modified: Fri, 11 Oct 2024 04:41:48 GMT  
		Size: 23.5 MB (23470304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3f7a8397059fca09a3b841b9b47ad382922b9b774e3da80dd14524248ab160`  
		Last Modified: Sat, 19 Oct 2024 04:02:45 GMT  
		Size: 9.6 MB (9637988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:20.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cd36506002bf14a5d00dc790fb57726443f5d21a5e4072e23d81a30faea8514f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3054237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2541cc0782b841d64b43fef60fc0de23e4676b09303756460d023d68b65d66`

```dockerfile
```

-	Layers:
	-	`sha256:43b403be2044cbef0569ac19158e5464762dad979d77e66171d808e34b1a96b0`  
		Last Modified: Sat, 19 Oct 2024 04:02:45 GMT  
		Size: 3.0 MB (3047281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e64e18cf52baacada1162860503b13cb0e61e70b5fc9a412874df2b2d252d6e9`  
		Last Modified: Sat, 19 Oct 2024 04:02:44 GMT  
		Size: 7.0 KB (6956 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:20.04-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6d0ac57e34e6bb9d9f6259248550710cd0058623e7e4ca78ab46b4192a2036c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37070082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f3ea841ac59ea4fbf46c6347106c6e25a2a0316de2c94b17e90eb9502ee05f`
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

### `buildpack-deps:20.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:84a2fd64d7421f9b58a38571d28640279ccf14b90c6610534fe2567eedfd7b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3061576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45953e26d9d11711c42489b08452279cdaf4d825d7d523cc54abd4e2f9dfd947`

```dockerfile
```

-	Layers:
	-	`sha256:5a3bfaf8e95468b6c63311e69ff1e42dfa9bd4cec20c212644f34d10aa625abe`  
		Last Modified: Sat, 19 Oct 2024 03:49:50 GMT  
		Size: 3.1 MB (3054651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a772f47e4c62792ece737b5a02011c8d96e4cbfbe9b8c37fedd7ee037d285a6f`  
		Last Modified: Sat, 19 Oct 2024 03:49:50 GMT  
		Size: 6.9 KB (6925 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:20.04-scm`

```console
$ docker pull buildpack-deps@sha256:5308dfd69986e614671317b78b8ad45eb8bcb97f72afad03eb557428a11526e1
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

### `buildpack-deps:20.04-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:34d00f41b14c40e6903e630fb94b859f9e05c36b7016df768ccfa1791d797151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.6 MB (99583642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e735b8910a6f0ef6d4a756b8614bd1c6fa2d31394533387b293ca533eae4490`
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

### `buildpack-deps:20.04-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5a367f3106529937f6d37be0ae11abc812d3e24785307e1385173da9994b8b50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6680317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad62135b54e4b9715fb84ab88175f2b45bd6498a4d542e12d0ccacdd3ff1cad2`

```dockerfile
```

-	Layers:
	-	`sha256:222103d54b5ac8552ee50b42ecb802826506750cb0de3b1f27df69091e2249e8`  
		Last Modified: Sat, 19 Oct 2024 02:52:26 GMT  
		Size: 6.7 MB (6672935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f7f1f4ec088e4b6693c82001f201f75294ee1d693ede49bcfb6da307ec1cd5b`  
		Last Modified: Sat, 19 Oct 2024 02:52:26 GMT  
		Size: 7.4 KB (7382 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:20.04-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0ba9733556367b696f7f8c98162a8b06ea14e455f9b4ce45e091a19a7df636e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.1 MB (89122961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:377e8a14c1c6f6f2f02d1e4e2b9794620d29ee881d57a1658519a7d1f9dbbea0`
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
ADD file:f76c848564adfa0c782654cd9423feee0ffacccd95abfe3e4e696203d5e61fbf in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:10b337d353b3ceaf6823ab2d8696989401feed741b22eb313c8a0cd378762d39`  
		Last Modified: Fri, 11 Oct 2024 04:41:36 GMT  
		Size: 23.6 MB (23620412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961fa3ee3eee16522e395458be87f5269ec5b27ec4fcb4d916faeb1068afaba7`  
		Last Modified: Sat, 19 Oct 2024 06:42:29 GMT  
		Size: 9.6 MB (9620727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a338f01587f18e017e42cf3dfc75e5bd303749299cb0e64ea2a2a0865922d2`  
		Last Modified: Sat, 19 Oct 2024 08:17:06 GMT  
		Size: 55.9 MB (55881822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:20.04-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c18c710ecbecc029c07733f7765b2f163752893001e68ce08dfa5f0f3e846abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6684182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29e5d67ea012adced3850967514aa055bc6596d9ef92cf55c25639702fbffec`

```dockerfile
```

-	Layers:
	-	`sha256:40f96d345c76424d7b3c8ace311292ea3a9aa7f22d9b83d18a60094bf4a764d6`  
		Last Modified: Sat, 19 Oct 2024 08:17:05 GMT  
		Size: 6.7 MB (6676742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f0da6b23a5b46534b605e78a83f2bf98bdfc1c58eaaf4142df4f9670439c20a`  
		Last Modified: Sat, 19 Oct 2024 08:17:04 GMT  
		Size: 7.4 KB (7440 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:20.04-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6b30fe5bf79eee34ede4c981ec37e717dac184636d31316f4b5aaa4cb6679c82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (98024179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78df7c0741cdc3adb599669b8f74233ec3eccaa3eb58c8a1976e46b9aa54db05`
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
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a902a6ffa3ee5a0c3f67d06b1a3bb3611210a02b2f2878ae8c1ba1419d989ce1`  
		Last Modified: Sat, 19 Oct 2024 05:21:18 GMT  
		Size: 11.0 MB (10992039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974843836b66b5df8f55da9465dfaca000af6e2d0abe0b8f6cf9013fb718f2c3`  
		Last Modified: Sat, 19 Oct 2024 06:23:32 GMT  
		Size: 61.1 MB (61058312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:20.04-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a19eb135cd6e631684d950b21e75be25d53d984b22fee5ac59d8c35efa2190aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6686824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eca2dc35be6a27a8a79e0940d953aece87ff8ecadf07487672f9c679d28c687`

```dockerfile
```

-	Layers:
	-	`sha256:a5b24f0e1d3b860b1596fd6b36a9dc5f9db79e913aea0444d579207d300136ce`  
		Last Modified: Sat, 19 Oct 2024 06:23:30 GMT  
		Size: 6.7 MB (6679362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:833904452c5bb38d61fb3efa3215ce3556792679f83594c2de9df3253152ac2d`  
		Last Modified: Sat, 19 Oct 2024 06:23:29 GMT  
		Size: 7.5 KB (7462 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:20.04-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b7f3a2a0b03c9b3739e20aac8fe63515dbfa0db054b4d24b1f85886a6ff78afd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114700904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9c4c3362426c92c41177005099f31d0b10f6ed46e627ba49bbe8370d37e691`
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
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e03dda56aeda86639422183ec93ff76ae68820943e9c534c079867713065a4`  
		Last Modified: Sat, 19 Oct 2024 04:11:36 GMT  
		Size: 13.0 MB (12961183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3475eebae315fac14d1638f5f55a0781ae70edd29e02e2525f0f7f09c1dc89ad`  
		Last Modified: Sat, 19 Oct 2024 05:26:29 GMT  
		Size: 69.7 MB (69663215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:20.04-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:899df7b946b9514a555cfa2a174864bb004b02e4e5ab38a3c92bcec8b94b329d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6688198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7310d0a6f41d33f7e0cde1d62a443ebd561f51eb96862dc216534bda751ce5d`

```dockerfile
```

-	Layers:
	-	`sha256:9afda855d0714a2365d893ece73ef0ab746d0b366447423313a1cbcaaada5c0b`  
		Last Modified: Sat, 19 Oct 2024 05:26:27 GMT  
		Size: 6.7 MB (6680784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a187459158467c0224722890e007ccbb8103fd30c10a7ab3846fd2bd76d1e2c6`  
		Last Modified: Sat, 19 Oct 2024 05:26:26 GMT  
		Size: 7.4 KB (7414 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:20.04-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:013c8233697ec9233865c4544b1cd30ba9279bbd680ab1cb5cd9ca29bab7f107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.4 MB (97425179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b297fa71b915ef8a232e93142c280bd8992a61966f6e1796c669dcd9df91b8`
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

### `buildpack-deps:20.04-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:726a303218623b57ec890bd1e8aeb189e63595dce25987a48c801b9e6eb88c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6680392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d6c1c134ce9f29796e2edb349dca6a5efb877a1488648756ec614249c4442b`

```dockerfile
```

-	Layers:
	-	`sha256:0461bcd63c219bd2ede354bbb15f8aefa56d2e62d062bbb9e4154abb83e120c3`  
		Last Modified: Sat, 19 Oct 2024 05:10:42 GMT  
		Size: 6.7 MB (6673010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0da6957fefcd4006ddf29690171e830dfa4d1fc366257b8fcccbe3e718288e03`  
		Last Modified: Sat, 19 Oct 2024 05:10:42 GMT  
		Size: 7.4 KB (7382 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:22.04`

```console
$ docker pull buildpack-deps@sha256:9c6387be70924dc253a6c5594fd11bf8c90a19528442ee8b0b4040362bf1a662
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

### `buildpack-deps:22.04` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d4b8b06ff286846741b4328c1bdf1657d2db64f40f60077770c684e6a84f227f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.0 MB (248987672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760f30692921f381d34172bbbdecd515b01faa8ca2938b65627e9deaa51a0e8a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8284ddf57c03d97884a998219f0fbd84edab303351cdba3ac1526a116e907210`  
		Last Modified: Sat, 19 Oct 2024 02:06:18 GMT  
		Size: 7.1 MB (7102850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9649a6c09e0ee6b937917264d660cd3c815e5ee060c6bc8b89795f658ce584`  
		Last Modified: Sat, 19 Oct 2024 02:52:49 GMT  
		Size: 39.5 MB (39468948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63a153d37d1263e4b6d637c2feb8c983a79dba3aed17ebc110021215169e062`  
		Last Modified: Sat, 19 Oct 2024 03:53:32 GMT  
		Size: 172.9 MB (172880186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:22.04` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:70feaa3e74d0fdb30ec118da0f1d026b137a88e5f7b3a1c9840b07b5baa4dfb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11483927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d97f427a14e1bfca0a95e4de47073b526915ae0f04dd9bb5e6427f9116625dc`

```dockerfile
```

-	Layers:
	-	`sha256:8a7b33f044878adb0a53509f4157f07964d9fe166ea13bf90834fc96ffd7ad99`  
		Last Modified: Sat, 19 Oct 2024 03:53:30 GMT  
		Size: 11.5 MB (11473724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b190dc68ad16997d500a1ec5f110f5645339adda6c4262af41508621b6e389b9`  
		Last Modified: Sat, 19 Oct 2024 03:53:29 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:22.04` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e9e8f9849a391919a9847d9a06e60353e4f78178d3a8b47af1bcbbf0e4bbd65b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.2 MB (216227091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bfdd0166ea17d4aabff352d18a61948531732eb65b495195cb8c34aeff83d8a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:291158c1d919b2d4290b5112a77dc0f7bdf0d45caa53b3556390707d29d2796a in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b477f0f37762a62f631ac4fbaed78c3b23c47db7ac1eaefe95bda0e85ce052a0`  
		Last Modified: Wed, 11 Sep 2024 17:24:53 GMT  
		Size: 26.6 MB (26639293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0953d000943dc8cda05d3be64d712749134d74c6845fe067d2f5a8238e2a5378`  
		Last Modified: Sat, 19 Oct 2024 06:44:26 GMT  
		Size: 7.0 MB (7008052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c5928c39ec338a3e1fcfb711133fed58c4bf8eecf83d91cb2d031a604ede55`  
		Last Modified: Sat, 19 Oct 2024 08:18:32 GMT  
		Size: 42.2 MB (42246833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a42398c457c6ff3c563e93ddd72302080b5be56e41fc4b9cd61c89a565f2d37`  
		Last Modified: Sat, 19 Oct 2024 10:35:16 GMT  
		Size: 140.3 MB (140332913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:22.04` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ddc64d488f547e916a2309a01182e17e703e71ee4eb231e65a82b8a5b1d85c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11274363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:798737324873cec731a9ea8db36d65ae241f36df6da922028438d244414c1bf1`

```dockerfile
```

-	Layers:
	-	`sha256:dce4007c347f0a6155e483e4e34dc4b824baecea35a2445b83d7878bccf4bb4f`  
		Last Modified: Sat, 19 Oct 2024 10:35:13 GMT  
		Size: 11.3 MB (11264100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:318e399acd31061100875c4637aad70762357b54bef40d932a04a3a0c9c9dbc6`  
		Last Modified: Sat, 19 Oct 2024 10:35:12 GMT  
		Size: 10.3 KB (10263 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:22.04` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c7234792a1b8cc508b4678cee66dfef20a0187287f0ff4f6bd2abcdb2f2e9206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.1 MB (240121701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a56bd018cc7818fcfc0c7d5e8d66aadd7a84c6c3687f88c35f9356319a89ad0c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee2b4e5eab18cf336bf82b89529f3587544f710c5e1a0aa67e5ed1fdec85146`  
		Last Modified: Sat, 19 Oct 2024 05:22:20 GMT  
		Size: 7.0 MB (7049559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b264c39c10afdefb042a206e923fa9957e0be85910e8e5065516f128089520da`  
		Last Modified: Sat, 19 Oct 2024 06:24:51 GMT  
		Size: 39.4 MB (39382310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b485acb9c0d30e4a45e9abe1af8dccd9801786bd715c74da323dad89f4bfa92a`  
		Last Modified: Sat, 19 Oct 2024 12:44:54 GMT  
		Size: 166.3 MB (166331503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:22.04` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:757afcc319006f3cf36e7e61ce4eb31547bf81200b78a9c1244d7cf46a2f3ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11479663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0939c54b503f2c5f969194073db614c6b9edf2f105e0999da8027cdf5ca846af`

```dockerfile
```

-	Layers:
	-	`sha256:113d1a92adab8cba7e14939a85617e525a4c413657fbdf36090f022e572d039a`  
		Last Modified: Sat, 19 Oct 2024 12:44:51 GMT  
		Size: 11.5 MB (11469380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96e77f50a0049e1a52a45ec497c71734226905319a0e31ae7d4e92e66f75ab39`  
		Last Modified: Sat, 19 Oct 2024 12:44:50 GMT  
		Size: 10.3 KB (10283 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:22.04` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:71c29684f3a500f9e7d9f88a61ccc3fbea0c72c0c6784e8fb33d799fb1f6e7d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269786527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5039907a5e2568a8b22a12f22cfce64c22f0494eb48f13be18dd296ff622bb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ba759f0622bf9c0e3a62cfaaeedbf629b4a47bad21f09b1f342bd764ad4fc6`  
		Last Modified: Sat, 19 Oct 2024 04:12:41 GMT  
		Size: 8.2 MB (8205814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c923a94cf4353da40bb3b1253640fb7f53899172c56a3d08e7ab97106e9fae`  
		Last Modified: Sat, 19 Oct 2024 05:28:18 GMT  
		Size: 43.8 MB (43761297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c7288a891c79b2e722c068b6342514abbaca2b0b8a59519d18f7bdc4d1bb4c`  
		Last Modified: Sat, 19 Oct 2024 14:00:45 GMT  
		Size: 183.4 MB (183371174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:22.04` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2e2b205d1fb1a96ad4dc8ce6319b090deaea483b19e72bd94eaec63fc7798594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11442701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d771cd24220f8c054a7bac19df98afae4690de4be490b95f0d69e37a607db97`

```dockerfile
```

-	Layers:
	-	`sha256:119f3b98f8d296ef4dea15628870f1bbd266cf1752e4b5abd67c2f84c4aa182e`  
		Last Modified: Sat, 19 Oct 2024 14:00:40 GMT  
		Size: 11.4 MB (11432466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0dd88025aa4b45ed0abc1ed1588f47870d67e6bca8ebd87d5c9f26fcafcc67b`  
		Last Modified: Sat, 19 Oct 2024 14:00:39 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:22.04` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:1afa69bd96855d8248fdba88a69258839c572cb7b2dac2ce75077bb67848c381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274113264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2adea3b29bae5fcd5a6adefbd9ff8f276c9e7fc97fb6fc64afd6b7126802699`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:d73c592fd8b1cf53b1e79e60cc01a9371bf9156f299ddf5a8482ea43525aaa9a in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6579073ec343e2eff1822992b7ff52b06a067be5c14999033789394aadca585d`  
		Last Modified: Wed, 11 Sep 2024 17:25:05 GMT  
		Size: 27.0 MB (27038996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef216c90e55bcafd475d74f40962beb13a5a26ac03f5cf90bc3879dfabc5db04`  
		Last Modified: Sat, 19 Oct 2024 04:05:55 GMT  
		Size: 7.1 MB (7116572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c25cfae42e3c0e2795e05916aefa3b950bc058947a8a8a9b1e38197627712b6`  
		Last Modified: Sat, 19 Oct 2024 05:36:08 GMT  
		Size: 42.3 MB (42309710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8b23b2911e88d71f2c712bc659cb5aeda7ad0f3bafcc8a08c792987ef23c64`  
		Last Modified: Sat, 19 Oct 2024 07:35:12 GMT  
		Size: 197.6 MB (197647986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:22.04` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:09045a7fabc47e2b581c1b01bab7aed6cc5f6883e9021d8d2b67a9058a1547d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11425790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a30f25b563bc0af385b3f10a6f762fd2c7e3830a01c7595566d6e22eb571e8f`

```dockerfile
```

-	Layers:
	-	`sha256:ab2b88b1bcd23b0b9ba9ef4832308137caf116dede95dd91410a525056b9d0ef`  
		Last Modified: Sat, 19 Oct 2024 07:34:46 GMT  
		Size: 11.4 MB (11415555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73c3843a7566422eb997cf6fd44192354044fb45f91880a3a4b88e73041a1348`  
		Last Modified: Sat, 19 Oct 2024 07:34:44 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:22.04` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ec33a2063ef5aa4756aef87fd8a958c89053f520e17b5beab973c72046ab73ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222948887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c6652a81bcdf5919387801cb65d42094fdbc9a4423f0ae1c0079c55eb9c997`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69520da589bb4a5afebcb33e75154687a27523df1667ed280e4056c48d0f9ab2`  
		Last Modified: Sat, 19 Oct 2024 03:50:51 GMT  
		Size: 7.0 MB (7016679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92120d25a5bd34685129dc03eb81c53d37e34f8d347a42193df4f92bbcdcc0e4`  
		Last Modified: Sat, 19 Oct 2024 05:12:06 GMT  
		Size: 39.4 MB (39401291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f27d67cf1107dad4d1fd687bc141375a87454b71e0b9fcc7f3f5e1f4142e177`  
		Last Modified: Sat, 19 Oct 2024 06:58:36 GMT  
		Size: 148.5 MB (148529442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:22.04` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8670708200c1354cc2305964d8f7e0e6e674cb76bee77589538cbf4a782c4566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11298722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5db8b36cafc56df975ba4f7f3249442e8ddb4f87ad576e344254e9bb3a3761d`

```dockerfile
```

-	Layers:
	-	`sha256:35631ba052bd0c28ea0d31125303e40050b1def645355f2943e41baf4d66b081`  
		Last Modified: Sat, 19 Oct 2024 06:58:33 GMT  
		Size: 11.3 MB (11288519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8c41a739e5a3f102f7913049b5db83525a238a20625272f15112ab8ffbef145`  
		Last Modified: Sat, 19 Oct 2024 06:58:32 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:22.04-curl`

```console
$ docker pull buildpack-deps@sha256:85596490cf18e74c534e123e29d7bcbc30182fae51129525148111645a7ad569
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

### `buildpack-deps:22.04-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e9e575bbf5fbd08b92fddfefa92a1f03825ef05ad773b4487eee6acfed264837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36638538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f765ea36fa4c46759dd690bb21cb8e45f32e1aa331cf9ad0da8b14816aa41ea3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8284ddf57c03d97884a998219f0fbd84edab303351cdba3ac1526a116e907210`  
		Last Modified: Sat, 19 Oct 2024 02:06:18 GMT  
		Size: 7.1 MB (7102850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:22.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3ad27316a38d3124ad8c0ef153c2a1fd356e6101cd2de78b49c0a1517f8e5f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3059492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078a608399f965e1ef663c83205965174b05b375eba24e149c27e9cab4aeb91d`

```dockerfile
```

-	Layers:
	-	`sha256:1abede6965aa4c2f6dc7a23f51f9c10eab34e628cee2f9817cc259b2558d4d18`  
		Last Modified: Sat, 19 Oct 2024 02:06:18 GMT  
		Size: 3.1 MB (3052568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1388bf3300d1894b794c3a79d61de4d5106bdcc7c16afd59021479c3346dc8a5`  
		Last Modified: Sat, 19 Oct 2024 02:06:18 GMT  
		Size: 6.9 KB (6924 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:22.04-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:20fc212e38dd71fb2c3c9914fc825a38358e81e134db6923889a1c303f0ae326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.6 MB (33647345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbba2125fdb8a2505c8f55e2499e2f13553a82c47d377d9c493fcb3f60c7f4ed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:291158c1d919b2d4290b5112a77dc0f7bdf0d45caa53b3556390707d29d2796a in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b477f0f37762a62f631ac4fbaed78c3b23c47db7ac1eaefe95bda0e85ce052a0`  
		Last Modified: Wed, 11 Sep 2024 17:24:53 GMT  
		Size: 26.6 MB (26639293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0953d000943dc8cda05d3be64d712749134d74c6845fe067d2f5a8238e2a5378`  
		Last Modified: Sat, 19 Oct 2024 06:44:26 GMT  
		Size: 7.0 MB (7008052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:22.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:eece698d153df1f89fadfff448417adeb8215fd72b047ac459cb49353fce45c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3061858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79401084f8905bad1c4c968bee99d939840fae67ed54244f77a6d632b50ab6c4`

```dockerfile
```

-	Layers:
	-	`sha256:f07353059a36e79f6b9030cb13757b44c6245824987503b83d6f536a4e693a47`  
		Last Modified: Sat, 19 Oct 2024 06:44:26 GMT  
		Size: 3.1 MB (3054874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb0a469469d317122a2932b0e26adba945e4a5d58bb8da9bc08083568288073b`  
		Last Modified: Sat, 19 Oct 2024 06:44:25 GMT  
		Size: 7.0 KB (6984 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:22.04-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:41102486bd331fc045ca4dd0c7ab19df349ce8fa115a386073d582c5ebaf4b77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34407888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f8ad5d876c3264e3479b020c677f69f46a7e69fe13035ad9e201a14c7d7a6a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee2b4e5eab18cf336bf82b89529f3587544f710c5e1a0aa67e5ed1fdec85146`  
		Last Modified: Sat, 19 Oct 2024 05:22:20 GMT  
		Size: 7.0 MB (7049559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:22.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6ab6df736a4f64794b5d01d640d59584d49c7c2fb01273eb94880893d1ad7b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3059838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5452a80b64ba34c05b9e80ad169c456c03a4d42060f09c71f9ee69d77e1914b4`

```dockerfile
```

-	Layers:
	-	`sha256:ceb05956e7d16f0743e8d98b6d5fbaff860dab57442acf4c9f2976636ebde31a`  
		Last Modified: Sat, 19 Oct 2024 05:22:20 GMT  
		Size: 3.1 MB (3052834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:853ec9692386086ec112b4a3f1d935035560feac8084776b25e1da098a367767`  
		Last Modified: Sat, 19 Oct 2024 05:22:20 GMT  
		Size: 7.0 KB (7004 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:22.04-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8c440e8edd3fc6eb6303246ef73f5fa811c9701bbb92966f11d77e3772040b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.7 MB (42654056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ebb57a604797dde5d006fe5668f0568828131689c956f6a9f96516dde9378c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ba759f0622bf9c0e3a62cfaaeedbf629b4a47bad21f09b1f342bd764ad4fc6`  
		Last Modified: Sat, 19 Oct 2024 04:12:41 GMT  
		Size: 8.2 MB (8205814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:22.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fb640bcc8b1fb70fe5dbe39d90903b445716812fdf4a37ad87f41db230205f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92641cdf3683b1f21313af156d1c37fe47ef9052962af565bbf3a34a63c5e49a`

```dockerfile
```

-	Layers:
	-	`sha256:d957ab9ba0e3cfef7c2cd76d148d5d72b675f5cab4596bedc554a0c7c965c4d4`  
		Last Modified: Sat, 19 Oct 2024 04:12:41 GMT  
		Size: 3.1 MB (3057063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30ad65d10290bd28b22bc51bbf57a7def5ae2d467694c5087b06f33c038c8b63`  
		Last Modified: Sat, 19 Oct 2024 04:12:40 GMT  
		Size: 7.0 KB (6956 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:22.04-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:179857b8adde6f954375127a2dd12caeef247d7be9af5c177b00fe3c40076222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34155568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f190c58725abd84359210464a4a8e6e08e5c21a2e2f30c4d6619fcd0f427c4e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:d73c592fd8b1cf53b1e79e60cc01a9371bf9156f299ddf5a8482ea43525aaa9a in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6579073ec343e2eff1822992b7ff52b06a067be5c14999033789394aadca585d`  
		Last Modified: Wed, 11 Sep 2024 17:25:05 GMT  
		Size: 27.0 MB (27038996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef216c90e55bcafd475d74f40962beb13a5a26ac03f5cf90bc3879dfabc5db04`  
		Last Modified: Sat, 19 Oct 2024 04:05:55 GMT  
		Size: 7.1 MB (7116572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:22.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9543357c11475894edd32d6735f47929fbdcc2009261bfd0f41ae2fd3acd156d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a67e05f8df84faa6dd71a4f2fecfc217e7394e6a5e95728cc5fc96ac6419608`

```dockerfile
```

-	Layers:
	-	`sha256:9add722049583dcb3f1fa4cbff5ab2c66da1d0d4a7599508207ef70e62a77c73`  
		Last Modified: Sat, 19 Oct 2024 04:05:54 GMT  
		Size: 3.0 MB (3046665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42a956a517e54dbc6ea7485daeb102dfa8babacace0704cce1c28d03ace46992`  
		Last Modified: Sat, 19 Oct 2024 04:05:54 GMT  
		Size: 7.0 KB (6956 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:22.04-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a057da907e6159116c1d6b558d76d2a226bd00cc61f02d6c039bd9ead6cd6bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (35018154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ccb112658f15462f21c737ef77f946e275af373679709c0f95834404e426235`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69520da589bb4a5afebcb33e75154687a27523df1667ed280e4056c48d0f9ab2`  
		Last Modified: Sat, 19 Oct 2024 03:50:51 GMT  
		Size: 7.0 MB (7016679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:22.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:86df1e572c2fdf579e24bf8ca6d6bbfd8905398fa586cdc97cc9a957aff4ca75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3061713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb63a62d2750a3d6dab0c24c174e5480aebb92715818dfc54fa348c77a25ba9`

```dockerfile
```

-	Layers:
	-	`sha256:77ac86a3a24d3e0653a3ae6467144940afee5c73c0bdc2583a25dcb8e2ae75c4`  
		Last Modified: Sat, 19 Oct 2024 03:50:51 GMT  
		Size: 3.1 MB (3054789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19f8b337c9885e2ecf77ae2d622ed549a5f5f5485df0dccadac74cd47c47d940`  
		Last Modified: Sat, 19 Oct 2024 03:50:51 GMT  
		Size: 6.9 KB (6924 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:22.04-scm`

```console
$ docker pull buildpack-deps@sha256:65b6be032f9d7e64ea541e00e48c71bd961be04741c6d688f33218ab031a9f9c
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

### `buildpack-deps:22.04-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:17942397e5fced3f8b300ac7c7eb615dff08e3bf4b25ff7d4fdf0e50dc0e3637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76107486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8ee0b5a3fd03948f634e632da31c66362c3663e3c5dd9e1e0c262c2266ed67`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8284ddf57c03d97884a998219f0fbd84edab303351cdba3ac1526a116e907210`  
		Last Modified: Sat, 19 Oct 2024 02:06:18 GMT  
		Size: 7.1 MB (7102850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9649a6c09e0ee6b937917264d660cd3c815e5ee060c6bc8b89795f658ce584`  
		Last Modified: Sat, 19 Oct 2024 02:52:49 GMT  
		Size: 39.5 MB (39468948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:22.04-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:754d2bec28ffc00a26e2f7a1354ed7ae0d3775ed7f8e8ef4d4d940cf534818f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5616367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1aef2e9a39d9f88806281cb44ebdae0758f7e0875bb44eec230ab7b038d1f21`

```dockerfile
```

-	Layers:
	-	`sha256:3746959abc49b330e29be49c40d27e7319253b12cd58a2f8585e96ca7d34fa7c`  
		Last Modified: Sat, 19 Oct 2024 02:52:49 GMT  
		Size: 5.6 MB (5609043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f77b1e734b0869190432a877573774367e039f62d93c379d4dffcf3156b081a7`  
		Last Modified: Sat, 19 Oct 2024 02:52:48 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:22.04-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:36f7f482089e1c9ff1e74c91cd11616da25679c73d6f5b9402c848167bc1560c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75894178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98bb0b7cfb61a6bb25c1de92dc0b7b3b9880b0cb8143292ebd52ffda4d80d9ed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:291158c1d919b2d4290b5112a77dc0f7bdf0d45caa53b3556390707d29d2796a in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b477f0f37762a62f631ac4fbaed78c3b23c47db7ac1eaefe95bda0e85ce052a0`  
		Last Modified: Wed, 11 Sep 2024 17:24:53 GMT  
		Size: 26.6 MB (26639293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0953d000943dc8cda05d3be64d712749134d74c6845fe067d2f5a8238e2a5378`  
		Last Modified: Sat, 19 Oct 2024 06:44:26 GMT  
		Size: 7.0 MB (7008052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c5928c39ec338a3e1fcfb711133fed58c4bf8eecf83d91cb2d031a604ede55`  
		Last Modified: Sat, 19 Oct 2024 08:18:32 GMT  
		Size: 42.2 MB (42246833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:22.04-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b6fdd0ec46e198e0ec0a9fa83af06d9521e50887c9083df6f8b93b265c06c118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5617703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62d57e04a27948c0eb865140b4c66fe12724cc8de7227bfa2d2c599e14ef1ba5`

```dockerfile
```

-	Layers:
	-	`sha256:c81a8e1f595d9f463820b3485fecf663109b333695ec89dd112ce92d25397383`  
		Last Modified: Sat, 19 Oct 2024 08:18:30 GMT  
		Size: 5.6 MB (5610319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aea552147d8c9174fa2a375b8191da83bac8a92276871696f8078bcc4d2208aa`  
		Last Modified: Sat, 19 Oct 2024 08:18:30 GMT  
		Size: 7.4 KB (7384 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:22.04-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3b4dc315b2f43492a8caf18705f18b4ecf52ef4f30ae0b852c5b43bd83f1edcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73790198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0040e9b18bab25e40c4dc3bcb25bbeff1e6e35d6c4156e9559e032772c502f6e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee2b4e5eab18cf336bf82b89529f3587544f710c5e1a0aa67e5ed1fdec85146`  
		Last Modified: Sat, 19 Oct 2024 05:22:20 GMT  
		Size: 7.0 MB (7049559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b264c39c10afdefb042a206e923fa9957e0be85910e8e5065516f128089520da`  
		Last Modified: Sat, 19 Oct 2024 06:24:51 GMT  
		Size: 39.4 MB (39382310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:22.04-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:457c35d342663a69ec383a5df6b75820fdfb7f2dd8d5d94169416d8320c0143c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5622847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22210069278fbb79bfaf97a95dcaac2c228a24e7481e7d2f350821064c3e2c1c`

```dockerfile
```

-	Layers:
	-	`sha256:c4f843d61bcf7f9c51d7e2a70cbfda18a9a4dce752481ec5d0da09f4a91f0682`  
		Last Modified: Sat, 19 Oct 2024 06:24:50 GMT  
		Size: 5.6 MB (5615443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49eec21858e105c95bdf207c9a3a4473510b952446b3cdeb902fbcfbc1d5574e`  
		Last Modified: Sat, 19 Oct 2024 06:24:50 GMT  
		Size: 7.4 KB (7404 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:22.04-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:dc92a9760be21890e640c7a93bd240ae83b1dd8cd476082ec342f8bbb0589dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86415353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f942098a3824a00b40abfa837c90a6702a23adae15d4aab412018f90518f4e1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ba759f0622bf9c0e3a62cfaaeedbf629b4a47bad21f09b1f342bd764ad4fc6`  
		Last Modified: Sat, 19 Oct 2024 04:12:41 GMT  
		Size: 8.2 MB (8205814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c923a94cf4353da40bb3b1253640fb7f53899172c56a3d08e7ab97106e9fae`  
		Last Modified: Sat, 19 Oct 2024 05:28:18 GMT  
		Size: 43.8 MB (43761297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:22.04-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ca42ab3869cefe7a695a4e1f169c8bbf958e6c018b01d10eff974346b2253ebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5624067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec53006865d81586277bbd8d711c33a775261feefb77a1abce185763b0414f47`

```dockerfile
```

-	Layers:
	-	`sha256:69b993149892bd952ac1d559783e53290067df7e12a0f4a411971f13fbfb7eb6`  
		Last Modified: Sat, 19 Oct 2024 05:28:17 GMT  
		Size: 5.6 MB (5616711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe45130b58e9b94959acbac2f5825ca053b3c0be9651aebeea0abc0f0441c826`  
		Last Modified: Sat, 19 Oct 2024 05:28:17 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:22.04-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:4ddc9e5dc332305f385db2d46e6106bdb9a6df770d34cce1a7b1328e9f773581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76465278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596a39522065aaa5259e07bfd7e3ab09944aa66546dfb4f4072cdd1c36988395`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:d73c592fd8b1cf53b1e79e60cc01a9371bf9156f299ddf5a8482ea43525aaa9a in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6579073ec343e2eff1822992b7ff52b06a067be5c14999033789394aadca585d`  
		Last Modified: Wed, 11 Sep 2024 17:25:05 GMT  
		Size: 27.0 MB (27038996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef216c90e55bcafd475d74f40962beb13a5a26ac03f5cf90bc3879dfabc5db04`  
		Last Modified: Sat, 19 Oct 2024 04:05:55 GMT  
		Size: 7.1 MB (7116572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c25cfae42e3c0e2795e05916aefa3b950bc058947a8a8a9b1e38197627712b6`  
		Last Modified: Sat, 19 Oct 2024 05:36:08 GMT  
		Size: 42.3 MB (42309710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:22.04-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:677e3217d2dc918ca5ab384bfca869b7e8c8305316cb1cc037f141956b0b3272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5606953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55cf4c2b60436fb8bd0fa2d4b50a36c087d7488d743693396d221ec0491c7180`

```dockerfile
```

-	Layers:
	-	`sha256:b1f512202dcb2b5d928ecb4585d6de15c42669027b7a5d4579e1bddcdb7a2df2`  
		Last Modified: Sat, 19 Oct 2024 05:36:02 GMT  
		Size: 5.6 MB (5599597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7354a339140b887de10c47610cf80258f8ee49298f940c212168e99cf717cd83`  
		Last Modified: Sat, 19 Oct 2024 05:36:01 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:22.04-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3f5839289113a1c014b308f044c1d2090b5de0b459d03509d92a76e98dd8c5e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74419445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e04f9df778c0f0af647e3031be3af40bb003c80f1d79b43a2fb836cbafb4bb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69520da589bb4a5afebcb33e75154687a27523df1667ed280e4056c48d0f9ab2`  
		Last Modified: Sat, 19 Oct 2024 03:50:51 GMT  
		Size: 7.0 MB (7016679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92120d25a5bd34685129dc03eb81c53d37e34f8d347a42193df4f92bbcdcc0e4`  
		Last Modified: Sat, 19 Oct 2024 05:12:06 GMT  
		Size: 39.4 MB (39401291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:22.04-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a9165337d0ebf9676d18fa86b71698b5a66daf7200d6d69d6a1dd668bedef442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5617289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77825930997f20c071742d9d36a54d7a6e0c03a1323f48f103041531e03bf62b`

```dockerfile
```

-	Layers:
	-	`sha256:dc56c2effd84be465d89ab77f837d7abd693a4b0a819c52bbe97ac0e6e9d1984`  
		Last Modified: Sat, 19 Oct 2024 05:12:06 GMT  
		Size: 5.6 MB (5609965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8c2021cef4f4ba0d46679bd7621ac751c2924e23cef9ded9a605a5867443e0b`  
		Last Modified: Sat, 19 Oct 2024 05:12:05 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:24.04`

```console
$ docker pull buildpack-deps@sha256:f6c88b5183ccb4873ff006ffa7e148856ae0bc9607a961198837bc3ee1c8123f
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

### `buildpack-deps:24.04` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:bb83ff53a86c956b665a684cdc6d251a9d5ba84bf82e97e566d398d5e27d2c45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.7 MB (278694752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7cb61cb2b87dc4a68b6ea91ebea0d11384037db0ebe0fd7c66f83b1da30f57`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5235aa939f41c34b69f4fe37736745fde8e1a4676950add7459e7b957c4cfd55`  
		Last Modified: Tue, 03 Dec 2024 02:28:51 GMT  
		Size: 13.6 MB (13617608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48cf16388a9a3471d6a91777a42a673b8db99767b831de048212ce4136744cd4`  
		Last Modified: Tue, 03 Dec 2024 03:17:02 GMT  
		Size: 45.4 MB (45394654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafede1dd30b73e66552948455e76ed828e5f7c7098be8fff3596c51c6277fc9`  
		Last Modified: Tue, 03 Dec 2024 04:32:10 GMT  
		Size: 189.9 MB (189930522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fd83f7ce1b0a238e27ecbc0207f69f63a64267b67fd7dc91ca0c49747cdd7863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11373395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad5d6dfff524e78a2901c016b52d0653fc960c88f14fd01abd1818d0b24f49f4`

```dockerfile
```

-	Layers:
	-	`sha256:f3007db501bfab1f0450753095c7788798dd7f6b71b8a20aca7128ff937003c4`  
		Last Modified: Tue, 03 Dec 2024 04:32:07 GMT  
		Size: 11.4 MB (11363211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9ea8ae9a98f8b881899f6107f12ba787f9d886379f1542a2b8eac45c8572fe0`  
		Last Modified: Tue, 03 Dec 2024 04:32:07 GMT  
		Size: 10.2 KB (10184 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:bd5ebd5467d1524eaf40250310b664291c17aa0d2bf8d1eef73d1da23227edd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.9 MB (238926365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3315e6b7232f3b7f0fb4c657dd3ca3fc43c5f47643b63605e65d2838e3682ed2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:786ab064bf2d82faf7ca3fbb6c2e6983bbdb3228800d6d64e5dec4a67f778a7a in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b25adda5718ef4d96696ce8f0e58cde58fbe9977456036f84293bba8f26c5567`  
		Last Modified: Tue, 19 Nov 2024 17:38:39 GMT  
		Size: 26.9 MB (26869639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f072a621863f98c6e93487af2148d3199cc2cf579bfe20feab8e50641003f0`  
		Last Modified: Tue, 03 Dec 2024 07:39:05 GMT  
		Size: 12.8 MB (12774963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335cf1f7da64ab01e02577f00ca7c83d14ba94593eeb2b94921fa0dd578a4e4c`  
		Last Modified: Tue, 03 Dec 2024 17:19:41 GMT  
		Size: 48.9 MB (48944185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24ddd4b0f02d6d7bf38be9b41c408f1242fd536d325d89fa0c43fb580051af0`  
		Last Modified: Tue, 03 Dec 2024 20:16:12 GMT  
		Size: 150.3 MB (150337578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d69b102a8f2f6d9742411b7b3d9cbf306e0c5a6545618dff2a16bca42464b032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10720389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f24e38cfa99bdd21a9cda91104e80836989f73eda79cfeb91ebca5291cc0977`

```dockerfile
```

-	Layers:
	-	`sha256:de156d5d70a7cbc8ffc728612e41c8daf31719edf4827741f797e6cba4acfc70`  
		Last Modified: Tue, 03 Dec 2024 20:16:08 GMT  
		Size: 10.7 MB (10710145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abd9017c402a1607859ce1331ee22a2877d983bc44296cf9bde3cc8bba6a5060`  
		Last Modified: Tue, 03 Dec 2024 20:16:07 GMT  
		Size: 10.2 KB (10244 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:48ec7d59dec4b33f187e27c867d6de4a9dae6c184ea08969623f0f84a75dfe40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.7 MB (269660566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9624081441bd36cf08652ff2ce33e156fb26dca65c8a428dc5fb617711f58c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331da7d4a8631a606292d353129b9398a4db3f2798d686a807920d0a81e2c741`  
		Last Modified: Tue, 03 Dec 2024 05:40:42 GMT  
		Size: 13.5 MB (13452932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af04d25eb37c1d037171f5c201d5753407b0902b0f09c9b548efca5b1d914b62`  
		Last Modified: Tue, 03 Dec 2024 11:53:13 GMT  
		Size: 45.4 MB (45358165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf8a464ed6ede506dbb704c616401409e9edba9adddd90f8285bf3e38569f37`  
		Last Modified: Tue, 03 Dec 2024 16:29:28 GMT  
		Size: 182.0 MB (181956798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7b1c5169af505db4fd177e93d7cc7d418eefa1aba2c5c543ed7585a7a7e5924b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10942946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b3d4def8c8d0db456ca7cf9dbb53398901530f28a25db7b20ea8a5855a6060`

```dockerfile
```

-	Layers:
	-	`sha256:c64ad584569af3cc34359825ecc15b46f6923a382b0a26aa88caa615a37fb2ba`  
		Last Modified: Tue, 03 Dec 2024 16:29:24 GMT  
		Size: 10.9 MB (10932683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55d65706b0c815a3c6f9b755f469cfd2d5792895758cf29b8087a6e473b836c5`  
		Last Modified: Tue, 03 Dec 2024 16:29:23 GMT  
		Size: 10.3 KB (10263 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0f081dc43aae4c0264f372db9ff26f642234d719c5cea169e1313110d0a71da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.2 MB (297192499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72973b5074015731ccd005dc3a9f728cadc21a785b5d63f7bcbad915e99b48f2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb006e560e9a807b6372fb925c588d9d83a6052a65248653a1f5708527a24d4`  
		Last Modified: Tue, 03 Dec 2024 04:39:54 GMT  
		Size: 16.0 MB (15980138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9deff409e8ce76af2a5a7095a7e708fdcadb9e212359c8655149b857100b432d`  
		Last Modified: Tue, 03 Dec 2024 09:46:22 GMT  
		Size: 50.6 MB (50557592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af77c7fb06c47d86e7daf6d244287862d5f022cbd73a8f24b0c9652bed607668`  
		Last Modified: Tue, 03 Dec 2024 16:27:22 GMT  
		Size: 196.3 MB (196265949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:eea638158cb24d7f4cebc2c98af5c3442a994d30e18797d991d9a56f6e93e905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10890073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f222e319fed14c024b6c5b08c679eec3c08b07fb9e16818e07ac8c244442113c`

```dockerfile
```

-	Layers:
	-	`sha256:adf0e9d2e4c57e9958e4fb4db04302367e0f365aa0f6f875539e6758cfbaba18`  
		Last Modified: Tue, 03 Dec 2024 16:27:17 GMT  
		Size: 10.9 MB (10879857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccd908e1ab77b3bd255cafb4cbf55047b3e614ba53fcb8d474b607099e6d2a54`  
		Last Modified: Tue, 03 Dec 2024 16:27:16 GMT  
		Size: 10.2 KB (10216 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:5e1605aa43abc928356ba673ef6be9bd9319e90a23c606d51d650fdf5df34018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.0 MB (329034579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835d261ccf3765d3b5873291e25e82e57429821f2acedbbccf22f8d6c8d6e811`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:23c2e341d6cf3572f2762ef1304c406cf6d4f5ee8ee8719ef289a3b75a8323aa in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0dcc8c973ba119a0fb5275114fd0456179bba1132bdc69f2afa4e1c4a235c540`  
		Last Modified: Tue, 19 Nov 2024 17:38:52 GMT  
		Size: 31.0 MB (30980838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789bf3edf440eb67602bc2c6173f31d3292b752b03bbf690c473a5038b858343`  
		Last Modified: Tue, 03 Dec 2024 06:44:43 GMT  
		Size: 14.3 MB (14321082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f505f2c8e1079fb73360d2ba6b4c3130e06fd9586abaa35474f69fd6f08ac0c3`  
		Last Modified: Tue, 03 Dec 2024 09:51:22 GMT  
		Size: 53.9 MB (53856700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f5c18773f973d35cc8bb879ed0254ec6d05cca16b3f9339f4eb2b99b6426a9`  
		Last Modified: Tue, 03 Dec 2024 11:10:32 GMT  
		Size: 229.9 MB (229875959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:42ac014c17c16ec26d33081987bc40ec5449f24b0cebd4ee754cfbab8def7dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10878996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e072ce08a23db75befa02226181a0b4b1e33930050fd5c9b2e1c5b4654b2dc21`

```dockerfile
```

-	Layers:
	-	`sha256:9d8ab87d7a49129567a98c7b079a08bf77f826fa903e25c72412c2f803d9b4ca`  
		Last Modified: Tue, 03 Dec 2024 11:10:02 GMT  
		Size: 10.9 MB (10868780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b587665ba1f2bb0c50e0efbceb471e61c7abcb950f38d26c6ca2fe44e136d6f3`  
		Last Modified: Tue, 03 Dec 2024 11:10:01 GMT  
		Size: 10.2 KB (10216 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4a55093eb0048c2456e122785f6ca1890b9359d3efce4ff6f3e109bba8e87e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 MB (260854060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ea0f30aa2bb668752c8f50eb109cdf7d802314c2a55a318a7c42919b9026592`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:1c391e128b3c5e552a1401f9520290446bf94ba089c2d74a5d661001d3d8b60c in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:755503a8fb36d6a0d08275c3792ab81b69fdff95054dff0aa932d6dc30107609`  
		Last Modified: Tue, 19 Nov 2024 17:38:58 GMT  
		Size: 30.0 MB (30020826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35190d0c1306f85de6133cb1ceca330cd03ee2f6baead3be847b0c8e4273f57`  
		Last Modified: Tue, 03 Dec 2024 04:10:05 GMT  
		Size: 15.0 MB (14960770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05107eaec609414c9540f16903f6f4fed09e9055d47bca5a3188db8c2f781888`  
		Last Modified: Tue, 03 Dec 2024 07:57:25 GMT  
		Size: 46.9 MB (46912688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec9245ce6aafa9002bb642e97c63ac3ef077f28fd50c83064b68bc310d8f457`  
		Last Modified: Tue, 03 Dec 2024 10:54:15 GMT  
		Size: 169.0 MB (168959776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3d39c6be03b02a7e807a6d25ccfc5b0d68a2220dfc7704f2c5bfae8c2ab2c53a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10735769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea05009d300f9ae1c0b408d9cbe080d09822698e52361e856112d74572ec003`

```dockerfile
```

-	Layers:
	-	`sha256:8cc51ba0c454962e736809e6968abb638f186854bdc7e4dc494c5f531eb8e880`  
		Last Modified: Tue, 03 Dec 2024 10:54:13 GMT  
		Size: 10.7 MB (10725585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e5587fd8db9cff37c4d4ae0d1693c3695f27c5deabe39009de2b8bc3d8bde7d`  
		Last Modified: Tue, 03 Dec 2024 10:54:12 GMT  
		Size: 10.2 KB (10184 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:24.04-curl`

```console
$ docker pull buildpack-deps@sha256:9911aa92f07dc4100c07880f79859cd1c67533e6188c47141c1e2cabcce9ce1c
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

### `buildpack-deps:24.04-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0fa4cc5ad043306df0d2c2c4e6a9d1219084de8f003aec1e02f776b4e23e6ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43369576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42fd4116a699db2d4e7a8dcc690dd3362f29a31d0305d44e60b1da7400121a8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5235aa939f41c34b69f4fe37736745fde8e1a4676950add7459e7b957c4cfd55`  
		Last Modified: Tue, 03 Dec 2024 02:28:51 GMT  
		Size: 13.6 MB (13617608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a2f44a037cce80f83c04568a366e5fb90b861a4d43f58289c5687cb79912923e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aff44ca61232543e0e4008545e3442593e8dd41caa992235517167a8846a6fe`

```dockerfile
```

-	Layers:
	-	`sha256:9afde91d62e4816e8bed19458ec653775b86b7302dc68c386a6913f2723252a8`  
		Last Modified: Tue, 03 Dec 2024 02:28:51 GMT  
		Size: 2.5 MB (2460157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edaf4a88adf6a30c34e18b08bc3714cfed92a82b366bbf936d5b93a235d9085c`  
		Last Modified: Tue, 03 Dec 2024 02:28:51 GMT  
		Size: 7.0 KB (6958 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2da8ecab6d61772b7679a305ec87fe82ab997fe5f88e6889153581f9b8e0129e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39644602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5c83fea6dbb69e662877b22fdaa2d1195b4698e1ecef022de83e0c9bc2b735`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:786ab064bf2d82faf7ca3fbb6c2e6983bbdb3228800d6d64e5dec4a67f778a7a in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b25adda5718ef4d96696ce8f0e58cde58fbe9977456036f84293bba8f26c5567`  
		Last Modified: Tue, 19 Nov 2024 17:38:39 GMT  
		Size: 26.9 MB (26869639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f072a621863f98c6e93487af2148d3199cc2cf579bfe20feab8e50641003f0`  
		Last Modified: Tue, 03 Dec 2024 07:39:05 GMT  
		Size: 12.8 MB (12774963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:07168df7c99826ff59dbaa035f61d4f7a5c6f0e49f39caa0a21044f77d3970a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2469479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825fefe71ffe4a6f13d42aac4254e18436de1618fd7dd424f7c38c48283034be`

```dockerfile
```

-	Layers:
	-	`sha256:c0918bea141dc274a311f371547de2fc014d951a996ae68df6dc4cb49fc63c91`  
		Last Modified: Tue, 03 Dec 2024 07:39:04 GMT  
		Size: 2.5 MB (2462460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e25cca77142a6540d318afa3e83cca144ba327a2a445583fd27160b200cf96a`  
		Last Modified: Tue, 03 Dec 2024 07:39:04 GMT  
		Size: 7.0 KB (7019 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3f12b281d4c7e441ca6b2ed447d7b8ddcb738e8146fd51eaa15c5946c476d9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42345603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d55ad38d6ad3b1975d81df0d33cf24df7c080c89a5a6e833d8fe7c0e826303`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331da7d4a8631a606292d353129b9398a4db3f2798d686a807920d0a81e2c741`  
		Last Modified: Tue, 03 Dec 2024 05:40:42 GMT  
		Size: 13.5 MB (13452932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c33ab3937c7073dda570cd34197c5e3f67b52a83eb735c5a0345c96d2dd09ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56ae62139fee889a90664cb93c0b7504ef9db10d54e683dcc9d27f492f86ebb`

```dockerfile
```

-	Layers:
	-	`sha256:6432e9ae2dbac0fd9b0b261fa1aaa14c198e831ab1d9e88950df498125b93e63`  
		Last Modified: Tue, 03 Dec 2024 05:40:42 GMT  
		Size: 2.5 MB (2461215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a01727f7c98822d422cb960375c8c525f7aa192239eb880b79b9acca421a728`  
		Last Modified: Tue, 03 Dec 2024 05:40:41 GMT  
		Size: 7.0 KB (7039 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:53f47b381774bf1fb84602bc0b56726a929f843c79b80b5b25623908f15bc318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50368958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd68d72e23a609767f38fa4dd1e15adf3cad28cedce39399ac29e4014874941d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb006e560e9a807b6372fb925c588d9d83a6052a65248653a1f5708527a24d4`  
		Last Modified: Tue, 03 Dec 2024 04:39:54 GMT  
		Size: 16.0 MB (15980138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e3c0d30c9776b2e964822e3f9884b555a6ff0c2875d8365faf49d773c1a3cda0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2471632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078a7fb980e93ad0004a00f7f1c98d54288c1735f320327ccc764a8b66f56e81`

```dockerfile
```

-	Layers:
	-	`sha256:4285ede008935a505df8c503de2dd6047bd3480e9e2a298b783ba07b1e7abf7f`  
		Last Modified: Tue, 03 Dec 2024 04:39:46 GMT  
		Size: 2.5 MB (2464643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:464acb1349a4f65e154e4589d2a9df0ceb12ae177be44a38fbe8c417d0757c99`  
		Last Modified: Tue, 03 Dec 2024 04:39:44 GMT  
		Size: 7.0 KB (6989 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:427093dd420b73785f4c697433aa021ca695d93925872ce11cd14177982d2eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45301920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae64a028798fd8ac0ccf9a37363e97545ec4956264ef73eb76ae7577755dcf1e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:23c2e341d6cf3572f2762ef1304c406cf6d4f5ee8ee8719ef289a3b75a8323aa in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0dcc8c973ba119a0fb5275114fd0456179bba1132bdc69f2afa4e1c4a235c540`  
		Last Modified: Tue, 19 Nov 2024 17:38:52 GMT  
		Size: 31.0 MB (30980838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789bf3edf440eb67602bc2c6173f31d3292b752b03bbf690c473a5038b858343`  
		Last Modified: Tue, 03 Dec 2024 06:44:43 GMT  
		Size: 14.3 MB (14321082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5bbefa7271de6bbbb050f868fd8c93c0b06bd8ac418f05ca3f557ad4ffd224d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf1b461033a2a3da9c2e37123ce819ca1a426d0f9fa1355d6598f08a1fb7183d`

```dockerfile
```

-	Layers:
	-	`sha256:e5d6092dc376a01da04528366bd6a4155bdbd5514aefb3e96208b9c850a66408`  
		Last Modified: Tue, 03 Dec 2024 06:44:41 GMT  
		Size: 2.5 MB (2454241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:899d9df5d9acb6c3234e977feabe3521391b2a97fe481da2ee4a03d84d8c7b21`  
		Last Modified: Tue, 03 Dec 2024 06:44:41 GMT  
		Size: 7.0 KB (6991 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:55352dd01a4d52c21cb5808514851662c32e697c5c36bc01c77f7c8b8fc5e27a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44981596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db79a0430094f1439e67e85049cbcca6769dedd36964c969dabba0a35eee024`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:1c391e128b3c5e552a1401f9520290446bf94ba089c2d74a5d661001d3d8b60c in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:755503a8fb36d6a0d08275c3792ab81b69fdff95054dff0aa932d6dc30107609`  
		Last Modified: Tue, 19 Nov 2024 17:38:58 GMT  
		Size: 30.0 MB (30020826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35190d0c1306f85de6133cb1ceca330cd03ee2f6baead3be847b0c8e4273f57`  
		Last Modified: Tue, 03 Dec 2024 04:10:05 GMT  
		Size: 15.0 MB (14960770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e5ad476e5c52f4c913df3940b7db405f957a1c7cf075189daca46398c5c33a69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2469946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d5622a0d16455c00e33057665c5693a31579b1b6c611cbaf3ecb2e447535492`

```dockerfile
```

-	Layers:
	-	`sha256:d7201d5e83923888de806997daab87596447e51f8b6cf2d6f885c539143f49ac`  
		Last Modified: Tue, 03 Dec 2024 04:10:05 GMT  
		Size: 2.5 MB (2462987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f33aaa2db5113f324f58022583f74349375ad676c84dff81388db1011b74a55`  
		Last Modified: Tue, 03 Dec 2024 04:10:05 GMT  
		Size: 7.0 KB (6959 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:24.04-scm`

```console
$ docker pull buildpack-deps@sha256:722970809edab74b0a85408f69d6ae9af04fbc3ad50f8ee4596345f89baa01a7
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

### `buildpack-deps:24.04-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:6d50b3e92542a04322fbc2914286d49e5915ddaffcf191c07e06661fad7f646a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88764230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131aa2852b90e0ada1162bf44687db88ffbac12639b7a8d6f057c2bfa7a0354e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5235aa939f41c34b69f4fe37736745fde8e1a4676950add7459e7b957c4cfd55`  
		Last Modified: Tue, 03 Dec 2024 02:28:51 GMT  
		Size: 13.6 MB (13617608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48cf16388a9a3471d6a91777a42a673b8db99767b831de048212ce4136744cd4`  
		Last Modified: Tue, 03 Dec 2024 03:17:02 GMT  
		Size: 45.4 MB (45394654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e3f04deeea996b84aa1dd1dfee85837b0a2f1bfe56fd34469d8686c2b2df4193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5083420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8858ee1939cf86150c60e81cac0c8fb87a608744c7ec96f3a8af6fa531324a19`

```dockerfile
```

-	Layers:
	-	`sha256:addc9e17fc74d7040b9ab7245bbaadcde580f924bbad026c4091e477cab1bf6e`  
		Last Modified: Tue, 03 Dec 2024 03:17:02 GMT  
		Size: 5.1 MB (5076115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bd67f97ec250bb62ffa5140cbe45a6491aab2a87e36613851e4c406872536f6`  
		Last Modified: Tue, 03 Dec 2024 03:17:02 GMT  
		Size: 7.3 KB (7305 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c2fe6de00fc138830d287fb0dc0f6b911dca32d344e4701eed3aa2b0c86a015f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88588787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60bcc54a6f059b5e96eb76abd6d7c54f157230e6b9450227a6df12a929e8bbf5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:786ab064bf2d82faf7ca3fbb6c2e6983bbdb3228800d6d64e5dec4a67f778a7a in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b25adda5718ef4d96696ce8f0e58cde58fbe9977456036f84293bba8f26c5567`  
		Last Modified: Tue, 19 Nov 2024 17:38:39 GMT  
		Size: 26.9 MB (26869639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f072a621863f98c6e93487af2148d3199cc2cf579bfe20feab8e50641003f0`  
		Last Modified: Tue, 03 Dec 2024 07:39:05 GMT  
		Size: 12.8 MB (12774963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335cf1f7da64ab01e02577f00ca7c83d14ba94593eeb2b94921fa0dd578a4e4c`  
		Last Modified: Tue, 03 Dec 2024 17:19:41 GMT  
		Size: 48.9 MB (48944185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:36916e586b63927eb00c8e6fc63fbdc374caea9a8df5db0df3a2bab37d3fec16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5084774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:365716965de5497a66aa242643334c3251b18756a3f44fc87b04e53b504d7903`

```dockerfile
```

-	Layers:
	-	`sha256:dc29ff92dbf3d2987aeef7bb9b8c549b1acc9af15014d4fe428d6a049cd9aa52`  
		Last Modified: Tue, 03 Dec 2024 17:19:39 GMT  
		Size: 5.1 MB (5077409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45fd512c1fead54e3108bb7fe7ec75f4060f3a0fd9edbf39d3c7428b311bd686`  
		Last Modified: Tue, 03 Dec 2024 17:19:39 GMT  
		Size: 7.4 KB (7365 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:69e40459579cbc0b138d9a20aaf0d3486dc42eb8b3a836e30cf427ab277de42b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87703768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c718600a8934d0b44f5569edde9431dc42eb30d26710bcc02a6d96f08bac5ffe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331da7d4a8631a606292d353129b9398a4db3f2798d686a807920d0a81e2c741`  
		Last Modified: Tue, 03 Dec 2024 05:40:42 GMT  
		Size: 13.5 MB (13452932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af04d25eb37c1d037171f5c201d5753407b0902b0f09c9b548efca5b1d914b62`  
		Last Modified: Tue, 03 Dec 2024 11:53:13 GMT  
		Size: 45.4 MB (45358165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:eb791a3b3cca1c3b2935910956af05c9087a209ff88a70ac70ef9205d8c79156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5090699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bef7269cc872128c8e5932c12378ebd1a268b567dc24551c926c91fa85e57050`

```dockerfile
```

-	Layers:
	-	`sha256:1ada12157811656b092a572f885b9ac7f9ea75283b5e90e82f9b3c671db09087`  
		Last Modified: Tue, 03 Dec 2024 11:53:11 GMT  
		Size: 5.1 MB (5083314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a31276f86b42d0658076bc44da5d06e42007914f26474b55afed3926035e7dad`  
		Last Modified: Tue, 03 Dec 2024 11:53:11 GMT  
		Size: 7.4 KB (7385 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:384d387998aa64a6f5d109bff122bdea8b9ab1963ae663995810afaf4a7d2428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100926550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6946101467ca3a91ca35f8d779b675ebf382a27e84ec752d94adbf307d0d7407`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb006e560e9a807b6372fb925c588d9d83a6052a65248653a1f5708527a24d4`  
		Last Modified: Tue, 03 Dec 2024 04:39:54 GMT  
		Size: 16.0 MB (15980138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9deff409e8ce76af2a5a7095a7e708fdcadb9e212359c8655149b857100b432d`  
		Last Modified: Tue, 03 Dec 2024 09:46:22 GMT  
		Size: 50.6 MB (50557592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c0e1990e1e896cfb17ed7ecabf67bc00438fc31b10d3dfff8831d270ae4fc861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5091142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa976460f062d23b11e4b7e0374784807e804a1c84c7238400828ea4535f2be5`

```dockerfile
```

-	Layers:
	-	`sha256:98cb5d30b844718d1d8bbdaf254185490e39d7b24a525348d26bbaa41ef83c76`  
		Last Modified: Tue, 03 Dec 2024 09:46:21 GMT  
		Size: 5.1 MB (5083805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37f843b90490e92473c16e8e26ee5619d996af35343267bf4b7e5e268185f27b`  
		Last Modified: Tue, 03 Dec 2024 09:46:20 GMT  
		Size: 7.3 KB (7337 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:bfb5191debc6043e213d5fba8deaf56abc330de1eae2e2d4fa1eb38d09f1863a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99158620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1c3db312baebc205d4ae5320db8ea455b1d2c806396175a7f8f3d5d53560d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:23c2e341d6cf3572f2762ef1304c406cf6d4f5ee8ee8719ef289a3b75a8323aa in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0dcc8c973ba119a0fb5275114fd0456179bba1132bdc69f2afa4e1c4a235c540`  
		Last Modified: Tue, 19 Nov 2024 17:38:52 GMT  
		Size: 31.0 MB (30980838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789bf3edf440eb67602bc2c6173f31d3292b752b03bbf690c473a5038b858343`  
		Last Modified: Tue, 03 Dec 2024 06:44:43 GMT  
		Size: 14.3 MB (14321082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f505f2c8e1079fb73360d2ba6b4c3130e06fd9586abaa35474f69fd6f08ac0c3`  
		Last Modified: Tue, 03 Dec 2024 09:51:22 GMT  
		Size: 53.9 MB (53856700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2ad46ad8d7e5e2137bad7101c0d437b7fee331f0b8d0e6350b5887027183d1f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5073996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d3bd34af4146e39294b5bbb3fa5cef688457671071e5506732c9f6c13431c6`

```dockerfile
```

-	Layers:
	-	`sha256:0a4cc0ae30668e7591cd209c89d192583fba68aabb43372e03f01edab1d00e88`  
		Last Modified: Tue, 03 Dec 2024 09:51:14 GMT  
		Size: 5.1 MB (5066659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b02388bcac06974d94d50c9bf05df475bfa01487bba4a6f5101eb76f87477102`  
		Last Modified: Tue, 03 Dec 2024 09:51:13 GMT  
		Size: 7.3 KB (7337 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f6aa36b071cd1ed3f37f0b7bcc5a2325c8ea64c33d9746502b6992862e3e3cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91894284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac5d4c058ad27c00d235e7baf11e7972e559d439a340e03f8b86d1a4b2fd0639`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:1c391e128b3c5e552a1401f9520290446bf94ba089c2d74a5d661001d3d8b60c in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:755503a8fb36d6a0d08275c3792ab81b69fdff95054dff0aa932d6dc30107609`  
		Last Modified: Tue, 19 Nov 2024 17:38:58 GMT  
		Size: 30.0 MB (30020826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35190d0c1306f85de6133cb1ceca330cd03ee2f6baead3be847b0c8e4273f57`  
		Last Modified: Tue, 03 Dec 2024 04:10:05 GMT  
		Size: 15.0 MB (14960770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05107eaec609414c9540f16903f6f4fed09e9055d47bca5a3188db8c2f781888`  
		Last Modified: Tue, 03 Dec 2024 07:57:25 GMT  
		Size: 46.9 MB (46912688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6ed16ad608670de1d059165b62dc4296f911a80f55ef213cb9ac578a594dcd03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5085757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3f3c4fa5ca2bd0225ba612c07217a53faef57db897899cceeaafa4923145fb`

```dockerfile
```

-	Layers:
	-	`sha256:afe48d2c0a0654f448b9f66dbab36a88607d875e7c911c05e8c35914c9cffc68`  
		Last Modified: Tue, 03 Dec 2024 07:57:25 GMT  
		Size: 5.1 MB (5078452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95f4e0a101ac487e58274d0e6e005419118d9466a66d95d30a72475ea5022f9a`  
		Last Modified: Tue, 03 Dec 2024 07:57:24 GMT  
		Size: 7.3 KB (7305 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:24.10`

```console
$ docker pull buildpack-deps@sha256:b08deb0d33d7f80992b25716c4fac0662387ea504455b28b26f1033220fe7096
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

### `buildpack-deps:24.10` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f2d468863910d62e7330375fd0395f4ad0779ec27a3ee0b00c49b0ea6b23afcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.2 MB (286231930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b5a46626d0cc438768876575effe13f925efd7379f00d0400c7b3741369191`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:08360137caccff53ccad4b814b2e19f27aa9fe2a71175550a7f6b13fe243924d in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:31734b193a814b7d6f96f0d11a89c942ca61ac79d819105323c548bf31f98613`  
		Last Modified: Wed, 20 Nov 2024 04:18:12 GMT  
		Size: 30.6 MB (30601312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb3a0dc114c54fd18d42d481f5d85eb84000d5cd297bd2f753d1290eb36719c`  
		Last Modified: Tue, 03 Dec 2024 02:29:09 GMT  
		Size: 15.4 MB (15374140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64ddd91578315b54cf47f01baf6ea302d702c1bc46efefdcad51af4f6a7812b`  
		Last Modified: Tue, 03 Dec 2024 03:17:12 GMT  
		Size: 46.5 MB (46491318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4065e49aa231bcf1f2eedf5b60edcdd89df6863377a6110a492b6bb6c2daf66`  
		Last Modified: Tue, 03 Dec 2024 04:32:09 GMT  
		Size: 193.8 MB (193765160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c5312bff979618340f2d1556c3453421e1e55f873bf4efe7ddc7d25705766245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11369581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8527a70c975c34f4def1074b8ee7f1aabf34798e8772d52d20aedd7f33eeda4f`

```dockerfile
```

-	Layers:
	-	`sha256:c5b9641e0dec7e5403d1612f3ae20c9d246f99bf083b7747bf196a3cfd9f730b`  
		Last Modified: Tue, 03 Dec 2024 04:32:07 GMT  
		Size: 11.4 MB (11359378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07ec353f310cb5323bbb08e4760de895cdc7de806f12f1ba46515611d0372297`  
		Last Modified: Tue, 03 Dec 2024 04:32:06 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.10` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5e6c535541d799fcadbade99bcad57a32135142047242193e8c6c420b1aa93e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 MB (248408833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9875927388483d1bb47a79ad5e415dfed6a83a9f1b688632c124b47324a667c5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:5cf848783aed3abcaefd540a7a70f443ef2bead6c50d01e0a72cd1aa6f542081 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c553618cfeea14cb253bd7777b2e3299019b3065e1cb073744b43353379582a7`  
		Last Modified: Wed, 20 Nov 2024 04:18:39 GMT  
		Size: 27.5 MB (27546971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a00677e72221e7026f8e6b0ed5b47e7316c84195a5d85d7c2cf005d741e670`  
		Last Modified: Tue, 03 Dec 2024 07:40:05 GMT  
		Size: 14.1 MB (14060900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c52f0d85713a2f01f551bbf8afba0de5917d8a73a492b3fca6575c2696d83eb`  
		Last Modified: Tue, 03 Dec 2024 17:21:00 GMT  
		Size: 49.5 MB (49462929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a1ade74a0a0a3cb322d91a5b98afa058c0268e2ceebea121af375e348bed51`  
		Last Modified: Tue, 03 Dec 2024 20:20:38 GMT  
		Size: 157.3 MB (157338033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c9b4c62d6c5815bea5eb2dd0d5b3c2d844959ccd8f09eab126117f4c48a373a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11149176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5650dba2bfa8ac954879544aa3ba225de09a50747a66b3d7deb6b194e3a56d`

```dockerfile
```

-	Layers:
	-	`sha256:998154eeaa3b2c9daa4fa63ce0763edc00fe6c7a8960cf03ff43f5137b32c574`  
		Last Modified: Tue, 03 Dec 2024 20:20:35 GMT  
		Size: 11.1 MB (11138913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:065d062a0d03124977ef15b202544942d5dcd3547f37a77db3a62bb85fa307b8`  
		Last Modified: Tue, 03 Dec 2024 20:20:34 GMT  
		Size: 10.3 KB (10263 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.10` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:42e5d1c5d818a085ca5eb3e65007a5613672626901be13287e2eb8977e12cbb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.9 MB (279937838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d17ee958e00a1a6edf4a25addf51b7d7cbe299dba12ade1e5849aa5e006b1f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:11edc0b5b8a0810c86ff8de1ece47e84856118afa9f296152b12c0bdabf33154 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6d229850a7784435237486a1406ffb5a4f0a4ac3b993928d18b30ad6853c6845`  
		Last Modified: Wed, 20 Nov 2024 04:18:26 GMT  
		Size: 30.3 MB (30284785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c08bcb2cbebb6d9db3a5ad2c52e975d21aa32088786303f6c521a0bb1f93f0`  
		Last Modified: Tue, 03 Dec 2024 05:41:40 GMT  
		Size: 15.1 MB (15147474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be5c9e4ce5805ad177f3aba8a70b5f1255051eb50b349f3819d9ee550186986`  
		Last Modified: Tue, 03 Dec 2024 11:54:23 GMT  
		Size: 46.4 MB (46423354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f144299644d986372fc7ab74c3e363056d5b1e93d2c8b4c856cb8d36c2a238d`  
		Last Modified: Tue, 03 Dec 2024 16:33:41 GMT  
		Size: 188.1 MB (188082225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a454f0ce4fefaaaf46eb66f48c64c50fb9f2005aad6a461386bf2369f9787302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11446009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73565036103c3e95c080e8ac4cd9db7e4f3901ca503409000edab5a9833aa071`

```dockerfile
```

-	Layers:
	-	`sha256:d9331ccd4adb34076f9c1de43104541397d3f4cad61b4f3912f2f5926f05f390`  
		Last Modified: Tue, 03 Dec 2024 16:33:37 GMT  
		Size: 11.4 MB (11435726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a806f212f7a6ab953efafd515e1def1e01f226f4883138d23f91068b4ae8cdcc`  
		Last Modified: Tue, 03 Dec 2024 16:33:37 GMT  
		Size: 10.3 KB (10283 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.10` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:07f2d3407c4086803bd20bacc23257dd31fd4031c8e86b5fb5c3620df1b3d0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301587069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7e09496b7805c1cef26d55c8f0982819a893d10d3d489717c57ffae9df60b9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:c92b611280c7d224d58f2a2a7dfdc19380dda99a38e10495643ec0b43d2f3cac in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2039ab37391bfea5163cf2545fcb585344c981096040149e81aec9301f35f97b`  
		Last Modified: Wed, 20 Nov 2024 04:18:53 GMT  
		Size: 35.1 MB (35063190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335ed3d865eafcfc72459a536871a40009d4a399d947a0418657fd44f442c19d`  
		Last Modified: Tue, 03 Dec 2024 04:41:29 GMT  
		Size: 17.2 MB (17249971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19dd08a4345b11dbad4e6464f658a55387f7b1317148b558d997474d998e8fe5`  
		Last Modified: Tue, 03 Dec 2024 09:48:00 GMT  
		Size: 51.8 MB (51759651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1e7838794de9de838af4f642fa9a2c7787fc250fe2e6ea745400b6b118189b`  
		Last Modified: Tue, 03 Dec 2024 16:33:24 GMT  
		Size: 197.5 MB (197514257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a639d44639e78ee7c6cd1b7d424ba1c4d797a91d6c804122fb85a0d4e7fd4696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11361895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896d60018831607d6cf171e3307e4738e1ca84613d5375a7c6513eb779e8d90e`

```dockerfile
```

-	Layers:
	-	`sha256:1245cc6f4d67addb23dc7ac9e404400d3a787b5fa977037662ca4247d44923dc`  
		Last Modified: Tue, 03 Dec 2024 16:33:20 GMT  
		Size: 11.4 MB (11351660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76663542be6a991f1c7a41dca7b3cd4aab48b5c7bdb938e0deaade848e7b5561`  
		Last Modified: Tue, 03 Dec 2024 16:33:19 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.10` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8d5a7f2f0db10b545763695bb927af0842ee2cfba1caefe2966992777d27afb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.2 MB (378202631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c665ea6044af20b4b12d2b65300f30d5b7695ba2bc0e5cf82b306177f50003f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:76a233bff3b463f93cb832f44963527276c1cd491cd0a75c9c5d2eac75da2380 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9d51f6335bdd76dd9dcfd4d3eaa2272acccc262c17300716acd3ffb0ec5f5846`  
		Last Modified: Wed, 20 Nov 2024 04:19:07 GMT  
		Size: 31.8 MB (31787958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48e90448070e192152f471d2c8fd1cfc67ec60c6cb742a212ead9de030d94d6`  
		Last Modified: Tue, 03 Dec 2024 06:47:45 GMT  
		Size: 15.9 MB (15890462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4180e9749ee9c2cd33764d68a8a49f4513db415bcf81e499f6bd3b0b7312f056`  
		Last Modified: Tue, 03 Dec 2024 09:56:53 GMT  
		Size: 54.6 MB (54615995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d229559deb983f34d263c1186e731a20b3d9db40451b4063f3de51f6fc326219`  
		Last Modified: Tue, 03 Dec 2024 11:31:19 GMT  
		Size: 275.9 MB (275908216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4e00820dd6ff6beb8effa14dc6357c1c4e04d951a758caacf793ec7dd2b33fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11417908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:664c2c34bd590b1f1e97e2d7910c02c94c1aeca1d6b7bba8fc435b595c252143`

```dockerfile
```

-	Layers:
	-	`sha256:d75666c5ed1b37cd483e2f968e564cfb994c3b7cb8acfabb93f8b56c5b7bb8d5`  
		Last Modified: Tue, 03 Dec 2024 11:30:44 GMT  
		Size: 11.4 MB (11407673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00bd0cdc0851b621344bcdeb7d234bb1dd772ad6c7004714a0e5ee05418e0d98`  
		Last Modified: Tue, 03 Dec 2024 11:30:42 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.10` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6f95adf3a52b8a9b79ba8f14c9b9ceddd5c0d7e858dddfc5423b476ef0221492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265507437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fcdc2270c2fb7756c24dfddace9096deec97390161569734095a649c3603a4e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:d8a0fd6e6a1b5571de35cb60b4e05523a0290523534ad63464fdf47dfbe0b041 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8ccad27fc3ed57037242d8c7dde5d5ce195749a63f65f7d9a663f7b822c4429a`  
		Last Modified: Wed, 20 Nov 2024 04:19:18 GMT  
		Size: 30.8 MB (30775034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d6a6da1657d09f717e7f94493d3e0563278583e47322d423316da636b93135`  
		Last Modified: Tue, 03 Dec 2024 04:11:01 GMT  
		Size: 16.9 MB (16937481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae51c456fa63fca49c43c89a34927e42baace55350a312e11092478ffa7894cf`  
		Last Modified: Tue, 03 Dec 2024 07:58:31 GMT  
		Size: 47.8 MB (47774022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9602e6e79d8a9afdd7c8691bf80181cc5be4942308ba620ef74fe70421e13ce3`  
		Last Modified: Tue, 03 Dec 2024 10:59:07 GMT  
		Size: 170.0 MB (170020900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c6c0e1f425fdb1d84c16cbbe7a6878cd2598f37f3526144365efe934b8b8a0be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11168896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb66150459757f9898298255cd0cb66c204688a4cf85ae139b5689db0254223`

```dockerfile
```

-	Layers:
	-	`sha256:7d36c1b3ced50159e6fdb1185db60346dc278bb5afe7507c3174f447100ae1e0`  
		Last Modified: Tue, 03 Dec 2024 10:59:03 GMT  
		Size: 11.2 MB (11158693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0de5e93240ee180a47ee52972d2c014e4e8cd4da6ee12024db5bd71f405d3966`  
		Last Modified: Tue, 03 Dec 2024 10:59:03 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:24.10-curl`

```console
$ docker pull buildpack-deps@sha256:5a54dd814c6322f357e43081a669e905c192ed0e4c17cd27e064d0def5fa804c
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

### `buildpack-deps:24.10-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:ea60a237b355b924d37dfe9aac67a3852d8b7c482233cb73265efeb09ae05ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45975452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c44578c4539dd052a272af1de7f824a2b22957771ec3454116fb0e0cdf6b203`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:08360137caccff53ccad4b814b2e19f27aa9fe2a71175550a7f6b13fe243924d in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:31734b193a814b7d6f96f0d11a89c942ca61ac79d819105323c548bf31f98613`  
		Last Modified: Wed, 20 Nov 2024 04:18:12 GMT  
		Size: 30.6 MB (30601312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb3a0dc114c54fd18d42d481f5d85eb84000d5cd297bd2f753d1290eb36719c`  
		Last Modified: Tue, 03 Dec 2024 02:29:09 GMT  
		Size: 15.4 MB (15374140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:957effd5c0cfdec1d2236e1c818d395fb9708f82fde1c0159a51006c10c4db0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b38744fcc95f8c64b212f80dbbf264a20abc2d1a16ea8ec9ae244f28dd1540`

```dockerfile
```

-	Layers:
	-	`sha256:8a09e8f1e8d49e683c807fbae21bec087375e537be6f69b9ce9487ac6f62914e`  
		Last Modified: Tue, 03 Dec 2024 02:29:09 GMT  
		Size: 2.5 MB (2458673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79e22805520c08d0bf06b9f9f7cb9b9d661114bc018017f25a45245d6f198ab7`  
		Last Modified: Tue, 03 Dec 2024 02:29:09 GMT  
		Size: 7.0 KB (6978 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.10-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:73c945b3d503d44be0dd39a8a3f5396dc07aa17344ef7f13d50dc5a35233c306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41607871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2428ec7695bd98edafe42303b40ca4ba3bd6cb2cd70a531dc2778e08123a19af`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:5cf848783aed3abcaefd540a7a70f443ef2bead6c50d01e0a72cd1aa6f542081 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c553618cfeea14cb253bd7777b2e3299019b3065e1cb073744b43353379582a7`  
		Last Modified: Wed, 20 Nov 2024 04:18:39 GMT  
		Size: 27.5 MB (27546971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a00677e72221e7026f8e6b0ed5b47e7316c84195a5d85d7c2cf005d741e670`  
		Last Modified: Tue, 03 Dec 2024 07:40:05 GMT  
		Size: 14.1 MB (14060900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:64158a88b94a807bc6c406afd30c1103e0a1f68b5ac32de7806d44a2139a2b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9439d1914bedbefbf8318533d3206dff74db23f82d6ecd51cc21da18bbb6242e`

```dockerfile
```

-	Layers:
	-	`sha256:b009ed268a6a16395e4b189138dfb01b08a1e04b7a9716b204143d5a7732e0e0`  
		Last Modified: Tue, 03 Dec 2024 07:40:05 GMT  
		Size: 2.5 MB (2460973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6749341c5939dcf0a0a5bfddb6738504b32558cb0fcd532ec7cfe233188ea4f2`  
		Last Modified: Tue, 03 Dec 2024 07:40:04 GMT  
		Size: 7.0 KB (7038 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.10-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f09db2479b3d7468d20c049a2ea861604f9a93f92357f5556e5953ada059807a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45432259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d138568e5d92a875546b89405710cf9c20c0cb837387f6e522e2dd6d78552a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:11edc0b5b8a0810c86ff8de1ece47e84856118afa9f296152b12c0bdabf33154 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6d229850a7784435237486a1406ffb5a4f0a4ac3b993928d18b30ad6853c6845`  
		Last Modified: Wed, 20 Nov 2024 04:18:26 GMT  
		Size: 30.3 MB (30284785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c08bcb2cbebb6d9db3a5ad2c52e975d21aa32088786303f6c521a0bb1f93f0`  
		Last Modified: Tue, 03 Dec 2024 05:41:40 GMT  
		Size: 15.1 MB (15147474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:302f64a92207589244d087350938653e787432e5ec6c888242a21c9244d5d2aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5084369ecb31ed6773a085b710f5afb7f8303a0ea405410a36fce2bbadc1fd91`

```dockerfile
```

-	Layers:
	-	`sha256:9b2a5e54b80389f06a288d3c2d31dd9785df28e6b3e45c1c02bb41ec2f5f7e0d`  
		Last Modified: Tue, 03 Dec 2024 05:41:40 GMT  
		Size: 2.5 MB (2459730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b10471618780d2cd17e1eb02c1f75d997b02047f3a6cce0d7ddabbb9a94ed840`  
		Last Modified: Tue, 03 Dec 2024 05:41:39 GMT  
		Size: 7.1 KB (7058 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.10-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:afcf6137703d492a678411153ac8bf0b6e55855e6d12c748e94ee79e57c7daed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52313161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e08b55ac61d2952ce86a0a9078c907bcae065e32f2b400770ed5b6a16d5bae4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:c92b611280c7d224d58f2a2a7dfdc19380dda99a38e10495643ec0b43d2f3cac in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2039ab37391bfea5163cf2545fcb585344c981096040149e81aec9301f35f97b`  
		Last Modified: Wed, 20 Nov 2024 04:18:53 GMT  
		Size: 35.1 MB (35063190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335ed3d865eafcfc72459a536871a40009d4a399d947a0418657fd44f442c19d`  
		Last Modified: Tue, 03 Dec 2024 04:41:29 GMT  
		Size: 17.2 MB (17249971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7fbed868bdfb8c0fa54ac0a7279ca61b33eeed3c2a9e726ae9bb38d573e0b530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2470166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52f7fe4f05dc1680e076f9aef3d1bc2134faee073b9ba0bc18b05119256d2fcb`

```dockerfile
```

-	Layers:
	-	`sha256:023e9cee20e6331d60b57fb976920eb158cbbd04e0fd5b4e078a377c498a3564`  
		Last Modified: Tue, 03 Dec 2024 04:41:29 GMT  
		Size: 2.5 MB (2463156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e962bf2a789e982d8814853042d4eae3e2593e723f80be215416b6b2339747f3`  
		Last Modified: Tue, 03 Dec 2024 04:41:28 GMT  
		Size: 7.0 KB (7010 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.10-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:935ce885aaf07bbae20dbdde74e64c6259174a52c31411d4d72246b46db888f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47678420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049e555341f0ccf882cd39e4a089dd2ca7abf815adc24e9ecd509f2c07e2dd03`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:76a233bff3b463f93cb832f44963527276c1cd491cd0a75c9c5d2eac75da2380 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9d51f6335bdd76dd9dcfd4d3eaa2272acccc262c17300716acd3ffb0ec5f5846`  
		Last Modified: Wed, 20 Nov 2024 04:19:07 GMT  
		Size: 31.8 MB (31787958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48e90448070e192152f471d2c8fd1cfc67ec60c6cb742a212ead9de030d94d6`  
		Last Modified: Tue, 03 Dec 2024 06:47:45 GMT  
		Size: 15.9 MB (15890462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4d2b49e90550c9c246be3d0a4bf462f6acedb554909b1dfcb1a519d9c36d4559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f301393f12913e8c6105d70130106fd53d8bdce15d8a7c4363bce194005f44`

```dockerfile
```

-	Layers:
	-	`sha256:96472992941cb5871f2eec833e53855a80be80e7b2a9db41e05de788c055a6c6`  
		Last Modified: Tue, 03 Dec 2024 06:47:43 GMT  
		Size: 2.5 MB (2452760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba079d972f1aa5b3c65cf4d4c0a20c942d9a5a9872a12ec2394241b40fa083b3`  
		Last Modified: Tue, 03 Dec 2024 06:47:43 GMT  
		Size: 7.0 KB (7010 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.10-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:474003861666c2558971d1f219ca0cf541319c9cc0ae74cec1f095764456d6bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47712515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bbdf4934968526ebef31cbef00996bd1644b8b673488498fe04ef2f4ae2a03d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:d8a0fd6e6a1b5571de35cb60b4e05523a0290523534ad63464fdf47dfbe0b041 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8ccad27fc3ed57037242d8c7dde5d5ce195749a63f65f7d9a663f7b822c4429a`  
		Last Modified: Wed, 20 Nov 2024 04:19:18 GMT  
		Size: 30.8 MB (30775034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d6a6da1657d09f717e7f94493d3e0563278583e47322d423316da636b93135`  
		Last Modified: Tue, 03 Dec 2024 04:11:01 GMT  
		Size: 16.9 MB (16937481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9ccdc5a771ad4d7e34fba168ad55fa04ffbdc5e1cd4d33921e18e2bfc7cfe988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e46556e422491046164719725145041e108a986a7b989584413193fdb296ff3`

```dockerfile
```

-	Layers:
	-	`sha256:1392030aa2010eab698fd29006239c1c0ace7587f2c6563790bc468c30ba86b0`  
		Last Modified: Tue, 03 Dec 2024 04:11:00 GMT  
		Size: 2.5 MB (2461504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3873b36bfe6641bfeee779ada1358ed661c445aaa055118aaf947bd635bea5f`  
		Last Modified: Tue, 03 Dec 2024 04:10:59 GMT  
		Size: 7.0 KB (6978 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:24.10-scm`

```console
$ docker pull buildpack-deps@sha256:0325cd014a1561ff9039b66c2bf45acf5981fde10dd02e119c30705e51c4b862
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

### `buildpack-deps:24.10-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:563e8451c6e61acd1253e9387da1481be89ae5e02a0111a8fc481ece758ea0eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92466770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d68ca44aa08186ffc80697404b975b0f1762747a215809a8a9f250099ea38b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:08360137caccff53ccad4b814b2e19f27aa9fe2a71175550a7f6b13fe243924d in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:31734b193a814b7d6f96f0d11a89c942ca61ac79d819105323c548bf31f98613`  
		Last Modified: Wed, 20 Nov 2024 04:18:12 GMT  
		Size: 30.6 MB (30601312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb3a0dc114c54fd18d42d481f5d85eb84000d5cd297bd2f753d1290eb36719c`  
		Last Modified: Tue, 03 Dec 2024 02:29:09 GMT  
		Size: 15.4 MB (15374140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64ddd91578315b54cf47f01baf6ea302d702c1bc46efefdcad51af4f6a7812b`  
		Last Modified: Tue, 03 Dec 2024 03:17:12 GMT  
		Size: 46.5 MB (46491318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8ba9fad56bedf47846b079812c8a6d4f47a1dc796f1dbccd5a2d1818033f9fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f725ce812a005ebd7092e7623bfe9c5a339b6bd4da22634dae370ff500604947`

```dockerfile
```

-	Layers:
	-	`sha256:c23bc9c092c296df444d5a1fbe7d557d5c72492a03d7b3b366f8a8106b1c9c9a`  
		Last Modified: Tue, 03 Dec 2024 03:17:11 GMT  
		Size: 5.1 MB (5090553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ba7f94c1ac96e0c4b0ea537df4662194ce9f2b029b822a146f047255b3af022`  
		Last Modified: Tue, 03 Dec 2024 03:17:11 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.10-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f35e17de918b1ab011fb1b0334a6c8c87fff4b4a798a2a2dd80bb307e39cdb6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91070800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27344efd4600537f2d0179a82ce6aa58a2d6a24a8cb1bc5ca2b9f675b5ba4d8c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:5cf848783aed3abcaefd540a7a70f443ef2bead6c50d01e0a72cd1aa6f542081 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c553618cfeea14cb253bd7777b2e3299019b3065e1cb073744b43353379582a7`  
		Last Modified: Wed, 20 Nov 2024 04:18:39 GMT  
		Size: 27.5 MB (27546971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a00677e72221e7026f8e6b0ed5b47e7316c84195a5d85d7c2cf005d741e670`  
		Last Modified: Tue, 03 Dec 2024 07:40:05 GMT  
		Size: 14.1 MB (14060900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c52f0d85713a2f01f551bbf8afba0de5917d8a73a492b3fca6575c2696d83eb`  
		Last Modified: Tue, 03 Dec 2024 17:21:00 GMT  
		Size: 49.5 MB (49462929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:321e47836c05fbb02e1fd02fcc1ddc2c3c9659ace387ed72c88a22a232eb575a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5099237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d40379b9a864667266d066d886c9bcad244b1e2b00a22868aeb7f34d7b32bef`

```dockerfile
```

-	Layers:
	-	`sha256:1ac741d22a8e2ee37128ae932b86c198778eea3fd1c9530edaa933db1bd2bcdf`  
		Last Modified: Tue, 03 Dec 2024 17:20:58 GMT  
		Size: 5.1 MB (5091853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86ff1a3ca795c61cc4e63a408b81086ade9a98c28eec81011f6ef2d2f5a94d23`  
		Last Modified: Tue, 03 Dec 2024 17:20:58 GMT  
		Size: 7.4 KB (7384 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.10-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cdd5ac19c22ca37622957e9f58856f47133d1411fe3dfd34e5351a0d0fb7618f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91855613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8100dbfdf0f4d4dff2d6d2e852b149139fee0a29c4411415c911d1f1751d4e6c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:11edc0b5b8a0810c86ff8de1ece47e84856118afa9f296152b12c0bdabf33154 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6d229850a7784435237486a1406ffb5a4f0a4ac3b993928d18b30ad6853c6845`  
		Last Modified: Wed, 20 Nov 2024 04:18:26 GMT  
		Size: 30.3 MB (30284785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c08bcb2cbebb6d9db3a5ad2c52e975d21aa32088786303f6c521a0bb1f93f0`  
		Last Modified: Tue, 03 Dec 2024 05:41:40 GMT  
		Size: 15.1 MB (15147474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be5c9e4ce5805ad177f3aba8a70b5f1255051eb50b349f3819d9ee550186986`  
		Last Modified: Tue, 03 Dec 2024 11:54:23 GMT  
		Size: 46.4 MB (46423354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:247fbd221ad5fefbf18c52d8696177a8e67b46e00e7d5e256a9bb950b590c27c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5105157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c6b74132fb1f57a9d10c9981fefad798e3ac9551eafd4bccce198df20b4cea`

```dockerfile
```

-	Layers:
	-	`sha256:5b41ccdf769d6aa00d98c9cdb9bbb11353d81d3f89b2d37beceb76d737d5c56b`  
		Last Modified: Tue, 03 Dec 2024 11:54:22 GMT  
		Size: 5.1 MB (5097754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:573bf2b358841fdfccaf73d76bb65caadd9092547578f7cb821e1c8bb50d90d5`  
		Last Modified: Tue, 03 Dec 2024 11:54:22 GMT  
		Size: 7.4 KB (7403 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.10-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a239a47dc8e5b6806865a5e03070765f807e7da9a0c102422dd3a07c529acd74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104072812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90eb7eda48c9009759efa5a71b21c19232dd9e939b9bfb8b227e2184996544a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:c92b611280c7d224d58f2a2a7dfdc19380dda99a38e10495643ec0b43d2f3cac in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2039ab37391bfea5163cf2545fcb585344c981096040149e81aec9301f35f97b`  
		Last Modified: Wed, 20 Nov 2024 04:18:53 GMT  
		Size: 35.1 MB (35063190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335ed3d865eafcfc72459a536871a40009d4a399d947a0418657fd44f442c19d`  
		Last Modified: Tue, 03 Dec 2024 04:41:29 GMT  
		Size: 17.2 MB (17249971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19dd08a4345b11dbad4e6464f658a55387f7b1317148b558d997474d998e8fe5`  
		Last Modified: Tue, 03 Dec 2024 09:48:00 GMT  
		Size: 51.8 MB (51759651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c130a7e829a6b443f2b97c312dd323c9a462ca1e026e197aadc5b21ecc986790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5105613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1625028337b25c7ac210d33078ca5ac38f23bfd2e34520ad48f429c8ca92ef68`

```dockerfile
```

-	Layers:
	-	`sha256:a3c2a14b768bf44d6822d31a9593eaf47e27792f166ba4409c25ab3efc284940`  
		Last Modified: Tue, 03 Dec 2024 09:47:59 GMT  
		Size: 5.1 MB (5098257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86c20aa62daf40d0f747e05c4aa0d8c6812e31a7c227af22143256968b2ff99c`  
		Last Modified: Tue, 03 Dec 2024 09:47:58 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.10-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:433d7c7534db974f6efa271e3c5a0f5a505951ec05bc1521bdc947528b7810b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102294415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ca9a8119745c25aeca54ed77326269bf0a54ea4e69be1a42f0f6019dc22d93`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:76a233bff3b463f93cb832f44963527276c1cd491cd0a75c9c5d2eac75da2380 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9d51f6335bdd76dd9dcfd4d3eaa2272acccc262c17300716acd3ffb0ec5f5846`  
		Last Modified: Wed, 20 Nov 2024 04:19:07 GMT  
		Size: 31.8 MB (31787958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48e90448070e192152f471d2c8fd1cfc67ec60c6cb742a212ead9de030d94d6`  
		Last Modified: Tue, 03 Dec 2024 06:47:45 GMT  
		Size: 15.9 MB (15890462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4180e9749ee9c2cd33764d68a8a49f4513db415bcf81e499f6bd3b0b7312f056`  
		Last Modified: Tue, 03 Dec 2024 09:56:53 GMT  
		Size: 54.6 MB (54615995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:245d67b3be9b6d8a36b5477106bc596ada0fed35d74e3e1a31a6a15a7046e41c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5088461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd75e0600209041192ec38179e6dfae3df9f1dc2525c0c16567bc7347656842`

```dockerfile
```

-	Layers:
	-	`sha256:9d4e7dcb1858d2f2531abf6ef24471fb2839217b70f08b487c477e1dfd58b118`  
		Last Modified: Tue, 03 Dec 2024 09:56:46 GMT  
		Size: 5.1 MB (5081105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e42cb4187568748dbfad0592a9dae3060f3ea3d1ca9bd6b07064ed838f66c8e5`  
		Last Modified: Tue, 03 Dec 2024 09:56:45 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.10-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6a9b27f24dfc6b4b5e36fc6f6151bb1580c136eb5a093d2d23f101392f7a30ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.5 MB (95486537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04161d746ba9ccae4b062c0456e0a82b55715a96f941ea113ee86cd4330059b5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:d8a0fd6e6a1b5571de35cb60b4e05523a0290523534ad63464fdf47dfbe0b041 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8ccad27fc3ed57037242d8c7dde5d5ce195749a63f65f7d9a663f7b822c4429a`  
		Last Modified: Wed, 20 Nov 2024 04:19:18 GMT  
		Size: 30.8 MB (30775034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d6a6da1657d09f717e7f94493d3e0563278583e47322d423316da636b93135`  
		Last Modified: Tue, 03 Dec 2024 04:11:01 GMT  
		Size: 16.9 MB (16937481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae51c456fa63fca49c43c89a34927e42baace55350a312e11092478ffa7894cf`  
		Last Modified: Tue, 03 Dec 2024 07:58:31 GMT  
		Size: 47.8 MB (47774022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:85a4c838344e21fdd6d0f53cf053cf9b033e8b5342d575dc09a6fc4a6355265a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5100212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690aa5a5d111b8e111274bdd5677c6c857f256dd71b29eaf8361700dd37e8047`

```dockerfile
```

-	Layers:
	-	`sha256:25b383443ef461e858ce8f8bd24de079c904448278eddb7473125e532a039dda`  
		Last Modified: Tue, 03 Dec 2024 07:58:29 GMT  
		Size: 5.1 MB (5092888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d29ee9c23c653e4f2f33a482a3aeb189af8c6d4b173b4ee25bd0046348f82cdb`  
		Last Modified: Tue, 03 Dec 2024 07:58:29 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:bookworm`

```console
$ docker pull buildpack-deps@sha256:08d61da2eb4b661e95088f6999704803985f9bd7be23b3c5d7acce26cd2d521b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:bookworm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d7d6286e853f4cad78b9bacc9962ed13b3fae93c940bc951a473bf59f7f1e406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.1 MB (348060715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fffceae85e2c8f384b15a112be85e0068e283d5c5a20b5b6569421c24c2d23f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd71677db44bb63b94de61b6f1f95d5540b4ba2d6a8a6bc4d19f422b25e0c2b`  
		Last Modified: Tue, 03 Dec 2024 02:28:49 GMT  
		Size: 23.9 MB (23865876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551df7f94f9c131f2fec0e8063142411365f0a1c88b935b9fac22be91af227e0`  
		Last Modified: Tue, 03 Dec 2024 03:17:14 GMT  
		Size: 64.4 MB (64391508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce82e98d553dd62ca6a12bebfe83992ae9f9ae2748275e74b66a68cc094f868b`  
		Last Modified: Tue, 03 Dec 2024 04:31:20 GMT  
		Size: 211.3 MB (211306121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:22a0e2166ec5a7010a99174c9c5a4b92eb963a4c9b850ffc869e3ae672a4dd19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15507109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e432f0cc69ae07b4e7a310d24f8c071f75c5c31a75f80f558a30a9de615e1d90`

```dockerfile
```

-	Layers:
	-	`sha256:28a6ec7885ff79f670b70218ace6d532c8d6d4ee96e883c5eea08d923c243220`  
		Last Modified: Tue, 03 Dec 2024 04:31:18 GMT  
		Size: 15.5 MB (15496569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4526bb391e6ae70edf822e4ae77d44dce58b597a0adf995d87ca2061831eafe0`  
		Last Modified: Tue, 03 Dec 2024 04:31:17 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:5493da36ae1be44ee45e6f2a21e8eb7a1651f02980e111eb4b77fcc9de0a28a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.2 MB (315162492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1431cc1ab0a9621e4af9c733d49b9b97de509516dcbcd2b4c7b5b24edab2124`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a8ab0b752e573ceb3480052f24bc5fe3f4f4665c13a338db39c1d51f749528e9`  
		Last Modified: Tue, 03 Dec 2024 01:27:04 GMT  
		Size: 46.0 MB (46024374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff6779451547ba3f0647f15a65068290fed53b6a4ac506257de98e02857bea6`  
		Last Modified: Tue, 03 Dec 2024 05:23:42 GMT  
		Size: 22.5 MB (22540382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536c3cdef529f6d2993cf137c109a079266cd3effbffc602a136a2a60ee743a0`  
		Last Modified: Tue, 03 Dec 2024 08:40:08 GMT  
		Size: 62.0 MB (61996814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f689132b2bca5271eb471905bd9f8eeca3a8c74df88b2f1c85f7c43568f20e7f`  
		Last Modified: Tue, 03 Dec 2024 10:05:05 GMT  
		Size: 184.6 MB (184600922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9c4417f2e99d2695ac62a5424fe36d0c44cca3243f219bea81261e45beaf3b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15305788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153481c7eaadccabe24fb8bb164c037031dfbfdd932085326ec034ee9a386d98`

```dockerfile
```

-	Layers:
	-	`sha256:5aa70f8227a7f0f719920d36ec18fa8bd67edfb3e40293ba3716fb81b5aef76b`  
		Last Modified: Tue, 03 Dec 2024 10:05:01 GMT  
		Size: 15.3 MB (15295180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b8c7629b4f7dd625175f4302ed859bd0ad93857f5dbca59a30b70d298562b4e`  
		Last Modified: Tue, 03 Dec 2024 10:05:00 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:437e11f7b48081f9d3169d3f0b57c19ccbf5d90f78824f50b59ee48d4e0d9fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300850185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1add49ced00435fc4e660bf2b8efd6d6f065f88334295c8dc979ad7f0ab8297f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4d43724a324f138c88a78ca6df0a39ab6868bf1f121eb974439c5a51284e1ac2`  
		Last Modified: Tue, 03 Dec 2024 01:27:59 GMT  
		Size: 44.2 MB (44200109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff0e53b92c3d0f5c370d71aeac1be1d23e475f1afba41d896ace0ff6eeefc90`  
		Last Modified: Tue, 03 Dec 2024 07:36:14 GMT  
		Size: 21.8 MB (21767161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9625bef464ab08848044651374e04f75d37ada02fe71387c3f9f83d0c9376c59`  
		Last Modified: Tue, 03 Dec 2024 17:15:53 GMT  
		Size: 59.6 MB (59641126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d83c079d9e82f91aeec2e9d84797bc47fa7f3b69f4094b837cbb4a9c25c5613`  
		Last Modified: Tue, 03 Dec 2024 20:03:34 GMT  
		Size: 175.2 MB (175241789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c37a07b310ce0346c0b105b93643ae7804934f50b5803137d2397fda42284ad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15311262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212be7441ad84dc59844b2e1479e05aaff0604670d910cd493e41a9ee0f3f9a6`

```dockerfile
```

-	Layers:
	-	`sha256:d6a56c836aa67f6706e6eacb06bc1edf226a862c6df77e58f7a17171c9494731`  
		Last Modified: Tue, 03 Dec 2024 20:03:30 GMT  
		Size: 15.3 MB (15300654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20d1d9165217046eef0f65fd0f02af670a48e312e840cc150c0713c8769cc7b5`  
		Last Modified: Tue, 03 Dec 2024 20:03:29 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:39b25cdea8a4133052cf8976d884cd9f4a28c36fc7ea1d200a82c3054510ff15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.8 MB (338766544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14cf9bca2791cef90a5b1313fb25c31438e4cf72dfec291fec9d3abfcc7b8674`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac722d9cf93b238dec2480278a2df5f8ccb672c97ec39f191191fd39f6721a8`  
		Last Modified: Tue, 03 Dec 2024 05:38:46 GMT  
		Size: 23.4 MB (23405813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261351ed796deb9fdad22dc734919eaf6726dd79a8dea99327d9e1376ecdcbce`  
		Last Modified: Tue, 03 Dec 2024 11:50:22 GMT  
		Size: 64.3 MB (64347852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d319298afc8bd728b8009e80320fe04e864fe92783eb06238a3b9f67dac7c3`  
		Last Modified: Tue, 03 Dec 2024 16:19:47 GMT  
		Size: 202.7 MB (202687199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d273ba454f05ac7b5489806499d16a8fc8ebf4171d5b07f144b245ce6d48a92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15535745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a83186039bd3ea2e021d2749e90f67f3e94a9e21027127ab2af7156513301e0`

```dockerfile
```

-	Layers:
	-	`sha256:578a4e71415013356a8cd37b5030e980c95edd8780c5a2f5a02a5d3585b92925`  
		Last Modified: Tue, 03 Dec 2024 16:19:42 GMT  
		Size: 15.5 MB (15525113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c493ff614776a1782e0bbac3137f383ef0eaad4fffed2bc981261fb4770db246`  
		Last Modified: Tue, 03 Dec 2024 16:19:42 GMT  
		Size: 10.6 KB (10632 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0ab7c71d79bd872a655352313f52121a6bcff2ffbac86045c95275339c23dd99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.6 MB (350616786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3ef764469eb7f8569265b9f9540132de83292a18992941d2995b96bcb6332e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:53769c348e57d646b1ec110dabf9d81a3f570afdb3b8216d1178515e4ea4ce1f`  
		Last Modified: Tue, 03 Dec 2024 01:27:09 GMT  
		Size: 49.5 MB (49476152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b0c73f75a815ce87bbf2841b694fdc4c29bcd072480b8752e8e91f0b59097b`  
		Last Modified: Tue, 03 Dec 2024 03:23:49 GMT  
		Size: 24.7 MB (24706896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2cf0351f309a0cf554972555b46b2ed97868d801e25eeed28a9f742a5e555c`  
		Last Modified: Tue, 03 Dec 2024 04:29:18 GMT  
		Size: 66.2 MB (66211191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adec659d61840fa9345456f332914b715e5d645a246d8ebd23b1c1c4b49b4996`  
		Last Modified: Tue, 03 Dec 2024 05:13:33 GMT  
		Size: 210.2 MB (210222547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:beeefbfff2ab941591ca7b91831c773ed391314b2de8511095bed0ee45cc98dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15485661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8bad9e7072ba65013bcf0c51e6857d3cbf652a07f0e5daa83e3d046e94995f`

```dockerfile
```

-	Layers:
	-	`sha256:87a64892961d327a139e2c8827b6f3f38d3383d5f173df4dfebfbfa09ef41385`  
		Last Modified: Tue, 03 Dec 2024 05:13:28 GMT  
		Size: 15.5 MB (15475148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e958a20d62bb83ee3421e3a3e2d16608731c94121983988380170f328b7e9f2c`  
		Last Modified: Tue, 03 Dec 2024 05:13:27 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:9a4df2f86567815e32dbc326f5e5710e33ae4f7e2c64c4ce81c28b6ee888b1ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325389432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3307c2bfac9eb9bd9ffeca8fbb60c761663449db1d61e6b4628d2dc291c3d8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8f7c3140f4f3af477253c748b229283137cca4214e1c3df21109b821f9227620`  
		Last Modified: Tue, 03 Dec 2024 01:27:53 GMT  
		Size: 48.8 MB (48771844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa54d74c5fddb1e648e0a4d95fcc8338f5800ff817646baaa9e6e65596d80c5a`  
		Last Modified: Tue, 03 Dec 2024 15:45:04 GMT  
		Size: 23.5 MB (23458105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a279e7254de3fa3935af4b6008753d14fcd8db605c58b83903cf8c5f880324cd`  
		Last Modified: Tue, 03 Dec 2024 23:22:12 GMT  
		Size: 63.3 MB (63283098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dffedca1364b4f303c66eee15c30c1fe70fb1db9416edf06602e694b41c50f8`  
		Last Modified: Wed, 04 Dec 2024 04:38:35 GMT  
		Size: 189.9 MB (189876385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0b9e0ac2a57702f5a76c6ff8a70e27672e95eabbe67a9141687c6917de5e0b46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aad0047efd61ce3266f344221ab7efa1e1390e8fa64a6831adff99b0275fcfb`

```dockerfile
```

-	Layers:
	-	`sha256:10d62b0e0d641ac025f308f802b13bf87690a2a5ecfbbc2f4f58a5d28559ba58`  
		Last Modified: Wed, 04 Dec 2024 04:38:18 GMT  
		Size: 10.4 KB (10382 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4ff5e7a9649060e6cec9389c3206397b83ccf21a3ef73f6da914d6a2b64f07fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.0 MB (362005295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f8e120cfb46d308aaefc2f3eb5e8f7580c23131f19cd4b52ef9a90bfce89cb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c84d784fe3c6c2bd95dea1c0d6eeba7c981bfb75bd53f81e83bcaadd87bba6f9`  
		Last Modified: Tue, 03 Dec 2024 01:28:03 GMT  
		Size: 52.3 MB (52328222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f0cfea13db30ebc69124696ada25182d1141398cd301a47a2cbf3c10d7fa9b`  
		Last Modified: Tue, 03 Dec 2024 04:36:57 GMT  
		Size: 25.5 MB (25523892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac73bc765d61ec6125ff5203c6c3d44543e6c3030684bfed0cb8f169640ae757`  
		Last Modified: Tue, 03 Dec 2024 09:41:44 GMT  
		Size: 69.8 MB (69812337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96099d400daf72e276203923fc855b1b1e5db81df04082e3505683bb398ec9ca`  
		Last Modified: Tue, 03 Dec 2024 16:12:55 GMT  
		Size: 214.3 MB (214340844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c38259992ff8adb65a540669780917a3ab0b4eb2a7bacfc0defc08aabe1954a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15483450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f228c3be5f23d0c8799c7a0da21c5bdc94a05195f09c48ab4f5756a9444da4d3`

```dockerfile
```

-	Layers:
	-	`sha256:4440c44dd5ab1d5632e5b9c675b3baff9156597169f4d38bade9241401960420`  
		Last Modified: Tue, 03 Dec 2024 16:12:35 GMT  
		Size: 15.5 MB (15472872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0489521282efca47f374796943fd138778aa10144bb693e59944fe88b32e855c`  
		Last Modified: Tue, 03 Dec 2024 16:12:31 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cea2ed2882f4bb7184acceea3fb0d08f2c273af35929de4d26ec1770b8329e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.8 MB (317814279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df084175632dd7bf0baf95424425d7b56f2dc329be6919e564076bfc0c0b66e7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:53a5c0dbd93a4a7f540e18bbe49ba3d7fadaa390ebbce009c756e34c5b1ae048`  
		Last Modified: Tue, 03 Dec 2024 01:27:55 GMT  
		Size: 47.1 MB (47149767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ded5bb0b377b736e6c5f45164fe8916ada3485441e963fe2fc0671949650049`  
		Last Modified: Tue, 03 Dec 2024 04:07:42 GMT  
		Size: 23.9 MB (23864625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b626037a925f80e453161d124c98cc5578e9d47f3f90a050168552e9727a34e`  
		Last Modified: Tue, 03 Dec 2024 07:53:40 GMT  
		Size: 63.5 MB (63473216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877241890f0b72dfe408c616ea9dde1f1c0afbbe3e7b91d9ceab73e7963ef0eb`  
		Last Modified: Tue, 03 Dec 2024 10:39:34 GMT  
		Size: 183.3 MB (183326671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ebbeeed93d90a07f2bf61c939dc6239ec6d8f6061e3eb49598381e313d2fb582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15319550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:017d6c05bd78e755bb45830a2c4afd3694c60f8b2019aa34942d6d1c91f3951b`

```dockerfile
```

-	Layers:
	-	`sha256:a14fcfe55eaddefca48b5c90a0ebb9e879a4899937c7f283124a5b4f9155e8fe`  
		Last Modified: Tue, 03 Dec 2024 10:39:31 GMT  
		Size: 15.3 MB (15309010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81a7f4e3bcc82457c7631f0aa274731bcc28c78bab41b2d89951556c508a2a32`  
		Last Modified: Tue, 03 Dec 2024 10:39:31 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:60fa59330635bb3360b021ffa0f96b1fbd61b19cf522290bf966f3bde25a9ca1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:bookworm-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e4e69a8b7f9e04139295fb9dcdf37d823b148d1c112e36b0653d11ba96c6604e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72363086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d5ef6bc224b02787f00cbbce868ebbadc4fe38a2a978313291c878413ee721f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd71677db44bb63b94de61b6f1f95d5540b4ba2d6a8a6bc4d19f422b25e0c2b`  
		Last Modified: Tue, 03 Dec 2024 02:28:49 GMT  
		Size: 23.9 MB (23865876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7ff9434e13b1f41e3fdde66e19d17f3c35636e0cd182bf0bd4386e2af4124d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4371222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43bd9c68c9fe0a5c3db25a9086681f8f9c104c591606a18bea36b7dad3af97b7`

```dockerfile
```

-	Layers:
	-	`sha256:996b54fd1b681c68f21142e93f996d2ce61d3345a3aacb49c85c12238b4a15e3`  
		Last Modified: Tue, 03 Dec 2024 02:28:49 GMT  
		Size: 4.4 MB (4364058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aef3835c1fc0e6916ee36bb9b108d4e0947caab9bf621401475a88e457ab409d`  
		Last Modified: Tue, 03 Dec 2024 02:28:48 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9ca627c143143071812435f20a31d7ca4a98f8f69eb5772238d5ab4c289773e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68564756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d52aedd03a58bb0c09f5e307d64f49efd1f50d13619447fd27ad609070014374`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a8ab0b752e573ceb3480052f24bc5fe3f4f4665c13a338db39c1d51f749528e9`  
		Last Modified: Tue, 03 Dec 2024 01:27:04 GMT  
		Size: 46.0 MB (46024374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff6779451547ba3f0647f15a65068290fed53b6a4ac506257de98e02857bea6`  
		Last Modified: Tue, 03 Dec 2024 05:23:42 GMT  
		Size: 22.5 MB (22540382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2e2143039fd9074ac1c8fdaa9a11a3ffe40a93f547cf21b14da9b30f7dc7c54e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4374804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdf6d29be9af0b06c9bc426a0e4301f021a0d39b9c43f96faaf88c5fae8fdee9`

```dockerfile
```

-	Layers:
	-	`sha256:39e78f22f1d8edef86ca11b2156afabce6625a25d4fe1969f2b9b7fe1e12e885`  
		Last Modified: Tue, 03 Dec 2024 05:23:42 GMT  
		Size: 4.4 MB (4367573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0f81f00ceef9b327ef81f33ce0ac9ef30236b95c3793935d843dbbae8791bbf`  
		Last Modified: Tue, 03 Dec 2024 05:23:41 GMT  
		Size: 7.2 KB (7231 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3117bcbd993e3753ba7f62fed2092e261302219fc4794bd60744b540753d2b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (65967270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae811cf19b5c01de9b3482a0673dadcd8b1b0567a12e943446c319bddbadee9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4d43724a324f138c88a78ca6df0a39ab6868bf1f121eb974439c5a51284e1ac2`  
		Last Modified: Tue, 03 Dec 2024 01:27:59 GMT  
		Size: 44.2 MB (44200109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff0e53b92c3d0f5c370d71aeac1be1d23e475f1afba41d896ace0ff6eeefc90`  
		Last Modified: Tue, 03 Dec 2024 07:36:14 GMT  
		Size: 21.8 MB (21767161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8bbb04311c4caa959ede4991344d0b4395a37e8c603b0c5b9755e7d0ac6b02bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4373586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2806b2b8fd080b94514ac3e7a4280190841cecba2a389c4572f92b9ad6b4352a`

```dockerfile
```

-	Layers:
	-	`sha256:9457386cd8923d16e0e33114929e464cb25582e303b69193cdfeb4b31b7ddf7b`  
		Last Modified: Tue, 03 Dec 2024 07:36:13 GMT  
		Size: 4.4 MB (4366354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dde010eb4616c79d3ca142e42b4cc8fb81c4de83e8cde4e7c18080b5fe8d6b0`  
		Last Modified: Tue, 03 Dec 2024 07:36:13 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:757ecd28399473cce91e6be523aec8e79ca9f576cfed067466bcffa71ff9ac70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71731493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed0620fbee6bbd337320d030c3be4e71b8e2883828902bf89672a74d1a36278b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac722d9cf93b238dec2480278a2df5f8ccb672c97ec39f191191fd39f6721a8`  
		Last Modified: Tue, 03 Dec 2024 05:38:46 GMT  
		Size: 23.4 MB (23405813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:79739c087c54ec0d652199829c30eaba59e426e5edf317a72b3a318dd0cd8bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4371586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc692a177ab4525e660f0d3f47205fd6ed2ad3a54e419ff10a28b6e48bc78535`

```dockerfile
```

-	Layers:
	-	`sha256:4816aacc299c61ab88c4e10c38abd2b3d51afb73adba3b8bb1debfd6846287a1`  
		Last Modified: Tue, 03 Dec 2024 05:38:46 GMT  
		Size: 4.4 MB (4364330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:913b8b80c5fa22b390e28ca34404e62e7d38090c8e99339fc5cdde2cf477b4ed`  
		Last Modified: Tue, 03 Dec 2024 05:38:45 GMT  
		Size: 7.3 KB (7256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5ddf951a80c7dec860666e1ff917ced4535353326c546dab88edcbab700e2345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74183048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:129a653e602a0fe253a2b069b2e2ab67f1ea9115e2fd72cc3ced51c193a26a5f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:53769c348e57d646b1ec110dabf9d81a3f570afdb3b8216d1178515e4ea4ce1f`  
		Last Modified: Tue, 03 Dec 2024 01:27:09 GMT  
		Size: 49.5 MB (49476152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b0c73f75a815ce87bbf2841b694fdc4c29bcd072480b8752e8e91f0b59097b`  
		Last Modified: Tue, 03 Dec 2024 03:23:49 GMT  
		Size: 24.7 MB (24706896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:eebaeeda8054688d6fd8c142a0fc0a9ccfa4fc3ca2b3499bfe916319c4994ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4368251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8937659e583da0ff6a76c8f743b3e42f34bd06dbbe6d065e151fb9bfada42aa`

```dockerfile
```

-	Layers:
	-	`sha256:729bb902df2997852a31087017dd8b75ede98123a831591b1b48e5519566d1b0`  
		Last Modified: Tue, 03 Dec 2024 03:23:48 GMT  
		Size: 4.4 MB (4361114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:310a36eb7785ee15a990c5d5843eb5ce31f673057b5dd6940687e2392aafaffb`  
		Last Modified: Tue, 03 Dec 2024 03:23:48 GMT  
		Size: 7.1 KB (7137 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:7ae289bc030a4b5e312465d3e015385f878f438f21b1723c31ae05301d012675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72229949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f8bd8c5b5ea753d9188c3db86b7f053f010d9de2a9dd1dfceb0a49d52a4d4c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8f7c3140f4f3af477253c748b229283137cca4214e1c3df21109b821f9227620`  
		Last Modified: Tue, 03 Dec 2024 01:27:53 GMT  
		Size: 48.8 MB (48771844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa54d74c5fddb1e648e0a4d95fcc8338f5800ff817646baaa9e6e65596d80c5a`  
		Last Modified: Tue, 03 Dec 2024 15:45:04 GMT  
		Size: 23.5 MB (23458105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0f04f4b64d87c286d8281dc28e82e764fcf2429c6f431b927f4f2b1b0e2e1b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 KB (7005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df656bed5425ba40a59f661b24a9ef00be8b445ae9820ef34b56825c81995052`

```dockerfile
```

-	Layers:
	-	`sha256:9973e5e44c5c8a102b2079d03531741e8919c0d04a2f710f280f74d5169fe092`  
		Last Modified: Tue, 03 Dec 2024 15:45:01 GMT  
		Size: 7.0 KB (7005 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:989e244c7923bf0590fb8ddd1cfda40228425477aed2564c4f1d68d5bf4c1211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77852114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9269507941157f6d8c2a6aaf7d982955bbd6ad996a59aa0c335382fa56fedbf3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c84d784fe3c6c2bd95dea1c0d6eeba7c981bfb75bd53f81e83bcaadd87bba6f9`  
		Last Modified: Tue, 03 Dec 2024 01:28:03 GMT  
		Size: 52.3 MB (52328222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f0cfea13db30ebc69124696ada25182d1141398cd301a47a2cbf3c10d7fa9b`  
		Last Modified: Tue, 03 Dec 2024 04:36:57 GMT  
		Size: 25.5 MB (25523892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a45e69e0d085a116675b75a7b725f816d6446a3fb4ca0543c48e95c3f3fd3978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4375753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e3cdc76dad87b7234f6f31c723d08c241a2a7efa8c9039144506f957faabb9`

```dockerfile
```

-	Layers:
	-	`sha256:238d77a8b35e0e5b35ee3bdf19e0102de9c1fb1aa37b9dbc272bed8d60d9852c`  
		Last Modified: Tue, 03 Dec 2024 04:36:57 GMT  
		Size: 4.4 MB (4368551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec9892333b13de0bc61e2cdc3ecce83c24ed20bb5579e82cfaa2d4bbcfb85f33`  
		Last Modified: Tue, 03 Dec 2024 04:36:56 GMT  
		Size: 7.2 KB (7202 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a0a6eb40a58c78dab49f2a7fbb55665c1a2af22ac7a1ac77580e07074365ec0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71014392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68d8461201f6697d48a6322c9ab07b91a4490ee92e53b559914223bb89b0a6c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:53a5c0dbd93a4a7f540e18bbe49ba3d7fadaa390ebbce009c756e34c5b1ae048`  
		Last Modified: Tue, 03 Dec 2024 01:27:55 GMT  
		Size: 47.1 MB (47149767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ded5bb0b377b736e6c5f45164fe8916ada3485441e963fe2fc0671949650049`  
		Last Modified: Tue, 03 Dec 2024 04:07:42 GMT  
		Size: 23.9 MB (23864625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bae73931459a569e6aa2c77e5721402acdd0fa87c8499ac00c378f09da2b74e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4370919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb35bd02c831221f27c85d64464a87ff1e458b43c43e1a167b9614f44689a992`

```dockerfile
```

-	Layers:
	-	`sha256:9c310eee549867fde8b1fd56ec371ef6cbb8f19c03df6ec7b8c6a49b4dcd0703`  
		Last Modified: Tue, 03 Dec 2024 04:07:42 GMT  
		Size: 4.4 MB (4363755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e932d932ad0e9d02444cefa5146dd7acdbe99b89f0389f686355c2b3271a1eea`  
		Last Modified: Tue, 03 Dec 2024 04:07:41 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:9cb2ad7d26df8c138d5932843e460988b87f61ac5346721a3d1ad60c6d8a41d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:bookworm-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:081b378225dd3efe7d85a0720370cbfd29b95001f7a0fb7073af54694ac974b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.8 MB (136754594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf470aba1a92d0771a65417e8a1beca6b311c9d18bcc12eb965032af2ee32b8a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd71677db44bb63b94de61b6f1f95d5540b4ba2d6a8a6bc4d19f422b25e0c2b`  
		Last Modified: Tue, 03 Dec 2024 02:28:49 GMT  
		Size: 23.9 MB (23865876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551df7f94f9c131f2fec0e8063142411365f0a1c88b935b9fac22be91af227e0`  
		Last Modified: Tue, 03 Dec 2024 03:17:14 GMT  
		Size: 64.4 MB (64391508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:20e125aea8586458a38f6d6b5fc4e799b157c40f6827bcdeede53d9deae5face
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7770849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed90e1697fb72676df77dcda5236274c90f61c17282ceccfc72e15b82f41da6`

```dockerfile
```

-	Layers:
	-	`sha256:012f88be9d04d99db39c2e75975d319894fe143e2f1d2c6b22032f733dc8c9a2`  
		Last Modified: Tue, 03 Dec 2024 03:17:12 GMT  
		Size: 7.8 MB (7763194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffa6b104b3f4a17660de0197b48ec8fbd2132b50b103011b72bafd123a894939`  
		Last Modified: Tue, 03 Dec 2024 03:17:12 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9b05d826a9aea2d34ea09a27fa55a3c9149103ac03323af230c8d2fcbcc8c5b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130561570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220e7a63ad00370b6e1c4651783b941fd094c6d2f66623cc356f07353ced08c9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a8ab0b752e573ceb3480052f24bc5fe3f4f4665c13a338db39c1d51f749528e9`  
		Last Modified: Tue, 03 Dec 2024 01:27:04 GMT  
		Size: 46.0 MB (46024374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff6779451547ba3f0647f15a65068290fed53b6a4ac506257de98e02857bea6`  
		Last Modified: Tue, 03 Dec 2024 05:23:42 GMT  
		Size: 22.5 MB (22540382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536c3cdef529f6d2993cf137c109a079266cd3effbffc602a136a2a60ee743a0`  
		Last Modified: Tue, 03 Dec 2024 08:40:08 GMT  
		Size: 62.0 MB (61996814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ba33181894b95455834717fb83a3cab2650b256f61a539f7419fc4f2e9c101c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7772471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49b76ea2636dae7de0703b48ca2f666e83f0a87977aff0a7884206898bf9654`

```dockerfile
```

-	Layers:
	-	`sha256:7b65f3800eb2add9f15ccf14f61be70696d82161b63f30b569972b0c8bd6a72e`  
		Last Modified: Tue, 03 Dec 2024 08:40:07 GMT  
		Size: 7.8 MB (7764748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4172764014ee95b8731a943cfba1e0f4e0e07007f8a4395720c1e0f1339fcccc`  
		Last Modified: Tue, 03 Dec 2024 08:40:06 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:390b0a015b9c6bd4a91717ab50b2da649b0e953291c1f6f179ac799ef34e25dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125608396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e6c420c1f7fb64fa485887316c939461f82ec6dbdf0ccd26e9a5970807dbee`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4d43724a324f138c88a78ca6df0a39ab6868bf1f121eb974439c5a51284e1ac2`  
		Last Modified: Tue, 03 Dec 2024 01:27:59 GMT  
		Size: 44.2 MB (44200109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff0e53b92c3d0f5c370d71aeac1be1d23e475f1afba41d896ace0ff6eeefc90`  
		Last Modified: Tue, 03 Dec 2024 07:36:14 GMT  
		Size: 21.8 MB (21767161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9625bef464ab08848044651374e04f75d37ada02fe71387c3f9f83d0c9376c59`  
		Last Modified: Tue, 03 Dec 2024 17:15:53 GMT  
		Size: 59.6 MB (59641126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:97cad46bffd054d5464b24f3898b89857a83b9327bd544db3f756fe68e8e5eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7772198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a53c50a14cb4d17416ad8c2b9f6ae29f07e4a2b9360068459000d153cbfa28`

```dockerfile
```

-	Layers:
	-	`sha256:98bbc215633288506c1cd937a4043acf7e3f2d79ced4e6d1b78fb36f63f12c90`  
		Last Modified: Tue, 03 Dec 2024 17:15:52 GMT  
		Size: 7.8 MB (7764475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4b268dda7212f4c955489072ec118680aa47218128cabc0b36f57ab7211081a`  
		Last Modified: Tue, 03 Dec 2024 17:15:51 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4b4fd9f631b9294a9c2600d58e03ea6aabe8064c9023517e3c004147a248c706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136079345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:294a87bc6560e0bb4acbf480b18930ca99a2863c50d4817579003ad59c8dcf5b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac722d9cf93b238dec2480278a2df5f8ccb672c97ec39f191191fd39f6721a8`  
		Last Modified: Tue, 03 Dec 2024 05:38:46 GMT  
		Size: 23.4 MB (23405813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261351ed796deb9fdad22dc734919eaf6726dd79a8dea99327d9e1376ecdcbce`  
		Last Modified: Tue, 03 Dec 2024 11:50:22 GMT  
		Size: 64.3 MB (64347852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:296b38d3b5682f620d8d350576747bedddd836671036ca931158e5fcc0abeba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7777352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6feeb02a68d010871c1233be105b538ae59e9b1d4fc972aaf364445fbcb678bd`

```dockerfile
```

-	Layers:
	-	`sha256:52070a7e355cffc4a9d0da8f0dc19e32ab40a808d402a964b8802456ba6e889f`  
		Last Modified: Tue, 03 Dec 2024 11:50:20 GMT  
		Size: 7.8 MB (7769605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:559dec8b2f1952ab63dd3ad11af3f0cab12b2904ee9ac16805ff6743224ac486`  
		Last Modified: Tue, 03 Dec 2024 11:50:19 GMT  
		Size: 7.7 KB (7747 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:efadcac373fc964d9e687e3c3acd546ed1243f3de78c4dfaa3cab0c1c44164bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140394239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c6c2127f1e3c3cff2f2545cac8268fc28d1eca7e5f18ebd9811301efedbc12`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:53769c348e57d646b1ec110dabf9d81a3f570afdb3b8216d1178515e4ea4ce1f`  
		Last Modified: Tue, 03 Dec 2024 01:27:09 GMT  
		Size: 49.5 MB (49476152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b0c73f75a815ce87bbf2841b694fdc4c29bcd072480b8752e8e91f0b59097b`  
		Last Modified: Tue, 03 Dec 2024 03:23:49 GMT  
		Size: 24.7 MB (24706896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2cf0351f309a0cf554972555b46b2ed97868d801e25eeed28a9f742a5e555c`  
		Last Modified: Tue, 03 Dec 2024 04:29:18 GMT  
		Size: 66.2 MB (66211191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:90045c81ec640293d6faa0394f96a1a985df7ff3d81fada2cfde8db780172edb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7766897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e344e02c870074180a5c7834575f4d8030d1e8969592d6bfa37194677c4d8bf3`

```dockerfile
```

-	Layers:
	-	`sha256:9855bce4e2e113f8c216ac6ecdad8a6af90932e14bc9bf28815c4fa67b760275`  
		Last Modified: Tue, 03 Dec 2024 04:29:16 GMT  
		Size: 7.8 MB (7759270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:487dfc9a24b2a2d5a2e18670b6601e6e1927433744a4d83a1dd8813646329b52`  
		Last Modified: Tue, 03 Dec 2024 04:29:16 GMT  
		Size: 7.6 KB (7627 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8915c51839fedacb07adb7002f8c190c948a12fcb503b7696ffc03b6a1b61ce2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135513047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbc8ce69146cef10089880f0995e0f8904567b5f315696d227d654aea381c65`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8f7c3140f4f3af477253c748b229283137cca4214e1c3df21109b821f9227620`  
		Last Modified: Tue, 03 Dec 2024 01:27:53 GMT  
		Size: 48.8 MB (48771844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa54d74c5fddb1e648e0a4d95fcc8338f5800ff817646baaa9e6e65596d80c5a`  
		Last Modified: Tue, 03 Dec 2024 15:45:04 GMT  
		Size: 23.5 MB (23458105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a279e7254de3fa3935af4b6008753d14fcd8db605c58b83903cf8c5f880324cd`  
		Last Modified: Tue, 03 Dec 2024 23:22:12 GMT  
		Size: 63.3 MB (63283098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1c84b11a183c60766b72298df7807d4c7092c9c2f73f1d21017e277fc9ab23ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a1f59aac2c22a1238dc51a66bd9dce102857527b4849511e58dc50dac965a0`

```dockerfile
```

-	Layers:
	-	`sha256:20ab0e5caa843ee96726eb9c38d13c80976c82e15ba6ba6202d3e1ba959cd413`  
		Last Modified: Tue, 03 Dec 2024 23:22:05 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f41ac76702c18986d7791e88468e69b4dc78c623d28e1a490e6c0cbbfc6b1082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147664451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514cb07cf8569c7b8531ad437622c499eedef341c3f377fe235d298f7e8ac991`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c84d784fe3c6c2bd95dea1c0d6eeba7c981bfb75bd53f81e83bcaadd87bba6f9`  
		Last Modified: Tue, 03 Dec 2024 01:28:03 GMT  
		Size: 52.3 MB (52328222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f0cfea13db30ebc69124696ada25182d1141398cd301a47a2cbf3c10d7fa9b`  
		Last Modified: Tue, 03 Dec 2024 04:36:57 GMT  
		Size: 25.5 MB (25523892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac73bc765d61ec6125ff5203c6c3d44543e6c3030684bfed0cb8f169640ae757`  
		Last Modified: Tue, 03 Dec 2024 09:41:44 GMT  
		Size: 69.8 MB (69812337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2a89a02d7b0a3fc01937338322a3adbfec4f8acf6ca3ccbf611a6bfea596fec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7778593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296a47c62b0745a03c2b02e5a3f2df0ebe6f985dc10f4132e1e9b9ea44ffc350`

```dockerfile
```

-	Layers:
	-	`sha256:4b033dd73e35183deec51e3e2b0975d4838f1627c9589d8d0a263fdb61430e94`  
		Last Modified: Tue, 03 Dec 2024 09:41:42 GMT  
		Size: 7.8 MB (7770901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1815558343ccce9363e7d65977e06bb87d6b20878e7dfbcffc07133ed7dee487`  
		Last Modified: Tue, 03 Dec 2024 09:41:41 GMT  
		Size: 7.7 KB (7692 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3b238b3a7258d279b52146096b4beb7f45782123399ba1107028fffcda72845a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134487608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55812b2c5a9e20ae6c6e47ae8abb5ecd135751de9755ada12406aef2a0ded189`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:53a5c0dbd93a4a7f540e18bbe49ba3d7fadaa390ebbce009c756e34c5b1ae048`  
		Last Modified: Tue, 03 Dec 2024 01:27:55 GMT  
		Size: 47.1 MB (47149767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ded5bb0b377b736e6c5f45164fe8916ada3485441e963fe2fc0671949650049`  
		Last Modified: Tue, 03 Dec 2024 04:07:42 GMT  
		Size: 23.9 MB (23864625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b626037a925f80e453161d124c98cc5578e9d47f3f90a050168552e9727a34e`  
		Last Modified: Tue, 03 Dec 2024 07:53:40 GMT  
		Size: 63.5 MB (63473216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2006631c59dc1f6d83026dc68c6f3367d6c4a1954eaaa7c817120bfb69572ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7770055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9c6b8467b7d857fa1c079d9b3e0091c74f5fa80c8cc76afe7c7a05ea96e216`

```dockerfile
```

-	Layers:
	-	`sha256:fcf08fd6e06e7a3eb093b7470b9f4abc277ecb5601672f6d97c6e6712c678832`  
		Last Modified: Tue, 03 Dec 2024 07:53:39 GMT  
		Size: 7.8 MB (7762400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f3eab35b34c262dbc9b817602d68d99ea2c9634756836744ea2d6a546474acd`  
		Last Modified: Tue, 03 Dec 2024 07:53:39 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:bullseye`

```console
$ docker pull buildpack-deps@sha256:6617cc54bbc414524636f43515d5758f5604cc7593f4f5bfa4fde63979c9f5e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:bullseye` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e0d6c0821a6dde10bbbdece51ac39dda933b43eecff08f7e63ac59d3bcd4a430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.1 MB (321124868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b2a985a94697b011595fb26ac7b67b6ce31cdf7865b728074d3e9bfa281a23`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cd606f6f489eb66f1307280aec321b3af3aa998dca447ae1cc91c6b884240064`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 53.7 MB (53739147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925257a7168ed219a5d7c2a69af3245ca4cd9e376424f7f006535d9714437bd4`  
		Last Modified: Tue, 03 Dec 2024 02:15:41 GMT  
		Size: 15.6 MB (15558387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb34ce34679cf6bc8738a0166300fb0af605abff20bb9c1c8008dbc48722061`  
		Last Modified: Tue, 03 Dec 2024 03:17:12 GMT  
		Size: 54.8 MB (54753972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3364194d1839c998f7fa1f479212c49598df894b8a851ba42e54ebf7f4344a6`  
		Last Modified: Tue, 03 Dec 2024 04:31:23 GMT  
		Size: 197.1 MB (197073362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8f9bc52a4b9058ebee98d176fc69cd8bf21a27c6245f17b4d3087013525758e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15106111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21575104da17a45216c5ce6c3a73dc26a8ada6165dde7fd794ac310447e20dc`

```dockerfile
```

-	Layers:
	-	`sha256:b31d3b1cf134daaea9fb2cfda7f939fa9f5839cb80ce98eebefc56b34fc3ee03`  
		Last Modified: Tue, 03 Dec 2024 04:31:20 GMT  
		Size: 15.1 MB (15095881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df9e1efc148b23800b4ba72ccc8257c464c12b25ce6a320c4e0da8fc364e373b`  
		Last Modified: Tue, 03 Dec 2024 04:31:19 GMT  
		Size: 10.2 KB (10230 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:101d2910fe70365e13b014a949b79cb186ef725f82a81d6b7a958b204115d057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.9 MB (281864569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128f14c6ce29f3fef0ff687097e850601ab4f4083445e1bc6c3b96e3cdd70b69`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:69dbedc8019388fd330866fcfa04c35d28f86d1ef986691ee290054433639992`  
		Last Modified: Tue, 03 Dec 2024 01:28:37 GMT  
		Size: 49.0 MB (49025021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370e6aa30e16daf07d99e3fb5cd8610cda77f49507a7b2ba76a646359cf7db6b`  
		Last Modified: Tue, 03 Dec 2024 07:36:42 GMT  
		Size: 14.7 MB (14673759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54bf5af43178bf200a2aed84d9a42570d6bde94092c2ac746652561137c9a86`  
		Last Modified: Tue, 03 Dec 2024 17:16:41 GMT  
		Size: 50.6 MB (50640414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc87552ca09a0a5990453aa951869124cba4735d7a52f3622106c01546e373a`  
		Last Modified: Tue, 03 Dec 2024 20:05:40 GMT  
		Size: 167.5 MB (167525375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:035b3b07213c9cd6b7466b4c027ada5be1692df26badec6b966d6f692fd19426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14906654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb5361840c7746526ead3ae89167d36ad1143c1b7df099c2fbfcd912dd7113e`

```dockerfile
```

-	Layers:
	-	`sha256:ded25ba07dc8d62e794782cee821ef5d52408076e35018add12f5be63c561c90`  
		Last Modified: Tue, 03 Dec 2024 20:05:37 GMT  
		Size: 14.9 MB (14896362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f743bc17c8386d4b723625d2399313181fdc49772f10c5eb6ec78655b2417a4a`  
		Last Modified: Tue, 03 Dec 2024 20:05:36 GMT  
		Size: 10.3 KB (10292 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:780d0f15e7619876d37b53039e6f51b58e8d0d265fba615224516eb583144186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.6 MB (312622132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1743f570b8f94d50fa3e1a84df0091ce88b6984faf43f5b44acf5282c4fdeac1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e357e1f94476a03fde298261e8c007d487d3cfade45a9eef064eba724a5c5e2e`  
		Last Modified: Tue, 03 Dec 2024 01:30:26 GMT  
		Size: 52.2 MB (52245994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b2279cee7374c65ae079e8ccdceeeb8b20c07ffc727e5b7cd595285b44a3a0`  
		Last Modified: Tue, 03 Dec 2024 05:39:10 GMT  
		Size: 15.5 MB (15544048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2749caeb5baae1b5e6316a6f02e57835aa548497fba6792be844c743a57c72a2`  
		Last Modified: Tue, 03 Dec 2024 11:51:00 GMT  
		Size: 54.9 MB (54852316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e711ab753fd7e271d97eb54f50e7e1a99221d70c2b97b5351966959fcf945e2`  
		Last Modified: Tue, 03 Dec 2024 16:21:21 GMT  
		Size: 190.0 MB (189979774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6df896ad394cb1b54cc7a2c567bdf97061976656abda845a14c944d59fe8c3c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15108429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c57d40db60495718c6e83fc7933db3de6a1be5fd584376fe24955a31f773f6`

```dockerfile
```

-	Layers:
	-	`sha256:843ccf6a63c7a10aa55c6b9f6e228e5306cf5645e4d74300fc291eb62ce500ab`  
		Last Modified: Tue, 03 Dec 2024 16:21:17 GMT  
		Size: 15.1 MB (15098117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16da700212edda2cb9fe9d637750a50e7fd4839d9ca011891f1319a1d1e2b61e`  
		Last Modified: Tue, 03 Dec 2024 16:21:17 GMT  
		Size: 10.3 KB (10312 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; 386

```console
$ docker pull buildpack-deps@sha256:33b3ef54a930506240ef7bf977b1df29288dc03a3f976af6ce263711adbf3e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.7 MB (326745403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e00120fb81bef803d7b8e0f1bb7fad0c3609b8e87e321c3b3a5e13feef1f0b3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:862f429b4105c1e5714d48631896837c3ca6f797479296293b7c33c6699eae95`  
		Last Modified: Tue, 03 Dec 2024 01:27:25 GMT  
		Size: 54.7 MB (54676275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ac5b88f14d979c6f071eb85aa8a772f827338af23171657add5b5e4fc91e2e`  
		Last Modified: Tue, 03 Dec 2024 02:14:36 GMT  
		Size: 16.1 MB (16062064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc99b34aeb38c1b23bfa1cbb2b4b9d6e5a643b78e7b238368942282890609c8`  
		Last Modified: Tue, 03 Dec 2024 03:17:12 GMT  
		Size: 56.0 MB (56027112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be1f6c2fc5941e6a645f4c32428da25f169e1c1d2334e0ecff55e66ef42af0f`  
		Last Modified: Tue, 03 Dec 2024 04:31:23 GMT  
		Size: 200.0 MB (199979952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0ee5f3c14c8de3a45dc235d315dda69908563e08874df4c64ccc6be4b514835f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15094432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e896e7fc71dbe5419b6bb986ba800d3cf89ae25defdbe13f79dbef31d3b4b721`

```dockerfile
```

-	Layers:
	-	`sha256:19229e7774fcedc6f939363a74467c99e4b95654811270bd461373df7d969c7d`  
		Last Modified: Tue, 03 Dec 2024 04:31:19 GMT  
		Size: 15.1 MB (15084222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6f72559a0a226f99fa93e36c5b7d8c59dac91fb8311c939981e5bb56b593ff5`  
		Last Modified: Tue, 03 Dec 2024 04:31:19 GMT  
		Size: 10.2 KB (10210 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:5e60bf8ec14591bd01ed6138482cac4011620d5c34ad8ae6165acf0d8e2f9e91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:bullseye-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b960e9a35b94d98f8e28b9e7c6902cb6c0b00730da4c43b30bad6b65e1197205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69297534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8497e82cb3900277c279f7b4301f59ecc6cefa8ddfd2ee6cceece3a5d69cb179`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cd606f6f489eb66f1307280aec321b3af3aa998dca447ae1cc91c6b884240064`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 53.7 MB (53739147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925257a7168ed219a5d7c2a69af3245ca4cd9e376424f7f006535d9714437bd4`  
		Last Modified: Tue, 03 Dec 2024 02:15:41 GMT  
		Size: 15.6 MB (15558387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:17c6283204c87400f89a5054443c5bd83c77d1717114cdadc95a10f8743d9c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4497104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b5e44850ee339d6ee93ec71f2fdcf0bf2391e31821461866209ad64c7411c82`

```dockerfile
```

-	Layers:
	-	`sha256:0d955dfaeae326d60e2abe1818cb737d6839251fcf25ad39f452038fba101b22`  
		Last Modified: Tue, 03 Dec 2024 02:15:41 GMT  
		Size: 4.5 MB (4490305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aec84ba0adf96199bf08ed6c2d5fdf57c284d93fe90956bc7b22619c8b75f645`  
		Last Modified: Tue, 03 Dec 2024 02:15:41 GMT  
		Size: 6.8 KB (6799 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4112b0ea48c39076359cd3eba06afcb4a74fa3d7cc57a55d879a9aa5b8249ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63698780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f10e9c5003d1d069fa395b9c8bb04b9cf61629c642c305ef4eb6cc40ba150d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:69dbedc8019388fd330866fcfa04c35d28f86d1ef986691ee290054433639992`  
		Last Modified: Tue, 03 Dec 2024 01:28:37 GMT  
		Size: 49.0 MB (49025021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370e6aa30e16daf07d99e3fb5cd8610cda77f49507a7b2ba76a646359cf7db6b`  
		Last Modified: Tue, 03 Dec 2024 07:36:42 GMT  
		Size: 14.7 MB (14673759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fa0394388fbb2a06608ef60f548e97fb3dd04c124707abb27578eb19d4e6f14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4498800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979dce311168a7be5bf4db153de64d7238907994412a09c48bb1b9e90237c04a`

```dockerfile
```

-	Layers:
	-	`sha256:06d605c34375c728220a4ced5a6ef0b6de1d2c8d13c3694bd27ff80985cfc089`  
		Last Modified: Tue, 03 Dec 2024 07:36:42 GMT  
		Size: 4.5 MB (4491939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bd2b302e4bff90978f3a1a096b66e375120e062ebbfa0bdfbba17516df34eb4`  
		Last Modified: Tue, 03 Dec 2024 07:36:42 GMT  
		Size: 6.9 KB (6861 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:23d2e1f65f73a35eb78b1b28fd68d7c1afb54f666591c04bcd3c16d30c96bc32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67790042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b248a8c7acfb43452ba7e26d3295d2ccc04591a6e674dd2d21bdc45de3f447d7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e357e1f94476a03fde298261e8c007d487d3cfade45a9eef064eba724a5c5e2e`  
		Last Modified: Tue, 03 Dec 2024 01:30:26 GMT  
		Size: 52.2 MB (52245994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b2279cee7374c65ae079e8ccdceeeb8b20c07ffc727e5b7cd595285b44a3a0`  
		Last Modified: Tue, 03 Dec 2024 05:39:10 GMT  
		Size: 15.5 MB (15544048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:81ac6e124e736bf967e063a3be5ee9b9bc7a1db57f6f079af2e4f756295f352c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4496798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c81d5ecfe36c80b4b6452433e578e91ccf9f1f0fb214f9ce715756e93f6588b0`

```dockerfile
```

-	Layers:
	-	`sha256:95096dac33f7eff76e3eba5f7831fc981095785df44edb3b25fe21023899b42a`  
		Last Modified: Tue, 03 Dec 2024 05:39:10 GMT  
		Size: 4.5 MB (4489917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:831bc2da230f1470d9903f490c7d5b04257b7e79ab6f7c41792d2f326379e813`  
		Last Modified: Tue, 03 Dec 2024 05:39:09 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:79f35d801d1e471f31b46e8499d002d0bb08ba26829b87a89b481e981b8a1a4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70738339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081736c16bfcf7e7b6410b208723d39963512d09f222f018031e6b377fdc34fc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:862f429b4105c1e5714d48631896837c3ca6f797479296293b7c33c6699eae95`  
		Last Modified: Tue, 03 Dec 2024 01:27:25 GMT  
		Size: 54.7 MB (54676275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ac5b88f14d979c6f071eb85aa8a772f827338af23171657add5b5e4fc91e2e`  
		Last Modified: Tue, 03 Dec 2024 02:14:36 GMT  
		Size: 16.1 MB (16062064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9b682a0742c1a6381c26d03803ccca7a0f2619d756c223d42fad73eaf58f7533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4493522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844f4f11fe8d04e3b69e4f23063bf7551dcd49afa2df8b22ff09ab932d85f1a8`

```dockerfile
```

-	Layers:
	-	`sha256:2708918bcd4c0cd8a9295c30d52757ec544382da6221ae3e99b0c308054e3e91`  
		Last Modified: Tue, 03 Dec 2024 02:14:35 GMT  
		Size: 4.5 MB (4486744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d34f64a1c514c02f7b13010a041e7b1c35aa623aff72b601bb643cd6ba4519f5`  
		Last Modified: Tue, 03 Dec 2024 02:14:36 GMT  
		Size: 6.8 KB (6778 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:2c45feec361abb226bbf435f864494690255c4299754d9acd1f737535a7abe5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:bullseye-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0f366899853a39f6d5bfefd3a1d87b9a6e77b0d1693f159852589bab14fa56de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 MB (124051506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e03eddae311a28e3cdc3b1e06a73fec0df44fe8ffe18ec3cd0a6beaa3679a61`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cd606f6f489eb66f1307280aec321b3af3aa998dca447ae1cc91c6b884240064`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 53.7 MB (53739147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925257a7168ed219a5d7c2a69af3245ca4cd9e376424f7f006535d9714437bd4`  
		Last Modified: Tue, 03 Dec 2024 02:15:41 GMT  
		Size: 15.6 MB (15558387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb34ce34679cf6bc8738a0166300fb0af605abff20bb9c1c8008dbc48722061`  
		Last Modified: Tue, 03 Dec 2024 03:17:12 GMT  
		Size: 54.8 MB (54753972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e95a5f98efdd6e08a12735a0fd6c4c5a3051965595a72f2c708ea4166ad4fd68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7725686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d18063dd303c3df8c4bc0ba7ee19280ba8273ba222cdf8806418d7ae0614de0`

```dockerfile
```

-	Layers:
	-	`sha256:8f8714a5245415496d1184c9bf67324931b783e6e2576f6937a4fee947db486f`  
		Last Modified: Tue, 03 Dec 2024 03:17:10 GMT  
		Size: 7.7 MB (7718333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea2d08ec39059b267a5fa537e634436554e564153de6341031fd87f0045d90b6`  
		Last Modified: Tue, 03 Dec 2024 03:17:10 GMT  
		Size: 7.4 KB (7353 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:be78aa16820580cada63d809a8bfb504aa1276f7dd084f6c2f84e0bb02c007ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114339194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a03adb57e3f60161d493f8c8f2d91f2d2c5df173bd292bc160c9c579cceef9f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:69dbedc8019388fd330866fcfa04c35d28f86d1ef986691ee290054433639992`  
		Last Modified: Tue, 03 Dec 2024 01:28:37 GMT  
		Size: 49.0 MB (49025021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370e6aa30e16daf07d99e3fb5cd8610cda77f49507a7b2ba76a646359cf7db6b`  
		Last Modified: Tue, 03 Dec 2024 07:36:42 GMT  
		Size: 14.7 MB (14673759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54bf5af43178bf200a2aed84d9a42570d6bde94092c2ac746652561137c9a86`  
		Last Modified: Tue, 03 Dec 2024 17:16:41 GMT  
		Size: 50.6 MB (50640414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e492de4a1bcc068b39955b80d874bf462808c59bf0ec31bb6bd280d936713d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7727144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd315f13cbfceff99c6d58272b95dd096b9512de6dd7537f6d6afe2fd3e64d2d`

```dockerfile
```

-	Layers:
	-	`sha256:21a97e5fb320768479f40b78f22eaeeef9eb396a0aed03b8d41ca681056c0752`  
		Last Modified: Tue, 03 Dec 2024 17:16:40 GMT  
		Size: 7.7 MB (7719731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51c5b9e593196a516856494c0dbea31bc158ff6fcc6058ea5e8c3d1a983de169`  
		Last Modified: Tue, 03 Dec 2024 17:16:40 GMT  
		Size: 7.4 KB (7413 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:96fa200ba907ff5f10dcad7d3e89a5fd73d7a5d5e9659f3ea75a0d9e5e39cb23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122642358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc6c1ae1ad1d343f3ddbe86366b8189c8c804cebc4df7e87157d0ffa17f9d336`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e357e1f94476a03fde298261e8c007d487d3cfade45a9eef064eba724a5c5e2e`  
		Last Modified: Tue, 03 Dec 2024 01:30:26 GMT  
		Size: 52.2 MB (52245994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b2279cee7374c65ae079e8ccdceeeb8b20c07ffc727e5b7cd595285b44a3a0`  
		Last Modified: Tue, 03 Dec 2024 05:39:10 GMT  
		Size: 15.5 MB (15544048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2749caeb5baae1b5e6316a6f02e57835aa548497fba6792be844c743a57c72a2`  
		Last Modified: Tue, 03 Dec 2024 11:51:00 GMT  
		Size: 54.9 MB (54852316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6f1b608089d0dcbf42f5fc54da8bb34eaf30baac382624cfcc5f1a0989e401a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7731504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1dc80dda6eb42786edf9a0b24dc97cc6190d25aee82b1fd1276db616e8ccbc3`

```dockerfile
```

-	Layers:
	-	`sha256:30fed3f253d5a80620794c68dafe113a0924ca7001e8da4f4d974c019fa6166f`  
		Last Modified: Tue, 03 Dec 2024 11:50:58 GMT  
		Size: 7.7 MB (7724072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a78a3d3e15864eb8fa9847638a76c54bab0eec07868a25d3aa7add0d432da7e`  
		Last Modified: Tue, 03 Dec 2024 11:50:57 GMT  
		Size: 7.4 KB (7432 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:eba00443a4dc065f45bcbede0181fa8dc5c28cbe1f55a18a9251feec5922c7ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126765451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ac82b6418e195c7b206d1965a4d4632534d11a24c0e88216d341de0b6ae49a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:862f429b4105c1e5714d48631896837c3ca6f797479296293b7c33c6699eae95`  
		Last Modified: Tue, 03 Dec 2024 01:27:25 GMT  
		Size: 54.7 MB (54676275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ac5b88f14d979c6f071eb85aa8a772f827338af23171657add5b5e4fc91e2e`  
		Last Modified: Tue, 03 Dec 2024 02:14:36 GMT  
		Size: 16.1 MB (16062064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc99b34aeb38c1b23bfa1cbb2b4b9d6e5a643b78e7b238368942282890609c8`  
		Last Modified: Tue, 03 Dec 2024 03:17:12 GMT  
		Size: 56.0 MB (56027112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2720d09566864abb3abb4f25253ebe3a61d88eb16747e675596008f1490ad5cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7721152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58543cbb4d408bacf014776698e3640af6c46424a52d359af87b4aec6dc23232`

```dockerfile
```

-	Layers:
	-	`sha256:652571b4e42beeac87dbcf820f654e65b967d8c560bdc560c5df4ce567fbfef1`  
		Last Modified: Tue, 03 Dec 2024 03:17:11 GMT  
		Size: 7.7 MB (7713821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5d6dbfe0b90b6c9489145208f3876d82d9a5511a023b5420de9795b688a43e9`  
		Last Modified: Tue, 03 Dec 2024 03:17:10 GMT  
		Size: 7.3 KB (7331 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:curl`

```console
$ docker pull buildpack-deps@sha256:60fa59330635bb3360b021ffa0f96b1fbd61b19cf522290bf966f3bde25a9ca1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e4e69a8b7f9e04139295fb9dcdf37d823b148d1c112e36b0653d11ba96c6604e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72363086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d5ef6bc224b02787f00cbbce868ebbadc4fe38a2a978313291c878413ee721f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd71677db44bb63b94de61b6f1f95d5540b4ba2d6a8a6bc4d19f422b25e0c2b`  
		Last Modified: Tue, 03 Dec 2024 02:28:49 GMT  
		Size: 23.9 MB (23865876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7ff9434e13b1f41e3fdde66e19d17f3c35636e0cd182bf0bd4386e2af4124d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4371222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43bd9c68c9fe0a5c3db25a9086681f8f9c104c591606a18bea36b7dad3af97b7`

```dockerfile
```

-	Layers:
	-	`sha256:996b54fd1b681c68f21142e93f996d2ce61d3345a3aacb49c85c12238b4a15e3`  
		Last Modified: Tue, 03 Dec 2024 02:28:49 GMT  
		Size: 4.4 MB (4364058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aef3835c1fc0e6916ee36bb9b108d4e0947caab9bf621401475a88e457ab409d`  
		Last Modified: Tue, 03 Dec 2024 02:28:48 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9ca627c143143071812435f20a31d7ca4a98f8f69eb5772238d5ab4c289773e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68564756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d52aedd03a58bb0c09f5e307d64f49efd1f50d13619447fd27ad609070014374`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a8ab0b752e573ceb3480052f24bc5fe3f4f4665c13a338db39c1d51f749528e9`  
		Last Modified: Tue, 03 Dec 2024 01:27:04 GMT  
		Size: 46.0 MB (46024374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff6779451547ba3f0647f15a65068290fed53b6a4ac506257de98e02857bea6`  
		Last Modified: Tue, 03 Dec 2024 05:23:42 GMT  
		Size: 22.5 MB (22540382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2e2143039fd9074ac1c8fdaa9a11a3ffe40a93f547cf21b14da9b30f7dc7c54e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4374804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdf6d29be9af0b06c9bc426a0e4301f021a0d39b9c43f96faaf88c5fae8fdee9`

```dockerfile
```

-	Layers:
	-	`sha256:39e78f22f1d8edef86ca11b2156afabce6625a25d4fe1969f2b9b7fe1e12e885`  
		Last Modified: Tue, 03 Dec 2024 05:23:42 GMT  
		Size: 4.4 MB (4367573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0f81f00ceef9b327ef81f33ce0ac9ef30236b95c3793935d843dbbae8791bbf`  
		Last Modified: Tue, 03 Dec 2024 05:23:41 GMT  
		Size: 7.2 KB (7231 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3117bcbd993e3753ba7f62fed2092e261302219fc4794bd60744b540753d2b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (65967270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae811cf19b5c01de9b3482a0673dadcd8b1b0567a12e943446c319bddbadee9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4d43724a324f138c88a78ca6df0a39ab6868bf1f121eb974439c5a51284e1ac2`  
		Last Modified: Tue, 03 Dec 2024 01:27:59 GMT  
		Size: 44.2 MB (44200109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff0e53b92c3d0f5c370d71aeac1be1d23e475f1afba41d896ace0ff6eeefc90`  
		Last Modified: Tue, 03 Dec 2024 07:36:14 GMT  
		Size: 21.8 MB (21767161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8bbb04311c4caa959ede4991344d0b4395a37e8c603b0c5b9755e7d0ac6b02bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4373586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2806b2b8fd080b94514ac3e7a4280190841cecba2a389c4572f92b9ad6b4352a`

```dockerfile
```

-	Layers:
	-	`sha256:9457386cd8923d16e0e33114929e464cb25582e303b69193cdfeb4b31b7ddf7b`  
		Last Modified: Tue, 03 Dec 2024 07:36:13 GMT  
		Size: 4.4 MB (4366354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dde010eb4616c79d3ca142e42b4cc8fb81c4de83e8cde4e7c18080b5fe8d6b0`  
		Last Modified: Tue, 03 Dec 2024 07:36:13 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:757ecd28399473cce91e6be523aec8e79ca9f576cfed067466bcffa71ff9ac70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71731493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed0620fbee6bbd337320d030c3be4e71b8e2883828902bf89672a74d1a36278b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac722d9cf93b238dec2480278a2df5f8ccb672c97ec39f191191fd39f6721a8`  
		Last Modified: Tue, 03 Dec 2024 05:38:46 GMT  
		Size: 23.4 MB (23405813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:79739c087c54ec0d652199829c30eaba59e426e5edf317a72b3a318dd0cd8bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4371586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc692a177ab4525e660f0d3f47205fd6ed2ad3a54e419ff10a28b6e48bc78535`

```dockerfile
```

-	Layers:
	-	`sha256:4816aacc299c61ab88c4e10c38abd2b3d51afb73adba3b8bb1debfd6846287a1`  
		Last Modified: Tue, 03 Dec 2024 05:38:46 GMT  
		Size: 4.4 MB (4364330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:913b8b80c5fa22b390e28ca34404e62e7d38090c8e99339fc5cdde2cf477b4ed`  
		Last Modified: Tue, 03 Dec 2024 05:38:45 GMT  
		Size: 7.3 KB (7256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5ddf951a80c7dec860666e1ff917ced4535353326c546dab88edcbab700e2345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74183048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:129a653e602a0fe253a2b069b2e2ab67f1ea9115e2fd72cc3ced51c193a26a5f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:53769c348e57d646b1ec110dabf9d81a3f570afdb3b8216d1178515e4ea4ce1f`  
		Last Modified: Tue, 03 Dec 2024 01:27:09 GMT  
		Size: 49.5 MB (49476152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b0c73f75a815ce87bbf2841b694fdc4c29bcd072480b8752e8e91f0b59097b`  
		Last Modified: Tue, 03 Dec 2024 03:23:49 GMT  
		Size: 24.7 MB (24706896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:eebaeeda8054688d6fd8c142a0fc0a9ccfa4fc3ca2b3499bfe916319c4994ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4368251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8937659e583da0ff6a76c8f743b3e42f34bd06dbbe6d065e151fb9bfada42aa`

```dockerfile
```

-	Layers:
	-	`sha256:729bb902df2997852a31087017dd8b75ede98123a831591b1b48e5519566d1b0`  
		Last Modified: Tue, 03 Dec 2024 03:23:48 GMT  
		Size: 4.4 MB (4361114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:310a36eb7785ee15a990c5d5843eb5ce31f673057b5dd6940687e2392aafaffb`  
		Last Modified: Tue, 03 Dec 2024 03:23:48 GMT  
		Size: 7.1 KB (7137 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:7ae289bc030a4b5e312465d3e015385f878f438f21b1723c31ae05301d012675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72229949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f8bd8c5b5ea753d9188c3db86b7f053f010d9de2a9dd1dfceb0a49d52a4d4c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8f7c3140f4f3af477253c748b229283137cca4214e1c3df21109b821f9227620`  
		Last Modified: Tue, 03 Dec 2024 01:27:53 GMT  
		Size: 48.8 MB (48771844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa54d74c5fddb1e648e0a4d95fcc8338f5800ff817646baaa9e6e65596d80c5a`  
		Last Modified: Tue, 03 Dec 2024 15:45:04 GMT  
		Size: 23.5 MB (23458105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0f04f4b64d87c286d8281dc28e82e764fcf2429c6f431b927f4f2b1b0e2e1b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 KB (7005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df656bed5425ba40a59f661b24a9ef00be8b445ae9820ef34b56825c81995052`

```dockerfile
```

-	Layers:
	-	`sha256:9973e5e44c5c8a102b2079d03531741e8919c0d04a2f710f280f74d5169fe092`  
		Last Modified: Tue, 03 Dec 2024 15:45:01 GMT  
		Size: 7.0 KB (7005 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:989e244c7923bf0590fb8ddd1cfda40228425477aed2564c4f1d68d5bf4c1211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77852114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9269507941157f6d8c2a6aaf7d982955bbd6ad996a59aa0c335382fa56fedbf3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c84d784fe3c6c2bd95dea1c0d6eeba7c981bfb75bd53f81e83bcaadd87bba6f9`  
		Last Modified: Tue, 03 Dec 2024 01:28:03 GMT  
		Size: 52.3 MB (52328222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f0cfea13db30ebc69124696ada25182d1141398cd301a47a2cbf3c10d7fa9b`  
		Last Modified: Tue, 03 Dec 2024 04:36:57 GMT  
		Size: 25.5 MB (25523892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a45e69e0d085a116675b75a7b725f816d6446a3fb4ca0543c48e95c3f3fd3978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4375753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e3cdc76dad87b7234f6f31c723d08c241a2a7efa8c9039144506f957faabb9`

```dockerfile
```

-	Layers:
	-	`sha256:238d77a8b35e0e5b35ee3bdf19e0102de9c1fb1aa37b9dbc272bed8d60d9852c`  
		Last Modified: Tue, 03 Dec 2024 04:36:57 GMT  
		Size: 4.4 MB (4368551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec9892333b13de0bc61e2cdc3ecce83c24ed20bb5579e82cfaa2d4bbcfb85f33`  
		Last Modified: Tue, 03 Dec 2024 04:36:56 GMT  
		Size: 7.2 KB (7202 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a0a6eb40a58c78dab49f2a7fbb55665c1a2af22ac7a1ac77580e07074365ec0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71014392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68d8461201f6697d48a6322c9ab07b91a4490ee92e53b559914223bb89b0a6c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:53a5c0dbd93a4a7f540e18bbe49ba3d7fadaa390ebbce009c756e34c5b1ae048`  
		Last Modified: Tue, 03 Dec 2024 01:27:55 GMT  
		Size: 47.1 MB (47149767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ded5bb0b377b736e6c5f45164fe8916ada3485441e963fe2fc0671949650049`  
		Last Modified: Tue, 03 Dec 2024 04:07:42 GMT  
		Size: 23.9 MB (23864625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bae73931459a569e6aa2c77e5721402acdd0fa87c8499ac00c378f09da2b74e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4370919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb35bd02c831221f27c85d64464a87ff1e458b43c43e1a167b9614f44689a992`

```dockerfile
```

-	Layers:
	-	`sha256:9c310eee549867fde8b1fd56ec371ef6cbb8f19c03df6ec7b8c6a49b4dcd0703`  
		Last Modified: Tue, 03 Dec 2024 04:07:42 GMT  
		Size: 4.4 MB (4363755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e932d932ad0e9d02444cefa5146dd7acdbe99b89f0389f686355c2b3271a1eea`  
		Last Modified: Tue, 03 Dec 2024 04:07:41 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:focal`

```console
$ docker pull buildpack-deps@sha256:1a40dd9495bc10ecfa6b69e15a1da148b54c00ab0f1b24adc2f26881947ab0f2
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
$ docker pull buildpack-deps@sha256:40083431ca62c9c4dc7354235efc7e8a272de74d3cad4ffe2efd08ecd5029363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210863816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:874eb12226c1dad0ceed95327494dc99847c16fe906f23654b5d83dba771022c`
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
ADD file:f76c848564adfa0c782654cd9423feee0ffacccd95abfe3e4e696203d5e61fbf in / 
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
	-	`sha256:10b337d353b3ceaf6823ab2d8696989401feed741b22eb313c8a0cd378762d39`  
		Last Modified: Fri, 11 Oct 2024 04:41:36 GMT  
		Size: 23.6 MB (23620412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961fa3ee3eee16522e395458be87f5269ec5b27ec4fcb4d916faeb1068afaba7`  
		Last Modified: Sat, 19 Oct 2024 06:42:29 GMT  
		Size: 9.6 MB (9620727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a338f01587f18e017e42cf3dfc75e5bd303749299cb0e64ea2a2a0865922d2`  
		Last Modified: Sat, 19 Oct 2024 08:17:06 GMT  
		Size: 55.9 MB (55881822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483891405091050bef8215a64be70ff765bb19eee55901429b24ee283116d3b7`  
		Last Modified: Sat, 19 Oct 2024 10:31:06 GMT  
		Size: 121.7 MB (121740855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:focal` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:93efc80be5ecab52a464d9fe7ee867901486937a09303516dfaefe6856243530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12105240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc243d6b55f7a192331109744e9df94b733026d4e2e155b63e40f6f0260451c`

```dockerfile
```

-	Layers:
	-	`sha256:a3dfa5079336624661fb047c1126818aed138720d84626c43c7747288cdc7e20`  
		Last Modified: Sat, 19 Oct 2024 10:31:03 GMT  
		Size: 12.1 MB (12094977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e0a3efb0dd55efc5a6fa32017808ac86585ba4027123cba07c6d7a58dc3cd9e`  
		Last Modified: Sat, 19 Oct 2024 10:31:03 GMT  
		Size: 10.3 KB (10263 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:focal` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d4c044d8e0f1effba941cff238b571cfeb2e4a19ef48e834457abf6cdc14e429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234622538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec51c60e90612793ad7dd898106f7378adf3b78ee245ebece43e8a95fedc228`
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
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a902a6ffa3ee5a0c3f67d06b1a3bb3611210a02b2f2878ae8c1ba1419d989ce1`  
		Last Modified: Sat, 19 Oct 2024 05:21:18 GMT  
		Size: 11.0 MB (10992039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974843836b66b5df8f55da9465dfaca000af6e2d0abe0b8f6cf9013fb718f2c3`  
		Last Modified: Sat, 19 Oct 2024 06:23:32 GMT  
		Size: 61.1 MB (61058312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa0b091012b7f1d636c962fb0be5c5cc11429d7830d5e6b97c54b6d42ef9e875`  
		Last Modified: Sat, 19 Oct 2024 12:40:50 GMT  
		Size: 136.6 MB (136598359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:focal` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:081e8fe779a686657480a819933b8e270cc9d4a9ed0057fea740342d5b1f93d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12294104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741bd60f669b009e3e0a4062ca49f681e688e44817deffa24b9007acdbd2d06b`

```dockerfile
```

-	Layers:
	-	`sha256:5a19cb8bb2ddaa8e4f7f6306c58bc420202117bf5f4953c8266fc40becfde627`  
		Last Modified: Sat, 19 Oct 2024 12:40:48 GMT  
		Size: 12.3 MB (12283819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8c2a0daf3e80482a28ac6ff19751369ba0d8a59de020a210728c4c86666bbf3`  
		Last Modified: Sat, 19 Oct 2024 12:40:47 GMT  
		Size: 10.3 KB (10285 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:focal` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ee2a5a58c33e111cce242e157196083fad8519580932bafb9f60fc1c7d30b42f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.1 MB (268105351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3117badda098ded0d13268050fc8f6f7a49dc25190131f2ce1a2f161da37e01d`
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
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
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
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e03dda56aeda86639422183ec93ff76ae68820943e9c534c079867713065a4`  
		Last Modified: Sat, 19 Oct 2024 04:11:36 GMT  
		Size: 13.0 MB (12961183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3475eebae315fac14d1638f5f55a0781ae70edd29e02e2525f0f7f09c1dc89ad`  
		Last Modified: Sat, 19 Oct 2024 05:26:29 GMT  
		Size: 69.7 MB (69663215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e33a43aa68ef75c0c7f240422932e3091598ee81550af17d6083e9a5023cb5`  
		Last Modified: Sat, 19 Oct 2024 13:55:28 GMT  
		Size: 153.4 MB (153404447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:focal` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c611eff47846c518010eca80d80d699ba66b52f8c53f95ece158a4ea61414de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12262058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd084947b42c1e302e6ec2e560ca6f80266cafe8f3d7aeab6bfade07cbcec2e0`

```dockerfile
```

-	Layers:
	-	`sha256:d51c35d85c5aeff236489fab5d3e8a4884636f3d091cea2a6eafedca79a9c924`  
		Last Modified: Sat, 19 Oct 2024 13:55:24 GMT  
		Size: 12.3 MB (12251821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbe51e9d84b971b16202ed46c5eac6475dcfae44ad6bf132ddc4f5014dc023aa`  
		Last Modified: Sat, 19 Oct 2024 13:55:24 GMT  
		Size: 10.2 KB (10237 bytes)  
		MIME: application/vnd.in-toto+json

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

## `buildpack-deps:focal-curl`

```console
$ docker pull buildpack-deps@sha256:4da6b2ff6ddf2c4364d0236b0a6fee455f768788ece240518c756ff7d4b06a8c
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

### `buildpack-deps:focal-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0422293bc781517a1205b2ba6dff7ba236217c9327f8af92e264ba52f93484b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38658092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90edfc157d0d40a2b2be22d1471c22b1abd30fce2d83cc55b4f3927fd7a3f52a`
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

### `buildpack-deps:focal-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:116a19e525bb1d8197b26528a2b5ef7fedd9b8d08d42e8f0a74b5f58b28976fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3060155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef3471432bdf86cd7eed5ee88b82b6d4f8bfa3b8b7fdcce6c6319530cd28365`

```dockerfile
```

-	Layers:
	-	`sha256:304c699502debcf5c70a97fb9fb35a4238f59c74a383b028c33d0138d0244daa`  
		Last Modified: Sat, 19 Oct 2024 02:06:13 GMT  
		Size: 3.1 MB (3053230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0ad0bc1951b5669a88f7481c27f808527008c18d6b05fcf4e25e2ac39fadc42`  
		Last Modified: Sat, 19 Oct 2024 02:06:13 GMT  
		Size: 6.9 KB (6925 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:focal-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0fdf25a37e79618b2acc9d2ffc3b5a1bd46effc5727538657c57796d88900e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 MB (33241139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7921c1e13d1125fcc881dee683609e7270392d779373f4b9fbddc619310ac41f`
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
ADD file:f76c848564adfa0c782654cd9423feee0ffacccd95abfe3e4e696203d5e61fbf in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:10b337d353b3ceaf6823ab2d8696989401feed741b22eb313c8a0cd378762d39`  
		Last Modified: Fri, 11 Oct 2024 04:41:36 GMT  
		Size: 23.6 MB (23620412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961fa3ee3eee16522e395458be87f5269ec5b27ec4fcb4d916faeb1068afaba7`  
		Last Modified: Sat, 19 Oct 2024 06:42:29 GMT  
		Size: 9.6 MB (9620727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:focal-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:94a31eb3318b611219d30a7394399d37e3208fcd20b753ee6afab05d21c37424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3062470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c57bae5f7f4ebbacc3f176472d95468cc7f460acc61b103e42637be1d2f6bdb`

```dockerfile
```

-	Layers:
	-	`sha256:7c2ec0cb6889c0b75216697a3f1ce6e08b6d61ffbb3a957ab4bfb07b47fe8bb9`  
		Last Modified: Sat, 19 Oct 2024 06:42:28 GMT  
		Size: 3.1 MB (3055486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c797b5ccbd5650ce46791a1edf2868f666be13330d6821a02488a65487ca39bd`  
		Last Modified: Sat, 19 Oct 2024 06:42:28 GMT  
		Size: 7.0 KB (6984 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:focal-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9d491d90c508287b19fbdd3b93681f83acebbef4632d594cb41d9ebf722f3e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36965867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44cef15a32fbc51f174b3570e4b8be2e24c07a196b0466fc546b6e5fe1d74c02`
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
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a902a6ffa3ee5a0c3f67d06b1a3bb3611210a02b2f2878ae8c1ba1419d989ce1`  
		Last Modified: Sat, 19 Oct 2024 05:21:18 GMT  
		Size: 11.0 MB (10992039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:focal-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ecaa54a4ed8a3abf2a0edd2e615be9a8e18fdb4eb9bc0b91d0afb8d2c4926720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3060481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7add9cc6fef9939e1897cc36b8fe6321415b509c213759804a5480ab813bba2`

```dockerfile
```

-	Layers:
	-	`sha256:b992674687c31519661dd0d849a6ad5bb284cd8612dff3f15d0b802fe207fd72`  
		Last Modified: Sat, 19 Oct 2024 05:21:17 GMT  
		Size: 3.1 MB (3053476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d1ca8e8e16915ab9608c16690a682d2d645bd137d2fbc137b9329b2bb15901e`  
		Last Modified: Sat, 19 Oct 2024 05:21:17 GMT  
		Size: 7.0 KB (7005 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:focal-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9810120f0cd96478e176022922fd783e953c80d776219d0319c2ae20c9813916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45037689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96261e974791e765a0357ae79f5e219bb3cd323acab789ba9da04094be5a8c5`
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
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e03dda56aeda86639422183ec93ff76ae68820943e9c534c079867713065a4`  
		Last Modified: Sat, 19 Oct 2024 04:11:36 GMT  
		Size: 13.0 MB (12961183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:focal-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c64242d8de1d7656fc9862aa1d77468227bf5bf5c630ef1bc407704a9d977e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51db9f907e8c6d21692c40ac2aa42d785ec63653e6c18cbad0ae4e8f7682939f`

```dockerfile
```

-	Layers:
	-	`sha256:9fb29c41083da621d5ef8abe6da2303447585e7fb9d9e85676cf0583d168977e`  
		Last Modified: Sat, 19 Oct 2024 04:11:36 GMT  
		Size: 3.1 MB (3057665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd60afd512ca4047963ff916bc36024a260432f1f636a594eb480fa5cce35737`  
		Last Modified: Sat, 19 Oct 2024 04:11:35 GMT  
		Size: 7.0 KB (6957 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:focal-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:c8428cf20044f6bc7409d9e28f1f66af5a3e7da17b81a9e33554bad3cb05a08a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.1 MB (33108292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2542a60b19a8a9a3b537e38fea15b2986fd1acdda726099843dd377022fbb1ad`
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
ADD file:f99ddac77e3940392223df513cab07fbc1fbae5269b21e7c49c63c99a7e47b14 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cdd35cb9ddeba9facdedc5a699ecb5f7e1e084b8cdfda59220bfd27ee7a2023a`  
		Last Modified: Fri, 11 Oct 2024 04:41:48 GMT  
		Size: 23.5 MB (23470304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3f7a8397059fca09a3b841b9b47ad382922b9b774e3da80dd14524248ab160`  
		Last Modified: Sat, 19 Oct 2024 04:02:45 GMT  
		Size: 9.6 MB (9637988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:focal-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cd36506002bf14a5d00dc790fb57726443f5d21a5e4072e23d81a30faea8514f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3054237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2541cc0782b841d64b43fef60fc0de23e4676b09303756460d023d68b65d66`

```dockerfile
```

-	Layers:
	-	`sha256:43b403be2044cbef0569ac19158e5464762dad979d77e66171d808e34b1a96b0`  
		Last Modified: Sat, 19 Oct 2024 04:02:45 GMT  
		Size: 3.0 MB (3047281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e64e18cf52baacada1162860503b13cb0e61e70b5fc9a412874df2b2d252d6e9`  
		Last Modified: Sat, 19 Oct 2024 04:02:44 GMT  
		Size: 7.0 KB (6956 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:focal-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6d0ac57e34e6bb9d9f6259248550710cd0058623e7e4ca78ab46b4192a2036c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37070082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f3ea841ac59ea4fbf46c6347106c6e25a2a0316de2c94b17e90eb9502ee05f`
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

### `buildpack-deps:focal-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:84a2fd64d7421f9b58a38571d28640279ccf14b90c6610534fe2567eedfd7b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3061576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45953e26d9d11711c42489b08452279cdaf4d825d7d523cc54abd4e2f9dfd947`

```dockerfile
```

-	Layers:
	-	`sha256:5a3bfaf8e95468b6c63311e69ff1e42dfa9bd4cec20c212644f34d10aa625abe`  
		Last Modified: Sat, 19 Oct 2024 03:49:50 GMT  
		Size: 3.1 MB (3054651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a772f47e4c62792ece737b5a02011c8d96e4cbfbe9b8c37fedd7ee037d285a6f`  
		Last Modified: Sat, 19 Oct 2024 03:49:50 GMT  
		Size: 6.9 KB (6925 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:focal-scm`

```console
$ docker pull buildpack-deps@sha256:5308dfd69986e614671317b78b8ad45eb8bcb97f72afad03eb557428a11526e1
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

### `buildpack-deps:focal-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:34d00f41b14c40e6903e630fb94b859f9e05c36b7016df768ccfa1791d797151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.6 MB (99583642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e735b8910a6f0ef6d4a756b8614bd1c6fa2d31394533387b293ca533eae4490`
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

### `buildpack-deps:focal-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5a367f3106529937f6d37be0ae11abc812d3e24785307e1385173da9994b8b50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6680317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad62135b54e4b9715fb84ab88175f2b45bd6498a4d542e12d0ccacdd3ff1cad2`

```dockerfile
```

-	Layers:
	-	`sha256:222103d54b5ac8552ee50b42ecb802826506750cb0de3b1f27df69091e2249e8`  
		Last Modified: Sat, 19 Oct 2024 02:52:26 GMT  
		Size: 6.7 MB (6672935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f7f1f4ec088e4b6693c82001f201f75294ee1d693ede49bcfb6da307ec1cd5b`  
		Last Modified: Sat, 19 Oct 2024 02:52:26 GMT  
		Size: 7.4 KB (7382 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:focal-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0ba9733556367b696f7f8c98162a8b06ea14e455f9b4ce45e091a19a7df636e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.1 MB (89122961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:377e8a14c1c6f6f2f02d1e4e2b9794620d29ee881d57a1658519a7d1f9dbbea0`
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
ADD file:f76c848564adfa0c782654cd9423feee0ffacccd95abfe3e4e696203d5e61fbf in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:10b337d353b3ceaf6823ab2d8696989401feed741b22eb313c8a0cd378762d39`  
		Last Modified: Fri, 11 Oct 2024 04:41:36 GMT  
		Size: 23.6 MB (23620412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961fa3ee3eee16522e395458be87f5269ec5b27ec4fcb4d916faeb1068afaba7`  
		Last Modified: Sat, 19 Oct 2024 06:42:29 GMT  
		Size: 9.6 MB (9620727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a338f01587f18e017e42cf3dfc75e5bd303749299cb0e64ea2a2a0865922d2`  
		Last Modified: Sat, 19 Oct 2024 08:17:06 GMT  
		Size: 55.9 MB (55881822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:focal-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c18c710ecbecc029c07733f7765b2f163752893001e68ce08dfa5f0f3e846abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6684182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29e5d67ea012adced3850967514aa055bc6596d9ef92cf55c25639702fbffec`

```dockerfile
```

-	Layers:
	-	`sha256:40f96d345c76424d7b3c8ace311292ea3a9aa7f22d9b83d18a60094bf4a764d6`  
		Last Modified: Sat, 19 Oct 2024 08:17:05 GMT  
		Size: 6.7 MB (6676742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f0da6b23a5b46534b605e78a83f2bf98bdfc1c58eaaf4142df4f9670439c20a`  
		Last Modified: Sat, 19 Oct 2024 08:17:04 GMT  
		Size: 7.4 KB (7440 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:focal-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6b30fe5bf79eee34ede4c981ec37e717dac184636d31316f4b5aaa4cb6679c82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (98024179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78df7c0741cdc3adb599669b8f74233ec3eccaa3eb58c8a1976e46b9aa54db05`
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
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a902a6ffa3ee5a0c3f67d06b1a3bb3611210a02b2f2878ae8c1ba1419d989ce1`  
		Last Modified: Sat, 19 Oct 2024 05:21:18 GMT  
		Size: 11.0 MB (10992039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974843836b66b5df8f55da9465dfaca000af6e2d0abe0b8f6cf9013fb718f2c3`  
		Last Modified: Sat, 19 Oct 2024 06:23:32 GMT  
		Size: 61.1 MB (61058312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:focal-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a19eb135cd6e631684d950b21e75be25d53d984b22fee5ac59d8c35efa2190aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6686824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eca2dc35be6a27a8a79e0940d953aece87ff8ecadf07487672f9c679d28c687`

```dockerfile
```

-	Layers:
	-	`sha256:a5b24f0e1d3b860b1596fd6b36a9dc5f9db79e913aea0444d579207d300136ce`  
		Last Modified: Sat, 19 Oct 2024 06:23:30 GMT  
		Size: 6.7 MB (6679362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:833904452c5bb38d61fb3efa3215ce3556792679f83594c2de9df3253152ac2d`  
		Last Modified: Sat, 19 Oct 2024 06:23:29 GMT  
		Size: 7.5 KB (7462 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:focal-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b7f3a2a0b03c9b3739e20aac8fe63515dbfa0db054b4d24b1f85886a6ff78afd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114700904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9c4c3362426c92c41177005099f31d0b10f6ed46e627ba49bbe8370d37e691`
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
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e03dda56aeda86639422183ec93ff76ae68820943e9c534c079867713065a4`  
		Last Modified: Sat, 19 Oct 2024 04:11:36 GMT  
		Size: 13.0 MB (12961183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3475eebae315fac14d1638f5f55a0781ae70edd29e02e2525f0f7f09c1dc89ad`  
		Last Modified: Sat, 19 Oct 2024 05:26:29 GMT  
		Size: 69.7 MB (69663215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:focal-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:899df7b946b9514a555cfa2a174864bb004b02e4e5ab38a3c92bcec8b94b329d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6688198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7310d0a6f41d33f7e0cde1d62a443ebd561f51eb96862dc216534bda751ce5d`

```dockerfile
```

-	Layers:
	-	`sha256:9afda855d0714a2365d893ece73ef0ab746d0b366447423313a1cbcaaada5c0b`  
		Last Modified: Sat, 19 Oct 2024 05:26:27 GMT  
		Size: 6.7 MB (6680784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a187459158467c0224722890e007ccbb8103fd30c10a7ab3846fd2bd76d1e2c6`  
		Last Modified: Sat, 19 Oct 2024 05:26:26 GMT  
		Size: 7.4 KB (7414 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:focal-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:013c8233697ec9233865c4544b1cd30ba9279bbd680ab1cb5cd9ca29bab7f107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.4 MB (97425179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b297fa71b915ef8a232e93142c280bd8992a61966f6e1796c669dcd9df91b8`
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

### `buildpack-deps:focal-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:726a303218623b57ec890bd1e8aeb189e63595dce25987a48c801b9e6eb88c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6680392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d6c1c134ce9f29796e2edb349dca6a5efb877a1488648756ec614249c4442b`

```dockerfile
```

-	Layers:
	-	`sha256:0461bcd63c219bd2ede354bbb15f8aefa56d2e62d062bbb9e4154abb83e120c3`  
		Last Modified: Sat, 19 Oct 2024 05:10:42 GMT  
		Size: 6.7 MB (6673010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0da6957fefcd4006ddf29690171e830dfa4d1fc366257b8fcccbe3e718288e03`  
		Last Modified: Sat, 19 Oct 2024 05:10:42 GMT  
		Size: 7.4 KB (7382 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:jammy`

```console
$ docker pull buildpack-deps@sha256:9c6387be70924dc253a6c5594fd11bf8c90a19528442ee8b0b4040362bf1a662
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

### `buildpack-deps:jammy` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d4b8b06ff286846741b4328c1bdf1657d2db64f40f60077770c684e6a84f227f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.0 MB (248987672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760f30692921f381d34172bbbdecd515b01faa8ca2938b65627e9deaa51a0e8a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8284ddf57c03d97884a998219f0fbd84edab303351cdba3ac1526a116e907210`  
		Last Modified: Sat, 19 Oct 2024 02:06:18 GMT  
		Size: 7.1 MB (7102850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9649a6c09e0ee6b937917264d660cd3c815e5ee060c6bc8b89795f658ce584`  
		Last Modified: Sat, 19 Oct 2024 02:52:49 GMT  
		Size: 39.5 MB (39468948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63a153d37d1263e4b6d637c2feb8c983a79dba3aed17ebc110021215169e062`  
		Last Modified: Sat, 19 Oct 2024 03:53:32 GMT  
		Size: 172.9 MB (172880186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:70feaa3e74d0fdb30ec118da0f1d026b137a88e5f7b3a1c9840b07b5baa4dfb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11483927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d97f427a14e1bfca0a95e4de47073b526915ae0f04dd9bb5e6427f9116625dc`

```dockerfile
```

-	Layers:
	-	`sha256:8a7b33f044878adb0a53509f4157f07964d9fe166ea13bf90834fc96ffd7ad99`  
		Last Modified: Sat, 19 Oct 2024 03:53:30 GMT  
		Size: 11.5 MB (11473724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b190dc68ad16997d500a1ec5f110f5645339adda6c4262af41508621b6e389b9`  
		Last Modified: Sat, 19 Oct 2024 03:53:29 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e9e8f9849a391919a9847d9a06e60353e4f78178d3a8b47af1bcbbf0e4bbd65b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.2 MB (216227091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bfdd0166ea17d4aabff352d18a61948531732eb65b495195cb8c34aeff83d8a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:291158c1d919b2d4290b5112a77dc0f7bdf0d45caa53b3556390707d29d2796a in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b477f0f37762a62f631ac4fbaed78c3b23c47db7ac1eaefe95bda0e85ce052a0`  
		Last Modified: Wed, 11 Sep 2024 17:24:53 GMT  
		Size: 26.6 MB (26639293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0953d000943dc8cda05d3be64d712749134d74c6845fe067d2f5a8238e2a5378`  
		Last Modified: Sat, 19 Oct 2024 06:44:26 GMT  
		Size: 7.0 MB (7008052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c5928c39ec338a3e1fcfb711133fed58c4bf8eecf83d91cb2d031a604ede55`  
		Last Modified: Sat, 19 Oct 2024 08:18:32 GMT  
		Size: 42.2 MB (42246833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a42398c457c6ff3c563e93ddd72302080b5be56e41fc4b9cd61c89a565f2d37`  
		Last Modified: Sat, 19 Oct 2024 10:35:16 GMT  
		Size: 140.3 MB (140332913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ddc64d488f547e916a2309a01182e17e703e71ee4eb231e65a82b8a5b1d85c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11274363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:798737324873cec731a9ea8db36d65ae241f36df6da922028438d244414c1bf1`

```dockerfile
```

-	Layers:
	-	`sha256:dce4007c347f0a6155e483e4e34dc4b824baecea35a2445b83d7878bccf4bb4f`  
		Last Modified: Sat, 19 Oct 2024 10:35:13 GMT  
		Size: 11.3 MB (11264100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:318e399acd31061100875c4637aad70762357b54bef40d932a04a3a0c9c9dbc6`  
		Last Modified: Sat, 19 Oct 2024 10:35:12 GMT  
		Size: 10.3 KB (10263 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c7234792a1b8cc508b4678cee66dfef20a0187287f0ff4f6bd2abcdb2f2e9206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.1 MB (240121701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a56bd018cc7818fcfc0c7d5e8d66aadd7a84c6c3687f88c35f9356319a89ad0c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee2b4e5eab18cf336bf82b89529f3587544f710c5e1a0aa67e5ed1fdec85146`  
		Last Modified: Sat, 19 Oct 2024 05:22:20 GMT  
		Size: 7.0 MB (7049559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b264c39c10afdefb042a206e923fa9957e0be85910e8e5065516f128089520da`  
		Last Modified: Sat, 19 Oct 2024 06:24:51 GMT  
		Size: 39.4 MB (39382310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b485acb9c0d30e4a45e9abe1af8dccd9801786bd715c74da323dad89f4bfa92a`  
		Last Modified: Sat, 19 Oct 2024 12:44:54 GMT  
		Size: 166.3 MB (166331503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:757afcc319006f3cf36e7e61ce4eb31547bf81200b78a9c1244d7cf46a2f3ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11479663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0939c54b503f2c5f969194073db614c6b9edf2f105e0999da8027cdf5ca846af`

```dockerfile
```

-	Layers:
	-	`sha256:113d1a92adab8cba7e14939a85617e525a4c413657fbdf36090f022e572d039a`  
		Last Modified: Sat, 19 Oct 2024 12:44:51 GMT  
		Size: 11.5 MB (11469380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96e77f50a0049e1a52a45ec497c71734226905319a0e31ae7d4e92e66f75ab39`  
		Last Modified: Sat, 19 Oct 2024 12:44:50 GMT  
		Size: 10.3 KB (10283 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:71c29684f3a500f9e7d9f88a61ccc3fbea0c72c0c6784e8fb33d799fb1f6e7d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269786527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5039907a5e2568a8b22a12f22cfce64c22f0494eb48f13be18dd296ff622bb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ba759f0622bf9c0e3a62cfaaeedbf629b4a47bad21f09b1f342bd764ad4fc6`  
		Last Modified: Sat, 19 Oct 2024 04:12:41 GMT  
		Size: 8.2 MB (8205814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c923a94cf4353da40bb3b1253640fb7f53899172c56a3d08e7ab97106e9fae`  
		Last Modified: Sat, 19 Oct 2024 05:28:18 GMT  
		Size: 43.8 MB (43761297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c7288a891c79b2e722c068b6342514abbaca2b0b8a59519d18f7bdc4d1bb4c`  
		Last Modified: Sat, 19 Oct 2024 14:00:45 GMT  
		Size: 183.4 MB (183371174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2e2b205d1fb1a96ad4dc8ce6319b090deaea483b19e72bd94eaec63fc7798594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11442701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d771cd24220f8c054a7bac19df98afae4690de4be490b95f0d69e37a607db97`

```dockerfile
```

-	Layers:
	-	`sha256:119f3b98f8d296ef4dea15628870f1bbd266cf1752e4b5abd67c2f84c4aa182e`  
		Last Modified: Sat, 19 Oct 2024 14:00:40 GMT  
		Size: 11.4 MB (11432466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0dd88025aa4b45ed0abc1ed1588f47870d67e6bca8ebd87d5c9f26fcafcc67b`  
		Last Modified: Sat, 19 Oct 2024 14:00:39 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:1afa69bd96855d8248fdba88a69258839c572cb7b2dac2ce75077bb67848c381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274113264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2adea3b29bae5fcd5a6adefbd9ff8f276c9e7fc97fb6fc64afd6b7126802699`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:d73c592fd8b1cf53b1e79e60cc01a9371bf9156f299ddf5a8482ea43525aaa9a in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6579073ec343e2eff1822992b7ff52b06a067be5c14999033789394aadca585d`  
		Last Modified: Wed, 11 Sep 2024 17:25:05 GMT  
		Size: 27.0 MB (27038996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef216c90e55bcafd475d74f40962beb13a5a26ac03f5cf90bc3879dfabc5db04`  
		Last Modified: Sat, 19 Oct 2024 04:05:55 GMT  
		Size: 7.1 MB (7116572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c25cfae42e3c0e2795e05916aefa3b950bc058947a8a8a9b1e38197627712b6`  
		Last Modified: Sat, 19 Oct 2024 05:36:08 GMT  
		Size: 42.3 MB (42309710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8b23b2911e88d71f2c712bc659cb5aeda7ad0f3bafcc8a08c792987ef23c64`  
		Last Modified: Sat, 19 Oct 2024 07:35:12 GMT  
		Size: 197.6 MB (197647986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:09045a7fabc47e2b581c1b01bab7aed6cc5f6883e9021d8d2b67a9058a1547d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11425790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a30f25b563bc0af385b3f10a6f762fd2c7e3830a01c7595566d6e22eb571e8f`

```dockerfile
```

-	Layers:
	-	`sha256:ab2b88b1bcd23b0b9ba9ef4832308137caf116dede95dd91410a525056b9d0ef`  
		Last Modified: Sat, 19 Oct 2024 07:34:46 GMT  
		Size: 11.4 MB (11415555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73c3843a7566422eb997cf6fd44192354044fb45f91880a3a4b88e73041a1348`  
		Last Modified: Sat, 19 Oct 2024 07:34:44 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ec33a2063ef5aa4756aef87fd8a958c89053f520e17b5beab973c72046ab73ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222948887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c6652a81bcdf5919387801cb65d42094fdbc9a4423f0ae1c0079c55eb9c997`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69520da589bb4a5afebcb33e75154687a27523df1667ed280e4056c48d0f9ab2`  
		Last Modified: Sat, 19 Oct 2024 03:50:51 GMT  
		Size: 7.0 MB (7016679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92120d25a5bd34685129dc03eb81c53d37e34f8d347a42193df4f92bbcdcc0e4`  
		Last Modified: Sat, 19 Oct 2024 05:12:06 GMT  
		Size: 39.4 MB (39401291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f27d67cf1107dad4d1fd687bc141375a87454b71e0b9fcc7f3f5e1f4142e177`  
		Last Modified: Sat, 19 Oct 2024 06:58:36 GMT  
		Size: 148.5 MB (148529442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8670708200c1354cc2305964d8f7e0e6e674cb76bee77589538cbf4a782c4566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11298722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5db8b36cafc56df975ba4f7f3249442e8ddb4f87ad576e344254e9bb3a3761d`

```dockerfile
```

-	Layers:
	-	`sha256:35631ba052bd0c28ea0d31125303e40050b1def645355f2943e41baf4d66b081`  
		Last Modified: Sat, 19 Oct 2024 06:58:33 GMT  
		Size: 11.3 MB (11288519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8c41a739e5a3f102f7913049b5db83525a238a20625272f15112ab8ffbef145`  
		Last Modified: Sat, 19 Oct 2024 06:58:32 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:jammy-curl`

```console
$ docker pull buildpack-deps@sha256:85596490cf18e74c534e123e29d7bcbc30182fae51129525148111645a7ad569
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

### `buildpack-deps:jammy-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e9e575bbf5fbd08b92fddfefa92a1f03825ef05ad773b4487eee6acfed264837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36638538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f765ea36fa4c46759dd690bb21cb8e45f32e1aa331cf9ad0da8b14816aa41ea3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8284ddf57c03d97884a998219f0fbd84edab303351cdba3ac1526a116e907210`  
		Last Modified: Sat, 19 Oct 2024 02:06:18 GMT  
		Size: 7.1 MB (7102850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3ad27316a38d3124ad8c0ef153c2a1fd356e6101cd2de78b49c0a1517f8e5f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3059492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078a608399f965e1ef663c83205965174b05b375eba24e149c27e9cab4aeb91d`

```dockerfile
```

-	Layers:
	-	`sha256:1abede6965aa4c2f6dc7a23f51f9c10eab34e628cee2f9817cc259b2558d4d18`  
		Last Modified: Sat, 19 Oct 2024 02:06:18 GMT  
		Size: 3.1 MB (3052568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1388bf3300d1894b794c3a79d61de4d5106bdcc7c16afd59021479c3346dc8a5`  
		Last Modified: Sat, 19 Oct 2024 02:06:18 GMT  
		Size: 6.9 KB (6924 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:20fc212e38dd71fb2c3c9914fc825a38358e81e134db6923889a1c303f0ae326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.6 MB (33647345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbba2125fdb8a2505c8f55e2499e2f13553a82c47d377d9c493fcb3f60c7f4ed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:291158c1d919b2d4290b5112a77dc0f7bdf0d45caa53b3556390707d29d2796a in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b477f0f37762a62f631ac4fbaed78c3b23c47db7ac1eaefe95bda0e85ce052a0`  
		Last Modified: Wed, 11 Sep 2024 17:24:53 GMT  
		Size: 26.6 MB (26639293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0953d000943dc8cda05d3be64d712749134d74c6845fe067d2f5a8238e2a5378`  
		Last Modified: Sat, 19 Oct 2024 06:44:26 GMT  
		Size: 7.0 MB (7008052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:eece698d153df1f89fadfff448417adeb8215fd72b047ac459cb49353fce45c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3061858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79401084f8905bad1c4c968bee99d939840fae67ed54244f77a6d632b50ab6c4`

```dockerfile
```

-	Layers:
	-	`sha256:f07353059a36e79f6b9030cb13757b44c6245824987503b83d6f536a4e693a47`  
		Last Modified: Sat, 19 Oct 2024 06:44:26 GMT  
		Size: 3.1 MB (3054874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb0a469469d317122a2932b0e26adba945e4a5d58bb8da9bc08083568288073b`  
		Last Modified: Sat, 19 Oct 2024 06:44:25 GMT  
		Size: 7.0 KB (6984 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:41102486bd331fc045ca4dd0c7ab19df349ce8fa115a386073d582c5ebaf4b77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34407888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f8ad5d876c3264e3479b020c677f69f46a7e69fe13035ad9e201a14c7d7a6a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee2b4e5eab18cf336bf82b89529f3587544f710c5e1a0aa67e5ed1fdec85146`  
		Last Modified: Sat, 19 Oct 2024 05:22:20 GMT  
		Size: 7.0 MB (7049559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6ab6df736a4f64794b5d01d640d59584d49c7c2fb01273eb94880893d1ad7b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3059838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5452a80b64ba34c05b9e80ad169c456c03a4d42060f09c71f9ee69d77e1914b4`

```dockerfile
```

-	Layers:
	-	`sha256:ceb05956e7d16f0743e8d98b6d5fbaff860dab57442acf4c9f2976636ebde31a`  
		Last Modified: Sat, 19 Oct 2024 05:22:20 GMT  
		Size: 3.1 MB (3052834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:853ec9692386086ec112b4a3f1d935035560feac8084776b25e1da098a367767`  
		Last Modified: Sat, 19 Oct 2024 05:22:20 GMT  
		Size: 7.0 KB (7004 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8c440e8edd3fc6eb6303246ef73f5fa811c9701bbb92966f11d77e3772040b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.7 MB (42654056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ebb57a604797dde5d006fe5668f0568828131689c956f6a9f96516dde9378c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ba759f0622bf9c0e3a62cfaaeedbf629b4a47bad21f09b1f342bd764ad4fc6`  
		Last Modified: Sat, 19 Oct 2024 04:12:41 GMT  
		Size: 8.2 MB (8205814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fb640bcc8b1fb70fe5dbe39d90903b445716812fdf4a37ad87f41db230205f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92641cdf3683b1f21313af156d1c37fe47ef9052962af565bbf3a34a63c5e49a`

```dockerfile
```

-	Layers:
	-	`sha256:d957ab9ba0e3cfef7c2cd76d148d5d72b675f5cab4596bedc554a0c7c965c4d4`  
		Last Modified: Sat, 19 Oct 2024 04:12:41 GMT  
		Size: 3.1 MB (3057063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30ad65d10290bd28b22bc51bbf57a7def5ae2d467694c5087b06f33c038c8b63`  
		Last Modified: Sat, 19 Oct 2024 04:12:40 GMT  
		Size: 7.0 KB (6956 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:179857b8adde6f954375127a2dd12caeef247d7be9af5c177b00fe3c40076222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34155568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f190c58725abd84359210464a4a8e6e08e5c21a2e2f30c4d6619fcd0f427c4e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:d73c592fd8b1cf53b1e79e60cc01a9371bf9156f299ddf5a8482ea43525aaa9a in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6579073ec343e2eff1822992b7ff52b06a067be5c14999033789394aadca585d`  
		Last Modified: Wed, 11 Sep 2024 17:25:05 GMT  
		Size: 27.0 MB (27038996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef216c90e55bcafd475d74f40962beb13a5a26ac03f5cf90bc3879dfabc5db04`  
		Last Modified: Sat, 19 Oct 2024 04:05:55 GMT  
		Size: 7.1 MB (7116572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9543357c11475894edd32d6735f47929fbdcc2009261bfd0f41ae2fd3acd156d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a67e05f8df84faa6dd71a4f2fecfc217e7394e6a5e95728cc5fc96ac6419608`

```dockerfile
```

-	Layers:
	-	`sha256:9add722049583dcb3f1fa4cbff5ab2c66da1d0d4a7599508207ef70e62a77c73`  
		Last Modified: Sat, 19 Oct 2024 04:05:54 GMT  
		Size: 3.0 MB (3046665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42a956a517e54dbc6ea7485daeb102dfa8babacace0704cce1c28d03ace46992`  
		Last Modified: Sat, 19 Oct 2024 04:05:54 GMT  
		Size: 7.0 KB (6956 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a057da907e6159116c1d6b558d76d2a226bd00cc61f02d6c039bd9ead6cd6bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (35018154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ccb112658f15462f21c737ef77f946e275af373679709c0f95834404e426235`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69520da589bb4a5afebcb33e75154687a27523df1667ed280e4056c48d0f9ab2`  
		Last Modified: Sat, 19 Oct 2024 03:50:51 GMT  
		Size: 7.0 MB (7016679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:86df1e572c2fdf579e24bf8ca6d6bbfd8905398fa586cdc97cc9a957aff4ca75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3061713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb63a62d2750a3d6dab0c24c174e5480aebb92715818dfc54fa348c77a25ba9`

```dockerfile
```

-	Layers:
	-	`sha256:77ac86a3a24d3e0653a3ae6467144940afee5c73c0bdc2583a25dcb8e2ae75c4`  
		Last Modified: Sat, 19 Oct 2024 03:50:51 GMT  
		Size: 3.1 MB (3054789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19f8b337c9885e2ecf77ae2d622ed549a5f5f5485df0dccadac74cd47c47d940`  
		Last Modified: Sat, 19 Oct 2024 03:50:51 GMT  
		Size: 6.9 KB (6924 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:jammy-scm`

```console
$ docker pull buildpack-deps@sha256:65b6be032f9d7e64ea541e00e48c71bd961be04741c6d688f33218ab031a9f9c
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

### `buildpack-deps:jammy-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:17942397e5fced3f8b300ac7c7eb615dff08e3bf4b25ff7d4fdf0e50dc0e3637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76107486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8ee0b5a3fd03948f634e632da31c66362c3663e3c5dd9e1e0c262c2266ed67`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8284ddf57c03d97884a998219f0fbd84edab303351cdba3ac1526a116e907210`  
		Last Modified: Sat, 19 Oct 2024 02:06:18 GMT  
		Size: 7.1 MB (7102850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9649a6c09e0ee6b937917264d660cd3c815e5ee060c6bc8b89795f658ce584`  
		Last Modified: Sat, 19 Oct 2024 02:52:49 GMT  
		Size: 39.5 MB (39468948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:754d2bec28ffc00a26e2f7a1354ed7ae0d3775ed7f8e8ef4d4d940cf534818f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5616367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1aef2e9a39d9f88806281cb44ebdae0758f7e0875bb44eec230ab7b038d1f21`

```dockerfile
```

-	Layers:
	-	`sha256:3746959abc49b330e29be49c40d27e7319253b12cd58a2f8585e96ca7d34fa7c`  
		Last Modified: Sat, 19 Oct 2024 02:52:49 GMT  
		Size: 5.6 MB (5609043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f77b1e734b0869190432a877573774367e039f62d93c379d4dffcf3156b081a7`  
		Last Modified: Sat, 19 Oct 2024 02:52:48 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:36f7f482089e1c9ff1e74c91cd11616da25679c73d6f5b9402c848167bc1560c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75894178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98bb0b7cfb61a6bb25c1de92dc0b7b3b9880b0cb8143292ebd52ffda4d80d9ed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:291158c1d919b2d4290b5112a77dc0f7bdf0d45caa53b3556390707d29d2796a in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b477f0f37762a62f631ac4fbaed78c3b23c47db7ac1eaefe95bda0e85ce052a0`  
		Last Modified: Wed, 11 Sep 2024 17:24:53 GMT  
		Size: 26.6 MB (26639293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0953d000943dc8cda05d3be64d712749134d74c6845fe067d2f5a8238e2a5378`  
		Last Modified: Sat, 19 Oct 2024 06:44:26 GMT  
		Size: 7.0 MB (7008052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c5928c39ec338a3e1fcfb711133fed58c4bf8eecf83d91cb2d031a604ede55`  
		Last Modified: Sat, 19 Oct 2024 08:18:32 GMT  
		Size: 42.2 MB (42246833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b6fdd0ec46e198e0ec0a9fa83af06d9521e50887c9083df6f8b93b265c06c118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5617703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62d57e04a27948c0eb865140b4c66fe12724cc8de7227bfa2d2c599e14ef1ba5`

```dockerfile
```

-	Layers:
	-	`sha256:c81a8e1f595d9f463820b3485fecf663109b333695ec89dd112ce92d25397383`  
		Last Modified: Sat, 19 Oct 2024 08:18:30 GMT  
		Size: 5.6 MB (5610319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aea552147d8c9174fa2a375b8191da83bac8a92276871696f8078bcc4d2208aa`  
		Last Modified: Sat, 19 Oct 2024 08:18:30 GMT  
		Size: 7.4 KB (7384 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3b4dc315b2f43492a8caf18705f18b4ecf52ef4f30ae0b852c5b43bd83f1edcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73790198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0040e9b18bab25e40c4dc3bcb25bbeff1e6e35d6c4156e9559e032772c502f6e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee2b4e5eab18cf336bf82b89529f3587544f710c5e1a0aa67e5ed1fdec85146`  
		Last Modified: Sat, 19 Oct 2024 05:22:20 GMT  
		Size: 7.0 MB (7049559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b264c39c10afdefb042a206e923fa9957e0be85910e8e5065516f128089520da`  
		Last Modified: Sat, 19 Oct 2024 06:24:51 GMT  
		Size: 39.4 MB (39382310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:457c35d342663a69ec383a5df6b75820fdfb7f2dd8d5d94169416d8320c0143c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5622847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22210069278fbb79bfaf97a95dcaac2c228a24e7481e7d2f350821064c3e2c1c`

```dockerfile
```

-	Layers:
	-	`sha256:c4f843d61bcf7f9c51d7e2a70cbfda18a9a4dce752481ec5d0da09f4a91f0682`  
		Last Modified: Sat, 19 Oct 2024 06:24:50 GMT  
		Size: 5.6 MB (5615443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49eec21858e105c95bdf207c9a3a4473510b952446b3cdeb902fbcfbc1d5574e`  
		Last Modified: Sat, 19 Oct 2024 06:24:50 GMT  
		Size: 7.4 KB (7404 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:dc92a9760be21890e640c7a93bd240ae83b1dd8cd476082ec342f8bbb0589dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86415353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f942098a3824a00b40abfa837c90a6702a23adae15d4aab412018f90518f4e1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ba759f0622bf9c0e3a62cfaaeedbf629b4a47bad21f09b1f342bd764ad4fc6`  
		Last Modified: Sat, 19 Oct 2024 04:12:41 GMT  
		Size: 8.2 MB (8205814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c923a94cf4353da40bb3b1253640fb7f53899172c56a3d08e7ab97106e9fae`  
		Last Modified: Sat, 19 Oct 2024 05:28:18 GMT  
		Size: 43.8 MB (43761297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ca42ab3869cefe7a695a4e1f169c8bbf958e6c018b01d10eff974346b2253ebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5624067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec53006865d81586277bbd8d711c33a775261feefb77a1abce185763b0414f47`

```dockerfile
```

-	Layers:
	-	`sha256:69b993149892bd952ac1d559783e53290067df7e12a0f4a411971f13fbfb7eb6`  
		Last Modified: Sat, 19 Oct 2024 05:28:17 GMT  
		Size: 5.6 MB (5616711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe45130b58e9b94959acbac2f5825ca053b3c0be9651aebeea0abc0f0441c826`  
		Last Modified: Sat, 19 Oct 2024 05:28:17 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:4ddc9e5dc332305f385db2d46e6106bdb9a6df770d34cce1a7b1328e9f773581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76465278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596a39522065aaa5259e07bfd7e3ab09944aa66546dfb4f4072cdd1c36988395`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:d73c592fd8b1cf53b1e79e60cc01a9371bf9156f299ddf5a8482ea43525aaa9a in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6579073ec343e2eff1822992b7ff52b06a067be5c14999033789394aadca585d`  
		Last Modified: Wed, 11 Sep 2024 17:25:05 GMT  
		Size: 27.0 MB (27038996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef216c90e55bcafd475d74f40962beb13a5a26ac03f5cf90bc3879dfabc5db04`  
		Last Modified: Sat, 19 Oct 2024 04:05:55 GMT  
		Size: 7.1 MB (7116572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c25cfae42e3c0e2795e05916aefa3b950bc058947a8a8a9b1e38197627712b6`  
		Last Modified: Sat, 19 Oct 2024 05:36:08 GMT  
		Size: 42.3 MB (42309710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:677e3217d2dc918ca5ab384bfca869b7e8c8305316cb1cc037f141956b0b3272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5606953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55cf4c2b60436fb8bd0fa2d4b50a36c087d7488d743693396d221ec0491c7180`

```dockerfile
```

-	Layers:
	-	`sha256:b1f512202dcb2b5d928ecb4585d6de15c42669027b7a5d4579e1bddcdb7a2df2`  
		Last Modified: Sat, 19 Oct 2024 05:36:02 GMT  
		Size: 5.6 MB (5599597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7354a339140b887de10c47610cf80258f8ee49298f940c212168e99cf717cd83`  
		Last Modified: Sat, 19 Oct 2024 05:36:01 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3f5839289113a1c014b308f044c1d2090b5de0b459d03509d92a76e98dd8c5e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74419445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e04f9df778c0f0af647e3031be3af40bb003c80f1d79b43a2fb836cbafb4bb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69520da589bb4a5afebcb33e75154687a27523df1667ed280e4056c48d0f9ab2`  
		Last Modified: Sat, 19 Oct 2024 03:50:51 GMT  
		Size: 7.0 MB (7016679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92120d25a5bd34685129dc03eb81c53d37e34f8d347a42193df4f92bbcdcc0e4`  
		Last Modified: Sat, 19 Oct 2024 05:12:06 GMT  
		Size: 39.4 MB (39401291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a9165337d0ebf9676d18fa86b71698b5a66daf7200d6d69d6a1dd668bedef442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5617289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77825930997f20c071742d9d36a54d7a6e0c03a1323f48f103041531e03bf62b`

```dockerfile
```

-	Layers:
	-	`sha256:dc56c2effd84be465d89ab77f837d7abd693a4b0a819c52bbe97ac0e6e9d1984`  
		Last Modified: Sat, 19 Oct 2024 05:12:06 GMT  
		Size: 5.6 MB (5609965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8c2021cef4f4ba0d46679bd7621ac751c2924e23cef9ded9a605a5867443e0b`  
		Last Modified: Sat, 19 Oct 2024 05:12:05 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:latest`

```console
$ docker pull buildpack-deps@sha256:08d61da2eb4b661e95088f6999704803985f9bd7be23b3c5d7acce26cd2d521b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:latest` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d7d6286e853f4cad78b9bacc9962ed13b3fae93c940bc951a473bf59f7f1e406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.1 MB (348060715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fffceae85e2c8f384b15a112be85e0068e283d5c5a20b5b6569421c24c2d23f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd71677db44bb63b94de61b6f1f95d5540b4ba2d6a8a6bc4d19f422b25e0c2b`  
		Last Modified: Tue, 03 Dec 2024 02:28:49 GMT  
		Size: 23.9 MB (23865876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551df7f94f9c131f2fec0e8063142411365f0a1c88b935b9fac22be91af227e0`  
		Last Modified: Tue, 03 Dec 2024 03:17:14 GMT  
		Size: 64.4 MB (64391508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce82e98d553dd62ca6a12bebfe83992ae9f9ae2748275e74b66a68cc094f868b`  
		Last Modified: Tue, 03 Dec 2024 04:31:20 GMT  
		Size: 211.3 MB (211306121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:22a0e2166ec5a7010a99174c9c5a4b92eb963a4c9b850ffc869e3ae672a4dd19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15507109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e432f0cc69ae07b4e7a310d24f8c071f75c5c31a75f80f558a30a9de615e1d90`

```dockerfile
```

-	Layers:
	-	`sha256:28a6ec7885ff79f670b70218ace6d532c8d6d4ee96e883c5eea08d923c243220`  
		Last Modified: Tue, 03 Dec 2024 04:31:18 GMT  
		Size: 15.5 MB (15496569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4526bb391e6ae70edf822e4ae77d44dce58b597a0adf995d87ca2061831eafe0`  
		Last Modified: Tue, 03 Dec 2024 04:31:17 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:5493da36ae1be44ee45e6f2a21e8eb7a1651f02980e111eb4b77fcc9de0a28a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.2 MB (315162492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1431cc1ab0a9621e4af9c733d49b9b97de509516dcbcd2b4c7b5b24edab2124`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a8ab0b752e573ceb3480052f24bc5fe3f4f4665c13a338db39c1d51f749528e9`  
		Last Modified: Tue, 03 Dec 2024 01:27:04 GMT  
		Size: 46.0 MB (46024374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff6779451547ba3f0647f15a65068290fed53b6a4ac506257de98e02857bea6`  
		Last Modified: Tue, 03 Dec 2024 05:23:42 GMT  
		Size: 22.5 MB (22540382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536c3cdef529f6d2993cf137c109a079266cd3effbffc602a136a2a60ee743a0`  
		Last Modified: Tue, 03 Dec 2024 08:40:08 GMT  
		Size: 62.0 MB (61996814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f689132b2bca5271eb471905bd9f8eeca3a8c74df88b2f1c85f7c43568f20e7f`  
		Last Modified: Tue, 03 Dec 2024 10:05:05 GMT  
		Size: 184.6 MB (184600922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9c4417f2e99d2695ac62a5424fe36d0c44cca3243f219bea81261e45beaf3b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15305788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153481c7eaadccabe24fb8bb164c037031dfbfdd932085326ec034ee9a386d98`

```dockerfile
```

-	Layers:
	-	`sha256:5aa70f8227a7f0f719920d36ec18fa8bd67edfb3e40293ba3716fb81b5aef76b`  
		Last Modified: Tue, 03 Dec 2024 10:05:01 GMT  
		Size: 15.3 MB (15295180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b8c7629b4f7dd625175f4302ed859bd0ad93857f5dbca59a30b70d298562b4e`  
		Last Modified: Tue, 03 Dec 2024 10:05:00 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:437e11f7b48081f9d3169d3f0b57c19ccbf5d90f78824f50b59ee48d4e0d9fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300850185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1add49ced00435fc4e660bf2b8efd6d6f065f88334295c8dc979ad7f0ab8297f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4d43724a324f138c88a78ca6df0a39ab6868bf1f121eb974439c5a51284e1ac2`  
		Last Modified: Tue, 03 Dec 2024 01:27:59 GMT  
		Size: 44.2 MB (44200109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff0e53b92c3d0f5c370d71aeac1be1d23e475f1afba41d896ace0ff6eeefc90`  
		Last Modified: Tue, 03 Dec 2024 07:36:14 GMT  
		Size: 21.8 MB (21767161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9625bef464ab08848044651374e04f75d37ada02fe71387c3f9f83d0c9376c59`  
		Last Modified: Tue, 03 Dec 2024 17:15:53 GMT  
		Size: 59.6 MB (59641126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d83c079d9e82f91aeec2e9d84797bc47fa7f3b69f4094b837cbb4a9c25c5613`  
		Last Modified: Tue, 03 Dec 2024 20:03:34 GMT  
		Size: 175.2 MB (175241789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c37a07b310ce0346c0b105b93643ae7804934f50b5803137d2397fda42284ad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15311262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212be7441ad84dc59844b2e1479e05aaff0604670d910cd493e41a9ee0f3f9a6`

```dockerfile
```

-	Layers:
	-	`sha256:d6a56c836aa67f6706e6eacb06bc1edf226a862c6df77e58f7a17171c9494731`  
		Last Modified: Tue, 03 Dec 2024 20:03:30 GMT  
		Size: 15.3 MB (15300654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20d1d9165217046eef0f65fd0f02af670a48e312e840cc150c0713c8769cc7b5`  
		Last Modified: Tue, 03 Dec 2024 20:03:29 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:39b25cdea8a4133052cf8976d884cd9f4a28c36fc7ea1d200a82c3054510ff15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.8 MB (338766544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14cf9bca2791cef90a5b1313fb25c31438e4cf72dfec291fec9d3abfcc7b8674`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac722d9cf93b238dec2480278a2df5f8ccb672c97ec39f191191fd39f6721a8`  
		Last Modified: Tue, 03 Dec 2024 05:38:46 GMT  
		Size: 23.4 MB (23405813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261351ed796deb9fdad22dc734919eaf6726dd79a8dea99327d9e1376ecdcbce`  
		Last Modified: Tue, 03 Dec 2024 11:50:22 GMT  
		Size: 64.3 MB (64347852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d319298afc8bd728b8009e80320fe04e864fe92783eb06238a3b9f67dac7c3`  
		Last Modified: Tue, 03 Dec 2024 16:19:47 GMT  
		Size: 202.7 MB (202687199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d273ba454f05ac7b5489806499d16a8fc8ebf4171d5b07f144b245ce6d48a92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15535745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a83186039bd3ea2e021d2749e90f67f3e94a9e21027127ab2af7156513301e0`

```dockerfile
```

-	Layers:
	-	`sha256:578a4e71415013356a8cd37b5030e980c95edd8780c5a2f5a02a5d3585b92925`  
		Last Modified: Tue, 03 Dec 2024 16:19:42 GMT  
		Size: 15.5 MB (15525113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c493ff614776a1782e0bbac3137f383ef0eaad4fffed2bc981261fb4770db246`  
		Last Modified: Tue, 03 Dec 2024 16:19:42 GMT  
		Size: 10.6 KB (10632 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0ab7c71d79bd872a655352313f52121a6bcff2ffbac86045c95275339c23dd99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.6 MB (350616786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3ef764469eb7f8569265b9f9540132de83292a18992941d2995b96bcb6332e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:53769c348e57d646b1ec110dabf9d81a3f570afdb3b8216d1178515e4ea4ce1f`  
		Last Modified: Tue, 03 Dec 2024 01:27:09 GMT  
		Size: 49.5 MB (49476152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b0c73f75a815ce87bbf2841b694fdc4c29bcd072480b8752e8e91f0b59097b`  
		Last Modified: Tue, 03 Dec 2024 03:23:49 GMT  
		Size: 24.7 MB (24706896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2cf0351f309a0cf554972555b46b2ed97868d801e25eeed28a9f742a5e555c`  
		Last Modified: Tue, 03 Dec 2024 04:29:18 GMT  
		Size: 66.2 MB (66211191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adec659d61840fa9345456f332914b715e5d645a246d8ebd23b1c1c4b49b4996`  
		Last Modified: Tue, 03 Dec 2024 05:13:33 GMT  
		Size: 210.2 MB (210222547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:beeefbfff2ab941591ca7b91831c773ed391314b2de8511095bed0ee45cc98dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15485661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8bad9e7072ba65013bcf0c51e6857d3cbf652a07f0e5daa83e3d046e94995f`

```dockerfile
```

-	Layers:
	-	`sha256:87a64892961d327a139e2c8827b6f3f38d3383d5f173df4dfebfbfa09ef41385`  
		Last Modified: Tue, 03 Dec 2024 05:13:28 GMT  
		Size: 15.5 MB (15475148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e958a20d62bb83ee3421e3a3e2d16608731c94121983988380170f328b7e9f2c`  
		Last Modified: Tue, 03 Dec 2024 05:13:27 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:9a4df2f86567815e32dbc326f5e5710e33ae4f7e2c64c4ce81c28b6ee888b1ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325389432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3307c2bfac9eb9bd9ffeca8fbb60c761663449db1d61e6b4628d2dc291c3d8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8f7c3140f4f3af477253c748b229283137cca4214e1c3df21109b821f9227620`  
		Last Modified: Tue, 03 Dec 2024 01:27:53 GMT  
		Size: 48.8 MB (48771844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa54d74c5fddb1e648e0a4d95fcc8338f5800ff817646baaa9e6e65596d80c5a`  
		Last Modified: Tue, 03 Dec 2024 15:45:04 GMT  
		Size: 23.5 MB (23458105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a279e7254de3fa3935af4b6008753d14fcd8db605c58b83903cf8c5f880324cd`  
		Last Modified: Tue, 03 Dec 2024 23:22:12 GMT  
		Size: 63.3 MB (63283098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dffedca1364b4f303c66eee15c30c1fe70fb1db9416edf06602e694b41c50f8`  
		Last Modified: Wed, 04 Dec 2024 04:38:35 GMT  
		Size: 189.9 MB (189876385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0b9e0ac2a57702f5a76c6ff8a70e27672e95eabbe67a9141687c6917de5e0b46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aad0047efd61ce3266f344221ab7efa1e1390e8fa64a6831adff99b0275fcfb`

```dockerfile
```

-	Layers:
	-	`sha256:10d62b0e0d641ac025f308f802b13bf87690a2a5ecfbbc2f4f58a5d28559ba58`  
		Last Modified: Wed, 04 Dec 2024 04:38:18 GMT  
		Size: 10.4 KB (10382 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4ff5e7a9649060e6cec9389c3206397b83ccf21a3ef73f6da914d6a2b64f07fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.0 MB (362005295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f8e120cfb46d308aaefc2f3eb5e8f7580c23131f19cd4b52ef9a90bfce89cb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c84d784fe3c6c2bd95dea1c0d6eeba7c981bfb75bd53f81e83bcaadd87bba6f9`  
		Last Modified: Tue, 03 Dec 2024 01:28:03 GMT  
		Size: 52.3 MB (52328222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f0cfea13db30ebc69124696ada25182d1141398cd301a47a2cbf3c10d7fa9b`  
		Last Modified: Tue, 03 Dec 2024 04:36:57 GMT  
		Size: 25.5 MB (25523892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac73bc765d61ec6125ff5203c6c3d44543e6c3030684bfed0cb8f169640ae757`  
		Last Modified: Tue, 03 Dec 2024 09:41:44 GMT  
		Size: 69.8 MB (69812337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96099d400daf72e276203923fc855b1b1e5db81df04082e3505683bb398ec9ca`  
		Last Modified: Tue, 03 Dec 2024 16:12:55 GMT  
		Size: 214.3 MB (214340844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c38259992ff8adb65a540669780917a3ab0b4eb2a7bacfc0defc08aabe1954a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15483450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f228c3be5f23d0c8799c7a0da21c5bdc94a05195f09c48ab4f5756a9444da4d3`

```dockerfile
```

-	Layers:
	-	`sha256:4440c44dd5ab1d5632e5b9c675b3baff9156597169f4d38bade9241401960420`  
		Last Modified: Tue, 03 Dec 2024 16:12:35 GMT  
		Size: 15.5 MB (15472872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0489521282efca47f374796943fd138778aa10144bb693e59944fe88b32e855c`  
		Last Modified: Tue, 03 Dec 2024 16:12:31 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cea2ed2882f4bb7184acceea3fb0d08f2c273af35929de4d26ec1770b8329e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.8 MB (317814279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df084175632dd7bf0baf95424425d7b56f2dc329be6919e564076bfc0c0b66e7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:53a5c0dbd93a4a7f540e18bbe49ba3d7fadaa390ebbce009c756e34c5b1ae048`  
		Last Modified: Tue, 03 Dec 2024 01:27:55 GMT  
		Size: 47.1 MB (47149767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ded5bb0b377b736e6c5f45164fe8916ada3485441e963fe2fc0671949650049`  
		Last Modified: Tue, 03 Dec 2024 04:07:42 GMT  
		Size: 23.9 MB (23864625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b626037a925f80e453161d124c98cc5578e9d47f3f90a050168552e9727a34e`  
		Last Modified: Tue, 03 Dec 2024 07:53:40 GMT  
		Size: 63.5 MB (63473216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877241890f0b72dfe408c616ea9dde1f1c0afbbe3e7b91d9ceab73e7963ef0eb`  
		Last Modified: Tue, 03 Dec 2024 10:39:34 GMT  
		Size: 183.3 MB (183326671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ebbeeed93d90a07f2bf61c939dc6239ec6d8f6061e3eb49598381e313d2fb582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15319550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:017d6c05bd78e755bb45830a2c4afd3694c60f8b2019aa34942d6d1c91f3951b`

```dockerfile
```

-	Layers:
	-	`sha256:a14fcfe55eaddefca48b5c90a0ebb9e879a4899937c7f283124a5b4f9155e8fe`  
		Last Modified: Tue, 03 Dec 2024 10:39:31 GMT  
		Size: 15.3 MB (15309010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81a7f4e3bcc82457c7631f0aa274731bcc28c78bab41b2d89951556c508a2a32`  
		Last Modified: Tue, 03 Dec 2024 10:39:31 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:f6c88b5183ccb4873ff006ffa7e148856ae0bc9607a961198837bc3ee1c8123f
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
$ docker pull buildpack-deps@sha256:bb83ff53a86c956b665a684cdc6d251a9d5ba84bf82e97e566d398d5e27d2c45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.7 MB (278694752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7cb61cb2b87dc4a68b6ea91ebea0d11384037db0ebe0fd7c66f83b1da30f57`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5235aa939f41c34b69f4fe37736745fde8e1a4676950add7459e7b957c4cfd55`  
		Last Modified: Tue, 03 Dec 2024 02:28:51 GMT  
		Size: 13.6 MB (13617608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48cf16388a9a3471d6a91777a42a673b8db99767b831de048212ce4136744cd4`  
		Last Modified: Tue, 03 Dec 2024 03:17:02 GMT  
		Size: 45.4 MB (45394654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafede1dd30b73e66552948455e76ed828e5f7c7098be8fff3596c51c6277fc9`  
		Last Modified: Tue, 03 Dec 2024 04:32:10 GMT  
		Size: 189.9 MB (189930522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fd83f7ce1b0a238e27ecbc0207f69f63a64267b67fd7dc91ca0c49747cdd7863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11373395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad5d6dfff524e78a2901c016b52d0653fc960c88f14fd01abd1818d0b24f49f4`

```dockerfile
```

-	Layers:
	-	`sha256:f3007db501bfab1f0450753095c7788798dd7f6b71b8a20aca7128ff937003c4`  
		Last Modified: Tue, 03 Dec 2024 04:32:07 GMT  
		Size: 11.4 MB (11363211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9ea8ae9a98f8b881899f6107f12ba787f9d886379f1542a2b8eac45c8572fe0`  
		Last Modified: Tue, 03 Dec 2024 04:32:07 GMT  
		Size: 10.2 KB (10184 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:bd5ebd5467d1524eaf40250310b664291c17aa0d2bf8d1eef73d1da23227edd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.9 MB (238926365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3315e6b7232f3b7f0fb4c657dd3ca3fc43c5f47643b63605e65d2838e3682ed2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:786ab064bf2d82faf7ca3fbb6c2e6983bbdb3228800d6d64e5dec4a67f778a7a in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b25adda5718ef4d96696ce8f0e58cde58fbe9977456036f84293bba8f26c5567`  
		Last Modified: Tue, 19 Nov 2024 17:38:39 GMT  
		Size: 26.9 MB (26869639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f072a621863f98c6e93487af2148d3199cc2cf579bfe20feab8e50641003f0`  
		Last Modified: Tue, 03 Dec 2024 07:39:05 GMT  
		Size: 12.8 MB (12774963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335cf1f7da64ab01e02577f00ca7c83d14ba94593eeb2b94921fa0dd578a4e4c`  
		Last Modified: Tue, 03 Dec 2024 17:19:41 GMT  
		Size: 48.9 MB (48944185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24ddd4b0f02d6d7bf38be9b41c408f1242fd536d325d89fa0c43fb580051af0`  
		Last Modified: Tue, 03 Dec 2024 20:16:12 GMT  
		Size: 150.3 MB (150337578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d69b102a8f2f6d9742411b7b3d9cbf306e0c5a6545618dff2a16bca42464b032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10720389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f24e38cfa99bdd21a9cda91104e80836989f73eda79cfeb91ebca5291cc0977`

```dockerfile
```

-	Layers:
	-	`sha256:de156d5d70a7cbc8ffc728612e41c8daf31719edf4827741f797e6cba4acfc70`  
		Last Modified: Tue, 03 Dec 2024 20:16:08 GMT  
		Size: 10.7 MB (10710145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abd9017c402a1607859ce1331ee22a2877d983bc44296cf9bde3cc8bba6a5060`  
		Last Modified: Tue, 03 Dec 2024 20:16:07 GMT  
		Size: 10.2 KB (10244 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:48ec7d59dec4b33f187e27c867d6de4a9dae6c184ea08969623f0f84a75dfe40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.7 MB (269660566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9624081441bd36cf08652ff2ce33e156fb26dca65c8a428dc5fb617711f58c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331da7d4a8631a606292d353129b9398a4db3f2798d686a807920d0a81e2c741`  
		Last Modified: Tue, 03 Dec 2024 05:40:42 GMT  
		Size: 13.5 MB (13452932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af04d25eb37c1d037171f5c201d5753407b0902b0f09c9b548efca5b1d914b62`  
		Last Modified: Tue, 03 Dec 2024 11:53:13 GMT  
		Size: 45.4 MB (45358165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf8a464ed6ede506dbb704c616401409e9edba9adddd90f8285bf3e38569f37`  
		Last Modified: Tue, 03 Dec 2024 16:29:28 GMT  
		Size: 182.0 MB (181956798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7b1c5169af505db4fd177e93d7cc7d418eefa1aba2c5c543ed7585a7a7e5924b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10942946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b3d4def8c8d0db456ca7cf9dbb53398901530f28a25db7b20ea8a5855a6060`

```dockerfile
```

-	Layers:
	-	`sha256:c64ad584569af3cc34359825ecc15b46f6923a382b0a26aa88caa615a37fb2ba`  
		Last Modified: Tue, 03 Dec 2024 16:29:24 GMT  
		Size: 10.9 MB (10932683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55d65706b0c815a3c6f9b755f469cfd2d5792895758cf29b8087a6e473b836c5`  
		Last Modified: Tue, 03 Dec 2024 16:29:23 GMT  
		Size: 10.3 KB (10263 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0f081dc43aae4c0264f372db9ff26f642234d719c5cea169e1313110d0a71da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.2 MB (297192499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72973b5074015731ccd005dc3a9f728cadc21a785b5d63f7bcbad915e99b48f2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb006e560e9a807b6372fb925c588d9d83a6052a65248653a1f5708527a24d4`  
		Last Modified: Tue, 03 Dec 2024 04:39:54 GMT  
		Size: 16.0 MB (15980138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9deff409e8ce76af2a5a7095a7e708fdcadb9e212359c8655149b857100b432d`  
		Last Modified: Tue, 03 Dec 2024 09:46:22 GMT  
		Size: 50.6 MB (50557592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af77c7fb06c47d86e7daf6d244287862d5f022cbd73a8f24b0c9652bed607668`  
		Last Modified: Tue, 03 Dec 2024 16:27:22 GMT  
		Size: 196.3 MB (196265949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:eea638158cb24d7f4cebc2c98af5c3442a994d30e18797d991d9a56f6e93e905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10890073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f222e319fed14c024b6c5b08c679eec3c08b07fb9e16818e07ac8c244442113c`

```dockerfile
```

-	Layers:
	-	`sha256:adf0e9d2e4c57e9958e4fb4db04302367e0f365aa0f6f875539e6758cfbaba18`  
		Last Modified: Tue, 03 Dec 2024 16:27:17 GMT  
		Size: 10.9 MB (10879857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccd908e1ab77b3bd255cafb4cbf55047b3e614ba53fcb8d474b607099e6d2a54`  
		Last Modified: Tue, 03 Dec 2024 16:27:16 GMT  
		Size: 10.2 KB (10216 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:5e1605aa43abc928356ba673ef6be9bd9319e90a23c606d51d650fdf5df34018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.0 MB (329034579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835d261ccf3765d3b5873291e25e82e57429821f2acedbbccf22f8d6c8d6e811`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:23c2e341d6cf3572f2762ef1304c406cf6d4f5ee8ee8719ef289a3b75a8323aa in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0dcc8c973ba119a0fb5275114fd0456179bba1132bdc69f2afa4e1c4a235c540`  
		Last Modified: Tue, 19 Nov 2024 17:38:52 GMT  
		Size: 31.0 MB (30980838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789bf3edf440eb67602bc2c6173f31d3292b752b03bbf690c473a5038b858343`  
		Last Modified: Tue, 03 Dec 2024 06:44:43 GMT  
		Size: 14.3 MB (14321082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f505f2c8e1079fb73360d2ba6b4c3130e06fd9586abaa35474f69fd6f08ac0c3`  
		Last Modified: Tue, 03 Dec 2024 09:51:22 GMT  
		Size: 53.9 MB (53856700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f5c18773f973d35cc8bb879ed0254ec6d05cca16b3f9339f4eb2b99b6426a9`  
		Last Modified: Tue, 03 Dec 2024 11:10:32 GMT  
		Size: 229.9 MB (229875959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:42ac014c17c16ec26d33081987bc40ec5449f24b0cebd4ee754cfbab8def7dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10878996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e072ce08a23db75befa02226181a0b4b1e33930050fd5c9b2e1c5b4654b2dc21`

```dockerfile
```

-	Layers:
	-	`sha256:9d8ab87d7a49129567a98c7b079a08bf77f826fa903e25c72412c2f803d9b4ca`  
		Last Modified: Tue, 03 Dec 2024 11:10:02 GMT  
		Size: 10.9 MB (10868780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b587665ba1f2bb0c50e0efbceb471e61c7abcb950f38d26c6ca2fe44e136d6f3`  
		Last Modified: Tue, 03 Dec 2024 11:10:01 GMT  
		Size: 10.2 KB (10216 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4a55093eb0048c2456e122785f6ca1890b9359d3efce4ff6f3e109bba8e87e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 MB (260854060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ea0f30aa2bb668752c8f50eb109cdf7d802314c2a55a318a7c42919b9026592`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:1c391e128b3c5e552a1401f9520290446bf94ba089c2d74a5d661001d3d8b60c in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:755503a8fb36d6a0d08275c3792ab81b69fdff95054dff0aa932d6dc30107609`  
		Last Modified: Tue, 19 Nov 2024 17:38:58 GMT  
		Size: 30.0 MB (30020826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35190d0c1306f85de6133cb1ceca330cd03ee2f6baead3be847b0c8e4273f57`  
		Last Modified: Tue, 03 Dec 2024 04:10:05 GMT  
		Size: 15.0 MB (14960770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05107eaec609414c9540f16903f6f4fed09e9055d47bca5a3188db8c2f781888`  
		Last Modified: Tue, 03 Dec 2024 07:57:25 GMT  
		Size: 46.9 MB (46912688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec9245ce6aafa9002bb642e97c63ac3ef077f28fd50c83064b68bc310d8f457`  
		Last Modified: Tue, 03 Dec 2024 10:54:15 GMT  
		Size: 169.0 MB (168959776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3d39c6be03b02a7e807a6d25ccfc5b0d68a2220dfc7704f2c5bfae8c2ab2c53a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10735769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea05009d300f9ae1c0b408d9cbe080d09822698e52361e856112d74572ec003`

```dockerfile
```

-	Layers:
	-	`sha256:8cc51ba0c454962e736809e6968abb638f186854bdc7e4dc494c5f531eb8e880`  
		Last Modified: Tue, 03 Dec 2024 10:54:13 GMT  
		Size: 10.7 MB (10725585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e5587fd8db9cff37c4d4ae0d1693c3695f27c5deabe39009de2b8bc3d8bde7d`  
		Last Modified: Tue, 03 Dec 2024 10:54:12 GMT  
		Size: 10.2 KB (10184 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:9911aa92f07dc4100c07880f79859cd1c67533e6188c47141c1e2cabcce9ce1c
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

### `buildpack-deps:noble-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0fa4cc5ad043306df0d2c2c4e6a9d1219084de8f003aec1e02f776b4e23e6ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43369576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42fd4116a699db2d4e7a8dcc690dd3362f29a31d0305d44e60b1da7400121a8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5235aa939f41c34b69f4fe37736745fde8e1a4676950add7459e7b957c4cfd55`  
		Last Modified: Tue, 03 Dec 2024 02:28:51 GMT  
		Size: 13.6 MB (13617608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a2f44a037cce80f83c04568a366e5fb90b861a4d43f58289c5687cb79912923e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aff44ca61232543e0e4008545e3442593e8dd41caa992235517167a8846a6fe`

```dockerfile
```

-	Layers:
	-	`sha256:9afde91d62e4816e8bed19458ec653775b86b7302dc68c386a6913f2723252a8`  
		Last Modified: Tue, 03 Dec 2024 02:28:51 GMT  
		Size: 2.5 MB (2460157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edaf4a88adf6a30c34e18b08bc3714cfed92a82b366bbf936d5b93a235d9085c`  
		Last Modified: Tue, 03 Dec 2024 02:28:51 GMT  
		Size: 7.0 KB (6958 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2da8ecab6d61772b7679a305ec87fe82ab997fe5f88e6889153581f9b8e0129e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39644602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5c83fea6dbb69e662877b22fdaa2d1195b4698e1ecef022de83e0c9bc2b735`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:786ab064bf2d82faf7ca3fbb6c2e6983bbdb3228800d6d64e5dec4a67f778a7a in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b25adda5718ef4d96696ce8f0e58cde58fbe9977456036f84293bba8f26c5567`  
		Last Modified: Tue, 19 Nov 2024 17:38:39 GMT  
		Size: 26.9 MB (26869639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f072a621863f98c6e93487af2148d3199cc2cf579bfe20feab8e50641003f0`  
		Last Modified: Tue, 03 Dec 2024 07:39:05 GMT  
		Size: 12.8 MB (12774963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:07168df7c99826ff59dbaa035f61d4f7a5c6f0e49f39caa0a21044f77d3970a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2469479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825fefe71ffe4a6f13d42aac4254e18436de1618fd7dd424f7c38c48283034be`

```dockerfile
```

-	Layers:
	-	`sha256:c0918bea141dc274a311f371547de2fc014d951a996ae68df6dc4cb49fc63c91`  
		Last Modified: Tue, 03 Dec 2024 07:39:04 GMT  
		Size: 2.5 MB (2462460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e25cca77142a6540d318afa3e83cca144ba327a2a445583fd27160b200cf96a`  
		Last Modified: Tue, 03 Dec 2024 07:39:04 GMT  
		Size: 7.0 KB (7019 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3f12b281d4c7e441ca6b2ed447d7b8ddcb738e8146fd51eaa15c5946c476d9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42345603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d55ad38d6ad3b1975d81df0d33cf24df7c080c89a5a6e833d8fe7c0e826303`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331da7d4a8631a606292d353129b9398a4db3f2798d686a807920d0a81e2c741`  
		Last Modified: Tue, 03 Dec 2024 05:40:42 GMT  
		Size: 13.5 MB (13452932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c33ab3937c7073dda570cd34197c5e3f67b52a83eb735c5a0345c96d2dd09ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56ae62139fee889a90664cb93c0b7504ef9db10d54e683dcc9d27f492f86ebb`

```dockerfile
```

-	Layers:
	-	`sha256:6432e9ae2dbac0fd9b0b261fa1aaa14c198e831ab1d9e88950df498125b93e63`  
		Last Modified: Tue, 03 Dec 2024 05:40:42 GMT  
		Size: 2.5 MB (2461215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a01727f7c98822d422cb960375c8c525f7aa192239eb880b79b9acca421a728`  
		Last Modified: Tue, 03 Dec 2024 05:40:41 GMT  
		Size: 7.0 KB (7039 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:53f47b381774bf1fb84602bc0b56726a929f843c79b80b5b25623908f15bc318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50368958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd68d72e23a609767f38fa4dd1e15adf3cad28cedce39399ac29e4014874941d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb006e560e9a807b6372fb925c588d9d83a6052a65248653a1f5708527a24d4`  
		Last Modified: Tue, 03 Dec 2024 04:39:54 GMT  
		Size: 16.0 MB (15980138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e3c0d30c9776b2e964822e3f9884b555a6ff0c2875d8365faf49d773c1a3cda0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2471632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078a7fb980e93ad0004a00f7f1c98d54288c1735f320327ccc764a8b66f56e81`

```dockerfile
```

-	Layers:
	-	`sha256:4285ede008935a505df8c503de2dd6047bd3480e9e2a298b783ba07b1e7abf7f`  
		Last Modified: Tue, 03 Dec 2024 04:39:46 GMT  
		Size: 2.5 MB (2464643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:464acb1349a4f65e154e4589d2a9df0ceb12ae177be44a38fbe8c417d0757c99`  
		Last Modified: Tue, 03 Dec 2024 04:39:44 GMT  
		Size: 7.0 KB (6989 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:427093dd420b73785f4c697433aa021ca695d93925872ce11cd14177982d2eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45301920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae64a028798fd8ac0ccf9a37363e97545ec4956264ef73eb76ae7577755dcf1e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:23c2e341d6cf3572f2762ef1304c406cf6d4f5ee8ee8719ef289a3b75a8323aa in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0dcc8c973ba119a0fb5275114fd0456179bba1132bdc69f2afa4e1c4a235c540`  
		Last Modified: Tue, 19 Nov 2024 17:38:52 GMT  
		Size: 31.0 MB (30980838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789bf3edf440eb67602bc2c6173f31d3292b752b03bbf690c473a5038b858343`  
		Last Modified: Tue, 03 Dec 2024 06:44:43 GMT  
		Size: 14.3 MB (14321082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5bbefa7271de6bbbb050f868fd8c93c0b06bd8ac418f05ca3f557ad4ffd224d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf1b461033a2a3da9c2e37123ce819ca1a426d0f9fa1355d6598f08a1fb7183d`

```dockerfile
```

-	Layers:
	-	`sha256:e5d6092dc376a01da04528366bd6a4155bdbd5514aefb3e96208b9c850a66408`  
		Last Modified: Tue, 03 Dec 2024 06:44:41 GMT  
		Size: 2.5 MB (2454241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:899d9df5d9acb6c3234e977feabe3521391b2a97fe481da2ee4a03d84d8c7b21`  
		Last Modified: Tue, 03 Dec 2024 06:44:41 GMT  
		Size: 7.0 KB (6991 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:55352dd01a4d52c21cb5808514851662c32e697c5c36bc01c77f7c8b8fc5e27a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44981596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db79a0430094f1439e67e85049cbcca6769dedd36964c969dabba0a35eee024`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:1c391e128b3c5e552a1401f9520290446bf94ba089c2d74a5d661001d3d8b60c in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:755503a8fb36d6a0d08275c3792ab81b69fdff95054dff0aa932d6dc30107609`  
		Last Modified: Tue, 19 Nov 2024 17:38:58 GMT  
		Size: 30.0 MB (30020826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35190d0c1306f85de6133cb1ceca330cd03ee2f6baead3be847b0c8e4273f57`  
		Last Modified: Tue, 03 Dec 2024 04:10:05 GMT  
		Size: 15.0 MB (14960770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e5ad476e5c52f4c913df3940b7db405f957a1c7cf075189daca46398c5c33a69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2469946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d5622a0d16455c00e33057665c5693a31579b1b6c611cbaf3ecb2e447535492`

```dockerfile
```

-	Layers:
	-	`sha256:d7201d5e83923888de806997daab87596447e51f8b6cf2d6f885c539143f49ac`  
		Last Modified: Tue, 03 Dec 2024 04:10:05 GMT  
		Size: 2.5 MB (2462987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f33aaa2db5113f324f58022583f74349375ad676c84dff81388db1011b74a55`  
		Last Modified: Tue, 03 Dec 2024 04:10:05 GMT  
		Size: 7.0 KB (6959 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:noble-scm`

```console
$ docker pull buildpack-deps@sha256:722970809edab74b0a85408f69d6ae9af04fbc3ad50f8ee4596345f89baa01a7
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

### `buildpack-deps:noble-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:6d50b3e92542a04322fbc2914286d49e5915ddaffcf191c07e06661fad7f646a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88764230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131aa2852b90e0ada1162bf44687db88ffbac12639b7a8d6f057c2bfa7a0354e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5235aa939f41c34b69f4fe37736745fde8e1a4676950add7459e7b957c4cfd55`  
		Last Modified: Tue, 03 Dec 2024 02:28:51 GMT  
		Size: 13.6 MB (13617608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48cf16388a9a3471d6a91777a42a673b8db99767b831de048212ce4136744cd4`  
		Last Modified: Tue, 03 Dec 2024 03:17:02 GMT  
		Size: 45.4 MB (45394654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e3f04deeea996b84aa1dd1dfee85837b0a2f1bfe56fd34469d8686c2b2df4193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5083420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8858ee1939cf86150c60e81cac0c8fb87a608744c7ec96f3a8af6fa531324a19`

```dockerfile
```

-	Layers:
	-	`sha256:addc9e17fc74d7040b9ab7245bbaadcde580f924bbad026c4091e477cab1bf6e`  
		Last Modified: Tue, 03 Dec 2024 03:17:02 GMT  
		Size: 5.1 MB (5076115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bd67f97ec250bb62ffa5140cbe45a6491aab2a87e36613851e4c406872536f6`  
		Last Modified: Tue, 03 Dec 2024 03:17:02 GMT  
		Size: 7.3 KB (7305 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c2fe6de00fc138830d287fb0dc0f6b911dca32d344e4701eed3aa2b0c86a015f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88588787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60bcc54a6f059b5e96eb76abd6d7c54f157230e6b9450227a6df12a929e8bbf5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:786ab064bf2d82faf7ca3fbb6c2e6983bbdb3228800d6d64e5dec4a67f778a7a in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b25adda5718ef4d96696ce8f0e58cde58fbe9977456036f84293bba8f26c5567`  
		Last Modified: Tue, 19 Nov 2024 17:38:39 GMT  
		Size: 26.9 MB (26869639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f072a621863f98c6e93487af2148d3199cc2cf579bfe20feab8e50641003f0`  
		Last Modified: Tue, 03 Dec 2024 07:39:05 GMT  
		Size: 12.8 MB (12774963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335cf1f7da64ab01e02577f00ca7c83d14ba94593eeb2b94921fa0dd578a4e4c`  
		Last Modified: Tue, 03 Dec 2024 17:19:41 GMT  
		Size: 48.9 MB (48944185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:36916e586b63927eb00c8e6fc63fbdc374caea9a8df5db0df3a2bab37d3fec16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5084774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:365716965de5497a66aa242643334c3251b18756a3f44fc87b04e53b504d7903`

```dockerfile
```

-	Layers:
	-	`sha256:dc29ff92dbf3d2987aeef7bb9b8c549b1acc9af15014d4fe428d6a049cd9aa52`  
		Last Modified: Tue, 03 Dec 2024 17:19:39 GMT  
		Size: 5.1 MB (5077409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45fd512c1fead54e3108bb7fe7ec75f4060f3a0fd9edbf39d3c7428b311bd686`  
		Last Modified: Tue, 03 Dec 2024 17:19:39 GMT  
		Size: 7.4 KB (7365 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:69e40459579cbc0b138d9a20aaf0d3486dc42eb8b3a836e30cf427ab277de42b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87703768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c718600a8934d0b44f5569edde9431dc42eb30d26710bcc02a6d96f08bac5ffe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331da7d4a8631a606292d353129b9398a4db3f2798d686a807920d0a81e2c741`  
		Last Modified: Tue, 03 Dec 2024 05:40:42 GMT  
		Size: 13.5 MB (13452932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af04d25eb37c1d037171f5c201d5753407b0902b0f09c9b548efca5b1d914b62`  
		Last Modified: Tue, 03 Dec 2024 11:53:13 GMT  
		Size: 45.4 MB (45358165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:eb791a3b3cca1c3b2935910956af05c9087a209ff88a70ac70ef9205d8c79156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5090699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bef7269cc872128c8e5932c12378ebd1a268b567dc24551c926c91fa85e57050`

```dockerfile
```

-	Layers:
	-	`sha256:1ada12157811656b092a572f885b9ac7f9ea75283b5e90e82f9b3c671db09087`  
		Last Modified: Tue, 03 Dec 2024 11:53:11 GMT  
		Size: 5.1 MB (5083314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a31276f86b42d0658076bc44da5d06e42007914f26474b55afed3926035e7dad`  
		Last Modified: Tue, 03 Dec 2024 11:53:11 GMT  
		Size: 7.4 KB (7385 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:384d387998aa64a6f5d109bff122bdea8b9ab1963ae663995810afaf4a7d2428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100926550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6946101467ca3a91ca35f8d779b675ebf382a27e84ec752d94adbf307d0d7407`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb006e560e9a807b6372fb925c588d9d83a6052a65248653a1f5708527a24d4`  
		Last Modified: Tue, 03 Dec 2024 04:39:54 GMT  
		Size: 16.0 MB (15980138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9deff409e8ce76af2a5a7095a7e708fdcadb9e212359c8655149b857100b432d`  
		Last Modified: Tue, 03 Dec 2024 09:46:22 GMT  
		Size: 50.6 MB (50557592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c0e1990e1e896cfb17ed7ecabf67bc00438fc31b10d3dfff8831d270ae4fc861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5091142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa976460f062d23b11e4b7e0374784807e804a1c84c7238400828ea4535f2be5`

```dockerfile
```

-	Layers:
	-	`sha256:98cb5d30b844718d1d8bbdaf254185490e39d7b24a525348d26bbaa41ef83c76`  
		Last Modified: Tue, 03 Dec 2024 09:46:21 GMT  
		Size: 5.1 MB (5083805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37f843b90490e92473c16e8e26ee5619d996af35343267bf4b7e5e268185f27b`  
		Last Modified: Tue, 03 Dec 2024 09:46:20 GMT  
		Size: 7.3 KB (7337 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:bfb5191debc6043e213d5fba8deaf56abc330de1eae2e2d4fa1eb38d09f1863a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99158620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1c3db312baebc205d4ae5320db8ea455b1d2c806396175a7f8f3d5d53560d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:23c2e341d6cf3572f2762ef1304c406cf6d4f5ee8ee8719ef289a3b75a8323aa in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0dcc8c973ba119a0fb5275114fd0456179bba1132bdc69f2afa4e1c4a235c540`  
		Last Modified: Tue, 19 Nov 2024 17:38:52 GMT  
		Size: 31.0 MB (30980838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789bf3edf440eb67602bc2c6173f31d3292b752b03bbf690c473a5038b858343`  
		Last Modified: Tue, 03 Dec 2024 06:44:43 GMT  
		Size: 14.3 MB (14321082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f505f2c8e1079fb73360d2ba6b4c3130e06fd9586abaa35474f69fd6f08ac0c3`  
		Last Modified: Tue, 03 Dec 2024 09:51:22 GMT  
		Size: 53.9 MB (53856700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2ad46ad8d7e5e2137bad7101c0d437b7fee331f0b8d0e6350b5887027183d1f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5073996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d3bd34af4146e39294b5bbb3fa5cef688457671071e5506732c9f6c13431c6`

```dockerfile
```

-	Layers:
	-	`sha256:0a4cc0ae30668e7591cd209c89d192583fba68aabb43372e03f01edab1d00e88`  
		Last Modified: Tue, 03 Dec 2024 09:51:14 GMT  
		Size: 5.1 MB (5066659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b02388bcac06974d94d50c9bf05df475bfa01487bba4a6f5101eb76f87477102`  
		Last Modified: Tue, 03 Dec 2024 09:51:13 GMT  
		Size: 7.3 KB (7337 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f6aa36b071cd1ed3f37f0b7bcc5a2325c8ea64c33d9746502b6992862e3e3cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91894284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac5d4c058ad27c00d235e7baf11e7972e559d439a340e03f8b86d1a4b2fd0639`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:1c391e128b3c5e552a1401f9520290446bf94ba089c2d74a5d661001d3d8b60c in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:755503a8fb36d6a0d08275c3792ab81b69fdff95054dff0aa932d6dc30107609`  
		Last Modified: Tue, 19 Nov 2024 17:38:58 GMT  
		Size: 30.0 MB (30020826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35190d0c1306f85de6133cb1ceca330cd03ee2f6baead3be847b0c8e4273f57`  
		Last Modified: Tue, 03 Dec 2024 04:10:05 GMT  
		Size: 15.0 MB (14960770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05107eaec609414c9540f16903f6f4fed09e9055d47bca5a3188db8c2f781888`  
		Last Modified: Tue, 03 Dec 2024 07:57:25 GMT  
		Size: 46.9 MB (46912688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6ed16ad608670de1d059165b62dc4296f911a80f55ef213cb9ac578a594dcd03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5085757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3f3c4fa5ca2bd0225ba612c07217a53faef57db897899cceeaafa4923145fb`

```dockerfile
```

-	Layers:
	-	`sha256:afe48d2c0a0654f448b9f66dbab36a88607d875e7c911c05e8c35914c9cffc68`  
		Last Modified: Tue, 03 Dec 2024 07:57:25 GMT  
		Size: 5.1 MB (5078452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95f4e0a101ac487e58274d0e6e005419118d9466a66d95d30a72475ea5022f9a`  
		Last Modified: Tue, 03 Dec 2024 07:57:24 GMT  
		Size: 7.3 KB (7305 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:oldstable`

```console
$ docker pull buildpack-deps@sha256:6617cc54bbc414524636f43515d5758f5604cc7593f4f5bfa4fde63979c9f5e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:oldstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e0d6c0821a6dde10bbbdece51ac39dda933b43eecff08f7e63ac59d3bcd4a430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.1 MB (321124868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b2a985a94697b011595fb26ac7b67b6ce31cdf7865b728074d3e9bfa281a23`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cd606f6f489eb66f1307280aec321b3af3aa998dca447ae1cc91c6b884240064`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 53.7 MB (53739147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925257a7168ed219a5d7c2a69af3245ca4cd9e376424f7f006535d9714437bd4`  
		Last Modified: Tue, 03 Dec 2024 02:15:41 GMT  
		Size: 15.6 MB (15558387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb34ce34679cf6bc8738a0166300fb0af605abff20bb9c1c8008dbc48722061`  
		Last Modified: Tue, 03 Dec 2024 03:17:12 GMT  
		Size: 54.8 MB (54753972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3364194d1839c998f7fa1f479212c49598df894b8a851ba42e54ebf7f4344a6`  
		Last Modified: Tue, 03 Dec 2024 04:31:23 GMT  
		Size: 197.1 MB (197073362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8f9bc52a4b9058ebee98d176fc69cd8bf21a27c6245f17b4d3087013525758e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15106111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21575104da17a45216c5ce6c3a73dc26a8ada6165dde7fd794ac310447e20dc`

```dockerfile
```

-	Layers:
	-	`sha256:b31d3b1cf134daaea9fb2cfda7f939fa9f5839cb80ce98eebefc56b34fc3ee03`  
		Last Modified: Tue, 03 Dec 2024 04:31:20 GMT  
		Size: 15.1 MB (15095881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df9e1efc148b23800b4ba72ccc8257c464c12b25ce6a320c4e0da8fc364e373b`  
		Last Modified: Tue, 03 Dec 2024 04:31:19 GMT  
		Size: 10.2 KB (10230 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:101d2910fe70365e13b014a949b79cb186ef725f82a81d6b7a958b204115d057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.9 MB (281864569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128f14c6ce29f3fef0ff687097e850601ab4f4083445e1bc6c3b96e3cdd70b69`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:69dbedc8019388fd330866fcfa04c35d28f86d1ef986691ee290054433639992`  
		Last Modified: Tue, 03 Dec 2024 01:28:37 GMT  
		Size: 49.0 MB (49025021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370e6aa30e16daf07d99e3fb5cd8610cda77f49507a7b2ba76a646359cf7db6b`  
		Last Modified: Tue, 03 Dec 2024 07:36:42 GMT  
		Size: 14.7 MB (14673759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54bf5af43178bf200a2aed84d9a42570d6bde94092c2ac746652561137c9a86`  
		Last Modified: Tue, 03 Dec 2024 17:16:41 GMT  
		Size: 50.6 MB (50640414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc87552ca09a0a5990453aa951869124cba4735d7a52f3622106c01546e373a`  
		Last Modified: Tue, 03 Dec 2024 20:05:40 GMT  
		Size: 167.5 MB (167525375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:035b3b07213c9cd6b7466b4c027ada5be1692df26badec6b966d6f692fd19426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14906654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb5361840c7746526ead3ae89167d36ad1143c1b7df099c2fbfcd912dd7113e`

```dockerfile
```

-	Layers:
	-	`sha256:ded25ba07dc8d62e794782cee821ef5d52408076e35018add12f5be63c561c90`  
		Last Modified: Tue, 03 Dec 2024 20:05:37 GMT  
		Size: 14.9 MB (14896362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f743bc17c8386d4b723625d2399313181fdc49772f10c5eb6ec78655b2417a4a`  
		Last Modified: Tue, 03 Dec 2024 20:05:36 GMT  
		Size: 10.3 KB (10292 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:780d0f15e7619876d37b53039e6f51b58e8d0d265fba615224516eb583144186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.6 MB (312622132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1743f570b8f94d50fa3e1a84df0091ce88b6984faf43f5b44acf5282c4fdeac1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e357e1f94476a03fde298261e8c007d487d3cfade45a9eef064eba724a5c5e2e`  
		Last Modified: Tue, 03 Dec 2024 01:30:26 GMT  
		Size: 52.2 MB (52245994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b2279cee7374c65ae079e8ccdceeeb8b20c07ffc727e5b7cd595285b44a3a0`  
		Last Modified: Tue, 03 Dec 2024 05:39:10 GMT  
		Size: 15.5 MB (15544048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2749caeb5baae1b5e6316a6f02e57835aa548497fba6792be844c743a57c72a2`  
		Last Modified: Tue, 03 Dec 2024 11:51:00 GMT  
		Size: 54.9 MB (54852316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e711ab753fd7e271d97eb54f50e7e1a99221d70c2b97b5351966959fcf945e2`  
		Last Modified: Tue, 03 Dec 2024 16:21:21 GMT  
		Size: 190.0 MB (189979774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6df896ad394cb1b54cc7a2c567bdf97061976656abda845a14c944d59fe8c3c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15108429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c57d40db60495718c6e83fc7933db3de6a1be5fd584376fe24955a31f773f6`

```dockerfile
```

-	Layers:
	-	`sha256:843ccf6a63c7a10aa55c6b9f6e228e5306cf5645e4d74300fc291eb62ce500ab`  
		Last Modified: Tue, 03 Dec 2024 16:21:17 GMT  
		Size: 15.1 MB (15098117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16da700212edda2cb9fe9d637750a50e7fd4839d9ca011891f1319a1d1e2b61e`  
		Last Modified: Tue, 03 Dec 2024 16:21:17 GMT  
		Size: 10.3 KB (10312 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:33b3ef54a930506240ef7bf977b1df29288dc03a3f976af6ce263711adbf3e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.7 MB (326745403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e00120fb81bef803d7b8e0f1bb7fad0c3609b8e87e321c3b3a5e13feef1f0b3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:862f429b4105c1e5714d48631896837c3ca6f797479296293b7c33c6699eae95`  
		Last Modified: Tue, 03 Dec 2024 01:27:25 GMT  
		Size: 54.7 MB (54676275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ac5b88f14d979c6f071eb85aa8a772f827338af23171657add5b5e4fc91e2e`  
		Last Modified: Tue, 03 Dec 2024 02:14:36 GMT  
		Size: 16.1 MB (16062064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc99b34aeb38c1b23bfa1cbb2b4b9d6e5a643b78e7b238368942282890609c8`  
		Last Modified: Tue, 03 Dec 2024 03:17:12 GMT  
		Size: 56.0 MB (56027112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be1f6c2fc5941e6a645f4c32428da25f169e1c1d2334e0ecff55e66ef42af0f`  
		Last Modified: Tue, 03 Dec 2024 04:31:23 GMT  
		Size: 200.0 MB (199979952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0ee5f3c14c8de3a45dc235d315dda69908563e08874df4c64ccc6be4b514835f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15094432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e896e7fc71dbe5419b6bb986ba800d3cf89ae25defdbe13f79dbef31d3b4b721`

```dockerfile
```

-	Layers:
	-	`sha256:19229e7774fcedc6f939363a74467c99e4b95654811270bd461373df7d969c7d`  
		Last Modified: Tue, 03 Dec 2024 04:31:19 GMT  
		Size: 15.1 MB (15084222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6f72559a0a226f99fa93e36c5b7d8c59dac91fb8311c939981e5bb56b593ff5`  
		Last Modified: Tue, 03 Dec 2024 04:31:19 GMT  
		Size: 10.2 KB (10210 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:5e60bf8ec14591bd01ed6138482cac4011620d5c34ad8ae6165acf0d8e2f9e91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:oldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b960e9a35b94d98f8e28b9e7c6902cb6c0b00730da4c43b30bad6b65e1197205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69297534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8497e82cb3900277c279f7b4301f59ecc6cefa8ddfd2ee6cceece3a5d69cb179`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cd606f6f489eb66f1307280aec321b3af3aa998dca447ae1cc91c6b884240064`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 53.7 MB (53739147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925257a7168ed219a5d7c2a69af3245ca4cd9e376424f7f006535d9714437bd4`  
		Last Modified: Tue, 03 Dec 2024 02:15:41 GMT  
		Size: 15.6 MB (15558387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:17c6283204c87400f89a5054443c5bd83c77d1717114cdadc95a10f8743d9c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4497104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b5e44850ee339d6ee93ec71f2fdcf0bf2391e31821461866209ad64c7411c82`

```dockerfile
```

-	Layers:
	-	`sha256:0d955dfaeae326d60e2abe1818cb737d6839251fcf25ad39f452038fba101b22`  
		Last Modified: Tue, 03 Dec 2024 02:15:41 GMT  
		Size: 4.5 MB (4490305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aec84ba0adf96199bf08ed6c2d5fdf57c284d93fe90956bc7b22619c8b75f645`  
		Last Modified: Tue, 03 Dec 2024 02:15:41 GMT  
		Size: 6.8 KB (6799 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4112b0ea48c39076359cd3eba06afcb4a74fa3d7cc57a55d879a9aa5b8249ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63698780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f10e9c5003d1d069fa395b9c8bb04b9cf61629c642c305ef4eb6cc40ba150d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:69dbedc8019388fd330866fcfa04c35d28f86d1ef986691ee290054433639992`  
		Last Modified: Tue, 03 Dec 2024 01:28:37 GMT  
		Size: 49.0 MB (49025021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370e6aa30e16daf07d99e3fb5cd8610cda77f49507a7b2ba76a646359cf7db6b`  
		Last Modified: Tue, 03 Dec 2024 07:36:42 GMT  
		Size: 14.7 MB (14673759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fa0394388fbb2a06608ef60f548e97fb3dd04c124707abb27578eb19d4e6f14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4498800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979dce311168a7be5bf4db153de64d7238907994412a09c48bb1b9e90237c04a`

```dockerfile
```

-	Layers:
	-	`sha256:06d605c34375c728220a4ced5a6ef0b6de1d2c8d13c3694bd27ff80985cfc089`  
		Last Modified: Tue, 03 Dec 2024 07:36:42 GMT  
		Size: 4.5 MB (4491939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bd2b302e4bff90978f3a1a096b66e375120e062ebbfa0bdfbba17516df34eb4`  
		Last Modified: Tue, 03 Dec 2024 07:36:42 GMT  
		Size: 6.9 KB (6861 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:23d2e1f65f73a35eb78b1b28fd68d7c1afb54f666591c04bcd3c16d30c96bc32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67790042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b248a8c7acfb43452ba7e26d3295d2ccc04591a6e674dd2d21bdc45de3f447d7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e357e1f94476a03fde298261e8c007d487d3cfade45a9eef064eba724a5c5e2e`  
		Last Modified: Tue, 03 Dec 2024 01:30:26 GMT  
		Size: 52.2 MB (52245994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b2279cee7374c65ae079e8ccdceeeb8b20c07ffc727e5b7cd595285b44a3a0`  
		Last Modified: Tue, 03 Dec 2024 05:39:10 GMT  
		Size: 15.5 MB (15544048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:81ac6e124e736bf967e063a3be5ee9b9bc7a1db57f6f079af2e4f756295f352c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4496798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c81d5ecfe36c80b4b6452433e578e91ccf9f1f0fb214f9ce715756e93f6588b0`

```dockerfile
```

-	Layers:
	-	`sha256:95096dac33f7eff76e3eba5f7831fc981095785df44edb3b25fe21023899b42a`  
		Last Modified: Tue, 03 Dec 2024 05:39:10 GMT  
		Size: 4.5 MB (4489917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:831bc2da230f1470d9903f490c7d5b04257b7e79ab6f7c41792d2f326379e813`  
		Last Modified: Tue, 03 Dec 2024 05:39:09 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:79f35d801d1e471f31b46e8499d002d0bb08ba26829b87a89b481e981b8a1a4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70738339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081736c16bfcf7e7b6410b208723d39963512d09f222f018031e6b377fdc34fc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:862f429b4105c1e5714d48631896837c3ca6f797479296293b7c33c6699eae95`  
		Last Modified: Tue, 03 Dec 2024 01:27:25 GMT  
		Size: 54.7 MB (54676275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ac5b88f14d979c6f071eb85aa8a772f827338af23171657add5b5e4fc91e2e`  
		Last Modified: Tue, 03 Dec 2024 02:14:36 GMT  
		Size: 16.1 MB (16062064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9b682a0742c1a6381c26d03803ccca7a0f2619d756c223d42fad73eaf58f7533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4493522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844f4f11fe8d04e3b69e4f23063bf7551dcd49afa2df8b22ff09ab932d85f1a8`

```dockerfile
```

-	Layers:
	-	`sha256:2708918bcd4c0cd8a9295c30d52757ec544382da6221ae3e99b0c308054e3e91`  
		Last Modified: Tue, 03 Dec 2024 02:14:35 GMT  
		Size: 4.5 MB (4486744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d34f64a1c514c02f7b13010a041e7b1c35aa623aff72b601bb643cd6ba4519f5`  
		Last Modified: Tue, 03 Dec 2024 02:14:36 GMT  
		Size: 6.8 KB (6778 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:2c45feec361abb226bbf435f864494690255c4299754d9acd1f737535a7abe5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:oldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0f366899853a39f6d5bfefd3a1d87b9a6e77b0d1693f159852589bab14fa56de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 MB (124051506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e03eddae311a28e3cdc3b1e06a73fec0df44fe8ffe18ec3cd0a6beaa3679a61`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cd606f6f489eb66f1307280aec321b3af3aa998dca447ae1cc91c6b884240064`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 53.7 MB (53739147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925257a7168ed219a5d7c2a69af3245ca4cd9e376424f7f006535d9714437bd4`  
		Last Modified: Tue, 03 Dec 2024 02:15:41 GMT  
		Size: 15.6 MB (15558387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb34ce34679cf6bc8738a0166300fb0af605abff20bb9c1c8008dbc48722061`  
		Last Modified: Tue, 03 Dec 2024 03:17:12 GMT  
		Size: 54.8 MB (54753972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e95a5f98efdd6e08a12735a0fd6c4c5a3051965595a72f2c708ea4166ad4fd68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7725686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d18063dd303c3df8c4bc0ba7ee19280ba8273ba222cdf8806418d7ae0614de0`

```dockerfile
```

-	Layers:
	-	`sha256:8f8714a5245415496d1184c9bf67324931b783e6e2576f6937a4fee947db486f`  
		Last Modified: Tue, 03 Dec 2024 03:17:10 GMT  
		Size: 7.7 MB (7718333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea2d08ec39059b267a5fa537e634436554e564153de6341031fd87f0045d90b6`  
		Last Modified: Tue, 03 Dec 2024 03:17:10 GMT  
		Size: 7.4 KB (7353 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:be78aa16820580cada63d809a8bfb504aa1276f7dd084f6c2f84e0bb02c007ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114339194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a03adb57e3f60161d493f8c8f2d91f2d2c5df173bd292bc160c9c579cceef9f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:69dbedc8019388fd330866fcfa04c35d28f86d1ef986691ee290054433639992`  
		Last Modified: Tue, 03 Dec 2024 01:28:37 GMT  
		Size: 49.0 MB (49025021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370e6aa30e16daf07d99e3fb5cd8610cda77f49507a7b2ba76a646359cf7db6b`  
		Last Modified: Tue, 03 Dec 2024 07:36:42 GMT  
		Size: 14.7 MB (14673759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54bf5af43178bf200a2aed84d9a42570d6bde94092c2ac746652561137c9a86`  
		Last Modified: Tue, 03 Dec 2024 17:16:41 GMT  
		Size: 50.6 MB (50640414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e492de4a1bcc068b39955b80d874bf462808c59bf0ec31bb6bd280d936713d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7727144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd315f13cbfceff99c6d58272b95dd096b9512de6dd7537f6d6afe2fd3e64d2d`

```dockerfile
```

-	Layers:
	-	`sha256:21a97e5fb320768479f40b78f22eaeeef9eb396a0aed03b8d41ca681056c0752`  
		Last Modified: Tue, 03 Dec 2024 17:16:40 GMT  
		Size: 7.7 MB (7719731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51c5b9e593196a516856494c0dbea31bc158ff6fcc6058ea5e8c3d1a983de169`  
		Last Modified: Tue, 03 Dec 2024 17:16:40 GMT  
		Size: 7.4 KB (7413 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:96fa200ba907ff5f10dcad7d3e89a5fd73d7a5d5e9659f3ea75a0d9e5e39cb23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122642358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc6c1ae1ad1d343f3ddbe86366b8189c8c804cebc4df7e87157d0ffa17f9d336`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e357e1f94476a03fde298261e8c007d487d3cfade45a9eef064eba724a5c5e2e`  
		Last Modified: Tue, 03 Dec 2024 01:30:26 GMT  
		Size: 52.2 MB (52245994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b2279cee7374c65ae079e8ccdceeeb8b20c07ffc727e5b7cd595285b44a3a0`  
		Last Modified: Tue, 03 Dec 2024 05:39:10 GMT  
		Size: 15.5 MB (15544048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2749caeb5baae1b5e6316a6f02e57835aa548497fba6792be844c743a57c72a2`  
		Last Modified: Tue, 03 Dec 2024 11:51:00 GMT  
		Size: 54.9 MB (54852316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6f1b608089d0dcbf42f5fc54da8bb34eaf30baac382624cfcc5f1a0989e401a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7731504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1dc80dda6eb42786edf9a0b24dc97cc6190d25aee82b1fd1276db616e8ccbc3`

```dockerfile
```

-	Layers:
	-	`sha256:30fed3f253d5a80620794c68dafe113a0924ca7001e8da4f4d974c019fa6166f`  
		Last Modified: Tue, 03 Dec 2024 11:50:58 GMT  
		Size: 7.7 MB (7724072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a78a3d3e15864eb8fa9847638a76c54bab0eec07868a25d3aa7add0d432da7e`  
		Last Modified: Tue, 03 Dec 2024 11:50:57 GMT  
		Size: 7.4 KB (7432 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:eba00443a4dc065f45bcbede0181fa8dc5c28cbe1f55a18a9251feec5922c7ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126765451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ac82b6418e195c7b206d1965a4d4632534d11a24c0e88216d341de0b6ae49a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:862f429b4105c1e5714d48631896837c3ca6f797479296293b7c33c6699eae95`  
		Last Modified: Tue, 03 Dec 2024 01:27:25 GMT  
		Size: 54.7 MB (54676275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ac5b88f14d979c6f071eb85aa8a772f827338af23171657add5b5e4fc91e2e`  
		Last Modified: Tue, 03 Dec 2024 02:14:36 GMT  
		Size: 16.1 MB (16062064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc99b34aeb38c1b23bfa1cbb2b4b9d6e5a643b78e7b238368942282890609c8`  
		Last Modified: Tue, 03 Dec 2024 03:17:12 GMT  
		Size: 56.0 MB (56027112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2720d09566864abb3abb4f25253ebe3a61d88eb16747e675596008f1490ad5cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7721152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58543cbb4d408bacf014776698e3640af6c46424a52d359af87b4aec6dc23232`

```dockerfile
```

-	Layers:
	-	`sha256:652571b4e42beeac87dbcf820f654e65b967d8c560bdc560c5df4ce567fbfef1`  
		Last Modified: Tue, 03 Dec 2024 03:17:11 GMT  
		Size: 7.7 MB (7713821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5d6dbfe0b90b6c9489145208f3876d82d9a5511a023b5420de9795b688a43e9`  
		Last Modified: Tue, 03 Dec 2024 03:17:10 GMT  
		Size: 7.3 KB (7331 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:oracular`

```console
$ docker pull buildpack-deps@sha256:b08deb0d33d7f80992b25716c4fac0662387ea504455b28b26f1033220fe7096
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

### `buildpack-deps:oracular` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f2d468863910d62e7330375fd0395f4ad0779ec27a3ee0b00c49b0ea6b23afcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.2 MB (286231930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b5a46626d0cc438768876575effe13f925efd7379f00d0400c7b3741369191`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:08360137caccff53ccad4b814b2e19f27aa9fe2a71175550a7f6b13fe243924d in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:31734b193a814b7d6f96f0d11a89c942ca61ac79d819105323c548bf31f98613`  
		Last Modified: Wed, 20 Nov 2024 04:18:12 GMT  
		Size: 30.6 MB (30601312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb3a0dc114c54fd18d42d481f5d85eb84000d5cd297bd2f753d1290eb36719c`  
		Last Modified: Tue, 03 Dec 2024 02:29:09 GMT  
		Size: 15.4 MB (15374140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64ddd91578315b54cf47f01baf6ea302d702c1bc46efefdcad51af4f6a7812b`  
		Last Modified: Tue, 03 Dec 2024 03:17:12 GMT  
		Size: 46.5 MB (46491318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4065e49aa231bcf1f2eedf5b60edcdd89df6863377a6110a492b6bb6c2daf66`  
		Last Modified: Tue, 03 Dec 2024 04:32:09 GMT  
		Size: 193.8 MB (193765160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c5312bff979618340f2d1556c3453421e1e55f873bf4efe7ddc7d25705766245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11369581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8527a70c975c34f4def1074b8ee7f1aabf34798e8772d52d20aedd7f33eeda4f`

```dockerfile
```

-	Layers:
	-	`sha256:c5b9641e0dec7e5403d1612f3ae20c9d246f99bf083b7747bf196a3cfd9f730b`  
		Last Modified: Tue, 03 Dec 2024 04:32:07 GMT  
		Size: 11.4 MB (11359378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07ec353f310cb5323bbb08e4760de895cdc7de806f12f1ba46515611d0372297`  
		Last Modified: Tue, 03 Dec 2024 04:32:06 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5e6c535541d799fcadbade99bcad57a32135142047242193e8c6c420b1aa93e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 MB (248408833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9875927388483d1bb47a79ad5e415dfed6a83a9f1b688632c124b47324a667c5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:5cf848783aed3abcaefd540a7a70f443ef2bead6c50d01e0a72cd1aa6f542081 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c553618cfeea14cb253bd7777b2e3299019b3065e1cb073744b43353379582a7`  
		Last Modified: Wed, 20 Nov 2024 04:18:39 GMT  
		Size: 27.5 MB (27546971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a00677e72221e7026f8e6b0ed5b47e7316c84195a5d85d7c2cf005d741e670`  
		Last Modified: Tue, 03 Dec 2024 07:40:05 GMT  
		Size: 14.1 MB (14060900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c52f0d85713a2f01f551bbf8afba0de5917d8a73a492b3fca6575c2696d83eb`  
		Last Modified: Tue, 03 Dec 2024 17:21:00 GMT  
		Size: 49.5 MB (49462929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a1ade74a0a0a3cb322d91a5b98afa058c0268e2ceebea121af375e348bed51`  
		Last Modified: Tue, 03 Dec 2024 20:20:38 GMT  
		Size: 157.3 MB (157338033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c9b4c62d6c5815bea5eb2dd0d5b3c2d844959ccd8f09eab126117f4c48a373a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11149176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5650dba2bfa8ac954879544aa3ba225de09a50747a66b3d7deb6b194e3a56d`

```dockerfile
```

-	Layers:
	-	`sha256:998154eeaa3b2c9daa4fa63ce0763edc00fe6c7a8960cf03ff43f5137b32c574`  
		Last Modified: Tue, 03 Dec 2024 20:20:35 GMT  
		Size: 11.1 MB (11138913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:065d062a0d03124977ef15b202544942d5dcd3547f37a77db3a62bb85fa307b8`  
		Last Modified: Tue, 03 Dec 2024 20:20:34 GMT  
		Size: 10.3 KB (10263 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:42e5d1c5d818a085ca5eb3e65007a5613672626901be13287e2eb8977e12cbb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.9 MB (279937838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d17ee958e00a1a6edf4a25addf51b7d7cbe299dba12ade1e5849aa5e006b1f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:11edc0b5b8a0810c86ff8de1ece47e84856118afa9f296152b12c0bdabf33154 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6d229850a7784435237486a1406ffb5a4f0a4ac3b993928d18b30ad6853c6845`  
		Last Modified: Wed, 20 Nov 2024 04:18:26 GMT  
		Size: 30.3 MB (30284785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c08bcb2cbebb6d9db3a5ad2c52e975d21aa32088786303f6c521a0bb1f93f0`  
		Last Modified: Tue, 03 Dec 2024 05:41:40 GMT  
		Size: 15.1 MB (15147474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be5c9e4ce5805ad177f3aba8a70b5f1255051eb50b349f3819d9ee550186986`  
		Last Modified: Tue, 03 Dec 2024 11:54:23 GMT  
		Size: 46.4 MB (46423354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f144299644d986372fc7ab74c3e363056d5b1e93d2c8b4c856cb8d36c2a238d`  
		Last Modified: Tue, 03 Dec 2024 16:33:41 GMT  
		Size: 188.1 MB (188082225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a454f0ce4fefaaaf46eb66f48c64c50fb9f2005aad6a461386bf2369f9787302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11446009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73565036103c3e95c080e8ac4cd9db7e4f3901ca503409000edab5a9833aa071`

```dockerfile
```

-	Layers:
	-	`sha256:d9331ccd4adb34076f9c1de43104541397d3f4cad61b4f3912f2f5926f05f390`  
		Last Modified: Tue, 03 Dec 2024 16:33:37 GMT  
		Size: 11.4 MB (11435726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a806f212f7a6ab953efafd515e1def1e01f226f4883138d23f91068b4ae8cdcc`  
		Last Modified: Tue, 03 Dec 2024 16:33:37 GMT  
		Size: 10.3 KB (10283 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:07f2d3407c4086803bd20bacc23257dd31fd4031c8e86b5fb5c3620df1b3d0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301587069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7e09496b7805c1cef26d55c8f0982819a893d10d3d489717c57ffae9df60b9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:c92b611280c7d224d58f2a2a7dfdc19380dda99a38e10495643ec0b43d2f3cac in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2039ab37391bfea5163cf2545fcb585344c981096040149e81aec9301f35f97b`  
		Last Modified: Wed, 20 Nov 2024 04:18:53 GMT  
		Size: 35.1 MB (35063190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335ed3d865eafcfc72459a536871a40009d4a399d947a0418657fd44f442c19d`  
		Last Modified: Tue, 03 Dec 2024 04:41:29 GMT  
		Size: 17.2 MB (17249971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19dd08a4345b11dbad4e6464f658a55387f7b1317148b558d997474d998e8fe5`  
		Last Modified: Tue, 03 Dec 2024 09:48:00 GMT  
		Size: 51.8 MB (51759651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1e7838794de9de838af4f642fa9a2c7787fc250fe2e6ea745400b6b118189b`  
		Last Modified: Tue, 03 Dec 2024 16:33:24 GMT  
		Size: 197.5 MB (197514257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a639d44639e78ee7c6cd1b7d424ba1c4d797a91d6c804122fb85a0d4e7fd4696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11361895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896d60018831607d6cf171e3307e4738e1ca84613d5375a7c6513eb779e8d90e`

```dockerfile
```

-	Layers:
	-	`sha256:1245cc6f4d67addb23dc7ac9e404400d3a787b5fa977037662ca4247d44923dc`  
		Last Modified: Tue, 03 Dec 2024 16:33:20 GMT  
		Size: 11.4 MB (11351660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76663542be6a991f1c7a41dca7b3cd4aab48b5c7bdb938e0deaade848e7b5561`  
		Last Modified: Tue, 03 Dec 2024 16:33:19 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8d5a7f2f0db10b545763695bb927af0842ee2cfba1caefe2966992777d27afb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.2 MB (378202631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c665ea6044af20b4b12d2b65300f30d5b7695ba2bc0e5cf82b306177f50003f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:76a233bff3b463f93cb832f44963527276c1cd491cd0a75c9c5d2eac75da2380 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9d51f6335bdd76dd9dcfd4d3eaa2272acccc262c17300716acd3ffb0ec5f5846`  
		Last Modified: Wed, 20 Nov 2024 04:19:07 GMT  
		Size: 31.8 MB (31787958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48e90448070e192152f471d2c8fd1cfc67ec60c6cb742a212ead9de030d94d6`  
		Last Modified: Tue, 03 Dec 2024 06:47:45 GMT  
		Size: 15.9 MB (15890462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4180e9749ee9c2cd33764d68a8a49f4513db415bcf81e499f6bd3b0b7312f056`  
		Last Modified: Tue, 03 Dec 2024 09:56:53 GMT  
		Size: 54.6 MB (54615995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d229559deb983f34d263c1186e731a20b3d9db40451b4063f3de51f6fc326219`  
		Last Modified: Tue, 03 Dec 2024 11:31:19 GMT  
		Size: 275.9 MB (275908216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4e00820dd6ff6beb8effa14dc6357c1c4e04d951a758caacf793ec7dd2b33fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11417908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:664c2c34bd590b1f1e97e2d7910c02c94c1aeca1d6b7bba8fc435b595c252143`

```dockerfile
```

-	Layers:
	-	`sha256:d75666c5ed1b37cd483e2f968e564cfb994c3b7cb8acfabb93f8b56c5b7bb8d5`  
		Last Modified: Tue, 03 Dec 2024 11:30:44 GMT  
		Size: 11.4 MB (11407673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00bd0cdc0851b621344bcdeb7d234bb1dd772ad6c7004714a0e5ee05418e0d98`  
		Last Modified: Tue, 03 Dec 2024 11:30:42 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6f95adf3a52b8a9b79ba8f14c9b9ceddd5c0d7e858dddfc5423b476ef0221492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265507437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fcdc2270c2fb7756c24dfddace9096deec97390161569734095a649c3603a4e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:d8a0fd6e6a1b5571de35cb60b4e05523a0290523534ad63464fdf47dfbe0b041 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8ccad27fc3ed57037242d8c7dde5d5ce195749a63f65f7d9a663f7b822c4429a`  
		Last Modified: Wed, 20 Nov 2024 04:19:18 GMT  
		Size: 30.8 MB (30775034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d6a6da1657d09f717e7f94493d3e0563278583e47322d423316da636b93135`  
		Last Modified: Tue, 03 Dec 2024 04:11:01 GMT  
		Size: 16.9 MB (16937481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae51c456fa63fca49c43c89a34927e42baace55350a312e11092478ffa7894cf`  
		Last Modified: Tue, 03 Dec 2024 07:58:31 GMT  
		Size: 47.8 MB (47774022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9602e6e79d8a9afdd7c8691bf80181cc5be4942308ba620ef74fe70421e13ce3`  
		Last Modified: Tue, 03 Dec 2024 10:59:07 GMT  
		Size: 170.0 MB (170020900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c6c0e1f425fdb1d84c16cbbe7a6878cd2598f37f3526144365efe934b8b8a0be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11168896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb66150459757f9898298255cd0cb66c204688a4cf85ae139b5689db0254223`

```dockerfile
```

-	Layers:
	-	`sha256:7d36c1b3ced50159e6fdb1185db60346dc278bb5afe7507c3174f447100ae1e0`  
		Last Modified: Tue, 03 Dec 2024 10:59:03 GMT  
		Size: 11.2 MB (11158693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0de5e93240ee180a47ee52972d2c014e4e8cd4da6ee12024db5bd71f405d3966`  
		Last Modified: Tue, 03 Dec 2024 10:59:03 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:oracular-curl`

```console
$ docker pull buildpack-deps@sha256:5a54dd814c6322f357e43081a669e905c192ed0e4c17cd27e064d0def5fa804c
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

### `buildpack-deps:oracular-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:ea60a237b355b924d37dfe9aac67a3852d8b7c482233cb73265efeb09ae05ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45975452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c44578c4539dd052a272af1de7f824a2b22957771ec3454116fb0e0cdf6b203`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:08360137caccff53ccad4b814b2e19f27aa9fe2a71175550a7f6b13fe243924d in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:31734b193a814b7d6f96f0d11a89c942ca61ac79d819105323c548bf31f98613`  
		Last Modified: Wed, 20 Nov 2024 04:18:12 GMT  
		Size: 30.6 MB (30601312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb3a0dc114c54fd18d42d481f5d85eb84000d5cd297bd2f753d1290eb36719c`  
		Last Modified: Tue, 03 Dec 2024 02:29:09 GMT  
		Size: 15.4 MB (15374140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:957effd5c0cfdec1d2236e1c818d395fb9708f82fde1c0159a51006c10c4db0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b38744fcc95f8c64b212f80dbbf264a20abc2d1a16ea8ec9ae244f28dd1540`

```dockerfile
```

-	Layers:
	-	`sha256:8a09e8f1e8d49e683c807fbae21bec087375e537be6f69b9ce9487ac6f62914e`  
		Last Modified: Tue, 03 Dec 2024 02:29:09 GMT  
		Size: 2.5 MB (2458673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79e22805520c08d0bf06b9f9f7cb9b9d661114bc018017f25a45245d6f198ab7`  
		Last Modified: Tue, 03 Dec 2024 02:29:09 GMT  
		Size: 7.0 KB (6978 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:73c945b3d503d44be0dd39a8a3f5396dc07aa17344ef7f13d50dc5a35233c306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41607871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2428ec7695bd98edafe42303b40ca4ba3bd6cb2cd70a531dc2778e08123a19af`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:5cf848783aed3abcaefd540a7a70f443ef2bead6c50d01e0a72cd1aa6f542081 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c553618cfeea14cb253bd7777b2e3299019b3065e1cb073744b43353379582a7`  
		Last Modified: Wed, 20 Nov 2024 04:18:39 GMT  
		Size: 27.5 MB (27546971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a00677e72221e7026f8e6b0ed5b47e7316c84195a5d85d7c2cf005d741e670`  
		Last Modified: Tue, 03 Dec 2024 07:40:05 GMT  
		Size: 14.1 MB (14060900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:64158a88b94a807bc6c406afd30c1103e0a1f68b5ac32de7806d44a2139a2b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9439d1914bedbefbf8318533d3206dff74db23f82d6ecd51cc21da18bbb6242e`

```dockerfile
```

-	Layers:
	-	`sha256:b009ed268a6a16395e4b189138dfb01b08a1e04b7a9716b204143d5a7732e0e0`  
		Last Modified: Tue, 03 Dec 2024 07:40:05 GMT  
		Size: 2.5 MB (2460973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6749341c5939dcf0a0a5bfddb6738504b32558cb0fcd532ec7cfe233188ea4f2`  
		Last Modified: Tue, 03 Dec 2024 07:40:04 GMT  
		Size: 7.0 KB (7038 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f09db2479b3d7468d20c049a2ea861604f9a93f92357f5556e5953ada059807a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45432259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d138568e5d92a875546b89405710cf9c20c0cb837387f6e522e2dd6d78552a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:11edc0b5b8a0810c86ff8de1ece47e84856118afa9f296152b12c0bdabf33154 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6d229850a7784435237486a1406ffb5a4f0a4ac3b993928d18b30ad6853c6845`  
		Last Modified: Wed, 20 Nov 2024 04:18:26 GMT  
		Size: 30.3 MB (30284785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c08bcb2cbebb6d9db3a5ad2c52e975d21aa32088786303f6c521a0bb1f93f0`  
		Last Modified: Tue, 03 Dec 2024 05:41:40 GMT  
		Size: 15.1 MB (15147474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:302f64a92207589244d087350938653e787432e5ec6c888242a21c9244d5d2aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5084369ecb31ed6773a085b710f5afb7f8303a0ea405410a36fce2bbadc1fd91`

```dockerfile
```

-	Layers:
	-	`sha256:9b2a5e54b80389f06a288d3c2d31dd9785df28e6b3e45c1c02bb41ec2f5f7e0d`  
		Last Modified: Tue, 03 Dec 2024 05:41:40 GMT  
		Size: 2.5 MB (2459730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b10471618780d2cd17e1eb02c1f75d997b02047f3a6cce0d7ddabbb9a94ed840`  
		Last Modified: Tue, 03 Dec 2024 05:41:39 GMT  
		Size: 7.1 KB (7058 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:afcf6137703d492a678411153ac8bf0b6e55855e6d12c748e94ee79e57c7daed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52313161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e08b55ac61d2952ce86a0a9078c907bcae065e32f2b400770ed5b6a16d5bae4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:c92b611280c7d224d58f2a2a7dfdc19380dda99a38e10495643ec0b43d2f3cac in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2039ab37391bfea5163cf2545fcb585344c981096040149e81aec9301f35f97b`  
		Last Modified: Wed, 20 Nov 2024 04:18:53 GMT  
		Size: 35.1 MB (35063190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335ed3d865eafcfc72459a536871a40009d4a399d947a0418657fd44f442c19d`  
		Last Modified: Tue, 03 Dec 2024 04:41:29 GMT  
		Size: 17.2 MB (17249971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7fbed868bdfb8c0fa54ac0a7279ca61b33eeed3c2a9e726ae9bb38d573e0b530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2470166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52f7fe4f05dc1680e076f9aef3d1bc2134faee073b9ba0bc18b05119256d2fcb`

```dockerfile
```

-	Layers:
	-	`sha256:023e9cee20e6331d60b57fb976920eb158cbbd04e0fd5b4e078a377c498a3564`  
		Last Modified: Tue, 03 Dec 2024 04:41:29 GMT  
		Size: 2.5 MB (2463156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e962bf2a789e982d8814853042d4eae3e2593e723f80be215416b6b2339747f3`  
		Last Modified: Tue, 03 Dec 2024 04:41:28 GMT  
		Size: 7.0 KB (7010 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:935ce885aaf07bbae20dbdde74e64c6259174a52c31411d4d72246b46db888f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47678420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049e555341f0ccf882cd39e4a089dd2ca7abf815adc24e9ecd509f2c07e2dd03`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:76a233bff3b463f93cb832f44963527276c1cd491cd0a75c9c5d2eac75da2380 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9d51f6335bdd76dd9dcfd4d3eaa2272acccc262c17300716acd3ffb0ec5f5846`  
		Last Modified: Wed, 20 Nov 2024 04:19:07 GMT  
		Size: 31.8 MB (31787958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48e90448070e192152f471d2c8fd1cfc67ec60c6cb742a212ead9de030d94d6`  
		Last Modified: Tue, 03 Dec 2024 06:47:45 GMT  
		Size: 15.9 MB (15890462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4d2b49e90550c9c246be3d0a4bf462f6acedb554909b1dfcb1a519d9c36d4559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f301393f12913e8c6105d70130106fd53d8bdce15d8a7c4363bce194005f44`

```dockerfile
```

-	Layers:
	-	`sha256:96472992941cb5871f2eec833e53855a80be80e7b2a9db41e05de788c055a6c6`  
		Last Modified: Tue, 03 Dec 2024 06:47:43 GMT  
		Size: 2.5 MB (2452760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba079d972f1aa5b3c65cf4d4c0a20c942d9a5a9872a12ec2394241b40fa083b3`  
		Last Modified: Tue, 03 Dec 2024 06:47:43 GMT  
		Size: 7.0 KB (7010 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:474003861666c2558971d1f219ca0cf541319c9cc0ae74cec1f095764456d6bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47712515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bbdf4934968526ebef31cbef00996bd1644b8b673488498fe04ef2f4ae2a03d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:d8a0fd6e6a1b5571de35cb60b4e05523a0290523534ad63464fdf47dfbe0b041 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8ccad27fc3ed57037242d8c7dde5d5ce195749a63f65f7d9a663f7b822c4429a`  
		Last Modified: Wed, 20 Nov 2024 04:19:18 GMT  
		Size: 30.8 MB (30775034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d6a6da1657d09f717e7f94493d3e0563278583e47322d423316da636b93135`  
		Last Modified: Tue, 03 Dec 2024 04:11:01 GMT  
		Size: 16.9 MB (16937481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9ccdc5a771ad4d7e34fba168ad55fa04ffbdc5e1cd4d33921e18e2bfc7cfe988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e46556e422491046164719725145041e108a986a7b989584413193fdb296ff3`

```dockerfile
```

-	Layers:
	-	`sha256:1392030aa2010eab698fd29006239c1c0ace7587f2c6563790bc468c30ba86b0`  
		Last Modified: Tue, 03 Dec 2024 04:11:00 GMT  
		Size: 2.5 MB (2461504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3873b36bfe6641bfeee779ada1358ed661c445aaa055118aaf947bd635bea5f`  
		Last Modified: Tue, 03 Dec 2024 04:10:59 GMT  
		Size: 7.0 KB (6978 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:oracular-scm`

```console
$ docker pull buildpack-deps@sha256:0325cd014a1561ff9039b66c2bf45acf5981fde10dd02e119c30705e51c4b862
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

### `buildpack-deps:oracular-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:563e8451c6e61acd1253e9387da1481be89ae5e02a0111a8fc481ece758ea0eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92466770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d68ca44aa08186ffc80697404b975b0f1762747a215809a8a9f250099ea38b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:08360137caccff53ccad4b814b2e19f27aa9fe2a71175550a7f6b13fe243924d in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:31734b193a814b7d6f96f0d11a89c942ca61ac79d819105323c548bf31f98613`  
		Last Modified: Wed, 20 Nov 2024 04:18:12 GMT  
		Size: 30.6 MB (30601312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb3a0dc114c54fd18d42d481f5d85eb84000d5cd297bd2f753d1290eb36719c`  
		Last Modified: Tue, 03 Dec 2024 02:29:09 GMT  
		Size: 15.4 MB (15374140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64ddd91578315b54cf47f01baf6ea302d702c1bc46efefdcad51af4f6a7812b`  
		Last Modified: Tue, 03 Dec 2024 03:17:12 GMT  
		Size: 46.5 MB (46491318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8ba9fad56bedf47846b079812c8a6d4f47a1dc796f1dbccd5a2d1818033f9fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f725ce812a005ebd7092e7623bfe9c5a339b6bd4da22634dae370ff500604947`

```dockerfile
```

-	Layers:
	-	`sha256:c23bc9c092c296df444d5a1fbe7d557d5c72492a03d7b3b366f8a8106b1c9c9a`  
		Last Modified: Tue, 03 Dec 2024 03:17:11 GMT  
		Size: 5.1 MB (5090553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ba7f94c1ac96e0c4b0ea537df4662194ce9f2b029b822a146f047255b3af022`  
		Last Modified: Tue, 03 Dec 2024 03:17:11 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f35e17de918b1ab011fb1b0334a6c8c87fff4b4a798a2a2dd80bb307e39cdb6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91070800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27344efd4600537f2d0179a82ce6aa58a2d6a24a8cb1bc5ca2b9f675b5ba4d8c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:5cf848783aed3abcaefd540a7a70f443ef2bead6c50d01e0a72cd1aa6f542081 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c553618cfeea14cb253bd7777b2e3299019b3065e1cb073744b43353379582a7`  
		Last Modified: Wed, 20 Nov 2024 04:18:39 GMT  
		Size: 27.5 MB (27546971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a00677e72221e7026f8e6b0ed5b47e7316c84195a5d85d7c2cf005d741e670`  
		Last Modified: Tue, 03 Dec 2024 07:40:05 GMT  
		Size: 14.1 MB (14060900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c52f0d85713a2f01f551bbf8afba0de5917d8a73a492b3fca6575c2696d83eb`  
		Last Modified: Tue, 03 Dec 2024 17:21:00 GMT  
		Size: 49.5 MB (49462929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:321e47836c05fbb02e1fd02fcc1ddc2c3c9659ace387ed72c88a22a232eb575a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5099237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d40379b9a864667266d066d886c9bcad244b1e2b00a22868aeb7f34d7b32bef`

```dockerfile
```

-	Layers:
	-	`sha256:1ac741d22a8e2ee37128ae932b86c198778eea3fd1c9530edaa933db1bd2bcdf`  
		Last Modified: Tue, 03 Dec 2024 17:20:58 GMT  
		Size: 5.1 MB (5091853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86ff1a3ca795c61cc4e63a408b81086ade9a98c28eec81011f6ef2d2f5a94d23`  
		Last Modified: Tue, 03 Dec 2024 17:20:58 GMT  
		Size: 7.4 KB (7384 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cdd5ac19c22ca37622957e9f58856f47133d1411fe3dfd34e5351a0d0fb7618f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91855613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8100dbfdf0f4d4dff2d6d2e852b149139fee0a29c4411415c911d1f1751d4e6c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:11edc0b5b8a0810c86ff8de1ece47e84856118afa9f296152b12c0bdabf33154 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6d229850a7784435237486a1406ffb5a4f0a4ac3b993928d18b30ad6853c6845`  
		Last Modified: Wed, 20 Nov 2024 04:18:26 GMT  
		Size: 30.3 MB (30284785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c08bcb2cbebb6d9db3a5ad2c52e975d21aa32088786303f6c521a0bb1f93f0`  
		Last Modified: Tue, 03 Dec 2024 05:41:40 GMT  
		Size: 15.1 MB (15147474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be5c9e4ce5805ad177f3aba8a70b5f1255051eb50b349f3819d9ee550186986`  
		Last Modified: Tue, 03 Dec 2024 11:54:23 GMT  
		Size: 46.4 MB (46423354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:247fbd221ad5fefbf18c52d8696177a8e67b46e00e7d5e256a9bb950b590c27c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5105157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c6b74132fb1f57a9d10c9981fefad798e3ac9551eafd4bccce198df20b4cea`

```dockerfile
```

-	Layers:
	-	`sha256:5b41ccdf769d6aa00d98c9cdb9bbb11353d81d3f89b2d37beceb76d737d5c56b`  
		Last Modified: Tue, 03 Dec 2024 11:54:22 GMT  
		Size: 5.1 MB (5097754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:573bf2b358841fdfccaf73d76bb65caadd9092547578f7cb821e1c8bb50d90d5`  
		Last Modified: Tue, 03 Dec 2024 11:54:22 GMT  
		Size: 7.4 KB (7403 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a239a47dc8e5b6806865a5e03070765f807e7da9a0c102422dd3a07c529acd74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104072812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90eb7eda48c9009759efa5a71b21c19232dd9e939b9bfb8b227e2184996544a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:c92b611280c7d224d58f2a2a7dfdc19380dda99a38e10495643ec0b43d2f3cac in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2039ab37391bfea5163cf2545fcb585344c981096040149e81aec9301f35f97b`  
		Last Modified: Wed, 20 Nov 2024 04:18:53 GMT  
		Size: 35.1 MB (35063190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335ed3d865eafcfc72459a536871a40009d4a399d947a0418657fd44f442c19d`  
		Last Modified: Tue, 03 Dec 2024 04:41:29 GMT  
		Size: 17.2 MB (17249971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19dd08a4345b11dbad4e6464f658a55387f7b1317148b558d997474d998e8fe5`  
		Last Modified: Tue, 03 Dec 2024 09:48:00 GMT  
		Size: 51.8 MB (51759651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c130a7e829a6b443f2b97c312dd323c9a462ca1e026e197aadc5b21ecc986790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5105613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1625028337b25c7ac210d33078ca5ac38f23bfd2e34520ad48f429c8ca92ef68`

```dockerfile
```

-	Layers:
	-	`sha256:a3c2a14b768bf44d6822d31a9593eaf47e27792f166ba4409c25ab3efc284940`  
		Last Modified: Tue, 03 Dec 2024 09:47:59 GMT  
		Size: 5.1 MB (5098257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86c20aa62daf40d0f747e05c4aa0d8c6812e31a7c227af22143256968b2ff99c`  
		Last Modified: Tue, 03 Dec 2024 09:47:58 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:433d7c7534db974f6efa271e3c5a0f5a505951ec05bc1521bdc947528b7810b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102294415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ca9a8119745c25aeca54ed77326269bf0a54ea4e69be1a42f0f6019dc22d93`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:76a233bff3b463f93cb832f44963527276c1cd491cd0a75c9c5d2eac75da2380 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9d51f6335bdd76dd9dcfd4d3eaa2272acccc262c17300716acd3ffb0ec5f5846`  
		Last Modified: Wed, 20 Nov 2024 04:19:07 GMT  
		Size: 31.8 MB (31787958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48e90448070e192152f471d2c8fd1cfc67ec60c6cb742a212ead9de030d94d6`  
		Last Modified: Tue, 03 Dec 2024 06:47:45 GMT  
		Size: 15.9 MB (15890462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4180e9749ee9c2cd33764d68a8a49f4513db415bcf81e499f6bd3b0b7312f056`  
		Last Modified: Tue, 03 Dec 2024 09:56:53 GMT  
		Size: 54.6 MB (54615995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:245d67b3be9b6d8a36b5477106bc596ada0fed35d74e3e1a31a6a15a7046e41c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5088461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd75e0600209041192ec38179e6dfae3df9f1dc2525c0c16567bc7347656842`

```dockerfile
```

-	Layers:
	-	`sha256:9d4e7dcb1858d2f2531abf6ef24471fb2839217b70f08b487c477e1dfd58b118`  
		Last Modified: Tue, 03 Dec 2024 09:56:46 GMT  
		Size: 5.1 MB (5081105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e42cb4187568748dbfad0592a9dae3060f3ea3d1ca9bd6b07064ed838f66c8e5`  
		Last Modified: Tue, 03 Dec 2024 09:56:45 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6a9b27f24dfc6b4b5e36fc6f6151bb1580c136eb5a093d2d23f101392f7a30ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.5 MB (95486537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04161d746ba9ccae4b062c0456e0a82b55715a96f941ea113ee86cd4330059b5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:d8a0fd6e6a1b5571de35cb60b4e05523a0290523534ad63464fdf47dfbe0b041 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8ccad27fc3ed57037242d8c7dde5d5ce195749a63f65f7d9a663f7b822c4429a`  
		Last Modified: Wed, 20 Nov 2024 04:19:18 GMT  
		Size: 30.8 MB (30775034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d6a6da1657d09f717e7f94493d3e0563278583e47322d423316da636b93135`  
		Last Modified: Tue, 03 Dec 2024 04:11:01 GMT  
		Size: 16.9 MB (16937481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae51c456fa63fca49c43c89a34927e42baace55350a312e11092478ffa7894cf`  
		Last Modified: Tue, 03 Dec 2024 07:58:31 GMT  
		Size: 47.8 MB (47774022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:85a4c838344e21fdd6d0f53cf053cf9b033e8b5342d575dc09a6fc4a6355265a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5100212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690aa5a5d111b8e111274bdd5677c6c857f256dd71b29eaf8361700dd37e8047`

```dockerfile
```

-	Layers:
	-	`sha256:25b383443ef461e858ce8f8bd24de079c904448278eddb7473125e532a039dda`  
		Last Modified: Tue, 03 Dec 2024 07:58:29 GMT  
		Size: 5.1 MB (5092888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d29ee9c23c653e4f2f33a482a3aeb189af8c6d4b173b4ee25bd0046348f82cdb`  
		Last Modified: Tue, 03 Dec 2024 07:58:29 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:scm`

```console
$ docker pull buildpack-deps@sha256:9cb2ad7d26df8c138d5932843e460988b87f61ac5346721a3d1ad60c6d8a41d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:081b378225dd3efe7d85a0720370cbfd29b95001f7a0fb7073af54694ac974b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.8 MB (136754594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf470aba1a92d0771a65417e8a1beca6b311c9d18bcc12eb965032af2ee32b8a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd71677db44bb63b94de61b6f1f95d5540b4ba2d6a8a6bc4d19f422b25e0c2b`  
		Last Modified: Tue, 03 Dec 2024 02:28:49 GMT  
		Size: 23.9 MB (23865876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551df7f94f9c131f2fec0e8063142411365f0a1c88b935b9fac22be91af227e0`  
		Last Modified: Tue, 03 Dec 2024 03:17:14 GMT  
		Size: 64.4 MB (64391508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:20e125aea8586458a38f6d6b5fc4e799b157c40f6827bcdeede53d9deae5face
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7770849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed90e1697fb72676df77dcda5236274c90f61c17282ceccfc72e15b82f41da6`

```dockerfile
```

-	Layers:
	-	`sha256:012f88be9d04d99db39c2e75975d319894fe143e2f1d2c6b22032f733dc8c9a2`  
		Last Modified: Tue, 03 Dec 2024 03:17:12 GMT  
		Size: 7.8 MB (7763194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffa6b104b3f4a17660de0197b48ec8fbd2132b50b103011b72bafd123a894939`  
		Last Modified: Tue, 03 Dec 2024 03:17:12 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9b05d826a9aea2d34ea09a27fa55a3c9149103ac03323af230c8d2fcbcc8c5b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130561570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220e7a63ad00370b6e1c4651783b941fd094c6d2f66623cc356f07353ced08c9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a8ab0b752e573ceb3480052f24bc5fe3f4f4665c13a338db39c1d51f749528e9`  
		Last Modified: Tue, 03 Dec 2024 01:27:04 GMT  
		Size: 46.0 MB (46024374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff6779451547ba3f0647f15a65068290fed53b6a4ac506257de98e02857bea6`  
		Last Modified: Tue, 03 Dec 2024 05:23:42 GMT  
		Size: 22.5 MB (22540382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536c3cdef529f6d2993cf137c109a079266cd3effbffc602a136a2a60ee743a0`  
		Last Modified: Tue, 03 Dec 2024 08:40:08 GMT  
		Size: 62.0 MB (61996814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ba33181894b95455834717fb83a3cab2650b256f61a539f7419fc4f2e9c101c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7772471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49b76ea2636dae7de0703b48ca2f666e83f0a87977aff0a7884206898bf9654`

```dockerfile
```

-	Layers:
	-	`sha256:7b65f3800eb2add9f15ccf14f61be70696d82161b63f30b569972b0c8bd6a72e`  
		Last Modified: Tue, 03 Dec 2024 08:40:07 GMT  
		Size: 7.8 MB (7764748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4172764014ee95b8731a943cfba1e0f4e0e07007f8a4395720c1e0f1339fcccc`  
		Last Modified: Tue, 03 Dec 2024 08:40:06 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:390b0a015b9c6bd4a91717ab50b2da649b0e953291c1f6f179ac799ef34e25dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125608396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e6c420c1f7fb64fa485887316c939461f82ec6dbdf0ccd26e9a5970807dbee`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4d43724a324f138c88a78ca6df0a39ab6868bf1f121eb974439c5a51284e1ac2`  
		Last Modified: Tue, 03 Dec 2024 01:27:59 GMT  
		Size: 44.2 MB (44200109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff0e53b92c3d0f5c370d71aeac1be1d23e475f1afba41d896ace0ff6eeefc90`  
		Last Modified: Tue, 03 Dec 2024 07:36:14 GMT  
		Size: 21.8 MB (21767161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9625bef464ab08848044651374e04f75d37ada02fe71387c3f9f83d0c9376c59`  
		Last Modified: Tue, 03 Dec 2024 17:15:53 GMT  
		Size: 59.6 MB (59641126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:97cad46bffd054d5464b24f3898b89857a83b9327bd544db3f756fe68e8e5eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7772198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a53c50a14cb4d17416ad8c2b9f6ae29f07e4a2b9360068459000d153cbfa28`

```dockerfile
```

-	Layers:
	-	`sha256:98bbc215633288506c1cd937a4043acf7e3f2d79ced4e6d1b78fb36f63f12c90`  
		Last Modified: Tue, 03 Dec 2024 17:15:52 GMT  
		Size: 7.8 MB (7764475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4b268dda7212f4c955489072ec118680aa47218128cabc0b36f57ab7211081a`  
		Last Modified: Tue, 03 Dec 2024 17:15:51 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4b4fd9f631b9294a9c2600d58e03ea6aabe8064c9023517e3c004147a248c706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136079345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:294a87bc6560e0bb4acbf480b18930ca99a2863c50d4817579003ad59c8dcf5b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac722d9cf93b238dec2480278a2df5f8ccb672c97ec39f191191fd39f6721a8`  
		Last Modified: Tue, 03 Dec 2024 05:38:46 GMT  
		Size: 23.4 MB (23405813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261351ed796deb9fdad22dc734919eaf6726dd79a8dea99327d9e1376ecdcbce`  
		Last Modified: Tue, 03 Dec 2024 11:50:22 GMT  
		Size: 64.3 MB (64347852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:296b38d3b5682f620d8d350576747bedddd836671036ca931158e5fcc0abeba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7777352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6feeb02a68d010871c1233be105b538ae59e9b1d4fc972aaf364445fbcb678bd`

```dockerfile
```

-	Layers:
	-	`sha256:52070a7e355cffc4a9d0da8f0dc19e32ab40a808d402a964b8802456ba6e889f`  
		Last Modified: Tue, 03 Dec 2024 11:50:20 GMT  
		Size: 7.8 MB (7769605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:559dec8b2f1952ab63dd3ad11af3f0cab12b2904ee9ac16805ff6743224ac486`  
		Last Modified: Tue, 03 Dec 2024 11:50:19 GMT  
		Size: 7.7 KB (7747 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:efadcac373fc964d9e687e3c3acd546ed1243f3de78c4dfaa3cab0c1c44164bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140394239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c6c2127f1e3c3cff2f2545cac8268fc28d1eca7e5f18ebd9811301efedbc12`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:53769c348e57d646b1ec110dabf9d81a3f570afdb3b8216d1178515e4ea4ce1f`  
		Last Modified: Tue, 03 Dec 2024 01:27:09 GMT  
		Size: 49.5 MB (49476152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b0c73f75a815ce87bbf2841b694fdc4c29bcd072480b8752e8e91f0b59097b`  
		Last Modified: Tue, 03 Dec 2024 03:23:49 GMT  
		Size: 24.7 MB (24706896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2cf0351f309a0cf554972555b46b2ed97868d801e25eeed28a9f742a5e555c`  
		Last Modified: Tue, 03 Dec 2024 04:29:18 GMT  
		Size: 66.2 MB (66211191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:90045c81ec640293d6faa0394f96a1a985df7ff3d81fada2cfde8db780172edb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7766897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e344e02c870074180a5c7834575f4d8030d1e8969592d6bfa37194677c4d8bf3`

```dockerfile
```

-	Layers:
	-	`sha256:9855bce4e2e113f8c216ac6ecdad8a6af90932e14bc9bf28815c4fa67b760275`  
		Last Modified: Tue, 03 Dec 2024 04:29:16 GMT  
		Size: 7.8 MB (7759270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:487dfc9a24b2a2d5a2e18670b6601e6e1927433744a4d83a1dd8813646329b52`  
		Last Modified: Tue, 03 Dec 2024 04:29:16 GMT  
		Size: 7.6 KB (7627 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8915c51839fedacb07adb7002f8c190c948a12fcb503b7696ffc03b6a1b61ce2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135513047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbc8ce69146cef10089880f0995e0f8904567b5f315696d227d654aea381c65`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8f7c3140f4f3af477253c748b229283137cca4214e1c3df21109b821f9227620`  
		Last Modified: Tue, 03 Dec 2024 01:27:53 GMT  
		Size: 48.8 MB (48771844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa54d74c5fddb1e648e0a4d95fcc8338f5800ff817646baaa9e6e65596d80c5a`  
		Last Modified: Tue, 03 Dec 2024 15:45:04 GMT  
		Size: 23.5 MB (23458105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a279e7254de3fa3935af4b6008753d14fcd8db605c58b83903cf8c5f880324cd`  
		Last Modified: Tue, 03 Dec 2024 23:22:12 GMT  
		Size: 63.3 MB (63283098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1c84b11a183c60766b72298df7807d4c7092c9c2f73f1d21017e277fc9ab23ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a1f59aac2c22a1238dc51a66bd9dce102857527b4849511e58dc50dac965a0`

```dockerfile
```

-	Layers:
	-	`sha256:20ab0e5caa843ee96726eb9c38d13c80976c82e15ba6ba6202d3e1ba959cd413`  
		Last Modified: Tue, 03 Dec 2024 23:22:05 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f41ac76702c18986d7791e88468e69b4dc78c623d28e1a490e6c0cbbfc6b1082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147664451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514cb07cf8569c7b8531ad437622c499eedef341c3f377fe235d298f7e8ac991`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c84d784fe3c6c2bd95dea1c0d6eeba7c981bfb75bd53f81e83bcaadd87bba6f9`  
		Last Modified: Tue, 03 Dec 2024 01:28:03 GMT  
		Size: 52.3 MB (52328222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f0cfea13db30ebc69124696ada25182d1141398cd301a47a2cbf3c10d7fa9b`  
		Last Modified: Tue, 03 Dec 2024 04:36:57 GMT  
		Size: 25.5 MB (25523892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac73bc765d61ec6125ff5203c6c3d44543e6c3030684bfed0cb8f169640ae757`  
		Last Modified: Tue, 03 Dec 2024 09:41:44 GMT  
		Size: 69.8 MB (69812337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2a89a02d7b0a3fc01937338322a3adbfec4f8acf6ca3ccbf611a6bfea596fec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7778593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296a47c62b0745a03c2b02e5a3f2df0ebe6f985dc10f4132e1e9b9ea44ffc350`

```dockerfile
```

-	Layers:
	-	`sha256:4b033dd73e35183deec51e3e2b0975d4838f1627c9589d8d0a263fdb61430e94`  
		Last Modified: Tue, 03 Dec 2024 09:41:42 GMT  
		Size: 7.8 MB (7770901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1815558343ccce9363e7d65977e06bb87d6b20878e7dfbcffc07133ed7dee487`  
		Last Modified: Tue, 03 Dec 2024 09:41:41 GMT  
		Size: 7.7 KB (7692 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3b238b3a7258d279b52146096b4beb7f45782123399ba1107028fffcda72845a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134487608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55812b2c5a9e20ae6c6e47ae8abb5ecd135751de9755ada12406aef2a0ded189`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:53a5c0dbd93a4a7f540e18bbe49ba3d7fadaa390ebbce009c756e34c5b1ae048`  
		Last Modified: Tue, 03 Dec 2024 01:27:55 GMT  
		Size: 47.1 MB (47149767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ded5bb0b377b736e6c5f45164fe8916ada3485441e963fe2fc0671949650049`  
		Last Modified: Tue, 03 Dec 2024 04:07:42 GMT  
		Size: 23.9 MB (23864625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b626037a925f80e453161d124c98cc5578e9d47f3f90a050168552e9727a34e`  
		Last Modified: Tue, 03 Dec 2024 07:53:40 GMT  
		Size: 63.5 MB (63473216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2006631c59dc1f6d83026dc68c6f3367d6c4a1954eaaa7c817120bfb69572ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7770055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9c6b8467b7d857fa1c079d9b3e0091c74f5fa80c8cc76afe7c7a05ea96e216`

```dockerfile
```

-	Layers:
	-	`sha256:fcf08fd6e06e7a3eb093b7470b9f4abc277ecb5601672f6d97c6e6712c678832`  
		Last Modified: Tue, 03 Dec 2024 07:53:39 GMT  
		Size: 7.8 MB (7762400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f3eab35b34c262dbc9b817602d68d99ea2c9634756836744ea2d6a546474acd`  
		Last Modified: Tue, 03 Dec 2024 07:53:39 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:41fb2e2f70ae250becde9d66e7993eba6398121f63259e896c29939023f48122
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:sid` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:49a2b3da37cd499dea1130c7499ba1292cf6df9b0d9bbc31110bdb1f8cd8126e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.1 MB (376109677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6424a40167b63cc5bfd53ad8a9fed4471a02461aa8f996b50244a9cee25eb306`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9d0fec2ddc88227c9ea9ee67204e0e6a57a98553e405c78f6403be7627bc3834`  
		Last Modified: Tue, 03 Dec 2024 01:27:34 GMT  
		Size: 52.1 MB (52141610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e69332be439e88615e518602f8f7a133592f44d454cc5181ec830b7d4907dc`  
		Last Modified: Tue, 03 Dec 2024 02:28:57 GMT  
		Size: 21.4 MB (21366193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b9b96ccb05d400b1173a82c26d045cd47d1fcb41dec65a7bdc799295c8199e0`  
		Last Modified: Tue, 03 Dec 2024 03:17:08 GMT  
		Size: 67.2 MB (67204217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5aca1310c7893c8969698b84214f772ad0bb081926610513c433a74753433a6`  
		Last Modified: Tue, 03 Dec 2024 04:32:32 GMT  
		Size: 235.4 MB (235397657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cd46236b51a0c0457f02a62e58b36d7a2479b238241f6023be4d6f665e9a7203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16966812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee490560fe66570d36e832a5d2af23d37a6fb0193b9dd060959382f8722c7c2`

```dockerfile
```

-	Layers:
	-	`sha256:95ea3aa99343091b6c530e5b4003bb9943baa3728eec9189ceaf82ac8f4d10a7`  
		Last Modified: Tue, 03 Dec 2024 04:32:29 GMT  
		Size: 17.0 MB (16956636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:347ee90123489714c8c51b8c101dad86568718f1d6cf9349528215be573dd0a5`  
		Last Modified: Tue, 03 Dec 2024 04:32:27 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:fc11ba063b82a26c1aaaf9ff913e2f42b38968fc96aabba5f348fa24bb84e2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.6 MB (339648124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2412990718bb4a573f9f18cbe21335f389216ae3a56619ded3e9fe3a2d1b79f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:73a543e699956c37f431f5272a06bec8db5c16078190c6cd83886ca8de7b3dce`  
		Last Modified: Tue, 03 Dec 2024 01:27:39 GMT  
		Size: 48.7 MB (48676786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f2a807b7a079a7e314d111ccef3f84d1aec497cac9fbafa581f1603c0f9618`  
		Last Modified: Tue, 03 Dec 2024 05:24:32 GMT  
		Size: 20.3 MB (20286838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f15a8cfecadeff23ef5dad822a05b369166f8b1b8b5de808578d74b36d40854`  
		Last Modified: Tue, 03 Dec 2024 08:41:19 GMT  
		Size: 64.5 MB (64485676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f1d176aaf0da811a990a68b00d62be046f5280d8af55d181ec19374dc20c48`  
		Last Modified: Tue, 03 Dec 2024 10:09:16 GMT  
		Size: 206.2 MB (206198824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e16dc7b915d3d0791b2041d90a71ecc8ea1c0bf99101bf3b662e76079e74796e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16726539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66439361d67768c2375720d24cefced238c05f8ac79e1bde6cc06c0da714b789`

```dockerfile
```

-	Layers:
	-	`sha256:866634565228e1d5aa4a5e80f89ce85ac632f579ef0877313377f0be77c0ae38`  
		Last Modified: Tue, 03 Dec 2024 10:09:11 GMT  
		Size: 16.7 MB (16716303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f9ad5080cd41fe18f0fc7d92d9fa984cebecf82fc59f5b44440982d9eeb3217`  
		Last Modified: Tue, 03 Dec 2024 10:09:10 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:55385985caedb19950b81c9de475696914e04672e836beb3c49f895ae604d806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.7 MB (321702301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b34f202cc9b7e97c8977b98f75093537b9a0ac583436bf3e2f98d37f2cb5d5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b3be1b8d31fc4a12cecca1f9e259b73553bed584845788fd1fc2b66b29ec0da2`  
		Last Modified: Tue, 03 Dec 2024 01:29:47 GMT  
		Size: 46.7 MB (46707234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9942887cd0e4c0dbd616c261161d431660cfe04df19f0fb88f7040ab43995e`  
		Last Modified: Tue, 03 Dec 2024 07:37:28 GMT  
		Size: 19.6 MB (19598543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e09ace64d434f04ef956980b3273a080b684493925dd0ee78451c801f466f0`  
		Last Modified: Tue, 03 Dec 2024 17:17:42 GMT  
		Size: 62.0 MB (62009521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff06fd2d61b65d377aaab6adf0bb8120fbb9c2e98330722bd3c1c1dac2b6a938`  
		Last Modified: Tue, 03 Dec 2024 20:09:22 GMT  
		Size: 193.4 MB (193387003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1c7748deb3acaee05b2c2a23e55bac1b3ea86610b8cf98f2701b585873e98aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16732337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f9154eeb6c0b65c758f69fdaefe7849c9ba13a1080413b077e77af7aab7be1`

```dockerfile
```

-	Layers:
	-	`sha256:a3774835b78bdec0bc10768902dd8784a7302b6c4bda4c4f4f571b9c60c0ac2b`  
		Last Modified: Tue, 03 Dec 2024 20:09:18 GMT  
		Size: 16.7 MB (16722101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06696dd3871b1157c5fa70e82fdb3835c17190237bc1370b85860a2e7e8e6981`  
		Last Modified: Tue, 03 Dec 2024 20:09:17 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ca61d6852b240556b0c5025d7f1014496fd6dbd6959ba15284125e8f227db88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.6 MB (367594810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca9c8a6d0a7704491e80b1b6051b22b8da2b45b5ab7c289a8b4b898bdb2403e1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b484292747a3f8af5e498e897086e128c39ecc7aa3e027f8ce6a7b27ab3585c8`  
		Last Modified: Tue, 03 Dec 2024 01:31:21 GMT  
		Size: 52.4 MB (52363551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb4e12ac809713029b921818f315112d9a68fd814039c91956b3cdd9d07cd03`  
		Last Modified: Tue, 03 Dec 2024 05:39:40 GMT  
		Size: 21.0 MB (20983976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620061c3ebb2b35dbb417affed40f3038b1d12ab7ec1b666d509e18d8cc8ad18`  
		Last Modified: Tue, 03 Dec 2024 11:51:44 GMT  
		Size: 67.2 MB (67165131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5b28a91332cf32753c210d1c85e5266c3b7e92424235f8727d4db4f66ded61`  
		Last Modified: Tue, 03 Dec 2024 16:23:31 GMT  
		Size: 227.1 MB (227082152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7394f0f1c8a9b15dccaa6fefc028952784772f293e1527e33fc2efc01fc6f8f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17052000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0acf323e37d0ebafb9b1996e2fb4dd9c969df7be1b7497e4bbd149a119488abd`

```dockerfile
```

-	Layers:
	-	`sha256:f4a8d74b3828d20c625ad2d3d2553dfff0eea81de99a2522eaa7d503bbb04182`  
		Last Modified: Tue, 03 Dec 2024 16:23:27 GMT  
		Size: 17.0 MB (17041744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6d829fcc8e021404ee2581ca56cf93a9bf72b86fc9de94a648f2798d2f734be`  
		Last Modified: Tue, 03 Dec 2024 16:23:26 GMT  
		Size: 10.3 KB (10256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d366ce6267a346f53038978516f23bd4d6ee034c737fe7bdf5d54debb9dd3ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.2 MB (384246787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6f01c0e2e128b69c8f5020fffbdb84045ec77cd5254f9d865979f7e15f3029`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ef86bca2ffea293f73079f660a3399886008871df454d90312b7145d4395af98`  
		Last Modified: Tue, 03 Dec 2024 01:27:14 GMT  
		Size: 53.0 MB (52973420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183206547155d13d62e451041e3603fd7f5a0f4b1d6c8db0eaaf7ca1b4e51b07`  
		Last Modified: Tue, 03 Dec 2024 02:14:44 GMT  
		Size: 22.5 MB (22527751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8dd8a498f4405479d9e2bf04b4ed73d5dc63deb1d79c9d70eec7ddd7add1c35`  
		Last Modified: Tue, 03 Dec 2024 03:17:09 GMT  
		Size: 69.1 MB (69057622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b49bfdd692e8513701b0f0d930158f3f4d2aef5d64dff7bc22f6ccce56cf71b`  
		Last Modified: Tue, 03 Dec 2024 04:32:15 GMT  
		Size: 239.7 MB (239687994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7223f9d88774500fc3d64c0972df630401a88904948b414d81db8a6657f26dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16936367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff36bf12fbb75872174d04ce6204332f1de5ce54543955ba832418a0bee14ad`

```dockerfile
```

-	Layers:
	-	`sha256:4b6ef7d7bc0977f2ee04016de60f61d61f1e875ffc5ded21289b535075ef5236`  
		Last Modified: Tue, 03 Dec 2024 04:32:10 GMT  
		Size: 16.9 MB (16926213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7ada5f052e281d272d1947417f47424ce48e4072642dfae1ee7e16d1720a591`  
		Last Modified: Tue, 03 Dec 2024 04:32:09 GMT  
		Size: 10.2 KB (10154 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:97caf8af9ccb753cb7f0a15dd4d6e7b85df199b941e53e473528de89c603957f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.7 MB (352719608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62f24378805246617f053066f67939fc8f86f8c2e0536c869801c4c57300b4a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:547779e8d3d4ddde41b340ccc5c55eed6547696507cc0168eca950de620def24`  
		Last Modified: Tue, 03 Dec 2024 01:28:45 GMT  
		Size: 51.5 MB (51502465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fd17db4d55a0362abe181f4687b9308ab24eba56bf7c357aaf0150dda37b50`  
		Last Modified: Tue, 03 Dec 2024 15:47:12 GMT  
		Size: 21.7 MB (21747415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faad181192abe7945e2597dbe5a13adb7a6c4fc91c9cc8ed7907444e118bfa3f`  
		Last Modified: Tue, 03 Dec 2024 23:25:18 GMT  
		Size: 66.1 MB (66061059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df5e2e3f8704cd8f57eadead12d86fce2f48f9c5471960a3d7caa911e1ba9be`  
		Last Modified: Wed, 04 Dec 2024 04:49:12 GMT  
		Size: 213.4 MB (213408669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a8fc1d3466ccfed6239df0794a374e4154c2dbe91e7dfb3c88eb714ec9781125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab85850533c58616e5ba9342b19d94baa414e3caae56b247f2fd7324b4e2aba1`

```dockerfile
```

-	Layers:
	-	`sha256:e8a2386f905b3062ec0484433f9fdb32f3b1814e63a581a4fb0f013698107e33`  
		Last Modified: Wed, 04 Dec 2024 04:48:53 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6bc19564fe24be256fafa93692fee2e057f1bfce2a467077582364c36f312501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.1 MB (383146258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b3a3d439cd386298430241ef8eb9396878bfeb4ed9bef7199ba205959d5ef3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f96af90d82a1692028e6cdf912ac7419c2ecdd75603a19fc1f1b3b9e9bd29a53`  
		Last Modified: Tue, 03 Dec 2024 01:29:07 GMT  
		Size: 56.0 MB (55979543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5109fb930f5078004be0affb782c6af72db917a8e8c95675e33088c19131df3`  
		Last Modified: Tue, 03 Dec 2024 04:37:41 GMT  
		Size: 22.8 MB (22802436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77093ba8fdd419c4df155b02b29ff2686cd2a1d51168effbff5b4e39d31c96b6`  
		Last Modified: Tue, 03 Dec 2024 09:43:21 GMT  
		Size: 72.5 MB (72483296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a580742dd0d6b25eae1fa9319e34f6aec541ba477a9cef1cdf4484b82dd70279`  
		Last Modified: Tue, 03 Dec 2024 16:17:11 GMT  
		Size: 231.9 MB (231880983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5e0b7842efee0560cbb97a8bf463f8ce0017e26ab3fb70853b19dfd42cf19f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16947386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490dc7b944706942ddc307593cfcf31eb6789669a5421161813ca686742e43d3`

```dockerfile
```

-	Layers:
	-	`sha256:adea640ebcb9f657019594233f9ed28bb4fd297667bf3496b4bc59c52d3184df`  
		Last Modified: Tue, 03 Dec 2024 16:17:06 GMT  
		Size: 16.9 MB (16937178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:317a52d715af8ed8e9f6aa2c264eaf47458539127bf4f5013692e6e37b8712e3`  
		Last Modified: Tue, 03 Dec 2024 16:17:05 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:28f75fbff7fea1754f66f2ff9c7640c4c06fd16ffdfc224eb2f8fd1772f538b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **457.0 MB (456979288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155400acc66a00f8f4f35c553e7f4f9c8e73796171ecaec90abeb17edf42806a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6a129056497962be3ca4efb9ff44f747d1222200200be5fae7999b10e3156cc0`  
		Last Modified: Tue, 03 Dec 2024 01:29:15 GMT  
		Size: 50.6 MB (50632627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d233c7b4fb57ebb3fc06e5b0c070fac8c8f89639814479f25441c1938943ba`  
		Last Modified: Tue, 03 Dec 2024 02:51:09 GMT  
		Size: 20.8 MB (20822777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f14784271331931f12f38e0de1c6c4183501776dd43b01c47876c85796c8558`  
		Last Modified: Tue, 03 Dec 2024 06:42:00 GMT  
		Size: 66.2 MB (66176026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916fb889a6cd610a8a181a1ed9f57ffa7abe21fee8ea8ac8ad30325ce0b47c57`  
		Last Modified: Tue, 03 Dec 2024 09:46:02 GMT  
		Size: 319.3 MB (319347858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:aa374b77f1ca17f70075124a2c8053c4dafb365a746fcadab9fbd94e0e9c1a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17012542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857a6ebeb6a5606160740b66667e437826698b5d6d0790a7f6fd64dc0e8d105b`

```dockerfile
```

-	Layers:
	-	`sha256:a43d787d954c874af6db8dbc822b7d6e42a06c9c0cef5bcd7c1559891005d498`  
		Last Modified: Tue, 03 Dec 2024 09:45:19 GMT  
		Size: 17.0 MB (17002334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a213c48f55ff98d0845193b83743c6cf5dedca52db3ce6eab0b9aff84a3cf00`  
		Last Modified: Tue, 03 Dec 2024 09:45:16 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1df3ba79cb55d883ad913395b36a513bfc917c15b7caf38cd88c8c665777683c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.7 MB (349670575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b982bb3ebcb5f081cb00461966a8802023bcb16a8a774a3730540353081667e2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5d3fd94703dd00b00c7acc09539942c89a4634b13c2ae0ee29086b6288d43a47`  
		Last Modified: Tue, 03 Dec 2024 01:29:01 GMT  
		Size: 52.1 MB (52083835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79c38d4fbdb1d980e95882f99ea9064cdd90b1c1070a263467e442acb813b03`  
		Last Modified: Tue, 03 Dec 2024 04:08:31 GMT  
		Size: 22.6 MB (22559777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1dd971e7560ef90c41327cadf96b46eeb95360bc6b43dff330bf117ebb3df64`  
		Last Modified: Tue, 03 Dec 2024 07:55:00 GMT  
		Size: 68.3 MB (68263935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f973d95ee4eb4554be6abf2f8a00814eee05529e41a4930c8ffae282529578`  
		Last Modified: Tue, 03 Dec 2024 10:44:48 GMT  
		Size: 206.8 MB (206763028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fe39f39f7f1bde3d6c9e5c818bc628469875b2aa3b927edc66c74bf70a22412b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16747718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ebe5f6db202526925c56ad1faf6b865d027a0465734a2288e2f1ecc5c74d2b`

```dockerfile
```

-	Layers:
	-	`sha256:3d93d11363e6dc9d7925d0a3b5dbdca207392f40e1f417fe1bace7d8da06f1be`  
		Last Modified: Tue, 03 Dec 2024 10:44:38 GMT  
		Size: 16.7 MB (16737543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:125fd07fab195f7bfaf54230410ce6eb672c899fbd818dc4533083b58c05c9d2`  
		Last Modified: Tue, 03 Dec 2024 10:44:38 GMT  
		Size: 10.2 KB (10175 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:f5e71aa29f2601128aa7050df6278f4f29c1bb8bc57a61344d969e0124f2d910
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:204fc7cb93e6b1c5d3701d9bb7b17f47f36c32312b13aab7a3e1eecb149cae55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73507803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d3aa6b1c65c3ca1c85ad847490f6b3aaaa53facd8fbf401d4ddec6b5807971`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9d0fec2ddc88227c9ea9ee67204e0e6a57a98553e405c78f6403be7627bc3834`  
		Last Modified: Tue, 03 Dec 2024 01:27:34 GMT  
		Size: 52.1 MB (52141610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e69332be439e88615e518602f8f7a133592f44d454cc5181ec830b7d4907dc`  
		Last Modified: Tue, 03 Dec 2024 02:28:57 GMT  
		Size: 21.4 MB (21366193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3c19b6e7dc1bfd1817f85314eb3cad6f9b646341f80cd03cd40656b1ede3672b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4050455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15c4d7443fd64f1c8254c1ccb0d676a805bf354e184fbf250932ab147b99693`

```dockerfile
```

-	Layers:
	-	`sha256:8b30370abcd3c800357528cee52c171f19f828ebd96c3d2beb8fb8bb113da450`  
		Last Modified: Tue, 03 Dec 2024 02:28:56 GMT  
		Size: 4.0 MB (4043653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44bc99210dbb035b3c8e40a98c8830893bcf5823bcaab362c506ced9d2e06c17`  
		Last Modified: Tue, 03 Dec 2024 02:28:56 GMT  
		Size: 6.8 KB (6802 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e0c26364853da5e75896f031d3d2066ca0b0ebea6064c0802e48cb002b909a39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68963624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2e1229b95235bac1c5cbcf446d7e9e39ec403dd559a52fa597f5ea92286169`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:73a543e699956c37f431f5272a06bec8db5c16078190c6cd83886ca8de7b3dce`  
		Last Modified: Tue, 03 Dec 2024 01:27:39 GMT  
		Size: 48.7 MB (48676786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f2a807b7a079a7e314d111ccef3f84d1aec497cac9fbafa581f1603c0f9618`  
		Last Modified: Tue, 03 Dec 2024 05:24:32 GMT  
		Size: 20.3 MB (20286838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:81227ab69595f9829c5e51c760a792f754393155a80fa9e5c7ea97270b64b66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4052738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd6a50c2ec5b6f28659d8ac5731b5b191b0bef1493df2890fece6c6bda7b1918`

```dockerfile
```

-	Layers:
	-	`sha256:8a6d09a593299d0ecf8ccbedf48989b9fa1e80596cba5f0888fd729d08e03de0`  
		Last Modified: Tue, 03 Dec 2024 05:24:31 GMT  
		Size: 4.0 MB (4045875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3815fe36d9422647ced3357e6453c8f5a123a633108c99d47a75621924d53a30`  
		Last Modified: Tue, 03 Dec 2024 05:24:31 GMT  
		Size: 6.9 KB (6863 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:cc4b2bdff03629d69feb728d273e0d532e0d425550d77fc4d428a98662e506ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66305777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08dd76319b781f4765aebe68e8f8f83425d978da56b8908c1f9a09fd10cd4fac`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b3be1b8d31fc4a12cecca1f9e259b73553bed584845788fd1fc2b66b29ec0da2`  
		Last Modified: Tue, 03 Dec 2024 01:29:47 GMT  
		Size: 46.7 MB (46707234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9942887cd0e4c0dbd616c261161d431660cfe04df19f0fb88f7040ab43995e`  
		Last Modified: Tue, 03 Dec 2024 07:37:28 GMT  
		Size: 19.6 MB (19598543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:07eef967eb655fb18f0d2c2c11f4c816279a67bdd59790b99251f3f5e1d908e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18671eba9c6dac63abf5e1aacde8418a8ec079f015aba5a58f71d647b0eb7f11`

```dockerfile
```

-	Layers:
	-	`sha256:a73bb5456d7763921c5061137bf4a7b19f10585c609ef3370e5bd8e6975c4870`  
		Last Modified: Tue, 03 Dec 2024 07:37:27 GMT  
		Size: 4.0 MB (4044673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c5cb0ef0323af3e1a3e008d5e57343569405babcfaa127188257693204bc034`  
		Last Modified: Tue, 03 Dec 2024 07:37:27 GMT  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8ea9887f4714527d9d5254f762de02c92d4f7bae369fa18b0ba9ee5d8a5f7a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73347527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b445d459eed6e2aaa0ca2873d2fef7a47c8f779e4e527578f018fee5542d5d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b484292747a3f8af5e498e897086e128c39ecc7aa3e027f8ce6a7b27ab3585c8`  
		Last Modified: Tue, 03 Dec 2024 01:31:21 GMT  
		Size: 52.4 MB (52363551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb4e12ac809713029b921818f315112d9a68fd814039c91956b3cdd9d07cd03`  
		Last Modified: Tue, 03 Dec 2024 05:39:40 GMT  
		Size: 21.0 MB (20983976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:efb2879bdbe93ed419ee51ad67c5b73260cbe9762f879b6525c357a6a1c79dfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4054793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0104e88a325a66592832bfa12159a43f2db9c0662ddc2a476e9b5b61eefe533`

```dockerfile
```

-	Layers:
	-	`sha256:21a43c5405ce1ce47e7024330b2a77d04d6962e99937eb27750094d8f9088a75`  
		Last Modified: Tue, 03 Dec 2024 05:39:38 GMT  
		Size: 4.0 MB (4047909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e42bbda426096d69b867a0dc63238898e7dbec844f816cdc22f46d8ec7561d9`  
		Last Modified: Tue, 03 Dec 2024 05:39:38 GMT  
		Size: 6.9 KB (6884 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:8dae1c26ca64bef3fd697b7cf02f4b2c366e85a6c73f01b5e0b9afb622c5fdb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75501171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875a11a23487b00a03f1f0044e25daf842fb4cdab0a6dcdb4c3a2f74eda5811d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ef86bca2ffea293f73079f660a3399886008871df454d90312b7145d4395af98`  
		Last Modified: Tue, 03 Dec 2024 01:27:14 GMT  
		Size: 53.0 MB (52973420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183206547155d13d62e451041e3603fd7f5a0f4b1d6c8db0eaaf7ca1b4e51b07`  
		Last Modified: Tue, 03 Dec 2024 02:14:44 GMT  
		Size: 22.5 MB (22527751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fc30c76fa56490aa8d4359be5a51f884a93180fe27ba95093b6f4249461d8ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4046182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526990c3201f01d1bd4d6d57dcf3e812be838f5800ba8ff10188b3839c34d19c`

```dockerfile
```

-	Layers:
	-	`sha256:ef89ebeb6f21e1f73525cefa6b3bb32a2c605d18a8f97b9fd5da7036c0295c46`  
		Last Modified: Tue, 03 Dec 2024 02:14:43 GMT  
		Size: 4.0 MB (4039400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d6a2f676cc8e92c792af6635a13a376cb77dde477c35e1d9465bf4009920b0d`  
		Last Modified: Tue, 03 Dec 2024 02:14:43 GMT  
		Size: 6.8 KB (6782 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:891f8b0644f2ce029fdfb4250af9c7c22f3ffdd76191782fccffef0b9e3b249a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73249880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4673bea9b1756010dfb677b2ee62e809bade3a1de565fe922df855fddf5849aa`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:547779e8d3d4ddde41b340ccc5c55eed6547696507cc0168eca950de620def24`  
		Last Modified: Tue, 03 Dec 2024 01:28:45 GMT  
		Size: 51.5 MB (51502465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fd17db4d55a0362abe181f4687b9308ab24eba56bf7c357aaf0150dda37b50`  
		Last Modified: Tue, 03 Dec 2024 15:47:12 GMT  
		Size: 21.7 MB (21747415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d32b69785698093e0be0f82a00aaef093cb1391c8da6cb9dcea17352e1f56697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 KB (6637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:349e281e55adf0a1012c38c3ecee53c2afce3499397ddf5f3c275529952692a9`

```dockerfile
```

-	Layers:
	-	`sha256:5746c842a00740e7c683b3e380cb5794aef1759e591efcca8935e86ea9691f85`  
		Last Modified: Tue, 03 Dec 2024 15:47:09 GMT  
		Size: 6.6 KB (6637 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:47ee79acdeb89205c257ecbedda3b0eb55e581f832165079a17a7b01cd288b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 MB (78781979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32bcf58578328b1231b58d5b8944d36bc4ba40ee49ae98c44558d7b7ed3a54ea`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f96af90d82a1692028e6cdf912ac7419c2ecdd75603a19fc1f1b3b9e9bd29a53`  
		Last Modified: Tue, 03 Dec 2024 01:29:07 GMT  
		Size: 56.0 MB (55979543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5109fb930f5078004be0affb782c6af72db917a8e8c95675e33088c19131df3`  
		Last Modified: Tue, 03 Dec 2024 04:37:41 GMT  
		Size: 22.8 MB (22802436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1264f415c874219bf1d93ed1a65ffb3823a4a931fed9bcc0dd443056df716e5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4053760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39caff4ffb294476abd1b4095aa9254d65feebe0abe1b8add2b60d2243cee46b`

```dockerfile
```

-	Layers:
	-	`sha256:cf5ac8a981390a4e2c3640c75cbafcab45c0cda33f1490731ff4029c7048ddfc`  
		Last Modified: Tue, 03 Dec 2024 04:37:40 GMT  
		Size: 4.0 MB (4046924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9669a33d493726e89d132782bdb9de12e182fd2b8f0009472a97ff07522a0575`  
		Last Modified: Tue, 03 Dec 2024 04:37:40 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:b586a30adedcf91253b4e723a2fb98577d3112ba0edafae4a3169cbbe4b467c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71455404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f858b529436819defd2e23a4d8d4cc35636897a62586414cf76f538931ad6e5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6a129056497962be3ca4efb9ff44f747d1222200200be5fae7999b10e3156cc0`  
		Last Modified: Tue, 03 Dec 2024 01:29:15 GMT  
		Size: 50.6 MB (50632627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d233c7b4fb57ebb3fc06e5b0c070fac8c8f89639814479f25441c1938943ba`  
		Last Modified: Tue, 03 Dec 2024 02:51:09 GMT  
		Size: 20.8 MB (20822777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d4b9830bd87fccccf6e3080d90de56b90eaabeba62546b0628aefaa4ae2da16b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4043359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103e57e6a56d779b28625d6494beb70b785b3fc5feb250ae02f6560c186c31de`

```dockerfile
```

-	Layers:
	-	`sha256:bbef88f018a4f6f847dcbacbd9fae201001983766aaa9ba52cf76fcc836d22c6`  
		Last Modified: Tue, 03 Dec 2024 02:51:06 GMT  
		Size: 4.0 MB (4036523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f42fe56ae477e436b08ca6348817a884c70598cd0cf20f64af658727e556813`  
		Last Modified: Tue, 03 Dec 2024 02:51:06 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:aa8bd5667c1e53625735710349a9740d77fa5aaa879d3a977adf6247b361421c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74643612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4653b03d76739840fe4be4479dc8274aefd31736a0302005a389e88cbf472bc0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5d3fd94703dd00b00c7acc09539942c89a4634b13c2ae0ee29086b6288d43a47`  
		Last Modified: Tue, 03 Dec 2024 01:29:01 GMT  
		Size: 52.1 MB (52083835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79c38d4fbdb1d980e95882f99ea9064cdd90b1c1070a263467e442acb813b03`  
		Last Modified: Tue, 03 Dec 2024 04:08:31 GMT  
		Size: 22.6 MB (22559777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c50b19b70400d98afbb0a18ed63e699890ce23cddf01fc0abb0fbfe916dbfe6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4056542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0cb0567221a8fdf7e234accf3825319db8e5a4ce9cfa46e3d7f786610a1bdb5`

```dockerfile
```

-	Layers:
	-	`sha256:0e58fd28fae7b037ea9d243d9a380a50fd4bf594f2960b0e40d34a4510d2522c`  
		Last Modified: Tue, 03 Dec 2024 04:08:31 GMT  
		Size: 4.0 MB (4049739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:367e00e07da6a96ad160be887964afb0f841afb80806423c924a594dcf18c990`  
		Last Modified: Tue, 03 Dec 2024 04:08:31 GMT  
		Size: 6.8 KB (6803 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:5d3a345d10db23f764771a5183825102d0412407a3c3e7a1b3241422f8342781
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:sid-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:98ae8322e21402d9d1a47ae330578c281bedd95f82e7551694698c1c73d150b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140712020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff602ec12cae508a5eff7f955f1f3b4a7b0116e7f63fd95e3aede38e2531f3b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9d0fec2ddc88227c9ea9ee67204e0e6a57a98553e405c78f6403be7627bc3834`  
		Last Modified: Tue, 03 Dec 2024 01:27:34 GMT  
		Size: 52.1 MB (52141610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e69332be439e88615e518602f8f7a133592f44d454cc5181ec830b7d4907dc`  
		Last Modified: Tue, 03 Dec 2024 02:28:57 GMT  
		Size: 21.4 MB (21366193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b9b96ccb05d400b1173a82c26d045cd47d1fcb41dec65a7bdc799295c8199e0`  
		Last Modified: Tue, 03 Dec 2024 03:17:08 GMT  
		Size: 67.2 MB (67204217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c7f7f8c9fe198f76ea4d557014b74867442af6b19728ed19e19b5db24d2c9787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7673901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9655e2d30b820946d8a9271aebee6149dad6dd472e02bd0dd2490a28bc82a1`

```dockerfile
```

-	Layers:
	-	`sha256:9b8dcc9e196bdf56ae35756553a098b57ee3322218cfe81f94b8d219dffaf1cf`  
		Last Modified: Tue, 03 Dec 2024 03:17:07 GMT  
		Size: 7.7 MB (7666604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cb4b8ce456f309d5ac4f45927a3297061e4c2e8acfb4c80126d9bf3ee145d25`  
		Last Modified: Tue, 03 Dec 2024 03:17:07 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:2966584a59d9e0b9d32e6387a215e424e5bc2afa5c60c678e1a02c0fe9157edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.4 MB (133449300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d6416fa362396520065273d8b095ca52c840c3f07b1a58aff7022f82309846`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:73a543e699956c37f431f5272a06bec8db5c16078190c6cd83886ca8de7b3dce`  
		Last Modified: Tue, 03 Dec 2024 01:27:39 GMT  
		Size: 48.7 MB (48676786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f2a807b7a079a7e314d111ccef3f84d1aec497cac9fbafa581f1603c0f9618`  
		Last Modified: Tue, 03 Dec 2024 05:24:32 GMT  
		Size: 20.3 MB (20286838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f15a8cfecadeff23ef5dad822a05b369166f8b1b8b5de808578d74b36d40854`  
		Last Modified: Tue, 03 Dec 2024 08:41:19 GMT  
		Size: 64.5 MB (64485676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:774970a968d4bd940468709784d0674f8143d9516348b45292c1efa99c37307a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7674236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a1bbb775be08af72d3f2b911e5d67dc53477881a4678e428606938e9329a5f1`

```dockerfile
```

-	Layers:
	-	`sha256:be2af54aca073400cedd5c0c72179622b7d427625d2e6476881c2fd812ffaa14`  
		Last Modified: Tue, 03 Dec 2024 08:41:17 GMT  
		Size: 7.7 MB (7666879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b328f7f3ac3c501a7f6ae35a51e43d86de914bbc0bad3222005f311fcd396127`  
		Last Modified: Tue, 03 Dec 2024 08:41:17 GMT  
		Size: 7.4 KB (7357 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:387e61670c0dd5342002ec5ff918f89043546aeb014c47740d6a6eb73e793cf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128315298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83744aacda8eb7e6caeaf7ffde4ac82bdcb20f28f3e0fd1209a6eb0f6e93d062`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b3be1b8d31fc4a12cecca1f9e259b73553bed584845788fd1fc2b66b29ec0da2`  
		Last Modified: Tue, 03 Dec 2024 01:29:47 GMT  
		Size: 46.7 MB (46707234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9942887cd0e4c0dbd616c261161d431660cfe04df19f0fb88f7040ab43995e`  
		Last Modified: Tue, 03 Dec 2024 07:37:28 GMT  
		Size: 19.6 MB (19598543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e09ace64d434f04ef956980b3273a080b684493925dd0ee78451c801f466f0`  
		Last Modified: Tue, 03 Dec 2024 17:17:42 GMT  
		Size: 62.0 MB (62009521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1dc94d5835984fdc1913e5dac619d4dde7f4a1411d27b563c296a3ac14bc1397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7674007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2b45b5bbe0d268dbd9fbef0e1d7003f86def947cd36bdd6998c1492df05c71`

```dockerfile
```

-	Layers:
	-	`sha256:1b67bdad54ee7d3cf3d2bed02ab7da4f2712603a6854f36a13d5422c730edd72`  
		Last Modified: Tue, 03 Dec 2024 17:17:40 GMT  
		Size: 7.7 MB (7666651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3f1e3c2cd17fdeaa8aab05283566fc3819f300894aa57674c19ce25ecbe50a1`  
		Last Modified: Tue, 03 Dec 2024 17:17:40 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ba6f42ba7aefae054d5f3f1bb2c078cc0b42154bf67985259ea51890f16e92f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140512658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4bc14651d67b3d787ab2c20f60a20cd4624ada311d68df39bb40b296c58f4c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b484292747a3f8af5e498e897086e128c39ecc7aa3e027f8ce6a7b27ab3585c8`  
		Last Modified: Tue, 03 Dec 2024 01:31:21 GMT  
		Size: 52.4 MB (52363551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb4e12ac809713029b921818f315112d9a68fd814039c91956b3cdd9d07cd03`  
		Last Modified: Tue, 03 Dec 2024 05:39:40 GMT  
		Size: 21.0 MB (20983976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620061c3ebb2b35dbb417affed40f3038b1d12ab7ec1b666d509e18d8cc8ad18`  
		Last Modified: Tue, 03 Dec 2024 11:51:44 GMT  
		Size: 67.2 MB (67165131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:aa757aa7912e5aa5e678a45ae35e15003eb74a602d8da40aa9ffaf5e93f5a840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7684385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ff85394930bde7b388d9d6c1cf7bab862637d3629f3cdb3e6953a2fced1b40`

```dockerfile
```

-	Layers:
	-	`sha256:035677f5fb6f054407dcea7a584fe83af8c3343ee7a4ee69e62dfb3955679e5b`  
		Last Modified: Tue, 03 Dec 2024 11:51:42 GMT  
		Size: 7.7 MB (7677008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbdd037048e81b72bd044d348d4ce9bb4e7a97b2f9ee3680fd1ae6a27f7622c9`  
		Last Modified: Tue, 03 Dec 2024 11:51:42 GMT  
		Size: 7.4 KB (7377 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:28aa3b92afdeceb776855973c3b211c28230c89a81b458bb7e67b11d8cefe2e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144558793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afc5aee69b53785c60a0927a7b5c28ef293efdde6e25767537d489ed2d6e1d2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ef86bca2ffea293f73079f660a3399886008871df454d90312b7145d4395af98`  
		Last Modified: Tue, 03 Dec 2024 01:27:14 GMT  
		Size: 53.0 MB (52973420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183206547155d13d62e451041e3603fd7f5a0f4b1d6c8db0eaaf7ca1b4e51b07`  
		Last Modified: Tue, 03 Dec 2024 02:14:44 GMT  
		Size: 22.5 MB (22527751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8dd8a498f4405479d9e2bf04b4ed73d5dc63deb1d79c9d70eec7ddd7add1c35`  
		Last Modified: Tue, 03 Dec 2024 03:17:09 GMT  
		Size: 69.1 MB (69057622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d1de5a48dfe09b9f75e84d47faa561d68418835bb76363623eb981f370a7eeec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7668619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91810c997ab4ca1105aac3782040f194980cc9236686d98672c7a9c1b2c8411`

```dockerfile
```

-	Layers:
	-	`sha256:c5867b09adbc4524a9ca98728702a0177022b1afc0e4e8385d9a61636c8345ae`  
		Last Modified: Tue, 03 Dec 2024 03:17:07 GMT  
		Size: 7.7 MB (7661345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0640817c4ab08d0cfc6d0fb5beaa13797d1e7a88cd7885d6a37b80373ce2b256`  
		Last Modified: Tue, 03 Dec 2024 03:17:06 GMT  
		Size: 7.3 KB (7274 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:1fe95458c2a1597e474ab22eeab992b0dd3ca20270c9cb0ad29e34b758dc1365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.3 MB (139310939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3f05b1af333bd7a1d6548c97aa50a24c70ffe4d0dfb262d84bda07341eee6d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:547779e8d3d4ddde41b340ccc5c55eed6547696507cc0168eca950de620def24`  
		Last Modified: Tue, 03 Dec 2024 01:28:45 GMT  
		Size: 51.5 MB (51502465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fd17db4d55a0362abe181f4687b9308ab24eba56bf7c357aaf0150dda37b50`  
		Last Modified: Tue, 03 Dec 2024 15:47:12 GMT  
		Size: 21.7 MB (21747415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faad181192abe7945e2597dbe5a13adb7a6c4fc91c9cc8ed7907444e118bfa3f`  
		Last Modified: Tue, 03 Dec 2024 23:25:18 GMT  
		Size: 66.1 MB (66061059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5c8e5db01f6b4a196282e03ee3a072fdb6b0441419552c9108c75a93cc07190d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:602ee0707cc9c4d48ec4a571aec1a7a4f397e1c9249737bb9ec632733138fac7`

```dockerfile
```

-	Layers:
	-	`sha256:365963a85ceae17855bfd0702f9bc4c91835f90acdc457783db8dc5fb090e31f`  
		Last Modified: Tue, 03 Dec 2024 23:25:11 GMT  
		Size: 7.1 KB (7130 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:59a6796beeb3b9d0867665f4811ee1eee275a710e6a5a458dcc6fb93f8e48524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151265275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75fd8aab6398f04086341d332deb43da5a6cd1a16ef1b5a5e6dc0a987ef76111`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f96af90d82a1692028e6cdf912ac7419c2ecdd75603a19fc1f1b3b9e9bd29a53`  
		Last Modified: Tue, 03 Dec 2024 01:29:07 GMT  
		Size: 56.0 MB (55979543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5109fb930f5078004be0affb782c6af72db917a8e8c95675e33088c19131df3`  
		Last Modified: Tue, 03 Dec 2024 04:37:41 GMT  
		Size: 22.8 MB (22802436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77093ba8fdd419c4df155b02b29ff2686cd2a1d51168effbff5b4e39d31c96b6`  
		Last Modified: Tue, 03 Dec 2024 09:43:21 GMT  
		Size: 72.5 MB (72483296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5af9d705848c2dce3bc462b3b76df9b1b1d306e6bd09c2e26bd22bfc3f0c9876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f651af8b104ea346af37805901de2cc5ba97cf50ebaaa790cf0de9c570f5583f`

```dockerfile
```

-	Layers:
	-	`sha256:1db2caa964222e7b334c9d443db179aa27f6a7916d2932972cac65ad9c1e5d72`  
		Last Modified: Tue, 03 Dec 2024 09:43:19 GMT  
		Size: 7.7 MB (7673155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b523a122ad81c64df21fce3272cb02fca3d3a9206244cbe6d869788cadee4d0`  
		Last Modified: Tue, 03 Dec 2024 09:43:18 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:fc674a43ff201f8797f66dd82257b4196d80d7c095fc868cbe749cb36beeda09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137631430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f17059d9a1dcc6bf58ee32ba614a1fcbe226f8043520b842b184d3a9c6f28ff4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6a129056497962be3ca4efb9ff44f747d1222200200be5fae7999b10e3156cc0`  
		Last Modified: Tue, 03 Dec 2024 01:29:15 GMT  
		Size: 50.6 MB (50632627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d233c7b4fb57ebb3fc06e5b0c070fac8c8f89639814479f25441c1938943ba`  
		Last Modified: Tue, 03 Dec 2024 02:51:09 GMT  
		Size: 20.8 MB (20822777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f14784271331931f12f38e0de1c6c4183501776dd43b01c47876c85796c8558`  
		Last Modified: Tue, 03 Dec 2024 06:42:00 GMT  
		Size: 66.2 MB (66176026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fbd26b4002d80a7a7d2202c479c7daee401e8a0b0b2bc1e4e4d3dff743cc317f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7664095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79590c6ba7424ad6bb084619f4ed4331d5e05aaad65648779da965666f5b52e4`

```dockerfile
```

-	Layers:
	-	`sha256:ee9a4121ef32c4ac3a622baed8c3121fa68a4974fd0e3a4c5b2491d3285a4d59`  
		Last Modified: Tue, 03 Dec 2024 06:41:52 GMT  
		Size: 7.7 MB (7656766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8d83211651559187f1abcb4d829c94f914b0ee443046ecda9f19c4daaef0296`  
		Last Modified: Tue, 03 Dec 2024 06:41:50 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a6e7b7995a1caf452b3d1632d89a67fd503bce71d349a2d66b6b3489271ff30a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.9 MB (142907547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e646e8bc9897fc238aa02a1d8ac855f8561e8a87d9bf6b3034ff59ef5aafae4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5d3fd94703dd00b00c7acc09539942c89a4634b13c2ae0ee29086b6288d43a47`  
		Last Modified: Tue, 03 Dec 2024 01:29:01 GMT  
		Size: 52.1 MB (52083835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79c38d4fbdb1d980e95882f99ea9064cdd90b1c1070a263467e442acb813b03`  
		Last Modified: Tue, 03 Dec 2024 04:08:31 GMT  
		Size: 22.6 MB (22559777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1dd971e7560ef90c41327cadf96b46eeb95360bc6b43dff330bf117ebb3df64`  
		Last Modified: Tue, 03 Dec 2024 07:55:00 GMT  
		Size: 68.3 MB (68263935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:62bdb3d02e3a0d3e18eeefd51b090d298257bf08d95c74c779af75c028b32601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7679482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7371548547570d681cba1e2bec0c6958cf1f1b85b053244a30643706e814711`

```dockerfile
```

-	Layers:
	-	`sha256:baf8d91bd601ab293980e1fbe3335dc904de9a3306b89908c5075675c6676f3e`  
		Last Modified: Tue, 03 Dec 2024 07:54:58 GMT  
		Size: 7.7 MB (7672185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9961d929cf0d31cbf6d32963cbe3e25aedaa9b59f3f87385c96f28d64519dbf`  
		Last Modified: Tue, 03 Dec 2024 07:54:58 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:stable`

```console
$ docker pull buildpack-deps@sha256:08d61da2eb4b661e95088f6999704803985f9bd7be23b3c5d7acce26cd2d521b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:stable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d7d6286e853f4cad78b9bacc9962ed13b3fae93c940bc951a473bf59f7f1e406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.1 MB (348060715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fffceae85e2c8f384b15a112be85e0068e283d5c5a20b5b6569421c24c2d23f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd71677db44bb63b94de61b6f1f95d5540b4ba2d6a8a6bc4d19f422b25e0c2b`  
		Last Modified: Tue, 03 Dec 2024 02:28:49 GMT  
		Size: 23.9 MB (23865876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551df7f94f9c131f2fec0e8063142411365f0a1c88b935b9fac22be91af227e0`  
		Last Modified: Tue, 03 Dec 2024 03:17:14 GMT  
		Size: 64.4 MB (64391508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce82e98d553dd62ca6a12bebfe83992ae9f9ae2748275e74b66a68cc094f868b`  
		Last Modified: Tue, 03 Dec 2024 04:31:20 GMT  
		Size: 211.3 MB (211306121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:22a0e2166ec5a7010a99174c9c5a4b92eb963a4c9b850ffc869e3ae672a4dd19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15507109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e432f0cc69ae07b4e7a310d24f8c071f75c5c31a75f80f558a30a9de615e1d90`

```dockerfile
```

-	Layers:
	-	`sha256:28a6ec7885ff79f670b70218ace6d532c8d6d4ee96e883c5eea08d923c243220`  
		Last Modified: Tue, 03 Dec 2024 04:31:18 GMT  
		Size: 15.5 MB (15496569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4526bb391e6ae70edf822e4ae77d44dce58b597a0adf995d87ca2061831eafe0`  
		Last Modified: Tue, 03 Dec 2024 04:31:17 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:5493da36ae1be44ee45e6f2a21e8eb7a1651f02980e111eb4b77fcc9de0a28a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.2 MB (315162492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1431cc1ab0a9621e4af9c733d49b9b97de509516dcbcd2b4c7b5b24edab2124`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a8ab0b752e573ceb3480052f24bc5fe3f4f4665c13a338db39c1d51f749528e9`  
		Last Modified: Tue, 03 Dec 2024 01:27:04 GMT  
		Size: 46.0 MB (46024374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff6779451547ba3f0647f15a65068290fed53b6a4ac506257de98e02857bea6`  
		Last Modified: Tue, 03 Dec 2024 05:23:42 GMT  
		Size: 22.5 MB (22540382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536c3cdef529f6d2993cf137c109a079266cd3effbffc602a136a2a60ee743a0`  
		Last Modified: Tue, 03 Dec 2024 08:40:08 GMT  
		Size: 62.0 MB (61996814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f689132b2bca5271eb471905bd9f8eeca3a8c74df88b2f1c85f7c43568f20e7f`  
		Last Modified: Tue, 03 Dec 2024 10:05:05 GMT  
		Size: 184.6 MB (184600922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9c4417f2e99d2695ac62a5424fe36d0c44cca3243f219bea81261e45beaf3b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15305788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153481c7eaadccabe24fb8bb164c037031dfbfdd932085326ec034ee9a386d98`

```dockerfile
```

-	Layers:
	-	`sha256:5aa70f8227a7f0f719920d36ec18fa8bd67edfb3e40293ba3716fb81b5aef76b`  
		Last Modified: Tue, 03 Dec 2024 10:05:01 GMT  
		Size: 15.3 MB (15295180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b8c7629b4f7dd625175f4302ed859bd0ad93857f5dbca59a30b70d298562b4e`  
		Last Modified: Tue, 03 Dec 2024 10:05:00 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:437e11f7b48081f9d3169d3f0b57c19ccbf5d90f78824f50b59ee48d4e0d9fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300850185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1add49ced00435fc4e660bf2b8efd6d6f065f88334295c8dc979ad7f0ab8297f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4d43724a324f138c88a78ca6df0a39ab6868bf1f121eb974439c5a51284e1ac2`  
		Last Modified: Tue, 03 Dec 2024 01:27:59 GMT  
		Size: 44.2 MB (44200109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff0e53b92c3d0f5c370d71aeac1be1d23e475f1afba41d896ace0ff6eeefc90`  
		Last Modified: Tue, 03 Dec 2024 07:36:14 GMT  
		Size: 21.8 MB (21767161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9625bef464ab08848044651374e04f75d37ada02fe71387c3f9f83d0c9376c59`  
		Last Modified: Tue, 03 Dec 2024 17:15:53 GMT  
		Size: 59.6 MB (59641126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d83c079d9e82f91aeec2e9d84797bc47fa7f3b69f4094b837cbb4a9c25c5613`  
		Last Modified: Tue, 03 Dec 2024 20:03:34 GMT  
		Size: 175.2 MB (175241789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c37a07b310ce0346c0b105b93643ae7804934f50b5803137d2397fda42284ad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15311262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212be7441ad84dc59844b2e1479e05aaff0604670d910cd493e41a9ee0f3f9a6`

```dockerfile
```

-	Layers:
	-	`sha256:d6a56c836aa67f6706e6eacb06bc1edf226a862c6df77e58f7a17171c9494731`  
		Last Modified: Tue, 03 Dec 2024 20:03:30 GMT  
		Size: 15.3 MB (15300654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20d1d9165217046eef0f65fd0f02af670a48e312e840cc150c0713c8769cc7b5`  
		Last Modified: Tue, 03 Dec 2024 20:03:29 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:39b25cdea8a4133052cf8976d884cd9f4a28c36fc7ea1d200a82c3054510ff15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.8 MB (338766544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14cf9bca2791cef90a5b1313fb25c31438e4cf72dfec291fec9d3abfcc7b8674`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac722d9cf93b238dec2480278a2df5f8ccb672c97ec39f191191fd39f6721a8`  
		Last Modified: Tue, 03 Dec 2024 05:38:46 GMT  
		Size: 23.4 MB (23405813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261351ed796deb9fdad22dc734919eaf6726dd79a8dea99327d9e1376ecdcbce`  
		Last Modified: Tue, 03 Dec 2024 11:50:22 GMT  
		Size: 64.3 MB (64347852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d319298afc8bd728b8009e80320fe04e864fe92783eb06238a3b9f67dac7c3`  
		Last Modified: Tue, 03 Dec 2024 16:19:47 GMT  
		Size: 202.7 MB (202687199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d273ba454f05ac7b5489806499d16a8fc8ebf4171d5b07f144b245ce6d48a92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15535745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a83186039bd3ea2e021d2749e90f67f3e94a9e21027127ab2af7156513301e0`

```dockerfile
```

-	Layers:
	-	`sha256:578a4e71415013356a8cd37b5030e980c95edd8780c5a2f5a02a5d3585b92925`  
		Last Modified: Tue, 03 Dec 2024 16:19:42 GMT  
		Size: 15.5 MB (15525113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c493ff614776a1782e0bbac3137f383ef0eaad4fffed2bc981261fb4770db246`  
		Last Modified: Tue, 03 Dec 2024 16:19:42 GMT  
		Size: 10.6 KB (10632 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0ab7c71d79bd872a655352313f52121a6bcff2ffbac86045c95275339c23dd99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.6 MB (350616786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3ef764469eb7f8569265b9f9540132de83292a18992941d2995b96bcb6332e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:53769c348e57d646b1ec110dabf9d81a3f570afdb3b8216d1178515e4ea4ce1f`  
		Last Modified: Tue, 03 Dec 2024 01:27:09 GMT  
		Size: 49.5 MB (49476152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b0c73f75a815ce87bbf2841b694fdc4c29bcd072480b8752e8e91f0b59097b`  
		Last Modified: Tue, 03 Dec 2024 03:23:49 GMT  
		Size: 24.7 MB (24706896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2cf0351f309a0cf554972555b46b2ed97868d801e25eeed28a9f742a5e555c`  
		Last Modified: Tue, 03 Dec 2024 04:29:18 GMT  
		Size: 66.2 MB (66211191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adec659d61840fa9345456f332914b715e5d645a246d8ebd23b1c1c4b49b4996`  
		Last Modified: Tue, 03 Dec 2024 05:13:33 GMT  
		Size: 210.2 MB (210222547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:beeefbfff2ab941591ca7b91831c773ed391314b2de8511095bed0ee45cc98dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15485661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8bad9e7072ba65013bcf0c51e6857d3cbf652a07f0e5daa83e3d046e94995f`

```dockerfile
```

-	Layers:
	-	`sha256:87a64892961d327a139e2c8827b6f3f38d3383d5f173df4dfebfbfa09ef41385`  
		Last Modified: Tue, 03 Dec 2024 05:13:28 GMT  
		Size: 15.5 MB (15475148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e958a20d62bb83ee3421e3a3e2d16608731c94121983988380170f328b7e9f2c`  
		Last Modified: Tue, 03 Dec 2024 05:13:27 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:9a4df2f86567815e32dbc326f5e5710e33ae4f7e2c64c4ce81c28b6ee888b1ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325389432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3307c2bfac9eb9bd9ffeca8fbb60c761663449db1d61e6b4628d2dc291c3d8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8f7c3140f4f3af477253c748b229283137cca4214e1c3df21109b821f9227620`  
		Last Modified: Tue, 03 Dec 2024 01:27:53 GMT  
		Size: 48.8 MB (48771844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa54d74c5fddb1e648e0a4d95fcc8338f5800ff817646baaa9e6e65596d80c5a`  
		Last Modified: Tue, 03 Dec 2024 15:45:04 GMT  
		Size: 23.5 MB (23458105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a279e7254de3fa3935af4b6008753d14fcd8db605c58b83903cf8c5f880324cd`  
		Last Modified: Tue, 03 Dec 2024 23:22:12 GMT  
		Size: 63.3 MB (63283098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dffedca1364b4f303c66eee15c30c1fe70fb1db9416edf06602e694b41c50f8`  
		Last Modified: Wed, 04 Dec 2024 04:38:35 GMT  
		Size: 189.9 MB (189876385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0b9e0ac2a57702f5a76c6ff8a70e27672e95eabbe67a9141687c6917de5e0b46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aad0047efd61ce3266f344221ab7efa1e1390e8fa64a6831adff99b0275fcfb`

```dockerfile
```

-	Layers:
	-	`sha256:10d62b0e0d641ac025f308f802b13bf87690a2a5ecfbbc2f4f58a5d28559ba58`  
		Last Modified: Wed, 04 Dec 2024 04:38:18 GMT  
		Size: 10.4 KB (10382 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4ff5e7a9649060e6cec9389c3206397b83ccf21a3ef73f6da914d6a2b64f07fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.0 MB (362005295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f8e120cfb46d308aaefc2f3eb5e8f7580c23131f19cd4b52ef9a90bfce89cb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c84d784fe3c6c2bd95dea1c0d6eeba7c981bfb75bd53f81e83bcaadd87bba6f9`  
		Last Modified: Tue, 03 Dec 2024 01:28:03 GMT  
		Size: 52.3 MB (52328222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f0cfea13db30ebc69124696ada25182d1141398cd301a47a2cbf3c10d7fa9b`  
		Last Modified: Tue, 03 Dec 2024 04:36:57 GMT  
		Size: 25.5 MB (25523892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac73bc765d61ec6125ff5203c6c3d44543e6c3030684bfed0cb8f169640ae757`  
		Last Modified: Tue, 03 Dec 2024 09:41:44 GMT  
		Size: 69.8 MB (69812337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96099d400daf72e276203923fc855b1b1e5db81df04082e3505683bb398ec9ca`  
		Last Modified: Tue, 03 Dec 2024 16:12:55 GMT  
		Size: 214.3 MB (214340844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c38259992ff8adb65a540669780917a3ab0b4eb2a7bacfc0defc08aabe1954a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15483450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f228c3be5f23d0c8799c7a0da21c5bdc94a05195f09c48ab4f5756a9444da4d3`

```dockerfile
```

-	Layers:
	-	`sha256:4440c44dd5ab1d5632e5b9c675b3baff9156597169f4d38bade9241401960420`  
		Last Modified: Tue, 03 Dec 2024 16:12:35 GMT  
		Size: 15.5 MB (15472872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0489521282efca47f374796943fd138778aa10144bb693e59944fe88b32e855c`  
		Last Modified: Tue, 03 Dec 2024 16:12:31 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cea2ed2882f4bb7184acceea3fb0d08f2c273af35929de4d26ec1770b8329e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.8 MB (317814279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df084175632dd7bf0baf95424425d7b56f2dc329be6919e564076bfc0c0b66e7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:53a5c0dbd93a4a7f540e18bbe49ba3d7fadaa390ebbce009c756e34c5b1ae048`  
		Last Modified: Tue, 03 Dec 2024 01:27:55 GMT  
		Size: 47.1 MB (47149767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ded5bb0b377b736e6c5f45164fe8916ada3485441e963fe2fc0671949650049`  
		Last Modified: Tue, 03 Dec 2024 04:07:42 GMT  
		Size: 23.9 MB (23864625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b626037a925f80e453161d124c98cc5578e9d47f3f90a050168552e9727a34e`  
		Last Modified: Tue, 03 Dec 2024 07:53:40 GMT  
		Size: 63.5 MB (63473216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877241890f0b72dfe408c616ea9dde1f1c0afbbe3e7b91d9ceab73e7963ef0eb`  
		Last Modified: Tue, 03 Dec 2024 10:39:34 GMT  
		Size: 183.3 MB (183326671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ebbeeed93d90a07f2bf61c939dc6239ec6d8f6061e3eb49598381e313d2fb582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15319550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:017d6c05bd78e755bb45830a2c4afd3694c60f8b2019aa34942d6d1c91f3951b`

```dockerfile
```

-	Layers:
	-	`sha256:a14fcfe55eaddefca48b5c90a0ebb9e879a4899937c7f283124a5b4f9155e8fe`  
		Last Modified: Tue, 03 Dec 2024 10:39:31 GMT  
		Size: 15.3 MB (15309010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81a7f4e3bcc82457c7631f0aa274731bcc28c78bab41b2d89951556c508a2a32`  
		Last Modified: Tue, 03 Dec 2024 10:39:31 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:60fa59330635bb3360b021ffa0f96b1fbd61b19cf522290bf966f3bde25a9ca1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:stable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e4e69a8b7f9e04139295fb9dcdf37d823b148d1c112e36b0653d11ba96c6604e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72363086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d5ef6bc224b02787f00cbbce868ebbadc4fe38a2a978313291c878413ee721f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd71677db44bb63b94de61b6f1f95d5540b4ba2d6a8a6bc4d19f422b25e0c2b`  
		Last Modified: Tue, 03 Dec 2024 02:28:49 GMT  
		Size: 23.9 MB (23865876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7ff9434e13b1f41e3fdde66e19d17f3c35636e0cd182bf0bd4386e2af4124d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4371222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43bd9c68c9fe0a5c3db25a9086681f8f9c104c591606a18bea36b7dad3af97b7`

```dockerfile
```

-	Layers:
	-	`sha256:996b54fd1b681c68f21142e93f996d2ce61d3345a3aacb49c85c12238b4a15e3`  
		Last Modified: Tue, 03 Dec 2024 02:28:49 GMT  
		Size: 4.4 MB (4364058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aef3835c1fc0e6916ee36bb9b108d4e0947caab9bf621401475a88e457ab409d`  
		Last Modified: Tue, 03 Dec 2024 02:28:48 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9ca627c143143071812435f20a31d7ca4a98f8f69eb5772238d5ab4c289773e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68564756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d52aedd03a58bb0c09f5e307d64f49efd1f50d13619447fd27ad609070014374`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a8ab0b752e573ceb3480052f24bc5fe3f4f4665c13a338db39c1d51f749528e9`  
		Last Modified: Tue, 03 Dec 2024 01:27:04 GMT  
		Size: 46.0 MB (46024374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff6779451547ba3f0647f15a65068290fed53b6a4ac506257de98e02857bea6`  
		Last Modified: Tue, 03 Dec 2024 05:23:42 GMT  
		Size: 22.5 MB (22540382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2e2143039fd9074ac1c8fdaa9a11a3ffe40a93f547cf21b14da9b30f7dc7c54e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4374804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdf6d29be9af0b06c9bc426a0e4301f021a0d39b9c43f96faaf88c5fae8fdee9`

```dockerfile
```

-	Layers:
	-	`sha256:39e78f22f1d8edef86ca11b2156afabce6625a25d4fe1969f2b9b7fe1e12e885`  
		Last Modified: Tue, 03 Dec 2024 05:23:42 GMT  
		Size: 4.4 MB (4367573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0f81f00ceef9b327ef81f33ce0ac9ef30236b95c3793935d843dbbae8791bbf`  
		Last Modified: Tue, 03 Dec 2024 05:23:41 GMT  
		Size: 7.2 KB (7231 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3117bcbd993e3753ba7f62fed2092e261302219fc4794bd60744b540753d2b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (65967270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae811cf19b5c01de9b3482a0673dadcd8b1b0567a12e943446c319bddbadee9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4d43724a324f138c88a78ca6df0a39ab6868bf1f121eb974439c5a51284e1ac2`  
		Last Modified: Tue, 03 Dec 2024 01:27:59 GMT  
		Size: 44.2 MB (44200109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff0e53b92c3d0f5c370d71aeac1be1d23e475f1afba41d896ace0ff6eeefc90`  
		Last Modified: Tue, 03 Dec 2024 07:36:14 GMT  
		Size: 21.8 MB (21767161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8bbb04311c4caa959ede4991344d0b4395a37e8c603b0c5b9755e7d0ac6b02bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4373586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2806b2b8fd080b94514ac3e7a4280190841cecba2a389c4572f92b9ad6b4352a`

```dockerfile
```

-	Layers:
	-	`sha256:9457386cd8923d16e0e33114929e464cb25582e303b69193cdfeb4b31b7ddf7b`  
		Last Modified: Tue, 03 Dec 2024 07:36:13 GMT  
		Size: 4.4 MB (4366354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dde010eb4616c79d3ca142e42b4cc8fb81c4de83e8cde4e7c18080b5fe8d6b0`  
		Last Modified: Tue, 03 Dec 2024 07:36:13 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:757ecd28399473cce91e6be523aec8e79ca9f576cfed067466bcffa71ff9ac70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71731493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed0620fbee6bbd337320d030c3be4e71b8e2883828902bf89672a74d1a36278b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac722d9cf93b238dec2480278a2df5f8ccb672c97ec39f191191fd39f6721a8`  
		Last Modified: Tue, 03 Dec 2024 05:38:46 GMT  
		Size: 23.4 MB (23405813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:79739c087c54ec0d652199829c30eaba59e426e5edf317a72b3a318dd0cd8bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4371586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc692a177ab4525e660f0d3f47205fd6ed2ad3a54e419ff10a28b6e48bc78535`

```dockerfile
```

-	Layers:
	-	`sha256:4816aacc299c61ab88c4e10c38abd2b3d51afb73adba3b8bb1debfd6846287a1`  
		Last Modified: Tue, 03 Dec 2024 05:38:46 GMT  
		Size: 4.4 MB (4364330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:913b8b80c5fa22b390e28ca34404e62e7d38090c8e99339fc5cdde2cf477b4ed`  
		Last Modified: Tue, 03 Dec 2024 05:38:45 GMT  
		Size: 7.3 KB (7256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5ddf951a80c7dec860666e1ff917ced4535353326c546dab88edcbab700e2345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74183048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:129a653e602a0fe253a2b069b2e2ab67f1ea9115e2fd72cc3ced51c193a26a5f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:53769c348e57d646b1ec110dabf9d81a3f570afdb3b8216d1178515e4ea4ce1f`  
		Last Modified: Tue, 03 Dec 2024 01:27:09 GMT  
		Size: 49.5 MB (49476152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b0c73f75a815ce87bbf2841b694fdc4c29bcd072480b8752e8e91f0b59097b`  
		Last Modified: Tue, 03 Dec 2024 03:23:49 GMT  
		Size: 24.7 MB (24706896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:eebaeeda8054688d6fd8c142a0fc0a9ccfa4fc3ca2b3499bfe916319c4994ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4368251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8937659e583da0ff6a76c8f743b3e42f34bd06dbbe6d065e151fb9bfada42aa`

```dockerfile
```

-	Layers:
	-	`sha256:729bb902df2997852a31087017dd8b75ede98123a831591b1b48e5519566d1b0`  
		Last Modified: Tue, 03 Dec 2024 03:23:48 GMT  
		Size: 4.4 MB (4361114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:310a36eb7785ee15a990c5d5843eb5ce31f673057b5dd6940687e2392aafaffb`  
		Last Modified: Tue, 03 Dec 2024 03:23:48 GMT  
		Size: 7.1 KB (7137 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:7ae289bc030a4b5e312465d3e015385f878f438f21b1723c31ae05301d012675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72229949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f8bd8c5b5ea753d9188c3db86b7f053f010d9de2a9dd1dfceb0a49d52a4d4c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8f7c3140f4f3af477253c748b229283137cca4214e1c3df21109b821f9227620`  
		Last Modified: Tue, 03 Dec 2024 01:27:53 GMT  
		Size: 48.8 MB (48771844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa54d74c5fddb1e648e0a4d95fcc8338f5800ff817646baaa9e6e65596d80c5a`  
		Last Modified: Tue, 03 Dec 2024 15:45:04 GMT  
		Size: 23.5 MB (23458105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0f04f4b64d87c286d8281dc28e82e764fcf2429c6f431b927f4f2b1b0e2e1b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 KB (7005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df656bed5425ba40a59f661b24a9ef00be8b445ae9820ef34b56825c81995052`

```dockerfile
```

-	Layers:
	-	`sha256:9973e5e44c5c8a102b2079d03531741e8919c0d04a2f710f280f74d5169fe092`  
		Last Modified: Tue, 03 Dec 2024 15:45:01 GMT  
		Size: 7.0 KB (7005 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:989e244c7923bf0590fb8ddd1cfda40228425477aed2564c4f1d68d5bf4c1211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77852114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9269507941157f6d8c2a6aaf7d982955bbd6ad996a59aa0c335382fa56fedbf3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c84d784fe3c6c2bd95dea1c0d6eeba7c981bfb75bd53f81e83bcaadd87bba6f9`  
		Last Modified: Tue, 03 Dec 2024 01:28:03 GMT  
		Size: 52.3 MB (52328222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f0cfea13db30ebc69124696ada25182d1141398cd301a47a2cbf3c10d7fa9b`  
		Last Modified: Tue, 03 Dec 2024 04:36:57 GMT  
		Size: 25.5 MB (25523892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a45e69e0d085a116675b75a7b725f816d6446a3fb4ca0543c48e95c3f3fd3978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4375753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e3cdc76dad87b7234f6f31c723d08c241a2a7efa8c9039144506f957faabb9`

```dockerfile
```

-	Layers:
	-	`sha256:238d77a8b35e0e5b35ee3bdf19e0102de9c1fb1aa37b9dbc272bed8d60d9852c`  
		Last Modified: Tue, 03 Dec 2024 04:36:57 GMT  
		Size: 4.4 MB (4368551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec9892333b13de0bc61e2cdc3ecce83c24ed20bb5579e82cfaa2d4bbcfb85f33`  
		Last Modified: Tue, 03 Dec 2024 04:36:56 GMT  
		Size: 7.2 KB (7202 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a0a6eb40a58c78dab49f2a7fbb55665c1a2af22ac7a1ac77580e07074365ec0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71014392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68d8461201f6697d48a6322c9ab07b91a4490ee92e53b559914223bb89b0a6c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:53a5c0dbd93a4a7f540e18bbe49ba3d7fadaa390ebbce009c756e34c5b1ae048`  
		Last Modified: Tue, 03 Dec 2024 01:27:55 GMT  
		Size: 47.1 MB (47149767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ded5bb0b377b736e6c5f45164fe8916ada3485441e963fe2fc0671949650049`  
		Last Modified: Tue, 03 Dec 2024 04:07:42 GMT  
		Size: 23.9 MB (23864625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bae73931459a569e6aa2c77e5721402acdd0fa87c8499ac00c378f09da2b74e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4370919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb35bd02c831221f27c85d64464a87ff1e458b43c43e1a167b9614f44689a992`

```dockerfile
```

-	Layers:
	-	`sha256:9c310eee549867fde8b1fd56ec371ef6cbb8f19c03df6ec7b8c6a49b4dcd0703`  
		Last Modified: Tue, 03 Dec 2024 04:07:42 GMT  
		Size: 4.4 MB (4363755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e932d932ad0e9d02444cefa5146dd7acdbe99b89f0389f686355c2b3271a1eea`  
		Last Modified: Tue, 03 Dec 2024 04:07:41 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:stable-scm`

```console
$ docker pull buildpack-deps@sha256:9cb2ad7d26df8c138d5932843e460988b87f61ac5346721a3d1ad60c6d8a41d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:stable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:081b378225dd3efe7d85a0720370cbfd29b95001f7a0fb7073af54694ac974b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.8 MB (136754594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf470aba1a92d0771a65417e8a1beca6b311c9d18bcc12eb965032af2ee32b8a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd71677db44bb63b94de61b6f1f95d5540b4ba2d6a8a6bc4d19f422b25e0c2b`  
		Last Modified: Tue, 03 Dec 2024 02:28:49 GMT  
		Size: 23.9 MB (23865876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551df7f94f9c131f2fec0e8063142411365f0a1c88b935b9fac22be91af227e0`  
		Last Modified: Tue, 03 Dec 2024 03:17:14 GMT  
		Size: 64.4 MB (64391508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:20e125aea8586458a38f6d6b5fc4e799b157c40f6827bcdeede53d9deae5face
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7770849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed90e1697fb72676df77dcda5236274c90f61c17282ceccfc72e15b82f41da6`

```dockerfile
```

-	Layers:
	-	`sha256:012f88be9d04d99db39c2e75975d319894fe143e2f1d2c6b22032f733dc8c9a2`  
		Last Modified: Tue, 03 Dec 2024 03:17:12 GMT  
		Size: 7.8 MB (7763194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffa6b104b3f4a17660de0197b48ec8fbd2132b50b103011b72bafd123a894939`  
		Last Modified: Tue, 03 Dec 2024 03:17:12 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9b05d826a9aea2d34ea09a27fa55a3c9149103ac03323af230c8d2fcbcc8c5b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130561570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220e7a63ad00370b6e1c4651783b941fd094c6d2f66623cc356f07353ced08c9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a8ab0b752e573ceb3480052f24bc5fe3f4f4665c13a338db39c1d51f749528e9`  
		Last Modified: Tue, 03 Dec 2024 01:27:04 GMT  
		Size: 46.0 MB (46024374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff6779451547ba3f0647f15a65068290fed53b6a4ac506257de98e02857bea6`  
		Last Modified: Tue, 03 Dec 2024 05:23:42 GMT  
		Size: 22.5 MB (22540382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536c3cdef529f6d2993cf137c109a079266cd3effbffc602a136a2a60ee743a0`  
		Last Modified: Tue, 03 Dec 2024 08:40:08 GMT  
		Size: 62.0 MB (61996814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ba33181894b95455834717fb83a3cab2650b256f61a539f7419fc4f2e9c101c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7772471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49b76ea2636dae7de0703b48ca2f666e83f0a87977aff0a7884206898bf9654`

```dockerfile
```

-	Layers:
	-	`sha256:7b65f3800eb2add9f15ccf14f61be70696d82161b63f30b569972b0c8bd6a72e`  
		Last Modified: Tue, 03 Dec 2024 08:40:07 GMT  
		Size: 7.8 MB (7764748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4172764014ee95b8731a943cfba1e0f4e0e07007f8a4395720c1e0f1339fcccc`  
		Last Modified: Tue, 03 Dec 2024 08:40:06 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:390b0a015b9c6bd4a91717ab50b2da649b0e953291c1f6f179ac799ef34e25dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125608396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e6c420c1f7fb64fa485887316c939461f82ec6dbdf0ccd26e9a5970807dbee`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4d43724a324f138c88a78ca6df0a39ab6868bf1f121eb974439c5a51284e1ac2`  
		Last Modified: Tue, 03 Dec 2024 01:27:59 GMT  
		Size: 44.2 MB (44200109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff0e53b92c3d0f5c370d71aeac1be1d23e475f1afba41d896ace0ff6eeefc90`  
		Last Modified: Tue, 03 Dec 2024 07:36:14 GMT  
		Size: 21.8 MB (21767161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9625bef464ab08848044651374e04f75d37ada02fe71387c3f9f83d0c9376c59`  
		Last Modified: Tue, 03 Dec 2024 17:15:53 GMT  
		Size: 59.6 MB (59641126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:97cad46bffd054d5464b24f3898b89857a83b9327bd544db3f756fe68e8e5eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7772198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a53c50a14cb4d17416ad8c2b9f6ae29f07e4a2b9360068459000d153cbfa28`

```dockerfile
```

-	Layers:
	-	`sha256:98bbc215633288506c1cd937a4043acf7e3f2d79ced4e6d1b78fb36f63f12c90`  
		Last Modified: Tue, 03 Dec 2024 17:15:52 GMT  
		Size: 7.8 MB (7764475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4b268dda7212f4c955489072ec118680aa47218128cabc0b36f57ab7211081a`  
		Last Modified: Tue, 03 Dec 2024 17:15:51 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4b4fd9f631b9294a9c2600d58e03ea6aabe8064c9023517e3c004147a248c706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136079345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:294a87bc6560e0bb4acbf480b18930ca99a2863c50d4817579003ad59c8dcf5b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac722d9cf93b238dec2480278a2df5f8ccb672c97ec39f191191fd39f6721a8`  
		Last Modified: Tue, 03 Dec 2024 05:38:46 GMT  
		Size: 23.4 MB (23405813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261351ed796deb9fdad22dc734919eaf6726dd79a8dea99327d9e1376ecdcbce`  
		Last Modified: Tue, 03 Dec 2024 11:50:22 GMT  
		Size: 64.3 MB (64347852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:296b38d3b5682f620d8d350576747bedddd836671036ca931158e5fcc0abeba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7777352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6feeb02a68d010871c1233be105b538ae59e9b1d4fc972aaf364445fbcb678bd`

```dockerfile
```

-	Layers:
	-	`sha256:52070a7e355cffc4a9d0da8f0dc19e32ab40a808d402a964b8802456ba6e889f`  
		Last Modified: Tue, 03 Dec 2024 11:50:20 GMT  
		Size: 7.8 MB (7769605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:559dec8b2f1952ab63dd3ad11af3f0cab12b2904ee9ac16805ff6743224ac486`  
		Last Modified: Tue, 03 Dec 2024 11:50:19 GMT  
		Size: 7.7 KB (7747 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:efadcac373fc964d9e687e3c3acd546ed1243f3de78c4dfaa3cab0c1c44164bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140394239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c6c2127f1e3c3cff2f2545cac8268fc28d1eca7e5f18ebd9811301efedbc12`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:53769c348e57d646b1ec110dabf9d81a3f570afdb3b8216d1178515e4ea4ce1f`  
		Last Modified: Tue, 03 Dec 2024 01:27:09 GMT  
		Size: 49.5 MB (49476152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b0c73f75a815ce87bbf2841b694fdc4c29bcd072480b8752e8e91f0b59097b`  
		Last Modified: Tue, 03 Dec 2024 03:23:49 GMT  
		Size: 24.7 MB (24706896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2cf0351f309a0cf554972555b46b2ed97868d801e25eeed28a9f742a5e555c`  
		Last Modified: Tue, 03 Dec 2024 04:29:18 GMT  
		Size: 66.2 MB (66211191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:90045c81ec640293d6faa0394f96a1a985df7ff3d81fada2cfde8db780172edb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7766897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e344e02c870074180a5c7834575f4d8030d1e8969592d6bfa37194677c4d8bf3`

```dockerfile
```

-	Layers:
	-	`sha256:9855bce4e2e113f8c216ac6ecdad8a6af90932e14bc9bf28815c4fa67b760275`  
		Last Modified: Tue, 03 Dec 2024 04:29:16 GMT  
		Size: 7.8 MB (7759270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:487dfc9a24b2a2d5a2e18670b6601e6e1927433744a4d83a1dd8813646329b52`  
		Last Modified: Tue, 03 Dec 2024 04:29:16 GMT  
		Size: 7.6 KB (7627 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8915c51839fedacb07adb7002f8c190c948a12fcb503b7696ffc03b6a1b61ce2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135513047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbc8ce69146cef10089880f0995e0f8904567b5f315696d227d654aea381c65`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8f7c3140f4f3af477253c748b229283137cca4214e1c3df21109b821f9227620`  
		Last Modified: Tue, 03 Dec 2024 01:27:53 GMT  
		Size: 48.8 MB (48771844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa54d74c5fddb1e648e0a4d95fcc8338f5800ff817646baaa9e6e65596d80c5a`  
		Last Modified: Tue, 03 Dec 2024 15:45:04 GMT  
		Size: 23.5 MB (23458105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a279e7254de3fa3935af4b6008753d14fcd8db605c58b83903cf8c5f880324cd`  
		Last Modified: Tue, 03 Dec 2024 23:22:12 GMT  
		Size: 63.3 MB (63283098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1c84b11a183c60766b72298df7807d4c7092c9c2f73f1d21017e277fc9ab23ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a1f59aac2c22a1238dc51a66bd9dce102857527b4849511e58dc50dac965a0`

```dockerfile
```

-	Layers:
	-	`sha256:20ab0e5caa843ee96726eb9c38d13c80976c82e15ba6ba6202d3e1ba959cd413`  
		Last Modified: Tue, 03 Dec 2024 23:22:05 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f41ac76702c18986d7791e88468e69b4dc78c623d28e1a490e6c0cbbfc6b1082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147664451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514cb07cf8569c7b8531ad437622c499eedef341c3f377fe235d298f7e8ac991`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c84d784fe3c6c2bd95dea1c0d6eeba7c981bfb75bd53f81e83bcaadd87bba6f9`  
		Last Modified: Tue, 03 Dec 2024 01:28:03 GMT  
		Size: 52.3 MB (52328222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f0cfea13db30ebc69124696ada25182d1141398cd301a47a2cbf3c10d7fa9b`  
		Last Modified: Tue, 03 Dec 2024 04:36:57 GMT  
		Size: 25.5 MB (25523892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac73bc765d61ec6125ff5203c6c3d44543e6c3030684bfed0cb8f169640ae757`  
		Last Modified: Tue, 03 Dec 2024 09:41:44 GMT  
		Size: 69.8 MB (69812337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2a89a02d7b0a3fc01937338322a3adbfec4f8acf6ca3ccbf611a6bfea596fec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7778593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296a47c62b0745a03c2b02e5a3f2df0ebe6f985dc10f4132e1e9b9ea44ffc350`

```dockerfile
```

-	Layers:
	-	`sha256:4b033dd73e35183deec51e3e2b0975d4838f1627c9589d8d0a263fdb61430e94`  
		Last Modified: Tue, 03 Dec 2024 09:41:42 GMT  
		Size: 7.8 MB (7770901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1815558343ccce9363e7d65977e06bb87d6b20878e7dfbcffc07133ed7dee487`  
		Last Modified: Tue, 03 Dec 2024 09:41:41 GMT  
		Size: 7.7 KB (7692 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3b238b3a7258d279b52146096b4beb7f45782123399ba1107028fffcda72845a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134487608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55812b2c5a9e20ae6c6e47ae8abb5ecd135751de9755ada12406aef2a0ded189`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:53a5c0dbd93a4a7f540e18bbe49ba3d7fadaa390ebbce009c756e34c5b1ae048`  
		Last Modified: Tue, 03 Dec 2024 01:27:55 GMT  
		Size: 47.1 MB (47149767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ded5bb0b377b736e6c5f45164fe8916ada3485441e963fe2fc0671949650049`  
		Last Modified: Tue, 03 Dec 2024 04:07:42 GMT  
		Size: 23.9 MB (23864625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b626037a925f80e453161d124c98cc5578e9d47f3f90a050168552e9727a34e`  
		Last Modified: Tue, 03 Dec 2024 07:53:40 GMT  
		Size: 63.5 MB (63473216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2006631c59dc1f6d83026dc68c6f3367d6c4a1954eaaa7c817120bfb69572ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7770055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9c6b8467b7d857fa1c079d9b3e0091c74f5fa80c8cc76afe7c7a05ea96e216`

```dockerfile
```

-	Layers:
	-	`sha256:fcf08fd6e06e7a3eb093b7470b9f4abc277ecb5601672f6d97c6e6712c678832`  
		Last Modified: Tue, 03 Dec 2024 07:53:39 GMT  
		Size: 7.8 MB (7762400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f3eab35b34c262dbc9b817602d68d99ea2c9634756836744ea2d6a546474acd`  
		Last Modified: Tue, 03 Dec 2024 07:53:39 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:dc94202ffb172b4ed42f494065683069f8f248c4becc329362cb8ad4f0ba6cc7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:testing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:ed757090c92b4dfba07b522d16daa7c7356e9a37794b71fd2cfc716b5f00df72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.2 MB (375207066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b1c36fa0c38ceed250a0a4e36aac2b80e6c07f522cff8eb8077ebfb6142e86`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e4743b5a77e386ff2c8b73b5f4786349b4c3b4a5bba77f60a49c3b94a3b29584`  
		Last Modified: Tue, 03 Dec 2024 01:27:30 GMT  
		Size: 52.1 MB (52113554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4547041a33b6c57d94bf3840b901ad1987b2672b67b1e68ff564d9703716a01`  
		Last Modified: Tue, 03 Dec 2024 02:29:17 GMT  
		Size: 20.6 MB (20599021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46b5387da4a2f31c146885e44d705069d7906eee138ab3588a9fee7bcae723e`  
		Last Modified: Tue, 03 Dec 2024 03:17:15 GMT  
		Size: 67.1 MB (67058436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba00f95a0fc91aa5af7f7128d1d9cb3461821c06ee197cedb64680239a9330fc`  
		Last Modified: Tue, 03 Dec 2024 04:32:21 GMT  
		Size: 235.4 MB (235436055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b9c8f539ce39e7b8310b4aa26beaf75d8b1c786c599118c0d371f9c05b88a7b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16974493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:499c1f23296ed70dd90fa678b5fffbcc3db5cdd0ba780ad4d8af8c81152bb1ba`

```dockerfile
```

-	Layers:
	-	`sha256:aeba652bd408371681685be2385bf3915a6ad86227cff4372d75fbd81cf44cf1`  
		Last Modified: Tue, 03 Dec 2024 04:32:17 GMT  
		Size: 17.0 MB (16964300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5d83ffd4c714db14b14c9bbfae084789a2ff936e4b23cf8b86d02f09a72ec0a`  
		Last Modified: Tue, 03 Dec 2024 04:32:17 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c636e9375ce9ccdf6de8efa6e3d973ffdce8751197773590d30484535124384a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.5 MB (338494634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:460619e39697127cad08ce61ca20ce2c9b6925d9fa694376134c3c7eac13d236`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5bc3ae687a9226ba4c006ebae837bdf4fc9ce21a92c2280c2fe34aaa801bc170`  
		Last Modified: Tue, 03 Dec 2024 01:29:30 GMT  
		Size: 48.7 MB (48667592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f104f4b59037c21344a76456c37d0109c126d6df42220396b04d3aaad3cdf4`  
		Last Modified: Tue, 03 Dec 2024 05:25:08 GMT  
		Size: 19.6 MB (19608590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b47bb9243d7017922dcc62de48c63d8cfb54c3c1e685c3e38d7cea429218c0e`  
		Last Modified: Tue, 03 Dec 2024 08:42:18 GMT  
		Size: 64.4 MB (64402187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0d6acc584d696ab456ac89386f5313fd7dbb30f7a4ea1f0fc6fa6832d72040`  
		Last Modified: Tue, 03 Dec 2024 10:11:48 GMT  
		Size: 205.8 MB (205816265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f530a531eb2590391f82e8e4cf42b9419b8e54b1381e532255b22150fa621551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16735915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d32ec904a4b93001545f14f059e71cb6ae5158832bee02312bbec5e06e5313f`

```dockerfile
```

-	Layers:
	-	`sha256:f53e2672493aee51835e2d7b671b1b06b1e16d7bd8ebfcf18e7f433cc21ce3de`  
		Last Modified: Tue, 03 Dec 2024 10:11:44 GMT  
		Size: 16.7 MB (16725662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d755ff4cd7ec164c2eea1f946a539eb3f3b3245d9a12843366600c388e0af987`  
		Last Modified: Tue, 03 Dec 2024 10:11:43 GMT  
		Size: 10.3 KB (10253 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c54092137aef82673b628701fffae1d7bb5cdee16036652cf8c5680b2311507d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.6 MB (320566678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd69e8784e9a9a24c7018a57f98312596b243e702223ff357301ebb75ff9f02a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:20c73c374f639d431be81d6bb3157ee925cb0c99f0451d2cd165921c444373d3`  
		Last Modified: Tue, 03 Dec 2024 01:31:30 GMT  
		Size: 46.7 MB (46679645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c705f22774d3593ddb8b7b982bc9e82a21362788a9fdc05272e21016ed52debc`  
		Last Modified: Tue, 03 Dec 2024 07:38:00 GMT  
		Size: 18.9 MB (18944460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a431a228225acac55e8846f5426c9cadb4b56af6577e4fc2e206ee3b42a287`  
		Last Modified: Tue, 03 Dec 2024 17:18:35 GMT  
		Size: 61.9 MB (61898433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2250e50c3b0d1679c6a6f0905a6bb14cdf995965365d96a0ed0af0a1cabeda41`  
		Last Modified: Tue, 03 Dec 2024 20:11:47 GMT  
		Size: 193.0 MB (193044140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3f0d17f8af67e79adb9ba470f17c5f6f7b4423ebee7b062e14e0213e7ddd14ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16741713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20fbf3a659f9762253c3305e4a0dcd4ebf822c59152a12c4d414fb236c480a1c`

```dockerfile
```

-	Layers:
	-	`sha256:021ec9171dbfc19c071bd17673d2e89c9aa2b95717e117707175c7f3598da4f0`  
		Last Modified: Tue, 03 Dec 2024 20:11:42 GMT  
		Size: 16.7 MB (16731460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e86dd2f315ea5820a2680250233eb394bd4e588be2acb1a7a10b9232f138f95`  
		Last Modified: Tue, 03 Dec 2024 20:11:42 GMT  
		Size: 10.3 KB (10253 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:37a190a761023c4e140ccf9149b71929db84f08fec40f69f81803e339f665a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.5 MB (366490575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdbec0ffdb40aa93cc2227f7e64678ce9711e69280737c2d9d4a8a2a696b515e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9eb21918436f171705acc6e3469286cf27466cc89ea0d17c1699761c888e169c`  
		Last Modified: Tue, 03 Dec 2024 01:32:46 GMT  
		Size: 52.3 MB (52340851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937167b9612f87af0bddfb5d6d68eeee5ceeb8c8e8837f1f9918d7f613aa06c4`  
		Last Modified: Tue, 03 Dec 2024 05:40:08 GMT  
		Size: 20.3 MB (20251872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5eb80243bfd344e12541595272ea8f33faae6f5a77fc26a37baef8d6c8ea36`  
		Last Modified: Tue, 03 Dec 2024 11:52:25 GMT  
		Size: 67.1 MB (67107203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be95ee2ae477988acf1c4f6dcfc88e1ae5a55fd73cb1208a350d7951447cd5c2`  
		Last Modified: Tue, 03 Dec 2024 16:25:24 GMT  
		Size: 226.8 MB (226790649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b69fd275d0a8e244814ebfebaa3277de3c5c799239fc1179eeb59b49cff6bb8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17061306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d61e81a066f2bf03ec9ede670c559770001733b72dccaee56894ce1afe09a2`

```dockerfile
```

-	Layers:
	-	`sha256:10fd39fd24a909e9e91ac353e116e838d10121424f2fb2dd2eb94b5253aef4c7`  
		Last Modified: Tue, 03 Dec 2024 16:25:20 GMT  
		Size: 17.1 MB (17051033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:781c922e20f55229b5dc779d96f6a85737b2f5c7ab8068980abbb055be1f8609`  
		Last Modified: Tue, 03 Dec 2024 16:25:19 GMT  
		Size: 10.3 KB (10273 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b1e1cdc198e59acb495d0927ea674cff22326dfa3019424fb0a344a66225ca12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.2 MB (383151595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107ab0c39dc78b9e57ebf91be11e68f4bfea2c3c8274b2817e739d1abd96b2cb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1a5aa91e83fa5cc5d15dce96bbfdc6d2483a659fdee76a341522b60ff87dc849`  
		Last Modified: Tue, 03 Dec 2024 01:27:32 GMT  
		Size: 53.0 MB (52956284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79565d36fc8ccc76d07975f07b5cf916b84627952cb6785e10e8d0301cc2acdd`  
		Last Modified: Tue, 03 Dec 2024 02:14:48 GMT  
		Size: 21.7 MB (21726798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad782586fddb10041571d568c827bae913dd109647631cce2fe893ecfe4b9488`  
		Last Modified: Tue, 03 Dec 2024 03:17:11 GMT  
		Size: 68.9 MB (68861394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e0699983953a7cec342f58306a547a993dc86fcdd09293e817b3e01512494b`  
		Last Modified: Tue, 03 Dec 2024 04:32:37 GMT  
		Size: 239.6 MB (239607119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:de2d63fd3a08165ba0533d04f1b6b235cf235ac4d014dea6d58b91bc768784f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16944039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835d1e208a7980646971042bf95ed3c919253fb965855df2f98f7c5d3284d1dd`

```dockerfile
```

-	Layers:
	-	`sha256:d0cb59f5654fc36e2048aa3b18128bf0764b4cba7b7276d4734c553f6b495f85`  
		Last Modified: Tue, 03 Dec 2024 04:32:32 GMT  
		Size: 16.9 MB (16933868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bea586dcbbe73941b9db0060e0fb5b46aa2e20eeb654f2758421e9b06508583`  
		Last Modified: Tue, 03 Dec 2024 04:32:32 GMT  
		Size: 10.2 KB (10171 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:6aed94b346224a907374352ffe52a244f6fb845bb6fa77af0dbf33caabf6b925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.5 MB (349523155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c8a6f92b61aee8dc5319671b6c4838f2c5cc076f392dd5e5a5ed52f09243017`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e5a8d7ead1bc1f754b3a65ff28bee76dc2dc6179a698bf1402b64ec3d987e4e2`  
		Last Modified: Tue, 03 Dec 2024 01:30:45 GMT  
		Size: 51.4 MB (51439925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6d7c128c8894ab5647ca7070a8c53cc1626367f0fee2913a8ce5fe2237ac2e`  
		Last Modified: Tue, 03 Dec 2024 15:48:58 GMT  
		Size: 21.0 MB (20951581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddd6435addf48f219bf6a9a7272ed63c493377979c37d721428b6d2c65dab1f`  
		Last Modified: Tue, 03 Dec 2024 23:28:11 GMT  
		Size: 65.9 MB (65912927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982cc02c1e97f3987f1a40bace25f4f97248212c53b960fbe66ac9c773ce7ca2`  
		Last Modified: Wed, 04 Dec 2024 04:58:21 GMT  
		Size: 211.2 MB (211218722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:62a3dabe91f7108ef0c06eb9b6acea0b172d897697c9160cdbcb678f3da17ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3266f96a84806158d2d80e622846075de301f496c29d3f3045aa367a97adb73`

```dockerfile
```

-	Layers:
	-	`sha256:daa5a4b1199b129238891d666d4691b1ba0ccaa01bbdc77033f58a0747a4a008`  
		Last Modified: Wed, 04 Dec 2024 04:58:02 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6664a3df9dc9bec277c19ee01729befd3ce661e183f2a0d86777890babc7a779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.6 MB (382552567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6645f0cf430b3644a88d2853e79a959d668b36a2196104d494e19ca8ee0e1e67`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5e74ce1d603959ee7e791ff530dd1c46ce3dbdbf2d00f3d3917cd370d2c2ca56`  
		Last Modified: Tue, 03 Dec 2024 01:31:51 GMT  
		Size: 56.0 MB (55955673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e3c1d8feca2b36465cdfb5b57d9969f0fb66fe43bf079a81607bc309440b99`  
		Last Modified: Tue, 03 Dec 2024 04:38:34 GMT  
		Size: 22.0 MB (21990810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f35d27e17f5faa7b717fcd51d2689cc9f5f0b57184433a4eae97a42f95da04f`  
		Last Modified: Tue, 03 Dec 2024 09:44:41 GMT  
		Size: 72.5 MB (72470223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52a720b71dddcb2a25df1c62f4df5be637ee1b44f6c72e886501e695c3e8491`  
		Last Modified: Tue, 03 Dec 2024 16:21:25 GMT  
		Size: 232.1 MB (232135861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:46c273b1c0cfbdacdd361fa947c0ae293856b1182058b608e17adb484abd5c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16956784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a972b3130f5c0e09be05cbf098c2fe9f102fb226330c6a9f77a9e59b4e34ab07`

```dockerfile
```

-	Layers:
	-	`sha256:a680bd893b317b1e20138c7cae82c062fd4718a73928c1fe154c9a60ac52e652`  
		Last Modified: Tue, 03 Dec 2024 16:21:19 GMT  
		Size: 16.9 MB (16946559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3348c230fc094aec79e85591b44365b40fe471dceb5ef063384a1515e5721ca6`  
		Last Modified: Tue, 03 Dec 2024 16:21:19 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:59ba1941b5338aeec3a0cfa33e35cbf7a6634dbab19b243d5e1f2ad7ec4edf98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.1 MB (348067149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6efa8ee7b2b6de06d44ececdfdcf93f69002163b468f5578a592d090d370e3f8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:33a597a4ae2eff9c605f460e3e4517cc31e0999c816baef2a6ee6ab3da5c61ec`  
		Last Modified: Tue, 03 Dec 2024 01:31:39 GMT  
		Size: 52.1 MB (52069406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3f8d29d82faa501360f9fefd446cacd0bf557a29588aa4fc37c50e750000a3`  
		Last Modified: Tue, 03 Dec 2024 04:09:18 GMT  
		Size: 21.7 MB (21710113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0425f6ff87e23ba6d559005a68cf32aede99d5bc0259e82af81721ec006b580`  
		Last Modified: Tue, 03 Dec 2024 07:56:17 GMT  
		Size: 68.1 MB (68095081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a64f4307ce70127ee567b338e88f1f2ee649800226efa44ea3c43335519c09`  
		Last Modified: Tue, 03 Dec 2024 10:49:03 GMT  
		Size: 206.2 MB (206192549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:915b11ec0eb96e2382ab827e0c58348af0eb0010af39c06e25906d2554e54c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16750919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92ad08bd30a617ab04ded34f7ee68e3521cbd1873667b36e210d31b28ce4f22`

```dockerfile
```

-	Layers:
	-	`sha256:ffaa49c4f1fce0f42bb1e16887927e5258dce89de673597e30a5b6c1eb3e39e1`  
		Last Modified: Tue, 03 Dec 2024 10:48:58 GMT  
		Size: 16.7 MB (16740726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:268a900434e3fa87efb67b84131d2f3d4b3d3693ad01f9f225707ca1c505edd3`  
		Last Modified: Tue, 03 Dec 2024 10:48:58 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:79a806d31cdc6c591136ee0af2dc5b3c5dfa90fb03fb3663f93e69b03b7109dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:09347ab21dbe40771d99a15cab37312df2d79b84b20f00024dd9d2aa86c134c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72712575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff8729e7826c86f479423ac5f4b4021c14f66333d084863578bd0fb752e50b1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e4743b5a77e386ff2c8b73b5f4786349b4c3b4a5bba77f60a49c3b94a3b29584`  
		Last Modified: Tue, 03 Dec 2024 01:27:30 GMT  
		Size: 52.1 MB (52113554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4547041a33b6c57d94bf3840b901ad1987b2672b67b1e68ff564d9703716a01`  
		Last Modified: Tue, 03 Dec 2024 02:29:17 GMT  
		Size: 20.6 MB (20599021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:92cb7df0e0568b7fc8be80e75c42503f0f546decb5c3004df7a857015f9c975a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4057349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a0c85f012d61a9fc7143b1a644830e03f38003f09652809b711fab14b97fd6`

```dockerfile
```

-	Layers:
	-	`sha256:5569ed63877a3b72ccc15acbc764971d91622137a10c5bbd4fc02fc9be1de3e7`  
		Last Modified: Tue, 03 Dec 2024 02:29:16 GMT  
		Size: 4.1 MB (4050528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:627d4a6c9c39fbb055fdb6079287f7c327c52f47c42cb61d4a295b5c69546de9`  
		Last Modified: Tue, 03 Dec 2024 02:29:16 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d8ea82934f2fc0340bc3dd165bd2631df066fb4b99ee2604429d93d1063b2fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68276182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18abdcf7f029537135a3bf80ff6fca091e446b667218bc2bb526050acab29df1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5bc3ae687a9226ba4c006ebae837bdf4fc9ce21a92c2280c2fe34aaa801bc170`  
		Last Modified: Tue, 03 Dec 2024 01:29:30 GMT  
		Size: 48.7 MB (48667592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f104f4b59037c21344a76456c37d0109c126d6df42220396b04d3aaad3cdf4`  
		Last Modified: Tue, 03 Dec 2024 05:25:08 GMT  
		Size: 19.6 MB (19608590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1eb34888c6bcf558d750c7870dda70fdf0f677466a2bbbcc3f6c637b22487b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4058816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9c7af33842f88d04619f7cc12b57fd5b403c23cd2614ee934cdf3ae837c5d2`

```dockerfile
```

-	Layers:
	-	`sha256:2cf1cf74dc8eeed6c1bb5790c8f26feba27f7b6d1c40fe71aac84b9b41a01e49`  
		Last Modified: Tue, 03 Dec 2024 05:25:07 GMT  
		Size: 4.1 MB (4051935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7fe5c7ac56fdbff4e2873392d02ec8b314fa10e354a7ba07fc4635a599cf911`  
		Last Modified: Tue, 03 Dec 2024 05:25:07 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:acd26f3cde2cb8c0011b40a7b0fc5f0a085202c16b4132a48d4b3d87f7320906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65624105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f26ea020b4f82368d5ef1e6cb507abe84309a1b314dfb9db8cb576d853ed190`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:20c73c374f639d431be81d6bb3157ee925cb0c99f0451d2cd165921c444373d3`  
		Last Modified: Tue, 03 Dec 2024 01:31:30 GMT  
		Size: 46.7 MB (46679645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c705f22774d3593ddb8b7b982bc9e82a21362788a9fdc05272e21016ed52debc`  
		Last Modified: Tue, 03 Dec 2024 07:38:00 GMT  
		Size: 18.9 MB (18944460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:101f490c884b9cd93cbe5704b63416147543d777774b8b5c862ba04c18399b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4057613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d117f4a67f0037b64012c761740f848591f2442aec41c99f45ab63e5768e10f4`

```dockerfile
```

-	Layers:
	-	`sha256:c5df70f728c876481178cf40ebe01a3784fdd9a2149063c5f02e1eecb5aa28a5`  
		Last Modified: Tue, 03 Dec 2024 07:37:59 GMT  
		Size: 4.1 MB (4050733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09b863d8b4f478adde6ff40f677f96fc244f9856730428221034288571d480b9`  
		Last Modified: Tue, 03 Dec 2024 07:37:59 GMT  
		Size: 6.9 KB (6880 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:62ca8e183f695e07fd77d42de9eb952a9ce0f2bd81914352258fd5df3fabc163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72592723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dd542b1b36710b3cbdcdd7517cffaa02e85e218a11eefe72c00236aaf47c454`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9eb21918436f171705acc6e3469286cf27466cc89ea0d17c1699761c888e169c`  
		Last Modified: Tue, 03 Dec 2024 01:32:46 GMT  
		Size: 52.3 MB (52340851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937167b9612f87af0bddfb5d6d68eeee5ceeb8c8e8837f1f9918d7f613aa06c4`  
		Last Modified: Tue, 03 Dec 2024 05:40:08 GMT  
		Size: 20.3 MB (20251872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a94476264c1e7242d723c3365da1c45377d31fd1a12b6a62e469be2e43827db3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4060870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a37982247246a3d113bc6f1432d81fa74d3f8414b545b61a9fd23ecc2dba41`

```dockerfile
```

-	Layers:
	-	`sha256:eace2bf523f290287e5780c39e5c7eec9eff8cad96e1b70253ed0df332f690ea`  
		Last Modified: Tue, 03 Dec 2024 05:40:07 GMT  
		Size: 4.1 MB (4053969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4099db3e98b8a583ea5f7762fa8bd19aef21d9cef7e7a12da3fc6ad75000894`  
		Last Modified: Tue, 03 Dec 2024 05:40:07 GMT  
		Size: 6.9 KB (6901 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a6ebcd0c7cea790946057fda68727834fcb1f1ab8c2a2cbecc0cd00b7689a8f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74683082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86fbea63eca11a42df3be73da5082f4836dbbea12db110a6cd99fde0a9151cfd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1a5aa91e83fa5cc5d15dce96bbfdc6d2483a659fdee76a341522b60ff87dc849`  
		Last Modified: Tue, 03 Dec 2024 01:27:32 GMT  
		Size: 53.0 MB (52956284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79565d36fc8ccc76d07975f07b5cf916b84627952cb6785e10e8d0301cc2acdd`  
		Last Modified: Tue, 03 Dec 2024 02:14:48 GMT  
		Size: 21.7 MB (21726798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5ba1442a97ff789f6bb2cb0d3049639905dc572d7bf741c036f717f65d149fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4053067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:015381732709d1c297b791898e04c69ae4c5205990adce22b4655b7e46a671c7`

```dockerfile
```

-	Layers:
	-	`sha256:176cb187e2706652c4ca5818dd406d955898e774f7115bc3bb60b1a2d168736f`  
		Last Modified: Tue, 03 Dec 2024 02:14:47 GMT  
		Size: 4.0 MB (4046268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f486e67dad6e670961faa1e0fcb8fc2739fd1e62af0f0638302edce42641d7c`  
		Last Modified: Tue, 03 Dec 2024 02:14:47 GMT  
		Size: 6.8 KB (6799 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:3273fc19b105f1dfd937701442cf89bfcc6c8ff3a076033c180e2f51118458a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72391506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c409a3c7797ab483334737512d8eedfafaddce425c696405bbc3b2d667fdc49c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e5a8d7ead1bc1f754b3a65ff28bee76dc2dc6179a698bf1402b64ec3d987e4e2`  
		Last Modified: Tue, 03 Dec 2024 01:30:45 GMT  
		Size: 51.4 MB (51439925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6d7c128c8894ab5647ca7070a8c53cc1626367f0fee2913a8ce5fe2237ac2e`  
		Last Modified: Tue, 03 Dec 2024 15:48:58 GMT  
		Size: 21.0 MB (20951581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a58895b7d926bba7c0cca0d5b91df4b745e5271a871af001e29691500a75f0db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 KB (6653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2123ede53fa8c7d66f8ae9105ab89ac4c539576aa0e57cc98ab2a430a4a54d28`

```dockerfile
```

-	Layers:
	-	`sha256:4759fd75a413bf9635e5be843b1d8031c808636266b8d6d8dadee61ccc0c3195`  
		Last Modified: Tue, 03 Dec 2024 15:48:55 GMT  
		Size: 6.7 KB (6653 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b24a6f3bfb5d90eae9a5f1291087f4524ece57b6baaf6d55faaee5f3ec3be691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77946483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05f2ca9d89910187afd4b082d53679045965e64a48835dec4c14980dee2f82b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5e74ce1d603959ee7e791ff530dd1c46ce3dbdbf2d00f3d3917cd370d2c2ca56`  
		Last Modified: Tue, 03 Dec 2024 01:31:51 GMT  
		Size: 56.0 MB (55955673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e3c1d8feca2b36465cdfb5b57d9969f0fb66fe43bf079a81607bc309440b99`  
		Last Modified: Tue, 03 Dec 2024 04:38:34 GMT  
		Size: 22.0 MB (21990810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6129433d73c80b125b33b97afa7b275525f8e7db7fa264888e3dcbee986ea82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4059849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb0dfe20db3e1186849044f17a622ccbcf2b0502819273cefab07e313414925`

```dockerfile
```

-	Layers:
	-	`sha256:fe3644c932e0d3d66e82b55f78268ecaa3c0f2e959e1d2a65cb58ae92b6780a0`  
		Last Modified: Tue, 03 Dec 2024 04:38:33 GMT  
		Size: 4.1 MB (4052996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d4161de8029270d73443c8adfd4374ea3a2773bd54db17c0c25b5bd34a74bdb`  
		Last Modified: Tue, 03 Dec 2024 04:38:33 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8c9562888bee88d31280e1a6f71a3eecacaf01e807555ec7050bdc331b4149cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70690922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59cd5d12ab06814d0d844853a51b3cdcdfea7b42f07dd7cde645329f035b04b0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:758bf82feb19a3477451e92c0cc7de2b281e4c03b2e4688fc172a592db81eb9b`  
		Last Modified: Tue, 03 Dec 2024 01:35:35 GMT  
		Size: 50.6 MB (50615063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfb15a1cc625368226ad4eb800a5fd3d4d9ac31fa481466aeee4edfc63619ab`  
		Last Modified: Tue, 03 Dec 2024 02:54:06 GMT  
		Size: 20.1 MB (20075859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:59b85afd46f933fd6f5ff6f4a36a63102c7d09a2efb622556244f4adbfefd1a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4049448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:021bdc3fd08f8b7d753a98ac09f988951399486c003e94f0afb7c53b12481988`

```dockerfile
```

-	Layers:
	-	`sha256:5e778ee90e5fbcd40a0e66c2a7740a616bb73e77471081714c36d6ae613ffa18`  
		Last Modified: Tue, 03 Dec 2024 02:54:04 GMT  
		Size: 4.0 MB (4042595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52b2fb840650ee03d4b7ddaf411e70923f4705cda031f920aacd2b11d68c809d`  
		Last Modified: Tue, 03 Dec 2024 02:54:03 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3492864c7bec0307681feb0e9e57419d8f196d4dc4c8802f2082355b7ead6126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73779519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79ac88e31d068c210c3337af30b80a35b12b5e36c13a10634fad46c9a179246f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:33a597a4ae2eff9c605f460e3e4517cc31e0999c816baef2a6ee6ab3da5c61ec`  
		Last Modified: Tue, 03 Dec 2024 01:31:39 GMT  
		Size: 52.1 MB (52069406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3f8d29d82faa501360f9fefd446cacd0bf557a29588aa4fc37c50e750000a3`  
		Last Modified: Tue, 03 Dec 2024 04:09:18 GMT  
		Size: 21.7 MB (21710113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b7b0bf870b7e705d773a392381394d425ef8eabd790acf1ca29817d904cf1bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4057460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39894dbbed8a03548b063995700454cdbae478d087f58f6db396c8545c0b3274`

```dockerfile
```

-	Layers:
	-	`sha256:bf623140f2dc9c2b694480e2869281e5d59e053b494e21260276ab187ffe8245`  
		Last Modified: Tue, 03 Dec 2024 04:09:17 GMT  
		Size: 4.1 MB (4050639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb1b7101e22a03ccec00af26972c90c63723d98e0d5310dbd1ac6e0ae345ad7a`  
		Last Modified: Tue, 03 Dec 2024 04:09:16 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:1a683724cd1481a99f1be814d9203d1225b731e173089e3e62c046780abf1ca6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:testing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:da06b24525cf008d45f41cb668247eee87a08689df068a618d546916d6ae1c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139771011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ca6d8dd9a27942e7de592f7688c5ce9541beb0071fbb2c608ceb2bef3f6f6f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e4743b5a77e386ff2c8b73b5f4786349b4c3b4a5bba77f60a49c3b94a3b29584`  
		Last Modified: Tue, 03 Dec 2024 01:27:30 GMT  
		Size: 52.1 MB (52113554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4547041a33b6c57d94bf3840b901ad1987b2672b67b1e68ff564d9703716a01`  
		Last Modified: Tue, 03 Dec 2024 02:29:17 GMT  
		Size: 20.6 MB (20599021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46b5387da4a2f31c146885e44d705069d7906eee138ab3588a9fee7bcae723e`  
		Last Modified: Tue, 03 Dec 2024 03:17:15 GMT  
		Size: 67.1 MB (67058436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a8a576689048442f9285b1e2d3b8e70de8ffdfb4c20c56d6e70985784cd861a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8be949d7ff95df28359fe769be1e7b26f6f2bd935fc6ca92743ef514696ee24`

```dockerfile
```

-	Layers:
	-	`sha256:d392955327241dbd4fa732bf7f7bf2f671035b7dff2ce50e2a7fd0802cc79306`  
		Last Modified: Tue, 03 Dec 2024 03:17:14 GMT  
		Size: 7.7 MB (7673471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68f3b7d42efb398b3cb47bbe501e8f1d88b26d69ba97707db98f4be1d3a213b4`  
		Last Modified: Tue, 03 Dec 2024 03:17:14 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f58998c164b872a995e8c2488d4449c575c973afdd5328339dce33bbaecbb6ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 MB (132678369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996871804936b7a5ef88a59edfb5ff11a638889c5c06ba22cac89fae0dcb7aaa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5bc3ae687a9226ba4c006ebae837bdf4fc9ce21a92c2280c2fe34aaa801bc170`  
		Last Modified: Tue, 03 Dec 2024 01:29:30 GMT  
		Size: 48.7 MB (48667592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f104f4b59037c21344a76456c37d0109c126d6df42220396b04d3aaad3cdf4`  
		Last Modified: Tue, 03 Dec 2024 05:25:08 GMT  
		Size: 19.6 MB (19608590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b47bb9243d7017922dcc62de48c63d8cfb54c3c1e685c3e38d7cea429218c0e`  
		Last Modified: Tue, 03 Dec 2024 08:42:18 GMT  
		Size: 64.4 MB (64402187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9eac8d18f0d619b921e87fb696ec7ddd1dcd909048886f90f96abca7fef946bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4899ab3a5d47d295306707e3a125b9526e97ba5ee2e8421e14431b21b28ecf7`

```dockerfile
```

-	Layers:
	-	`sha256:24d68fa4daa45f024376e555272bf77b2c06ea5f777b7d93ddb7878d49d60ecb`  
		Last Modified: Tue, 03 Dec 2024 08:42:17 GMT  
		Size: 7.7 MB (7672931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c14de663ae0734d8f5151fdf3a515dceefedcce57432d1cd70a5f5e9a49cc37c`  
		Last Modified: Tue, 03 Dec 2024 08:42:16 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8d39deb50460a075e5ebaf45c7b356d7aa6926e0e4f6057a529fdf1828aa0cc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127522538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d34bcfbc7c0a8a66fb81bf7e930bcfc56b7ba0f6804bb489d2094768bd39d3f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:20c73c374f639d431be81d6bb3157ee925cb0c99f0451d2cd165921c444373d3`  
		Last Modified: Tue, 03 Dec 2024 01:31:30 GMT  
		Size: 46.7 MB (46679645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c705f22774d3593ddb8b7b982bc9e82a21362788a9fdc05272e21016ed52debc`  
		Last Modified: Tue, 03 Dec 2024 07:38:00 GMT  
		Size: 18.9 MB (18944460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a431a228225acac55e8846f5426c9cadb4b56af6577e4fc2e206ee3b42a287`  
		Last Modified: Tue, 03 Dec 2024 17:18:35 GMT  
		Size: 61.9 MB (61898433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f20d4b16748272026d508703532e62ad1f72e903aaef04835eddd35e1decfdb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b962f3d7ce0aa2602c4d46b70ba89b538cdeafedebdb91bd90afa6ec3a1251e`

```dockerfile
```

-	Layers:
	-	`sha256:693052ed3df2b83fde4fa0800280114d8462930cdccb7241a2ca16b00cb08dbb`  
		Last Modified: Tue, 03 Dec 2024 17:18:33 GMT  
		Size: 7.7 MB (7672703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db2a8779eafb68a0aed7fc5d3002a09e4385f40c35f0d5b8c3c25910c9afd1e2`  
		Last Modified: Tue, 03 Dec 2024 17:18:32 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d49da1c0ab574f1ee82048183744e7c4a20a58e2630de30576536864742e3b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139699926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1edb438449340747f9d5156a2a723ab8c85b0976e68c66f9498ee726545578dd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9eb21918436f171705acc6e3469286cf27466cc89ea0d17c1699761c888e169c`  
		Last Modified: Tue, 03 Dec 2024 01:32:46 GMT  
		Size: 52.3 MB (52340851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937167b9612f87af0bddfb5d6d68eeee5ceeb8c8e8837f1f9918d7f613aa06c4`  
		Last Modified: Tue, 03 Dec 2024 05:40:08 GMT  
		Size: 20.3 MB (20251872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5eb80243bfd344e12541595272ea8f33faae6f5a77fc26a37baef8d6c8ea36`  
		Last Modified: Tue, 03 Dec 2024 11:52:25 GMT  
		Size: 67.1 MB (67107203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9b7a4e8e3b0b85db390656b6b8cca5621a23e152efdffe411a8f9d5475cd97dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7690453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bca429ac0be19736a53bcdd86c8110a6b3d096b8578d09b9e8cc4847630157e`

```dockerfile
```

-	Layers:
	-	`sha256:875d04078eea0a2500a40cad84a0a00885b05d146a2b6d2e56489b96860538cb`  
		Last Modified: Tue, 03 Dec 2024 11:52:23 GMT  
		Size: 7.7 MB (7683060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4fb854e6b21f3d5083b4dd91df66eed9eacff04eac2761219dc9f5beb7ad194`  
		Last Modified: Tue, 03 Dec 2024 11:52:23 GMT  
		Size: 7.4 KB (7393 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:719ff7c42eefa5f6811c72f3d92c194797cadf5b65455e346d3cb3e9b7705616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.5 MB (143544476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e3ad359f205a750b81d425ca9d2f51cd5eeefadb8cd309a411bc9397fd7e21`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1a5aa91e83fa5cc5d15dce96bbfdc6d2483a659fdee76a341522b60ff87dc849`  
		Last Modified: Tue, 03 Dec 2024 01:27:32 GMT  
		Size: 53.0 MB (52956284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79565d36fc8ccc76d07975f07b5cf916b84627952cb6785e10e8d0301cc2acdd`  
		Last Modified: Tue, 03 Dec 2024 02:14:48 GMT  
		Size: 21.7 MB (21726798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad782586fddb10041571d568c827bae913dd109647631cce2fe893ecfe4b9488`  
		Last Modified: Tue, 03 Dec 2024 03:17:11 GMT  
		Size: 68.9 MB (68861394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:535718f08215a34be3c30316648e76a757427791ab2fd9e70495b1e6a5e58b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7675497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa66fa78d05f3be959bc718b8f26030aa9c1a00679251a79660446336a3ffee`

```dockerfile
```

-	Layers:
	-	`sha256:d64db0dc614cd414a9d0e4644feae150e0f1e8c7eda3e0b58ee2612315e3f67e`  
		Last Modified: Tue, 03 Dec 2024 03:17:10 GMT  
		Size: 7.7 MB (7668205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c80bd9ae34e9602bb84c05a4ddf8a0caa783edcbe6ea469738ea67b68efdc55`  
		Last Modified: Tue, 03 Dec 2024 03:17:09 GMT  
		Size: 7.3 KB (7292 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:c079df95e76a9a8894714db9abb0277635d739c02b9038af4c21f30993c8cd2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138304433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3d5dd81e344958a5a800b0939a8ef1c7fc30d9d447fcd4586c175cb5aad950`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e5a8d7ead1bc1f754b3a65ff28bee76dc2dc6179a698bf1402b64ec3d987e4e2`  
		Last Modified: Tue, 03 Dec 2024 01:30:45 GMT  
		Size: 51.4 MB (51439925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6d7c128c8894ab5647ca7070a8c53cc1626367f0fee2913a8ce5fe2237ac2e`  
		Last Modified: Tue, 03 Dec 2024 15:48:58 GMT  
		Size: 21.0 MB (20951581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddd6435addf48f219bf6a9a7272ed63c493377979c37d721428b6d2c65dab1f`  
		Last Modified: Tue, 03 Dec 2024 23:28:11 GMT  
		Size: 65.9 MB (65912927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ac901c44bfa9f9e8c10c0c7241b6e2071a9ce15aca6b3ff64884cc0a7debc7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efaf51db1c3fa8cb7c637485809ed264d0f11848e68054597ad746478f6a6130`

```dockerfile
```

-	Layers:
	-	`sha256:67a2e9f6b9101e016ca82f90ddb239e70c70d069ab2d1ff8fe9468b7dfab7232`  
		Last Modified: Tue, 03 Dec 2024 23:28:05 GMT  
		Size: 7.1 KB (7147 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:29106e083d3f0884ff2ab67cab04de54b2948f989c84c1de72a1ceb5d72f2900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.4 MB (150416706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ec1fbf43792ca3ab0d994b9fbdf8d4c8fc7e96b90202e42e6e6c01520a25cb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5e74ce1d603959ee7e791ff530dd1c46ce3dbdbf2d00f3d3917cd370d2c2ca56`  
		Last Modified: Tue, 03 Dec 2024 01:31:51 GMT  
		Size: 56.0 MB (55955673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e3c1d8feca2b36465cdfb5b57d9969f0fb66fe43bf079a81607bc309440b99`  
		Last Modified: Tue, 03 Dec 2024 04:38:34 GMT  
		Size: 22.0 MB (21990810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f35d27e17f5faa7b717fcd51d2689cc9f5f0b57184433a4eae97a42f95da04f`  
		Last Modified: Tue, 03 Dec 2024 09:44:41 GMT  
		Size: 72.5 MB (72470223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d7a5f51f1d75eb637e939fe2c1d001071a9ffca3db92bd98f0f44b1414ddf061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7686565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be05632c83a4dc663ff459ace817ccabda153cf61714e31816283eed707acf41`

```dockerfile
```

-	Layers:
	-	`sha256:e80dad17cad41492690720cb23ab6f99daa18133ee238fccb5bfbdfefd17ab40`  
		Last Modified: Tue, 03 Dec 2024 09:44:39 GMT  
		Size: 7.7 MB (7679219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:413f4d207e490cadfa1567ed05b98441f383ecc08e32f7c8d9168196cbb75d3b`  
		Last Modified: Tue, 03 Dec 2024 09:44:38 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7cbdb5aaa9bdb372290824b75edeb47013f021005307c350766138665edeb373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141874600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a0fb9ae5e7d29b1b0cf491d5393a5ac639936cf966ffa23da517254253e92f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:33a597a4ae2eff9c605f460e3e4517cc31e0999c816baef2a6ee6ab3da5c61ec`  
		Last Modified: Tue, 03 Dec 2024 01:31:39 GMT  
		Size: 52.1 MB (52069406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3f8d29d82faa501360f9fefd446cacd0bf557a29588aa4fc37c50e750000a3`  
		Last Modified: Tue, 03 Dec 2024 04:09:18 GMT  
		Size: 21.7 MB (21710113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0425f6ff87e23ba6d559005a68cf32aede99d5bc0259e82af81721ec006b580`  
		Last Modified: Tue, 03 Dec 2024 07:56:17 GMT  
		Size: 68.1 MB (68095081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:39a2f7b3b1fb4e73530d08d088bcd30eafd6d5d786bc9387b653d8f8d8b3ba55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c702e9c9410935d4299af789c96c665239bfb53818cf765a6699f89a9cca41`

```dockerfile
```

-	Layers:
	-	`sha256:a366d37dc4c5fab3169fa8005fbfd07ec0cdacfc63c176b0074314ab29054942`  
		Last Modified: Tue, 03 Dec 2024 07:56:16 GMT  
		Size: 7.7 MB (7673077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13d3948af2dd637e8a6e5a87efaa2a0c83e3771e6c96a7300299f8a4fa0515d9`  
		Last Modified: Tue, 03 Dec 2024 07:56:15 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:dc94202ffb172b4ed42f494065683069f8f248c4becc329362cb8ad4f0ba6cc7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:trixie` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:ed757090c92b4dfba07b522d16daa7c7356e9a37794b71fd2cfc716b5f00df72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.2 MB (375207066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b1c36fa0c38ceed250a0a4e36aac2b80e6c07f522cff8eb8077ebfb6142e86`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e4743b5a77e386ff2c8b73b5f4786349b4c3b4a5bba77f60a49c3b94a3b29584`  
		Last Modified: Tue, 03 Dec 2024 01:27:30 GMT  
		Size: 52.1 MB (52113554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4547041a33b6c57d94bf3840b901ad1987b2672b67b1e68ff564d9703716a01`  
		Last Modified: Tue, 03 Dec 2024 02:29:17 GMT  
		Size: 20.6 MB (20599021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46b5387da4a2f31c146885e44d705069d7906eee138ab3588a9fee7bcae723e`  
		Last Modified: Tue, 03 Dec 2024 03:17:15 GMT  
		Size: 67.1 MB (67058436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba00f95a0fc91aa5af7f7128d1d9cb3461821c06ee197cedb64680239a9330fc`  
		Last Modified: Tue, 03 Dec 2024 04:32:21 GMT  
		Size: 235.4 MB (235436055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b9c8f539ce39e7b8310b4aa26beaf75d8b1c786c599118c0d371f9c05b88a7b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16974493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:499c1f23296ed70dd90fa678b5fffbcc3db5cdd0ba780ad4d8af8c81152bb1ba`

```dockerfile
```

-	Layers:
	-	`sha256:aeba652bd408371681685be2385bf3915a6ad86227cff4372d75fbd81cf44cf1`  
		Last Modified: Tue, 03 Dec 2024 04:32:17 GMT  
		Size: 17.0 MB (16964300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5d83ffd4c714db14b14c9bbfae084789a2ff936e4b23cf8b86d02f09a72ec0a`  
		Last Modified: Tue, 03 Dec 2024 04:32:17 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c636e9375ce9ccdf6de8efa6e3d973ffdce8751197773590d30484535124384a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.5 MB (338494634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:460619e39697127cad08ce61ca20ce2c9b6925d9fa694376134c3c7eac13d236`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5bc3ae687a9226ba4c006ebae837bdf4fc9ce21a92c2280c2fe34aaa801bc170`  
		Last Modified: Tue, 03 Dec 2024 01:29:30 GMT  
		Size: 48.7 MB (48667592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f104f4b59037c21344a76456c37d0109c126d6df42220396b04d3aaad3cdf4`  
		Last Modified: Tue, 03 Dec 2024 05:25:08 GMT  
		Size: 19.6 MB (19608590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b47bb9243d7017922dcc62de48c63d8cfb54c3c1e685c3e38d7cea429218c0e`  
		Last Modified: Tue, 03 Dec 2024 08:42:18 GMT  
		Size: 64.4 MB (64402187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0d6acc584d696ab456ac89386f5313fd7dbb30f7a4ea1f0fc6fa6832d72040`  
		Last Modified: Tue, 03 Dec 2024 10:11:48 GMT  
		Size: 205.8 MB (205816265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f530a531eb2590391f82e8e4cf42b9419b8e54b1381e532255b22150fa621551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16735915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d32ec904a4b93001545f14f059e71cb6ae5158832bee02312bbec5e06e5313f`

```dockerfile
```

-	Layers:
	-	`sha256:f53e2672493aee51835e2d7b671b1b06b1e16d7bd8ebfcf18e7f433cc21ce3de`  
		Last Modified: Tue, 03 Dec 2024 10:11:44 GMT  
		Size: 16.7 MB (16725662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d755ff4cd7ec164c2eea1f946a539eb3f3b3245d9a12843366600c388e0af987`  
		Last Modified: Tue, 03 Dec 2024 10:11:43 GMT  
		Size: 10.3 KB (10253 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c54092137aef82673b628701fffae1d7bb5cdee16036652cf8c5680b2311507d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.6 MB (320566678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd69e8784e9a9a24c7018a57f98312596b243e702223ff357301ebb75ff9f02a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:20c73c374f639d431be81d6bb3157ee925cb0c99f0451d2cd165921c444373d3`  
		Last Modified: Tue, 03 Dec 2024 01:31:30 GMT  
		Size: 46.7 MB (46679645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c705f22774d3593ddb8b7b982bc9e82a21362788a9fdc05272e21016ed52debc`  
		Last Modified: Tue, 03 Dec 2024 07:38:00 GMT  
		Size: 18.9 MB (18944460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a431a228225acac55e8846f5426c9cadb4b56af6577e4fc2e206ee3b42a287`  
		Last Modified: Tue, 03 Dec 2024 17:18:35 GMT  
		Size: 61.9 MB (61898433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2250e50c3b0d1679c6a6f0905a6bb14cdf995965365d96a0ed0af0a1cabeda41`  
		Last Modified: Tue, 03 Dec 2024 20:11:47 GMT  
		Size: 193.0 MB (193044140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3f0d17f8af67e79adb9ba470f17c5f6f7b4423ebee7b062e14e0213e7ddd14ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16741713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20fbf3a659f9762253c3305e4a0dcd4ebf822c59152a12c4d414fb236c480a1c`

```dockerfile
```

-	Layers:
	-	`sha256:021ec9171dbfc19c071bd17673d2e89c9aa2b95717e117707175c7f3598da4f0`  
		Last Modified: Tue, 03 Dec 2024 20:11:42 GMT  
		Size: 16.7 MB (16731460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e86dd2f315ea5820a2680250233eb394bd4e588be2acb1a7a10b9232f138f95`  
		Last Modified: Tue, 03 Dec 2024 20:11:42 GMT  
		Size: 10.3 KB (10253 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:37a190a761023c4e140ccf9149b71929db84f08fec40f69f81803e339f665a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.5 MB (366490575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdbec0ffdb40aa93cc2227f7e64678ce9711e69280737c2d9d4a8a2a696b515e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9eb21918436f171705acc6e3469286cf27466cc89ea0d17c1699761c888e169c`  
		Last Modified: Tue, 03 Dec 2024 01:32:46 GMT  
		Size: 52.3 MB (52340851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937167b9612f87af0bddfb5d6d68eeee5ceeb8c8e8837f1f9918d7f613aa06c4`  
		Last Modified: Tue, 03 Dec 2024 05:40:08 GMT  
		Size: 20.3 MB (20251872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5eb80243bfd344e12541595272ea8f33faae6f5a77fc26a37baef8d6c8ea36`  
		Last Modified: Tue, 03 Dec 2024 11:52:25 GMT  
		Size: 67.1 MB (67107203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be95ee2ae477988acf1c4f6dcfc88e1ae5a55fd73cb1208a350d7951447cd5c2`  
		Last Modified: Tue, 03 Dec 2024 16:25:24 GMT  
		Size: 226.8 MB (226790649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b69fd275d0a8e244814ebfebaa3277de3c5c799239fc1179eeb59b49cff6bb8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17061306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d61e81a066f2bf03ec9ede670c559770001733b72dccaee56894ce1afe09a2`

```dockerfile
```

-	Layers:
	-	`sha256:10fd39fd24a909e9e91ac353e116e838d10121424f2fb2dd2eb94b5253aef4c7`  
		Last Modified: Tue, 03 Dec 2024 16:25:20 GMT  
		Size: 17.1 MB (17051033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:781c922e20f55229b5dc779d96f6a85737b2f5c7ab8068980abbb055be1f8609`  
		Last Modified: Tue, 03 Dec 2024 16:25:19 GMT  
		Size: 10.3 KB (10273 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b1e1cdc198e59acb495d0927ea674cff22326dfa3019424fb0a344a66225ca12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.2 MB (383151595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107ab0c39dc78b9e57ebf91be11e68f4bfea2c3c8274b2817e739d1abd96b2cb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1a5aa91e83fa5cc5d15dce96bbfdc6d2483a659fdee76a341522b60ff87dc849`  
		Last Modified: Tue, 03 Dec 2024 01:27:32 GMT  
		Size: 53.0 MB (52956284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79565d36fc8ccc76d07975f07b5cf916b84627952cb6785e10e8d0301cc2acdd`  
		Last Modified: Tue, 03 Dec 2024 02:14:48 GMT  
		Size: 21.7 MB (21726798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad782586fddb10041571d568c827bae913dd109647631cce2fe893ecfe4b9488`  
		Last Modified: Tue, 03 Dec 2024 03:17:11 GMT  
		Size: 68.9 MB (68861394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e0699983953a7cec342f58306a547a993dc86fcdd09293e817b3e01512494b`  
		Last Modified: Tue, 03 Dec 2024 04:32:37 GMT  
		Size: 239.6 MB (239607119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:de2d63fd3a08165ba0533d04f1b6b235cf235ac4d014dea6d58b91bc768784f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16944039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835d1e208a7980646971042bf95ed3c919253fb965855df2f98f7c5d3284d1dd`

```dockerfile
```

-	Layers:
	-	`sha256:d0cb59f5654fc36e2048aa3b18128bf0764b4cba7b7276d4734c553f6b495f85`  
		Last Modified: Tue, 03 Dec 2024 04:32:32 GMT  
		Size: 16.9 MB (16933868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bea586dcbbe73941b9db0060e0fb5b46aa2e20eeb654f2758421e9b06508583`  
		Last Modified: Tue, 03 Dec 2024 04:32:32 GMT  
		Size: 10.2 KB (10171 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:6aed94b346224a907374352ffe52a244f6fb845bb6fa77af0dbf33caabf6b925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.5 MB (349523155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c8a6f92b61aee8dc5319671b6c4838f2c5cc076f392dd5e5a5ed52f09243017`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e5a8d7ead1bc1f754b3a65ff28bee76dc2dc6179a698bf1402b64ec3d987e4e2`  
		Last Modified: Tue, 03 Dec 2024 01:30:45 GMT  
		Size: 51.4 MB (51439925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6d7c128c8894ab5647ca7070a8c53cc1626367f0fee2913a8ce5fe2237ac2e`  
		Last Modified: Tue, 03 Dec 2024 15:48:58 GMT  
		Size: 21.0 MB (20951581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddd6435addf48f219bf6a9a7272ed63c493377979c37d721428b6d2c65dab1f`  
		Last Modified: Tue, 03 Dec 2024 23:28:11 GMT  
		Size: 65.9 MB (65912927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982cc02c1e97f3987f1a40bace25f4f97248212c53b960fbe66ac9c773ce7ca2`  
		Last Modified: Wed, 04 Dec 2024 04:58:21 GMT  
		Size: 211.2 MB (211218722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:62a3dabe91f7108ef0c06eb9b6acea0b172d897697c9160cdbcb678f3da17ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3266f96a84806158d2d80e622846075de301f496c29d3f3045aa367a97adb73`

```dockerfile
```

-	Layers:
	-	`sha256:daa5a4b1199b129238891d666d4691b1ba0ccaa01bbdc77033f58a0747a4a008`  
		Last Modified: Wed, 04 Dec 2024 04:58:02 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6664a3df9dc9bec277c19ee01729befd3ce661e183f2a0d86777890babc7a779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.6 MB (382552567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6645f0cf430b3644a88d2853e79a959d668b36a2196104d494e19ca8ee0e1e67`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5e74ce1d603959ee7e791ff530dd1c46ce3dbdbf2d00f3d3917cd370d2c2ca56`  
		Last Modified: Tue, 03 Dec 2024 01:31:51 GMT  
		Size: 56.0 MB (55955673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e3c1d8feca2b36465cdfb5b57d9969f0fb66fe43bf079a81607bc309440b99`  
		Last Modified: Tue, 03 Dec 2024 04:38:34 GMT  
		Size: 22.0 MB (21990810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f35d27e17f5faa7b717fcd51d2689cc9f5f0b57184433a4eae97a42f95da04f`  
		Last Modified: Tue, 03 Dec 2024 09:44:41 GMT  
		Size: 72.5 MB (72470223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52a720b71dddcb2a25df1c62f4df5be637ee1b44f6c72e886501e695c3e8491`  
		Last Modified: Tue, 03 Dec 2024 16:21:25 GMT  
		Size: 232.1 MB (232135861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:46c273b1c0cfbdacdd361fa947c0ae293856b1182058b608e17adb484abd5c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16956784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a972b3130f5c0e09be05cbf098c2fe9f102fb226330c6a9f77a9e59b4e34ab07`

```dockerfile
```

-	Layers:
	-	`sha256:a680bd893b317b1e20138c7cae82c062fd4718a73928c1fe154c9a60ac52e652`  
		Last Modified: Tue, 03 Dec 2024 16:21:19 GMT  
		Size: 16.9 MB (16946559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3348c230fc094aec79e85591b44365b40fe471dceb5ef063384a1515e5721ca6`  
		Last Modified: Tue, 03 Dec 2024 16:21:19 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:59ba1941b5338aeec3a0cfa33e35cbf7a6634dbab19b243d5e1f2ad7ec4edf98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.1 MB (348067149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6efa8ee7b2b6de06d44ececdfdcf93f69002163b468f5578a592d090d370e3f8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:33a597a4ae2eff9c605f460e3e4517cc31e0999c816baef2a6ee6ab3da5c61ec`  
		Last Modified: Tue, 03 Dec 2024 01:31:39 GMT  
		Size: 52.1 MB (52069406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3f8d29d82faa501360f9fefd446cacd0bf557a29588aa4fc37c50e750000a3`  
		Last Modified: Tue, 03 Dec 2024 04:09:18 GMT  
		Size: 21.7 MB (21710113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0425f6ff87e23ba6d559005a68cf32aede99d5bc0259e82af81721ec006b580`  
		Last Modified: Tue, 03 Dec 2024 07:56:17 GMT  
		Size: 68.1 MB (68095081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a64f4307ce70127ee567b338e88f1f2ee649800226efa44ea3c43335519c09`  
		Last Modified: Tue, 03 Dec 2024 10:49:03 GMT  
		Size: 206.2 MB (206192549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:915b11ec0eb96e2382ab827e0c58348af0eb0010af39c06e25906d2554e54c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16750919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92ad08bd30a617ab04ded34f7ee68e3521cbd1873667b36e210d31b28ce4f22`

```dockerfile
```

-	Layers:
	-	`sha256:ffaa49c4f1fce0f42bb1e16887927e5258dce89de673597e30a5b6c1eb3e39e1`  
		Last Modified: Tue, 03 Dec 2024 10:48:58 GMT  
		Size: 16.7 MB (16740726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:268a900434e3fa87efb67b84131d2f3d4b3d3693ad01f9f225707ca1c505edd3`  
		Last Modified: Tue, 03 Dec 2024 10:48:58 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:79a806d31cdc6c591136ee0af2dc5b3c5dfa90fb03fb3663f93e69b03b7109dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:trixie-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:09347ab21dbe40771d99a15cab37312df2d79b84b20f00024dd9d2aa86c134c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72712575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff8729e7826c86f479423ac5f4b4021c14f66333d084863578bd0fb752e50b1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e4743b5a77e386ff2c8b73b5f4786349b4c3b4a5bba77f60a49c3b94a3b29584`  
		Last Modified: Tue, 03 Dec 2024 01:27:30 GMT  
		Size: 52.1 MB (52113554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4547041a33b6c57d94bf3840b901ad1987b2672b67b1e68ff564d9703716a01`  
		Last Modified: Tue, 03 Dec 2024 02:29:17 GMT  
		Size: 20.6 MB (20599021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:92cb7df0e0568b7fc8be80e75c42503f0f546decb5c3004df7a857015f9c975a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4057349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a0c85f012d61a9fc7143b1a644830e03f38003f09652809b711fab14b97fd6`

```dockerfile
```

-	Layers:
	-	`sha256:5569ed63877a3b72ccc15acbc764971d91622137a10c5bbd4fc02fc9be1de3e7`  
		Last Modified: Tue, 03 Dec 2024 02:29:16 GMT  
		Size: 4.1 MB (4050528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:627d4a6c9c39fbb055fdb6079287f7c327c52f47c42cb61d4a295b5c69546de9`  
		Last Modified: Tue, 03 Dec 2024 02:29:16 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d8ea82934f2fc0340bc3dd165bd2631df066fb4b99ee2604429d93d1063b2fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68276182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18abdcf7f029537135a3bf80ff6fca091e446b667218bc2bb526050acab29df1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5bc3ae687a9226ba4c006ebae837bdf4fc9ce21a92c2280c2fe34aaa801bc170`  
		Last Modified: Tue, 03 Dec 2024 01:29:30 GMT  
		Size: 48.7 MB (48667592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f104f4b59037c21344a76456c37d0109c126d6df42220396b04d3aaad3cdf4`  
		Last Modified: Tue, 03 Dec 2024 05:25:08 GMT  
		Size: 19.6 MB (19608590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1eb34888c6bcf558d750c7870dda70fdf0f677466a2bbbcc3f6c637b22487b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4058816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9c7af33842f88d04619f7cc12b57fd5b403c23cd2614ee934cdf3ae837c5d2`

```dockerfile
```

-	Layers:
	-	`sha256:2cf1cf74dc8eeed6c1bb5790c8f26feba27f7b6d1c40fe71aac84b9b41a01e49`  
		Last Modified: Tue, 03 Dec 2024 05:25:07 GMT  
		Size: 4.1 MB (4051935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7fe5c7ac56fdbff4e2873392d02ec8b314fa10e354a7ba07fc4635a599cf911`  
		Last Modified: Tue, 03 Dec 2024 05:25:07 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:acd26f3cde2cb8c0011b40a7b0fc5f0a085202c16b4132a48d4b3d87f7320906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65624105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f26ea020b4f82368d5ef1e6cb507abe84309a1b314dfb9db8cb576d853ed190`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:20c73c374f639d431be81d6bb3157ee925cb0c99f0451d2cd165921c444373d3`  
		Last Modified: Tue, 03 Dec 2024 01:31:30 GMT  
		Size: 46.7 MB (46679645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c705f22774d3593ddb8b7b982bc9e82a21362788a9fdc05272e21016ed52debc`  
		Last Modified: Tue, 03 Dec 2024 07:38:00 GMT  
		Size: 18.9 MB (18944460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:101f490c884b9cd93cbe5704b63416147543d777774b8b5c862ba04c18399b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4057613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d117f4a67f0037b64012c761740f848591f2442aec41c99f45ab63e5768e10f4`

```dockerfile
```

-	Layers:
	-	`sha256:c5df70f728c876481178cf40ebe01a3784fdd9a2149063c5f02e1eecb5aa28a5`  
		Last Modified: Tue, 03 Dec 2024 07:37:59 GMT  
		Size: 4.1 MB (4050733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09b863d8b4f478adde6ff40f677f96fc244f9856730428221034288571d480b9`  
		Last Modified: Tue, 03 Dec 2024 07:37:59 GMT  
		Size: 6.9 KB (6880 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:62ca8e183f695e07fd77d42de9eb952a9ce0f2bd81914352258fd5df3fabc163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72592723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dd542b1b36710b3cbdcdd7517cffaa02e85e218a11eefe72c00236aaf47c454`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9eb21918436f171705acc6e3469286cf27466cc89ea0d17c1699761c888e169c`  
		Last Modified: Tue, 03 Dec 2024 01:32:46 GMT  
		Size: 52.3 MB (52340851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937167b9612f87af0bddfb5d6d68eeee5ceeb8c8e8837f1f9918d7f613aa06c4`  
		Last Modified: Tue, 03 Dec 2024 05:40:08 GMT  
		Size: 20.3 MB (20251872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a94476264c1e7242d723c3365da1c45377d31fd1a12b6a62e469be2e43827db3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4060870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a37982247246a3d113bc6f1432d81fa74d3f8414b545b61a9fd23ecc2dba41`

```dockerfile
```

-	Layers:
	-	`sha256:eace2bf523f290287e5780c39e5c7eec9eff8cad96e1b70253ed0df332f690ea`  
		Last Modified: Tue, 03 Dec 2024 05:40:07 GMT  
		Size: 4.1 MB (4053969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4099db3e98b8a583ea5f7762fa8bd19aef21d9cef7e7a12da3fc6ad75000894`  
		Last Modified: Tue, 03 Dec 2024 05:40:07 GMT  
		Size: 6.9 KB (6901 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a6ebcd0c7cea790946057fda68727834fcb1f1ab8c2a2cbecc0cd00b7689a8f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74683082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86fbea63eca11a42df3be73da5082f4836dbbea12db110a6cd99fde0a9151cfd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1a5aa91e83fa5cc5d15dce96bbfdc6d2483a659fdee76a341522b60ff87dc849`  
		Last Modified: Tue, 03 Dec 2024 01:27:32 GMT  
		Size: 53.0 MB (52956284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79565d36fc8ccc76d07975f07b5cf916b84627952cb6785e10e8d0301cc2acdd`  
		Last Modified: Tue, 03 Dec 2024 02:14:48 GMT  
		Size: 21.7 MB (21726798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5ba1442a97ff789f6bb2cb0d3049639905dc572d7bf741c036f717f65d149fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4053067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:015381732709d1c297b791898e04c69ae4c5205990adce22b4655b7e46a671c7`

```dockerfile
```

-	Layers:
	-	`sha256:176cb187e2706652c4ca5818dd406d955898e774f7115bc3bb60b1a2d168736f`  
		Last Modified: Tue, 03 Dec 2024 02:14:47 GMT  
		Size: 4.0 MB (4046268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f486e67dad6e670961faa1e0fcb8fc2739fd1e62af0f0638302edce42641d7c`  
		Last Modified: Tue, 03 Dec 2024 02:14:47 GMT  
		Size: 6.8 KB (6799 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:3273fc19b105f1dfd937701442cf89bfcc6c8ff3a076033c180e2f51118458a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72391506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c409a3c7797ab483334737512d8eedfafaddce425c696405bbc3b2d667fdc49c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e5a8d7ead1bc1f754b3a65ff28bee76dc2dc6179a698bf1402b64ec3d987e4e2`  
		Last Modified: Tue, 03 Dec 2024 01:30:45 GMT  
		Size: 51.4 MB (51439925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6d7c128c8894ab5647ca7070a8c53cc1626367f0fee2913a8ce5fe2237ac2e`  
		Last Modified: Tue, 03 Dec 2024 15:48:58 GMT  
		Size: 21.0 MB (20951581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a58895b7d926bba7c0cca0d5b91df4b745e5271a871af001e29691500a75f0db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 KB (6653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2123ede53fa8c7d66f8ae9105ab89ac4c539576aa0e57cc98ab2a430a4a54d28`

```dockerfile
```

-	Layers:
	-	`sha256:4759fd75a413bf9635e5be843b1d8031c808636266b8d6d8dadee61ccc0c3195`  
		Last Modified: Tue, 03 Dec 2024 15:48:55 GMT  
		Size: 6.7 KB (6653 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b24a6f3bfb5d90eae9a5f1291087f4524ece57b6baaf6d55faaee5f3ec3be691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77946483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05f2ca9d89910187afd4b082d53679045965e64a48835dec4c14980dee2f82b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5e74ce1d603959ee7e791ff530dd1c46ce3dbdbf2d00f3d3917cd370d2c2ca56`  
		Last Modified: Tue, 03 Dec 2024 01:31:51 GMT  
		Size: 56.0 MB (55955673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e3c1d8feca2b36465cdfb5b57d9969f0fb66fe43bf079a81607bc309440b99`  
		Last Modified: Tue, 03 Dec 2024 04:38:34 GMT  
		Size: 22.0 MB (21990810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6129433d73c80b125b33b97afa7b275525f8e7db7fa264888e3dcbee986ea82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4059849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb0dfe20db3e1186849044f17a622ccbcf2b0502819273cefab07e313414925`

```dockerfile
```

-	Layers:
	-	`sha256:fe3644c932e0d3d66e82b55f78268ecaa3c0f2e959e1d2a65cb58ae92b6780a0`  
		Last Modified: Tue, 03 Dec 2024 04:38:33 GMT  
		Size: 4.1 MB (4052996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d4161de8029270d73443c8adfd4374ea3a2773bd54db17c0c25b5bd34a74bdb`  
		Last Modified: Tue, 03 Dec 2024 04:38:33 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8c9562888bee88d31280e1a6f71a3eecacaf01e807555ec7050bdc331b4149cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70690922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59cd5d12ab06814d0d844853a51b3cdcdfea7b42f07dd7cde645329f035b04b0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:758bf82feb19a3477451e92c0cc7de2b281e4c03b2e4688fc172a592db81eb9b`  
		Last Modified: Tue, 03 Dec 2024 01:35:35 GMT  
		Size: 50.6 MB (50615063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfb15a1cc625368226ad4eb800a5fd3d4d9ac31fa481466aeee4edfc63619ab`  
		Last Modified: Tue, 03 Dec 2024 02:54:06 GMT  
		Size: 20.1 MB (20075859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:59b85afd46f933fd6f5ff6f4a36a63102c7d09a2efb622556244f4adbfefd1a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4049448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:021bdc3fd08f8b7d753a98ac09f988951399486c003e94f0afb7c53b12481988`

```dockerfile
```

-	Layers:
	-	`sha256:5e778ee90e5fbcd40a0e66c2a7740a616bb73e77471081714c36d6ae613ffa18`  
		Last Modified: Tue, 03 Dec 2024 02:54:04 GMT  
		Size: 4.0 MB (4042595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52b2fb840650ee03d4b7ddaf411e70923f4705cda031f920aacd2b11d68c809d`  
		Last Modified: Tue, 03 Dec 2024 02:54:03 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3492864c7bec0307681feb0e9e57419d8f196d4dc4c8802f2082355b7ead6126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73779519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79ac88e31d068c210c3337af30b80a35b12b5e36c13a10634fad46c9a179246f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:33a597a4ae2eff9c605f460e3e4517cc31e0999c816baef2a6ee6ab3da5c61ec`  
		Last Modified: Tue, 03 Dec 2024 01:31:39 GMT  
		Size: 52.1 MB (52069406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3f8d29d82faa501360f9fefd446cacd0bf557a29588aa4fc37c50e750000a3`  
		Last Modified: Tue, 03 Dec 2024 04:09:18 GMT  
		Size: 21.7 MB (21710113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b7b0bf870b7e705d773a392381394d425ef8eabd790acf1ca29817d904cf1bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4057460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39894dbbed8a03548b063995700454cdbae478d087f58f6db396c8545c0b3274`

```dockerfile
```

-	Layers:
	-	`sha256:bf623140f2dc9c2b694480e2869281e5d59e053b494e21260276ab187ffe8245`  
		Last Modified: Tue, 03 Dec 2024 04:09:17 GMT  
		Size: 4.1 MB (4050639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb1b7101e22a03ccec00af26972c90c63723d98e0d5310dbd1ac6e0ae345ad7a`  
		Last Modified: Tue, 03 Dec 2024 04:09:16 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:1a683724cd1481a99f1be814d9203d1225b731e173089e3e62c046780abf1ca6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:trixie-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:da06b24525cf008d45f41cb668247eee87a08689df068a618d546916d6ae1c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139771011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ca6d8dd9a27942e7de592f7688c5ce9541beb0071fbb2c608ceb2bef3f6f6f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e4743b5a77e386ff2c8b73b5f4786349b4c3b4a5bba77f60a49c3b94a3b29584`  
		Last Modified: Tue, 03 Dec 2024 01:27:30 GMT  
		Size: 52.1 MB (52113554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4547041a33b6c57d94bf3840b901ad1987b2672b67b1e68ff564d9703716a01`  
		Last Modified: Tue, 03 Dec 2024 02:29:17 GMT  
		Size: 20.6 MB (20599021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46b5387da4a2f31c146885e44d705069d7906eee138ab3588a9fee7bcae723e`  
		Last Modified: Tue, 03 Dec 2024 03:17:15 GMT  
		Size: 67.1 MB (67058436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a8a576689048442f9285b1e2d3b8e70de8ffdfb4c20c56d6e70985784cd861a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8be949d7ff95df28359fe769be1e7b26f6f2bd935fc6ca92743ef514696ee24`

```dockerfile
```

-	Layers:
	-	`sha256:d392955327241dbd4fa732bf7f7bf2f671035b7dff2ce50e2a7fd0802cc79306`  
		Last Modified: Tue, 03 Dec 2024 03:17:14 GMT  
		Size: 7.7 MB (7673471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68f3b7d42efb398b3cb47bbe501e8f1d88b26d69ba97707db98f4be1d3a213b4`  
		Last Modified: Tue, 03 Dec 2024 03:17:14 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f58998c164b872a995e8c2488d4449c575c973afdd5328339dce33bbaecbb6ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 MB (132678369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996871804936b7a5ef88a59edfb5ff11a638889c5c06ba22cac89fae0dcb7aaa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5bc3ae687a9226ba4c006ebae837bdf4fc9ce21a92c2280c2fe34aaa801bc170`  
		Last Modified: Tue, 03 Dec 2024 01:29:30 GMT  
		Size: 48.7 MB (48667592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f104f4b59037c21344a76456c37d0109c126d6df42220396b04d3aaad3cdf4`  
		Last Modified: Tue, 03 Dec 2024 05:25:08 GMT  
		Size: 19.6 MB (19608590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b47bb9243d7017922dcc62de48c63d8cfb54c3c1e685c3e38d7cea429218c0e`  
		Last Modified: Tue, 03 Dec 2024 08:42:18 GMT  
		Size: 64.4 MB (64402187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9eac8d18f0d619b921e87fb696ec7ddd1dcd909048886f90f96abca7fef946bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4899ab3a5d47d295306707e3a125b9526e97ba5ee2e8421e14431b21b28ecf7`

```dockerfile
```

-	Layers:
	-	`sha256:24d68fa4daa45f024376e555272bf77b2c06ea5f777b7d93ddb7878d49d60ecb`  
		Last Modified: Tue, 03 Dec 2024 08:42:17 GMT  
		Size: 7.7 MB (7672931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c14de663ae0734d8f5151fdf3a515dceefedcce57432d1cd70a5f5e9a49cc37c`  
		Last Modified: Tue, 03 Dec 2024 08:42:16 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8d39deb50460a075e5ebaf45c7b356d7aa6926e0e4f6057a529fdf1828aa0cc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127522538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d34bcfbc7c0a8a66fb81bf7e930bcfc56b7ba0f6804bb489d2094768bd39d3f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:20c73c374f639d431be81d6bb3157ee925cb0c99f0451d2cd165921c444373d3`  
		Last Modified: Tue, 03 Dec 2024 01:31:30 GMT  
		Size: 46.7 MB (46679645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c705f22774d3593ddb8b7b982bc9e82a21362788a9fdc05272e21016ed52debc`  
		Last Modified: Tue, 03 Dec 2024 07:38:00 GMT  
		Size: 18.9 MB (18944460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a431a228225acac55e8846f5426c9cadb4b56af6577e4fc2e206ee3b42a287`  
		Last Modified: Tue, 03 Dec 2024 17:18:35 GMT  
		Size: 61.9 MB (61898433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f20d4b16748272026d508703532e62ad1f72e903aaef04835eddd35e1decfdb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b962f3d7ce0aa2602c4d46b70ba89b538cdeafedebdb91bd90afa6ec3a1251e`

```dockerfile
```

-	Layers:
	-	`sha256:693052ed3df2b83fde4fa0800280114d8462930cdccb7241a2ca16b00cb08dbb`  
		Last Modified: Tue, 03 Dec 2024 17:18:33 GMT  
		Size: 7.7 MB (7672703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db2a8779eafb68a0aed7fc5d3002a09e4385f40c35f0d5b8c3c25910c9afd1e2`  
		Last Modified: Tue, 03 Dec 2024 17:18:32 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d49da1c0ab574f1ee82048183744e7c4a20a58e2630de30576536864742e3b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139699926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1edb438449340747f9d5156a2a723ab8c85b0976e68c66f9498ee726545578dd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9eb21918436f171705acc6e3469286cf27466cc89ea0d17c1699761c888e169c`  
		Last Modified: Tue, 03 Dec 2024 01:32:46 GMT  
		Size: 52.3 MB (52340851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937167b9612f87af0bddfb5d6d68eeee5ceeb8c8e8837f1f9918d7f613aa06c4`  
		Last Modified: Tue, 03 Dec 2024 05:40:08 GMT  
		Size: 20.3 MB (20251872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5eb80243bfd344e12541595272ea8f33faae6f5a77fc26a37baef8d6c8ea36`  
		Last Modified: Tue, 03 Dec 2024 11:52:25 GMT  
		Size: 67.1 MB (67107203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9b7a4e8e3b0b85db390656b6b8cca5621a23e152efdffe411a8f9d5475cd97dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7690453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bca429ac0be19736a53bcdd86c8110a6b3d096b8578d09b9e8cc4847630157e`

```dockerfile
```

-	Layers:
	-	`sha256:875d04078eea0a2500a40cad84a0a00885b05d146a2b6d2e56489b96860538cb`  
		Last Modified: Tue, 03 Dec 2024 11:52:23 GMT  
		Size: 7.7 MB (7683060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4fb854e6b21f3d5083b4dd91df66eed9eacff04eac2761219dc9f5beb7ad194`  
		Last Modified: Tue, 03 Dec 2024 11:52:23 GMT  
		Size: 7.4 KB (7393 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:719ff7c42eefa5f6811c72f3d92c194797cadf5b65455e346d3cb3e9b7705616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.5 MB (143544476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e3ad359f205a750b81d425ca9d2f51cd5eeefadb8cd309a411bc9397fd7e21`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1a5aa91e83fa5cc5d15dce96bbfdc6d2483a659fdee76a341522b60ff87dc849`  
		Last Modified: Tue, 03 Dec 2024 01:27:32 GMT  
		Size: 53.0 MB (52956284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79565d36fc8ccc76d07975f07b5cf916b84627952cb6785e10e8d0301cc2acdd`  
		Last Modified: Tue, 03 Dec 2024 02:14:48 GMT  
		Size: 21.7 MB (21726798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad782586fddb10041571d568c827bae913dd109647631cce2fe893ecfe4b9488`  
		Last Modified: Tue, 03 Dec 2024 03:17:11 GMT  
		Size: 68.9 MB (68861394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:535718f08215a34be3c30316648e76a757427791ab2fd9e70495b1e6a5e58b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7675497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa66fa78d05f3be959bc718b8f26030aa9c1a00679251a79660446336a3ffee`

```dockerfile
```

-	Layers:
	-	`sha256:d64db0dc614cd414a9d0e4644feae150e0f1e8c7eda3e0b58ee2612315e3f67e`  
		Last Modified: Tue, 03 Dec 2024 03:17:10 GMT  
		Size: 7.7 MB (7668205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c80bd9ae34e9602bb84c05a4ddf8a0caa783edcbe6ea469738ea67b68efdc55`  
		Last Modified: Tue, 03 Dec 2024 03:17:09 GMT  
		Size: 7.3 KB (7292 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:c079df95e76a9a8894714db9abb0277635d739c02b9038af4c21f30993c8cd2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138304433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3d5dd81e344958a5a800b0939a8ef1c7fc30d9d447fcd4586c175cb5aad950`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e5a8d7ead1bc1f754b3a65ff28bee76dc2dc6179a698bf1402b64ec3d987e4e2`  
		Last Modified: Tue, 03 Dec 2024 01:30:45 GMT  
		Size: 51.4 MB (51439925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6d7c128c8894ab5647ca7070a8c53cc1626367f0fee2913a8ce5fe2237ac2e`  
		Last Modified: Tue, 03 Dec 2024 15:48:58 GMT  
		Size: 21.0 MB (20951581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddd6435addf48f219bf6a9a7272ed63c493377979c37d721428b6d2c65dab1f`  
		Last Modified: Tue, 03 Dec 2024 23:28:11 GMT  
		Size: 65.9 MB (65912927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ac901c44bfa9f9e8c10c0c7241b6e2071a9ce15aca6b3ff64884cc0a7debc7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efaf51db1c3fa8cb7c637485809ed264d0f11848e68054597ad746478f6a6130`

```dockerfile
```

-	Layers:
	-	`sha256:67a2e9f6b9101e016ca82f90ddb239e70c70d069ab2d1ff8fe9468b7dfab7232`  
		Last Modified: Tue, 03 Dec 2024 23:28:05 GMT  
		Size: 7.1 KB (7147 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:29106e083d3f0884ff2ab67cab04de54b2948f989c84c1de72a1ceb5d72f2900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.4 MB (150416706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ec1fbf43792ca3ab0d994b9fbdf8d4c8fc7e96b90202e42e6e6c01520a25cb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5e74ce1d603959ee7e791ff530dd1c46ce3dbdbf2d00f3d3917cd370d2c2ca56`  
		Last Modified: Tue, 03 Dec 2024 01:31:51 GMT  
		Size: 56.0 MB (55955673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e3c1d8feca2b36465cdfb5b57d9969f0fb66fe43bf079a81607bc309440b99`  
		Last Modified: Tue, 03 Dec 2024 04:38:34 GMT  
		Size: 22.0 MB (21990810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f35d27e17f5faa7b717fcd51d2689cc9f5f0b57184433a4eae97a42f95da04f`  
		Last Modified: Tue, 03 Dec 2024 09:44:41 GMT  
		Size: 72.5 MB (72470223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d7a5f51f1d75eb637e939fe2c1d001071a9ffca3db92bd98f0f44b1414ddf061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7686565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be05632c83a4dc663ff459ace817ccabda153cf61714e31816283eed707acf41`

```dockerfile
```

-	Layers:
	-	`sha256:e80dad17cad41492690720cb23ab6f99daa18133ee238fccb5bfbdfefd17ab40`  
		Last Modified: Tue, 03 Dec 2024 09:44:39 GMT  
		Size: 7.7 MB (7679219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:413f4d207e490cadfa1567ed05b98441f383ecc08e32f7c8d9168196cbb75d3b`  
		Last Modified: Tue, 03 Dec 2024 09:44:38 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7cbdb5aaa9bdb372290824b75edeb47013f021005307c350766138665edeb373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141874600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a0fb9ae5e7d29b1b0cf491d5393a5ac639936cf966ffa23da517254253e92f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:33a597a4ae2eff9c605f460e3e4517cc31e0999c816baef2a6ee6ab3da5c61ec`  
		Last Modified: Tue, 03 Dec 2024 01:31:39 GMT  
		Size: 52.1 MB (52069406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3f8d29d82faa501360f9fefd446cacd0bf557a29588aa4fc37c50e750000a3`  
		Last Modified: Tue, 03 Dec 2024 04:09:18 GMT  
		Size: 21.7 MB (21710113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0425f6ff87e23ba6d559005a68cf32aede99d5bc0259e82af81721ec006b580`  
		Last Modified: Tue, 03 Dec 2024 07:56:17 GMT  
		Size: 68.1 MB (68095081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:39a2f7b3b1fb4e73530d08d088bcd30eafd6d5d786bc9387b653d8f8d8b3ba55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c702e9c9410935d4299af789c96c665239bfb53818cf765a6699f89a9cca41`

```dockerfile
```

-	Layers:
	-	`sha256:a366d37dc4c5fab3169fa8005fbfd07ec0cdacfc63c176b0074314ab29054942`  
		Last Modified: Tue, 03 Dec 2024 07:56:16 GMT  
		Size: 7.7 MB (7673077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13d3948af2dd637e8a6e5a87efaa2a0c83e3771e6c96a7300299f8a4fa0515d9`  
		Last Modified: Tue, 03 Dec 2024 07:56:15 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:41fb2e2f70ae250becde9d66e7993eba6398121f63259e896c29939023f48122
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:unstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:49a2b3da37cd499dea1130c7499ba1292cf6df9b0d9bbc31110bdb1f8cd8126e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.1 MB (376109677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6424a40167b63cc5bfd53ad8a9fed4471a02461aa8f996b50244a9cee25eb306`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9d0fec2ddc88227c9ea9ee67204e0e6a57a98553e405c78f6403be7627bc3834`  
		Last Modified: Tue, 03 Dec 2024 01:27:34 GMT  
		Size: 52.1 MB (52141610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e69332be439e88615e518602f8f7a133592f44d454cc5181ec830b7d4907dc`  
		Last Modified: Tue, 03 Dec 2024 02:28:57 GMT  
		Size: 21.4 MB (21366193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b9b96ccb05d400b1173a82c26d045cd47d1fcb41dec65a7bdc799295c8199e0`  
		Last Modified: Tue, 03 Dec 2024 03:17:08 GMT  
		Size: 67.2 MB (67204217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5aca1310c7893c8969698b84214f772ad0bb081926610513c433a74753433a6`  
		Last Modified: Tue, 03 Dec 2024 04:32:32 GMT  
		Size: 235.4 MB (235397657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cd46236b51a0c0457f02a62e58b36d7a2479b238241f6023be4d6f665e9a7203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16966812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee490560fe66570d36e832a5d2af23d37a6fb0193b9dd060959382f8722c7c2`

```dockerfile
```

-	Layers:
	-	`sha256:95ea3aa99343091b6c530e5b4003bb9943baa3728eec9189ceaf82ac8f4d10a7`  
		Last Modified: Tue, 03 Dec 2024 04:32:29 GMT  
		Size: 17.0 MB (16956636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:347ee90123489714c8c51b8c101dad86568718f1d6cf9349528215be573dd0a5`  
		Last Modified: Tue, 03 Dec 2024 04:32:27 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:fc11ba063b82a26c1aaaf9ff913e2f42b38968fc96aabba5f348fa24bb84e2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.6 MB (339648124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2412990718bb4a573f9f18cbe21335f389216ae3a56619ded3e9fe3a2d1b79f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:73a543e699956c37f431f5272a06bec8db5c16078190c6cd83886ca8de7b3dce`  
		Last Modified: Tue, 03 Dec 2024 01:27:39 GMT  
		Size: 48.7 MB (48676786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f2a807b7a079a7e314d111ccef3f84d1aec497cac9fbafa581f1603c0f9618`  
		Last Modified: Tue, 03 Dec 2024 05:24:32 GMT  
		Size: 20.3 MB (20286838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f15a8cfecadeff23ef5dad822a05b369166f8b1b8b5de808578d74b36d40854`  
		Last Modified: Tue, 03 Dec 2024 08:41:19 GMT  
		Size: 64.5 MB (64485676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f1d176aaf0da811a990a68b00d62be046f5280d8af55d181ec19374dc20c48`  
		Last Modified: Tue, 03 Dec 2024 10:09:16 GMT  
		Size: 206.2 MB (206198824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e16dc7b915d3d0791b2041d90a71ecc8ea1c0bf99101bf3b662e76079e74796e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16726539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66439361d67768c2375720d24cefced238c05f8ac79e1bde6cc06c0da714b789`

```dockerfile
```

-	Layers:
	-	`sha256:866634565228e1d5aa4a5e80f89ce85ac632f579ef0877313377f0be77c0ae38`  
		Last Modified: Tue, 03 Dec 2024 10:09:11 GMT  
		Size: 16.7 MB (16716303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f9ad5080cd41fe18f0fc7d92d9fa984cebecf82fc59f5b44440982d9eeb3217`  
		Last Modified: Tue, 03 Dec 2024 10:09:10 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:55385985caedb19950b81c9de475696914e04672e836beb3c49f895ae604d806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.7 MB (321702301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b34f202cc9b7e97c8977b98f75093537b9a0ac583436bf3e2f98d37f2cb5d5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b3be1b8d31fc4a12cecca1f9e259b73553bed584845788fd1fc2b66b29ec0da2`  
		Last Modified: Tue, 03 Dec 2024 01:29:47 GMT  
		Size: 46.7 MB (46707234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9942887cd0e4c0dbd616c261161d431660cfe04df19f0fb88f7040ab43995e`  
		Last Modified: Tue, 03 Dec 2024 07:37:28 GMT  
		Size: 19.6 MB (19598543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e09ace64d434f04ef956980b3273a080b684493925dd0ee78451c801f466f0`  
		Last Modified: Tue, 03 Dec 2024 17:17:42 GMT  
		Size: 62.0 MB (62009521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff06fd2d61b65d377aaab6adf0bb8120fbb9c2e98330722bd3c1c1dac2b6a938`  
		Last Modified: Tue, 03 Dec 2024 20:09:22 GMT  
		Size: 193.4 MB (193387003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1c7748deb3acaee05b2c2a23e55bac1b3ea86610b8cf98f2701b585873e98aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16732337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f9154eeb6c0b65c758f69fdaefe7849c9ba13a1080413b077e77af7aab7be1`

```dockerfile
```

-	Layers:
	-	`sha256:a3774835b78bdec0bc10768902dd8784a7302b6c4bda4c4f4f571b9c60c0ac2b`  
		Last Modified: Tue, 03 Dec 2024 20:09:18 GMT  
		Size: 16.7 MB (16722101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06696dd3871b1157c5fa70e82fdb3835c17190237bc1370b85860a2e7e8e6981`  
		Last Modified: Tue, 03 Dec 2024 20:09:17 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ca61d6852b240556b0c5025d7f1014496fd6dbd6959ba15284125e8f227db88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.6 MB (367594810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca9c8a6d0a7704491e80b1b6051b22b8da2b45b5ab7c289a8b4b898bdb2403e1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b484292747a3f8af5e498e897086e128c39ecc7aa3e027f8ce6a7b27ab3585c8`  
		Last Modified: Tue, 03 Dec 2024 01:31:21 GMT  
		Size: 52.4 MB (52363551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb4e12ac809713029b921818f315112d9a68fd814039c91956b3cdd9d07cd03`  
		Last Modified: Tue, 03 Dec 2024 05:39:40 GMT  
		Size: 21.0 MB (20983976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620061c3ebb2b35dbb417affed40f3038b1d12ab7ec1b666d509e18d8cc8ad18`  
		Last Modified: Tue, 03 Dec 2024 11:51:44 GMT  
		Size: 67.2 MB (67165131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5b28a91332cf32753c210d1c85e5266c3b7e92424235f8727d4db4f66ded61`  
		Last Modified: Tue, 03 Dec 2024 16:23:31 GMT  
		Size: 227.1 MB (227082152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7394f0f1c8a9b15dccaa6fefc028952784772f293e1527e33fc2efc01fc6f8f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17052000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0acf323e37d0ebafb9b1996e2fb4dd9c969df7be1b7497e4bbd149a119488abd`

```dockerfile
```

-	Layers:
	-	`sha256:f4a8d74b3828d20c625ad2d3d2553dfff0eea81de99a2522eaa7d503bbb04182`  
		Last Modified: Tue, 03 Dec 2024 16:23:27 GMT  
		Size: 17.0 MB (17041744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6d829fcc8e021404ee2581ca56cf93a9bf72b86fc9de94a648f2798d2f734be`  
		Last Modified: Tue, 03 Dec 2024 16:23:26 GMT  
		Size: 10.3 KB (10256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d366ce6267a346f53038978516f23bd4d6ee034c737fe7bdf5d54debb9dd3ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.2 MB (384246787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6f01c0e2e128b69c8f5020fffbdb84045ec77cd5254f9d865979f7e15f3029`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ef86bca2ffea293f73079f660a3399886008871df454d90312b7145d4395af98`  
		Last Modified: Tue, 03 Dec 2024 01:27:14 GMT  
		Size: 53.0 MB (52973420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183206547155d13d62e451041e3603fd7f5a0f4b1d6c8db0eaaf7ca1b4e51b07`  
		Last Modified: Tue, 03 Dec 2024 02:14:44 GMT  
		Size: 22.5 MB (22527751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8dd8a498f4405479d9e2bf04b4ed73d5dc63deb1d79c9d70eec7ddd7add1c35`  
		Last Modified: Tue, 03 Dec 2024 03:17:09 GMT  
		Size: 69.1 MB (69057622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b49bfdd692e8513701b0f0d930158f3f4d2aef5d64dff7bc22f6ccce56cf71b`  
		Last Modified: Tue, 03 Dec 2024 04:32:15 GMT  
		Size: 239.7 MB (239687994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7223f9d88774500fc3d64c0972df630401a88904948b414d81db8a6657f26dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16936367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff36bf12fbb75872174d04ce6204332f1de5ce54543955ba832418a0bee14ad`

```dockerfile
```

-	Layers:
	-	`sha256:4b6ef7d7bc0977f2ee04016de60f61d61f1e875ffc5ded21289b535075ef5236`  
		Last Modified: Tue, 03 Dec 2024 04:32:10 GMT  
		Size: 16.9 MB (16926213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7ada5f052e281d272d1947417f47424ce48e4072642dfae1ee7e16d1720a591`  
		Last Modified: Tue, 03 Dec 2024 04:32:09 GMT  
		Size: 10.2 KB (10154 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:97caf8af9ccb753cb7f0a15dd4d6e7b85df199b941e53e473528de89c603957f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.7 MB (352719608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62f24378805246617f053066f67939fc8f86f8c2e0536c869801c4c57300b4a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:547779e8d3d4ddde41b340ccc5c55eed6547696507cc0168eca950de620def24`  
		Last Modified: Tue, 03 Dec 2024 01:28:45 GMT  
		Size: 51.5 MB (51502465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fd17db4d55a0362abe181f4687b9308ab24eba56bf7c357aaf0150dda37b50`  
		Last Modified: Tue, 03 Dec 2024 15:47:12 GMT  
		Size: 21.7 MB (21747415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faad181192abe7945e2597dbe5a13adb7a6c4fc91c9cc8ed7907444e118bfa3f`  
		Last Modified: Tue, 03 Dec 2024 23:25:18 GMT  
		Size: 66.1 MB (66061059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df5e2e3f8704cd8f57eadead12d86fce2f48f9c5471960a3d7caa911e1ba9be`  
		Last Modified: Wed, 04 Dec 2024 04:49:12 GMT  
		Size: 213.4 MB (213408669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a8fc1d3466ccfed6239df0794a374e4154c2dbe91e7dfb3c88eb714ec9781125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab85850533c58616e5ba9342b19d94baa414e3caae56b247f2fd7324b4e2aba1`

```dockerfile
```

-	Layers:
	-	`sha256:e8a2386f905b3062ec0484433f9fdb32f3b1814e63a581a4fb0f013698107e33`  
		Last Modified: Wed, 04 Dec 2024 04:48:53 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6bc19564fe24be256fafa93692fee2e057f1bfce2a467077582364c36f312501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.1 MB (383146258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b3a3d439cd386298430241ef8eb9396878bfeb4ed9bef7199ba205959d5ef3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f96af90d82a1692028e6cdf912ac7419c2ecdd75603a19fc1f1b3b9e9bd29a53`  
		Last Modified: Tue, 03 Dec 2024 01:29:07 GMT  
		Size: 56.0 MB (55979543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5109fb930f5078004be0affb782c6af72db917a8e8c95675e33088c19131df3`  
		Last Modified: Tue, 03 Dec 2024 04:37:41 GMT  
		Size: 22.8 MB (22802436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77093ba8fdd419c4df155b02b29ff2686cd2a1d51168effbff5b4e39d31c96b6`  
		Last Modified: Tue, 03 Dec 2024 09:43:21 GMT  
		Size: 72.5 MB (72483296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a580742dd0d6b25eae1fa9319e34f6aec541ba477a9cef1cdf4484b82dd70279`  
		Last Modified: Tue, 03 Dec 2024 16:17:11 GMT  
		Size: 231.9 MB (231880983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5e0b7842efee0560cbb97a8bf463f8ce0017e26ab3fb70853b19dfd42cf19f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16947386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490dc7b944706942ddc307593cfcf31eb6789669a5421161813ca686742e43d3`

```dockerfile
```

-	Layers:
	-	`sha256:adea640ebcb9f657019594233f9ed28bb4fd297667bf3496b4bc59c52d3184df`  
		Last Modified: Tue, 03 Dec 2024 16:17:06 GMT  
		Size: 16.9 MB (16937178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:317a52d715af8ed8e9f6aa2c264eaf47458539127bf4f5013692e6e37b8712e3`  
		Last Modified: Tue, 03 Dec 2024 16:17:05 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:28f75fbff7fea1754f66f2ff9c7640c4c06fd16ffdfc224eb2f8fd1772f538b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **457.0 MB (456979288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155400acc66a00f8f4f35c553e7f4f9c8e73796171ecaec90abeb17edf42806a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6a129056497962be3ca4efb9ff44f747d1222200200be5fae7999b10e3156cc0`  
		Last Modified: Tue, 03 Dec 2024 01:29:15 GMT  
		Size: 50.6 MB (50632627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d233c7b4fb57ebb3fc06e5b0c070fac8c8f89639814479f25441c1938943ba`  
		Last Modified: Tue, 03 Dec 2024 02:51:09 GMT  
		Size: 20.8 MB (20822777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f14784271331931f12f38e0de1c6c4183501776dd43b01c47876c85796c8558`  
		Last Modified: Tue, 03 Dec 2024 06:42:00 GMT  
		Size: 66.2 MB (66176026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916fb889a6cd610a8a181a1ed9f57ffa7abe21fee8ea8ac8ad30325ce0b47c57`  
		Last Modified: Tue, 03 Dec 2024 09:46:02 GMT  
		Size: 319.3 MB (319347858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:aa374b77f1ca17f70075124a2c8053c4dafb365a746fcadab9fbd94e0e9c1a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17012542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857a6ebeb6a5606160740b66667e437826698b5d6d0790a7f6fd64dc0e8d105b`

```dockerfile
```

-	Layers:
	-	`sha256:a43d787d954c874af6db8dbc822b7d6e42a06c9c0cef5bcd7c1559891005d498`  
		Last Modified: Tue, 03 Dec 2024 09:45:19 GMT  
		Size: 17.0 MB (17002334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a213c48f55ff98d0845193b83743c6cf5dedca52db3ce6eab0b9aff84a3cf00`  
		Last Modified: Tue, 03 Dec 2024 09:45:16 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1df3ba79cb55d883ad913395b36a513bfc917c15b7caf38cd88c8c665777683c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.7 MB (349670575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b982bb3ebcb5f081cb00461966a8802023bcb16a8a774a3730540353081667e2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5d3fd94703dd00b00c7acc09539942c89a4634b13c2ae0ee29086b6288d43a47`  
		Last Modified: Tue, 03 Dec 2024 01:29:01 GMT  
		Size: 52.1 MB (52083835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79c38d4fbdb1d980e95882f99ea9064cdd90b1c1070a263467e442acb813b03`  
		Last Modified: Tue, 03 Dec 2024 04:08:31 GMT  
		Size: 22.6 MB (22559777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1dd971e7560ef90c41327cadf96b46eeb95360bc6b43dff330bf117ebb3df64`  
		Last Modified: Tue, 03 Dec 2024 07:55:00 GMT  
		Size: 68.3 MB (68263935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f973d95ee4eb4554be6abf2f8a00814eee05529e41a4930c8ffae282529578`  
		Last Modified: Tue, 03 Dec 2024 10:44:48 GMT  
		Size: 206.8 MB (206763028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fe39f39f7f1bde3d6c9e5c818bc628469875b2aa3b927edc66c74bf70a22412b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16747718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ebe5f6db202526925c56ad1faf6b865d027a0465734a2288e2f1ecc5c74d2b`

```dockerfile
```

-	Layers:
	-	`sha256:3d93d11363e6dc9d7925d0a3b5dbdca207392f40e1f417fe1bace7d8da06f1be`  
		Last Modified: Tue, 03 Dec 2024 10:44:38 GMT  
		Size: 16.7 MB (16737543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:125fd07fab195f7bfaf54230410ce6eb672c899fbd818dc4533083b58c05c9d2`  
		Last Modified: Tue, 03 Dec 2024 10:44:38 GMT  
		Size: 10.2 KB (10175 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:f5e71aa29f2601128aa7050df6278f4f29c1bb8bc57a61344d969e0124f2d910
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:204fc7cb93e6b1c5d3701d9bb7b17f47f36c32312b13aab7a3e1eecb149cae55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73507803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d3aa6b1c65c3ca1c85ad847490f6b3aaaa53facd8fbf401d4ddec6b5807971`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9d0fec2ddc88227c9ea9ee67204e0e6a57a98553e405c78f6403be7627bc3834`  
		Last Modified: Tue, 03 Dec 2024 01:27:34 GMT  
		Size: 52.1 MB (52141610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e69332be439e88615e518602f8f7a133592f44d454cc5181ec830b7d4907dc`  
		Last Modified: Tue, 03 Dec 2024 02:28:57 GMT  
		Size: 21.4 MB (21366193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3c19b6e7dc1bfd1817f85314eb3cad6f9b646341f80cd03cd40656b1ede3672b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4050455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15c4d7443fd64f1c8254c1ccb0d676a805bf354e184fbf250932ab147b99693`

```dockerfile
```

-	Layers:
	-	`sha256:8b30370abcd3c800357528cee52c171f19f828ebd96c3d2beb8fb8bb113da450`  
		Last Modified: Tue, 03 Dec 2024 02:28:56 GMT  
		Size: 4.0 MB (4043653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44bc99210dbb035b3c8e40a98c8830893bcf5823bcaab362c506ced9d2e06c17`  
		Last Modified: Tue, 03 Dec 2024 02:28:56 GMT  
		Size: 6.8 KB (6802 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e0c26364853da5e75896f031d3d2066ca0b0ebea6064c0802e48cb002b909a39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68963624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2e1229b95235bac1c5cbcf446d7e9e39ec403dd559a52fa597f5ea92286169`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:73a543e699956c37f431f5272a06bec8db5c16078190c6cd83886ca8de7b3dce`  
		Last Modified: Tue, 03 Dec 2024 01:27:39 GMT  
		Size: 48.7 MB (48676786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f2a807b7a079a7e314d111ccef3f84d1aec497cac9fbafa581f1603c0f9618`  
		Last Modified: Tue, 03 Dec 2024 05:24:32 GMT  
		Size: 20.3 MB (20286838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:81227ab69595f9829c5e51c760a792f754393155a80fa9e5c7ea97270b64b66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4052738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd6a50c2ec5b6f28659d8ac5731b5b191b0bef1493df2890fece6c6bda7b1918`

```dockerfile
```

-	Layers:
	-	`sha256:8a6d09a593299d0ecf8ccbedf48989b9fa1e80596cba5f0888fd729d08e03de0`  
		Last Modified: Tue, 03 Dec 2024 05:24:31 GMT  
		Size: 4.0 MB (4045875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3815fe36d9422647ced3357e6453c8f5a123a633108c99d47a75621924d53a30`  
		Last Modified: Tue, 03 Dec 2024 05:24:31 GMT  
		Size: 6.9 KB (6863 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:cc4b2bdff03629d69feb728d273e0d532e0d425550d77fc4d428a98662e506ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66305777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08dd76319b781f4765aebe68e8f8f83425d978da56b8908c1f9a09fd10cd4fac`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b3be1b8d31fc4a12cecca1f9e259b73553bed584845788fd1fc2b66b29ec0da2`  
		Last Modified: Tue, 03 Dec 2024 01:29:47 GMT  
		Size: 46.7 MB (46707234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9942887cd0e4c0dbd616c261161d431660cfe04df19f0fb88f7040ab43995e`  
		Last Modified: Tue, 03 Dec 2024 07:37:28 GMT  
		Size: 19.6 MB (19598543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:07eef967eb655fb18f0d2c2c11f4c816279a67bdd59790b99251f3f5e1d908e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18671eba9c6dac63abf5e1aacde8418a8ec079f015aba5a58f71d647b0eb7f11`

```dockerfile
```

-	Layers:
	-	`sha256:a73bb5456d7763921c5061137bf4a7b19f10585c609ef3370e5bd8e6975c4870`  
		Last Modified: Tue, 03 Dec 2024 07:37:27 GMT  
		Size: 4.0 MB (4044673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c5cb0ef0323af3e1a3e008d5e57343569405babcfaa127188257693204bc034`  
		Last Modified: Tue, 03 Dec 2024 07:37:27 GMT  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8ea9887f4714527d9d5254f762de02c92d4f7bae369fa18b0ba9ee5d8a5f7a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73347527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b445d459eed6e2aaa0ca2873d2fef7a47c8f779e4e527578f018fee5542d5d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b484292747a3f8af5e498e897086e128c39ecc7aa3e027f8ce6a7b27ab3585c8`  
		Last Modified: Tue, 03 Dec 2024 01:31:21 GMT  
		Size: 52.4 MB (52363551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb4e12ac809713029b921818f315112d9a68fd814039c91956b3cdd9d07cd03`  
		Last Modified: Tue, 03 Dec 2024 05:39:40 GMT  
		Size: 21.0 MB (20983976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:efb2879bdbe93ed419ee51ad67c5b73260cbe9762f879b6525c357a6a1c79dfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4054793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0104e88a325a66592832bfa12159a43f2db9c0662ddc2a476e9b5b61eefe533`

```dockerfile
```

-	Layers:
	-	`sha256:21a43c5405ce1ce47e7024330b2a77d04d6962e99937eb27750094d8f9088a75`  
		Last Modified: Tue, 03 Dec 2024 05:39:38 GMT  
		Size: 4.0 MB (4047909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e42bbda426096d69b867a0dc63238898e7dbec844f816cdc22f46d8ec7561d9`  
		Last Modified: Tue, 03 Dec 2024 05:39:38 GMT  
		Size: 6.9 KB (6884 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:8dae1c26ca64bef3fd697b7cf02f4b2c366e85a6c73f01b5e0b9afb622c5fdb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75501171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875a11a23487b00a03f1f0044e25daf842fb4cdab0a6dcdb4c3a2f74eda5811d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ef86bca2ffea293f73079f660a3399886008871df454d90312b7145d4395af98`  
		Last Modified: Tue, 03 Dec 2024 01:27:14 GMT  
		Size: 53.0 MB (52973420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183206547155d13d62e451041e3603fd7f5a0f4b1d6c8db0eaaf7ca1b4e51b07`  
		Last Modified: Tue, 03 Dec 2024 02:14:44 GMT  
		Size: 22.5 MB (22527751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fc30c76fa56490aa8d4359be5a51f884a93180fe27ba95093b6f4249461d8ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4046182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526990c3201f01d1bd4d6d57dcf3e812be838f5800ba8ff10188b3839c34d19c`

```dockerfile
```

-	Layers:
	-	`sha256:ef89ebeb6f21e1f73525cefa6b3bb32a2c605d18a8f97b9fd5da7036c0295c46`  
		Last Modified: Tue, 03 Dec 2024 02:14:43 GMT  
		Size: 4.0 MB (4039400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d6a2f676cc8e92c792af6635a13a376cb77dde477c35e1d9465bf4009920b0d`  
		Last Modified: Tue, 03 Dec 2024 02:14:43 GMT  
		Size: 6.8 KB (6782 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:891f8b0644f2ce029fdfb4250af9c7c22f3ffdd76191782fccffef0b9e3b249a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73249880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4673bea9b1756010dfb677b2ee62e809bade3a1de565fe922df855fddf5849aa`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:547779e8d3d4ddde41b340ccc5c55eed6547696507cc0168eca950de620def24`  
		Last Modified: Tue, 03 Dec 2024 01:28:45 GMT  
		Size: 51.5 MB (51502465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fd17db4d55a0362abe181f4687b9308ab24eba56bf7c357aaf0150dda37b50`  
		Last Modified: Tue, 03 Dec 2024 15:47:12 GMT  
		Size: 21.7 MB (21747415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d32b69785698093e0be0f82a00aaef093cb1391c8da6cb9dcea17352e1f56697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 KB (6637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:349e281e55adf0a1012c38c3ecee53c2afce3499397ddf5f3c275529952692a9`

```dockerfile
```

-	Layers:
	-	`sha256:5746c842a00740e7c683b3e380cb5794aef1759e591efcca8935e86ea9691f85`  
		Last Modified: Tue, 03 Dec 2024 15:47:09 GMT  
		Size: 6.6 KB (6637 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:47ee79acdeb89205c257ecbedda3b0eb55e581f832165079a17a7b01cd288b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 MB (78781979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32bcf58578328b1231b58d5b8944d36bc4ba40ee49ae98c44558d7b7ed3a54ea`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f96af90d82a1692028e6cdf912ac7419c2ecdd75603a19fc1f1b3b9e9bd29a53`  
		Last Modified: Tue, 03 Dec 2024 01:29:07 GMT  
		Size: 56.0 MB (55979543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5109fb930f5078004be0affb782c6af72db917a8e8c95675e33088c19131df3`  
		Last Modified: Tue, 03 Dec 2024 04:37:41 GMT  
		Size: 22.8 MB (22802436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1264f415c874219bf1d93ed1a65ffb3823a4a931fed9bcc0dd443056df716e5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4053760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39caff4ffb294476abd1b4095aa9254d65feebe0abe1b8add2b60d2243cee46b`

```dockerfile
```

-	Layers:
	-	`sha256:cf5ac8a981390a4e2c3640c75cbafcab45c0cda33f1490731ff4029c7048ddfc`  
		Last Modified: Tue, 03 Dec 2024 04:37:40 GMT  
		Size: 4.0 MB (4046924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9669a33d493726e89d132782bdb9de12e182fd2b8f0009472a97ff07522a0575`  
		Last Modified: Tue, 03 Dec 2024 04:37:40 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:b586a30adedcf91253b4e723a2fb98577d3112ba0edafae4a3169cbbe4b467c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71455404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f858b529436819defd2e23a4d8d4cc35636897a62586414cf76f538931ad6e5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6a129056497962be3ca4efb9ff44f747d1222200200be5fae7999b10e3156cc0`  
		Last Modified: Tue, 03 Dec 2024 01:29:15 GMT  
		Size: 50.6 MB (50632627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d233c7b4fb57ebb3fc06e5b0c070fac8c8f89639814479f25441c1938943ba`  
		Last Modified: Tue, 03 Dec 2024 02:51:09 GMT  
		Size: 20.8 MB (20822777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d4b9830bd87fccccf6e3080d90de56b90eaabeba62546b0628aefaa4ae2da16b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4043359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103e57e6a56d779b28625d6494beb70b785b3fc5feb250ae02f6560c186c31de`

```dockerfile
```

-	Layers:
	-	`sha256:bbef88f018a4f6f847dcbacbd9fae201001983766aaa9ba52cf76fcc836d22c6`  
		Last Modified: Tue, 03 Dec 2024 02:51:06 GMT  
		Size: 4.0 MB (4036523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f42fe56ae477e436b08ca6348817a884c70598cd0cf20f64af658727e556813`  
		Last Modified: Tue, 03 Dec 2024 02:51:06 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:aa8bd5667c1e53625735710349a9740d77fa5aaa879d3a977adf6247b361421c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74643612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4653b03d76739840fe4be4479dc8274aefd31736a0302005a389e88cbf472bc0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5d3fd94703dd00b00c7acc09539942c89a4634b13c2ae0ee29086b6288d43a47`  
		Last Modified: Tue, 03 Dec 2024 01:29:01 GMT  
		Size: 52.1 MB (52083835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79c38d4fbdb1d980e95882f99ea9064cdd90b1c1070a263467e442acb813b03`  
		Last Modified: Tue, 03 Dec 2024 04:08:31 GMT  
		Size: 22.6 MB (22559777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c50b19b70400d98afbb0a18ed63e699890ce23cddf01fc0abb0fbfe916dbfe6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4056542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0cb0567221a8fdf7e234accf3825319db8e5a4ce9cfa46e3d7f786610a1bdb5`

```dockerfile
```

-	Layers:
	-	`sha256:0e58fd28fae7b037ea9d243d9a380a50fd4bf594f2960b0e40d34a4510d2522c`  
		Last Modified: Tue, 03 Dec 2024 04:08:31 GMT  
		Size: 4.0 MB (4049739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:367e00e07da6a96ad160be887964afb0f841afb80806423c924a594dcf18c990`  
		Last Modified: Tue, 03 Dec 2024 04:08:31 GMT  
		Size: 6.8 KB (6803 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:5d3a345d10db23f764771a5183825102d0412407a3c3e7a1b3241422f8342781
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:unstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:98ae8322e21402d9d1a47ae330578c281bedd95f82e7551694698c1c73d150b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140712020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff602ec12cae508a5eff7f955f1f3b4a7b0116e7f63fd95e3aede38e2531f3b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9d0fec2ddc88227c9ea9ee67204e0e6a57a98553e405c78f6403be7627bc3834`  
		Last Modified: Tue, 03 Dec 2024 01:27:34 GMT  
		Size: 52.1 MB (52141610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e69332be439e88615e518602f8f7a133592f44d454cc5181ec830b7d4907dc`  
		Last Modified: Tue, 03 Dec 2024 02:28:57 GMT  
		Size: 21.4 MB (21366193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b9b96ccb05d400b1173a82c26d045cd47d1fcb41dec65a7bdc799295c8199e0`  
		Last Modified: Tue, 03 Dec 2024 03:17:08 GMT  
		Size: 67.2 MB (67204217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c7f7f8c9fe198f76ea4d557014b74867442af6b19728ed19e19b5db24d2c9787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7673901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9655e2d30b820946d8a9271aebee6149dad6dd472e02bd0dd2490a28bc82a1`

```dockerfile
```

-	Layers:
	-	`sha256:9b8dcc9e196bdf56ae35756553a098b57ee3322218cfe81f94b8d219dffaf1cf`  
		Last Modified: Tue, 03 Dec 2024 03:17:07 GMT  
		Size: 7.7 MB (7666604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cb4b8ce456f309d5ac4f45927a3297061e4c2e8acfb4c80126d9bf3ee145d25`  
		Last Modified: Tue, 03 Dec 2024 03:17:07 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:2966584a59d9e0b9d32e6387a215e424e5bc2afa5c60c678e1a02c0fe9157edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.4 MB (133449300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d6416fa362396520065273d8b095ca52c840c3f07b1a58aff7022f82309846`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:73a543e699956c37f431f5272a06bec8db5c16078190c6cd83886ca8de7b3dce`  
		Last Modified: Tue, 03 Dec 2024 01:27:39 GMT  
		Size: 48.7 MB (48676786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f2a807b7a079a7e314d111ccef3f84d1aec497cac9fbafa581f1603c0f9618`  
		Last Modified: Tue, 03 Dec 2024 05:24:32 GMT  
		Size: 20.3 MB (20286838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f15a8cfecadeff23ef5dad822a05b369166f8b1b8b5de808578d74b36d40854`  
		Last Modified: Tue, 03 Dec 2024 08:41:19 GMT  
		Size: 64.5 MB (64485676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:774970a968d4bd940468709784d0674f8143d9516348b45292c1efa99c37307a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7674236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a1bbb775be08af72d3f2b911e5d67dc53477881a4678e428606938e9329a5f1`

```dockerfile
```

-	Layers:
	-	`sha256:be2af54aca073400cedd5c0c72179622b7d427625d2e6476881c2fd812ffaa14`  
		Last Modified: Tue, 03 Dec 2024 08:41:17 GMT  
		Size: 7.7 MB (7666879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b328f7f3ac3c501a7f6ae35a51e43d86de914bbc0bad3222005f311fcd396127`  
		Last Modified: Tue, 03 Dec 2024 08:41:17 GMT  
		Size: 7.4 KB (7357 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:387e61670c0dd5342002ec5ff918f89043546aeb014c47740d6a6eb73e793cf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128315298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83744aacda8eb7e6caeaf7ffde4ac82bdcb20f28f3e0fd1209a6eb0f6e93d062`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b3be1b8d31fc4a12cecca1f9e259b73553bed584845788fd1fc2b66b29ec0da2`  
		Last Modified: Tue, 03 Dec 2024 01:29:47 GMT  
		Size: 46.7 MB (46707234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9942887cd0e4c0dbd616c261161d431660cfe04df19f0fb88f7040ab43995e`  
		Last Modified: Tue, 03 Dec 2024 07:37:28 GMT  
		Size: 19.6 MB (19598543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e09ace64d434f04ef956980b3273a080b684493925dd0ee78451c801f466f0`  
		Last Modified: Tue, 03 Dec 2024 17:17:42 GMT  
		Size: 62.0 MB (62009521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1dc94d5835984fdc1913e5dac619d4dde7f4a1411d27b563c296a3ac14bc1397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7674007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2b45b5bbe0d268dbd9fbef0e1d7003f86def947cd36bdd6998c1492df05c71`

```dockerfile
```

-	Layers:
	-	`sha256:1b67bdad54ee7d3cf3d2bed02ab7da4f2712603a6854f36a13d5422c730edd72`  
		Last Modified: Tue, 03 Dec 2024 17:17:40 GMT  
		Size: 7.7 MB (7666651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3f1e3c2cd17fdeaa8aab05283566fc3819f300894aa57674c19ce25ecbe50a1`  
		Last Modified: Tue, 03 Dec 2024 17:17:40 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ba6f42ba7aefae054d5f3f1bb2c078cc0b42154bf67985259ea51890f16e92f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140512658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4bc14651d67b3d787ab2c20f60a20cd4624ada311d68df39bb40b296c58f4c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b484292747a3f8af5e498e897086e128c39ecc7aa3e027f8ce6a7b27ab3585c8`  
		Last Modified: Tue, 03 Dec 2024 01:31:21 GMT  
		Size: 52.4 MB (52363551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb4e12ac809713029b921818f315112d9a68fd814039c91956b3cdd9d07cd03`  
		Last Modified: Tue, 03 Dec 2024 05:39:40 GMT  
		Size: 21.0 MB (20983976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620061c3ebb2b35dbb417affed40f3038b1d12ab7ec1b666d509e18d8cc8ad18`  
		Last Modified: Tue, 03 Dec 2024 11:51:44 GMT  
		Size: 67.2 MB (67165131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:aa757aa7912e5aa5e678a45ae35e15003eb74a602d8da40aa9ffaf5e93f5a840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7684385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ff85394930bde7b388d9d6c1cf7bab862637d3629f3cdb3e6953a2fced1b40`

```dockerfile
```

-	Layers:
	-	`sha256:035677f5fb6f054407dcea7a584fe83af8c3343ee7a4ee69e62dfb3955679e5b`  
		Last Modified: Tue, 03 Dec 2024 11:51:42 GMT  
		Size: 7.7 MB (7677008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbdd037048e81b72bd044d348d4ce9bb4e7a97b2f9ee3680fd1ae6a27f7622c9`  
		Last Modified: Tue, 03 Dec 2024 11:51:42 GMT  
		Size: 7.4 KB (7377 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:28aa3b92afdeceb776855973c3b211c28230c89a81b458bb7e67b11d8cefe2e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144558793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afc5aee69b53785c60a0927a7b5c28ef293efdde6e25767537d489ed2d6e1d2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ef86bca2ffea293f73079f660a3399886008871df454d90312b7145d4395af98`  
		Last Modified: Tue, 03 Dec 2024 01:27:14 GMT  
		Size: 53.0 MB (52973420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183206547155d13d62e451041e3603fd7f5a0f4b1d6c8db0eaaf7ca1b4e51b07`  
		Last Modified: Tue, 03 Dec 2024 02:14:44 GMT  
		Size: 22.5 MB (22527751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8dd8a498f4405479d9e2bf04b4ed73d5dc63deb1d79c9d70eec7ddd7add1c35`  
		Last Modified: Tue, 03 Dec 2024 03:17:09 GMT  
		Size: 69.1 MB (69057622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d1de5a48dfe09b9f75e84d47faa561d68418835bb76363623eb981f370a7eeec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7668619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91810c997ab4ca1105aac3782040f194980cc9236686d98672c7a9c1b2c8411`

```dockerfile
```

-	Layers:
	-	`sha256:c5867b09adbc4524a9ca98728702a0177022b1afc0e4e8385d9a61636c8345ae`  
		Last Modified: Tue, 03 Dec 2024 03:17:07 GMT  
		Size: 7.7 MB (7661345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0640817c4ab08d0cfc6d0fb5beaa13797d1e7a88cd7885d6a37b80373ce2b256`  
		Last Modified: Tue, 03 Dec 2024 03:17:06 GMT  
		Size: 7.3 KB (7274 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:1fe95458c2a1597e474ab22eeab992b0dd3ca20270c9cb0ad29e34b758dc1365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.3 MB (139310939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3f05b1af333bd7a1d6548c97aa50a24c70ffe4d0dfb262d84bda07341eee6d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:547779e8d3d4ddde41b340ccc5c55eed6547696507cc0168eca950de620def24`  
		Last Modified: Tue, 03 Dec 2024 01:28:45 GMT  
		Size: 51.5 MB (51502465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fd17db4d55a0362abe181f4687b9308ab24eba56bf7c357aaf0150dda37b50`  
		Last Modified: Tue, 03 Dec 2024 15:47:12 GMT  
		Size: 21.7 MB (21747415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faad181192abe7945e2597dbe5a13adb7a6c4fc91c9cc8ed7907444e118bfa3f`  
		Last Modified: Tue, 03 Dec 2024 23:25:18 GMT  
		Size: 66.1 MB (66061059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5c8e5db01f6b4a196282e03ee3a072fdb6b0441419552c9108c75a93cc07190d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:602ee0707cc9c4d48ec4a571aec1a7a4f397e1c9249737bb9ec632733138fac7`

```dockerfile
```

-	Layers:
	-	`sha256:365963a85ceae17855bfd0702f9bc4c91835f90acdc457783db8dc5fb090e31f`  
		Last Modified: Tue, 03 Dec 2024 23:25:11 GMT  
		Size: 7.1 KB (7130 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:59a6796beeb3b9d0867665f4811ee1eee275a710e6a5a458dcc6fb93f8e48524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151265275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75fd8aab6398f04086341d332deb43da5a6cd1a16ef1b5a5e6dc0a987ef76111`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f96af90d82a1692028e6cdf912ac7419c2ecdd75603a19fc1f1b3b9e9bd29a53`  
		Last Modified: Tue, 03 Dec 2024 01:29:07 GMT  
		Size: 56.0 MB (55979543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5109fb930f5078004be0affb782c6af72db917a8e8c95675e33088c19131df3`  
		Last Modified: Tue, 03 Dec 2024 04:37:41 GMT  
		Size: 22.8 MB (22802436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77093ba8fdd419c4df155b02b29ff2686cd2a1d51168effbff5b4e39d31c96b6`  
		Last Modified: Tue, 03 Dec 2024 09:43:21 GMT  
		Size: 72.5 MB (72483296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5af9d705848c2dce3bc462b3b76df9b1b1d306e6bd09c2e26bd22bfc3f0c9876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f651af8b104ea346af37805901de2cc5ba97cf50ebaaa790cf0de9c570f5583f`

```dockerfile
```

-	Layers:
	-	`sha256:1db2caa964222e7b334c9d443db179aa27f6a7916d2932972cac65ad9c1e5d72`  
		Last Modified: Tue, 03 Dec 2024 09:43:19 GMT  
		Size: 7.7 MB (7673155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b523a122ad81c64df21fce3272cb02fca3d3a9206244cbe6d869788cadee4d0`  
		Last Modified: Tue, 03 Dec 2024 09:43:18 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:fc674a43ff201f8797f66dd82257b4196d80d7c095fc868cbe749cb36beeda09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137631430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f17059d9a1dcc6bf58ee32ba614a1fcbe226f8043520b842b184d3a9c6f28ff4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6a129056497962be3ca4efb9ff44f747d1222200200be5fae7999b10e3156cc0`  
		Last Modified: Tue, 03 Dec 2024 01:29:15 GMT  
		Size: 50.6 MB (50632627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d233c7b4fb57ebb3fc06e5b0c070fac8c8f89639814479f25441c1938943ba`  
		Last Modified: Tue, 03 Dec 2024 02:51:09 GMT  
		Size: 20.8 MB (20822777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f14784271331931f12f38e0de1c6c4183501776dd43b01c47876c85796c8558`  
		Last Modified: Tue, 03 Dec 2024 06:42:00 GMT  
		Size: 66.2 MB (66176026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fbd26b4002d80a7a7d2202c479c7daee401e8a0b0b2bc1e4e4d3dff743cc317f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7664095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79590c6ba7424ad6bb084619f4ed4331d5e05aaad65648779da965666f5b52e4`

```dockerfile
```

-	Layers:
	-	`sha256:ee9a4121ef32c4ac3a622baed8c3121fa68a4974fd0e3a4c5b2491d3285a4d59`  
		Last Modified: Tue, 03 Dec 2024 06:41:52 GMT  
		Size: 7.7 MB (7656766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8d83211651559187f1abcb4d829c94f914b0ee443046ecda9f19c4daaef0296`  
		Last Modified: Tue, 03 Dec 2024 06:41:50 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a6e7b7995a1caf452b3d1632d89a67fd503bce71d349a2d66b6b3489271ff30a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.9 MB (142907547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e646e8bc9897fc238aa02a1d8ac855f8561e8a87d9bf6b3034ff59ef5aafae4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5d3fd94703dd00b00c7acc09539942c89a4634b13c2ae0ee29086b6288d43a47`  
		Last Modified: Tue, 03 Dec 2024 01:29:01 GMT  
		Size: 52.1 MB (52083835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79c38d4fbdb1d980e95882f99ea9064cdd90b1c1070a263467e442acb813b03`  
		Last Modified: Tue, 03 Dec 2024 04:08:31 GMT  
		Size: 22.6 MB (22559777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1dd971e7560ef90c41327cadf96b46eeb95360bc6b43dff330bf117ebb3df64`  
		Last Modified: Tue, 03 Dec 2024 07:55:00 GMT  
		Size: 68.3 MB (68263935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:62bdb3d02e3a0d3e18eeefd51b090d298257bf08d95c74c779af75c028b32601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7679482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7371548547570d681cba1e2bec0c6958cf1f1b85b053244a30643706e814711`

```dockerfile
```

-	Layers:
	-	`sha256:baf8d91bd601ab293980e1fbe3335dc904de9a3306b89908c5075675c6676f3e`  
		Last Modified: Tue, 03 Dec 2024 07:54:58 GMT  
		Size: 7.7 MB (7672185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9961d929cf0d31cbf6d32963cbe3e25aedaa9b59f3f87385c96f28d64519dbf`  
		Last Modified: Tue, 03 Dec 2024 07:54:58 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json
