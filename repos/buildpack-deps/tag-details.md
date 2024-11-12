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
$ docker pull buildpack-deps@sha256:a2c379af057a249a7ae251d68571aadf7dd43837219ff38e4e797eaa408cf417
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
$ docker pull buildpack-deps@sha256:28ea314ba57e342bac3799c06c1a8d44cfe585fc0f66bf3719030da3cb2942d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.7 MB (279731027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34bda0190071cc444553b7a709fd8cd57d63a7c2c2186ba13b47282c6abd6acb`
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
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
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
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb10f2d793001e79ccc6be8c28ad194b0142e46f3ea6c14095699bb7ba44ef3c`  
		Last Modified: Sat, 19 Oct 2024 02:06:23 GMT  
		Size: 13.6 MB (13616706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ed9a6a1726d06e0402223e684a198aad45fe01804a81aa58967a03d085b6dd`  
		Last Modified: Sat, 19 Oct 2024 02:52:33 GMT  
		Size: 45.3 MB (45337669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ed0593d2f3316b832ab07d1fbfad306dbde92bee837a9184eb10b2a3300bd0`  
		Last Modified: Sat, 19 Oct 2024 03:53:25 GMT  
		Size: 191.0 MB (191026289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:74cb68ef31f5c607d038fcb183848fcaffb976bd546d14dae852e490e46b56cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11373351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a8a6050b4550be41f53ffa005549538f26068b3cacf2abfa1da72aa307bd59`

```dockerfile
```

-	Layers:
	-	`sha256:d7c719a514e8fc78963ff42a7fb6ebbd21a0ff436cd8a5186432d7a685f011cf`  
		Last Modified: Sat, 19 Oct 2024 03:53:22 GMT  
		Size: 11.4 MB (11363167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c096c09217c24f206f019b6dc90b89e2b27ac53a5d6eaf8626e3d44371ca1646`  
		Last Modified: Sat, 19 Oct 2024 03:53:22 GMT  
		Size: 10.2 KB (10184 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6df0bff9783b406ab00cbbda757f863979ba37f124d5f652a7aef6590dd93034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.8 MB (239782925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2613357626d500c34646039b65cf3728fcb7ee25fcba491909817b4d127793`
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
ADD file:eba80434f5df435e13e0c4a971c865a8fe930d18d36089192130267316506ded in / 
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
	-	`sha256:7749ef83ff0cd36ce0d199799a4be8de9b91c6731f586202ab39a4605d27c4c7`  
		Last Modified: Fri, 11 Oct 2024 05:07:29 GMT  
		Size: 26.9 MB (26866046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88500305391cd04c9a51ca6c9aae31a7f848fe911db6b2e22771dc1f0ef20864`  
		Last Modified: Sat, 19 Oct 2024 06:46:02 GMT  
		Size: 12.8 MB (12774273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a981c012b2ef93c0e4d3e5c624f415b9703e3e959bb801b3dd95edaebb3125`  
		Last Modified: Sat, 19 Oct 2024 08:19:59 GMT  
		Size: 48.9 MB (48888193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6111e812a892c1df5c539e5b9144e27e342290cd1693c23ea9a0fd9af6cb81e`  
		Last Modified: Sat, 19 Oct 2024 10:39:31 GMT  
		Size: 151.3 MB (151254413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8ddf5e5c2e97e71884c6af59abaf942dda549a0a8e4349acddc30bf53aaca77c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10720345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69080b2ac5985eaef5312663eba1507c3e224f0ca99d510ec3e6c5f24af1e6af`

```dockerfile
```

-	Layers:
	-	`sha256:ff09a1a21c7a669640b186c38daf3432183226bb6915336b625e08abd0f519d8`  
		Last Modified: Sat, 19 Oct 2024 10:39:27 GMT  
		Size: 10.7 MB (10710101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d7cb0cfc1d43f5f4dd6b09ac9eee91b4f76fb782e39f64fbd2831d27f34b482`  
		Last Modified: Sat, 19 Oct 2024 10:39:27 GMT  
		Size: 10.2 KB (10244 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e86d60447a52a1d6346524144985645a0423e4438ac233095fbc47d240456122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270652388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61a37454df2d40c917660e881cfea5faf51970ec24bf7ec4bcbf36147b9cf49`
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
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
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
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4950c6def722ac96f41618bdff1f82e38c2b3d5849ce2c07b4049db764444b`  
		Last Modified: Sat, 19 Oct 2024 05:23:22 GMT  
		Size: 13.5 MB (13452782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a3b9ee069311be4d8fca64a1f65e93cf73601746ef5283dfcbda615585143a`  
		Last Modified: Sat, 19 Oct 2024 06:27:05 GMT  
		Size: 45.3 MB (45297451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b98ba6826884a2dad7daedbb1abf09b61205cdbe1087c0d7f2cc328a44d2576`  
		Last Modified: Sat, 19 Oct 2024 12:49:21 GMT  
		Size: 183.0 MB (183016310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:487291d9e5158e997ddcee07b7408e8ec4675ebf87af60ea1b6acc29af0ca097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10942902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d377595d1f627e3b763cc7f7cc0d30f37e6d0cd1c2475fe6e99bdf32a75aa21c`

```dockerfile
```

-	Layers:
	-	`sha256:73bdac28c0f1e731d44a1bd44adbf20ae706d6d04310ea44cb41713a52d534a9`  
		Last Modified: Sat, 19 Oct 2024 12:49:17 GMT  
		Size: 10.9 MB (10932639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9b7bed5da457db1844d3d47e9497ba0a94df919a495851764dfdaf6d6d48e2c`  
		Last Modified: Sat, 19 Oct 2024 12:49:17 GMT  
		Size: 10.3 KB (10263 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b136aa8ebec3bb967cc748b99e9041c7df81fa0657c03f91136c543bc747513f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298476454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a7466eeae1673a2a6eac2e305c1e044edc3a09b06556eba461f50b1566da56`
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
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
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
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5bb7422168207a94659a7d755a71642577184a266af0a8a3afb47316450f6c`  
		Last Modified: Sat, 19 Oct 2024 04:14:07 GMT  
		Size: 16.0 MB (15990504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48479dfc2b7d427cb9b67d6c2ae25148b5cdad254e89920f302994550cebd409`  
		Last Modified: Sat, 19 Oct 2024 05:30:15 GMT  
		Size: 50.5 MB (50501654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378c1db9206641309be4ad1ed79478d79b600494ca52532597de42a2b7a249d4`  
		Last Modified: Sat, 19 Oct 2024 14:06:18 GMT  
		Size: 197.6 MB (197595327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c01988cb15f09691ff8b01e0328e80006a031f3258d706abaf30c43e0319b9c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10890029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6fed5214b877e2ef17d810fdefb5ec60b07bb5cdc66600357fe12e36dc36b9`

```dockerfile
```

-	Layers:
	-	`sha256:467c9adaa1534646b005cdb1ef70ebbebe92475898081a075c6e0177838ba246`  
		Last Modified: Sat, 19 Oct 2024 14:06:10 GMT  
		Size: 10.9 MB (10879813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8f22eda885975b6b07ea3ff187a442f984cd2da711532ddcaa211c23421c961`  
		Last Modified: Sat, 19 Oct 2024 14:06:09 GMT  
		Size: 10.2 KB (10216 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a48cd0fe0e3c96594b73a23e16a9f5f31cdd20d3dbb21889bec661254886606c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.0 MB (330029007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9914ffe80b60c5d35aa4ca731a127513eab9e5a4d21a9f132c9eaa136e80143`
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
ADD file:008d2e9e73153005eafa485b2ecca3ca9fd6996da5b5c99a52a7376427350f8d in / 
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
	-	`sha256:53300d777b1a34c849b57f3a3ccdc52f3ad795ea045079e7bcca5f63efab0327`  
		Last Modified: Fri, 11 Oct 2024 05:07:42 GMT  
		Size: 31.0 MB (30951587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a51cb0bf7686a8c2782160996192e9d89c09949101fc6d8c09083eb1013e91`  
		Last Modified: Sat, 19 Oct 2024 04:08:40 GMT  
		Size: 14.3 MB (14320414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0a2eaf274204c5bf93c79db9bc33e24b045b07aacb49995d18798544f6f56f`  
		Last Modified: Sat, 19 Oct 2024 05:41:12 GMT  
		Size: 53.8 MB (53801364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4a00631efcf264d6f9c5d8e41eee22c784fe6c727c1b65108038ef79a629b0`  
		Last Modified: Sat, 19 Oct 2024 07:50:42 GMT  
		Size: 231.0 MB (230955642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:de8c1a1ec27d92b20abc2f5650dd64af570c41d20931db30c0388d3370ed6ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10878952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65989ed3c96055e01b2f0033330d1a72ca1763345e024c3b6af226128a57aa98`

```dockerfile
```

-	Layers:
	-	`sha256:93701c93d6240b07395f73b128019d2a57242924acf950bccb621dcad2cb367a`  
		Last Modified: Sat, 19 Oct 2024 07:50:13 GMT  
		Size: 10.9 MB (10868736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ebba5414a868eb48c1037144a61dd35172010195fb71a791d9d80cb2a56c48a`  
		Last Modified: Sat, 19 Oct 2024 07:50:11 GMT  
		Size: 10.2 KB (10216 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8882db19e6755eb70cff00b9ab99c4e1eee12dddd74c4c6e46b0541cc6c8e4bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.1 MB (262094181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cffe492eab9f9ed8773d2b2a20e04bac69cd7543c8b9a9fb973fa1c15cf7dfe`
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
ADD file:77ba16e2cf3c210906ec7587ab14314afc15cb73af4337fde69ac35187fdb263 in / 
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
	-	`sha256:3d2abe11fb3bab133e95a31c3eeb04ba27eaed096cd5d4d3baeb8f12c3473633`  
		Last Modified: Fri, 11 Oct 2024 05:07:47 GMT  
		Size: 30.0 MB (30019614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1e22806c936cf352e8613a36cc00e41a5fc02ec3a1756fa36d836ba0f8dd58`  
		Last Modified: Sat, 19 Oct 2024 03:51:58 GMT  
		Size: 15.0 MB (14974773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3949ce1635c27257c28d76c25291d89d75979fb73e8177e9220f5e051d01fddf`  
		Last Modified: Sat, 19 Oct 2024 05:13:20 GMT  
		Size: 46.9 MB (46923171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4691bf2965046c25f376c2a1cdfcbd9c93c528a56464249e4aaff8d9bfe446e3`  
		Last Modified: Sat, 19 Oct 2024 07:01:51 GMT  
		Size: 170.2 MB (170176623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7807c6e272fe6f4640072ea3e39d7b2cd741f5025513129276568b362c231d50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10735725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9020d42999b45905436b9fce6b0368db0877f80ed31d2360ad50c6cd1fce82bc`

```dockerfile
```

-	Layers:
	-	`sha256:508877c0409dec14e70443d06c870e2ed2fe781820e7ed895cb0de132f6f0125`  
		Last Modified: Sat, 19 Oct 2024 07:01:49 GMT  
		Size: 10.7 MB (10725541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab8c395543308d5310678a3ac6bed1a1588cb39882a045f402dee11218c16300`  
		Last Modified: Sat, 19 Oct 2024 07:01:48 GMT  
		Size: 10.2 KB (10184 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:24.04-curl`

```console
$ docker pull buildpack-deps@sha256:61a02a85f7bd808d46ba3bd1dd757f277dc3026c68497a61d40c954ae277519a
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
$ docker pull buildpack-deps@sha256:69a53f84746bd2372529e6294f001436f888e30870daf61281a69619b86057ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43367069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5303bd2f189e17d8fbd2e62d67886dec77343f278c3c75cd273d299207c7b73a`
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
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb10f2d793001e79ccc6be8c28ad194b0142e46f3ea6c14095699bb7ba44ef3c`  
		Last Modified: Sat, 19 Oct 2024 02:06:23 GMT  
		Size: 13.6 MB (13616706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c0dff7df9d3a560fec4504795a8a76af7930b39ab2547e3ad5d56ae1246b7712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33382ecb57f630cddd0121e9581f247c374c0a13913cca08bc2ae9cf658ed9c8`

```dockerfile
```

-	Layers:
	-	`sha256:aae0f7d55899e7c0940b7b61d432d39e39e21cf565b7228a0eeba668dd220f63`  
		Last Modified: Sat, 19 Oct 2024 02:06:23 GMT  
		Size: 2.5 MB (2460121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5e5735a561089783c9f33d6a1c22c03d2914ddba32944dc3804408ca6f390f8`  
		Last Modified: Sat, 19 Oct 2024 02:06:22 GMT  
		Size: 7.0 KB (6959 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:bf67b389c162359f2b441024b2b7f89697063af26786e43d3ba27dd16b346d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39640319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d70429189febc1c7f120a2728c8d4a2b2b36ca1101c112ab10b03c376932632`
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
ADD file:eba80434f5df435e13e0c4a971c865a8fe930d18d36089192130267316506ded in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7749ef83ff0cd36ce0d199799a4be8de9b91c6731f586202ab39a4605d27c4c7`  
		Last Modified: Fri, 11 Oct 2024 05:07:29 GMT  
		Size: 26.9 MB (26866046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88500305391cd04c9a51ca6c9aae31a7f848fe911db6b2e22771dc1f0ef20864`  
		Last Modified: Sat, 19 Oct 2024 06:46:02 GMT  
		Size: 12.8 MB (12774273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0a4a978974bd38c1c6b56539b3ade7a20d784dabcdde222fea7c10ab1952d423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2469442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753a918dea5e27dff5ccad5ffbdedddcd18560a8ed92d0ffe7e85fc413f2caaf`

```dockerfile
```

-	Layers:
	-	`sha256:f6ee94b67ea69af693bb63300fcd2a72f7c7b0641ebb305828624092a786d5ad`  
		Last Modified: Sat, 19 Oct 2024 06:46:02 GMT  
		Size: 2.5 MB (2462424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a08b7584e68e048ec746fad58924742a4448c4aa658c8176d0cc77ae4d8aa9e`  
		Last Modified: Sat, 19 Oct 2024 06:46:01 GMT  
		Size: 7.0 KB (7018 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cdaa9366946071023e1f96102056d61ee8d5813c648e5e443ad775377a9aca37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42338627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd103c37af2bfabfeba88731e3900a13344638ade7dd0cf35713c06b44c019a8`
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
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4950c6def722ac96f41618bdff1f82e38c2b3d5849ce2c07b4049db764444b`  
		Last Modified: Sat, 19 Oct 2024 05:23:22 GMT  
		Size: 13.5 MB (13452782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d597e073523447174c59bb9339d4e921315e6010cd65e7a8755ff6115fdeb031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9c60a9160ad5646d9fc916f16cbb8b13ab91a4d08eb7b0212b2ae4f0f735e0`

```dockerfile
```

-	Layers:
	-	`sha256:e53b756c5aca4d1d0fc8e68b5476dbb34c0592709fa3d5c106120d622d0d4a20`  
		Last Modified: Sat, 19 Oct 2024 05:23:21 GMT  
		Size: 2.5 MB (2461179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7983d358f6b848383136c8117c7dcf53cae037638cf1ffb01ee404c5bb6e3666`  
		Last Modified: Sat, 19 Oct 2024 05:23:21 GMT  
		Size: 7.0 KB (7039 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b655e7c7154dd2e45e599d42b4097933c95c98cf7b78b205fb4822c1d0fe43b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50379473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:778119530d1d3acb12623754e4aca31b15520b5e05d341cb87242e71bf02b11e`
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
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5bb7422168207a94659a7d755a71642577184a266af0a8a3afb47316450f6c`  
		Last Modified: Sat, 19 Oct 2024 04:14:07 GMT  
		Size: 16.0 MB (15990504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e9bd42e00d50a337eb6ae71acada0521952731d883ac3674c61ede4b6941cfa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2471598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc9ccef8ea2d95e6746f6910ef5c892fbd2fccf5633f3131aec3d0c40461a20`

```dockerfile
```

-	Layers:
	-	`sha256:cbbf862c11201133c8b1aef247405d5920b029ac32240b23d848dd20991ac250`  
		Last Modified: Sat, 19 Oct 2024 04:14:06 GMT  
		Size: 2.5 MB (2464607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15c4b71488bd7802d0d94fd3377dc27a700634f63f50d3d5032eef9f97d50589`  
		Last Modified: Sat, 19 Oct 2024 04:14:06 GMT  
		Size: 7.0 KB (6991 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:ed5ce75d1f4a620f01d0702d00faccfb5034aa47070c521d27be46692bc8b17b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45272001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa560d2123906a1eb27b1cd3fe84a41430d89dedc458d78495edb54a85e0cf3`
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
ADD file:008d2e9e73153005eafa485b2ecca3ca9fd6996da5b5c99a52a7376427350f8d in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:53300d777b1a34c849b57f3a3ccdc52f3ad795ea045079e7bcca5f63efab0327`  
		Last Modified: Fri, 11 Oct 2024 05:07:42 GMT  
		Size: 31.0 MB (30951587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a51cb0bf7686a8c2782160996192e9d89c09949101fc6d8c09083eb1013e91`  
		Last Modified: Sat, 19 Oct 2024 04:08:40 GMT  
		Size: 14.3 MB (14320414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:de682863d227036d5fe3a3d7207a85d92150a6d9b33ec0eb35f889ac3ff1471e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df1d0f629afff1832da077572992ad1229b1a9418393fc4bf4a1dbfec892ce96`

```dockerfile
```

-	Layers:
	-	`sha256:5da38e61e6a6326b47d7e44c6dc7b33b4a4b50f7ba4c1b11a697e586c7125702`  
		Last Modified: Sat, 19 Oct 2024 04:08:38 GMT  
		Size: 2.5 MB (2454205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fabf745c39c42d34cc0c475f1e2405f99e54eb30c56c802a0faa5b6401afadbb`  
		Last Modified: Sat, 19 Oct 2024 04:08:38 GMT  
		Size: 7.0 KB (6991 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cf2a4959c2ed6d7db6865a457e57f54f9133f61bdd71b89242b459a082ef2537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44994387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a458243e47a17fd216799e5fff9f87276e7519972bc41b477bd5f94785b8e2e`
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
ADD file:77ba16e2cf3c210906ec7587ab14314afc15cb73af4337fde69ac35187fdb263 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3d2abe11fb3bab133e95a31c3eeb04ba27eaed096cd5d4d3baeb8f12c3473633`  
		Last Modified: Fri, 11 Oct 2024 05:07:47 GMT  
		Size: 30.0 MB (30019614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1e22806c936cf352e8613a36cc00e41a5fc02ec3a1756fa36d836ba0f8dd58`  
		Last Modified: Sat, 19 Oct 2024 03:51:58 GMT  
		Size: 15.0 MB (14974773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8d29373003ee556463b8160d06035b70e7db1c3ec70559bd70c6195c677c2d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2469910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754d483c2a3ff5a5c1d88c4e43d97d4898d69fcbe01129c3a527042b92293f4a`

```dockerfile
```

-	Layers:
	-	`sha256:b81404d5535fdfe5a867765c9910eec76fea2b0b598aea04c12256f25e7ca67e`  
		Last Modified: Sat, 19 Oct 2024 03:51:58 GMT  
		Size: 2.5 MB (2462951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba29dacf77349b19b8ba8519424b7ffc7358b40c96462346edb75c87b78b41da`  
		Last Modified: Sat, 19 Oct 2024 03:51:58 GMT  
		Size: 7.0 KB (6959 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:24.04-scm`

```console
$ docker pull buildpack-deps@sha256:7c6bcb87a65951b2e02f596e3b6a80492d3e692d53407d1448d7a909abeeaace
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
$ docker pull buildpack-deps@sha256:8eab756f646b732a7dc889ae8b8edc6b7910c99a726dbfef4d55b84e097001c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88704738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc073b53d6ac3a55820ef7f37b3b01f8eab8d306c872ee6dd8cc8c3273bfb59a`
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
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb10f2d793001e79ccc6be8c28ad194b0142e46f3ea6c14095699bb7ba44ef3c`  
		Last Modified: Sat, 19 Oct 2024 02:06:23 GMT  
		Size: 13.6 MB (13616706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ed9a6a1726d06e0402223e684a198aad45fe01804a81aa58967a03d085b6dd`  
		Last Modified: Sat, 19 Oct 2024 02:52:33 GMT  
		Size: 45.3 MB (45337669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d2a09e9dc33036b61d80e379ffd5129d921c9af74fa05aac5fca717149fb56f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5083384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9cebdd3000d8052a20f7ae88451c5cd8ccf95751b8cbbd1374dd8c343905396`

```dockerfile
```

-	Layers:
	-	`sha256:fb57808df518ee10975192da49d52cf1942c3a864b2a5633e74b8359dc522a03`  
		Last Modified: Sat, 19 Oct 2024 02:52:32 GMT  
		Size: 5.1 MB (5076079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3045d24ebd20c1b16edafcb0f97642f4592eece82164dc9a906540d80177a4e`  
		Last Modified: Sat, 19 Oct 2024 02:52:32 GMT  
		Size: 7.3 KB (7305 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3cd10ae720029b6f1e428242a31c39af8ac4cfbc7117cd5d4d5287d8c5c87b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88528512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e16b3a161f0305bb749b01f52df04acf799601cb668fc2c55dc38b372834938`
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
ADD file:eba80434f5df435e13e0c4a971c865a8fe930d18d36089192130267316506ded in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7749ef83ff0cd36ce0d199799a4be8de9b91c6731f586202ab39a4605d27c4c7`  
		Last Modified: Fri, 11 Oct 2024 05:07:29 GMT  
		Size: 26.9 MB (26866046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88500305391cd04c9a51ca6c9aae31a7f848fe911db6b2e22771dc1f0ef20864`  
		Last Modified: Sat, 19 Oct 2024 06:46:02 GMT  
		Size: 12.8 MB (12774273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a981c012b2ef93c0e4d3e5c624f415b9703e3e959bb801b3dd95edaebb3125`  
		Last Modified: Sat, 19 Oct 2024 08:19:59 GMT  
		Size: 48.9 MB (48888193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:39c0f3d8abe6f4afd0242c7b449931a0bb21724b5ead8efe3c45c3b6913dbc81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5084737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf11b3d8775bd3422f2101fdabbc1073cb34db0f6228c997645fa5811fc8c920`

```dockerfile
```

-	Layers:
	-	`sha256:5578902e989bba6e6b2f359545c72f2bef2d807b89042c546be24f1541e1bba9`  
		Last Modified: Sat, 19 Oct 2024 08:19:57 GMT  
		Size: 5.1 MB (5077373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:039fdeaea77eab0be7598620955214b21e6704ed6c85a04fccaef2b3adf1dbc8`  
		Last Modified: Sat, 19 Oct 2024 08:19:57 GMT  
		Size: 7.4 KB (7364 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:99381b633665998b79690396699aeecda8a6021ba7f48ef5dc0b11d61d8f0977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87636078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de004308e59e863c2497e47864e8d59c4739b921649cdbf16ebb5dcc4d490bb4`
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
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4950c6def722ac96f41618bdff1f82e38c2b3d5849ce2c07b4049db764444b`  
		Last Modified: Sat, 19 Oct 2024 05:23:22 GMT  
		Size: 13.5 MB (13452782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a3b9ee069311be4d8fca64a1f65e93cf73601746ef5283dfcbda615585143a`  
		Last Modified: Sat, 19 Oct 2024 06:27:05 GMT  
		Size: 45.3 MB (45297451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c537019769318d6441a1a0ccde858638029672a31a138cdea08c817a02d85a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5090662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0417cb63caa30943de8542749d15b831605f70f171fb340489aa486804153b0d`

```dockerfile
```

-	Layers:
	-	`sha256:6564a5d55c888b25e3b018c49e151e8df03e9f22c64b33c89509fc90c86a0d6f`  
		Last Modified: Sat, 19 Oct 2024 06:27:04 GMT  
		Size: 5.1 MB (5083278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c74f6858d965dcd2c8366c220ab6a8e4c2213babf582ac0bdc402982d06317bc`  
		Last Modified: Sat, 19 Oct 2024 06:27:03 GMT  
		Size: 7.4 KB (7384 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5fa4b463c6bad8c325cf2a680beae1b5bdedf56de3341022116b1cacbe932088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100881127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de165e6533312f2db04bbb6972e5c0c6e9bf6b9572b6e1356fe2934adc94bcb`
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
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5bb7422168207a94659a7d755a71642577184a266af0a8a3afb47316450f6c`  
		Last Modified: Sat, 19 Oct 2024 04:14:07 GMT  
		Size: 16.0 MB (15990504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48479dfc2b7d427cb9b67d6c2ae25148b5cdad254e89920f302994550cebd409`  
		Last Modified: Sat, 19 Oct 2024 05:30:15 GMT  
		Size: 50.5 MB (50501654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:489d19de386867de888327079b1653eb5c2145f06deb5463336a053265851639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5091106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ec07f3c69822c7b50ff6231d02fa11ef9873228a0ee554cda3b170d2c5f41a`

```dockerfile
```

-	Layers:
	-	`sha256:a42262aa516f6d496beeb73cfcd4241bca3fdef81c466f632fab58c0d5a6784e`  
		Last Modified: Sat, 19 Oct 2024 05:30:13 GMT  
		Size: 5.1 MB (5083769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c7e14fa4672f84ec2b48325ebcbe2b010f0936ce050f44bc4ba250e171457eb`  
		Last Modified: Sat, 19 Oct 2024 05:30:13 GMT  
		Size: 7.3 KB (7337 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:cfe4a44771a4894331c387dfbfd41699d4082635a6d03edf2941e0a316b4d4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99073365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2edee905bdc81d5092eafd62cb7be9c063fa42d60d447d2cc14041cbdf81c0e6`
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
ADD file:008d2e9e73153005eafa485b2ecca3ca9fd6996da5b5c99a52a7376427350f8d in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:53300d777b1a34c849b57f3a3ccdc52f3ad795ea045079e7bcca5f63efab0327`  
		Last Modified: Fri, 11 Oct 2024 05:07:42 GMT  
		Size: 31.0 MB (30951587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a51cb0bf7686a8c2782160996192e9d89c09949101fc6d8c09083eb1013e91`  
		Last Modified: Sat, 19 Oct 2024 04:08:40 GMT  
		Size: 14.3 MB (14320414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0a2eaf274204c5bf93c79db9bc33e24b045b07aacb49995d18798544f6f56f`  
		Last Modified: Sat, 19 Oct 2024 05:41:12 GMT  
		Size: 53.8 MB (53801364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c1c88e5543520ba78e7e211adf00aab3892c369fcf8456da61a453ed97ba8b17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5073960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dba033ffdf0708f27422d708abdda6f4c7605566d9f1d37e2125e8c12426e23`

```dockerfile
```

-	Layers:
	-	`sha256:5e58895d95772019ad0fdcbe6b4be69f49a47be40659f1043c291ca842db57e0`  
		Last Modified: Sat, 19 Oct 2024 05:41:05 GMT  
		Size: 5.1 MB (5066623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f7fac63c0870d1c2791b08f5b05f46d2480ad4a0bc9c88d45b5d99d94de2d5f`  
		Last Modified: Sat, 19 Oct 2024 05:41:04 GMT  
		Size: 7.3 KB (7337 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1ed21863e54c46bb6a3e2a234ea3fa2be1aefa81129997fb2ce3ddf556d4b2eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91917558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845a06f98ce3734e6f2f38f914787f29ed85439d1730e933b3a44bdb334c6638`
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
ADD file:77ba16e2cf3c210906ec7587ab14314afc15cb73af4337fde69ac35187fdb263 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3d2abe11fb3bab133e95a31c3eeb04ba27eaed096cd5d4d3baeb8f12c3473633`  
		Last Modified: Fri, 11 Oct 2024 05:07:47 GMT  
		Size: 30.0 MB (30019614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1e22806c936cf352e8613a36cc00e41a5fc02ec3a1756fa36d836ba0f8dd58`  
		Last Modified: Sat, 19 Oct 2024 03:51:58 GMT  
		Size: 15.0 MB (14974773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3949ce1635c27257c28d76c25291d89d75979fb73e8177e9220f5e051d01fddf`  
		Last Modified: Sat, 19 Oct 2024 05:13:20 GMT  
		Size: 46.9 MB (46923171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:64971ad19818eaa5aec413e6610f11a061fbca500b06d502ed9ae51be25b0b69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5085721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bcadac4f51c1e199a96b69a99209a7b38d7d773d63d289914616fda48513d23`

```dockerfile
```

-	Layers:
	-	`sha256:618826a9976b9b06ed1c6f291f504f0edb80abfff6d55911eb84ed2e273db8d6`  
		Last Modified: Sat, 19 Oct 2024 05:13:19 GMT  
		Size: 5.1 MB (5078416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b08e90487ee45bafeb6e1dce6760b32074eb2786e00670505a3efa62c24f56e3`  
		Last Modified: Sat, 19 Oct 2024 05:13:19 GMT  
		Size: 7.3 KB (7305 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:24.10`

```console
$ docker pull buildpack-deps@sha256:e49c7154627792ef43468deb6b21949caed97e986e790accff535d2fd2d03b52
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
$ docker pull buildpack-deps@sha256:03d93a4dc70e0132312bea3f1d241698a735458531e6df70f8de510a99be38ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 MB (286146913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d3c744fb1b4abd4294a55843131e06d21bd63a052da9f1f5d0a5407fbbc7aaa`
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
ADD file:c6c1fcc53cf2d3beb705eee292dd1e6ef2980e7f6221cba9d5c4081038760fc1 in / 
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
	-	`sha256:372111cb3b6e75bbceae9a3a6c2d060e2fb7b2573e9ff6e1931f6de2798246c4`  
		Last Modified: Wed, 09 Oct 2024 16:53:13 GMT  
		Size: 30.6 MB (30600773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a944d883315edf8742919f6ef5b3c26a8ad272f5008425c60a2142fb1f5df853`  
		Last Modified: Sat, 19 Oct 2024 02:06:13 GMT  
		Size: 15.4 MB (15357098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d878515a2f78c562568bfe3981dd590eda252ccb805e73b9e3bb9f4485eee6`  
		Last Modified: Sat, 19 Oct 2024 02:52:39 GMT  
		Size: 46.4 MB (46428074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dfce72fe356e6ebf544894d58f638ff9283ef9eed257a7a26f09653c15fc48`  
		Last Modified: Sat, 19 Oct 2024 03:53:52 GMT  
		Size: 193.8 MB (193760968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dfd11ecc3b5e6efe6a85840a418c50473d20695918a939e92395a6673b25afc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11369292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01547e315200ee1c635fc2b988ed54edf58553cc8109fd67f8b267bb649967f9`

```dockerfile
```

-	Layers:
	-	`sha256:3a816cfdfd4c5b798f42ea76c86af988d85dbab1ad7e6d7f12ce754eb5a04550`  
		Last Modified: Sat, 19 Oct 2024 03:53:49 GMT  
		Size: 11.4 MB (11359090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24bcad713b0485bae1e33d23f06741842a9e36907a3b77602c55b9240a031125`  
		Last Modified: Sat, 19 Oct 2024 03:53:48 GMT  
		Size: 10.2 KB (10202 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.10` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:630f53d8b5cbe6bbc84776f9ce87fadcd5a4446d919c7cb3131d545498342f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.3 MB (248330372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51dea34a0a62782a1c0751d9eb5db63fc8e83b044206c17a17c064d29726c99`
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
ADD file:8e23d3c59f96fb90ac280b31339b3cdff6ade1865ca64b22d81f85a66b3808c2 in / 
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
	-	`sha256:c481ad0a3e91be308525ddb3271f2aa7bc25d4f2a1241c1e05f6552ebecd91b1`  
		Last Modified: Wed, 09 Oct 2024 16:53:25 GMT  
		Size: 27.5 MB (27546645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a20a0e501d15d9e4692975ca8c07ba367bbaed9ea09bf0a9d8382aca8abe0a4`  
		Last Modified: Sat, 19 Oct 2024 06:47:28 GMT  
		Size: 14.0 MB (14044586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804a8684eb96a4656dd0e6aee99ef9f42b140a0e1e97b15155ef8a8e3d346151`  
		Last Modified: Sat, 19 Oct 2024 08:21:23 GMT  
		Size: 49.4 MB (49402478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7af6233872298dc63a4b96ca3d1ad4917e7c750d92c59ae6a8eeab5a64c5ea`  
		Last Modified: Sat, 19 Oct 2024 10:44:09 GMT  
		Size: 157.3 MB (157336663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f9462d6a45142c84bbcfd22fe47b0ac534c01162292591fca5ea528d0deafcaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11148888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f39e15ad55084b6335173c3de143c8a0e38e4cde3d42d8c4a3ecbd516137e07e`

```dockerfile
```

-	Layers:
	-	`sha256:1a989d7ca518404b833d33a8cf7f72f10a5f7104fd5e03ad99094e564367fa2b`  
		Last Modified: Sat, 19 Oct 2024 10:44:05 GMT  
		Size: 11.1 MB (11138625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89b99890690fe15f551a601dfe804c776d6d483a7877e307f5353690c357d17b`  
		Last Modified: Sat, 19 Oct 2024 10:44:04 GMT  
		Size: 10.3 KB (10263 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.10` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:84d0664dfd2b7f563861dfa74c8a174ecdb0091aea34bb02a7b943c686275e1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279807550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d71d1ce194c71f9b9af6c05f830867b1ddf5d44645ad0cd92d12d98e5feb0d`
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
ADD file:897556c1de01d47a95fb4d7011c66a17502f56fb3838b2231407a26c3ec19779 in / 
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
	-	`sha256:e311dff5272f98c3a90f3b733cf3131b33de66a713a49c4dc345811451dabaf7`  
		Last Modified: Wed, 09 Oct 2024 16:53:19 GMT  
		Size: 30.3 MB (30284490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d09b70567f67458b69e57931b7ba0045a67a5ea93d03cd34ced355035e4ddb4`  
		Last Modified: Sat, 19 Oct 2024 05:24:26 GMT  
		Size: 15.1 MB (15130151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69ca0bd1e67582a527f0561d210442a28387165346cd80417b469dfff4c9547`  
		Last Modified: Sat, 19 Oct 2024 06:28:24 GMT  
		Size: 46.3 MB (46331301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030000a4c1910257f23efc5cdfddbdb4aba77b7d1fdce703b768b07b6f492d5d`  
		Last Modified: Sat, 19 Oct 2024 12:53:55 GMT  
		Size: 188.1 MB (188061608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:96d2130893caf1ac77491d2e7d95742afdca190fe40edf5ce971375631ed3193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11445721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8949f2aa5abfbcb022ba552ac0126c9345dc69676addf82d952a3019c2b72c`

```dockerfile
```

-	Layers:
	-	`sha256:58f90ead50d1b376ba369a2a113b94350268f9704ebcea6e3d84d48d9dda0172`  
		Last Modified: Sat, 19 Oct 2024 12:53:52 GMT  
		Size: 11.4 MB (11435438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0ff5188d23de71d755b5930ba82cc0aee31ad6837df0aea820a0d04d4adb5a0`  
		Last Modified: Sat, 19 Oct 2024 12:53:51 GMT  
		Size: 10.3 KB (10283 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.10` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f018a86da66f653058daa2ada02f288bbbcf6f749fda70307b1af30d1515415f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301463127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1af8ec41b66d08cb5ad10a41c28449d022deb952bfa8309eb6753b4062aa3ec`
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
ADD file:1f33027337aeb38d1fecb5ee33f2c55c6bd442e269ee902f5364ec863e957998 in / 
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
	-	`sha256:fc0886b1c0801753f6a7a5ef62947406857faa2987b1df5781427e2c559ea218`  
		Last Modified: Wed, 09 Oct 2024 16:53:31 GMT  
		Size: 35.1 MB (35062896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c073ca505f4363ebfcb898f4d2a8b23427ba6069a5fb5b06cc80cb0df05291`  
		Last Modified: Sat, 19 Oct 2024 04:15:45 GMT  
		Size: 17.2 MB (17233776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce660df8e8e7bcaf60343fbb14080cb0995f3ab4cdfa5765f101525c99d3070`  
		Last Modified: Sat, 19 Oct 2024 05:32:02 GMT  
		Size: 51.7 MB (51671410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596c50e5bb435c1b4a27ed920914c64a0ad7d69705ed612654dd283d064e22e6`  
		Last Modified: Sat, 19 Oct 2024 14:12:58 GMT  
		Size: 197.5 MB (197495045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:715439154d0004d30ceb5772a168331d85a8a651b5c0c0fcd3b16693663b5839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11361607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4855e8320c89ed136787ffb877830cf3eb8a3683cb45f5233407f1aea366b5`

```dockerfile
```

-	Layers:
	-	`sha256:356ba3c7ba5f2df4bc4020620c2c965b2dc3473074d8d6721d261dd8f9b36e1d`  
		Last Modified: Sat, 19 Oct 2024 14:12:51 GMT  
		Size: 11.4 MB (11351372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd06c235c1e7ea4f700bab41332ebcb85d7db422c3138e05256ac60bda4d75ab`  
		Last Modified: Sat, 19 Oct 2024 14:12:51 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.10` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:48afd56882a4b2e3cd2396ebcfa6e4a835b44e2ac04a5f3ab9f4ba6d8eb0a1f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.1 MB (378116068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed04263e45289e5f145f6fa1279c85e0232fdede3ddeef5cf9a6af3211db885b`
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
ADD file:9744fb771a3525b1ecc8bb8c4ca623db4381f3fa78cd865afd2dc853a7ec0106 in / 
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
	-	`sha256:c4c3b7ce35ec01feb67389e9cc9ac164fd53001e09b63553078d8d1e6ad0c713`  
		Last Modified: Wed, 09 Oct 2024 16:53:37 GMT  
		Size: 31.8 MB (31787862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe51613addcb9aebac5d02d07ded0ea6c171908f331d835d7c75b1cebb4be19`  
		Last Modified: Sat, 19 Oct 2024 04:11:36 GMT  
		Size: 15.9 MB (15873939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7fb3831c114a36b0b2c3c75c497b9581ec083768d0aa69432339a049abe6101`  
		Last Modified: Sat, 19 Oct 2024 05:47:19 GMT  
		Size: 54.5 MB (54527660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426ce57cb131e2d638c81a485aed90f4cc1f8072f4a53013aa398fc96a3519f7`  
		Last Modified: Sat, 19 Oct 2024 08:11:05 GMT  
		Size: 275.9 MB (275926607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:650c38330916f8997d1d90788e774e46303f5d7b2c5147840f279d3e1f98a264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11417620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00179a05622dfbd93368ab3c0a9428ccf2a6bdc0286a2cbc2218e30e0affd999`

```dockerfile
```

-	Layers:
	-	`sha256:39cf10949df20e5ba0d106882dbfb72fc8685318991973dfa3a3b5c842cd96db`  
		Last Modified: Sat, 19 Oct 2024 08:10:29 GMT  
		Size: 11.4 MB (11407385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87c7dc51389f4537c713630a36116841bf82cbad0e379c3bfc42e5dd40a3f7e9`  
		Last Modified: Sat, 19 Oct 2024 08:10:26 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.10` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8d59ef204da03954a30f9b0437508e53dec88b738a35578ce5f60417f353c7d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.4 MB (265362951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36345074e94238af3d93afa020f1524b28079f416dc16d8b6f309ade31492f64`
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
ADD file:e8f85fdb92ac3e5e436757449ac2447ad1520aad2682c8e0077efcce841566a1 in / 
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
	-	`sha256:303831814b37c8b218003169a08ba9ba85ed2a888e73d505841b5db92ec79efa`  
		Last Modified: Wed, 09 Oct 2024 16:53:43 GMT  
		Size: 30.8 MB (30774664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e574d553080236f570c1f83ee295b636102f93cefde1b709e84380c22d451f3f`  
		Last Modified: Sat, 19 Oct 2024 03:53:04 GMT  
		Size: 16.9 MB (16920088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e923714151c14f08933fe23d1283ee8fe44eabf4047feae2eb487e323f6a4b75`  
		Last Modified: Sat, 19 Oct 2024 05:14:35 GMT  
		Size: 47.7 MB (47742541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5d42432f385ba186920d2e84eaf784a7d78569b2bc0837372053989e4fa52a`  
		Last Modified: Sat, 19 Oct 2024 07:05:12 GMT  
		Size: 169.9 MB (169925658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:38efad609d88402a46e87ef6252a59b8be391b8d1f1f0d3eb729b63a1dfe6fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11168608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a0e82c9491dc1299b1420daf98d289e7033fdf06052c84abb656751893b8af`

```dockerfile
```

-	Layers:
	-	`sha256:13ec0e282ca8256dce1466b4d42ff3bf10a41da8a9fb66930ac757847bc48c2e`  
		Last Modified: Sat, 19 Oct 2024 07:05:10 GMT  
		Size: 11.2 MB (11158405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8e5600e4c78301d5bcd6fda1b318ba76b5210f34227b50361695f7309bf8152`  
		Last Modified: Sat, 19 Oct 2024 07:05:09 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:24.10-curl`

```console
$ docker pull buildpack-deps@sha256:1652e3648a28be38b38e993b799eabaf859dc696e231df39219d5f8d0602e6a4
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
$ docker pull buildpack-deps@sha256:c8064ce954a2d9c90bd2e16fdd31c7c0b20e66720232e562b71c781f6c00bf56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45957871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7b838a1e6a2498c0f2b75d67c8db81136efdc82a162f30a7585633d1d465a7`
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
ADD file:c6c1fcc53cf2d3beb705eee292dd1e6ef2980e7f6221cba9d5c4081038760fc1 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:372111cb3b6e75bbceae9a3a6c2d060e2fb7b2573e9ff6e1931f6de2798246c4`  
		Last Modified: Wed, 09 Oct 2024 16:53:13 GMT  
		Size: 30.6 MB (30600773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a944d883315edf8742919f6ef5b3c26a8ad272f5008425c60a2142fb1f5df853`  
		Last Modified: Sat, 19 Oct 2024 02:06:13 GMT  
		Size: 15.4 MB (15357098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:734f143b619a054aeaf675404b5a8b6bf169fef11b9e111e8a691436743a0b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d2b611b8af5dbe471921a51a30ed516be558eeaf85c1466481a13d6640a4ae`

```dockerfile
```

-	Layers:
	-	`sha256:04d1691c1daa2c8f7f4ed5fbb5bcfaa1d228a7b3502a02d4d0c606c8e2a69420`  
		Last Modified: Sat, 19 Oct 2024 02:06:13 GMT  
		Size: 2.5 MB (2458653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:470d7dbf100349d28fe574b0fc0e6eb056c846f0a7430a28ea4919e451ed1b6b`  
		Last Modified: Sat, 19 Oct 2024 02:06:13 GMT  
		Size: 7.0 KB (6978 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.10-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1e977fad87b7530f371b33c739f5b93816160035131817f7a37a12d811020346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41591231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e40ada5b94a3ac9d258dd7bc19b46d3216e7a081fc464acbf184e0c7af2ea3`
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
ADD file:8e23d3c59f96fb90ac280b31339b3cdff6ade1865ca64b22d81f85a66b3808c2 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c481ad0a3e91be308525ddb3271f2aa7bc25d4f2a1241c1e05f6552ebecd91b1`  
		Last Modified: Wed, 09 Oct 2024 16:53:25 GMT  
		Size: 27.5 MB (27546645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a20a0e501d15d9e4692975ca8c07ba367bbaed9ea09bf0a9d8382aca8abe0a4`  
		Last Modified: Sat, 19 Oct 2024 06:47:28 GMT  
		Size: 14.0 MB (14044586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7a3c3fae690959857baae5e83af87100f40797adf2708e30a85ee740cee3c37b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45cc8c06dadd6e69d7d01110cc90a328f09396e9cf95b2c8b380ba67473c314`

```dockerfile
```

-	Layers:
	-	`sha256:45bfb28afe372c81ef53acef056634d56ef2a00ac96381bd9866544d98c9d564`  
		Last Modified: Sat, 19 Oct 2024 06:47:28 GMT  
		Size: 2.5 MB (2460953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24c7480d5a4f13eca905b975d689fa52da17373cfa8107861a5c3954f890547d`  
		Last Modified: Sat, 19 Oct 2024 06:47:28 GMT  
		Size: 7.0 KB (7038 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.10-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e1dbce1c5f56458cb1879d905878b21a3aee8ad27ed8352bddb8e0c0b9bc248d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45414641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91f14a1161bb53b5d7cfb783d6af7a25904c299ac877d6bdcd8241f35b372ab`
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
ADD file:897556c1de01d47a95fb4d7011c66a17502f56fb3838b2231407a26c3ec19779 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e311dff5272f98c3a90f3b733cf3131b33de66a713a49c4dc345811451dabaf7`  
		Last Modified: Wed, 09 Oct 2024 16:53:19 GMT  
		Size: 30.3 MB (30284490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d09b70567f67458b69e57931b7ba0045a67a5ea93d03cd34ced355035e4ddb4`  
		Last Modified: Sat, 19 Oct 2024 05:24:26 GMT  
		Size: 15.1 MB (15130151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:77f2bd6376f24142b5a91b775d8e4d8cc19c37a9810da513eeffe24dfb904445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6396bf800ad99952b2d919edf4c9fcd01524725ed1328c9f7cbc6534cbe25ed7`

```dockerfile
```

-	Layers:
	-	`sha256:81847d8bf181c9da1a90aa9c5ef4ce09b6d0e5b180e825deba709789dd602d3c`  
		Last Modified: Sat, 19 Oct 2024 05:24:26 GMT  
		Size: 2.5 MB (2459710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d1eea14e97d018bb367fead4ed16ce0ac4bb8416b69ee8061c0934dbd8863b6`  
		Last Modified: Sat, 19 Oct 2024 05:24:26 GMT  
		Size: 7.1 KB (7058 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.10-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:eeb6cecc2bb9417e66a3c75ec146ffaeec184ddedd753033d517ab7cb3a59b9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52296672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9376d70f331306fb3aa3ebaef1c250863ae8b80e4b04f920c28edf8914603ba8`
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
ADD file:1f33027337aeb38d1fecb5ee33f2c55c6bd442e269ee902f5364ec863e957998 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fc0886b1c0801753f6a7a5ef62947406857faa2987b1df5781427e2c559ea218`  
		Last Modified: Wed, 09 Oct 2024 16:53:31 GMT  
		Size: 35.1 MB (35062896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c073ca505f4363ebfcb898f4d2a8b23427ba6069a5fb5b06cc80cb0df05291`  
		Last Modified: Sat, 19 Oct 2024 04:15:45 GMT  
		Size: 17.2 MB (17233776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d20c9d8b8a834172fa6ab55ecf8510e1f3288ae1cab193bc3cb3a40dbc6d700a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2470146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e85a5e2147848947205e6b9181c7b04afd71ac6a6c0ec75a150b21113084a031`

```dockerfile
```

-	Layers:
	-	`sha256:e0ca164efe4d449288e97a4a886a9454a1ff230e6a906e603a0cf8db8a519a08`  
		Last Modified: Sat, 19 Oct 2024 04:15:45 GMT  
		Size: 2.5 MB (2463136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da04dcb833f90e27bf5cae38acaa5f667c25b35a1a5c25c0a91a6f3cd82d474`  
		Last Modified: Sat, 19 Oct 2024 04:15:44 GMT  
		Size: 7.0 KB (7010 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.10-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:ba3f481bcb07a41a539397bc1c6c9e459810a28f0f1506f37a8a729e996ce91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47661801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85952ebe22570db7d5e17a085e44f5e0433d35d4d31df07edfe08fd4f9d96902`
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
ADD file:9744fb771a3525b1ecc8bb8c4ca623db4381f3fa78cd865afd2dc853a7ec0106 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c4c3b7ce35ec01feb67389e9cc9ac164fd53001e09b63553078d8d1e6ad0c713`  
		Last Modified: Wed, 09 Oct 2024 16:53:37 GMT  
		Size: 31.8 MB (31787862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe51613addcb9aebac5d02d07ded0ea6c171908f331d835d7c75b1cebb4be19`  
		Last Modified: Sat, 19 Oct 2024 04:11:36 GMT  
		Size: 15.9 MB (15873939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:634fb24146ea687622924739ef9b584455f9a8b0f46d250895d61afd83fd9b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff4081f19bf3b625147bc02f0fabbcdaed17eb0cbc383068ccce8a22992cc97`

```dockerfile
```

-	Layers:
	-	`sha256:a1bf1f852c1c38b69e6d718d23e7c17f4c060958d8bfe172ee8388b792786c33`  
		Last Modified: Sat, 19 Oct 2024 04:11:34 GMT  
		Size: 2.5 MB (2452740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a61d43411874b66aa52b6d698db1bab53c6e12085fc8967ba7377d7b05addb30`  
		Last Modified: Sat, 19 Oct 2024 04:11:34 GMT  
		Size: 7.0 KB (7010 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.10-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e2c3db1f649ee912aa1c6427c632b81bb6c446b42548649b72d9a1ea659d711c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47694752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c00d8aa43de987de73c99b16f375fd3a4214ef5b99cb8715edde84e954c74e`
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
ADD file:e8f85fdb92ac3e5e436757449ac2447ad1520aad2682c8e0077efcce841566a1 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:303831814b37c8b218003169a08ba9ba85ed2a888e73d505841b5db92ec79efa`  
		Last Modified: Wed, 09 Oct 2024 16:53:43 GMT  
		Size: 30.8 MB (30774664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e574d553080236f570c1f83ee295b636102f93cefde1b709e84380c22d451f3f`  
		Last Modified: Sat, 19 Oct 2024 03:53:04 GMT  
		Size: 16.9 MB (16920088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7a677b57cccf9a1f90f3301ea0e84d2d171768119ab573b8a9bf7bcbdb0cd06e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c969f11cafa5b99510b90103a69d2a55f244aee6afa3692abf5080f2a2d1d1`

```dockerfile
```

-	Layers:
	-	`sha256:484a058821f5b4ec587da2191d697a8a1ff80c40808532d11f42b48486c07a7b`  
		Last Modified: Sat, 19 Oct 2024 03:53:04 GMT  
		Size: 2.5 MB (2461484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98d0f3ef3b18565614a54559f250dd845d30c8b07e1b179f76446556d63bd434`  
		Last Modified: Sat, 19 Oct 2024 03:53:04 GMT  
		Size: 7.0 KB (6978 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:24.10-scm`

```console
$ docker pull buildpack-deps@sha256:400675c9f31f95df51dc1a53754e64c451d52626a17e58e141e8b47a9587a842
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
$ docker pull buildpack-deps@sha256:2e1a10606d94d1341f4291bfe145a175659c824965e8fd3865cf838d843ce4af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92385945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0113271dcab80bce9700ced13a5585c0c989e1b56647edc2486bdbf7e270ae92`
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
ADD file:c6c1fcc53cf2d3beb705eee292dd1e6ef2980e7f6221cba9d5c4081038760fc1 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:372111cb3b6e75bbceae9a3a6c2d060e2fb7b2573e9ff6e1931f6de2798246c4`  
		Last Modified: Wed, 09 Oct 2024 16:53:13 GMT  
		Size: 30.6 MB (30600773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a944d883315edf8742919f6ef5b3c26a8ad272f5008425c60a2142fb1f5df853`  
		Last Modified: Sat, 19 Oct 2024 02:06:13 GMT  
		Size: 15.4 MB (15357098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d878515a2f78c562568bfe3981dd590eda252ccb805e73b9e3bb9f4485eee6`  
		Last Modified: Sat, 19 Oct 2024 02:52:39 GMT  
		Size: 46.4 MB (46428074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1e3606b1ecf3ff7025ba8e1ea5e42df37408b840635cb63b334f037e41989f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10503c61c856cf28d7a99d4c07c844f5c8055fc334e6a3789c4c5d7d52bcbf1`

```dockerfile
```

-	Layers:
	-	`sha256:78722da52930ac15ebf0a6bcfd0e1fe261a2746c127f81b162b628725a8bdabc`  
		Last Modified: Sat, 19 Oct 2024 02:52:38 GMT  
		Size: 5.1 MB (5090433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ebf53812943cf5a8aa3587eeb1d7aa692dfc6b67872b34031c7959d49e6fbd2`  
		Last Modified: Sat, 19 Oct 2024 02:52:37 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.10-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a3b8436385f7e5f61c631de58b96267ca63424b7a1f2edddd2d8ade83de6b753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (90993709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b52a03a0d1525d7c051d4c6bd661df3d4d7fee021c5a779c43e15834a45a7a9`
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
ADD file:8e23d3c59f96fb90ac280b31339b3cdff6ade1865ca64b22d81f85a66b3808c2 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c481ad0a3e91be308525ddb3271f2aa7bc25d4f2a1241c1e05f6552ebecd91b1`  
		Last Modified: Wed, 09 Oct 2024 16:53:25 GMT  
		Size: 27.5 MB (27546645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a20a0e501d15d9e4692975ca8c07ba367bbaed9ea09bf0a9d8382aca8abe0a4`  
		Last Modified: Sat, 19 Oct 2024 06:47:28 GMT  
		Size: 14.0 MB (14044586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804a8684eb96a4656dd0e6aee99ef9f42b140a0e1e97b15155ef8a8e3d346151`  
		Last Modified: Sat, 19 Oct 2024 08:21:23 GMT  
		Size: 49.4 MB (49402478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d103e4ed295a6a17ce4ca2aaf307617dc876868f98530c47d5092cf36e24df7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5099116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f11a591fe13fa3511e7c434069e50379f13bca29a10d3e0fe37f00752ec2444`

```dockerfile
```

-	Layers:
	-	`sha256:41a132977d310714ddf9c74d7d7f6bb0c0fc8fc8d203c5ee774807bde513510e`  
		Last Modified: Sat, 19 Oct 2024 08:21:21 GMT  
		Size: 5.1 MB (5091733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93f60af3718c85df129bbd180f5861a4d382da0308f6619ba9d48d10963992d1`  
		Last Modified: Sat, 19 Oct 2024 08:21:21 GMT  
		Size: 7.4 KB (7383 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.10-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bdc102418f7661b306dba7cd1da9a44bf88dace880f30af2f9c99b3a14a70b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91745942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4ce0d24b5556cec948c7c2fef72f177b0aea727b2a74df8bfc0697e3acf7df`
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
ADD file:897556c1de01d47a95fb4d7011c66a17502f56fb3838b2231407a26c3ec19779 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e311dff5272f98c3a90f3b733cf3131b33de66a713a49c4dc345811451dabaf7`  
		Last Modified: Wed, 09 Oct 2024 16:53:19 GMT  
		Size: 30.3 MB (30284490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d09b70567f67458b69e57931b7ba0045a67a5ea93d03cd34ced355035e4ddb4`  
		Last Modified: Sat, 19 Oct 2024 05:24:26 GMT  
		Size: 15.1 MB (15130151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69ca0bd1e67582a527f0561d210442a28387165346cd80417b469dfff4c9547`  
		Last Modified: Sat, 19 Oct 2024 06:28:24 GMT  
		Size: 46.3 MB (46331301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ab39cbabd5fe378c4643b80257a53677158249d426e7dd238dafa3b47e2c23c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5105038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59aa480168513e7b6e1132c5fce9ca710815717ec675bb7f7683906de832e0ad`

```dockerfile
```

-	Layers:
	-	`sha256:3fe20449803338205830ae7041a7b5f211304706c435c32c2b2d96c4343ef0ba`  
		Last Modified: Sat, 19 Oct 2024 06:28:19 GMT  
		Size: 5.1 MB (5097634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:186178c3e379c352c1f9be0efb33fe165a2c5b8523674617e0abe790219eda5a`  
		Last Modified: Sat, 19 Oct 2024 06:28:19 GMT  
		Size: 7.4 KB (7404 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.10-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0ac0c11864cbe79f5d7936b1647a570a0f2ba6cd664790f20cfc6f15b37608bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 MB (103968082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6a3610d9b7eaf58f24c59c9906fb1fdcf0a7a86990394f21a175fad79451913`
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
ADD file:1f33027337aeb38d1fecb5ee33f2c55c6bd442e269ee902f5364ec863e957998 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fc0886b1c0801753f6a7a5ef62947406857faa2987b1df5781427e2c559ea218`  
		Last Modified: Wed, 09 Oct 2024 16:53:31 GMT  
		Size: 35.1 MB (35062896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c073ca505f4363ebfcb898f4d2a8b23427ba6069a5fb5b06cc80cb0df05291`  
		Last Modified: Sat, 19 Oct 2024 04:15:45 GMT  
		Size: 17.2 MB (17233776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce660df8e8e7bcaf60343fbb14080cb0995f3ab4cdfa5765f101525c99d3070`  
		Last Modified: Sat, 19 Oct 2024 05:32:02 GMT  
		Size: 51.7 MB (51671410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5e02463caf7de9f88f37613d8aa094b11341b4cf12a34e9c0cb5027b0a9154cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5105493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235e9b4dcf3d3b82a5b8a27770b6a8e1a16ee59f6f386771ef017a1d1f0d09b7`

```dockerfile
```

-	Layers:
	-	`sha256:18870027b00c8c1377dd93c6eae92bb606dbca04aeab0de9c5fcd1072358b90d`  
		Last Modified: Sat, 19 Oct 2024 05:32:01 GMT  
		Size: 5.1 MB (5098137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:644e927eea334c580d389006aa4b50d25abb00af7db86adaccf02768e08bb128`  
		Last Modified: Sat, 19 Oct 2024 05:32:00 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.10-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:7dcd4c9c250173f5241136de13c5d76c68cb13aea4202921dea27c75ff1bec55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.2 MB (102189461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45f5a29ff8520f0558ca8e6608ba4ed24e3bf003240379dc112d01b77636ca0`
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
ADD file:9744fb771a3525b1ecc8bb8c4ca623db4381f3fa78cd865afd2dc853a7ec0106 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c4c3b7ce35ec01feb67389e9cc9ac164fd53001e09b63553078d8d1e6ad0c713`  
		Last Modified: Wed, 09 Oct 2024 16:53:37 GMT  
		Size: 31.8 MB (31787862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe51613addcb9aebac5d02d07ded0ea6c171908f331d835d7c75b1cebb4be19`  
		Last Modified: Sat, 19 Oct 2024 04:11:36 GMT  
		Size: 15.9 MB (15873939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7fb3831c114a36b0b2c3c75c497b9581ec083768d0aa69432339a049abe6101`  
		Last Modified: Sat, 19 Oct 2024 05:47:19 GMT  
		Size: 54.5 MB (54527660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d9075d5353086f9f8f1d5ad1a4b08c86a8a2c42556bffdbed753c0d64f0af4fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5088341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eba17dc0ec912cb2bacd4d472b7bddedb156b6ade5d5d3950856afc4543f185`

```dockerfile
```

-	Layers:
	-	`sha256:a64d8c8fd891c47bfc45a5d57836ddd52829df56f468a9fa971eb9937cffe786`  
		Last Modified: Sat, 19 Oct 2024 05:47:12 GMT  
		Size: 5.1 MB (5080985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c8e227a3bf93254df4fb125746e67c01e90854fe7dba6b678862e2db84837cf`  
		Last Modified: Sat, 19 Oct 2024 05:47:11 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.10-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a3ac7dc97eb63d9013a092f3db71cfad7e4540dbe0e97a8b436c75e9add963f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95437293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a958ada935a3b94f4f9b08c16d40617d4a578b02c03f0bb7608f066c501304`
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
ADD file:e8f85fdb92ac3e5e436757449ac2447ad1520aad2682c8e0077efcce841566a1 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:303831814b37c8b218003169a08ba9ba85ed2a888e73d505841b5db92ec79efa`  
		Last Modified: Wed, 09 Oct 2024 16:53:43 GMT  
		Size: 30.8 MB (30774664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e574d553080236f570c1f83ee295b636102f93cefde1b709e84380c22d451f3f`  
		Last Modified: Sat, 19 Oct 2024 03:53:04 GMT  
		Size: 16.9 MB (16920088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e923714151c14f08933fe23d1283ee8fe44eabf4047feae2eb487e323f6a4b75`  
		Last Modified: Sat, 19 Oct 2024 05:14:35 GMT  
		Size: 47.7 MB (47742541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.10-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:eb8d26565a771439c11809356c7869ad7aeb0eb7eb0858f7c608d5356ef72274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5100092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8bd351ec2a646df3fff90485d2df39f601e0944b80d8b4143c9ccb3320d507f`

```dockerfile
```

-	Layers:
	-	`sha256:816052d2a74f2d518fe4b39b3f4c2ac66c3da2d731a25c9a46406294074d0043`  
		Last Modified: Sat, 19 Oct 2024 05:14:34 GMT  
		Size: 5.1 MB (5092768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb149f548535a0814f4e007c20ce2d36141cfc59043d9afd9bc1ff5f4bd4f4af`  
		Last Modified: Sat, 19 Oct 2024 05:14:34 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:bookworm`

```console
$ docker pull buildpack-deps@sha256:50daa6a4a65cbac68729b91d5d06a1868478187249e698c87a2fb6e1f7cd51e9
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
$ docker pull buildpack-deps@sha256:dfed95ded883b6221ceb01535be2c71864524606aefd9f39949acdb699e2c00c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.3 MB (349319218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd41bc93efcd7b454fddab4980d002a30aac51e898252f069988c36ca1cbf063`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2112e5e7c3ff699043b282f1ff24d3ef185c080c28846f1d7acc5ccf650bc13d`  
		Last Modified: Tue, 12 Nov 2024 03:58:28 GMT  
		Size: 64.4 MB (64391376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af247aac076473044d24960a352a8ec6f154cf0a28f4fbf35fe5d43b52687ba2`  
		Last Modified: Tue, 12 Nov 2024 04:55:08 GMT  
		Size: 211.3 MB (211293801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:88f0760f365d43d99e88c2c6c5f2efd4b604c21d71066254c3a95c591389825c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15508351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec10518bd3b236cdf9e7e299443317c4d3acea2d1d813eb18856745df0c8a77e`

```dockerfile
```

-	Layers:
	-	`sha256:84596790680ca7003b3b19983029b13d9eaca878c1b8bfb32be4d3dc30c06db8`  
		Last Modified: Tue, 12 Nov 2024 04:55:06 GMT  
		Size: 15.5 MB (15497811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6cf56ff8e4b2e1dbe2a80e23d5505991b3f7fb5386efd3ec112fe58e0de491a`  
		Last Modified: Tue, 12 Nov 2024 04:55:05 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c46a02bfc21fd7053f71092fa78fa842bbe70d7d3e8974a8f3e0d74c644ccaa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.7 MB (316656991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:978045ca96d7326e22edd7f3435c24ae52863a21d0e3c7300db1f7ffc12a58ec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:895d07844c9c09054971f530ffd0794c329a785344079a01ce24e3d51727407e`  
		Last Modified: Tue, 12 Nov 2024 00:54:43 GMT  
		Size: 47.3 MB (47338750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93efb128382700f7090be7bec74d12308eb11ced11717aae4403b7bccde20f24`  
		Last Modified: Tue, 12 Nov 2024 06:28:08 GMT  
		Size: 22.7 MB (22733304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5d34c31582cec80127fc538f65a56104fac2a20c87dbcaafc70b88f7a0a8b7`  
		Last Modified: Tue, 12 Nov 2024 11:29:42 GMT  
		Size: 62.0 MB (61996880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95228092402ee38dddb194f1bc5fef6e2e5917508ae15c94e0a077aa28cdd790`  
		Last Modified: Tue, 12 Nov 2024 13:53:10 GMT  
		Size: 184.6 MB (184588057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:068453375709d05dfab2e4f14fa04e65107704f3f15168fb7fadfc8922cbdaa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15307030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b3d2e6239bad3254d95f9349fb85402afcf4ea34b641d2c5bba65fe20ce54b`

```dockerfile
```

-	Layers:
	-	`sha256:bf286d0910d797df5b78752d6a8354956fb50cbd4a09db96b2e373c0f7358f01`  
		Last Modified: Tue, 12 Nov 2024 13:53:06 GMT  
		Size: 15.3 MB (15296422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dbd9d8c58fb1bb6415885f21668416442eec559a928dedf198c14f800323de1`  
		Last Modified: Tue, 12 Nov 2024 13:53:06 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:06bb2db41f7fbeb1ec1b7250e0bd11f1107b7c431d2089d90ced37389022d435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (301951405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d9fe338d80f977597c98ae1e707ffa5d324da2a547b20f01e17705aa675bea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7fd5031c50fee563f16760ae6e5334672d6c9ba07d159b9e3a17a3b62011`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 22.0 MB (21957404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542f68420f2ab6efd74aba4b4ff72fe115144308ecea01703acfd9de4db386df`  
		Last Modified: Sat, 19 Oct 2024 06:36:59 GMT  
		Size: 59.6 MB (59635104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad67b816dd3ebfab16dd19d0768f67e218ed3070e064a66bfa1b026ea84191e`  
		Last Modified: Sat, 19 Oct 2024 08:07:03 GMT  
		Size: 175.2 MB (175210957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0314a3678d8f3f88eabfb762a695986a02033d8fb22d77a5d6f5068b717b407c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15312390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2a075e1bcaa59170be86abde46ad32565b5db5716b6bd4e3da16477be91660`

```dockerfile
```

-	Layers:
	-	`sha256:690295df0718cc2104e887058f7a94786df16dea2499af3f048f8511ab87238a`  
		Last Modified: Sat, 19 Oct 2024 08:06:59 GMT  
		Size: 15.3 MB (15301770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d637639be757ccbf573e7b4da768bda5c46ef6deff9a9496fc6e85f0a17b9c7`  
		Last Modified: Sat, 19 Oct 2024 08:06:58 GMT  
		Size: 10.6 KB (10620 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:76778860e25ffd9449a5994b5617879cc83c194ea51d1d8f9ab1a157d3391e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.2 MB (340173078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65e32d70e63fc1d3ada53df6166c0952afb010d4eeeaf2703b3e4b858f866af0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5594266b1bacf9ad6855b00d9c5c98e721001eb115218eda673e548e04fdbf`  
		Last Modified: Sat, 19 Oct 2024 05:17:15 GMT  
		Size: 64.4 MB (64350044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d4884f85282b9a352dbcedf2cccd073a63e60b151be84375ce9279dec1c553`  
		Last Modified: Sat, 19 Oct 2024 06:16:07 GMT  
		Size: 202.6 MB (202644222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ddb4caa8d4e2a15bc8aff07048659c0464e1bd2e7d3d764a302f33abf3c24339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15536872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7b433acebb5d16e21a72e9664cc189b65f93aa069993c6093cf331dc21a67e`

```dockerfile
```

-	Layers:
	-	`sha256:8aa4d837f97e1bd618517d2b35e969ca84b0fb0999327cd9e82b934e5e8feb3a`  
		Last Modified: Sat, 19 Oct 2024 06:16:03 GMT  
		Size: 15.5 MB (15526229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7f3e5acc815d52ab17f8f3858cd0738538ffefcb45cdee80e1b80809203edff`  
		Last Modified: Sat, 19 Oct 2024 06:16:02 GMT  
		Size: 10.6 KB (10643 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c93bf79e093bc04f8c7b6197e087be2b58188acbffba4200487f158970c815ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.9 MB (351897372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20085e6d5ca38d0d5efc920deda4f2c7b7f1cc516d13009ea742ea8158c2e446`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:832e5094f1d1a0806638216e108f8c5f304112749840ba33b550928d48d45f1f`  
		Last Modified: Tue, 12 Nov 2024 00:55:00 GMT  
		Size: 50.6 MB (50577048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7251b79b00fcda89d3d742332ebf95721ed377cc22dfc14fb4cc7d2086df8c8e`  
		Last Modified: Tue, 12 Nov 2024 02:37:55 GMT  
		Size: 24.9 MB (24899410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c46592415d8ae65247d6cff038217c0ae0c38f5f2fee88eaa3f5ae09743a290`  
		Last Modified: Tue, 12 Nov 2024 03:14:24 GMT  
		Size: 66.2 MB (66211304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f62d20ad9a58cf75459d448e04c818e5c7b20e4e0a9bd426ba0fdb30a427c0`  
		Last Modified: Tue, 12 Nov 2024 03:59:17 GMT  
		Size: 210.2 MB (210209610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0d785b0b0dfdc303e5c56e4d82f2d2bcd5324e327f7369f8a74f002fa09de00d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15486902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48cdd77c324b475203dfbffac68943494c3b20562c2fd7429bf011a97c6e523e`

```dockerfile
```

-	Layers:
	-	`sha256:3a3c6d3d3ff3129f37bfb0c59da4947b5efcfd67883d5459c890df826501384b`  
		Last Modified: Tue, 12 Nov 2024 03:59:13 GMT  
		Size: 15.5 MB (15476390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9258c5560c651fe26a375f83d4a42a46cc4ebaa1259d05526d19698320d05260`  
		Last Modified: Tue, 12 Nov 2024 03:59:12 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:7f2bc5242e17eac9490e908a2be63894f0a7381dcee30ec3dcf97ffc7e9f66cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.3 MB (326336355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc411215ceea19c8d66017c4c6c30a8263150a2170118d61d0188869e4adcdc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:5fa3d47e52ee376ed002c84d34e93fe11e6db2308915238c5d7a9a5840814eda in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bf8417b2ab139177317d556c6249cee54f60148ccee016ec60d45a13a21c7c2`  
		Last Modified: Thu, 17 Oct 2024 01:17:24 GMT  
		Size: 49.6 MB (49561619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba3cc6e574320e30c42f84b70c8e03fff0393ea65f20833b10b3a8aa1415e1`  
		Last Modified: Sat, 19 Oct 2024 00:56:12 GMT  
		Size: 23.6 MB (23648020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d702889c46052954a44f8b6ab39510d9b55acfe4a180194a7cb475c90b2b76e`  
		Last Modified: Sat, 19 Oct 2024 02:08:09 GMT  
		Size: 63.3 MB (63284387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbfb08e05dc5bd87f1bd1a6b1f7e1b3b709ea1bd67292b849b2cb2c26e2e7f3`  
		Last Modified: Sat, 19 Oct 2024 02:59:32 GMT  
		Size: 189.8 MB (189842329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:61877dcc36039290e4794b30548c16e84cba90a23025191394e70b71ae1c7e34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f6b2043ca0dc4f8dfd910788dc24c8058ed42300412714c5cc8ef674411cc86`

```dockerfile
```

-	Layers:
	-	`sha256:d284443815833cb6d5b05811d4a9aeeb5999f336721792c8e9b8df2051fb143c`  
		Last Modified: Sat, 19 Oct 2024 02:59:14 GMT  
		Size: 10.4 KB (10394 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:855a926cac624799b5b29e9e12c4a338a63508a60be4531db78f1854f45fbb21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.4 MB (363387524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4970e9caeb34b2bc82b8ac0a0fa85e493b833304680e062d0ad48796f31e459f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:c7ce4329d7c0cdfb8efa822e20a44ab1922fe70e4e8be36a317ec45c565a260b in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bbeb3fa4a5ad17047af70a984a8c9e89b0702821c59cb2290ff6c49eec8d704f`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 53.6 MB (53555597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1823a3ab0dcc6f88db2bc0c18d80304ad0e6a3cad08984b6ce0a7abefd371d55`  
		Last Modified: Sat, 19 Oct 2024 00:56:54 GMT  
		Size: 25.7 MB (25705977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3666a280304f3727f745e818ab5e252dd98676495517a360e23f821dee0fa6`  
		Last Modified: Sat, 19 Oct 2024 04:07:03 GMT  
		Size: 69.8 MB (69825530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81280667d7d6fa822ac7a45807cf98017526f614373fad289bacbeb84f61f73`  
		Last Modified: Sat, 19 Oct 2024 05:17:30 GMT  
		Size: 214.3 MB (214300420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b82239446d14aa796e3669145e0e4144e317024a47609818e67ccbd29abd061b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15484578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff7ba63cf1b1fdc77923361094664727253800983f28cc61f7aad9a84413081`

```dockerfile
```

-	Layers:
	-	`sha256:865d6af4dc1d0e2e578fa465f323f0b0362de6a63a4a7ddeb009cb407518f3a3`  
		Last Modified: Sat, 19 Oct 2024 05:17:24 GMT  
		Size: 15.5 MB (15473988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c857e04d79ec517fe7bdcb6e41dd0c8e8e8f030360535d2f3ad03f299fac1efc`  
		Last Modified: Sat, 19 Oct 2024 05:17:23 GMT  
		Size: 10.6 KB (10590 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:976e837fdf70dcad33dbb610aafc511db5e9e60883e690bd7682cb21557370fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.8 MB (318783168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb932672417afb874ffa1d6dcf687e42f3012df2af781a13680c2312d984d00d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:be1cd8a5c7d60ebbe308ecf258da8f3d2dd59f7c877549c96e98e31165ba1eaf in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:510daf83b7a2b266658f37f8849eeeba99ab0f02d08ef5c1ea7f613451a81239`  
		Last Modified: Thu, 17 Oct 2024 01:50:15 GMT  
		Size: 47.9 MB (47938447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b213e07d4abfcac72292a81e546e7d80ad0bd5377b4de866c7a61ca19b5837c`  
		Last Modified: Sat, 19 Oct 2024 00:57:06 GMT  
		Size: 24.1 MB (24050397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a99db1e4eb0a57b7be4b1376a7fdf886d4118a6263595ad414d052eb69ee9b4`  
		Last Modified: Sat, 19 Oct 2024 03:46:26 GMT  
		Size: 63.5 MB (63494580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2eccbc8d9b18898de6fc12769f52101d4af82f32957d095f8ab217c6886c2e`  
		Last Modified: Sat, 19 Oct 2024 05:04:19 GMT  
		Size: 183.3 MB (183299744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ed818f64d43e758653782aa4360eb15f84ce2a0952f08c9a9c2eb514723b2d34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15320678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2d212ca9b7a5946af205d9faabe9078a4422f84204de3eff0b79a4d9c76652`

```dockerfile
```

-	Layers:
	-	`sha256:150045fb989d3aa406e6943b9a50d396ee3d83ca315d5b553f09d68b02783d8d`  
		Last Modified: Sat, 19 Oct 2024 05:04:17 GMT  
		Size: 15.3 MB (15310126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6d6b263a153d82f2f5af8d644a5c79f02fa8cf89453e0498e1e3ec099c03301`  
		Last Modified: Sat, 19 Oct 2024 05:04:16 GMT  
		Size: 10.6 KB (10552 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:41a24bb5f87a336e821481c8495904b7ccab850ddb7d3c7819c2c4e2c7fb7cb9
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
$ docker pull buildpack-deps@sha256:41e41eb5a1eb21e97dc86dcc037ad0f73605f83b56c1c73464dd1db9196a4983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73634041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0afb2b1893cde96efc8d8210faaf240bf974567fcffc52c897c2f3c7dc9d79e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:986d0095b9a0c1ba3301eb55fd09b2d313291d46eb689d40f40ba5e22fe89c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4372469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d2308a6a913223982e9855dd8579b6c1952e064d55b55df3b488871308faebe`

```dockerfile
```

-	Layers:
	-	`sha256:ecebc53c12ddd3cdc651d3ac8588af340efb560dfff14086c45f26e4a6845d00`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 4.4 MB (4365306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b27611db305d9c1eaa6265accc831e7dd709d1ce5a580841bed26a4b03073d79`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 7.2 KB (7163 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:8e3fafd00e93960e28affb776bf24b68be5f16c8ae8264d6512d64e04638b301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70072054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ae47018992349a5e2058c7afa3cbbfad33c53a796b526639fdcbc544a232dd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:895d07844c9c09054971f530ffd0794c329a785344079a01ce24e3d51727407e`  
		Last Modified: Tue, 12 Nov 2024 00:54:43 GMT  
		Size: 47.3 MB (47338750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93efb128382700f7090be7bec74d12308eb11ced11717aae4403b7bccde20f24`  
		Last Modified: Tue, 12 Nov 2024 06:28:08 GMT  
		Size: 22.7 MB (22733304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5e697f44f82c828c459781743ae81c1b1fa2efd11d0ef16c315af40a6bf46a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4376053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29044c644def0ce321a888bed6b2e6a887e065d64284048b8cefbfab2415ff06`

```dockerfile
```

-	Layers:
	-	`sha256:0021462fa99eaa3af9d3f7856d66255747ce9d86290f0a67360aad6258734a1d`  
		Last Modified: Tue, 12 Nov 2024 06:28:07 GMT  
		Size: 4.4 MB (4368821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ccdb91b8a0e2609fdd39cee4ab8cac4e44254f455c3f6e89719b35df75eed9c`  
		Last Modified: Tue, 12 Nov 2024 06:28:06 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4df85825662d4ccaf0c53f0b0f706602fca0555267dd2d31a62e8ef87e1d558d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67110580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b88071c4591f6c7f807b8cad4c84e19227e69998bf7945120dfc8071b9014f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:46618ec96098836cac7950050ba554a969ebf8e9938d85d5f0d97015d3d25076`  
		Last Modified: Tue, 12 Nov 2024 00:56:14 GMT  
		Size: 45.2 MB (45150563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9660b2b46aa0c77f5dd078f4e57432faf3dbcda91672b9e3f8c1b7892e0ee2`  
		Last Modified: Tue, 12 Nov 2024 15:59:18 GMT  
		Size: 22.0 MB (21960017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:305784099f58635cead38aa11453521226000d86d85d52ee7848ca2c3be385c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4374834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8010ae6e055d2fc8797a75c67215cd400f64870bba5fb87b2503a4bb2fd1ae`

```dockerfile
```

-	Layers:
	-	`sha256:54c117e288564eb3719195c06d6bc879daa602feb6e27a0feb1a1ec9e18bf464`  
		Last Modified: Tue, 12 Nov 2024 15:59:18 GMT  
		Size: 4.4 MB (4367602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fcbbc798229c876fdfad98f81fb68cc54fb00ac95a2c847e9e133d91ce28ce3`  
		Last Modified: Tue, 12 Nov 2024 15:59:17 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e46fcc0c7385b7dccc516a32fb6dfc4d75a18dc39b9963b799d0cc2425554da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73185454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93ad60e192318acaeb45178aa2a8ced73c3b5c2075f1d0909094e482012ae304`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464f864cfaa846fbe1b8a889827404e18374f805d29d77c288a813ae8c4f6d91`  
		Last Modified: Tue, 12 Nov 2024 11:16:03 GMT  
		Size: 23.6 MB (23598253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7f238c1fe83bd003f1036848cda78a6c3cf076fcbed76560d0c41ed12edf3889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4372832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e335a8c4a64c4e0fae9e376895c95ac74dec942b688c1d5712b76326b89a71f`

```dockerfile
```

-	Layers:
	-	`sha256:a0d5ed8ce9f0036a2700ad927fefc558470f78b81f0b62876e96ad9516c09e17`  
		Last Modified: Tue, 12 Nov 2024 11:16:03 GMT  
		Size: 4.4 MB (4365578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3af911d4ac8fc50b9625684b9dfc26cb7861e3d51df952fe066d4eb1c8f230a`  
		Last Modified: Tue, 12 Nov 2024 11:16:02 GMT  
		Size: 7.3 KB (7254 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ac574690768b372f5dffd3fdba2f1316b68ee58133eada25d6f76b945c3503ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75476458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec174eb03e66f601edeb0488058e18636473d68377651065577803c0ac3d03f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:832e5094f1d1a0806638216e108f8c5f304112749840ba33b550928d48d45f1f`  
		Last Modified: Tue, 12 Nov 2024 00:55:00 GMT  
		Size: 50.6 MB (50577048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7251b79b00fcda89d3d742332ebf95721ed377cc22dfc14fb4cc7d2086df8c8e`  
		Last Modified: Tue, 12 Nov 2024 02:37:55 GMT  
		Size: 24.9 MB (24899410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d746769d0ce07c638d82090c56538afac5862001d98ec7ae5b23ae300ec87e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4369499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1441e57a6c764c8c7ccd95b08a608a908f3a9b0e5c6b666386e59faebc024b53`

```dockerfile
```

-	Layers:
	-	`sha256:8f720d960686e4104e12b5daa17252fea926f0989e5e2d35e3b5ace686835b71`  
		Last Modified: Tue, 12 Nov 2024 02:37:55 GMT  
		Size: 4.4 MB (4362362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce198488c58998d3efa8241e574d30337efbc03936c45f6efd2f314bd790083f`  
		Last Modified: Tue, 12 Nov 2024 02:37:55 GMT  
		Size: 7.1 KB (7137 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:de1a2b9066af1286e9d8175eef66425cfbddc0251cbdc6e6263a68b742ee6437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73211352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b5e3786aaeddd9bd8e5b8cd2245dc5be46353f3dbe4aa169166a83607577e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:17191dc8a469e4ef93330c5c8402fa0c0761218a5fa02ad2db7b34508d0e995c`  
		Last Modified: Tue, 12 Nov 2024 00:57:16 GMT  
		Size: 49.6 MB (49559181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf888157372a89189e8193ccb502b1003341993a439a6f526f90dc05a6100692`  
		Last Modified: Tue, 12 Nov 2024 18:00:45 GMT  
		Size: 23.7 MB (23652171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ee37e62e2a4f2b37b5059c26f65c50e79e8f12bede1551fe7c38dde1371e0e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 KB (7005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087a573000fee443714e51f8a22272ec23d27c5ef680d3b9f288f8ea41e63a91`

```dockerfile
```

-	Layers:
	-	`sha256:36da5312bc8de97460d5ca2df24b0a099c7af0db6158b101c163700559263cd6`  
		Last Modified: Tue, 12 Nov 2024 18:00:43 GMT  
		Size: 7.0 KB (7005 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:466f233ffc3b8ce8fc8e24fe4e0a478f467ee9c1b9e07ccaabb6d7f4dd82b50e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79272813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8258da2a3b826e8087b187be36e101338667cc4c8f4296ef4b30bf4867d89e8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9170cd93e372271efe7b34bbee8de26bbb094efba80a15cff49f580f87e5fe40`  
		Last Modified: Tue, 12 Nov 2024 00:57:37 GMT  
		Size: 53.6 MB (53555270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92051d5a3f7afdf0c89db06ce83fb963b8719a7024153e1520472673570e9d51`  
		Last Modified: Tue, 12 Nov 2024 08:29:09 GMT  
		Size: 25.7 MB (25717543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2238f5c37875dcd6505f74cd1d75fcbb33c40ab59512d84b295b8205ca2a6912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4377001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a107c661e17348313475322db42ffce8541848e8dd47876d57a3062cd14c027`

```dockerfile
```

-	Layers:
	-	`sha256:f1df1624c9d126aec722784a58ffe81fe99f97613ee2061a4ec42a2636a26b04`  
		Last Modified: Tue, 12 Nov 2024 08:29:08 GMT  
		Size: 4.4 MB (4369799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18a16b8c21a8a4d843e70acb35845f9570090375bdc2418cb56cbc1f86835707`  
		Last Modified: Tue, 12 Nov 2024 08:29:08 GMT  
		Size: 7.2 KB (7202 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:556f5aa74f180a341fe894576c8df3a358c7ad6432d78efbbc0da3bb71f523e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71996571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cac9802c1503429c3afb4b5bcf9abbc62bf5678126c5a817806438584d76da7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9f9f8fa8b12064144bd5037b70d4d9ac4fcbcd94f2921feb1e017764a273f798`  
		Last Modified: Tue, 12 Nov 2024 00:58:23 GMT  
		Size: 47.9 MB (47938688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53b034664a3d7aeeede4479f8aebfb2fff094119ae93ccf99e62d557e92b31f`  
		Last Modified: Tue, 12 Nov 2024 09:01:46 GMT  
		Size: 24.1 MB (24057883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b5638e5d412c4935cdb5c941063892a1c760db5bd429ef01755d419da71ac16e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4372167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7196d3bd3ce51a1e06975a87f93ccac12d11dcde272e5ea99e71a63a7bf9d9b6`

```dockerfile
```

-	Layers:
	-	`sha256:86a46b41b61f05b5bf553bb19fecd56edefa4c046740d61578dbcfda5746f13f`  
		Last Modified: Tue, 12 Nov 2024 09:01:44 GMT  
		Size: 4.4 MB (4365003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63952b86a5ed4c59bfbf8d5f3f31a85aed5da9a9298e45cbdcf514945aedb636`  
		Last Modified: Tue, 12 Nov 2024 09:01:44 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:234ad1de0c6bd8ae1024516f64646becce5040299546d61dce815cb7ec74454d
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
$ docker pull buildpack-deps@sha256:6fbde97d2c5f38678ecc77dba69ae37004e01c5fe1060195a6fa0a03a166b6f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (138025417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:408d444d56480b9093884d1bd6088cbd039fc990d5bf1507bd57a0e13bdd3a33`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2112e5e7c3ff699043b282f1ff24d3ef185c080c28846f1d7acc5ccf650bc13d`  
		Last Modified: Tue, 12 Nov 2024 03:58:28 GMT  
		Size: 64.4 MB (64391376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d933d77fc474f2f63922bf70e05b7ea0af809991a3e5cb05967accda9f937dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7772096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5efb1b53407bad0cf8f47b0a1d54a6a9e90a27ae1c86a6a6de8f9bb3c8cc85c3`

```dockerfile
```

-	Layers:
	-	`sha256:b6f4689c52467b37f8370b7c0f6ac7fb405ab637e983b4ad7353590dd0a8a2cc`  
		Last Modified: Tue, 12 Nov 2024 03:58:27 GMT  
		Size: 7.8 MB (7764442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91abd18c81a94564d4a7151834429ae9fbf19f28c3a4e2937046f1a765ce3039`  
		Last Modified: Tue, 12 Nov 2024 03:58:27 GMT  
		Size: 7.7 KB (7654 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9a1f00aee35fdbfc3bbef35f7b430afe4b7d61335911b8ca883d4ee277540158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132068934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28e47e232c9eb35167cfd394f5c0f26dd9550bca5ee8ac3a7fb762992cd8e96`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:895d07844c9c09054971f530ffd0794c329a785344079a01ce24e3d51727407e`  
		Last Modified: Tue, 12 Nov 2024 00:54:43 GMT  
		Size: 47.3 MB (47338750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93efb128382700f7090be7bec74d12308eb11ced11717aae4403b7bccde20f24`  
		Last Modified: Tue, 12 Nov 2024 06:28:08 GMT  
		Size: 22.7 MB (22733304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5d34c31582cec80127fc538f65a56104fac2a20c87dbcaafc70b88f7a0a8b7`  
		Last Modified: Tue, 12 Nov 2024 11:29:42 GMT  
		Size: 62.0 MB (61996880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:146afff14da66d2415f7e870a0b5475327d3b8c5c3012e0e73e9929ce55432aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7773719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1139b21f47128807aca40d8f91d82ce8acf1684a9f67bba7bd10747e93444a31`

```dockerfile
```

-	Layers:
	-	`sha256:e5dc3d0311f5fe151c6c570f37bed7153cdc58ca55dc3f8244a7b0463ad6f4b5`  
		Last Modified: Tue, 12 Nov 2024 11:29:41 GMT  
		Size: 7.8 MB (7765996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3878cd87f19cd6baf6f4baacf94bb729da9783cc7ba94a83e2575efb914f143`  
		Last Modified: Tue, 12 Nov 2024 11:29:40 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d8da1a84da0bff207409bbac38dd1a02df0945b14ffd1fa2e34036a968789458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126740448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11391af0d1d3a25dfc5836b449c838b6faf132d3b8f3207da24d749b265ef353`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7fd5031c50fee563f16760ae6e5334672d6c9ba07d159b9e3a17a3b62011`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 22.0 MB (21957404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542f68420f2ab6efd74aba4b4ff72fe115144308ecea01703acfd9de4db386df`  
		Last Modified: Sat, 19 Oct 2024 06:36:59 GMT  
		Size: 59.6 MB (59635104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:82abbe189e4134358a35de062d14a33ab4ef2350f5335ed22d488f490c39e3f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7773386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a185c3d89851dea1a6599e78d946fb300c3e2ee6fe011b211285a182fc5e834`

```dockerfile
```

-	Layers:
	-	`sha256:f581eedd8301e57f012174ed44c98b695ef71465963ae45671ac92102a1eaafe`  
		Last Modified: Sat, 19 Oct 2024 06:36:58 GMT  
		Size: 7.8 MB (7765651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcf5b6a5be36ea85b8ff05143189e2f676d385b38504343c20e9f59dc37a002e`  
		Last Modified: Sat, 19 Oct 2024 06:36:57 GMT  
		Size: 7.7 KB (7735 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1b238ddfffd81f1788a7575612d8a052bad65a59129adf13b225091a1f798575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137528856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c89ba4d07f4ae3ae3debaa56c19ea06e7c0b9d2773c56679e3399263fadd9488`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5594266b1bacf9ad6855b00d9c5c98e721001eb115218eda673e548e04fdbf`  
		Last Modified: Sat, 19 Oct 2024 05:17:15 GMT  
		Size: 64.4 MB (64350044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4ae890e89350690ad59722f03f334f49def59e9a7a1b4eb60f59e60964f978fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7778540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ce0978485db8f8cd9635afd0ac7fc48b931593fe09f24a19d60b0d76c4e639`

```dockerfile
```

-	Layers:
	-	`sha256:5be58f0330ad5ad6c6e1439539fff91b3e586695d4806db0cf17398a4ea80ff7`  
		Last Modified: Sat, 19 Oct 2024 05:17:14 GMT  
		Size: 7.8 MB (7770781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd7d4cdd0c303535f95e2806de4f42d422c025d70f90f72882a1301f380aa64`  
		Last Modified: Sat, 19 Oct 2024 05:17:13 GMT  
		Size: 7.8 KB (7759 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:3a9a1cd1d4fc50ae45994fcf166dd95bd945fddb91781ffb82b09f84b8d70daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141687762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de9bf2a38fcbf043555508c597839677889c027dfa88e84f35a66f1493b14a2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:832e5094f1d1a0806638216e108f8c5f304112749840ba33b550928d48d45f1f`  
		Last Modified: Tue, 12 Nov 2024 00:55:00 GMT  
		Size: 50.6 MB (50577048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7251b79b00fcda89d3d742332ebf95721ed377cc22dfc14fb4cc7d2086df8c8e`  
		Last Modified: Tue, 12 Nov 2024 02:37:55 GMT  
		Size: 24.9 MB (24899410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c46592415d8ae65247d6cff038217c0ae0c38f5f2fee88eaa3f5ae09743a290`  
		Last Modified: Tue, 12 Nov 2024 03:14:24 GMT  
		Size: 66.2 MB (66211304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d29c3a56480553061917153ef4826fea0ff6b84616cfc7a020c1682e578f5c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7768146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23a9925b36e8fa4b0eddfc89cf9f299ae4e6da2ab487e270d5483829a67266f7`

```dockerfile
```

-	Layers:
	-	`sha256:21211546a412a59b68e54a0883d6e64098cc26325b2fac0f05cf5b94ab27c266`  
		Last Modified: Tue, 12 Nov 2024 03:14:22 GMT  
		Size: 7.8 MB (7760518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac6f9f590da617c7f5124adbdf5cc841c3d0456606c3d5617a33a51ecf792f53`  
		Last Modified: Tue, 12 Nov 2024 03:14:21 GMT  
		Size: 7.6 KB (7628 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:cadf76ca0578af7d2c32dce3d1860f04b28959bb1cb0f27e982288bba02c972e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136494026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0434755538859a36858a1cf943ffb9a3464378e9371f90644cb583fdfeefe551`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:5fa3d47e52ee376ed002c84d34e93fe11e6db2308915238c5d7a9a5840814eda in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bf8417b2ab139177317d556c6249cee54f60148ccee016ec60d45a13a21c7c2`  
		Last Modified: Thu, 17 Oct 2024 01:17:24 GMT  
		Size: 49.6 MB (49561619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba3cc6e574320e30c42f84b70c8e03fff0393ea65f20833b10b3a8aa1415e1`  
		Last Modified: Sat, 19 Oct 2024 00:56:12 GMT  
		Size: 23.6 MB (23648020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d702889c46052954a44f8b6ab39510d9b55acfe4a180194a7cb475c90b2b76e`  
		Last Modified: Sat, 19 Oct 2024 02:08:09 GMT  
		Size: 63.3 MB (63284387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:821b714bf8d6778d6d1b920a2baace275ae17c38d2e45770d4702d64b3d8634a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae759b8a8a22e7725a44091355ef141327e65f7a7442e018dfb5b90b94cf0cce`

```dockerfile
```

-	Layers:
	-	`sha256:7bab8cd7f7cc5b0a4b903dd7d23a799c7767e8dec89874cd1de2cc7ac2343c85`  
		Last Modified: Sat, 19 Oct 2024 02:08:03 GMT  
		Size: 7.5 KB (7509 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4a4289d5bc6db05198984f4e81697f55cc0d7ac6720bdcbdb13af2b5b385c231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149085096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3875cb156e725ad37ee97b98abf0f972f2ac10c4ff305204b30071a468158a4f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9170cd93e372271efe7b34bbee8de26bbb094efba80a15cff49f580f87e5fe40`  
		Last Modified: Tue, 12 Nov 2024 00:57:37 GMT  
		Size: 53.6 MB (53555270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92051d5a3f7afdf0c89db06ce83fb963b8719a7024153e1520472673570e9d51`  
		Last Modified: Tue, 12 Nov 2024 08:29:09 GMT  
		Size: 25.7 MB (25717543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913acd64029d37b20e9e161bb8659516cb78a99cfd56eb921fc4ccd76ae7c0c7`  
		Last Modified: Tue, 12 Nov 2024 16:09:31 GMT  
		Size: 69.8 MB (69812283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c21374c30e5f547aa9e66b04b1997909f699921da61d213ed3fb3d2a7de64c0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7779842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a315c2156e595de5e483e597dd3ea85ea0533d0e98f410011d7326f27679968f`

```dockerfile
```

-	Layers:
	-	`sha256:d9c5acd4f7b46ec0c9c2839752d6be8030b1bcc4d58b67483ad71a717d9899cb`  
		Last Modified: Tue, 12 Nov 2024 16:09:28 GMT  
		Size: 7.8 MB (7772149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1014f338054fa217964a7cd584f29304bb70ac47f3c759f554c010e2b966ee4`  
		Last Modified: Tue, 12 Nov 2024 16:09:27 GMT  
		Size: 7.7 KB (7693 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:029bcbdc4d92b810548bb6fe4d4a5d4fed99197e43c6a7cf1366a8d78db2c8fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135483424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ab4b43343266a1cc583fb48be5a34866624b123c7e48c1a091011da24be0f2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:be1cd8a5c7d60ebbe308ecf258da8f3d2dd59f7c877549c96e98e31165ba1eaf in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:510daf83b7a2b266658f37f8849eeeba99ab0f02d08ef5c1ea7f613451a81239`  
		Last Modified: Thu, 17 Oct 2024 01:50:15 GMT  
		Size: 47.9 MB (47938447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b213e07d4abfcac72292a81e546e7d80ad0bd5377b4de866c7a61ca19b5837c`  
		Last Modified: Sat, 19 Oct 2024 00:57:06 GMT  
		Size: 24.1 MB (24050397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a99db1e4eb0a57b7be4b1376a7fdf886d4118a6263595ad414d052eb69ee9b4`  
		Last Modified: Sat, 19 Oct 2024 03:46:26 GMT  
		Size: 63.5 MB (63494580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ecf9164fa7d6fe0f7178e89f1831c99d40d886c359e875262bf5d2f7fedb45bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7771243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8b973ea0fea3dbb11fa12a9b53632b91fca04c49806d2caf99693e37c78d69`

```dockerfile
```

-	Layers:
	-	`sha256:6e7b6cf839452bb8901601f821aa42480d98fc226c60373c907ff55920f3d325`  
		Last Modified: Sat, 19 Oct 2024 03:46:25 GMT  
		Size: 7.8 MB (7763576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ad6de2140fc403088cce711e23a06bd50be647583ddfcdda8b53b2134309157`  
		Last Modified: Sat, 19 Oct 2024 03:46:25 GMT  
		Size: 7.7 KB (7667 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:bullseye`

```console
$ docker pull buildpack-deps@sha256:4d15729c8eeb65bb265a30fe8a40747be2108ddc0afc976073bbf3061aa7fb01
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
$ docker pull buildpack-deps@sha256:53dfb2729c2ea5c681e9cc5b42af756ee2c8454c5a17c50c941e6ebddfb77e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.5 MB (322476759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a13bb52d64137bbfef4f596c20eb11be62bc22b837c7a8e686bf135c43ac16`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f895247ac53f8ccaff2388685ac5288e243187f243654f4af6205a31f8b693`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 15.6 MB (15557923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d199724b11b5ccb55a34503a046bfe20064837b3f7beb547b9a3eab1cb57e0`  
		Last Modified: Tue, 12 Nov 2024 03:14:06 GMT  
		Size: 54.7 MB (54735758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293ef60bdfab8ecc34823af26b3df1d9742e9cb94c1103aa66259e0d57784e72`  
		Last Modified: Tue, 12 Nov 2024 03:59:17 GMT  
		Size: 197.1 MB (197074298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6a30dd51335eb7fa371f0c5c3578e31ea1e657405af15cdbe610a70b0f860481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15107915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7616d68f81bc999bf5452b8b43940cd3b46d540ea4f71115ce69871554a2588`

```dockerfile
```

-	Layers:
	-	`sha256:5be5f4ee1b44d0e9aa1dba97561bc4d202ac1188a34c0a7994c931dec99f8303`  
		Last Modified: Tue, 12 Nov 2024 03:59:15 GMT  
		Size: 15.1 MB (15097684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5f4c658a590f8d5785004ec575558228d9e61e0d82304feeb72e9e60105c912`  
		Last Modified: Tue, 12 Nov 2024 03:59:14 GMT  
		Size: 10.2 KB (10231 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7b8ca851482f3ac5dd83f7f776c70287f0e396c927ced8b45b5ea35dc87974e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.2 MB (283245288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69abe948f0dfc547c7a71483c492df89477394a305ebdb17f6869f98afa00207`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:d2ab4547fbd8c2ffd1467397e3bf7357c565dd0ddab7b1fe46a7af555c5a2d58 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a95f74ee8cb74ceb08cfe11180d99d077de86d07cce20c373d10c20ce9885b49`  
		Last Modified: Thu, 17 Oct 2024 03:07:14 GMT  
		Size: 50.2 MB (50241596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f418fba84fbaf7bab67bcb059341b214f170e38610e4b70f45295fd8324614f`  
		Last Modified: Sat, 19 Oct 2024 00:56:46 GMT  
		Size: 14.9 MB (14877684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27a9032c7c4d1cfb31e96212773919f51ec2f6be760fc0f5c35bafbcdb50249`  
		Last Modified: Sat, 19 Oct 2024 06:37:59 GMT  
		Size: 50.6 MB (50613654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0525b656ff73752501ad6cdcf4137840983e49d8b07af0619e3185c5e925fb`  
		Last Modified: Sat, 19 Oct 2024 08:10:07 GMT  
		Size: 167.5 MB (167512354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:99b4df02852c5c9ef436da722253c6fd613682c2b9bce412b4b84eccb3100d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14908379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfbdcebad2cc9a5cf666dadee37e579872b3e9128215ef08cb6e2ff416e2cb19`

```dockerfile
```

-	Layers:
	-	`sha256:265b31aeaa92380f8c3f6425c52713027f95784e4b52573f632e8e7d38cebf55`  
		Last Modified: Sat, 19 Oct 2024 08:10:03 GMT  
		Size: 14.9 MB (14898075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b941b2a22320cb6c9bf38cc58a5be6077fbb15967c5c3ad3119f189d6344a351`  
		Last Modified: Sat, 19 Oct 2024 08:10:02 GMT  
		Size: 10.3 KB (10304 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6fcca6c2686873d338b72e222bcb158f9b6f212d9496aa46386d1570f3ccd69d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314286584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9960592e533e108fb3fcc1d20fc49c509fe953e1b3a136de1b615a35aea5ff42`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1deb2c2ef23607994f7238c8d97d113f5ebd868b8eb64a0c10d2e0983f036a39`  
		Last Modified: Sat, 19 Oct 2024 01:11:09 GMT  
		Size: 15.7 MB (15747789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbc6072bf5318ca0f9f250b4fcc6254d92483650689f0b0d77274be187abd96`  
		Last Modified: Sat, 19 Oct 2024 05:18:19 GMT  
		Size: 54.8 MB (54832658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13f3e7a61817231ad609702b6918e16648b3eec453567dbedd80952df7e3957`  
		Last Modified: Sat, 19 Oct 2024 06:17:47 GMT  
		Size: 190.0 MB (189971242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:820241d97196cee59900426af9c3bb7e6490fc2906443c04683fa92e277a2b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e441d6a78110371211f6fa8bd15f27a2b2446e97f40e2cefa3b4aaee7748bd`

```dockerfile
```

-	Layers:
	-	`sha256:3f974dae5571e312b034e2e30b7c42b00e5cd62d80d5aa904fc79d3c8f7ee648`  
		Last Modified: Sat, 19 Oct 2024 06:17:43 GMT  
		Size: 15.1 MB (15099830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:268bfc28ef38d7046c158f0988d2a132ffa8e524a824f7c055f6abd6bf05a9aa`  
		Last Modified: Sat, 19 Oct 2024 06:17:42 GMT  
		Size: 10.3 KB (10324 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; 386

```console
$ docker pull buildpack-deps@sha256:40024780c8ab41709798e05afd646c7d83816bbb7bb97d6886d978aaf4b5f314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.2 MB (328166848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfaf42b79695cbbb92c8d381a03a9d409a6148104819b2da33347b8905185497`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:401daab178046178ea38abc84ce80fe4a7e7530a75e6b198a161344b358750f7`  
		Last Modified: Tue, 12 Nov 2024 00:54:54 GMT  
		Size: 56.1 MB (56093682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7489e598cae5c0812e1ddaf1d0b649b6033369bedffceac2506c8d523d0a1c5d`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 16.1 MB (16061669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d3219f513bfa7d5289477f316932047bf97c5e63cdb25a5f5d84119699c8fa`  
		Last Modified: Tue, 12 Nov 2024 03:14:14 GMT  
		Size: 56.0 MB (56032476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989e2f9c439cb2101c7b9646a5f44226e8fce450b536fbbdf42b489a8b29cfc2`  
		Last Modified: Tue, 12 Nov 2024 03:59:24 GMT  
		Size: 200.0 MB (199979021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:99aa603c582d2d59b66ba6c53f22a13729334619991cd21f2ac319cccfcb9581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15096234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df97f8ff7c85fa15f17cd6dcd3ea675c70d7e49971247d6cba5f01f7f4b6b7e3`

```dockerfile
```

-	Layers:
	-	`sha256:66246ecf14a66fc01ddb14bad096f8a122ae7266dab2f9f517d0c2e78278d6c3`  
		Last Modified: Tue, 12 Nov 2024 03:59:17 GMT  
		Size: 15.1 MB (15086025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:471d13d8c1ae4297812155d8e61a16689ac6eaf1dea869327f30e24d8bcbcef3`  
		Last Modified: Tue, 12 Nov 2024 03:59:16 GMT  
		Size: 10.2 KB (10209 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:ca6c782fe8ec07a7cc6410453df28e7cca0cac02f890c922070d237f73ea0be1
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
$ docker pull buildpack-deps@sha256:2df346f6bf0a09c1b581bfa52800a87da97dc79a4c075abe911cfa512ddaafc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70666703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8aa56ed68dba89d198819c24d6f7406f16d7068d0490cc5648d04cb04f7722`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f895247ac53f8ccaff2388685ac5288e243187f243654f4af6205a31f8b693`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 15.6 MB (15557923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4ea105f4c54a69fdf29a66bcead17f11b33895523ec9eb4786da771c122e0936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4498981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f358d4fcc3f6327c0916ed130bd1c75b5731f999b5556491b61eab4f9885f33c`

```dockerfile
```

-	Layers:
	-	`sha256:41bc55e2a522382fd133dfd3161739a2e1becdf81df08d432ceece6009104b53`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 4.5 MB (4492180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:563ae519ad78eb8647e2644e539048e36d372cf39041bf4f75247792a023461b`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 6.8 KB (6801 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5763e2f5bf1629bec5c9e16d00a72e3dfd8f17b3a5667e72a651d18e71ef39b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64945646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce309396159795b0c45db2909a8559c1303270bf296bbe0f73ab8e2a6054b4c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c18c6ef253e2b87a07739846b10eb333531241b80c23e3aec0643adc1b449e1a`  
		Last Modified: Tue, 12 Nov 2024 00:57:22 GMT  
		Size: 50.3 MB (50272340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907b69db4cf1745187b07df647e4ed72539303d8747c006695c2bc15e5e1e185`  
		Last Modified: Tue, 12 Nov 2024 16:00:17 GMT  
		Size: 14.7 MB (14673306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d1fb45a0a4b3ee70c293b961eb04d26ff1a65af954b91132ee444cb2d991f128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4500675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33537d7ac7b5ad3b240e3e4da843d63123e8c262462e97cfeca2cb40e962ad7d`

```dockerfile
```

-	Layers:
	-	`sha256:87ec50285f2a8b3ca66ab532e7620f2de6bd499824493288de9a55c1fd4f6151`  
		Last Modified: Tue, 12 Nov 2024 16:00:16 GMT  
		Size: 4.5 MB (4493814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9433113985ed5cf511a7ff1fedca93ced3a78d7b8b35ab174e59d410af70d257`  
		Last Modified: Tue, 12 Nov 2024 16:00:16 GMT  
		Size: 6.9 KB (6861 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b3ca5e481e6e265be7ff4f1f665bc4702a4e7fd5c3592baa01884a67936d99b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69300660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e48eea012caf1b9fdcee3a320590d0f965b183ccbd3e2ac9027d6a49ab8425e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9e545ff305fe56558a94b064a901c16b373a3501daf5519f82ec19db6a3655`  
		Last Modified: Tue, 12 Nov 2024 11:16:34 GMT  
		Size: 15.5 MB (15543588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e95d2cbb57128b37e3aeb93434885a8fd4f24488e58be893a7fc19edced4c584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4498673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5dd407061bac2bbf6554ae718d25b67268b9b4f1229edd0431ca2b3e092472`

```dockerfile
```

-	Layers:
	-	`sha256:3d5cdaf50f3868d2492b29e300367b85b38f1460b7b8f6e9c9a20540301e0778`  
		Last Modified: Tue, 12 Nov 2024 11:16:33 GMT  
		Size: 4.5 MB (4491792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:914df286e10eadb4badd71b8c9c813a4d97e87d5866664eec95ab4e0f7030517`  
		Last Modified: Tue, 12 Nov 2024 11:16:33 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:28db40634d8196c741694964927ffbcce7a32e46ce629d076ac4180059acc1f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72155351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4af437b3c1ada7e3c006fa019ec1cb83212d5e1723583a7a203963cd7812b6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:401daab178046178ea38abc84ce80fe4a7e7530a75e6b198a161344b358750f7`  
		Last Modified: Tue, 12 Nov 2024 00:54:54 GMT  
		Size: 56.1 MB (56093682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7489e598cae5c0812e1ddaf1d0b649b6033369bedffceac2506c8d523d0a1c5d`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 16.1 MB (16061669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:adaffba9878783500c58c160462f440fa73a4d51cc25f766be5463aa7ac39bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4495398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:779e7f15590d0bf3c8710f0aac9cc10c85719c2601c08b05b9695f106959c996`

```dockerfile
```

-	Layers:
	-	`sha256:0654c325eacf20f2fa53094181831e09fd652d1356c43ddcab4d5bd8bcd3fefa`  
		Last Modified: Tue, 12 Nov 2024 02:37:52 GMT  
		Size: 4.5 MB (4488619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4019c97fc7b3b49f34fc5ee695b048f164cef6227b6864fdb3a3d5d99adaf8c`  
		Last Modified: Tue, 12 Nov 2024 02:37:52 GMT  
		Size: 6.8 KB (6779 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:dece6b2b6cff356b300bab333df2eebe764526754b4cdb38b1fb8f98998eee06
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
$ docker pull buildpack-deps@sha256:540e7a62b63872321d2c383afd57c95a18ae18b2f5ceb5bcc0cdd6df05db8576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125402461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd55a9e99939cf7c5acf4c269136ff35f63aaa9a844090e0b1371e26552ae01c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f895247ac53f8ccaff2388685ac5288e243187f243654f4af6205a31f8b693`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 15.6 MB (15557923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d199724b11b5ccb55a34503a046bfe20064837b3f7beb547b9a3eab1cb57e0`  
		Last Modified: Tue, 12 Nov 2024 03:14:06 GMT  
		Size: 54.7 MB (54735758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b7aa7ab778ad756a4f5b94a9de226627f55235ccdf11496a0d182f3bc0ee3f6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7727489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bcf6ce98fa3bc15782ab2f19e9d7e2b0086c50da9d6bb74813f7de64b3a923f`

```dockerfile
```

-	Layers:
	-	`sha256:a1e5ea0b3a869821c16ffa4ba2bf5f7cac5d4d91a864463741aed3d1441e916e`  
		Last Modified: Tue, 12 Nov 2024 03:14:06 GMT  
		Size: 7.7 MB (7720136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3f7d1a03ede92d8e8005d05cde3f0bc5596c387c4c736f94ba3a94d1aa52014`  
		Last Modified: Tue, 12 Nov 2024 03:14:05 GMT  
		Size: 7.4 KB (7353 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0b27afdfd77d75f7daa15242cc63d12c81c15bef9bfdf3389220b78e4b71c5d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115732934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fea1c1109f52736fe3129fe2d91df3883572414c5c1c122f693e794c1cca2a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:d2ab4547fbd8c2ffd1467397e3bf7357c565dd0ddab7b1fe46a7af555c5a2d58 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a95f74ee8cb74ceb08cfe11180d99d077de86d07cce20c373d10c20ce9885b49`  
		Last Modified: Thu, 17 Oct 2024 03:07:14 GMT  
		Size: 50.2 MB (50241596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f418fba84fbaf7bab67bcb059341b214f170e38610e4b70f45295fd8324614f`  
		Last Modified: Sat, 19 Oct 2024 00:56:46 GMT  
		Size: 14.9 MB (14877684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27a9032c7c4d1cfb31e96212773919f51ec2f6be760fc0f5c35bafbcdb50249`  
		Last Modified: Sat, 19 Oct 2024 06:37:59 GMT  
		Size: 50.6 MB (50613654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d17122d5550612fcfb8bdb86e3884095b4bb789a98d27dec66b7b6363b515ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7728923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a8a3069eb6e9c82d3c4c18ddb245fd1e026f21f27ffd7382878abd6e0251e7`

```dockerfile
```

-	Layers:
	-	`sha256:6875125c6a3662c299a57970ecff8767213464540a3f4b2443f46582d4b59612`  
		Last Modified: Sat, 19 Oct 2024 06:37:58 GMT  
		Size: 7.7 MB (7721498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c133ef3869a8610514a32152844f53057e7d5043e5788c21cc57d2487ebb1a5`  
		Last Modified: Sat, 19 Oct 2024 06:37:57 GMT  
		Size: 7.4 KB (7425 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:663f17b029a1bf24ca58f209ff1577c2d1b9a7aed2ecadbfc6ba889c327a0382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124315342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2754992e17ca3179605d3f122e480a5b71db85b29892344fbaadb8f3fd43c5e2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1deb2c2ef23607994f7238c8d97d113f5ebd868b8eb64a0c10d2e0983f036a39`  
		Last Modified: Sat, 19 Oct 2024 01:11:09 GMT  
		Size: 15.7 MB (15747789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbc6072bf5318ca0f9f250b4fcc6254d92483650689f0b0d77274be187abd96`  
		Last Modified: Sat, 19 Oct 2024 05:18:19 GMT  
		Size: 54.8 MB (54832658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1965623055033a3db2cd3d6d55f03b896eeeca6c187d658624bfdb8ad6528736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7733284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6670f84a12848f56394136665a519aceecb0d2286466693304dc42e0605ca50a`

```dockerfile
```

-	Layers:
	-	`sha256:e2d1f70c81ca0b6cd23296d317fd5165b255a7e0a1572a49f179932ebb08e535`  
		Last Modified: Sat, 19 Oct 2024 05:18:17 GMT  
		Size: 7.7 MB (7725839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b826fcef0fc38aaa49e948810018ef936f777127503a8a92bbbab59aabd9f1c5`  
		Last Modified: Sat, 19 Oct 2024 05:18:17 GMT  
		Size: 7.4 KB (7445 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:abdacb8dd3629c36873bb6565bb5355bb43e35599717521edddba9275708ca78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128187827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3519d81e879877e50e48707a4c989ea967331bf5b66e4edbd4517f2f68c0c5e2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:401daab178046178ea38abc84ce80fe4a7e7530a75e6b198a161344b358750f7`  
		Last Modified: Tue, 12 Nov 2024 00:54:54 GMT  
		Size: 56.1 MB (56093682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7489e598cae5c0812e1ddaf1d0b649b6033369bedffceac2506c8d523d0a1c5d`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 16.1 MB (16061669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d3219f513bfa7d5289477f316932047bf97c5e63cdb25a5f5d84119699c8fa`  
		Last Modified: Tue, 12 Nov 2024 03:14:14 GMT  
		Size: 56.0 MB (56032476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f57fdf5c9316bd657fa92242f94a7a45fc7b72ff77e45c1afb81c50264750afb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7722954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da7c49e19c31ee997e83662326c7457752c1ae0084f5cf1d96e437c0a414b61a`

```dockerfile
```

-	Layers:
	-	`sha256:cac73e9dd9c0a64923bfc98da0ae2d1e496fc28c574c818636b78b29f41a46f8`  
		Last Modified: Tue, 12 Nov 2024 03:14:13 GMT  
		Size: 7.7 MB (7715624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea5177cad227d9b19951172f747480276aa38502fbfbca8407d68577dff7fc57`  
		Last Modified: Tue, 12 Nov 2024 03:14:13 GMT  
		Size: 7.3 KB (7330 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:curl`

```console
$ docker pull buildpack-deps@sha256:41a24bb5f87a336e821481c8495904b7ccab850ddb7d3c7819c2c4e2c7fb7cb9
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
$ docker pull buildpack-deps@sha256:41e41eb5a1eb21e97dc86dcc037ad0f73605f83b56c1c73464dd1db9196a4983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73634041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0afb2b1893cde96efc8d8210faaf240bf974567fcffc52c897c2f3c7dc9d79e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:986d0095b9a0c1ba3301eb55fd09b2d313291d46eb689d40f40ba5e22fe89c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4372469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d2308a6a913223982e9855dd8579b6c1952e064d55b55df3b488871308faebe`

```dockerfile
```

-	Layers:
	-	`sha256:ecebc53c12ddd3cdc651d3ac8588af340efb560dfff14086c45f26e4a6845d00`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 4.4 MB (4365306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b27611db305d9c1eaa6265accc831e7dd709d1ce5a580841bed26a4b03073d79`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 7.2 KB (7163 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:8e3fafd00e93960e28affb776bf24b68be5f16c8ae8264d6512d64e04638b301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70072054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ae47018992349a5e2058c7afa3cbbfad33c53a796b526639fdcbc544a232dd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:895d07844c9c09054971f530ffd0794c329a785344079a01ce24e3d51727407e`  
		Last Modified: Tue, 12 Nov 2024 00:54:43 GMT  
		Size: 47.3 MB (47338750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93efb128382700f7090be7bec74d12308eb11ced11717aae4403b7bccde20f24`  
		Last Modified: Tue, 12 Nov 2024 06:28:08 GMT  
		Size: 22.7 MB (22733304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5e697f44f82c828c459781743ae81c1b1fa2efd11d0ef16c315af40a6bf46a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4376053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29044c644def0ce321a888bed6b2e6a887e065d64284048b8cefbfab2415ff06`

```dockerfile
```

-	Layers:
	-	`sha256:0021462fa99eaa3af9d3f7856d66255747ce9d86290f0a67360aad6258734a1d`  
		Last Modified: Tue, 12 Nov 2024 06:28:07 GMT  
		Size: 4.4 MB (4368821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ccdb91b8a0e2609fdd39cee4ab8cac4e44254f455c3f6e89719b35df75eed9c`  
		Last Modified: Tue, 12 Nov 2024 06:28:06 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4df85825662d4ccaf0c53f0b0f706602fca0555267dd2d31a62e8ef87e1d558d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67110580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b88071c4591f6c7f807b8cad4c84e19227e69998bf7945120dfc8071b9014f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:46618ec96098836cac7950050ba554a969ebf8e9938d85d5f0d97015d3d25076`  
		Last Modified: Tue, 12 Nov 2024 00:56:14 GMT  
		Size: 45.2 MB (45150563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9660b2b46aa0c77f5dd078f4e57432faf3dbcda91672b9e3f8c1b7892e0ee2`  
		Last Modified: Tue, 12 Nov 2024 15:59:18 GMT  
		Size: 22.0 MB (21960017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:305784099f58635cead38aa11453521226000d86d85d52ee7848ca2c3be385c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4374834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8010ae6e055d2fc8797a75c67215cd400f64870bba5fb87b2503a4bb2fd1ae`

```dockerfile
```

-	Layers:
	-	`sha256:54c117e288564eb3719195c06d6bc879daa602feb6e27a0feb1a1ec9e18bf464`  
		Last Modified: Tue, 12 Nov 2024 15:59:18 GMT  
		Size: 4.4 MB (4367602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fcbbc798229c876fdfad98f81fb68cc54fb00ac95a2c847e9e133d91ce28ce3`  
		Last Modified: Tue, 12 Nov 2024 15:59:17 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e46fcc0c7385b7dccc516a32fb6dfc4d75a18dc39b9963b799d0cc2425554da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73185454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93ad60e192318acaeb45178aa2a8ced73c3b5c2075f1d0909094e482012ae304`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464f864cfaa846fbe1b8a889827404e18374f805d29d77c288a813ae8c4f6d91`  
		Last Modified: Tue, 12 Nov 2024 11:16:03 GMT  
		Size: 23.6 MB (23598253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7f238c1fe83bd003f1036848cda78a6c3cf076fcbed76560d0c41ed12edf3889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4372832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e335a8c4a64c4e0fae9e376895c95ac74dec942b688c1d5712b76326b89a71f`

```dockerfile
```

-	Layers:
	-	`sha256:a0d5ed8ce9f0036a2700ad927fefc558470f78b81f0b62876e96ad9516c09e17`  
		Last Modified: Tue, 12 Nov 2024 11:16:03 GMT  
		Size: 4.4 MB (4365578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3af911d4ac8fc50b9625684b9dfc26cb7861e3d51df952fe066d4eb1c8f230a`  
		Last Modified: Tue, 12 Nov 2024 11:16:02 GMT  
		Size: 7.3 KB (7254 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ac574690768b372f5dffd3fdba2f1316b68ee58133eada25d6f76b945c3503ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75476458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec174eb03e66f601edeb0488058e18636473d68377651065577803c0ac3d03f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:832e5094f1d1a0806638216e108f8c5f304112749840ba33b550928d48d45f1f`  
		Last Modified: Tue, 12 Nov 2024 00:55:00 GMT  
		Size: 50.6 MB (50577048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7251b79b00fcda89d3d742332ebf95721ed377cc22dfc14fb4cc7d2086df8c8e`  
		Last Modified: Tue, 12 Nov 2024 02:37:55 GMT  
		Size: 24.9 MB (24899410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d746769d0ce07c638d82090c56538afac5862001d98ec7ae5b23ae300ec87e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4369499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1441e57a6c764c8c7ccd95b08a608a908f3a9b0e5c6b666386e59faebc024b53`

```dockerfile
```

-	Layers:
	-	`sha256:8f720d960686e4104e12b5daa17252fea926f0989e5e2d35e3b5ace686835b71`  
		Last Modified: Tue, 12 Nov 2024 02:37:55 GMT  
		Size: 4.4 MB (4362362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce198488c58998d3efa8241e574d30337efbc03936c45f6efd2f314bd790083f`  
		Last Modified: Tue, 12 Nov 2024 02:37:55 GMT  
		Size: 7.1 KB (7137 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:de1a2b9066af1286e9d8175eef66425cfbddc0251cbdc6e6263a68b742ee6437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73211352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b5e3786aaeddd9bd8e5b8cd2245dc5be46353f3dbe4aa169166a83607577e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:17191dc8a469e4ef93330c5c8402fa0c0761218a5fa02ad2db7b34508d0e995c`  
		Last Modified: Tue, 12 Nov 2024 00:57:16 GMT  
		Size: 49.6 MB (49559181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf888157372a89189e8193ccb502b1003341993a439a6f526f90dc05a6100692`  
		Last Modified: Tue, 12 Nov 2024 18:00:45 GMT  
		Size: 23.7 MB (23652171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ee37e62e2a4f2b37b5059c26f65c50e79e8f12bede1551fe7c38dde1371e0e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 KB (7005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087a573000fee443714e51f8a22272ec23d27c5ef680d3b9f288f8ea41e63a91`

```dockerfile
```

-	Layers:
	-	`sha256:36da5312bc8de97460d5ca2df24b0a099c7af0db6158b101c163700559263cd6`  
		Last Modified: Tue, 12 Nov 2024 18:00:43 GMT  
		Size: 7.0 KB (7005 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:466f233ffc3b8ce8fc8e24fe4e0a478f467ee9c1b9e07ccaabb6d7f4dd82b50e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79272813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8258da2a3b826e8087b187be36e101338667cc4c8f4296ef4b30bf4867d89e8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9170cd93e372271efe7b34bbee8de26bbb094efba80a15cff49f580f87e5fe40`  
		Last Modified: Tue, 12 Nov 2024 00:57:37 GMT  
		Size: 53.6 MB (53555270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92051d5a3f7afdf0c89db06ce83fb963b8719a7024153e1520472673570e9d51`  
		Last Modified: Tue, 12 Nov 2024 08:29:09 GMT  
		Size: 25.7 MB (25717543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2238f5c37875dcd6505f74cd1d75fcbb33c40ab59512d84b295b8205ca2a6912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4377001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a107c661e17348313475322db42ffce8541848e8dd47876d57a3062cd14c027`

```dockerfile
```

-	Layers:
	-	`sha256:f1df1624c9d126aec722784a58ffe81fe99f97613ee2061a4ec42a2636a26b04`  
		Last Modified: Tue, 12 Nov 2024 08:29:08 GMT  
		Size: 4.4 MB (4369799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18a16b8c21a8a4d843e70acb35845f9570090375bdc2418cb56cbc1f86835707`  
		Last Modified: Tue, 12 Nov 2024 08:29:08 GMT  
		Size: 7.2 KB (7202 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:556f5aa74f180a341fe894576c8df3a358c7ad6432d78efbbc0da3bb71f523e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71996571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cac9802c1503429c3afb4b5bcf9abbc62bf5678126c5a817806438584d76da7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9f9f8fa8b12064144bd5037b70d4d9ac4fcbcd94f2921feb1e017764a273f798`  
		Last Modified: Tue, 12 Nov 2024 00:58:23 GMT  
		Size: 47.9 MB (47938688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53b034664a3d7aeeede4479f8aebfb2fff094119ae93ccf99e62d557e92b31f`  
		Last Modified: Tue, 12 Nov 2024 09:01:46 GMT  
		Size: 24.1 MB (24057883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b5638e5d412c4935cdb5c941063892a1c760db5bd429ef01755d419da71ac16e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4372167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7196d3bd3ce51a1e06975a87f93ccac12d11dcde272e5ea99e71a63a7bf9d9b6`

```dockerfile
```

-	Layers:
	-	`sha256:86a46b41b61f05b5bf553bb19fecd56edefa4c046740d61578dbcfda5746f13f`  
		Last Modified: Tue, 12 Nov 2024 09:01:44 GMT  
		Size: 4.4 MB (4365003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63952b86a5ed4c59bfbf8d5f3f31a85aed5da9a9298e45cbdcf514945aedb636`  
		Last Modified: Tue, 12 Nov 2024 09:01:44 GMT  
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
$ docker pull buildpack-deps@sha256:50daa6a4a65cbac68729b91d5d06a1868478187249e698c87a2fb6e1f7cd51e9
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
$ docker pull buildpack-deps@sha256:dfed95ded883b6221ceb01535be2c71864524606aefd9f39949acdb699e2c00c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.3 MB (349319218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd41bc93efcd7b454fddab4980d002a30aac51e898252f069988c36ca1cbf063`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2112e5e7c3ff699043b282f1ff24d3ef185c080c28846f1d7acc5ccf650bc13d`  
		Last Modified: Tue, 12 Nov 2024 03:58:28 GMT  
		Size: 64.4 MB (64391376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af247aac076473044d24960a352a8ec6f154cf0a28f4fbf35fe5d43b52687ba2`  
		Last Modified: Tue, 12 Nov 2024 04:55:08 GMT  
		Size: 211.3 MB (211293801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:88f0760f365d43d99e88c2c6c5f2efd4b604c21d71066254c3a95c591389825c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15508351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec10518bd3b236cdf9e7e299443317c4d3acea2d1d813eb18856745df0c8a77e`

```dockerfile
```

-	Layers:
	-	`sha256:84596790680ca7003b3b19983029b13d9eaca878c1b8bfb32be4d3dc30c06db8`  
		Last Modified: Tue, 12 Nov 2024 04:55:06 GMT  
		Size: 15.5 MB (15497811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6cf56ff8e4b2e1dbe2a80e23d5505991b3f7fb5386efd3ec112fe58e0de491a`  
		Last Modified: Tue, 12 Nov 2024 04:55:05 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c46a02bfc21fd7053f71092fa78fa842bbe70d7d3e8974a8f3e0d74c644ccaa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.7 MB (316656991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:978045ca96d7326e22edd7f3435c24ae52863a21d0e3c7300db1f7ffc12a58ec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:895d07844c9c09054971f530ffd0794c329a785344079a01ce24e3d51727407e`  
		Last Modified: Tue, 12 Nov 2024 00:54:43 GMT  
		Size: 47.3 MB (47338750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93efb128382700f7090be7bec74d12308eb11ced11717aae4403b7bccde20f24`  
		Last Modified: Tue, 12 Nov 2024 06:28:08 GMT  
		Size: 22.7 MB (22733304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5d34c31582cec80127fc538f65a56104fac2a20c87dbcaafc70b88f7a0a8b7`  
		Last Modified: Tue, 12 Nov 2024 11:29:42 GMT  
		Size: 62.0 MB (61996880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95228092402ee38dddb194f1bc5fef6e2e5917508ae15c94e0a077aa28cdd790`  
		Last Modified: Tue, 12 Nov 2024 13:53:10 GMT  
		Size: 184.6 MB (184588057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:068453375709d05dfab2e4f14fa04e65107704f3f15168fb7fadfc8922cbdaa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15307030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b3d2e6239bad3254d95f9349fb85402afcf4ea34b641d2c5bba65fe20ce54b`

```dockerfile
```

-	Layers:
	-	`sha256:bf286d0910d797df5b78752d6a8354956fb50cbd4a09db96b2e373c0f7358f01`  
		Last Modified: Tue, 12 Nov 2024 13:53:06 GMT  
		Size: 15.3 MB (15296422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dbd9d8c58fb1bb6415885f21668416442eec559a928dedf198c14f800323de1`  
		Last Modified: Tue, 12 Nov 2024 13:53:06 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:06bb2db41f7fbeb1ec1b7250e0bd11f1107b7c431d2089d90ced37389022d435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (301951405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d9fe338d80f977597c98ae1e707ffa5d324da2a547b20f01e17705aa675bea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7fd5031c50fee563f16760ae6e5334672d6c9ba07d159b9e3a17a3b62011`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 22.0 MB (21957404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542f68420f2ab6efd74aba4b4ff72fe115144308ecea01703acfd9de4db386df`  
		Last Modified: Sat, 19 Oct 2024 06:36:59 GMT  
		Size: 59.6 MB (59635104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad67b816dd3ebfab16dd19d0768f67e218ed3070e064a66bfa1b026ea84191e`  
		Last Modified: Sat, 19 Oct 2024 08:07:03 GMT  
		Size: 175.2 MB (175210957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0314a3678d8f3f88eabfb762a695986a02033d8fb22d77a5d6f5068b717b407c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15312390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2a075e1bcaa59170be86abde46ad32565b5db5716b6bd4e3da16477be91660`

```dockerfile
```

-	Layers:
	-	`sha256:690295df0718cc2104e887058f7a94786df16dea2499af3f048f8511ab87238a`  
		Last Modified: Sat, 19 Oct 2024 08:06:59 GMT  
		Size: 15.3 MB (15301770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d637639be757ccbf573e7b4da768bda5c46ef6deff9a9496fc6e85f0a17b9c7`  
		Last Modified: Sat, 19 Oct 2024 08:06:58 GMT  
		Size: 10.6 KB (10620 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:76778860e25ffd9449a5994b5617879cc83c194ea51d1d8f9ab1a157d3391e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.2 MB (340173078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65e32d70e63fc1d3ada53df6166c0952afb010d4eeeaf2703b3e4b858f866af0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5594266b1bacf9ad6855b00d9c5c98e721001eb115218eda673e548e04fdbf`  
		Last Modified: Sat, 19 Oct 2024 05:17:15 GMT  
		Size: 64.4 MB (64350044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d4884f85282b9a352dbcedf2cccd073a63e60b151be84375ce9279dec1c553`  
		Last Modified: Sat, 19 Oct 2024 06:16:07 GMT  
		Size: 202.6 MB (202644222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ddb4caa8d4e2a15bc8aff07048659c0464e1bd2e7d3d764a302f33abf3c24339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15536872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7b433acebb5d16e21a72e9664cc189b65f93aa069993c6093cf331dc21a67e`

```dockerfile
```

-	Layers:
	-	`sha256:8aa4d837f97e1bd618517d2b35e969ca84b0fb0999327cd9e82b934e5e8feb3a`  
		Last Modified: Sat, 19 Oct 2024 06:16:03 GMT  
		Size: 15.5 MB (15526229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7f3e5acc815d52ab17f8f3858cd0738538ffefcb45cdee80e1b80809203edff`  
		Last Modified: Sat, 19 Oct 2024 06:16:02 GMT  
		Size: 10.6 KB (10643 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c93bf79e093bc04f8c7b6197e087be2b58188acbffba4200487f158970c815ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.9 MB (351897372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20085e6d5ca38d0d5efc920deda4f2c7b7f1cc516d13009ea742ea8158c2e446`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:832e5094f1d1a0806638216e108f8c5f304112749840ba33b550928d48d45f1f`  
		Last Modified: Tue, 12 Nov 2024 00:55:00 GMT  
		Size: 50.6 MB (50577048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7251b79b00fcda89d3d742332ebf95721ed377cc22dfc14fb4cc7d2086df8c8e`  
		Last Modified: Tue, 12 Nov 2024 02:37:55 GMT  
		Size: 24.9 MB (24899410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c46592415d8ae65247d6cff038217c0ae0c38f5f2fee88eaa3f5ae09743a290`  
		Last Modified: Tue, 12 Nov 2024 03:14:24 GMT  
		Size: 66.2 MB (66211304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f62d20ad9a58cf75459d448e04c818e5c7b20e4e0a9bd426ba0fdb30a427c0`  
		Last Modified: Tue, 12 Nov 2024 03:59:17 GMT  
		Size: 210.2 MB (210209610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0d785b0b0dfdc303e5c56e4d82f2d2bcd5324e327f7369f8a74f002fa09de00d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15486902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48cdd77c324b475203dfbffac68943494c3b20562c2fd7429bf011a97c6e523e`

```dockerfile
```

-	Layers:
	-	`sha256:3a3c6d3d3ff3129f37bfb0c59da4947b5efcfd67883d5459c890df826501384b`  
		Last Modified: Tue, 12 Nov 2024 03:59:13 GMT  
		Size: 15.5 MB (15476390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9258c5560c651fe26a375f83d4a42a46cc4ebaa1259d05526d19698320d05260`  
		Last Modified: Tue, 12 Nov 2024 03:59:12 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:7f2bc5242e17eac9490e908a2be63894f0a7381dcee30ec3dcf97ffc7e9f66cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.3 MB (326336355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc411215ceea19c8d66017c4c6c30a8263150a2170118d61d0188869e4adcdc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:5fa3d47e52ee376ed002c84d34e93fe11e6db2308915238c5d7a9a5840814eda in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bf8417b2ab139177317d556c6249cee54f60148ccee016ec60d45a13a21c7c2`  
		Last Modified: Thu, 17 Oct 2024 01:17:24 GMT  
		Size: 49.6 MB (49561619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba3cc6e574320e30c42f84b70c8e03fff0393ea65f20833b10b3a8aa1415e1`  
		Last Modified: Sat, 19 Oct 2024 00:56:12 GMT  
		Size: 23.6 MB (23648020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d702889c46052954a44f8b6ab39510d9b55acfe4a180194a7cb475c90b2b76e`  
		Last Modified: Sat, 19 Oct 2024 02:08:09 GMT  
		Size: 63.3 MB (63284387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbfb08e05dc5bd87f1bd1a6b1f7e1b3b709ea1bd67292b849b2cb2c26e2e7f3`  
		Last Modified: Sat, 19 Oct 2024 02:59:32 GMT  
		Size: 189.8 MB (189842329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:61877dcc36039290e4794b30548c16e84cba90a23025191394e70b71ae1c7e34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f6b2043ca0dc4f8dfd910788dc24c8058ed42300412714c5cc8ef674411cc86`

```dockerfile
```

-	Layers:
	-	`sha256:d284443815833cb6d5b05811d4a9aeeb5999f336721792c8e9b8df2051fb143c`  
		Last Modified: Sat, 19 Oct 2024 02:59:14 GMT  
		Size: 10.4 KB (10394 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:855a926cac624799b5b29e9e12c4a338a63508a60be4531db78f1854f45fbb21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.4 MB (363387524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4970e9caeb34b2bc82b8ac0a0fa85e493b833304680e062d0ad48796f31e459f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:c7ce4329d7c0cdfb8efa822e20a44ab1922fe70e4e8be36a317ec45c565a260b in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bbeb3fa4a5ad17047af70a984a8c9e89b0702821c59cb2290ff6c49eec8d704f`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 53.6 MB (53555597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1823a3ab0dcc6f88db2bc0c18d80304ad0e6a3cad08984b6ce0a7abefd371d55`  
		Last Modified: Sat, 19 Oct 2024 00:56:54 GMT  
		Size: 25.7 MB (25705977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3666a280304f3727f745e818ab5e252dd98676495517a360e23f821dee0fa6`  
		Last Modified: Sat, 19 Oct 2024 04:07:03 GMT  
		Size: 69.8 MB (69825530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81280667d7d6fa822ac7a45807cf98017526f614373fad289bacbeb84f61f73`  
		Last Modified: Sat, 19 Oct 2024 05:17:30 GMT  
		Size: 214.3 MB (214300420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b82239446d14aa796e3669145e0e4144e317024a47609818e67ccbd29abd061b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15484578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff7ba63cf1b1fdc77923361094664727253800983f28cc61f7aad9a84413081`

```dockerfile
```

-	Layers:
	-	`sha256:865d6af4dc1d0e2e578fa465f323f0b0362de6a63a4a7ddeb009cb407518f3a3`  
		Last Modified: Sat, 19 Oct 2024 05:17:24 GMT  
		Size: 15.5 MB (15473988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c857e04d79ec517fe7bdcb6e41dd0c8e8e8f030360535d2f3ad03f299fac1efc`  
		Last Modified: Sat, 19 Oct 2024 05:17:23 GMT  
		Size: 10.6 KB (10590 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:976e837fdf70dcad33dbb610aafc511db5e9e60883e690bd7682cb21557370fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.8 MB (318783168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb932672417afb874ffa1d6dcf687e42f3012df2af781a13680c2312d984d00d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:be1cd8a5c7d60ebbe308ecf258da8f3d2dd59f7c877549c96e98e31165ba1eaf in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:510daf83b7a2b266658f37f8849eeeba99ab0f02d08ef5c1ea7f613451a81239`  
		Last Modified: Thu, 17 Oct 2024 01:50:15 GMT  
		Size: 47.9 MB (47938447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b213e07d4abfcac72292a81e546e7d80ad0bd5377b4de866c7a61ca19b5837c`  
		Last Modified: Sat, 19 Oct 2024 00:57:06 GMT  
		Size: 24.1 MB (24050397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a99db1e4eb0a57b7be4b1376a7fdf886d4118a6263595ad414d052eb69ee9b4`  
		Last Modified: Sat, 19 Oct 2024 03:46:26 GMT  
		Size: 63.5 MB (63494580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2eccbc8d9b18898de6fc12769f52101d4af82f32957d095f8ab217c6886c2e`  
		Last Modified: Sat, 19 Oct 2024 05:04:19 GMT  
		Size: 183.3 MB (183299744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ed818f64d43e758653782aa4360eb15f84ce2a0952f08c9a9c2eb514723b2d34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15320678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2d212ca9b7a5946af205d9faabe9078a4422f84204de3eff0b79a4d9c76652`

```dockerfile
```

-	Layers:
	-	`sha256:150045fb989d3aa406e6943b9a50d396ee3d83ca315d5b553f09d68b02783d8d`  
		Last Modified: Sat, 19 Oct 2024 05:04:17 GMT  
		Size: 15.3 MB (15310126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6d6b263a153d82f2f5af8d644a5c79f02fa8cf89453e0498e1e3ec099c03301`  
		Last Modified: Sat, 19 Oct 2024 05:04:16 GMT  
		Size: 10.6 KB (10552 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:a2c379af057a249a7ae251d68571aadf7dd43837219ff38e4e797eaa408cf417
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
$ docker pull buildpack-deps@sha256:28ea314ba57e342bac3799c06c1a8d44cfe585fc0f66bf3719030da3cb2942d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.7 MB (279731027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34bda0190071cc444553b7a709fd8cd57d63a7c2c2186ba13b47282c6abd6acb`
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
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
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
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb10f2d793001e79ccc6be8c28ad194b0142e46f3ea6c14095699bb7ba44ef3c`  
		Last Modified: Sat, 19 Oct 2024 02:06:23 GMT  
		Size: 13.6 MB (13616706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ed9a6a1726d06e0402223e684a198aad45fe01804a81aa58967a03d085b6dd`  
		Last Modified: Sat, 19 Oct 2024 02:52:33 GMT  
		Size: 45.3 MB (45337669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ed0593d2f3316b832ab07d1fbfad306dbde92bee837a9184eb10b2a3300bd0`  
		Last Modified: Sat, 19 Oct 2024 03:53:25 GMT  
		Size: 191.0 MB (191026289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:74cb68ef31f5c607d038fcb183848fcaffb976bd546d14dae852e490e46b56cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11373351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a8a6050b4550be41f53ffa005549538f26068b3cacf2abfa1da72aa307bd59`

```dockerfile
```

-	Layers:
	-	`sha256:d7c719a514e8fc78963ff42a7fb6ebbd21a0ff436cd8a5186432d7a685f011cf`  
		Last Modified: Sat, 19 Oct 2024 03:53:22 GMT  
		Size: 11.4 MB (11363167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c096c09217c24f206f019b6dc90b89e2b27ac53a5d6eaf8626e3d44371ca1646`  
		Last Modified: Sat, 19 Oct 2024 03:53:22 GMT  
		Size: 10.2 KB (10184 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6df0bff9783b406ab00cbbda757f863979ba37f124d5f652a7aef6590dd93034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.8 MB (239782925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2613357626d500c34646039b65cf3728fcb7ee25fcba491909817b4d127793`
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
ADD file:eba80434f5df435e13e0c4a971c865a8fe930d18d36089192130267316506ded in / 
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
	-	`sha256:7749ef83ff0cd36ce0d199799a4be8de9b91c6731f586202ab39a4605d27c4c7`  
		Last Modified: Fri, 11 Oct 2024 05:07:29 GMT  
		Size: 26.9 MB (26866046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88500305391cd04c9a51ca6c9aae31a7f848fe911db6b2e22771dc1f0ef20864`  
		Last Modified: Sat, 19 Oct 2024 06:46:02 GMT  
		Size: 12.8 MB (12774273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a981c012b2ef93c0e4d3e5c624f415b9703e3e959bb801b3dd95edaebb3125`  
		Last Modified: Sat, 19 Oct 2024 08:19:59 GMT  
		Size: 48.9 MB (48888193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6111e812a892c1df5c539e5b9144e27e342290cd1693c23ea9a0fd9af6cb81e`  
		Last Modified: Sat, 19 Oct 2024 10:39:31 GMT  
		Size: 151.3 MB (151254413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8ddf5e5c2e97e71884c6af59abaf942dda549a0a8e4349acddc30bf53aaca77c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10720345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69080b2ac5985eaef5312663eba1507c3e224f0ca99d510ec3e6c5f24af1e6af`

```dockerfile
```

-	Layers:
	-	`sha256:ff09a1a21c7a669640b186c38daf3432183226bb6915336b625e08abd0f519d8`  
		Last Modified: Sat, 19 Oct 2024 10:39:27 GMT  
		Size: 10.7 MB (10710101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d7cb0cfc1d43f5f4dd6b09ac9eee91b4f76fb782e39f64fbd2831d27f34b482`  
		Last Modified: Sat, 19 Oct 2024 10:39:27 GMT  
		Size: 10.2 KB (10244 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e86d60447a52a1d6346524144985645a0423e4438ac233095fbc47d240456122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270652388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61a37454df2d40c917660e881cfea5faf51970ec24bf7ec4bcbf36147b9cf49`
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
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
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
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4950c6def722ac96f41618bdff1f82e38c2b3d5849ce2c07b4049db764444b`  
		Last Modified: Sat, 19 Oct 2024 05:23:22 GMT  
		Size: 13.5 MB (13452782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a3b9ee069311be4d8fca64a1f65e93cf73601746ef5283dfcbda615585143a`  
		Last Modified: Sat, 19 Oct 2024 06:27:05 GMT  
		Size: 45.3 MB (45297451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b98ba6826884a2dad7daedbb1abf09b61205cdbe1087c0d7f2cc328a44d2576`  
		Last Modified: Sat, 19 Oct 2024 12:49:21 GMT  
		Size: 183.0 MB (183016310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:487291d9e5158e997ddcee07b7408e8ec4675ebf87af60ea1b6acc29af0ca097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10942902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d377595d1f627e3b763cc7f7cc0d30f37e6d0cd1c2475fe6e99bdf32a75aa21c`

```dockerfile
```

-	Layers:
	-	`sha256:73bdac28c0f1e731d44a1bd44adbf20ae706d6d04310ea44cb41713a52d534a9`  
		Last Modified: Sat, 19 Oct 2024 12:49:17 GMT  
		Size: 10.9 MB (10932639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9b7bed5da457db1844d3d47e9497ba0a94df919a495851764dfdaf6d6d48e2c`  
		Last Modified: Sat, 19 Oct 2024 12:49:17 GMT  
		Size: 10.3 KB (10263 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b136aa8ebec3bb967cc748b99e9041c7df81fa0657c03f91136c543bc747513f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298476454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a7466eeae1673a2a6eac2e305c1e044edc3a09b06556eba461f50b1566da56`
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
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
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
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5bb7422168207a94659a7d755a71642577184a266af0a8a3afb47316450f6c`  
		Last Modified: Sat, 19 Oct 2024 04:14:07 GMT  
		Size: 16.0 MB (15990504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48479dfc2b7d427cb9b67d6c2ae25148b5cdad254e89920f302994550cebd409`  
		Last Modified: Sat, 19 Oct 2024 05:30:15 GMT  
		Size: 50.5 MB (50501654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378c1db9206641309be4ad1ed79478d79b600494ca52532597de42a2b7a249d4`  
		Last Modified: Sat, 19 Oct 2024 14:06:18 GMT  
		Size: 197.6 MB (197595327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c01988cb15f09691ff8b01e0328e80006a031f3258d706abaf30c43e0319b9c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10890029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6fed5214b877e2ef17d810fdefb5ec60b07bb5cdc66600357fe12e36dc36b9`

```dockerfile
```

-	Layers:
	-	`sha256:467c9adaa1534646b005cdb1ef70ebbebe92475898081a075c6e0177838ba246`  
		Last Modified: Sat, 19 Oct 2024 14:06:10 GMT  
		Size: 10.9 MB (10879813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8f22eda885975b6b07ea3ff187a442f984cd2da711532ddcaa211c23421c961`  
		Last Modified: Sat, 19 Oct 2024 14:06:09 GMT  
		Size: 10.2 KB (10216 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a48cd0fe0e3c96594b73a23e16a9f5f31cdd20d3dbb21889bec661254886606c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.0 MB (330029007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9914ffe80b60c5d35aa4ca731a127513eab9e5a4d21a9f132c9eaa136e80143`
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
ADD file:008d2e9e73153005eafa485b2ecca3ca9fd6996da5b5c99a52a7376427350f8d in / 
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
	-	`sha256:53300d777b1a34c849b57f3a3ccdc52f3ad795ea045079e7bcca5f63efab0327`  
		Last Modified: Fri, 11 Oct 2024 05:07:42 GMT  
		Size: 31.0 MB (30951587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a51cb0bf7686a8c2782160996192e9d89c09949101fc6d8c09083eb1013e91`  
		Last Modified: Sat, 19 Oct 2024 04:08:40 GMT  
		Size: 14.3 MB (14320414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0a2eaf274204c5bf93c79db9bc33e24b045b07aacb49995d18798544f6f56f`  
		Last Modified: Sat, 19 Oct 2024 05:41:12 GMT  
		Size: 53.8 MB (53801364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4a00631efcf264d6f9c5d8e41eee22c784fe6c727c1b65108038ef79a629b0`  
		Last Modified: Sat, 19 Oct 2024 07:50:42 GMT  
		Size: 231.0 MB (230955642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:de8c1a1ec27d92b20abc2f5650dd64af570c41d20931db30c0388d3370ed6ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10878952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65989ed3c96055e01b2f0033330d1a72ca1763345e024c3b6af226128a57aa98`

```dockerfile
```

-	Layers:
	-	`sha256:93701c93d6240b07395f73b128019d2a57242924acf950bccb621dcad2cb367a`  
		Last Modified: Sat, 19 Oct 2024 07:50:13 GMT  
		Size: 10.9 MB (10868736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ebba5414a868eb48c1037144a61dd35172010195fb71a791d9d80cb2a56c48a`  
		Last Modified: Sat, 19 Oct 2024 07:50:11 GMT  
		Size: 10.2 KB (10216 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8882db19e6755eb70cff00b9ab99c4e1eee12dddd74c4c6e46b0541cc6c8e4bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.1 MB (262094181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cffe492eab9f9ed8773d2b2a20e04bac69cd7543c8b9a9fb973fa1c15cf7dfe`
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
ADD file:77ba16e2cf3c210906ec7587ab14314afc15cb73af4337fde69ac35187fdb263 in / 
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
	-	`sha256:3d2abe11fb3bab133e95a31c3eeb04ba27eaed096cd5d4d3baeb8f12c3473633`  
		Last Modified: Fri, 11 Oct 2024 05:07:47 GMT  
		Size: 30.0 MB (30019614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1e22806c936cf352e8613a36cc00e41a5fc02ec3a1756fa36d836ba0f8dd58`  
		Last Modified: Sat, 19 Oct 2024 03:51:58 GMT  
		Size: 15.0 MB (14974773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3949ce1635c27257c28d76c25291d89d75979fb73e8177e9220f5e051d01fddf`  
		Last Modified: Sat, 19 Oct 2024 05:13:20 GMT  
		Size: 46.9 MB (46923171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4691bf2965046c25f376c2a1cdfcbd9c93c528a56464249e4aaff8d9bfe446e3`  
		Last Modified: Sat, 19 Oct 2024 07:01:51 GMT  
		Size: 170.2 MB (170176623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7807c6e272fe6f4640072ea3e39d7b2cd741f5025513129276568b362c231d50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10735725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9020d42999b45905436b9fce6b0368db0877f80ed31d2360ad50c6cd1fce82bc`

```dockerfile
```

-	Layers:
	-	`sha256:508877c0409dec14e70443d06c870e2ed2fe781820e7ed895cb0de132f6f0125`  
		Last Modified: Sat, 19 Oct 2024 07:01:49 GMT  
		Size: 10.7 MB (10725541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab8c395543308d5310678a3ac6bed1a1588cb39882a045f402dee11218c16300`  
		Last Modified: Sat, 19 Oct 2024 07:01:48 GMT  
		Size: 10.2 KB (10184 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:61a02a85f7bd808d46ba3bd1dd757f277dc3026c68497a61d40c954ae277519a
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
$ docker pull buildpack-deps@sha256:69a53f84746bd2372529e6294f001436f888e30870daf61281a69619b86057ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43367069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5303bd2f189e17d8fbd2e62d67886dec77343f278c3c75cd273d299207c7b73a`
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
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb10f2d793001e79ccc6be8c28ad194b0142e46f3ea6c14095699bb7ba44ef3c`  
		Last Modified: Sat, 19 Oct 2024 02:06:23 GMT  
		Size: 13.6 MB (13616706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c0dff7df9d3a560fec4504795a8a76af7930b39ab2547e3ad5d56ae1246b7712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33382ecb57f630cddd0121e9581f247c374c0a13913cca08bc2ae9cf658ed9c8`

```dockerfile
```

-	Layers:
	-	`sha256:aae0f7d55899e7c0940b7b61d432d39e39e21cf565b7228a0eeba668dd220f63`  
		Last Modified: Sat, 19 Oct 2024 02:06:23 GMT  
		Size: 2.5 MB (2460121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5e5735a561089783c9f33d6a1c22c03d2914ddba32944dc3804408ca6f390f8`  
		Last Modified: Sat, 19 Oct 2024 02:06:22 GMT  
		Size: 7.0 KB (6959 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:bf67b389c162359f2b441024b2b7f89697063af26786e43d3ba27dd16b346d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39640319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d70429189febc1c7f120a2728c8d4a2b2b36ca1101c112ab10b03c376932632`
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
ADD file:eba80434f5df435e13e0c4a971c865a8fe930d18d36089192130267316506ded in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7749ef83ff0cd36ce0d199799a4be8de9b91c6731f586202ab39a4605d27c4c7`  
		Last Modified: Fri, 11 Oct 2024 05:07:29 GMT  
		Size: 26.9 MB (26866046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88500305391cd04c9a51ca6c9aae31a7f848fe911db6b2e22771dc1f0ef20864`  
		Last Modified: Sat, 19 Oct 2024 06:46:02 GMT  
		Size: 12.8 MB (12774273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0a4a978974bd38c1c6b56539b3ade7a20d784dabcdde222fea7c10ab1952d423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2469442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753a918dea5e27dff5ccad5ffbdedddcd18560a8ed92d0ffe7e85fc413f2caaf`

```dockerfile
```

-	Layers:
	-	`sha256:f6ee94b67ea69af693bb63300fcd2a72f7c7b0641ebb305828624092a786d5ad`  
		Last Modified: Sat, 19 Oct 2024 06:46:02 GMT  
		Size: 2.5 MB (2462424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a08b7584e68e048ec746fad58924742a4448c4aa658c8176d0cc77ae4d8aa9e`  
		Last Modified: Sat, 19 Oct 2024 06:46:01 GMT  
		Size: 7.0 KB (7018 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cdaa9366946071023e1f96102056d61ee8d5813c648e5e443ad775377a9aca37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42338627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd103c37af2bfabfeba88731e3900a13344638ade7dd0cf35713c06b44c019a8`
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
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4950c6def722ac96f41618bdff1f82e38c2b3d5849ce2c07b4049db764444b`  
		Last Modified: Sat, 19 Oct 2024 05:23:22 GMT  
		Size: 13.5 MB (13452782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d597e073523447174c59bb9339d4e921315e6010cd65e7a8755ff6115fdeb031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9c60a9160ad5646d9fc916f16cbb8b13ab91a4d08eb7b0212b2ae4f0f735e0`

```dockerfile
```

-	Layers:
	-	`sha256:e53b756c5aca4d1d0fc8e68b5476dbb34c0592709fa3d5c106120d622d0d4a20`  
		Last Modified: Sat, 19 Oct 2024 05:23:21 GMT  
		Size: 2.5 MB (2461179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7983d358f6b848383136c8117c7dcf53cae037638cf1ffb01ee404c5bb6e3666`  
		Last Modified: Sat, 19 Oct 2024 05:23:21 GMT  
		Size: 7.0 KB (7039 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b655e7c7154dd2e45e599d42b4097933c95c98cf7b78b205fb4822c1d0fe43b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50379473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:778119530d1d3acb12623754e4aca31b15520b5e05d341cb87242e71bf02b11e`
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
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5bb7422168207a94659a7d755a71642577184a266af0a8a3afb47316450f6c`  
		Last Modified: Sat, 19 Oct 2024 04:14:07 GMT  
		Size: 16.0 MB (15990504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e9bd42e00d50a337eb6ae71acada0521952731d883ac3674c61ede4b6941cfa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2471598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc9ccef8ea2d95e6746f6910ef5c892fbd2fccf5633f3131aec3d0c40461a20`

```dockerfile
```

-	Layers:
	-	`sha256:cbbf862c11201133c8b1aef247405d5920b029ac32240b23d848dd20991ac250`  
		Last Modified: Sat, 19 Oct 2024 04:14:06 GMT  
		Size: 2.5 MB (2464607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15c4b71488bd7802d0d94fd3377dc27a700634f63f50d3d5032eef9f97d50589`  
		Last Modified: Sat, 19 Oct 2024 04:14:06 GMT  
		Size: 7.0 KB (6991 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:ed5ce75d1f4a620f01d0702d00faccfb5034aa47070c521d27be46692bc8b17b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45272001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa560d2123906a1eb27b1cd3fe84a41430d89dedc458d78495edb54a85e0cf3`
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
ADD file:008d2e9e73153005eafa485b2ecca3ca9fd6996da5b5c99a52a7376427350f8d in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:53300d777b1a34c849b57f3a3ccdc52f3ad795ea045079e7bcca5f63efab0327`  
		Last Modified: Fri, 11 Oct 2024 05:07:42 GMT  
		Size: 31.0 MB (30951587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a51cb0bf7686a8c2782160996192e9d89c09949101fc6d8c09083eb1013e91`  
		Last Modified: Sat, 19 Oct 2024 04:08:40 GMT  
		Size: 14.3 MB (14320414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:de682863d227036d5fe3a3d7207a85d92150a6d9b33ec0eb35f889ac3ff1471e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df1d0f629afff1832da077572992ad1229b1a9418393fc4bf4a1dbfec892ce96`

```dockerfile
```

-	Layers:
	-	`sha256:5da38e61e6a6326b47d7e44c6dc7b33b4a4b50f7ba4c1b11a697e586c7125702`  
		Last Modified: Sat, 19 Oct 2024 04:08:38 GMT  
		Size: 2.5 MB (2454205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fabf745c39c42d34cc0c475f1e2405f99e54eb30c56c802a0faa5b6401afadbb`  
		Last Modified: Sat, 19 Oct 2024 04:08:38 GMT  
		Size: 7.0 KB (6991 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cf2a4959c2ed6d7db6865a457e57f54f9133f61bdd71b89242b459a082ef2537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44994387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a458243e47a17fd216799e5fff9f87276e7519972bc41b477bd5f94785b8e2e`
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
ADD file:77ba16e2cf3c210906ec7587ab14314afc15cb73af4337fde69ac35187fdb263 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3d2abe11fb3bab133e95a31c3eeb04ba27eaed096cd5d4d3baeb8f12c3473633`  
		Last Modified: Fri, 11 Oct 2024 05:07:47 GMT  
		Size: 30.0 MB (30019614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1e22806c936cf352e8613a36cc00e41a5fc02ec3a1756fa36d836ba0f8dd58`  
		Last Modified: Sat, 19 Oct 2024 03:51:58 GMT  
		Size: 15.0 MB (14974773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8d29373003ee556463b8160d06035b70e7db1c3ec70559bd70c6195c677c2d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2469910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754d483c2a3ff5a5c1d88c4e43d97d4898d69fcbe01129c3a527042b92293f4a`

```dockerfile
```

-	Layers:
	-	`sha256:b81404d5535fdfe5a867765c9910eec76fea2b0b598aea04c12256f25e7ca67e`  
		Last Modified: Sat, 19 Oct 2024 03:51:58 GMT  
		Size: 2.5 MB (2462951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba29dacf77349b19b8ba8519424b7ffc7358b40c96462346edb75c87b78b41da`  
		Last Modified: Sat, 19 Oct 2024 03:51:58 GMT  
		Size: 7.0 KB (6959 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:noble-scm`

```console
$ docker pull buildpack-deps@sha256:7c6bcb87a65951b2e02f596e3b6a80492d3e692d53407d1448d7a909abeeaace
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
$ docker pull buildpack-deps@sha256:8eab756f646b732a7dc889ae8b8edc6b7910c99a726dbfef4d55b84e097001c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88704738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc073b53d6ac3a55820ef7f37b3b01f8eab8d306c872ee6dd8cc8c3273bfb59a`
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
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb10f2d793001e79ccc6be8c28ad194b0142e46f3ea6c14095699bb7ba44ef3c`  
		Last Modified: Sat, 19 Oct 2024 02:06:23 GMT  
		Size: 13.6 MB (13616706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ed9a6a1726d06e0402223e684a198aad45fe01804a81aa58967a03d085b6dd`  
		Last Modified: Sat, 19 Oct 2024 02:52:33 GMT  
		Size: 45.3 MB (45337669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d2a09e9dc33036b61d80e379ffd5129d921c9af74fa05aac5fca717149fb56f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5083384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9cebdd3000d8052a20f7ae88451c5cd8ccf95751b8cbbd1374dd8c343905396`

```dockerfile
```

-	Layers:
	-	`sha256:fb57808df518ee10975192da49d52cf1942c3a864b2a5633e74b8359dc522a03`  
		Last Modified: Sat, 19 Oct 2024 02:52:32 GMT  
		Size: 5.1 MB (5076079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3045d24ebd20c1b16edafcb0f97642f4592eece82164dc9a906540d80177a4e`  
		Last Modified: Sat, 19 Oct 2024 02:52:32 GMT  
		Size: 7.3 KB (7305 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3cd10ae720029b6f1e428242a31c39af8ac4cfbc7117cd5d4d5287d8c5c87b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88528512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e16b3a161f0305bb749b01f52df04acf799601cb668fc2c55dc38b372834938`
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
ADD file:eba80434f5df435e13e0c4a971c865a8fe930d18d36089192130267316506ded in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7749ef83ff0cd36ce0d199799a4be8de9b91c6731f586202ab39a4605d27c4c7`  
		Last Modified: Fri, 11 Oct 2024 05:07:29 GMT  
		Size: 26.9 MB (26866046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88500305391cd04c9a51ca6c9aae31a7f848fe911db6b2e22771dc1f0ef20864`  
		Last Modified: Sat, 19 Oct 2024 06:46:02 GMT  
		Size: 12.8 MB (12774273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a981c012b2ef93c0e4d3e5c624f415b9703e3e959bb801b3dd95edaebb3125`  
		Last Modified: Sat, 19 Oct 2024 08:19:59 GMT  
		Size: 48.9 MB (48888193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:39c0f3d8abe6f4afd0242c7b449931a0bb21724b5ead8efe3c45c3b6913dbc81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5084737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf11b3d8775bd3422f2101fdabbc1073cb34db0f6228c997645fa5811fc8c920`

```dockerfile
```

-	Layers:
	-	`sha256:5578902e989bba6e6b2f359545c72f2bef2d807b89042c546be24f1541e1bba9`  
		Last Modified: Sat, 19 Oct 2024 08:19:57 GMT  
		Size: 5.1 MB (5077373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:039fdeaea77eab0be7598620955214b21e6704ed6c85a04fccaef2b3adf1dbc8`  
		Last Modified: Sat, 19 Oct 2024 08:19:57 GMT  
		Size: 7.4 KB (7364 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:99381b633665998b79690396699aeecda8a6021ba7f48ef5dc0b11d61d8f0977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87636078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de004308e59e863c2497e47864e8d59c4739b921649cdbf16ebb5dcc4d490bb4`
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
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4950c6def722ac96f41618bdff1f82e38c2b3d5849ce2c07b4049db764444b`  
		Last Modified: Sat, 19 Oct 2024 05:23:22 GMT  
		Size: 13.5 MB (13452782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a3b9ee069311be4d8fca64a1f65e93cf73601746ef5283dfcbda615585143a`  
		Last Modified: Sat, 19 Oct 2024 06:27:05 GMT  
		Size: 45.3 MB (45297451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c537019769318d6441a1a0ccde858638029672a31a138cdea08c817a02d85a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5090662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0417cb63caa30943de8542749d15b831605f70f171fb340489aa486804153b0d`

```dockerfile
```

-	Layers:
	-	`sha256:6564a5d55c888b25e3b018c49e151e8df03e9f22c64b33c89509fc90c86a0d6f`  
		Last Modified: Sat, 19 Oct 2024 06:27:04 GMT  
		Size: 5.1 MB (5083278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c74f6858d965dcd2c8366c220ab6a8e4c2213babf582ac0bdc402982d06317bc`  
		Last Modified: Sat, 19 Oct 2024 06:27:03 GMT  
		Size: 7.4 KB (7384 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5fa4b463c6bad8c325cf2a680beae1b5bdedf56de3341022116b1cacbe932088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100881127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de165e6533312f2db04bbb6972e5c0c6e9bf6b9572b6e1356fe2934adc94bcb`
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
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5bb7422168207a94659a7d755a71642577184a266af0a8a3afb47316450f6c`  
		Last Modified: Sat, 19 Oct 2024 04:14:07 GMT  
		Size: 16.0 MB (15990504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48479dfc2b7d427cb9b67d6c2ae25148b5cdad254e89920f302994550cebd409`  
		Last Modified: Sat, 19 Oct 2024 05:30:15 GMT  
		Size: 50.5 MB (50501654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:489d19de386867de888327079b1653eb5c2145f06deb5463336a053265851639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5091106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ec07f3c69822c7b50ff6231d02fa11ef9873228a0ee554cda3b170d2c5f41a`

```dockerfile
```

-	Layers:
	-	`sha256:a42262aa516f6d496beeb73cfcd4241bca3fdef81c466f632fab58c0d5a6784e`  
		Last Modified: Sat, 19 Oct 2024 05:30:13 GMT  
		Size: 5.1 MB (5083769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c7e14fa4672f84ec2b48325ebcbe2b010f0936ce050f44bc4ba250e171457eb`  
		Last Modified: Sat, 19 Oct 2024 05:30:13 GMT  
		Size: 7.3 KB (7337 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:cfe4a44771a4894331c387dfbfd41699d4082635a6d03edf2941e0a316b4d4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99073365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2edee905bdc81d5092eafd62cb7be9c063fa42d60d447d2cc14041cbdf81c0e6`
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
ADD file:008d2e9e73153005eafa485b2ecca3ca9fd6996da5b5c99a52a7376427350f8d in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:53300d777b1a34c849b57f3a3ccdc52f3ad795ea045079e7bcca5f63efab0327`  
		Last Modified: Fri, 11 Oct 2024 05:07:42 GMT  
		Size: 31.0 MB (30951587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a51cb0bf7686a8c2782160996192e9d89c09949101fc6d8c09083eb1013e91`  
		Last Modified: Sat, 19 Oct 2024 04:08:40 GMT  
		Size: 14.3 MB (14320414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0a2eaf274204c5bf93c79db9bc33e24b045b07aacb49995d18798544f6f56f`  
		Last Modified: Sat, 19 Oct 2024 05:41:12 GMT  
		Size: 53.8 MB (53801364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c1c88e5543520ba78e7e211adf00aab3892c369fcf8456da61a453ed97ba8b17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5073960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dba033ffdf0708f27422d708abdda6f4c7605566d9f1d37e2125e8c12426e23`

```dockerfile
```

-	Layers:
	-	`sha256:5e58895d95772019ad0fdcbe6b4be69f49a47be40659f1043c291ca842db57e0`  
		Last Modified: Sat, 19 Oct 2024 05:41:05 GMT  
		Size: 5.1 MB (5066623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f7fac63c0870d1c2791b08f5b05f46d2480ad4a0bc9c88d45b5d99d94de2d5f`  
		Last Modified: Sat, 19 Oct 2024 05:41:04 GMT  
		Size: 7.3 KB (7337 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1ed21863e54c46bb6a3e2a234ea3fa2be1aefa81129997fb2ce3ddf556d4b2eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91917558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845a06f98ce3734e6f2f38f914787f29ed85439d1730e933b3a44bdb334c6638`
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
ADD file:77ba16e2cf3c210906ec7587ab14314afc15cb73af4337fde69ac35187fdb263 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3d2abe11fb3bab133e95a31c3eeb04ba27eaed096cd5d4d3baeb8f12c3473633`  
		Last Modified: Fri, 11 Oct 2024 05:07:47 GMT  
		Size: 30.0 MB (30019614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1e22806c936cf352e8613a36cc00e41a5fc02ec3a1756fa36d836ba0f8dd58`  
		Last Modified: Sat, 19 Oct 2024 03:51:58 GMT  
		Size: 15.0 MB (14974773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3949ce1635c27257c28d76c25291d89d75979fb73e8177e9220f5e051d01fddf`  
		Last Modified: Sat, 19 Oct 2024 05:13:20 GMT  
		Size: 46.9 MB (46923171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:64971ad19818eaa5aec413e6610f11a061fbca500b06d502ed9ae51be25b0b69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5085721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bcadac4f51c1e199a96b69a99209a7b38d7d773d63d289914616fda48513d23`

```dockerfile
```

-	Layers:
	-	`sha256:618826a9976b9b06ed1c6f291f504f0edb80abfff6d55911eb84ed2e273db8d6`  
		Last Modified: Sat, 19 Oct 2024 05:13:19 GMT  
		Size: 5.1 MB (5078416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b08e90487ee45bafeb6e1dce6760b32074eb2786e00670505a3efa62c24f56e3`  
		Last Modified: Sat, 19 Oct 2024 05:13:19 GMT  
		Size: 7.3 KB (7305 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:oldstable`

```console
$ docker pull buildpack-deps@sha256:4d15729c8eeb65bb265a30fe8a40747be2108ddc0afc976073bbf3061aa7fb01
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
$ docker pull buildpack-deps@sha256:53dfb2729c2ea5c681e9cc5b42af756ee2c8454c5a17c50c941e6ebddfb77e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.5 MB (322476759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a13bb52d64137bbfef4f596c20eb11be62bc22b837c7a8e686bf135c43ac16`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f895247ac53f8ccaff2388685ac5288e243187f243654f4af6205a31f8b693`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 15.6 MB (15557923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d199724b11b5ccb55a34503a046bfe20064837b3f7beb547b9a3eab1cb57e0`  
		Last Modified: Tue, 12 Nov 2024 03:14:06 GMT  
		Size: 54.7 MB (54735758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293ef60bdfab8ecc34823af26b3df1d9742e9cb94c1103aa66259e0d57784e72`  
		Last Modified: Tue, 12 Nov 2024 03:59:17 GMT  
		Size: 197.1 MB (197074298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6a30dd51335eb7fa371f0c5c3578e31ea1e657405af15cdbe610a70b0f860481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15107915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7616d68f81bc999bf5452b8b43940cd3b46d540ea4f71115ce69871554a2588`

```dockerfile
```

-	Layers:
	-	`sha256:5be5f4ee1b44d0e9aa1dba97561bc4d202ac1188a34c0a7994c931dec99f8303`  
		Last Modified: Tue, 12 Nov 2024 03:59:15 GMT  
		Size: 15.1 MB (15097684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5f4c658a590f8d5785004ec575558228d9e61e0d82304feeb72e9e60105c912`  
		Last Modified: Tue, 12 Nov 2024 03:59:14 GMT  
		Size: 10.2 KB (10231 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7b8ca851482f3ac5dd83f7f776c70287f0e396c927ced8b45b5ea35dc87974e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.2 MB (283245288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69abe948f0dfc547c7a71483c492df89477394a305ebdb17f6869f98afa00207`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:d2ab4547fbd8c2ffd1467397e3bf7357c565dd0ddab7b1fe46a7af555c5a2d58 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a95f74ee8cb74ceb08cfe11180d99d077de86d07cce20c373d10c20ce9885b49`  
		Last Modified: Thu, 17 Oct 2024 03:07:14 GMT  
		Size: 50.2 MB (50241596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f418fba84fbaf7bab67bcb059341b214f170e38610e4b70f45295fd8324614f`  
		Last Modified: Sat, 19 Oct 2024 00:56:46 GMT  
		Size: 14.9 MB (14877684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27a9032c7c4d1cfb31e96212773919f51ec2f6be760fc0f5c35bafbcdb50249`  
		Last Modified: Sat, 19 Oct 2024 06:37:59 GMT  
		Size: 50.6 MB (50613654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0525b656ff73752501ad6cdcf4137840983e49d8b07af0619e3185c5e925fb`  
		Last Modified: Sat, 19 Oct 2024 08:10:07 GMT  
		Size: 167.5 MB (167512354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:99b4df02852c5c9ef436da722253c6fd613682c2b9bce412b4b84eccb3100d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14908379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfbdcebad2cc9a5cf666dadee37e579872b3e9128215ef08cb6e2ff416e2cb19`

```dockerfile
```

-	Layers:
	-	`sha256:265b31aeaa92380f8c3f6425c52713027f95784e4b52573f632e8e7d38cebf55`  
		Last Modified: Sat, 19 Oct 2024 08:10:03 GMT  
		Size: 14.9 MB (14898075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b941b2a22320cb6c9bf38cc58a5be6077fbb15967c5c3ad3119f189d6344a351`  
		Last Modified: Sat, 19 Oct 2024 08:10:02 GMT  
		Size: 10.3 KB (10304 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6fcca6c2686873d338b72e222bcb158f9b6f212d9496aa46386d1570f3ccd69d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314286584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9960592e533e108fb3fcc1d20fc49c509fe953e1b3a136de1b615a35aea5ff42`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1deb2c2ef23607994f7238c8d97d113f5ebd868b8eb64a0c10d2e0983f036a39`  
		Last Modified: Sat, 19 Oct 2024 01:11:09 GMT  
		Size: 15.7 MB (15747789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbc6072bf5318ca0f9f250b4fcc6254d92483650689f0b0d77274be187abd96`  
		Last Modified: Sat, 19 Oct 2024 05:18:19 GMT  
		Size: 54.8 MB (54832658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13f3e7a61817231ad609702b6918e16648b3eec453567dbedd80952df7e3957`  
		Last Modified: Sat, 19 Oct 2024 06:17:47 GMT  
		Size: 190.0 MB (189971242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:820241d97196cee59900426af9c3bb7e6490fc2906443c04683fa92e277a2b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e441d6a78110371211f6fa8bd15f27a2b2446e97f40e2cefa3b4aaee7748bd`

```dockerfile
```

-	Layers:
	-	`sha256:3f974dae5571e312b034e2e30b7c42b00e5cd62d80d5aa904fc79d3c8f7ee648`  
		Last Modified: Sat, 19 Oct 2024 06:17:43 GMT  
		Size: 15.1 MB (15099830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:268bfc28ef38d7046c158f0988d2a132ffa8e524a824f7c055f6abd6bf05a9aa`  
		Last Modified: Sat, 19 Oct 2024 06:17:42 GMT  
		Size: 10.3 KB (10324 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:40024780c8ab41709798e05afd646c7d83816bbb7bb97d6886d978aaf4b5f314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.2 MB (328166848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfaf42b79695cbbb92c8d381a03a9d409a6148104819b2da33347b8905185497`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:401daab178046178ea38abc84ce80fe4a7e7530a75e6b198a161344b358750f7`  
		Last Modified: Tue, 12 Nov 2024 00:54:54 GMT  
		Size: 56.1 MB (56093682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7489e598cae5c0812e1ddaf1d0b649b6033369bedffceac2506c8d523d0a1c5d`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 16.1 MB (16061669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d3219f513bfa7d5289477f316932047bf97c5e63cdb25a5f5d84119699c8fa`  
		Last Modified: Tue, 12 Nov 2024 03:14:14 GMT  
		Size: 56.0 MB (56032476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989e2f9c439cb2101c7b9646a5f44226e8fce450b536fbbdf42b489a8b29cfc2`  
		Last Modified: Tue, 12 Nov 2024 03:59:24 GMT  
		Size: 200.0 MB (199979021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:99aa603c582d2d59b66ba6c53f22a13729334619991cd21f2ac319cccfcb9581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15096234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df97f8ff7c85fa15f17cd6dcd3ea675c70d7e49971247d6cba5f01f7f4b6b7e3`

```dockerfile
```

-	Layers:
	-	`sha256:66246ecf14a66fc01ddb14bad096f8a122ae7266dab2f9f517d0c2e78278d6c3`  
		Last Modified: Tue, 12 Nov 2024 03:59:17 GMT  
		Size: 15.1 MB (15086025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:471d13d8c1ae4297812155d8e61a16689ac6eaf1dea869327f30e24d8bcbcef3`  
		Last Modified: Tue, 12 Nov 2024 03:59:16 GMT  
		Size: 10.2 KB (10209 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:ca6c782fe8ec07a7cc6410453df28e7cca0cac02f890c922070d237f73ea0be1
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
$ docker pull buildpack-deps@sha256:2df346f6bf0a09c1b581bfa52800a87da97dc79a4c075abe911cfa512ddaafc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70666703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8aa56ed68dba89d198819c24d6f7406f16d7068d0490cc5648d04cb04f7722`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f895247ac53f8ccaff2388685ac5288e243187f243654f4af6205a31f8b693`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 15.6 MB (15557923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4ea105f4c54a69fdf29a66bcead17f11b33895523ec9eb4786da771c122e0936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4498981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f358d4fcc3f6327c0916ed130bd1c75b5731f999b5556491b61eab4f9885f33c`

```dockerfile
```

-	Layers:
	-	`sha256:41bc55e2a522382fd133dfd3161739a2e1becdf81df08d432ceece6009104b53`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 4.5 MB (4492180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:563ae519ad78eb8647e2644e539048e36d372cf39041bf4f75247792a023461b`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 6.8 KB (6801 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5763e2f5bf1629bec5c9e16d00a72e3dfd8f17b3a5667e72a651d18e71ef39b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64945646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce309396159795b0c45db2909a8559c1303270bf296bbe0f73ab8e2a6054b4c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c18c6ef253e2b87a07739846b10eb333531241b80c23e3aec0643adc1b449e1a`  
		Last Modified: Tue, 12 Nov 2024 00:57:22 GMT  
		Size: 50.3 MB (50272340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907b69db4cf1745187b07df647e4ed72539303d8747c006695c2bc15e5e1e185`  
		Last Modified: Tue, 12 Nov 2024 16:00:17 GMT  
		Size: 14.7 MB (14673306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d1fb45a0a4b3ee70c293b961eb04d26ff1a65af954b91132ee444cb2d991f128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4500675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33537d7ac7b5ad3b240e3e4da843d63123e8c262462e97cfeca2cb40e962ad7d`

```dockerfile
```

-	Layers:
	-	`sha256:87ec50285f2a8b3ca66ab532e7620f2de6bd499824493288de9a55c1fd4f6151`  
		Last Modified: Tue, 12 Nov 2024 16:00:16 GMT  
		Size: 4.5 MB (4493814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9433113985ed5cf511a7ff1fedca93ced3a78d7b8b35ab174e59d410af70d257`  
		Last Modified: Tue, 12 Nov 2024 16:00:16 GMT  
		Size: 6.9 KB (6861 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b3ca5e481e6e265be7ff4f1f665bc4702a4e7fd5c3592baa01884a67936d99b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69300660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e48eea012caf1b9fdcee3a320590d0f965b183ccbd3e2ac9027d6a49ab8425e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9e545ff305fe56558a94b064a901c16b373a3501daf5519f82ec19db6a3655`  
		Last Modified: Tue, 12 Nov 2024 11:16:34 GMT  
		Size: 15.5 MB (15543588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e95d2cbb57128b37e3aeb93434885a8fd4f24488e58be893a7fc19edced4c584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4498673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5dd407061bac2bbf6554ae718d25b67268b9b4f1229edd0431ca2b3e092472`

```dockerfile
```

-	Layers:
	-	`sha256:3d5cdaf50f3868d2492b29e300367b85b38f1460b7b8f6e9c9a20540301e0778`  
		Last Modified: Tue, 12 Nov 2024 11:16:33 GMT  
		Size: 4.5 MB (4491792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:914df286e10eadb4badd71b8c9c813a4d97e87d5866664eec95ab4e0f7030517`  
		Last Modified: Tue, 12 Nov 2024 11:16:33 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:28db40634d8196c741694964927ffbcce7a32e46ce629d076ac4180059acc1f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72155351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4af437b3c1ada7e3c006fa019ec1cb83212d5e1723583a7a203963cd7812b6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:401daab178046178ea38abc84ce80fe4a7e7530a75e6b198a161344b358750f7`  
		Last Modified: Tue, 12 Nov 2024 00:54:54 GMT  
		Size: 56.1 MB (56093682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7489e598cae5c0812e1ddaf1d0b649b6033369bedffceac2506c8d523d0a1c5d`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 16.1 MB (16061669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:adaffba9878783500c58c160462f440fa73a4d51cc25f766be5463aa7ac39bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4495398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:779e7f15590d0bf3c8710f0aac9cc10c85719c2601c08b05b9695f106959c996`

```dockerfile
```

-	Layers:
	-	`sha256:0654c325eacf20f2fa53094181831e09fd652d1356c43ddcab4d5bd8bcd3fefa`  
		Last Modified: Tue, 12 Nov 2024 02:37:52 GMT  
		Size: 4.5 MB (4488619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4019c97fc7b3b49f34fc5ee695b048f164cef6227b6864fdb3a3d5d99adaf8c`  
		Last Modified: Tue, 12 Nov 2024 02:37:52 GMT  
		Size: 6.8 KB (6779 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:dece6b2b6cff356b300bab333df2eebe764526754b4cdb38b1fb8f98998eee06
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
$ docker pull buildpack-deps@sha256:540e7a62b63872321d2c383afd57c95a18ae18b2f5ceb5bcc0cdd6df05db8576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125402461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd55a9e99939cf7c5acf4c269136ff35f63aaa9a844090e0b1371e26552ae01c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f895247ac53f8ccaff2388685ac5288e243187f243654f4af6205a31f8b693`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 15.6 MB (15557923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d199724b11b5ccb55a34503a046bfe20064837b3f7beb547b9a3eab1cb57e0`  
		Last Modified: Tue, 12 Nov 2024 03:14:06 GMT  
		Size: 54.7 MB (54735758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b7aa7ab778ad756a4f5b94a9de226627f55235ccdf11496a0d182f3bc0ee3f6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7727489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bcf6ce98fa3bc15782ab2f19e9d7e2b0086c50da9d6bb74813f7de64b3a923f`

```dockerfile
```

-	Layers:
	-	`sha256:a1e5ea0b3a869821c16ffa4ba2bf5f7cac5d4d91a864463741aed3d1441e916e`  
		Last Modified: Tue, 12 Nov 2024 03:14:06 GMT  
		Size: 7.7 MB (7720136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3f7d1a03ede92d8e8005d05cde3f0bc5596c387c4c736f94ba3a94d1aa52014`  
		Last Modified: Tue, 12 Nov 2024 03:14:05 GMT  
		Size: 7.4 KB (7353 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0b27afdfd77d75f7daa15242cc63d12c81c15bef9bfdf3389220b78e4b71c5d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115732934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fea1c1109f52736fe3129fe2d91df3883572414c5c1c122f693e794c1cca2a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:d2ab4547fbd8c2ffd1467397e3bf7357c565dd0ddab7b1fe46a7af555c5a2d58 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a95f74ee8cb74ceb08cfe11180d99d077de86d07cce20c373d10c20ce9885b49`  
		Last Modified: Thu, 17 Oct 2024 03:07:14 GMT  
		Size: 50.2 MB (50241596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f418fba84fbaf7bab67bcb059341b214f170e38610e4b70f45295fd8324614f`  
		Last Modified: Sat, 19 Oct 2024 00:56:46 GMT  
		Size: 14.9 MB (14877684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27a9032c7c4d1cfb31e96212773919f51ec2f6be760fc0f5c35bafbcdb50249`  
		Last Modified: Sat, 19 Oct 2024 06:37:59 GMT  
		Size: 50.6 MB (50613654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d17122d5550612fcfb8bdb86e3884095b4bb789a98d27dec66b7b6363b515ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7728923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a8a3069eb6e9c82d3c4c18ddb245fd1e026f21f27ffd7382878abd6e0251e7`

```dockerfile
```

-	Layers:
	-	`sha256:6875125c6a3662c299a57970ecff8767213464540a3f4b2443f46582d4b59612`  
		Last Modified: Sat, 19 Oct 2024 06:37:58 GMT  
		Size: 7.7 MB (7721498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c133ef3869a8610514a32152844f53057e7d5043e5788c21cc57d2487ebb1a5`  
		Last Modified: Sat, 19 Oct 2024 06:37:57 GMT  
		Size: 7.4 KB (7425 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:663f17b029a1bf24ca58f209ff1577c2d1b9a7aed2ecadbfc6ba889c327a0382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124315342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2754992e17ca3179605d3f122e480a5b71db85b29892344fbaadb8f3fd43c5e2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1deb2c2ef23607994f7238c8d97d113f5ebd868b8eb64a0c10d2e0983f036a39`  
		Last Modified: Sat, 19 Oct 2024 01:11:09 GMT  
		Size: 15.7 MB (15747789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbc6072bf5318ca0f9f250b4fcc6254d92483650689f0b0d77274be187abd96`  
		Last Modified: Sat, 19 Oct 2024 05:18:19 GMT  
		Size: 54.8 MB (54832658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1965623055033a3db2cd3d6d55f03b896eeeca6c187d658624bfdb8ad6528736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7733284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6670f84a12848f56394136665a519aceecb0d2286466693304dc42e0605ca50a`

```dockerfile
```

-	Layers:
	-	`sha256:e2d1f70c81ca0b6cd23296d317fd5165b255a7e0a1572a49f179932ebb08e535`  
		Last Modified: Sat, 19 Oct 2024 05:18:17 GMT  
		Size: 7.7 MB (7725839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b826fcef0fc38aaa49e948810018ef936f777127503a8a92bbbab59aabd9f1c5`  
		Last Modified: Sat, 19 Oct 2024 05:18:17 GMT  
		Size: 7.4 KB (7445 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:abdacb8dd3629c36873bb6565bb5355bb43e35599717521edddba9275708ca78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128187827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3519d81e879877e50e48707a4c989ea967331bf5b66e4edbd4517f2f68c0c5e2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:401daab178046178ea38abc84ce80fe4a7e7530a75e6b198a161344b358750f7`  
		Last Modified: Tue, 12 Nov 2024 00:54:54 GMT  
		Size: 56.1 MB (56093682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7489e598cae5c0812e1ddaf1d0b649b6033369bedffceac2506c8d523d0a1c5d`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 16.1 MB (16061669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d3219f513bfa7d5289477f316932047bf97c5e63cdb25a5f5d84119699c8fa`  
		Last Modified: Tue, 12 Nov 2024 03:14:14 GMT  
		Size: 56.0 MB (56032476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f57fdf5c9316bd657fa92242f94a7a45fc7b72ff77e45c1afb81c50264750afb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7722954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da7c49e19c31ee997e83662326c7457752c1ae0084f5cf1d96e437c0a414b61a`

```dockerfile
```

-	Layers:
	-	`sha256:cac73e9dd9c0a64923bfc98da0ae2d1e496fc28c574c818636b78b29f41a46f8`  
		Last Modified: Tue, 12 Nov 2024 03:14:13 GMT  
		Size: 7.7 MB (7715624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea5177cad227d9b19951172f747480276aa38502fbfbca8407d68577dff7fc57`  
		Last Modified: Tue, 12 Nov 2024 03:14:13 GMT  
		Size: 7.3 KB (7330 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:oracular`

```console
$ docker pull buildpack-deps@sha256:e49c7154627792ef43468deb6b21949caed97e986e790accff535d2fd2d03b52
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
$ docker pull buildpack-deps@sha256:03d93a4dc70e0132312bea3f1d241698a735458531e6df70f8de510a99be38ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 MB (286146913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d3c744fb1b4abd4294a55843131e06d21bd63a052da9f1f5d0a5407fbbc7aaa`
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
ADD file:c6c1fcc53cf2d3beb705eee292dd1e6ef2980e7f6221cba9d5c4081038760fc1 in / 
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
	-	`sha256:372111cb3b6e75bbceae9a3a6c2d060e2fb7b2573e9ff6e1931f6de2798246c4`  
		Last Modified: Wed, 09 Oct 2024 16:53:13 GMT  
		Size: 30.6 MB (30600773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a944d883315edf8742919f6ef5b3c26a8ad272f5008425c60a2142fb1f5df853`  
		Last Modified: Sat, 19 Oct 2024 02:06:13 GMT  
		Size: 15.4 MB (15357098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d878515a2f78c562568bfe3981dd590eda252ccb805e73b9e3bb9f4485eee6`  
		Last Modified: Sat, 19 Oct 2024 02:52:39 GMT  
		Size: 46.4 MB (46428074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dfce72fe356e6ebf544894d58f638ff9283ef9eed257a7a26f09653c15fc48`  
		Last Modified: Sat, 19 Oct 2024 03:53:52 GMT  
		Size: 193.8 MB (193760968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dfd11ecc3b5e6efe6a85840a418c50473d20695918a939e92395a6673b25afc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11369292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01547e315200ee1c635fc2b988ed54edf58553cc8109fd67f8b267bb649967f9`

```dockerfile
```

-	Layers:
	-	`sha256:3a816cfdfd4c5b798f42ea76c86af988d85dbab1ad7e6d7f12ce754eb5a04550`  
		Last Modified: Sat, 19 Oct 2024 03:53:49 GMT  
		Size: 11.4 MB (11359090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24bcad713b0485bae1e33d23f06741842a9e36907a3b77602c55b9240a031125`  
		Last Modified: Sat, 19 Oct 2024 03:53:48 GMT  
		Size: 10.2 KB (10202 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:630f53d8b5cbe6bbc84776f9ce87fadcd5a4446d919c7cb3131d545498342f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.3 MB (248330372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51dea34a0a62782a1c0751d9eb5db63fc8e83b044206c17a17c064d29726c99`
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
ADD file:8e23d3c59f96fb90ac280b31339b3cdff6ade1865ca64b22d81f85a66b3808c2 in / 
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
	-	`sha256:c481ad0a3e91be308525ddb3271f2aa7bc25d4f2a1241c1e05f6552ebecd91b1`  
		Last Modified: Wed, 09 Oct 2024 16:53:25 GMT  
		Size: 27.5 MB (27546645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a20a0e501d15d9e4692975ca8c07ba367bbaed9ea09bf0a9d8382aca8abe0a4`  
		Last Modified: Sat, 19 Oct 2024 06:47:28 GMT  
		Size: 14.0 MB (14044586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804a8684eb96a4656dd0e6aee99ef9f42b140a0e1e97b15155ef8a8e3d346151`  
		Last Modified: Sat, 19 Oct 2024 08:21:23 GMT  
		Size: 49.4 MB (49402478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7af6233872298dc63a4b96ca3d1ad4917e7c750d92c59ae6a8eeab5a64c5ea`  
		Last Modified: Sat, 19 Oct 2024 10:44:09 GMT  
		Size: 157.3 MB (157336663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f9462d6a45142c84bbcfd22fe47b0ac534c01162292591fca5ea528d0deafcaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11148888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f39e15ad55084b6335173c3de143c8a0e38e4cde3d42d8c4a3ecbd516137e07e`

```dockerfile
```

-	Layers:
	-	`sha256:1a989d7ca518404b833d33a8cf7f72f10a5f7104fd5e03ad99094e564367fa2b`  
		Last Modified: Sat, 19 Oct 2024 10:44:05 GMT  
		Size: 11.1 MB (11138625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89b99890690fe15f551a601dfe804c776d6d483a7877e307f5353690c357d17b`  
		Last Modified: Sat, 19 Oct 2024 10:44:04 GMT  
		Size: 10.3 KB (10263 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:84d0664dfd2b7f563861dfa74c8a174ecdb0091aea34bb02a7b943c686275e1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279807550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d71d1ce194c71f9b9af6c05f830867b1ddf5d44645ad0cd92d12d98e5feb0d`
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
ADD file:897556c1de01d47a95fb4d7011c66a17502f56fb3838b2231407a26c3ec19779 in / 
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
	-	`sha256:e311dff5272f98c3a90f3b733cf3131b33de66a713a49c4dc345811451dabaf7`  
		Last Modified: Wed, 09 Oct 2024 16:53:19 GMT  
		Size: 30.3 MB (30284490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d09b70567f67458b69e57931b7ba0045a67a5ea93d03cd34ced355035e4ddb4`  
		Last Modified: Sat, 19 Oct 2024 05:24:26 GMT  
		Size: 15.1 MB (15130151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69ca0bd1e67582a527f0561d210442a28387165346cd80417b469dfff4c9547`  
		Last Modified: Sat, 19 Oct 2024 06:28:24 GMT  
		Size: 46.3 MB (46331301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030000a4c1910257f23efc5cdfddbdb4aba77b7d1fdce703b768b07b6f492d5d`  
		Last Modified: Sat, 19 Oct 2024 12:53:55 GMT  
		Size: 188.1 MB (188061608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:96d2130893caf1ac77491d2e7d95742afdca190fe40edf5ce971375631ed3193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11445721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8949f2aa5abfbcb022ba552ac0126c9345dc69676addf82d952a3019c2b72c`

```dockerfile
```

-	Layers:
	-	`sha256:58f90ead50d1b376ba369a2a113b94350268f9704ebcea6e3d84d48d9dda0172`  
		Last Modified: Sat, 19 Oct 2024 12:53:52 GMT  
		Size: 11.4 MB (11435438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0ff5188d23de71d755b5930ba82cc0aee31ad6837df0aea820a0d04d4adb5a0`  
		Last Modified: Sat, 19 Oct 2024 12:53:51 GMT  
		Size: 10.3 KB (10283 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f018a86da66f653058daa2ada02f288bbbcf6f749fda70307b1af30d1515415f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301463127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1af8ec41b66d08cb5ad10a41c28449d022deb952bfa8309eb6753b4062aa3ec`
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
ADD file:1f33027337aeb38d1fecb5ee33f2c55c6bd442e269ee902f5364ec863e957998 in / 
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
	-	`sha256:fc0886b1c0801753f6a7a5ef62947406857faa2987b1df5781427e2c559ea218`  
		Last Modified: Wed, 09 Oct 2024 16:53:31 GMT  
		Size: 35.1 MB (35062896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c073ca505f4363ebfcb898f4d2a8b23427ba6069a5fb5b06cc80cb0df05291`  
		Last Modified: Sat, 19 Oct 2024 04:15:45 GMT  
		Size: 17.2 MB (17233776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce660df8e8e7bcaf60343fbb14080cb0995f3ab4cdfa5765f101525c99d3070`  
		Last Modified: Sat, 19 Oct 2024 05:32:02 GMT  
		Size: 51.7 MB (51671410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596c50e5bb435c1b4a27ed920914c64a0ad7d69705ed612654dd283d064e22e6`  
		Last Modified: Sat, 19 Oct 2024 14:12:58 GMT  
		Size: 197.5 MB (197495045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:715439154d0004d30ceb5772a168331d85a8a651b5c0c0fcd3b16693663b5839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11361607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4855e8320c89ed136787ffb877830cf3eb8a3683cb45f5233407f1aea366b5`

```dockerfile
```

-	Layers:
	-	`sha256:356ba3c7ba5f2df4bc4020620c2c965b2dc3473074d8d6721d261dd8f9b36e1d`  
		Last Modified: Sat, 19 Oct 2024 14:12:51 GMT  
		Size: 11.4 MB (11351372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd06c235c1e7ea4f700bab41332ebcb85d7db422c3138e05256ac60bda4d75ab`  
		Last Modified: Sat, 19 Oct 2024 14:12:51 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:48afd56882a4b2e3cd2396ebcfa6e4a835b44e2ac04a5f3ab9f4ba6d8eb0a1f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.1 MB (378116068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed04263e45289e5f145f6fa1279c85e0232fdede3ddeef5cf9a6af3211db885b`
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
ADD file:9744fb771a3525b1ecc8bb8c4ca623db4381f3fa78cd865afd2dc853a7ec0106 in / 
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
	-	`sha256:c4c3b7ce35ec01feb67389e9cc9ac164fd53001e09b63553078d8d1e6ad0c713`  
		Last Modified: Wed, 09 Oct 2024 16:53:37 GMT  
		Size: 31.8 MB (31787862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe51613addcb9aebac5d02d07ded0ea6c171908f331d835d7c75b1cebb4be19`  
		Last Modified: Sat, 19 Oct 2024 04:11:36 GMT  
		Size: 15.9 MB (15873939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7fb3831c114a36b0b2c3c75c497b9581ec083768d0aa69432339a049abe6101`  
		Last Modified: Sat, 19 Oct 2024 05:47:19 GMT  
		Size: 54.5 MB (54527660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426ce57cb131e2d638c81a485aed90f4cc1f8072f4a53013aa398fc96a3519f7`  
		Last Modified: Sat, 19 Oct 2024 08:11:05 GMT  
		Size: 275.9 MB (275926607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:650c38330916f8997d1d90788e774e46303f5d7b2c5147840f279d3e1f98a264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11417620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00179a05622dfbd93368ab3c0a9428ccf2a6bdc0286a2cbc2218e30e0affd999`

```dockerfile
```

-	Layers:
	-	`sha256:39cf10949df20e5ba0d106882dbfb72fc8685318991973dfa3a3b5c842cd96db`  
		Last Modified: Sat, 19 Oct 2024 08:10:29 GMT  
		Size: 11.4 MB (11407385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87c7dc51389f4537c713630a36116841bf82cbad0e379c3bfc42e5dd40a3f7e9`  
		Last Modified: Sat, 19 Oct 2024 08:10:26 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8d59ef204da03954a30f9b0437508e53dec88b738a35578ce5f60417f353c7d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.4 MB (265362951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36345074e94238af3d93afa020f1524b28079f416dc16d8b6f309ade31492f64`
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
ADD file:e8f85fdb92ac3e5e436757449ac2447ad1520aad2682c8e0077efcce841566a1 in / 
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
	-	`sha256:303831814b37c8b218003169a08ba9ba85ed2a888e73d505841b5db92ec79efa`  
		Last Modified: Wed, 09 Oct 2024 16:53:43 GMT  
		Size: 30.8 MB (30774664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e574d553080236f570c1f83ee295b636102f93cefde1b709e84380c22d451f3f`  
		Last Modified: Sat, 19 Oct 2024 03:53:04 GMT  
		Size: 16.9 MB (16920088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e923714151c14f08933fe23d1283ee8fe44eabf4047feae2eb487e323f6a4b75`  
		Last Modified: Sat, 19 Oct 2024 05:14:35 GMT  
		Size: 47.7 MB (47742541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5d42432f385ba186920d2e84eaf784a7d78569b2bc0837372053989e4fa52a`  
		Last Modified: Sat, 19 Oct 2024 07:05:12 GMT  
		Size: 169.9 MB (169925658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:38efad609d88402a46e87ef6252a59b8be391b8d1f1f0d3eb729b63a1dfe6fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11168608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a0e82c9491dc1299b1420daf98d289e7033fdf06052c84abb656751893b8af`

```dockerfile
```

-	Layers:
	-	`sha256:13ec0e282ca8256dce1466b4d42ff3bf10a41da8a9fb66930ac757847bc48c2e`  
		Last Modified: Sat, 19 Oct 2024 07:05:10 GMT  
		Size: 11.2 MB (11158405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8e5600e4c78301d5bcd6fda1b318ba76b5210f34227b50361695f7309bf8152`  
		Last Modified: Sat, 19 Oct 2024 07:05:09 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:oracular-curl`

```console
$ docker pull buildpack-deps@sha256:1652e3648a28be38b38e993b799eabaf859dc696e231df39219d5f8d0602e6a4
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
$ docker pull buildpack-deps@sha256:c8064ce954a2d9c90bd2e16fdd31c7c0b20e66720232e562b71c781f6c00bf56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45957871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7b838a1e6a2498c0f2b75d67c8db81136efdc82a162f30a7585633d1d465a7`
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
ADD file:c6c1fcc53cf2d3beb705eee292dd1e6ef2980e7f6221cba9d5c4081038760fc1 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:372111cb3b6e75bbceae9a3a6c2d060e2fb7b2573e9ff6e1931f6de2798246c4`  
		Last Modified: Wed, 09 Oct 2024 16:53:13 GMT  
		Size: 30.6 MB (30600773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a944d883315edf8742919f6ef5b3c26a8ad272f5008425c60a2142fb1f5df853`  
		Last Modified: Sat, 19 Oct 2024 02:06:13 GMT  
		Size: 15.4 MB (15357098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:734f143b619a054aeaf675404b5a8b6bf169fef11b9e111e8a691436743a0b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d2b611b8af5dbe471921a51a30ed516be558eeaf85c1466481a13d6640a4ae`

```dockerfile
```

-	Layers:
	-	`sha256:04d1691c1daa2c8f7f4ed5fbb5bcfaa1d228a7b3502a02d4d0c606c8e2a69420`  
		Last Modified: Sat, 19 Oct 2024 02:06:13 GMT  
		Size: 2.5 MB (2458653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:470d7dbf100349d28fe574b0fc0e6eb056c846f0a7430a28ea4919e451ed1b6b`  
		Last Modified: Sat, 19 Oct 2024 02:06:13 GMT  
		Size: 7.0 KB (6978 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1e977fad87b7530f371b33c739f5b93816160035131817f7a37a12d811020346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41591231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e40ada5b94a3ac9d258dd7bc19b46d3216e7a081fc464acbf184e0c7af2ea3`
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
ADD file:8e23d3c59f96fb90ac280b31339b3cdff6ade1865ca64b22d81f85a66b3808c2 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c481ad0a3e91be308525ddb3271f2aa7bc25d4f2a1241c1e05f6552ebecd91b1`  
		Last Modified: Wed, 09 Oct 2024 16:53:25 GMT  
		Size: 27.5 MB (27546645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a20a0e501d15d9e4692975ca8c07ba367bbaed9ea09bf0a9d8382aca8abe0a4`  
		Last Modified: Sat, 19 Oct 2024 06:47:28 GMT  
		Size: 14.0 MB (14044586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7a3c3fae690959857baae5e83af87100f40797adf2708e30a85ee740cee3c37b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45cc8c06dadd6e69d7d01110cc90a328f09396e9cf95b2c8b380ba67473c314`

```dockerfile
```

-	Layers:
	-	`sha256:45bfb28afe372c81ef53acef056634d56ef2a00ac96381bd9866544d98c9d564`  
		Last Modified: Sat, 19 Oct 2024 06:47:28 GMT  
		Size: 2.5 MB (2460953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24c7480d5a4f13eca905b975d689fa52da17373cfa8107861a5c3954f890547d`  
		Last Modified: Sat, 19 Oct 2024 06:47:28 GMT  
		Size: 7.0 KB (7038 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e1dbce1c5f56458cb1879d905878b21a3aee8ad27ed8352bddb8e0c0b9bc248d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45414641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91f14a1161bb53b5d7cfb783d6af7a25904c299ac877d6bdcd8241f35b372ab`
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
ADD file:897556c1de01d47a95fb4d7011c66a17502f56fb3838b2231407a26c3ec19779 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e311dff5272f98c3a90f3b733cf3131b33de66a713a49c4dc345811451dabaf7`  
		Last Modified: Wed, 09 Oct 2024 16:53:19 GMT  
		Size: 30.3 MB (30284490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d09b70567f67458b69e57931b7ba0045a67a5ea93d03cd34ced355035e4ddb4`  
		Last Modified: Sat, 19 Oct 2024 05:24:26 GMT  
		Size: 15.1 MB (15130151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:77f2bd6376f24142b5a91b775d8e4d8cc19c37a9810da513eeffe24dfb904445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6396bf800ad99952b2d919edf4c9fcd01524725ed1328c9f7cbc6534cbe25ed7`

```dockerfile
```

-	Layers:
	-	`sha256:81847d8bf181c9da1a90aa9c5ef4ce09b6d0e5b180e825deba709789dd602d3c`  
		Last Modified: Sat, 19 Oct 2024 05:24:26 GMT  
		Size: 2.5 MB (2459710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d1eea14e97d018bb367fead4ed16ce0ac4bb8416b69ee8061c0934dbd8863b6`  
		Last Modified: Sat, 19 Oct 2024 05:24:26 GMT  
		Size: 7.1 KB (7058 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:eeb6cecc2bb9417e66a3c75ec146ffaeec184ddedd753033d517ab7cb3a59b9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52296672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9376d70f331306fb3aa3ebaef1c250863ae8b80e4b04f920c28edf8914603ba8`
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
ADD file:1f33027337aeb38d1fecb5ee33f2c55c6bd442e269ee902f5364ec863e957998 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fc0886b1c0801753f6a7a5ef62947406857faa2987b1df5781427e2c559ea218`  
		Last Modified: Wed, 09 Oct 2024 16:53:31 GMT  
		Size: 35.1 MB (35062896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c073ca505f4363ebfcb898f4d2a8b23427ba6069a5fb5b06cc80cb0df05291`  
		Last Modified: Sat, 19 Oct 2024 04:15:45 GMT  
		Size: 17.2 MB (17233776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d20c9d8b8a834172fa6ab55ecf8510e1f3288ae1cab193bc3cb3a40dbc6d700a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2470146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e85a5e2147848947205e6b9181c7b04afd71ac6a6c0ec75a150b21113084a031`

```dockerfile
```

-	Layers:
	-	`sha256:e0ca164efe4d449288e97a4a886a9454a1ff230e6a906e603a0cf8db8a519a08`  
		Last Modified: Sat, 19 Oct 2024 04:15:45 GMT  
		Size: 2.5 MB (2463136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da04dcb833f90e27bf5cae38acaa5f667c25b35a1a5c25c0a91a6f3cd82d474`  
		Last Modified: Sat, 19 Oct 2024 04:15:44 GMT  
		Size: 7.0 KB (7010 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:ba3f481bcb07a41a539397bc1c6c9e459810a28f0f1506f37a8a729e996ce91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47661801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85952ebe22570db7d5e17a085e44f5e0433d35d4d31df07edfe08fd4f9d96902`
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
ADD file:9744fb771a3525b1ecc8bb8c4ca623db4381f3fa78cd865afd2dc853a7ec0106 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c4c3b7ce35ec01feb67389e9cc9ac164fd53001e09b63553078d8d1e6ad0c713`  
		Last Modified: Wed, 09 Oct 2024 16:53:37 GMT  
		Size: 31.8 MB (31787862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe51613addcb9aebac5d02d07ded0ea6c171908f331d835d7c75b1cebb4be19`  
		Last Modified: Sat, 19 Oct 2024 04:11:36 GMT  
		Size: 15.9 MB (15873939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:634fb24146ea687622924739ef9b584455f9a8b0f46d250895d61afd83fd9b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff4081f19bf3b625147bc02f0fabbcdaed17eb0cbc383068ccce8a22992cc97`

```dockerfile
```

-	Layers:
	-	`sha256:a1bf1f852c1c38b69e6d718d23e7c17f4c060958d8bfe172ee8388b792786c33`  
		Last Modified: Sat, 19 Oct 2024 04:11:34 GMT  
		Size: 2.5 MB (2452740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a61d43411874b66aa52b6d698db1bab53c6e12085fc8967ba7377d7b05addb30`  
		Last Modified: Sat, 19 Oct 2024 04:11:34 GMT  
		Size: 7.0 KB (7010 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e2c3db1f649ee912aa1c6427c632b81bb6c446b42548649b72d9a1ea659d711c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47694752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c00d8aa43de987de73c99b16f375fd3a4214ef5b99cb8715edde84e954c74e`
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
ADD file:e8f85fdb92ac3e5e436757449ac2447ad1520aad2682c8e0077efcce841566a1 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:303831814b37c8b218003169a08ba9ba85ed2a888e73d505841b5db92ec79efa`  
		Last Modified: Wed, 09 Oct 2024 16:53:43 GMT  
		Size: 30.8 MB (30774664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e574d553080236f570c1f83ee295b636102f93cefde1b709e84380c22d451f3f`  
		Last Modified: Sat, 19 Oct 2024 03:53:04 GMT  
		Size: 16.9 MB (16920088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7a677b57cccf9a1f90f3301ea0e84d2d171768119ab573b8a9bf7bcbdb0cd06e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c969f11cafa5b99510b90103a69d2a55f244aee6afa3692abf5080f2a2d1d1`

```dockerfile
```

-	Layers:
	-	`sha256:484a058821f5b4ec587da2191d697a8a1ff80c40808532d11f42b48486c07a7b`  
		Last Modified: Sat, 19 Oct 2024 03:53:04 GMT  
		Size: 2.5 MB (2461484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98d0f3ef3b18565614a54559f250dd845d30c8b07e1b179f76446556d63bd434`  
		Last Modified: Sat, 19 Oct 2024 03:53:04 GMT  
		Size: 7.0 KB (6978 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:oracular-scm`

```console
$ docker pull buildpack-deps@sha256:400675c9f31f95df51dc1a53754e64c451d52626a17e58e141e8b47a9587a842
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
$ docker pull buildpack-deps@sha256:2e1a10606d94d1341f4291bfe145a175659c824965e8fd3865cf838d843ce4af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92385945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0113271dcab80bce9700ced13a5585c0c989e1b56647edc2486bdbf7e270ae92`
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
ADD file:c6c1fcc53cf2d3beb705eee292dd1e6ef2980e7f6221cba9d5c4081038760fc1 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:372111cb3b6e75bbceae9a3a6c2d060e2fb7b2573e9ff6e1931f6de2798246c4`  
		Last Modified: Wed, 09 Oct 2024 16:53:13 GMT  
		Size: 30.6 MB (30600773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a944d883315edf8742919f6ef5b3c26a8ad272f5008425c60a2142fb1f5df853`  
		Last Modified: Sat, 19 Oct 2024 02:06:13 GMT  
		Size: 15.4 MB (15357098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d878515a2f78c562568bfe3981dd590eda252ccb805e73b9e3bb9f4485eee6`  
		Last Modified: Sat, 19 Oct 2024 02:52:39 GMT  
		Size: 46.4 MB (46428074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1e3606b1ecf3ff7025ba8e1ea5e42df37408b840635cb63b334f037e41989f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10503c61c856cf28d7a99d4c07c844f5c8055fc334e6a3789c4c5d7d52bcbf1`

```dockerfile
```

-	Layers:
	-	`sha256:78722da52930ac15ebf0a6bcfd0e1fe261a2746c127f81b162b628725a8bdabc`  
		Last Modified: Sat, 19 Oct 2024 02:52:38 GMT  
		Size: 5.1 MB (5090433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ebf53812943cf5a8aa3587eeb1d7aa692dfc6b67872b34031c7959d49e6fbd2`  
		Last Modified: Sat, 19 Oct 2024 02:52:37 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a3b8436385f7e5f61c631de58b96267ca63424b7a1f2edddd2d8ade83de6b753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (90993709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b52a03a0d1525d7c051d4c6bd661df3d4d7fee021c5a779c43e15834a45a7a9`
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
ADD file:8e23d3c59f96fb90ac280b31339b3cdff6ade1865ca64b22d81f85a66b3808c2 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c481ad0a3e91be308525ddb3271f2aa7bc25d4f2a1241c1e05f6552ebecd91b1`  
		Last Modified: Wed, 09 Oct 2024 16:53:25 GMT  
		Size: 27.5 MB (27546645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a20a0e501d15d9e4692975ca8c07ba367bbaed9ea09bf0a9d8382aca8abe0a4`  
		Last Modified: Sat, 19 Oct 2024 06:47:28 GMT  
		Size: 14.0 MB (14044586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804a8684eb96a4656dd0e6aee99ef9f42b140a0e1e97b15155ef8a8e3d346151`  
		Last Modified: Sat, 19 Oct 2024 08:21:23 GMT  
		Size: 49.4 MB (49402478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d103e4ed295a6a17ce4ca2aaf307617dc876868f98530c47d5092cf36e24df7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5099116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f11a591fe13fa3511e7c434069e50379f13bca29a10d3e0fe37f00752ec2444`

```dockerfile
```

-	Layers:
	-	`sha256:41a132977d310714ddf9c74d7d7f6bb0c0fc8fc8d203c5ee774807bde513510e`  
		Last Modified: Sat, 19 Oct 2024 08:21:21 GMT  
		Size: 5.1 MB (5091733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93f60af3718c85df129bbd180f5861a4d382da0308f6619ba9d48d10963992d1`  
		Last Modified: Sat, 19 Oct 2024 08:21:21 GMT  
		Size: 7.4 KB (7383 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bdc102418f7661b306dba7cd1da9a44bf88dace880f30af2f9c99b3a14a70b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91745942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4ce0d24b5556cec948c7c2fef72f177b0aea727b2a74df8bfc0697e3acf7df`
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
ADD file:897556c1de01d47a95fb4d7011c66a17502f56fb3838b2231407a26c3ec19779 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e311dff5272f98c3a90f3b733cf3131b33de66a713a49c4dc345811451dabaf7`  
		Last Modified: Wed, 09 Oct 2024 16:53:19 GMT  
		Size: 30.3 MB (30284490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d09b70567f67458b69e57931b7ba0045a67a5ea93d03cd34ced355035e4ddb4`  
		Last Modified: Sat, 19 Oct 2024 05:24:26 GMT  
		Size: 15.1 MB (15130151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69ca0bd1e67582a527f0561d210442a28387165346cd80417b469dfff4c9547`  
		Last Modified: Sat, 19 Oct 2024 06:28:24 GMT  
		Size: 46.3 MB (46331301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ab39cbabd5fe378c4643b80257a53677158249d426e7dd238dafa3b47e2c23c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5105038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59aa480168513e7b6e1132c5fce9ca710815717ec675bb7f7683906de832e0ad`

```dockerfile
```

-	Layers:
	-	`sha256:3fe20449803338205830ae7041a7b5f211304706c435c32c2b2d96c4343ef0ba`  
		Last Modified: Sat, 19 Oct 2024 06:28:19 GMT  
		Size: 5.1 MB (5097634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:186178c3e379c352c1f9be0efb33fe165a2c5b8523674617e0abe790219eda5a`  
		Last Modified: Sat, 19 Oct 2024 06:28:19 GMT  
		Size: 7.4 KB (7404 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0ac0c11864cbe79f5d7936b1647a570a0f2ba6cd664790f20cfc6f15b37608bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 MB (103968082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6a3610d9b7eaf58f24c59c9906fb1fdcf0a7a86990394f21a175fad79451913`
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
ADD file:1f33027337aeb38d1fecb5ee33f2c55c6bd442e269ee902f5364ec863e957998 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fc0886b1c0801753f6a7a5ef62947406857faa2987b1df5781427e2c559ea218`  
		Last Modified: Wed, 09 Oct 2024 16:53:31 GMT  
		Size: 35.1 MB (35062896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c073ca505f4363ebfcb898f4d2a8b23427ba6069a5fb5b06cc80cb0df05291`  
		Last Modified: Sat, 19 Oct 2024 04:15:45 GMT  
		Size: 17.2 MB (17233776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce660df8e8e7bcaf60343fbb14080cb0995f3ab4cdfa5765f101525c99d3070`  
		Last Modified: Sat, 19 Oct 2024 05:32:02 GMT  
		Size: 51.7 MB (51671410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5e02463caf7de9f88f37613d8aa094b11341b4cf12a34e9c0cb5027b0a9154cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5105493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235e9b4dcf3d3b82a5b8a27770b6a8e1a16ee59f6f386771ef017a1d1f0d09b7`

```dockerfile
```

-	Layers:
	-	`sha256:18870027b00c8c1377dd93c6eae92bb606dbca04aeab0de9c5fcd1072358b90d`  
		Last Modified: Sat, 19 Oct 2024 05:32:01 GMT  
		Size: 5.1 MB (5098137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:644e927eea334c580d389006aa4b50d25abb00af7db86adaccf02768e08bb128`  
		Last Modified: Sat, 19 Oct 2024 05:32:00 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:7dcd4c9c250173f5241136de13c5d76c68cb13aea4202921dea27c75ff1bec55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.2 MB (102189461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45f5a29ff8520f0558ca8e6608ba4ed24e3bf003240379dc112d01b77636ca0`
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
ADD file:9744fb771a3525b1ecc8bb8c4ca623db4381f3fa78cd865afd2dc853a7ec0106 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c4c3b7ce35ec01feb67389e9cc9ac164fd53001e09b63553078d8d1e6ad0c713`  
		Last Modified: Wed, 09 Oct 2024 16:53:37 GMT  
		Size: 31.8 MB (31787862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe51613addcb9aebac5d02d07ded0ea6c171908f331d835d7c75b1cebb4be19`  
		Last Modified: Sat, 19 Oct 2024 04:11:36 GMT  
		Size: 15.9 MB (15873939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7fb3831c114a36b0b2c3c75c497b9581ec083768d0aa69432339a049abe6101`  
		Last Modified: Sat, 19 Oct 2024 05:47:19 GMT  
		Size: 54.5 MB (54527660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d9075d5353086f9f8f1d5ad1a4b08c86a8a2c42556bffdbed753c0d64f0af4fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5088341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eba17dc0ec912cb2bacd4d472b7bddedb156b6ade5d5d3950856afc4543f185`

```dockerfile
```

-	Layers:
	-	`sha256:a64d8c8fd891c47bfc45a5d57836ddd52829df56f468a9fa971eb9937cffe786`  
		Last Modified: Sat, 19 Oct 2024 05:47:12 GMT  
		Size: 5.1 MB (5080985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c8e227a3bf93254df4fb125746e67c01e90854fe7dba6b678862e2db84837cf`  
		Last Modified: Sat, 19 Oct 2024 05:47:11 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a3ac7dc97eb63d9013a092f3db71cfad7e4540dbe0e97a8b436c75e9add963f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95437293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a958ada935a3b94f4f9b08c16d40617d4a578b02c03f0bb7608f066c501304`
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
ADD file:e8f85fdb92ac3e5e436757449ac2447ad1520aad2682c8e0077efcce841566a1 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:303831814b37c8b218003169a08ba9ba85ed2a888e73d505841b5db92ec79efa`  
		Last Modified: Wed, 09 Oct 2024 16:53:43 GMT  
		Size: 30.8 MB (30774664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e574d553080236f570c1f83ee295b636102f93cefde1b709e84380c22d451f3f`  
		Last Modified: Sat, 19 Oct 2024 03:53:04 GMT  
		Size: 16.9 MB (16920088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e923714151c14f08933fe23d1283ee8fe44eabf4047feae2eb487e323f6a4b75`  
		Last Modified: Sat, 19 Oct 2024 05:14:35 GMT  
		Size: 47.7 MB (47742541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:eb8d26565a771439c11809356c7869ad7aeb0eb7eb0858f7c608d5356ef72274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5100092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8bd351ec2a646df3fff90485d2df39f601e0944b80d8b4143c9ccb3320d507f`

```dockerfile
```

-	Layers:
	-	`sha256:816052d2a74f2d518fe4b39b3f4c2ac66c3da2d731a25c9a46406294074d0043`  
		Last Modified: Sat, 19 Oct 2024 05:14:34 GMT  
		Size: 5.1 MB (5092768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb149f548535a0814f4e007c20ce2d36141cfc59043d9afd9bc1ff5f4bd4f4af`  
		Last Modified: Sat, 19 Oct 2024 05:14:34 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:scm`

```console
$ docker pull buildpack-deps@sha256:234ad1de0c6bd8ae1024516f64646becce5040299546d61dce815cb7ec74454d
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
$ docker pull buildpack-deps@sha256:6fbde97d2c5f38678ecc77dba69ae37004e01c5fe1060195a6fa0a03a166b6f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (138025417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:408d444d56480b9093884d1bd6088cbd039fc990d5bf1507bd57a0e13bdd3a33`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2112e5e7c3ff699043b282f1ff24d3ef185c080c28846f1d7acc5ccf650bc13d`  
		Last Modified: Tue, 12 Nov 2024 03:58:28 GMT  
		Size: 64.4 MB (64391376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d933d77fc474f2f63922bf70e05b7ea0af809991a3e5cb05967accda9f937dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7772096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5efb1b53407bad0cf8f47b0a1d54a6a9e90a27ae1c86a6a6de8f9bb3c8cc85c3`

```dockerfile
```

-	Layers:
	-	`sha256:b6f4689c52467b37f8370b7c0f6ac7fb405ab637e983b4ad7353590dd0a8a2cc`  
		Last Modified: Tue, 12 Nov 2024 03:58:27 GMT  
		Size: 7.8 MB (7764442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91abd18c81a94564d4a7151834429ae9fbf19f28c3a4e2937046f1a765ce3039`  
		Last Modified: Tue, 12 Nov 2024 03:58:27 GMT  
		Size: 7.7 KB (7654 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9a1f00aee35fdbfc3bbef35f7b430afe4b7d61335911b8ca883d4ee277540158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132068934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28e47e232c9eb35167cfd394f5c0f26dd9550bca5ee8ac3a7fb762992cd8e96`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:895d07844c9c09054971f530ffd0794c329a785344079a01ce24e3d51727407e`  
		Last Modified: Tue, 12 Nov 2024 00:54:43 GMT  
		Size: 47.3 MB (47338750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93efb128382700f7090be7bec74d12308eb11ced11717aae4403b7bccde20f24`  
		Last Modified: Tue, 12 Nov 2024 06:28:08 GMT  
		Size: 22.7 MB (22733304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5d34c31582cec80127fc538f65a56104fac2a20c87dbcaafc70b88f7a0a8b7`  
		Last Modified: Tue, 12 Nov 2024 11:29:42 GMT  
		Size: 62.0 MB (61996880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:146afff14da66d2415f7e870a0b5475327d3b8c5c3012e0e73e9929ce55432aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7773719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1139b21f47128807aca40d8f91d82ce8acf1684a9f67bba7bd10747e93444a31`

```dockerfile
```

-	Layers:
	-	`sha256:e5dc3d0311f5fe151c6c570f37bed7153cdc58ca55dc3f8244a7b0463ad6f4b5`  
		Last Modified: Tue, 12 Nov 2024 11:29:41 GMT  
		Size: 7.8 MB (7765996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3878cd87f19cd6baf6f4baacf94bb729da9783cc7ba94a83e2575efb914f143`  
		Last Modified: Tue, 12 Nov 2024 11:29:40 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d8da1a84da0bff207409bbac38dd1a02df0945b14ffd1fa2e34036a968789458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126740448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11391af0d1d3a25dfc5836b449c838b6faf132d3b8f3207da24d749b265ef353`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7fd5031c50fee563f16760ae6e5334672d6c9ba07d159b9e3a17a3b62011`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 22.0 MB (21957404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542f68420f2ab6efd74aba4b4ff72fe115144308ecea01703acfd9de4db386df`  
		Last Modified: Sat, 19 Oct 2024 06:36:59 GMT  
		Size: 59.6 MB (59635104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:82abbe189e4134358a35de062d14a33ab4ef2350f5335ed22d488f490c39e3f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7773386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a185c3d89851dea1a6599e78d946fb300c3e2ee6fe011b211285a182fc5e834`

```dockerfile
```

-	Layers:
	-	`sha256:f581eedd8301e57f012174ed44c98b695ef71465963ae45671ac92102a1eaafe`  
		Last Modified: Sat, 19 Oct 2024 06:36:58 GMT  
		Size: 7.8 MB (7765651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcf5b6a5be36ea85b8ff05143189e2f676d385b38504343c20e9f59dc37a002e`  
		Last Modified: Sat, 19 Oct 2024 06:36:57 GMT  
		Size: 7.7 KB (7735 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1b238ddfffd81f1788a7575612d8a052bad65a59129adf13b225091a1f798575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137528856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c89ba4d07f4ae3ae3debaa56c19ea06e7c0b9d2773c56679e3399263fadd9488`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5594266b1bacf9ad6855b00d9c5c98e721001eb115218eda673e548e04fdbf`  
		Last Modified: Sat, 19 Oct 2024 05:17:15 GMT  
		Size: 64.4 MB (64350044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4ae890e89350690ad59722f03f334f49def59e9a7a1b4eb60f59e60964f978fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7778540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ce0978485db8f8cd9635afd0ac7fc48b931593fe09f24a19d60b0d76c4e639`

```dockerfile
```

-	Layers:
	-	`sha256:5be58f0330ad5ad6c6e1439539fff91b3e586695d4806db0cf17398a4ea80ff7`  
		Last Modified: Sat, 19 Oct 2024 05:17:14 GMT  
		Size: 7.8 MB (7770781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd7d4cdd0c303535f95e2806de4f42d422c025d70f90f72882a1301f380aa64`  
		Last Modified: Sat, 19 Oct 2024 05:17:13 GMT  
		Size: 7.8 KB (7759 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:3a9a1cd1d4fc50ae45994fcf166dd95bd945fddb91781ffb82b09f84b8d70daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141687762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de9bf2a38fcbf043555508c597839677889c027dfa88e84f35a66f1493b14a2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:832e5094f1d1a0806638216e108f8c5f304112749840ba33b550928d48d45f1f`  
		Last Modified: Tue, 12 Nov 2024 00:55:00 GMT  
		Size: 50.6 MB (50577048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7251b79b00fcda89d3d742332ebf95721ed377cc22dfc14fb4cc7d2086df8c8e`  
		Last Modified: Tue, 12 Nov 2024 02:37:55 GMT  
		Size: 24.9 MB (24899410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c46592415d8ae65247d6cff038217c0ae0c38f5f2fee88eaa3f5ae09743a290`  
		Last Modified: Tue, 12 Nov 2024 03:14:24 GMT  
		Size: 66.2 MB (66211304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d29c3a56480553061917153ef4826fea0ff6b84616cfc7a020c1682e578f5c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7768146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23a9925b36e8fa4b0eddfc89cf9f299ae4e6da2ab487e270d5483829a67266f7`

```dockerfile
```

-	Layers:
	-	`sha256:21211546a412a59b68e54a0883d6e64098cc26325b2fac0f05cf5b94ab27c266`  
		Last Modified: Tue, 12 Nov 2024 03:14:22 GMT  
		Size: 7.8 MB (7760518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac6f9f590da617c7f5124adbdf5cc841c3d0456606c3d5617a33a51ecf792f53`  
		Last Modified: Tue, 12 Nov 2024 03:14:21 GMT  
		Size: 7.6 KB (7628 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:cadf76ca0578af7d2c32dce3d1860f04b28959bb1cb0f27e982288bba02c972e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136494026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0434755538859a36858a1cf943ffb9a3464378e9371f90644cb583fdfeefe551`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:5fa3d47e52ee376ed002c84d34e93fe11e6db2308915238c5d7a9a5840814eda in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bf8417b2ab139177317d556c6249cee54f60148ccee016ec60d45a13a21c7c2`  
		Last Modified: Thu, 17 Oct 2024 01:17:24 GMT  
		Size: 49.6 MB (49561619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba3cc6e574320e30c42f84b70c8e03fff0393ea65f20833b10b3a8aa1415e1`  
		Last Modified: Sat, 19 Oct 2024 00:56:12 GMT  
		Size: 23.6 MB (23648020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d702889c46052954a44f8b6ab39510d9b55acfe4a180194a7cb475c90b2b76e`  
		Last Modified: Sat, 19 Oct 2024 02:08:09 GMT  
		Size: 63.3 MB (63284387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:821b714bf8d6778d6d1b920a2baace275ae17c38d2e45770d4702d64b3d8634a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae759b8a8a22e7725a44091355ef141327e65f7a7442e018dfb5b90b94cf0cce`

```dockerfile
```

-	Layers:
	-	`sha256:7bab8cd7f7cc5b0a4b903dd7d23a799c7767e8dec89874cd1de2cc7ac2343c85`  
		Last Modified: Sat, 19 Oct 2024 02:08:03 GMT  
		Size: 7.5 KB (7509 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4a4289d5bc6db05198984f4e81697f55cc0d7ac6720bdcbdb13af2b5b385c231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149085096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3875cb156e725ad37ee97b98abf0f972f2ac10c4ff305204b30071a468158a4f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9170cd93e372271efe7b34bbee8de26bbb094efba80a15cff49f580f87e5fe40`  
		Last Modified: Tue, 12 Nov 2024 00:57:37 GMT  
		Size: 53.6 MB (53555270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92051d5a3f7afdf0c89db06ce83fb963b8719a7024153e1520472673570e9d51`  
		Last Modified: Tue, 12 Nov 2024 08:29:09 GMT  
		Size: 25.7 MB (25717543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913acd64029d37b20e9e161bb8659516cb78a99cfd56eb921fc4ccd76ae7c0c7`  
		Last Modified: Tue, 12 Nov 2024 16:09:31 GMT  
		Size: 69.8 MB (69812283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c21374c30e5f547aa9e66b04b1997909f699921da61d213ed3fb3d2a7de64c0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7779842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a315c2156e595de5e483e597dd3ea85ea0533d0e98f410011d7326f27679968f`

```dockerfile
```

-	Layers:
	-	`sha256:d9c5acd4f7b46ec0c9c2839752d6be8030b1bcc4d58b67483ad71a717d9899cb`  
		Last Modified: Tue, 12 Nov 2024 16:09:28 GMT  
		Size: 7.8 MB (7772149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1014f338054fa217964a7cd584f29304bb70ac47f3c759f554c010e2b966ee4`  
		Last Modified: Tue, 12 Nov 2024 16:09:27 GMT  
		Size: 7.7 KB (7693 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:029bcbdc4d92b810548bb6fe4d4a5d4fed99197e43c6a7cf1366a8d78db2c8fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135483424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ab4b43343266a1cc583fb48be5a34866624b123c7e48c1a091011da24be0f2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:be1cd8a5c7d60ebbe308ecf258da8f3d2dd59f7c877549c96e98e31165ba1eaf in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:510daf83b7a2b266658f37f8849eeeba99ab0f02d08ef5c1ea7f613451a81239`  
		Last Modified: Thu, 17 Oct 2024 01:50:15 GMT  
		Size: 47.9 MB (47938447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b213e07d4abfcac72292a81e546e7d80ad0bd5377b4de866c7a61ca19b5837c`  
		Last Modified: Sat, 19 Oct 2024 00:57:06 GMT  
		Size: 24.1 MB (24050397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a99db1e4eb0a57b7be4b1376a7fdf886d4118a6263595ad414d052eb69ee9b4`  
		Last Modified: Sat, 19 Oct 2024 03:46:26 GMT  
		Size: 63.5 MB (63494580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ecf9164fa7d6fe0f7178e89f1831c99d40d886c359e875262bf5d2f7fedb45bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7771243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8b973ea0fea3dbb11fa12a9b53632b91fca04c49806d2caf99693e37c78d69`

```dockerfile
```

-	Layers:
	-	`sha256:6e7b6cf839452bb8901601f821aa42480d98fc226c60373c907ff55920f3d325`  
		Last Modified: Sat, 19 Oct 2024 03:46:25 GMT  
		Size: 7.8 MB (7763576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ad6de2140fc403088cce711e23a06bd50be647583ddfcdda8b53b2134309157`  
		Last Modified: Sat, 19 Oct 2024 03:46:25 GMT  
		Size: 7.7 KB (7667 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:314578a876bdd46be55c7384f57a459c7197175df7e70c5e969f54eeef74beec
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
$ docker pull buildpack-deps@sha256:b0afb66526d240be44af24d222b1ce19acfe78052893de838fda19973402d501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.4 MB (369418391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667b3261aaabd8a7375c74cad935ce525d633924294649dbe9843ca6d64b82be`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c6dd4b778062640e2abc4c889c6db9feecceff7f28c2100dcfa570652558218c`  
		Last Modified: Tue, 12 Nov 2024 00:54:59 GMT  
		Size: 53.3 MB (53319444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73df9c0ffd5cfef9ed63d0dfdae57285f543f78320d947c5c4c2ab1422641cb3`  
		Last Modified: Tue, 12 Nov 2024 03:14:01 GMT  
		Size: 20.6 MB (20596172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0899f4ba4649838a893d7f1a70928afc27b147ea5051eac0853a716ef24ac8c8`  
		Last Modified: Tue, 12 Nov 2024 03:58:48 GMT  
		Size: 66.6 MB (66611604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ed16753ac0d236589a2917598d5bb24201a1ceaea372a998220ce50b9205de`  
		Last Modified: Tue, 12 Nov 2024 04:55:30 GMT  
		Size: 228.9 MB (228891171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1b890f2498c3d06d74a7599cb7d559795eec3be2ba36f8a137314885003385aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16842737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c73e51bc26aec5f86f0bc30b85d6af0a0476863bd7bcbefedc0bc2678c495610`

```dockerfile
```

-	Layers:
	-	`sha256:3442b9a36e4134cf6b67919c2d04b50476534f845c966ca8e6fb00848e915279`  
		Last Modified: Tue, 12 Nov 2024 04:55:27 GMT  
		Size: 16.8 MB (16832561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:540e6d55dabb7696f8459f07f029499d23edaa473f9379257c196530e33b6b4e`  
		Last Modified: Tue, 12 Nov 2024 04:55:27 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:64f60ab32c8ad2e44569bd34aeabfcbcae655596ac34599c5336dcb78f1347f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.7 MB (337698112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fef2df89ec55a84f53ca077a2e2093c773663a924f03a53bdb6116f54dd565`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:48142c53989e584e5008e025d7add416317666ef57f1383dab96cb3b5dd1610c`  
		Last Modified: Tue, 12 Nov 2024 00:55:48 GMT  
		Size: 50.2 MB (50178305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677e719f1a345c9d868951b12d49877be0a8ce88c74c1d28554e382cb36c8fb0`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 19.6 MB (19609396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a80294a22345764a6f713791d5e78ceccbfde6983b0bf68a23d16e31cb7a8d6`  
		Last Modified: Tue, 12 Nov 2024 11:31:21 GMT  
		Size: 64.1 MB (64064343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeecbd78ab8f389d36bc7c389a258f35fcb1d7c525c852264f355392a01b52a`  
		Last Modified: Tue, 12 Nov 2024 13:57:37 GMT  
		Size: 203.8 MB (203846068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d6d24b2e38e21cc1d214a4e09d6ef1cda2fb1f0fffa2e118fef221c726e42ede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16634683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da72b7f704e230a29b6d8886bd354cea7afd55b586897a8685011369124695d`

```dockerfile
```

-	Layers:
	-	`sha256:5cf2be7911debe59da7ccf2740ddae1696946eaf5fec6399bba7ceafa9082524`  
		Last Modified: Tue, 12 Nov 2024 13:57:33 GMT  
		Size: 16.6 MB (16624447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a10c1a45b73521ebcf10c889a4ba4d096cb8325e02ba6a3ce6727a8947f2c49`  
		Last Modified: Tue, 12 Nov 2024 13:57:32 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:51225fd5a278a81a1c2e8baf0a39084f097446e073dd1cab41c44757e14c006f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.3 MB (318326856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c31c7bdbc1cdd6c1b92e543e9f56aa00f75503c3f8522f27070a52efdb4d313`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:bf9375f2b0e5c66c0a1840e13cfa8b3f0aa55934d9c92c13e479c8cf7909e923 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cf1d8a933c6efa9a7129c6faf202eeab8feff677f32fbc0037a3ab76003edcf8`  
		Last Modified: Thu, 17 Oct 2024 03:09:00 GMT  
		Size: 47.7 MB (47691399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5bb5787cc9d2878988b37d2049fa1d6b67ff3450f012cef9603dcff05b03ef`  
		Last Modified: Sat, 19 Oct 2024 00:57:32 GMT  
		Size: 18.9 MB (18893656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f7ad36a85c1a25fec35fecdd0c231974acf44c7aaeec9321464cf908e0e452`  
		Last Modified: Sat, 19 Oct 2024 06:39:20 GMT  
		Size: 61.5 MB (61460990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b53af5a773d7f35e45f47783bfcad7fdfe09493d624315c463438ee3dd9f85`  
		Last Modified: Sat, 19 Oct 2024 08:12:52 GMT  
		Size: 190.3 MB (190280811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a1176727d50799e82d4d2bfa3c69443f0367037f3feabb08f8d57c4d756d9f41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16421324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ab1f5a6bf51385b18a4b74c31ca3c7819e926eba8582453cccb6dfda27e50c`

```dockerfile
```

-	Layers:
	-	`sha256:1851bd99397931249134eeccbef9025844d241e61f0ab5fbf1a0e8ec2a0aac9e`  
		Last Modified: Sat, 19 Oct 2024 08:12:48 GMT  
		Size: 16.4 MB (16411076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef72ff3aacc21648a8dc4406f49449fc8d535604650bcc28f2cb04734076428c`  
		Last Modified: Sat, 19 Oct 2024 08:12:47 GMT  
		Size: 10.2 KB (10248 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a5bff4e6897ef7ce3d60f235ece06477a670c718938744616f5c5be5f3cc0dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.2 MB (362218506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4617705cb588626ef2ee3fd18d59a3c8c267abb961000229b9cada35dd22a8fc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:58acae53f12429504dea737cd60eba46c5f2eea862974a8d8fe218c17d285565 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d246237d395a465ccb5ede6b1a321d43a78766a62bc93015a0368a88624aedff`  
		Last Modified: Thu, 17 Oct 2024 01:15:57 GMT  
		Size: 53.6 MB (53629485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b80bac00a06288366529b5187b9485c685d4f46018bcb866049abf9f952247d`  
		Last Modified: Sat, 19 Oct 2024 01:11:43 GMT  
		Size: 20.2 MB (20196615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19663fa8e0a57915a50484edf1e2599200b05cd9b029d04f6246f46e4ebd7b8`  
		Last Modified: Sat, 19 Oct 2024 05:19:11 GMT  
		Size: 66.6 MB (66554364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a1930b82ab676514849567fb2f84c77abe6dd46e00fdaf27bdffdd5e50852c`  
		Last Modified: Sat, 19 Oct 2024 06:19:49 GMT  
		Size: 221.8 MB (221838042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:aee10b071d72be87195fdd239fc32f4bc897cf5365082395c39d748923726e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16719540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce06ab8b69758fa40926415c0cc6e0fc487417847973ce13cf61898b34595a31`

```dockerfile
```

-	Layers:
	-	`sha256:0c705747a331f205ed3932bd8aebffa27283a5197af7462eb8b34649f08b2b6b`  
		Last Modified: Sat, 19 Oct 2024 06:19:44 GMT  
		Size: 16.7 MB (16709272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88f34d6a5ad6f6573131d992417c533e6d9e3aa6754dd91f84650909955ea149`  
		Last Modified: Sat, 19 Oct 2024 06:19:43 GMT  
		Size: 10.3 KB (10268 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:174aa49a8c627409e7b2ef469e0b4ca424e1d67801529a24e00206f67c85e020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.6 MB (374625880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e991a9111b7923adb2bf1517a0cea45e0e2cbe21c971a883abc5d20fe7018c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:266f316e766c7029b1cbb65159b6d9ea1da28d00e28cf109ea069ce95b082ac4`  
		Last Modified: Tue, 12 Nov 2024 00:55:10 GMT  
		Size: 54.2 MB (54192046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24546888a84a1c2171ba5648f213b4d3b8fee560f454ad1c12f583f6ce895c81`  
		Last Modified: Tue, 12 Nov 2024 02:37:52 GMT  
		Size: 21.7 MB (21725392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885dfc308254678967ab6d79ba6d40d73a4ad263c111beedb94327edea737b17`  
		Last Modified: Tue, 12 Nov 2024 03:14:27 GMT  
		Size: 68.5 MB (68538589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470064ab8c694d08e8b01d3ab58e57e6bbb9021d73b77eab103438c7c9d1b9de`  
		Last Modified: Tue, 12 Nov 2024 03:59:40 GMT  
		Size: 230.2 MB (230169853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c68dc1085e970079c0dad9475c90a626f3fac854d399d14c64fc0624e1214a07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16812358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c69c51ca15442a3ea0f50ed9b720d7bc599cb88cfe9ea50099b42ec77303de`

```dockerfile
```

-	Layers:
	-	`sha256:e8d60b7da8728b26a8fa539127c6eb8ccfc4ff307613730c7801c4e74932bef0`  
		Last Modified: Tue, 12 Nov 2024 03:59:36 GMT  
		Size: 16.8 MB (16802204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5db9b50ef37135bc668d6adde1f571e925b918ed88cc1254591868dd645594d0`  
		Last Modified: Tue, 12 Nov 2024 03:59:35 GMT  
		Size: 10.2 KB (10154 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:7aed501446d1d4aff5e4e665344ff39c2bb23697f79269ade9d17d43c74bc637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.4 MB (346369313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d558ca969f15110f47b12e6e5f8ac0b3c2bc1d5aef4bccd85c13c7d012683040`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:8ffd9575546e69884562db46178b841df2ba1ed04549599485b7c502f81ac4cc in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e3c6aca2e6ea9e1b19b3c46a60581e28de71137e5bd8fe9c8ea62365a8e75d74`  
		Last Modified: Thu, 17 Oct 2024 01:18:46 GMT  
		Size: 52.2 MB (52157899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35efd481e6347988498fa292e64d8b2f0d728f327f48bccb1d2c2bf371f2f1e1`  
		Last Modified: Sat, 19 Oct 2024 00:58:29 GMT  
		Size: 20.9 MB (20887623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10d42e894e27bd8661997e28ccc989f4b18c73e3892449a02653f995d796aea`  
		Last Modified: Sat, 19 Oct 2024 02:11:09 GMT  
		Size: 65.3 MB (65280292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5494e53db7cb17f11f8f3553b0b8f89e494429f535472ab40c3dc0a4a53a958b`  
		Last Modified: Sat, 19 Oct 2024 03:09:12 GMT  
		Size: 208.0 MB (208043499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0c7f47bdc09a05b6d948bb27b33411f3b5a300b2c8d1c54d84eebe0c13592d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52a53cd41b52a2ffac4c7c5eff91689862f82eab42ecf464a1ad8ccafa36f61`

```dockerfile
```

-	Layers:
	-	`sha256:c6c4c3b65b2f2ee5188b595c005cab57e11fa88adc238818500a0f9d289bb37a`  
		Last Modified: Sat, 19 Oct 2024 03:08:54 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6e1614575430aae725ce4d1ca72a021b64b14a73524639c6866a13aba370b80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.0 MB (378020992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972288b37cca39db49db1bfbe29a851813a8543f0a7f4c72ce65531923b42a8b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:3f30d2b91e08061eb3185f2f9c67756024dc8f3e6cda74d75d6ae54a603cdd2b in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:df36361b5ac72face21de9a14adcec98ba3abb2261a8339bf516725d8753f43e`  
		Last Modified: Thu, 17 Oct 2024 01:22:16 GMT  
		Size: 57.2 MB (57176824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30f3cdfb0755564cd3c4456a7fa23e621d79e4f8f43bd8107c734f66d381334`  
		Last Modified: Sat, 19 Oct 2024 00:57:49 GMT  
		Size: 21.9 MB (21944061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fc954d509992bc0347fcedb989b7696ca6b5029587c5a3cacd05686fe99e03`  
		Last Modified: Sat, 19 Oct 2024 04:08:51 GMT  
		Size: 71.9 MB (71893560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e8fc7c4002604d4ecd95f73b88e6577ffdafa0c5d8add4adfe85a32b924574`  
		Last Modified: Sat, 19 Oct 2024 05:20:49 GMT  
		Size: 227.0 MB (227006547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e5a372eadfc10bc82dad638f92376f112fff82b71cd161e5b05c835e3e4d7423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16621262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46ae6569046be118b2021b37e251e01f3d851d6b370fb2e380a09f956b1c437`

```dockerfile
```

-	Layers:
	-	`sha256:4b845df74b1833d65eff42db4f1e60c04ccfa5b2e99372f560c60ba8e33d6eff`  
		Last Modified: Sat, 19 Oct 2024 05:20:41 GMT  
		Size: 16.6 MB (16611042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:080d4475f5f734ac76d094f5229cb78e77712607292807a5e1b8fba7c54e82aa`  
		Last Modified: Sat, 19 Oct 2024 05:20:40 GMT  
		Size: 10.2 KB (10220 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:9170b718174b1a2155dc6f1f30be5d257ea77bfb5cfd20c8b882eb76bd970ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.9 MB (449863543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578f59755f82ae837d05d043953beeddcd5bed8e73b690b8f7d707e36ed9644e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:9748961f840a27ae3342039309a28acc84e3a482f5ca3ece5bdaf9f92e7ebe33 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:29cf887cb660615390407db841ad4c44be2414b9bf999ba668d93a8305675c7e`  
		Last Modified: Thu, 17 Oct 2024 01:14:47 GMT  
		Size: 51.6 MB (51562685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de12fa48532c87115805a1e3efbbdd980575096676ddd00868f642d72782b610`  
		Last Modified: Sat, 19 Oct 2024 01:03:17 GMT  
		Size: 20.0 MB (20023981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c05579e9b49f41a2b6960286d8ab9b1d090127915ab4b5f2c9ec35e3db7815`  
		Last Modified: Sat, 19 Oct 2024 03:48:10 GMT  
		Size: 65.8 MB (65756980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1c1438a38b6b5f19898954943b519c13357a75b5de527c10fdfa839a2bf9bb`  
		Last Modified: Sat, 19 Oct 2024 05:19:52 GMT  
		Size: 312.5 MB (312519897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9d4efa39a2089a0bae14fc598dc2be9721c56cf31ca6d013b630959dd86d0a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16684099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c950fcfad2f9ac619e283071159fabbe0d2519f685c971de572607a5a2ab72c`

```dockerfile
```

-	Layers:
	-	`sha256:c00879de8cdfbb4f86a8411d81ebbb57bfefc3b7b5517bb5e81cdec0f5d57951`  
		Last Modified: Sat, 19 Oct 2024 05:19:13 GMT  
		Size: 16.7 MB (16673879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7759997ee312035b99e28a615c8b12688bb5567df93ee0be4e659c908478b864`  
		Last Modified: Sat, 19 Oct 2024 05:19:10 GMT  
		Size: 10.2 KB (10220 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:03ae369846cbc99feaec0d7a675c3f1cb296806fe18be3ea3f2b2fcd60ecb688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.8 MB (343811634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2955362ae47bf0486452d86b59e314d1f8357dca737a96af3e6f917fc1c7969`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:2f1a819570e851a9bce2342f32c7927abdb02af08d5e469e6f5d41a193235bb2 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:79590eb16acf1f35f7a00e8c30e7daf7ed5d8bc9d65ff782665704f532af0ac0`  
		Last Modified: Thu, 17 Oct 2024 01:50:44 GMT  
		Size: 52.9 MB (52851981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf56c8e1a853602c0af0f40a2561d6ca90c547c99b9bdd2c5349a88e1f5cc1a`  
		Last Modified: Sat, 19 Oct 2024 00:58:05 GMT  
		Size: 21.6 MB (21639639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a7102bce19ae53b519fb58ec97dd26aadbdffdfec95cd2613f51b842e60866`  
		Last Modified: Sat, 19 Oct 2024 03:47:42 GMT  
		Size: 67.6 MB (67567932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006e2316904bd5e5d8b5be83f2d3c16ffc8b744bd23f895fab2465c751a090a2`  
		Last Modified: Sat, 19 Oct 2024 05:06:51 GMT  
		Size: 201.8 MB (201752082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ba7e3ba1bbeac3a6078f008e5ee17b68529098e3909600dfbe90edb605f54c0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16414228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc84b27183ff88f33658ac103e14e91bb216a76083e15c060fef435fa42bfad`

```dockerfile
```

-	Layers:
	-	`sha256:1ee265a8788e328e9fef94039d90ab4df6d624dfc385d1e5faa95efe0c935af1`  
		Last Modified: Sat, 19 Oct 2024 05:06:49 GMT  
		Size: 16.4 MB (16404040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:306d2621686c7e09b57487558deeb4f574d7074bcde002751c60c8186e07ee0b`  
		Last Modified: Sat, 19 Oct 2024 05:06:48 GMT  
		Size: 10.2 KB (10188 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:1404bcfbcdcb783c0c131bfaf3a6e2b6d8789eaa3160d997450ecaadffa8b4da
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
$ docker pull buildpack-deps@sha256:9f132228a17ef7148bdb181e503e91853e85e87c2bc91361f6705a2ea4818832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73915616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33126cfb84f42e1dee4d3bcd8e62d6e742b0c0fc0da59e149a079f4174ed740b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c6dd4b778062640e2abc4c889c6db9feecceff7f28c2100dcfa570652558218c`  
		Last Modified: Tue, 12 Nov 2024 00:54:59 GMT  
		Size: 53.3 MB (53319444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73df9c0ffd5cfef9ed63d0dfdae57285f543f78320d947c5c4c2ab1422641cb3`  
		Last Modified: Tue, 12 Nov 2024 03:14:01 GMT  
		Size: 20.6 MB (20596172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:39c0a59346b52c497cdfee9ee501696a0137d33c4d869b8ccfb052b35a48c57f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4059772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d64c3f557019664b8ed03939a488b65f662ae5ba8df3f8558e7eb7f4ef96f1d`

```dockerfile
```

-	Layers:
	-	`sha256:6c5e88c9e7aefc1e66a2fb244bc4a7ee4a01996d4d1643d54fd9141b9d68c098`  
		Last Modified: Tue, 12 Nov 2024 03:14:00 GMT  
		Size: 4.1 MB (4052968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e06a147cc0d21461ddf7350b95eadd2a56c4f93dd20e46f3562015b2a9cc19c`  
		Last Modified: Tue, 12 Nov 2024 03:14:00 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:6fa397aad3f688ae8c5a6a419b92021b1cdd17421ded456fab3c2ba159b1728e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69787701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4def3959c1ec2cc47ca9f650e6e392ddcdf199ed79296fefa9f23c546bc85b9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:48142c53989e584e5008e025d7add416317666ef57f1383dab96cb3b5dd1610c`  
		Last Modified: Tue, 12 Nov 2024 00:55:48 GMT  
		Size: 50.2 MB (50178305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677e719f1a345c9d868951b12d49877be0a8ce88c74c1d28554e382cb36c8fb0`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 19.6 MB (19609396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:957883ff2bb35b1ce0198b37996e8b3b914135501561c94a4a330818e42e78a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4062054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e70fea3252b42f59d8b501dd5ad764980a1381758257617d06e4dfa151cc2c7`

```dockerfile
```

-	Layers:
	-	`sha256:88ff8e75bfa6830f20cbe46c2c6274c66debaf6f7cb42e797f70f8ed1ee639ac`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 4.1 MB (4055190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:289839fa0d0c8815427f524a3c398ca48fb266a4cc30b70e149da06d2f68dec8`  
		Last Modified: Tue, 12 Nov 2024 06:29:06 GMT  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e9f57fadeb4e2571a3ec639deb0bc50041f8eb09f1c35e7dd31f63f51219c7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66708282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a041b6b0da1491b1f95275953492d2a5af327c22639fae585debed4b0683d27e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e17a4ae99f3dc5642f3037bdf67fdb8d526cf44879dc2a2a82dd78799b94cb90`  
		Last Modified: Tue, 12 Nov 2024 00:59:40 GMT  
		Size: 47.8 MB (47762858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0690a3ea44bb2abf7747807b4adbbe717ea3308dcc90d88289979cc43a641049`  
		Last Modified: Tue, 12 Nov 2024 16:01:31 GMT  
		Size: 18.9 MB (18945424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:43d8aae958a0e128d324dc93a72825f729ab6fa94ca19355525166bb05a47f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4060852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b10f2357762de298e91d49a699d21a40cda9a432c28280f401740f16e5a614`

```dockerfile
```

-	Layers:
	-	`sha256:bf93bf2e4fce3088d42a757f8456cd7a2023638444e133ff88b357911a40ea9a`  
		Last Modified: Tue, 12 Nov 2024 16:01:30 GMT  
		Size: 4.1 MB (4053988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:751e72f96ac24e34e31ae67f31c52b074761c75e5706d996f2d7158d36e3ecb4`  
		Last Modified: Tue, 12 Nov 2024 16:01:30 GMT  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f2d64356db4518efc4b1d5c851bbec90bffc5a3786a1d40a66641c2ddfc581d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74010502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755881583c95b82ca8b14fb557a3d30c6d7372621bc567aded061824b5eb9e13`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0c8e2196f060907b4d5381cc165d86913c4b9e9c632b3596563398b5e178a84a`  
		Last Modified: Tue, 12 Nov 2024 00:59:55 GMT  
		Size: 53.8 MB (53759747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2180b05bcdf8eaedc4db9cf7f65afe026827aad32c4e4b7f24679e6ea2c63305`  
		Last Modified: Tue, 12 Nov 2024 11:17:08 GMT  
		Size: 20.3 MB (20250755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:88c0a9ebb6e4d36deef41d358c47e1c05da025bfee528155d8dd8ae4a515c78b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4064747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23d1f98393785b001948920b2a88dc59d5b07744d55dcaa5407498fb1c5c887`

```dockerfile
```

-	Layers:
	-	`sha256:cf4589ea08d8203c40a828f62b71489ecadea32a9e41505f049036274b6fa84a`  
		Last Modified: Tue, 12 Nov 2024 11:17:08 GMT  
		Size: 4.1 MB (4057863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6e1e9a818425575ef20fea5def0c73f7b9ed82c20a2be689147698cbb1b6340`  
		Last Modified: Tue, 12 Nov 2024 11:17:07 GMT  
		Size: 6.9 KB (6884 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:713ac9d8ce038686ba88e304844d03029927103f715e36c6e3e7e643f648cba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75917438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcbbb27c071a87a94f9d4da6a554ba80e231a4d61d781ef5427f2ea0cb7bfad9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:266f316e766c7029b1cbb65159b6d9ea1da28d00e28cf109ea069ce95b082ac4`  
		Last Modified: Tue, 12 Nov 2024 00:55:10 GMT  
		Size: 54.2 MB (54192046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24546888a84a1c2171ba5648f213b4d3b8fee560f454ad1c12f583f6ce895c81`  
		Last Modified: Tue, 12 Nov 2024 02:37:52 GMT  
		Size: 21.7 MB (21725392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e72acbe40d1dada9f63a05e02f9a246749c53f9785c0f442cc4a3c00ab26b48d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4055490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58971737022f0686ee08a7e75b6b49ac4d35e293b2ac50c454cd02dac2be18d`

```dockerfile
```

-	Layers:
	-	`sha256:f398d7abacfae0299acc85184a23c92cb8040f679acc31f49830129acfcebcea`  
		Last Modified: Tue, 12 Nov 2024 02:37:52 GMT  
		Size: 4.0 MB (4048708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d240f2a814476b467a314a67e75244714b4479add937403e3b8169171e9cce8`  
		Last Modified: Tue, 12 Nov 2024 02:37:52 GMT  
		Size: 6.8 KB (6782 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:62e1a2cab54ce402ef56d67975b9e97f7db49042e7d9bcf2803dad0e2b4f5507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73225428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f90f18670b8a0f2f53c92f8dd49e6e04300c5b5b5ee0a08f2c595286336db07`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1f6d00c97864e98dad498c4c1087cda2fb16f2ac6e7a71ac1353418dd4215995`  
		Last Modified: Tue, 12 Nov 2024 00:59:58 GMT  
		Size: 52.3 MB (52275237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ee73bc743170bb5e4087d57c95a63d610fb1282220d73ff90af4707b831d99`  
		Last Modified: Tue, 12 Nov 2024 18:03:00 GMT  
		Size: 21.0 MB (20950191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2cd9138da59d486eee86b97f0b2ef5c327cbddacc8555d0ca1e2f100ddab0c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 KB (6635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e8f2688580c7be9086b175b4a45597708a571c9d0545210c877212967e0e9a`

```dockerfile
```

-	Layers:
	-	`sha256:6c68010a95014043302ab3a4f944d5dd5ce7882ce431430ff613035bcd549ba7`  
		Last Modified: Tue, 12 Nov 2024 18:02:58 GMT  
		Size: 6.6 KB (6635 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a4f1105859b8534b986cb747f39eeb29301d977a7735a4d128f7a9b8cde3fde6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79301505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b6e4d2082fca0422d715db56ed40d43739efbf27aeb90a1bed244f273c5c7d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ac2d911f8489db0bbd6f313128660ffb4f315b3d99baed39d7128c198fea25b9`  
		Last Modified: Tue, 12 Nov 2024 00:59:35 GMT  
		Size: 57.3 MB (57309355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5f3e8aa1353894772b7fd9d91dc6448cf8573234fedf1ba1c8596471c52519`  
		Last Modified: Tue, 12 Nov 2024 08:30:11 GMT  
		Size: 22.0 MB (21992150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b2a081bdf1d2cc2fd96de5e53f9ad7551c0c1a4edf1d7e6e4e7b1b039d1a8817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4063088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f435dd30d7af7fe9206c19d35ee69326d7c1322625a8ce82779e9a352afe5b`

```dockerfile
```

-	Layers:
	-	`sha256:89d1f5a9bb4126e98982aeb9314bfa7d6ecd1747d5476ccf95e8bdadbc5a0c40`  
		Last Modified: Tue, 12 Nov 2024 08:30:10 GMT  
		Size: 4.1 MB (4056253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a91d4883ebc57f8ab63c60eb7aee2ae34e1523993d2abe0379238091fa712ec`  
		Last Modified: Tue, 12 Nov 2024 08:30:09 GMT  
		Size: 6.8 KB (6835 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:f2563b5986e1cbd6355ebaa519efbefd1ace7d95ec4dc05fb43d702a17656346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71586666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2201578f73abedc744f4f2994cc04bf7653e03e6fc71c488b56b938fa6133682`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:9748961f840a27ae3342039309a28acc84e3a482f5ca3ece5bdaf9f92e7ebe33 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:29cf887cb660615390407db841ad4c44be2414b9bf999ba668d93a8305675c7e`  
		Last Modified: Thu, 17 Oct 2024 01:14:47 GMT  
		Size: 51.6 MB (51562685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de12fa48532c87115805a1e3efbbdd980575096676ddd00868f642d72782b610`  
		Last Modified: Sat, 19 Oct 2024 01:03:17 GMT  
		Size: 20.0 MB (20023981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:07e79f5072ea67bddca2130da2f9d315fd8222cd0609708a470e88dfa7353806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b8dcf549e44ce65cf2139914167a0d0f4b1a4302bf162cbab4d7642cccbbb69`

```dockerfile
```

-	Layers:
	-	`sha256:4e7d1496ab905e4028f005f5a14166826563eecf34a3ccd9a6dd3ce4b9c1412c`  
		Last Modified: Sat, 19 Oct 2024 01:03:15 GMT  
		Size: 4.0 MB (4022143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d30c866b540503398d1018dd68b46d07f0f51532b55b00079c6208979ebb5f5`  
		Last Modified: Sat, 19 Oct 2024 01:03:14 GMT  
		Size: 6.6 KB (6616 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:584fa4000f2547dc5479f02874a482edade85498ae0ebc4df274f79647fb3ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74690422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0022a7a4ff00d7705bd101cdcaa1424b4499051d4964d76bba5c85e1d5288b04`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:01b62be41cbf7168e02a9fa648a1525f0c9095aef51faa9027bf3a9ff89c6b84`  
		Last Modified: Tue, 12 Nov 2024 01:00:18 GMT  
		Size: 53.0 MB (52980914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa52c56b4fa2fb05d933bf62d254d5f4371a5a9e6992ccf74613eefe11aaa96`  
		Last Modified: Tue, 12 Nov 2024 09:02:57 GMT  
		Size: 21.7 MB (21709508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:138584e0a4f75cbcf1075cd15e1a74e213a01490927fd7a2e7cb7cfc2f20ca9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4060697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf8abf20b9018f2f62da56f1e38c88bc5b0f2b665cd3aa99e863dd2d57a1832`

```dockerfile
```

-	Layers:
	-	`sha256:0c53ff2c3883ba64e4c118aa75e4d48c078ec5aeb46b97155e2600f1a4197361`  
		Last Modified: Tue, 12 Nov 2024 09:02:56 GMT  
		Size: 4.1 MB (4053894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1f3c58081085a03c94c082ad8f5d4a525cd67ff9c8789de1a9dd1e752fe8722`  
		Last Modified: Tue, 12 Nov 2024 09:02:56 GMT  
		Size: 6.8 KB (6803 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:c7516a6d3202303a24246bddec8a9bfd8031ffeb797b10dd3485479bcd6f431e
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
$ docker pull buildpack-deps@sha256:8ab7ea446bf8fc89524695d33da2ef73a78861037d001ca1d09acdf7d7614c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140527220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f3d6b5bdecf0d50cba2b30fcfef9e6c15ece0fec037adce41d28e2fb76e848`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c6dd4b778062640e2abc4c889c6db9feecceff7f28c2100dcfa570652558218c`  
		Last Modified: Tue, 12 Nov 2024 00:54:59 GMT  
		Size: 53.3 MB (53319444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73df9c0ffd5cfef9ed63d0dfdae57285f543f78320d947c5c4c2ab1422641cb3`  
		Last Modified: Tue, 12 Nov 2024 03:14:01 GMT  
		Size: 20.6 MB (20596172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0899f4ba4649838a893d7f1a70928afc27b147ea5051eac0853a716ef24ac8c8`  
		Last Modified: Tue, 12 Nov 2024 03:58:48 GMT  
		Size: 66.6 MB (66611604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:983d3401a2f2ef93b8b63c76b3eaea3455a247cf97c2b075dcbcc144f508ae42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7621436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767f303cc728dc43cf2a4fd72997cf80938888305f42cb037c7aabd481ab5a54`

```dockerfile
```

-	Layers:
	-	`sha256:f39cef2c674b6a5197868f663359c3af90f575a188282358e57c0aa4ce6b0328`  
		Last Modified: Tue, 12 Nov 2024 03:58:46 GMT  
		Size: 7.6 MB (7614139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32690f39b8e5187bfe3b6b0929620b5230e9bf80dafd63d62c533cf04b46233f`  
		Last Modified: Tue, 12 Nov 2024 03:58:45 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:848ee71fe2c9412ccf8a147c76f6ec97c3acd3ebf83a5f18775f0c48b308e851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133852044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e043f8c929df470ba036b874156f397c9e570d1adaf2e85b886e5efb33f5d473`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:48142c53989e584e5008e025d7add416317666ef57f1383dab96cb3b5dd1610c`  
		Last Modified: Tue, 12 Nov 2024 00:55:48 GMT  
		Size: 50.2 MB (50178305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677e719f1a345c9d868951b12d49877be0a8ce88c74c1d28554e382cb36c8fb0`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 19.6 MB (19609396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a80294a22345764a6f713791d5e78ceccbfde6983b0bf68a23d16e31cb7a8d6`  
		Last Modified: Tue, 12 Nov 2024 11:31:21 GMT  
		Size: 64.1 MB (64064343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ad4c5dc36112c0c74e99ac96fc1805df43ef5c11db6b7fcdba77b0eb0c0d3713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7621762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de220d7aa70d91d334a8498c9ae1e10d8f8c53b8508bceece7f84a5803c9f1a9`

```dockerfile
```

-	Layers:
	-	`sha256:2b742fb0e0d70644066c1472b3cb6559ba91cdd89925f703883bb76e11cfd5da`  
		Last Modified: Tue, 12 Nov 2024 11:31:19 GMT  
		Size: 7.6 MB (7614405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cfee709989da69a1418471850a2f2c0f2c90e1bf104a675f2aa68f702e9f8df`  
		Last Modified: Tue, 12 Nov 2024 11:31:18 GMT  
		Size: 7.4 KB (7357 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b3c420a89727b5dc5067f3f9dd02acb063f57893e27884c02d8f2104e5e05870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (128046045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738f1c2cb570c23741cfe2b7fe5652af9bef05fa04bdba68ae8b35b33e93925b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:bf9375f2b0e5c66c0a1840e13cfa8b3f0aa55934d9c92c13e479c8cf7909e923 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cf1d8a933c6efa9a7129c6faf202eeab8feff677f32fbc0037a3ab76003edcf8`  
		Last Modified: Thu, 17 Oct 2024 03:09:00 GMT  
		Size: 47.7 MB (47691399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5bb5787cc9d2878988b37d2049fa1d6b67ff3450f012cef9603dcff05b03ef`  
		Last Modified: Sat, 19 Oct 2024 00:57:32 GMT  
		Size: 18.9 MB (18893656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f7ad36a85c1a25fec35fecdd0c231974acf44c7aaeec9321464cf908e0e452`  
		Last Modified: Sat, 19 Oct 2024 06:39:20 GMT  
		Size: 61.5 MB (61460990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b9db4cf0319144959de60546593784cc663d31b4196f01692f0735bbb32f55ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7598561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5a3d725a4310da5f1831130375142b0c20d3b76ad85c1979e28711f6289983`

```dockerfile
```

-	Layers:
	-	`sha256:fc2860af086787f7758af329dc104412d3c616d8f41f41ca89aad651c478bed6`  
		Last Modified: Sat, 19 Oct 2024 06:39:18 GMT  
		Size: 7.6 MB (7591192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ab2ce55dca633eda9a90680cc443df4c7645b5e860e2cf82d4861989c3d253a`  
		Last Modified: Sat, 19 Oct 2024 06:39:17 GMT  
		Size: 7.4 KB (7369 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:802c828bc2d5c912348dee436053e3aa7d82d26837f894566a3f6381b19a0ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140380464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877345af7ef312c479c5be927342731e90dd345572ff8fde69dde61a4aa757fe`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:58acae53f12429504dea737cd60eba46c5f2eea862974a8d8fe218c17d285565 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d246237d395a465ccb5ede6b1a321d43a78766a62bc93015a0368a88624aedff`  
		Last Modified: Thu, 17 Oct 2024 01:15:57 GMT  
		Size: 53.6 MB (53629485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b80bac00a06288366529b5187b9485c685d4f46018bcb866049abf9f952247d`  
		Last Modified: Sat, 19 Oct 2024 01:11:43 GMT  
		Size: 20.2 MB (20196615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19663fa8e0a57915a50484edf1e2599200b05cd9b029d04f6246f46e4ebd7b8`  
		Last Modified: Sat, 19 Oct 2024 05:19:11 GMT  
		Size: 66.6 MB (66554364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3bdc370b125ed8b8193e8750270c2d8ec3cf86815e299ac1b5e01a42224844b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7604477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739a6c936ffbddb93e2f0497b97a3910e5b4a89d807763c9a97116823c23aefc`

```dockerfile
```

-	Layers:
	-	`sha256:95ec60fa71429ed1b411dc8b543221800db7aba2271e78572346255708271d50`  
		Last Modified: Sat, 19 Oct 2024 05:19:10 GMT  
		Size: 7.6 MB (7597088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0473ea6aaf55e12d5241f62663f89556fbee6b5d58ad766cf0d2a66168faf10`  
		Last Modified: Sat, 19 Oct 2024 05:19:09 GMT  
		Size: 7.4 KB (7389 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c104a59a3c4fb391a52f93cbfb13639f2687fc4366f11bd4751a0070ae46295d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.5 MB (144456027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b888da81dfbdafdde34e7d00d58c2571e37c5eb4452bcb663b3985887540668b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:266f316e766c7029b1cbb65159b6d9ea1da28d00e28cf109ea069ce95b082ac4`  
		Last Modified: Tue, 12 Nov 2024 00:55:10 GMT  
		Size: 54.2 MB (54192046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24546888a84a1c2171ba5648f213b4d3b8fee560f454ad1c12f583f6ce895c81`  
		Last Modified: Tue, 12 Nov 2024 02:37:52 GMT  
		Size: 21.7 MB (21725392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885dfc308254678967ab6d79ba6d40d73a4ad263c111beedb94327edea737b17`  
		Last Modified: Tue, 12 Nov 2024 03:14:27 GMT  
		Size: 68.5 MB (68538589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8c24aadad36af251cd9bf21f434e87afe3221731362b3949ed6041b42e0106d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7616166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048981b783cc2bc2805b479186421c83a673d18f0c7f4ff8aaddaccc1c439cdb`

```dockerfile
```

-	Layers:
	-	`sha256:c118844549e4437f38e352a7c47675cf37b87544393f46164905c9d0236b7bec`  
		Last Modified: Tue, 12 Nov 2024 03:14:26 GMT  
		Size: 7.6 MB (7608893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f38ce5f76d34336732dd1258471ae700b6196172c7e61fece81d951971e0645c`  
		Last Modified: Tue, 12 Nov 2024 03:14:25 GMT  
		Size: 7.3 KB (7273 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:90e7b41bb44f0aabb12b036d985456deb388ccec89696004083da5b293198773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138325814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6bf84c04011b93921d0604ae5f4b5ff157d7ce4141958a4446f7682abc63e18`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:8ffd9575546e69884562db46178b841df2ba1ed04549599485b7c502f81ac4cc in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e3c6aca2e6ea9e1b19b3c46a60581e28de71137e5bd8fe9c8ea62365a8e75d74`  
		Last Modified: Thu, 17 Oct 2024 01:18:46 GMT  
		Size: 52.2 MB (52157899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35efd481e6347988498fa292e64d8b2f0d728f327f48bccb1d2c2bf371f2f1e1`  
		Last Modified: Sat, 19 Oct 2024 00:58:29 GMT  
		Size: 20.9 MB (20887623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10d42e894e27bd8661997e28ccc989f4b18c73e3892449a02653f995d796aea`  
		Last Modified: Sat, 19 Oct 2024 02:11:09 GMT  
		Size: 65.3 MB (65280292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0552c8f1cd92a1e8490dffddb1bdf464601603e6f79a1d72baa7fc8463fe5fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0ddef53b5b2c40e1838553c952ea8f3401900b10956137e1528e15ff24bcbd`

```dockerfile
```

-	Layers:
	-	`sha256:793454691f682b72aa95b4fbab2aa8dfbd92025fc02eebcd17d82fb50e48bb05`  
		Last Modified: Sat, 19 Oct 2024 02:11:03 GMT  
		Size: 7.1 KB (7141 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:070c7700d7f47048e9a84488481f5eeca3f322a2db8cf0063079bf0485af6022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151160749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461e9769ea2dda7d988b6bf2cf460318a930a39b684be2f7a4133a884c4eb101`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ac2d911f8489db0bbd6f313128660ffb4f315b3d99baed39d7128c198fea25b9`  
		Last Modified: Tue, 12 Nov 2024 00:59:35 GMT  
		Size: 57.3 MB (57309355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5f3e8aa1353894772b7fd9d91dc6448cf8573234fedf1ba1c8596471c52519`  
		Last Modified: Tue, 12 Nov 2024 08:30:11 GMT  
		Size: 22.0 MB (21992150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f36575664f661fb4663abf9a54ae38f6714b2f1a53511cc1ffe3d8ddb1acb8`  
		Last Modified: Tue, 12 Nov 2024 16:11:05 GMT  
		Size: 71.9 MB (71859244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e104f83870e9f99a4669b944a6bbcbebacf57fc258995d778499ee21445f42c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7627984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c47416740f5541249a4cef52d3b7e47f7681543d006c0c3ec02ff1b67bbcffd`

```dockerfile
```

-	Layers:
	-	`sha256:92fb0bcde05bbbbbd4d0f942437bf003e06cd1076856b50441ea3830631de34a`  
		Last Modified: Tue, 12 Nov 2024 16:11:04 GMT  
		Size: 7.6 MB (7620655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2a50d8c663179edf632a443d2292c19b83099aa6fc312e4f3fa057911bd68e2`  
		Last Modified: Tue, 12 Nov 2024 16:11:03 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:ab2c9935ec3cd5ea01e59c813479dfdbe44a93881633c9ab35a027bc963fbb2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137343646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b025b9611b4913fb2e9ce20401ffc0abdc8d1d1f86c8933186f6b02ff7f4c8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:9748961f840a27ae3342039309a28acc84e3a482f5ca3ece5bdaf9f92e7ebe33 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:29cf887cb660615390407db841ad4c44be2414b9bf999ba668d93a8305675c7e`  
		Last Modified: Thu, 17 Oct 2024 01:14:47 GMT  
		Size: 51.6 MB (51562685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de12fa48532c87115805a1e3efbbdd980575096676ddd00868f642d72782b610`  
		Last Modified: Sat, 19 Oct 2024 01:03:17 GMT  
		Size: 20.0 MB (20023981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c05579e9b49f41a2b6960286d8ab9b1d090127915ab4b5f2c9ec35e3db7815`  
		Last Modified: Sat, 19 Oct 2024 03:48:10 GMT  
		Size: 65.8 MB (65756980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1c2cf945f847e73794eaad19c99277f7632971602dd13cc6de4b1f441087c709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7588619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00950719b6663cf9a97df3b358162af671f7ca9b8b02fe2daa10b4ab5abc3f80`

```dockerfile
```

-	Layers:
	-	`sha256:953dc6ddab24f26925a8b0c459f5e303f3adc5374831eed917b8e26a9c0deaee`  
		Last Modified: Sat, 19 Oct 2024 03:48:02 GMT  
		Size: 7.6 MB (7581279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da3224b770b161aa53b6afc3fd6cca8fa7a8e2c13cf53415c7f406ae104506e5`  
		Last Modified: Sat, 19 Oct 2024 03:48:01 GMT  
		Size: 7.3 KB (7340 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:75798f8edcf34cc806383a3cb0d582183149dbf1634de5c038911c2d039a57db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142059552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e3c4460532df5edbadaa408870e0284979bdf475836695ee5d0a66eed35f17`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:2f1a819570e851a9bce2342f32c7927abdb02af08d5e469e6f5d41a193235bb2 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:79590eb16acf1f35f7a00e8c30e7daf7ed5d8bc9d65ff782665704f532af0ac0`  
		Last Modified: Thu, 17 Oct 2024 01:50:44 GMT  
		Size: 52.9 MB (52851981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf56c8e1a853602c0af0f40a2561d6ca90c547c99b9bdd2c5349a88e1f5cc1a`  
		Last Modified: Sat, 19 Oct 2024 00:58:05 GMT  
		Size: 21.6 MB (21639639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a7102bce19ae53b519fb58ec97dd26aadbdffdfec95cd2613f51b842e60866`  
		Last Modified: Sat, 19 Oct 2024 03:47:42 GMT  
		Size: 67.6 MB (67567932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:678287387bbebd1636e0fe5a2aeb073194add8b6f5c394616c9e1c23ce56b241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7598915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d5a40b14913c0e75a4b4bfbe1fb8e67f0bff40be7dd304d7a42dc794b6abe0`

```dockerfile
```

-	Layers:
	-	`sha256:849570392004a4d0cd1b888908893e70054109b2a9280a5ec80ecc396d7baa25`  
		Last Modified: Sat, 19 Oct 2024 03:47:41 GMT  
		Size: 7.6 MB (7591606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcaf34e81575ac3e7c8e9cb223f3661f4b719530508731fbbe38bec3829d0ac9`  
		Last Modified: Sat, 19 Oct 2024 03:47:40 GMT  
		Size: 7.3 KB (7309 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:stable`

```console
$ docker pull buildpack-deps@sha256:50daa6a4a65cbac68729b91d5d06a1868478187249e698c87a2fb6e1f7cd51e9
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
$ docker pull buildpack-deps@sha256:dfed95ded883b6221ceb01535be2c71864524606aefd9f39949acdb699e2c00c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.3 MB (349319218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd41bc93efcd7b454fddab4980d002a30aac51e898252f069988c36ca1cbf063`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2112e5e7c3ff699043b282f1ff24d3ef185c080c28846f1d7acc5ccf650bc13d`  
		Last Modified: Tue, 12 Nov 2024 03:58:28 GMT  
		Size: 64.4 MB (64391376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af247aac076473044d24960a352a8ec6f154cf0a28f4fbf35fe5d43b52687ba2`  
		Last Modified: Tue, 12 Nov 2024 04:55:08 GMT  
		Size: 211.3 MB (211293801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:88f0760f365d43d99e88c2c6c5f2efd4b604c21d71066254c3a95c591389825c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15508351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec10518bd3b236cdf9e7e299443317c4d3acea2d1d813eb18856745df0c8a77e`

```dockerfile
```

-	Layers:
	-	`sha256:84596790680ca7003b3b19983029b13d9eaca878c1b8bfb32be4d3dc30c06db8`  
		Last Modified: Tue, 12 Nov 2024 04:55:06 GMT  
		Size: 15.5 MB (15497811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6cf56ff8e4b2e1dbe2a80e23d5505991b3f7fb5386efd3ec112fe58e0de491a`  
		Last Modified: Tue, 12 Nov 2024 04:55:05 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c46a02bfc21fd7053f71092fa78fa842bbe70d7d3e8974a8f3e0d74c644ccaa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.7 MB (316656991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:978045ca96d7326e22edd7f3435c24ae52863a21d0e3c7300db1f7ffc12a58ec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:895d07844c9c09054971f530ffd0794c329a785344079a01ce24e3d51727407e`  
		Last Modified: Tue, 12 Nov 2024 00:54:43 GMT  
		Size: 47.3 MB (47338750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93efb128382700f7090be7bec74d12308eb11ced11717aae4403b7bccde20f24`  
		Last Modified: Tue, 12 Nov 2024 06:28:08 GMT  
		Size: 22.7 MB (22733304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5d34c31582cec80127fc538f65a56104fac2a20c87dbcaafc70b88f7a0a8b7`  
		Last Modified: Tue, 12 Nov 2024 11:29:42 GMT  
		Size: 62.0 MB (61996880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95228092402ee38dddb194f1bc5fef6e2e5917508ae15c94e0a077aa28cdd790`  
		Last Modified: Tue, 12 Nov 2024 13:53:10 GMT  
		Size: 184.6 MB (184588057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:068453375709d05dfab2e4f14fa04e65107704f3f15168fb7fadfc8922cbdaa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15307030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b3d2e6239bad3254d95f9349fb85402afcf4ea34b641d2c5bba65fe20ce54b`

```dockerfile
```

-	Layers:
	-	`sha256:bf286d0910d797df5b78752d6a8354956fb50cbd4a09db96b2e373c0f7358f01`  
		Last Modified: Tue, 12 Nov 2024 13:53:06 GMT  
		Size: 15.3 MB (15296422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dbd9d8c58fb1bb6415885f21668416442eec559a928dedf198c14f800323de1`  
		Last Modified: Tue, 12 Nov 2024 13:53:06 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:06bb2db41f7fbeb1ec1b7250e0bd11f1107b7c431d2089d90ced37389022d435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (301951405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d9fe338d80f977597c98ae1e707ffa5d324da2a547b20f01e17705aa675bea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7fd5031c50fee563f16760ae6e5334672d6c9ba07d159b9e3a17a3b62011`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 22.0 MB (21957404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542f68420f2ab6efd74aba4b4ff72fe115144308ecea01703acfd9de4db386df`  
		Last Modified: Sat, 19 Oct 2024 06:36:59 GMT  
		Size: 59.6 MB (59635104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad67b816dd3ebfab16dd19d0768f67e218ed3070e064a66bfa1b026ea84191e`  
		Last Modified: Sat, 19 Oct 2024 08:07:03 GMT  
		Size: 175.2 MB (175210957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0314a3678d8f3f88eabfb762a695986a02033d8fb22d77a5d6f5068b717b407c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15312390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2a075e1bcaa59170be86abde46ad32565b5db5716b6bd4e3da16477be91660`

```dockerfile
```

-	Layers:
	-	`sha256:690295df0718cc2104e887058f7a94786df16dea2499af3f048f8511ab87238a`  
		Last Modified: Sat, 19 Oct 2024 08:06:59 GMT  
		Size: 15.3 MB (15301770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d637639be757ccbf573e7b4da768bda5c46ef6deff9a9496fc6e85f0a17b9c7`  
		Last Modified: Sat, 19 Oct 2024 08:06:58 GMT  
		Size: 10.6 KB (10620 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:76778860e25ffd9449a5994b5617879cc83c194ea51d1d8f9ab1a157d3391e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.2 MB (340173078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65e32d70e63fc1d3ada53df6166c0952afb010d4eeeaf2703b3e4b858f866af0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5594266b1bacf9ad6855b00d9c5c98e721001eb115218eda673e548e04fdbf`  
		Last Modified: Sat, 19 Oct 2024 05:17:15 GMT  
		Size: 64.4 MB (64350044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d4884f85282b9a352dbcedf2cccd073a63e60b151be84375ce9279dec1c553`  
		Last Modified: Sat, 19 Oct 2024 06:16:07 GMT  
		Size: 202.6 MB (202644222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ddb4caa8d4e2a15bc8aff07048659c0464e1bd2e7d3d764a302f33abf3c24339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15536872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7b433acebb5d16e21a72e9664cc189b65f93aa069993c6093cf331dc21a67e`

```dockerfile
```

-	Layers:
	-	`sha256:8aa4d837f97e1bd618517d2b35e969ca84b0fb0999327cd9e82b934e5e8feb3a`  
		Last Modified: Sat, 19 Oct 2024 06:16:03 GMT  
		Size: 15.5 MB (15526229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7f3e5acc815d52ab17f8f3858cd0738538ffefcb45cdee80e1b80809203edff`  
		Last Modified: Sat, 19 Oct 2024 06:16:02 GMT  
		Size: 10.6 KB (10643 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c93bf79e093bc04f8c7b6197e087be2b58188acbffba4200487f158970c815ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.9 MB (351897372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20085e6d5ca38d0d5efc920deda4f2c7b7f1cc516d13009ea742ea8158c2e446`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:832e5094f1d1a0806638216e108f8c5f304112749840ba33b550928d48d45f1f`  
		Last Modified: Tue, 12 Nov 2024 00:55:00 GMT  
		Size: 50.6 MB (50577048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7251b79b00fcda89d3d742332ebf95721ed377cc22dfc14fb4cc7d2086df8c8e`  
		Last Modified: Tue, 12 Nov 2024 02:37:55 GMT  
		Size: 24.9 MB (24899410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c46592415d8ae65247d6cff038217c0ae0c38f5f2fee88eaa3f5ae09743a290`  
		Last Modified: Tue, 12 Nov 2024 03:14:24 GMT  
		Size: 66.2 MB (66211304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f62d20ad9a58cf75459d448e04c818e5c7b20e4e0a9bd426ba0fdb30a427c0`  
		Last Modified: Tue, 12 Nov 2024 03:59:17 GMT  
		Size: 210.2 MB (210209610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0d785b0b0dfdc303e5c56e4d82f2d2bcd5324e327f7369f8a74f002fa09de00d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15486902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48cdd77c324b475203dfbffac68943494c3b20562c2fd7429bf011a97c6e523e`

```dockerfile
```

-	Layers:
	-	`sha256:3a3c6d3d3ff3129f37bfb0c59da4947b5efcfd67883d5459c890df826501384b`  
		Last Modified: Tue, 12 Nov 2024 03:59:13 GMT  
		Size: 15.5 MB (15476390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9258c5560c651fe26a375f83d4a42a46cc4ebaa1259d05526d19698320d05260`  
		Last Modified: Tue, 12 Nov 2024 03:59:12 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:7f2bc5242e17eac9490e908a2be63894f0a7381dcee30ec3dcf97ffc7e9f66cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.3 MB (326336355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc411215ceea19c8d66017c4c6c30a8263150a2170118d61d0188869e4adcdc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:5fa3d47e52ee376ed002c84d34e93fe11e6db2308915238c5d7a9a5840814eda in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bf8417b2ab139177317d556c6249cee54f60148ccee016ec60d45a13a21c7c2`  
		Last Modified: Thu, 17 Oct 2024 01:17:24 GMT  
		Size: 49.6 MB (49561619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba3cc6e574320e30c42f84b70c8e03fff0393ea65f20833b10b3a8aa1415e1`  
		Last Modified: Sat, 19 Oct 2024 00:56:12 GMT  
		Size: 23.6 MB (23648020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d702889c46052954a44f8b6ab39510d9b55acfe4a180194a7cb475c90b2b76e`  
		Last Modified: Sat, 19 Oct 2024 02:08:09 GMT  
		Size: 63.3 MB (63284387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbfb08e05dc5bd87f1bd1a6b1f7e1b3b709ea1bd67292b849b2cb2c26e2e7f3`  
		Last Modified: Sat, 19 Oct 2024 02:59:32 GMT  
		Size: 189.8 MB (189842329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:61877dcc36039290e4794b30548c16e84cba90a23025191394e70b71ae1c7e34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f6b2043ca0dc4f8dfd910788dc24c8058ed42300412714c5cc8ef674411cc86`

```dockerfile
```

-	Layers:
	-	`sha256:d284443815833cb6d5b05811d4a9aeeb5999f336721792c8e9b8df2051fb143c`  
		Last Modified: Sat, 19 Oct 2024 02:59:14 GMT  
		Size: 10.4 KB (10394 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:855a926cac624799b5b29e9e12c4a338a63508a60be4531db78f1854f45fbb21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.4 MB (363387524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4970e9caeb34b2bc82b8ac0a0fa85e493b833304680e062d0ad48796f31e459f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:c7ce4329d7c0cdfb8efa822e20a44ab1922fe70e4e8be36a317ec45c565a260b in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bbeb3fa4a5ad17047af70a984a8c9e89b0702821c59cb2290ff6c49eec8d704f`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 53.6 MB (53555597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1823a3ab0dcc6f88db2bc0c18d80304ad0e6a3cad08984b6ce0a7abefd371d55`  
		Last Modified: Sat, 19 Oct 2024 00:56:54 GMT  
		Size: 25.7 MB (25705977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3666a280304f3727f745e818ab5e252dd98676495517a360e23f821dee0fa6`  
		Last Modified: Sat, 19 Oct 2024 04:07:03 GMT  
		Size: 69.8 MB (69825530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81280667d7d6fa822ac7a45807cf98017526f614373fad289bacbeb84f61f73`  
		Last Modified: Sat, 19 Oct 2024 05:17:30 GMT  
		Size: 214.3 MB (214300420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b82239446d14aa796e3669145e0e4144e317024a47609818e67ccbd29abd061b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15484578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff7ba63cf1b1fdc77923361094664727253800983f28cc61f7aad9a84413081`

```dockerfile
```

-	Layers:
	-	`sha256:865d6af4dc1d0e2e578fa465f323f0b0362de6a63a4a7ddeb009cb407518f3a3`  
		Last Modified: Sat, 19 Oct 2024 05:17:24 GMT  
		Size: 15.5 MB (15473988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c857e04d79ec517fe7bdcb6e41dd0c8e8e8f030360535d2f3ad03f299fac1efc`  
		Last Modified: Sat, 19 Oct 2024 05:17:23 GMT  
		Size: 10.6 KB (10590 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:976e837fdf70dcad33dbb610aafc511db5e9e60883e690bd7682cb21557370fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.8 MB (318783168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb932672417afb874ffa1d6dcf687e42f3012df2af781a13680c2312d984d00d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:be1cd8a5c7d60ebbe308ecf258da8f3d2dd59f7c877549c96e98e31165ba1eaf in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:510daf83b7a2b266658f37f8849eeeba99ab0f02d08ef5c1ea7f613451a81239`  
		Last Modified: Thu, 17 Oct 2024 01:50:15 GMT  
		Size: 47.9 MB (47938447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b213e07d4abfcac72292a81e546e7d80ad0bd5377b4de866c7a61ca19b5837c`  
		Last Modified: Sat, 19 Oct 2024 00:57:06 GMT  
		Size: 24.1 MB (24050397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a99db1e4eb0a57b7be4b1376a7fdf886d4118a6263595ad414d052eb69ee9b4`  
		Last Modified: Sat, 19 Oct 2024 03:46:26 GMT  
		Size: 63.5 MB (63494580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2eccbc8d9b18898de6fc12769f52101d4af82f32957d095f8ab217c6886c2e`  
		Last Modified: Sat, 19 Oct 2024 05:04:19 GMT  
		Size: 183.3 MB (183299744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ed818f64d43e758653782aa4360eb15f84ce2a0952f08c9a9c2eb514723b2d34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15320678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2d212ca9b7a5946af205d9faabe9078a4422f84204de3eff0b79a4d9c76652`

```dockerfile
```

-	Layers:
	-	`sha256:150045fb989d3aa406e6943b9a50d396ee3d83ca315d5b553f09d68b02783d8d`  
		Last Modified: Sat, 19 Oct 2024 05:04:17 GMT  
		Size: 15.3 MB (15310126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6d6b263a153d82f2f5af8d644a5c79f02fa8cf89453e0498e1e3ec099c03301`  
		Last Modified: Sat, 19 Oct 2024 05:04:16 GMT  
		Size: 10.6 KB (10552 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:41a24bb5f87a336e821481c8495904b7ccab850ddb7d3c7819c2c4e2c7fb7cb9
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
$ docker pull buildpack-deps@sha256:41e41eb5a1eb21e97dc86dcc037ad0f73605f83b56c1c73464dd1db9196a4983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73634041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0afb2b1893cde96efc8d8210faaf240bf974567fcffc52c897c2f3c7dc9d79e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:986d0095b9a0c1ba3301eb55fd09b2d313291d46eb689d40f40ba5e22fe89c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4372469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d2308a6a913223982e9855dd8579b6c1952e064d55b55df3b488871308faebe`

```dockerfile
```

-	Layers:
	-	`sha256:ecebc53c12ddd3cdc651d3ac8588af340efb560dfff14086c45f26e4a6845d00`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 4.4 MB (4365306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b27611db305d9c1eaa6265accc831e7dd709d1ce5a580841bed26a4b03073d79`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 7.2 KB (7163 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:8e3fafd00e93960e28affb776bf24b68be5f16c8ae8264d6512d64e04638b301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70072054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ae47018992349a5e2058c7afa3cbbfad33c53a796b526639fdcbc544a232dd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:895d07844c9c09054971f530ffd0794c329a785344079a01ce24e3d51727407e`  
		Last Modified: Tue, 12 Nov 2024 00:54:43 GMT  
		Size: 47.3 MB (47338750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93efb128382700f7090be7bec74d12308eb11ced11717aae4403b7bccde20f24`  
		Last Modified: Tue, 12 Nov 2024 06:28:08 GMT  
		Size: 22.7 MB (22733304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5e697f44f82c828c459781743ae81c1b1fa2efd11d0ef16c315af40a6bf46a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4376053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29044c644def0ce321a888bed6b2e6a887e065d64284048b8cefbfab2415ff06`

```dockerfile
```

-	Layers:
	-	`sha256:0021462fa99eaa3af9d3f7856d66255747ce9d86290f0a67360aad6258734a1d`  
		Last Modified: Tue, 12 Nov 2024 06:28:07 GMT  
		Size: 4.4 MB (4368821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ccdb91b8a0e2609fdd39cee4ab8cac4e44254f455c3f6e89719b35df75eed9c`  
		Last Modified: Tue, 12 Nov 2024 06:28:06 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4df85825662d4ccaf0c53f0b0f706602fca0555267dd2d31a62e8ef87e1d558d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67110580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b88071c4591f6c7f807b8cad4c84e19227e69998bf7945120dfc8071b9014f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:46618ec96098836cac7950050ba554a969ebf8e9938d85d5f0d97015d3d25076`  
		Last Modified: Tue, 12 Nov 2024 00:56:14 GMT  
		Size: 45.2 MB (45150563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9660b2b46aa0c77f5dd078f4e57432faf3dbcda91672b9e3f8c1b7892e0ee2`  
		Last Modified: Tue, 12 Nov 2024 15:59:18 GMT  
		Size: 22.0 MB (21960017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:305784099f58635cead38aa11453521226000d86d85d52ee7848ca2c3be385c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4374834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8010ae6e055d2fc8797a75c67215cd400f64870bba5fb87b2503a4bb2fd1ae`

```dockerfile
```

-	Layers:
	-	`sha256:54c117e288564eb3719195c06d6bc879daa602feb6e27a0feb1a1ec9e18bf464`  
		Last Modified: Tue, 12 Nov 2024 15:59:18 GMT  
		Size: 4.4 MB (4367602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fcbbc798229c876fdfad98f81fb68cc54fb00ac95a2c847e9e133d91ce28ce3`  
		Last Modified: Tue, 12 Nov 2024 15:59:17 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e46fcc0c7385b7dccc516a32fb6dfc4d75a18dc39b9963b799d0cc2425554da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73185454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93ad60e192318acaeb45178aa2a8ced73c3b5c2075f1d0909094e482012ae304`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464f864cfaa846fbe1b8a889827404e18374f805d29d77c288a813ae8c4f6d91`  
		Last Modified: Tue, 12 Nov 2024 11:16:03 GMT  
		Size: 23.6 MB (23598253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7f238c1fe83bd003f1036848cda78a6c3cf076fcbed76560d0c41ed12edf3889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4372832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e335a8c4a64c4e0fae9e376895c95ac74dec942b688c1d5712b76326b89a71f`

```dockerfile
```

-	Layers:
	-	`sha256:a0d5ed8ce9f0036a2700ad927fefc558470f78b81f0b62876e96ad9516c09e17`  
		Last Modified: Tue, 12 Nov 2024 11:16:03 GMT  
		Size: 4.4 MB (4365578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3af911d4ac8fc50b9625684b9dfc26cb7861e3d51df952fe066d4eb1c8f230a`  
		Last Modified: Tue, 12 Nov 2024 11:16:02 GMT  
		Size: 7.3 KB (7254 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ac574690768b372f5dffd3fdba2f1316b68ee58133eada25d6f76b945c3503ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75476458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec174eb03e66f601edeb0488058e18636473d68377651065577803c0ac3d03f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:832e5094f1d1a0806638216e108f8c5f304112749840ba33b550928d48d45f1f`  
		Last Modified: Tue, 12 Nov 2024 00:55:00 GMT  
		Size: 50.6 MB (50577048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7251b79b00fcda89d3d742332ebf95721ed377cc22dfc14fb4cc7d2086df8c8e`  
		Last Modified: Tue, 12 Nov 2024 02:37:55 GMT  
		Size: 24.9 MB (24899410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d746769d0ce07c638d82090c56538afac5862001d98ec7ae5b23ae300ec87e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4369499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1441e57a6c764c8c7ccd95b08a608a908f3a9b0e5c6b666386e59faebc024b53`

```dockerfile
```

-	Layers:
	-	`sha256:8f720d960686e4104e12b5daa17252fea926f0989e5e2d35e3b5ace686835b71`  
		Last Modified: Tue, 12 Nov 2024 02:37:55 GMT  
		Size: 4.4 MB (4362362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce198488c58998d3efa8241e574d30337efbc03936c45f6efd2f314bd790083f`  
		Last Modified: Tue, 12 Nov 2024 02:37:55 GMT  
		Size: 7.1 KB (7137 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:de1a2b9066af1286e9d8175eef66425cfbddc0251cbdc6e6263a68b742ee6437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73211352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b5e3786aaeddd9bd8e5b8cd2245dc5be46353f3dbe4aa169166a83607577e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:17191dc8a469e4ef93330c5c8402fa0c0761218a5fa02ad2db7b34508d0e995c`  
		Last Modified: Tue, 12 Nov 2024 00:57:16 GMT  
		Size: 49.6 MB (49559181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf888157372a89189e8193ccb502b1003341993a439a6f526f90dc05a6100692`  
		Last Modified: Tue, 12 Nov 2024 18:00:45 GMT  
		Size: 23.7 MB (23652171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ee37e62e2a4f2b37b5059c26f65c50e79e8f12bede1551fe7c38dde1371e0e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 KB (7005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087a573000fee443714e51f8a22272ec23d27c5ef680d3b9f288f8ea41e63a91`

```dockerfile
```

-	Layers:
	-	`sha256:36da5312bc8de97460d5ca2df24b0a099c7af0db6158b101c163700559263cd6`  
		Last Modified: Tue, 12 Nov 2024 18:00:43 GMT  
		Size: 7.0 KB (7005 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:466f233ffc3b8ce8fc8e24fe4e0a478f467ee9c1b9e07ccaabb6d7f4dd82b50e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79272813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8258da2a3b826e8087b187be36e101338667cc4c8f4296ef4b30bf4867d89e8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9170cd93e372271efe7b34bbee8de26bbb094efba80a15cff49f580f87e5fe40`  
		Last Modified: Tue, 12 Nov 2024 00:57:37 GMT  
		Size: 53.6 MB (53555270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92051d5a3f7afdf0c89db06ce83fb963b8719a7024153e1520472673570e9d51`  
		Last Modified: Tue, 12 Nov 2024 08:29:09 GMT  
		Size: 25.7 MB (25717543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2238f5c37875dcd6505f74cd1d75fcbb33c40ab59512d84b295b8205ca2a6912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4377001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a107c661e17348313475322db42ffce8541848e8dd47876d57a3062cd14c027`

```dockerfile
```

-	Layers:
	-	`sha256:f1df1624c9d126aec722784a58ffe81fe99f97613ee2061a4ec42a2636a26b04`  
		Last Modified: Tue, 12 Nov 2024 08:29:08 GMT  
		Size: 4.4 MB (4369799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18a16b8c21a8a4d843e70acb35845f9570090375bdc2418cb56cbc1f86835707`  
		Last Modified: Tue, 12 Nov 2024 08:29:08 GMT  
		Size: 7.2 KB (7202 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:556f5aa74f180a341fe894576c8df3a358c7ad6432d78efbbc0da3bb71f523e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71996571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cac9802c1503429c3afb4b5bcf9abbc62bf5678126c5a817806438584d76da7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9f9f8fa8b12064144bd5037b70d4d9ac4fcbcd94f2921feb1e017764a273f798`  
		Last Modified: Tue, 12 Nov 2024 00:58:23 GMT  
		Size: 47.9 MB (47938688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53b034664a3d7aeeede4479f8aebfb2fff094119ae93ccf99e62d557e92b31f`  
		Last Modified: Tue, 12 Nov 2024 09:01:46 GMT  
		Size: 24.1 MB (24057883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b5638e5d412c4935cdb5c941063892a1c760db5bd429ef01755d419da71ac16e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4372167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7196d3bd3ce51a1e06975a87f93ccac12d11dcde272e5ea99e71a63a7bf9d9b6`

```dockerfile
```

-	Layers:
	-	`sha256:86a46b41b61f05b5bf553bb19fecd56edefa4c046740d61578dbcfda5746f13f`  
		Last Modified: Tue, 12 Nov 2024 09:01:44 GMT  
		Size: 4.4 MB (4365003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63952b86a5ed4c59bfbf8d5f3f31a85aed5da9a9298e45cbdcf514945aedb636`  
		Last Modified: Tue, 12 Nov 2024 09:01:44 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:stable-scm`

```console
$ docker pull buildpack-deps@sha256:234ad1de0c6bd8ae1024516f64646becce5040299546d61dce815cb7ec74454d
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
$ docker pull buildpack-deps@sha256:6fbde97d2c5f38678ecc77dba69ae37004e01c5fe1060195a6fa0a03a166b6f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (138025417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:408d444d56480b9093884d1bd6088cbd039fc990d5bf1507bd57a0e13bdd3a33`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc7b6f04730c072f8b292917e0d95bb886096a2b2b1781196170965161cd27`  
		Last Modified: Tue, 12 Nov 2024 02:38:12 GMT  
		Size: 24.1 MB (24058346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2112e5e7c3ff699043b282f1ff24d3ef185c080c28846f1d7acc5ccf650bc13d`  
		Last Modified: Tue, 12 Nov 2024 03:58:28 GMT  
		Size: 64.4 MB (64391376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d933d77fc474f2f63922bf70e05b7ea0af809991a3e5cb05967accda9f937dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7772096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5efb1b53407bad0cf8f47b0a1d54a6a9e90a27ae1c86a6a6de8f9bb3c8cc85c3`

```dockerfile
```

-	Layers:
	-	`sha256:b6f4689c52467b37f8370b7c0f6ac7fb405ab637e983b4ad7353590dd0a8a2cc`  
		Last Modified: Tue, 12 Nov 2024 03:58:27 GMT  
		Size: 7.8 MB (7764442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91abd18c81a94564d4a7151834429ae9fbf19f28c3a4e2937046f1a765ce3039`  
		Last Modified: Tue, 12 Nov 2024 03:58:27 GMT  
		Size: 7.7 KB (7654 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9a1f00aee35fdbfc3bbef35f7b430afe4b7d61335911b8ca883d4ee277540158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132068934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28e47e232c9eb35167cfd394f5c0f26dd9550bca5ee8ac3a7fb762992cd8e96`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:895d07844c9c09054971f530ffd0794c329a785344079a01ce24e3d51727407e`  
		Last Modified: Tue, 12 Nov 2024 00:54:43 GMT  
		Size: 47.3 MB (47338750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93efb128382700f7090be7bec74d12308eb11ced11717aae4403b7bccde20f24`  
		Last Modified: Tue, 12 Nov 2024 06:28:08 GMT  
		Size: 22.7 MB (22733304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5d34c31582cec80127fc538f65a56104fac2a20c87dbcaafc70b88f7a0a8b7`  
		Last Modified: Tue, 12 Nov 2024 11:29:42 GMT  
		Size: 62.0 MB (61996880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:146afff14da66d2415f7e870a0b5475327d3b8c5c3012e0e73e9929ce55432aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7773719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1139b21f47128807aca40d8f91d82ce8acf1684a9f67bba7bd10747e93444a31`

```dockerfile
```

-	Layers:
	-	`sha256:e5dc3d0311f5fe151c6c570f37bed7153cdc58ca55dc3f8244a7b0463ad6f4b5`  
		Last Modified: Tue, 12 Nov 2024 11:29:41 GMT  
		Size: 7.8 MB (7765996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3878cd87f19cd6baf6f4baacf94bb729da9783cc7ba94a83e2575efb914f143`  
		Last Modified: Tue, 12 Nov 2024 11:29:40 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d8da1a84da0bff207409bbac38dd1a02df0945b14ffd1fa2e34036a968789458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126740448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11391af0d1d3a25dfc5836b449c838b6faf132d3b8f3207da24d749b265ef353`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7fd5031c50fee563f16760ae6e5334672d6c9ba07d159b9e3a17a3b62011`  
		Last Modified: Sat, 19 Oct 2024 00:56:10 GMT  
		Size: 22.0 MB (21957404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542f68420f2ab6efd74aba4b4ff72fe115144308ecea01703acfd9de4db386df`  
		Last Modified: Sat, 19 Oct 2024 06:36:59 GMT  
		Size: 59.6 MB (59635104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:82abbe189e4134358a35de062d14a33ab4ef2350f5335ed22d488f490c39e3f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7773386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a185c3d89851dea1a6599e78d946fb300c3e2ee6fe011b211285a182fc5e834`

```dockerfile
```

-	Layers:
	-	`sha256:f581eedd8301e57f012174ed44c98b695ef71465963ae45671ac92102a1eaafe`  
		Last Modified: Sat, 19 Oct 2024 06:36:58 GMT  
		Size: 7.8 MB (7765651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcf5b6a5be36ea85b8ff05143189e2f676d385b38504343c20e9f59dc37a002e`  
		Last Modified: Sat, 19 Oct 2024 06:36:57 GMT  
		Size: 7.7 KB (7735 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1b238ddfffd81f1788a7575612d8a052bad65a59129adf13b225091a1f798575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137528856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c89ba4d07f4ae3ae3debaa56c19ea06e7c0b9d2773c56679e3399263fadd9488`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5594266b1bacf9ad6855b00d9c5c98e721001eb115218eda673e548e04fdbf`  
		Last Modified: Sat, 19 Oct 2024 05:17:15 GMT  
		Size: 64.4 MB (64350044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4ae890e89350690ad59722f03f334f49def59e9a7a1b4eb60f59e60964f978fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7778540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ce0978485db8f8cd9635afd0ac7fc48b931593fe09f24a19d60b0d76c4e639`

```dockerfile
```

-	Layers:
	-	`sha256:5be58f0330ad5ad6c6e1439539fff91b3e586695d4806db0cf17398a4ea80ff7`  
		Last Modified: Sat, 19 Oct 2024 05:17:14 GMT  
		Size: 7.8 MB (7770781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd7d4cdd0c303535f95e2806de4f42d422c025d70f90f72882a1301f380aa64`  
		Last Modified: Sat, 19 Oct 2024 05:17:13 GMT  
		Size: 7.8 KB (7759 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:3a9a1cd1d4fc50ae45994fcf166dd95bd945fddb91781ffb82b09f84b8d70daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141687762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de9bf2a38fcbf043555508c597839677889c027dfa88e84f35a66f1493b14a2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:832e5094f1d1a0806638216e108f8c5f304112749840ba33b550928d48d45f1f`  
		Last Modified: Tue, 12 Nov 2024 00:55:00 GMT  
		Size: 50.6 MB (50577048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7251b79b00fcda89d3d742332ebf95721ed377cc22dfc14fb4cc7d2086df8c8e`  
		Last Modified: Tue, 12 Nov 2024 02:37:55 GMT  
		Size: 24.9 MB (24899410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c46592415d8ae65247d6cff038217c0ae0c38f5f2fee88eaa3f5ae09743a290`  
		Last Modified: Tue, 12 Nov 2024 03:14:24 GMT  
		Size: 66.2 MB (66211304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d29c3a56480553061917153ef4826fea0ff6b84616cfc7a020c1682e578f5c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7768146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23a9925b36e8fa4b0eddfc89cf9f299ae4e6da2ab487e270d5483829a67266f7`

```dockerfile
```

-	Layers:
	-	`sha256:21211546a412a59b68e54a0883d6e64098cc26325b2fac0f05cf5b94ab27c266`  
		Last Modified: Tue, 12 Nov 2024 03:14:22 GMT  
		Size: 7.8 MB (7760518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac6f9f590da617c7f5124adbdf5cc841c3d0456606c3d5617a33a51ecf792f53`  
		Last Modified: Tue, 12 Nov 2024 03:14:21 GMT  
		Size: 7.6 KB (7628 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:cadf76ca0578af7d2c32dce3d1860f04b28959bb1cb0f27e982288bba02c972e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136494026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0434755538859a36858a1cf943ffb9a3464378e9371f90644cb583fdfeefe551`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:5fa3d47e52ee376ed002c84d34e93fe11e6db2308915238c5d7a9a5840814eda in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bf8417b2ab139177317d556c6249cee54f60148ccee016ec60d45a13a21c7c2`  
		Last Modified: Thu, 17 Oct 2024 01:17:24 GMT  
		Size: 49.6 MB (49561619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ba3cc6e574320e30c42f84b70c8e03fff0393ea65f20833b10b3a8aa1415e1`  
		Last Modified: Sat, 19 Oct 2024 00:56:12 GMT  
		Size: 23.6 MB (23648020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d702889c46052954a44f8b6ab39510d9b55acfe4a180194a7cb475c90b2b76e`  
		Last Modified: Sat, 19 Oct 2024 02:08:09 GMT  
		Size: 63.3 MB (63284387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:821b714bf8d6778d6d1b920a2baace275ae17c38d2e45770d4702d64b3d8634a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae759b8a8a22e7725a44091355ef141327e65f7a7442e018dfb5b90b94cf0cce`

```dockerfile
```

-	Layers:
	-	`sha256:7bab8cd7f7cc5b0a4b903dd7d23a799c7767e8dec89874cd1de2cc7ac2343c85`  
		Last Modified: Sat, 19 Oct 2024 02:08:03 GMT  
		Size: 7.5 KB (7509 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4a4289d5bc6db05198984f4e81697f55cc0d7ac6720bdcbdb13af2b5b385c231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149085096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3875cb156e725ad37ee97b98abf0f972f2ac10c4ff305204b30071a468158a4f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9170cd93e372271efe7b34bbee8de26bbb094efba80a15cff49f580f87e5fe40`  
		Last Modified: Tue, 12 Nov 2024 00:57:37 GMT  
		Size: 53.6 MB (53555270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92051d5a3f7afdf0c89db06ce83fb963b8719a7024153e1520472673570e9d51`  
		Last Modified: Tue, 12 Nov 2024 08:29:09 GMT  
		Size: 25.7 MB (25717543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913acd64029d37b20e9e161bb8659516cb78a99cfd56eb921fc4ccd76ae7c0c7`  
		Last Modified: Tue, 12 Nov 2024 16:09:31 GMT  
		Size: 69.8 MB (69812283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c21374c30e5f547aa9e66b04b1997909f699921da61d213ed3fb3d2a7de64c0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7779842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a315c2156e595de5e483e597dd3ea85ea0533d0e98f410011d7326f27679968f`

```dockerfile
```

-	Layers:
	-	`sha256:d9c5acd4f7b46ec0c9c2839752d6be8030b1bcc4d58b67483ad71a717d9899cb`  
		Last Modified: Tue, 12 Nov 2024 16:09:28 GMT  
		Size: 7.8 MB (7772149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1014f338054fa217964a7cd584f29304bb70ac47f3c759f554c010e2b966ee4`  
		Last Modified: Tue, 12 Nov 2024 16:09:27 GMT  
		Size: 7.7 KB (7693 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:029bcbdc4d92b810548bb6fe4d4a5d4fed99197e43c6a7cf1366a8d78db2c8fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135483424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ab4b43343266a1cc583fb48be5a34866624b123c7e48c1a091011da24be0f2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:be1cd8a5c7d60ebbe308ecf258da8f3d2dd59f7c877549c96e98e31165ba1eaf in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:510daf83b7a2b266658f37f8849eeeba99ab0f02d08ef5c1ea7f613451a81239`  
		Last Modified: Thu, 17 Oct 2024 01:50:15 GMT  
		Size: 47.9 MB (47938447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b213e07d4abfcac72292a81e546e7d80ad0bd5377b4de866c7a61ca19b5837c`  
		Last Modified: Sat, 19 Oct 2024 00:57:06 GMT  
		Size: 24.1 MB (24050397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a99db1e4eb0a57b7be4b1376a7fdf886d4118a6263595ad414d052eb69ee9b4`  
		Last Modified: Sat, 19 Oct 2024 03:46:26 GMT  
		Size: 63.5 MB (63494580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ecf9164fa7d6fe0f7178e89f1831c99d40d886c359e875262bf5d2f7fedb45bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7771243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8b973ea0fea3dbb11fa12a9b53632b91fca04c49806d2caf99693e37c78d69`

```dockerfile
```

-	Layers:
	-	`sha256:6e7b6cf839452bb8901601f821aa42480d98fc226c60373c907ff55920f3d325`  
		Last Modified: Sat, 19 Oct 2024 03:46:25 GMT  
		Size: 7.8 MB (7763576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ad6de2140fc403088cce711e23a06bd50be647583ddfcdda8b53b2134309157`  
		Last Modified: Sat, 19 Oct 2024 03:46:25 GMT  
		Size: 7.7 KB (7667 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:5413e56f36811f5d5634b0a0f23944df58b3536b3a54ca3fe2c21ed2adc784c9
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
$ docker pull buildpack-deps@sha256:7cbe3791c734ad4570773a958b63e1371d045a3aff24011c5716ccfadeb65a08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.0 MB (368973816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7703f03776d03820bc730c7ba4a1357b289a3c1e5cd0d41bab150afffe8d752`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:723f7d6ce61509bbccf2af45aa75a4c5cd83b188d6e85822321cdc68268417bf`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 53.2 MB (53226763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1538514cb923497c68c854e6f9e45945ca05f4a0f5a179472e7f81b1ee0cfbb`  
		Last Modified: Tue, 12 Nov 2024 02:38:24 GMT  
		Size: 20.6 MB (20597910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa039132691ce2d5258743dd8ecefd941d85955a38506ba77c3fb6d2f554298`  
		Last Modified: Tue, 12 Nov 2024 03:18:08 GMT  
		Size: 66.5 MB (66531021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c24554062853c5674b963d550e30ca0a757e9eb981889481f056f908bfb85e`  
		Last Modified: Tue, 12 Nov 2024 03:59:20 GMT  
		Size: 228.6 MB (228618122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fde6ad638d3489c2565f8fd9372ea5a582fde062402076e49c07d546cbce9f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16694153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af1b4e4371b4516fbe01c132347fd12fc0e48c4c84d419d3f4d87a1585cddc59`

```dockerfile
```

-	Layers:
	-	`sha256:ecac10a1f2388f1010f072658b62094485c4427f64b84a05b42df2b85a715e3d`  
		Last Modified: Tue, 12 Nov 2024 03:59:17 GMT  
		Size: 16.7 MB (16683960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5443e4fb350c11c56dd93b8946e2d787d3ec950b1cf9ba87f19e87f295b7e40`  
		Last Modified: Tue, 12 Nov 2024 03:59:17 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:bb3cf03abb1e11b70090a8ca17faf8d5f6e9af798e64c8fbb6cc6fce6b7c67a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.3 MB (337265046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e60b6a1fbca262eafa40df4cd4c57a7f24721394b8bcc7556c626b414caa1c5b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4ff391534f557bd19067799d6e6b7e386e43cbf7d061a795a182546eb2145e99`  
		Last Modified: Tue, 12 Nov 2024 00:58:57 GMT  
		Size: 50.1 MB (50091523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d129d70e5af0f50e5354ff02342f42eba97458b43a0df2209f72566f664a4a`  
		Last Modified: Tue, 12 Nov 2024 06:29:56 GMT  
		Size: 19.6 MB (19607774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a342b984b6752601eb44f7fa9cc6f866d747d925571f5c63f8db143a85f2fc46`  
		Last Modified: Tue, 12 Nov 2024 11:32:48 GMT  
		Size: 64.0 MB (63966009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028167967e0788114dab10f0fa1afeca8ecbb50011cd2627a38462981e159174`  
		Last Modified: Tue, 12 Nov 2024 14:00:43 GMT  
		Size: 203.6 MB (203599740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1284c8ed67cf389d2a9f9ff026521d12046ee702bad2602fb6536d2689ec86d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16486074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c884655403838f628e98896e91e34a18dd06a0b51f0c1c370e20e732bb864e15`

```dockerfile
```

-	Layers:
	-	`sha256:53c9b04be44740a94267bb9e60dbcd57098849e3b57e866add59c69ab31bdde4`  
		Last Modified: Tue, 12 Nov 2024 14:00:39 GMT  
		Size: 16.5 MB (16475821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85e24f36060e6aee12a7007f4582acdc6c5bc92b806e1c824b5b78c1f596e1e5`  
		Last Modified: Tue, 12 Nov 2024 14:00:38 GMT  
		Size: 10.3 KB (10253 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:43decaa0c198ea49c25e0579b8e4459dd1eccbb162c2f3b3cf60c5f105c30532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.8 MB (317793004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e5bbbfe2db111d7c0a74257c7e0efd4390af8f93f7a297fced39742d6fee01`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:7b183110c42f24584c122a8e76db1e925d5fd8b3489ae273dbca0b0cc3bc0090 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a5589eaa1616610f1da5585cd04faf9e418fe913dd4e9ef827abdbe93f8caa5b`  
		Last Modified: Thu, 17 Oct 2024 03:10:29 GMT  
		Size: 47.7 MB (47659640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a052304c7554ffebe70b582d4e2eb7d1d61098f5f96c8c9603940278d081561`  
		Last Modified: Sat, 19 Oct 2024 00:58:30 GMT  
		Size: 19.0 MB (18971211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfcca10ec23fe707cc08f7ab790838065704861f60c0f678095482cc25ef593`  
		Last Modified: Sat, 19 Oct 2024 06:40:45 GMT  
		Size: 61.2 MB (61228559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b8715cfc77ca9de75ae3a4c97787dddb260f81e6774113adb34eeb4df9fbab`  
		Last Modified: Sat, 19 Oct 2024 08:15:21 GMT  
		Size: 189.9 MB (189933594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:201e31e97b8198b5b73245292db7ee57ccbcbff11baedb28f3c8716c3712a460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16305861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e54ca52b2d36a1153fe982f6c91426c036c1c8752aefa37315bbb6ae468eca`

```dockerfile
```

-	Layers:
	-	`sha256:db8b42ad1f6e5f980314f108470f162b14dd14f2b57c0eb4a15526b533e7ffc4`  
		Last Modified: Sat, 19 Oct 2024 08:15:17 GMT  
		Size: 16.3 MB (16295596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1dd62a0b90c1f4d9670edefd460b2729d71461a06b59b621e01e0e5c090f59f`  
		Last Modified: Sat, 19 Oct 2024 08:15:16 GMT  
		Size: 10.3 KB (10265 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4ae9574eaaaa819eee22d771b30ecfd1b6a61732dfedf09f4d626004b7756023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.7 MB (361701064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcbbe0de592c14b77f79d5364ba45b6b102a8f12377baa10181a3daeae528fa0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:5d91cfda460a83c91802e918bddf6951978599b67dbd5e3c0a492a53f20d6ad6 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6f4ac25c892a8a547634a70e67af9f356a5f2b1f34e7c78d52074f2a21999111`  
		Last Modified: Thu, 17 Oct 2024 01:17:18 GMT  
		Size: 53.6 MB (53599725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b74f65518d0117b47b1d80b0bf8981ebb7ddb04cdeeadd261af699b6e5d50`  
		Last Modified: Sat, 19 Oct 2024 01:12:15 GMT  
		Size: 20.4 MB (20382473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b125c1d7d6d0668d3d31049e15ed26c5f15741a45a407eab00423ec50972be12`  
		Last Modified: Sat, 19 Oct 2024 05:20:09 GMT  
		Size: 66.3 MB (66298697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd09379a59f4bf2683bfc63736559fb02ca078899a46853d3dbb50955d6ce02`  
		Last Modified: Sat, 19 Oct 2024 06:21:51 GMT  
		Size: 221.4 MB (221420169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a5e44adae95a33c8855a957d37239c524418aa044cf210b118df590bc5c617ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16604076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53d6fdab1445139470616a1ba7e76135d8184f2d94c3e977392d6f83c93cee3c`

```dockerfile
```

-	Layers:
	-	`sha256:49838c80534b422aa73f107fe50cea0e08b56cb8df4bed441762f4c6fc8da938`  
		Last Modified: Sat, 19 Oct 2024 06:21:46 GMT  
		Size: 16.6 MB (16593791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:130ddeaced8e30940ccc1ba76f5f1b1037cbac31ce7fb4fea621f464b45b9969`  
		Last Modified: Sat, 19 Oct 2024 06:21:45 GMT  
		Size: 10.3 KB (10285 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:13a5f075e4b03beecdfe160afa42b8b6109f2e26e8e33707314cef4940012410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.1 MB (374066765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43bc8c18b13cac0f90dc06c003982716d8f2c3d57540c4dd475cd2bf2aeb0768`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a04f0591b5521dc9360454fa2fd6b21d9b7d989bb4c88327ad94f8282af3b267`  
		Last Modified: Tue, 12 Nov 2024 00:55:13 GMT  
		Size: 54.1 MB (54095157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914cc5c9bed5c786b85a6e40864cd3fb4af442dea3455ca88a01cfa26707d8df`  
		Last Modified: Tue, 12 Nov 2024 02:38:04 GMT  
		Size: 21.7 MB (21722460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c207d20a70d18f9e95ac6b10fd58bbc5d2a036845c50cdab8e2fa983066a990`  
		Last Modified: Tue, 12 Nov 2024 03:14:35 GMT  
		Size: 68.3 MB (68343373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2790a8863dae4d5397c7a550a69104b8b23dcb717967ee6e4eaadfbb1e2b031a`  
		Last Modified: Tue, 12 Nov 2024 04:00:28 GMT  
		Size: 229.9 MB (229905775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ca9a1ae52fdac26a890763e00bccfb82d42e7c8eb0f3b6d31f79942c3f9a34e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16663809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:283d90ebc233386f9ee9c40e4a432225230f776486c2e00d3fd2ad23d5160970`

```dockerfile
```

-	Layers:
	-	`sha256:d3892b08125fc65dd00ec24cf04745b40b69e5b08348457ba04c1bdb60167dbf`  
		Last Modified: Tue, 12 Nov 2024 04:00:24 GMT  
		Size: 16.7 MB (16653639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84ebaf548cb0955edc73a8e3008964cb55db8614f1c4e3ca7733ffebe47caccf`  
		Last Modified: Tue, 12 Nov 2024 04:00:23 GMT  
		Size: 10.2 KB (10170 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:2d79e8b7e96fe38d9e45a4d282bd0f95d67001a444552087bd3cc32f25d08084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.8 MB (345787888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56875b7a504b29b2bb3123f42f536d1f78dc908550e86383f2d6486887d1a44`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:7540ed5b693bb419df5aaa69483f55c19bc0566d076c5e65757a0a6fe38375a3 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bd6795a0a311ac784071ff263d2b83d646956234334d40fe908b91a1dde11378`  
		Last Modified: Thu, 17 Oct 2024 01:22:22 GMT  
		Size: 52.1 MB (52128468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bde6977c24ffe15c007c6606184010ccb92606e6158cbd76d8e770997debfa`  
		Last Modified: Sat, 19 Oct 2024 01:01:31 GMT  
		Size: 21.0 MB (20966640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdea9feeed917171d6d06a6129bb34f0f75c8fdb0fc8f9755f248adca6eee285`  
		Last Modified: Sat, 19 Oct 2024 02:14:28 GMT  
		Size: 65.1 MB (65056004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64eacd2dd173c3ffb6f366cf5087686edf0379bf94a7576a971e2b52513c8882`  
		Last Modified: Sat, 19 Oct 2024 03:18:15 GMT  
		Size: 207.6 MB (207636776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:25e904418fdd672b948405e1f14bcb5c092286565f8ea58f426a76778aedf70f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce2990a7740c1ee661056d1286c412d9aa033ccfad23335960773e59e4582da`

```dockerfile
```

-	Layers:
	-	`sha256:529b4851b6d08464af5c7c7f70b64a67057dc822143fa9cdf853e9719b9b0d5f`  
		Last Modified: Sat, 19 Oct 2024 03:17:55 GMT  
		Size: 10.0 KB (10038 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:fb2d0b8252543fd9aac6afd2358f8c036517399d15ab671d2c26238bf25b8817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.7 MB (378675496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2934ca0774acb5c953ccff3f166b5c11443c95326cb52e98f91e9aa4cb675ae2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:7d34de8e15cda6686099080e64714532070b3d06a451fa9d77a5716745974490 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8299bac21377f71d4bbd00f3075290f241c45c39e6a9a76012dbff5b62d14e88`  
		Last Modified: Thu, 17 Oct 2024 01:23:55 GMT  
		Size: 57.1 MB (57126645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739c73c116650c722a140d5e98dc4d5b306e6daaa1f611e7f00699c828890445`  
		Last Modified: Sat, 19 Oct 2024 00:58:55 GMT  
		Size: 23.3 MB (23314858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888fc73ea70716bfd3afc5289dca8e001895bc72345d7defb80ef4274358afe4`  
		Last Modified: Sat, 19 Oct 2024 04:10:18 GMT  
		Size: 71.6 MB (71620992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e85c4c362f2752b90470a2e9c73e4b582008ca3b0314740e6a4e1c756cc08f0`  
		Last Modified: Sat, 19 Oct 2024 05:24:17 GMT  
		Size: 226.6 MB (226613001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bb68d7efafd7d984c6f1b48c59077419faf23c6d84bc1bacccfda22722f3d873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16505785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07402716cde3edbdad9c0a69eaa180c73b700706e17afbcf700e741832b7c2d3`

```dockerfile
```

-	Layers:
	-	`sha256:4b95db3e2321004c462504333af6b67a31f8bf670842e66a4656832a64ce8ec1`  
		Last Modified: Sat, 19 Oct 2024 05:24:10 GMT  
		Size: 16.5 MB (16495548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26c87f6f72bd68371ce1cee3cc527c15b062c2dba5a32da15805811213cc92cc`  
		Last Modified: Sat, 19 Oct 2024 05:24:09 GMT  
		Size: 10.2 KB (10237 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:64db136082af530566b7ed8329ddad4bb6bc67827f9ed7e770fb7c7d363aaa30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343151504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b638beec4f55aadeb0294811090591f2020966a01e0943d5ce76f0a912864f80`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:fe7c88cb45fa7097d71f60ba00c0d6ad76dd030e8e34771e5ee3735b59a4d6e6 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:53440987c87b8deb9090e5298bf822ffc945f186eb4c81cecc0ebf58717ca549`  
		Last Modified: Thu, 17 Oct 2024 01:51:55 GMT  
		Size: 52.8 MB (52808844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3816f9124671541da45f7e11a0a925de47e719482f5bcd085247ecdcb8c613`  
		Last Modified: Sat, 19 Oct 2024 00:59:12 GMT  
		Size: 21.7 MB (21656188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cc2aa2fcdc4addb1b596c3dbc6f3699d60107644fd49f54f3050356c21437c`  
		Last Modified: Sat, 19 Oct 2024 03:48:52 GMT  
		Size: 67.3 MB (67332572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc706768a06fa9cf16504e13939b12c91809de8a89473cc7b793fbce1b5adb60`  
		Last Modified: Sat, 19 Oct 2024 05:09:06 GMT  
		Size: 201.4 MB (201353900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8964bba7c715a5e8f0de47782dfc27bfae53b34e72337817658a05402ea8c5fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16298751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de39e96e1289fd9ad90558f1d9bc9ba89833a4dc736aa81a7d1eec6e72ae985a`

```dockerfile
```

-	Layers:
	-	`sha256:2e89bddb8da9917b83fcd1c1c9cd13cb701e559da0f070b1b66e91712318f5db`  
		Last Modified: Sat, 19 Oct 2024 05:09:03 GMT  
		Size: 16.3 MB (16288548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d292472b39d06e2e9473e3ce69b1cd5133a331271d388009a134a30414dbc91`  
		Last Modified: Sat, 19 Oct 2024 05:09:02 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:ab834ad536df5563da2eb202fbf667204c33c7c69f3e9d455af94182feef8593
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
$ docker pull buildpack-deps@sha256:2c9dda7b58f3cc1b6b5e844de7f661770af7817eeef0978bcb78f577596eca7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73824673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb86d3cefef9bea16dba2bada8facb004fefd5f8630d2c2e9ef621dc30fc334d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:723f7d6ce61509bbccf2af45aa75a4c5cd83b188d6e85822321cdc68268417bf`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 53.2 MB (53226763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1538514cb923497c68c854e6f9e45945ca05f4a0f5a179472e7f81b1ee0cfbb`  
		Last Modified: Tue, 12 Nov 2024 02:38:24 GMT  
		Size: 20.6 MB (20597910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:341e02af8da6e03d6cb6c843c920d1e11a358ba849e80427f814ea7d8167df0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4061376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f70136036ca06b148cdae061bc19b58ac4328268fb771f3a7d56712d4afa47`

```dockerfile
```

-	Layers:
	-	`sha256:cc3306c9a01b6e93fe278e11e07f05c659419817f5e82f4aac8bfeb2207d137a`  
		Last Modified: Tue, 12 Nov 2024 02:38:23 GMT  
		Size: 4.1 MB (4054555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b7ee26ecf9dc640a238d3ae29c2b9614a6a82f979626b18d6f48299c4e2c3b`  
		Last Modified: Tue, 12 Nov 2024 02:38:23 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c09dcf78f1b0a06c8bd6f465a1adbebc5feb2fbe3f83cd9dfd2969b1f5feceb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69699297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a10d26a23af3144f1ea9c16aecef6411b34e0b5968162d389df222b05cad850a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4ff391534f557bd19067799d6e6b7e386e43cbf7d061a795a182546eb2145e99`  
		Last Modified: Tue, 12 Nov 2024 00:58:57 GMT  
		Size: 50.1 MB (50091523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d129d70e5af0f50e5354ff02342f42eba97458b43a0df2209f72566f664a4a`  
		Last Modified: Tue, 12 Nov 2024 06:29:56 GMT  
		Size: 19.6 MB (19607774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:36013fb61628706615c5cf999a5952e22dc0dcfc8f985bb9b318ff8349ace822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4063658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5becb61b4809956e3da35a939f26fabba7ff7639d8c825ccb68d86ceb2f66025`

```dockerfile
```

-	Layers:
	-	`sha256:7a526bf7c983b9f3e240fb3a59d54f61c33f79916e8fcee7c9f0071815b438f7`  
		Last Modified: Tue, 12 Nov 2024 06:29:56 GMT  
		Size: 4.1 MB (4056777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f435a4ab56f4980a90c473c5c339e287f55acb946c26cc36ddbba38e0739a1fe`  
		Last Modified: Tue, 12 Nov 2024 06:29:55 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3244cb4ae15e09963fb818758a3171b84d208a914cecf7b8948bab3070d8268f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.6 MB (66626866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c40d70011a851a088c8939609eb972337202cf9ca4e44713222d2060b3b8f0f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:da23906b82d0da338b0e507d1bef5cf2747e130d745e77708e8f5279af9a4764`  
		Last Modified: Tue, 12 Nov 2024 01:02:46 GMT  
		Size: 47.7 MB (47681766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9b00d9d0a43af35aa09caad4b98ca01f5b7a33e4efde2bc19aa6be0499f216`  
		Last Modified: Tue, 12 Nov 2024 16:02:34 GMT  
		Size: 18.9 MB (18945100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:939536ff2e2f735538e7914b008724ca3b0776bbd3785d5342bf15bd5ba7f06a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4062456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab45a4af1054cc4670e39ae2a067e67945abecaf95ad1fb893d51e1e6600893a`

```dockerfile
```

-	Layers:
	-	`sha256:a928037a0af31f797489ef0af5dcac5f8acfe6e04948025ea1d72dd175d5bacd`  
		Last Modified: Tue, 12 Nov 2024 16:02:33 GMT  
		Size: 4.1 MB (4055575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed54083f197d3df360b288c743be5a16f3d315e19c0cbc3a73ca735da45a5e4c`  
		Last Modified: Tue, 12 Nov 2024 16:02:33 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:556e7e00b135aa369fc03c74579f79f4eae25c78e4bee00635729b6f12018df8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73922052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be941a9867f832ef97ccf00bc779f0b68e380cb201a0a24c3026c9c509b135d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4de57c6718ff0fb4c76cd3ff1a33db2bde24e482395a89d0d4f6c7e6b3c20f53`  
		Last Modified: Tue, 12 Nov 2024 01:03:14 GMT  
		Size: 53.7 MB (53669977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27cb33ae9e17116eb9be8382614725b619742aeedfb992b4bc26c5d5efa717e`  
		Last Modified: Tue, 12 Nov 2024 11:17:43 GMT  
		Size: 20.3 MB (20252075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d29c4fe931cedbe6dfa651e2107a03afd42cf2d8299d01445482c14cda8f0831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4066350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44cd0cad434906c6088ae004cae4327ef76d01dffa1a84cf157f7b78eb178589`

```dockerfile
```

-	Layers:
	-	`sha256:2a8bb80f2fa2059b19dee0dd06a01b5cc7aa7b85877be888124ee5bb76a4d3e4`  
		Last Modified: Tue, 12 Nov 2024 11:17:42 GMT  
		Size: 4.1 MB (4059450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9fd3ca1a9a3a8d76e8e4b087e685f0d1e2b32ab3bff8f0063a6c264d63c9949`  
		Last Modified: Tue, 12 Nov 2024 11:17:42 GMT  
		Size: 6.9 KB (6900 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:da816f8eb964403dca1d95dba259e31f140b9fc698f9815a96303413255f25fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75817617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad9ee0f4bec9c6fef7ee3aafc5b49c3ce72fe4c7009a22352f698636585b21cf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a04f0591b5521dc9360454fa2fd6b21d9b7d989bb4c88327ad94f8282af3b267`  
		Last Modified: Tue, 12 Nov 2024 00:55:13 GMT  
		Size: 54.1 MB (54095157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914cc5c9bed5c786b85a6e40864cd3fb4af442dea3455ca88a01cfa26707d8df`  
		Last Modified: Tue, 12 Nov 2024 02:38:04 GMT  
		Size: 21.7 MB (21722460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9d0e6300c6451b2db0ff47a7b39d3b135872ec077ef50f473bddebefe68c2581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4057092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49fa3c56c66f4081ff0151f120b4b13784284fdcc2fe4a32b10b05bc9831a8d`

```dockerfile
```

-	Layers:
	-	`sha256:9b0f991f6eed552a6a904617d1e2af1fae7d23a97a5853ddb4b44b53b774fbba`  
		Last Modified: Tue, 12 Nov 2024 02:38:04 GMT  
		Size: 4.1 MB (4050293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa54182865e1c17ec6dd4311af29948d3270ee77ef5541ad3a9c3fd8fb0c8c68`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 6.8 KB (6799 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:81c589f2e660a5b752bfae2db7fa09038bd3ba6ee6a790235d41ca922ea2f163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73152229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f3b3755b9c9a37637278ae88121f4293b8b3478b630d2a334fbc0f53bc7795`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e85824c3ce994136e0b1f6545ca38052c56e3faf7dc4ab5102ef2c2e357cee02`  
		Last Modified: Tue, 12 Nov 2024 01:08:01 GMT  
		Size: 52.2 MB (52200415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40c4cfa8a0eedb22460a31984d56495095c0e6d072ab4be3aa70aec30584cf7`  
		Last Modified: Tue, 12 Nov 2024 18:05:03 GMT  
		Size: 21.0 MB (20951814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:22b45c3877321b46a20730e3995b95b27059501e1bcc9cf8fde2e2a9fadbc978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 KB (6654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d30710b7ecf8b19351e2cf995144203be23417de25869ea2d576f55f685ce89`

```dockerfile
```

-	Layers:
	-	`sha256:1674988eace870937b148290b435d75c369a1f4ef2f39991693861bc4aeaeff7`  
		Last Modified: Tue, 12 Nov 2024 18:05:00 GMT  
		Size: 6.7 KB (6654 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b36ab86690611318dcc37e932f66352a6a608990639315d31b5db60822e3152e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79177514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8767495c53385436730670f594cf2570df7c4332029e877e7ccaa0497d0db1c6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:554b3bf5ec10b22cc962f7afc042e96c50635c0e2b0d817544a202afc2a52711`  
		Last Modified: Tue, 12 Nov 2024 01:05:47 GMT  
		Size: 57.2 MB (57193598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08187472bfe4fce6e3b2fc2951e231ce30c71f70be1dc829ad73735e312d479f`  
		Last Modified: Tue, 12 Nov 2024 08:31:04 GMT  
		Size: 22.0 MB (21983916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4163f50eacc16a9a74dacef16c13fe5b0e88708e96517b2d33282f53abb663bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4064697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea12c2369d549c15187a9e4de29519d195d5e11321f44ca7565e6f43ccd8c68`

```dockerfile
```

-	Layers:
	-	`sha256:8bc27c99b4b763ad4265fdae7572bf9de79c8c842950e22de9451dc57b21f89e`  
		Last Modified: Tue, 12 Nov 2024 08:31:03 GMT  
		Size: 4.1 MB (4057844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d89080bcc025993b77857d5b2cecb80f56da462e48216a66ae8586a554111e2`  
		Last Modified: Tue, 12 Nov 2024 08:31:02 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:24dcbbd0e2ee32d1dba9e2e5844af10d131703be2f58837fd22aa7f1f036bf17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71667113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4bd6b050755f4e2f11dc7120e640aa938167574228c3e901d4ae13e0d782f07`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:a39f1e594ed2d718a6cabab2e5ea2ce29b47a86f2d43588cafbf682ddc9af2ca in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5c18b80e18178230beda6e484fe9dcde3f9663fa4695718e63800e23f1c0399f`  
		Last Modified: Thu, 17 Oct 2024 01:17:23 GMT  
		Size: 51.5 MB (51529184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9afe98cafb187775506b46e655b83f4d919ff657d9c24036a88a37c7e186b3`  
		Last Modified: Sat, 19 Oct 2024 01:06:46 GMT  
		Size: 20.1 MB (20137929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2125c80eac7fb61dee0bf4629df8ac0785422e6e4c56f8f15ff090b697e76324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4031349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc49637a86d8c0ceaf270f6bc7ded55e1afba9aee8479567a486af0a1a9b906b`

```dockerfile
```

-	Layers:
	-	`sha256:a45cc8e562fd303037be29b476fa881a7ec77fd72466df42383dc6c612c2088f`  
		Last Modified: Sat, 19 Oct 2024 01:06:44 GMT  
		Size: 4.0 MB (4024707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c9bb89a3de98c2ea298a2ff66fa98c5e299403e1665068622932e7b890ab2b`  
		Last Modified: Sat, 19 Oct 2024 01:06:43 GMT  
		Size: 6.6 KB (6642 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:dae85776025d232213b996742b5a8627c1670b132b805534906e88e0ecfbd920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74594615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f467ac0e350dd644702d1948d2a30ebef2ae600aeccdc895d9a61a3afc0ed91e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a54a131d29bb2d4a9258476cdcb51efa9314272b8894e2474e100e5d38d85679`  
		Last Modified: Tue, 12 Nov 2024 01:05:54 GMT  
		Size: 52.9 MB (52885488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a20f0f48b3016dae43f5b6fa4b9b89a2e08fbca4da340a0b01b79f3c8a37e0f`  
		Last Modified: Tue, 12 Nov 2024 09:03:50 GMT  
		Size: 21.7 MB (21709127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6bac11572437bb986cc2a3d91d185683c1877927cfeb576f23d4bd47c966ad22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4062302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c186f0d8a809a7d02f80d17bea3cd8be3931de9e10af463efc5ca9f15f6bfa`

```dockerfile
```

-	Layers:
	-	`sha256:0b946d20078a601263710f001ee104501a07e38f3ed5d718971c854aa87fe4f1`  
		Last Modified: Tue, 12 Nov 2024 09:03:50 GMT  
		Size: 4.1 MB (4055481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d2d0b1740b206909317d79e93207de19502facc9b8442347f2ab05b9e999748`  
		Last Modified: Tue, 12 Nov 2024 09:03:49 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:b4b757d748fa726c2bd2cf871ddcb888abc2629d4d810d39f96d38a8459f2f64
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
$ docker pull buildpack-deps@sha256:2a1bd17b9e1179e78a37cda2c95e93951c6eb4a1124428a1956a423ea7e13d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140355694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543cc9466a8dcd1ed3904970a2c6b3a94865825d52f80c81fd62f72298710c59`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:723f7d6ce61509bbccf2af45aa75a4c5cd83b188d6e85822321cdc68268417bf`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 53.2 MB (53226763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1538514cb923497c68c854e6f9e45945ca05f4a0f5a179472e7f81b1ee0cfbb`  
		Last Modified: Tue, 12 Nov 2024 02:38:24 GMT  
		Size: 20.6 MB (20597910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa039132691ce2d5258743dd8ecefd941d85955a38506ba77c3fb6d2f554298`  
		Last Modified: Tue, 12 Nov 2024 03:18:08 GMT  
		Size: 66.5 MB (66531021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:006c1a4f157ca8332c37cfc903f51fe99c90c9e534a72cac860f9fb8365b84af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7623030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e23d95e10f0fa5f7d7bb7c419adb4b4efc852e89db69d30cfe318be44e81af`

```dockerfile
```

-	Layers:
	-	`sha256:f66b32ff82c0df69c59a686e88a8d08a6ae82c59c9462bd2249d9876a847eaca`  
		Last Modified: Tue, 12 Nov 2024 03:18:08 GMT  
		Size: 7.6 MB (7615716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6de0676f525b54096e36412a85f3c6647ed8bc777fe9cf6dbc7352a34d09c157`  
		Last Modified: Tue, 12 Nov 2024 03:18:07 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:8d8e3fdc5829aed1b63ea33f435469be1517cd603483aabe32fe43e31b9b84e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133665306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16cf4cc1b27f69e3f63ac0b103f60c88fafda72f2853563fccebf54e71da792d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4ff391534f557bd19067799d6e6b7e386e43cbf7d061a795a182546eb2145e99`  
		Last Modified: Tue, 12 Nov 2024 00:58:57 GMT  
		Size: 50.1 MB (50091523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d129d70e5af0f50e5354ff02342f42eba97458b43a0df2209f72566f664a4a`  
		Last Modified: Tue, 12 Nov 2024 06:29:56 GMT  
		Size: 19.6 MB (19607774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a342b984b6752601eb44f7fa9cc6f866d747d925571f5c63f8db143a85f2fc46`  
		Last Modified: Tue, 12 Nov 2024 11:32:48 GMT  
		Size: 64.0 MB (63966009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:55cb1fe2158d176fa5dcb4daeac857818c62b2e9366dc456933b6f31765d4469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7623355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5037e5aaa8ca5213b9ca8057df32fbe8e1b104c09243d715658e4a29226b356c`

```dockerfile
```

-	Layers:
	-	`sha256:cb82e81672aacf72d387cbc2f43da98514547c58c1480ebf7b5835d0e3fb28c7`  
		Last Modified: Tue, 12 Nov 2024 11:32:47 GMT  
		Size: 7.6 MB (7615982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d98118b2ef6e507ba56174c04789b05d0d96599c8d4772447261b2491bdffb5`  
		Last Modified: Tue, 12 Nov 2024 11:32:46 GMT  
		Size: 7.4 KB (7373 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:da6fdb925b5de7f3beaaf9f7138cfab36ec0cbfdcdabf72cdad10c36ca194511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127859410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:290b778918d3f0776bc82777549e9e66202608ae29931c36c3a39cb680f69433`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:7b183110c42f24584c122a8e76db1e925d5fd8b3489ae273dbca0b0cc3bc0090 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a5589eaa1616610f1da5585cd04faf9e418fe913dd4e9ef827abdbe93f8caa5b`  
		Last Modified: Thu, 17 Oct 2024 03:10:29 GMT  
		Size: 47.7 MB (47659640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a052304c7554ffebe70b582d4e2eb7d1d61098f5f96c8c9603940278d081561`  
		Last Modified: Sat, 19 Oct 2024 00:58:30 GMT  
		Size: 19.0 MB (18971211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfcca10ec23fe707cc08f7ab790838065704861f60c0f678095482cc25ef593`  
		Last Modified: Sat, 19 Oct 2024 06:40:45 GMT  
		Size: 61.2 MB (61228559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a9757a6eef12d8e4457f63d8128b0b8c16a0230cee675ce2af94935916d16c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eea98d047064758984f353ad89edcd13307d0700c40c376b60bdac9d397af66c`

```dockerfile
```

-	Layers:
	-	`sha256:7a93cf475e613ba4986581169e51da296f5eab2d1af2eec23ca1a4ebddd8c326`  
		Last Modified: Sat, 19 Oct 2024 06:40:43 GMT  
		Size: 7.5 MB (7486524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20c2dfc26ee7918a49826fed2ffc0d36d6dd4dab8b3cc5d2ec3b13523d04f02c`  
		Last Modified: Sat, 19 Oct 2024 06:40:42 GMT  
		Size: 7.4 KB (7386 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3b629d663679a2b2b40868852c5dfbda509fd66bd6f901cdf256592706f0da24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.3 MB (140280895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6f779d0370a31853b4d9b6ad68485f28d2bdeb59641df30882b6ee54f6a915`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:5d91cfda460a83c91802e918bddf6951978599b67dbd5e3c0a492a53f20d6ad6 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6f4ac25c892a8a547634a70e67af9f356a5f2b1f34e7c78d52074f2a21999111`  
		Last Modified: Thu, 17 Oct 2024 01:17:18 GMT  
		Size: 53.6 MB (53599725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b74f65518d0117b47b1d80b0bf8981ebb7ddb04cdeeadd261af699b6e5d50`  
		Last Modified: Sat, 19 Oct 2024 01:12:15 GMT  
		Size: 20.4 MB (20382473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b125c1d7d6d0668d3d31049e15ed26c5f15741a45a407eab00423ec50972be12`  
		Last Modified: Sat, 19 Oct 2024 05:20:09 GMT  
		Size: 66.3 MB (66298697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:981b9d0b27672f9ae58a479116f2d44a4372d329f9e65910623c50857c7f2012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7499825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83b16a06a55282321f67d9ada42e21d02d811ecc3a3fc386acf84684d93a15b`

```dockerfile
```

-	Layers:
	-	`sha256:e31fe82ca59e0b11c21807625cd32304cb7c70ed6c502b0b98468e11df80130f`  
		Last Modified: Sat, 19 Oct 2024 05:20:07 GMT  
		Size: 7.5 MB (7492419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:859f0a00775cceb04089b3a21a3466d9b86a3ba87b410318a08e54198cb54287`  
		Last Modified: Sat, 19 Oct 2024 05:20:06 GMT  
		Size: 7.4 KB (7406 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:17f77e1c82b223cf3f38382724d4a83f63a07ca65e77321db1ec9ea444466eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.2 MB (144160990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558df670cd95356ddd37034014ece4572b6e5b0c6d1d40dda1c173413f7e507c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a04f0591b5521dc9360454fa2fd6b21d9b7d989bb4c88327ad94f8282af3b267`  
		Last Modified: Tue, 12 Nov 2024 00:55:13 GMT  
		Size: 54.1 MB (54095157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914cc5c9bed5c786b85a6e40864cd3fb4af442dea3455ca88a01cfa26707d8df`  
		Last Modified: Tue, 12 Nov 2024 02:38:04 GMT  
		Size: 21.7 MB (21722460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c207d20a70d18f9e95ac6b10fd58bbc5d2a036845c50cdab8e2fa983066a990`  
		Last Modified: Tue, 12 Nov 2024 03:14:35 GMT  
		Size: 68.3 MB (68343373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a7af66e9bf190aefa86e1f76abfec0fe4c44a04ddbc03d55ff18c4ef7c863f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7617759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3fbadbc2198b4e131475280b87df5241639ec83a1ca1198e19eb4022f3dc1a`

```dockerfile
```

-	Layers:
	-	`sha256:cb12d5a0477c96ee0bf9ebe5630d302496423079ffd94280db676664955ca33a`  
		Last Modified: Tue, 12 Nov 2024 03:14:33 GMT  
		Size: 7.6 MB (7610468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:534ad46e5e83d3c45f05ba6b7886be6e67993ce4f589506783f49296f2c60595`  
		Last Modified: Tue, 12 Nov 2024 03:14:32 GMT  
		Size: 7.3 KB (7291 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:78d50bdb37e5bb8ce65015b943145de8356d61c7bf9ac0d2b70b5bb19d61592f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138151112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c40a1f4ab862506927452bfc655b5b498b376a47d0ebbd5c7fe468eb7a88db`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:7540ed5b693bb419df5aaa69483f55c19bc0566d076c5e65757a0a6fe38375a3 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bd6795a0a311ac784071ff263d2b83d646956234334d40fe908b91a1dde11378`  
		Last Modified: Thu, 17 Oct 2024 01:22:22 GMT  
		Size: 52.1 MB (52128468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bde6977c24ffe15c007c6606184010ccb92606e6158cbd76d8e770997debfa`  
		Last Modified: Sat, 19 Oct 2024 01:01:31 GMT  
		Size: 21.0 MB (20966640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdea9feeed917171d6d06a6129bb34f0f75c8fdb0fc8f9755f248adca6eee285`  
		Last Modified: Sat, 19 Oct 2024 02:14:28 GMT  
		Size: 65.1 MB (65056004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:81190818ed7d83b0f92ee66dc853e7c6f22b9535d8e52f4f00fcfdc4354973ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 KB (7159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f37bae74959741f2259d72bed0704bd028bbb2ff4414f68912774344bbdbf3c`

```dockerfile
```

-	Layers:
	-	`sha256:c02dd3eab5f5e9db4c0f38c6e763e61d6cf4e72819705f3060c07ec5c7819c76`  
		Last Modified: Sat, 19 Oct 2024 02:14:21 GMT  
		Size: 7.2 KB (7159 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:fccf093e3bb36008832e5ec58a51f1ac32d0d886c98f75c4f37ebb863d6885a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (151013309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ebeec5bc9376d17e01d51bb7962444e7575f3df8a16e27526ab9a4ffac838a4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:554b3bf5ec10b22cc962f7afc042e96c50635c0e2b0d817544a202afc2a52711`  
		Last Modified: Tue, 12 Nov 2024 01:05:47 GMT  
		Size: 57.2 MB (57193598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08187472bfe4fce6e3b2fc2951e231ce30c71f70be1dc829ad73735e312d479f`  
		Last Modified: Tue, 12 Nov 2024 08:31:04 GMT  
		Size: 22.0 MB (21983916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5445db0db78751088bfd85b5a3ee628352f9d78288ca29fed636c550e50e6235`  
		Last Modified: Tue, 12 Nov 2024 16:12:54 GMT  
		Size: 71.8 MB (71835795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e94f6be5b6eddf231fce0e6606fd38a9209523a97cc3e95f0c1f15a4652074c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7629581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46fa744652a5277bf95624921ad212b186a9d9c17913d20b62f2bbb489029e5c`

```dockerfile
```

-	Layers:
	-	`sha256:1dc404b8f0d7ebf05e25893e3c6825872d16ff0cae8abaaf48f9a7649d8bff42`  
		Last Modified: Tue, 12 Nov 2024 16:12:52 GMT  
		Size: 7.6 MB (7622236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b0339d7f4b34fc047dba3dca04265fd1aa21572185158b43c3d4d366e80585d`  
		Last Modified: Tue, 12 Nov 2024 16:12:51 GMT  
		Size: 7.3 KB (7345 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cb2e75552a2d042a659ba547ccb0609e06f697798884a74c6805ee8b1ab38d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141797604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9b44ffe80f44627eca35eaa520ed53a92ed54585062c43ba93198f9ec59a05`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:fe7c88cb45fa7097d71f60ba00c0d6ad76dd030e8e34771e5ee3735b59a4d6e6 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:53440987c87b8deb9090e5298bf822ffc945f186eb4c81cecc0ebf58717ca549`  
		Last Modified: Thu, 17 Oct 2024 01:51:55 GMT  
		Size: 52.8 MB (52808844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3816f9124671541da45f7e11a0a925de47e719482f5bcd085247ecdcb8c613`  
		Last Modified: Sat, 19 Oct 2024 00:59:12 GMT  
		Size: 21.7 MB (21656188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cc2aa2fcdc4addb1b596c3dbc6f3699d60107644fd49f54f3050356c21437c`  
		Last Modified: Sat, 19 Oct 2024 03:48:52 GMT  
		Size: 67.3 MB (67332572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b270aaa7768e4a2d159ff7b5f42829b62c59d4ef131517f86c9ae12564beddae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7494252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942bb4de50d03290e36368d5b3922ed61f5adbe88b45bdc98fe4f5ece352669e`

```dockerfile
```

-	Layers:
	-	`sha256:be9cc770647715d3212ab0a996c38d93ff0e416f9d91de05c1000fc1ed5dc2b7`  
		Last Modified: Sat, 19 Oct 2024 03:48:52 GMT  
		Size: 7.5 MB (7486926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dd9a3268144974562f1606345489a7a1d2317d957179ab65d447e065d5173d3`  
		Last Modified: Sat, 19 Oct 2024 03:48:51 GMT  
		Size: 7.3 KB (7326 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:5413e56f36811f5d5634b0a0f23944df58b3536b3a54ca3fe2c21ed2adc784c9
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
$ docker pull buildpack-deps@sha256:7cbe3791c734ad4570773a958b63e1371d045a3aff24011c5716ccfadeb65a08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.0 MB (368973816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7703f03776d03820bc730c7ba4a1357b289a3c1e5cd0d41bab150afffe8d752`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:723f7d6ce61509bbccf2af45aa75a4c5cd83b188d6e85822321cdc68268417bf`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 53.2 MB (53226763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1538514cb923497c68c854e6f9e45945ca05f4a0f5a179472e7f81b1ee0cfbb`  
		Last Modified: Tue, 12 Nov 2024 02:38:24 GMT  
		Size: 20.6 MB (20597910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa039132691ce2d5258743dd8ecefd941d85955a38506ba77c3fb6d2f554298`  
		Last Modified: Tue, 12 Nov 2024 03:18:08 GMT  
		Size: 66.5 MB (66531021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c24554062853c5674b963d550e30ca0a757e9eb981889481f056f908bfb85e`  
		Last Modified: Tue, 12 Nov 2024 03:59:20 GMT  
		Size: 228.6 MB (228618122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fde6ad638d3489c2565f8fd9372ea5a582fde062402076e49c07d546cbce9f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16694153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af1b4e4371b4516fbe01c132347fd12fc0e48c4c84d419d3f4d87a1585cddc59`

```dockerfile
```

-	Layers:
	-	`sha256:ecac10a1f2388f1010f072658b62094485c4427f64b84a05b42df2b85a715e3d`  
		Last Modified: Tue, 12 Nov 2024 03:59:17 GMT  
		Size: 16.7 MB (16683960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5443e4fb350c11c56dd93b8946e2d787d3ec950b1cf9ba87f19e87f295b7e40`  
		Last Modified: Tue, 12 Nov 2024 03:59:17 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:bb3cf03abb1e11b70090a8ca17faf8d5f6e9af798e64c8fbb6cc6fce6b7c67a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.3 MB (337265046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e60b6a1fbca262eafa40df4cd4c57a7f24721394b8bcc7556c626b414caa1c5b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4ff391534f557bd19067799d6e6b7e386e43cbf7d061a795a182546eb2145e99`  
		Last Modified: Tue, 12 Nov 2024 00:58:57 GMT  
		Size: 50.1 MB (50091523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d129d70e5af0f50e5354ff02342f42eba97458b43a0df2209f72566f664a4a`  
		Last Modified: Tue, 12 Nov 2024 06:29:56 GMT  
		Size: 19.6 MB (19607774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a342b984b6752601eb44f7fa9cc6f866d747d925571f5c63f8db143a85f2fc46`  
		Last Modified: Tue, 12 Nov 2024 11:32:48 GMT  
		Size: 64.0 MB (63966009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028167967e0788114dab10f0fa1afeca8ecbb50011cd2627a38462981e159174`  
		Last Modified: Tue, 12 Nov 2024 14:00:43 GMT  
		Size: 203.6 MB (203599740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1284c8ed67cf389d2a9f9ff026521d12046ee702bad2602fb6536d2689ec86d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16486074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c884655403838f628e98896e91e34a18dd06a0b51f0c1c370e20e732bb864e15`

```dockerfile
```

-	Layers:
	-	`sha256:53c9b04be44740a94267bb9e60dbcd57098849e3b57e866add59c69ab31bdde4`  
		Last Modified: Tue, 12 Nov 2024 14:00:39 GMT  
		Size: 16.5 MB (16475821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85e24f36060e6aee12a7007f4582acdc6c5bc92b806e1c824b5b78c1f596e1e5`  
		Last Modified: Tue, 12 Nov 2024 14:00:38 GMT  
		Size: 10.3 KB (10253 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:43decaa0c198ea49c25e0579b8e4459dd1eccbb162c2f3b3cf60c5f105c30532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.8 MB (317793004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e5bbbfe2db111d7c0a74257c7e0efd4390af8f93f7a297fced39742d6fee01`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:7b183110c42f24584c122a8e76db1e925d5fd8b3489ae273dbca0b0cc3bc0090 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a5589eaa1616610f1da5585cd04faf9e418fe913dd4e9ef827abdbe93f8caa5b`  
		Last Modified: Thu, 17 Oct 2024 03:10:29 GMT  
		Size: 47.7 MB (47659640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a052304c7554ffebe70b582d4e2eb7d1d61098f5f96c8c9603940278d081561`  
		Last Modified: Sat, 19 Oct 2024 00:58:30 GMT  
		Size: 19.0 MB (18971211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfcca10ec23fe707cc08f7ab790838065704861f60c0f678095482cc25ef593`  
		Last Modified: Sat, 19 Oct 2024 06:40:45 GMT  
		Size: 61.2 MB (61228559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b8715cfc77ca9de75ae3a4c97787dddb260f81e6774113adb34eeb4df9fbab`  
		Last Modified: Sat, 19 Oct 2024 08:15:21 GMT  
		Size: 189.9 MB (189933594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:201e31e97b8198b5b73245292db7ee57ccbcbff11baedb28f3c8716c3712a460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16305861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e54ca52b2d36a1153fe982f6c91426c036c1c8752aefa37315bbb6ae468eca`

```dockerfile
```

-	Layers:
	-	`sha256:db8b42ad1f6e5f980314f108470f162b14dd14f2b57c0eb4a15526b533e7ffc4`  
		Last Modified: Sat, 19 Oct 2024 08:15:17 GMT  
		Size: 16.3 MB (16295596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1dd62a0b90c1f4d9670edefd460b2729d71461a06b59b621e01e0e5c090f59f`  
		Last Modified: Sat, 19 Oct 2024 08:15:16 GMT  
		Size: 10.3 KB (10265 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4ae9574eaaaa819eee22d771b30ecfd1b6a61732dfedf09f4d626004b7756023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.7 MB (361701064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcbbe0de592c14b77f79d5364ba45b6b102a8f12377baa10181a3daeae528fa0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:5d91cfda460a83c91802e918bddf6951978599b67dbd5e3c0a492a53f20d6ad6 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6f4ac25c892a8a547634a70e67af9f356a5f2b1f34e7c78d52074f2a21999111`  
		Last Modified: Thu, 17 Oct 2024 01:17:18 GMT  
		Size: 53.6 MB (53599725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b74f65518d0117b47b1d80b0bf8981ebb7ddb04cdeeadd261af699b6e5d50`  
		Last Modified: Sat, 19 Oct 2024 01:12:15 GMT  
		Size: 20.4 MB (20382473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b125c1d7d6d0668d3d31049e15ed26c5f15741a45a407eab00423ec50972be12`  
		Last Modified: Sat, 19 Oct 2024 05:20:09 GMT  
		Size: 66.3 MB (66298697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd09379a59f4bf2683bfc63736559fb02ca078899a46853d3dbb50955d6ce02`  
		Last Modified: Sat, 19 Oct 2024 06:21:51 GMT  
		Size: 221.4 MB (221420169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a5e44adae95a33c8855a957d37239c524418aa044cf210b118df590bc5c617ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16604076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53d6fdab1445139470616a1ba7e76135d8184f2d94c3e977392d6f83c93cee3c`

```dockerfile
```

-	Layers:
	-	`sha256:49838c80534b422aa73f107fe50cea0e08b56cb8df4bed441762f4c6fc8da938`  
		Last Modified: Sat, 19 Oct 2024 06:21:46 GMT  
		Size: 16.6 MB (16593791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:130ddeaced8e30940ccc1ba76f5f1b1037cbac31ce7fb4fea621f464b45b9969`  
		Last Modified: Sat, 19 Oct 2024 06:21:45 GMT  
		Size: 10.3 KB (10285 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:13a5f075e4b03beecdfe160afa42b8b6109f2e26e8e33707314cef4940012410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.1 MB (374066765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43bc8c18b13cac0f90dc06c003982716d8f2c3d57540c4dd475cd2bf2aeb0768`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a04f0591b5521dc9360454fa2fd6b21d9b7d989bb4c88327ad94f8282af3b267`  
		Last Modified: Tue, 12 Nov 2024 00:55:13 GMT  
		Size: 54.1 MB (54095157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914cc5c9bed5c786b85a6e40864cd3fb4af442dea3455ca88a01cfa26707d8df`  
		Last Modified: Tue, 12 Nov 2024 02:38:04 GMT  
		Size: 21.7 MB (21722460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c207d20a70d18f9e95ac6b10fd58bbc5d2a036845c50cdab8e2fa983066a990`  
		Last Modified: Tue, 12 Nov 2024 03:14:35 GMT  
		Size: 68.3 MB (68343373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2790a8863dae4d5397c7a550a69104b8b23dcb717967ee6e4eaadfbb1e2b031a`  
		Last Modified: Tue, 12 Nov 2024 04:00:28 GMT  
		Size: 229.9 MB (229905775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ca9a1ae52fdac26a890763e00bccfb82d42e7c8eb0f3b6d31f79942c3f9a34e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16663809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:283d90ebc233386f9ee9c40e4a432225230f776486c2e00d3fd2ad23d5160970`

```dockerfile
```

-	Layers:
	-	`sha256:d3892b08125fc65dd00ec24cf04745b40b69e5b08348457ba04c1bdb60167dbf`  
		Last Modified: Tue, 12 Nov 2024 04:00:24 GMT  
		Size: 16.7 MB (16653639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84ebaf548cb0955edc73a8e3008964cb55db8614f1c4e3ca7733ffebe47caccf`  
		Last Modified: Tue, 12 Nov 2024 04:00:23 GMT  
		Size: 10.2 KB (10170 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:2d79e8b7e96fe38d9e45a4d282bd0f95d67001a444552087bd3cc32f25d08084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.8 MB (345787888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56875b7a504b29b2bb3123f42f536d1f78dc908550e86383f2d6486887d1a44`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:7540ed5b693bb419df5aaa69483f55c19bc0566d076c5e65757a0a6fe38375a3 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bd6795a0a311ac784071ff263d2b83d646956234334d40fe908b91a1dde11378`  
		Last Modified: Thu, 17 Oct 2024 01:22:22 GMT  
		Size: 52.1 MB (52128468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bde6977c24ffe15c007c6606184010ccb92606e6158cbd76d8e770997debfa`  
		Last Modified: Sat, 19 Oct 2024 01:01:31 GMT  
		Size: 21.0 MB (20966640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdea9feeed917171d6d06a6129bb34f0f75c8fdb0fc8f9755f248adca6eee285`  
		Last Modified: Sat, 19 Oct 2024 02:14:28 GMT  
		Size: 65.1 MB (65056004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64eacd2dd173c3ffb6f366cf5087686edf0379bf94a7576a971e2b52513c8882`  
		Last Modified: Sat, 19 Oct 2024 03:18:15 GMT  
		Size: 207.6 MB (207636776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:25e904418fdd672b948405e1f14bcb5c092286565f8ea58f426a76778aedf70f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce2990a7740c1ee661056d1286c412d9aa033ccfad23335960773e59e4582da`

```dockerfile
```

-	Layers:
	-	`sha256:529b4851b6d08464af5c7c7f70b64a67057dc822143fa9cdf853e9719b9b0d5f`  
		Last Modified: Sat, 19 Oct 2024 03:17:55 GMT  
		Size: 10.0 KB (10038 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:fb2d0b8252543fd9aac6afd2358f8c036517399d15ab671d2c26238bf25b8817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.7 MB (378675496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2934ca0774acb5c953ccff3f166b5c11443c95326cb52e98f91e9aa4cb675ae2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:7d34de8e15cda6686099080e64714532070b3d06a451fa9d77a5716745974490 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8299bac21377f71d4bbd00f3075290f241c45c39e6a9a76012dbff5b62d14e88`  
		Last Modified: Thu, 17 Oct 2024 01:23:55 GMT  
		Size: 57.1 MB (57126645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739c73c116650c722a140d5e98dc4d5b306e6daaa1f611e7f00699c828890445`  
		Last Modified: Sat, 19 Oct 2024 00:58:55 GMT  
		Size: 23.3 MB (23314858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888fc73ea70716bfd3afc5289dca8e001895bc72345d7defb80ef4274358afe4`  
		Last Modified: Sat, 19 Oct 2024 04:10:18 GMT  
		Size: 71.6 MB (71620992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e85c4c362f2752b90470a2e9c73e4b582008ca3b0314740e6a4e1c756cc08f0`  
		Last Modified: Sat, 19 Oct 2024 05:24:17 GMT  
		Size: 226.6 MB (226613001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bb68d7efafd7d984c6f1b48c59077419faf23c6d84bc1bacccfda22722f3d873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16505785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07402716cde3edbdad9c0a69eaa180c73b700706e17afbcf700e741832b7c2d3`

```dockerfile
```

-	Layers:
	-	`sha256:4b95db3e2321004c462504333af6b67a31f8bf670842e66a4656832a64ce8ec1`  
		Last Modified: Sat, 19 Oct 2024 05:24:10 GMT  
		Size: 16.5 MB (16495548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26c87f6f72bd68371ce1cee3cc527c15b062c2dba5a32da15805811213cc92cc`  
		Last Modified: Sat, 19 Oct 2024 05:24:09 GMT  
		Size: 10.2 KB (10237 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:64db136082af530566b7ed8329ddad4bb6bc67827f9ed7e770fb7c7d363aaa30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343151504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b638beec4f55aadeb0294811090591f2020966a01e0943d5ce76f0a912864f80`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:fe7c88cb45fa7097d71f60ba00c0d6ad76dd030e8e34771e5ee3735b59a4d6e6 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:53440987c87b8deb9090e5298bf822ffc945f186eb4c81cecc0ebf58717ca549`  
		Last Modified: Thu, 17 Oct 2024 01:51:55 GMT  
		Size: 52.8 MB (52808844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3816f9124671541da45f7e11a0a925de47e719482f5bcd085247ecdcb8c613`  
		Last Modified: Sat, 19 Oct 2024 00:59:12 GMT  
		Size: 21.7 MB (21656188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cc2aa2fcdc4addb1b596c3dbc6f3699d60107644fd49f54f3050356c21437c`  
		Last Modified: Sat, 19 Oct 2024 03:48:52 GMT  
		Size: 67.3 MB (67332572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc706768a06fa9cf16504e13939b12c91809de8a89473cc7b793fbce1b5adb60`  
		Last Modified: Sat, 19 Oct 2024 05:09:06 GMT  
		Size: 201.4 MB (201353900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8964bba7c715a5e8f0de47782dfc27bfae53b34e72337817658a05402ea8c5fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16298751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de39e96e1289fd9ad90558f1d9bc9ba89833a4dc736aa81a7d1eec6e72ae985a`

```dockerfile
```

-	Layers:
	-	`sha256:2e89bddb8da9917b83fcd1c1c9cd13cb701e559da0f070b1b66e91712318f5db`  
		Last Modified: Sat, 19 Oct 2024 05:09:03 GMT  
		Size: 16.3 MB (16288548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d292472b39d06e2e9473e3ce69b1cd5133a331271d388009a134a30414dbc91`  
		Last Modified: Sat, 19 Oct 2024 05:09:02 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:ab834ad536df5563da2eb202fbf667204c33c7c69f3e9d455af94182feef8593
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
$ docker pull buildpack-deps@sha256:2c9dda7b58f3cc1b6b5e844de7f661770af7817eeef0978bcb78f577596eca7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73824673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb86d3cefef9bea16dba2bada8facb004fefd5f8630d2c2e9ef621dc30fc334d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:723f7d6ce61509bbccf2af45aa75a4c5cd83b188d6e85822321cdc68268417bf`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 53.2 MB (53226763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1538514cb923497c68c854e6f9e45945ca05f4a0f5a179472e7f81b1ee0cfbb`  
		Last Modified: Tue, 12 Nov 2024 02:38:24 GMT  
		Size: 20.6 MB (20597910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:341e02af8da6e03d6cb6c843c920d1e11a358ba849e80427f814ea7d8167df0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4061376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f70136036ca06b148cdae061bc19b58ac4328268fb771f3a7d56712d4afa47`

```dockerfile
```

-	Layers:
	-	`sha256:cc3306c9a01b6e93fe278e11e07f05c659419817f5e82f4aac8bfeb2207d137a`  
		Last Modified: Tue, 12 Nov 2024 02:38:23 GMT  
		Size: 4.1 MB (4054555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b7ee26ecf9dc640a238d3ae29c2b9614a6a82f979626b18d6f48299c4e2c3b`  
		Last Modified: Tue, 12 Nov 2024 02:38:23 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c09dcf78f1b0a06c8bd6f465a1adbebc5feb2fbe3f83cd9dfd2969b1f5feceb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69699297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a10d26a23af3144f1ea9c16aecef6411b34e0b5968162d389df222b05cad850a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4ff391534f557bd19067799d6e6b7e386e43cbf7d061a795a182546eb2145e99`  
		Last Modified: Tue, 12 Nov 2024 00:58:57 GMT  
		Size: 50.1 MB (50091523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d129d70e5af0f50e5354ff02342f42eba97458b43a0df2209f72566f664a4a`  
		Last Modified: Tue, 12 Nov 2024 06:29:56 GMT  
		Size: 19.6 MB (19607774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:36013fb61628706615c5cf999a5952e22dc0dcfc8f985bb9b318ff8349ace822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4063658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5becb61b4809956e3da35a939f26fabba7ff7639d8c825ccb68d86ceb2f66025`

```dockerfile
```

-	Layers:
	-	`sha256:7a526bf7c983b9f3e240fb3a59d54f61c33f79916e8fcee7c9f0071815b438f7`  
		Last Modified: Tue, 12 Nov 2024 06:29:56 GMT  
		Size: 4.1 MB (4056777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f435a4ab56f4980a90c473c5c339e287f55acb946c26cc36ddbba38e0739a1fe`  
		Last Modified: Tue, 12 Nov 2024 06:29:55 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3244cb4ae15e09963fb818758a3171b84d208a914cecf7b8948bab3070d8268f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.6 MB (66626866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c40d70011a851a088c8939609eb972337202cf9ca4e44713222d2060b3b8f0f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:da23906b82d0da338b0e507d1bef5cf2747e130d745e77708e8f5279af9a4764`  
		Last Modified: Tue, 12 Nov 2024 01:02:46 GMT  
		Size: 47.7 MB (47681766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9b00d9d0a43af35aa09caad4b98ca01f5b7a33e4efde2bc19aa6be0499f216`  
		Last Modified: Tue, 12 Nov 2024 16:02:34 GMT  
		Size: 18.9 MB (18945100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:939536ff2e2f735538e7914b008724ca3b0776bbd3785d5342bf15bd5ba7f06a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4062456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab45a4af1054cc4670e39ae2a067e67945abecaf95ad1fb893d51e1e6600893a`

```dockerfile
```

-	Layers:
	-	`sha256:a928037a0af31f797489ef0af5dcac5f8acfe6e04948025ea1d72dd175d5bacd`  
		Last Modified: Tue, 12 Nov 2024 16:02:33 GMT  
		Size: 4.1 MB (4055575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed54083f197d3df360b288c743be5a16f3d315e19c0cbc3a73ca735da45a5e4c`  
		Last Modified: Tue, 12 Nov 2024 16:02:33 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:556e7e00b135aa369fc03c74579f79f4eae25c78e4bee00635729b6f12018df8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73922052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be941a9867f832ef97ccf00bc779f0b68e380cb201a0a24c3026c9c509b135d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4de57c6718ff0fb4c76cd3ff1a33db2bde24e482395a89d0d4f6c7e6b3c20f53`  
		Last Modified: Tue, 12 Nov 2024 01:03:14 GMT  
		Size: 53.7 MB (53669977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27cb33ae9e17116eb9be8382614725b619742aeedfb992b4bc26c5d5efa717e`  
		Last Modified: Tue, 12 Nov 2024 11:17:43 GMT  
		Size: 20.3 MB (20252075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d29c4fe931cedbe6dfa651e2107a03afd42cf2d8299d01445482c14cda8f0831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4066350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44cd0cad434906c6088ae004cae4327ef76d01dffa1a84cf157f7b78eb178589`

```dockerfile
```

-	Layers:
	-	`sha256:2a8bb80f2fa2059b19dee0dd06a01b5cc7aa7b85877be888124ee5bb76a4d3e4`  
		Last Modified: Tue, 12 Nov 2024 11:17:42 GMT  
		Size: 4.1 MB (4059450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9fd3ca1a9a3a8d76e8e4b087e685f0d1e2b32ab3bff8f0063a6c264d63c9949`  
		Last Modified: Tue, 12 Nov 2024 11:17:42 GMT  
		Size: 6.9 KB (6900 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:da816f8eb964403dca1d95dba259e31f140b9fc698f9815a96303413255f25fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75817617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad9ee0f4bec9c6fef7ee3aafc5b49c3ce72fe4c7009a22352f698636585b21cf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a04f0591b5521dc9360454fa2fd6b21d9b7d989bb4c88327ad94f8282af3b267`  
		Last Modified: Tue, 12 Nov 2024 00:55:13 GMT  
		Size: 54.1 MB (54095157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914cc5c9bed5c786b85a6e40864cd3fb4af442dea3455ca88a01cfa26707d8df`  
		Last Modified: Tue, 12 Nov 2024 02:38:04 GMT  
		Size: 21.7 MB (21722460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9d0e6300c6451b2db0ff47a7b39d3b135872ec077ef50f473bddebefe68c2581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4057092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49fa3c56c66f4081ff0151f120b4b13784284fdcc2fe4a32b10b05bc9831a8d`

```dockerfile
```

-	Layers:
	-	`sha256:9b0f991f6eed552a6a904617d1e2af1fae7d23a97a5853ddb4b44b53b774fbba`  
		Last Modified: Tue, 12 Nov 2024 02:38:04 GMT  
		Size: 4.1 MB (4050293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa54182865e1c17ec6dd4311af29948d3270ee77ef5541ad3a9c3fd8fb0c8c68`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 6.8 KB (6799 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:81c589f2e660a5b752bfae2db7fa09038bd3ba6ee6a790235d41ca922ea2f163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73152229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f3b3755b9c9a37637278ae88121f4293b8b3478b630d2a334fbc0f53bc7795`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e85824c3ce994136e0b1f6545ca38052c56e3faf7dc4ab5102ef2c2e357cee02`  
		Last Modified: Tue, 12 Nov 2024 01:08:01 GMT  
		Size: 52.2 MB (52200415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40c4cfa8a0eedb22460a31984d56495095c0e6d072ab4be3aa70aec30584cf7`  
		Last Modified: Tue, 12 Nov 2024 18:05:03 GMT  
		Size: 21.0 MB (20951814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:22b45c3877321b46a20730e3995b95b27059501e1bcc9cf8fde2e2a9fadbc978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 KB (6654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d30710b7ecf8b19351e2cf995144203be23417de25869ea2d576f55f685ce89`

```dockerfile
```

-	Layers:
	-	`sha256:1674988eace870937b148290b435d75c369a1f4ef2f39991693861bc4aeaeff7`  
		Last Modified: Tue, 12 Nov 2024 18:05:00 GMT  
		Size: 6.7 KB (6654 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b36ab86690611318dcc37e932f66352a6a608990639315d31b5db60822e3152e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79177514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8767495c53385436730670f594cf2570df7c4332029e877e7ccaa0497d0db1c6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:554b3bf5ec10b22cc962f7afc042e96c50635c0e2b0d817544a202afc2a52711`  
		Last Modified: Tue, 12 Nov 2024 01:05:47 GMT  
		Size: 57.2 MB (57193598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08187472bfe4fce6e3b2fc2951e231ce30c71f70be1dc829ad73735e312d479f`  
		Last Modified: Tue, 12 Nov 2024 08:31:04 GMT  
		Size: 22.0 MB (21983916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4163f50eacc16a9a74dacef16c13fe5b0e88708e96517b2d33282f53abb663bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4064697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea12c2369d549c15187a9e4de29519d195d5e11321f44ca7565e6f43ccd8c68`

```dockerfile
```

-	Layers:
	-	`sha256:8bc27c99b4b763ad4265fdae7572bf9de79c8c842950e22de9451dc57b21f89e`  
		Last Modified: Tue, 12 Nov 2024 08:31:03 GMT  
		Size: 4.1 MB (4057844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d89080bcc025993b77857d5b2cecb80f56da462e48216a66ae8586a554111e2`  
		Last Modified: Tue, 12 Nov 2024 08:31:02 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:24dcbbd0e2ee32d1dba9e2e5844af10d131703be2f58837fd22aa7f1f036bf17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71667113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4bd6b050755f4e2f11dc7120e640aa938167574228c3e901d4ae13e0d782f07`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:a39f1e594ed2d718a6cabab2e5ea2ce29b47a86f2d43588cafbf682ddc9af2ca in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5c18b80e18178230beda6e484fe9dcde3f9663fa4695718e63800e23f1c0399f`  
		Last Modified: Thu, 17 Oct 2024 01:17:23 GMT  
		Size: 51.5 MB (51529184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9afe98cafb187775506b46e655b83f4d919ff657d9c24036a88a37c7e186b3`  
		Last Modified: Sat, 19 Oct 2024 01:06:46 GMT  
		Size: 20.1 MB (20137929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2125c80eac7fb61dee0bf4629df8ac0785422e6e4c56f8f15ff090b697e76324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4031349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc49637a86d8c0ceaf270f6bc7ded55e1afba9aee8479567a486af0a1a9b906b`

```dockerfile
```

-	Layers:
	-	`sha256:a45cc8e562fd303037be29b476fa881a7ec77fd72466df42383dc6c612c2088f`  
		Last Modified: Sat, 19 Oct 2024 01:06:44 GMT  
		Size: 4.0 MB (4024707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c9bb89a3de98c2ea298a2ff66fa98c5e299403e1665068622932e7b890ab2b`  
		Last Modified: Sat, 19 Oct 2024 01:06:43 GMT  
		Size: 6.6 KB (6642 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:dae85776025d232213b996742b5a8627c1670b132b805534906e88e0ecfbd920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74594615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f467ac0e350dd644702d1948d2a30ebef2ae600aeccdc895d9a61a3afc0ed91e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a54a131d29bb2d4a9258476cdcb51efa9314272b8894e2474e100e5d38d85679`  
		Last Modified: Tue, 12 Nov 2024 01:05:54 GMT  
		Size: 52.9 MB (52885488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a20f0f48b3016dae43f5b6fa4b9b89a2e08fbca4da340a0b01b79f3c8a37e0f`  
		Last Modified: Tue, 12 Nov 2024 09:03:50 GMT  
		Size: 21.7 MB (21709127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6bac11572437bb986cc2a3d91d185683c1877927cfeb576f23d4bd47c966ad22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4062302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c186f0d8a809a7d02f80d17bea3cd8be3931de9e10af463efc5ca9f15f6bfa`

```dockerfile
```

-	Layers:
	-	`sha256:0b946d20078a601263710f001ee104501a07e38f3ed5d718971c854aa87fe4f1`  
		Last Modified: Tue, 12 Nov 2024 09:03:50 GMT  
		Size: 4.1 MB (4055481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d2d0b1740b206909317d79e93207de19502facc9b8442347f2ab05b9e999748`  
		Last Modified: Tue, 12 Nov 2024 09:03:49 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:b4b757d748fa726c2bd2cf871ddcb888abc2629d4d810d39f96d38a8459f2f64
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
$ docker pull buildpack-deps@sha256:2a1bd17b9e1179e78a37cda2c95e93951c6eb4a1124428a1956a423ea7e13d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140355694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543cc9466a8dcd1ed3904970a2c6b3a94865825d52f80c81fd62f72298710c59`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:723f7d6ce61509bbccf2af45aa75a4c5cd83b188d6e85822321cdc68268417bf`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 53.2 MB (53226763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1538514cb923497c68c854e6f9e45945ca05f4a0f5a179472e7f81b1ee0cfbb`  
		Last Modified: Tue, 12 Nov 2024 02:38:24 GMT  
		Size: 20.6 MB (20597910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa039132691ce2d5258743dd8ecefd941d85955a38506ba77c3fb6d2f554298`  
		Last Modified: Tue, 12 Nov 2024 03:18:08 GMT  
		Size: 66.5 MB (66531021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:006c1a4f157ca8332c37cfc903f51fe99c90c9e534a72cac860f9fb8365b84af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7623030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e23d95e10f0fa5f7d7bb7c419adb4b4efc852e89db69d30cfe318be44e81af`

```dockerfile
```

-	Layers:
	-	`sha256:f66b32ff82c0df69c59a686e88a8d08a6ae82c59c9462bd2249d9876a847eaca`  
		Last Modified: Tue, 12 Nov 2024 03:18:08 GMT  
		Size: 7.6 MB (7615716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6de0676f525b54096e36412a85f3c6647ed8bc777fe9cf6dbc7352a34d09c157`  
		Last Modified: Tue, 12 Nov 2024 03:18:07 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:8d8e3fdc5829aed1b63ea33f435469be1517cd603483aabe32fe43e31b9b84e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133665306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16cf4cc1b27f69e3f63ac0b103f60c88fafda72f2853563fccebf54e71da792d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4ff391534f557bd19067799d6e6b7e386e43cbf7d061a795a182546eb2145e99`  
		Last Modified: Tue, 12 Nov 2024 00:58:57 GMT  
		Size: 50.1 MB (50091523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d129d70e5af0f50e5354ff02342f42eba97458b43a0df2209f72566f664a4a`  
		Last Modified: Tue, 12 Nov 2024 06:29:56 GMT  
		Size: 19.6 MB (19607774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a342b984b6752601eb44f7fa9cc6f866d747d925571f5c63f8db143a85f2fc46`  
		Last Modified: Tue, 12 Nov 2024 11:32:48 GMT  
		Size: 64.0 MB (63966009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:55cb1fe2158d176fa5dcb4daeac857818c62b2e9366dc456933b6f31765d4469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7623355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5037e5aaa8ca5213b9ca8057df32fbe8e1b104c09243d715658e4a29226b356c`

```dockerfile
```

-	Layers:
	-	`sha256:cb82e81672aacf72d387cbc2f43da98514547c58c1480ebf7b5835d0e3fb28c7`  
		Last Modified: Tue, 12 Nov 2024 11:32:47 GMT  
		Size: 7.6 MB (7615982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d98118b2ef6e507ba56174c04789b05d0d96599c8d4772447261b2491bdffb5`  
		Last Modified: Tue, 12 Nov 2024 11:32:46 GMT  
		Size: 7.4 KB (7373 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:da6fdb925b5de7f3beaaf9f7138cfab36ec0cbfdcdabf72cdad10c36ca194511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127859410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:290b778918d3f0776bc82777549e9e66202608ae29931c36c3a39cb680f69433`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:7b183110c42f24584c122a8e76db1e925d5fd8b3489ae273dbca0b0cc3bc0090 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a5589eaa1616610f1da5585cd04faf9e418fe913dd4e9ef827abdbe93f8caa5b`  
		Last Modified: Thu, 17 Oct 2024 03:10:29 GMT  
		Size: 47.7 MB (47659640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a052304c7554ffebe70b582d4e2eb7d1d61098f5f96c8c9603940278d081561`  
		Last Modified: Sat, 19 Oct 2024 00:58:30 GMT  
		Size: 19.0 MB (18971211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfcca10ec23fe707cc08f7ab790838065704861f60c0f678095482cc25ef593`  
		Last Modified: Sat, 19 Oct 2024 06:40:45 GMT  
		Size: 61.2 MB (61228559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a9757a6eef12d8e4457f63d8128b0b8c16a0230cee675ce2af94935916d16c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eea98d047064758984f353ad89edcd13307d0700c40c376b60bdac9d397af66c`

```dockerfile
```

-	Layers:
	-	`sha256:7a93cf475e613ba4986581169e51da296f5eab2d1af2eec23ca1a4ebddd8c326`  
		Last Modified: Sat, 19 Oct 2024 06:40:43 GMT  
		Size: 7.5 MB (7486524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20c2dfc26ee7918a49826fed2ffc0d36d6dd4dab8b3cc5d2ec3b13523d04f02c`  
		Last Modified: Sat, 19 Oct 2024 06:40:42 GMT  
		Size: 7.4 KB (7386 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3b629d663679a2b2b40868852c5dfbda509fd66bd6f901cdf256592706f0da24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.3 MB (140280895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6f779d0370a31853b4d9b6ad68485f28d2bdeb59641df30882b6ee54f6a915`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:5d91cfda460a83c91802e918bddf6951978599b67dbd5e3c0a492a53f20d6ad6 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6f4ac25c892a8a547634a70e67af9f356a5f2b1f34e7c78d52074f2a21999111`  
		Last Modified: Thu, 17 Oct 2024 01:17:18 GMT  
		Size: 53.6 MB (53599725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b74f65518d0117b47b1d80b0bf8981ebb7ddb04cdeeadd261af699b6e5d50`  
		Last Modified: Sat, 19 Oct 2024 01:12:15 GMT  
		Size: 20.4 MB (20382473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b125c1d7d6d0668d3d31049e15ed26c5f15741a45a407eab00423ec50972be12`  
		Last Modified: Sat, 19 Oct 2024 05:20:09 GMT  
		Size: 66.3 MB (66298697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:981b9d0b27672f9ae58a479116f2d44a4372d329f9e65910623c50857c7f2012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7499825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83b16a06a55282321f67d9ada42e21d02d811ecc3a3fc386acf84684d93a15b`

```dockerfile
```

-	Layers:
	-	`sha256:e31fe82ca59e0b11c21807625cd32304cb7c70ed6c502b0b98468e11df80130f`  
		Last Modified: Sat, 19 Oct 2024 05:20:07 GMT  
		Size: 7.5 MB (7492419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:859f0a00775cceb04089b3a21a3466d9b86a3ba87b410318a08e54198cb54287`  
		Last Modified: Sat, 19 Oct 2024 05:20:06 GMT  
		Size: 7.4 KB (7406 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:17f77e1c82b223cf3f38382724d4a83f63a07ca65e77321db1ec9ea444466eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.2 MB (144160990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558df670cd95356ddd37034014ece4572b6e5b0c6d1d40dda1c173413f7e507c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a04f0591b5521dc9360454fa2fd6b21d9b7d989bb4c88327ad94f8282af3b267`  
		Last Modified: Tue, 12 Nov 2024 00:55:13 GMT  
		Size: 54.1 MB (54095157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914cc5c9bed5c786b85a6e40864cd3fb4af442dea3455ca88a01cfa26707d8df`  
		Last Modified: Tue, 12 Nov 2024 02:38:04 GMT  
		Size: 21.7 MB (21722460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c207d20a70d18f9e95ac6b10fd58bbc5d2a036845c50cdab8e2fa983066a990`  
		Last Modified: Tue, 12 Nov 2024 03:14:35 GMT  
		Size: 68.3 MB (68343373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a7af66e9bf190aefa86e1f76abfec0fe4c44a04ddbc03d55ff18c4ef7c863f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7617759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3fbadbc2198b4e131475280b87df5241639ec83a1ca1198e19eb4022f3dc1a`

```dockerfile
```

-	Layers:
	-	`sha256:cb12d5a0477c96ee0bf9ebe5630d302496423079ffd94280db676664955ca33a`  
		Last Modified: Tue, 12 Nov 2024 03:14:33 GMT  
		Size: 7.6 MB (7610468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:534ad46e5e83d3c45f05ba6b7886be6e67993ce4f589506783f49296f2c60595`  
		Last Modified: Tue, 12 Nov 2024 03:14:32 GMT  
		Size: 7.3 KB (7291 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:78d50bdb37e5bb8ce65015b943145de8356d61c7bf9ac0d2b70b5bb19d61592f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138151112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c40a1f4ab862506927452bfc655b5b498b376a47d0ebbd5c7fe468eb7a88db`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:7540ed5b693bb419df5aaa69483f55c19bc0566d076c5e65757a0a6fe38375a3 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bd6795a0a311ac784071ff263d2b83d646956234334d40fe908b91a1dde11378`  
		Last Modified: Thu, 17 Oct 2024 01:22:22 GMT  
		Size: 52.1 MB (52128468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bde6977c24ffe15c007c6606184010ccb92606e6158cbd76d8e770997debfa`  
		Last Modified: Sat, 19 Oct 2024 01:01:31 GMT  
		Size: 21.0 MB (20966640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdea9feeed917171d6d06a6129bb34f0f75c8fdb0fc8f9755f248adca6eee285`  
		Last Modified: Sat, 19 Oct 2024 02:14:28 GMT  
		Size: 65.1 MB (65056004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:81190818ed7d83b0f92ee66dc853e7c6f22b9535d8e52f4f00fcfdc4354973ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 KB (7159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f37bae74959741f2259d72bed0704bd028bbb2ff4414f68912774344bbdbf3c`

```dockerfile
```

-	Layers:
	-	`sha256:c02dd3eab5f5e9db4c0f38c6e763e61d6cf4e72819705f3060c07ec5c7819c76`  
		Last Modified: Sat, 19 Oct 2024 02:14:21 GMT  
		Size: 7.2 KB (7159 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:fccf093e3bb36008832e5ec58a51f1ac32d0d886c98f75c4f37ebb863d6885a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (151013309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ebeec5bc9376d17e01d51bb7962444e7575f3df8a16e27526ab9a4ffac838a4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:554b3bf5ec10b22cc962f7afc042e96c50635c0e2b0d817544a202afc2a52711`  
		Last Modified: Tue, 12 Nov 2024 01:05:47 GMT  
		Size: 57.2 MB (57193598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08187472bfe4fce6e3b2fc2951e231ce30c71f70be1dc829ad73735e312d479f`  
		Last Modified: Tue, 12 Nov 2024 08:31:04 GMT  
		Size: 22.0 MB (21983916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5445db0db78751088bfd85b5a3ee628352f9d78288ca29fed636c550e50e6235`  
		Last Modified: Tue, 12 Nov 2024 16:12:54 GMT  
		Size: 71.8 MB (71835795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e94f6be5b6eddf231fce0e6606fd38a9209523a97cc3e95f0c1f15a4652074c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7629581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46fa744652a5277bf95624921ad212b186a9d9c17913d20b62f2bbb489029e5c`

```dockerfile
```

-	Layers:
	-	`sha256:1dc404b8f0d7ebf05e25893e3c6825872d16ff0cae8abaaf48f9a7649d8bff42`  
		Last Modified: Tue, 12 Nov 2024 16:12:52 GMT  
		Size: 7.6 MB (7622236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b0339d7f4b34fc047dba3dca04265fd1aa21572185158b43c3d4d366e80585d`  
		Last Modified: Tue, 12 Nov 2024 16:12:51 GMT  
		Size: 7.3 KB (7345 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cb2e75552a2d042a659ba547ccb0609e06f697798884a74c6805ee8b1ab38d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141797604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9b44ffe80f44627eca35eaa520ed53a92ed54585062c43ba93198f9ec59a05`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:fe7c88cb45fa7097d71f60ba00c0d6ad76dd030e8e34771e5ee3735b59a4d6e6 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:53440987c87b8deb9090e5298bf822ffc945f186eb4c81cecc0ebf58717ca549`  
		Last Modified: Thu, 17 Oct 2024 01:51:55 GMT  
		Size: 52.8 MB (52808844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3816f9124671541da45f7e11a0a925de47e719482f5bcd085247ecdcb8c613`  
		Last Modified: Sat, 19 Oct 2024 00:59:12 GMT  
		Size: 21.7 MB (21656188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cc2aa2fcdc4addb1b596c3dbc6f3699d60107644fd49f54f3050356c21437c`  
		Last Modified: Sat, 19 Oct 2024 03:48:52 GMT  
		Size: 67.3 MB (67332572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b270aaa7768e4a2d159ff7b5f42829b62c59d4ef131517f86c9ae12564beddae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7494252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942bb4de50d03290e36368d5b3922ed61f5adbe88b45bdc98fe4f5ece352669e`

```dockerfile
```

-	Layers:
	-	`sha256:be9cc770647715d3212ab0a996c38d93ff0e416f9d91de05c1000fc1ed5dc2b7`  
		Last Modified: Sat, 19 Oct 2024 03:48:52 GMT  
		Size: 7.5 MB (7486926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dd9a3268144974562f1606345489a7a1d2317d957179ab65d447e065d5173d3`  
		Last Modified: Sat, 19 Oct 2024 03:48:51 GMT  
		Size: 7.3 KB (7326 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:314578a876bdd46be55c7384f57a459c7197175df7e70c5e969f54eeef74beec
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
$ docker pull buildpack-deps@sha256:b0afb66526d240be44af24d222b1ce19acfe78052893de838fda19973402d501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.4 MB (369418391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667b3261aaabd8a7375c74cad935ce525d633924294649dbe9843ca6d64b82be`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c6dd4b778062640e2abc4c889c6db9feecceff7f28c2100dcfa570652558218c`  
		Last Modified: Tue, 12 Nov 2024 00:54:59 GMT  
		Size: 53.3 MB (53319444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73df9c0ffd5cfef9ed63d0dfdae57285f543f78320d947c5c4c2ab1422641cb3`  
		Last Modified: Tue, 12 Nov 2024 03:14:01 GMT  
		Size: 20.6 MB (20596172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0899f4ba4649838a893d7f1a70928afc27b147ea5051eac0853a716ef24ac8c8`  
		Last Modified: Tue, 12 Nov 2024 03:58:48 GMT  
		Size: 66.6 MB (66611604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ed16753ac0d236589a2917598d5bb24201a1ceaea372a998220ce50b9205de`  
		Last Modified: Tue, 12 Nov 2024 04:55:30 GMT  
		Size: 228.9 MB (228891171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1b890f2498c3d06d74a7599cb7d559795eec3be2ba36f8a137314885003385aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16842737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c73e51bc26aec5f86f0bc30b85d6af0a0476863bd7bcbefedc0bc2678c495610`

```dockerfile
```

-	Layers:
	-	`sha256:3442b9a36e4134cf6b67919c2d04b50476534f845c966ca8e6fb00848e915279`  
		Last Modified: Tue, 12 Nov 2024 04:55:27 GMT  
		Size: 16.8 MB (16832561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:540e6d55dabb7696f8459f07f029499d23edaa473f9379257c196530e33b6b4e`  
		Last Modified: Tue, 12 Nov 2024 04:55:27 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:64f60ab32c8ad2e44569bd34aeabfcbcae655596ac34599c5336dcb78f1347f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.7 MB (337698112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fef2df89ec55a84f53ca077a2e2093c773663a924f03a53bdb6116f54dd565`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:48142c53989e584e5008e025d7add416317666ef57f1383dab96cb3b5dd1610c`  
		Last Modified: Tue, 12 Nov 2024 00:55:48 GMT  
		Size: 50.2 MB (50178305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677e719f1a345c9d868951b12d49877be0a8ce88c74c1d28554e382cb36c8fb0`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 19.6 MB (19609396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a80294a22345764a6f713791d5e78ceccbfde6983b0bf68a23d16e31cb7a8d6`  
		Last Modified: Tue, 12 Nov 2024 11:31:21 GMT  
		Size: 64.1 MB (64064343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeecbd78ab8f389d36bc7c389a258f35fcb1d7c525c852264f355392a01b52a`  
		Last Modified: Tue, 12 Nov 2024 13:57:37 GMT  
		Size: 203.8 MB (203846068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d6d24b2e38e21cc1d214a4e09d6ef1cda2fb1f0fffa2e118fef221c726e42ede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16634683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da72b7f704e230a29b6d8886bd354cea7afd55b586897a8685011369124695d`

```dockerfile
```

-	Layers:
	-	`sha256:5cf2be7911debe59da7ccf2740ddae1696946eaf5fec6399bba7ceafa9082524`  
		Last Modified: Tue, 12 Nov 2024 13:57:33 GMT  
		Size: 16.6 MB (16624447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a10c1a45b73521ebcf10c889a4ba4d096cb8325e02ba6a3ce6727a8947f2c49`  
		Last Modified: Tue, 12 Nov 2024 13:57:32 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:51225fd5a278a81a1c2e8baf0a39084f097446e073dd1cab41c44757e14c006f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.3 MB (318326856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c31c7bdbc1cdd6c1b92e543e9f56aa00f75503c3f8522f27070a52efdb4d313`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:bf9375f2b0e5c66c0a1840e13cfa8b3f0aa55934d9c92c13e479c8cf7909e923 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cf1d8a933c6efa9a7129c6faf202eeab8feff677f32fbc0037a3ab76003edcf8`  
		Last Modified: Thu, 17 Oct 2024 03:09:00 GMT  
		Size: 47.7 MB (47691399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5bb5787cc9d2878988b37d2049fa1d6b67ff3450f012cef9603dcff05b03ef`  
		Last Modified: Sat, 19 Oct 2024 00:57:32 GMT  
		Size: 18.9 MB (18893656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f7ad36a85c1a25fec35fecdd0c231974acf44c7aaeec9321464cf908e0e452`  
		Last Modified: Sat, 19 Oct 2024 06:39:20 GMT  
		Size: 61.5 MB (61460990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b53af5a773d7f35e45f47783bfcad7fdfe09493d624315c463438ee3dd9f85`  
		Last Modified: Sat, 19 Oct 2024 08:12:52 GMT  
		Size: 190.3 MB (190280811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a1176727d50799e82d4d2bfa3c69443f0367037f3feabb08f8d57c4d756d9f41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16421324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ab1f5a6bf51385b18a4b74c31ca3c7819e926eba8582453cccb6dfda27e50c`

```dockerfile
```

-	Layers:
	-	`sha256:1851bd99397931249134eeccbef9025844d241e61f0ab5fbf1a0e8ec2a0aac9e`  
		Last Modified: Sat, 19 Oct 2024 08:12:48 GMT  
		Size: 16.4 MB (16411076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef72ff3aacc21648a8dc4406f49449fc8d535604650bcc28f2cb04734076428c`  
		Last Modified: Sat, 19 Oct 2024 08:12:47 GMT  
		Size: 10.2 KB (10248 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a5bff4e6897ef7ce3d60f235ece06477a670c718938744616f5c5be5f3cc0dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.2 MB (362218506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4617705cb588626ef2ee3fd18d59a3c8c267abb961000229b9cada35dd22a8fc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:58acae53f12429504dea737cd60eba46c5f2eea862974a8d8fe218c17d285565 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d246237d395a465ccb5ede6b1a321d43a78766a62bc93015a0368a88624aedff`  
		Last Modified: Thu, 17 Oct 2024 01:15:57 GMT  
		Size: 53.6 MB (53629485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b80bac00a06288366529b5187b9485c685d4f46018bcb866049abf9f952247d`  
		Last Modified: Sat, 19 Oct 2024 01:11:43 GMT  
		Size: 20.2 MB (20196615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19663fa8e0a57915a50484edf1e2599200b05cd9b029d04f6246f46e4ebd7b8`  
		Last Modified: Sat, 19 Oct 2024 05:19:11 GMT  
		Size: 66.6 MB (66554364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a1930b82ab676514849567fb2f84c77abe6dd46e00fdaf27bdffdd5e50852c`  
		Last Modified: Sat, 19 Oct 2024 06:19:49 GMT  
		Size: 221.8 MB (221838042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:aee10b071d72be87195fdd239fc32f4bc897cf5365082395c39d748923726e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16719540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce06ab8b69758fa40926415c0cc6e0fc487417847973ce13cf61898b34595a31`

```dockerfile
```

-	Layers:
	-	`sha256:0c705747a331f205ed3932bd8aebffa27283a5197af7462eb8b34649f08b2b6b`  
		Last Modified: Sat, 19 Oct 2024 06:19:44 GMT  
		Size: 16.7 MB (16709272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88f34d6a5ad6f6573131d992417c533e6d9e3aa6754dd91f84650909955ea149`  
		Last Modified: Sat, 19 Oct 2024 06:19:43 GMT  
		Size: 10.3 KB (10268 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:174aa49a8c627409e7b2ef469e0b4ca424e1d67801529a24e00206f67c85e020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.6 MB (374625880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e991a9111b7923adb2bf1517a0cea45e0e2cbe21c971a883abc5d20fe7018c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:266f316e766c7029b1cbb65159b6d9ea1da28d00e28cf109ea069ce95b082ac4`  
		Last Modified: Tue, 12 Nov 2024 00:55:10 GMT  
		Size: 54.2 MB (54192046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24546888a84a1c2171ba5648f213b4d3b8fee560f454ad1c12f583f6ce895c81`  
		Last Modified: Tue, 12 Nov 2024 02:37:52 GMT  
		Size: 21.7 MB (21725392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885dfc308254678967ab6d79ba6d40d73a4ad263c111beedb94327edea737b17`  
		Last Modified: Tue, 12 Nov 2024 03:14:27 GMT  
		Size: 68.5 MB (68538589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470064ab8c694d08e8b01d3ab58e57e6bbb9021d73b77eab103438c7c9d1b9de`  
		Last Modified: Tue, 12 Nov 2024 03:59:40 GMT  
		Size: 230.2 MB (230169853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c68dc1085e970079c0dad9475c90a626f3fac854d399d14c64fc0624e1214a07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16812358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c69c51ca15442a3ea0f50ed9b720d7bc599cb88cfe9ea50099b42ec77303de`

```dockerfile
```

-	Layers:
	-	`sha256:e8d60b7da8728b26a8fa539127c6eb8ccfc4ff307613730c7801c4e74932bef0`  
		Last Modified: Tue, 12 Nov 2024 03:59:36 GMT  
		Size: 16.8 MB (16802204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5db9b50ef37135bc668d6adde1f571e925b918ed88cc1254591868dd645594d0`  
		Last Modified: Tue, 12 Nov 2024 03:59:35 GMT  
		Size: 10.2 KB (10154 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:7aed501446d1d4aff5e4e665344ff39c2bb23697f79269ade9d17d43c74bc637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.4 MB (346369313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d558ca969f15110f47b12e6e5f8ac0b3c2bc1d5aef4bccd85c13c7d012683040`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:8ffd9575546e69884562db46178b841df2ba1ed04549599485b7c502f81ac4cc in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e3c6aca2e6ea9e1b19b3c46a60581e28de71137e5bd8fe9c8ea62365a8e75d74`  
		Last Modified: Thu, 17 Oct 2024 01:18:46 GMT  
		Size: 52.2 MB (52157899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35efd481e6347988498fa292e64d8b2f0d728f327f48bccb1d2c2bf371f2f1e1`  
		Last Modified: Sat, 19 Oct 2024 00:58:29 GMT  
		Size: 20.9 MB (20887623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10d42e894e27bd8661997e28ccc989f4b18c73e3892449a02653f995d796aea`  
		Last Modified: Sat, 19 Oct 2024 02:11:09 GMT  
		Size: 65.3 MB (65280292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5494e53db7cb17f11f8f3553b0b8f89e494429f535472ab40c3dc0a4a53a958b`  
		Last Modified: Sat, 19 Oct 2024 03:09:12 GMT  
		Size: 208.0 MB (208043499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0c7f47bdc09a05b6d948bb27b33411f3b5a300b2c8d1c54d84eebe0c13592d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52a53cd41b52a2ffac4c7c5eff91689862f82eab42ecf464a1ad8ccafa36f61`

```dockerfile
```

-	Layers:
	-	`sha256:c6c4c3b65b2f2ee5188b595c005cab57e11fa88adc238818500a0f9d289bb37a`  
		Last Modified: Sat, 19 Oct 2024 03:08:54 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6e1614575430aae725ce4d1ca72a021b64b14a73524639c6866a13aba370b80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.0 MB (378020992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972288b37cca39db49db1bfbe29a851813a8543f0a7f4c72ce65531923b42a8b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:3f30d2b91e08061eb3185f2f9c67756024dc8f3e6cda74d75d6ae54a603cdd2b in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:df36361b5ac72face21de9a14adcec98ba3abb2261a8339bf516725d8753f43e`  
		Last Modified: Thu, 17 Oct 2024 01:22:16 GMT  
		Size: 57.2 MB (57176824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30f3cdfb0755564cd3c4456a7fa23e621d79e4f8f43bd8107c734f66d381334`  
		Last Modified: Sat, 19 Oct 2024 00:57:49 GMT  
		Size: 21.9 MB (21944061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fc954d509992bc0347fcedb989b7696ca6b5029587c5a3cacd05686fe99e03`  
		Last Modified: Sat, 19 Oct 2024 04:08:51 GMT  
		Size: 71.9 MB (71893560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e8fc7c4002604d4ecd95f73b88e6577ffdafa0c5d8add4adfe85a32b924574`  
		Last Modified: Sat, 19 Oct 2024 05:20:49 GMT  
		Size: 227.0 MB (227006547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e5a372eadfc10bc82dad638f92376f112fff82b71cd161e5b05c835e3e4d7423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16621262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46ae6569046be118b2021b37e251e01f3d851d6b370fb2e380a09f956b1c437`

```dockerfile
```

-	Layers:
	-	`sha256:4b845df74b1833d65eff42db4f1e60c04ccfa5b2e99372f560c60ba8e33d6eff`  
		Last Modified: Sat, 19 Oct 2024 05:20:41 GMT  
		Size: 16.6 MB (16611042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:080d4475f5f734ac76d094f5229cb78e77712607292807a5e1b8fba7c54e82aa`  
		Last Modified: Sat, 19 Oct 2024 05:20:40 GMT  
		Size: 10.2 KB (10220 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:9170b718174b1a2155dc6f1f30be5d257ea77bfb5cfd20c8b882eb76bd970ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.9 MB (449863543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578f59755f82ae837d05d043953beeddcd5bed8e73b690b8f7d707e36ed9644e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:9748961f840a27ae3342039309a28acc84e3a482f5ca3ece5bdaf9f92e7ebe33 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:29cf887cb660615390407db841ad4c44be2414b9bf999ba668d93a8305675c7e`  
		Last Modified: Thu, 17 Oct 2024 01:14:47 GMT  
		Size: 51.6 MB (51562685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de12fa48532c87115805a1e3efbbdd980575096676ddd00868f642d72782b610`  
		Last Modified: Sat, 19 Oct 2024 01:03:17 GMT  
		Size: 20.0 MB (20023981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c05579e9b49f41a2b6960286d8ab9b1d090127915ab4b5f2c9ec35e3db7815`  
		Last Modified: Sat, 19 Oct 2024 03:48:10 GMT  
		Size: 65.8 MB (65756980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1c1438a38b6b5f19898954943b519c13357a75b5de527c10fdfa839a2bf9bb`  
		Last Modified: Sat, 19 Oct 2024 05:19:52 GMT  
		Size: 312.5 MB (312519897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9d4efa39a2089a0bae14fc598dc2be9721c56cf31ca6d013b630959dd86d0a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16684099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c950fcfad2f9ac619e283071159fabbe0d2519f685c971de572607a5a2ab72c`

```dockerfile
```

-	Layers:
	-	`sha256:c00879de8cdfbb4f86a8411d81ebbb57bfefc3b7b5517bb5e81cdec0f5d57951`  
		Last Modified: Sat, 19 Oct 2024 05:19:13 GMT  
		Size: 16.7 MB (16673879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7759997ee312035b99e28a615c8b12688bb5567df93ee0be4e659c908478b864`  
		Last Modified: Sat, 19 Oct 2024 05:19:10 GMT  
		Size: 10.2 KB (10220 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:03ae369846cbc99feaec0d7a675c3f1cb296806fe18be3ea3f2b2fcd60ecb688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.8 MB (343811634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2955362ae47bf0486452d86b59e314d1f8357dca737a96af3e6f917fc1c7969`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:2f1a819570e851a9bce2342f32c7927abdb02af08d5e469e6f5d41a193235bb2 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:79590eb16acf1f35f7a00e8c30e7daf7ed5d8bc9d65ff782665704f532af0ac0`  
		Last Modified: Thu, 17 Oct 2024 01:50:44 GMT  
		Size: 52.9 MB (52851981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf56c8e1a853602c0af0f40a2561d6ca90c547c99b9bdd2c5349a88e1f5cc1a`  
		Last Modified: Sat, 19 Oct 2024 00:58:05 GMT  
		Size: 21.6 MB (21639639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a7102bce19ae53b519fb58ec97dd26aadbdffdfec95cd2613f51b842e60866`  
		Last Modified: Sat, 19 Oct 2024 03:47:42 GMT  
		Size: 67.6 MB (67567932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006e2316904bd5e5d8b5be83f2d3c16ffc8b744bd23f895fab2465c751a090a2`  
		Last Modified: Sat, 19 Oct 2024 05:06:51 GMT  
		Size: 201.8 MB (201752082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ba7e3ba1bbeac3a6078f008e5ee17b68529098e3909600dfbe90edb605f54c0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16414228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc84b27183ff88f33658ac103e14e91bb216a76083e15c060fef435fa42bfad`

```dockerfile
```

-	Layers:
	-	`sha256:1ee265a8788e328e9fef94039d90ab4df6d624dfc385d1e5faa95efe0c935af1`  
		Last Modified: Sat, 19 Oct 2024 05:06:49 GMT  
		Size: 16.4 MB (16404040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:306d2621686c7e09b57487558deeb4f574d7074bcde002751c60c8186e07ee0b`  
		Last Modified: Sat, 19 Oct 2024 05:06:48 GMT  
		Size: 10.2 KB (10188 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:1404bcfbcdcb783c0c131bfaf3a6e2b6d8789eaa3160d997450ecaadffa8b4da
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
$ docker pull buildpack-deps@sha256:9f132228a17ef7148bdb181e503e91853e85e87c2bc91361f6705a2ea4818832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73915616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33126cfb84f42e1dee4d3bcd8e62d6e742b0c0fc0da59e149a079f4174ed740b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c6dd4b778062640e2abc4c889c6db9feecceff7f28c2100dcfa570652558218c`  
		Last Modified: Tue, 12 Nov 2024 00:54:59 GMT  
		Size: 53.3 MB (53319444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73df9c0ffd5cfef9ed63d0dfdae57285f543f78320d947c5c4c2ab1422641cb3`  
		Last Modified: Tue, 12 Nov 2024 03:14:01 GMT  
		Size: 20.6 MB (20596172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:39c0a59346b52c497cdfee9ee501696a0137d33c4d869b8ccfb052b35a48c57f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4059772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d64c3f557019664b8ed03939a488b65f662ae5ba8df3f8558e7eb7f4ef96f1d`

```dockerfile
```

-	Layers:
	-	`sha256:6c5e88c9e7aefc1e66a2fb244bc4a7ee4a01996d4d1643d54fd9141b9d68c098`  
		Last Modified: Tue, 12 Nov 2024 03:14:00 GMT  
		Size: 4.1 MB (4052968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e06a147cc0d21461ddf7350b95eadd2a56c4f93dd20e46f3562015b2a9cc19c`  
		Last Modified: Tue, 12 Nov 2024 03:14:00 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:6fa397aad3f688ae8c5a6a419b92021b1cdd17421ded456fab3c2ba159b1728e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69787701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4def3959c1ec2cc47ca9f650e6e392ddcdf199ed79296fefa9f23c546bc85b9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:48142c53989e584e5008e025d7add416317666ef57f1383dab96cb3b5dd1610c`  
		Last Modified: Tue, 12 Nov 2024 00:55:48 GMT  
		Size: 50.2 MB (50178305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677e719f1a345c9d868951b12d49877be0a8ce88c74c1d28554e382cb36c8fb0`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 19.6 MB (19609396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:957883ff2bb35b1ce0198b37996e8b3b914135501561c94a4a330818e42e78a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4062054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e70fea3252b42f59d8b501dd5ad764980a1381758257617d06e4dfa151cc2c7`

```dockerfile
```

-	Layers:
	-	`sha256:88ff8e75bfa6830f20cbe46c2c6274c66debaf6f7cb42e797f70f8ed1ee639ac`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 4.1 MB (4055190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:289839fa0d0c8815427f524a3c398ca48fb266a4cc30b70e149da06d2f68dec8`  
		Last Modified: Tue, 12 Nov 2024 06:29:06 GMT  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e9f57fadeb4e2571a3ec639deb0bc50041f8eb09f1c35e7dd31f63f51219c7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66708282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a041b6b0da1491b1f95275953492d2a5af327c22639fae585debed4b0683d27e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e17a4ae99f3dc5642f3037bdf67fdb8d526cf44879dc2a2a82dd78799b94cb90`  
		Last Modified: Tue, 12 Nov 2024 00:59:40 GMT  
		Size: 47.8 MB (47762858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0690a3ea44bb2abf7747807b4adbbe717ea3308dcc90d88289979cc43a641049`  
		Last Modified: Tue, 12 Nov 2024 16:01:31 GMT  
		Size: 18.9 MB (18945424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:43d8aae958a0e128d324dc93a72825f729ab6fa94ca19355525166bb05a47f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4060852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b10f2357762de298e91d49a699d21a40cda9a432c28280f401740f16e5a614`

```dockerfile
```

-	Layers:
	-	`sha256:bf93bf2e4fce3088d42a757f8456cd7a2023638444e133ff88b357911a40ea9a`  
		Last Modified: Tue, 12 Nov 2024 16:01:30 GMT  
		Size: 4.1 MB (4053988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:751e72f96ac24e34e31ae67f31c52b074761c75e5706d996f2d7158d36e3ecb4`  
		Last Modified: Tue, 12 Nov 2024 16:01:30 GMT  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f2d64356db4518efc4b1d5c851bbec90bffc5a3786a1d40a66641c2ddfc581d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74010502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755881583c95b82ca8b14fb557a3d30c6d7372621bc567aded061824b5eb9e13`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0c8e2196f060907b4d5381cc165d86913c4b9e9c632b3596563398b5e178a84a`  
		Last Modified: Tue, 12 Nov 2024 00:59:55 GMT  
		Size: 53.8 MB (53759747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2180b05bcdf8eaedc4db9cf7f65afe026827aad32c4e4b7f24679e6ea2c63305`  
		Last Modified: Tue, 12 Nov 2024 11:17:08 GMT  
		Size: 20.3 MB (20250755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:88c0a9ebb6e4d36deef41d358c47e1c05da025bfee528155d8dd8ae4a515c78b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4064747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23d1f98393785b001948920b2a88dc59d5b07744d55dcaa5407498fb1c5c887`

```dockerfile
```

-	Layers:
	-	`sha256:cf4589ea08d8203c40a828f62b71489ecadea32a9e41505f049036274b6fa84a`  
		Last Modified: Tue, 12 Nov 2024 11:17:08 GMT  
		Size: 4.1 MB (4057863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6e1e9a818425575ef20fea5def0c73f7b9ed82c20a2be689147698cbb1b6340`  
		Last Modified: Tue, 12 Nov 2024 11:17:07 GMT  
		Size: 6.9 KB (6884 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:713ac9d8ce038686ba88e304844d03029927103f715e36c6e3e7e643f648cba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75917438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcbbb27c071a87a94f9d4da6a554ba80e231a4d61d781ef5427f2ea0cb7bfad9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:266f316e766c7029b1cbb65159b6d9ea1da28d00e28cf109ea069ce95b082ac4`  
		Last Modified: Tue, 12 Nov 2024 00:55:10 GMT  
		Size: 54.2 MB (54192046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24546888a84a1c2171ba5648f213b4d3b8fee560f454ad1c12f583f6ce895c81`  
		Last Modified: Tue, 12 Nov 2024 02:37:52 GMT  
		Size: 21.7 MB (21725392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e72acbe40d1dada9f63a05e02f9a246749c53f9785c0f442cc4a3c00ab26b48d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4055490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58971737022f0686ee08a7e75b6b49ac4d35e293b2ac50c454cd02dac2be18d`

```dockerfile
```

-	Layers:
	-	`sha256:f398d7abacfae0299acc85184a23c92cb8040f679acc31f49830129acfcebcea`  
		Last Modified: Tue, 12 Nov 2024 02:37:52 GMT  
		Size: 4.0 MB (4048708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d240f2a814476b467a314a67e75244714b4479add937403e3b8169171e9cce8`  
		Last Modified: Tue, 12 Nov 2024 02:37:52 GMT  
		Size: 6.8 KB (6782 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:62e1a2cab54ce402ef56d67975b9e97f7db49042e7d9bcf2803dad0e2b4f5507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73225428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f90f18670b8a0f2f53c92f8dd49e6e04300c5b5b5ee0a08f2c595286336db07`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1f6d00c97864e98dad498c4c1087cda2fb16f2ac6e7a71ac1353418dd4215995`  
		Last Modified: Tue, 12 Nov 2024 00:59:58 GMT  
		Size: 52.3 MB (52275237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ee73bc743170bb5e4087d57c95a63d610fb1282220d73ff90af4707b831d99`  
		Last Modified: Tue, 12 Nov 2024 18:03:00 GMT  
		Size: 21.0 MB (20950191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2cd9138da59d486eee86b97f0b2ef5c327cbddacc8555d0ca1e2f100ddab0c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 KB (6635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e8f2688580c7be9086b175b4a45597708a571c9d0545210c877212967e0e9a`

```dockerfile
```

-	Layers:
	-	`sha256:6c68010a95014043302ab3a4f944d5dd5ce7882ce431430ff613035bcd549ba7`  
		Last Modified: Tue, 12 Nov 2024 18:02:58 GMT  
		Size: 6.6 KB (6635 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a4f1105859b8534b986cb747f39eeb29301d977a7735a4d128f7a9b8cde3fde6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79301505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b6e4d2082fca0422d715db56ed40d43739efbf27aeb90a1bed244f273c5c7d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ac2d911f8489db0bbd6f313128660ffb4f315b3d99baed39d7128c198fea25b9`  
		Last Modified: Tue, 12 Nov 2024 00:59:35 GMT  
		Size: 57.3 MB (57309355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5f3e8aa1353894772b7fd9d91dc6448cf8573234fedf1ba1c8596471c52519`  
		Last Modified: Tue, 12 Nov 2024 08:30:11 GMT  
		Size: 22.0 MB (21992150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b2a081bdf1d2cc2fd96de5e53f9ad7551c0c1a4edf1d7e6e4e7b1b039d1a8817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4063088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f435dd30d7af7fe9206c19d35ee69326d7c1322625a8ce82779e9a352afe5b`

```dockerfile
```

-	Layers:
	-	`sha256:89d1f5a9bb4126e98982aeb9314bfa7d6ecd1747d5476ccf95e8bdadbc5a0c40`  
		Last Modified: Tue, 12 Nov 2024 08:30:10 GMT  
		Size: 4.1 MB (4056253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a91d4883ebc57f8ab63c60eb7aee2ae34e1523993d2abe0379238091fa712ec`  
		Last Modified: Tue, 12 Nov 2024 08:30:09 GMT  
		Size: 6.8 KB (6835 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:f2563b5986e1cbd6355ebaa519efbefd1ace7d95ec4dc05fb43d702a17656346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71586666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2201578f73abedc744f4f2994cc04bf7653e03e6fc71c488b56b938fa6133682`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:9748961f840a27ae3342039309a28acc84e3a482f5ca3ece5bdaf9f92e7ebe33 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:29cf887cb660615390407db841ad4c44be2414b9bf999ba668d93a8305675c7e`  
		Last Modified: Thu, 17 Oct 2024 01:14:47 GMT  
		Size: 51.6 MB (51562685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de12fa48532c87115805a1e3efbbdd980575096676ddd00868f642d72782b610`  
		Last Modified: Sat, 19 Oct 2024 01:03:17 GMT  
		Size: 20.0 MB (20023981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:07e79f5072ea67bddca2130da2f9d315fd8222cd0609708a470e88dfa7353806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b8dcf549e44ce65cf2139914167a0d0f4b1a4302bf162cbab4d7642cccbbb69`

```dockerfile
```

-	Layers:
	-	`sha256:4e7d1496ab905e4028f005f5a14166826563eecf34a3ccd9a6dd3ce4b9c1412c`  
		Last Modified: Sat, 19 Oct 2024 01:03:15 GMT  
		Size: 4.0 MB (4022143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d30c866b540503398d1018dd68b46d07f0f51532b55b00079c6208979ebb5f5`  
		Last Modified: Sat, 19 Oct 2024 01:03:14 GMT  
		Size: 6.6 KB (6616 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:584fa4000f2547dc5479f02874a482edade85498ae0ebc4df274f79647fb3ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74690422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0022a7a4ff00d7705bd101cdcaa1424b4499051d4964d76bba5c85e1d5288b04`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:01b62be41cbf7168e02a9fa648a1525f0c9095aef51faa9027bf3a9ff89c6b84`  
		Last Modified: Tue, 12 Nov 2024 01:00:18 GMT  
		Size: 53.0 MB (52980914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa52c56b4fa2fb05d933bf62d254d5f4371a5a9e6992ccf74613eefe11aaa96`  
		Last Modified: Tue, 12 Nov 2024 09:02:57 GMT  
		Size: 21.7 MB (21709508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:138584e0a4f75cbcf1075cd15e1a74e213a01490927fd7a2e7cb7cfc2f20ca9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4060697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf8abf20b9018f2f62da56f1e38c88bc5b0f2b665cd3aa99e863dd2d57a1832`

```dockerfile
```

-	Layers:
	-	`sha256:0c53ff2c3883ba64e4c118aa75e4d48c078ec5aeb46b97155e2600f1a4197361`  
		Last Modified: Tue, 12 Nov 2024 09:02:56 GMT  
		Size: 4.1 MB (4053894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1f3c58081085a03c94c082ad8f5d4a525cd67ff9c8789de1a9dd1e752fe8722`  
		Last Modified: Tue, 12 Nov 2024 09:02:56 GMT  
		Size: 6.8 KB (6803 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:c7516a6d3202303a24246bddec8a9bfd8031ffeb797b10dd3485479bcd6f431e
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
$ docker pull buildpack-deps@sha256:8ab7ea446bf8fc89524695d33da2ef73a78861037d001ca1d09acdf7d7614c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140527220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f3d6b5bdecf0d50cba2b30fcfef9e6c15ece0fec037adce41d28e2fb76e848`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c6dd4b778062640e2abc4c889c6db9feecceff7f28c2100dcfa570652558218c`  
		Last Modified: Tue, 12 Nov 2024 00:54:59 GMT  
		Size: 53.3 MB (53319444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73df9c0ffd5cfef9ed63d0dfdae57285f543f78320d947c5c4c2ab1422641cb3`  
		Last Modified: Tue, 12 Nov 2024 03:14:01 GMT  
		Size: 20.6 MB (20596172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0899f4ba4649838a893d7f1a70928afc27b147ea5051eac0853a716ef24ac8c8`  
		Last Modified: Tue, 12 Nov 2024 03:58:48 GMT  
		Size: 66.6 MB (66611604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:983d3401a2f2ef93b8b63c76b3eaea3455a247cf97c2b075dcbcc144f508ae42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7621436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767f303cc728dc43cf2a4fd72997cf80938888305f42cb037c7aabd481ab5a54`

```dockerfile
```

-	Layers:
	-	`sha256:f39cef2c674b6a5197868f663359c3af90f575a188282358e57c0aa4ce6b0328`  
		Last Modified: Tue, 12 Nov 2024 03:58:46 GMT  
		Size: 7.6 MB (7614139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32690f39b8e5187bfe3b6b0929620b5230e9bf80dafd63d62c533cf04b46233f`  
		Last Modified: Tue, 12 Nov 2024 03:58:45 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:848ee71fe2c9412ccf8a147c76f6ec97c3acd3ebf83a5f18775f0c48b308e851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133852044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e043f8c929df470ba036b874156f397c9e570d1adaf2e85b886e5efb33f5d473`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:48142c53989e584e5008e025d7add416317666ef57f1383dab96cb3b5dd1610c`  
		Last Modified: Tue, 12 Nov 2024 00:55:48 GMT  
		Size: 50.2 MB (50178305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677e719f1a345c9d868951b12d49877be0a8ce88c74c1d28554e382cb36c8fb0`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 19.6 MB (19609396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a80294a22345764a6f713791d5e78ceccbfde6983b0bf68a23d16e31cb7a8d6`  
		Last Modified: Tue, 12 Nov 2024 11:31:21 GMT  
		Size: 64.1 MB (64064343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ad4c5dc36112c0c74e99ac96fc1805df43ef5c11db6b7fcdba77b0eb0c0d3713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7621762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de220d7aa70d91d334a8498c9ae1e10d8f8c53b8508bceece7f84a5803c9f1a9`

```dockerfile
```

-	Layers:
	-	`sha256:2b742fb0e0d70644066c1472b3cb6559ba91cdd89925f703883bb76e11cfd5da`  
		Last Modified: Tue, 12 Nov 2024 11:31:19 GMT  
		Size: 7.6 MB (7614405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cfee709989da69a1418471850a2f2c0f2c90e1bf104a675f2aa68f702e9f8df`  
		Last Modified: Tue, 12 Nov 2024 11:31:18 GMT  
		Size: 7.4 KB (7357 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b3c420a89727b5dc5067f3f9dd02acb063f57893e27884c02d8f2104e5e05870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (128046045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738f1c2cb570c23741cfe2b7fe5652af9bef05fa04bdba68ae8b35b33e93925b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:bf9375f2b0e5c66c0a1840e13cfa8b3f0aa55934d9c92c13e479c8cf7909e923 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cf1d8a933c6efa9a7129c6faf202eeab8feff677f32fbc0037a3ab76003edcf8`  
		Last Modified: Thu, 17 Oct 2024 03:09:00 GMT  
		Size: 47.7 MB (47691399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5bb5787cc9d2878988b37d2049fa1d6b67ff3450f012cef9603dcff05b03ef`  
		Last Modified: Sat, 19 Oct 2024 00:57:32 GMT  
		Size: 18.9 MB (18893656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f7ad36a85c1a25fec35fecdd0c231974acf44c7aaeec9321464cf908e0e452`  
		Last Modified: Sat, 19 Oct 2024 06:39:20 GMT  
		Size: 61.5 MB (61460990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b9db4cf0319144959de60546593784cc663d31b4196f01692f0735bbb32f55ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7598561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5a3d725a4310da5f1831130375142b0c20d3b76ad85c1979e28711f6289983`

```dockerfile
```

-	Layers:
	-	`sha256:fc2860af086787f7758af329dc104412d3c616d8f41f41ca89aad651c478bed6`  
		Last Modified: Sat, 19 Oct 2024 06:39:18 GMT  
		Size: 7.6 MB (7591192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ab2ce55dca633eda9a90680cc443df4c7645b5e860e2cf82d4861989c3d253a`  
		Last Modified: Sat, 19 Oct 2024 06:39:17 GMT  
		Size: 7.4 KB (7369 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:802c828bc2d5c912348dee436053e3aa7d82d26837f894566a3f6381b19a0ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140380464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877345af7ef312c479c5be927342731e90dd345572ff8fde69dde61a4aa757fe`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:58acae53f12429504dea737cd60eba46c5f2eea862974a8d8fe218c17d285565 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d246237d395a465ccb5ede6b1a321d43a78766a62bc93015a0368a88624aedff`  
		Last Modified: Thu, 17 Oct 2024 01:15:57 GMT  
		Size: 53.6 MB (53629485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b80bac00a06288366529b5187b9485c685d4f46018bcb866049abf9f952247d`  
		Last Modified: Sat, 19 Oct 2024 01:11:43 GMT  
		Size: 20.2 MB (20196615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19663fa8e0a57915a50484edf1e2599200b05cd9b029d04f6246f46e4ebd7b8`  
		Last Modified: Sat, 19 Oct 2024 05:19:11 GMT  
		Size: 66.6 MB (66554364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3bdc370b125ed8b8193e8750270c2d8ec3cf86815e299ac1b5e01a42224844b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7604477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739a6c936ffbddb93e2f0497b97a3910e5b4a89d807763c9a97116823c23aefc`

```dockerfile
```

-	Layers:
	-	`sha256:95ec60fa71429ed1b411dc8b543221800db7aba2271e78572346255708271d50`  
		Last Modified: Sat, 19 Oct 2024 05:19:10 GMT  
		Size: 7.6 MB (7597088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0473ea6aaf55e12d5241f62663f89556fbee6b5d58ad766cf0d2a66168faf10`  
		Last Modified: Sat, 19 Oct 2024 05:19:09 GMT  
		Size: 7.4 KB (7389 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c104a59a3c4fb391a52f93cbfb13639f2687fc4366f11bd4751a0070ae46295d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.5 MB (144456027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b888da81dfbdafdde34e7d00d58c2571e37c5eb4452bcb663b3985887540668b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:266f316e766c7029b1cbb65159b6d9ea1da28d00e28cf109ea069ce95b082ac4`  
		Last Modified: Tue, 12 Nov 2024 00:55:10 GMT  
		Size: 54.2 MB (54192046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24546888a84a1c2171ba5648f213b4d3b8fee560f454ad1c12f583f6ce895c81`  
		Last Modified: Tue, 12 Nov 2024 02:37:52 GMT  
		Size: 21.7 MB (21725392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885dfc308254678967ab6d79ba6d40d73a4ad263c111beedb94327edea737b17`  
		Last Modified: Tue, 12 Nov 2024 03:14:27 GMT  
		Size: 68.5 MB (68538589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8c24aadad36af251cd9bf21f434e87afe3221731362b3949ed6041b42e0106d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7616166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048981b783cc2bc2805b479186421c83a673d18f0c7f4ff8aaddaccc1c439cdb`

```dockerfile
```

-	Layers:
	-	`sha256:c118844549e4437f38e352a7c47675cf37b87544393f46164905c9d0236b7bec`  
		Last Modified: Tue, 12 Nov 2024 03:14:26 GMT  
		Size: 7.6 MB (7608893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f38ce5f76d34336732dd1258471ae700b6196172c7e61fece81d951971e0645c`  
		Last Modified: Tue, 12 Nov 2024 03:14:25 GMT  
		Size: 7.3 KB (7273 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:90e7b41bb44f0aabb12b036d985456deb388ccec89696004083da5b293198773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138325814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6bf84c04011b93921d0604ae5f4b5ff157d7ce4141958a4446f7682abc63e18`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:8ffd9575546e69884562db46178b841df2ba1ed04549599485b7c502f81ac4cc in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e3c6aca2e6ea9e1b19b3c46a60581e28de71137e5bd8fe9c8ea62365a8e75d74`  
		Last Modified: Thu, 17 Oct 2024 01:18:46 GMT  
		Size: 52.2 MB (52157899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35efd481e6347988498fa292e64d8b2f0d728f327f48bccb1d2c2bf371f2f1e1`  
		Last Modified: Sat, 19 Oct 2024 00:58:29 GMT  
		Size: 20.9 MB (20887623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10d42e894e27bd8661997e28ccc989f4b18c73e3892449a02653f995d796aea`  
		Last Modified: Sat, 19 Oct 2024 02:11:09 GMT  
		Size: 65.3 MB (65280292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0552c8f1cd92a1e8490dffddb1bdf464601603e6f79a1d72baa7fc8463fe5fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0ddef53b5b2c40e1838553c952ea8f3401900b10956137e1528e15ff24bcbd`

```dockerfile
```

-	Layers:
	-	`sha256:793454691f682b72aa95b4fbab2aa8dfbd92025fc02eebcd17d82fb50e48bb05`  
		Last Modified: Sat, 19 Oct 2024 02:11:03 GMT  
		Size: 7.1 KB (7141 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:070c7700d7f47048e9a84488481f5eeca3f322a2db8cf0063079bf0485af6022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151160749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461e9769ea2dda7d988b6bf2cf460318a930a39b684be2f7a4133a884c4eb101`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ac2d911f8489db0bbd6f313128660ffb4f315b3d99baed39d7128c198fea25b9`  
		Last Modified: Tue, 12 Nov 2024 00:59:35 GMT  
		Size: 57.3 MB (57309355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5f3e8aa1353894772b7fd9d91dc6448cf8573234fedf1ba1c8596471c52519`  
		Last Modified: Tue, 12 Nov 2024 08:30:11 GMT  
		Size: 22.0 MB (21992150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f36575664f661fb4663abf9a54ae38f6714b2f1a53511cc1ffe3d8ddb1acb8`  
		Last Modified: Tue, 12 Nov 2024 16:11:05 GMT  
		Size: 71.9 MB (71859244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e104f83870e9f99a4669b944a6bbcbebacf57fc258995d778499ee21445f42c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7627984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c47416740f5541249a4cef52d3b7e47f7681543d006c0c3ec02ff1b67bbcffd`

```dockerfile
```

-	Layers:
	-	`sha256:92fb0bcde05bbbbbd4d0f942437bf003e06cd1076856b50441ea3830631de34a`  
		Last Modified: Tue, 12 Nov 2024 16:11:04 GMT  
		Size: 7.6 MB (7620655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2a50d8c663179edf632a443d2292c19b83099aa6fc312e4f3fa057911bd68e2`  
		Last Modified: Tue, 12 Nov 2024 16:11:03 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:ab2c9935ec3cd5ea01e59c813479dfdbe44a93881633c9ab35a027bc963fbb2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137343646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b025b9611b4913fb2e9ce20401ffc0abdc8d1d1f86c8933186f6b02ff7f4c8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:9748961f840a27ae3342039309a28acc84e3a482f5ca3ece5bdaf9f92e7ebe33 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:29cf887cb660615390407db841ad4c44be2414b9bf999ba668d93a8305675c7e`  
		Last Modified: Thu, 17 Oct 2024 01:14:47 GMT  
		Size: 51.6 MB (51562685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de12fa48532c87115805a1e3efbbdd980575096676ddd00868f642d72782b610`  
		Last Modified: Sat, 19 Oct 2024 01:03:17 GMT  
		Size: 20.0 MB (20023981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c05579e9b49f41a2b6960286d8ab9b1d090127915ab4b5f2c9ec35e3db7815`  
		Last Modified: Sat, 19 Oct 2024 03:48:10 GMT  
		Size: 65.8 MB (65756980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1c2cf945f847e73794eaad19c99277f7632971602dd13cc6de4b1f441087c709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7588619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00950719b6663cf9a97df3b358162af671f7ca9b8b02fe2daa10b4ab5abc3f80`

```dockerfile
```

-	Layers:
	-	`sha256:953dc6ddab24f26925a8b0c459f5e303f3adc5374831eed917b8e26a9c0deaee`  
		Last Modified: Sat, 19 Oct 2024 03:48:02 GMT  
		Size: 7.6 MB (7581279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da3224b770b161aa53b6afc3fd6cca8fa7a8e2c13cf53415c7f406ae104506e5`  
		Last Modified: Sat, 19 Oct 2024 03:48:01 GMT  
		Size: 7.3 KB (7340 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:75798f8edcf34cc806383a3cb0d582183149dbf1634de5c038911c2d039a57db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142059552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e3c4460532df5edbadaa408870e0284979bdf475836695ee5d0a66eed35f17`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:2f1a819570e851a9bce2342f32c7927abdb02af08d5e469e6f5d41a193235bb2 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:79590eb16acf1f35f7a00e8c30e7daf7ed5d8bc9d65ff782665704f532af0ac0`  
		Last Modified: Thu, 17 Oct 2024 01:50:44 GMT  
		Size: 52.9 MB (52851981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf56c8e1a853602c0af0f40a2561d6ca90c547c99b9bdd2c5349a88e1f5cc1a`  
		Last Modified: Sat, 19 Oct 2024 00:58:05 GMT  
		Size: 21.6 MB (21639639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a7102bce19ae53b519fb58ec97dd26aadbdffdfec95cd2613f51b842e60866`  
		Last Modified: Sat, 19 Oct 2024 03:47:42 GMT  
		Size: 67.6 MB (67567932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:678287387bbebd1636e0fe5a2aeb073194add8b6f5c394616c9e1c23ce56b241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7598915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d5a40b14913c0e75a4b4bfbe1fb8e67f0bff40be7dd304d7a42dc794b6abe0`

```dockerfile
```

-	Layers:
	-	`sha256:849570392004a4d0cd1b888908893e70054109b2a9280a5ec80ecc396d7baa25`  
		Last Modified: Sat, 19 Oct 2024 03:47:41 GMT  
		Size: 7.6 MB (7591606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcaf34e81575ac3e7c8e9cb223f3661f4b719530508731fbbe38bec3829d0ac9`  
		Last Modified: Sat, 19 Oct 2024 03:47:40 GMT  
		Size: 7.3 KB (7309 bytes)  
		MIME: application/vnd.in-toto+json
