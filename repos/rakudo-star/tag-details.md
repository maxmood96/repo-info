<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rakudo-star`

-	[`rakudo-star:2025.08.1-alpine`](#rakudo-star2025081-alpine)
-	[`rakudo-star:2025.08.1-bookworm`](#rakudo-star2025081-bookworm)
-	[`rakudo-star:2025.08.1-trixie`](#rakudo-star2025081-trixie)
-	[`rakudo-star:alpine`](#rakudo-staralpine)
-	[`rakudo-star:bookworm`](#rakudo-starbookworm)
-	[`rakudo-star:latest`](#rakudo-starlatest)
-	[`rakudo-star:trixie`](#rakudo-startrixie)

## `rakudo-star:2025.08.1-alpine`

```console
$ docker pull rakudo-star@sha256:20b4f2da16dcaec43872f73740c8ffb09d15844e970990e791087e6456c99729
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2025.08.1-alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:7ba68152715de27831884af0929ad67fc5470c165da6b61f080ba28df758ae2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52786197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4293cea04569f8cba4ea278e22e92c2a645a4555b2e49b5b59b000dde53acbd`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 25 Sep 2025 18:16:25 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 18:16:25 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
ARG rakudo_version=2025.08.1-01
# Thu, 25 Sep 2025 18:16:25 GMT
ENV rakudo_version=2025.08.1-01
# Thu, 25 Sep 2025 18:16:25 GMT
# ARGS: rakudo_version=2025.08.1-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 25 Sep 2025 18:16:25 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb568ddd1c171fa25eaf659e843ae544a16f6a01eeb1e49e2024de09d2859802`  
		Last Modified: Wed, 08 Oct 2025 23:32:04 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7abdd7824a25e48b2cb7b3b9601d90324022ce1dc44cccee3103958cb9b8bc`  
		Last Modified: Wed, 08 Oct 2025 23:32:06 GMT  
		Size: 49.0 MB (48982798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.08.1-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:802766c89ee57467889670b301f1181f4f9c7fb9e3d24ba21b1e63f2a6382266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.8 KB (197795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6093dbbd728edc0b4134ae851df675c55fb021ea696a066df63154b31d0fef`

```dockerfile
```

