<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rakudo-star`

-	[`rakudo-star:2025.02-alpine`](#rakudo-star202502-alpine)
-	[`rakudo-star:2025.04`](#rakudo-star202504)
-	[`rakudo-star:alpine`](#rakudo-staralpine)
-	[`rakudo-star:bookworm`](#rakudo-starbookworm)
-	[`rakudo-star:latest`](#rakudo-starlatest)

## `rakudo-star:2025.02-alpine`

```console
$ docker pull rakudo-star@sha256:733926aaef881636c8d41b6d9fe512fa4737c276c6f21c2d73cc47e64faf8b23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2025.02-alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:65ccf5a6535365ec0e66eea091ef60399ffda33516f8e8c38e9e0e2d4aecbd71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46495094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141b28e760a6e18d2e29f898e3ba59d899f7cfb1cb55220edbdf571fa8131177`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 06 Mar 2025 03:06:23 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
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
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb53db3671de4f8476a6eaf70e8b7f2afb36a19230d96cecfe6b4ac374c0bc7`  
		Last Modified: Tue, 03 Jun 2025 18:05:38 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67645ceca8b9a31967a6ae3e839ef199a712b1ad66c4a21dc7b44f75c3b06ff`  
		Last Modified: Tue, 03 Jun 2025 18:05:42 GMT  
		Size: 42.7 MB (42697302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.02-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:3b4a1355f7be87536ae0b6657480a1ce4e5032d7ac54410d60df17109038c536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 KB (135970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5acf83fc6e32ce0cc80718ef6c901589404a7bd50a0045eeb9c746012318bf75`

```dockerfile
```

