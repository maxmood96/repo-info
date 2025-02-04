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
$ docker pull buildpack-deps@sha256:eaad1fbcab2ded0365c860b403c77cf52b549bfe52e1d494a43c2f6630311456
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
$ docker pull buildpack-deps@sha256:d719e1b3685b07437141f3cf9c3d496640fa957490d940fb6c8af304c9ee5b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.0 MB (249049639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f693ae883e3235266008e0e119241f5cbf9e66651e5d5e37467bde618d617335`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee445cc5e2b6b7936777d1af58476890507382191edc76cf636f7e69381a0f7`  
		Last Modified: Tue, 04 Feb 2025 04:37:54 GMT  
		Size: 7.1 MB (7095774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c481194f5cf954d821c9180450bf9cbfe7d778d31dd54b13e0f37be46d837e`  
		Last Modified: Tue, 04 Feb 2025 05:20:43 GMT  
		Size: 39.5 MB (39488061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ff89f6579baee318f96b07c9b40341a1d6992851e8ea7c38718236c6c02186`  
		Last Modified: Tue, 04 Feb 2025 06:14:30 GMT  
		Size: 172.9 MB (172929863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:22.04` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f3cda331a4992c50877bb591e55621583b2bc85eb6ec5bfe048dfd9afa12b82a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11463053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508568c85c5c43517a2dea7d1beefeae59140318409a07e148d327ecc388d8bd`

```dockerfile
```

-	Layers:
	-	`sha256:1b0fb76c9081098812d4f10f5a9210232acdd68a70bdce5c86529b0187833759`  
		Last Modified: Tue, 04 Feb 2025 06:14:25 GMT  
		Size: 11.5 MB (11452850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fea7c33ef084e79abab04a0097d930daa4c248972b0a5835269f659a3b9a001`  
		Last Modified: Tue, 04 Feb 2025 06:14:24 GMT  
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
$ docker pull buildpack-deps@sha256:cb005a903174af55be4fd9061bf76c495b4e36e10b7086806532cb43c95dde2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274231046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90f0b33982a82b2568cb04a4cfd62ae71d860a15bfc21a21e67fba19170c92d`
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
ADD file:c95ac39f820c01b1c0a2d18f3df09346a389f9989c91cb636f75de0e3d63c97d in / 
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
	-	`sha256:cfa2d73aa16649863373431bec34ae49863b8b03f19e2c1fa29af96b0ea254fc`  
		Last Modified: Sun, 26 Jan 2025 07:02:26 GMT  
		Size: 27.0 MB (27039007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247fcfe5b002f706b4c9b3a78341f202606a547ef405c7ad03e2e33f28fec027`  
		Last Modified: Tue, 04 Feb 2025 04:44:46 GMT  
		Size: 7.1 MB (7108060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb811904a9072aa1e8962df9982276480172376fb423cfcf8aaec3ebb4f9f8ca`  
		Last Modified: Tue, 04 Feb 2025 08:14:03 GMT  
		Size: 42.3 MB (42307263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70089f8fa6e86f416dcc916a3a84e0eb779463cd666ed04f5784d45aa423ea9`  
		Last Modified: Tue, 04 Feb 2025 10:06:46 GMT  
		Size: 197.8 MB (197776716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:22.04` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5d87b26854a76501137f25370979c3cedeea170eb08484a6de7863cc3ab793ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11404981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d611b10a561d0c1c1e91fca1cb463bd6a7438a1f550263f51f55fe5fa896893`

```dockerfile
```

-	Layers:
	-	`sha256:3989dddbb46fe2b99dc6e1c31bf8f63b02f6d180ab5b721f4266b7fba5596421`  
		Last Modified: Tue, 04 Feb 2025 10:06:19 GMT  
		Size: 11.4 MB (11394746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ace35bc54c917e2c6c94ff6c186d49d7dec0aec2f43deb0dd7110a21c813e6aa`  
		Last Modified: Tue, 04 Feb 2025 10:06:18 GMT  
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
$ docker pull buildpack-deps@sha256:33a46dfd834f4a61b5866da863063dccd1160f248bbfab92581f4ace71be51de
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
$ docker pull buildpack-deps@sha256:49fdc396e3e2c388288ee868f80cc46793b115a7d855635f31fa2c84af1021cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36631715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127dfc62185b034f15bcc646d5535774677fcbfdd5d0c0774c75aa4b6d84655c`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee445cc5e2b6b7936777d1af58476890507382191edc76cf636f7e69381a0f7`  
		Last Modified: Tue, 04 Feb 2025 04:37:54 GMT  
		Size: 7.1 MB (7095774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:22.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:08e2b3186b703bd630a8a64b1a730e9fe7ad1b985ef44af18ac26b7664e38634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3054780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a864cc7fb6669139bfab22092b7aff2664a4d68078104b4d3492b3e6fb1cd4de`

```dockerfile
```

-	Layers:
	-	`sha256:c152abfc25cd0a72c5a3b91acb4071bd18d4f7477647237727f28c4873d9bc27`  
		Last Modified: Tue, 04 Feb 2025 04:37:54 GMT  
		Size: 3.0 MB (3047856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7acaf0a3198eef8de38c3053abc8d01f4a671d075e57f191a1d80246b2484071`  
		Last Modified: Tue, 04 Feb 2025 04:37:54 GMT  
		Size: 6.9 KB (6924 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:22.04-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:17d0d3dd1f949640b03303b80a650627955b363a2f9d06d9f4380ca3fc45903c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.6 MB (33637804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d8b2934575515d0bb55b5c063d6c24cd529eee32e94c81894b2b659b3b3fca`
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
ADD file:7e9e4d557a66a31de2a39930803dbe849ba710af36b4731e9cbc856f55c10018 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:eeaefd3c974dfe1d5e1b8eb1929496ae7befe434399b37e601701f6d012e3169`  
		Last Modified: Sun, 26 Jan 2025 07:02:14 GMT  
		Size: 26.6 MB (26639267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03a59df32a3c278c1a8e1b5a42ec5159ca064a182a7ceee73e4ebe1d86afa12`  
		Last Modified: Tue, 04 Feb 2025 10:44:17 GMT  
		Size: 7.0 MB (6998537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:22.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1081500fc1be6fc3b8945ee99cb880cad574141933dbf2029a9a700a348a715e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3057147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0464e0de96691547f00ea8cde65d4ce20b5600e2c75c0e12c4aa3273df345a`

```dockerfile
```

-	Layers:
	-	`sha256:be68de876ccd100fac7c846b873154fb9e5fd89aba869bb04540f87213adae7a`  
		Last Modified: Tue, 04 Feb 2025 10:44:16 GMT  
		Size: 3.1 MB (3050163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7e8cd613a05f23ccfbaa6b9282044f16d5b355c4674cb7f486f198d68be570c`  
		Last Modified: Tue, 04 Feb 2025 10:44:16 GMT  
		Size: 7.0 KB (6984 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:22.04-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0fe6929d44d620ffe7cd75fe5b40025de76aa74aa07685bf792230e7c91825c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34398721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d89d6c25abf119ba22786832d5f3a2a743d77c84a724cc975596b4ee8e86ba5`
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
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9c1e987316bb6701bafa74dadea41ea57299699f23daacaaeafa9fa05f6213`  
		Last Modified: Tue, 04 Feb 2025 09:02:41 GMT  
		Size: 7.0 MB (7040539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:22.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6fb6b46dca2ea64642d5dcd614a9ad3a335f6afc07964764d2a870482af7eed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3055127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9206dba5abd986116aadf3f44aa556ed7bc3c28b9fd8f2d751d5c5f8a078f029`

```dockerfile
```

-	Layers:
	-	`sha256:ea672570cd596ebccfbaf31f47d9266431bce6f9967097954cd1659360dbbf13`  
		Last Modified: Tue, 04 Feb 2025 09:02:41 GMT  
		Size: 3.0 MB (3048123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f612b7908009283b8c09df71f46498e69fb65338aa1acc7f8c26ba67098b173`  
		Last Modified: Tue, 04 Feb 2025 09:02:40 GMT  
		Size: 7.0 KB (7004 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:22.04-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f7a5a90bfae168264eeeb709cce4697ea63a9377abf6d16ba2581602a0a3c7cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42645600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3e4f50615188f5197de6d78f780e501719398fd833977679cfab950529acda`
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
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c3f11d98bfde7b2d484e86a27f312061b41c7e65028517cbad025bac990450`  
		Last Modified: Tue, 04 Feb 2025 07:27:33 GMT  
		Size: 8.2 MB (8197665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:22.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2c993ec04244791550b10adfbecaea533a100b4a380b704979de7ff258cc1e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3059308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c97eb7eeafb4c53e7972f390b01a7f523dc725404a2c9c5a95550c96ae12df91`

```dockerfile
```

-	Layers:
	-	`sha256:bba32565c3d514031e655b03a2f0a4c12b8bfea0bbc31f2aa1804ed1367d0233`  
		Last Modified: Tue, 04 Feb 2025 07:27:33 GMT  
		Size: 3.1 MB (3052352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c60f22569bd53f1851706f6784c9cdbf7c58dfa5d23a1de9e2c390c8a6e9e3fc`  
		Last Modified: Tue, 04 Feb 2025 07:27:32 GMT  
		Size: 7.0 KB (6956 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:22.04-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a6dd850306c6cc369b57522a19b04cc9df354d0667fea9d4aeb82ee101c0acd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34147067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67d75862f0c15955d1d425f409ce31bc3a9f4d1686620b242a3a4f82b9394cb2`
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
ADD file:c95ac39f820c01b1c0a2d18f3df09346a389f9989c91cb636f75de0e3d63c97d in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cfa2d73aa16649863373431bec34ae49863b8b03f19e2c1fa29af96b0ea254fc`  
		Last Modified: Sun, 26 Jan 2025 07:02:26 GMT  
		Size: 27.0 MB (27039007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247fcfe5b002f706b4c9b3a78341f202606a547ef405c7ad03e2e33f28fec027`  
		Last Modified: Tue, 04 Feb 2025 04:44:46 GMT  
		Size: 7.1 MB (7108060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:22.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:27bb19291d910241f49185bcc23ffdaa47f0cd3d8f6c1505d83c09a976b89813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3048884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9996e59dbe46469cbc1c0a9d12f8aa9e22e0eb47b6843d06576af759fb73ff59`

```dockerfile
```

-	Layers:
	-	`sha256:c0ab06483d85f040af1b5f357790820b1c4fc53e83d9f16c38e4bd4c710968dd`  
		Last Modified: Tue, 04 Feb 2025 04:44:45 GMT  
		Size: 3.0 MB (3041928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dea9caad6953ba858e383ba65ee141384c7eb1dbce3cd7fca008ea276ee7f644`  
		Last Modified: Tue, 04 Feb 2025 04:44:44 GMT  
		Size: 7.0 KB (6956 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:22.04-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c9240024d17797d3670c26e10209501dbdd01d047b288925c278736a64dd4143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (35008772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f00d83c6eebb1eba2dfe93dc896eab9f7af7d70e04e338b245c8cd3d27da9064`
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
ADD file:39a6583c8b71c00e0ea7562cadb2b343caf5c0c274178520c7476e53faed2e3e in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7ed94a91c4e77c2e320a028b45fcefc9419c4df2b3d6494bf92ab5d08bba4d77`  
		Last Modified: Sun, 26 Jan 2025 07:02:32 GMT  
		Size: 28.0 MB (28000931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e0e0eba9503675f1ef20409d7abb0dc538cffb5361ed38070285248d79ca72`  
		Last Modified: Tue, 04 Feb 2025 07:33:18 GMT  
		Size: 7.0 MB (7007841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:22.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:63ecb7ddf4472817977f6f2e8d7b9bc4b5b27b626e08d6093db38777b2223e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3056996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffcef3547b091a358212056be9c262d679e046d201a57c9f65f99ff5f687aae1`

```dockerfile
```

-	Layers:
	-	`sha256:e61b6f4a167e6db0669458a35acb4bb49bc224dd1587bf3faba988821f883cd7`  
		Last Modified: Tue, 04 Feb 2025 07:33:17 GMT  
		Size: 3.1 MB (3050073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:638f272136230740d6cb3a0f0b077fc9dd7467a6d19821f0b719f79c0377c955`  
		Last Modified: Tue, 04 Feb 2025 07:33:17 GMT  
		Size: 6.9 KB (6923 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:22.04-scm`

```console
$ docker pull buildpack-deps@sha256:023a100c019c6b7c4549fab14b6a91cd2e61ca09575ce75fbf6fc251a6be7cc5
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
$ docker pull buildpack-deps@sha256:91718149b4f53576557b3a5645fcb54ed8cfe681b6c1f734380f470ec388f8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76119776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0645d0ba933cbe9b814b1dfb1bd138139346974f8753b21f2b8e3bc651919ba4`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee445cc5e2b6b7936777d1af58476890507382191edc76cf636f7e69381a0f7`  
		Last Modified: Tue, 04 Feb 2025 04:37:54 GMT  
		Size: 7.1 MB (7095774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c481194f5cf954d821c9180450bf9cbfe7d778d31dd54b13e0f37be46d837e`  
		Last Modified: Tue, 04 Feb 2025 05:20:43 GMT  
		Size: 39.5 MB (39488061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:22.04-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:913d6f77f627a5bf919be07bda166a50763665912c67c95de1a7a0c2eddf56fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837e383278b13cc069dd1f374210c432d5da73fd03f906048d2a1c86bafd3ed4`

```dockerfile
```

-	Layers:
	-	`sha256:a4523ac5f5958d30b606668facc78038341dc66d269f673e094bed9cc3df3951`  
		Last Modified: Tue, 04 Feb 2025 05:20:42 GMT  
		Size: 5.6 MB (5599765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c7a1e41537563d3da2abde7ffa18474777946269f533ae09dd1ebddfecd36f3`  
		Last Modified: Tue, 04 Feb 2025 05:20:42 GMT  
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
$ docker pull buildpack-deps@sha256:057096cc3c93f1f8fb66031507a66e3964e19ebf13ba1506c10185bcd3d680df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76454330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d30085e843b181c9d6f4f2db62a64f5abc2075b8becfb389d85b5c26010172`
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
ADD file:c95ac39f820c01b1c0a2d18f3df09346a389f9989c91cb636f75de0e3d63c97d in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cfa2d73aa16649863373431bec34ae49863b8b03f19e2c1fa29af96b0ea254fc`  
		Last Modified: Sun, 26 Jan 2025 07:02:26 GMT  
		Size: 27.0 MB (27039007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247fcfe5b002f706b4c9b3a78341f202606a547ef405c7ad03e2e33f28fec027`  
		Last Modified: Tue, 04 Feb 2025 04:44:46 GMT  
		Size: 7.1 MB (7108060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb811904a9072aa1e8962df9982276480172376fb423cfcf8aaec3ebb4f9f8ca`  
		Last Modified: Tue, 04 Feb 2025 08:14:03 GMT  
		Size: 42.3 MB (42307263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:22.04-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:db7959de9f0bbc7f117458f02e843839a036cecd8be06014481d54e3e65988d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5597655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576c72a4fdb601de9b844fe21519fdf8a6175dedd057cee5a5aedb19f9ca8df2`

```dockerfile
```

-	Layers:
	-	`sha256:0f25233e0d3c13d7ff6ec6d10bf9d28c99eade027cb6b2c16f932fb3d4593f81`  
		Last Modified: Tue, 04 Feb 2025 08:13:58 GMT  
		Size: 5.6 MB (5590299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bba3b78cb50e20ecbdff1ccf6fa4223854971f17408346d0efc034f2c824f27`  
		Last Modified: Tue, 04 Feb 2025 08:13:56 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:22.04-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6102c2a37e0c3ad300dff3483bdad8123d61076b7a324ba074b7c9b0b65d3ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74429734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e92079504e248aa3e1839d4474b3d926c07679ced29323feb51c42b3841b82`
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
ADD file:39a6583c8b71c00e0ea7562cadb2b343caf5c0c274178520c7476e53faed2e3e in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7ed94a91c4e77c2e320a028b45fcefc9419c4df2b3d6494bf92ab5d08bba4d77`  
		Last Modified: Sun, 26 Jan 2025 07:02:32 GMT  
		Size: 28.0 MB (28000931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e0e0eba9503675f1ef20409d7abb0dc538cffb5361ed38070285248d79ca72`  
		Last Modified: Tue, 04 Feb 2025 07:33:18 GMT  
		Size: 7.0 MB (7007841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ceb4257b5f6dbcfe0b6e240c36bcdefe3066bed00810364bb9111fc2b142678`  
		Last Modified: Tue, 04 Feb 2025 11:41:04 GMT  
		Size: 39.4 MB (39420962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:22.04-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:150da59697f1fda4ccd2b151d902b5463a708a5b5b4f918b4cacbda4ab3ea8e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8acfd7255776abc5b50d08c625a299c1efb593b61475984c2f4253c647aefdd`

```dockerfile
```

-	Layers:
	-	`sha256:3b20d61e305f63b842292fddab5a24a44dd99d12e07539a87853a780cdc97c4c`  
		Last Modified: Tue, 04 Feb 2025 11:41:02 GMT  
		Size: 5.6 MB (5600684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f48cc83a24245e928a33854befaeb67bfc51d8a7139f4f7d39f930180822cfd`  
		Last Modified: Tue, 04 Feb 2025 11:41:02 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:24.04`

```console
$ docker pull buildpack-deps@sha256:51c0b7c0a60b769cb9e77492f6e77e6092be26b21bade5f50eb4b44c10f60700
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
$ docker pull buildpack-deps@sha256:05f037723a8daa90787e6a1637211ec41ce3b0bca77ca6596fb29ca637908007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278607273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ef6cacbdf5590762e0385cd5204d975695279bbc6f6faed361216b0278db670`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bca5f89848ce8fced9fabc99051bd86546e9b21ec911faa12d1b57517b419d`  
		Last Modified: Tue, 04 Feb 2025 04:37:54 GMT  
		Size: 13.6 MB (13612233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c239591c8fa2f14b9d884080d6e6888af267d5581800cd9aca9df2581c579ded`  
		Last Modified: Tue, 04 Feb 2025 05:20:45 GMT  
		Size: 47.7 MB (47706161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4002a449dfbeebc197aa37c9540569c67552048e4ea6f3e29d4680d8877810fd`  
		Last Modified: Tue, 04 Feb 2025 06:14:15 GMT  
		Size: 187.5 MB (187534589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ea56b9ef0ade587ac7c02b1d7068c32d6912c34bb3d22b99d146ece0c29e3819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11357581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91971766cecd1a460eb600747d6a6ecea74bedbcc256fa7547a9559067f3d6d6`

```dockerfile
```

-	Layers:
	-	`sha256:979f5fc4fdb0e002a48d35db1f28d78516b135296692a750da8f1a69c430293b`  
		Last Modified: Tue, 04 Feb 2025 06:14:12 GMT  
		Size: 11.3 MB (11347397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edc3bec74ae7fe6478fd68bdace1f3df91ce527a4f98599bc376e52bbeb84cab`  
		Last Modified: Tue, 04 Feb 2025 06:14:12 GMT  
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
$ docker pull buildpack-deps@sha256:d31f5bdb9913880c43a5a00471c71bf67e54951ad0562d4ecfd3df1a803ebbda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.2 MB (333185891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3cb0ade06c43af8ab75177b46cd822d33e79229563b4910a508c8b1c3ad48f7`
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
ADD file:69c46ae9666e78c27ca5b5f25cec1a5536ff16f17cb00104e5c77e722bd8d643 in / 
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
	-	`sha256:6e1053d729cc1718daa9369927cf6ddfbf892a846041de0e610d1c77ade136c5`  
		Last Modified: Mon, 27 Jan 2025 05:10:15 GMT  
		Size: 31.0 MB (30983910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1ff2b444c4e8d1278840900c3e27c00e5987f3c54a529299dbf9a2ed443657`  
		Last Modified: Tue, 04 Feb 2025 04:47:44 GMT  
		Size: 14.3 MB (14317230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec5a422d511e6bec6d017fced317ebf97a5f77ec1f6eff36a777fc69635d1c3`  
		Last Modified: Tue, 04 Feb 2025 08:19:44 GMT  
		Size: 56.2 MB (56219937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25582887dbbebf13b474bcce046935f9057ec77b7d60eb19fafce7fdcf42f073`  
		Last Modified: Tue, 04 Feb 2025 10:24:52 GMT  
		Size: 231.7 MB (231664814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e54aa815e93779c56670198616f3acdade74b3796475166f25881215682c4187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10870736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5808c0276f6f621d004fff61facb2f629fbaf4021749d5cb1299d184f771cc65`

```dockerfile
```

-	Layers:
	-	`sha256:40943108eb855797811a4ec15d39627861040402ea56a026d39ea8de5439224c`  
		Last Modified: Tue, 04 Feb 2025 10:24:22 GMT  
		Size: 10.9 MB (10860520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0dbedfe5b565ffed2c797524ab8f0e8765c8c9e9475f416aeb3a57a9df3cdc9`  
		Last Modified: Tue, 04 Feb 2025 10:24:20 GMT  
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
$ docker pull buildpack-deps@sha256:0591c4ff26a20c9bd55f2531bc515396f6d356830bbe9e1136205dcabcf857cf
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
$ docker pull buildpack-deps@sha256:644a9f032cf50b2a91f1c4e7312425a77195879e7178d6a6076c084e9d7457cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43366523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d93add3ca2246e80a01713194ef3cc70909c3ccce2b0fc64adb66e63e0d3fce`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bca5f89848ce8fced9fabc99051bd86546e9b21ec911faa12d1b57517b419d`  
		Last Modified: Tue, 04 Feb 2025 04:37:54 GMT  
		Size: 13.6 MB (13612233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a4e685fd1a1fdc8c51f92015aa36ade4193a409acedff0d9fc53f6f0e5e2a403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2469041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312348ef20d91871237e8ce4d0b2263ae4f719aac1e1106d85629a329e842c8f`

```dockerfile
```

-	Layers:
	-	`sha256:2a3a10bb9dcd0dd89b1e24f079336b7b12e0e0ce7d66b51b53ebd2caf71bdebb`  
		Last Modified: Tue, 04 Feb 2025 04:37:54 GMT  
		Size: 2.5 MB (2462082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:876478e0a9dd99b90b311614b8a249982e408c423a64c5b1cd1f707df848452c`  
		Last Modified: Tue, 04 Feb 2025 04:37:53 GMT  
		Size: 7.0 KB (6959 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5ae44b9cc101087fa183a9f8269d6d8f0d1c86230044d58ec0015e1fa706e1d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39645632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19c0792edbcf8119e6ef8d42938209118401d44f50d9674972ff99beec67a6aa`
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
ADD file:22301ffa2fa465db7a0f07e0c3ddc488f07cc6a745c39e6f450fdbe37da97418 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3492abb11babfb77cfc5a8904e67b22f4e4fd68c8d8a7fe1119861ed6503b36f`  
		Last Modified: Mon, 27 Jan 2025 05:10:02 GMT  
		Size: 26.9 MB (26874983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d26a8223ab81b7619d0fa204eaa4a52bd9e82a52dc44e8e3fd181d828b57c69`  
		Last Modified: Tue, 04 Feb 2025 10:45:28 GMT  
		Size: 12.8 MB (12770649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:88d98aa301ddf4ba195ae435b272e8dbc57ada124bc050d9584e020a2d0ed4cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2471405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f632e6a7a1f74c013a8732986b2644111dec9298d7588b4e37b61e3e5f87211`

```dockerfile
```

-	Layers:
	-	`sha256:e39ed50c31a6f47c59f9ff236393152bf088df00a815272e7d5f17eb16b93ed5`  
		Last Modified: Tue, 04 Feb 2025 10:45:28 GMT  
		Size: 2.5 MB (2464386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0299afeb76c3ef583558026c326712b4428d9f8d2f847835de29e219d670197a`  
		Last Modified: Tue, 04 Feb 2025 10:45:27 GMT  
		Size: 7.0 KB (7019 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f81e78c5e8cd92e7c0dd2c53f678e502b5539f88f7bbd62dcf110e487cdbd9a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42341516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a53f3d5ba81a42da827fd1d0fb748b572c23998d6ef79331d126adf57704c8da`
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
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e873299a39c8bb8cb3b5d978575339de6ade976cca414b5727de8d362ef599f2`  
		Last Modified: Tue, 04 Feb 2025 09:03:21 GMT  
		Size: 13.4 MB (13447918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a09851342c2a390434b8403c6567a044084514acfe1c895374c0d61cfd2021b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2470179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4fa8fa439cb9f6ef86fbfe6287983813d43ba022d392271dd37d7a11f8049b`

```dockerfile
```

-	Layers:
	-	`sha256:c45cb91762aa9ce3109b687f2eb31f4ee68d9a8723cfb10b81ba0e79e052a3be`  
		Last Modified: Tue, 04 Feb 2025 09:03:20 GMT  
		Size: 2.5 MB (2463140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be9ae4d5b446fb6dfc3bd1fa724ccedac7ac8e17b189771cdb3a350e25c59adf`  
		Last Modified: Tue, 04 Feb 2025 09:03:20 GMT  
		Size: 7.0 KB (7039 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b8a5136a89a7e6d03e7dd3aeffd99e0e9c7c281cc4d587c6c13bb18c89933e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50348767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec08d7af4854f7616cd6c24d855e9825f8d7b0a7cc3b33d388bb26bbbf087fd0`
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
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb3acc4132c7aebe44f31c42e40cc094c5403d3a66fea37f2373bf78812b25b`  
		Last Modified: Tue, 04 Feb 2025 07:28:52 GMT  
		Size: 16.0 MB (15958943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7780e111e7985c50976ae1a4c5c08bfb9c544701dadd2e2c140f1962ca104727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2473560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6409635aa1c47b491672f8162339c57a539d38011229da817788051e22787bd`

```dockerfile
```

-	Layers:
	-	`sha256:b5e2dfedfa809e8174ffef851627e9bf5e80f70465fbda8b396404490e83284b`  
		Last Modified: Tue, 04 Feb 2025 07:28:51 GMT  
		Size: 2.5 MB (2466569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a0559ba321ef6c4284cc87f3b5369d46603219db294ec6bf7e0a32e77f5486a`  
		Last Modified: Tue, 04 Feb 2025 07:28:51 GMT  
		Size: 7.0 KB (6991 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:31ce75f451962f5cb800331842c9a621e15380dc7a0d5e76cc27f614fb0789d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45301140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054c4b3eb9ab81c609b9e82f2d951c6cc3a86dd499d31378a9ed2556f5980ffe`
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
ADD file:69c46ae9666e78c27ca5b5f25cec1a5536ff16f17cb00104e5c77e722bd8d643 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6e1053d729cc1718daa9369927cf6ddfbf892a846041de0e610d1c77ade136c5`  
		Last Modified: Mon, 27 Jan 2025 05:10:15 GMT  
		Size: 31.0 MB (30983910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1ff2b444c4e8d1278840900c3e27c00e5987f3c54a529299dbf9a2ed443657`  
		Last Modified: Tue, 04 Feb 2025 04:47:44 GMT  
		Size: 14.3 MB (14317230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1a87e48a82b50c374c47c2c34dcd6c3fa330f2d9871e29fa616af48a4edc3cdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d637e0f6a904b9c985a5da321c9640e3c0f45e9288c8c31a84d6fe2281ce3cc`

```dockerfile
```

-	Layers:
	-	`sha256:1db32f151df67541b0541f324d7b140e38f2e4207414a4155bc3af99f47202e0`  
		Last Modified: Tue, 04 Feb 2025 04:47:42 GMT  
		Size: 2.5 MB (2456141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18f60c2b0b80254a366d8c7acb2cd5a488b2f72afe32467a2a687d6a7d8b17c4`  
		Last Modified: Tue, 04 Feb 2025 04:47:42 GMT  
		Size: 7.0 KB (6990 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:98518dff71ac71a87d5d35456508f00745860a4b1d5b936c9e65950ac33a07e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44964949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07262228767cdfdf011a42ed5559b01db0f589b6db2cacdf342b615fbe496383`
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
ADD file:1a65bb049384da7e51a2b1e9180f11d6ec22b1427da7ca5682814abd261ba57e in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8e1d25585ef2d346b71072d258a697a9d190e3c5754512c7cb978dbbe80911e6`  
		Last Modified: Mon, 27 Jan 2025 05:10:30 GMT  
		Size: 30.0 MB (30027563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cacc91036ba2e7e50d76ff2b2593ea149a0df971bb8069b913263b87ff517ac5`  
		Last Modified: Tue, 04 Feb 2025 07:34:27 GMT  
		Size: 14.9 MB (14937386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:89c4abc3a60eb48bcbd7a232595cc99c156532030ab21917410f175b25de736d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2471866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d0978b12b5385265529a2eb8e826ef6bed43e969869849f3968bd2061fbfb4`

```dockerfile
```

-	Layers:
	-	`sha256:1145ed6e6cc241993da9952d8c94810c5bdfc8691a649a7c93c330bbd18a2193`  
		Last Modified: Tue, 04 Feb 2025 07:34:26 GMT  
		Size: 2.5 MB (2464907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02a52d892c2d4165e68754e24393ef9f9addb502befc69210f9f58ff272ee843`  
		Last Modified: Tue, 04 Feb 2025 07:34:26 GMT  
		Size: 7.0 KB (6959 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:24.04-scm`

```console
$ docker pull buildpack-deps@sha256:6b3862bee46bcb79eec81b1bcfb760dd71c534bf2c04991022ef0a14b843baa8
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
$ docker pull buildpack-deps@sha256:b79f7b47aed24f23f5486c1047e9a8c86c3941402091c178acc9f1ef1aaf6e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91072684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8bca72d95b85c99311d1c63dd2fd9ac0b4bee3b2ed93eb890c666eb04e8da7e`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bca5f89848ce8fced9fabc99051bd86546e9b21ec911faa12d1b57517b419d`  
		Last Modified: Tue, 04 Feb 2025 04:37:54 GMT  
		Size: 13.6 MB (13612233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c239591c8fa2f14b9d884080d6e6888af267d5581800cd9aca9df2581c579ded`  
		Last Modified: Tue, 04 Feb 2025 05:20:45 GMT  
		Size: 47.7 MB (47706161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:db5fdb66e6c16e33934375372f2765e3ae9ba4dd6bdabb2c088d421f30df9443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5081162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5227624d892aa0359b9c2a9210f2fe3f732bdf2819487b88202a10c76f5877f7`

```dockerfile
```

-	Layers:
	-	`sha256:9a022b0c23577f479164b46a47db9343c2b2b7c92c88c45d94c1b7a74ea7f1ea`  
		Last Modified: Tue, 04 Feb 2025 05:20:44 GMT  
		Size: 5.1 MB (5073857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:751a37c758d13b6de22a81dd98828f7660e054da7277039fc7fd8fed7a65aa67`  
		Last Modified: Tue, 04 Feb 2025 05:20:44 GMT  
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
$ docker pull buildpack-deps@sha256:ac57716a31f673328d41905ee068cbf3d1e07eb18922ce4bc381166457a0bcb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.5 MB (101521077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9355b669720be435491e9014a723aa6ca9b19f0e95d1305384a0097607d3c47`
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
ADD file:69c46ae9666e78c27ca5b5f25cec1a5536ff16f17cb00104e5c77e722bd8d643 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6e1053d729cc1718daa9369927cf6ddfbf892a846041de0e610d1c77ade136c5`  
		Last Modified: Mon, 27 Jan 2025 05:10:15 GMT  
		Size: 31.0 MB (30983910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1ff2b444c4e8d1278840900c3e27c00e5987f3c54a529299dbf9a2ed443657`  
		Last Modified: Tue, 04 Feb 2025 04:47:44 GMT  
		Size: 14.3 MB (14317230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec5a422d511e6bec6d017fced317ebf97a5f77ec1f6eff36a777fc69635d1c3`  
		Last Modified: Tue, 04 Feb 2025 08:19:44 GMT  
		Size: 56.2 MB (56219937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:13ed8342d52d164a346aa9b5cb66623fe05636c2934ea795ba1b9e598f5399cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5071718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89c54bf63e8b39c08bc48b092a6c6475acb1a690c25fa70405580bc272a43a9`

```dockerfile
```

-	Layers:
	-	`sha256:e76485709ee792b4459b34b590a90e627928fa8bd423b6e42b45b5f7ba2a63de`  
		Last Modified: Tue, 04 Feb 2025 08:19:36 GMT  
		Size: 5.1 MB (5064381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b25f7384c82f182e09fec7b22eaceec3f8a595bcd3522a657ed9ee9e8c29af4`  
		Last Modified: Tue, 04 Feb 2025 08:19:35 GMT  
		Size: 7.3 KB (7337 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:24.04-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:14f5b18a8d3325c0aceabebe8cd762bf3a65f728d72f7b061c7e9df305b9a0d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94420581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7cb2db7e6b493a23389546282950b17a58fe374836a93a6806036f3dae3468`
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
ADD file:1a65bb049384da7e51a2b1e9180f11d6ec22b1427da7ca5682814abd261ba57e in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8e1d25585ef2d346b71072d258a697a9d190e3c5754512c7cb978dbbe80911e6`  
		Last Modified: Mon, 27 Jan 2025 05:10:30 GMT  
		Size: 30.0 MB (30027563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cacc91036ba2e7e50d76ff2b2593ea149a0df971bb8069b913263b87ff517ac5`  
		Last Modified: Tue, 04 Feb 2025 07:34:27 GMT  
		Size: 14.9 MB (14937386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ae03e34cf459247f3c12fdf3d38cb8c622dd2d321ebd9a1ced772465e12c97`  
		Last Modified: Tue, 04 Feb 2025 11:43:56 GMT  
		Size: 49.5 MB (49455632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:24.04-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1525fcbfa02c33484bb09e040a04e9b78c06c3672bf65abf24411ee3e09a500c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5083494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5270daea82df40b76ac970b7fa7c5f3be156d08cf87ed6a6907edbe2a94055b`

```dockerfile
```

-	Layers:
	-	`sha256:c35fa74f8bb61c22c923b1e0ae52e265c1c6f23b8b4bd3db45b9054419060965`  
		Last Modified: Tue, 04 Feb 2025 11:43:55 GMT  
		Size: 5.1 MB (5076189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bb7c13a886117d13a191bcc5c275e7edeffb54e8f7d21e7471bee9c043578fb`  
		Last Modified: Tue, 04 Feb 2025 11:43:55 GMT  
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
$ docker pull buildpack-deps@sha256:d0377c0c511f692ccbcad47f8a26ebbe316394a989429bc4ff2736d05df4d53f
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
$ docker pull buildpack-deps@sha256:e7c6d07cb9b481de9609912bbb49dde977f6989d9a5abd1e58a877d25ee62baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.3 MB (348260383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28b23ee01d152ebfcf4c1687e2584877089ca3ab4550256ebe7e14df2e8a231`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 01:36:22 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b550be6cb62359a0f3a96bc0dc289f8b45d097eaad275887f163c6780b4108`  
		Last Modified: Tue, 04 Feb 2025 04:37:13 GMT  
		Size: 24.1 MB (24058355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35af2a7690f2b43e7237d1fae8e3f2350dfb25f3249e9cf65121866f9c56c772`  
		Last Modified: Tue, 04 Feb 2025 05:19:13 GMT  
		Size: 64.4 MB (64394292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7576b00d9bb10cc967bb5bdeeb3d5fa078ac8800e112aa03ed15ec199662d4f7`  
		Last Modified: Tue, 04 Feb 2025 06:14:28 GMT  
		Size: 211.3 MB (211328049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c4a3dacd4e6c66cf75566584dfa9afd045080a4f3cb7838d7b19bdf30386bd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15482039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9745f0d897e65d430c556d16a3c325def078d21a52bbb041e100967e95bcb9`

```dockerfile
```

-	Layers:
	-	`sha256:d4539b9f2e09894ecde147e82b09f847fc1cb06d936b130a9294f2544a903dd5`  
		Last Modified: Tue, 04 Feb 2025 06:14:25 GMT  
		Size: 15.5 MB (15471499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac139212500e131144b63fc9539d38787370de7cc310e05d7c357c0311687a7b`  
		Last Modified: Tue, 04 Feb 2025 06:14:24 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:a83883a22760febadd59a5f9dbcee3274ad8e29a3721729caff1d538b14169aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.4 MB (315359212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94bd2fc9911efe73bc7196ef0b6034a2b83caa039a8fb7b62851437cb9f1123c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8816181beac5d7674f87060fb5deb0c2c6221a62562265e16f54a617961cbc53`  
		Last Modified: Tue, 04 Feb 2025 01:38:08 GMT  
		Size: 46.0 MB (46006574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28060e71ea1173228ae8eefd6f5fb4296e8c1c73672a593f2d0d8e6e5483072`  
		Last Modified: Tue, 04 Feb 2025 08:03:04 GMT  
		Size: 22.7 MB (22733102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f77895e90931fefcb9b0f936aeec6e8c95f160c764c504ceb6084ffc29b46c`  
		Last Modified: Tue, 04 Feb 2025 10:20:41 GMT  
		Size: 62.0 MB (62003807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1293092f82d991d58072eac031a86360954b6f4021cae9377a435006dbe3bc7`  
		Last Modified: Tue, 04 Feb 2025 11:42:01 GMT  
		Size: 184.6 MB (184615729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dbf7f817719a28df7a5b0171007394ed210843d7eedd3e5f60dab9c54ea16a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15281025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4329461743dc38347b3338b873032c837143ab544d4d8b0cb96a7c18daec6f`

```dockerfile
```

-	Layers:
	-	`sha256:e768728e70f32ce146520e69c30ec9ced53352e7567637f487df05ce3d7d7129`  
		Last Modified: Tue, 04 Feb 2025 11:41:57 GMT  
		Size: 15.3 MB (15270417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9491464fec5e26fdf277d68ee891162483ab440c7fd77e5e08cfb03348e7798f`  
		Last Modified: Tue, 04 Feb 2025 11:41:57 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8a4104d2a65b6d8e78e51a418866c930b56abf606da4fc0d4cecfddc42f4fb27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.1 MB (301064875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36eea9faf1fdc9eefd8d490a1327060dcd31e80229cbcf72c8fbdfac33162515`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 01:34:58 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787291d61ca82895d27d086bfaf14ce01f401dfbf42f462addc8d1cae464ebab`  
		Last Modified: Tue, 14 Jan 2025 08:58:07 GMT  
		Size: 22.0 MB (21960077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6667f6e75dc8bed2e36123666ac457a4e0228141514ab32e65b9c6f6c7960e3`  
		Last Modified: Tue, 14 Jan 2025 16:15:27 GMT  
		Size: 59.6 MB (59640375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4144d45660bbc672e908993d8838af3ec9cece3a56e658f25257a0ce09e20da`  
		Last Modified: Tue, 14 Jan 2025 21:54:34 GMT  
		Size: 175.3 MB (175280214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8dacc3fe87894c577fce996d588fe02c9310c8d81e60e546f643b8bc38d24a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15286445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928b1fb5074c6e11dcf3aa6aa9b892b9e4899a9642c9a64608c3c2b3c292bc35`

```dockerfile
```

-	Layers:
	-	`sha256:ac1c5fb32c5d00a68aaed8067c4a6d22e1f011861220b7ec007edfc4b12d7d51`  
		Last Modified: Tue, 14 Jan 2025 21:54:30 GMT  
		Size: 15.3 MB (15275837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:566b21fe4e655c7bf8464e3b325fcd43af0615ec261408dd779beb45ecd60308`  
		Last Modified: Tue, 14 Jan 2025 21:54:29 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b407977518dbe09e422e0f4fd8f8a9f1343227cd6b752a8748d68f690f6f9603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.0 MB (338978548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c89001a18c0a49ab405cbc818fc07891ef0b4a0e257208d905d299593218681`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b85d68f8a4dce392d372c8a196863eac6d111c36b714179b4ab30e00c00d1`  
		Last Modified: Tue, 14 Jan 2025 06:59:53 GMT  
		Size: 23.6 MB (23598225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936252136b926e9bca27f4a5442f6a5d10c0ea4a23ca8b30c65de1bde666d082`  
		Last Modified: Tue, 14 Jan 2025 13:31:06 GMT  
		Size: 64.4 MB (64356433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c5996c7a64a4f64139ff9df6a590216c8143f5bb1f4c0f41874cf5336645c0`  
		Last Modified: Tue, 14 Jan 2025 17:08:21 GMT  
		Size: 202.7 MB (202716994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d476ca8de345ec5844dc135bc6aa7a9ecb1340f8030bf64ad8a895eaf60ccff1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15510590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2784f3887d0a4b7392bfac8b68c3113a8ca00a1b74b490ca7b5e68fdbbafc50`

```dockerfile
```

-	Layers:
	-	`sha256:63f64955d6e1f03115feb763d448c8fcf074438056bbbfb5f955c3c0d1a4aab7`  
		Last Modified: Tue, 14 Jan 2025 17:08:17 GMT  
		Size: 15.5 MB (15499958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13ac6ce4737d9a952ca57fff0a7a7477bd10b8dc774b705c47fd2768a5a0a036`  
		Last Modified: Tue, 14 Jan 2025 17:08:16 GMT  
		Size: 10.6 KB (10632 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:882a152f2e57fff2b4e424ea3fb6a7d5273b93066678dfd0bdb95b0efba857c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.8 MB (350837945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9097785ed06e1ce4239bd8a49450234addc5a2f2cae02b789c3f0c6688239e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d6abb78404200438eb560450e089a4e7707a23d5ec913df260500d902666670a`  
		Last Modified: Tue, 04 Feb 2025 01:36:35 GMT  
		Size: 49.5 MB (49457456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7d7e5b6420845d0479145c8a18a31030093be0de73e11194d97fee1ac58ef5`  
		Last Modified: Tue, 04 Feb 2025 04:23:48 GMT  
		Size: 24.9 MB (24899338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43394bbbaab482132a05c8eb702c9ebbbf5ecccd558ce05fdf40c651b7fbfa10`  
		Last Modified: Tue, 04 Feb 2025 05:15:47 GMT  
		Size: 66.2 MB (66236925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a443d7b60dbf868d9542c672117d7e30786e753c999878424f61b36b47cb37e5`  
		Last Modified: Tue, 04 Feb 2025 06:14:56 GMT  
		Size: 210.2 MB (210244226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e54a789932b9f341ad41a0f58003c64ea627a572cfb7c893198b963e0f60b687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15460601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb037878e3a2b9b326d57a9255d1516b726264d93cdf05e3e5072ecf804fcb2`

```dockerfile
```

-	Layers:
	-	`sha256:65c94f4e47cb5c1d276ce88454d05b51a88e1f8b6e58588a30fcf1e870c57f76`  
		Last Modified: Tue, 04 Feb 2025 06:14:51 GMT  
		Size: 15.5 MB (15450089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a66dedb1b7b06480192ffed582731683a156dc109dbe02f773f96c60f11a9a78`  
		Last Modified: Tue, 04 Feb 2025 06:14:50 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:860a2755ec0568a4dbe46314a2ae387e90fc9b53a78c8889c779740d34c4d802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.6 MB (325612422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5fc62c757f45c6730d1d46ad5a4473bea7a37b382fd92a8928e79be83348e25`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:12e528bcd428b4b8475a045cfdce724675384eedf195bad13ce8015853db632c`  
		Last Modified: Tue, 14 Jan 2025 01:34:57 GMT  
		Size: 48.8 MB (48758103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dede5b838e92cbab015cc8e31645fbe220ba02a56693e3a7a144e0a5428690`  
		Last Modified: Tue, 14 Jan 2025 18:10:17 GMT  
		Size: 23.7 MB (23652164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be7513211e793708951d273ea21ae802b4bdb4109f4b12ca6122e317851db90`  
		Last Modified: Wed, 15 Jan 2025 02:00:51 GMT  
		Size: 63.3 MB (63296729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac18012fc3c757a7df4cc601b819ea75556dd5814ec840b12642602c54fe799`  
		Last Modified: Wed, 15 Jan 2025 17:56:32 GMT  
		Size: 189.9 MB (189905426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:66e4f671ba1b7ad4b6b317db70aa590923f42d88d1b145d7b89d506f0e9400a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54cc4402e6b3fab15abe9933de571318dc91188f9d8875898b7d714a8855c230`

```dockerfile
```

-	Layers:
	-	`sha256:c1eb17e50044ba359ef545be178a5605253131cd4cc227f70c88c9d2f1b519d8`  
		Last Modified: Wed, 15 Jan 2025 17:56:14 GMT  
		Size: 10.4 KB (10382 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4725d4b50cc3768c2f7586e853992b6f03926dce68a3456661da6f08b1708622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.2 MB (362239370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c43ee817227a27216e0e75060a8916507939c6d366bfed2662922b4b750de8a8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:60b6379697eb1bdc0a74d6aa762f7f8e36a4a46031b019e2c7651c9723194c8b`  
		Last Modified: Tue, 14 Jan 2025 01:36:59 GMT  
		Size: 52.3 MB (52313137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b1d1b75ad07ec92cebf5f30e6612d80907cb5a7323fdef7921893e816a53be`  
		Last Modified: Tue, 14 Jan 2025 05:30:15 GMT  
		Size: 25.7 MB (25717439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395bc8910e96064c02227d340de0ac8d0234f64dd58802df0e9bd0891ad39050`  
		Last Modified: Tue, 14 Jan 2025 09:41:58 GMT  
		Size: 69.8 MB (69844490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb75d2bb90f133e31006cdf083f7a1330b114cb8a3fd0025be19bce4d4ee89b`  
		Last Modified: Tue, 14 Jan 2025 13:00:17 GMT  
		Size: 214.4 MB (214364304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:91b60ba7af97ff988d44396cd69ffddfaa27f52f86ba804fcb0094052e59b774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15458402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7756e08eb53066769aa73f8cb07a547ba51e203c0032cd5932fc75d44e7a1f1`

```dockerfile
```

-	Layers:
	-	`sha256:fcc9fa1d49ed25f5c3c5a80a6668f2ea892ecb027237cec560258091a270b425`  
		Last Modified: Tue, 14 Jan 2025 13:00:11 GMT  
		Size: 15.4 MB (15447824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfa234786e191f6aea3b5a8c4236319884b3c104e4aa16502da685b5eb83170b`  
		Last Modified: Tue, 14 Jan 2025 13:00:10 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:76f9eb07fd39ec3202f7a15b37d5429dd3b1edbfe4c32a914320944ae5cb8bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.0 MB (318046600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3034f78e5badb663e2f50b27003c6f5999b3bfb09a5a46525d9ba997700d930b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:21aa15808dc85b52fca40d40118565ddcd1b7ca60220d34328c38ccbc43c6ec1`  
		Last Modified: Tue, 14 Jan 2025 01:34:07 GMT  
		Size: 47.1 MB (47131782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba976031c967b4215afb8ec45dd7db082bb0d532971c83a1e9acaaa24c91981`  
		Last Modified: Tue, 14 Jan 2025 04:59:37 GMT  
		Size: 24.1 MB (24057754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41403619947915f481f99b2b28eecf7aa168ff32ff64e044d73a504ac7472026`  
		Last Modified: Tue, 14 Jan 2025 09:09:48 GMT  
		Size: 63.5 MB (63498283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a63cbd668c99b32baa3a88a9298c02c22ab49ca16b889143b19cca1ed34c77`  
		Last Modified: Tue, 14 Jan 2025 11:15:21 GMT  
		Size: 183.4 MB (183358781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2bf1e3ba440aebd60ca46d51930af97653389a33635121e8f5bd73830a43f75d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15294675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14bf32054c104be3d3381618b5c360e0db2d6b2c7490f0488d421a0cf7d7533`

```dockerfile
```

-	Layers:
	-	`sha256:04571792130603857f093b41ea98376a26344db408bc745b4c87eefd65975728`  
		Last Modified: Tue, 14 Jan 2025 11:15:19 GMT  
		Size: 15.3 MB (15284135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c70a1a5bc411f177e1b25fd6a73313087cf5dae458f60beb639d7f5a37e27e22`  
		Last Modified: Tue, 14 Jan 2025 11:15:18 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:824fc1fe5550ab28263cd089192b340a0231f7fc291b96431a5414055f240016
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
$ docker pull buildpack-deps@sha256:42d7b1aa9523c41d0706d716059774a5339ef9eff81732cd005cced66180810d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72538042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1456917498963d78260f6047d96e9ae5da337da973e2add039994a1c587c54`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 01:36:22 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b550be6cb62359a0f3a96bc0dc289f8b45d097eaad275887f163c6780b4108`  
		Last Modified: Tue, 04 Feb 2025 04:37:13 GMT  
		Size: 24.1 MB (24058355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5e12a83fe4a7cb4e76f6fcc87651f6f22f1a6731dc00a5220a624343bcc75376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4366473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a3df9f3102541c5a0f162a43e695ce533b0c1013e1f7cef3bf1b926c193625`

```dockerfile
```

-	Layers:
	-	`sha256:296acce62133a37d0eb516ee2e6522e9f01ff2e94ff39445b822447fe3075389`  
		Last Modified: Tue, 04 Feb 2025 04:37:13 GMT  
		Size: 4.4 MB (4359309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5a7db7c9a3b4f61541a7a348619b6fe822b816462b9a8d93898ea295f5cc4cf`  
		Last Modified: Tue, 04 Feb 2025 04:37:13 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e764456a3e6c6389335e0ff69bdace1d13c5b030d304243e1722290b471c286a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68739676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935f4abb4053724cc68a4354ed014db1217540a036a7a3be554253d0245f80b5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8816181beac5d7674f87060fb5deb0c2c6221a62562265e16f54a617961cbc53`  
		Last Modified: Tue, 04 Feb 2025 01:38:08 GMT  
		Size: 46.0 MB (46006574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28060e71ea1173228ae8eefd6f5fb4296e8c1c73672a593f2d0d8e6e5483072`  
		Last Modified: Tue, 04 Feb 2025 08:03:04 GMT  
		Size: 22.7 MB (22733102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e186710650f352511d1d5a8d92e82b4ab611675b2a2c1375576087c3ddccab51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4370057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7549865aecc31cfe80ffb5ae0b5f574d035521979b19941329b24f42049e4458`

```dockerfile
```

-	Layers:
	-	`sha256:a2a0e3ffc25240693dd5981e32252a6d46b6492deb1caf4f83d8df12945ab3ef`  
		Last Modified: Tue, 04 Feb 2025 08:03:04 GMT  
		Size: 4.4 MB (4362825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4285e68bcbab8f2e3fa5e86740901937dd15fa0a0ba0e735aae994683fcc1a03`  
		Last Modified: Tue, 04 Feb 2025 08:03:03 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5464a6c00bf3369df4e693237564ff47e99bdd69bedd99f741b52db54e54d73a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66144137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65bc793d549914afbf589b58b35f4dd5809625733da540c83cf4151be1bae929`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bf65c309bba1c843ac26792f2d942bca2d7bfcc7024ba331cdfbb762d7573e8a`  
		Last Modified: Tue, 04 Feb 2025 01:37:07 GMT  
		Size: 44.2 MB (44184052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dba4073c18c1d2882f0eb9a2b0d9bf057770ac1b8829e3e149a095273df800`  
		Last Modified: Tue, 04 Feb 2025 10:41:49 GMT  
		Size: 22.0 MB (21960085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:00aa2b046765f483b718594d34141d1f51f7fd20833bf7286ffa4b129556ece0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4368838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cb903435b396d5ad4513c37e475a0f08b129bf393393a9e2530643c7ac14bd7`

```dockerfile
```

-	Layers:
	-	`sha256:34bb158550658f03bcce8efa68c7969bc65c471a9e506cb28d798eec15a2076d`  
		Last Modified: Tue, 04 Feb 2025 10:41:48 GMT  
		Size: 4.4 MB (4361606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f66f515e983898730e103baf32e4c46a679bce32182fa75c84d83de2c26f414f`  
		Last Modified: Tue, 04 Feb 2025 10:41:48 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9a4473adf94868119cd23aba34822796765e1e9ca2940b49af9d2c4a69981be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71904981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea33a0aedad9c06ff0e0a5c609080c1e233bec6767c5bf71303b3517faf7bd12`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193c44006e77abbadfdd7be72b4ab6d7a5c08640ef575970f722b798ee7800ac`  
		Last Modified: Tue, 04 Feb 2025 09:00:06 GMT  
		Size: 23.6 MB (23598428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a4f6f6f87f04b8778fa5ec2ac9bd44ab8d4272d110e8ba102b99dc2e2f5eefce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4366838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e487cc9f27cd8a6885e25366917d0762a29ac694a53b4e83c7cdc71e66e323b`

```dockerfile
```

-	Layers:
	-	`sha256:93abb4f4a6447eac7f2ae14bcf7f21dccbf201596f3d540fef65c480fd0d530f`  
		Last Modified: Tue, 04 Feb 2025 09:00:06 GMT  
		Size: 4.4 MB (4359582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e44aa7ce5f133036d4aa1d5fca2e277494c35e7224859760bf9d33b7ae677652`  
		Last Modified: Tue, 04 Feb 2025 09:00:05 GMT  
		Size: 7.3 KB (7256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5ae5647ace04cdeb0d18fa92a5458b98739d5e1b6a4e84972df6d75f83e25f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74356794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69579a1de6ce4d9dc06535f0f3c4ae3e546e5af273b2bd63f1fcc6a8d2e2d5a4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d6abb78404200438eb560450e089a4e7707a23d5ec913df260500d902666670a`  
		Last Modified: Tue, 04 Feb 2025 01:36:35 GMT  
		Size: 49.5 MB (49457456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7d7e5b6420845d0479145c8a18a31030093be0de73e11194d97fee1ac58ef5`  
		Last Modified: Tue, 04 Feb 2025 04:23:48 GMT  
		Size: 24.9 MB (24899338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d76a6d719652aac549ba39a4834d8132fc60ef855aabe24f97e463e68ee6de4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4363503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ef9c8e03996088176ba3cc1763716840532982c3c319cd6ca66ba14404d3c3`

```dockerfile
```

-	Layers:
	-	`sha256:745272fbc1c3fc0422b6ee341b729acf588740860e6a4f1e48f81e7ddff3effc`  
		Last Modified: Tue, 04 Feb 2025 04:23:47 GMT  
		Size: 4.4 MB (4356366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d54d9627cb1d90d284779bac9fb37ec6014e715706131fbe1387006abffd9bd`  
		Last Modified: Tue, 04 Feb 2025 04:23:47 GMT  
		Size: 7.1 KB (7137 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:7e82a0704e62d860a1aedcddb8d8649f97cf31831f64bc7cca3b3b57d143e5c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72410267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b93d76303f85bbe0d4d9125b1ba100a20c6c695a5ed02a407481017ce52c3617`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:12e528bcd428b4b8475a045cfdce724675384eedf195bad13ce8015853db632c`  
		Last Modified: Tue, 14 Jan 2025 01:34:57 GMT  
		Size: 48.8 MB (48758103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dede5b838e92cbab015cc8e31645fbe220ba02a56693e3a7a144e0a5428690`  
		Last Modified: Tue, 14 Jan 2025 18:10:17 GMT  
		Size: 23.7 MB (23652164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:748b0707022a125c271b74edb18d3879dc9255eac8b1414f8c2ae6fd4c121716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 KB (7003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8762ff7a77a47447b52f9c5837805de7f8f22ee4d1be2cfde565f6d959f16523`

```dockerfile
```

-	Layers:
	-	`sha256:68a0baf3a618dcbd62663d3685d9fc7dbcc554f6503f61dc83b86d7a287f8558`  
		Last Modified: Tue, 14 Jan 2025 18:10:15 GMT  
		Size: 7.0 KB (7003 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1e45989e97eaefa92658fd519fe2bae68cf9b053f0ab1b4f97d2735d21aba44c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78030525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0f70646e162cc979805350ac13127a566de8fb22c660b84d7bbd3faa2f3a5e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d32dc8295067a6f744a1fca9cfffe021a324e651f2834ad7b587e0380c3f2981`  
		Last Modified: Tue, 04 Feb 2025 01:37:34 GMT  
		Size: 52.3 MB (52312857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f161b1ac6fcd1e84495441a30458604c921f0c00816d0cd0926964e56d9717`  
		Last Modified: Tue, 04 Feb 2025 07:24:32 GMT  
		Size: 25.7 MB (25717668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c2a7f7c65904bc8dbcef3f3674f9caa66ce22f118b10c07c5675c7bc71d3047c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4371005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b9b8c3614fab2c939b24f0810da2c3fa1417067587c3105ac1f38654dd8c69`

```dockerfile
```

-	Layers:
	-	`sha256:65fc8bdcff2c2f6b97523146ca1a93865fa69badfea9f63fe7fe97f682f0b786`  
		Last Modified: Tue, 04 Feb 2025 07:24:32 GMT  
		Size: 4.4 MB (4363803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a2d971f0014ca2a549954a195e82af206f6943ced95309a2c4f0a7537e5c7d2`  
		Last Modified: Tue, 04 Feb 2025 07:24:31 GMT  
		Size: 7.2 KB (7202 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b2a040f9b5018f30ff73eeec1b0fe2f17a7c4929c613c58f2b112dbcc04b56e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71189070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6395dd5d74061c3b3bb036f052a372a32e9397377bb49e680986df2988310a3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:92bc3bb38690fde96c4bb788f15f365b04d4cb8ab9368675dc9294bc24a9c7b6`  
		Last Modified: Tue, 04 Feb 2025 01:37:03 GMT  
		Size: 47.1 MB (47131492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe7257ceffda4bd6219bda9d63efd9f5fc932de95d2f5db69f3d95df88e73b0`  
		Last Modified: Tue, 04 Feb 2025 07:30:08 GMT  
		Size: 24.1 MB (24057578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1cd79d9353a8a124773d7df05bae9236f4c1332118a1326552145122efe1b76e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4366169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a06dc43215ca62307e19d496fb94d3cdbb3d051126d2acbe246a73e1c75a1ff`

```dockerfile
```

-	Layers:
	-	`sha256:c5153387a5e1a2df7538970109cebfccd70cb85fd9c58daf5aad24f956ff7702`  
		Last Modified: Tue, 04 Feb 2025 07:30:08 GMT  
		Size: 4.4 MB (4359005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d92a83e28f3acadfd1ec9397c65d21dea67b1ad648ce759c72010c142c2c10c`  
		Last Modified: Tue, 04 Feb 2025 07:30:08 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:b8921eb6d9c99f9c2bf37f929be3c7a74c50a58149662f72b4dfd90591547e5a
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
$ docker pull buildpack-deps@sha256:107b7c021186efe3ed164cfea1c3d06c8ed6b8ce4582f691ff74a2dc4901a562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136932334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc6260661cca62da45094b3d5d01eb10b3ae352ca934691651dd8543956046a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 01:36:22 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b550be6cb62359a0f3a96bc0dc289f8b45d097eaad275887f163c6780b4108`  
		Last Modified: Tue, 04 Feb 2025 04:37:13 GMT  
		Size: 24.1 MB (24058355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35af2a7690f2b43e7237d1fae8e3f2350dfb25f3249e9cf65121866f9c56c772`  
		Last Modified: Tue, 04 Feb 2025 05:19:13 GMT  
		Size: 64.4 MB (64394292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c45671abb650eed88ec7038f7152842ad8d557322d1c488be20f05be096cb46c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7760401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e2a1f4e1a96a61d654b4ceb41ea6775eaade5e6d735639e5bbea80e9f6294dd`

```dockerfile
```

-	Layers:
	-	`sha256:b87149b2f1486609a2af0770d2c2c37d036fd5e551b650c92f01ea43a97e54c9`  
		Last Modified: Tue, 04 Feb 2025 05:19:11 GMT  
		Size: 7.8 MB (7752746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16de0d9ec26360b8605a9e23ae24c8fa01bba49c7df7a2c647e0c7c43e7a807b`  
		Last Modified: Tue, 04 Feb 2025 05:19:10 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4485452def37f53d9fea2e251dce6eec0c7a015f96823123284127e52bd259de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130743483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4bd79e1728ba3eb164b6a77dc3f9b0cd9778a70d2143f9d9af57d9e10a42a0d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8816181beac5d7674f87060fb5deb0c2c6221a62562265e16f54a617961cbc53`  
		Last Modified: Tue, 04 Feb 2025 01:38:08 GMT  
		Size: 46.0 MB (46006574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28060e71ea1173228ae8eefd6f5fb4296e8c1c73672a593f2d0d8e6e5483072`  
		Last Modified: Tue, 04 Feb 2025 08:03:04 GMT  
		Size: 22.7 MB (22733102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f77895e90931fefcb9b0f936aeec6e8c95f160c764c504ceb6084ffc29b46c`  
		Last Modified: Tue, 04 Feb 2025 10:20:41 GMT  
		Size: 62.0 MB (62003807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9325e1f31ac79d5ec224fd4a72d88769f24ae26a8b0657571c7ed3ab028f0b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7762027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78cbcdcc4c7120567403bfd7323fcb4c9cfc1f4ad85dd84655b4106038f895e1`

```dockerfile
```

-	Layers:
	-	`sha256:787a1a81ca68983478e9b85146549b7060b5bda7b817fb5fa748e29968505496`  
		Last Modified: Tue, 04 Feb 2025 10:20:40 GMT  
		Size: 7.8 MB (7754304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9ae5dbc955356ce8d85cb9395d5a07e003732510094b71b218d7c7f691b41fb`  
		Last Modified: Tue, 04 Feb 2025 10:20:39 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:49e4ccaedbca671c339d8a55242d7f25e1af167a096aca68b56da8a26e979622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125784661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5d6202e1e5273856a4827dd5f9a1aaf9c5c9df9e95e406f72acc587373ce0c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 01:34:58 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787291d61ca82895d27d086bfaf14ce01f401dfbf42f462addc8d1cae464ebab`  
		Last Modified: Tue, 14 Jan 2025 08:58:07 GMT  
		Size: 22.0 MB (21960077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6667f6e75dc8bed2e36123666ac457a4e0228141514ab32e65b9c6f6c7960e3`  
		Last Modified: Tue, 14 Jan 2025 16:15:27 GMT  
		Size: 59.6 MB (59640375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f893443c0cff99fae6cfd9ee2d82f7d9fa1764c42e4b44d6bd02b54a5f8860e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7761753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71830b5b97fe489d694c4fdd593c37b208f010a9b30f5fbbd200b1d5bb8f78f0`

```dockerfile
```

-	Layers:
	-	`sha256:ed0713d12be1303423be5246de90d43ee0ccba8f617f41d991598bef4a257e57`  
		Last Modified: Tue, 14 Jan 2025 16:15:26 GMT  
		Size: 7.8 MB (7754031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dab6ec41bbe5e21c735259ad96692c0dc9cc772b9c0cf51e02e186b1620bc8af`  
		Last Modified: Tue, 14 Jan 2025 16:15:25 GMT  
		Size: 7.7 KB (7722 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3d3e7297c13b3097bf5fb9991ffa9aad0816798a907a8fff792165491174b39a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136261554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413ebeaa354b3c0feb020579c81777bbfe6e0b44434cbb51e0423a9a5e072539`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b85d68f8a4dce392d372c8a196863eac6d111c36b714179b4ab30e00c00d1`  
		Last Modified: Tue, 14 Jan 2025 06:59:53 GMT  
		Size: 23.6 MB (23598225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936252136b926e9bca27f4a5442f6a5d10c0ea4a23ca8b30c65de1bde666d082`  
		Last Modified: Tue, 14 Jan 2025 13:31:06 GMT  
		Size: 64.4 MB (64356433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e54b58bc89d63d6cb7a969a37a81bd05045e92b0531f2dea017d34389f50b348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7766898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cfdf225184ecb259a96744ec5072a8b6321e328e75488d08232ee1c90c8287a`

```dockerfile
```

-	Layers:
	-	`sha256:ee5a579a1304a0cd9ab66a341c82f90bd0673cbb06d2d921649dc6204d1298a5`  
		Last Modified: Tue, 14 Jan 2025 13:31:04 GMT  
		Size: 7.8 MB (7759151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4b7039d4910144475f784c47b0f938b47a0c5c3de6783cc5280520c1dea87bc`  
		Last Modified: Tue, 14 Jan 2025 13:31:03 GMT  
		Size: 7.7 KB (7747 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d1e072586740069d1b5e9086fdcd828de918bfb913d5055e1aaa194f62dcc265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140593719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29f7944ff637b8f0ba1c24926e7d9ef677ee299088eb49272b3ed9d4d155cfb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d6abb78404200438eb560450e089a4e7707a23d5ec913df260500d902666670a`  
		Last Modified: Tue, 04 Feb 2025 01:36:35 GMT  
		Size: 49.5 MB (49457456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7d7e5b6420845d0479145c8a18a31030093be0de73e11194d97fee1ac58ef5`  
		Last Modified: Tue, 04 Feb 2025 04:23:48 GMT  
		Size: 24.9 MB (24899338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43394bbbaab482132a05c8eb702c9ebbbf5ecccd558ce05fdf40c651b7fbfa10`  
		Last Modified: Tue, 04 Feb 2025 05:15:47 GMT  
		Size: 66.2 MB (66236925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9a8c7b49ce3106d816ea038fd374c442087a4e89e2fc93a79ec4684633bac082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7756451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d5b2ac5fd703de6ab1eddd79d25bbe48d83b138aa053a7a88e51177e6a976fd`

```dockerfile
```

-	Layers:
	-	`sha256:9d2a829989dc2c4ace1d5075358dc1cf0e96b3108c0e3b1e30669aa7592e69c9`  
		Last Modified: Tue, 04 Feb 2025 05:15:46 GMT  
		Size: 7.7 MB (7748823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d51ba6d7dd98693c417109d9f16fa8a019ed6cf65c04b4b463211d4e1d1ea1b9`  
		Last Modified: Tue, 04 Feb 2025 05:15:45 GMT  
		Size: 7.6 KB (7628 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:fe602d939df4cbddd8102a3ecbfbd2b79407c0d8a77a3c3a8b61111134ca7a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135706996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c87c17f18e534fcf9eaa672e16e2832528995e9e5780ff4c8964ebef619f07`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:12e528bcd428b4b8475a045cfdce724675384eedf195bad13ce8015853db632c`  
		Last Modified: Tue, 14 Jan 2025 01:34:57 GMT  
		Size: 48.8 MB (48758103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dede5b838e92cbab015cc8e31645fbe220ba02a56693e3a7a144e0a5428690`  
		Last Modified: Tue, 14 Jan 2025 18:10:17 GMT  
		Size: 23.7 MB (23652164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be7513211e793708951d273ea21ae802b4bdb4109f4b12ca6122e317851db90`  
		Last Modified: Wed, 15 Jan 2025 02:00:51 GMT  
		Size: 63.3 MB (63296729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:63f9dd3ac1b3f3fb150b43d7ee5d7172d3f9881b5149b99d19d50bfb75821e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:328981011361d0b51ce891a6cbbdd73023d076afad56601a031dafc25d1c316d`

```dockerfile
```

-	Layers:
	-	`sha256:ea2b61c81e84d989128047eb14c01db001abea44f3d40a2da08f942d63cb38cd`  
		Last Modified: Wed, 15 Jan 2025 02:00:45 GMT  
		Size: 7.5 KB (7497 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:05b4402223200277f406f99fc728e47988998b5946ff282b1a2f2b55db8967f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147875066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07253a39195775999a73cfa312e0fa0c5fa1cb97359e3cf5503e14f02d7368a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:60b6379697eb1bdc0a74d6aa762f7f8e36a4a46031b019e2c7651c9723194c8b`  
		Last Modified: Tue, 14 Jan 2025 01:36:59 GMT  
		Size: 52.3 MB (52313137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b1d1b75ad07ec92cebf5f30e6612d80907cb5a7323fdef7921893e816a53be`  
		Last Modified: Tue, 14 Jan 2025 05:30:15 GMT  
		Size: 25.7 MB (25717439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395bc8910e96064c02227d340de0ac8d0234f64dd58802df0e9bd0891ad39050`  
		Last Modified: Tue, 14 Jan 2025 09:41:58 GMT  
		Size: 69.8 MB (69844490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a9d572ddeddf65e9c94b552da6a41ddb37bb717818328f59458a028ff53349cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7768145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee4e94cc9d33bf313cfc300eb9c016f08f8e9c4621491174b10461db746fb4d`

```dockerfile
```

-	Layers:
	-	`sha256:231c3fce7984cd3e3de5dd5d140d65478f0236395546611c454b0e0421150d73`  
		Last Modified: Tue, 14 Jan 2025 09:41:56 GMT  
		Size: 7.8 MB (7760453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b75b5ea659daa8cc266903efd448b1e7d046a092e5d48598c2331e3ca388f11a`  
		Last Modified: Tue, 14 Jan 2025 09:41:56 GMT  
		Size: 7.7 KB (7692 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5261ec0a644e8aaf0410d07b3f6775921eb9dfd59122eb9155529fc4dd8e12d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134688525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67a46e44795d80467cac123f20812bc46798d0bebc2ca9b6c72285a776183381`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:92bc3bb38690fde96c4bb788f15f365b04d4cb8ab9368675dc9294bc24a9c7b6`  
		Last Modified: Tue, 04 Feb 2025 01:37:03 GMT  
		Size: 47.1 MB (47131492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe7257ceffda4bd6219bda9d63efd9f5fc932de95d2f5db69f3d95df88e73b0`  
		Last Modified: Tue, 04 Feb 2025 07:30:08 GMT  
		Size: 24.1 MB (24057578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800fd1d6411dfa44ccdbe5db47bb7e970909c1a08d63328dfd165607beb67e7c`  
		Last Modified: Tue, 04 Feb 2025 11:34:34 GMT  
		Size: 63.5 MB (63499455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c2ca21cdc0403c9f431731aa97d0c4db85a946a2bacf211d0cfe3ee4e5418bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7759606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5459c93da646c41b36d9e5eeee87162119e171e15ef61c37b7f488c907ac80`

```dockerfile
```

-	Layers:
	-	`sha256:e5d1da80e53060d3414c9fee17945ae782d9600f01876fe0136f6c4d962f8be8`  
		Last Modified: Tue, 04 Feb 2025 11:34:33 GMT  
		Size: 7.8 MB (7751951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd51d33d5be0950a97f8ce96f83c03da82e3ff767c4f51b3c48d301197f978df`  
		Last Modified: Tue, 04 Feb 2025 11:34:33 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:bullseye`

```console
$ docker pull buildpack-deps@sha256:d5b59dd4f8a672e49190a9ce5dcf7b972172402f7847f9ba403e6e6bdce3fce7
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
$ docker pull buildpack-deps@sha256:d2e93687f21da5853e92d5d2394b09c22c04252f3cf160684f835ca1a616f0be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.1 MB (321121810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246e22f571a0f5c491769a43d42a15a65de640fdb1075fdba4c2f3ca90722ebb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:478cb73646107d7b3f891aa53abaed926667463844c07b1d924bd760ae03f38a`  
		Last Modified: Tue, 04 Feb 2025 01:36:37 GMT  
		Size: 53.7 MB (53738873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0388f0d5bf1adc15e551cceee5a85f21b1ebf5b13c380ee0e941c5d55013598`  
		Last Modified: Tue, 04 Feb 2025 04:37:42 GMT  
		Size: 15.6 MB (15558271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d473f760e53d3d50afd1cebc7113387023a04ff8ec34073c4412b465ccc2fc5`  
		Last Modified: Tue, 04 Feb 2025 05:19:08 GMT  
		Size: 54.8 MB (54751917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d32181a1ed55cf7269c27a7a18858d7a4679d9fccbc616d5d878b6ddded25b`  
		Last Modified: Tue, 04 Feb 2025 06:14:22 GMT  
		Size: 197.1 MB (197072749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c20b6d0d8cf0bbb5a04f01ad8cd51019ec51de92a5f18c0de949f2e61d1189ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15081760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66acaa1540629854cd364629b821d7ce5c76de2a55eb5d7a1618e1d5ba5a3adf`

```dockerfile
```

-	Layers:
	-	`sha256:dc4a6b5f744e6d3c4ceaaae6439e7eef4457996ecf9f57bb36742af7b5636be1`  
		Last Modified: Tue, 04 Feb 2025 06:14:19 GMT  
		Size: 15.1 MB (15071528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73f76a037f50e1f86156c2121d6d9be40001cbdbec315dc9419f83848a2851e5`  
		Last Modified: Tue, 04 Feb 2025 06:14:19 GMT  
		Size: 10.2 KB (10232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e4d9a678765a1a4b36cb358955286fee41d3220580c5e1a5baac558d8916c560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.9 MB (281865027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a91082578b03acb86ea134738e540ea3f4dc35583a8c4c0ead0e3c632257ec80`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2d8b4e71b0057b288fa0b7cf9b1d15edc9bec9dc37df63d3463ce28e4f414dc9`  
		Last Modified: Tue, 14 Jan 2025 01:35:36 GMT  
		Size: 49.0 MB (49025062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7055bc7f040fce3e9b8f05fd7f56b8a568950e082ea8ea3aa96cf99f49523ca5`  
		Last Modified: Tue, 14 Jan 2025 08:58:39 GMT  
		Size: 14.7 MB (14673832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681398f28ce19a7af317e3774529df465ed1770ca10164fdba3b20f23a5d8026`  
		Last Modified: Tue, 14 Jan 2025 16:16:27 GMT  
		Size: 50.6 MB (50640646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526075af1d9c0b728ff0e8888d46f79edd8fb9bacc975b1eb824b9bca2c06ee2`  
		Last Modified: Tue, 14 Jan 2025 21:56:34 GMT  
		Size: 167.5 MB (167525487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8bf8fc0ea3d27fb38bf14664e4840df434a73985f82c716ca25a8d17dc10e1bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14882567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872ff66c39242f7fa5d2c10b491392327cc6c1b53521e020fa17d7d0e2850cf0`

```dockerfile
```

-	Layers:
	-	`sha256:e69e0689bd9054f8eca064739d1c8b693d08bec2ec5650f7353219866f3a0877`  
		Last Modified: Tue, 14 Jan 2025 21:56:31 GMT  
		Size: 14.9 MB (14872275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:067d8002d2b05e274736054645f782d61b1852b1436e0d26d6096257140c2ea5`  
		Last Modified: Tue, 14 Jan 2025 21:56:30 GMT  
		Size: 10.3 KB (10292 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:dbb29bd940d6ce2889e1c39cc81b6683adfb499d67e680dfcaed5fbba4f3f68e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.6 MB (312622972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88399fb643c94545384f7c5485ae56facab2b9a1a1565bb4af601f5685c9f8d6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dfd6b176342cb480b79cef9a7188364b0f5702ccc77422fcdb5d7d8f3f42c8`  
		Last Modified: Tue, 14 Jan 2025 07:00:18 GMT  
		Size: 15.5 MB (15544093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23ac0e9b25076f1cc90469f31bffaae783c6a3a88272620af5e7dcbe0b8202`  
		Last Modified: Tue, 14 Jan 2025 13:31:46 GMT  
		Size: 54.9 MB (54852602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5936a36467e76a2d54993295f16ff38dd2c24f30cf89a1f83a922f2440b869`  
		Last Modified: Tue, 14 Jan 2025 17:09:53 GMT  
		Size: 190.0 MB (189980217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ae8b0ba8fd091612a9687963576f73b13545fbb3ad9a144edb6a9a182046acc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15084056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f24494000d98572dbca61183102b7f0896f65ba2b83261b9f347e277f1d1197`

```dockerfile
```

-	Layers:
	-	`sha256:6947aa4dde02deb94734a78920905e8c7e6b9faffdf741577bf7bf716b79a153`  
		Last Modified: Tue, 14 Jan 2025 17:09:50 GMT  
		Size: 15.1 MB (15073744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:660f8ad159fda4b312cc890f08416761a6d93d6e239c511058aedc8a320496be`  
		Last Modified: Tue, 14 Jan 2025 17:09:48 GMT  
		Size: 10.3 KB (10312 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e1371f188b371bb212fdd0d81390dbf85709ab28ec7b27eee70183e5dd657633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.7 MB (326748309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5266d02805914d0cc09d2ed291fabb0999ab7f4bb986062d1bef17595301e921`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c2b5327eac1fcd49233dc8f6e5417e7e2efeea16edfcbff9dd025f389e15b11e`  
		Last Modified: Tue, 04 Feb 2025 01:36:38 GMT  
		Size: 54.7 MB (54675956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d372eab1872f98afed1da2c899af883a0b3a6e52e25e2690ed35b3d6f859e5`  
		Last Modified: Tue, 04 Feb 2025 04:23:38 GMT  
		Size: 16.1 MB (16062054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4520e7fd9b17628990db3e961c2d7570421849af1fe255937c0a9e48cf49a48f`  
		Last Modified: Tue, 04 Feb 2025 05:15:33 GMT  
		Size: 56.0 MB (56029876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b370f45f01968d6de3175fc994cf545ece88435b9abc17f2ed4705ac128c8d4`  
		Last Modified: Tue, 04 Feb 2025 06:14:51 GMT  
		Size: 200.0 MB (199980423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bd92c287cf99c6152f7f6cab08646996c38e4a491c76bcc3705ebc99d06f7992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15070078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea2facb97735295ed3258a51b2d9555ca11d49a07beaf4d8934198195fc6b2f`

```dockerfile
```

-	Layers:
	-	`sha256:d216381c85049dde4f65a8029d5e313e7f34e9bb9745a33902c596c23e197770`  
		Last Modified: Tue, 04 Feb 2025 06:14:45 GMT  
		Size: 15.1 MB (15059868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35f077caaeddfa1dda713b6d99bc1fadbcc6d2bd1f1ed6a4d3de3cb510bdade3`  
		Last Modified: Tue, 04 Feb 2025 06:14:44 GMT  
		Size: 10.2 KB (10210 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:845de4a60c3498098593185102842603fd86f171c9d51bcf4187a552ceb04f5d
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
$ docker pull buildpack-deps@sha256:7f278ea0e1aacd2ac3d797daf838446f76bb7fe002dabc269e3d32d27f939f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69297144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0422b90f4807ccd9614ef9118463e5e80990c61726943324bac5a3975fad401e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:478cb73646107d7b3f891aa53abaed926667463844c07b1d924bd760ae03f38a`  
		Last Modified: Tue, 04 Feb 2025 01:36:37 GMT  
		Size: 53.7 MB (53738873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0388f0d5bf1adc15e551cceee5a85f21b1ebf5b13c380ee0e941c5d55013598`  
		Last Modified: Tue, 04 Feb 2025 04:37:42 GMT  
		Size: 15.6 MB (15558271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2c10d26009d377cac6e65d06092dfb61fd1d729963f4514dca185a4cb86d039c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4492427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855812a9ac3b6ebaba4c3495c0e7c909ee453450b17678849e202a3eb77091b0`

```dockerfile
```

-	Layers:
	-	`sha256:1cd436b097ec741147c69b351e4e2e79a1af953b797934f02c828121818aa7d7`  
		Last Modified: Tue, 04 Feb 2025 04:37:42 GMT  
		Size: 4.5 MB (4485627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d1e31308f71b28230d96394763b0aa71c5225339cda77c606855758ef2d769e`  
		Last Modified: Tue, 04 Feb 2025 04:37:42 GMT  
		Size: 6.8 KB (6800 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d095285c12a1b99487b28af042f4ce855d09e71ccf4cfd805149f321614f1a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63698612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb55cfbf146794456e45adaf1201ab08eceffde02bbb25893d450fe648223cb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7dafa8b67e9b20318af5959237616a556f517d3359b4cec5bc2b6899a7c8336b`  
		Last Modified: Tue, 04 Feb 2025 01:37:44 GMT  
		Size: 49.0 MB (49024794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bfe1cf520a5741b594ed015a44e9386892026b5310b613c2207dbb1073919e7`  
		Last Modified: Tue, 04 Feb 2025 10:42:22 GMT  
		Size: 14.7 MB (14673818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7e0941255238d0b686ba4d057744cdb1334d8412c6bbe0222601c199a7825004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ea4476b8d9fb50bf3cb725815db433c4336d055be7f7d0270018b1fd893d64`

```dockerfile
```

-	Layers:
	-	`sha256:f5c4256cb66c59fa61a61b00edd596fb4ea9df538ddabb04405f6677e4055ce8`  
		Last Modified: Tue, 04 Feb 2025 10:42:22 GMT  
		Size: 4.5 MB (4487263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de126843dd3b845a38a5d44d84e924dca553937f671c097df333fd6d0bc14e19`  
		Last Modified: Tue, 04 Feb 2025 10:42:21 GMT  
		Size: 6.9 KB (6861 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:699d0f65411313f79bde102e935b03f05646e0ba90f9e589b53441d582595934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67789750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a6daba633b8e3b34a7f1ce1727329a37c04f9919263899a96fa7cf6ec202154`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0038ef039a89ede34c57806e684dc9d9be7dcd22d3c08b90deb36bb22a2c7122`  
		Last Modified: Tue, 04 Feb 2025 01:38:11 GMT  
		Size: 52.2 MB (52245695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c7afb1aa0f9672a06c4c7eaa6b7c7e111a91a8d45272dce1e361ac0b0ed79a`  
		Last Modified: Tue, 04 Feb 2025 09:00:33 GMT  
		Size: 15.5 MB (15544055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9d5ed3cd0162799c08609a036c8b39212da061b12174a4a202fbd657186c301d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4492122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c58d44733426488446ed36c9936b91cb83423e352e68b6fe40e74bc1561106`

```dockerfile
```

-	Layers:
	-	`sha256:87a5d01b879d7622edad54e86b025c3a014ac7f446b1556f2f242b7a52f27181`  
		Last Modified: Tue, 04 Feb 2025 09:00:32 GMT  
		Size: 4.5 MB (4485241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb2dad3364e37229e045f4ea4ac1d95ca1f1dccbe56ba9ffde542f483711d0ea`  
		Last Modified: Tue, 04 Feb 2025 09:00:32 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:fe810b67717e1433e97cbf12d1c8cac82a2bac40e14211e3c6b9164d68cf85e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70738010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b913c0ae133558275edee8f3575418d30a1f8c5cfe7b0861b45e33a499f4d32`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c2b5327eac1fcd49233dc8f6e5417e7e2efeea16edfcbff9dd025f389e15b11e`  
		Last Modified: Tue, 04 Feb 2025 01:36:38 GMT  
		Size: 54.7 MB (54675956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d372eab1872f98afed1da2c899af883a0b3a6e52e25e2690ed35b3d6f859e5`  
		Last Modified: Tue, 04 Feb 2025 04:23:38 GMT  
		Size: 16.1 MB (16062054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f08e0e3e50b65e876418183cfadf4b9d25087eae4563596822b7cbdd5b537b3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4488847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8d4a982f05b421f194496a7acb871eb45d55828addd847cd37b531dceb1e2e`

```dockerfile
```

-	Layers:
	-	`sha256:eca027a0d706d22c12a86d884435eb6e047b4cf46c279a5c80331993e00d3d10`  
		Last Modified: Tue, 04 Feb 2025 04:23:37 GMT  
		Size: 4.5 MB (4482068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29f26919f0b635f677f0d4b88840cf876653771192f92c6058a0ed2d4a72a971`  
		Last Modified: Tue, 04 Feb 2025 04:23:37 GMT  
		Size: 6.8 KB (6779 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:f8b44d871c904becd02992c1785520907b4166b7974db9aead2789ecbc5d00e0
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
$ docker pull buildpack-deps@sha256:4814e93af668ad776156987b0a30c8b308b118e01fbbd17f741b791b8851bad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (124049061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e581d121fb96975fea39e8d8b79c9c4de4cb6ac154abf3542985c05e89625228`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:478cb73646107d7b3f891aa53abaed926667463844c07b1d924bd760ae03f38a`  
		Last Modified: Tue, 04 Feb 2025 01:36:37 GMT  
		Size: 53.7 MB (53738873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0388f0d5bf1adc15e551cceee5a85f21b1ebf5b13c380ee0e941c5d55013598`  
		Last Modified: Tue, 04 Feb 2025 04:37:42 GMT  
		Size: 15.6 MB (15558271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d473f760e53d3d50afd1cebc7113387023a04ff8ec34073c4412b465ccc2fc5`  
		Last Modified: Tue, 04 Feb 2025 05:19:08 GMT  
		Size: 54.8 MB (54751917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ef9e6950a308d27ad0fed70063500c67d5f94b60458bf35e69a461c78d601501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7715539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c9ec6144be5fdec793e06b9bfe76a1ab2b4f60224d307ec385d56b9d387f4a`

```dockerfile
```

-	Layers:
	-	`sha256:52a22ae317e2876eea325b36b2cc60b6f80c3cb88a7dbdba1853d7465f8d0e0b`  
		Last Modified: Tue, 04 Feb 2025 05:19:07 GMT  
		Size: 7.7 MB (7708186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d5117857f7ca0d3e1bf3a461cdcb72b1ca27dbcbcf55684d0fb889d6ed4006b`  
		Last Modified: Tue, 04 Feb 2025 05:19:07 GMT  
		Size: 7.4 KB (7353 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d774943785660ecc2de823027779a925c87651bd40f06fbc6b58b9de1c8bd809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114339540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d5ee24dd46e5c5e26ee74d9f511fcc3735ef780de9003547e3a914b976008fd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2d8b4e71b0057b288fa0b7cf9b1d15edc9bec9dc37df63d3463ce28e4f414dc9`  
		Last Modified: Tue, 14 Jan 2025 01:35:36 GMT  
		Size: 49.0 MB (49025062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7055bc7f040fce3e9b8f05fd7f56b8a568950e082ea8ea3aa96cf99f49523ca5`  
		Last Modified: Tue, 14 Jan 2025 08:58:39 GMT  
		Size: 14.7 MB (14673832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681398f28ce19a7af317e3774529df465ed1770ca10164fdba3b20f23a5d8026`  
		Last Modified: Tue, 14 Jan 2025 16:16:27 GMT  
		Size: 50.6 MB (50640646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1c91b0f90f1ef91ce5f6c48aadb2477540546f65adf63b3d90982ec86f15a6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7716983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d58caa9f61dfed2e570b426db1959ba75ae97217fa6a9a80716c68ee7e4355f`

```dockerfile
```

-	Layers:
	-	`sha256:d98b7e41b3cd63c512f218dfab9c9d65b81f3eea63c8b836f660301b020c5d66`  
		Last Modified: Tue, 14 Jan 2025 16:16:26 GMT  
		Size: 7.7 MB (7709570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3bdd7383a4b1f4d3f50aaff18c4c7bc58547a6b215c9b01676e6337e8dfb72a`  
		Last Modified: Tue, 14 Jan 2025 16:16:25 GMT  
		Size: 7.4 KB (7413 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7cd12446ba7224b5c2917b1c38ea6cc66ca5d1b816e2220b6746099844d83a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122642755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c009330911b291df3f419696b4f356ad17a61817d491820586e38c2b0009d1bf`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dfd6b176342cb480b79cef9a7188364b0f5702ccc77422fcdb5d7d8f3f42c8`  
		Last Modified: Tue, 14 Jan 2025 07:00:18 GMT  
		Size: 15.5 MB (15544093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23ac0e9b25076f1cc90469f31bffaae783c6a3a88272620af5e7dcbe0b8202`  
		Last Modified: Tue, 14 Jan 2025 13:31:46 GMT  
		Size: 54.9 MB (54852602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c15cf8ae3f7c2b7a8e902962590e6c9064ebc3de259521e75513e13f2e9583c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7721335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea1bc11e1597522ba927e7cf032ac12c2f5c0b48f76688a2c41cc8df5ff6d4c`

```dockerfile
```

-	Layers:
	-	`sha256:cb5b7433e723b0023aeae558a9a132cd43f7fd43bf007e6f3bfc19ad25dd8b7c`  
		Last Modified: Tue, 14 Jan 2025 13:31:45 GMT  
		Size: 7.7 MB (7713902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1092df41e57f424822625c9e363e68af5c5429b0bfca3a72c6d7952e77fbb0a`  
		Last Modified: Tue, 14 Jan 2025 13:31:44 GMT  
		Size: 7.4 KB (7433 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:9a62f978f5fdc58bc19fc0153c3642c7986206935c5123229b9400de09265b18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126767886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb73a16d07dcda55523ead47dacd4d9749d94ac0ad37187950d43b0fdbab437`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c2b5327eac1fcd49233dc8f6e5417e7e2efeea16edfcbff9dd025f389e15b11e`  
		Last Modified: Tue, 04 Feb 2025 01:36:38 GMT  
		Size: 54.7 MB (54675956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d372eab1872f98afed1da2c899af883a0b3a6e52e25e2690ed35b3d6f859e5`  
		Last Modified: Tue, 04 Feb 2025 04:23:38 GMT  
		Size: 16.1 MB (16062054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4520e7fd9b17628990db3e961c2d7570421849af1fe255937c0a9e48cf49a48f`  
		Last Modified: Tue, 04 Feb 2025 05:15:33 GMT  
		Size: 56.0 MB (56029876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4c21667e744397eb3935c16797e52b0148b9d2656c9c5df160d776ef48f8019e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7711006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50bd9c61c42af2df265f3d3c98356591cf58dbc8635d76bca719e8339597bd94`

```dockerfile
```

-	Layers:
	-	`sha256:fcedc0c587cb91d36a7804b4632555da7225541fa346b9a49d88f2ea9ef0ba0d`  
		Last Modified: Tue, 04 Feb 2025 05:15:32 GMT  
		Size: 7.7 MB (7703676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23633969f8f239808620f33b97db5f047216cba12a362fa470b4395f1a8ed0b5`  
		Last Modified: Tue, 04 Feb 2025 05:15:32 GMT  
		Size: 7.3 KB (7330 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:curl`

```console
$ docker pull buildpack-deps@sha256:824fc1fe5550ab28263cd089192b340a0231f7fc291b96431a5414055f240016
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
$ docker pull buildpack-deps@sha256:42d7b1aa9523c41d0706d716059774a5339ef9eff81732cd005cced66180810d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72538042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1456917498963d78260f6047d96e9ae5da337da973e2add039994a1c587c54`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 01:36:22 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b550be6cb62359a0f3a96bc0dc289f8b45d097eaad275887f163c6780b4108`  
		Last Modified: Tue, 04 Feb 2025 04:37:13 GMT  
		Size: 24.1 MB (24058355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5e12a83fe4a7cb4e76f6fcc87651f6f22f1a6731dc00a5220a624343bcc75376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4366473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a3df9f3102541c5a0f162a43e695ce533b0c1013e1f7cef3bf1b926c193625`

```dockerfile
```

-	Layers:
	-	`sha256:296acce62133a37d0eb516ee2e6522e9f01ff2e94ff39445b822447fe3075389`  
		Last Modified: Tue, 04 Feb 2025 04:37:13 GMT  
		Size: 4.4 MB (4359309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5a7db7c9a3b4f61541a7a348619b6fe822b816462b9a8d93898ea295f5cc4cf`  
		Last Modified: Tue, 04 Feb 2025 04:37:13 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e764456a3e6c6389335e0ff69bdace1d13c5b030d304243e1722290b471c286a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68739676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935f4abb4053724cc68a4354ed014db1217540a036a7a3be554253d0245f80b5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8816181beac5d7674f87060fb5deb0c2c6221a62562265e16f54a617961cbc53`  
		Last Modified: Tue, 04 Feb 2025 01:38:08 GMT  
		Size: 46.0 MB (46006574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28060e71ea1173228ae8eefd6f5fb4296e8c1c73672a593f2d0d8e6e5483072`  
		Last Modified: Tue, 04 Feb 2025 08:03:04 GMT  
		Size: 22.7 MB (22733102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e186710650f352511d1d5a8d92e82b4ab611675b2a2c1375576087c3ddccab51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4370057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7549865aecc31cfe80ffb5ae0b5f574d035521979b19941329b24f42049e4458`

```dockerfile
```

-	Layers:
	-	`sha256:a2a0e3ffc25240693dd5981e32252a6d46b6492deb1caf4f83d8df12945ab3ef`  
		Last Modified: Tue, 04 Feb 2025 08:03:04 GMT  
		Size: 4.4 MB (4362825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4285e68bcbab8f2e3fa5e86740901937dd15fa0a0ba0e735aae994683fcc1a03`  
		Last Modified: Tue, 04 Feb 2025 08:03:03 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5464a6c00bf3369df4e693237564ff47e99bdd69bedd99f741b52db54e54d73a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66144137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65bc793d549914afbf589b58b35f4dd5809625733da540c83cf4151be1bae929`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bf65c309bba1c843ac26792f2d942bca2d7bfcc7024ba331cdfbb762d7573e8a`  
		Last Modified: Tue, 04 Feb 2025 01:37:07 GMT  
		Size: 44.2 MB (44184052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dba4073c18c1d2882f0eb9a2b0d9bf057770ac1b8829e3e149a095273df800`  
		Last Modified: Tue, 04 Feb 2025 10:41:49 GMT  
		Size: 22.0 MB (21960085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:00aa2b046765f483b718594d34141d1f51f7fd20833bf7286ffa4b129556ece0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4368838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cb903435b396d5ad4513c37e475a0f08b129bf393393a9e2530643c7ac14bd7`

```dockerfile
```

-	Layers:
	-	`sha256:34bb158550658f03bcce8efa68c7969bc65c471a9e506cb28d798eec15a2076d`  
		Last Modified: Tue, 04 Feb 2025 10:41:48 GMT  
		Size: 4.4 MB (4361606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f66f515e983898730e103baf32e4c46a679bce32182fa75c84d83de2c26f414f`  
		Last Modified: Tue, 04 Feb 2025 10:41:48 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9a4473adf94868119cd23aba34822796765e1e9ca2940b49af9d2c4a69981be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71904981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea33a0aedad9c06ff0e0a5c609080c1e233bec6767c5bf71303b3517faf7bd12`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193c44006e77abbadfdd7be72b4ab6d7a5c08640ef575970f722b798ee7800ac`  
		Last Modified: Tue, 04 Feb 2025 09:00:06 GMT  
		Size: 23.6 MB (23598428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a4f6f6f87f04b8778fa5ec2ac9bd44ab8d4272d110e8ba102b99dc2e2f5eefce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4366838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e487cc9f27cd8a6885e25366917d0762a29ac694a53b4e83c7cdc71e66e323b`

```dockerfile
```

-	Layers:
	-	`sha256:93abb4f4a6447eac7f2ae14bcf7f21dccbf201596f3d540fef65c480fd0d530f`  
		Last Modified: Tue, 04 Feb 2025 09:00:06 GMT  
		Size: 4.4 MB (4359582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e44aa7ce5f133036d4aa1d5fca2e277494c35e7224859760bf9d33b7ae677652`  
		Last Modified: Tue, 04 Feb 2025 09:00:05 GMT  
		Size: 7.3 KB (7256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5ae5647ace04cdeb0d18fa92a5458b98739d5e1b6a4e84972df6d75f83e25f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74356794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69579a1de6ce4d9dc06535f0f3c4ae3e546e5af273b2bd63f1fcc6a8d2e2d5a4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d6abb78404200438eb560450e089a4e7707a23d5ec913df260500d902666670a`  
		Last Modified: Tue, 04 Feb 2025 01:36:35 GMT  
		Size: 49.5 MB (49457456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7d7e5b6420845d0479145c8a18a31030093be0de73e11194d97fee1ac58ef5`  
		Last Modified: Tue, 04 Feb 2025 04:23:48 GMT  
		Size: 24.9 MB (24899338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d76a6d719652aac549ba39a4834d8132fc60ef855aabe24f97e463e68ee6de4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4363503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ef9c8e03996088176ba3cc1763716840532982c3c319cd6ca66ba14404d3c3`

```dockerfile
```

-	Layers:
	-	`sha256:745272fbc1c3fc0422b6ee341b729acf588740860e6a4f1e48f81e7ddff3effc`  
		Last Modified: Tue, 04 Feb 2025 04:23:47 GMT  
		Size: 4.4 MB (4356366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d54d9627cb1d90d284779bac9fb37ec6014e715706131fbe1387006abffd9bd`  
		Last Modified: Tue, 04 Feb 2025 04:23:47 GMT  
		Size: 7.1 KB (7137 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:7e82a0704e62d860a1aedcddb8d8649f97cf31831f64bc7cca3b3b57d143e5c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72410267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b93d76303f85bbe0d4d9125b1ba100a20c6c695a5ed02a407481017ce52c3617`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:12e528bcd428b4b8475a045cfdce724675384eedf195bad13ce8015853db632c`  
		Last Modified: Tue, 14 Jan 2025 01:34:57 GMT  
		Size: 48.8 MB (48758103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dede5b838e92cbab015cc8e31645fbe220ba02a56693e3a7a144e0a5428690`  
		Last Modified: Tue, 14 Jan 2025 18:10:17 GMT  
		Size: 23.7 MB (23652164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:748b0707022a125c271b74edb18d3879dc9255eac8b1414f8c2ae6fd4c121716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 KB (7003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8762ff7a77a47447b52f9c5837805de7f8f22ee4d1be2cfde565f6d959f16523`

```dockerfile
```

-	Layers:
	-	`sha256:68a0baf3a618dcbd62663d3685d9fc7dbcc554f6503f61dc83b86d7a287f8558`  
		Last Modified: Tue, 14 Jan 2025 18:10:15 GMT  
		Size: 7.0 KB (7003 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1e45989e97eaefa92658fd519fe2bae68cf9b053f0ab1b4f97d2735d21aba44c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78030525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0f70646e162cc979805350ac13127a566de8fb22c660b84d7bbd3faa2f3a5e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d32dc8295067a6f744a1fca9cfffe021a324e651f2834ad7b587e0380c3f2981`  
		Last Modified: Tue, 04 Feb 2025 01:37:34 GMT  
		Size: 52.3 MB (52312857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f161b1ac6fcd1e84495441a30458604c921f0c00816d0cd0926964e56d9717`  
		Last Modified: Tue, 04 Feb 2025 07:24:32 GMT  
		Size: 25.7 MB (25717668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c2a7f7c65904bc8dbcef3f3674f9caa66ce22f118b10c07c5675c7bc71d3047c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4371005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b9b8c3614fab2c939b24f0810da2c3fa1417067587c3105ac1f38654dd8c69`

```dockerfile
```

-	Layers:
	-	`sha256:65fc8bdcff2c2f6b97523146ca1a93865fa69badfea9f63fe7fe97f682f0b786`  
		Last Modified: Tue, 04 Feb 2025 07:24:32 GMT  
		Size: 4.4 MB (4363803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a2d971f0014ca2a549954a195e82af206f6943ced95309a2c4f0a7537e5c7d2`  
		Last Modified: Tue, 04 Feb 2025 07:24:31 GMT  
		Size: 7.2 KB (7202 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b2a040f9b5018f30ff73eeec1b0fe2f17a7c4929c613c58f2b112dbcc04b56e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71189070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6395dd5d74061c3b3bb036f052a372a32e9397377bb49e680986df2988310a3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:92bc3bb38690fde96c4bb788f15f365b04d4cb8ab9368675dc9294bc24a9c7b6`  
		Last Modified: Tue, 04 Feb 2025 01:37:03 GMT  
		Size: 47.1 MB (47131492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe7257ceffda4bd6219bda9d63efd9f5fc932de95d2f5db69f3d95df88e73b0`  
		Last Modified: Tue, 04 Feb 2025 07:30:08 GMT  
		Size: 24.1 MB (24057578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1cd79d9353a8a124773d7df05bae9236f4c1332118a1326552145122efe1b76e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4366169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a06dc43215ca62307e19d496fb94d3cdbb3d051126d2acbe246a73e1c75a1ff`

```dockerfile
```

-	Layers:
	-	`sha256:c5153387a5e1a2df7538970109cebfccd70cb85fd9c58daf5aad24f956ff7702`  
		Last Modified: Tue, 04 Feb 2025 07:30:08 GMT  
		Size: 4.4 MB (4359005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d92a83e28f3acadfd1ec9397c65d21dea67b1ad648ce759c72010c142c2c10c`  
		Last Modified: Tue, 04 Feb 2025 07:30:08 GMT  
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
$ docker pull buildpack-deps@sha256:eaad1fbcab2ded0365c860b403c77cf52b549bfe52e1d494a43c2f6630311456
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
$ docker pull buildpack-deps@sha256:d719e1b3685b07437141f3cf9c3d496640fa957490d940fb6c8af304c9ee5b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.0 MB (249049639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f693ae883e3235266008e0e119241f5cbf9e66651e5d5e37467bde618d617335`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee445cc5e2b6b7936777d1af58476890507382191edc76cf636f7e69381a0f7`  
		Last Modified: Tue, 04 Feb 2025 04:37:54 GMT  
		Size: 7.1 MB (7095774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c481194f5cf954d821c9180450bf9cbfe7d778d31dd54b13e0f37be46d837e`  
		Last Modified: Tue, 04 Feb 2025 05:20:43 GMT  
		Size: 39.5 MB (39488061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ff89f6579baee318f96b07c9b40341a1d6992851e8ea7c38718236c6c02186`  
		Last Modified: Tue, 04 Feb 2025 06:14:30 GMT  
		Size: 172.9 MB (172929863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f3cda331a4992c50877bb591e55621583b2bc85eb6ec5bfe048dfd9afa12b82a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11463053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508568c85c5c43517a2dea7d1beefeae59140318409a07e148d327ecc388d8bd`

```dockerfile
```

-	Layers:
	-	`sha256:1b0fb76c9081098812d4f10f5a9210232acdd68a70bdce5c86529b0187833759`  
		Last Modified: Tue, 04 Feb 2025 06:14:25 GMT  
		Size: 11.5 MB (11452850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fea7c33ef084e79abab04a0097d930daa4c248972b0a5835269f659a3b9a001`  
		Last Modified: Tue, 04 Feb 2025 06:14:24 GMT  
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
$ docker pull buildpack-deps@sha256:cb005a903174af55be4fd9061bf76c495b4e36e10b7086806532cb43c95dde2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274231046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90f0b33982a82b2568cb04a4cfd62ae71d860a15bfc21a21e67fba19170c92d`
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
ADD file:c95ac39f820c01b1c0a2d18f3df09346a389f9989c91cb636f75de0e3d63c97d in / 
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
	-	`sha256:cfa2d73aa16649863373431bec34ae49863b8b03f19e2c1fa29af96b0ea254fc`  
		Last Modified: Sun, 26 Jan 2025 07:02:26 GMT  
		Size: 27.0 MB (27039007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247fcfe5b002f706b4c9b3a78341f202606a547ef405c7ad03e2e33f28fec027`  
		Last Modified: Tue, 04 Feb 2025 04:44:46 GMT  
		Size: 7.1 MB (7108060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb811904a9072aa1e8962df9982276480172376fb423cfcf8aaec3ebb4f9f8ca`  
		Last Modified: Tue, 04 Feb 2025 08:14:03 GMT  
		Size: 42.3 MB (42307263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70089f8fa6e86f416dcc916a3a84e0eb779463cd666ed04f5784d45aa423ea9`  
		Last Modified: Tue, 04 Feb 2025 10:06:46 GMT  
		Size: 197.8 MB (197776716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5d87b26854a76501137f25370979c3cedeea170eb08484a6de7863cc3ab793ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11404981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d611b10a561d0c1c1e91fca1cb463bd6a7438a1f550263f51f55fe5fa896893`

```dockerfile
```

-	Layers:
	-	`sha256:3989dddbb46fe2b99dc6e1c31bf8f63b02f6d180ab5b721f4266b7fba5596421`  
		Last Modified: Tue, 04 Feb 2025 10:06:19 GMT  
		Size: 11.4 MB (11394746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ace35bc54c917e2c6c94ff6c186d49d7dec0aec2f43deb0dd7110a21c813e6aa`  
		Last Modified: Tue, 04 Feb 2025 10:06:18 GMT  
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
$ docker pull buildpack-deps@sha256:33a46dfd834f4a61b5866da863063dccd1160f248bbfab92581f4ace71be51de
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
$ docker pull buildpack-deps@sha256:49fdc396e3e2c388288ee868f80cc46793b115a7d855635f31fa2c84af1021cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36631715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127dfc62185b034f15bcc646d5535774677fcbfdd5d0c0774c75aa4b6d84655c`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee445cc5e2b6b7936777d1af58476890507382191edc76cf636f7e69381a0f7`  
		Last Modified: Tue, 04 Feb 2025 04:37:54 GMT  
		Size: 7.1 MB (7095774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:08e2b3186b703bd630a8a64b1a730e9fe7ad1b985ef44af18ac26b7664e38634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3054780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a864cc7fb6669139bfab22092b7aff2664a4d68078104b4d3492b3e6fb1cd4de`

```dockerfile
```

-	Layers:
	-	`sha256:c152abfc25cd0a72c5a3b91acb4071bd18d4f7477647237727f28c4873d9bc27`  
		Last Modified: Tue, 04 Feb 2025 04:37:54 GMT  
		Size: 3.0 MB (3047856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7acaf0a3198eef8de38c3053abc8d01f4a671d075e57f191a1d80246b2484071`  
		Last Modified: Tue, 04 Feb 2025 04:37:54 GMT  
		Size: 6.9 KB (6924 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:17d0d3dd1f949640b03303b80a650627955b363a2f9d06d9f4380ca3fc45903c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.6 MB (33637804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d8b2934575515d0bb55b5c063d6c24cd529eee32e94c81894b2b659b3b3fca`
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
ADD file:7e9e4d557a66a31de2a39930803dbe849ba710af36b4731e9cbc856f55c10018 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:eeaefd3c974dfe1d5e1b8eb1929496ae7befe434399b37e601701f6d012e3169`  
		Last Modified: Sun, 26 Jan 2025 07:02:14 GMT  
		Size: 26.6 MB (26639267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03a59df32a3c278c1a8e1b5a42ec5159ca064a182a7ceee73e4ebe1d86afa12`  
		Last Modified: Tue, 04 Feb 2025 10:44:17 GMT  
		Size: 7.0 MB (6998537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1081500fc1be6fc3b8945ee99cb880cad574141933dbf2029a9a700a348a715e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3057147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0464e0de96691547f00ea8cde65d4ce20b5600e2c75c0e12c4aa3273df345a`

```dockerfile
```

-	Layers:
	-	`sha256:be68de876ccd100fac7c846b873154fb9e5fd89aba869bb04540f87213adae7a`  
		Last Modified: Tue, 04 Feb 2025 10:44:16 GMT  
		Size: 3.1 MB (3050163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7e8cd613a05f23ccfbaa6b9282044f16d5b355c4674cb7f486f198d68be570c`  
		Last Modified: Tue, 04 Feb 2025 10:44:16 GMT  
		Size: 7.0 KB (6984 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0fe6929d44d620ffe7cd75fe5b40025de76aa74aa07685bf792230e7c91825c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34398721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d89d6c25abf119ba22786832d5f3a2a743d77c84a724cc975596b4ee8e86ba5`
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
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9c1e987316bb6701bafa74dadea41ea57299699f23daacaaeafa9fa05f6213`  
		Last Modified: Tue, 04 Feb 2025 09:02:41 GMT  
		Size: 7.0 MB (7040539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6fb6b46dca2ea64642d5dcd614a9ad3a335f6afc07964764d2a870482af7eed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3055127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9206dba5abd986116aadf3f44aa556ed7bc3c28b9fd8f2d751d5c5f8a078f029`

```dockerfile
```

-	Layers:
	-	`sha256:ea672570cd596ebccfbaf31f47d9266431bce6f9967097954cd1659360dbbf13`  
		Last Modified: Tue, 04 Feb 2025 09:02:41 GMT  
		Size: 3.0 MB (3048123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f612b7908009283b8c09df71f46498e69fb65338aa1acc7f8c26ba67098b173`  
		Last Modified: Tue, 04 Feb 2025 09:02:40 GMT  
		Size: 7.0 KB (7004 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f7a5a90bfae168264eeeb709cce4697ea63a9377abf6d16ba2581602a0a3c7cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42645600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3e4f50615188f5197de6d78f780e501719398fd833977679cfab950529acda`
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
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c3f11d98bfde7b2d484e86a27f312061b41c7e65028517cbad025bac990450`  
		Last Modified: Tue, 04 Feb 2025 07:27:33 GMT  
		Size: 8.2 MB (8197665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2c993ec04244791550b10adfbecaea533a100b4a380b704979de7ff258cc1e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3059308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c97eb7eeafb4c53e7972f390b01a7f523dc725404a2c9c5a95550c96ae12df91`

```dockerfile
```

-	Layers:
	-	`sha256:bba32565c3d514031e655b03a2f0a4c12b8bfea0bbc31f2aa1804ed1367d0233`  
		Last Modified: Tue, 04 Feb 2025 07:27:33 GMT  
		Size: 3.1 MB (3052352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c60f22569bd53f1851706f6784c9cdbf7c58dfa5d23a1de9e2c390c8a6e9e3fc`  
		Last Modified: Tue, 04 Feb 2025 07:27:32 GMT  
		Size: 7.0 KB (6956 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a6dd850306c6cc369b57522a19b04cc9df354d0667fea9d4aeb82ee101c0acd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34147067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67d75862f0c15955d1d425f409ce31bc3a9f4d1686620b242a3a4f82b9394cb2`
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
ADD file:c95ac39f820c01b1c0a2d18f3df09346a389f9989c91cb636f75de0e3d63c97d in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cfa2d73aa16649863373431bec34ae49863b8b03f19e2c1fa29af96b0ea254fc`  
		Last Modified: Sun, 26 Jan 2025 07:02:26 GMT  
		Size: 27.0 MB (27039007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247fcfe5b002f706b4c9b3a78341f202606a547ef405c7ad03e2e33f28fec027`  
		Last Modified: Tue, 04 Feb 2025 04:44:46 GMT  
		Size: 7.1 MB (7108060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:27bb19291d910241f49185bcc23ffdaa47f0cd3d8f6c1505d83c09a976b89813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3048884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9996e59dbe46469cbc1c0a9d12f8aa9e22e0eb47b6843d06576af759fb73ff59`

```dockerfile
```

-	Layers:
	-	`sha256:c0ab06483d85f040af1b5f357790820b1c4fc53e83d9f16c38e4bd4c710968dd`  
		Last Modified: Tue, 04 Feb 2025 04:44:45 GMT  
		Size: 3.0 MB (3041928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dea9caad6953ba858e383ba65ee141384c7eb1dbce3cd7fca008ea276ee7f644`  
		Last Modified: Tue, 04 Feb 2025 04:44:44 GMT  
		Size: 7.0 KB (6956 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c9240024d17797d3670c26e10209501dbdd01d047b288925c278736a64dd4143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (35008772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f00d83c6eebb1eba2dfe93dc896eab9f7af7d70e04e338b245c8cd3d27da9064`
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
ADD file:39a6583c8b71c00e0ea7562cadb2b343caf5c0c274178520c7476e53faed2e3e in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7ed94a91c4e77c2e320a028b45fcefc9419c4df2b3d6494bf92ab5d08bba4d77`  
		Last Modified: Sun, 26 Jan 2025 07:02:32 GMT  
		Size: 28.0 MB (28000931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e0e0eba9503675f1ef20409d7abb0dc538cffb5361ed38070285248d79ca72`  
		Last Modified: Tue, 04 Feb 2025 07:33:18 GMT  
		Size: 7.0 MB (7007841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:63ecb7ddf4472817977f6f2e8d7b9bc4b5b27b626e08d6093db38777b2223e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3056996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffcef3547b091a358212056be9c262d679e046d201a57c9f65f99ff5f687aae1`

```dockerfile
```

-	Layers:
	-	`sha256:e61b6f4a167e6db0669458a35acb4bb49bc224dd1587bf3faba988821f883cd7`  
		Last Modified: Tue, 04 Feb 2025 07:33:17 GMT  
		Size: 3.1 MB (3050073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:638f272136230740d6cb3a0f0b077fc9dd7467a6d19821f0b719f79c0377c955`  
		Last Modified: Tue, 04 Feb 2025 07:33:17 GMT  
		Size: 6.9 KB (6923 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:jammy-scm`

```console
$ docker pull buildpack-deps@sha256:023a100c019c6b7c4549fab14b6a91cd2e61ca09575ce75fbf6fc251a6be7cc5
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
$ docker pull buildpack-deps@sha256:91718149b4f53576557b3a5645fcb54ed8cfe681b6c1f734380f470ec388f8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76119776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0645d0ba933cbe9b814b1dfb1bd138139346974f8753b21f2b8e3bc651919ba4`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee445cc5e2b6b7936777d1af58476890507382191edc76cf636f7e69381a0f7`  
		Last Modified: Tue, 04 Feb 2025 04:37:54 GMT  
		Size: 7.1 MB (7095774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c481194f5cf954d821c9180450bf9cbfe7d778d31dd54b13e0f37be46d837e`  
		Last Modified: Tue, 04 Feb 2025 05:20:43 GMT  
		Size: 39.5 MB (39488061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:913d6f77f627a5bf919be07bda166a50763665912c67c95de1a7a0c2eddf56fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837e383278b13cc069dd1f374210c432d5da73fd03f906048d2a1c86bafd3ed4`

```dockerfile
```

-	Layers:
	-	`sha256:a4523ac5f5958d30b606668facc78038341dc66d269f673e094bed9cc3df3951`  
		Last Modified: Tue, 04 Feb 2025 05:20:42 GMT  
		Size: 5.6 MB (5599765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c7a1e41537563d3da2abde7ffa18474777946269f533ae09dd1ebddfecd36f3`  
		Last Modified: Tue, 04 Feb 2025 05:20:42 GMT  
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
$ docker pull buildpack-deps@sha256:057096cc3c93f1f8fb66031507a66e3964e19ebf13ba1506c10185bcd3d680df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76454330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d30085e843b181c9d6f4f2db62a64f5abc2075b8becfb389d85b5c26010172`
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
ADD file:c95ac39f820c01b1c0a2d18f3df09346a389f9989c91cb636f75de0e3d63c97d in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cfa2d73aa16649863373431bec34ae49863b8b03f19e2c1fa29af96b0ea254fc`  
		Last Modified: Sun, 26 Jan 2025 07:02:26 GMT  
		Size: 27.0 MB (27039007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247fcfe5b002f706b4c9b3a78341f202606a547ef405c7ad03e2e33f28fec027`  
		Last Modified: Tue, 04 Feb 2025 04:44:46 GMT  
		Size: 7.1 MB (7108060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb811904a9072aa1e8962df9982276480172376fb423cfcf8aaec3ebb4f9f8ca`  
		Last Modified: Tue, 04 Feb 2025 08:14:03 GMT  
		Size: 42.3 MB (42307263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:db7959de9f0bbc7f117458f02e843839a036cecd8be06014481d54e3e65988d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5597655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576c72a4fdb601de9b844fe21519fdf8a6175dedd057cee5a5aedb19f9ca8df2`

```dockerfile
```

-	Layers:
	-	`sha256:0f25233e0d3c13d7ff6ec6d10bf9d28c99eade027cb6b2c16f932fb3d4593f81`  
		Last Modified: Tue, 04 Feb 2025 08:13:58 GMT  
		Size: 5.6 MB (5590299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bba3b78cb50e20ecbdff1ccf6fa4223854971f17408346d0efc034f2c824f27`  
		Last Modified: Tue, 04 Feb 2025 08:13:56 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6102c2a37e0c3ad300dff3483bdad8123d61076b7a324ba074b7c9b0b65d3ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74429734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e92079504e248aa3e1839d4474b3d926c07679ced29323feb51c42b3841b82`
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
ADD file:39a6583c8b71c00e0ea7562cadb2b343caf5c0c274178520c7476e53faed2e3e in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7ed94a91c4e77c2e320a028b45fcefc9419c4df2b3d6494bf92ab5d08bba4d77`  
		Last Modified: Sun, 26 Jan 2025 07:02:32 GMT  
		Size: 28.0 MB (28000931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e0e0eba9503675f1ef20409d7abb0dc538cffb5361ed38070285248d79ca72`  
		Last Modified: Tue, 04 Feb 2025 07:33:18 GMT  
		Size: 7.0 MB (7007841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ceb4257b5f6dbcfe0b6e240c36bcdefe3066bed00810364bb9111fc2b142678`  
		Last Modified: Tue, 04 Feb 2025 11:41:04 GMT  
		Size: 39.4 MB (39420962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:150da59697f1fda4ccd2b151d902b5463a708a5b5b4f918b4cacbda4ab3ea8e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8acfd7255776abc5b50d08c625a299c1efb593b61475984c2f4253c647aefdd`

```dockerfile
```

-	Layers:
	-	`sha256:3b20d61e305f63b842292fddab5a24a44dd99d12e07539a87853a780cdc97c4c`  
		Last Modified: Tue, 04 Feb 2025 11:41:02 GMT  
		Size: 5.6 MB (5600684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f48cc83a24245e928a33854befaeb67bfc51d8a7139f4f7d39f930180822cfd`  
		Last Modified: Tue, 04 Feb 2025 11:41:02 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:latest`

```console
$ docker pull buildpack-deps@sha256:d0377c0c511f692ccbcad47f8a26ebbe316394a989429bc4ff2736d05df4d53f
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
$ docker pull buildpack-deps@sha256:e7c6d07cb9b481de9609912bbb49dde977f6989d9a5abd1e58a877d25ee62baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.3 MB (348260383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28b23ee01d152ebfcf4c1687e2584877089ca3ab4550256ebe7e14df2e8a231`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 01:36:22 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b550be6cb62359a0f3a96bc0dc289f8b45d097eaad275887f163c6780b4108`  
		Last Modified: Tue, 04 Feb 2025 04:37:13 GMT  
		Size: 24.1 MB (24058355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35af2a7690f2b43e7237d1fae8e3f2350dfb25f3249e9cf65121866f9c56c772`  
		Last Modified: Tue, 04 Feb 2025 05:19:13 GMT  
		Size: 64.4 MB (64394292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7576b00d9bb10cc967bb5bdeeb3d5fa078ac8800e112aa03ed15ec199662d4f7`  
		Last Modified: Tue, 04 Feb 2025 06:14:28 GMT  
		Size: 211.3 MB (211328049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c4a3dacd4e6c66cf75566584dfa9afd045080a4f3cb7838d7b19bdf30386bd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15482039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9745f0d897e65d430c556d16a3c325def078d21a52bbb041e100967e95bcb9`

```dockerfile
```

-	Layers:
	-	`sha256:d4539b9f2e09894ecde147e82b09f847fc1cb06d936b130a9294f2544a903dd5`  
		Last Modified: Tue, 04 Feb 2025 06:14:25 GMT  
		Size: 15.5 MB (15471499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac139212500e131144b63fc9539d38787370de7cc310e05d7c357c0311687a7b`  
		Last Modified: Tue, 04 Feb 2025 06:14:24 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:a83883a22760febadd59a5f9dbcee3274ad8e29a3721729caff1d538b14169aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.4 MB (315359212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94bd2fc9911efe73bc7196ef0b6034a2b83caa039a8fb7b62851437cb9f1123c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8816181beac5d7674f87060fb5deb0c2c6221a62562265e16f54a617961cbc53`  
		Last Modified: Tue, 04 Feb 2025 01:38:08 GMT  
		Size: 46.0 MB (46006574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28060e71ea1173228ae8eefd6f5fb4296e8c1c73672a593f2d0d8e6e5483072`  
		Last Modified: Tue, 04 Feb 2025 08:03:04 GMT  
		Size: 22.7 MB (22733102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f77895e90931fefcb9b0f936aeec6e8c95f160c764c504ceb6084ffc29b46c`  
		Last Modified: Tue, 04 Feb 2025 10:20:41 GMT  
		Size: 62.0 MB (62003807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1293092f82d991d58072eac031a86360954b6f4021cae9377a435006dbe3bc7`  
		Last Modified: Tue, 04 Feb 2025 11:42:01 GMT  
		Size: 184.6 MB (184615729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dbf7f817719a28df7a5b0171007394ed210843d7eedd3e5f60dab9c54ea16a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15281025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4329461743dc38347b3338b873032c837143ab544d4d8b0cb96a7c18daec6f`

```dockerfile
```

-	Layers:
	-	`sha256:e768728e70f32ce146520e69c30ec9ced53352e7567637f487df05ce3d7d7129`  
		Last Modified: Tue, 04 Feb 2025 11:41:57 GMT  
		Size: 15.3 MB (15270417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9491464fec5e26fdf277d68ee891162483ab440c7fd77e5e08cfb03348e7798f`  
		Last Modified: Tue, 04 Feb 2025 11:41:57 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8a4104d2a65b6d8e78e51a418866c930b56abf606da4fc0d4cecfddc42f4fb27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.1 MB (301064875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36eea9faf1fdc9eefd8d490a1327060dcd31e80229cbcf72c8fbdfac33162515`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 01:34:58 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787291d61ca82895d27d086bfaf14ce01f401dfbf42f462addc8d1cae464ebab`  
		Last Modified: Tue, 14 Jan 2025 08:58:07 GMT  
		Size: 22.0 MB (21960077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6667f6e75dc8bed2e36123666ac457a4e0228141514ab32e65b9c6f6c7960e3`  
		Last Modified: Tue, 14 Jan 2025 16:15:27 GMT  
		Size: 59.6 MB (59640375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4144d45660bbc672e908993d8838af3ec9cece3a56e658f25257a0ce09e20da`  
		Last Modified: Tue, 14 Jan 2025 21:54:34 GMT  
		Size: 175.3 MB (175280214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8dacc3fe87894c577fce996d588fe02c9310c8d81e60e546f643b8bc38d24a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15286445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928b1fb5074c6e11dcf3aa6aa9b892b9e4899a9642c9a64608c3c2b3c292bc35`

```dockerfile
```

-	Layers:
	-	`sha256:ac1c5fb32c5d00a68aaed8067c4a6d22e1f011861220b7ec007edfc4b12d7d51`  
		Last Modified: Tue, 14 Jan 2025 21:54:30 GMT  
		Size: 15.3 MB (15275837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:566b21fe4e655c7bf8464e3b325fcd43af0615ec261408dd779beb45ecd60308`  
		Last Modified: Tue, 14 Jan 2025 21:54:29 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b407977518dbe09e422e0f4fd8f8a9f1343227cd6b752a8748d68f690f6f9603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.0 MB (338978548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c89001a18c0a49ab405cbc818fc07891ef0b4a0e257208d905d299593218681`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b85d68f8a4dce392d372c8a196863eac6d111c36b714179b4ab30e00c00d1`  
		Last Modified: Tue, 14 Jan 2025 06:59:53 GMT  
		Size: 23.6 MB (23598225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936252136b926e9bca27f4a5442f6a5d10c0ea4a23ca8b30c65de1bde666d082`  
		Last Modified: Tue, 14 Jan 2025 13:31:06 GMT  
		Size: 64.4 MB (64356433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c5996c7a64a4f64139ff9df6a590216c8143f5bb1f4c0f41874cf5336645c0`  
		Last Modified: Tue, 14 Jan 2025 17:08:21 GMT  
		Size: 202.7 MB (202716994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d476ca8de345ec5844dc135bc6aa7a9ecb1340f8030bf64ad8a895eaf60ccff1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15510590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2784f3887d0a4b7392bfac8b68c3113a8ca00a1b74b490ca7b5e68fdbbafc50`

```dockerfile
```

-	Layers:
	-	`sha256:63f64955d6e1f03115feb763d448c8fcf074438056bbbfb5f955c3c0d1a4aab7`  
		Last Modified: Tue, 14 Jan 2025 17:08:17 GMT  
		Size: 15.5 MB (15499958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13ac6ce4737d9a952ca57fff0a7a7477bd10b8dc774b705c47fd2768a5a0a036`  
		Last Modified: Tue, 14 Jan 2025 17:08:16 GMT  
		Size: 10.6 KB (10632 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; 386

```console
$ docker pull buildpack-deps@sha256:882a152f2e57fff2b4e424ea3fb6a7d5273b93066678dfd0bdb95b0efba857c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.8 MB (350837945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9097785ed06e1ce4239bd8a49450234addc5a2f2cae02b789c3f0c6688239e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d6abb78404200438eb560450e089a4e7707a23d5ec913df260500d902666670a`  
		Last Modified: Tue, 04 Feb 2025 01:36:35 GMT  
		Size: 49.5 MB (49457456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7d7e5b6420845d0479145c8a18a31030093be0de73e11194d97fee1ac58ef5`  
		Last Modified: Tue, 04 Feb 2025 04:23:48 GMT  
		Size: 24.9 MB (24899338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43394bbbaab482132a05c8eb702c9ebbbf5ecccd558ce05fdf40c651b7fbfa10`  
		Last Modified: Tue, 04 Feb 2025 05:15:47 GMT  
		Size: 66.2 MB (66236925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a443d7b60dbf868d9542c672117d7e30786e753c999878424f61b36b47cb37e5`  
		Last Modified: Tue, 04 Feb 2025 06:14:56 GMT  
		Size: 210.2 MB (210244226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e54a789932b9f341ad41a0f58003c64ea627a572cfb7c893198b963e0f60b687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15460601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb037878e3a2b9b326d57a9255d1516b726264d93cdf05e3e5072ecf804fcb2`

```dockerfile
```

-	Layers:
	-	`sha256:65c94f4e47cb5c1d276ce88454d05b51a88e1f8b6e58588a30fcf1e870c57f76`  
		Last Modified: Tue, 04 Feb 2025 06:14:51 GMT  
		Size: 15.5 MB (15450089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a66dedb1b7b06480192ffed582731683a156dc109dbe02f773f96c60f11a9a78`  
		Last Modified: Tue, 04 Feb 2025 06:14:50 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:860a2755ec0568a4dbe46314a2ae387e90fc9b53a78c8889c779740d34c4d802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.6 MB (325612422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5fc62c757f45c6730d1d46ad5a4473bea7a37b382fd92a8928e79be83348e25`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:12e528bcd428b4b8475a045cfdce724675384eedf195bad13ce8015853db632c`  
		Last Modified: Tue, 14 Jan 2025 01:34:57 GMT  
		Size: 48.8 MB (48758103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dede5b838e92cbab015cc8e31645fbe220ba02a56693e3a7a144e0a5428690`  
		Last Modified: Tue, 14 Jan 2025 18:10:17 GMT  
		Size: 23.7 MB (23652164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be7513211e793708951d273ea21ae802b4bdb4109f4b12ca6122e317851db90`  
		Last Modified: Wed, 15 Jan 2025 02:00:51 GMT  
		Size: 63.3 MB (63296729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac18012fc3c757a7df4cc601b819ea75556dd5814ec840b12642602c54fe799`  
		Last Modified: Wed, 15 Jan 2025 17:56:32 GMT  
		Size: 189.9 MB (189905426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:66e4f671ba1b7ad4b6b317db70aa590923f42d88d1b145d7b89d506f0e9400a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54cc4402e6b3fab15abe9933de571318dc91188f9d8875898b7d714a8855c230`

```dockerfile
```

-	Layers:
	-	`sha256:c1eb17e50044ba359ef545be178a5605253131cd4cc227f70c88c9d2f1b519d8`  
		Last Modified: Wed, 15 Jan 2025 17:56:14 GMT  
		Size: 10.4 KB (10382 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4725d4b50cc3768c2f7586e853992b6f03926dce68a3456661da6f08b1708622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.2 MB (362239370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c43ee817227a27216e0e75060a8916507939c6d366bfed2662922b4b750de8a8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:60b6379697eb1bdc0a74d6aa762f7f8e36a4a46031b019e2c7651c9723194c8b`  
		Last Modified: Tue, 14 Jan 2025 01:36:59 GMT  
		Size: 52.3 MB (52313137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b1d1b75ad07ec92cebf5f30e6612d80907cb5a7323fdef7921893e816a53be`  
		Last Modified: Tue, 14 Jan 2025 05:30:15 GMT  
		Size: 25.7 MB (25717439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395bc8910e96064c02227d340de0ac8d0234f64dd58802df0e9bd0891ad39050`  
		Last Modified: Tue, 14 Jan 2025 09:41:58 GMT  
		Size: 69.8 MB (69844490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb75d2bb90f133e31006cdf083f7a1330b114cb8a3fd0025be19bce4d4ee89b`  
		Last Modified: Tue, 14 Jan 2025 13:00:17 GMT  
		Size: 214.4 MB (214364304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:91b60ba7af97ff988d44396cd69ffddfaa27f52f86ba804fcb0094052e59b774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15458402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7756e08eb53066769aa73f8cb07a547ba51e203c0032cd5932fc75d44e7a1f1`

```dockerfile
```

-	Layers:
	-	`sha256:fcc9fa1d49ed25f5c3c5a80a6668f2ea892ecb027237cec560258091a270b425`  
		Last Modified: Tue, 14 Jan 2025 13:00:11 GMT  
		Size: 15.4 MB (15447824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfa234786e191f6aea3b5a8c4236319884b3c104e4aa16502da685b5eb83170b`  
		Last Modified: Tue, 14 Jan 2025 13:00:10 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:latest` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:76f9eb07fd39ec3202f7a15b37d5429dd3b1edbfe4c32a914320944ae5cb8bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.0 MB (318046600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3034f78e5badb663e2f50b27003c6f5999b3bfb09a5a46525d9ba997700d930b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:21aa15808dc85b52fca40d40118565ddcd1b7ca60220d34328c38ccbc43c6ec1`  
		Last Modified: Tue, 14 Jan 2025 01:34:07 GMT  
		Size: 47.1 MB (47131782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba976031c967b4215afb8ec45dd7db082bb0d532971c83a1e9acaaa24c91981`  
		Last Modified: Tue, 14 Jan 2025 04:59:37 GMT  
		Size: 24.1 MB (24057754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41403619947915f481f99b2b28eecf7aa168ff32ff64e044d73a504ac7472026`  
		Last Modified: Tue, 14 Jan 2025 09:09:48 GMT  
		Size: 63.5 MB (63498283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a63cbd668c99b32baa3a88a9298c02c22ab49ca16b889143b19cca1ed34c77`  
		Last Modified: Tue, 14 Jan 2025 11:15:21 GMT  
		Size: 183.4 MB (183358781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:latest` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2bf1e3ba440aebd60ca46d51930af97653389a33635121e8f5bd73830a43f75d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15294675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14bf32054c104be3d3381618b5c360e0db2d6b2c7490f0488d421a0cf7d7533`

```dockerfile
```

-	Layers:
	-	`sha256:04571792130603857f093b41ea98376a26344db408bc745b4c87eefd65975728`  
		Last Modified: Tue, 14 Jan 2025 11:15:19 GMT  
		Size: 15.3 MB (15284135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c70a1a5bc411f177e1b25fd6a73313087cf5dae458f60beb639d7f5a37e27e22`  
		Last Modified: Tue, 14 Jan 2025 11:15:18 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:51c0b7c0a60b769cb9e77492f6e77e6092be26b21bade5f50eb4b44c10f60700
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
$ docker pull buildpack-deps@sha256:05f037723a8daa90787e6a1637211ec41ce3b0bca77ca6596fb29ca637908007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278607273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ef6cacbdf5590762e0385cd5204d975695279bbc6f6faed361216b0278db670`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bca5f89848ce8fced9fabc99051bd86546e9b21ec911faa12d1b57517b419d`  
		Last Modified: Tue, 04 Feb 2025 04:37:54 GMT  
		Size: 13.6 MB (13612233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c239591c8fa2f14b9d884080d6e6888af267d5581800cd9aca9df2581c579ded`  
		Last Modified: Tue, 04 Feb 2025 05:20:45 GMT  
		Size: 47.7 MB (47706161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4002a449dfbeebc197aa37c9540569c67552048e4ea6f3e29d4680d8877810fd`  
		Last Modified: Tue, 04 Feb 2025 06:14:15 GMT  
		Size: 187.5 MB (187534589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ea56b9ef0ade587ac7c02b1d7068c32d6912c34bb3d22b99d146ece0c29e3819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11357581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91971766cecd1a460eb600747d6a6ecea74bedbcc256fa7547a9559067f3d6d6`

```dockerfile
```

-	Layers:
	-	`sha256:979f5fc4fdb0e002a48d35db1f28d78516b135296692a750da8f1a69c430293b`  
		Last Modified: Tue, 04 Feb 2025 06:14:12 GMT  
		Size: 11.3 MB (11347397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edc3bec74ae7fe6478fd68bdace1f3df91ce527a4f98599bc376e52bbeb84cab`  
		Last Modified: Tue, 04 Feb 2025 06:14:12 GMT  
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
$ docker pull buildpack-deps@sha256:d31f5bdb9913880c43a5a00471c71bf67e54951ad0562d4ecfd3df1a803ebbda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.2 MB (333185891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3cb0ade06c43af8ab75177b46cd822d33e79229563b4910a508c8b1c3ad48f7`
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
ADD file:69c46ae9666e78c27ca5b5f25cec1a5536ff16f17cb00104e5c77e722bd8d643 in / 
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
	-	`sha256:6e1053d729cc1718daa9369927cf6ddfbf892a846041de0e610d1c77ade136c5`  
		Last Modified: Mon, 27 Jan 2025 05:10:15 GMT  
		Size: 31.0 MB (30983910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1ff2b444c4e8d1278840900c3e27c00e5987f3c54a529299dbf9a2ed443657`  
		Last Modified: Tue, 04 Feb 2025 04:47:44 GMT  
		Size: 14.3 MB (14317230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec5a422d511e6bec6d017fced317ebf97a5f77ec1f6eff36a777fc69635d1c3`  
		Last Modified: Tue, 04 Feb 2025 08:19:44 GMT  
		Size: 56.2 MB (56219937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25582887dbbebf13b474bcce046935f9057ec77b7d60eb19fafce7fdcf42f073`  
		Last Modified: Tue, 04 Feb 2025 10:24:52 GMT  
		Size: 231.7 MB (231664814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e54aa815e93779c56670198616f3acdade74b3796475166f25881215682c4187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10870736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5808c0276f6f621d004fff61facb2f629fbaf4021749d5cb1299d184f771cc65`

```dockerfile
```

-	Layers:
	-	`sha256:40943108eb855797811a4ec15d39627861040402ea56a026d39ea8de5439224c`  
		Last Modified: Tue, 04 Feb 2025 10:24:22 GMT  
		Size: 10.9 MB (10860520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0dbedfe5b565ffed2c797524ab8f0e8765c8c9e9475f416aeb3a57a9df3cdc9`  
		Last Modified: Tue, 04 Feb 2025 10:24:20 GMT  
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
$ docker pull buildpack-deps@sha256:0591c4ff26a20c9bd55f2531bc515396f6d356830bbe9e1136205dcabcf857cf
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
$ docker pull buildpack-deps@sha256:644a9f032cf50b2a91f1c4e7312425a77195879e7178d6a6076c084e9d7457cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43366523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d93add3ca2246e80a01713194ef3cc70909c3ccce2b0fc64adb66e63e0d3fce`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bca5f89848ce8fced9fabc99051bd86546e9b21ec911faa12d1b57517b419d`  
		Last Modified: Tue, 04 Feb 2025 04:37:54 GMT  
		Size: 13.6 MB (13612233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a4e685fd1a1fdc8c51f92015aa36ade4193a409acedff0d9fc53f6f0e5e2a403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2469041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312348ef20d91871237e8ce4d0b2263ae4f719aac1e1106d85629a329e842c8f`

```dockerfile
```

-	Layers:
	-	`sha256:2a3a10bb9dcd0dd89b1e24f079336b7b12e0e0ce7d66b51b53ebd2caf71bdebb`  
		Last Modified: Tue, 04 Feb 2025 04:37:54 GMT  
		Size: 2.5 MB (2462082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:876478e0a9dd99b90b311614b8a249982e408c423a64c5b1cd1f707df848452c`  
		Last Modified: Tue, 04 Feb 2025 04:37:53 GMT  
		Size: 7.0 KB (6959 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5ae44b9cc101087fa183a9f8269d6d8f0d1c86230044d58ec0015e1fa706e1d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39645632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19c0792edbcf8119e6ef8d42938209118401d44f50d9674972ff99beec67a6aa`
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
ADD file:22301ffa2fa465db7a0f07e0c3ddc488f07cc6a745c39e6f450fdbe37da97418 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3492abb11babfb77cfc5a8904e67b22f4e4fd68c8d8a7fe1119861ed6503b36f`  
		Last Modified: Mon, 27 Jan 2025 05:10:02 GMT  
		Size: 26.9 MB (26874983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d26a8223ab81b7619d0fa204eaa4a52bd9e82a52dc44e8e3fd181d828b57c69`  
		Last Modified: Tue, 04 Feb 2025 10:45:28 GMT  
		Size: 12.8 MB (12770649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:88d98aa301ddf4ba195ae435b272e8dbc57ada124bc050d9584e020a2d0ed4cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2471405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f632e6a7a1f74c013a8732986b2644111dec9298d7588b4e37b61e3e5f87211`

```dockerfile
```

-	Layers:
	-	`sha256:e39ed50c31a6f47c59f9ff236393152bf088df00a815272e7d5f17eb16b93ed5`  
		Last Modified: Tue, 04 Feb 2025 10:45:28 GMT  
		Size: 2.5 MB (2464386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0299afeb76c3ef583558026c326712b4428d9f8d2f847835de29e219d670197a`  
		Last Modified: Tue, 04 Feb 2025 10:45:27 GMT  
		Size: 7.0 KB (7019 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f81e78c5e8cd92e7c0dd2c53f678e502b5539f88f7bbd62dcf110e487cdbd9a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42341516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a53f3d5ba81a42da827fd1d0fb748b572c23998d6ef79331d126adf57704c8da`
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
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e873299a39c8bb8cb3b5d978575339de6ade976cca414b5727de8d362ef599f2`  
		Last Modified: Tue, 04 Feb 2025 09:03:21 GMT  
		Size: 13.4 MB (13447918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a09851342c2a390434b8403c6567a044084514acfe1c895374c0d61cfd2021b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2470179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4fa8fa439cb9f6ef86fbfe6287983813d43ba022d392271dd37d7a11f8049b`

```dockerfile
```

-	Layers:
	-	`sha256:c45cb91762aa9ce3109b687f2eb31f4ee68d9a8723cfb10b81ba0e79e052a3be`  
		Last Modified: Tue, 04 Feb 2025 09:03:20 GMT  
		Size: 2.5 MB (2463140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be9ae4d5b446fb6dfc3bd1fa724ccedac7ac8e17b189771cdb3a350e25c59adf`  
		Last Modified: Tue, 04 Feb 2025 09:03:20 GMT  
		Size: 7.0 KB (7039 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b8a5136a89a7e6d03e7dd3aeffd99e0e9c7c281cc4d587c6c13bb18c89933e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50348767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec08d7af4854f7616cd6c24d855e9825f8d7b0a7cc3b33d388bb26bbbf087fd0`
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
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb3acc4132c7aebe44f31c42e40cc094c5403d3a66fea37f2373bf78812b25b`  
		Last Modified: Tue, 04 Feb 2025 07:28:52 GMT  
		Size: 16.0 MB (15958943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7780e111e7985c50976ae1a4c5c08bfb9c544701dadd2e2c140f1962ca104727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2473560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6409635aa1c47b491672f8162339c57a539d38011229da817788051e22787bd`

```dockerfile
```

-	Layers:
	-	`sha256:b5e2dfedfa809e8174ffef851627e9bf5e80f70465fbda8b396404490e83284b`  
		Last Modified: Tue, 04 Feb 2025 07:28:51 GMT  
		Size: 2.5 MB (2466569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a0559ba321ef6c4284cc87f3b5369d46603219db294ec6bf7e0a32e77f5486a`  
		Last Modified: Tue, 04 Feb 2025 07:28:51 GMT  
		Size: 7.0 KB (6991 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:31ce75f451962f5cb800331842c9a621e15380dc7a0d5e76cc27f614fb0789d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45301140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054c4b3eb9ab81c609b9e82f2d951c6cc3a86dd499d31378a9ed2556f5980ffe`
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
ADD file:69c46ae9666e78c27ca5b5f25cec1a5536ff16f17cb00104e5c77e722bd8d643 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6e1053d729cc1718daa9369927cf6ddfbf892a846041de0e610d1c77ade136c5`  
		Last Modified: Mon, 27 Jan 2025 05:10:15 GMT  
		Size: 31.0 MB (30983910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1ff2b444c4e8d1278840900c3e27c00e5987f3c54a529299dbf9a2ed443657`  
		Last Modified: Tue, 04 Feb 2025 04:47:44 GMT  
		Size: 14.3 MB (14317230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1a87e48a82b50c374c47c2c34dcd6c3fa330f2d9871e29fa616af48a4edc3cdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d637e0f6a904b9c985a5da321c9640e3c0f45e9288c8c31a84d6fe2281ce3cc`

```dockerfile
```

-	Layers:
	-	`sha256:1db32f151df67541b0541f324d7b140e38f2e4207414a4155bc3af99f47202e0`  
		Last Modified: Tue, 04 Feb 2025 04:47:42 GMT  
		Size: 2.5 MB (2456141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18f60c2b0b80254a366d8c7acb2cd5a488b2f72afe32467a2a687d6a7d8b17c4`  
		Last Modified: Tue, 04 Feb 2025 04:47:42 GMT  
		Size: 7.0 KB (6990 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:98518dff71ac71a87d5d35456508f00745860a4b1d5b936c9e65950ac33a07e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44964949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07262228767cdfdf011a42ed5559b01db0f589b6db2cacdf342b615fbe496383`
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
ADD file:1a65bb049384da7e51a2b1e9180f11d6ec22b1427da7ca5682814abd261ba57e in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8e1d25585ef2d346b71072d258a697a9d190e3c5754512c7cb978dbbe80911e6`  
		Last Modified: Mon, 27 Jan 2025 05:10:30 GMT  
		Size: 30.0 MB (30027563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cacc91036ba2e7e50d76ff2b2593ea149a0df971bb8069b913263b87ff517ac5`  
		Last Modified: Tue, 04 Feb 2025 07:34:27 GMT  
		Size: 14.9 MB (14937386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:89c4abc3a60eb48bcbd7a232595cc99c156532030ab21917410f175b25de736d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2471866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d0978b12b5385265529a2eb8e826ef6bed43e969869849f3968bd2061fbfb4`

```dockerfile
```

-	Layers:
	-	`sha256:1145ed6e6cc241993da9952d8c94810c5bdfc8691a649a7c93c330bbd18a2193`  
		Last Modified: Tue, 04 Feb 2025 07:34:26 GMT  
		Size: 2.5 MB (2464907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02a52d892c2d4165e68754e24393ef9f9addb502befc69210f9f58ff272ee843`  
		Last Modified: Tue, 04 Feb 2025 07:34:26 GMT  
		Size: 7.0 KB (6959 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:noble-scm`

```console
$ docker pull buildpack-deps@sha256:6b3862bee46bcb79eec81b1bcfb760dd71c534bf2c04991022ef0a14b843baa8
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
$ docker pull buildpack-deps@sha256:b79f7b47aed24f23f5486c1047e9a8c86c3941402091c178acc9f1ef1aaf6e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91072684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8bca72d95b85c99311d1c63dd2fd9ac0b4bee3b2ed93eb890c666eb04e8da7e`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bca5f89848ce8fced9fabc99051bd86546e9b21ec911faa12d1b57517b419d`  
		Last Modified: Tue, 04 Feb 2025 04:37:54 GMT  
		Size: 13.6 MB (13612233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c239591c8fa2f14b9d884080d6e6888af267d5581800cd9aca9df2581c579ded`  
		Last Modified: Tue, 04 Feb 2025 05:20:45 GMT  
		Size: 47.7 MB (47706161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:db5fdb66e6c16e33934375372f2765e3ae9ba4dd6bdabb2c088d421f30df9443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5081162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5227624d892aa0359b9c2a9210f2fe3f732bdf2819487b88202a10c76f5877f7`

```dockerfile
```

-	Layers:
	-	`sha256:9a022b0c23577f479164b46a47db9343c2b2b7c92c88c45d94c1b7a74ea7f1ea`  
		Last Modified: Tue, 04 Feb 2025 05:20:44 GMT  
		Size: 5.1 MB (5073857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:751a37c758d13b6de22a81dd98828f7660e054da7277039fc7fd8fed7a65aa67`  
		Last Modified: Tue, 04 Feb 2025 05:20:44 GMT  
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
$ docker pull buildpack-deps@sha256:ac57716a31f673328d41905ee068cbf3d1e07eb18922ce4bc381166457a0bcb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.5 MB (101521077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9355b669720be435491e9014a723aa6ca9b19f0e95d1305384a0097607d3c47`
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
ADD file:69c46ae9666e78c27ca5b5f25cec1a5536ff16f17cb00104e5c77e722bd8d643 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6e1053d729cc1718daa9369927cf6ddfbf892a846041de0e610d1c77ade136c5`  
		Last Modified: Mon, 27 Jan 2025 05:10:15 GMT  
		Size: 31.0 MB (30983910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1ff2b444c4e8d1278840900c3e27c00e5987f3c54a529299dbf9a2ed443657`  
		Last Modified: Tue, 04 Feb 2025 04:47:44 GMT  
		Size: 14.3 MB (14317230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec5a422d511e6bec6d017fced317ebf97a5f77ec1f6eff36a777fc69635d1c3`  
		Last Modified: Tue, 04 Feb 2025 08:19:44 GMT  
		Size: 56.2 MB (56219937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:13ed8342d52d164a346aa9b5cb66623fe05636c2934ea795ba1b9e598f5399cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5071718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89c54bf63e8b39c08bc48b092a6c6475acb1a690c25fa70405580bc272a43a9`

```dockerfile
```

-	Layers:
	-	`sha256:e76485709ee792b4459b34b590a90e627928fa8bd423b6e42b45b5f7ba2a63de`  
		Last Modified: Tue, 04 Feb 2025 08:19:36 GMT  
		Size: 5.1 MB (5064381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b25f7384c82f182e09fec7b22eaceec3f8a595bcd3522a657ed9ee9e8c29af4`  
		Last Modified: Tue, 04 Feb 2025 08:19:35 GMT  
		Size: 7.3 KB (7337 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:14f5b18a8d3325c0aceabebe8cd762bf3a65f728d72f7b061c7e9df305b9a0d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94420581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7cb2db7e6b493a23389546282950b17a58fe374836a93a6806036f3dae3468`
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
ADD file:1a65bb049384da7e51a2b1e9180f11d6ec22b1427da7ca5682814abd261ba57e in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8e1d25585ef2d346b71072d258a697a9d190e3c5754512c7cb978dbbe80911e6`  
		Last Modified: Mon, 27 Jan 2025 05:10:30 GMT  
		Size: 30.0 MB (30027563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cacc91036ba2e7e50d76ff2b2593ea149a0df971bb8069b913263b87ff517ac5`  
		Last Modified: Tue, 04 Feb 2025 07:34:27 GMT  
		Size: 14.9 MB (14937386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ae03e34cf459247f3c12fdf3d38cb8c622dd2d321ebd9a1ced772465e12c97`  
		Last Modified: Tue, 04 Feb 2025 11:43:56 GMT  
		Size: 49.5 MB (49455632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1525fcbfa02c33484bb09e040a04e9b78c06c3672bf65abf24411ee3e09a500c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5083494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5270daea82df40b76ac970b7fa7c5f3be156d08cf87ed6a6907edbe2a94055b`

```dockerfile
```

-	Layers:
	-	`sha256:c35fa74f8bb61c22c923b1e0ae52e265c1c6f23b8b4bd3db45b9054419060965`  
		Last Modified: Tue, 04 Feb 2025 11:43:55 GMT  
		Size: 5.1 MB (5076189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bb7c13a886117d13a191bcc5c275e7edeffb54e8f7d21e7471bee9c043578fb`  
		Last Modified: Tue, 04 Feb 2025 11:43:55 GMT  
		Size: 7.3 KB (7305 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:oldstable`

```console
$ docker pull buildpack-deps@sha256:d5b59dd4f8a672e49190a9ce5dcf7b972172402f7847f9ba403e6e6bdce3fce7
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
$ docker pull buildpack-deps@sha256:d2e93687f21da5853e92d5d2394b09c22c04252f3cf160684f835ca1a616f0be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.1 MB (321121810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246e22f571a0f5c491769a43d42a15a65de640fdb1075fdba4c2f3ca90722ebb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:478cb73646107d7b3f891aa53abaed926667463844c07b1d924bd760ae03f38a`  
		Last Modified: Tue, 04 Feb 2025 01:36:37 GMT  
		Size: 53.7 MB (53738873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0388f0d5bf1adc15e551cceee5a85f21b1ebf5b13c380ee0e941c5d55013598`  
		Last Modified: Tue, 04 Feb 2025 04:37:42 GMT  
		Size: 15.6 MB (15558271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d473f760e53d3d50afd1cebc7113387023a04ff8ec34073c4412b465ccc2fc5`  
		Last Modified: Tue, 04 Feb 2025 05:19:08 GMT  
		Size: 54.8 MB (54751917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d32181a1ed55cf7269c27a7a18858d7a4679d9fccbc616d5d878b6ddded25b`  
		Last Modified: Tue, 04 Feb 2025 06:14:22 GMT  
		Size: 197.1 MB (197072749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c20b6d0d8cf0bbb5a04f01ad8cd51019ec51de92a5f18c0de949f2e61d1189ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15081760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66acaa1540629854cd364629b821d7ce5c76de2a55eb5d7a1618e1d5ba5a3adf`

```dockerfile
```

-	Layers:
	-	`sha256:dc4a6b5f744e6d3c4ceaaae6439e7eef4457996ecf9f57bb36742af7b5636be1`  
		Last Modified: Tue, 04 Feb 2025 06:14:19 GMT  
		Size: 15.1 MB (15071528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73f76a037f50e1f86156c2121d6d9be40001cbdbec315dc9419f83848a2851e5`  
		Last Modified: Tue, 04 Feb 2025 06:14:19 GMT  
		Size: 10.2 KB (10232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e4d9a678765a1a4b36cb358955286fee41d3220580c5e1a5baac558d8916c560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.9 MB (281865027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a91082578b03acb86ea134738e540ea3f4dc35583a8c4c0ead0e3c632257ec80`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2d8b4e71b0057b288fa0b7cf9b1d15edc9bec9dc37df63d3463ce28e4f414dc9`  
		Last Modified: Tue, 14 Jan 2025 01:35:36 GMT  
		Size: 49.0 MB (49025062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7055bc7f040fce3e9b8f05fd7f56b8a568950e082ea8ea3aa96cf99f49523ca5`  
		Last Modified: Tue, 14 Jan 2025 08:58:39 GMT  
		Size: 14.7 MB (14673832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681398f28ce19a7af317e3774529df465ed1770ca10164fdba3b20f23a5d8026`  
		Last Modified: Tue, 14 Jan 2025 16:16:27 GMT  
		Size: 50.6 MB (50640646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526075af1d9c0b728ff0e8888d46f79edd8fb9bacc975b1eb824b9bca2c06ee2`  
		Last Modified: Tue, 14 Jan 2025 21:56:34 GMT  
		Size: 167.5 MB (167525487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8bf8fc0ea3d27fb38bf14664e4840df434a73985f82c716ca25a8d17dc10e1bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14882567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872ff66c39242f7fa5d2c10b491392327cc6c1b53521e020fa17d7d0e2850cf0`

```dockerfile
```

-	Layers:
	-	`sha256:e69e0689bd9054f8eca064739d1c8b693d08bec2ec5650f7353219866f3a0877`  
		Last Modified: Tue, 14 Jan 2025 21:56:31 GMT  
		Size: 14.9 MB (14872275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:067d8002d2b05e274736054645f782d61b1852b1436e0d26d6096257140c2ea5`  
		Last Modified: Tue, 14 Jan 2025 21:56:30 GMT  
		Size: 10.3 KB (10292 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:dbb29bd940d6ce2889e1c39cc81b6683adfb499d67e680dfcaed5fbba4f3f68e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.6 MB (312622972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88399fb643c94545384f7c5485ae56facab2b9a1a1565bb4af601f5685c9f8d6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dfd6b176342cb480b79cef9a7188364b0f5702ccc77422fcdb5d7d8f3f42c8`  
		Last Modified: Tue, 14 Jan 2025 07:00:18 GMT  
		Size: 15.5 MB (15544093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23ac0e9b25076f1cc90469f31bffaae783c6a3a88272620af5e7dcbe0b8202`  
		Last Modified: Tue, 14 Jan 2025 13:31:46 GMT  
		Size: 54.9 MB (54852602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5936a36467e76a2d54993295f16ff38dd2c24f30cf89a1f83a922f2440b869`  
		Last Modified: Tue, 14 Jan 2025 17:09:53 GMT  
		Size: 190.0 MB (189980217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ae8b0ba8fd091612a9687963576f73b13545fbb3ad9a144edb6a9a182046acc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15084056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f24494000d98572dbca61183102b7f0896f65ba2b83261b9f347e277f1d1197`

```dockerfile
```

-	Layers:
	-	`sha256:6947aa4dde02deb94734a78920905e8c7e6b9faffdf741577bf7bf716b79a153`  
		Last Modified: Tue, 14 Jan 2025 17:09:50 GMT  
		Size: 15.1 MB (15073744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:660f8ad159fda4b312cc890f08416761a6d93d6e239c511058aedc8a320496be`  
		Last Modified: Tue, 14 Jan 2025 17:09:48 GMT  
		Size: 10.3 KB (10312 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e1371f188b371bb212fdd0d81390dbf85709ab28ec7b27eee70183e5dd657633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.7 MB (326748309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5266d02805914d0cc09d2ed291fabb0999ab7f4bb986062d1bef17595301e921`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c2b5327eac1fcd49233dc8f6e5417e7e2efeea16edfcbff9dd025f389e15b11e`  
		Last Modified: Tue, 04 Feb 2025 01:36:38 GMT  
		Size: 54.7 MB (54675956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d372eab1872f98afed1da2c899af883a0b3a6e52e25e2690ed35b3d6f859e5`  
		Last Modified: Tue, 04 Feb 2025 04:23:38 GMT  
		Size: 16.1 MB (16062054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4520e7fd9b17628990db3e961c2d7570421849af1fe255937c0a9e48cf49a48f`  
		Last Modified: Tue, 04 Feb 2025 05:15:33 GMT  
		Size: 56.0 MB (56029876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b370f45f01968d6de3175fc994cf545ece88435b9abc17f2ed4705ac128c8d4`  
		Last Modified: Tue, 04 Feb 2025 06:14:51 GMT  
		Size: 200.0 MB (199980423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bd92c287cf99c6152f7f6cab08646996c38e4a491c76bcc3705ebc99d06f7992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15070078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea2facb97735295ed3258a51b2d9555ca11d49a07beaf4d8934198195fc6b2f`

```dockerfile
```

-	Layers:
	-	`sha256:d216381c85049dde4f65a8029d5e313e7f34e9bb9745a33902c596c23e197770`  
		Last Modified: Tue, 04 Feb 2025 06:14:45 GMT  
		Size: 15.1 MB (15059868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35f077caaeddfa1dda713b6d99bc1fadbcc6d2bd1f1ed6a4d3de3cb510bdade3`  
		Last Modified: Tue, 04 Feb 2025 06:14:44 GMT  
		Size: 10.2 KB (10210 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:845de4a60c3498098593185102842603fd86f171c9d51bcf4187a552ceb04f5d
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
$ docker pull buildpack-deps@sha256:7f278ea0e1aacd2ac3d797daf838446f76bb7fe002dabc269e3d32d27f939f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69297144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0422b90f4807ccd9614ef9118463e5e80990c61726943324bac5a3975fad401e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:478cb73646107d7b3f891aa53abaed926667463844c07b1d924bd760ae03f38a`  
		Last Modified: Tue, 04 Feb 2025 01:36:37 GMT  
		Size: 53.7 MB (53738873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0388f0d5bf1adc15e551cceee5a85f21b1ebf5b13c380ee0e941c5d55013598`  
		Last Modified: Tue, 04 Feb 2025 04:37:42 GMT  
		Size: 15.6 MB (15558271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2c10d26009d377cac6e65d06092dfb61fd1d729963f4514dca185a4cb86d039c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4492427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855812a9ac3b6ebaba4c3495c0e7c909ee453450b17678849e202a3eb77091b0`

```dockerfile
```

-	Layers:
	-	`sha256:1cd436b097ec741147c69b351e4e2e79a1af953b797934f02c828121818aa7d7`  
		Last Modified: Tue, 04 Feb 2025 04:37:42 GMT  
		Size: 4.5 MB (4485627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d1e31308f71b28230d96394763b0aa71c5225339cda77c606855758ef2d769e`  
		Last Modified: Tue, 04 Feb 2025 04:37:42 GMT  
		Size: 6.8 KB (6800 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d095285c12a1b99487b28af042f4ce855d09e71ccf4cfd805149f321614f1a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63698612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb55cfbf146794456e45adaf1201ab08eceffde02bbb25893d450fe648223cb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7dafa8b67e9b20318af5959237616a556f517d3359b4cec5bc2b6899a7c8336b`  
		Last Modified: Tue, 04 Feb 2025 01:37:44 GMT  
		Size: 49.0 MB (49024794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bfe1cf520a5741b594ed015a44e9386892026b5310b613c2207dbb1073919e7`  
		Last Modified: Tue, 04 Feb 2025 10:42:22 GMT  
		Size: 14.7 MB (14673818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7e0941255238d0b686ba4d057744cdb1334d8412c6bbe0222601c199a7825004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ea4476b8d9fb50bf3cb725815db433c4336d055be7f7d0270018b1fd893d64`

```dockerfile
```

-	Layers:
	-	`sha256:f5c4256cb66c59fa61a61b00edd596fb4ea9df538ddabb04405f6677e4055ce8`  
		Last Modified: Tue, 04 Feb 2025 10:42:22 GMT  
		Size: 4.5 MB (4487263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de126843dd3b845a38a5d44d84e924dca553937f671c097df333fd6d0bc14e19`  
		Last Modified: Tue, 04 Feb 2025 10:42:21 GMT  
		Size: 6.9 KB (6861 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:699d0f65411313f79bde102e935b03f05646e0ba90f9e589b53441d582595934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67789750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a6daba633b8e3b34a7f1ce1727329a37c04f9919263899a96fa7cf6ec202154`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0038ef039a89ede34c57806e684dc9d9be7dcd22d3c08b90deb36bb22a2c7122`  
		Last Modified: Tue, 04 Feb 2025 01:38:11 GMT  
		Size: 52.2 MB (52245695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c7afb1aa0f9672a06c4c7eaa6b7c7e111a91a8d45272dce1e361ac0b0ed79a`  
		Last Modified: Tue, 04 Feb 2025 09:00:33 GMT  
		Size: 15.5 MB (15544055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9d5ed3cd0162799c08609a036c8b39212da061b12174a4a202fbd657186c301d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4492122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c58d44733426488446ed36c9936b91cb83423e352e68b6fe40e74bc1561106`

```dockerfile
```

-	Layers:
	-	`sha256:87a5d01b879d7622edad54e86b025c3a014ac7f446b1556f2f242b7a52f27181`  
		Last Modified: Tue, 04 Feb 2025 09:00:32 GMT  
		Size: 4.5 MB (4485241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb2dad3364e37229e045f4ea4ac1d95ca1f1dccbe56ba9ffde542f483711d0ea`  
		Last Modified: Tue, 04 Feb 2025 09:00:32 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:fe810b67717e1433e97cbf12d1c8cac82a2bac40e14211e3c6b9164d68cf85e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70738010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b913c0ae133558275edee8f3575418d30a1f8c5cfe7b0861b45e33a499f4d32`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c2b5327eac1fcd49233dc8f6e5417e7e2efeea16edfcbff9dd025f389e15b11e`  
		Last Modified: Tue, 04 Feb 2025 01:36:38 GMT  
		Size: 54.7 MB (54675956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d372eab1872f98afed1da2c899af883a0b3a6e52e25e2690ed35b3d6f859e5`  
		Last Modified: Tue, 04 Feb 2025 04:23:38 GMT  
		Size: 16.1 MB (16062054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f08e0e3e50b65e876418183cfadf4b9d25087eae4563596822b7cbdd5b537b3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4488847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8d4a982f05b421f194496a7acb871eb45d55828addd847cd37b531dceb1e2e`

```dockerfile
```

-	Layers:
	-	`sha256:eca027a0d706d22c12a86d884435eb6e047b4cf46c279a5c80331993e00d3d10`  
		Last Modified: Tue, 04 Feb 2025 04:23:37 GMT  
		Size: 4.5 MB (4482068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29f26919f0b635f677f0d4b88840cf876653771192f92c6058a0ed2d4a72a971`  
		Last Modified: Tue, 04 Feb 2025 04:23:37 GMT  
		Size: 6.8 KB (6779 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:f8b44d871c904becd02992c1785520907b4166b7974db9aead2789ecbc5d00e0
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
$ docker pull buildpack-deps@sha256:4814e93af668ad776156987b0a30c8b308b118e01fbbd17f741b791b8851bad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (124049061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e581d121fb96975fea39e8d8b79c9c4de4cb6ac154abf3542985c05e89625228`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:478cb73646107d7b3f891aa53abaed926667463844c07b1d924bd760ae03f38a`  
		Last Modified: Tue, 04 Feb 2025 01:36:37 GMT  
		Size: 53.7 MB (53738873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0388f0d5bf1adc15e551cceee5a85f21b1ebf5b13c380ee0e941c5d55013598`  
		Last Modified: Tue, 04 Feb 2025 04:37:42 GMT  
		Size: 15.6 MB (15558271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d473f760e53d3d50afd1cebc7113387023a04ff8ec34073c4412b465ccc2fc5`  
		Last Modified: Tue, 04 Feb 2025 05:19:08 GMT  
		Size: 54.8 MB (54751917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ef9e6950a308d27ad0fed70063500c67d5f94b60458bf35e69a461c78d601501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7715539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c9ec6144be5fdec793e06b9bfe76a1ab2b4f60224d307ec385d56b9d387f4a`

```dockerfile
```

-	Layers:
	-	`sha256:52a22ae317e2876eea325b36b2cc60b6f80c3cb88a7dbdba1853d7465f8d0e0b`  
		Last Modified: Tue, 04 Feb 2025 05:19:07 GMT  
		Size: 7.7 MB (7708186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d5117857f7ca0d3e1bf3a461cdcb72b1ca27dbcbcf55684d0fb889d6ed4006b`  
		Last Modified: Tue, 04 Feb 2025 05:19:07 GMT  
		Size: 7.4 KB (7353 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d774943785660ecc2de823027779a925c87651bd40f06fbc6b58b9de1c8bd809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114339540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d5ee24dd46e5c5e26ee74d9f511fcc3735ef780de9003547e3a914b976008fd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2d8b4e71b0057b288fa0b7cf9b1d15edc9bec9dc37df63d3463ce28e4f414dc9`  
		Last Modified: Tue, 14 Jan 2025 01:35:36 GMT  
		Size: 49.0 MB (49025062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7055bc7f040fce3e9b8f05fd7f56b8a568950e082ea8ea3aa96cf99f49523ca5`  
		Last Modified: Tue, 14 Jan 2025 08:58:39 GMT  
		Size: 14.7 MB (14673832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681398f28ce19a7af317e3774529df465ed1770ca10164fdba3b20f23a5d8026`  
		Last Modified: Tue, 14 Jan 2025 16:16:27 GMT  
		Size: 50.6 MB (50640646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1c91b0f90f1ef91ce5f6c48aadb2477540546f65adf63b3d90982ec86f15a6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7716983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d58caa9f61dfed2e570b426db1959ba75ae97217fa6a9a80716c68ee7e4355f`

```dockerfile
```

-	Layers:
	-	`sha256:d98b7e41b3cd63c512f218dfab9c9d65b81f3eea63c8b836f660301b020c5d66`  
		Last Modified: Tue, 14 Jan 2025 16:16:26 GMT  
		Size: 7.7 MB (7709570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3bdd7383a4b1f4d3f50aaff18c4c7bc58547a6b215c9b01676e6337e8dfb72a`  
		Last Modified: Tue, 14 Jan 2025 16:16:25 GMT  
		Size: 7.4 KB (7413 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7cd12446ba7224b5c2917b1c38ea6cc66ca5d1b816e2220b6746099844d83a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122642755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c009330911b291df3f419696b4f356ad17a61817d491820586e38c2b0009d1bf`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dfd6b176342cb480b79cef9a7188364b0f5702ccc77422fcdb5d7d8f3f42c8`  
		Last Modified: Tue, 14 Jan 2025 07:00:18 GMT  
		Size: 15.5 MB (15544093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23ac0e9b25076f1cc90469f31bffaae783c6a3a88272620af5e7dcbe0b8202`  
		Last Modified: Tue, 14 Jan 2025 13:31:46 GMT  
		Size: 54.9 MB (54852602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c15cf8ae3f7c2b7a8e902962590e6c9064ebc3de259521e75513e13f2e9583c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7721335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea1bc11e1597522ba927e7cf032ac12c2f5c0b48f76688a2c41cc8df5ff6d4c`

```dockerfile
```

-	Layers:
	-	`sha256:cb5b7433e723b0023aeae558a9a132cd43f7fd43bf007e6f3bfc19ad25dd8b7c`  
		Last Modified: Tue, 14 Jan 2025 13:31:45 GMT  
		Size: 7.7 MB (7713902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1092df41e57f424822625c9e363e68af5c5429b0bfca3a72c6d7952e77fbb0a`  
		Last Modified: Tue, 14 Jan 2025 13:31:44 GMT  
		Size: 7.4 KB (7433 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:9a62f978f5fdc58bc19fc0153c3642c7986206935c5123229b9400de09265b18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126767886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb73a16d07dcda55523ead47dacd4d9749d94ac0ad37187950d43b0fdbab437`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c2b5327eac1fcd49233dc8f6e5417e7e2efeea16edfcbff9dd025f389e15b11e`  
		Last Modified: Tue, 04 Feb 2025 01:36:38 GMT  
		Size: 54.7 MB (54675956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d372eab1872f98afed1da2c899af883a0b3a6e52e25e2690ed35b3d6f859e5`  
		Last Modified: Tue, 04 Feb 2025 04:23:38 GMT  
		Size: 16.1 MB (16062054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4520e7fd9b17628990db3e961c2d7570421849af1fe255937c0a9e48cf49a48f`  
		Last Modified: Tue, 04 Feb 2025 05:15:33 GMT  
		Size: 56.0 MB (56029876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4c21667e744397eb3935c16797e52b0148b9d2656c9c5df160d776ef48f8019e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7711006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50bd9c61c42af2df265f3d3c98356591cf58dbc8635d76bca719e8339597bd94`

```dockerfile
```

-	Layers:
	-	`sha256:fcedc0c587cb91d36a7804b4632555da7225541fa346b9a49d88f2ea9ef0ba0d`  
		Last Modified: Tue, 04 Feb 2025 05:15:32 GMT  
		Size: 7.7 MB (7703676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23633969f8f239808620f33b97db5f047216cba12a362fa470b4395f1a8ed0b5`  
		Last Modified: Tue, 04 Feb 2025 05:15:32 GMT  
		Size: 7.3 KB (7330 bytes)  
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
$ docker pull buildpack-deps@sha256:b8921eb6d9c99f9c2bf37f929be3c7a74c50a58149662f72b4dfd90591547e5a
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
$ docker pull buildpack-deps@sha256:107b7c021186efe3ed164cfea1c3d06c8ed6b8ce4582f691ff74a2dc4901a562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136932334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc6260661cca62da45094b3d5d01eb10b3ae352ca934691651dd8543956046a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 01:36:22 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b550be6cb62359a0f3a96bc0dc289f8b45d097eaad275887f163c6780b4108`  
		Last Modified: Tue, 04 Feb 2025 04:37:13 GMT  
		Size: 24.1 MB (24058355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35af2a7690f2b43e7237d1fae8e3f2350dfb25f3249e9cf65121866f9c56c772`  
		Last Modified: Tue, 04 Feb 2025 05:19:13 GMT  
		Size: 64.4 MB (64394292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c45671abb650eed88ec7038f7152842ad8d557322d1c488be20f05be096cb46c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7760401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e2a1f4e1a96a61d654b4ceb41ea6775eaade5e6d735639e5bbea80e9f6294dd`

```dockerfile
```

-	Layers:
	-	`sha256:b87149b2f1486609a2af0770d2c2c37d036fd5e551b650c92f01ea43a97e54c9`  
		Last Modified: Tue, 04 Feb 2025 05:19:11 GMT  
		Size: 7.8 MB (7752746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16de0d9ec26360b8605a9e23ae24c8fa01bba49c7df7a2c647e0c7c43e7a807b`  
		Last Modified: Tue, 04 Feb 2025 05:19:10 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4485452def37f53d9fea2e251dce6eec0c7a015f96823123284127e52bd259de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130743483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4bd79e1728ba3eb164b6a77dc3f9b0cd9778a70d2143f9d9af57d9e10a42a0d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8816181beac5d7674f87060fb5deb0c2c6221a62562265e16f54a617961cbc53`  
		Last Modified: Tue, 04 Feb 2025 01:38:08 GMT  
		Size: 46.0 MB (46006574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28060e71ea1173228ae8eefd6f5fb4296e8c1c73672a593f2d0d8e6e5483072`  
		Last Modified: Tue, 04 Feb 2025 08:03:04 GMT  
		Size: 22.7 MB (22733102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f77895e90931fefcb9b0f936aeec6e8c95f160c764c504ceb6084ffc29b46c`  
		Last Modified: Tue, 04 Feb 2025 10:20:41 GMT  
		Size: 62.0 MB (62003807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9325e1f31ac79d5ec224fd4a72d88769f24ae26a8b0657571c7ed3ab028f0b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7762027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78cbcdcc4c7120567403bfd7323fcb4c9cfc1f4ad85dd84655b4106038f895e1`

```dockerfile
```

-	Layers:
	-	`sha256:787a1a81ca68983478e9b85146549b7060b5bda7b817fb5fa748e29968505496`  
		Last Modified: Tue, 04 Feb 2025 10:20:40 GMT  
		Size: 7.8 MB (7754304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9ae5dbc955356ce8d85cb9395d5a07e003732510094b71b218d7c7f691b41fb`  
		Last Modified: Tue, 04 Feb 2025 10:20:39 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:49e4ccaedbca671c339d8a55242d7f25e1af167a096aca68b56da8a26e979622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125784661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5d6202e1e5273856a4827dd5f9a1aaf9c5c9df9e95e406f72acc587373ce0c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 01:34:58 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787291d61ca82895d27d086bfaf14ce01f401dfbf42f462addc8d1cae464ebab`  
		Last Modified: Tue, 14 Jan 2025 08:58:07 GMT  
		Size: 22.0 MB (21960077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6667f6e75dc8bed2e36123666ac457a4e0228141514ab32e65b9c6f6c7960e3`  
		Last Modified: Tue, 14 Jan 2025 16:15:27 GMT  
		Size: 59.6 MB (59640375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f893443c0cff99fae6cfd9ee2d82f7d9fa1764c42e4b44d6bd02b54a5f8860e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7761753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71830b5b97fe489d694c4fdd593c37b208f010a9b30f5fbbd200b1d5bb8f78f0`

```dockerfile
```

-	Layers:
	-	`sha256:ed0713d12be1303423be5246de90d43ee0ccba8f617f41d991598bef4a257e57`  
		Last Modified: Tue, 14 Jan 2025 16:15:26 GMT  
		Size: 7.8 MB (7754031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dab6ec41bbe5e21c735259ad96692c0dc9cc772b9c0cf51e02e186b1620bc8af`  
		Last Modified: Tue, 14 Jan 2025 16:15:25 GMT  
		Size: 7.7 KB (7722 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3d3e7297c13b3097bf5fb9991ffa9aad0816798a907a8fff792165491174b39a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136261554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413ebeaa354b3c0feb020579c81777bbfe6e0b44434cbb51e0423a9a5e072539`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b85d68f8a4dce392d372c8a196863eac6d111c36b714179b4ab30e00c00d1`  
		Last Modified: Tue, 14 Jan 2025 06:59:53 GMT  
		Size: 23.6 MB (23598225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936252136b926e9bca27f4a5442f6a5d10c0ea4a23ca8b30c65de1bde666d082`  
		Last Modified: Tue, 14 Jan 2025 13:31:06 GMT  
		Size: 64.4 MB (64356433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e54b58bc89d63d6cb7a969a37a81bd05045e92b0531f2dea017d34389f50b348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7766898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cfdf225184ecb259a96744ec5072a8b6321e328e75488d08232ee1c90c8287a`

```dockerfile
```

-	Layers:
	-	`sha256:ee5a579a1304a0cd9ab66a341c82f90bd0673cbb06d2d921649dc6204d1298a5`  
		Last Modified: Tue, 14 Jan 2025 13:31:04 GMT  
		Size: 7.8 MB (7759151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4b7039d4910144475f784c47b0f938b47a0c5c3de6783cc5280520c1dea87bc`  
		Last Modified: Tue, 14 Jan 2025 13:31:03 GMT  
		Size: 7.7 KB (7747 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d1e072586740069d1b5e9086fdcd828de918bfb913d5055e1aaa194f62dcc265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140593719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29f7944ff637b8f0ba1c24926e7d9ef677ee299088eb49272b3ed9d4d155cfb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d6abb78404200438eb560450e089a4e7707a23d5ec913df260500d902666670a`  
		Last Modified: Tue, 04 Feb 2025 01:36:35 GMT  
		Size: 49.5 MB (49457456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7d7e5b6420845d0479145c8a18a31030093be0de73e11194d97fee1ac58ef5`  
		Last Modified: Tue, 04 Feb 2025 04:23:48 GMT  
		Size: 24.9 MB (24899338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43394bbbaab482132a05c8eb702c9ebbbf5ecccd558ce05fdf40c651b7fbfa10`  
		Last Modified: Tue, 04 Feb 2025 05:15:47 GMT  
		Size: 66.2 MB (66236925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9a8c7b49ce3106d816ea038fd374c442087a4e89e2fc93a79ec4684633bac082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7756451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d5b2ac5fd703de6ab1eddd79d25bbe48d83b138aa053a7a88e51177e6a976fd`

```dockerfile
```

-	Layers:
	-	`sha256:9d2a829989dc2c4ace1d5075358dc1cf0e96b3108c0e3b1e30669aa7592e69c9`  
		Last Modified: Tue, 04 Feb 2025 05:15:46 GMT  
		Size: 7.7 MB (7748823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d51ba6d7dd98693c417109d9f16fa8a019ed6cf65c04b4b463211d4e1d1ea1b9`  
		Last Modified: Tue, 04 Feb 2025 05:15:45 GMT  
		Size: 7.6 KB (7628 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:fe602d939df4cbddd8102a3ecbfbd2b79407c0d8a77a3c3a8b61111134ca7a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135706996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c87c17f18e534fcf9eaa672e16e2832528995e9e5780ff4c8964ebef619f07`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:12e528bcd428b4b8475a045cfdce724675384eedf195bad13ce8015853db632c`  
		Last Modified: Tue, 14 Jan 2025 01:34:57 GMT  
		Size: 48.8 MB (48758103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dede5b838e92cbab015cc8e31645fbe220ba02a56693e3a7a144e0a5428690`  
		Last Modified: Tue, 14 Jan 2025 18:10:17 GMT  
		Size: 23.7 MB (23652164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be7513211e793708951d273ea21ae802b4bdb4109f4b12ca6122e317851db90`  
		Last Modified: Wed, 15 Jan 2025 02:00:51 GMT  
		Size: 63.3 MB (63296729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:63f9dd3ac1b3f3fb150b43d7ee5d7172d3f9881b5149b99d19d50bfb75821e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:328981011361d0b51ce891a6cbbdd73023d076afad56601a031dafc25d1c316d`

```dockerfile
```

-	Layers:
	-	`sha256:ea2b61c81e84d989128047eb14c01db001abea44f3d40a2da08f942d63cb38cd`  
		Last Modified: Wed, 15 Jan 2025 02:00:45 GMT  
		Size: 7.5 KB (7497 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:05b4402223200277f406f99fc728e47988998b5946ff282b1a2f2b55db8967f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147875066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07253a39195775999a73cfa312e0fa0c5fa1cb97359e3cf5503e14f02d7368a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:60b6379697eb1bdc0a74d6aa762f7f8e36a4a46031b019e2c7651c9723194c8b`  
		Last Modified: Tue, 14 Jan 2025 01:36:59 GMT  
		Size: 52.3 MB (52313137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b1d1b75ad07ec92cebf5f30e6612d80907cb5a7323fdef7921893e816a53be`  
		Last Modified: Tue, 14 Jan 2025 05:30:15 GMT  
		Size: 25.7 MB (25717439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395bc8910e96064c02227d340de0ac8d0234f64dd58802df0e9bd0891ad39050`  
		Last Modified: Tue, 14 Jan 2025 09:41:58 GMT  
		Size: 69.8 MB (69844490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a9d572ddeddf65e9c94b552da6a41ddb37bb717818328f59458a028ff53349cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7768145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee4e94cc9d33bf313cfc300eb9c016f08f8e9c4621491174b10461db746fb4d`

```dockerfile
```

-	Layers:
	-	`sha256:231c3fce7984cd3e3de5dd5d140d65478f0236395546611c454b0e0421150d73`  
		Last Modified: Tue, 14 Jan 2025 09:41:56 GMT  
		Size: 7.8 MB (7760453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b75b5ea659daa8cc266903efd448b1e7d046a092e5d48598c2331e3ca388f11a`  
		Last Modified: Tue, 14 Jan 2025 09:41:56 GMT  
		Size: 7.7 KB (7692 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5261ec0a644e8aaf0410d07b3f6775921eb9dfd59122eb9155529fc4dd8e12d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134688525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67a46e44795d80467cac123f20812bc46798d0bebc2ca9b6c72285a776183381`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:92bc3bb38690fde96c4bb788f15f365b04d4cb8ab9368675dc9294bc24a9c7b6`  
		Last Modified: Tue, 04 Feb 2025 01:37:03 GMT  
		Size: 47.1 MB (47131492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe7257ceffda4bd6219bda9d63efd9f5fc932de95d2f5db69f3d95df88e73b0`  
		Last Modified: Tue, 04 Feb 2025 07:30:08 GMT  
		Size: 24.1 MB (24057578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800fd1d6411dfa44ccdbe5db47bb7e970909c1a08d63328dfd165607beb67e7c`  
		Last Modified: Tue, 04 Feb 2025 11:34:34 GMT  
		Size: 63.5 MB (63499455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c2ca21cdc0403c9f431731aa97d0c4db85a946a2bacf211d0cfe3ee4e5418bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7759606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5459c93da646c41b36d9e5eeee87162119e171e15ef61c37b7f488c907ac80`

```dockerfile
```

-	Layers:
	-	`sha256:e5d1da80e53060d3414c9fee17945ae782d9600f01876fe0136f6c4d962f8be8`  
		Last Modified: Tue, 04 Feb 2025 11:34:33 GMT  
		Size: 7.8 MB (7751951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd51d33d5be0950a97f8ce96f83c03da82e3ff767c4f51b3c48d301197f978df`  
		Last Modified: Tue, 04 Feb 2025 11:34:33 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:7da2563d1257a09047d12c4b93c3cb98844f223a76f96290544d0476d9356002
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
$ docker pull buildpack-deps@sha256:a89441871a4e4261cfd8f3db1076ca49748dc17d638a043d1c23c6a10c831e0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.3 MB (378286862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec553f6acd4da30811d4a22121cf15fce8f4361e3e5bbe4ff4aae0487f625fa1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9a66d07ec06276723a9d844f79110db2c04e99b6e7ca9f2467ee7789a25614bc`  
		Last Modified: Tue, 04 Feb 2025 01:36:30 GMT  
		Size: 48.5 MB (48478504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37249eb6f9b3505b2330ba5132b480155ccfe125c06c5def806fca9a9daeec74`  
		Last Modified: Tue, 04 Feb 2025 04:37:52 GMT  
		Size: 26.0 MB (26036380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e4fa6b03ff4cb7e858ff5a14c844d64841c23889c0d907ba3b0dff91e9902c`  
		Last Modified: Tue, 04 Feb 2025 05:19:10 GMT  
		Size: 67.5 MB (67468344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79a80f133f68fe6301288293c6c55d0abe1750139940f392c2541c7856dc954`  
		Last Modified: Tue, 04 Feb 2025 06:14:31 GMT  
		Size: 236.3 MB (236303634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ef63815fc34fca45ace31b1a537fc01d787def667cd47e3f20bc2902cd988a1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16918509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d95b29521e7e9a9cbfad7bd2bf2f0c60feb61981efab1c979b548d099c1d258`

```dockerfile
```

-	Layers:
	-	`sha256:abbd56d590bdbd61585fbf3c94dc21f612324f29bfcd68e78cdca9969520472f`  
		Last Modified: Tue, 04 Feb 2025 06:14:28 GMT  
		Size: 16.9 MB (16908333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:642f9f638d888a947630031a8911443c6dfc2339e5c8eee02b7f95a6e283e06e`  
		Last Modified: Tue, 04 Feb 2025 06:14:27 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:bc797efcc1bfb1580fc82fef2235b5ae298f3c1a39da7bc1e3284a089c152205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.5 MB (342450921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4454bda53f727cd002c420b50b5434bb0a09863c78197e6fa36bd5dd1665a040`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:969faa28a060b3165779eb5369b5e31931290ad408fa4e8e60d177e2f80c2611`  
		Last Modified: Tue, 04 Feb 2025 01:38:51 GMT  
		Size: 46.7 MB (46706175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd2fe3d3c4202f31101bc1bc73cd3af8a62f52a1188e729c8a3228780cf83d0`  
		Last Modified: Tue, 04 Feb 2025 08:03:51 GMT  
		Size: 24.7 MB (24746488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b0ffd764a137045323ce5b430a010c0f27d927825897343bc94eb266304a12`  
		Last Modified: Tue, 04 Feb 2025 10:21:56 GMT  
		Size: 65.2 MB (65167643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8315467ee71a8ad5b2dec12ccab0e7fceaaf53e524d175daa1d5cf08d233072`  
		Last Modified: Tue, 04 Feb 2025 11:45:34 GMT  
		Size: 205.8 MB (205830615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:16dad910d55c70dfeba9c305910e8bbae19182f85b9380b16fddc7878158d74b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16687959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1ed49a8170d29bc351d2875938957f1037cdc6ff9d7545fa23f2fe1b181fe47`

```dockerfile
```

-	Layers:
	-	`sha256:19357ca9bf0b78bf8c5485b1935cb1fb4a1b0648d36bec0ee73d5b6072b898ee`  
		Last Modified: Tue, 04 Feb 2025 11:45:29 GMT  
		Size: 16.7 MB (16677723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c95894fead5209f44c8c99d0fd361dc9405cec026e929f9bf97f45e260a7640`  
		Last Modified: Tue, 04 Feb 2025 11:45:28 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fe578c1e871363d504bb8bab30736288c85647392e992202c6258e71e2f02462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.9 MB (327929744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51c46e692bb0a4dcb234fa5110bc74dbf398d106e8bf1908c30f71f200c22f98`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a0e0ff4d5bcbd6e2c25332ca46ec757661e665f67ef593a6f9b269659d2aeab0`  
		Last Modified: Tue, 14 Jan 2025 01:36:57 GMT  
		Size: 44.7 MB (44668351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6de100729dc42fca6e1da779a5cabf824cb59902a2e776e84fe6b7124d28a0`  
		Last Modified: Tue, 14 Jan 2025 08:59:23 GMT  
		Size: 23.9 MB (23876812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c133cb44b43ce8e0628b481f6d32820f19b92bbcee07e7706966c203b607284a`  
		Last Modified: Tue, 14 Jan 2025 16:17:30 GMT  
		Size: 62.5 MB (62467463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9795004ef2c293073508c69f28eb42c2d7b2f33f65dae4735b067629f5120204`  
		Last Modified: Tue, 14 Jan 2025 21:59:24 GMT  
		Size: 196.9 MB (196917118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e83811cfe7c760f9da87d6f1c5a150ea9a0dd21ade505b732fcdc8e7f0fc842b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16669569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e59fd63dd1941542b79def3463a82f3d0501a82065c295a5f9fdcb14c59198`

```dockerfile
```

-	Layers:
	-	`sha256:73f47150d048eba6124064fe6305a459362e7b0775142ef28c837992ad3c09b0`  
		Last Modified: Tue, 14 Jan 2025 21:59:19 GMT  
		Size: 16.7 MB (16659333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3eaa593dc99f801f19eba455556f9adb976b1822e75bc2877fe1dc8719fa838`  
		Last Modified: Tue, 14 Jan 2025 21:59:18 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:789f10d38342832bf75ef3e2b9ee9f29c017fac09a6f868925fe21d87a81f7cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.5 MB (372546196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e83d3f56d50bf5b5f068663d981200a5154d5a23a3d0c7bb6402edad1f5f64`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7cef9546887caee4cb752860ee90de96728f638ede0f77bda226ca44ac3e04db`  
		Last Modified: Tue, 14 Jan 2025 01:37:16 GMT  
		Size: 48.8 MB (48760872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fc550a04d72fdc48fc4716034190ede3de291a338b2c748b32584534d2c3f1`  
		Last Modified: Tue, 14 Jan 2025 07:00:48 GMT  
		Size: 25.5 MB (25487312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97035a0dde45440d902fa525c75a16c6689c0105aa65885137511ec2d09218fb`  
		Last Modified: Tue, 14 Jan 2025 13:32:31 GMT  
		Size: 67.5 MB (67473976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68415822cccaa14224085f576cbd5da670da2f1a5ddec7d638f697742f5d0fdd`  
		Last Modified: Tue, 14 Jan 2025 17:12:06 GMT  
		Size: 230.8 MB (230824036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a9d60646ee171c4bba05f9cc204056ad1c63baeeab442bfdb1f4eab411b29c2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16987901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc196fdb5c8549d2f62aff178e0847779860dbadc42b2b180f89b418ce37f93e`

```dockerfile
```

-	Layers:
	-	`sha256:6d0948f13d2062aca9845321a479880fb218c0b6ff7f1b94ac1794b6ff823c72`  
		Last Modified: Tue, 14 Jan 2025 17:12:02 GMT  
		Size: 17.0 MB (16977645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d591e35d33d3cfcf7cf730fcc9b68431bce541892eea719c801528f64c8f264`  
		Last Modified: Tue, 14 Jan 2025 17:12:01 GMT  
		Size: 10.3 KB (10256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0a346c8030f310001211274abb71e5c9c2279d293b63c22819e742b69a6c8532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.5 MB (386542332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877c96aa12281c5fd8180613fe153cb1b495b5ec73f62325e544bec45ba0ca20`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:51741382468681fc53992e03a5e8ce7f591198e39599d81f3b698e3652a63db4`  
		Last Modified: Tue, 04 Feb 2025 01:36:41 GMT  
		Size: 49.9 MB (49883916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4227754a1dcb648ed5c4c8f40f8d60f655bb96ef669b5da48ad50132dc9621`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 27.2 MB (27185942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74bb38fe259cd8a9e1ef2a45c45f0372cb16ddaf5c5facf3363ca9cfcede2c4d`  
		Last Modified: Tue, 04 Feb 2025 05:15:50 GMT  
		Size: 69.4 MB (69401812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e8429ab45660ec1d3a19982bbd0af3a786637fa24a29bbd4fe03f5d823ef2b`  
		Last Modified: Tue, 04 Feb 2025 06:15:15 GMT  
		Size: 240.1 MB (240070662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a856d0d673b5070a08ba0ef1a694cbcefafc2e847fe62a0db8908c9a890af238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16887333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bc2715ad9648f547ef50c6f946121d126d9bb8ea48f75afe0d30f539576721`

```dockerfile
```

-	Layers:
	-	`sha256:7228efcf52a85711aae46c80cce5e57101b9b21148249ea6e908d113190a5814`  
		Last Modified: Tue, 04 Feb 2025 06:15:10 GMT  
		Size: 16.9 MB (16877179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe4bb2dea9acf4e5f3939bebdc437405c35beb7e0d1876c48b51faed87418e36`  
		Last Modified: Tue, 04 Feb 2025 06:15:09 GMT  
		Size: 10.2 KB (10154 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:c3af075a6bb84a32799c35580e83b5601f890c8d940db050505b4dc6c8a93321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.1 MB (360106862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:969cf85422af15790fa0a4564ead6c8e64cd05059f896b02da84563dda047911`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1ad11d2c3d2c0479cee56b824f2514b710c0c76d88c22da7ef5ec7f2ccc527d0`  
		Last Modified: Tue, 14 Jan 2025 01:35:17 GMT  
		Size: 48.5 MB (48545883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7625cd98aa6d5c80fb0d1f627561581568ea6f268919dc1e831bfca9d1e853`  
		Last Modified: Tue, 14 Jan 2025 18:12:26 GMT  
		Size: 26.0 MB (26040345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d41982939111491c6252a19353da998fa5ef416acfaed05792f55a462ab11e`  
		Last Modified: Wed, 15 Jan 2025 02:04:08 GMT  
		Size: 66.1 MB (66119517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3de884e734576434f49639f4eac10e8ea4a8319859bf9f4ddab2b2535f94676`  
		Last Modified: Wed, 15 Jan 2025 18:07:13 GMT  
		Size: 219.4 MB (219401117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:98d12704efad8167ae328c80f2b65f7537104b8eb6d65dcb91e8169be51a56ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f78aef405075ee21b5576e2cd9614944b32c443a23c800108a83b0b40e8263`

```dockerfile
```

-	Layers:
	-	`sha256:be2f46aad2ab5b0965a4dcc567ad80fe2f0180465992cbaf83183ad959cc15fe`  
		Last Modified: Wed, 15 Jan 2025 18:06:53 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f945636514ae3362ca71164884853f2f404b1119ca45926602f12d477155a9ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.4 MB (384371887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0546df0594a9cf5437bf0c515631731c6d736876e68e9daaf7b025bc56efdd46`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fca4ba78a63cac2994d6f3576656e907e3a130a20f935b6a1e2c945c9e7be3af`  
		Last Modified: Tue, 14 Jan 2025 01:38:04 GMT  
		Size: 52.2 MB (52151887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f2cddc488774629199c39c9010734d4be824e6ca934835a5e2d444a85e0075`  
		Last Modified: Tue, 14 Jan 2025 05:31:14 GMT  
		Size: 27.6 MB (27591847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97154d7b719fe3158c773c51a570d7d8ab1e54dcb04c12ce4e93476ca16bbefc`  
		Last Modified: Tue, 14 Jan 2025 09:43:30 GMT  
		Size: 72.9 MB (72876836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6943e22d3036deb30248e5634a993ff72c73507d02437a5bb09280b60bf18d6a`  
		Last Modified: Tue, 14 Jan 2025 13:04:19 GMT  
		Size: 231.8 MB (231751317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f65afdda5fbd62f678db83abfa2fe8e77dda067ff81471cd5b968084e06b0463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16889169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ee6c8a1fa836d956d9ca48a65ac8f826a5d616d3bd16b7c2e016175f840e92`

```dockerfile
```

-	Layers:
	-	`sha256:2fce16de76b13f416770a657209c2106c50c3ec4ed409e55241d96278276993d`  
		Last Modified: Tue, 14 Jan 2025 13:04:14 GMT  
		Size: 16.9 MB (16878961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82b4b42020474e39ceb70591d326ad42b7fd3699657c3881062386d87d8f34a3`  
		Last Modified: Tue, 14 Jan 2025 13:04:13 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:3639f13190096719aac7a54bedfd4e09b26fc0dd2a909639e7cf0a3fd33ba631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.5 MB (460506022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e888d6f05533ef4be30c9b22e055cac880d4bb0df839b638fd86c8a2bc90772c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:41a19e48936e10f226b6bfe61097156b74f03101f788496e8860f0d4806f05ba`  
		Last Modified: Tue, 04 Feb 2025 01:38:33 GMT  
		Size: 47.0 MB (47040914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a706305f90a9f6f5a4662ef1063ca9b1d12e77b9f1482c3925294e4989eea2f`  
		Last Modified: Tue, 04 Feb 2025 04:38:37 GMT  
		Size: 25.4 MB (25411970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2279830c9cdcc3d6d50a4a0308903e5819e1f53fc61863f2bc9dae664a4b8e0e`  
		Last Modified: Tue, 04 Feb 2025 08:09:05 GMT  
		Size: 66.5 MB (66493760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0674f07b14526b99d8a1ad6e260fa13f5923299979b4990047db0a18f0e7754f`  
		Last Modified: Tue, 04 Feb 2025 09:50:26 GMT  
		Size: 321.6 MB (321559378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2b8df108a10b1e88d6b87824249ab1fb77f1b9afd698bc50f1911e8450899dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16974645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca31fb4b8ab775c0c89f10c2d00db316af5da9f635cec87da6421dcb44f602e`

```dockerfile
```

-	Layers:
	-	`sha256:844d407e0f895e351a3eb25d6945314331d6d457cefa01ea0b3de0ce8c11ee63`  
		Last Modified: Tue, 04 Feb 2025 09:49:44 GMT  
		Size: 17.0 MB (16964438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd8f8a3c148cbeea3b0e96dd11781e968a527ea4b64c2fd01544e28ce3ff8eba`  
		Last Modified: Tue, 04 Feb 2025 09:49:41 GMT  
		Size: 10.2 KB (10207 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c93ead5df32df5fda7821d7eea3245b3ad1fecf33ab58a7fbe75672128d2a94a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.8 MB (350769776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63bf6ddec63e07aaf55bebcf801af659826e992e4b6344ef4f3fb7b0f56001f1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:98a334b3a419c858b25979b9c4fcf97a87431d5b5cddfa6c4c566454b23fcf62`  
		Last Modified: Tue, 14 Jan 2025 01:35:18 GMT  
		Size: 48.4 MB (48434824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d732c90ca5b141c789480c7eea03644a6f254edf6c95ed1e124a245a18b8c3cf`  
		Last Modified: Tue, 14 Jan 2025 05:00:30 GMT  
		Size: 27.2 MB (27196670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c226835589caa484a321d0762131f155a336675c8b326b2fb32917038d1fe871`  
		Last Modified: Tue, 14 Jan 2025 09:11:02 GMT  
		Size: 68.5 MB (68532734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2ee3ebe99142809d95638070bf937a25f6487ab59250faa71ded6bbcd0dcf6`  
		Last Modified: Tue, 14 Jan 2025 11:17:51 GMT  
		Size: 206.6 MB (206605548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dd84808ef735ca84f852e884ede3f5d30f494c30ebdfcfac6d4acb304edcaefb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16682803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcba902ca02bdbd2fa325c971ad0d962569c31f8134d6bf80819cdd45ec97c3c`

```dockerfile
```

-	Layers:
	-	`sha256:33660ad64d7fe7f55455954a254a4ba36f59ffc22e0fc691fa83f9ce752069e9`  
		Last Modified: Tue, 14 Jan 2025 11:17:50 GMT  
		Size: 16.7 MB (16672627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69c6b274d24546c7f80941c17f12b7dc21cf3a4af00aa222a43f2173c9504ed9`  
		Last Modified: Tue, 14 Jan 2025 11:17:48 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:630da0806dd470371eca4a7554b6ba283509fa5e3af909ac5ac98b8958add90c
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
$ docker pull buildpack-deps@sha256:f638ef05d64605d170c445f4dbc6194cb452a48dd22e37b7c512306d638fdcc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74514884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3caddad04e472fcf3574c79b97ef9b2c377554176ebd3c85ca858bcbb8bdda2d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9a66d07ec06276723a9d844f79110db2c04e99b6e7ca9f2467ee7789a25614bc`  
		Last Modified: Tue, 04 Feb 2025 01:36:30 GMT  
		Size: 48.5 MB (48478504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37249eb6f9b3505b2330ba5132b480155ccfe125c06c5def806fca9a9daeec74`  
		Last Modified: Tue, 04 Feb 2025 04:37:52 GMT  
		Size: 26.0 MB (26036380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a5a03516c213b8395285411f64ab7e53b1a86f5a65de46a7d95fafb667e0d8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4043601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06af5378da6fdf718d35cb019e89f718b729a813ce8b83c506ee8a802ae4d389`

```dockerfile
```

-	Layers:
	-	`sha256:477cd3c19a37ed7a9ee13a81ff3da27cdcf9e27851258611a960eefd4f3e73ba`  
		Last Modified: Tue, 04 Feb 2025 04:37:52 GMT  
		Size: 4.0 MB (4036797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2f10ad7261a54ee4f8c56a579b66d638edab808a52504248debae6df278b9ac`  
		Last Modified: Tue, 04 Feb 2025 04:37:52 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f45875ec73ce9b7c8aeb688b988e4dd79e4b6c842cd21b893b5f398a492c94ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71452663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b92a325e484088d0c8688eb6aea68ba80bc45eb8aafc520d1518ed29e7fe90`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:969faa28a060b3165779eb5369b5e31931290ad408fa4e8e60d177e2f80c2611`  
		Last Modified: Tue, 04 Feb 2025 01:38:51 GMT  
		Size: 46.7 MB (46706175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd2fe3d3c4202f31101bc1bc73cd3af8a62f52a1188e729c8a3228780cf83d0`  
		Last Modified: Tue, 04 Feb 2025 08:03:51 GMT  
		Size: 24.7 MB (24746488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8134fda17aa6d80f9759a5952f0ffeae4602704b27b326298b638578d10d443c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59fbe16f31e28338f95f054b58a4401aa744e22829c9917e4841dedd2e5ab5a2`

```dockerfile
```

-	Layers:
	-	`sha256:c4e2ff509be119eb73702d3d519a72531f576a70f9908862c43a7786492a6d96`  
		Last Modified: Tue, 04 Feb 2025 08:03:50 GMT  
		Size: 4.0 MB (4044425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe41ba8a61745b055d7c1ff4fcead3d482410c8dc06a548e6382e5c4c140e1aa`  
		Last Modified: Tue, 04 Feb 2025 08:03:50 GMT  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:feb9c2d61fb4c4c7b0252883717ff509c78811124a512a8ce3ecb9807979175d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68731225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ba6aec6b23b2b51d61ff1c09d4b883bd1ccf368730e25c946e90282a46f6033`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:eaba0613b673e68ada7f5f2b5e4971d3556823043148e63c2a6887ee2d5edef0`  
		Last Modified: Tue, 04 Feb 2025 01:39:12 GMT  
		Size: 44.8 MB (44838928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6395c61799d55a9640c01c9ef3b8549d20d61a975f9340e0353ec8e6422685f`  
		Last Modified: Tue, 04 Feb 2025 10:43:02 GMT  
		Size: 23.9 MB (23892297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fd556847f4ae2a75b56788585a6dbed042bd64bebdf265e9ad9a60375b4529d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4043885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb443e4c1924cb01c661174585062ed0e2396c690d9a227622c118244322b84`

```dockerfile
```

-	Layers:
	-	`sha256:7a16946bcda3770000ccad1fec8abad756c10a59958b8efbc69b478d0a12a6a3`  
		Last Modified: Tue, 04 Feb 2025 10:43:01 GMT  
		Size: 4.0 MB (4037021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbd45c6d9e9057c1679f44da49613d30cf0a4b169f2b71b52dbe6b2392d94da8`  
		Last Modified: Tue, 04 Feb 2025 10:43:01 GMT  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3cf31dfb3b9a512d37f417618dc8d2c709472b36c3d7493768dcaa9a394e0b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74377354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc13d99c12b3cd6acb985c585b0342c53dd123416f363f2d506091c48cb376ab`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f518c8f510cd10fda797c5ee77280d7c81b61ff1077c267de12ce9c337ddbe7b`  
		Last Modified: Tue, 04 Feb 2025 01:39:15 GMT  
		Size: 48.9 MB (48874714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b09bd24e474d679cb3c70ae42560294c37e17235d92a739791f20279494fa5e`  
		Last Modified: Tue, 04 Feb 2025 09:01:04 GMT  
		Size: 25.5 MB (25502640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b762f13089947f528337b22e97a2034d96f4970fb44b8514f374c981f492adb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4044577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2924e69ba8c13f46c71be66ca59a7404e757deedae5b1d977d6d35cfdfe739d0`

```dockerfile
```

-	Layers:
	-	`sha256:e50add4bfa70921343045e27ae494c4ba6b21657d3117a96e9e96c8f3143af4d`  
		Last Modified: Tue, 04 Feb 2025 09:01:04 GMT  
		Size: 4.0 MB (4037693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:accd7297c44bb051bb6828c0c99e27d5fcba3fe49d95e31fdc9ff6b84e6b2fdf`  
		Last Modified: Tue, 04 Feb 2025 09:01:03 GMT  
		Size: 6.9 KB (6884 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0f50343f2052ca365fd8378a57d6e415675836af02416da168be148c36f4b236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77069858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e0fb9d10924a5ef45ec45f9c72c8b720d45649556a48e0328c36eff1c0af02`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:51741382468681fc53992e03a5e8ce7f591198e39599d81f3b698e3652a63db4`  
		Last Modified: Tue, 04 Feb 2025 01:36:41 GMT  
		Size: 49.9 MB (49883916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4227754a1dcb648ed5c4c8f40f8d60f655bb96ef669b5da48ad50132dc9621`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 27.2 MB (27185942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:69d9c63d976a1d2ec4df4b17cfbe241837c6d3fa77e82c0ae0239bc737f75989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4039334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dbff316c1752c79b0991fef1767dc049c843f8e4a6d26117434c6b95b5ec6b2`

```dockerfile
```

-	Layers:
	-	`sha256:80121ec0759de207705a8e6b0a5f2635b3c614ec56b2e4172a71cec99f8f701e`  
		Last Modified: Tue, 04 Feb 2025 04:23:41 GMT  
		Size: 4.0 MB (4032552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07ad54558e3d4158f6d4b0dc6bea4f73a317cde2c777f58a1128b0e6db038b16`  
		Last Modified: Tue, 04 Feb 2025 04:23:41 GMT  
		Size: 6.8 KB (6782 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:a11806098d728722edfd2ccc5eea62b183a99295300cc26c512aeb6ec5139688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74586228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df50432b3d5ec0d47a2f773ac1995550ce8a39eee1472f22dfa6eeb27139eed`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1ad11d2c3d2c0479cee56b824f2514b710c0c76d88c22da7ef5ec7f2ccc527d0`  
		Last Modified: Tue, 14 Jan 2025 01:35:17 GMT  
		Size: 48.5 MB (48545883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7625cd98aa6d5c80fb0d1f627561581568ea6f268919dc1e831bfca9d1e853`  
		Last Modified: Tue, 14 Jan 2025 18:12:26 GMT  
		Size: 26.0 MB (26040345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c1c4ea9e5260c374212eb1c5c7c2df5c612816c7260731a54415f310a87b225c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 KB (6637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e443da628babc958694dcf5f479e2146d07dbc4aa30f89627fde7e1994fb90e`

```dockerfile
```

-	Layers:
	-	`sha256:0fbd0b7dbca6501003c60a441261b32562fb2857b68853b4327ebb9c5e316444`  
		Last Modified: Tue, 14 Jan 2025 18:12:23 GMT  
		Size: 6.6 KB (6637 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b444e034fcd78a58112ed02d5089c9ed9523c0bcfeb72959d9d38b5e76918c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79881843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef59a3f5555ebb3a1ed91d3955dfa71dff4e43bc9f33b75541cb5c1d31ac0961`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:20ee406f6988f44113bcc71bae5adfb439e360c88b767260000751228a498e00`  
		Last Modified: Tue, 04 Feb 2025 01:38:35 GMT  
		Size: 52.3 MB (52287301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089b8eaf628cc7675b29225b3b455c5d86d2c6a1f5fa29d78dfb7f3bfa69b3ec`  
		Last Modified: Tue, 04 Feb 2025 07:25:22 GMT  
		Size: 27.6 MB (27594542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:104cc649b82b1e77cbd6184495b219156bcbf219aafc3ffa91c645b37c7397a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4052300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa49d461d527f74f3e9579c6ffbcd86bb78f64c91f1a79b6e24c087d80118384`

```dockerfile
```

-	Layers:
	-	`sha256:06ac9900b3736f9ef1743b06b377a584edf329ccb407da2e23a82060d06fbff4`  
		Last Modified: Tue, 04 Feb 2025 07:25:21 GMT  
		Size: 4.0 MB (4045465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb608baa041b04181310aae0975ae61d6de897858f601e0a076a01d775590fd5`  
		Last Modified: Tue, 04 Feb 2025 07:25:20 GMT  
		Size: 6.8 KB (6835 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:2734aa4dea895af92674c6244686355bcfa7c5f532af30ab2ccd9a106e755945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72452884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b17487fc2e48d4719f558a2b395daac4854c5cc8027f11e20fc0a057d484f87`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:41a19e48936e10f226b6bfe61097156b74f03101f788496e8860f0d4806f05ba`  
		Last Modified: Tue, 04 Feb 2025 01:38:33 GMT  
		Size: 47.0 MB (47040914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a706305f90a9f6f5a4662ef1063ca9b1d12e77b9f1482c3925294e4989eea2f`  
		Last Modified: Tue, 04 Feb 2025 04:38:37 GMT  
		Size: 25.4 MB (25411970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:44623c62d8dedafe11ab33444dff3d267c0b5a8cbf31207f2b7ea43d5854da5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4035021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d21dab2b6e78a3bd7ee008870193435baea98bbc4121d11d2482fec4e3e7e14`

```dockerfile
```

-	Layers:
	-	`sha256:dd80ddface841cec8633795f62cdd6ea9def4ba807b88f55db178fced191241e`  
		Last Modified: Tue, 04 Feb 2025 04:38:34 GMT  
		Size: 4.0 MB (4028186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:541368828ce448681a506ecc6bf3db770febf0bada8ea05ff3b963e42b1f3d0e`  
		Last Modified: Tue, 04 Feb 2025 04:38:33 GMT  
		Size: 6.8 KB (6835 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:171e8794c6153ede3b2dcd344446533bc1d8ea6b0b18282773719bc84686f7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75775246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63fe77152201f7c14106126b989c319db82ddb59047e1a6ed9a845747d8d6239`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1f48ea4a277664853f54eabe6340c7571241c845468906404bbb1efd60e69807`  
		Last Modified: Tue, 04 Feb 2025 01:38:18 GMT  
		Size: 48.6 MB (48560783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1f7d849459507f8a608795416d02b409e9f01c22159fa5acaf53ea0891b503`  
		Last Modified: Tue, 04 Feb 2025 07:31:13 GMT  
		Size: 27.2 MB (27214463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:87d777a50cfb26dc4d318ba34304296d2a7dfc51aff23790a64b8bf9d8c268a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4049932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68bcddd9e386b9d03f6814425470a8ea110334e24aa94511ea90bfc36742ec67`

```dockerfile
```

-	Layers:
	-	`sha256:9cba160456722d8e64ad7d4fc68cc65901918c0c5bca0dd5108b22cae6340e15`  
		Last Modified: Tue, 04 Feb 2025 07:31:12 GMT  
		Size: 4.0 MB (4043129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6b747fbcbe0026e5bbc6fd98c53854cdf3b2e96844372ef3cc2b6170266f168`  
		Last Modified: Tue, 04 Feb 2025 07:31:12 GMT  
		Size: 6.8 KB (6803 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:20c246ac9a42995c023ae7e4a72eb7f2584d01fde39596b6afcd9b5a821c619a
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
$ docker pull buildpack-deps@sha256:49050b174b7c280c7397a668862e7b07e65d41029fffd9a4289f0ba89f51830e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (141983228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de9e7ceb22c36a43a1fe888d57519e4006cca29fa80a1a9bbd024ae5aa7a57f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9a66d07ec06276723a9d844f79110db2c04e99b6e7ca9f2467ee7789a25614bc`  
		Last Modified: Tue, 04 Feb 2025 01:36:30 GMT  
		Size: 48.5 MB (48478504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37249eb6f9b3505b2330ba5132b480155ccfe125c06c5def806fca9a9daeec74`  
		Last Modified: Tue, 04 Feb 2025 04:37:52 GMT  
		Size: 26.0 MB (26036380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e4fa6b03ff4cb7e858ff5a14c844d64841c23889c0d907ba3b0dff91e9902c`  
		Last Modified: Tue, 04 Feb 2025 05:19:10 GMT  
		Size: 67.5 MB (67468344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:36ce389bcf9326720dbf7ecbf7a2a66e2953fbc3a32824120544ffc68c1a1f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7666507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7fcf6cb261b3b8b8689b31075e7690f118d26a8b64a4ab267a858e5255a765c`

```dockerfile
```

-	Layers:
	-	`sha256:18e8f73b18c7f8320da0a5c85645371cd9b3056ba3baf871fe86c4167ab951f9`  
		Last Modified: Tue, 04 Feb 2025 05:19:10 GMT  
		Size: 7.7 MB (7659210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20734c0cd4a50db3c1fe6185badc40dcd0819cdd78875967da043713cbe216fc`  
		Last Modified: Tue, 04 Feb 2025 05:19:09 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:84e24c852d00a207988799b1ad4a7cf719bd43f200246dedf394b1cb43ffcede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136620306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f68cffa395db19a15f11e2e54c002061f0eb04cf08a399d55f3be0d0214dba2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:969faa28a060b3165779eb5369b5e31931290ad408fa4e8e60d177e2f80c2611`  
		Last Modified: Tue, 04 Feb 2025 01:38:51 GMT  
		Size: 46.7 MB (46706175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd2fe3d3c4202f31101bc1bc73cd3af8a62f52a1188e729c8a3228780cf83d0`  
		Last Modified: Tue, 04 Feb 2025 08:03:51 GMT  
		Size: 24.7 MB (24746488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b0ffd764a137045323ce5b430a010c0f27d927825897343bc94eb266304a12`  
		Last Modified: Tue, 04 Feb 2025 10:21:56 GMT  
		Size: 65.2 MB (65167643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c25d78ad7955120511cf4a3329704af325854f4bcbc68110298967b337614378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7672250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b251aa22b2c24e45824d63d1866f50eb24f3fab6da989e814c81d535476a01`

```dockerfile
```

-	Layers:
	-	`sha256:0cc201c117d3c9d6a6d128311bc553cbb8f8288c95b25dc23d9056096e64f723`  
		Last Modified: Tue, 04 Feb 2025 10:21:51 GMT  
		Size: 7.7 MB (7664893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a9af14d91087ed924e26d790d458c6c4e9088eb5e6fea94d4bfe8a661552b19`  
		Last Modified: Tue, 04 Feb 2025 10:21:50 GMT  
		Size: 7.4 KB (7357 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:963821eab438cca62a72541d9517491b6b758bd7a71fb9dc131f2537230f081a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (131012626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ccae8cf93158ee853f476a9109dd2af22f33d5e8f8bea290aa1078ac2400a30`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a0e0ff4d5bcbd6e2c25332ca46ec757661e665f67ef593a6f9b269659d2aeab0`  
		Last Modified: Tue, 14 Jan 2025 01:36:57 GMT  
		Size: 44.7 MB (44668351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6de100729dc42fca6e1da779a5cabf824cb59902a2e776e84fe6b7124d28a0`  
		Last Modified: Tue, 14 Jan 2025 08:59:23 GMT  
		Size: 23.9 MB (23876812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c133cb44b43ce8e0628b481f6d32820f19b92bbcee07e7706966c203b607284a`  
		Last Modified: Tue, 14 Jan 2025 16:17:30 GMT  
		Size: 62.5 MB (62467463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c724c35f72f32fd7ce9fc73e81354004d117302c8a645746010e67cfad7bf7c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7634670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d157cfbee009a2005ad4f645cb3d386e308cd2dc1924ae726097376d3f653d82`

```dockerfile
```

-	Layers:
	-	`sha256:c32c99ffae3952178d8fa4d0f1ea8146402add0c6df485c7af1ff72bd75d8d32`  
		Last Modified: Tue, 14 Jan 2025 16:17:28 GMT  
		Size: 7.6 MB (7627313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56badd2735f45c4d8768ab030f31de125093b00e7776267191877090d63463cd`  
		Last Modified: Tue, 14 Jan 2025 16:17:27 GMT  
		Size: 7.4 KB (7357 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:99626c55ddc16b23335b0fc1995673efbb918649fbf4fab6f7784e7c96083405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141722160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:976b9892d2184abc5a382db5e3174b5e6a17000ec2933cce2be8e2e021845720`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7cef9546887caee4cb752860ee90de96728f638ede0f77bda226ca44ac3e04db`  
		Last Modified: Tue, 14 Jan 2025 01:37:16 GMT  
		Size: 48.8 MB (48760872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fc550a04d72fdc48fc4716034190ede3de291a338b2c748b32584534d2c3f1`  
		Last Modified: Tue, 14 Jan 2025 07:00:48 GMT  
		Size: 25.5 MB (25487312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97035a0dde45440d902fa525c75a16c6689c0105aa65885137511ec2d09218fb`  
		Last Modified: Tue, 14 Jan 2025 13:32:31 GMT  
		Size: 67.5 MB (67473976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:77aac8c09632d225ec7ad937466487a18fe44b41321162b63a495deb5d7b09bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7642481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb3664716cbc9827e0d4700eb1a943adee7374c4275ebb1f4c2ad10bfc88c09c`

```dockerfile
```

-	Layers:
	-	`sha256:37625ca4e83e7ecc5ab4a9bb6accc1b603a4513f134d31e5077dd26734898763`  
		Last Modified: Tue, 14 Jan 2025 13:32:29 GMT  
		Size: 7.6 MB (7635104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a47b95af4fcf2431e73ac39d0424c1dde7f7ee5b3a2c920721d4584e9afa5e36`  
		Last Modified: Tue, 14 Jan 2025 13:32:28 GMT  
		Size: 7.4 KB (7377 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6678694174d4f8eeeffa050f0fc716c554ad11fc7f6a029f8ebb4797c6fbe517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146471670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80da4043c23e99d797e3ac30aa56c3125b9748c66f5e6d89758cdbf9d9828488`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:51741382468681fc53992e03a5e8ce7f591198e39599d81f3b698e3652a63db4`  
		Last Modified: Tue, 04 Feb 2025 01:36:41 GMT  
		Size: 49.9 MB (49883916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4227754a1dcb648ed5c4c8f40f8d60f655bb96ef669b5da48ad50132dc9621`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 27.2 MB (27185942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74bb38fe259cd8a9e1ef2a45c45f0372cb16ddaf5c5facf3363ca9cfcede2c4d`  
		Last Modified: Tue, 04 Feb 2025 05:15:50 GMT  
		Size: 69.4 MB (69401812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:179c2eca5debb1d945c5b9eeaf22c0e8db8339553ed7d92bea95b044f525ea1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7661234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4a4108ec78cddbd0969cb329e129c9a6c49ee083712bc2b3c5c2803e244549`

```dockerfile
```

-	Layers:
	-	`sha256:7ce5bd96b9500a5bf64ca90b6006bd7805c45b65a27e6928eac71f99c067ff43`  
		Last Modified: Tue, 04 Feb 2025 05:15:49 GMT  
		Size: 7.7 MB (7653959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d21eccae88899113b9e0126cb64255aca549e84521b34ecc5fc1d7c273a2b36`  
		Last Modified: Tue, 04 Feb 2025 05:15:48 GMT  
		Size: 7.3 KB (7275 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:f77dbb626432088faf0677622876c0ec92e981900c02ed8d56d1e3f06b5437c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140705745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d330c8a9b3041cb1c438700b5ff456851b2af6ac9b9106c526d10f0cba85723c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1ad11d2c3d2c0479cee56b824f2514b710c0c76d88c22da7ef5ec7f2ccc527d0`  
		Last Modified: Tue, 14 Jan 2025 01:35:17 GMT  
		Size: 48.5 MB (48545883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7625cd98aa6d5c80fb0d1f627561581568ea6f268919dc1e831bfca9d1e853`  
		Last Modified: Tue, 14 Jan 2025 18:12:26 GMT  
		Size: 26.0 MB (26040345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d41982939111491c6252a19353da998fa5ef416acfaed05792f55a462ab11e`  
		Last Modified: Wed, 15 Jan 2025 02:04:08 GMT  
		Size: 66.1 MB (66119517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1dfe48479ceb60993458a81c57144d64932ad4edaa1a619c135cfbfc993bbfa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4940cfb76b69b556878c579c3491c1f9a4221722c4afce5e509358647ed38182`

```dockerfile
```

-	Layers:
	-	`sha256:1b8d88f19bb395c1257b1d2d02adadd9a2f3d61436407f852f9e9f4dbf20d914`  
		Last Modified: Wed, 15 Jan 2025 02:04:01 GMT  
		Size: 7.1 KB (7129 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c9dff46a695bbbd09928df43913acc08b77b33c6e5bbe3c67db3645450f3ec10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152620570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc5b403b395db45f384452fa3d991abd51cf8f7fcd540f565994f1ccb2e3791`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fca4ba78a63cac2994d6f3576656e907e3a130a20f935b6a1e2c945c9e7be3af`  
		Last Modified: Tue, 14 Jan 2025 01:38:04 GMT  
		Size: 52.2 MB (52151887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f2cddc488774629199c39c9010734d4be824e6ca934835a5e2d444a85e0075`  
		Last Modified: Tue, 14 Jan 2025 05:31:14 GMT  
		Size: 27.6 MB (27591847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97154d7b719fe3158c773c51a570d7d8ab1e54dcb04c12ce4e93476ca16bbefc`  
		Last Modified: Tue, 14 Jan 2025 09:43:30 GMT  
		Size: 72.9 MB (72876836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:de4a20ba75e03c0ff75c6080bd0eccad35fae0a9cdd8003b930a1c10359ba01f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7647309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7df2c6e85249573151aa8cd5130afefa5a2b540e14850e3ca08acd68a6e0cd2`

```dockerfile
```

-	Layers:
	-	`sha256:898d5118a17bda22e2ca116218625d18f3e8af744178649f307d32fa82a9375c`  
		Last Modified: Tue, 14 Jan 2025 09:43:28 GMT  
		Size: 7.6 MB (7639980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d5ea53d9432befce7809da77eac8d34ff51118b643a4b8fa31ef71e00df002d`  
		Last Modified: Tue, 14 Jan 2025 09:43:27 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:21b580e6d49c7e93d393cc4183b7953507a0d14a2c772cb813a045e6585ce821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.9 MB (138946644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa4fe23c7e5e0a9ff767ebb38c7e80622244bde6575d34e79b828167a5c05e51`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:41a19e48936e10f226b6bfe61097156b74f03101f788496e8860f0d4806f05ba`  
		Last Modified: Tue, 04 Feb 2025 01:38:33 GMT  
		Size: 47.0 MB (47040914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a706305f90a9f6f5a4662ef1063ca9b1d12e77b9f1482c3925294e4989eea2f`  
		Last Modified: Tue, 04 Feb 2025 04:38:37 GMT  
		Size: 25.4 MB (25411970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2279830c9cdcc3d6d50a4a0308903e5819e1f53fc61863f2bc9dae664a4b8e0e`  
		Last Modified: Tue, 04 Feb 2025 08:09:05 GMT  
		Size: 66.5 MB (66493760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:84d7869326707918f8017660abb61e07bf85545665587c47c75212b024d84ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7655227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f78cd334f922550d198aaced125697fe79820aa0e68451dc3687844c137eff`

```dockerfile
```

-	Layers:
	-	`sha256:69854c67014a55e3cbc0388c744d9f3bdef6b499bc255551489ddc567868be30`  
		Last Modified: Tue, 04 Feb 2025 08:08:56 GMT  
		Size: 7.6 MB (7647898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97e27ad8a4239ffd6edc6265d973c3ec43e3477ab76afac7cb1ee2b147937370`  
		Last Modified: Tue, 04 Feb 2025 08:08:55 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:24947995300edff9fe074d902dea0635e6d22ed2fd1937fa6508b0ec0c990968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144330742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdcab1fa96a7252e1d34e96a40a4923670646b93a75fa50937e7e7cbd46fe398`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1f48ea4a277664853f54eabe6340c7571241c845468906404bbb1efd60e69807`  
		Last Modified: Tue, 04 Feb 2025 01:38:18 GMT  
		Size: 48.6 MB (48560783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1f7d849459507f8a608795416d02b409e9f01c22159fa5acaf53ea0891b503`  
		Last Modified: Tue, 04 Feb 2025 07:31:13 GMT  
		Size: 27.2 MB (27214463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd8e9f79a90256c65272d5e3f7412b708597a6f16ea9693af76e4d17ce51d21`  
		Last Modified: Tue, 04 Feb 2025 11:36:07 GMT  
		Size: 68.6 MB (68555496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f2b1e81f1b440e5843aa24251b0b8923a99a1690c6dddfe027fb3ace5f939d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7672334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b609fc218e38ddd086dfc5bc64b9f12be4c636bbd78e05042313c048a7f24862`

```dockerfile
```

-	Layers:
	-	`sha256:e23016206115b86c9b36dd0ae2492aeb3ac7bef4a88beb722d8b794113fe07c3`  
		Last Modified: Tue, 04 Feb 2025 11:36:06 GMT  
		Size: 7.7 MB (7665038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b48b762e9223711dae7c7cdd1c675f03008477b830052c67c491f6c42f63dc4`  
		Last Modified: Tue, 04 Feb 2025 11:36:06 GMT  
		Size: 7.3 KB (7296 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:stable`

```console
$ docker pull buildpack-deps@sha256:d0377c0c511f692ccbcad47f8a26ebbe316394a989429bc4ff2736d05df4d53f
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
$ docker pull buildpack-deps@sha256:e7c6d07cb9b481de9609912bbb49dde977f6989d9a5abd1e58a877d25ee62baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.3 MB (348260383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28b23ee01d152ebfcf4c1687e2584877089ca3ab4550256ebe7e14df2e8a231`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 01:36:22 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b550be6cb62359a0f3a96bc0dc289f8b45d097eaad275887f163c6780b4108`  
		Last Modified: Tue, 04 Feb 2025 04:37:13 GMT  
		Size: 24.1 MB (24058355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35af2a7690f2b43e7237d1fae8e3f2350dfb25f3249e9cf65121866f9c56c772`  
		Last Modified: Tue, 04 Feb 2025 05:19:13 GMT  
		Size: 64.4 MB (64394292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7576b00d9bb10cc967bb5bdeeb3d5fa078ac8800e112aa03ed15ec199662d4f7`  
		Last Modified: Tue, 04 Feb 2025 06:14:28 GMT  
		Size: 211.3 MB (211328049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c4a3dacd4e6c66cf75566584dfa9afd045080a4f3cb7838d7b19bdf30386bd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15482039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9745f0d897e65d430c556d16a3c325def078d21a52bbb041e100967e95bcb9`

```dockerfile
```

-	Layers:
	-	`sha256:d4539b9f2e09894ecde147e82b09f847fc1cb06d936b130a9294f2544a903dd5`  
		Last Modified: Tue, 04 Feb 2025 06:14:25 GMT  
		Size: 15.5 MB (15471499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac139212500e131144b63fc9539d38787370de7cc310e05d7c357c0311687a7b`  
		Last Modified: Tue, 04 Feb 2025 06:14:24 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:a83883a22760febadd59a5f9dbcee3274ad8e29a3721729caff1d538b14169aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.4 MB (315359212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94bd2fc9911efe73bc7196ef0b6034a2b83caa039a8fb7b62851437cb9f1123c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8816181beac5d7674f87060fb5deb0c2c6221a62562265e16f54a617961cbc53`  
		Last Modified: Tue, 04 Feb 2025 01:38:08 GMT  
		Size: 46.0 MB (46006574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28060e71ea1173228ae8eefd6f5fb4296e8c1c73672a593f2d0d8e6e5483072`  
		Last Modified: Tue, 04 Feb 2025 08:03:04 GMT  
		Size: 22.7 MB (22733102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f77895e90931fefcb9b0f936aeec6e8c95f160c764c504ceb6084ffc29b46c`  
		Last Modified: Tue, 04 Feb 2025 10:20:41 GMT  
		Size: 62.0 MB (62003807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1293092f82d991d58072eac031a86360954b6f4021cae9377a435006dbe3bc7`  
		Last Modified: Tue, 04 Feb 2025 11:42:01 GMT  
		Size: 184.6 MB (184615729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dbf7f817719a28df7a5b0171007394ed210843d7eedd3e5f60dab9c54ea16a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15281025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4329461743dc38347b3338b873032c837143ab544d4d8b0cb96a7c18daec6f`

```dockerfile
```

-	Layers:
	-	`sha256:e768728e70f32ce146520e69c30ec9ced53352e7567637f487df05ce3d7d7129`  
		Last Modified: Tue, 04 Feb 2025 11:41:57 GMT  
		Size: 15.3 MB (15270417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9491464fec5e26fdf277d68ee891162483ab440c7fd77e5e08cfb03348e7798f`  
		Last Modified: Tue, 04 Feb 2025 11:41:57 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8a4104d2a65b6d8e78e51a418866c930b56abf606da4fc0d4cecfddc42f4fb27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.1 MB (301064875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36eea9faf1fdc9eefd8d490a1327060dcd31e80229cbcf72c8fbdfac33162515`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 01:34:58 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787291d61ca82895d27d086bfaf14ce01f401dfbf42f462addc8d1cae464ebab`  
		Last Modified: Tue, 14 Jan 2025 08:58:07 GMT  
		Size: 22.0 MB (21960077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6667f6e75dc8bed2e36123666ac457a4e0228141514ab32e65b9c6f6c7960e3`  
		Last Modified: Tue, 14 Jan 2025 16:15:27 GMT  
		Size: 59.6 MB (59640375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4144d45660bbc672e908993d8838af3ec9cece3a56e658f25257a0ce09e20da`  
		Last Modified: Tue, 14 Jan 2025 21:54:34 GMT  
		Size: 175.3 MB (175280214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8dacc3fe87894c577fce996d588fe02c9310c8d81e60e546f643b8bc38d24a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15286445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928b1fb5074c6e11dcf3aa6aa9b892b9e4899a9642c9a64608c3c2b3c292bc35`

```dockerfile
```

-	Layers:
	-	`sha256:ac1c5fb32c5d00a68aaed8067c4a6d22e1f011861220b7ec007edfc4b12d7d51`  
		Last Modified: Tue, 14 Jan 2025 21:54:30 GMT  
		Size: 15.3 MB (15275837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:566b21fe4e655c7bf8464e3b325fcd43af0615ec261408dd779beb45ecd60308`  
		Last Modified: Tue, 14 Jan 2025 21:54:29 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b407977518dbe09e422e0f4fd8f8a9f1343227cd6b752a8748d68f690f6f9603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.0 MB (338978548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c89001a18c0a49ab405cbc818fc07891ef0b4a0e257208d905d299593218681`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b85d68f8a4dce392d372c8a196863eac6d111c36b714179b4ab30e00c00d1`  
		Last Modified: Tue, 14 Jan 2025 06:59:53 GMT  
		Size: 23.6 MB (23598225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936252136b926e9bca27f4a5442f6a5d10c0ea4a23ca8b30c65de1bde666d082`  
		Last Modified: Tue, 14 Jan 2025 13:31:06 GMT  
		Size: 64.4 MB (64356433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c5996c7a64a4f64139ff9df6a590216c8143f5bb1f4c0f41874cf5336645c0`  
		Last Modified: Tue, 14 Jan 2025 17:08:21 GMT  
		Size: 202.7 MB (202716994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d476ca8de345ec5844dc135bc6aa7a9ecb1340f8030bf64ad8a895eaf60ccff1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15510590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2784f3887d0a4b7392bfac8b68c3113a8ca00a1b74b490ca7b5e68fdbbafc50`

```dockerfile
```

-	Layers:
	-	`sha256:63f64955d6e1f03115feb763d448c8fcf074438056bbbfb5f955c3c0d1a4aab7`  
		Last Modified: Tue, 14 Jan 2025 17:08:17 GMT  
		Size: 15.5 MB (15499958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13ac6ce4737d9a952ca57fff0a7a7477bd10b8dc774b705c47fd2768a5a0a036`  
		Last Modified: Tue, 14 Jan 2025 17:08:16 GMT  
		Size: 10.6 KB (10632 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:882a152f2e57fff2b4e424ea3fb6a7d5273b93066678dfd0bdb95b0efba857c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.8 MB (350837945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9097785ed06e1ce4239bd8a49450234addc5a2f2cae02b789c3f0c6688239e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d6abb78404200438eb560450e089a4e7707a23d5ec913df260500d902666670a`  
		Last Modified: Tue, 04 Feb 2025 01:36:35 GMT  
		Size: 49.5 MB (49457456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7d7e5b6420845d0479145c8a18a31030093be0de73e11194d97fee1ac58ef5`  
		Last Modified: Tue, 04 Feb 2025 04:23:48 GMT  
		Size: 24.9 MB (24899338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43394bbbaab482132a05c8eb702c9ebbbf5ecccd558ce05fdf40c651b7fbfa10`  
		Last Modified: Tue, 04 Feb 2025 05:15:47 GMT  
		Size: 66.2 MB (66236925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a443d7b60dbf868d9542c672117d7e30786e753c999878424f61b36b47cb37e5`  
		Last Modified: Tue, 04 Feb 2025 06:14:56 GMT  
		Size: 210.2 MB (210244226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e54a789932b9f341ad41a0f58003c64ea627a572cfb7c893198b963e0f60b687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15460601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb037878e3a2b9b326d57a9255d1516b726264d93cdf05e3e5072ecf804fcb2`

```dockerfile
```

-	Layers:
	-	`sha256:65c94f4e47cb5c1d276ce88454d05b51a88e1f8b6e58588a30fcf1e870c57f76`  
		Last Modified: Tue, 04 Feb 2025 06:14:51 GMT  
		Size: 15.5 MB (15450089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a66dedb1b7b06480192ffed582731683a156dc109dbe02f773f96c60f11a9a78`  
		Last Modified: Tue, 04 Feb 2025 06:14:50 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:860a2755ec0568a4dbe46314a2ae387e90fc9b53a78c8889c779740d34c4d802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.6 MB (325612422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5fc62c757f45c6730d1d46ad5a4473bea7a37b382fd92a8928e79be83348e25`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:12e528bcd428b4b8475a045cfdce724675384eedf195bad13ce8015853db632c`  
		Last Modified: Tue, 14 Jan 2025 01:34:57 GMT  
		Size: 48.8 MB (48758103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dede5b838e92cbab015cc8e31645fbe220ba02a56693e3a7a144e0a5428690`  
		Last Modified: Tue, 14 Jan 2025 18:10:17 GMT  
		Size: 23.7 MB (23652164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be7513211e793708951d273ea21ae802b4bdb4109f4b12ca6122e317851db90`  
		Last Modified: Wed, 15 Jan 2025 02:00:51 GMT  
		Size: 63.3 MB (63296729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac18012fc3c757a7df4cc601b819ea75556dd5814ec840b12642602c54fe799`  
		Last Modified: Wed, 15 Jan 2025 17:56:32 GMT  
		Size: 189.9 MB (189905426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:66e4f671ba1b7ad4b6b317db70aa590923f42d88d1b145d7b89d506f0e9400a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54cc4402e6b3fab15abe9933de571318dc91188f9d8875898b7d714a8855c230`

```dockerfile
```

-	Layers:
	-	`sha256:c1eb17e50044ba359ef545be178a5605253131cd4cc227f70c88c9d2f1b519d8`  
		Last Modified: Wed, 15 Jan 2025 17:56:14 GMT  
		Size: 10.4 KB (10382 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4725d4b50cc3768c2f7586e853992b6f03926dce68a3456661da6f08b1708622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.2 MB (362239370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c43ee817227a27216e0e75060a8916507939c6d366bfed2662922b4b750de8a8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:60b6379697eb1bdc0a74d6aa762f7f8e36a4a46031b019e2c7651c9723194c8b`  
		Last Modified: Tue, 14 Jan 2025 01:36:59 GMT  
		Size: 52.3 MB (52313137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b1d1b75ad07ec92cebf5f30e6612d80907cb5a7323fdef7921893e816a53be`  
		Last Modified: Tue, 14 Jan 2025 05:30:15 GMT  
		Size: 25.7 MB (25717439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395bc8910e96064c02227d340de0ac8d0234f64dd58802df0e9bd0891ad39050`  
		Last Modified: Tue, 14 Jan 2025 09:41:58 GMT  
		Size: 69.8 MB (69844490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb75d2bb90f133e31006cdf083f7a1330b114cb8a3fd0025be19bce4d4ee89b`  
		Last Modified: Tue, 14 Jan 2025 13:00:17 GMT  
		Size: 214.4 MB (214364304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:91b60ba7af97ff988d44396cd69ffddfaa27f52f86ba804fcb0094052e59b774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15458402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7756e08eb53066769aa73f8cb07a547ba51e203c0032cd5932fc75d44e7a1f1`

```dockerfile
```

-	Layers:
	-	`sha256:fcc9fa1d49ed25f5c3c5a80a6668f2ea892ecb027237cec560258091a270b425`  
		Last Modified: Tue, 14 Jan 2025 13:00:11 GMT  
		Size: 15.4 MB (15447824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfa234786e191f6aea3b5a8c4236319884b3c104e4aa16502da685b5eb83170b`  
		Last Modified: Tue, 14 Jan 2025 13:00:10 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:76f9eb07fd39ec3202f7a15b37d5429dd3b1edbfe4c32a914320944ae5cb8bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.0 MB (318046600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3034f78e5badb663e2f50b27003c6f5999b3bfb09a5a46525d9ba997700d930b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:21aa15808dc85b52fca40d40118565ddcd1b7ca60220d34328c38ccbc43c6ec1`  
		Last Modified: Tue, 14 Jan 2025 01:34:07 GMT  
		Size: 47.1 MB (47131782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba976031c967b4215afb8ec45dd7db082bb0d532971c83a1e9acaaa24c91981`  
		Last Modified: Tue, 14 Jan 2025 04:59:37 GMT  
		Size: 24.1 MB (24057754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41403619947915f481f99b2b28eecf7aa168ff32ff64e044d73a504ac7472026`  
		Last Modified: Tue, 14 Jan 2025 09:09:48 GMT  
		Size: 63.5 MB (63498283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a63cbd668c99b32baa3a88a9298c02c22ab49ca16b889143b19cca1ed34c77`  
		Last Modified: Tue, 14 Jan 2025 11:15:21 GMT  
		Size: 183.4 MB (183358781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2bf1e3ba440aebd60ca46d51930af97653389a33635121e8f5bd73830a43f75d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15294675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14bf32054c104be3d3381618b5c360e0db2d6b2c7490f0488d421a0cf7d7533`

```dockerfile
```

-	Layers:
	-	`sha256:04571792130603857f093b41ea98376a26344db408bc745b4c87eefd65975728`  
		Last Modified: Tue, 14 Jan 2025 11:15:19 GMT  
		Size: 15.3 MB (15284135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c70a1a5bc411f177e1b25fd6a73313087cf5dae458f60beb639d7f5a37e27e22`  
		Last Modified: Tue, 14 Jan 2025 11:15:18 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:824fc1fe5550ab28263cd089192b340a0231f7fc291b96431a5414055f240016
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
$ docker pull buildpack-deps@sha256:42d7b1aa9523c41d0706d716059774a5339ef9eff81732cd005cced66180810d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72538042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1456917498963d78260f6047d96e9ae5da337da973e2add039994a1c587c54`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 01:36:22 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b550be6cb62359a0f3a96bc0dc289f8b45d097eaad275887f163c6780b4108`  
		Last Modified: Tue, 04 Feb 2025 04:37:13 GMT  
		Size: 24.1 MB (24058355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5e12a83fe4a7cb4e76f6fcc87651f6f22f1a6731dc00a5220a624343bcc75376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4366473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a3df9f3102541c5a0f162a43e695ce533b0c1013e1f7cef3bf1b926c193625`

```dockerfile
```

-	Layers:
	-	`sha256:296acce62133a37d0eb516ee2e6522e9f01ff2e94ff39445b822447fe3075389`  
		Last Modified: Tue, 04 Feb 2025 04:37:13 GMT  
		Size: 4.4 MB (4359309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5a7db7c9a3b4f61541a7a348619b6fe822b816462b9a8d93898ea295f5cc4cf`  
		Last Modified: Tue, 04 Feb 2025 04:37:13 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e764456a3e6c6389335e0ff69bdace1d13c5b030d304243e1722290b471c286a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68739676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935f4abb4053724cc68a4354ed014db1217540a036a7a3be554253d0245f80b5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8816181beac5d7674f87060fb5deb0c2c6221a62562265e16f54a617961cbc53`  
		Last Modified: Tue, 04 Feb 2025 01:38:08 GMT  
		Size: 46.0 MB (46006574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28060e71ea1173228ae8eefd6f5fb4296e8c1c73672a593f2d0d8e6e5483072`  
		Last Modified: Tue, 04 Feb 2025 08:03:04 GMT  
		Size: 22.7 MB (22733102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e186710650f352511d1d5a8d92e82b4ab611675b2a2c1375576087c3ddccab51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4370057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7549865aecc31cfe80ffb5ae0b5f574d035521979b19941329b24f42049e4458`

```dockerfile
```

-	Layers:
	-	`sha256:a2a0e3ffc25240693dd5981e32252a6d46b6492deb1caf4f83d8df12945ab3ef`  
		Last Modified: Tue, 04 Feb 2025 08:03:04 GMT  
		Size: 4.4 MB (4362825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4285e68bcbab8f2e3fa5e86740901937dd15fa0a0ba0e735aae994683fcc1a03`  
		Last Modified: Tue, 04 Feb 2025 08:03:03 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5464a6c00bf3369df4e693237564ff47e99bdd69bedd99f741b52db54e54d73a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66144137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65bc793d549914afbf589b58b35f4dd5809625733da540c83cf4151be1bae929`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bf65c309bba1c843ac26792f2d942bca2d7bfcc7024ba331cdfbb762d7573e8a`  
		Last Modified: Tue, 04 Feb 2025 01:37:07 GMT  
		Size: 44.2 MB (44184052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dba4073c18c1d2882f0eb9a2b0d9bf057770ac1b8829e3e149a095273df800`  
		Last Modified: Tue, 04 Feb 2025 10:41:49 GMT  
		Size: 22.0 MB (21960085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:00aa2b046765f483b718594d34141d1f51f7fd20833bf7286ffa4b129556ece0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4368838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cb903435b396d5ad4513c37e475a0f08b129bf393393a9e2530643c7ac14bd7`

```dockerfile
```

-	Layers:
	-	`sha256:34bb158550658f03bcce8efa68c7969bc65c471a9e506cb28d798eec15a2076d`  
		Last Modified: Tue, 04 Feb 2025 10:41:48 GMT  
		Size: 4.4 MB (4361606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f66f515e983898730e103baf32e4c46a679bce32182fa75c84d83de2c26f414f`  
		Last Modified: Tue, 04 Feb 2025 10:41:48 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9a4473adf94868119cd23aba34822796765e1e9ca2940b49af9d2c4a69981be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71904981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea33a0aedad9c06ff0e0a5c609080c1e233bec6767c5bf71303b3517faf7bd12`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193c44006e77abbadfdd7be72b4ab6d7a5c08640ef575970f722b798ee7800ac`  
		Last Modified: Tue, 04 Feb 2025 09:00:06 GMT  
		Size: 23.6 MB (23598428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a4f6f6f87f04b8778fa5ec2ac9bd44ab8d4272d110e8ba102b99dc2e2f5eefce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4366838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e487cc9f27cd8a6885e25366917d0762a29ac694a53b4e83c7cdc71e66e323b`

```dockerfile
```

-	Layers:
	-	`sha256:93abb4f4a6447eac7f2ae14bcf7f21dccbf201596f3d540fef65c480fd0d530f`  
		Last Modified: Tue, 04 Feb 2025 09:00:06 GMT  
		Size: 4.4 MB (4359582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e44aa7ce5f133036d4aa1d5fca2e277494c35e7224859760bf9d33b7ae677652`  
		Last Modified: Tue, 04 Feb 2025 09:00:05 GMT  
		Size: 7.3 KB (7256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5ae5647ace04cdeb0d18fa92a5458b98739d5e1b6a4e84972df6d75f83e25f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74356794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69579a1de6ce4d9dc06535f0f3c4ae3e546e5af273b2bd63f1fcc6a8d2e2d5a4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d6abb78404200438eb560450e089a4e7707a23d5ec913df260500d902666670a`  
		Last Modified: Tue, 04 Feb 2025 01:36:35 GMT  
		Size: 49.5 MB (49457456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7d7e5b6420845d0479145c8a18a31030093be0de73e11194d97fee1ac58ef5`  
		Last Modified: Tue, 04 Feb 2025 04:23:48 GMT  
		Size: 24.9 MB (24899338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d76a6d719652aac549ba39a4834d8132fc60ef855aabe24f97e463e68ee6de4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4363503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ef9c8e03996088176ba3cc1763716840532982c3c319cd6ca66ba14404d3c3`

```dockerfile
```

-	Layers:
	-	`sha256:745272fbc1c3fc0422b6ee341b729acf588740860e6a4f1e48f81e7ddff3effc`  
		Last Modified: Tue, 04 Feb 2025 04:23:47 GMT  
		Size: 4.4 MB (4356366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d54d9627cb1d90d284779bac9fb37ec6014e715706131fbe1387006abffd9bd`  
		Last Modified: Tue, 04 Feb 2025 04:23:47 GMT  
		Size: 7.1 KB (7137 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:7e82a0704e62d860a1aedcddb8d8649f97cf31831f64bc7cca3b3b57d143e5c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72410267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b93d76303f85bbe0d4d9125b1ba100a20c6c695a5ed02a407481017ce52c3617`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:12e528bcd428b4b8475a045cfdce724675384eedf195bad13ce8015853db632c`  
		Last Modified: Tue, 14 Jan 2025 01:34:57 GMT  
		Size: 48.8 MB (48758103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dede5b838e92cbab015cc8e31645fbe220ba02a56693e3a7a144e0a5428690`  
		Last Modified: Tue, 14 Jan 2025 18:10:17 GMT  
		Size: 23.7 MB (23652164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:748b0707022a125c271b74edb18d3879dc9255eac8b1414f8c2ae6fd4c121716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 KB (7003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8762ff7a77a47447b52f9c5837805de7f8f22ee4d1be2cfde565f6d959f16523`

```dockerfile
```

-	Layers:
	-	`sha256:68a0baf3a618dcbd62663d3685d9fc7dbcc554f6503f61dc83b86d7a287f8558`  
		Last Modified: Tue, 14 Jan 2025 18:10:15 GMT  
		Size: 7.0 KB (7003 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1e45989e97eaefa92658fd519fe2bae68cf9b053f0ab1b4f97d2735d21aba44c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78030525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0f70646e162cc979805350ac13127a566de8fb22c660b84d7bbd3faa2f3a5e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d32dc8295067a6f744a1fca9cfffe021a324e651f2834ad7b587e0380c3f2981`  
		Last Modified: Tue, 04 Feb 2025 01:37:34 GMT  
		Size: 52.3 MB (52312857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f161b1ac6fcd1e84495441a30458604c921f0c00816d0cd0926964e56d9717`  
		Last Modified: Tue, 04 Feb 2025 07:24:32 GMT  
		Size: 25.7 MB (25717668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c2a7f7c65904bc8dbcef3f3674f9caa66ce22f118b10c07c5675c7bc71d3047c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4371005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b9b8c3614fab2c939b24f0810da2c3fa1417067587c3105ac1f38654dd8c69`

```dockerfile
```

-	Layers:
	-	`sha256:65fc8bdcff2c2f6b97523146ca1a93865fa69badfea9f63fe7fe97f682f0b786`  
		Last Modified: Tue, 04 Feb 2025 07:24:32 GMT  
		Size: 4.4 MB (4363803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a2d971f0014ca2a549954a195e82af206f6943ced95309a2c4f0a7537e5c7d2`  
		Last Modified: Tue, 04 Feb 2025 07:24:31 GMT  
		Size: 7.2 KB (7202 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b2a040f9b5018f30ff73eeec1b0fe2f17a7c4929c613c58f2b112dbcc04b56e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71189070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6395dd5d74061c3b3bb036f052a372a32e9397377bb49e680986df2988310a3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:92bc3bb38690fde96c4bb788f15f365b04d4cb8ab9368675dc9294bc24a9c7b6`  
		Last Modified: Tue, 04 Feb 2025 01:37:03 GMT  
		Size: 47.1 MB (47131492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe7257ceffda4bd6219bda9d63efd9f5fc932de95d2f5db69f3d95df88e73b0`  
		Last Modified: Tue, 04 Feb 2025 07:30:08 GMT  
		Size: 24.1 MB (24057578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1cd79d9353a8a124773d7df05bae9236f4c1332118a1326552145122efe1b76e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4366169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a06dc43215ca62307e19d496fb94d3cdbb3d051126d2acbe246a73e1c75a1ff`

```dockerfile
```

-	Layers:
	-	`sha256:c5153387a5e1a2df7538970109cebfccd70cb85fd9c58daf5aad24f956ff7702`  
		Last Modified: Tue, 04 Feb 2025 07:30:08 GMT  
		Size: 4.4 MB (4359005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d92a83e28f3acadfd1ec9397c65d21dea67b1ad648ce759c72010c142c2c10c`  
		Last Modified: Tue, 04 Feb 2025 07:30:08 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:stable-scm`

```console
$ docker pull buildpack-deps@sha256:b8921eb6d9c99f9c2bf37f929be3c7a74c50a58149662f72b4dfd90591547e5a
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
$ docker pull buildpack-deps@sha256:107b7c021186efe3ed164cfea1c3d06c8ed6b8ce4582f691ff74a2dc4901a562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136932334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc6260661cca62da45094b3d5d01eb10b3ae352ca934691651dd8543956046a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 01:36:22 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b550be6cb62359a0f3a96bc0dc289f8b45d097eaad275887f163c6780b4108`  
		Last Modified: Tue, 04 Feb 2025 04:37:13 GMT  
		Size: 24.1 MB (24058355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35af2a7690f2b43e7237d1fae8e3f2350dfb25f3249e9cf65121866f9c56c772`  
		Last Modified: Tue, 04 Feb 2025 05:19:13 GMT  
		Size: 64.4 MB (64394292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c45671abb650eed88ec7038f7152842ad8d557322d1c488be20f05be096cb46c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7760401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e2a1f4e1a96a61d654b4ceb41ea6775eaade5e6d735639e5bbea80e9f6294dd`

```dockerfile
```

-	Layers:
	-	`sha256:b87149b2f1486609a2af0770d2c2c37d036fd5e551b650c92f01ea43a97e54c9`  
		Last Modified: Tue, 04 Feb 2025 05:19:11 GMT  
		Size: 7.8 MB (7752746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16de0d9ec26360b8605a9e23ae24c8fa01bba49c7df7a2c647e0c7c43e7a807b`  
		Last Modified: Tue, 04 Feb 2025 05:19:10 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4485452def37f53d9fea2e251dce6eec0c7a015f96823123284127e52bd259de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130743483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4bd79e1728ba3eb164b6a77dc3f9b0cd9778a70d2143f9d9af57d9e10a42a0d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8816181beac5d7674f87060fb5deb0c2c6221a62562265e16f54a617961cbc53`  
		Last Modified: Tue, 04 Feb 2025 01:38:08 GMT  
		Size: 46.0 MB (46006574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28060e71ea1173228ae8eefd6f5fb4296e8c1c73672a593f2d0d8e6e5483072`  
		Last Modified: Tue, 04 Feb 2025 08:03:04 GMT  
		Size: 22.7 MB (22733102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f77895e90931fefcb9b0f936aeec6e8c95f160c764c504ceb6084ffc29b46c`  
		Last Modified: Tue, 04 Feb 2025 10:20:41 GMT  
		Size: 62.0 MB (62003807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9325e1f31ac79d5ec224fd4a72d88769f24ae26a8b0657571c7ed3ab028f0b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7762027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78cbcdcc4c7120567403bfd7323fcb4c9cfc1f4ad85dd84655b4106038f895e1`

```dockerfile
```

-	Layers:
	-	`sha256:787a1a81ca68983478e9b85146549b7060b5bda7b817fb5fa748e29968505496`  
		Last Modified: Tue, 04 Feb 2025 10:20:40 GMT  
		Size: 7.8 MB (7754304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9ae5dbc955356ce8d85cb9395d5a07e003732510094b71b218d7c7f691b41fb`  
		Last Modified: Tue, 04 Feb 2025 10:20:39 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:49e4ccaedbca671c339d8a55242d7f25e1af167a096aca68b56da8a26e979622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125784661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5d6202e1e5273856a4827dd5f9a1aaf9c5c9df9e95e406f72acc587373ce0c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 01:34:58 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787291d61ca82895d27d086bfaf14ce01f401dfbf42f462addc8d1cae464ebab`  
		Last Modified: Tue, 14 Jan 2025 08:58:07 GMT  
		Size: 22.0 MB (21960077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6667f6e75dc8bed2e36123666ac457a4e0228141514ab32e65b9c6f6c7960e3`  
		Last Modified: Tue, 14 Jan 2025 16:15:27 GMT  
		Size: 59.6 MB (59640375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f893443c0cff99fae6cfd9ee2d82f7d9fa1764c42e4b44d6bd02b54a5f8860e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7761753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71830b5b97fe489d694c4fdd593c37b208f010a9b30f5fbbd200b1d5bb8f78f0`

```dockerfile
```

-	Layers:
	-	`sha256:ed0713d12be1303423be5246de90d43ee0ccba8f617f41d991598bef4a257e57`  
		Last Modified: Tue, 14 Jan 2025 16:15:26 GMT  
		Size: 7.8 MB (7754031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dab6ec41bbe5e21c735259ad96692c0dc9cc772b9c0cf51e02e186b1620bc8af`  
		Last Modified: Tue, 14 Jan 2025 16:15:25 GMT  
		Size: 7.7 KB (7722 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3d3e7297c13b3097bf5fb9991ffa9aad0816798a907a8fff792165491174b39a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136261554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413ebeaa354b3c0feb020579c81777bbfe6e0b44434cbb51e0423a9a5e072539`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b85d68f8a4dce392d372c8a196863eac6d111c36b714179b4ab30e00c00d1`  
		Last Modified: Tue, 14 Jan 2025 06:59:53 GMT  
		Size: 23.6 MB (23598225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936252136b926e9bca27f4a5442f6a5d10c0ea4a23ca8b30c65de1bde666d082`  
		Last Modified: Tue, 14 Jan 2025 13:31:06 GMT  
		Size: 64.4 MB (64356433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e54b58bc89d63d6cb7a969a37a81bd05045e92b0531f2dea017d34389f50b348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7766898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cfdf225184ecb259a96744ec5072a8b6321e328e75488d08232ee1c90c8287a`

```dockerfile
```

-	Layers:
	-	`sha256:ee5a579a1304a0cd9ab66a341c82f90bd0673cbb06d2d921649dc6204d1298a5`  
		Last Modified: Tue, 14 Jan 2025 13:31:04 GMT  
		Size: 7.8 MB (7759151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4b7039d4910144475f784c47b0f938b47a0c5c3de6783cc5280520c1dea87bc`  
		Last Modified: Tue, 14 Jan 2025 13:31:03 GMT  
		Size: 7.7 KB (7747 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d1e072586740069d1b5e9086fdcd828de918bfb913d5055e1aaa194f62dcc265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140593719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29f7944ff637b8f0ba1c24926e7d9ef677ee299088eb49272b3ed9d4d155cfb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d6abb78404200438eb560450e089a4e7707a23d5ec913df260500d902666670a`  
		Last Modified: Tue, 04 Feb 2025 01:36:35 GMT  
		Size: 49.5 MB (49457456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7d7e5b6420845d0479145c8a18a31030093be0de73e11194d97fee1ac58ef5`  
		Last Modified: Tue, 04 Feb 2025 04:23:48 GMT  
		Size: 24.9 MB (24899338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43394bbbaab482132a05c8eb702c9ebbbf5ecccd558ce05fdf40c651b7fbfa10`  
		Last Modified: Tue, 04 Feb 2025 05:15:47 GMT  
		Size: 66.2 MB (66236925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9a8c7b49ce3106d816ea038fd374c442087a4e89e2fc93a79ec4684633bac082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7756451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d5b2ac5fd703de6ab1eddd79d25bbe48d83b138aa053a7a88e51177e6a976fd`

```dockerfile
```

-	Layers:
	-	`sha256:9d2a829989dc2c4ace1d5075358dc1cf0e96b3108c0e3b1e30669aa7592e69c9`  
		Last Modified: Tue, 04 Feb 2025 05:15:46 GMT  
		Size: 7.7 MB (7748823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d51ba6d7dd98693c417109d9f16fa8a019ed6cf65c04b4b463211d4e1d1ea1b9`  
		Last Modified: Tue, 04 Feb 2025 05:15:45 GMT  
		Size: 7.6 KB (7628 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:fe602d939df4cbddd8102a3ecbfbd2b79407c0d8a77a3c3a8b61111134ca7a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135706996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c87c17f18e534fcf9eaa672e16e2832528995e9e5780ff4c8964ebef619f07`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:12e528bcd428b4b8475a045cfdce724675384eedf195bad13ce8015853db632c`  
		Last Modified: Tue, 14 Jan 2025 01:34:57 GMT  
		Size: 48.8 MB (48758103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60dede5b838e92cbab015cc8e31645fbe220ba02a56693e3a7a144e0a5428690`  
		Last Modified: Tue, 14 Jan 2025 18:10:17 GMT  
		Size: 23.7 MB (23652164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be7513211e793708951d273ea21ae802b4bdb4109f4b12ca6122e317851db90`  
		Last Modified: Wed, 15 Jan 2025 02:00:51 GMT  
		Size: 63.3 MB (63296729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:63f9dd3ac1b3f3fb150b43d7ee5d7172d3f9881b5149b99d19d50bfb75821e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:328981011361d0b51ce891a6cbbdd73023d076afad56601a031dafc25d1c316d`

```dockerfile
```

-	Layers:
	-	`sha256:ea2b61c81e84d989128047eb14c01db001abea44f3d40a2da08f942d63cb38cd`  
		Last Modified: Wed, 15 Jan 2025 02:00:45 GMT  
		Size: 7.5 KB (7497 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:05b4402223200277f406f99fc728e47988998b5946ff282b1a2f2b55db8967f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147875066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07253a39195775999a73cfa312e0fa0c5fa1cb97359e3cf5503e14f02d7368a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:60b6379697eb1bdc0a74d6aa762f7f8e36a4a46031b019e2c7651c9723194c8b`  
		Last Modified: Tue, 14 Jan 2025 01:36:59 GMT  
		Size: 52.3 MB (52313137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b1d1b75ad07ec92cebf5f30e6612d80907cb5a7323fdef7921893e816a53be`  
		Last Modified: Tue, 14 Jan 2025 05:30:15 GMT  
		Size: 25.7 MB (25717439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395bc8910e96064c02227d340de0ac8d0234f64dd58802df0e9bd0891ad39050`  
		Last Modified: Tue, 14 Jan 2025 09:41:58 GMT  
		Size: 69.8 MB (69844490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a9d572ddeddf65e9c94b552da6a41ddb37bb717818328f59458a028ff53349cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7768145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee4e94cc9d33bf313cfc300eb9c016f08f8e9c4621491174b10461db746fb4d`

```dockerfile
```

-	Layers:
	-	`sha256:231c3fce7984cd3e3de5dd5d140d65478f0236395546611c454b0e0421150d73`  
		Last Modified: Tue, 14 Jan 2025 09:41:56 GMT  
		Size: 7.8 MB (7760453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b75b5ea659daa8cc266903efd448b1e7d046a092e5d48598c2331e3ca388f11a`  
		Last Modified: Tue, 14 Jan 2025 09:41:56 GMT  
		Size: 7.7 KB (7692 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5261ec0a644e8aaf0410d07b3f6775921eb9dfd59122eb9155529fc4dd8e12d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134688525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67a46e44795d80467cac123f20812bc46798d0bebc2ca9b6c72285a776183381`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:92bc3bb38690fde96c4bb788f15f365b04d4cb8ab9368675dc9294bc24a9c7b6`  
		Last Modified: Tue, 04 Feb 2025 01:37:03 GMT  
		Size: 47.1 MB (47131492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe7257ceffda4bd6219bda9d63efd9f5fc932de95d2f5db69f3d95df88e73b0`  
		Last Modified: Tue, 04 Feb 2025 07:30:08 GMT  
		Size: 24.1 MB (24057578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800fd1d6411dfa44ccdbe5db47bb7e970909c1a08d63328dfd165607beb67e7c`  
		Last Modified: Tue, 04 Feb 2025 11:34:34 GMT  
		Size: 63.5 MB (63499455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c2ca21cdc0403c9f431731aa97d0c4db85a946a2bacf211d0cfe3ee4e5418bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7759606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5459c93da646c41b36d9e5eeee87162119e171e15ef61c37b7f488c907ac80`

```dockerfile
```

-	Layers:
	-	`sha256:e5d1da80e53060d3414c9fee17945ae782d9600f01876fe0136f6c4d962f8be8`  
		Last Modified: Tue, 04 Feb 2025 11:34:33 GMT  
		Size: 7.8 MB (7751951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd51d33d5be0950a97f8ce96f83c03da82e3ff767c4f51b3c48d301197f978df`  
		Last Modified: Tue, 04 Feb 2025 11:34:33 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:88ea32c91e0088d334eee5839f76c663b0ece625a514c1ac24671005d47a308c
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
$ docker pull buildpack-deps@sha256:3862089c116e698ae8dcb267ff2dc3e41c7668bca19245d85626aeb69633bca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.3 MB (380342321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2042c40c5e97e9fded6f02ba0fd360931322d9bf5c9ba337effd0c197bb0f32`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:af4da4e2d364845ad19d8dada5d782436e7eefced1b551d8d6a613212d528000`  
		Last Modified: Tue, 04 Feb 2025 01:36:46 GMT  
		Size: 48.3 MB (48348905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1be2f67d683c399ce2229317b243539533edd5a34194175f614d9715ed155d`  
		Last Modified: Tue, 04 Feb 2025 04:37:54 GMT  
		Size: 26.0 MB (26038437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbda3f387ceab9c039dbe56e4c3555afaa795a6af95ca16374c71c1ceb40cd0`  
		Last Modified: Tue, 04 Feb 2025 05:20:47 GMT  
		Size: 67.5 MB (67467177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae05f536b0d5759ee824999756f5a55c1d4da8e35f66232cdfb6e42c5597bf7`  
		Last Modified: Tue, 04 Feb 2025 06:14:35 GMT  
		Size: 238.5 MB (238487802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5caf0ca48f5b68c01faa5d43e0744d3c9c6d7d530d19ff1468abed1fb8efcb17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16942937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b93fae4b0c13aa929b3de4e93e14455f02715975a7a9236bd9591bacb55e9e3`

```dockerfile
```

-	Layers:
	-	`sha256:afe3d7666554427076557c02f44cc7f668d341a34bd1ce4509f6352aeb88dbcd`  
		Last Modified: Tue, 04 Feb 2025 06:14:30 GMT  
		Size: 16.9 MB (16932744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a32a2743c857eb71e17a15d25c030656a2e839841377b829f90cc40b5244accc`  
		Last Modified: Tue, 04 Feb 2025 06:14:29 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ba095bb649386b16b9fc040a78d3178a0517fca394dcd6a794ac9edc2ed63c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.7 MB (345661913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c45ea7e4b70bf69715291cdd7917f482d0acfa53e0ac45ba3034532d2360631a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:65c8e105f1e96f93defe25039ead5b48a9870e86175b80348bfd23ae3445cf2f`  
		Last Modified: Tue, 04 Feb 2025 01:40:53 GMT  
		Size: 46.5 MB (46502404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e17e53e6ecbca4d6fed6a359edf4419edd97930a581be4b6ad999669de4cdfc`  
		Last Modified: Tue, 04 Feb 2025 08:04:29 GMT  
		Size: 24.7 MB (24743168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17d90b594a7d89931d5de1b198b2dc07a97b965a1b004c4da3948056c117a8d`  
		Last Modified: Tue, 04 Feb 2025 10:23:00 GMT  
		Size: 65.1 MB (65103555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d054220a6a95da9f3d586a2f3758d12b834db5f03df5446b2303636b5e04ce3a`  
		Last Modified: Tue, 04 Feb 2025 11:48:13 GMT  
		Size: 209.3 MB (209312786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:421e412642e50cc48434133d8fc62f191432878ad160c9067bad7a3999f6eca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16712372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617465c67c203784a67272318700e60f7d05912337ea5b12e0c42892846c4a81`

```dockerfile
```

-	Layers:
	-	`sha256:43cb58f621a1a135d73938e960d782544b1e1f86a646f1457e362731c292633d`  
		Last Modified: Tue, 04 Feb 2025 11:48:08 GMT  
		Size: 16.7 MB (16702119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:041297f6ef05786d56a6380863e85430c242c49e3901190b100bd6269cae8f43`  
		Last Modified: Tue, 04 Feb 2025 11:48:07 GMT  
		Size: 10.3 KB (10253 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:da6d5652822bbc0c3bcd4b1eff1dca2f76d1b48d397e547616f82d9638477e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.9 MB (323923481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b323295859897e21b08b6202c32b50b7dd25c1b6061ba4a47ba1a4430b263824`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:105ec2fcec8ae42e2b6cba4c3c8463bdd5ad21cffe232e9cfd7ed127e7ede3fa`  
		Last Modified: Tue, 14 Jan 2025 01:39:08 GMT  
		Size: 44.6 MB (44580459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881cf44810c526c17319a679eee937276e08c6767dabc96ffa22308bd53f7e1e`  
		Last Modified: Tue, 14 Jan 2025 09:00:07 GMT  
		Size: 23.8 MB (23806747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c787837970fa306cc5256b55f5173664552e3e16eb197389ac0c21aca92a24`  
		Last Modified: Tue, 14 Jan 2025 16:18:41 GMT  
		Size: 61.9 MB (61894400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9300ff4f70721ff1e9737e80c1a1eaa49b83fa08a552177c95c775ed44606a84`  
		Last Modified: Tue, 14 Jan 2025 22:01:42 GMT  
		Size: 193.6 MB (193641875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ef0530b783e5de869f817fd642dfb1caef42ac28d62ce6e28fdb91a456ea0c14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16671715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a75c8344b5fafc11d176ae43785d83e5059676edb9609011e2396efdb61abdb`

```dockerfile
```

-	Layers:
	-	`sha256:d25c91edb4beddef9af8441097837eeb335ad8933a5e6625886cf33db46cfcfc`  
		Last Modified: Tue, 14 Jan 2025 22:01:38 GMT  
		Size: 16.7 MB (16661463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad274817363339e07ad186527b366b93e96d7c027a00944b37f01ea200af71ff`  
		Last Modified: Tue, 14 Jan 2025 22:01:37 GMT  
		Size: 10.3 KB (10252 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2a64b528a91b982ca51b72ba47a808f07b867469d5da3954dc0a664f09f5b666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.2 MB (368167662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c41f5d3261ad99085f5e16f4d0a6ea0ee11050b3a28df955008125a52b7e3761`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:53cf00e5414c63ec005c43ad8342c8e55028d137e29e95d889d4247b0586d248`  
		Last Modified: Tue, 14 Jan 2025 01:38:51 GMT  
		Size: 48.7 MB (48661509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6216ff9e1bca52cad6d9119375ff8a9fe28c8b52c130d5380d5ded38210e688e`  
		Last Modified: Tue, 14 Jan 2025 07:01:19 GMT  
		Size: 25.4 MB (25426483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab5443d60c3808485433bb956012bfe58b69cebf352b638a921b47918c7b109`  
		Last Modified: Tue, 14 Jan 2025 13:33:15 GMT  
		Size: 67.1 MB (67101726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f57a614701f3245516a9cf7adb78fd0830fd5bea39e42e511c29cd73c44a41`  
		Last Modified: Tue, 14 Jan 2025 17:14:04 GMT  
		Size: 227.0 MB (226977944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f3c7d09cfe30fefb345323728b6556604e927d8c2a7201ccb407f5e42cad7208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16990040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb21a81412050be940a80a673b2d3dcb80be439fa563479e47b233929afbed70`

```dockerfile
```

-	Layers:
	-	`sha256:02eb0397b03f384d9a6d137f8060b59de6798f4277e6b7155091f20d26610ac0`  
		Last Modified: Tue, 14 Jan 2025 17:13:59 GMT  
		Size: 17.0 MB (16979767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc21006030d24c01acbe412539fa49a96ffd74930fd6fc2d23963e3bbc70eb9c`  
		Last Modified: Tue, 14 Jan 2025 17:13:58 GMT  
		Size: 10.3 KB (10273 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e143a351e131ff3e73d70f7435bfa3afceffe3d7df01784f838814d1d1a22aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.2 MB (389172398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09603d66d8ec957adc1b43b9cc1a42625aef0dfedc65c9533abdf747c9141153`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f6eab4c65eb241da9efbcd7f3af754621262244b11cdb15579a1ffe95621258b`  
		Last Modified: Tue, 04 Feb 2025 01:36:50 GMT  
		Size: 49.8 MB (49751669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f716b567c64e0e309015fd1a02f5a6cc44d9337e2d33b9f6b8078b32a497ea27`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 27.2 MB (27187291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4913bde8dd9201a45eb15eecac64dfe0033ec3938f3fffc5d62cb37095ca1ed5`  
		Last Modified: Tue, 04 Feb 2025 05:15:41 GMT  
		Size: 69.4 MB (69401603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afd1cfae6f514571d7f4226e482cdb485486ee849f4136f31c735d85704d269`  
		Last Modified: Tue, 04 Feb 2025 06:15:04 GMT  
		Size: 242.8 MB (242831835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dce6938c7089bbd10bf7f15ec6c70c8590e4f0498d62027fba33c63771e6fc3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16911735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abcdfa41e35edc5ae7563ebd6b4c808c7999d33caa3e08bf8dea4a6f197a618`

```dockerfile
```

-	Layers:
	-	`sha256:449f4108f7c12ed2ef005b79ca305e1fe108b45a0283ee92ce7581a0c26d787b`  
		Last Modified: Tue, 04 Feb 2025 06:14:59 GMT  
		Size: 16.9 MB (16901564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e08c7332c054a21ab001deb52f099531010f779b1a5b83889e1511ae98b65494`  
		Last Modified: Tue, 04 Feb 2025 06:14:59 GMT  
		Size: 10.2 KB (10171 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:aa5fa8fee1a908124ae3adc565543dfbc931cd430a4c68f7ad938fbcee2333fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.5 MB (354487822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af426ea9e9fe6cb17eb21147c060df9727d22c4a02f6d69ce356aad9242482b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7fc12d8a734ed45514ae5135503d718e9ff7693017677de649ab963638a639fe`  
		Last Modified: Tue, 14 Jan 2025 01:37:16 GMT  
		Size: 48.4 MB (48390219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0115509fb5cc85eda38403b37d75aa0d68bc08deb77a8f9d926a1f8c06d921c`  
		Last Modified: Tue, 14 Jan 2025 18:14:22 GMT  
		Size: 25.9 MB (25926715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ed8eab45779c4caaf48a3dd1f3e53c5b4079b75e32b657bac3bdc07a0f1e4b`  
		Last Modified: Wed, 15 Jan 2025 02:07:24 GMT  
		Size: 66.0 MB (65977015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dad556c93c7fbd44bd1df34a958ab27627b99c3df6076447109ea0903c46714`  
		Last Modified: Wed, 15 Jan 2025 18:16:26 GMT  
		Size: 214.2 MB (214193873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6353c960241b82e055e52d6a26b7606c8831cf880e464ed1d6255d758d19c3a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c5a82460cab0b82fc4e9188547d910028f8cab28c7d7bbee19dc3cd407f793`

```dockerfile
```

-	Layers:
	-	`sha256:4569235f2213d7cddb66a73d7068690a1abbeb777a4852b2697d7d207f52d8fe`  
		Last Modified: Wed, 15 Jan 2025 18:16:07 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e7ad1938d3920ab76b97cdb0269dc3e146e5e6df9228703a73d312deea2b970d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.5 MB (384517027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8fe2d0729ff9734c1cfabfd95b52648072a577e4cb67905bada67aaa788152f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:826e70a2bdfac0f05c49b7611afcf30a311c862a1beca6fc4059e4b6cd0e1a4a`  
		Last Modified: Tue, 14 Jan 2025 01:40:51 GMT  
		Size: 52.0 MB (52043133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f126b14e556a94eaec41c5a29f9164224f92b1080c74dca2491c3f7b9120c320`  
		Last Modified: Tue, 14 Jan 2025 05:32:11 GMT  
		Size: 27.5 MB (27531238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7311c304e2cd2735e9d0f4a75554811f3be94be0d57e4fd8ff5989c485af8c30`  
		Last Modified: Tue, 14 Jan 2025 09:44:47 GMT  
		Size: 72.5 MB (72524387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c13c3f363d5cb80dd126d46dc749469f09c6bcf87873368d4910edf4c8fab0`  
		Last Modified: Tue, 14 Jan 2025 13:08:14 GMT  
		Size: 232.4 MB (232418269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b272982f72f68b67efc7c6a61a563586c1ca471dac11804f4ebea07fa02c30bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16893502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d9551896361669f19dca1b2f2bfc5f14df31a73639e98be441623b4ab72783`

```dockerfile
```

-	Layers:
	-	`sha256:d0cebc80f7ba1e831ad0fd69b4cdb1a684550f85676baa46a01a0369228a2278`  
		Last Modified: Tue, 14 Jan 2025 13:08:11 GMT  
		Size: 16.9 MB (16883277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8973654c9bf96e1c45cbe69e6de6aac1822ccbd7a68456b5b54d6b1a3e3b206`  
		Last Modified: Tue, 14 Jan 2025 13:08:08 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c269b72c35b95814f21ceffb69ec1624b4531d8b4e87ab81af3ebfe16b455a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.1 MB (350086446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd137b601fa29b6959f2bf38bf9a5799d3bb6d994f910d052acbb470373194d3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a96882092e58b6b0f460c25e0b3fa57215487e6282387621e5c4dd2314637493`  
		Last Modified: Tue, 14 Jan 2025 01:38:54 GMT  
		Size: 48.3 MB (48329740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c639414a48a5e91286e442a3c2a376c94650966c4fede85d34f85e98bf430e8`  
		Last Modified: Tue, 14 Jan 2025 05:01:37 GMT  
		Size: 27.1 MB (27131328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a0617227e41b6c45ea475d62d65ee6e02048cb238dcbfd9f884635a3d44568`  
		Last Modified: Tue, 14 Jan 2025 09:12:11 GMT  
		Size: 68.2 MB (68150739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10418c2ff73fdb0d646523d4f04c8033e632051fd913baf1a7613485f088ba63`  
		Last Modified: Tue, 14 Jan 2025 11:20:04 GMT  
		Size: 206.5 MB (206474639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:80aae46b3af426dfe933e73c3da2bbc571f3155ad4fe717d4b07aa2dd9e41901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16687094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c455383ad764fc23d63f45994189401ea53025b6068ce94683f5defbe2125b`

```dockerfile
```

-	Layers:
	-	`sha256:dd52e57c85451a22dead751eaa430c4c6b1931235c8b39a3e7252e0700730938`  
		Last Modified: Tue, 14 Jan 2025 11:20:00 GMT  
		Size: 16.7 MB (16676901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f01ba2d6246ad25bd5819324375382448632dfb6c3c500a62dd94402529f9ffa`  
		Last Modified: Tue, 14 Jan 2025 11:19:59 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:b679578e99e891ce38c452a7e625eecc65caa06c50086f730a2eb1c2a4613a74
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
$ docker pull buildpack-deps@sha256:aee25dd8533c4987c4174b90b38c111bafbbcb7d62625571ed88e06c5d103e1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74387342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa1ba49db818dc17b8375378ca48a72a856869186b91b7cc1bc25cf591349ed9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:af4da4e2d364845ad19d8dada5d782436e7eefced1b551d8d6a613212d528000`  
		Last Modified: Tue, 04 Feb 2025 01:36:46 GMT  
		Size: 48.3 MB (48348905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1be2f67d683c399ce2229317b243539533edd5a34194175f614d9715ed155d`  
		Last Modified: Tue, 04 Feb 2025 04:37:54 GMT  
		Size: 26.0 MB (26038437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:13051b3a62affdef39f0b11959ab2f3e5be76cc4dbb01d84f0882ebae8ebe7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4048111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b6b5b4470cf325c65245a4121edda03884ee9dd31ca16a14c891cf36080c7cd`

```dockerfile
```

-	Layers:
	-	`sha256:baf1bd4a8e8ca39f8474004a7082c2789d2157ac1f6784ca6dd790f2c10e2726`  
		Last Modified: Tue, 04 Feb 2025 04:37:53 GMT  
		Size: 4.0 MB (4041291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77f014b0fdbc84aaa05d094e879a3865d8ff0c20f33326bde23301a0f144e7dd`  
		Last Modified: Tue, 04 Feb 2025 04:37:53 GMT  
		Size: 6.8 KB (6820 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c8b72309a00c55121660036dc53fc7a55227dd584a370f77d25f8d06e544c915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71245572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c5897d4a1b1f8a5acad55b61b1aac3c28340525f575546f22605ce71a4b008`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:65c8e105f1e96f93defe25039ead5b48a9870e86175b80348bfd23ae3445cf2f`  
		Last Modified: Tue, 04 Feb 2025 01:40:53 GMT  
		Size: 46.5 MB (46502404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e17e53e6ecbca4d6fed6a359edf4419edd97930a581be4b6ad999669de4cdfc`  
		Last Modified: Tue, 04 Feb 2025 08:04:29 GMT  
		Size: 24.7 MB (24743168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e3c37ea07ec604ed597239c3e420144e4445ac99f8ebe34ec8d721c622caa657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4055799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95d254ad2a5dead6eb395b06930bd6dd081a28e79a3adf074ed155d8dc59799`

```dockerfile
```

-	Layers:
	-	`sha256:008cc661fa77c12a00af319e8adc81a6ad24da66847717769b4f90b93b6dc8e8`  
		Last Modified: Tue, 04 Feb 2025 08:04:29 GMT  
		Size: 4.0 MB (4048918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:438f772e281905bb522f01575f7ec1286452b5b73198927e065d129b4448a0b9`  
		Last Modified: Tue, 04 Feb 2025 08:04:28 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0a6c357b2a5550465bbb58c8cb50f1b528f6e0b3bcb2cc03e8e4699e5cbbe01b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68387206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1403e33a3f014b9f3a79bfd150de00b1bcd52579b0635858ef7266499b6c4d08`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:105ec2fcec8ae42e2b6cba4c3c8463bdd5ad21cffe232e9cfd7ed127e7ede3fa`  
		Last Modified: Tue, 14 Jan 2025 01:39:08 GMT  
		Size: 44.6 MB (44580459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881cf44810c526c17319a679eee937276e08c6767dabc96ffa22308bd53f7e1e`  
		Last Modified: Tue, 14 Jan 2025 09:00:07 GMT  
		Size: 23.8 MB (23806747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:816e5ecae2afe97b2716b2fd5e97c09a92fa84b86e4724086e7bf7abc1da653b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4037015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:416f156bb04b0ec4ba73c579a5ada9b1d5888217d9012f51892ef6cbdbbe423b`

```dockerfile
```

-	Layers:
	-	`sha256:97fe398e375c081a578a94fa2865d947b15ecab68026812febb5a3eb42b36ec2`  
		Last Modified: Tue, 14 Jan 2025 09:00:06 GMT  
		Size: 4.0 MB (4030134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc05a4160f4ad6a923accd00f3bd549f0f7dfdf8ccd93e41214ce85b9a48ebdf`  
		Last Modified: Tue, 14 Jan 2025 09:00:06 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7680b91d4d72d5fa6e01ad7110a7be2a65c2c1255c7186a6bac50da12d15c650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74239100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410311625c1c975966a96b8c08c37737161d80e4792f19eee2142b7660a3528a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e5e40a2b9fe32b2158c946023b700f61f57f567701b6be2e04192bbcc68fb32d`  
		Last Modified: Tue, 04 Feb 2025 01:40:49 GMT  
		Size: 48.7 MB (48735381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e7a097e6822ff46406de4794f79cc58a671b1cf4aca2e12e0e5d75f3e88af8`  
		Last Modified: Tue, 04 Feb 2025 09:01:34 GMT  
		Size: 25.5 MB (25503719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:303d7512961423b549ecbc3135fa423ffc439df03b4168223325681753f21177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4049086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338e85b070ec19c90c8f570a3d068cfe50e05677cc95e41bb216dbc2aca9fcd1`

```dockerfile
```

-	Layers:
	-	`sha256:8da040da9e8301aa2cc9fab27ddedef51e88742ead9e384fd037dccfeeff1449`  
		Last Modified: Tue, 04 Feb 2025 09:01:34 GMT  
		Size: 4.0 MB (4042186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad182928bef2359b12df2205d712273972389550d13ce80f836942225a82f170`  
		Last Modified: Tue, 04 Feb 2025 09:01:33 GMT  
		Size: 6.9 KB (6900 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6b88c5ba9bea73f06a57983ae54bfd9807848ce638c923d2155fab2143198898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76938960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b74a863b4d8839ed028b8736187a5fd7519b596282d0e5c889f6d931183078`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f6eab4c65eb241da9efbcd7f3af754621262244b11cdb15579a1ffe95621258b`  
		Last Modified: Tue, 04 Feb 2025 01:36:50 GMT  
		Size: 49.8 MB (49751669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f716b567c64e0e309015fd1a02f5a6cc44d9337e2d33b9f6b8078b32a497ea27`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 27.2 MB (27187291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5bef7b21a0b6b48c3cc0c8710b313ea295df7028cfbd4a432cd82c296c19e3b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4043841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25fb60dd8531f4ef2f9f0ab88a0d2c4ca3bc676fe4d34ffb8edf7fef45312b50`

```dockerfile
```

-	Layers:
	-	`sha256:77f1f939488d24c35d246e6dc7da23e7bed192f4991546e81bd85ad236384f4c`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 4.0 MB (4037042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2058966afd76dd12c237c44e52deaa671faffd214c395bcd6637cae7358e86c`  
		Last Modified: Tue, 04 Feb 2025 04:23:41 GMT  
		Size: 6.8 KB (6799 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:fd98e3efa140486701af3bbad0bff036d650707ae765c07c4be22171c350d9a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74316934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83a748686d419b8c487d0d25d3f5da8fbf2607059a4fe9c9050131bfb153408a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7fc12d8a734ed45514ae5135503d718e9ff7693017677de649ab963638a639fe`  
		Last Modified: Tue, 14 Jan 2025 01:37:16 GMT  
		Size: 48.4 MB (48390219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0115509fb5cc85eda38403b37d75aa0d68bc08deb77a8f9d926a1f8c06d921c`  
		Last Modified: Tue, 14 Jan 2025 18:14:22 GMT  
		Size: 25.9 MB (25926715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b3b21d911bdbbe951623248f5bf342419c79a1e98a16566e970307e88aca9b4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 KB (6654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad8f6edf913998dda0a3027d7f7b577a96f8bd3b884fdf75b8a2659163eb80e`

```dockerfile
```

-	Layers:
	-	`sha256:f424bcd5f01098e3348abfb322c6399e19c51c96f327ebfcd35261b1ecabefa0`  
		Last Modified: Tue, 14 Jan 2025 18:14:19 GMT  
		Size: 6.7 KB (6654 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b417044fed6946b9ceedb24ded07ce965a1f3f21c1de47a18d938bdf6e2ebd25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79735448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29cfb8b66e8c24333411236ca2f6e24b1daccc2a8b815ba3b35f81ec2d2ebdb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9f8f4c2cf61c41cc250d2e87b5eba96ba3e64ef3a295453812dac1f66ba73216`  
		Last Modified: Tue, 04 Feb 2025 01:41:20 GMT  
		Size: 52.1 MB (52139243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae7e1fce86863c28c734873936872848b6798972c915ef83ac0ef8757fcc152`  
		Last Modified: Tue, 04 Feb 2025 07:26:33 GMT  
		Size: 27.6 MB (27596205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:83c2b87868ebccf9aefbed4a631970b5183e1e34f1b0335cb950386d48243ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4056819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7feed53bdcc8f3767006fd26ebd376b9354cdee8fa89f8b62ff1bc2cf5e3321e`

```dockerfile
```

-	Layers:
	-	`sha256:58ee292a17e1fe38d5ccfa1ab34ceeb018c8c04929e010691e86d22a0460d25b`  
		Last Modified: Tue, 04 Feb 2025 07:26:33 GMT  
		Size: 4.0 MB (4049966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f2714839e58afe52b34955a96c5e386d431aac0e80ebee0fa43014a0129f7b5`  
		Last Modified: Tue, 04 Feb 2025 07:26:32 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:08fb9b8e25fd7d2240644cc0fbab6ed7665dbb8639050790bc175b21bfabdf8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72320391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa13ec122275564ca0bc6af020b5182073076046dbb42e69280eca2af5af20d1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f61e2eb7e669ffedfd7c292056ec3801e1d5a47c8a1ba8e2c9d94bf08f67ed2d`  
		Last Modified: Tue, 04 Feb 2025 01:45:19 GMT  
		Size: 46.9 MB (46907213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f3a589a8b6cbf639225cd2803ad3cdd7c9e4e67dbab48d826e7a48a0cb9682`  
		Last Modified: Tue, 04 Feb 2025 04:41:59 GMT  
		Size: 25.4 MB (25413178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2e3fa6627834d0fe4a8f126e7a1eea14a37d385bf6decf38cf72e4454d76190c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4039544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30968d1267b0076b09edbb66aaff2d7245c6a25ae073593499bfd88c6da07b6`

```dockerfile
```

-	Layers:
	-	`sha256:0b516cb000b606b307b6aa5a0268e3a0bd502e28feda68e16fa55680fa39a28c`  
		Last Modified: Tue, 04 Feb 2025 04:41:56 GMT  
		Size: 4.0 MB (4032691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fefc9c5367ed3581681873bdd962151dcee6a14a309dd861250e7d9742ea6573`  
		Last Modified: Tue, 04 Feb 2025 04:41:55 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:17f8f4d673ad80a912bb54ea841d21fd9fd8cfd6b44b036d4e25be59403aaeb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75630946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ef2d13ba22b276248d3ae18b834d40b0699b7e34f64603fd8ac544927a1b6d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5071fbe67e05b7dce13c72a6b655c4750a6b0653fdce60a9071966d5a747a2d8`  
		Last Modified: Tue, 04 Feb 2025 01:42:04 GMT  
		Size: 48.4 MB (48414760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2748bb8f4316900467409f846adce939a746b7f2adbe1e2ba340715af7fac142`  
		Last Modified: Tue, 04 Feb 2025 07:31:59 GMT  
		Size: 27.2 MB (27216186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1daaf0aee6f2ad2190f02166b924c8e24614ac3d30aa97b32836c15cd9f0cbf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4054445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7bd75c7e66e74cfe8701b21e4e463f81141d737e3d0837bc0e7181fda7f6595`

```dockerfile
```

-	Layers:
	-	`sha256:4c3f5b5b0a126e49897e13924462d03bf660d7788720d25bbd342ca25d88cec6`  
		Last Modified: Tue, 04 Feb 2025 07:31:58 GMT  
		Size: 4.0 MB (4047624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1644a119df56dd6162ab16cb8894344b6c303f51c4ff22bb5a3d32f34108f3ef`  
		Last Modified: Tue, 04 Feb 2025 07:31:58 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:d7b1848913e9a5757409d3ebf1fe95cbf03b0d255094c75d90a86b41c8b3a7b5
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
$ docker pull buildpack-deps@sha256:f487291be51e5d478800f7c65b9a503ab6235673807bc1276e81e0a165624a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141854519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60aa521c539bbb22fc2d13831a07d461e35a6f60dde2bed5c7351dde8611f14f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:af4da4e2d364845ad19d8dada5d782436e7eefced1b551d8d6a613212d528000`  
		Last Modified: Tue, 04 Feb 2025 01:36:46 GMT  
		Size: 48.3 MB (48348905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1be2f67d683c399ce2229317b243539533edd5a34194175f614d9715ed155d`  
		Last Modified: Tue, 04 Feb 2025 04:37:54 GMT  
		Size: 26.0 MB (26038437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbda3f387ceab9c039dbe56e4c3555afaa795a6af95ca16374c71c1ceb40cd0`  
		Last Modified: Tue, 04 Feb 2025 05:20:47 GMT  
		Size: 67.5 MB (67467177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:970ef7fe550fa87b4dda566cd405b8ae6f28b8aee97254502f87fca5a6cb6de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7670994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9569b64e2970c7a04074ef638fe351f938cde9a55fd35b9e3a6e2a1d35598118`

```dockerfile
```

-	Layers:
	-	`sha256:cf583dc30a65517b178c214cfeb2ae61f807f7ff0b8399e83bade971a711b176`  
		Last Modified: Tue, 04 Feb 2025 05:20:46 GMT  
		Size: 7.7 MB (7663680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42405d7221cae1b07937ab33f691e1604bc9bf2ad52e2026873942465a64cab7`  
		Last Modified: Tue, 04 Feb 2025 05:20:45 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e880624c6dc241604b850a8cef96855202f8a48abc46d611cf70e79dfcc7e077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136349127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d34ac1c32b6ff9467ccf5a5594c9771fb9021215e7ffd7c7389b123a200000b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:65c8e105f1e96f93defe25039ead5b48a9870e86175b80348bfd23ae3445cf2f`  
		Last Modified: Tue, 04 Feb 2025 01:40:53 GMT  
		Size: 46.5 MB (46502404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e17e53e6ecbca4d6fed6a359edf4419edd97930a581be4b6ad999669de4cdfc`  
		Last Modified: Tue, 04 Feb 2025 08:04:29 GMT  
		Size: 24.7 MB (24743168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17d90b594a7d89931d5de1b198b2dc07a97b965a1b004c4da3948056c117a8d`  
		Last Modified: Tue, 04 Feb 2025 10:23:00 GMT  
		Size: 65.1 MB (65103555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:164785459bb6b6d0f90da7e56eee4d7769da486e2f0fdf3d2526b87780cd6f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7676736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40000da731b6ab54e168ce98808313d9c4f419da4bfad48e01858f95acbe9d86`

```dockerfile
```

-	Layers:
	-	`sha256:7323964efa1407c77824afce3e74d3d93019898273512e6e067825cc358be661`  
		Last Modified: Tue, 04 Feb 2025 10:22:58 GMT  
		Size: 7.7 MB (7669362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b489edbda41a57517e3aa2211157756cd4a998ff40b48e2ae2b4ea4082aeeefe`  
		Last Modified: Tue, 04 Feb 2025 10:22:57 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d453a71279f51a33275b104128b0ef32161442779adfc2eca21e932784dc76bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.3 MB (130281606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9ebc683d6a2e74f3f6523b76e88dabbcd91ef15a5b3f5ded12eb0d86431ca1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:105ec2fcec8ae42e2b6cba4c3c8463bdd5ad21cffe232e9cfd7ed127e7ede3fa`  
		Last Modified: Tue, 14 Jan 2025 01:39:08 GMT  
		Size: 44.6 MB (44580459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881cf44810c526c17319a679eee937276e08c6767dabc96ffa22308bd53f7e1e`  
		Last Modified: Tue, 14 Jan 2025 09:00:07 GMT  
		Size: 23.8 MB (23806747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c787837970fa306cc5256b55f5173664552e3e16eb197389ac0c21aca92a24`  
		Last Modified: Tue, 14 Jan 2025 16:18:41 GMT  
		Size: 61.9 MB (61894400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:375bd3b5de1e4ce62154a317a2eedf0fbbc645ba28a336dfc7f57083debea352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7635007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea55d1a9628c01c5e7ce251049e6ccd4398382e087631485ad1c0e2193be47e2`

```dockerfile
```

-	Layers:
	-	`sha256:6bb2101881c8c8c0ffd4bc5a8101bf663900fd2aca831c674d7a718df973f6cf`  
		Last Modified: Tue, 14 Jan 2025 16:18:40 GMT  
		Size: 7.6 MB (7627633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9ae19583f8bb3be289a75674345c6ef019990014243072a9ab03287e1490e6d`  
		Last Modified: Tue, 14 Jan 2025 16:18:39 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d70a8d9b484c5a769d008f881b427c8ecbce176197d8464dbecabe3acc2f5ecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141189718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae5585f17239bb791e7d4137500f2b26d5bbe9857b7c3b81e66b75e1ae44a32`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:53cf00e5414c63ec005c43ad8342c8e55028d137e29e95d889d4247b0586d248`  
		Last Modified: Tue, 14 Jan 2025 01:38:51 GMT  
		Size: 48.7 MB (48661509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6216ff9e1bca52cad6d9119375ff8a9fe28c8b52c130d5380d5ded38210e688e`  
		Last Modified: Tue, 14 Jan 2025 07:01:19 GMT  
		Size: 25.4 MB (25426483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab5443d60c3808485433bb956012bfe58b69cebf352b638a921b47918c7b109`  
		Last Modified: Tue, 14 Jan 2025 13:33:15 GMT  
		Size: 67.1 MB (67101726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:71b473c988201a15d0e20854c52a1e6f719e17af81f6b027cb96157e56a1d0eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7642809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a2500c367298cd1fc64543c18629eb985446986c8b845641b92ccf0347b2d2`

```dockerfile
```

-	Layers:
	-	`sha256:0c061376a90509fe3dde2e194e4939ff029461fcc3800e0f40ae80e36a483e6d`  
		Last Modified: Tue, 14 Jan 2025 13:33:13 GMT  
		Size: 7.6 MB (7635416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4308ad8e7f7805b5fd297337cf6f2cde3691af0c299efa78aa756c4c035d0284`  
		Last Modified: Tue, 14 Jan 2025 13:33:12 GMT  
		Size: 7.4 KB (7393 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:1ed16b0936c8407a72004889edad80759c99e5438a9a70e386b7ae83319f60b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.3 MB (146340563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f95befdc782b90fc6a9406d931871ece11c0fa8745cc0f868e5a054e49bbc0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f6eab4c65eb241da9efbcd7f3af754621262244b11cdb15579a1ffe95621258b`  
		Last Modified: Tue, 04 Feb 2025 01:36:50 GMT  
		Size: 49.8 MB (49751669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f716b567c64e0e309015fd1a02f5a6cc44d9337e2d33b9f6b8078b32a497ea27`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 27.2 MB (27187291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4913bde8dd9201a45eb15eecac64dfe0033ec3938f3fffc5d62cb37095ca1ed5`  
		Last Modified: Tue, 04 Feb 2025 05:15:41 GMT  
		Size: 69.4 MB (69401603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7c444a74ef507e91e25d322d7a1b1810d0152c6086cb9217466eac67f8718923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7665717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b7ce1fcd892fa25e8af962edc78a25e4d9b016b6647ea39c5b7cabf5d7b532`

```dockerfile
```

-	Layers:
	-	`sha256:a2408e37c2fa9db1a5073eac5690fc938e92771f4870a803b110f295386963b2`  
		Last Modified: Tue, 04 Feb 2025 05:15:39 GMT  
		Size: 7.7 MB (7658425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f03c5a7cb4320006cf4ff2e0e0755de4671f7f3552f66c41de44623e306df771`  
		Last Modified: Tue, 04 Feb 2025 05:15:38 GMT  
		Size: 7.3 KB (7292 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:4542f8065a818db739219a01e1b40b60efec5afadfcc4529d720a912a39ab61b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.3 MB (140293949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70012defa400db789835b3fce6a207e007f4872ca46448489c6c0af0fbb96add`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7fc12d8a734ed45514ae5135503d718e9ff7693017677de649ab963638a639fe`  
		Last Modified: Tue, 14 Jan 2025 01:37:16 GMT  
		Size: 48.4 MB (48390219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0115509fb5cc85eda38403b37d75aa0d68bc08deb77a8f9d926a1f8c06d921c`  
		Last Modified: Tue, 14 Jan 2025 18:14:22 GMT  
		Size: 25.9 MB (25926715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ed8eab45779c4caaf48a3dd1f3e53c5b4079b75e32b657bac3bdc07a0f1e4b`  
		Last Modified: Wed, 15 Jan 2025 02:07:24 GMT  
		Size: 66.0 MB (65977015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7cc83ae9e313ec8a4b0f9dee34a4c9c2af59dcda58e3a038fb4c36710dee4a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd3378118053b582710f3fff850eceaf69604c78fa7b42fc57a97a2a20686e2`

```dockerfile
```

-	Layers:
	-	`sha256:4ba40c128050744b384986d01d36e73805b787370c0dd4fbea02fcb7fd83acb3`  
		Last Modified: Wed, 15 Jan 2025 02:07:18 GMT  
		Size: 7.1 KB (7147 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:fcce0daab7df71c0a4d24ed7b777c4ad2f8e4e07c45ac14ca2f0984222d32abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152098758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4dea55014e43fd29a446e2658ddc4573c27a9139ba114d7a6515a269fd6e4e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:826e70a2bdfac0f05c49b7611afcf30a311c862a1beca6fc4059e4b6cd0e1a4a`  
		Last Modified: Tue, 14 Jan 2025 01:40:51 GMT  
		Size: 52.0 MB (52043133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f126b14e556a94eaec41c5a29f9164224f92b1080c74dca2491c3f7b9120c320`  
		Last Modified: Tue, 14 Jan 2025 05:32:11 GMT  
		Size: 27.5 MB (27531238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7311c304e2cd2735e9d0f4a75554811f3be94be0d57e4fd8ff5989c485af8c30`  
		Last Modified: Tue, 14 Jan 2025 09:44:47 GMT  
		Size: 72.5 MB (72524387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a001f2f6032e4930c80eebb2260702f3186b60b4d076204054369677f2e582d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7647664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff99e2b1587ec2a5c003050bc95171349435c39da73c56936d00f2a3ebdb3141`

```dockerfile
```

-	Layers:
	-	`sha256:64579d1288b78c8094cfe263e14ab072d6d69bfced7f13b129680dd8bfb1a06a`  
		Last Modified: Tue, 14 Jan 2025 09:44:45 GMT  
		Size: 7.6 MB (7640318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ba8f2daa2f44abd8160ed1034994c1d4c473f6eab21718fe570387334939b62`  
		Last Modified: Tue, 14 Jan 2025 09:44:44 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:841b670efa888fba12f3ca424d021bea46e276c2a406876d2805ebd30661cad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.2 MB (144183374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a538ed29c23de0033afa76c98443583277d7e4f244f6de7b22975a716779870`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5071fbe67e05b7dce13c72a6b655c4750a6b0653fdce60a9071966d5a747a2d8`  
		Last Modified: Tue, 04 Feb 2025 01:42:04 GMT  
		Size: 48.4 MB (48414760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2748bb8f4316900467409f846adce939a746b7f2adbe1e2ba340715af7fac142`  
		Last Modified: Tue, 04 Feb 2025 07:31:59 GMT  
		Size: 27.2 MB (27216186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9371642bbb4f2496e43eaeaa75efac59f54344b0c0beee1184503290cbf7343a`  
		Last Modified: Tue, 04 Feb 2025 11:38:14 GMT  
		Size: 68.6 MB (68552428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0b3506d5e6cc98bbe1f6132732531295f20e63be600a8132ce4f9e43c8b7f28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7676823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099bc7a3a7b814638927fff3374f349bfee6919065f69fbd17ab7afe592ae384`

```dockerfile
```

-	Layers:
	-	`sha256:9c9e3a34680550da80f6d8ed94a748afe42e82068c2fd150cf281d40fa61cba8`  
		Last Modified: Tue, 04 Feb 2025 11:38:12 GMT  
		Size: 7.7 MB (7669509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da0d790adc26bb3f35199a82b70f773864a308950b877536a295c0a79358143f`  
		Last Modified: Tue, 04 Feb 2025 11:38:12 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:88ea32c91e0088d334eee5839f76c663b0ece625a514c1ac24671005d47a308c
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
$ docker pull buildpack-deps@sha256:3862089c116e698ae8dcb267ff2dc3e41c7668bca19245d85626aeb69633bca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.3 MB (380342321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2042c40c5e97e9fded6f02ba0fd360931322d9bf5c9ba337effd0c197bb0f32`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:af4da4e2d364845ad19d8dada5d782436e7eefced1b551d8d6a613212d528000`  
		Last Modified: Tue, 04 Feb 2025 01:36:46 GMT  
		Size: 48.3 MB (48348905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1be2f67d683c399ce2229317b243539533edd5a34194175f614d9715ed155d`  
		Last Modified: Tue, 04 Feb 2025 04:37:54 GMT  
		Size: 26.0 MB (26038437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbda3f387ceab9c039dbe56e4c3555afaa795a6af95ca16374c71c1ceb40cd0`  
		Last Modified: Tue, 04 Feb 2025 05:20:47 GMT  
		Size: 67.5 MB (67467177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae05f536b0d5759ee824999756f5a55c1d4da8e35f66232cdfb6e42c5597bf7`  
		Last Modified: Tue, 04 Feb 2025 06:14:35 GMT  
		Size: 238.5 MB (238487802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5caf0ca48f5b68c01faa5d43e0744d3c9c6d7d530d19ff1468abed1fb8efcb17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16942937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b93fae4b0c13aa929b3de4e93e14455f02715975a7a9236bd9591bacb55e9e3`

```dockerfile
```

-	Layers:
	-	`sha256:afe3d7666554427076557c02f44cc7f668d341a34bd1ce4509f6352aeb88dbcd`  
		Last Modified: Tue, 04 Feb 2025 06:14:30 GMT  
		Size: 16.9 MB (16932744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a32a2743c857eb71e17a15d25c030656a2e839841377b829f90cc40b5244accc`  
		Last Modified: Tue, 04 Feb 2025 06:14:29 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ba095bb649386b16b9fc040a78d3178a0517fca394dcd6a794ac9edc2ed63c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.7 MB (345661913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c45ea7e4b70bf69715291cdd7917f482d0acfa53e0ac45ba3034532d2360631a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:65c8e105f1e96f93defe25039ead5b48a9870e86175b80348bfd23ae3445cf2f`  
		Last Modified: Tue, 04 Feb 2025 01:40:53 GMT  
		Size: 46.5 MB (46502404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e17e53e6ecbca4d6fed6a359edf4419edd97930a581be4b6ad999669de4cdfc`  
		Last Modified: Tue, 04 Feb 2025 08:04:29 GMT  
		Size: 24.7 MB (24743168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17d90b594a7d89931d5de1b198b2dc07a97b965a1b004c4da3948056c117a8d`  
		Last Modified: Tue, 04 Feb 2025 10:23:00 GMT  
		Size: 65.1 MB (65103555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d054220a6a95da9f3d586a2f3758d12b834db5f03df5446b2303636b5e04ce3a`  
		Last Modified: Tue, 04 Feb 2025 11:48:13 GMT  
		Size: 209.3 MB (209312786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:421e412642e50cc48434133d8fc62f191432878ad160c9067bad7a3999f6eca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16712372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617465c67c203784a67272318700e60f7d05912337ea5b12e0c42892846c4a81`

```dockerfile
```

-	Layers:
	-	`sha256:43cb58f621a1a135d73938e960d782544b1e1f86a646f1457e362731c292633d`  
		Last Modified: Tue, 04 Feb 2025 11:48:08 GMT  
		Size: 16.7 MB (16702119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:041297f6ef05786d56a6380863e85430c242c49e3901190b100bd6269cae8f43`  
		Last Modified: Tue, 04 Feb 2025 11:48:07 GMT  
		Size: 10.3 KB (10253 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:da6d5652822bbc0c3bcd4b1eff1dca2f76d1b48d397e547616f82d9638477e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.9 MB (323923481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b323295859897e21b08b6202c32b50b7dd25c1b6061ba4a47ba1a4430b263824`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:105ec2fcec8ae42e2b6cba4c3c8463bdd5ad21cffe232e9cfd7ed127e7ede3fa`  
		Last Modified: Tue, 14 Jan 2025 01:39:08 GMT  
		Size: 44.6 MB (44580459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881cf44810c526c17319a679eee937276e08c6767dabc96ffa22308bd53f7e1e`  
		Last Modified: Tue, 14 Jan 2025 09:00:07 GMT  
		Size: 23.8 MB (23806747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c787837970fa306cc5256b55f5173664552e3e16eb197389ac0c21aca92a24`  
		Last Modified: Tue, 14 Jan 2025 16:18:41 GMT  
		Size: 61.9 MB (61894400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9300ff4f70721ff1e9737e80c1a1eaa49b83fa08a552177c95c775ed44606a84`  
		Last Modified: Tue, 14 Jan 2025 22:01:42 GMT  
		Size: 193.6 MB (193641875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ef0530b783e5de869f817fd642dfb1caef42ac28d62ce6e28fdb91a456ea0c14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16671715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a75c8344b5fafc11d176ae43785d83e5059676edb9609011e2396efdb61abdb`

```dockerfile
```

-	Layers:
	-	`sha256:d25c91edb4beddef9af8441097837eeb335ad8933a5e6625886cf33db46cfcfc`  
		Last Modified: Tue, 14 Jan 2025 22:01:38 GMT  
		Size: 16.7 MB (16661463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad274817363339e07ad186527b366b93e96d7c027a00944b37f01ea200af71ff`  
		Last Modified: Tue, 14 Jan 2025 22:01:37 GMT  
		Size: 10.3 KB (10252 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2a64b528a91b982ca51b72ba47a808f07b867469d5da3954dc0a664f09f5b666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.2 MB (368167662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c41f5d3261ad99085f5e16f4d0a6ea0ee11050b3a28df955008125a52b7e3761`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:53cf00e5414c63ec005c43ad8342c8e55028d137e29e95d889d4247b0586d248`  
		Last Modified: Tue, 14 Jan 2025 01:38:51 GMT  
		Size: 48.7 MB (48661509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6216ff9e1bca52cad6d9119375ff8a9fe28c8b52c130d5380d5ded38210e688e`  
		Last Modified: Tue, 14 Jan 2025 07:01:19 GMT  
		Size: 25.4 MB (25426483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab5443d60c3808485433bb956012bfe58b69cebf352b638a921b47918c7b109`  
		Last Modified: Tue, 14 Jan 2025 13:33:15 GMT  
		Size: 67.1 MB (67101726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f57a614701f3245516a9cf7adb78fd0830fd5bea39e42e511c29cd73c44a41`  
		Last Modified: Tue, 14 Jan 2025 17:14:04 GMT  
		Size: 227.0 MB (226977944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f3c7d09cfe30fefb345323728b6556604e927d8c2a7201ccb407f5e42cad7208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16990040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb21a81412050be940a80a673b2d3dcb80be439fa563479e47b233929afbed70`

```dockerfile
```

-	Layers:
	-	`sha256:02eb0397b03f384d9a6d137f8060b59de6798f4277e6b7155091f20d26610ac0`  
		Last Modified: Tue, 14 Jan 2025 17:13:59 GMT  
		Size: 17.0 MB (16979767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc21006030d24c01acbe412539fa49a96ffd74930fd6fc2d23963e3bbc70eb9c`  
		Last Modified: Tue, 14 Jan 2025 17:13:58 GMT  
		Size: 10.3 KB (10273 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e143a351e131ff3e73d70f7435bfa3afceffe3d7df01784f838814d1d1a22aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.2 MB (389172398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09603d66d8ec957adc1b43b9cc1a42625aef0dfedc65c9533abdf747c9141153`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f6eab4c65eb241da9efbcd7f3af754621262244b11cdb15579a1ffe95621258b`  
		Last Modified: Tue, 04 Feb 2025 01:36:50 GMT  
		Size: 49.8 MB (49751669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f716b567c64e0e309015fd1a02f5a6cc44d9337e2d33b9f6b8078b32a497ea27`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 27.2 MB (27187291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4913bde8dd9201a45eb15eecac64dfe0033ec3938f3fffc5d62cb37095ca1ed5`  
		Last Modified: Tue, 04 Feb 2025 05:15:41 GMT  
		Size: 69.4 MB (69401603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afd1cfae6f514571d7f4226e482cdb485486ee849f4136f31c735d85704d269`  
		Last Modified: Tue, 04 Feb 2025 06:15:04 GMT  
		Size: 242.8 MB (242831835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dce6938c7089bbd10bf7f15ec6c70c8590e4f0498d62027fba33c63771e6fc3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16911735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abcdfa41e35edc5ae7563ebd6b4c808c7999d33caa3e08bf8dea4a6f197a618`

```dockerfile
```

-	Layers:
	-	`sha256:449f4108f7c12ed2ef005b79ca305e1fe108b45a0283ee92ce7581a0c26d787b`  
		Last Modified: Tue, 04 Feb 2025 06:14:59 GMT  
		Size: 16.9 MB (16901564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e08c7332c054a21ab001deb52f099531010f779b1a5b83889e1511ae98b65494`  
		Last Modified: Tue, 04 Feb 2025 06:14:59 GMT  
		Size: 10.2 KB (10171 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:aa5fa8fee1a908124ae3adc565543dfbc931cd430a4c68f7ad938fbcee2333fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.5 MB (354487822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af426ea9e9fe6cb17eb21147c060df9727d22c4a02f6d69ce356aad9242482b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7fc12d8a734ed45514ae5135503d718e9ff7693017677de649ab963638a639fe`  
		Last Modified: Tue, 14 Jan 2025 01:37:16 GMT  
		Size: 48.4 MB (48390219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0115509fb5cc85eda38403b37d75aa0d68bc08deb77a8f9d926a1f8c06d921c`  
		Last Modified: Tue, 14 Jan 2025 18:14:22 GMT  
		Size: 25.9 MB (25926715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ed8eab45779c4caaf48a3dd1f3e53c5b4079b75e32b657bac3bdc07a0f1e4b`  
		Last Modified: Wed, 15 Jan 2025 02:07:24 GMT  
		Size: 66.0 MB (65977015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dad556c93c7fbd44bd1df34a958ab27627b99c3df6076447109ea0903c46714`  
		Last Modified: Wed, 15 Jan 2025 18:16:26 GMT  
		Size: 214.2 MB (214193873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6353c960241b82e055e52d6a26b7606c8831cf880e464ed1d6255d758d19c3a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c5a82460cab0b82fc4e9188547d910028f8cab28c7d7bbee19dc3cd407f793`

```dockerfile
```

-	Layers:
	-	`sha256:4569235f2213d7cddb66a73d7068690a1abbeb777a4852b2697d7d207f52d8fe`  
		Last Modified: Wed, 15 Jan 2025 18:16:07 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e7ad1938d3920ab76b97cdb0269dc3e146e5e6df9228703a73d312deea2b970d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.5 MB (384517027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8fe2d0729ff9734c1cfabfd95b52648072a577e4cb67905bada67aaa788152f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:826e70a2bdfac0f05c49b7611afcf30a311c862a1beca6fc4059e4b6cd0e1a4a`  
		Last Modified: Tue, 14 Jan 2025 01:40:51 GMT  
		Size: 52.0 MB (52043133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f126b14e556a94eaec41c5a29f9164224f92b1080c74dca2491c3f7b9120c320`  
		Last Modified: Tue, 14 Jan 2025 05:32:11 GMT  
		Size: 27.5 MB (27531238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7311c304e2cd2735e9d0f4a75554811f3be94be0d57e4fd8ff5989c485af8c30`  
		Last Modified: Tue, 14 Jan 2025 09:44:47 GMT  
		Size: 72.5 MB (72524387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c13c3f363d5cb80dd126d46dc749469f09c6bcf87873368d4910edf4c8fab0`  
		Last Modified: Tue, 14 Jan 2025 13:08:14 GMT  
		Size: 232.4 MB (232418269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b272982f72f68b67efc7c6a61a563586c1ca471dac11804f4ebea07fa02c30bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16893502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d9551896361669f19dca1b2f2bfc5f14df31a73639e98be441623b4ab72783`

```dockerfile
```

-	Layers:
	-	`sha256:d0cebc80f7ba1e831ad0fd69b4cdb1a684550f85676baa46a01a0369228a2278`  
		Last Modified: Tue, 14 Jan 2025 13:08:11 GMT  
		Size: 16.9 MB (16883277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8973654c9bf96e1c45cbe69e6de6aac1822ccbd7a68456b5b54d6b1a3e3b206`  
		Last Modified: Tue, 14 Jan 2025 13:08:08 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c269b72c35b95814f21ceffb69ec1624b4531d8b4e87ab81af3ebfe16b455a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.1 MB (350086446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd137b601fa29b6959f2bf38bf9a5799d3bb6d994f910d052acbb470373194d3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a96882092e58b6b0f460c25e0b3fa57215487e6282387621e5c4dd2314637493`  
		Last Modified: Tue, 14 Jan 2025 01:38:54 GMT  
		Size: 48.3 MB (48329740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c639414a48a5e91286e442a3c2a376c94650966c4fede85d34f85e98bf430e8`  
		Last Modified: Tue, 14 Jan 2025 05:01:37 GMT  
		Size: 27.1 MB (27131328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a0617227e41b6c45ea475d62d65ee6e02048cb238dcbfd9f884635a3d44568`  
		Last Modified: Tue, 14 Jan 2025 09:12:11 GMT  
		Size: 68.2 MB (68150739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10418c2ff73fdb0d646523d4f04c8033e632051fd913baf1a7613485f088ba63`  
		Last Modified: Tue, 14 Jan 2025 11:20:04 GMT  
		Size: 206.5 MB (206474639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:80aae46b3af426dfe933e73c3da2bbc571f3155ad4fe717d4b07aa2dd9e41901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16687094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c455383ad764fc23d63f45994189401ea53025b6068ce94683f5defbe2125b`

```dockerfile
```

-	Layers:
	-	`sha256:dd52e57c85451a22dead751eaa430c4c6b1931235c8b39a3e7252e0700730938`  
		Last Modified: Tue, 14 Jan 2025 11:20:00 GMT  
		Size: 16.7 MB (16676901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f01ba2d6246ad25bd5819324375382448632dfb6c3c500a62dd94402529f9ffa`  
		Last Modified: Tue, 14 Jan 2025 11:19:59 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:b679578e99e891ce38c452a7e625eecc65caa06c50086f730a2eb1c2a4613a74
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
$ docker pull buildpack-deps@sha256:aee25dd8533c4987c4174b90b38c111bafbbcb7d62625571ed88e06c5d103e1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74387342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa1ba49db818dc17b8375378ca48a72a856869186b91b7cc1bc25cf591349ed9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:af4da4e2d364845ad19d8dada5d782436e7eefced1b551d8d6a613212d528000`  
		Last Modified: Tue, 04 Feb 2025 01:36:46 GMT  
		Size: 48.3 MB (48348905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1be2f67d683c399ce2229317b243539533edd5a34194175f614d9715ed155d`  
		Last Modified: Tue, 04 Feb 2025 04:37:54 GMT  
		Size: 26.0 MB (26038437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:13051b3a62affdef39f0b11959ab2f3e5be76cc4dbb01d84f0882ebae8ebe7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4048111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b6b5b4470cf325c65245a4121edda03884ee9dd31ca16a14c891cf36080c7cd`

```dockerfile
```

-	Layers:
	-	`sha256:baf1bd4a8e8ca39f8474004a7082c2789d2157ac1f6784ca6dd790f2c10e2726`  
		Last Modified: Tue, 04 Feb 2025 04:37:53 GMT  
		Size: 4.0 MB (4041291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77f014b0fdbc84aaa05d094e879a3865d8ff0c20f33326bde23301a0f144e7dd`  
		Last Modified: Tue, 04 Feb 2025 04:37:53 GMT  
		Size: 6.8 KB (6820 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c8b72309a00c55121660036dc53fc7a55227dd584a370f77d25f8d06e544c915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71245572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c5897d4a1b1f8a5acad55b61b1aac3c28340525f575546f22605ce71a4b008`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:65c8e105f1e96f93defe25039ead5b48a9870e86175b80348bfd23ae3445cf2f`  
		Last Modified: Tue, 04 Feb 2025 01:40:53 GMT  
		Size: 46.5 MB (46502404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e17e53e6ecbca4d6fed6a359edf4419edd97930a581be4b6ad999669de4cdfc`  
		Last Modified: Tue, 04 Feb 2025 08:04:29 GMT  
		Size: 24.7 MB (24743168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e3c37ea07ec604ed597239c3e420144e4445ac99f8ebe34ec8d721c622caa657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4055799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95d254ad2a5dead6eb395b06930bd6dd081a28e79a3adf074ed155d8dc59799`

```dockerfile
```

-	Layers:
	-	`sha256:008cc661fa77c12a00af319e8adc81a6ad24da66847717769b4f90b93b6dc8e8`  
		Last Modified: Tue, 04 Feb 2025 08:04:29 GMT  
		Size: 4.0 MB (4048918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:438f772e281905bb522f01575f7ec1286452b5b73198927e065d129b4448a0b9`  
		Last Modified: Tue, 04 Feb 2025 08:04:28 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0a6c357b2a5550465bbb58c8cb50f1b528f6e0b3bcb2cc03e8e4699e5cbbe01b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68387206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1403e33a3f014b9f3a79bfd150de00b1bcd52579b0635858ef7266499b6c4d08`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:105ec2fcec8ae42e2b6cba4c3c8463bdd5ad21cffe232e9cfd7ed127e7ede3fa`  
		Last Modified: Tue, 14 Jan 2025 01:39:08 GMT  
		Size: 44.6 MB (44580459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881cf44810c526c17319a679eee937276e08c6767dabc96ffa22308bd53f7e1e`  
		Last Modified: Tue, 14 Jan 2025 09:00:07 GMT  
		Size: 23.8 MB (23806747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:816e5ecae2afe97b2716b2fd5e97c09a92fa84b86e4724086e7bf7abc1da653b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4037015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:416f156bb04b0ec4ba73c579a5ada9b1d5888217d9012f51892ef6cbdbbe423b`

```dockerfile
```

-	Layers:
	-	`sha256:97fe398e375c081a578a94fa2865d947b15ecab68026812febb5a3eb42b36ec2`  
		Last Modified: Tue, 14 Jan 2025 09:00:06 GMT  
		Size: 4.0 MB (4030134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc05a4160f4ad6a923accd00f3bd549f0f7dfdf8ccd93e41214ce85b9a48ebdf`  
		Last Modified: Tue, 14 Jan 2025 09:00:06 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7680b91d4d72d5fa6e01ad7110a7be2a65c2c1255c7186a6bac50da12d15c650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74239100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410311625c1c975966a96b8c08c37737161d80e4792f19eee2142b7660a3528a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e5e40a2b9fe32b2158c946023b700f61f57f567701b6be2e04192bbcc68fb32d`  
		Last Modified: Tue, 04 Feb 2025 01:40:49 GMT  
		Size: 48.7 MB (48735381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e7a097e6822ff46406de4794f79cc58a671b1cf4aca2e12e0e5d75f3e88af8`  
		Last Modified: Tue, 04 Feb 2025 09:01:34 GMT  
		Size: 25.5 MB (25503719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:303d7512961423b549ecbc3135fa423ffc439df03b4168223325681753f21177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4049086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338e85b070ec19c90c8f570a3d068cfe50e05677cc95e41bb216dbc2aca9fcd1`

```dockerfile
```

-	Layers:
	-	`sha256:8da040da9e8301aa2cc9fab27ddedef51e88742ead9e384fd037dccfeeff1449`  
		Last Modified: Tue, 04 Feb 2025 09:01:34 GMT  
		Size: 4.0 MB (4042186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad182928bef2359b12df2205d712273972389550d13ce80f836942225a82f170`  
		Last Modified: Tue, 04 Feb 2025 09:01:33 GMT  
		Size: 6.9 KB (6900 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6b88c5ba9bea73f06a57983ae54bfd9807848ce638c923d2155fab2143198898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76938960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b74a863b4d8839ed028b8736187a5fd7519b596282d0e5c889f6d931183078`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f6eab4c65eb241da9efbcd7f3af754621262244b11cdb15579a1ffe95621258b`  
		Last Modified: Tue, 04 Feb 2025 01:36:50 GMT  
		Size: 49.8 MB (49751669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f716b567c64e0e309015fd1a02f5a6cc44d9337e2d33b9f6b8078b32a497ea27`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 27.2 MB (27187291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5bef7b21a0b6b48c3cc0c8710b313ea295df7028cfbd4a432cd82c296c19e3b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4043841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25fb60dd8531f4ef2f9f0ab88a0d2c4ca3bc676fe4d34ffb8edf7fef45312b50`

```dockerfile
```

-	Layers:
	-	`sha256:77f1f939488d24c35d246e6dc7da23e7bed192f4991546e81bd85ad236384f4c`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 4.0 MB (4037042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2058966afd76dd12c237c44e52deaa671faffd214c395bcd6637cae7358e86c`  
		Last Modified: Tue, 04 Feb 2025 04:23:41 GMT  
		Size: 6.8 KB (6799 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:fd98e3efa140486701af3bbad0bff036d650707ae765c07c4be22171c350d9a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74316934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83a748686d419b8c487d0d25d3f5da8fbf2607059a4fe9c9050131bfb153408a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7fc12d8a734ed45514ae5135503d718e9ff7693017677de649ab963638a639fe`  
		Last Modified: Tue, 14 Jan 2025 01:37:16 GMT  
		Size: 48.4 MB (48390219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0115509fb5cc85eda38403b37d75aa0d68bc08deb77a8f9d926a1f8c06d921c`  
		Last Modified: Tue, 14 Jan 2025 18:14:22 GMT  
		Size: 25.9 MB (25926715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b3b21d911bdbbe951623248f5bf342419c79a1e98a16566e970307e88aca9b4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 KB (6654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad8f6edf913998dda0a3027d7f7b577a96f8bd3b884fdf75b8a2659163eb80e`

```dockerfile
```

-	Layers:
	-	`sha256:f424bcd5f01098e3348abfb322c6399e19c51c96f327ebfcd35261b1ecabefa0`  
		Last Modified: Tue, 14 Jan 2025 18:14:19 GMT  
		Size: 6.7 KB (6654 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b417044fed6946b9ceedb24ded07ce965a1f3f21c1de47a18d938bdf6e2ebd25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79735448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29cfb8b66e8c24333411236ca2f6e24b1daccc2a8b815ba3b35f81ec2d2ebdb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9f8f4c2cf61c41cc250d2e87b5eba96ba3e64ef3a295453812dac1f66ba73216`  
		Last Modified: Tue, 04 Feb 2025 01:41:20 GMT  
		Size: 52.1 MB (52139243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae7e1fce86863c28c734873936872848b6798972c915ef83ac0ef8757fcc152`  
		Last Modified: Tue, 04 Feb 2025 07:26:33 GMT  
		Size: 27.6 MB (27596205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:83c2b87868ebccf9aefbed4a631970b5183e1e34f1b0335cb950386d48243ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4056819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7feed53bdcc8f3767006fd26ebd376b9354cdee8fa89f8b62ff1bc2cf5e3321e`

```dockerfile
```

-	Layers:
	-	`sha256:58ee292a17e1fe38d5ccfa1ab34ceeb018c8c04929e010691e86d22a0460d25b`  
		Last Modified: Tue, 04 Feb 2025 07:26:33 GMT  
		Size: 4.0 MB (4049966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f2714839e58afe52b34955a96c5e386d431aac0e80ebee0fa43014a0129f7b5`  
		Last Modified: Tue, 04 Feb 2025 07:26:32 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:08fb9b8e25fd7d2240644cc0fbab6ed7665dbb8639050790bc175b21bfabdf8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72320391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa13ec122275564ca0bc6af020b5182073076046dbb42e69280eca2af5af20d1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f61e2eb7e669ffedfd7c292056ec3801e1d5a47c8a1ba8e2c9d94bf08f67ed2d`  
		Last Modified: Tue, 04 Feb 2025 01:45:19 GMT  
		Size: 46.9 MB (46907213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f3a589a8b6cbf639225cd2803ad3cdd7c9e4e67dbab48d826e7a48a0cb9682`  
		Last Modified: Tue, 04 Feb 2025 04:41:59 GMT  
		Size: 25.4 MB (25413178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2e3fa6627834d0fe4a8f126e7a1eea14a37d385bf6decf38cf72e4454d76190c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4039544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30968d1267b0076b09edbb66aaff2d7245c6a25ae073593499bfd88c6da07b6`

```dockerfile
```

-	Layers:
	-	`sha256:0b516cb000b606b307b6aa5a0268e3a0bd502e28feda68e16fa55680fa39a28c`  
		Last Modified: Tue, 04 Feb 2025 04:41:56 GMT  
		Size: 4.0 MB (4032691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fefc9c5367ed3581681873bdd962151dcee6a14a309dd861250e7d9742ea6573`  
		Last Modified: Tue, 04 Feb 2025 04:41:55 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:17f8f4d673ad80a912bb54ea841d21fd9fd8cfd6b44b036d4e25be59403aaeb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75630946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ef2d13ba22b276248d3ae18b834d40b0699b7e34f64603fd8ac544927a1b6d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5071fbe67e05b7dce13c72a6b655c4750a6b0653fdce60a9071966d5a747a2d8`  
		Last Modified: Tue, 04 Feb 2025 01:42:04 GMT  
		Size: 48.4 MB (48414760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2748bb8f4316900467409f846adce939a746b7f2adbe1e2ba340715af7fac142`  
		Last Modified: Tue, 04 Feb 2025 07:31:59 GMT  
		Size: 27.2 MB (27216186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1daaf0aee6f2ad2190f02166b924c8e24614ac3d30aa97b32836c15cd9f0cbf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4054445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7bd75c7e66e74cfe8701b21e4e463f81141d737e3d0837bc0e7181fda7f6595`

```dockerfile
```

-	Layers:
	-	`sha256:4c3f5b5b0a126e49897e13924462d03bf660d7788720d25bbd342ca25d88cec6`  
		Last Modified: Tue, 04 Feb 2025 07:31:58 GMT  
		Size: 4.0 MB (4047624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1644a119df56dd6162ab16cb8894344b6c303f51c4ff22bb5a3d32f34108f3ef`  
		Last Modified: Tue, 04 Feb 2025 07:31:58 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:d7b1848913e9a5757409d3ebf1fe95cbf03b0d255094c75d90a86b41c8b3a7b5
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
$ docker pull buildpack-deps@sha256:f487291be51e5d478800f7c65b9a503ab6235673807bc1276e81e0a165624a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141854519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60aa521c539bbb22fc2d13831a07d461e35a6f60dde2bed5c7351dde8611f14f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:af4da4e2d364845ad19d8dada5d782436e7eefced1b551d8d6a613212d528000`  
		Last Modified: Tue, 04 Feb 2025 01:36:46 GMT  
		Size: 48.3 MB (48348905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1be2f67d683c399ce2229317b243539533edd5a34194175f614d9715ed155d`  
		Last Modified: Tue, 04 Feb 2025 04:37:54 GMT  
		Size: 26.0 MB (26038437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbda3f387ceab9c039dbe56e4c3555afaa795a6af95ca16374c71c1ceb40cd0`  
		Last Modified: Tue, 04 Feb 2025 05:20:47 GMT  
		Size: 67.5 MB (67467177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:970ef7fe550fa87b4dda566cd405b8ae6f28b8aee97254502f87fca5a6cb6de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7670994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9569b64e2970c7a04074ef638fe351f938cde9a55fd35b9e3a6e2a1d35598118`

```dockerfile
```

-	Layers:
	-	`sha256:cf583dc30a65517b178c214cfeb2ae61f807f7ff0b8399e83bade971a711b176`  
		Last Modified: Tue, 04 Feb 2025 05:20:46 GMT  
		Size: 7.7 MB (7663680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42405d7221cae1b07937ab33f691e1604bc9bf2ad52e2026873942465a64cab7`  
		Last Modified: Tue, 04 Feb 2025 05:20:45 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e880624c6dc241604b850a8cef96855202f8a48abc46d611cf70e79dfcc7e077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136349127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d34ac1c32b6ff9467ccf5a5594c9771fb9021215e7ffd7c7389b123a200000b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:65c8e105f1e96f93defe25039ead5b48a9870e86175b80348bfd23ae3445cf2f`  
		Last Modified: Tue, 04 Feb 2025 01:40:53 GMT  
		Size: 46.5 MB (46502404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e17e53e6ecbca4d6fed6a359edf4419edd97930a581be4b6ad999669de4cdfc`  
		Last Modified: Tue, 04 Feb 2025 08:04:29 GMT  
		Size: 24.7 MB (24743168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17d90b594a7d89931d5de1b198b2dc07a97b965a1b004c4da3948056c117a8d`  
		Last Modified: Tue, 04 Feb 2025 10:23:00 GMT  
		Size: 65.1 MB (65103555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:164785459bb6b6d0f90da7e56eee4d7769da486e2f0fdf3d2526b87780cd6f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7676736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40000da731b6ab54e168ce98808313d9c4f419da4bfad48e01858f95acbe9d86`

```dockerfile
```

-	Layers:
	-	`sha256:7323964efa1407c77824afce3e74d3d93019898273512e6e067825cc358be661`  
		Last Modified: Tue, 04 Feb 2025 10:22:58 GMT  
		Size: 7.7 MB (7669362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b489edbda41a57517e3aa2211157756cd4a998ff40b48e2ae2b4ea4082aeeefe`  
		Last Modified: Tue, 04 Feb 2025 10:22:57 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d453a71279f51a33275b104128b0ef32161442779adfc2eca21e932784dc76bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.3 MB (130281606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9ebc683d6a2e74f3f6523b76e88dabbcd91ef15a5b3f5ded12eb0d86431ca1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:105ec2fcec8ae42e2b6cba4c3c8463bdd5ad21cffe232e9cfd7ed127e7ede3fa`  
		Last Modified: Tue, 14 Jan 2025 01:39:08 GMT  
		Size: 44.6 MB (44580459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881cf44810c526c17319a679eee937276e08c6767dabc96ffa22308bd53f7e1e`  
		Last Modified: Tue, 14 Jan 2025 09:00:07 GMT  
		Size: 23.8 MB (23806747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c787837970fa306cc5256b55f5173664552e3e16eb197389ac0c21aca92a24`  
		Last Modified: Tue, 14 Jan 2025 16:18:41 GMT  
		Size: 61.9 MB (61894400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:375bd3b5de1e4ce62154a317a2eedf0fbbc645ba28a336dfc7f57083debea352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7635007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea55d1a9628c01c5e7ce251049e6ccd4398382e087631485ad1c0e2193be47e2`

```dockerfile
```

-	Layers:
	-	`sha256:6bb2101881c8c8c0ffd4bc5a8101bf663900fd2aca831c674d7a718df973f6cf`  
		Last Modified: Tue, 14 Jan 2025 16:18:40 GMT  
		Size: 7.6 MB (7627633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9ae19583f8bb3be289a75674345c6ef019990014243072a9ab03287e1490e6d`  
		Last Modified: Tue, 14 Jan 2025 16:18:39 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d70a8d9b484c5a769d008f881b427c8ecbce176197d8464dbecabe3acc2f5ecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141189718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae5585f17239bb791e7d4137500f2b26d5bbe9857b7c3b81e66b75e1ae44a32`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:53cf00e5414c63ec005c43ad8342c8e55028d137e29e95d889d4247b0586d248`  
		Last Modified: Tue, 14 Jan 2025 01:38:51 GMT  
		Size: 48.7 MB (48661509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6216ff9e1bca52cad6d9119375ff8a9fe28c8b52c130d5380d5ded38210e688e`  
		Last Modified: Tue, 14 Jan 2025 07:01:19 GMT  
		Size: 25.4 MB (25426483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab5443d60c3808485433bb956012bfe58b69cebf352b638a921b47918c7b109`  
		Last Modified: Tue, 14 Jan 2025 13:33:15 GMT  
		Size: 67.1 MB (67101726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:71b473c988201a15d0e20854c52a1e6f719e17af81f6b027cb96157e56a1d0eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7642809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a2500c367298cd1fc64543c18629eb985446986c8b845641b92ccf0347b2d2`

```dockerfile
```

-	Layers:
	-	`sha256:0c061376a90509fe3dde2e194e4939ff029461fcc3800e0f40ae80e36a483e6d`  
		Last Modified: Tue, 14 Jan 2025 13:33:13 GMT  
		Size: 7.6 MB (7635416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4308ad8e7f7805b5fd297337cf6f2cde3691af0c299efa78aa756c4c035d0284`  
		Last Modified: Tue, 14 Jan 2025 13:33:12 GMT  
		Size: 7.4 KB (7393 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:1ed16b0936c8407a72004889edad80759c99e5438a9a70e386b7ae83319f60b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.3 MB (146340563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f95befdc782b90fc6a9406d931871ece11c0fa8745cc0f868e5a054e49bbc0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f6eab4c65eb241da9efbcd7f3af754621262244b11cdb15579a1ffe95621258b`  
		Last Modified: Tue, 04 Feb 2025 01:36:50 GMT  
		Size: 49.8 MB (49751669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f716b567c64e0e309015fd1a02f5a6cc44d9337e2d33b9f6b8078b32a497ea27`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 27.2 MB (27187291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4913bde8dd9201a45eb15eecac64dfe0033ec3938f3fffc5d62cb37095ca1ed5`  
		Last Modified: Tue, 04 Feb 2025 05:15:41 GMT  
		Size: 69.4 MB (69401603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7c444a74ef507e91e25d322d7a1b1810d0152c6086cb9217466eac67f8718923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7665717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b7ce1fcd892fa25e8af962edc78a25e4d9b016b6647ea39c5b7cabf5d7b532`

```dockerfile
```

-	Layers:
	-	`sha256:a2408e37c2fa9db1a5073eac5690fc938e92771f4870a803b110f295386963b2`  
		Last Modified: Tue, 04 Feb 2025 05:15:39 GMT  
		Size: 7.7 MB (7658425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f03c5a7cb4320006cf4ff2e0e0755de4671f7f3552f66c41de44623e306df771`  
		Last Modified: Tue, 04 Feb 2025 05:15:38 GMT  
		Size: 7.3 KB (7292 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:4542f8065a818db739219a01e1b40b60efec5afadfcc4529d720a912a39ab61b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.3 MB (140293949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70012defa400db789835b3fce6a207e007f4872ca46448489c6c0af0fbb96add`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7fc12d8a734ed45514ae5135503d718e9ff7693017677de649ab963638a639fe`  
		Last Modified: Tue, 14 Jan 2025 01:37:16 GMT  
		Size: 48.4 MB (48390219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0115509fb5cc85eda38403b37d75aa0d68bc08deb77a8f9d926a1f8c06d921c`  
		Last Modified: Tue, 14 Jan 2025 18:14:22 GMT  
		Size: 25.9 MB (25926715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ed8eab45779c4caaf48a3dd1f3e53c5b4079b75e32b657bac3bdc07a0f1e4b`  
		Last Modified: Wed, 15 Jan 2025 02:07:24 GMT  
		Size: 66.0 MB (65977015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7cc83ae9e313ec8a4b0f9dee34a4c9c2af59dcda58e3a038fb4c36710dee4a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd3378118053b582710f3fff850eceaf69604c78fa7b42fc57a97a2a20686e2`

```dockerfile
```

-	Layers:
	-	`sha256:4ba40c128050744b384986d01d36e73805b787370c0dd4fbea02fcb7fd83acb3`  
		Last Modified: Wed, 15 Jan 2025 02:07:18 GMT  
		Size: 7.1 KB (7147 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:fcce0daab7df71c0a4d24ed7b777c4ad2f8e4e07c45ac14ca2f0984222d32abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152098758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4dea55014e43fd29a446e2658ddc4573c27a9139ba114d7a6515a269fd6e4e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:826e70a2bdfac0f05c49b7611afcf30a311c862a1beca6fc4059e4b6cd0e1a4a`  
		Last Modified: Tue, 14 Jan 2025 01:40:51 GMT  
		Size: 52.0 MB (52043133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f126b14e556a94eaec41c5a29f9164224f92b1080c74dca2491c3f7b9120c320`  
		Last Modified: Tue, 14 Jan 2025 05:32:11 GMT  
		Size: 27.5 MB (27531238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7311c304e2cd2735e9d0f4a75554811f3be94be0d57e4fd8ff5989c485af8c30`  
		Last Modified: Tue, 14 Jan 2025 09:44:47 GMT  
		Size: 72.5 MB (72524387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a001f2f6032e4930c80eebb2260702f3186b60b4d076204054369677f2e582d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7647664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff99e2b1587ec2a5c003050bc95171349435c39da73c56936d00f2a3ebdb3141`

```dockerfile
```

-	Layers:
	-	`sha256:64579d1288b78c8094cfe263e14ab072d6d69bfced7f13b129680dd8bfb1a06a`  
		Last Modified: Tue, 14 Jan 2025 09:44:45 GMT  
		Size: 7.6 MB (7640318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ba8f2daa2f44abd8160ed1034994c1d4c473f6eab21718fe570387334939b62`  
		Last Modified: Tue, 14 Jan 2025 09:44:44 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:841b670efa888fba12f3ca424d021bea46e276c2a406876d2805ebd30661cad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.2 MB (144183374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a538ed29c23de0033afa76c98443583277d7e4f244f6de7b22975a716779870`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5071fbe67e05b7dce13c72a6b655c4750a6b0653fdce60a9071966d5a747a2d8`  
		Last Modified: Tue, 04 Feb 2025 01:42:04 GMT  
		Size: 48.4 MB (48414760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2748bb8f4316900467409f846adce939a746b7f2adbe1e2ba340715af7fac142`  
		Last Modified: Tue, 04 Feb 2025 07:31:59 GMT  
		Size: 27.2 MB (27216186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9371642bbb4f2496e43eaeaa75efac59f54344b0c0beee1184503290cbf7343a`  
		Last Modified: Tue, 04 Feb 2025 11:38:14 GMT  
		Size: 68.6 MB (68552428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0b3506d5e6cc98bbe1f6132732531295f20e63be600a8132ce4f9e43c8b7f28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7676823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099bc7a3a7b814638927fff3374f349bfee6919065f69fbd17ab7afe592ae384`

```dockerfile
```

-	Layers:
	-	`sha256:9c9e3a34680550da80f6d8ed94a748afe42e82068c2fd150cf281d40fa61cba8`  
		Last Modified: Tue, 04 Feb 2025 11:38:12 GMT  
		Size: 7.7 MB (7669509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da0d790adc26bb3f35199a82b70f773864a308950b877536a295c0a79358143f`  
		Last Modified: Tue, 04 Feb 2025 11:38:12 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:7da2563d1257a09047d12c4b93c3cb98844f223a76f96290544d0476d9356002
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
$ docker pull buildpack-deps@sha256:a89441871a4e4261cfd8f3db1076ca49748dc17d638a043d1c23c6a10c831e0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.3 MB (378286862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec553f6acd4da30811d4a22121cf15fce8f4361e3e5bbe4ff4aae0487f625fa1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9a66d07ec06276723a9d844f79110db2c04e99b6e7ca9f2467ee7789a25614bc`  
		Last Modified: Tue, 04 Feb 2025 01:36:30 GMT  
		Size: 48.5 MB (48478504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37249eb6f9b3505b2330ba5132b480155ccfe125c06c5def806fca9a9daeec74`  
		Last Modified: Tue, 04 Feb 2025 04:37:52 GMT  
		Size: 26.0 MB (26036380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e4fa6b03ff4cb7e858ff5a14c844d64841c23889c0d907ba3b0dff91e9902c`  
		Last Modified: Tue, 04 Feb 2025 05:19:10 GMT  
		Size: 67.5 MB (67468344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79a80f133f68fe6301288293c6c55d0abe1750139940f392c2541c7856dc954`  
		Last Modified: Tue, 04 Feb 2025 06:14:31 GMT  
		Size: 236.3 MB (236303634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ef63815fc34fca45ace31b1a537fc01d787def667cd47e3f20bc2902cd988a1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16918509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d95b29521e7e9a9cbfad7bd2bf2f0c60feb61981efab1c979b548d099c1d258`

```dockerfile
```

-	Layers:
	-	`sha256:abbd56d590bdbd61585fbf3c94dc21f612324f29bfcd68e78cdca9969520472f`  
		Last Modified: Tue, 04 Feb 2025 06:14:28 GMT  
		Size: 16.9 MB (16908333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:642f9f638d888a947630031a8911443c6dfc2339e5c8eee02b7f95a6e283e06e`  
		Last Modified: Tue, 04 Feb 2025 06:14:27 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:bc797efcc1bfb1580fc82fef2235b5ae298f3c1a39da7bc1e3284a089c152205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.5 MB (342450921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4454bda53f727cd002c420b50b5434bb0a09863c78197e6fa36bd5dd1665a040`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:969faa28a060b3165779eb5369b5e31931290ad408fa4e8e60d177e2f80c2611`  
		Last Modified: Tue, 04 Feb 2025 01:38:51 GMT  
		Size: 46.7 MB (46706175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd2fe3d3c4202f31101bc1bc73cd3af8a62f52a1188e729c8a3228780cf83d0`  
		Last Modified: Tue, 04 Feb 2025 08:03:51 GMT  
		Size: 24.7 MB (24746488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b0ffd764a137045323ce5b430a010c0f27d927825897343bc94eb266304a12`  
		Last Modified: Tue, 04 Feb 2025 10:21:56 GMT  
		Size: 65.2 MB (65167643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8315467ee71a8ad5b2dec12ccab0e7fceaaf53e524d175daa1d5cf08d233072`  
		Last Modified: Tue, 04 Feb 2025 11:45:34 GMT  
		Size: 205.8 MB (205830615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:16dad910d55c70dfeba9c305910e8bbae19182f85b9380b16fddc7878158d74b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16687959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1ed49a8170d29bc351d2875938957f1037cdc6ff9d7545fa23f2fe1b181fe47`

```dockerfile
```

-	Layers:
	-	`sha256:19357ca9bf0b78bf8c5485b1935cb1fb4a1b0648d36bec0ee73d5b6072b898ee`  
		Last Modified: Tue, 04 Feb 2025 11:45:29 GMT  
		Size: 16.7 MB (16677723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c95894fead5209f44c8c99d0fd361dc9405cec026e929f9bf97f45e260a7640`  
		Last Modified: Tue, 04 Feb 2025 11:45:28 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fe578c1e871363d504bb8bab30736288c85647392e992202c6258e71e2f02462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.9 MB (327929744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51c46e692bb0a4dcb234fa5110bc74dbf398d106e8bf1908c30f71f200c22f98`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a0e0ff4d5bcbd6e2c25332ca46ec757661e665f67ef593a6f9b269659d2aeab0`  
		Last Modified: Tue, 14 Jan 2025 01:36:57 GMT  
		Size: 44.7 MB (44668351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6de100729dc42fca6e1da779a5cabf824cb59902a2e776e84fe6b7124d28a0`  
		Last Modified: Tue, 14 Jan 2025 08:59:23 GMT  
		Size: 23.9 MB (23876812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c133cb44b43ce8e0628b481f6d32820f19b92bbcee07e7706966c203b607284a`  
		Last Modified: Tue, 14 Jan 2025 16:17:30 GMT  
		Size: 62.5 MB (62467463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9795004ef2c293073508c69f28eb42c2d7b2f33f65dae4735b067629f5120204`  
		Last Modified: Tue, 14 Jan 2025 21:59:24 GMT  
		Size: 196.9 MB (196917118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e83811cfe7c760f9da87d6f1c5a150ea9a0dd21ade505b732fcdc8e7f0fc842b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16669569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e59fd63dd1941542b79def3463a82f3d0501a82065c295a5f9fdcb14c59198`

```dockerfile
```

-	Layers:
	-	`sha256:73f47150d048eba6124064fe6305a459362e7b0775142ef28c837992ad3c09b0`  
		Last Modified: Tue, 14 Jan 2025 21:59:19 GMT  
		Size: 16.7 MB (16659333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3eaa593dc99f801f19eba455556f9adb976b1822e75bc2877fe1dc8719fa838`  
		Last Modified: Tue, 14 Jan 2025 21:59:18 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:789f10d38342832bf75ef3e2b9ee9f29c017fac09a6f868925fe21d87a81f7cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.5 MB (372546196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e83d3f56d50bf5b5f068663d981200a5154d5a23a3d0c7bb6402edad1f5f64`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7cef9546887caee4cb752860ee90de96728f638ede0f77bda226ca44ac3e04db`  
		Last Modified: Tue, 14 Jan 2025 01:37:16 GMT  
		Size: 48.8 MB (48760872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fc550a04d72fdc48fc4716034190ede3de291a338b2c748b32584534d2c3f1`  
		Last Modified: Tue, 14 Jan 2025 07:00:48 GMT  
		Size: 25.5 MB (25487312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97035a0dde45440d902fa525c75a16c6689c0105aa65885137511ec2d09218fb`  
		Last Modified: Tue, 14 Jan 2025 13:32:31 GMT  
		Size: 67.5 MB (67473976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68415822cccaa14224085f576cbd5da670da2f1a5ddec7d638f697742f5d0fdd`  
		Last Modified: Tue, 14 Jan 2025 17:12:06 GMT  
		Size: 230.8 MB (230824036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a9d60646ee171c4bba05f9cc204056ad1c63baeeab442bfdb1f4eab411b29c2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16987901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc196fdb5c8549d2f62aff178e0847779860dbadc42b2b180f89b418ce37f93e`

```dockerfile
```

-	Layers:
	-	`sha256:6d0948f13d2062aca9845321a479880fb218c0b6ff7f1b94ac1794b6ff823c72`  
		Last Modified: Tue, 14 Jan 2025 17:12:02 GMT  
		Size: 17.0 MB (16977645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d591e35d33d3cfcf7cf730fcc9b68431bce541892eea719c801528f64c8f264`  
		Last Modified: Tue, 14 Jan 2025 17:12:01 GMT  
		Size: 10.3 KB (10256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0a346c8030f310001211274abb71e5c9c2279d293b63c22819e742b69a6c8532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.5 MB (386542332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877c96aa12281c5fd8180613fe153cb1b495b5ec73f62325e544bec45ba0ca20`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:51741382468681fc53992e03a5e8ce7f591198e39599d81f3b698e3652a63db4`  
		Last Modified: Tue, 04 Feb 2025 01:36:41 GMT  
		Size: 49.9 MB (49883916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4227754a1dcb648ed5c4c8f40f8d60f655bb96ef669b5da48ad50132dc9621`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 27.2 MB (27185942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74bb38fe259cd8a9e1ef2a45c45f0372cb16ddaf5c5facf3363ca9cfcede2c4d`  
		Last Modified: Tue, 04 Feb 2025 05:15:50 GMT  
		Size: 69.4 MB (69401812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e8429ab45660ec1d3a19982bbd0af3a786637fa24a29bbd4fe03f5d823ef2b`  
		Last Modified: Tue, 04 Feb 2025 06:15:15 GMT  
		Size: 240.1 MB (240070662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a856d0d673b5070a08ba0ef1a694cbcefafc2e847fe62a0db8908c9a890af238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16887333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bc2715ad9648f547ef50c6f946121d126d9bb8ea48f75afe0d30f539576721`

```dockerfile
```

-	Layers:
	-	`sha256:7228efcf52a85711aae46c80cce5e57101b9b21148249ea6e908d113190a5814`  
		Last Modified: Tue, 04 Feb 2025 06:15:10 GMT  
		Size: 16.9 MB (16877179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe4bb2dea9acf4e5f3939bebdc437405c35beb7e0d1876c48b51faed87418e36`  
		Last Modified: Tue, 04 Feb 2025 06:15:09 GMT  
		Size: 10.2 KB (10154 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:c3af075a6bb84a32799c35580e83b5601f890c8d940db050505b4dc6c8a93321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.1 MB (360106862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:969cf85422af15790fa0a4564ead6c8e64cd05059f896b02da84563dda047911`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1ad11d2c3d2c0479cee56b824f2514b710c0c76d88c22da7ef5ec7f2ccc527d0`  
		Last Modified: Tue, 14 Jan 2025 01:35:17 GMT  
		Size: 48.5 MB (48545883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7625cd98aa6d5c80fb0d1f627561581568ea6f268919dc1e831bfca9d1e853`  
		Last Modified: Tue, 14 Jan 2025 18:12:26 GMT  
		Size: 26.0 MB (26040345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d41982939111491c6252a19353da998fa5ef416acfaed05792f55a462ab11e`  
		Last Modified: Wed, 15 Jan 2025 02:04:08 GMT  
		Size: 66.1 MB (66119517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3de884e734576434f49639f4eac10e8ea4a8319859bf9f4ddab2b2535f94676`  
		Last Modified: Wed, 15 Jan 2025 18:07:13 GMT  
		Size: 219.4 MB (219401117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:98d12704efad8167ae328c80f2b65f7537104b8eb6d65dcb91e8169be51a56ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f78aef405075ee21b5576e2cd9614944b32c443a23c800108a83b0b40e8263`

```dockerfile
```

-	Layers:
	-	`sha256:be2f46aad2ab5b0965a4dcc567ad80fe2f0180465992cbaf83183ad959cc15fe`  
		Last Modified: Wed, 15 Jan 2025 18:06:53 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f945636514ae3362ca71164884853f2f404b1119ca45926602f12d477155a9ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.4 MB (384371887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0546df0594a9cf5437bf0c515631731c6d736876e68e9daaf7b025bc56efdd46`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fca4ba78a63cac2994d6f3576656e907e3a130a20f935b6a1e2c945c9e7be3af`  
		Last Modified: Tue, 14 Jan 2025 01:38:04 GMT  
		Size: 52.2 MB (52151887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f2cddc488774629199c39c9010734d4be824e6ca934835a5e2d444a85e0075`  
		Last Modified: Tue, 14 Jan 2025 05:31:14 GMT  
		Size: 27.6 MB (27591847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97154d7b719fe3158c773c51a570d7d8ab1e54dcb04c12ce4e93476ca16bbefc`  
		Last Modified: Tue, 14 Jan 2025 09:43:30 GMT  
		Size: 72.9 MB (72876836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6943e22d3036deb30248e5634a993ff72c73507d02437a5bb09280b60bf18d6a`  
		Last Modified: Tue, 14 Jan 2025 13:04:19 GMT  
		Size: 231.8 MB (231751317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f65afdda5fbd62f678db83abfa2fe8e77dda067ff81471cd5b968084e06b0463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16889169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ee6c8a1fa836d956d9ca48a65ac8f826a5d616d3bd16b7c2e016175f840e92`

```dockerfile
```

-	Layers:
	-	`sha256:2fce16de76b13f416770a657209c2106c50c3ec4ed409e55241d96278276993d`  
		Last Modified: Tue, 14 Jan 2025 13:04:14 GMT  
		Size: 16.9 MB (16878961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82b4b42020474e39ceb70591d326ad42b7fd3699657c3881062386d87d8f34a3`  
		Last Modified: Tue, 14 Jan 2025 13:04:13 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:3639f13190096719aac7a54bedfd4e09b26fc0dd2a909639e7cf0a3fd33ba631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.5 MB (460506022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e888d6f05533ef4be30c9b22e055cac880d4bb0df839b638fd86c8a2bc90772c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:41a19e48936e10f226b6bfe61097156b74f03101f788496e8860f0d4806f05ba`  
		Last Modified: Tue, 04 Feb 2025 01:38:33 GMT  
		Size: 47.0 MB (47040914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a706305f90a9f6f5a4662ef1063ca9b1d12e77b9f1482c3925294e4989eea2f`  
		Last Modified: Tue, 04 Feb 2025 04:38:37 GMT  
		Size: 25.4 MB (25411970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2279830c9cdcc3d6d50a4a0308903e5819e1f53fc61863f2bc9dae664a4b8e0e`  
		Last Modified: Tue, 04 Feb 2025 08:09:05 GMT  
		Size: 66.5 MB (66493760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0674f07b14526b99d8a1ad6e260fa13f5923299979b4990047db0a18f0e7754f`  
		Last Modified: Tue, 04 Feb 2025 09:50:26 GMT  
		Size: 321.6 MB (321559378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2b8df108a10b1e88d6b87824249ab1fb77f1b9afd698bc50f1911e8450899dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16974645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca31fb4b8ab775c0c89f10c2d00db316af5da9f635cec87da6421dcb44f602e`

```dockerfile
```

-	Layers:
	-	`sha256:844d407e0f895e351a3eb25d6945314331d6d457cefa01ea0b3de0ce8c11ee63`  
		Last Modified: Tue, 04 Feb 2025 09:49:44 GMT  
		Size: 17.0 MB (16964438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd8f8a3c148cbeea3b0e96dd11781e968a527ea4b64c2fd01544e28ce3ff8eba`  
		Last Modified: Tue, 04 Feb 2025 09:49:41 GMT  
		Size: 10.2 KB (10207 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c93ead5df32df5fda7821d7eea3245b3ad1fecf33ab58a7fbe75672128d2a94a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.8 MB (350769776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63bf6ddec63e07aaf55bebcf801af659826e992e4b6344ef4f3fb7b0f56001f1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:98a334b3a419c858b25979b9c4fcf97a87431d5b5cddfa6c4c566454b23fcf62`  
		Last Modified: Tue, 14 Jan 2025 01:35:18 GMT  
		Size: 48.4 MB (48434824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d732c90ca5b141c789480c7eea03644a6f254edf6c95ed1e124a245a18b8c3cf`  
		Last Modified: Tue, 14 Jan 2025 05:00:30 GMT  
		Size: 27.2 MB (27196670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c226835589caa484a321d0762131f155a336675c8b326b2fb32917038d1fe871`  
		Last Modified: Tue, 14 Jan 2025 09:11:02 GMT  
		Size: 68.5 MB (68532734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2ee3ebe99142809d95638070bf937a25f6487ab59250faa71ded6bbcd0dcf6`  
		Last Modified: Tue, 14 Jan 2025 11:17:51 GMT  
		Size: 206.6 MB (206605548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dd84808ef735ca84f852e884ede3f5d30f494c30ebdfcfac6d4acb304edcaefb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16682803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcba902ca02bdbd2fa325c971ad0d962569c31f8134d6bf80819cdd45ec97c3c`

```dockerfile
```

-	Layers:
	-	`sha256:33660ad64d7fe7f55455954a254a4ba36f59ffc22e0fc691fa83f9ce752069e9`  
		Last Modified: Tue, 14 Jan 2025 11:17:50 GMT  
		Size: 16.7 MB (16672627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69c6b274d24546c7f80941c17f12b7dc21cf3a4af00aa222a43f2173c9504ed9`  
		Last Modified: Tue, 14 Jan 2025 11:17:48 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:630da0806dd470371eca4a7554b6ba283509fa5e3af909ac5ac98b8958add90c
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
$ docker pull buildpack-deps@sha256:f638ef05d64605d170c445f4dbc6194cb452a48dd22e37b7c512306d638fdcc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74514884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3caddad04e472fcf3574c79b97ef9b2c377554176ebd3c85ca858bcbb8bdda2d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9a66d07ec06276723a9d844f79110db2c04e99b6e7ca9f2467ee7789a25614bc`  
		Last Modified: Tue, 04 Feb 2025 01:36:30 GMT  
		Size: 48.5 MB (48478504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37249eb6f9b3505b2330ba5132b480155ccfe125c06c5def806fca9a9daeec74`  
		Last Modified: Tue, 04 Feb 2025 04:37:52 GMT  
		Size: 26.0 MB (26036380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a5a03516c213b8395285411f64ab7e53b1a86f5a65de46a7d95fafb667e0d8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4043601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06af5378da6fdf718d35cb019e89f718b729a813ce8b83c506ee8a802ae4d389`

```dockerfile
```

-	Layers:
	-	`sha256:477cd3c19a37ed7a9ee13a81ff3da27cdcf9e27851258611a960eefd4f3e73ba`  
		Last Modified: Tue, 04 Feb 2025 04:37:52 GMT  
		Size: 4.0 MB (4036797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2f10ad7261a54ee4f8c56a579b66d638edab808a52504248debae6df278b9ac`  
		Last Modified: Tue, 04 Feb 2025 04:37:52 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f45875ec73ce9b7c8aeb688b988e4dd79e4b6c842cd21b893b5f398a492c94ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71452663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b92a325e484088d0c8688eb6aea68ba80bc45eb8aafc520d1518ed29e7fe90`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:969faa28a060b3165779eb5369b5e31931290ad408fa4e8e60d177e2f80c2611`  
		Last Modified: Tue, 04 Feb 2025 01:38:51 GMT  
		Size: 46.7 MB (46706175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd2fe3d3c4202f31101bc1bc73cd3af8a62f52a1188e729c8a3228780cf83d0`  
		Last Modified: Tue, 04 Feb 2025 08:03:51 GMT  
		Size: 24.7 MB (24746488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8134fda17aa6d80f9759a5952f0ffeae4602704b27b326298b638578d10d443c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59fbe16f31e28338f95f054b58a4401aa744e22829c9917e4841dedd2e5ab5a2`

```dockerfile
```

-	Layers:
	-	`sha256:c4e2ff509be119eb73702d3d519a72531f576a70f9908862c43a7786492a6d96`  
		Last Modified: Tue, 04 Feb 2025 08:03:50 GMT  
		Size: 4.0 MB (4044425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe41ba8a61745b055d7c1ff4fcead3d482410c8dc06a548e6382e5c4c140e1aa`  
		Last Modified: Tue, 04 Feb 2025 08:03:50 GMT  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:feb9c2d61fb4c4c7b0252883717ff509c78811124a512a8ce3ecb9807979175d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68731225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ba6aec6b23b2b51d61ff1c09d4b883bd1ccf368730e25c946e90282a46f6033`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:eaba0613b673e68ada7f5f2b5e4971d3556823043148e63c2a6887ee2d5edef0`  
		Last Modified: Tue, 04 Feb 2025 01:39:12 GMT  
		Size: 44.8 MB (44838928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6395c61799d55a9640c01c9ef3b8549d20d61a975f9340e0353ec8e6422685f`  
		Last Modified: Tue, 04 Feb 2025 10:43:02 GMT  
		Size: 23.9 MB (23892297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fd556847f4ae2a75b56788585a6dbed042bd64bebdf265e9ad9a60375b4529d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4043885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb443e4c1924cb01c661174585062ed0e2396c690d9a227622c118244322b84`

```dockerfile
```

-	Layers:
	-	`sha256:7a16946bcda3770000ccad1fec8abad756c10a59958b8efbc69b478d0a12a6a3`  
		Last Modified: Tue, 04 Feb 2025 10:43:01 GMT  
		Size: 4.0 MB (4037021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbd45c6d9e9057c1679f44da49613d30cf0a4b169f2b71b52dbe6b2392d94da8`  
		Last Modified: Tue, 04 Feb 2025 10:43:01 GMT  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3cf31dfb3b9a512d37f417618dc8d2c709472b36c3d7493768dcaa9a394e0b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74377354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc13d99c12b3cd6acb985c585b0342c53dd123416f363f2d506091c48cb376ab`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f518c8f510cd10fda797c5ee77280d7c81b61ff1077c267de12ce9c337ddbe7b`  
		Last Modified: Tue, 04 Feb 2025 01:39:15 GMT  
		Size: 48.9 MB (48874714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b09bd24e474d679cb3c70ae42560294c37e17235d92a739791f20279494fa5e`  
		Last Modified: Tue, 04 Feb 2025 09:01:04 GMT  
		Size: 25.5 MB (25502640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b762f13089947f528337b22e97a2034d96f4970fb44b8514f374c981f492adb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4044577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2924e69ba8c13f46c71be66ca59a7404e757deedae5b1d977d6d35cfdfe739d0`

```dockerfile
```

-	Layers:
	-	`sha256:e50add4bfa70921343045e27ae494c4ba6b21657d3117a96e9e96c8f3143af4d`  
		Last Modified: Tue, 04 Feb 2025 09:01:04 GMT  
		Size: 4.0 MB (4037693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:accd7297c44bb051bb6828c0c99e27d5fcba3fe49d95e31fdc9ff6b84e6b2fdf`  
		Last Modified: Tue, 04 Feb 2025 09:01:03 GMT  
		Size: 6.9 KB (6884 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0f50343f2052ca365fd8378a57d6e415675836af02416da168be148c36f4b236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77069858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e0fb9d10924a5ef45ec45f9c72c8b720d45649556a48e0328c36eff1c0af02`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:51741382468681fc53992e03a5e8ce7f591198e39599d81f3b698e3652a63db4`  
		Last Modified: Tue, 04 Feb 2025 01:36:41 GMT  
		Size: 49.9 MB (49883916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4227754a1dcb648ed5c4c8f40f8d60f655bb96ef669b5da48ad50132dc9621`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 27.2 MB (27185942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:69d9c63d976a1d2ec4df4b17cfbe241837c6d3fa77e82c0ae0239bc737f75989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4039334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dbff316c1752c79b0991fef1767dc049c843f8e4a6d26117434c6b95b5ec6b2`

```dockerfile
```

-	Layers:
	-	`sha256:80121ec0759de207705a8e6b0a5f2635b3c614ec56b2e4172a71cec99f8f701e`  
		Last Modified: Tue, 04 Feb 2025 04:23:41 GMT  
		Size: 4.0 MB (4032552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07ad54558e3d4158f6d4b0dc6bea4f73a317cde2c777f58a1128b0e6db038b16`  
		Last Modified: Tue, 04 Feb 2025 04:23:41 GMT  
		Size: 6.8 KB (6782 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:a11806098d728722edfd2ccc5eea62b183a99295300cc26c512aeb6ec5139688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74586228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df50432b3d5ec0d47a2f773ac1995550ce8a39eee1472f22dfa6eeb27139eed`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1ad11d2c3d2c0479cee56b824f2514b710c0c76d88c22da7ef5ec7f2ccc527d0`  
		Last Modified: Tue, 14 Jan 2025 01:35:17 GMT  
		Size: 48.5 MB (48545883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7625cd98aa6d5c80fb0d1f627561581568ea6f268919dc1e831bfca9d1e853`  
		Last Modified: Tue, 14 Jan 2025 18:12:26 GMT  
		Size: 26.0 MB (26040345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c1c4ea9e5260c374212eb1c5c7c2df5c612816c7260731a54415f310a87b225c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 KB (6637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e443da628babc958694dcf5f479e2146d07dbc4aa30f89627fde7e1994fb90e`

```dockerfile
```

-	Layers:
	-	`sha256:0fbd0b7dbca6501003c60a441261b32562fb2857b68853b4327ebb9c5e316444`  
		Last Modified: Tue, 14 Jan 2025 18:12:23 GMT  
		Size: 6.6 KB (6637 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b444e034fcd78a58112ed02d5089c9ed9523c0bcfeb72959d9d38b5e76918c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79881843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef59a3f5555ebb3a1ed91d3955dfa71dff4e43bc9f33b75541cb5c1d31ac0961`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:20ee406f6988f44113bcc71bae5adfb439e360c88b767260000751228a498e00`  
		Last Modified: Tue, 04 Feb 2025 01:38:35 GMT  
		Size: 52.3 MB (52287301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089b8eaf628cc7675b29225b3b455c5d86d2c6a1f5fa29d78dfb7f3bfa69b3ec`  
		Last Modified: Tue, 04 Feb 2025 07:25:22 GMT  
		Size: 27.6 MB (27594542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:104cc649b82b1e77cbd6184495b219156bcbf219aafc3ffa91c645b37c7397a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4052300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa49d461d527f74f3e9579c6ffbcd86bb78f64c91f1a79b6e24c087d80118384`

```dockerfile
```

-	Layers:
	-	`sha256:06ac9900b3736f9ef1743b06b377a584edf329ccb407da2e23a82060d06fbff4`  
		Last Modified: Tue, 04 Feb 2025 07:25:21 GMT  
		Size: 4.0 MB (4045465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb608baa041b04181310aae0975ae61d6de897858f601e0a076a01d775590fd5`  
		Last Modified: Tue, 04 Feb 2025 07:25:20 GMT  
		Size: 6.8 KB (6835 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:2734aa4dea895af92674c6244686355bcfa7c5f532af30ab2ccd9a106e755945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72452884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b17487fc2e48d4719f558a2b395daac4854c5cc8027f11e20fc0a057d484f87`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:41a19e48936e10f226b6bfe61097156b74f03101f788496e8860f0d4806f05ba`  
		Last Modified: Tue, 04 Feb 2025 01:38:33 GMT  
		Size: 47.0 MB (47040914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a706305f90a9f6f5a4662ef1063ca9b1d12e77b9f1482c3925294e4989eea2f`  
		Last Modified: Tue, 04 Feb 2025 04:38:37 GMT  
		Size: 25.4 MB (25411970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:44623c62d8dedafe11ab33444dff3d267c0b5a8cbf31207f2b7ea43d5854da5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4035021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d21dab2b6e78a3bd7ee008870193435baea98bbc4121d11d2482fec4e3e7e14`

```dockerfile
```

-	Layers:
	-	`sha256:dd80ddface841cec8633795f62cdd6ea9def4ba807b88f55db178fced191241e`  
		Last Modified: Tue, 04 Feb 2025 04:38:34 GMT  
		Size: 4.0 MB (4028186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:541368828ce448681a506ecc6bf3db770febf0bada8ea05ff3b963e42b1f3d0e`  
		Last Modified: Tue, 04 Feb 2025 04:38:33 GMT  
		Size: 6.8 KB (6835 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:171e8794c6153ede3b2dcd344446533bc1d8ea6b0b18282773719bc84686f7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75775246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63fe77152201f7c14106126b989c319db82ddb59047e1a6ed9a845747d8d6239`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1f48ea4a277664853f54eabe6340c7571241c845468906404bbb1efd60e69807`  
		Last Modified: Tue, 04 Feb 2025 01:38:18 GMT  
		Size: 48.6 MB (48560783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1f7d849459507f8a608795416d02b409e9f01c22159fa5acaf53ea0891b503`  
		Last Modified: Tue, 04 Feb 2025 07:31:13 GMT  
		Size: 27.2 MB (27214463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:87d777a50cfb26dc4d318ba34304296d2a7dfc51aff23790a64b8bf9d8c268a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4049932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68bcddd9e386b9d03f6814425470a8ea110334e24aa94511ea90bfc36742ec67`

```dockerfile
```

-	Layers:
	-	`sha256:9cba160456722d8e64ad7d4fc68cc65901918c0c5bca0dd5108b22cae6340e15`  
		Last Modified: Tue, 04 Feb 2025 07:31:12 GMT  
		Size: 4.0 MB (4043129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6b747fbcbe0026e5bbc6fd98c53854cdf3b2e96844372ef3cc2b6170266f168`  
		Last Modified: Tue, 04 Feb 2025 07:31:12 GMT  
		Size: 6.8 KB (6803 bytes)  
		MIME: application/vnd.in-toto+json

## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:20c246ac9a42995c023ae7e4a72eb7f2584d01fde39596b6afcd9b5a821c619a
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
$ docker pull buildpack-deps@sha256:49050b174b7c280c7397a668862e7b07e65d41029fffd9a4289f0ba89f51830e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (141983228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de9e7ceb22c36a43a1fe888d57519e4006cca29fa80a1a9bbd024ae5aa7a57f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9a66d07ec06276723a9d844f79110db2c04e99b6e7ca9f2467ee7789a25614bc`  
		Last Modified: Tue, 04 Feb 2025 01:36:30 GMT  
		Size: 48.5 MB (48478504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37249eb6f9b3505b2330ba5132b480155ccfe125c06c5def806fca9a9daeec74`  
		Last Modified: Tue, 04 Feb 2025 04:37:52 GMT  
		Size: 26.0 MB (26036380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e4fa6b03ff4cb7e858ff5a14c844d64841c23889c0d907ba3b0dff91e9902c`  
		Last Modified: Tue, 04 Feb 2025 05:19:10 GMT  
		Size: 67.5 MB (67468344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:36ce389bcf9326720dbf7ecbf7a2a66e2953fbc3a32824120544ffc68c1a1f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7666507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7fcf6cb261b3b8b8689b31075e7690f118d26a8b64a4ab267a858e5255a765c`

```dockerfile
```

-	Layers:
	-	`sha256:18e8f73b18c7f8320da0a5c85645371cd9b3056ba3baf871fe86c4167ab951f9`  
		Last Modified: Tue, 04 Feb 2025 05:19:10 GMT  
		Size: 7.7 MB (7659210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20734c0cd4a50db3c1fe6185badc40dcd0819cdd78875967da043713cbe216fc`  
		Last Modified: Tue, 04 Feb 2025 05:19:09 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:84e24c852d00a207988799b1ad4a7cf719bd43f200246dedf394b1cb43ffcede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136620306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f68cffa395db19a15f11e2e54c002061f0eb04cf08a399d55f3be0d0214dba2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:969faa28a060b3165779eb5369b5e31931290ad408fa4e8e60d177e2f80c2611`  
		Last Modified: Tue, 04 Feb 2025 01:38:51 GMT  
		Size: 46.7 MB (46706175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd2fe3d3c4202f31101bc1bc73cd3af8a62f52a1188e729c8a3228780cf83d0`  
		Last Modified: Tue, 04 Feb 2025 08:03:51 GMT  
		Size: 24.7 MB (24746488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b0ffd764a137045323ce5b430a010c0f27d927825897343bc94eb266304a12`  
		Last Modified: Tue, 04 Feb 2025 10:21:56 GMT  
		Size: 65.2 MB (65167643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c25d78ad7955120511cf4a3329704af325854f4bcbc68110298967b337614378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7672250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b251aa22b2c24e45824d63d1866f50eb24f3fab6da989e814c81d535476a01`

```dockerfile
```

-	Layers:
	-	`sha256:0cc201c117d3c9d6a6d128311bc553cbb8f8288c95b25dc23d9056096e64f723`  
		Last Modified: Tue, 04 Feb 2025 10:21:51 GMT  
		Size: 7.7 MB (7664893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a9af14d91087ed924e26d790d458c6c4e9088eb5e6fea94d4bfe8a661552b19`  
		Last Modified: Tue, 04 Feb 2025 10:21:50 GMT  
		Size: 7.4 KB (7357 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:963821eab438cca62a72541d9517491b6b758bd7a71fb9dc131f2537230f081a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (131012626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ccae8cf93158ee853f476a9109dd2af22f33d5e8f8bea290aa1078ac2400a30`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a0e0ff4d5bcbd6e2c25332ca46ec757661e665f67ef593a6f9b269659d2aeab0`  
		Last Modified: Tue, 14 Jan 2025 01:36:57 GMT  
		Size: 44.7 MB (44668351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6de100729dc42fca6e1da779a5cabf824cb59902a2e776e84fe6b7124d28a0`  
		Last Modified: Tue, 14 Jan 2025 08:59:23 GMT  
		Size: 23.9 MB (23876812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c133cb44b43ce8e0628b481f6d32820f19b92bbcee07e7706966c203b607284a`  
		Last Modified: Tue, 14 Jan 2025 16:17:30 GMT  
		Size: 62.5 MB (62467463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c724c35f72f32fd7ce9fc73e81354004d117302c8a645746010e67cfad7bf7c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7634670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d157cfbee009a2005ad4f645cb3d386e308cd2dc1924ae726097376d3f653d82`

```dockerfile
```

-	Layers:
	-	`sha256:c32c99ffae3952178d8fa4d0f1ea8146402add0c6df485c7af1ff72bd75d8d32`  
		Last Modified: Tue, 14 Jan 2025 16:17:28 GMT  
		Size: 7.6 MB (7627313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56badd2735f45c4d8768ab030f31de125093b00e7776267191877090d63463cd`  
		Last Modified: Tue, 14 Jan 2025 16:17:27 GMT  
		Size: 7.4 KB (7357 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:99626c55ddc16b23335b0fc1995673efbb918649fbf4fab6f7784e7c96083405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141722160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:976b9892d2184abc5a382db5e3174b5e6a17000ec2933cce2be8e2e021845720`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7cef9546887caee4cb752860ee90de96728f638ede0f77bda226ca44ac3e04db`  
		Last Modified: Tue, 14 Jan 2025 01:37:16 GMT  
		Size: 48.8 MB (48760872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fc550a04d72fdc48fc4716034190ede3de291a338b2c748b32584534d2c3f1`  
		Last Modified: Tue, 14 Jan 2025 07:00:48 GMT  
		Size: 25.5 MB (25487312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97035a0dde45440d902fa525c75a16c6689c0105aa65885137511ec2d09218fb`  
		Last Modified: Tue, 14 Jan 2025 13:32:31 GMT  
		Size: 67.5 MB (67473976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:77aac8c09632d225ec7ad937466487a18fe44b41321162b63a495deb5d7b09bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7642481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb3664716cbc9827e0d4700eb1a943adee7374c4275ebb1f4c2ad10bfc88c09c`

```dockerfile
```

-	Layers:
	-	`sha256:37625ca4e83e7ecc5ab4a9bb6accc1b603a4513f134d31e5077dd26734898763`  
		Last Modified: Tue, 14 Jan 2025 13:32:29 GMT  
		Size: 7.6 MB (7635104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a47b95af4fcf2431e73ac39d0424c1dde7f7ee5b3a2c920721d4584e9afa5e36`  
		Last Modified: Tue, 14 Jan 2025 13:32:28 GMT  
		Size: 7.4 KB (7377 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6678694174d4f8eeeffa050f0fc716c554ad11fc7f6a029f8ebb4797c6fbe517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146471670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80da4043c23e99d797e3ac30aa56c3125b9748c66f5e6d89758cdbf9d9828488`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:51741382468681fc53992e03a5e8ce7f591198e39599d81f3b698e3652a63db4`  
		Last Modified: Tue, 04 Feb 2025 01:36:41 GMT  
		Size: 49.9 MB (49883916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4227754a1dcb648ed5c4c8f40f8d60f655bb96ef669b5da48ad50132dc9621`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 27.2 MB (27185942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74bb38fe259cd8a9e1ef2a45c45f0372cb16ddaf5c5facf3363ca9cfcede2c4d`  
		Last Modified: Tue, 04 Feb 2025 05:15:50 GMT  
		Size: 69.4 MB (69401812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:179c2eca5debb1d945c5b9eeaf22c0e8db8339553ed7d92bea95b044f525ea1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7661234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4a4108ec78cddbd0969cb329e129c9a6c49ee083712bc2b3c5c2803e244549`

```dockerfile
```

-	Layers:
	-	`sha256:7ce5bd96b9500a5bf64ca90b6006bd7805c45b65a27e6928eac71f99c067ff43`  
		Last Modified: Tue, 04 Feb 2025 05:15:49 GMT  
		Size: 7.7 MB (7653959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d21eccae88899113b9e0126cb64255aca549e84521b34ecc5fc1d7c273a2b36`  
		Last Modified: Tue, 04 Feb 2025 05:15:48 GMT  
		Size: 7.3 KB (7275 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:f77dbb626432088faf0677622876c0ec92e981900c02ed8d56d1e3f06b5437c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140705745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d330c8a9b3041cb1c438700b5ff456851b2af6ac9b9106c526d10f0cba85723c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1ad11d2c3d2c0479cee56b824f2514b710c0c76d88c22da7ef5ec7f2ccc527d0`  
		Last Modified: Tue, 14 Jan 2025 01:35:17 GMT  
		Size: 48.5 MB (48545883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7625cd98aa6d5c80fb0d1f627561581568ea6f268919dc1e831bfca9d1e853`  
		Last Modified: Tue, 14 Jan 2025 18:12:26 GMT  
		Size: 26.0 MB (26040345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d41982939111491c6252a19353da998fa5ef416acfaed05792f55a462ab11e`  
		Last Modified: Wed, 15 Jan 2025 02:04:08 GMT  
		Size: 66.1 MB (66119517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1dfe48479ceb60993458a81c57144d64932ad4edaa1a619c135cfbfc993bbfa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4940cfb76b69b556878c579c3491c1f9a4221722c4afce5e509358647ed38182`

```dockerfile
```

-	Layers:
	-	`sha256:1b8d88f19bb395c1257b1d2d02adadd9a2f3d61436407f852f9e9f4dbf20d914`  
		Last Modified: Wed, 15 Jan 2025 02:04:01 GMT  
		Size: 7.1 KB (7129 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c9dff46a695bbbd09928df43913acc08b77b33c6e5bbe3c67db3645450f3ec10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152620570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc5b403b395db45f384452fa3d991abd51cf8f7fcd540f565994f1ccb2e3791`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1736726400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fca4ba78a63cac2994d6f3576656e907e3a130a20f935b6a1e2c945c9e7be3af`  
		Last Modified: Tue, 14 Jan 2025 01:38:04 GMT  
		Size: 52.2 MB (52151887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f2cddc488774629199c39c9010734d4be824e6ca934835a5e2d444a85e0075`  
		Last Modified: Tue, 14 Jan 2025 05:31:14 GMT  
		Size: 27.6 MB (27591847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97154d7b719fe3158c773c51a570d7d8ab1e54dcb04c12ce4e93476ca16bbefc`  
		Last Modified: Tue, 14 Jan 2025 09:43:30 GMT  
		Size: 72.9 MB (72876836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:de4a20ba75e03c0ff75c6080bd0eccad35fae0a9cdd8003b930a1c10359ba01f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7647309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7df2c6e85249573151aa8cd5130afefa5a2b540e14850e3ca08acd68a6e0cd2`

```dockerfile
```

-	Layers:
	-	`sha256:898d5118a17bda22e2ca116218625d18f3e8af744178649f307d32fa82a9375c`  
		Last Modified: Tue, 14 Jan 2025 09:43:28 GMT  
		Size: 7.6 MB (7639980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d5ea53d9432befce7809da77eac8d34ff51118b643a4b8fa31ef71e00df002d`  
		Last Modified: Tue, 14 Jan 2025 09:43:27 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:21b580e6d49c7e93d393cc4183b7953507a0d14a2c772cb813a045e6585ce821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.9 MB (138946644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa4fe23c7e5e0a9ff767ebb38c7e80622244bde6575d34e79b828167a5c05e51`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:41a19e48936e10f226b6bfe61097156b74f03101f788496e8860f0d4806f05ba`  
		Last Modified: Tue, 04 Feb 2025 01:38:33 GMT  
		Size: 47.0 MB (47040914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a706305f90a9f6f5a4662ef1063ca9b1d12e77b9f1482c3925294e4989eea2f`  
		Last Modified: Tue, 04 Feb 2025 04:38:37 GMT  
		Size: 25.4 MB (25411970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2279830c9cdcc3d6d50a4a0308903e5819e1f53fc61863f2bc9dae664a4b8e0e`  
		Last Modified: Tue, 04 Feb 2025 08:09:05 GMT  
		Size: 66.5 MB (66493760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:84d7869326707918f8017660abb61e07bf85545665587c47c75212b024d84ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7655227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f78cd334f922550d198aaced125697fe79820aa0e68451dc3687844c137eff`

```dockerfile
```

-	Layers:
	-	`sha256:69854c67014a55e3cbc0388c744d9f3bdef6b499bc255551489ddc567868be30`  
		Last Modified: Tue, 04 Feb 2025 08:08:56 GMT  
		Size: 7.6 MB (7647898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97e27ad8a4239ffd6edc6265d973c3ec43e3477ab76afac7cb1ee2b147937370`  
		Last Modified: Tue, 04 Feb 2025 08:08:55 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:24947995300edff9fe074d902dea0635e6d22ed2fd1937fa6508b0ec0c990968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144330742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdcab1fa96a7252e1d34e96a40a4923670646b93a75fa50937e7e7cbd46fe398`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1f48ea4a277664853f54eabe6340c7571241c845468906404bbb1efd60e69807`  
		Last Modified: Tue, 04 Feb 2025 01:38:18 GMT  
		Size: 48.6 MB (48560783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1f7d849459507f8a608795416d02b409e9f01c22159fa5acaf53ea0891b503`  
		Last Modified: Tue, 04 Feb 2025 07:31:13 GMT  
		Size: 27.2 MB (27214463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd8e9f79a90256c65272d5e3f7412b708597a6f16ea9693af76e4d17ce51d21`  
		Last Modified: Tue, 04 Feb 2025 11:36:07 GMT  
		Size: 68.6 MB (68555496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f2b1e81f1b440e5843aa24251b0b8923a99a1690c6dddfe027fb3ace5f939d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7672334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b609fc218e38ddd086dfc5bc64b9f12be4c636bbd78e05042313c048a7f24862`

```dockerfile
```

-	Layers:
	-	`sha256:e23016206115b86c9b36dd0ae2492aeb3ac7bef4a88beb722d8b794113fe07c3`  
		Last Modified: Tue, 04 Feb 2025 11:36:06 GMT  
		Size: 7.7 MB (7665038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b48b762e9223711dae7c7cdd1c675f03008477b830052c67c491f6c42f63dc4`  
		Last Modified: Tue, 04 Feb 2025 11:36:06 GMT  
		Size: 7.3 KB (7296 bytes)  
		MIME: application/vnd.in-toto+json