-	Layers:
	-	`sha256:cb14286aeb12efd3f73436a2d70d10dddcaef91fce106c2e570cfb6beeec1ef5`  
		Last Modified: Thu, 09 Oct 2025 01:33:20 GMT  
		Size: 186.0 KB (186024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78db66a19edca11888a6169ff5c8c4c411ced7b184935bec11adc74372e922a2`  
		Last Modified: Thu, 09 Oct 2025 01:33:21 GMT  
		Size: 11.8 KB (11771 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2025.08.1-alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:ab2c76d88bf5eb48e0825125345838d323cbf22ca901acd2e6bf3a32c9685b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52894513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc524f2968a5856e4cd97223a684ab54252d95580d6360f30b0215ed2dc9221`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 25 Sep 2025 18:16:25 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 18:16:25 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
ARG rakudo_version=2025.08.1-01
# Thu, 25 Sep 2025 18:16:25 GMT
ENV rakudo_version=2025.08.1-01
# Thu, 25 Sep 2025 18:16:25 GMT
# ARGS: rakudo_version=2025.08.1-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 25 Sep 2025 18:16:25 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b0d4bdb013522c8d0a0c94c80a2a4cf283e73f867aedd96e01f680dca84c9e`  
		Last Modified: Wed, 08 Oct 2025 22:22:04 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c738eb1065ed95605035bbec26e02e04090572ec08614269277b6ac389a7a891`  
		Last Modified: Wed, 08 Oct 2025 22:22:08 GMT  
		Size: 48.8 MB (48755496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.08.1-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:c87aff0017a83a37e45c37b8e4ad86ccc00f0b01234c9558b431cd8c9c51669e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 KB (197922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f266b2b5b18e42e51ccf7d210d6d02cd49fc7258a1c4274776f4ebfb671d614c`

```dockerfile
```

-	Layers:
	-	`sha256:695c5dc7135f76aac74050069cb34a1dcbcd61067e4d0bdeca4dff2fae1d8517`  
		Last Modified: Thu, 09 Oct 2025 01:33:24 GMT  
		Size: 186.1 KB (186056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a0177a3f02ba22841c9b3fb3c9898bfee297d5c9b13210c2af0f1d441b764b5`  
		Last Modified: Thu, 09 Oct 2025 01:33:25 GMT  
		Size: 11.9 KB (11866 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2025.08.1-bookworm`

```console
$ docker pull rakudo-star@sha256:17dd83f15c978a5a80571e1f958ae25cb1d67a16f24f6bc2c640295da7f1016b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2025.08.1-bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:352ff420643450a16c43c87e1f97c6cee6fba5878726663e0950d6c0c115c031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179586236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c1dffda3d5add728b06f03469d28f251eb67ab9b171d30c04f0061ab847921`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
MAINTAINER Rob Hoelz
# Tue, 23 Sep 2025 22:27:44 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
ARG rakudo_version=2025.08.1-01
# Tue, 23 Sep 2025 22:27:44 GMT
ENV rakudo_version=2025.08.1-01
# Tue, 23 Sep 2025 22:27:44 GMT
# ARGS: rakudo_version=2025.08.1-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 23 Sep 2025 22:27:44 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3dba6026a3c551d6b8e98308c073fff4fd569fd2fc61f21384cb996da82c9e`  
		Last Modified: Tue, 30 Sep 2025 01:43:53 GMT  
		Size: 24.0 MB (24025876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb1b35a6fc14463ada297f3f0605409cbfe29368b38fd5d1e41f7dcf29bb6fb`  
		Last Modified: Tue, 30 Sep 2025 03:17:35 GMT  
		Size: 64.4 MB (64397411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903144137f176adb6f6e7c4718d2985a73a4b27dd92430b0a084d15e5c1b6e03`  
		Last Modified: Tue, 30 Sep 2025 06:59:27 GMT  
		Size: 3.2 KB (3234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f639f94a1cf9c9440c4647c9dcce6fd056e621dbc18e14fb69e55a428660836e`  
		Last Modified: Tue, 30 Sep 2025 06:59:39 GMT  
		Size: 42.7 MB (42679158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.08.1-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:b90d05e6e04cbef1312bded53965e20d9b691483c40cd5f324604d5284292b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b7c33c20bf8b444e47b3e302fa7d1e8d68f16cd7ce038b7e8339f7eef66f9b`

```dockerfile
```

-	Layers:
	-	`sha256:6226809132fd8016d4031ab62b05d22d8d5d5b887a0dff6300d567f17bb085cb`  
		Last Modified: Tue, 30 Sep 2025 22:34:39 GMT  
		Size: 8.0 MB (7968098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca6210ccaa092d4cbccf0a7eaa2daa60a5d42f65d2125251661ae64ce3e777e3`  
		Last Modified: Tue, 30 Sep 2025 22:34:40 GMT  
		Size: 13.1 KB (13050 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2025.08.1-bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:f1be86e9027bbb58a6d679c0bb7351d20f4a7662390d7bea5e9519731515670e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177082402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896fe49690bd4a9516398fb4ef0910af5ad7a402bef870f42bbe1ab50c50d891`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
MAINTAINER Rob Hoelz
# Tue, 23 Sep 2025 22:27:44 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
ARG rakudo_version=2025.08.1-01
# Tue, 23 Sep 2025 22:27:44 GMT
ENV rakudo_version=2025.08.1-01
# Tue, 23 Sep 2025 22:27:44 GMT
# ARGS: rakudo_version=2025.08.1-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 23 Sep 2025 22:27:44 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:f7b43f0d0a8b99591b27457b368e70a582002600d32503fd07798c1bee7cd134`  
		Last Modified: Mon, 29 Sep 2025 23:34:16 GMT  
		Size: 48.4 MB (48358915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b261306f7eb1436ff95e3b9d948f5373b0dcf6ca1223aaa4c2fb303b03e744c`  
		Last Modified: Tue, 30 Sep 2025 00:56:21 GMT  
		Size: 23.6 MB (23594734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a2f93f2f0e198bff671333b38213c36ed741b7f552b83c033cf63f52b58c0e`  
		Last Modified: Tue, 30 Sep 2025 01:19:31 GMT  
		Size: 64.4 MB (64371209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b4abcc1f357c7e316def7b4750dd45497bdc2dbd28bb3dafcb05c4042483e9`  
		Last Modified: Tue, 30 Sep 2025 03:29:05 GMT  
		Size: 3.2 KB (3230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90eff6486d000d63e18b5f0d1576ec9e2467b25ef11a16734684fd9ceefaa3b2`  
		Last Modified: Tue, 30 Sep 2025 20:16:03 GMT  
		Size: 40.8 MB (40754314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.08.1-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:214fdb0f02b73a54cbcc92ccdfe23551d646f430e4c41f8365c4f547af222cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65513711243a0a8f6e5408903985e8ae401e727bac7a69647cd90ad061f8bfc0`

```dockerfile
```

-	Layers:
	-	`sha256:e1ce5dd2387b853a972e2b9c5e10c2c67c640d874734d9f1fbc47057a37716c2`  
		Last Modified: Tue, 30 Sep 2025 13:33:26 GMT  
		Size: 8.0 MB (7974503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48cc0c2538fb51e00c0fdf3e0f406e45ffa84bb15f320d994f8123a3365b29a2`  
		Last Modified: Tue, 30 Sep 2025 13:33:27 GMT  
		Size: 13.2 KB (13157 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2025.08.1-trixie`

```console
$ docker pull rakudo-star@sha256:e97b47695b8eb1f735148d8ef71c14d7162d3f13c1f4ea7c6c81cbc58fe5fe69
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2025.08.1-trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:87dcc7bab5ef5464224b3ca698f4b165bca4d21f3f633a9165eeca824db1f068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185394484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b29527da0ce99ca434e1c8ba79e884e14768afb3303474c323c598672548db`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
MAINTAINER AntonOks
# Thu, 25 Sep 2025 18:16:25 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
ARG rakudo_version=2025.08.1-01
# Thu, 25 Sep 2025 18:16:25 GMT
ENV rakudo_version=2025.08.1-01
# Thu, 25 Sep 2025 18:16:25 GMT
# ARGS: rakudo_version=2025.08.1-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 25 Sep 2025 18:16:25 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd090f42c4b7844c5846f9b4c719994f496fac3befe1d30f0ff20794e742370a`  
		Last Modified: Tue, 30 Sep 2025 03:17:21 GMT  
		Size: 25.6 MB (25614810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c9d6d993ac93f222ba87ca01097d40f632be9b48f6b5e399f2c5da1b3133d1`  
		Last Modified: Tue, 30 Sep 2025 03:18:12 GMT  
		Size: 67.8 MB (67784949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1297c8ccf0eb8dfa0df3420f0bb46bf9e4cfcf549f6694a1fcacc88b3aa336`  
		Last Modified: Fri, 03 Oct 2025 23:16:21 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65658563243478ca29dc615ae43641945fafdfd980394eed3121e1f09918316`  
		Last Modified: Fri, 03 Oct 2025 23:16:27 GMT  
		Size: 42.7 MB (42706862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.08.1-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:76f54d86e49d9f132a73bc72fc4f4b89788b83aae8879fe8d10b5de449761701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5205b15a668bc4f760518854d0e0546c350a7ff7b07f5603b125bd00062e3f84`

```dockerfile
```

-	Layers:
	-	`sha256:ee57d53a455f8922761abbaa5de2c5b7a5ad5a3cc03660bcefa90e8779116efa`  
		Last Modified: Sat, 04 Oct 2025 01:33:24 GMT  
		Size: 7.8 MB (7769401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e1ec45c35e5d12453110cc705c68a34f564a578bfdf29c0a841abcbb7d25ee8`  
		Last Modified: Sat, 04 Oct 2025 01:33:25 GMT  
		Size: 13.1 KB (13050 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2025.08.1-trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:1675f9a65b7ff9f96ac4d9ab4de3d28284b43e7d9f6edf4ae5015f1cdf4237fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (183015780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28450a2e0317b3b8d839d0921252434fca3b0ee439616ffcfeba1bff3f247dbd`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
MAINTAINER AntonOks
# Thu, 25 Sep 2025 18:16:25 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
ARG rakudo_version=2025.08.1-01
# Thu, 25 Sep 2025 18:16:25 GMT
ENV rakudo_version=2025.08.1-01
# Thu, 25 Sep 2025 18:16:25 GMT
# ARGS: rakudo_version=2025.08.1-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 25 Sep 2025 18:16:25 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003e6ed58c0c6ddbc757cdcbd876d66b9b5eed39128088a0055c819ebe15d20d`  
		Last Modified: Tue, 30 Sep 2025 00:14:22 GMT  
		Size: 25.0 MB (25016370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390c9631087ef516f060328537d417f223e1f264c968e39186895696e78090b7`  
		Last Modified: Tue, 30 Sep 2025 01:20:15 GMT  
		Size: 67.6 MB (67582977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76302333573cd0c816c6a1e49604ba7d12d233c917c62ad9e69bd6c72f2e4c64`  
		Last Modified: Sat, 04 Oct 2025 00:14:46 GMT  
		Size: 3.2 KB (3239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34510df6eeadf66ba234fd6b8163bf3320433cdf8450ec63607ef085099f32d9`  
		Last Modified: Sat, 04 Oct 2025 19:01:09 GMT  
		Size: 40.8 MB (40764499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.08.1-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:406cb4d90287d89900e02531350303abd0731a71d415fffc4635cb3fbb6dc515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45eb9dd3b446067c34dec941c2036905567cf82422ebcf0afb446c284215e0a8`

```dockerfile
```

-	Layers:
	-	`sha256:1eb15612e5aae3b9f8bd17b68e31de387631848b2886bce8c92a86a3c79efd04`  
		Last Modified: Sat, 04 Oct 2025 01:33:31 GMT  
		Size: 7.8 MB (7777076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d0ad3d7d26ddb014cb68172181be22a8875baba0ea4c9d18a62a003f37faf26`  
		Last Modified: Sat, 04 Oct 2025 01:33:31 GMT  
		Size: 13.2 KB (13157 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:20b4f2da16dcaec43872f73740c8ffb09d15844e970990e791087e6456c99729
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:7ba68152715de27831884af0929ad67fc5470c165da6b61f080ba28df758ae2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52786197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4293cea04569f8cba4ea278e22e92c2a645a4555b2e49b5b59b000dde53acbd`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 25 Sep 2025 18:16:25 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 18:16:25 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
ARG rakudo_version=2025.08.1-01
# Thu, 25 Sep 2025 18:16:25 GMT
ENV rakudo_version=2025.08.1-01
# Thu, 25 Sep 2025 18:16:25 GMT
# ARGS: rakudo_version=2025.08.1-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 25 Sep 2025 18:16:25 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb568ddd1c171fa25eaf659e843ae544a16f6a01eeb1e49e2024de09d2859802`  
		Last Modified: Wed, 08 Oct 2025 23:32:04 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7abdd7824a25e48b2cb7b3b9601d90324022ce1dc44cccee3103958cb9b8bc`  
		Last Modified: Wed, 08 Oct 2025 23:32:06 GMT  
		Size: 49.0 MB (48982798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:802766c89ee57467889670b301f1181f4f9c7fb9e3d24ba21b1e63f2a6382266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.8 KB (197795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6093dbbd728edc0b4134ae851df675c55fb021ea696a066df63154b31d0fef`

```dockerfile
```

-	Layers:
	-	`sha256:cb14286aeb12efd3f73436a2d70d10dddcaef91fce106c2e570cfb6beeec1ef5`  
		Last Modified: Thu, 09 Oct 2025 01:33:20 GMT  
		Size: 186.0 KB (186024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78db66a19edca11888a6169ff5c8c4c411ced7b184935bec11adc74372e922a2`  
		Last Modified: Thu, 09 Oct 2025 01:33:21 GMT  
		Size: 11.8 KB (11771 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:ab2c76d88bf5eb48e0825125345838d323cbf22ca901acd2e6bf3a32c9685b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52894513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc524f2968a5856e4cd97223a684ab54252d95580d6360f30b0215ed2dc9221`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 25 Sep 2025 18:16:25 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 18:16:25 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
ARG rakudo_version=2025.08.1-01
# Thu, 25 Sep 2025 18:16:25 GMT
ENV rakudo_version=2025.08.1-01
# Thu, 25 Sep 2025 18:16:25 GMT
# ARGS: rakudo_version=2025.08.1-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 25 Sep 2025 18:16:25 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b0d4bdb013522c8d0a0c94c80a2a4cf283e73f867aedd96e01f680dca84c9e`  
		Last Modified: Wed, 08 Oct 2025 22:22:04 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c738eb1065ed95605035bbec26e02e04090572ec08614269277b6ac389a7a891`  
		Last Modified: Wed, 08 Oct 2025 22:22:08 GMT  
		Size: 48.8 MB (48755496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:c87aff0017a83a37e45c37b8e4ad86ccc00f0b01234c9558b431cd8c9c51669e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 KB (197922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f266b2b5b18e42e51ccf7d210d6d02cd49fc7258a1c4274776f4ebfb671d614c`

```dockerfile
```

-	Layers:
	-	`sha256:695c5dc7135f76aac74050069cb34a1dcbcd61067e4d0bdeca4dff2fae1d8517`  
		Last Modified: Thu, 09 Oct 2025 01:33:24 GMT  
		Size: 186.1 KB (186056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a0177a3f02ba22841c9b3fb3c9898bfee297d5c9b13210c2af0f1d441b764b5`  
		Last Modified: Thu, 09 Oct 2025 01:33:25 GMT  
		Size: 11.9 KB (11866 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:bookworm`

```console
$ docker pull rakudo-star@sha256:17dd83f15c978a5a80571e1f958ae25cb1d67a16f24f6bc2c640295da7f1016b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:352ff420643450a16c43c87e1f97c6cee6fba5878726663e0950d6c0c115c031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179586236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c1dffda3d5add728b06f03469d28f251eb67ab9b171d30c04f0061ab847921`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
MAINTAINER Rob Hoelz
# Tue, 23 Sep 2025 22:27:44 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
ARG rakudo_version=2025.08.1-01
# Tue, 23 Sep 2025 22:27:44 GMT
ENV rakudo_version=2025.08.1-01
# Tue, 23 Sep 2025 22:27:44 GMT
# ARGS: rakudo_version=2025.08.1-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 23 Sep 2025 22:27:44 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3dba6026a3c551d6b8e98308c073fff4fd569fd2fc61f21384cb996da82c9e`  
		Last Modified: Tue, 30 Sep 2025 01:43:53 GMT  
		Size: 24.0 MB (24025876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb1b35a6fc14463ada297f3f0605409cbfe29368b38fd5d1e41f7dcf29bb6fb`  
		Last Modified: Tue, 30 Sep 2025 03:17:35 GMT  
		Size: 64.4 MB (64397411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903144137f176adb6f6e7c4718d2985a73a4b27dd92430b0a084d15e5c1b6e03`  
		Last Modified: Tue, 30 Sep 2025 06:59:27 GMT  
		Size: 3.2 KB (3234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f639f94a1cf9c9440c4647c9dcce6fd056e621dbc18e14fb69e55a428660836e`  
		Last Modified: Tue, 30 Sep 2025 06:59:39 GMT  
		Size: 42.7 MB (42679158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:b90d05e6e04cbef1312bded53965e20d9b691483c40cd5f324604d5284292b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b7c33c20bf8b444e47b3e302fa7d1e8d68f16cd7ce038b7e8339f7eef66f9b`

```dockerfile
```

-	Layers:
	-	`sha256:6226809132fd8016d4031ab62b05d22d8d5d5b887a0dff6300d567f17bb085cb`  
		Last Modified: Tue, 30 Sep 2025 22:34:39 GMT  
		Size: 8.0 MB (7968098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca6210ccaa092d4cbccf0a7eaa2daa60a5d42f65d2125251661ae64ce3e777e3`  
		Last Modified: Tue, 30 Sep 2025 22:34:40 GMT  
		Size: 13.1 KB (13050 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:f1be86e9027bbb58a6d679c0bb7351d20f4a7662390d7bea5e9519731515670e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177082402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896fe49690bd4a9516398fb4ef0910af5ad7a402bef870f42bbe1ab50c50d891`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
MAINTAINER Rob Hoelz
# Tue, 23 Sep 2025 22:27:44 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
ARG rakudo_version=2025.08.1-01
# Tue, 23 Sep 2025 22:27:44 GMT
ENV rakudo_version=2025.08.1-01
# Tue, 23 Sep 2025 22:27:44 GMT
# ARGS: rakudo_version=2025.08.1-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 23 Sep 2025 22:27:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 23 Sep 2025 22:27:44 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:f7b43f0d0a8b99591b27457b368e70a582002600d32503fd07798c1bee7cd134`  
		Last Modified: Mon, 29 Sep 2025 23:34:16 GMT  
		Size: 48.4 MB (48358915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b261306f7eb1436ff95e3b9d948f5373b0dcf6ca1223aaa4c2fb303b03e744c`  
		Last Modified: Tue, 30 Sep 2025 00:56:21 GMT  
		Size: 23.6 MB (23594734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a2f93f2f0e198bff671333b38213c36ed741b7f552b83c033cf63f52b58c0e`  
		Last Modified: Tue, 30 Sep 2025 01:19:31 GMT  
		Size: 64.4 MB (64371209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b4abcc1f357c7e316def7b4750dd45497bdc2dbd28bb3dafcb05c4042483e9`  
		Last Modified: Tue, 30 Sep 2025 03:29:05 GMT  
		Size: 3.2 KB (3230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90eff6486d000d63e18b5f0d1576ec9e2467b25ef11a16734684fd9ceefaa3b2`  
		Last Modified: Tue, 30 Sep 2025 20:16:03 GMT  
		Size: 40.8 MB (40754314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:214fdb0f02b73a54cbcc92ccdfe23551d646f430e4c41f8365c4f547af222cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65513711243a0a8f6e5408903985e8ae401e727bac7a69647cd90ad061f8bfc0`

```dockerfile
```

-	Layers:
	-	`sha256:e1ce5dd2387b853a972e2b9c5e10c2c67c640d874734d9f1fbc47057a37716c2`  
		Last Modified: Tue, 30 Sep 2025 13:33:26 GMT  
		Size: 8.0 MB (7974503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48cc0c2538fb51e00c0fdf3e0f406e45ffa84bb15f320d994f8123a3365b29a2`  
		Last Modified: Tue, 30 Sep 2025 13:33:27 GMT  
		Size: 13.2 KB (13157 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:e97b47695b8eb1f735148d8ef71c14d7162d3f13c1f4ea7c6c81cbc58fe5fe69
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:87dcc7bab5ef5464224b3ca698f4b165bca4d21f3f633a9165eeca824db1f068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185394484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b29527da0ce99ca434e1c8ba79e884e14768afb3303474c323c598672548db`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
MAINTAINER AntonOks
# Thu, 25 Sep 2025 18:16:25 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
ARG rakudo_version=2025.08.1-01
# Thu, 25 Sep 2025 18:16:25 GMT
ENV rakudo_version=2025.08.1-01
# Thu, 25 Sep 2025 18:16:25 GMT
# ARGS: rakudo_version=2025.08.1-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 25 Sep 2025 18:16:25 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd090f42c4b7844c5846f9b4c719994f496fac3befe1d30f0ff20794e742370a`  
		Last Modified: Tue, 30 Sep 2025 03:17:21 GMT  
		Size: 25.6 MB (25614810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c9d6d993ac93f222ba87ca01097d40f632be9b48f6b5e399f2c5da1b3133d1`  
		Last Modified: Tue, 30 Sep 2025 03:18:12 GMT  
		Size: 67.8 MB (67784949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1297c8ccf0eb8dfa0df3420f0bb46bf9e4cfcf549f6694a1fcacc88b3aa336`  
		Last Modified: Fri, 03 Oct 2025 23:16:21 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65658563243478ca29dc615ae43641945fafdfd980394eed3121e1f09918316`  
		Last Modified: Fri, 03 Oct 2025 23:16:27 GMT  
		Size: 42.7 MB (42706862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:76f54d86e49d9f132a73bc72fc4f4b89788b83aae8879fe8d10b5de449761701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5205b15a668bc4f760518854d0e0546c350a7ff7b07f5603b125bd00062e3f84`

```dockerfile
```

-	Layers:
	-	`sha256:ee57d53a455f8922761abbaa5de2c5b7a5ad5a3cc03660bcefa90e8779116efa`  
		Last Modified: Sat, 04 Oct 2025 01:33:24 GMT  
		Size: 7.8 MB (7769401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e1ec45c35e5d12453110cc705c68a34f564a578bfdf29c0a841abcbb7d25ee8`  
		Last Modified: Sat, 04 Oct 2025 01:33:25 GMT  
		Size: 13.1 KB (13050 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:1675f9a65b7ff9f96ac4d9ab4de3d28284b43e7d9f6edf4ae5015f1cdf4237fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (183015780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28450a2e0317b3b8d839d0921252434fca3b0ee439616ffcfeba1bff3f247dbd`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
MAINTAINER AntonOks
# Thu, 25 Sep 2025 18:16:25 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
ARG rakudo_version=2025.08.1-01
# Thu, 25 Sep 2025 18:16:25 GMT
ENV rakudo_version=2025.08.1-01
# Thu, 25 Sep 2025 18:16:25 GMT
# ARGS: rakudo_version=2025.08.1-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 25 Sep 2025 18:16:25 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003e6ed58c0c6ddbc757cdcbd876d66b9b5eed39128088a0055c819ebe15d20d`  
		Last Modified: Tue, 30 Sep 2025 00:14:22 GMT  
		Size: 25.0 MB (25016370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390c9631087ef516f060328537d417f223e1f264c968e39186895696e78090b7`  
		Last Modified: Tue, 30 Sep 2025 01:20:15 GMT  
		Size: 67.6 MB (67582977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76302333573cd0c816c6a1e49604ba7d12d233c917c62ad9e69bd6c72f2e4c64`  
		Last Modified: Sat, 04 Oct 2025 00:14:46 GMT  
		Size: 3.2 KB (3239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34510df6eeadf66ba234fd6b8163bf3320433cdf8450ec63607ef085099f32d9`  
		Last Modified: Sat, 04 Oct 2025 19:01:09 GMT  
		Size: 40.8 MB (40764499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:406cb4d90287d89900e02531350303abd0731a71d415fffc4635cb3fbb6dc515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45eb9dd3b446067c34dec941c2036905567cf82422ebcf0afb446c284215e0a8`

```dockerfile
```

-	Layers:
	-	`sha256:1eb15612e5aae3b9f8bd17b68e31de387631848b2886bce8c92a86a3c79efd04`  
		Last Modified: Sat, 04 Oct 2025 01:33:31 GMT  
		Size: 7.8 MB (7777076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d0ad3d7d26ddb014cb68172181be22a8875baba0ea4c9d18a62a003f37faf26`  
		Last Modified: Sat, 04 Oct 2025 01:33:31 GMT  
		Size: 13.2 KB (13157 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:trixie`

```console
$ docker pull rakudo-star@sha256:e97b47695b8eb1f735148d8ef71c14d7162d3f13c1f4ea7c6c81cbc58fe5fe69
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:87dcc7bab5ef5464224b3ca698f4b165bca4d21f3f633a9165eeca824db1f068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185394484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b29527da0ce99ca434e1c8ba79e884e14768afb3303474c323c598672548db`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
MAINTAINER AntonOks
# Thu, 25 Sep 2025 18:16:25 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
ARG rakudo_version=2025.08.1-01
# Thu, 25 Sep 2025 18:16:25 GMT
ENV rakudo_version=2025.08.1-01
# Thu, 25 Sep 2025 18:16:25 GMT
# ARGS: rakudo_version=2025.08.1-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 25 Sep 2025 18:16:25 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd090f42c4b7844c5846f9b4c719994f496fac3befe1d30f0ff20794e742370a`  
		Last Modified: Tue, 30 Sep 2025 03:17:21 GMT  
		Size: 25.6 MB (25614810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c9d6d993ac93f222ba87ca01097d40f632be9b48f6b5e399f2c5da1b3133d1`  
		Last Modified: Tue, 30 Sep 2025 03:18:12 GMT  
		Size: 67.8 MB (67784949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1297c8ccf0eb8dfa0df3420f0bb46bf9e4cfcf549f6694a1fcacc88b3aa336`  
		Last Modified: Fri, 03 Oct 2025 23:16:21 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65658563243478ca29dc615ae43641945fafdfd980394eed3121e1f09918316`  
		Last Modified: Fri, 03 Oct 2025 23:16:27 GMT  
		Size: 42.7 MB (42706862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:76f54d86e49d9f132a73bc72fc4f4b89788b83aae8879fe8d10b5de449761701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5205b15a668bc4f760518854d0e0546c350a7ff7b07f5603b125bd00062e3f84`

```dockerfile
```

-	Layers:
	-	`sha256:ee57d53a455f8922761abbaa5de2c5b7a5ad5a3cc03660bcefa90e8779116efa`  
		Last Modified: Sat, 04 Oct 2025 01:33:24 GMT  
		Size: 7.8 MB (7769401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e1ec45c35e5d12453110cc705c68a34f564a578bfdf29c0a841abcbb7d25ee8`  
		Last Modified: Sat, 04 Oct 2025 01:33:25 GMT  
		Size: 13.1 KB (13050 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:1675f9a65b7ff9f96ac4d9ab4de3d28284b43e7d9f6edf4ae5015f1cdf4237fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (183015780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28450a2e0317b3b8d839d0921252434fca3b0ee439616ffcfeba1bff3f247dbd`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
MAINTAINER AntonOks
# Thu, 25 Sep 2025 18:16:25 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
ARG rakudo_version=2025.08.1-01
# Thu, 25 Sep 2025 18:16:25 GMT
ENV rakudo_version=2025.08.1-01
# Thu, 25 Sep 2025 18:16:25 GMT
# ARGS: rakudo_version=2025.08.1-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 25 Sep 2025 18:16:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 25 Sep 2025 18:16:25 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003e6ed58c0c6ddbc757cdcbd876d66b9b5eed39128088a0055c819ebe15d20d`  
		Last Modified: Tue, 30 Sep 2025 00:14:22 GMT  
		Size: 25.0 MB (25016370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390c9631087ef516f060328537d417f223e1f264c968e39186895696e78090b7`  
		Last Modified: Tue, 30 Sep 2025 01:20:15 GMT  
		Size: 67.6 MB (67582977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76302333573cd0c816c6a1e49604ba7d12d233c917c62ad9e69bd6c72f2e4c64`  
		Last Modified: Sat, 04 Oct 2025 00:14:46 GMT  
		Size: 3.2 KB (3239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34510df6eeadf66ba234fd6b8163bf3320433cdf8450ec63607ef085099f32d9`  
		Last Modified: Sat, 04 Oct 2025 19:01:09 GMT  
		Size: 40.8 MB (40764499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:406cb4d90287d89900e02531350303abd0731a71d415fffc4635cb3fbb6dc515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45eb9dd3b446067c34dec941c2036905567cf82422ebcf0afb446c284215e0a8`

```dockerfile
```

-	Layers:
	-	`sha256:1eb15612e5aae3b9f8bd17b68e31de387631848b2886bce8c92a86a3c79efd04`  
		Last Modified: Sat, 04 Oct 2025 01:33:31 GMT  
		Size: 7.8 MB (7777076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d0ad3d7d26ddb014cb68172181be22a8875baba0ea4c9d18a62a003f37faf26`  
		Last Modified: Sat, 04 Oct 2025 01:33:31 GMT  
		Size: 13.2 KB (13157 bytes)  
		MIME: application/vnd.in-toto+json
