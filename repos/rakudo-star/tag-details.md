<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rakudo-star`

-	[`rakudo-star:2024.09`](#rakudo-star202409)
-	[`rakudo-star:2024.09-alpine`](#rakudo-star202409-alpine)
-	[`rakudo-star:alpine`](#rakudo-staralpine)
-	[`rakudo-star:bookworm`](#rakudo-starbookworm)
-	[`rakudo-star:latest`](#rakudo-starlatest)

## `rakudo-star:2024.09`

```console
$ docker pull rakudo-star@sha256:3c66ab24b9003b3bcf30bd734ecd1668b1aa92cd202bd601c90fae82ffc5e953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `rakudo-star:2024.09` - linux; amd64

```console
$ docker pull rakudo-star@sha256:c3525aee794b017677d25ef95ec6f61088264b4676e014cc712731180e638cf8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.9 MB (182942077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e34ae738998798cd2d5adb4a3b876b58c9c89e91c6db658b2d790a37a63aed2`
-	Default Command: `["raku"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:19 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 27 Sep 2024 04:29:20 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:08:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:08:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 08:02:12 GMT
MAINTAINER Rob Hoelz
# Fri, 27 Sep 2024 08:02:12 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku
# Thu, 10 Oct 2024 17:20:13 GMT
ARG rakudo_version=2024.09-01
# Thu, 10 Oct 2024 17:20:13 GMT
ENV rakudo_version=2024.09-01
# Thu, 10 Oct 2024 17:41:03 GMT
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps
# Thu, 10 Oct 2024 17:41:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 10 Oct 2024 17:41:04 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47cff7f31e941e78bf63ca19f0811b675283e2c00ddea10c57f78d93b2bc343`  
		Last Modified: Fri, 27 Sep 2024 05:14:26 GMT  
		Size: 24.1 MB (24053049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a173f2aee8e962ea19db1e418ae84a0c9f71480b51f768a19332dfa83d7722a5`  
		Last Modified: Fri, 27 Sep 2024 05:14:43 GMT  
		Size: 64.4 MB (64392323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e8464e51e45ebc26ab69d9f92f09e4264f985ba7d6489a5771bb52ea1f318e`  
		Last Modified: Fri, 27 Sep 2024 08:24:14 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e1d2984776a8ed2e087bbca3fdbdf104dc8d0632142c4ba0d1e747959e18243`  
		Last Modified: Thu, 10 Oct 2024 18:04:01 GMT  
		Size: 44.9 MB (44938398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rakudo-star:2024.09` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:40d2716707098db193b2f1240b655a9b820c085831172cb9db8109f69736f35f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.3 MB (182275722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c062c1a061328d366e09f046be51a1660ae540257023f362a5951ba70220d14a`
-	Default Command: `["raku"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:09 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 27 Sep 2024 04:38:10 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:18:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:19:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:46:03 GMT
MAINTAINER Rob Hoelz
# Fri, 27 Sep 2024 07:46:04 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku
# Thu, 10 Oct 2024 16:40:05 GMT
ARG rakudo_version=2024.09-01
# Thu, 10 Oct 2024 16:40:05 GMT
ENV rakudo_version=2024.09-01
# Thu, 10 Oct 2024 16:59:24 GMT
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps
# Thu, 10 Oct 2024 16:59:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 10 Oct 2024 16:59:25 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b238499ec52e0d6be479f948c76ba0bc3cc282f612d5a6a4b5ef52ff45f6b2c`  
		Last Modified: Fri, 27 Sep 2024 05:24:56 GMT  
		Size: 23.6 MB (23594043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b754d079e82fafdf15447cfc188868092eaf1cf4a3f96c9d90ab1b7db91230`  
		Last Modified: Fri, 27 Sep 2024 05:25:12 GMT  
		Size: 64.3 MB (64349696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee3809b793e21cdf5afbbcb60c65075b801d8d3a08f09e1052337af32303c25`  
		Last Modified: Fri, 27 Sep 2024 08:05:50 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:606938fd576cc4700ec7552e3173f1f7f8a332696e9f91794878a0acdf06a8a9`  
		Last Modified: Thu, 10 Oct 2024 17:19:50 GMT  
		Size: 44.7 MB (44743837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rakudo-star:2024.09-alpine`

```console
$ docker pull rakudo-star@sha256:40072da044539b71c57052bbf4a4281d7e5709b0bbfb35e1b283068aaf928522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `rakudo-star:2024.09-alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:f5495667f0ba2f7f2b1656354cc9bcb5edd5de3dd24d659e2d4a398276f984ac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48569872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5f199aef0707ea62095cb973f78c01f5eb3b7da231801e29f4701d59641cf82`
-	Default Command: `["raku"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 02:24:14 GMT
RUN addgroup -S raku && adduser -S raku -G raku
# Thu, 10 Oct 2024 17:41:07 GMT
ARG rakudo_version=2024.09-01
# Thu, 10 Oct 2024 17:41:07 GMT
ENV rakudo_version=2024.09-01
# Thu, 10 Oct 2024 18:03:30 GMT
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps
# Thu, 10 Oct 2024 18:03:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 10 Oct 2024 18:03:31 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fe32adfda79342e90b2feef2a7c596fdaccdbbf940912618607fc3e1234855`  
		Last Modified: Sat, 07 Sep 2024 02:46:16 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dca514336f4c3dbe79b44ab29fe0a1ae65945c838c225e4b8c0855ec1abc777`  
		Last Modified: Thu, 10 Oct 2024 18:04:19 GMT  
		Size: 44.9 MB (44945107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rakudo-star:2024.09-alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:54f58717b18fb91f8f261c851e69d21441ce034d2ea6f0bc0bcadeb291e5e5af
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48873645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7fd22d351bf4266e99549348f4b2e9a0f7b27564fe132b2484c7c57b6a84022`
-	Default Command: `["raku"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:04:20 GMT
RUN addgroup -S raku && adduser -S raku -G raku
# Thu, 10 Oct 2024 16:59:28 GMT
ARG rakudo_version=2024.09-01
# Thu, 10 Oct 2024 16:59:28 GMT
ENV rakudo_version=2024.09-01
# Thu, 10 Oct 2024 17:19:23 GMT
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps
# Thu, 10 Oct 2024 17:19:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 10 Oct 2024 17:19:24 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8245056ac056fa1d9046a2b3d4b2cc366c40480c75ad48208959f70fc7b1526d`  
		Last Modified: Fri, 06 Sep 2024 23:24:49 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957dede726b72756ec81e05ee90be0187a5ae8b080f1c39dd8fbbcdebf2ab3d4`  
		Last Modified: Thu, 10 Oct 2024 17:20:06 GMT  
		Size: 44.8 MB (44785041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:40072da044539b71c57052bbf4a4281d7e5709b0bbfb35e1b283068aaf928522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:f5495667f0ba2f7f2b1656354cc9bcb5edd5de3dd24d659e2d4a398276f984ac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48569872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5f199aef0707ea62095cb973f78c01f5eb3b7da231801e29f4701d59641cf82`
-	Default Command: `["raku"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 02:24:14 GMT
RUN addgroup -S raku && adduser -S raku -G raku
# Thu, 10 Oct 2024 17:41:07 GMT
ARG rakudo_version=2024.09-01
# Thu, 10 Oct 2024 17:41:07 GMT
ENV rakudo_version=2024.09-01
# Thu, 10 Oct 2024 18:03:30 GMT
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps
# Thu, 10 Oct 2024 18:03:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 10 Oct 2024 18:03:31 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fe32adfda79342e90b2feef2a7c596fdaccdbbf940912618607fc3e1234855`  
		Last Modified: Sat, 07 Sep 2024 02:46:16 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dca514336f4c3dbe79b44ab29fe0a1ae65945c838c225e4b8c0855ec1abc777`  
		Last Modified: Thu, 10 Oct 2024 18:04:19 GMT  
		Size: 44.9 MB (44945107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:54f58717b18fb91f8f261c851e69d21441ce034d2ea6f0bc0bcadeb291e5e5af
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48873645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7fd22d351bf4266e99549348f4b2e9a0f7b27564fe132b2484c7c57b6a84022`
-	Default Command: `["raku"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:04:20 GMT
RUN addgroup -S raku && adduser -S raku -G raku
# Thu, 10 Oct 2024 16:59:28 GMT
ARG rakudo_version=2024.09-01
# Thu, 10 Oct 2024 16:59:28 GMT
ENV rakudo_version=2024.09-01
# Thu, 10 Oct 2024 17:19:23 GMT
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps
# Thu, 10 Oct 2024 17:19:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 10 Oct 2024 17:19:24 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8245056ac056fa1d9046a2b3d4b2cc366c40480c75ad48208959f70fc7b1526d`  
		Last Modified: Fri, 06 Sep 2024 23:24:49 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957dede726b72756ec81e05ee90be0187a5ae8b080f1c39dd8fbbcdebf2ab3d4`  
		Last Modified: Thu, 10 Oct 2024 17:20:06 GMT  
		Size: 44.8 MB (44785041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rakudo-star:bookworm`

```console
$ docker pull rakudo-star@sha256:3c66ab24b9003b3bcf30bd734ecd1668b1aa92cd202bd601c90fae82ffc5e953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `rakudo-star:bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:c3525aee794b017677d25ef95ec6f61088264b4676e014cc712731180e638cf8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.9 MB (182942077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e34ae738998798cd2d5adb4a3b876b58c9c89e91c6db658b2d790a37a63aed2`
-	Default Command: `["raku"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:19 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 27 Sep 2024 04:29:20 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:08:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:08:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 08:02:12 GMT
MAINTAINER Rob Hoelz
# Fri, 27 Sep 2024 08:02:12 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku
# Thu, 10 Oct 2024 17:20:13 GMT
ARG rakudo_version=2024.09-01
# Thu, 10 Oct 2024 17:20:13 GMT
ENV rakudo_version=2024.09-01
# Thu, 10 Oct 2024 17:41:03 GMT
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps
# Thu, 10 Oct 2024 17:41:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 10 Oct 2024 17:41:04 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47cff7f31e941e78bf63ca19f0811b675283e2c00ddea10c57f78d93b2bc343`  
		Last Modified: Fri, 27 Sep 2024 05:14:26 GMT  
		Size: 24.1 MB (24053049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a173f2aee8e962ea19db1e418ae84a0c9f71480b51f768a19332dfa83d7722a5`  
		Last Modified: Fri, 27 Sep 2024 05:14:43 GMT  
		Size: 64.4 MB (64392323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e8464e51e45ebc26ab69d9f92f09e4264f985ba7d6489a5771bb52ea1f318e`  
		Last Modified: Fri, 27 Sep 2024 08:24:14 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e1d2984776a8ed2e087bbca3fdbdf104dc8d0632142c4ba0d1e747959e18243`  
		Last Modified: Thu, 10 Oct 2024 18:04:01 GMT  
		Size: 44.9 MB (44938398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rakudo-star:bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:40d2716707098db193b2f1240b655a9b820c085831172cb9db8109f69736f35f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.3 MB (182275722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c062c1a061328d366e09f046be51a1660ae540257023f362a5951ba70220d14a`
-	Default Command: `["raku"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:09 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 27 Sep 2024 04:38:10 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:18:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:19:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:46:03 GMT
MAINTAINER Rob Hoelz
# Fri, 27 Sep 2024 07:46:04 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku
# Thu, 10 Oct 2024 16:40:05 GMT
ARG rakudo_version=2024.09-01
# Thu, 10 Oct 2024 16:40:05 GMT
ENV rakudo_version=2024.09-01
# Thu, 10 Oct 2024 16:59:24 GMT
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps
# Thu, 10 Oct 2024 16:59:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 10 Oct 2024 16:59:25 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b238499ec52e0d6be479f948c76ba0bc3cc282f612d5a6a4b5ef52ff45f6b2c`  
		Last Modified: Fri, 27 Sep 2024 05:24:56 GMT  
		Size: 23.6 MB (23594043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b754d079e82fafdf15447cfc188868092eaf1cf4a3f96c9d90ab1b7db91230`  
		Last Modified: Fri, 27 Sep 2024 05:25:12 GMT  
		Size: 64.3 MB (64349696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee3809b793e21cdf5afbbcb60c65075b801d8d3a08f09e1052337af32303c25`  
		Last Modified: Fri, 27 Sep 2024 08:05:50 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:606938fd576cc4700ec7552e3173f1f7f8a332696e9f91794878a0acdf06a8a9`  
		Last Modified: Thu, 10 Oct 2024 17:19:50 GMT  
		Size: 44.7 MB (44743837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:3c66ab24b9003b3bcf30bd734ecd1668b1aa92cd202bd601c90fae82ffc5e953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:c3525aee794b017677d25ef95ec6f61088264b4676e014cc712731180e638cf8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.9 MB (182942077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e34ae738998798cd2d5adb4a3b876b58c9c89e91c6db658b2d790a37a63aed2`
-	Default Command: `["raku"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:19 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 27 Sep 2024 04:29:20 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:08:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:08:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 08:02:12 GMT
MAINTAINER Rob Hoelz
# Fri, 27 Sep 2024 08:02:12 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku
# Thu, 10 Oct 2024 17:20:13 GMT
ARG rakudo_version=2024.09-01
# Thu, 10 Oct 2024 17:20:13 GMT
ENV rakudo_version=2024.09-01
# Thu, 10 Oct 2024 17:41:03 GMT
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps
# Thu, 10 Oct 2024 17:41:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 10 Oct 2024 17:41:04 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47cff7f31e941e78bf63ca19f0811b675283e2c00ddea10c57f78d93b2bc343`  
		Last Modified: Fri, 27 Sep 2024 05:14:26 GMT  
		Size: 24.1 MB (24053049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a173f2aee8e962ea19db1e418ae84a0c9f71480b51f768a19332dfa83d7722a5`  
		Last Modified: Fri, 27 Sep 2024 05:14:43 GMT  
		Size: 64.4 MB (64392323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e8464e51e45ebc26ab69d9f92f09e4264f985ba7d6489a5771bb52ea1f318e`  
		Last Modified: Fri, 27 Sep 2024 08:24:14 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e1d2984776a8ed2e087bbca3fdbdf104dc8d0632142c4ba0d1e747959e18243`  
		Last Modified: Thu, 10 Oct 2024 18:04:01 GMT  
		Size: 44.9 MB (44938398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:40d2716707098db193b2f1240b655a9b820c085831172cb9db8109f69736f35f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.3 MB (182275722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c062c1a061328d366e09f046be51a1660ae540257023f362a5951ba70220d14a`
-	Default Command: `["raku"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:09 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 27 Sep 2024 04:38:10 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:18:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:19:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:46:03 GMT
MAINTAINER Rob Hoelz
# Fri, 27 Sep 2024 07:46:04 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku
# Thu, 10 Oct 2024 16:40:05 GMT
ARG rakudo_version=2024.09-01
# Thu, 10 Oct 2024 16:40:05 GMT
ENV rakudo_version=2024.09-01
# Thu, 10 Oct 2024 16:59:24 GMT
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps
# Thu, 10 Oct 2024 16:59:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 10 Oct 2024 16:59:25 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b238499ec52e0d6be479f948c76ba0bc3cc282f612d5a6a4b5ef52ff45f6b2c`  
		Last Modified: Fri, 27 Sep 2024 05:24:56 GMT  
		Size: 23.6 MB (23594043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b754d079e82fafdf15447cfc188868092eaf1cf4a3f96c9d90ab1b7db91230`  
		Last Modified: Fri, 27 Sep 2024 05:25:12 GMT  
		Size: 64.3 MB (64349696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee3809b793e21cdf5afbbcb60c65075b801d8d3a08f09e1052337af32303c25`  
		Last Modified: Fri, 27 Sep 2024 08:05:50 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:606938fd576cc4700ec7552e3173f1f7f8a332696e9f91794878a0acdf06a8a9`  
		Last Modified: Thu, 10 Oct 2024 17:19:50 GMT  
		Size: 44.7 MB (44743837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