-	Layers:
	-	`sha256:fbaab3828903602344fabb36ba9922996d8a4e992345956de3e8de849963a5f9`  
		Last Modified: Fri, 30 May 2025 18:28:29 GMT  
		Size: 124.2 KB (124221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96075b0510448a463b05851acb6c3cdb26047db661c6ab1e5df701ee4afbf857`  
		Last Modified: Fri, 30 May 2025 18:28:29 GMT  
		Size: 11.7 KB (11749 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2025.02-alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:45a53f0e8b2e098e8bc167bef237602d20ae1d123dcb8ae6313504a61f8ff6ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46061907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a1817895d6647351a32f552dd5d1f19ca57bb650f8c952369c09c90e6b9a0ad`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 06 Mar 2025 03:06:23 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
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
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8fcd5bb33822e32875db9d76923db3d2607b14440de8c282f58f1e60427b19`  
		Last Modified: Sat, 07 Jun 2025 10:02:23 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b81fbc145f194ef534bd5e79650e4772b4ff2bc733b6c46e49cf3b1d774a14b`  
		Last Modified: Sat, 07 Jun 2025 10:02:26 GMT  
		Size: 41.9 MB (41925020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.02-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:658ab323283df3bab5d630fd4ce10c7455271da935f814d0153ac77b7d368a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 KB (136097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3df9752c11f6e5bbd4a90d610ff3f4ea861bf8903e07135e2dc8700c468de476`

```dockerfile
```

-	Layers:
	-	`sha256:d5126d560c303e194b739b46b27a49648933b4b366ed10511c35deefe3c43c61`  
		Last Modified: Fri, 30 May 2025 18:50:04 GMT  
		Size: 124.3 KB (124253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18a30ae3a2307818923c1d2463fcc892d62c82542cfa2567c9d652fdc2a0912c`  
		Last Modified: Fri, 30 May 2025 18:50:04 GMT  
		Size: 11.8 KB (11844 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2025.04`

```console
$ docker pull rakudo-star@sha256:4df675ca634dbb1afd689f8a89a72693551175f86d45c03212575e5128ba423e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2025.04` - linux; amd64

```console
$ docker pull rakudo-star@sha256:81558fd9ebdf5f42a0630d36dc7b67f290c23485c1f1d6aa7fc3e69fb0db59fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.4 MB (178363465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e916c40263620670e8c5ab1e24081682f6213b2c04c3ec45e856cf95842ec87a`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Apr 2025 03:13:04 GMT
MAINTAINER Rob Hoelz
# Thu, 24 Apr 2025 03:13:04 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 24 Apr 2025 03:13:04 GMT
ARG rakudo_version=2025.04-01
# Thu, 24 Apr 2025 03:13:04 GMT
ENV rakudo_version=2025.04-01
# Thu, 24 Apr 2025 03:13:04 GMT
# ARGS: rakudo_version=2025.04-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 24 Apr 2025 03:13:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 24 Apr 2025 03:13:04 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b8a0660a31403a35d70b276c3c86b1200b8683e83cd77a92ec98744017684a`  
		Last Modified: Wed, 11 Jun 2025 00:02:18 GMT  
		Size: 64.4 MB (64399794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068456311fedebd1b2656282dcb35f0e4623994f69d727546ca7611584aff9f1`  
		Last Modified: Wed, 11 Jun 2025 01:34:33 GMT  
		Size: 3.2 KB (3241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d2b0f60cf9cb3716e55a68dd040f3a339bb863368ec1f8a949a6e88070180a`  
		Last Modified: Wed, 11 Jun 2025 04:42:37 GMT  
		Size: 41.5 MB (41450450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.04` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:e525174ea6d0518e410d4e66a0cfaad9f9c20a29fef2b8878088c6166d8e78a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7973001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fd4fc4cdd62d101df5323930cdbf9e7e6f2cc4ee6b584f200bf4ecc7b91d4d2`

```dockerfile
```

-	Layers:
	-	`sha256:715b7e027af961fe106c2fa5cd2b5621190698b0197e959d020215274c9a65fd`  
		Last Modified: Wed, 11 Jun 2025 04:33:19 GMT  
		Size: 8.0 MB (7959965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd1136216a709f0595980a32e4e0c070ea353db561ddb21a43a36b65f81c8a2f`  
		Last Modified: Wed, 11 Jun 2025 04:33:20 GMT  
		Size: 13.0 KB (13036 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2025.04` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:e29b54b3d047e02a16d862f486e05f3e25b9663773921a5880eab31626ab5cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175360191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ff3e8e1407c700846c9b24c543d9742d4a0d1f1e0ff1448ff6febbecd27107`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Apr 2025 03:13:04 GMT
MAINTAINER Rob Hoelz
# Thu, 24 Apr 2025 03:13:04 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 24 Apr 2025 03:13:04 GMT
ARG rakudo_version=2025.04-01
# Thu, 24 Apr 2025 03:13:04 GMT
ENV rakudo_version=2025.04-01
# Thu, 24 Apr 2025 03:13:04 GMT
# ARGS: rakudo_version=2025.04-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 24 Apr 2025 03:13:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 24 Apr 2025 03:13:04 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e137b9ec173f900a44376f31987bb15c0f5bb562aa6f8ad5db5a090ec88b2e`  
		Last Modified: Wed, 11 Jun 2025 02:56:23 GMT  
		Size: 23.6 MB (23551557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f5719d6358cc525f45e16c04ce36e5245978df9021dec8d0619729d9de8537`  
		Last Modified: Wed, 11 Jun 2025 10:32:40 GMT  
		Size: 64.4 MB (64362852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3ab978bb90e433bb72f30e43795229cf857c7fe5fea07a609567d094447f26`  
		Last Modified: Wed, 11 Jun 2025 16:49:58 GMT  
		Size: 3.2 KB (3239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1d5546fc81c2152986f6da7cde9916c0eb0d40e8f35866b331852f0b481b3c`  
		Last Modified: Wed, 11 Jun 2025 16:50:01 GMT  
		Size: 39.1 MB (39103691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.04` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:32a52fe72e100c85f3948a4a0df542d9a604216d189a6432b2a47cb3b07bf685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7979513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13d55ef5344a439f05d7a80c9999549cb3445d1193de013c563511b153a26df`

```dockerfile
```

-	Layers:
	-	`sha256:4f69a15b9932da8c3fb6409707a4b9f8937ef5f6ceb6ca705cb1b262bfd4dce2`  
		Last Modified: Wed, 11 Jun 2025 19:33:23 GMT  
		Size: 8.0 MB (7966370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b40af88763a2e0ec4816a9eabedcbbb136526825c5f949093c810abe5910cc3b`  
		Last Modified: Wed, 11 Jun 2025 19:33:24 GMT  
		Size: 13.1 KB (13143 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:733926aaef881636c8d41b6d9fe512fa4737c276c6f21c2d73cc47e64faf8b23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:65ccf5a6535365ec0e66eea091ef60399ffda33516f8e8c38e9e0e2d4aecbd71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46495094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141b28e760a6e18d2e29f898e3ba59d899f7cfb1cb55220edbdf571fa8131177`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 06 Mar 2025 03:06:23 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
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
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb53db3671de4f8476a6eaf70e8b7f2afb36a19230d96cecfe6b4ac374c0bc7`  
		Last Modified: Tue, 03 Jun 2025 18:05:38 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67645ceca8b9a31967a6ae3e839ef199a712b1ad66c4a21dc7b44f75c3b06ff`  
		Last Modified: Tue, 03 Jun 2025 18:05:42 GMT  
		Size: 42.7 MB (42697302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:3b4a1355f7be87536ae0b6657480a1ce4e5032d7ac54410d60df17109038c536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 KB (135970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5acf83fc6e32ce0cc80718ef6c901589404a7bd50a0045eeb9c746012318bf75`

```dockerfile
```

-	Layers:
	-	`sha256:fbaab3828903602344fabb36ba9922996d8a4e992345956de3e8de849963a5f9`  
		Last Modified: Fri, 30 May 2025 18:28:29 GMT  
		Size: 124.2 KB (124221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96075b0510448a463b05851acb6c3cdb26047db661c6ab1e5df701ee4afbf857`  
		Last Modified: Fri, 30 May 2025 18:28:29 GMT  
		Size: 11.7 KB (11749 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:45a53f0e8b2e098e8bc167bef237602d20ae1d123dcb8ae6313504a61f8ff6ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46061907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a1817895d6647351a32f552dd5d1f19ca57bb650f8c952369c09c90e6b9a0ad`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 06 Mar 2025 03:06:23 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Thu, 06 Mar 2025 03:06:23 GMT
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
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8fcd5bb33822e32875db9d76923db3d2607b14440de8c282f58f1e60427b19`  
		Last Modified: Sat, 07 Jun 2025 10:02:23 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b81fbc145f194ef534bd5e79650e4772b4ff2bc733b6c46e49cf3b1d774a14b`  
		Last Modified: Sat, 07 Jun 2025 10:02:26 GMT  
		Size: 41.9 MB (41925020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:658ab323283df3bab5d630fd4ce10c7455271da935f814d0153ac77b7d368a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 KB (136097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3df9752c11f6e5bbd4a90d610ff3f4ea861bf8903e07135e2dc8700c468de476`

```dockerfile
```

-	Layers:
	-	`sha256:d5126d560c303e194b739b46b27a49648933b4b366ed10511c35deefe3c43c61`  
		Last Modified: Fri, 30 May 2025 18:50:04 GMT  
		Size: 124.3 KB (124253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18a30ae3a2307818923c1d2463fcc892d62c82542cfa2567c9d652fdc2a0912c`  
		Last Modified: Fri, 30 May 2025 18:50:04 GMT  
		Size: 11.8 KB (11844 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:bookworm`

```console
$ docker pull rakudo-star@sha256:4df675ca634dbb1afd689f8a89a72693551175f86d45c03212575e5128ba423e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:81558fd9ebdf5f42a0630d36dc7b67f290c23485c1f1d6aa7fc3e69fb0db59fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.4 MB (178363465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e916c40263620670e8c5ab1e24081682f6213b2c04c3ec45e856cf95842ec87a`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Apr 2025 03:13:04 GMT
MAINTAINER Rob Hoelz
# Thu, 24 Apr 2025 03:13:04 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 24 Apr 2025 03:13:04 GMT
ARG rakudo_version=2025.04-01
# Thu, 24 Apr 2025 03:13:04 GMT
ENV rakudo_version=2025.04-01
# Thu, 24 Apr 2025 03:13:04 GMT
# ARGS: rakudo_version=2025.04-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 24 Apr 2025 03:13:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 24 Apr 2025 03:13:04 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b8a0660a31403a35d70b276c3c86b1200b8683e83cd77a92ec98744017684a`  
		Last Modified: Wed, 11 Jun 2025 00:02:18 GMT  
		Size: 64.4 MB (64399794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068456311fedebd1b2656282dcb35f0e4623994f69d727546ca7611584aff9f1`  
		Last Modified: Wed, 11 Jun 2025 01:34:33 GMT  
		Size: 3.2 KB (3241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d2b0f60cf9cb3716e55a68dd040f3a339bb863368ec1f8a949a6e88070180a`  
		Last Modified: Wed, 11 Jun 2025 04:42:37 GMT  
		Size: 41.5 MB (41450450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:e525174ea6d0518e410d4e66a0cfaad9f9c20a29fef2b8878088c6166d8e78a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7973001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fd4fc4cdd62d101df5323930cdbf9e7e6f2cc4ee6b584f200bf4ecc7b91d4d2`

```dockerfile
```

-	Layers:
	-	`sha256:715b7e027af961fe106c2fa5cd2b5621190698b0197e959d020215274c9a65fd`  
		Last Modified: Wed, 11 Jun 2025 04:33:19 GMT  
		Size: 8.0 MB (7959965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd1136216a709f0595980a32e4e0c070ea353db561ddb21a43a36b65f81c8a2f`  
		Last Modified: Wed, 11 Jun 2025 04:33:20 GMT  
		Size: 13.0 KB (13036 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:e29b54b3d047e02a16d862f486e05f3e25b9663773921a5880eab31626ab5cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175360191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ff3e8e1407c700846c9b24c543d9742d4a0d1f1e0ff1448ff6febbecd27107`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Apr 2025 03:13:04 GMT
MAINTAINER Rob Hoelz
# Thu, 24 Apr 2025 03:13:04 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 24 Apr 2025 03:13:04 GMT
ARG rakudo_version=2025.04-01
# Thu, 24 Apr 2025 03:13:04 GMT
ENV rakudo_version=2025.04-01
# Thu, 24 Apr 2025 03:13:04 GMT
# ARGS: rakudo_version=2025.04-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 24 Apr 2025 03:13:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 24 Apr 2025 03:13:04 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e137b9ec173f900a44376f31987bb15c0f5bb562aa6f8ad5db5a090ec88b2e`  
		Last Modified: Wed, 11 Jun 2025 02:56:23 GMT  
		Size: 23.6 MB (23551557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f5719d6358cc525f45e16c04ce36e5245978df9021dec8d0619729d9de8537`  
		Last Modified: Wed, 11 Jun 2025 10:32:40 GMT  
		Size: 64.4 MB (64362852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3ab978bb90e433bb72f30e43795229cf857c7fe5fea07a609567d094447f26`  
		Last Modified: Wed, 11 Jun 2025 16:49:58 GMT  
		Size: 3.2 KB (3239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1d5546fc81c2152986f6da7cde9916c0eb0d40e8f35866b331852f0b481b3c`  
		Last Modified: Wed, 11 Jun 2025 16:50:01 GMT  
		Size: 39.1 MB (39103691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:32a52fe72e100c85f3948a4a0df542d9a604216d189a6432b2a47cb3b07bf685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7979513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13d55ef5344a439f05d7a80c9999549cb3445d1193de013c563511b153a26df`

```dockerfile
```

-	Layers:
	-	`sha256:4f69a15b9932da8c3fb6409707a4b9f8937ef5f6ceb6ca705cb1b262bfd4dce2`  
		Last Modified: Wed, 11 Jun 2025 19:33:23 GMT  
		Size: 8.0 MB (7966370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b40af88763a2e0ec4816a9eabedcbbb136526825c5f949093c810abe5910cc3b`  
		Last Modified: Wed, 11 Jun 2025 19:33:24 GMT  
		Size: 13.1 KB (13143 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:4df675ca634dbb1afd689f8a89a72693551175f86d45c03212575e5128ba423e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:81558fd9ebdf5f42a0630d36dc7b67f290c23485c1f1d6aa7fc3e69fb0db59fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.4 MB (178363465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e916c40263620670e8c5ab1e24081682f6213b2c04c3ec45e856cf95842ec87a`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Apr 2025 03:13:04 GMT
MAINTAINER Rob Hoelz
# Thu, 24 Apr 2025 03:13:04 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 24 Apr 2025 03:13:04 GMT
ARG rakudo_version=2025.04-01
# Thu, 24 Apr 2025 03:13:04 GMT
ENV rakudo_version=2025.04-01
# Thu, 24 Apr 2025 03:13:04 GMT
# ARGS: rakudo_version=2025.04-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 24 Apr 2025 03:13:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 24 Apr 2025 03:13:04 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b8a0660a31403a35d70b276c3c86b1200b8683e83cd77a92ec98744017684a`  
		Last Modified: Wed, 11 Jun 2025 00:02:18 GMT  
		Size: 64.4 MB (64399794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068456311fedebd1b2656282dcb35f0e4623994f69d727546ca7611584aff9f1`  
		Last Modified: Wed, 11 Jun 2025 01:34:33 GMT  
		Size: 3.2 KB (3241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d2b0f60cf9cb3716e55a68dd040f3a339bb863368ec1f8a949a6e88070180a`  
		Last Modified: Wed, 11 Jun 2025 04:42:37 GMT  
		Size: 41.5 MB (41450450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:e525174ea6d0518e410d4e66a0cfaad9f9c20a29fef2b8878088c6166d8e78a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7973001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fd4fc4cdd62d101df5323930cdbf9e7e6f2cc4ee6b584f200bf4ecc7b91d4d2`

```dockerfile
```

-	Layers:
	-	`sha256:715b7e027af961fe106c2fa5cd2b5621190698b0197e959d020215274c9a65fd`  
		Last Modified: Wed, 11 Jun 2025 04:33:19 GMT  
		Size: 8.0 MB (7959965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd1136216a709f0595980a32e4e0c070ea353db561ddb21a43a36b65f81c8a2f`  
		Last Modified: Wed, 11 Jun 2025 04:33:20 GMT  
		Size: 13.0 KB (13036 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:e29b54b3d047e02a16d862f486e05f3e25b9663773921a5880eab31626ab5cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175360191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ff3e8e1407c700846c9b24c543d9742d4a0d1f1e0ff1448ff6febbecd27107`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Apr 2025 03:13:04 GMT
MAINTAINER Rob Hoelz
# Thu, 24 Apr 2025 03:13:04 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Thu, 24 Apr 2025 03:13:04 GMT
ARG rakudo_version=2025.04-01
# Thu, 24 Apr 2025 03:13:04 GMT
ENV rakudo_version=2025.04-01
# Thu, 24 Apr 2025 03:13:04 GMT
# ARGS: rakudo_version=2025.04-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 24 Apr 2025 03:13:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 24 Apr 2025 03:13:04 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e137b9ec173f900a44376f31987bb15c0f5bb562aa6f8ad5db5a090ec88b2e`  
		Last Modified: Wed, 11 Jun 2025 02:56:23 GMT  
		Size: 23.6 MB (23551557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f5719d6358cc525f45e16c04ce36e5245978df9021dec8d0619729d9de8537`  
		Last Modified: Wed, 11 Jun 2025 10:32:40 GMT  
		Size: 64.4 MB (64362852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3ab978bb90e433bb72f30e43795229cf857c7fe5fea07a609567d094447f26`  
		Last Modified: Wed, 11 Jun 2025 16:49:58 GMT  
		Size: 3.2 KB (3239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1d5546fc81c2152986f6da7cde9916c0eb0d40e8f35866b331852f0b481b3c`  
		Last Modified: Wed, 11 Jun 2025 16:50:01 GMT  
		Size: 39.1 MB (39103691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:32a52fe72e100c85f3948a4a0df542d9a604216d189a6432b2a47cb3b07bf685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7979513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13d55ef5344a439f05d7a80c9999549cb3445d1193de013c563511b153a26df`

```dockerfile
```

-	Layers:
	-	`sha256:4f69a15b9932da8c3fb6409707a4b9f8937ef5f6ceb6ca705cb1b262bfd4dce2`  
		Last Modified: Wed, 11 Jun 2025 19:33:23 GMT  
		Size: 8.0 MB (7966370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b40af88763a2e0ec4816a9eabedcbbb136526825c5f949093c810abe5910cc3b`  
		Last Modified: Wed, 11 Jun 2025 19:33:24 GMT  
		Size: 13.1 KB (13143 bytes)  
		MIME: application/vnd.in-toto+json
