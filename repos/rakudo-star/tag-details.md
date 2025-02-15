<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rakudo-star`

-	[`rakudo-star:2024.12`](#rakudo-star202412)
-	[`rakudo-star:2024.12-alpine`](#rakudo-star202412-alpine)
-	[`rakudo-star:alpine`](#rakudo-staralpine)
-	[`rakudo-star:bookworm`](#rakudo-starbookworm)
-	[`rakudo-star:latest`](#rakudo-starlatest)

## `rakudo-star:2024.12`

```console
$ docker pull rakudo-star@sha256:e2f35bb1232faffb3b43a352517b0f5bc8d97481f6dd7d0d8bd880827c4f13a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2024.12` - linux; amd64

```console
$ docker pull rakudo-star@sha256:3a4062904dbd3387131c9b80f89533c248112a3ed7b12ad0e0e894f9e7aaca1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.7 MB (178659761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf258844201e9f05e50e70d58e4a6070b60a2b62a5cc6c9c10c1ec9e52d2b34e`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
MAINTAINER Rob Hoelz
# Mon, 16 Dec 2024 03:29:03 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ARG rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
ENV rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
# ARGS: rakudo_version=2024.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 04:24:49 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b550be6cb62359a0f3a96bc0dc289f8b45d097eaad275887f163c6780b4108`  
		Last Modified: Tue, 04 Feb 2025 07:11:25 GMT  
		Size: 24.1 MB (24058355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35af2a7690f2b43e7237d1fae8e3f2350dfb25f3249e9cf65121866f9c56c772`  
		Last Modified: Tue, 04 Feb 2025 08:41:29 GMT  
		Size: 64.4 MB (64394292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50803f5821153c4815b343850583733544b394fb4526c10452604bffa99df14d`  
		Last Modified: Wed, 05 Feb 2025 08:46:50 GMT  
		Size: 3.2 KB (3238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68cdfa22ab87593dc8af61fca81db647e9daa6916fbd761b0107a4b69c851069`  
		Last Modified: Tue, 04 Feb 2025 21:26:08 GMT  
		Size: 41.7 MB (41724189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2024.12` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:54ffc5a0ec100afce4792e6062bd9a6441e55081380a191e3cb605b2857dddff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7771997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ea66be6b290be0a36a385f95ee2d28f2a2a13a8440c6b872265cfb9d55a222`

```dockerfile
```

-	Layers:
	-	`sha256:7879d8cf0f8e635e4f708501e8300dbf8920d59c6c686a650318426b89423f2c`  
		Last Modified: Tue, 04 Feb 2025 06:32:27 GMT  
		Size: 7.8 MB (7758969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4b6cb850752414c1cd91d59db69e7563155288508516242efee07d678e3ed65`  
		Last Modified: Mon, 10 Feb 2025 23:28:44 GMT  
		Size: 13.0 KB (13028 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2024.12` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:b5576f83de9ac7199101fbadb51bc30ee64461f70aa802135b3ebc83c5538ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176253404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c74c30955383794eac475da2e5134948d656eafa62c74b6afd6fafb94ade1e`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
MAINTAINER Rob Hoelz
# Mon, 16 Dec 2024 03:29:03 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ARG rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
ENV rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
# ARGS: rakudo_version=2024.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 04:37:12 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193c44006e77abbadfdd7be72b4ab6d7a5c08640ef575970f722b798ee7800ac`  
		Last Modified: Wed, 05 Feb 2025 00:14:09 GMT  
		Size: 23.6 MB (23598428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d3572a68af0b860060b7ea84adfa8406fa20cfd1337c947dfb661aa965eee7`  
		Last Modified: Wed, 05 Feb 2025 02:21:14 GMT  
		Size: 64.4 MB (64357505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bef71704d9770a225e086540bae0d91a4c634990dc498fec26164490b2da66d`  
		Last Modified: Wed, 05 Feb 2025 03:22:58 GMT  
		Size: 3.2 KB (3243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc84db82893390f59835731f42d37a0d0aa46b91cfe1e4c1baf512a440e3fc4f`  
		Last Modified: Tue, 11 Feb 2025 00:56:22 GMT  
		Size: 40.0 MB (39987675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2024.12` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:d21301157f5199a0d268089e4b014429df52286755e53d0511b68456d5cf3fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7778509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aad112d73a39b3f326a80dfce6b6b9980ee1f1dbf9d141a8d0b03073f661108`

```dockerfile
```

-	Layers:
	-	`sha256:8cf33e3a2b068d3df517ebafb3259a6105603d14e9af3e98197fffbcead33972`  
		Last Modified: Mon, 10 Feb 2025 23:28:55 GMT  
		Size: 7.8 MB (7765374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0696a575dc03abc39bdf4b87dda9fff379c846cc7f3c81d93eca0fc4fb836a74`  
		Last Modified: Mon, 10 Feb 2025 23:28:54 GMT  
		Size: 13.1 KB (13135 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2024.12-alpine`

```console
$ docker pull rakudo-star@sha256:1d47c0dee5ff2579c3849dac0af1e63d9eb48da97a01c4efed8215d31ba49f84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2024.12-alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:23aba77146bc8518c7b882a04d72749bd661b2e15f8e7bc64ec9b7143f25c00b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45643641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f165d0f253935f04b5df1a8895c9ba661d597d9fcd432f01798f090c328da2d`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 16 Dec 2024 03:29:03 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 03:29:03 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ARG rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
ENV rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
# ARGS: rakudo_version=2024.12-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86564e6fe6ca585100328a41da0634754a68eb70c2bb2651af6fbf3c1e476c53`  
		Last Modified: Fri, 14 Feb 2025 19:33:14 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb98552c75fa02b9c86ca7980afddf4c289744ec8e900b52c14d978ef1ecc0a`  
		Last Modified: Fri, 14 Feb 2025 19:33:15 GMT  
		Size: 42.0 MB (42000448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2024.12-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:585611c8c5765b7e6a84c3530fdbd447823b8307477459a4265d8d7d19e8859b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 KB (132467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e0ae7369b89ac49eb5fa521d9ed93363fed9a60a74e56a6a1b67fca59e1b055`

```dockerfile
```

-	Layers:
	-	`sha256:55793d27d7b434e2fe29bc1b8e7098ca4ee42b21e9ae9bcddf3f810a1fe4d8a5`  
		Last Modified: Fri, 14 Feb 2025 23:33:15 GMT  
		Size: 120.7 KB (120726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afafa4aabe01f776e18ecc64c0f92be2b5fb24a745a2279314dae3c4d9b4df56`  
		Last Modified: Fri, 14 Feb 2025 23:33:16 GMT  
		Size: 11.7 KB (11741 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2024.12-alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:622a48f5c6f2f624089d829f8f0be7210b374c7581c7f9a458b10aa7adea71db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46532725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9eb6dc302a7500dbf738e889b531af4ce324c83fd0470ca1750f100088e411b`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 16 Dec 2024 03:29:03 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 03:29:03 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ARG rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
ENV rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
# ARGS: rakudo_version=2024.12-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59a85858ab78fc027ff09d8a5376e12d1c253c404713d7efe7405d9485c0658`  
		Last Modified: Thu, 09 Jan 2025 05:36:34 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bc37222c9c2729eb1560eab770571b8489e1b2a41d6798313691fa0d2bdce2`  
		Last Modified: Thu, 09 Jan 2025 05:36:36 GMT  
		Size: 42.5 MB (42539409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2024.12-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:32b4351b519969f0c07291760aa7923e07c04e43ba7d76032284154f54c3ef12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 KB (132588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ed771a17bc112b5eac37f476c31631d522c7fa10f84498efa3c8e98e02a3f0`

```dockerfile
```

-	Layers:
	-	`sha256:53a7bbdb39dd309755f0b861de59689e4c3d7ac365f1250395d2919a76fb13bc`  
		Last Modified: Fri, 14 Feb 2025 23:33:17 GMT  
		Size: 120.8 KB (120752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f29f769a60dffdc0a10299cbe78eceef4ea168da59c2a6d6d4d2f8f00091385`  
		Last Modified: Fri, 14 Feb 2025 23:33:17 GMT  
		Size: 11.8 KB (11836 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:1d47c0dee5ff2579c3849dac0af1e63d9eb48da97a01c4efed8215d31ba49f84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:23aba77146bc8518c7b882a04d72749bd661b2e15f8e7bc64ec9b7143f25c00b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45643641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f165d0f253935f04b5df1a8895c9ba661d597d9fcd432f01798f090c328da2d`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 16 Dec 2024 03:29:03 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 03:29:03 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ARG rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
ENV rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
# ARGS: rakudo_version=2024.12-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86564e6fe6ca585100328a41da0634754a68eb70c2bb2651af6fbf3c1e476c53`  
		Last Modified: Fri, 14 Feb 2025 19:33:14 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb98552c75fa02b9c86ca7980afddf4c289744ec8e900b52c14d978ef1ecc0a`  
		Last Modified: Fri, 14 Feb 2025 19:33:15 GMT  
		Size: 42.0 MB (42000448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:585611c8c5765b7e6a84c3530fdbd447823b8307477459a4265d8d7d19e8859b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 KB (132467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e0ae7369b89ac49eb5fa521d9ed93363fed9a60a74e56a6a1b67fca59e1b055`

```dockerfile
```

-	Layers:
	-	`sha256:55793d27d7b434e2fe29bc1b8e7098ca4ee42b21e9ae9bcddf3f810a1fe4d8a5`  
		Last Modified: Fri, 14 Feb 2025 23:33:15 GMT  
		Size: 120.7 KB (120726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afafa4aabe01f776e18ecc64c0f92be2b5fb24a745a2279314dae3c4d9b4df56`  
		Last Modified: Fri, 14 Feb 2025 23:33:16 GMT  
		Size: 11.7 KB (11741 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:622a48f5c6f2f624089d829f8f0be7210b374c7581c7f9a458b10aa7adea71db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46532725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9eb6dc302a7500dbf738e889b531af4ce324c83fd0470ca1750f100088e411b`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 16 Dec 2024 03:29:03 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 03:29:03 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ARG rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
ENV rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
# ARGS: rakudo_version=2024.12-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59a85858ab78fc027ff09d8a5376e12d1c253c404713d7efe7405d9485c0658`  
		Last Modified: Thu, 09 Jan 2025 05:36:34 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bc37222c9c2729eb1560eab770571b8489e1b2a41d6798313691fa0d2bdce2`  
		Last Modified: Thu, 09 Jan 2025 05:36:36 GMT  
		Size: 42.5 MB (42539409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:32b4351b519969f0c07291760aa7923e07c04e43ba7d76032284154f54c3ef12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 KB (132588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ed771a17bc112b5eac37f476c31631d522c7fa10f84498efa3c8e98e02a3f0`

```dockerfile
```

-	Layers:
	-	`sha256:53a7bbdb39dd309755f0b861de59689e4c3d7ac365f1250395d2919a76fb13bc`  
		Last Modified: Fri, 14 Feb 2025 23:33:17 GMT  
		Size: 120.8 KB (120752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f29f769a60dffdc0a10299cbe78eceef4ea168da59c2a6d6d4d2f8f00091385`  
		Last Modified: Fri, 14 Feb 2025 23:33:17 GMT  
		Size: 11.8 KB (11836 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:bookworm`

```console
$ docker pull rakudo-star@sha256:e2f35bb1232faffb3b43a352517b0f5bc8d97481f6dd7d0d8bd880827c4f13a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:3a4062904dbd3387131c9b80f89533c248112a3ed7b12ad0e0e894f9e7aaca1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.7 MB (178659761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf258844201e9f05e50e70d58e4a6070b60a2b62a5cc6c9c10c1ec9e52d2b34e`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
MAINTAINER Rob Hoelz
# Mon, 16 Dec 2024 03:29:03 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ARG rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
ENV rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
# ARGS: rakudo_version=2024.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 04:24:49 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b550be6cb62359a0f3a96bc0dc289f8b45d097eaad275887f163c6780b4108`  
		Last Modified: Tue, 04 Feb 2025 07:11:25 GMT  
		Size: 24.1 MB (24058355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35af2a7690f2b43e7237d1fae8e3f2350dfb25f3249e9cf65121866f9c56c772`  
		Last Modified: Tue, 04 Feb 2025 08:41:29 GMT  
		Size: 64.4 MB (64394292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50803f5821153c4815b343850583733544b394fb4526c10452604bffa99df14d`  
		Last Modified: Wed, 05 Feb 2025 08:46:50 GMT  
		Size: 3.2 KB (3238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68cdfa22ab87593dc8af61fca81db647e9daa6916fbd761b0107a4b69c851069`  
		Last Modified: Tue, 04 Feb 2025 21:26:08 GMT  
		Size: 41.7 MB (41724189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:54ffc5a0ec100afce4792e6062bd9a6441e55081380a191e3cb605b2857dddff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7771997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ea66be6b290be0a36a385f95ee2d28f2a2a13a8440c6b872265cfb9d55a222`

```dockerfile
```

-	Layers:
	-	`sha256:7879d8cf0f8e635e4f708501e8300dbf8920d59c6c686a650318426b89423f2c`  
		Last Modified: Tue, 04 Feb 2025 06:32:27 GMT  
		Size: 7.8 MB (7758969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4b6cb850752414c1cd91d59db69e7563155288508516242efee07d678e3ed65`  
		Last Modified: Mon, 10 Feb 2025 23:28:44 GMT  
		Size: 13.0 KB (13028 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:b5576f83de9ac7199101fbadb51bc30ee64461f70aa802135b3ebc83c5538ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176253404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c74c30955383794eac475da2e5134948d656eafa62c74b6afd6fafb94ade1e`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
MAINTAINER Rob Hoelz
# Mon, 16 Dec 2024 03:29:03 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ARG rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
ENV rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
# ARGS: rakudo_version=2024.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 04:37:12 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193c44006e77abbadfdd7be72b4ab6d7a5c08640ef575970f722b798ee7800ac`  
		Last Modified: Wed, 05 Feb 2025 00:14:09 GMT  
		Size: 23.6 MB (23598428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d3572a68af0b860060b7ea84adfa8406fa20cfd1337c947dfb661aa965eee7`  
		Last Modified: Wed, 05 Feb 2025 02:21:14 GMT  
		Size: 64.4 MB (64357505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bef71704d9770a225e086540bae0d91a4c634990dc498fec26164490b2da66d`  
		Last Modified: Wed, 05 Feb 2025 03:22:58 GMT  
		Size: 3.2 KB (3243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc84db82893390f59835731f42d37a0d0aa46b91cfe1e4c1baf512a440e3fc4f`  
		Last Modified: Tue, 11 Feb 2025 00:56:22 GMT  
		Size: 40.0 MB (39987675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:d21301157f5199a0d268089e4b014429df52286755e53d0511b68456d5cf3fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7778509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aad112d73a39b3f326a80dfce6b6b9980ee1f1dbf9d141a8d0b03073f661108`

```dockerfile
```

-	Layers:
	-	`sha256:8cf33e3a2b068d3df517ebafb3259a6105603d14e9af3e98197fffbcead33972`  
		Last Modified: Mon, 10 Feb 2025 23:28:55 GMT  
		Size: 7.8 MB (7765374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0696a575dc03abc39bdf4b87dda9fff379c846cc7f3c81d93eca0fc4fb836a74`  
		Last Modified: Mon, 10 Feb 2025 23:28:54 GMT  
		Size: 13.1 KB (13135 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:e2f35bb1232faffb3b43a352517b0f5bc8d97481f6dd7d0d8bd880827c4f13a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:3a4062904dbd3387131c9b80f89533c248112a3ed7b12ad0e0e894f9e7aaca1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.7 MB (178659761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf258844201e9f05e50e70d58e4a6070b60a2b62a5cc6c9c10c1ec9e52d2b34e`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
MAINTAINER Rob Hoelz
# Mon, 16 Dec 2024 03:29:03 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ARG rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
ENV rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
# ARGS: rakudo_version=2024.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 04:24:49 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b550be6cb62359a0f3a96bc0dc289f8b45d097eaad275887f163c6780b4108`  
		Last Modified: Tue, 04 Feb 2025 07:11:25 GMT  
		Size: 24.1 MB (24058355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35af2a7690f2b43e7237d1fae8e3f2350dfb25f3249e9cf65121866f9c56c772`  
		Last Modified: Tue, 04 Feb 2025 08:41:29 GMT  
		Size: 64.4 MB (64394292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50803f5821153c4815b343850583733544b394fb4526c10452604bffa99df14d`  
		Last Modified: Wed, 05 Feb 2025 08:46:50 GMT  
		Size: 3.2 KB (3238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68cdfa22ab87593dc8af61fca81db647e9daa6916fbd761b0107a4b69c851069`  
		Last Modified: Tue, 04 Feb 2025 21:26:08 GMT  
		Size: 41.7 MB (41724189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:54ffc5a0ec100afce4792e6062bd9a6441e55081380a191e3cb605b2857dddff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7771997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ea66be6b290be0a36a385f95ee2d28f2a2a13a8440c6b872265cfb9d55a222`

```dockerfile
```

-	Layers:
	-	`sha256:7879d8cf0f8e635e4f708501e8300dbf8920d59c6c686a650318426b89423f2c`  
		Last Modified: Tue, 04 Feb 2025 06:32:27 GMT  
		Size: 7.8 MB (7758969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4b6cb850752414c1cd91d59db69e7563155288508516242efee07d678e3ed65`  
		Last Modified: Mon, 10 Feb 2025 23:28:44 GMT  
		Size: 13.0 KB (13028 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:b5576f83de9ac7199101fbadb51bc30ee64461f70aa802135b3ebc83c5538ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176253404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c74c30955383794eac475da2e5134948d656eafa62c74b6afd6fafb94ade1e`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
MAINTAINER Rob Hoelz
# Mon, 16 Dec 2024 03:29:03 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ARG rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
ENV rakudo_version=2024.12-01
# Mon, 16 Dec 2024 03:29:03 GMT
# ARGS: rakudo_version=2024.12-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Dec 2024 03:29:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 16 Dec 2024 03:29:03 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 04:37:12 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193c44006e77abbadfdd7be72b4ab6d7a5c08640ef575970f722b798ee7800ac`  
		Last Modified: Wed, 05 Feb 2025 00:14:09 GMT  
		Size: 23.6 MB (23598428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d3572a68af0b860060b7ea84adfa8406fa20cfd1337c947dfb661aa965eee7`  
		Last Modified: Wed, 05 Feb 2025 02:21:14 GMT  
		Size: 64.4 MB (64357505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bef71704d9770a225e086540bae0d91a4c634990dc498fec26164490b2da66d`  
		Last Modified: Wed, 05 Feb 2025 03:22:58 GMT  
		Size: 3.2 KB (3243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc84db82893390f59835731f42d37a0d0aa46b91cfe1e4c1baf512a440e3fc4f`  
		Last Modified: Tue, 11 Feb 2025 00:56:22 GMT  
		Size: 40.0 MB (39987675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:d21301157f5199a0d268089e4b014429df52286755e53d0511b68456d5cf3fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7778509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aad112d73a39b3f326a80dfce6b6b9980ee1f1dbf9d141a8d0b03073f661108`

```dockerfile
```

-	Layers:
	-	`sha256:8cf33e3a2b068d3df517ebafb3259a6105603d14e9af3e98197fffbcead33972`  
		Last Modified: Mon, 10 Feb 2025 23:28:55 GMT  
		Size: 7.8 MB (7765374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0696a575dc03abc39bdf4b87dda9fff379c846cc7f3c81d93eca0fc4fb836a74`  
		Last Modified: Mon, 10 Feb 2025 23:28:54 GMT  
		Size: 13.1 KB (13135 bytes)  
		MIME: application/vnd.in-toto+json
