<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rakudo-star`

-	[`rakudo-star:2021.04`](#rakudo-star202104)
-	[`rakudo-star:2021.04-alpine`](#rakudo-star202104-alpine)
-	[`rakudo-star:alpine`](#rakudo-staralpine)
-	[`rakudo-star:latest`](#rakudo-starlatest)

## `rakudo-star:2021.04`

```console
$ docker pull rakudo-star@sha256:97daecbf6008c1545f489c1d52ab43cd9c9baf54d77eb62a3604971afa2fb5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `rakudo-star:2021.04` - linux; amd64

```console
$ docker pull rakudo-star@sha256:36f8f465398de2f669dfa28222eea41d886a07ac3806c0a5e2fd6bc0fbf17e92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.9 MB (161907567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17018f9b31aeda41c822cd86f88b2f44f86eb0ac3ff9e0392318978b486caeb1`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:14 GMT
ADD file:647206e0e9c1daa306e4ebbdc26c3ef1840dd316ba4ffea905d17b0858e58e34 in / 
# Tue, 02 Aug 2022 01:20:14 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:48:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 01:48:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 02:08:58 GMT
MAINTAINER Rob Hoelz
# Wed, 03 Aug 2022 02:08:58 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku
# Wed, 03 Aug 2022 02:08:58 GMT
ARG rakudo_version=2021.04
# Wed, 03 Aug 2022 02:08:59 GMT
ENV rakudo_version=2021.04
# Wed, 03 Aug 2022 02:18:26 GMT
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir"     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps
# Wed, 03 Aug 2022 02:18:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 03 Aug 2022 02:18:27 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:7e6a53d1988fa8e19db6bcfc96ee6783afb079c38dbe047528e691815d19a9fa`  
		Last Modified: Tue, 02 Aug 2022 01:24:34 GMT  
		Size: 50.4 MB (50440980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe4e1c58b4af82939a918665dd1e7b5b636dd73c710b4bccb530edbb15470d2`  
		Last Modified: Tue, 02 Aug 2022 02:19:38 GMT  
		Size: 7.9 MB (7856856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc915d298757b72963f0d061cc16ca4925e9f4481446b87a5297b4043ffc8033`  
		Last Modified: Tue, 02 Aug 2022 02:19:38 GMT  
		Size: 10.0 MB (9998020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f08b88f29371de7c9ac165381b7426349760f6af3f205e8716426fafce4a1ff2`  
		Last Modified: Tue, 02 Aug 2022 02:19:56 GMT  
		Size: 51.8 MB (51843653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62c59945875f380a99e1d6fa4b5b794a7dba285671f9403ad18133696379332b`  
		Last Modified: Wed, 03 Aug 2022 02:18:47 GMT  
		Size: 4.1 KB (4127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d940b82db4b9fe2c5aaa6ab368df4cf7d061e036f551ab6c350ed01b44bf37`  
		Last Modified: Wed, 03 Aug 2022 02:18:55 GMT  
		Size: 41.8 MB (41763931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rakudo-star:2021.04` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:94e2dd8132cf0ca7a088357300ae5db7522121c00ab78a257c41f8c77b226bd3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160211161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e266fb3b6b34cf3337a2717c6bc43633b0487f580c64dd0cd8ea611abdb21c9`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:49 GMT
ADD file:dfd7e3791fa0512f0f7c9cc8530233d6bc1b0a586a3656fd3950ea386754808a in / 
# Tue, 02 Aug 2022 00:40:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:25:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:25:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 01:26:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 23:00:28 GMT
MAINTAINER Rob Hoelz
# Tue, 02 Aug 2022 23:00:29 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku
# Tue, 02 Aug 2022 23:00:29 GMT
ARG rakudo_version=2021.04
# Tue, 02 Aug 2022 23:00:30 GMT
ENV rakudo_version=2021.04
# Tue, 02 Aug 2022 23:10:13 GMT
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir"     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Aug 2022 23:10:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 02 Aug 2022 23:10:15 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:71209d5eb534b9e48223962276993c68559f68e230f73c8a0efc2a2998362bd9`  
		Last Modified: Tue, 02 Aug 2022 00:46:28 GMT  
		Size: 49.2 MB (49229053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31ca5ccee8fca6610f14b5ed35ac33bb5f545532b6583e1461037a083c3d87b`  
		Last Modified: Tue, 02 Aug 2022 01:45:50 GMT  
		Size: 7.7 MB (7719992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32de8e1f96ccb825d3be85704be7218044a19ff05ea1eea0222e8c942fbf6f8f`  
		Last Modified: Tue, 02 Aug 2022 01:45:50 GMT  
		Size: 9.8 MB (9768645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:965555a6fd3b7a1727fd927269ea37139a09652f2545ea1c825b36af887f2713`  
		Last Modified: Tue, 02 Aug 2022 01:46:10 GMT  
		Size: 52.2 MB (52175033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4405304c275f947b2c2cd44abbdad41b2ad3851ad174f217480ed639c6353dc8`  
		Last Modified: Tue, 02 Aug 2022 23:10:43 GMT  
		Size: 4.0 KB (4008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748006999ceac23695300bdb57f01e26118715adeb16d830c84a9e3226446f6d`  
		Last Modified: Tue, 02 Aug 2022 23:10:51 GMT  
		Size: 41.3 MB (41314430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rakudo-star:2021.04-alpine`

```console
$ docker pull rakudo-star@sha256:61cd3d96123f2d71643fb1785370ba283f777876ddc6ea72880043a373e1c49a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `rakudo-star:2021.04-alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:46491f4b4f12431344aeb426e7505b7c898470a7042fc9f6eaec4d75c6db188b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44244087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:445e260c20a3cb96b8664a85e96cc0568500d69589b8b08d4f4e0b856882e88a`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:26 GMT
ADD file:e15461ac94648d9599df6304a53587fc8bfceaf6e111ee5917860e95ed9e751c in / 
# Tue, 19 Jul 2022 22:20:26 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 01:48:35 GMT
RUN addgroup -S raku && adduser -S raku -G raku
# Wed, 20 Jul 2022 01:48:35 GMT
ARG rakudo_version=2021.04
# Wed, 20 Jul 2022 01:48:35 GMT
ENV rakudo_version=2021.04
# Wed, 20 Jul 2022 01:59:52 GMT
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir"     && apk add --no-cache --virtual .build-deps $buildDeps     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps
# Wed, 20 Jul 2022 01:59:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 20 Jul 2022 01:59:52 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:627fad6f28f79c3907ad18a4399be4d810c0e1bb503fe3712217145c555b9d2f`  
		Last Modified: Tue, 19 Jul 2022 22:21:04 GMT  
		Size: 2.8 MB (2819330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b46bdccf24903754fe9cb19010b423e8fd4098d0a24c2cead6052a7db252548`  
		Last Modified: Wed, 20 Jul 2022 02:00:07 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f72a7e6485c9191c2af8c469c27fa952ecb29b0bd540ca230e2ee8ce22db6f8`  
		Last Modified: Wed, 20 Jul 2022 02:00:15 GMT  
		Size: 41.4 MB (41423502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rakudo-star:2021.04-alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:51d1fd251ca7f00e06df63672a26f933a4d1367d570f0b33f56dcf9bec31cf5e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43948297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2487d5a483e46f3b3a88136575e09216f633d87c1de5df26db856675d77d8847`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 19 Jul 2022 22:39:59 GMT
ADD file:b501d234551d6b0f6f40b3533140338e5bc0d798a5699409f0fb5974318507d7 in / 
# Tue, 19 Jul 2022 22:40:00 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 03:16:39 GMT
RUN addgroup -S raku && adduser -S raku -G raku
# Wed, 20 Jul 2022 03:16:40 GMT
ARG rakudo_version=2021.04
# Wed, 20 Jul 2022 03:16:41 GMT
ENV rakudo_version=2021.04
# Wed, 20 Jul 2022 03:28:20 GMT
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir"     && apk add --no-cache --virtual .build-deps $buildDeps     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps
# Wed, 20 Jul 2022 03:28:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 20 Jul 2022 03:28:21 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:e1e3bb43032bb6c47cf7fce8f9be50ba91100ca9d50c31130e9f56d3664daa23`  
		Last Modified: Tue, 19 Jul 2022 22:40:55 GMT  
		Size: 2.7 MB (2721189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c43b617165c243ac407a4ad03d6ad8d615d43707ea02dc1ad073281bf67b8d`  
		Last Modified: Wed, 20 Jul 2022 03:28:50 GMT  
		Size: 1.2 KB (1227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03ec038028bf949800eb04ae9a3279e57821c6d40b05076c73a43248da3c053`  
		Last Modified: Wed, 20 Jul 2022 03:28:58 GMT  
		Size: 41.2 MB (41225881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:61cd3d96123f2d71643fb1785370ba283f777876ddc6ea72880043a373e1c49a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:46491f4b4f12431344aeb426e7505b7c898470a7042fc9f6eaec4d75c6db188b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44244087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:445e260c20a3cb96b8664a85e96cc0568500d69589b8b08d4f4e0b856882e88a`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:26 GMT
ADD file:e15461ac94648d9599df6304a53587fc8bfceaf6e111ee5917860e95ed9e751c in / 
# Tue, 19 Jul 2022 22:20:26 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 01:48:35 GMT
RUN addgroup -S raku && adduser -S raku -G raku
# Wed, 20 Jul 2022 01:48:35 GMT
ARG rakudo_version=2021.04
# Wed, 20 Jul 2022 01:48:35 GMT
ENV rakudo_version=2021.04
# Wed, 20 Jul 2022 01:59:52 GMT
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir"     && apk add --no-cache --virtual .build-deps $buildDeps     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps
# Wed, 20 Jul 2022 01:59:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 20 Jul 2022 01:59:52 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:627fad6f28f79c3907ad18a4399be4d810c0e1bb503fe3712217145c555b9d2f`  
		Last Modified: Tue, 19 Jul 2022 22:21:04 GMT  
		Size: 2.8 MB (2819330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b46bdccf24903754fe9cb19010b423e8fd4098d0a24c2cead6052a7db252548`  
		Last Modified: Wed, 20 Jul 2022 02:00:07 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f72a7e6485c9191c2af8c469c27fa952ecb29b0bd540ca230e2ee8ce22db6f8`  
		Last Modified: Wed, 20 Jul 2022 02:00:15 GMT  
		Size: 41.4 MB (41423502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:51d1fd251ca7f00e06df63672a26f933a4d1367d570f0b33f56dcf9bec31cf5e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43948297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2487d5a483e46f3b3a88136575e09216f633d87c1de5df26db856675d77d8847`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 19 Jul 2022 22:39:59 GMT
ADD file:b501d234551d6b0f6f40b3533140338e5bc0d798a5699409f0fb5974318507d7 in / 
# Tue, 19 Jul 2022 22:40:00 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 03:16:39 GMT
RUN addgroup -S raku && adduser -S raku -G raku
# Wed, 20 Jul 2022 03:16:40 GMT
ARG rakudo_version=2021.04
# Wed, 20 Jul 2022 03:16:41 GMT
ENV rakudo_version=2021.04
# Wed, 20 Jul 2022 03:28:20 GMT
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir"     && apk add --no-cache --virtual .build-deps $buildDeps     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps
# Wed, 20 Jul 2022 03:28:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 20 Jul 2022 03:28:21 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:e1e3bb43032bb6c47cf7fce8f9be50ba91100ca9d50c31130e9f56d3664daa23`  
		Last Modified: Tue, 19 Jul 2022 22:40:55 GMT  
		Size: 2.7 MB (2721189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c43b617165c243ac407a4ad03d6ad8d615d43707ea02dc1ad073281bf67b8d`  
		Last Modified: Wed, 20 Jul 2022 03:28:50 GMT  
		Size: 1.2 KB (1227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03ec038028bf949800eb04ae9a3279e57821c6d40b05076c73a43248da3c053`  
		Last Modified: Wed, 20 Jul 2022 03:28:58 GMT  
		Size: 41.2 MB (41225881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:97daecbf6008c1545f489c1d52ab43cd9c9baf54d77eb62a3604971afa2fb5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:36f8f465398de2f669dfa28222eea41d886a07ac3806c0a5e2fd6bc0fbf17e92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.9 MB (161907567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17018f9b31aeda41c822cd86f88b2f44f86eb0ac3ff9e0392318978b486caeb1`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:14 GMT
ADD file:647206e0e9c1daa306e4ebbdc26c3ef1840dd316ba4ffea905d17b0858e58e34 in / 
# Tue, 02 Aug 2022 01:20:14 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:48:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 01:48:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 02:08:58 GMT
MAINTAINER Rob Hoelz
# Wed, 03 Aug 2022 02:08:58 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku
# Wed, 03 Aug 2022 02:08:58 GMT
ARG rakudo_version=2021.04
# Wed, 03 Aug 2022 02:08:59 GMT
ENV rakudo_version=2021.04
# Wed, 03 Aug 2022 02:18:26 GMT
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir"     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps
# Wed, 03 Aug 2022 02:18:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 03 Aug 2022 02:18:27 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:7e6a53d1988fa8e19db6bcfc96ee6783afb079c38dbe047528e691815d19a9fa`  
		Last Modified: Tue, 02 Aug 2022 01:24:34 GMT  
		Size: 50.4 MB (50440980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe4e1c58b4af82939a918665dd1e7b5b636dd73c710b4bccb530edbb15470d2`  
		Last Modified: Tue, 02 Aug 2022 02:19:38 GMT  
		Size: 7.9 MB (7856856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc915d298757b72963f0d061cc16ca4925e9f4481446b87a5297b4043ffc8033`  
		Last Modified: Tue, 02 Aug 2022 02:19:38 GMT  
		Size: 10.0 MB (9998020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f08b88f29371de7c9ac165381b7426349760f6af3f205e8716426fafce4a1ff2`  
		Last Modified: Tue, 02 Aug 2022 02:19:56 GMT  
		Size: 51.8 MB (51843653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62c59945875f380a99e1d6fa4b5b794a7dba285671f9403ad18133696379332b`  
		Last Modified: Wed, 03 Aug 2022 02:18:47 GMT  
		Size: 4.1 KB (4127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d940b82db4b9fe2c5aaa6ab368df4cf7d061e036f551ab6c350ed01b44bf37`  
		Last Modified: Wed, 03 Aug 2022 02:18:55 GMT  
		Size: 41.8 MB (41763931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:94e2dd8132cf0ca7a088357300ae5db7522121c00ab78a257c41f8c77b226bd3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160211161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e266fb3b6b34cf3337a2717c6bc43633b0487f580c64dd0cd8ea611abdb21c9`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:49 GMT
ADD file:dfd7e3791fa0512f0f7c9cc8530233d6bc1b0a586a3656fd3950ea386754808a in / 
# Tue, 02 Aug 2022 00:40:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:25:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:25:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 01:26:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 23:00:28 GMT
MAINTAINER Rob Hoelz
# Tue, 02 Aug 2022 23:00:29 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku
# Tue, 02 Aug 2022 23:00:29 GMT
ARG rakudo_version=2021.04
# Tue, 02 Aug 2022 23:00:30 GMT
ENV rakudo_version=2021.04
# Tue, 02 Aug 2022 23:10:13 GMT
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir"     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Aug 2022 23:10:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 02 Aug 2022 23:10:15 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:71209d5eb534b9e48223962276993c68559f68e230f73c8a0efc2a2998362bd9`  
		Last Modified: Tue, 02 Aug 2022 00:46:28 GMT  
		Size: 49.2 MB (49229053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31ca5ccee8fca6610f14b5ed35ac33bb5f545532b6583e1461037a083c3d87b`  
		Last Modified: Tue, 02 Aug 2022 01:45:50 GMT  
		Size: 7.7 MB (7719992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32de8e1f96ccb825d3be85704be7218044a19ff05ea1eea0222e8c942fbf6f8f`  
		Last Modified: Tue, 02 Aug 2022 01:45:50 GMT  
		Size: 9.8 MB (9768645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:965555a6fd3b7a1727fd927269ea37139a09652f2545ea1c825b36af887f2713`  
		Last Modified: Tue, 02 Aug 2022 01:46:10 GMT  
		Size: 52.2 MB (52175033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4405304c275f947b2c2cd44abbdad41b2ad3851ad174f217480ed639c6353dc8`  
		Last Modified: Tue, 02 Aug 2022 23:10:43 GMT  
		Size: 4.0 KB (4008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748006999ceac23695300bdb57f01e26118715adeb16d830c84a9e3226446f6d`  
		Last Modified: Tue, 02 Aug 2022 23:10:51 GMT  
		Size: 41.3 MB (41314430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
