<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rakudo-star`

-	[`rakudo-star:2025.02`](#rakudo-star202502)
-	[`rakudo-star:2025.02-alpine`](#rakudo-star202502-alpine)
-	[`rakudo-star:alpine`](#rakudo-staralpine)
-	[`rakudo-star:bookworm`](#rakudo-starbookworm)
-	[`rakudo-star:latest`](#rakudo-starlatest)

## `rakudo-star:2025.02`

```console
$ docker pull rakudo-star@sha256:e70be654d8b33bcfab2f2f7839e1ae59c05a97a08f16b5c0d3c33407b7c573cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2025.02` - linux; amd64

```console
$ docker pull rakudo-star@sha256:e9887f051c5fa5e1dcdd0e9ac9c3d7ee5d2693ef5d9ce33eb4f55452f9b58802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.6 MB (178630487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f423b1c0663a9132fcbe25dc3907fcba8853bc18ed04550915400340bed2ebfb`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:7cd785773db44407e20a679ce5439222e505475eed5b99f1910eb2cda51729ab`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.5 MB (48467838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091eb8249475f42de217265c501e0186f0a3ea7490ef7f51458c30db91fb3cac`  
		Last Modified: Mon, 17 Mar 2025 23:13:26 GMT  
		Size: 24.0 MB (24011136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255774e0027b72d2327719e78dbad5ad8c9cf446d055e45be7fc149418470bae`  
		Last Modified: Tue, 18 Mar 2025 00:18:51 GMT  
		Size: 64.4 MB (64396484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e27ac1f4272b0af84649adf99c649bbc532c7ec9ab8ab5bc7e2dbcb6ad7e102`  
		Last Modified: Tue, 18 Mar 2025 01:31:47 GMT  
		Size: 3.2 KB (3236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf1b777a1099ef2c277830c719a06e1fa460f82c79a69590695c01fb6cb194a`  
		Last Modified: Tue, 18 Mar 2025 01:31:48 GMT  
		Size: 41.8 MB (41751793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.02` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:22db685875cb5e29a00d625a627e991b05d90a99b7e2ab825d4bf28f3554f9b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7768331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51058cd23fcf9ea2c73402f38feba2c68697b53d2ac131dbc46abb8501004507`

```dockerfile
```

-	Layers:
	-	`sha256:5e4e2ed77d79b10d897f2aed47c80858297690b07c637f8ab61fdf256efb00af`  
		Last Modified: Tue, 18 Mar 2025 01:31:48 GMT  
		Size: 7.8 MB (7755297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9628364246804de046f8d1fcc83a38ad4a6ec28838210178e18358c0298ad3`  
		Last Modified: Tue, 18 Mar 2025 01:31:48 GMT  
		Size: 13.0 KB (13034 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2025.02` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:56424347cbdb58d545dd024aa74e36812bb5cd504429d962fc9cfa18a3710121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176142842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1cd4355d4bfa12a5dbcd64e7aed3fb84e957e29101a8e98c45de8d713c03ca0`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4378a6c11dea5043896b9425853a850807e5845b0018fe01ddee56c16245fc3c`  
		Last Modified: Tue, 18 Mar 2025 05:00:37 GMT  
		Size: 23.5 MB (23544349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140d15be2fea6dcd21c20cadae2601a118c08a938168718b2612ad6aca91f74a`  
		Last Modified: Tue, 18 Mar 2025 13:13:07 GMT  
		Size: 64.4 MB (64355791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47adee9c6c100b72968c4214c8212a437fd4133a55e025becbfcf80201321f3`  
		Last Modified: Tue, 18 Mar 2025 14:35:10 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4f6ef112049b8b6a8d542134e78cbde095354fa59ffe018f391a219f755315`  
		Last Modified: Tue, 18 Mar 2025 14:35:12 GMT  
		Size: 39.9 MB (39934610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.02` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:3a0374e87a7fa8842cf91c55fafac0a8399735033a634dc04745e4105d694e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7774845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720cb8db8cc384888c52a6866e0c3f8b701aaa5695e86d06a748bdf50e972c09`

```dockerfile
```

-	Layers:
	-	`sha256:e598025b798fa61da776de6416222a57b31bec0d9f5b7c68e594e2e955ee30b9`  
		Last Modified: Tue, 18 Mar 2025 14:35:11 GMT  
		Size: 7.8 MB (7761702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:034ca069e9f372350214d5597a510d089b132965ace7419cb1f6415ce17cbec8`  
		Last Modified: Tue, 18 Mar 2025 14:35:10 GMT  
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
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
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
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
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
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
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
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
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
$ docker pull rakudo-star@sha256:e70be654d8b33bcfab2f2f7839e1ae59c05a97a08f16b5c0d3c33407b7c573cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:e9887f051c5fa5e1dcdd0e9ac9c3d7ee5d2693ef5d9ce33eb4f55452f9b58802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.6 MB (178630487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f423b1c0663a9132fcbe25dc3907fcba8853bc18ed04550915400340bed2ebfb`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:7cd785773db44407e20a679ce5439222e505475eed5b99f1910eb2cda51729ab`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.5 MB (48467838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091eb8249475f42de217265c501e0186f0a3ea7490ef7f51458c30db91fb3cac`  
		Last Modified: Mon, 17 Mar 2025 23:13:26 GMT  
		Size: 24.0 MB (24011136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255774e0027b72d2327719e78dbad5ad8c9cf446d055e45be7fc149418470bae`  
		Last Modified: Tue, 18 Mar 2025 00:18:51 GMT  
		Size: 64.4 MB (64396484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e27ac1f4272b0af84649adf99c649bbc532c7ec9ab8ab5bc7e2dbcb6ad7e102`  
		Last Modified: Tue, 18 Mar 2025 01:31:47 GMT  
		Size: 3.2 KB (3236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf1b777a1099ef2c277830c719a06e1fa460f82c79a69590695c01fb6cb194a`  
		Last Modified: Tue, 18 Mar 2025 01:31:48 GMT  
		Size: 41.8 MB (41751793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:22db685875cb5e29a00d625a627e991b05d90a99b7e2ab825d4bf28f3554f9b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7768331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51058cd23fcf9ea2c73402f38feba2c68697b53d2ac131dbc46abb8501004507`

```dockerfile
```

-	Layers:
	-	`sha256:5e4e2ed77d79b10d897f2aed47c80858297690b07c637f8ab61fdf256efb00af`  
		Last Modified: Tue, 18 Mar 2025 01:31:48 GMT  
		Size: 7.8 MB (7755297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9628364246804de046f8d1fcc83a38ad4a6ec28838210178e18358c0298ad3`  
		Last Modified: Tue, 18 Mar 2025 01:31:48 GMT  
		Size: 13.0 KB (13034 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:56424347cbdb58d545dd024aa74e36812bb5cd504429d962fc9cfa18a3710121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176142842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1cd4355d4bfa12a5dbcd64e7aed3fb84e957e29101a8e98c45de8d713c03ca0`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4378a6c11dea5043896b9425853a850807e5845b0018fe01ddee56c16245fc3c`  
		Last Modified: Tue, 18 Mar 2025 05:00:37 GMT  
		Size: 23.5 MB (23544349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140d15be2fea6dcd21c20cadae2601a118c08a938168718b2612ad6aca91f74a`  
		Last Modified: Tue, 18 Mar 2025 13:13:07 GMT  
		Size: 64.4 MB (64355791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47adee9c6c100b72968c4214c8212a437fd4133a55e025becbfcf80201321f3`  
		Last Modified: Tue, 18 Mar 2025 14:35:10 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4f6ef112049b8b6a8d542134e78cbde095354fa59ffe018f391a219f755315`  
		Last Modified: Tue, 18 Mar 2025 14:35:12 GMT  
		Size: 39.9 MB (39934610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:3a0374e87a7fa8842cf91c55fafac0a8399735033a634dc04745e4105d694e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7774845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720cb8db8cc384888c52a6866e0c3f8b701aaa5695e86d06a748bdf50e972c09`

```dockerfile
```

-	Layers:
	-	`sha256:e598025b798fa61da776de6416222a57b31bec0d9f5b7c68e594e2e955ee30b9`  
		Last Modified: Tue, 18 Mar 2025 14:35:11 GMT  
		Size: 7.8 MB (7761702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:034ca069e9f372350214d5597a510d089b132965ace7419cb1f6415ce17cbec8`  
		Last Modified: Tue, 18 Mar 2025 14:35:10 GMT  
		Size: 13.1 KB (13143 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:944b0a29f1a3df2e2b3e79f2bb13dfdfb3a2b5b7e99b6987d316594946f07aa9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:0e88efedb05bcc7aaabacf6394a17660e11367c0767a64f3c1db2cc61d7197bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.6 MB (178637819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1b2930ec1013188ebb6c13e4e2c510b8be77b0d31df46cf374185d7707be51b`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d1b5af933d2dfc3d0dd509d6e20534825e4a537f7b006a6cb5b8e5a1f20905`  
		Last Modified: Tue, 08 Apr 2025 01:24:20 GMT  
		Size: 24.0 MB (24011090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb98adba0eb44a2e4facf9ca3626a4a66feedd0dd56d159cca90a35205744e7`  
		Last Modified: Tue, 08 Apr 2025 02:13:59 GMT  
		Size: 64.4 MB (64396468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658453baa222297e44ad439ac8d327171f4fbe033497ffa8e0e660a6107d16fd`  
		Last Modified: Tue, 08 Apr 2025 03:35:06 GMT  
		Size: 3.2 KB (3239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fde98860aa91372d1565b08fcb781798ea873a30d648bc9df749f82f4808cf3`  
		Last Modified: Tue, 08 Apr 2025 03:35:07 GMT  
		Size: 41.7 MB (41736481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:962d5df0b96909a741c47237f15064000303987883fb0c8db1087eedddf2f169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7769717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6339d9bfe76e514acfd2739109f46f2284aa4068ef043e66fa9e1e5ac97717`

```dockerfile
```

-	Layers:
	-	`sha256:8431dae4abc467001570a94ab98929de075ebec526cab7d64358937269e7ddf7`  
		Last Modified: Tue, 08 Apr 2025 03:35:07 GMT  
		Size: 7.8 MB (7756681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e30b9d461abb953c63c9f4fe3161b222b4b5d80375cb28ffbad512f440234d2`  
		Last Modified: Tue, 08 Apr 2025 03:35:06 GMT  
		Size: 13.0 KB (13036 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:56424347cbdb58d545dd024aa74e36812bb5cd504429d962fc9cfa18a3710121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176142842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1cd4355d4bfa12a5dbcd64e7aed3fb84e957e29101a8e98c45de8d713c03ca0`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4378a6c11dea5043896b9425853a850807e5845b0018fe01ddee56c16245fc3c`  
		Last Modified: Tue, 18 Mar 2025 05:00:37 GMT  
		Size: 23.5 MB (23544349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140d15be2fea6dcd21c20cadae2601a118c08a938168718b2612ad6aca91f74a`  
		Last Modified: Tue, 18 Mar 2025 13:13:07 GMT  
		Size: 64.4 MB (64355791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47adee9c6c100b72968c4214c8212a437fd4133a55e025becbfcf80201321f3`  
		Last Modified: Tue, 18 Mar 2025 14:35:10 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4f6ef112049b8b6a8d542134e78cbde095354fa59ffe018f391a219f755315`  
		Last Modified: Tue, 18 Mar 2025 14:35:12 GMT  
		Size: 39.9 MB (39934610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:3a0374e87a7fa8842cf91c55fafac0a8399735033a634dc04745e4105d694e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7774845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720cb8db8cc384888c52a6866e0c3f8b701aaa5695e86d06a748bdf50e972c09`

```dockerfile
```

-	Layers:
	-	`sha256:e598025b798fa61da776de6416222a57b31bec0d9f5b7c68e594e2e955ee30b9`  
		Last Modified: Tue, 18 Mar 2025 14:35:11 GMT  
		Size: 7.8 MB (7761702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:034ca069e9f372350214d5597a510d089b132965ace7419cb1f6415ce17cbec8`  
		Last Modified: Tue, 18 Mar 2025 14:35:10 GMT  
		Size: 13.1 KB (13143 bytes)  
		MIME: application/vnd.in-toto+json
