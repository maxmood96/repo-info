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
