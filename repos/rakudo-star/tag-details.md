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
		Last Modified: Mon, 16 Jun 2025 03:47:18 GMT  
		Size: 124.2 KB (124221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96075b0510448a463b05851acb6c3cdb26047db661c6ab1e5df701ee4afbf857`  
		Last Modified: Mon, 16 Jun 2025 03:47:19 GMT  
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
$ docker pull rakudo-star@sha256:b21385a6f96a7684c093ea08bc5417ae7798a039a7fd9acf19c2c75deb821c6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2025.04` - linux; amd64

```console
$ docker pull rakudo-star@sha256:acf666c513f065de62925ebd7d7aee090c3cd9c4545b755c9f313882ae35df01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.4 MB (178382584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf90d23258646eafaed225eeeffe197683fe1516128c23ad55f7ec7e7e4a60b`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900e2c02f17f686733f4f957ddfb07b3342d1957d87b56254634d4fbb2abb81d`  
		Last Modified: Tue, 01 Jul 2025 04:11:56 GMT  
		Size: 64.4 MB (64399879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d4b7319b8a3b34d03a9ed723e7f518722746ccfeb2aafdad93406e9e335990`  
		Last Modified: Tue, 01 Jul 2025 04:31:11 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ba8478eda206f6db20407d032c0b357f1cc76ae47c622917ed35b12c3d8935`  
		Last Modified: Tue, 01 Jul 2025 04:31:26 GMT  
		Size: 41.5 MB (41464492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.04` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:fe8ed06d765a4d56d196e647a4f0594ce5d72d07057860c8fe05a357c702e215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7974357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a75ee6663fbb6bb7fb0939a160111af776b8b02d6076b7c08ae5e776439936a`

```dockerfile
```

-	Layers:
	-	`sha256:a6be1bdb709e5a70552abf8be2afb9d9432fc13fabb9b33136fadb19dc2e68ed`  
		Last Modified: Tue, 01 Jul 2025 07:33:18 GMT  
		Size: 8.0 MB (7961321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdb02959d3314eb5e832ac5423d322879eeb0e6fa24fbe6882f9ed1580119a0a`  
		Last Modified: Tue, 01 Jul 2025 07:33:19 GMT  
		Size: 13.0 KB (13036 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2025.04` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:89363d26909cdc9754fc0b0c5331ba244d4946b5eb2ec331dc0c68111b931ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.0 MB (175982630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b7f5278bef58d6a95ef1ceaef43041bb6e9de950eebb585b3dfa2c60b95465b`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be9cdb9167a8712f78cfe8da9fdf771134a84b1ee0fdab42bace39b895aaa9d`  
		Last Modified: Tue, 01 Jul 2025 06:52:02 GMT  
		Size: 23.6 MB (23558008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f9cdd730a2c32e544c8de28ddcb3800bc8b143e551c286d3ccb2704444d69f`  
		Last Modified: Tue, 01 Jul 2025 13:28:57 GMT  
		Size: 64.4 MB (64363294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810694a7c9b70571b989d087356548ddb0c0f4840974ae230cc33d2045f59c75`  
		Last Modified: Tue, 01 Jul 2025 18:07:59 GMT  
		Size: 3.2 KB (3238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae610f3522099a091d723c3d92da086df9bed8f7f297d18f6552cd9cd526e8dd`  
		Last Modified: Tue, 01 Jul 2025 18:07:59 GMT  
		Size: 39.7 MB (39719305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2025.04` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:e761ee342e7075cb67a15842296791d379d10b9481d345c62628bbbc3f138335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7980868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f6eb109efc21c9e65f34c071d678021a52cdaa5471a789f3b3c544ab85f06e`

```dockerfile
```

-	Layers:
	-	`sha256:c8df14fc19706182361890a9665d9b9088c90f105c1c14004cdb380bf8cc2d1d`  
		Last Modified: Tue, 01 Jul 2025 19:33:24 GMT  
		Size: 8.0 MB (7967726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d00f396a11c3d5c81415e57aab2164249d6c7b45560db909e85bfcab7ad4d69b`  
		Last Modified: Tue, 01 Jul 2025 19:33:25 GMT  
		Size: 13.1 KB (13142 bytes)  
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
		Last Modified: Mon, 16 Jun 2025 03:47:18 GMT  
		Size: 124.2 KB (124221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96075b0510448a463b05851acb6c3cdb26047db661c6ab1e5df701ee4afbf857`  
		Last Modified: Mon, 16 Jun 2025 03:47:19 GMT  
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
$ docker pull rakudo-star@sha256:b21385a6f96a7684c093ea08bc5417ae7798a039a7fd9acf19c2c75deb821c6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:acf666c513f065de62925ebd7d7aee090c3cd9c4545b755c9f313882ae35df01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.4 MB (178382584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf90d23258646eafaed225eeeffe197683fe1516128c23ad55f7ec7e7e4a60b`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900e2c02f17f686733f4f957ddfb07b3342d1957d87b56254634d4fbb2abb81d`  
		Last Modified: Tue, 01 Jul 2025 04:11:56 GMT  
		Size: 64.4 MB (64399879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d4b7319b8a3b34d03a9ed723e7f518722746ccfeb2aafdad93406e9e335990`  
		Last Modified: Tue, 01 Jul 2025 04:31:11 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ba8478eda206f6db20407d032c0b357f1cc76ae47c622917ed35b12c3d8935`  
		Last Modified: Tue, 01 Jul 2025 04:31:26 GMT  
		Size: 41.5 MB (41464492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:fe8ed06d765a4d56d196e647a4f0594ce5d72d07057860c8fe05a357c702e215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7974357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a75ee6663fbb6bb7fb0939a160111af776b8b02d6076b7c08ae5e776439936a`

```dockerfile
```

-	Layers:
	-	`sha256:a6be1bdb709e5a70552abf8be2afb9d9432fc13fabb9b33136fadb19dc2e68ed`  
		Last Modified: Tue, 01 Jul 2025 07:33:18 GMT  
		Size: 8.0 MB (7961321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdb02959d3314eb5e832ac5423d322879eeb0e6fa24fbe6882f9ed1580119a0a`  
		Last Modified: Tue, 01 Jul 2025 07:33:19 GMT  
		Size: 13.0 KB (13036 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:89363d26909cdc9754fc0b0c5331ba244d4946b5eb2ec331dc0c68111b931ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.0 MB (175982630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b7f5278bef58d6a95ef1ceaef43041bb6e9de950eebb585b3dfa2c60b95465b`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be9cdb9167a8712f78cfe8da9fdf771134a84b1ee0fdab42bace39b895aaa9d`  
		Last Modified: Tue, 01 Jul 2025 06:52:02 GMT  
		Size: 23.6 MB (23558008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f9cdd730a2c32e544c8de28ddcb3800bc8b143e551c286d3ccb2704444d69f`  
		Last Modified: Tue, 01 Jul 2025 13:28:57 GMT  
		Size: 64.4 MB (64363294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810694a7c9b70571b989d087356548ddb0c0f4840974ae230cc33d2045f59c75`  
		Last Modified: Tue, 01 Jul 2025 18:07:59 GMT  
		Size: 3.2 KB (3238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae610f3522099a091d723c3d92da086df9bed8f7f297d18f6552cd9cd526e8dd`  
		Last Modified: Tue, 01 Jul 2025 18:07:59 GMT  
		Size: 39.7 MB (39719305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:e761ee342e7075cb67a15842296791d379d10b9481d345c62628bbbc3f138335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7980868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f6eb109efc21c9e65f34c071d678021a52cdaa5471a789f3b3c544ab85f06e`

```dockerfile
```

-	Layers:
	-	`sha256:c8df14fc19706182361890a9665d9b9088c90f105c1c14004cdb380bf8cc2d1d`  
		Last Modified: Tue, 01 Jul 2025 19:33:24 GMT  
		Size: 8.0 MB (7967726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d00f396a11c3d5c81415e57aab2164249d6c7b45560db909e85bfcab7ad4d69b`  
		Last Modified: Tue, 01 Jul 2025 19:33:25 GMT  
		Size: 13.1 KB (13142 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:b21385a6f96a7684c093ea08bc5417ae7798a039a7fd9acf19c2c75deb821c6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:acf666c513f065de62925ebd7d7aee090c3cd9c4545b755c9f313882ae35df01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.4 MB (178382584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf90d23258646eafaed225eeeffe197683fe1516128c23ad55f7ec7e7e4a60b`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900e2c02f17f686733f4f957ddfb07b3342d1957d87b56254634d4fbb2abb81d`  
		Last Modified: Tue, 01 Jul 2025 04:11:56 GMT  
		Size: 64.4 MB (64399879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d4b7319b8a3b34d03a9ed723e7f518722746ccfeb2aafdad93406e9e335990`  
		Last Modified: Tue, 01 Jul 2025 04:31:11 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ba8478eda206f6db20407d032c0b357f1cc76ae47c622917ed35b12c3d8935`  
		Last Modified: Tue, 01 Jul 2025 04:31:26 GMT  
		Size: 41.5 MB (41464492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:fe8ed06d765a4d56d196e647a4f0594ce5d72d07057860c8fe05a357c702e215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7974357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a75ee6663fbb6bb7fb0939a160111af776b8b02d6076b7c08ae5e776439936a`

```dockerfile
```

-	Layers:
	-	`sha256:a6be1bdb709e5a70552abf8be2afb9d9432fc13fabb9b33136fadb19dc2e68ed`  
		Last Modified: Tue, 01 Jul 2025 07:33:18 GMT  
		Size: 8.0 MB (7961321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdb02959d3314eb5e832ac5423d322879eeb0e6fa24fbe6882f9ed1580119a0a`  
		Last Modified: Tue, 01 Jul 2025 07:33:19 GMT  
		Size: 13.0 KB (13036 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:89363d26909cdc9754fc0b0c5331ba244d4946b5eb2ec331dc0c68111b931ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.0 MB (175982630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b7f5278bef58d6a95ef1ceaef43041bb6e9de950eebb585b3dfa2c60b95465b`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be9cdb9167a8712f78cfe8da9fdf771134a84b1ee0fdab42bace39b895aaa9d`  
		Last Modified: Tue, 01 Jul 2025 06:52:02 GMT  
		Size: 23.6 MB (23558008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f9cdd730a2c32e544c8de28ddcb3800bc8b143e551c286d3ccb2704444d69f`  
		Last Modified: Tue, 01 Jul 2025 13:28:57 GMT  
		Size: 64.4 MB (64363294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810694a7c9b70571b989d087356548ddb0c0f4840974ae230cc33d2045f59c75`  
		Last Modified: Tue, 01 Jul 2025 18:07:59 GMT  
		Size: 3.2 KB (3238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae610f3522099a091d723c3d92da086df9bed8f7f297d18f6552cd9cd526e8dd`  
		Last Modified: Tue, 01 Jul 2025 18:07:59 GMT  
		Size: 39.7 MB (39719305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:e761ee342e7075cb67a15842296791d379d10b9481d345c62628bbbc3f138335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7980868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f6eb109efc21c9e65f34c071d678021a52cdaa5471a789f3b3c544ab85f06e`

```dockerfile
```

-	Layers:
	-	`sha256:c8df14fc19706182361890a9665d9b9088c90f105c1c14004cdb380bf8cc2d1d`  
		Last Modified: Tue, 01 Jul 2025 19:33:24 GMT  
		Size: 8.0 MB (7967726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d00f396a11c3d5c81415e57aab2164249d6c7b45560db909e85bfcab7ad4d69b`  
		Last Modified: Tue, 01 Jul 2025 19:33:25 GMT  
		Size: 13.1 KB (13142 bytes)  
		MIME: application/vnd.in-toto+json
