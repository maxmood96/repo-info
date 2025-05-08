<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rakudo-star`

-	[`rakudo-star:2025.02`](#rakudo-star202502)
-	[`rakudo-star:2025.02-alpine`](#rakudo-star202502-alpine)
-	[`rakudo-star:alpine`](#rakudo-staralpine)
-	[`rakudo-star:bookworm`](#rakudo-starbookworm)
-	[`rakudo-star:latest`](#rakudo-starlatest)

## `rakudo-star:2025.02`

```console
$ docker pull rakudo-star@sha256:fa3d14caad7f2621951f2091e787c29500fa743bef3008cc1eed7e177dac9092
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2025.02` - linux; amd64

```console
$ docker pull rakudo-star@sha256:238c5b0d505dc5b78269cde195a14ffd65bbe92f0d1c0cd28f382bf4b18a2f71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.7 MB (178683420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe3c74dd3fd2be2735dc7048d6e5bcb23a885ce304908f364a4e8eeba23ecf2`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
MAINTAINER Rob Hoelz
# Thu, 06 Mar 2025 03:06:23 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
ARG rakudo_version=2025.02-01
# Thu, 06 Mar 2025 03:06:23 GMT
ENV rakudo_version=2025.02-01
# Thu, 06 Mar 2025 03:06:23 GMT
# ARGS: rakudo_version=2025.02-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 06 Mar 2025 03:06:23 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca513cad200b13ead2c745498459eed58a6db3480e3ba6117f854da097262526`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 64.4 MB (64394427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3c3cf117e981eb4ea7cbe20abb9fccc3dbfa905c5847b023ab0ca0ae4084c7`  
		Last Modified: Thu, 08 May 2025 18:05:16 GMT  
		Size: 3.2 KB (3239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568510810cc04ed50deb6d51640050762f8d08015ed07c10ef6b2fe9e70185bb`  
		Last Modified: Thu, 08 May 2025 18:05:20 GMT  
		Size: 41.8 MB (41783374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.02` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:b346b09c0663de6243f69749766f1c511997187c12e55dbe9c9807773884f321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7769719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde5e0fcd4eb1b8f26d8226be5a36962879a3bf742a01ca89b29be74cf307038`

```dockerfile
```

-	Layers:
	-	`sha256:5d67147cf84216dd4217d55ce59105e94e9f097ce34e453a015640c427f79993`  
		Last Modified: Mon, 28 Apr 2025 23:30:57 GMT  
		Size: 7.8 MB (7756683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5357806317ca0773241900509638f331a617331d51c9aa5f98cc5d2d39be3bee`  
		Last Modified: Mon, 28 Apr 2025 23:30:57 GMT  
		Size: 13.0 KB (13036 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2025.02` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:f694ec948beb839326c5ca1b9b8ac280209a109ca34d1b9fde06ace011fa089d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176288200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba837f92f110f3f11cea49db714f7aac681d436ff5ae90d41e3ebf60b46da7a`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
MAINTAINER Rob Hoelz
# Thu, 06 Mar 2025 03:06:23 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
ARG rakudo_version=2025.02-01
# Thu, 06 Mar 2025 03:06:23 GMT
ENV rakudo_version=2025.02-01
# Thu, 06 Mar 2025 03:06:23 GMT
# ARGS: rakudo_version=2025.02-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 06 Mar 2025 03:06:23 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84649bff67ea459549b6f371f7045d9968d6ebf370b815c922a625f3ab065724`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 23.5 MB (23544262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a2a14f59a002f5ef50911a0687d30beadf65bbe35bde8bd3823c3496cbd465`  
		Last Modified: Thu, 08 May 2025 17:04:49 GMT  
		Size: 64.4 MB (64355683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781b80c35313a1ba9ed1578ba03abb4c15eb910f357035d79a8c637a44ce433d`  
		Last Modified: Wed, 30 Apr 2025 04:15:24 GMT  
		Size: 3.2 KB (3239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856d3f0ff0b0b5d732a3f2dc76f806634f1606d136b457ff7eb1cccb9f754721`  
		Last Modified: Wed, 30 Apr 2025 04:15:26 GMT  
		Size: 40.1 MB (40057372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.02` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:007e7e606ddcf6eb88c8b5cfa2236596981ae5b3c844ca52ffa147225a17df7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64a2263813161fda71d2a10f9e4977c0c91a8196d10e829cca06dd11765a882`

```dockerfile
```

-	Layers:
	-	`sha256:3bd37bffca30737207b5206f9c8c4da188c88156e18d71bc59002da28ce65f1b`  
		Last Modified: Wed, 30 Apr 2025 04:15:25 GMT  
		Size: 7.8 MB (7763088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6c2cd80c913ebbd89631d43c278929b47f97234eec06dc6da8b20455683aa15`  
		Last Modified: Wed, 30 Apr 2025 04:15:24 GMT  
		Size: 13.1 KB (13143 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2025.02-alpine`

```console
$ docker pull rakudo-star@sha256:1bfd397fd753010d3f8d0b35b323888818f9d9a7dbb1092f3cf71218793fc772
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2025.02-alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:1f9ae6b68b7433de5e7968e21b1ecf8ce03c14595e97743c7626afdcfb6a0f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45618868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9527b7bbb74679b33bc214e027538f4331c5a623e972c5631bb644491faa8d43`
-	Default Command: `["raku"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 06 Mar 2025 03:06:23 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
ARG rakudo_version=2025.02-01
# Thu, 06 Mar 2025 03:06:23 GMT
ENV rakudo_version=2025.02-01
# Thu, 06 Mar 2025 03:06:23 GMT
# ARGS: rakudo_version=2025.02-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 06 Mar 2025 03:06:23 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86afc9064b7c78f6594dfbba7e76938353e34c7dfc22aa47ffc717f05851e48d`  
		Last Modified: Thu, 06 Mar 2025 21:12:56 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4102ff2f36b7fb27c643f364230c681f6395da28ff04125a67ec3dabc2aa30c0`  
		Last Modified: Thu, 06 Mar 2025 21:12:57 GMT  
		Size: 42.0 MB (41975676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.02-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:aa148ec68b7356cd512261e5eb5232e63afc3cbddd3285775e67eeb84f3ac87c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 KB (132475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e831d741bc685cd44ea32e01fa9b706501a3635c8e147fc74f32cb19a84f7556`

```dockerfile
```

-	Layers:
	-	`sha256:07bfd11fb093fc26625bef4091a49ad46b0e700779b3f0b504bceed03cffeb3b`  
		Last Modified: Thu, 06 Mar 2025 21:12:56 GMT  
		Size: 120.7 KB (120726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7e4f522dc135a03e07fb4f27b803c2235ec91b29e4879e1bca4e95be934c35e`  
		Last Modified: Thu, 06 Mar 2025 21:12:56 GMT  
		Size: 11.7 KB (11749 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2025.02-alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:cb06a8846183956aa56c6ce96b5c4767a76457fa981601effde3c93fd096e9bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45806931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4275697de24c9d5189bd92a95d7fb9f0b6cee8f0099a17cd968b16335e176abb`
-	Default Command: `["raku"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 06 Mar 2025 03:06:23 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
ARG rakudo_version=2025.02-01
# Thu, 06 Mar 2025 03:06:23 GMT
ENV rakudo_version=2025.02-01
# Thu, 06 Mar 2025 03:06:23 GMT
# ARGS: rakudo_version=2025.02-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 06 Mar 2025 03:06:23 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3620dce991340c0f0dbedb81ef0f818da3fe468615291bcea7c3cd1b7507f5a9`  
		Last Modified: Thu, 06 Mar 2025 21:37:44 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53a386934ca9b7aacfd007984fc93c146eb78a06ef375f216866f071d801a19`  
		Last Modified: Thu, 06 Mar 2025 21:37:46 GMT  
		Size: 41.8 MB (41812955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.02-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:9c39407c1e6596aea1ea76710a42e3a4582e65cb5435700d982c9b8b81d0d2dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 KB (132602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706fd910ba49c2d6e53ba71bea2dc7bad6aeb06789bb494c6255aa577950d208`

```dockerfile
```

-	Layers:
	-	`sha256:7c04b9a2c8919fcad294778955eba6c72fe50404dd34904a81606507e2961cd6`  
		Last Modified: Thu, 06 Mar 2025 21:37:44 GMT  
		Size: 120.8 KB (120758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00aaf5bdb5f398e2478e751e6abe0dd648eafc39ea4cc36a4c69807a4476f213`  
		Last Modified: Thu, 06 Mar 2025 21:37:44 GMT  
		Size: 11.8 KB (11844 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:1bfd397fd753010d3f8d0b35b323888818f9d9a7dbb1092f3cf71218793fc772
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:1f9ae6b68b7433de5e7968e21b1ecf8ce03c14595e97743c7626afdcfb6a0f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45618868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9527b7bbb74679b33bc214e027538f4331c5a623e972c5631bb644491faa8d43`
-	Default Command: `["raku"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 06 Mar 2025 03:06:23 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
ARG rakudo_version=2025.02-01
# Thu, 06 Mar 2025 03:06:23 GMT
ENV rakudo_version=2025.02-01
# Thu, 06 Mar 2025 03:06:23 GMT
# ARGS: rakudo_version=2025.02-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 06 Mar 2025 03:06:23 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86afc9064b7c78f6594dfbba7e76938353e34c7dfc22aa47ffc717f05851e48d`  
		Last Modified: Thu, 06 Mar 2025 21:12:56 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4102ff2f36b7fb27c643f364230c681f6395da28ff04125a67ec3dabc2aa30c0`  
		Last Modified: Thu, 06 Mar 2025 21:12:57 GMT  
		Size: 42.0 MB (41975676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:aa148ec68b7356cd512261e5eb5232e63afc3cbddd3285775e67eeb84f3ac87c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 KB (132475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e831d741bc685cd44ea32e01fa9b706501a3635c8e147fc74f32cb19a84f7556`

```dockerfile
```

-	Layers:
	-	`sha256:07bfd11fb093fc26625bef4091a49ad46b0e700779b3f0b504bceed03cffeb3b`  
		Last Modified: Thu, 06 Mar 2025 21:12:56 GMT  
		Size: 120.7 KB (120726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7e4f522dc135a03e07fb4f27b803c2235ec91b29e4879e1bca4e95be934c35e`  
		Last Modified: Thu, 06 Mar 2025 21:12:56 GMT  
		Size: 11.7 KB (11749 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:cb06a8846183956aa56c6ce96b5c4767a76457fa981601effde3c93fd096e9bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45806931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4275697de24c9d5189bd92a95d7fb9f0b6cee8f0099a17cd968b16335e176abb`
-	Default Command: `["raku"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 06 Mar 2025 03:06:23 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
ARG rakudo_version=2025.02-01
# Thu, 06 Mar 2025 03:06:23 GMT
ENV rakudo_version=2025.02-01
# Thu, 06 Mar 2025 03:06:23 GMT
# ARGS: rakudo_version=2025.02-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 06 Mar 2025 03:06:23 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3620dce991340c0f0dbedb81ef0f818da3fe468615291bcea7c3cd1b7507f5a9`  
		Last Modified: Thu, 06 Mar 2025 21:37:44 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53a386934ca9b7aacfd007984fc93c146eb78a06ef375f216866f071d801a19`  
		Last Modified: Thu, 06 Mar 2025 21:37:46 GMT  
		Size: 41.8 MB (41812955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:9c39407c1e6596aea1ea76710a42e3a4582e65cb5435700d982c9b8b81d0d2dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 KB (132602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706fd910ba49c2d6e53ba71bea2dc7bad6aeb06789bb494c6255aa577950d208`

```dockerfile
```

-	Layers:
	-	`sha256:7c04b9a2c8919fcad294778955eba6c72fe50404dd34904a81606507e2961cd6`  
		Last Modified: Thu, 06 Mar 2025 21:37:44 GMT  
		Size: 120.8 KB (120758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00aaf5bdb5f398e2478e751e6abe0dd648eafc39ea4cc36a4c69807a4476f213`  
		Last Modified: Thu, 06 Mar 2025 21:37:44 GMT  
		Size: 11.8 KB (11844 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:bookworm`

```console
$ docker pull rakudo-star@sha256:fa3d14caad7f2621951f2091e787c29500fa743bef3008cc1eed7e177dac9092
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:238c5b0d505dc5b78269cde195a14ffd65bbe92f0d1c0cd28f382bf4b18a2f71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.7 MB (178683420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe3c74dd3fd2be2735dc7048d6e5bcb23a885ce304908f364a4e8eeba23ecf2`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
MAINTAINER Rob Hoelz
# Thu, 06 Mar 2025 03:06:23 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
ARG rakudo_version=2025.02-01
# Thu, 06 Mar 2025 03:06:23 GMT
ENV rakudo_version=2025.02-01
# Thu, 06 Mar 2025 03:06:23 GMT
# ARGS: rakudo_version=2025.02-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 06 Mar 2025 03:06:23 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca513cad200b13ead2c745498459eed58a6db3480e3ba6117f854da097262526`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 64.4 MB (64394427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3c3cf117e981eb4ea7cbe20abb9fccc3dbfa905c5847b023ab0ca0ae4084c7`  
		Last Modified: Thu, 08 May 2025 18:05:16 GMT  
		Size: 3.2 KB (3239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568510810cc04ed50deb6d51640050762f8d08015ed07c10ef6b2fe9e70185bb`  
		Last Modified: Thu, 08 May 2025 18:05:20 GMT  
		Size: 41.8 MB (41783374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:b346b09c0663de6243f69749766f1c511997187c12e55dbe9c9807773884f321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7769719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde5e0fcd4eb1b8f26d8226be5a36962879a3bf742a01ca89b29be74cf307038`

```dockerfile
```

-	Layers:
	-	`sha256:5d67147cf84216dd4217d55ce59105e94e9f097ce34e453a015640c427f79993`  
		Last Modified: Mon, 28 Apr 2025 23:30:57 GMT  
		Size: 7.8 MB (7756683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5357806317ca0773241900509638f331a617331d51c9aa5f98cc5d2d39be3bee`  
		Last Modified: Mon, 28 Apr 2025 23:30:57 GMT  
		Size: 13.0 KB (13036 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:f694ec948beb839326c5ca1b9b8ac280209a109ca34d1b9fde06ace011fa089d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176288200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba837f92f110f3f11cea49db714f7aac681d436ff5ae90d41e3ebf60b46da7a`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
MAINTAINER Rob Hoelz
# Thu, 06 Mar 2025 03:06:23 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
ARG rakudo_version=2025.02-01
# Thu, 06 Mar 2025 03:06:23 GMT
ENV rakudo_version=2025.02-01
# Thu, 06 Mar 2025 03:06:23 GMT
# ARGS: rakudo_version=2025.02-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 06 Mar 2025 03:06:23 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84649bff67ea459549b6f371f7045d9968d6ebf370b815c922a625f3ab065724`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 23.5 MB (23544262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a2a14f59a002f5ef50911a0687d30beadf65bbe35bde8bd3823c3496cbd465`  
		Last Modified: Thu, 08 May 2025 17:04:49 GMT  
		Size: 64.4 MB (64355683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781b80c35313a1ba9ed1578ba03abb4c15eb910f357035d79a8c637a44ce433d`  
		Last Modified: Wed, 30 Apr 2025 04:15:24 GMT  
		Size: 3.2 KB (3239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856d3f0ff0b0b5d732a3f2dc76f806634f1606d136b457ff7eb1cccb9f754721`  
		Last Modified: Wed, 30 Apr 2025 04:15:26 GMT  
		Size: 40.1 MB (40057372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:007e7e606ddcf6eb88c8b5cfa2236596981ae5b3c844ca52ffa147225a17df7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64a2263813161fda71d2a10f9e4977c0c91a8196d10e829cca06dd11765a882`

```dockerfile
```

-	Layers:
	-	`sha256:3bd37bffca30737207b5206f9c8c4da188c88156e18d71bc59002da28ce65f1b`  
		Last Modified: Wed, 30 Apr 2025 04:15:25 GMT  
		Size: 7.8 MB (7763088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6c2cd80c913ebbd89631d43c278929b47f97234eec06dc6da8b20455683aa15`  
		Last Modified: Wed, 30 Apr 2025 04:15:24 GMT  
		Size: 13.1 KB (13143 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:fa3d14caad7f2621951f2091e787c29500fa743bef3008cc1eed7e177dac9092
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:238c5b0d505dc5b78269cde195a14ffd65bbe92f0d1c0cd28f382bf4b18a2f71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.7 MB (178683420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe3c74dd3fd2be2735dc7048d6e5bcb23a885ce304908f364a4e8eeba23ecf2`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
MAINTAINER Rob Hoelz
# Thu, 06 Mar 2025 03:06:23 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
ARG rakudo_version=2025.02-01
# Thu, 06 Mar 2025 03:06:23 GMT
ENV rakudo_version=2025.02-01
# Thu, 06 Mar 2025 03:06:23 GMT
# ARGS: rakudo_version=2025.02-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 06 Mar 2025 03:06:23 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca513cad200b13ead2c745498459eed58a6db3480e3ba6117f854da097262526`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 64.4 MB (64394427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3c3cf117e981eb4ea7cbe20abb9fccc3dbfa905c5847b023ab0ca0ae4084c7`  
		Last Modified: Thu, 08 May 2025 18:05:16 GMT  
		Size: 3.2 KB (3239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568510810cc04ed50deb6d51640050762f8d08015ed07c10ef6b2fe9e70185bb`  
		Last Modified: Thu, 08 May 2025 18:05:20 GMT  
		Size: 41.8 MB (41783374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:b346b09c0663de6243f69749766f1c511997187c12e55dbe9c9807773884f321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7769719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde5e0fcd4eb1b8f26d8226be5a36962879a3bf742a01ca89b29be74cf307038`

```dockerfile
```

-	Layers:
	-	`sha256:5d67147cf84216dd4217d55ce59105e94e9f097ce34e453a015640c427f79993`  
		Last Modified: Mon, 28 Apr 2025 23:30:57 GMT  
		Size: 7.8 MB (7756683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5357806317ca0773241900509638f331a617331d51c9aa5f98cc5d2d39be3bee`  
		Last Modified: Mon, 28 Apr 2025 23:30:57 GMT  
		Size: 13.0 KB (13036 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:f694ec948beb839326c5ca1b9b8ac280209a109ca34d1b9fde06ace011fa089d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176288200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba837f92f110f3f11cea49db714f7aac681d436ff5ae90d41e3ebf60b46da7a`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
MAINTAINER Rob Hoelz
# Thu, 06 Mar 2025 03:06:23 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
ARG rakudo_version=2025.02-01
# Thu, 06 Mar 2025 03:06:23 GMT
ENV rakudo_version=2025.02-01
# Thu, 06 Mar 2025 03:06:23 GMT
# ARGS: rakudo_version=2025.02-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 06 Mar 2025 03:06:23 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84649bff67ea459549b6f371f7045d9968d6ebf370b815c922a625f3ab065724`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 23.5 MB (23544262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a2a14f59a002f5ef50911a0687d30beadf65bbe35bde8bd3823c3496cbd465`  
		Last Modified: Thu, 08 May 2025 17:04:49 GMT  
		Size: 64.4 MB (64355683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781b80c35313a1ba9ed1578ba03abb4c15eb910f357035d79a8c637a44ce433d`  
		Last Modified: Wed, 30 Apr 2025 04:15:24 GMT  
		Size: 3.2 KB (3239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856d3f0ff0b0b5d732a3f2dc76f806634f1606d136b457ff7eb1cccb9f754721`  
		Last Modified: Wed, 30 Apr 2025 04:15:26 GMT  
		Size: 40.1 MB (40057372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:007e7e606ddcf6eb88c8b5cfa2236596981ae5b3c844ca52ffa147225a17df7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64a2263813161fda71d2a10f9e4977c0c91a8196d10e829cca06dd11765a882`

```dockerfile
```

-	Layers:
	-	`sha256:3bd37bffca30737207b5206f9c8c4da188c88156e18d71bc59002da28ce65f1b`  
		Last Modified: Wed, 30 Apr 2025 04:15:25 GMT  
		Size: 7.8 MB (7763088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6c2cd80c913ebbd89631d43c278929b47f97234eec06dc6da8b20455683aa15`  
		Last Modified: Wed, 30 Apr 2025 04:15:24 GMT  
		Size: 13.1 KB (13143 bytes)  
		MIME: application/vnd.in-toto+json
