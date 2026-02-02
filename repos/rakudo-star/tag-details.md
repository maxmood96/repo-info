<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rakudo-star`

-	[`rakudo-star:2026.01-alpine`](#rakudo-star202601-alpine)
-	[`rakudo-star:2026.01-bookworm`](#rakudo-star202601-bookworm)
-	[`rakudo-star:2026.01-trixie`](#rakudo-star202601-trixie)
-	[`rakudo-star:alpine`](#rakudo-staralpine)
-	[`rakudo-star:bookworm`](#rakudo-starbookworm)
-	[`rakudo-star:latest`](#rakudo-starlatest)
-	[`rakudo-star:trixie`](#rakudo-startrixie)

## `rakudo-star:2026.01-alpine`

```console
$ docker pull rakudo-star@sha256:78a228970ec5e9b42567b9d6da6629b1a49c3f6175f2e7a52b1afdbdaef0b31f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2026.01-alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:a5bff11023898fb0a4aea0041a2914ae3088ab11afd6965cb5fa4e8382531b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51337346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad9dfeb15cf9dd0010a9ddd7e4938e03a6c544adb4a84edc2b3ebf14219bbe3f`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:03:04 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Mon, 02 Feb 2026 19:19:20 GMT
ARG rakudo_version=2026.01-01
# Mon, 02 Feb 2026 19:19:20 GMT
ENV rakudo_version=2026.01-01
# Mon, 02 Feb 2026 19:19:20 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Mon, 02 Feb 2026 19:19:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 02 Feb 2026 19:19:20 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3060884c0be28f953f468c7201d683ba6c0e82dddfc2564c09b2d3b821b4e4fb`  
		Last Modified: Mon, 02 Feb 2026 19:19:31 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe45a1b0764dd266b786344adcb3b4c60c26489d59bdf104692f0849be7c390c`  
		Last Modified: Mon, 02 Feb 2026 19:19:36 GMT  
		Size: 47.5 MB (47474577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.01-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:4658d3cab6fd635f2f098ac62c80fcda5ce29fc291cf7e04be980103cf93a655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 KB (198691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5115d4e0288db5efbf0f47419b95453d7567d45a1c64368a45ad162f8ed98d33`

```dockerfile
```

-	Layers:
	-	`sha256:cbd4c48955e5af20ebde87c4430550e568b58e1e4da10059a9e7a37b8991b3b5`  
		Last Modified: Mon, 02 Feb 2026 19:19:31 GMT  
		Size: 187.0 KB (186973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bd9039c43e0e55fadf6c78efbca2ca8533cfb57e7ac6a2962c6cc8d85aeb6ee`  
		Last Modified: Mon, 02 Feb 2026 19:19:31 GMT  
		Size: 11.7 KB (11718 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2026.01-alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:e23968cc99cf3d7329dffb6df4a788bbff56e8660ba05b60140cb3dc85415aef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51410918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44523c43bffe91994ab0d41cac40b9586c81063423cf08a6095b4b47039f3df`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:03:53 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Mon, 02 Feb 2026 19:23:15 GMT
ARG rakudo_version=2026.01-01
# Mon, 02 Feb 2026 19:23:15 GMT
ENV rakudo_version=2026.01-01
# Mon, 02 Feb 2026 19:23:15 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Mon, 02 Feb 2026 19:23:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 02 Feb 2026 19:23:15 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637aa627dfc01bebed15028112f215606ab0f1cd1d25c2a41fdd2ab88fc60530`  
		Last Modified: Mon, 02 Feb 2026 19:23:27 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52008d4f177e3efc234c3aaabeaf66f73e9add81659a303f773a078438c24ee`  
		Last Modified: Mon, 02 Feb 2026 19:23:28 GMT  
		Size: 47.2 MB (47212880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.01-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:212cd58719d10575eec5bbc600a315b36c9171b8d70d6117876511f7caa74d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 KB (198168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588030a4c73d35971132596be85090e56b1d035c0f1fdc39cabcb3371f47e6ec`

```dockerfile
```

-	Layers:
	-	`sha256:f57e8b7aa80eafc12962eb9f7d1a3d01a9e49ce3dd50381059874a3017cd2e83`  
		Last Modified: Mon, 02 Feb 2026 19:23:27 GMT  
		Size: 186.4 KB (186355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ee180b9438495f5dd822ac0813970d7a53c6fc36cc9b2cf00d14ecfa17f2b9b`  
		Last Modified: Mon, 02 Feb 2026 19:23:27 GMT  
		Size: 11.8 KB (11813 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2026.01-bookworm`

```console
$ docker pull rakudo-star@sha256:a2edc259f9c14e5ed81276da46960acb5694c32c7369b64c552d4c2e081d9f4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2026.01-bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:9aa53c7ab51f45c64c31c9b42932c886d0cd5b9cf74f98d8b27daea84884a595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177809492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d015be3534e46fae29d8c77993337cd21a4d2ccba5a4869b64468f150793f1ce`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:53:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Feb 2026 19:02:51 GMT
MAINTAINER Rob Hoelz
# Mon, 02 Feb 2026 19:02:51 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 02 Feb 2026 19:02:51 GMT
ARG rakudo_version=2026.01-01
# Mon, 02 Feb 2026 19:02:51 GMT
ENV rakudo_version=2026.01-01
# Mon, 02 Feb 2026 19:15:55 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 02 Feb 2026 19:15:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 02 Feb 2026 19:15:55 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1872fa12cc6b1145803f1a0679ca26cc65fa1b4e0ee389bfb30267594736b6`  
		Last Modified: Tue, 13 Jan 2026 03:53:27 GMT  
		Size: 64.4 MB (64395833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb84c343193d87e30e6c44b8214db4fb8233999f647f28e9e501bc0a3b123533`  
		Last Modified: Mon, 02 Feb 2026 19:16:10 GMT  
		Size: 3.2 KB (3243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d05b3c70d33048ed2fbfa2b4ee89f6e300a3f8aeeb25801a928950492d3df0f`  
		Last Modified: Mon, 02 Feb 2026 19:16:12 GMT  
		Size: 40.9 MB (40891927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.01-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:0bfd5ca308a9a7453bb1f609d377a74109df04272580d502a1143551446c0d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d7e1d86570f972e2d0345aba7bca198dadcc8365ba01ea330d751d4c70a22f`

```dockerfile
```

-	Layers:
	-	`sha256:c643143c4971fa54aaecf85c2c78daec5e967c7e67664335423f3a2dbc6e8b52`  
		Last Modified: Mon, 02 Feb 2026 19:16:11 GMT  
		Size: 8.0 MB (7968447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e72c8492f948f827089c144856eb5644979cce4edf3a2f4222e8b71b7fd8978f`  
		Last Modified: Mon, 02 Feb 2026 19:16:10 GMT  
		Size: 12.7 KB (12702 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2026.01-bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:55829a31ccf62ae3c1558965f6c321f71fc050ad982c271b0f5daf05cf563f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175375730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023a7efaab8ae35b16ba5b7389dac50708a3810d8a6a43e58a73668b7f8b7428`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:56:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Feb 2026 19:03:40 GMT
MAINTAINER Rob Hoelz
# Mon, 02 Feb 2026 19:03:40 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 02 Feb 2026 19:03:40 GMT
ARG rakudo_version=2026.01-01
# Mon, 02 Feb 2026 19:03:40 GMT
ENV rakudo_version=2026.01-01
# Mon, 02 Feb 2026 19:22:17 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 02 Feb 2026 19:22:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 02 Feb 2026 19:22:17 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c713ab317dd7f302a6ff5a345af5b61cddc864fca2d96a23e6ef3c90a6657`  
		Last Modified: Tue, 13 Jan 2026 02:12:45 GMT  
		Size: 23.6 MB (23604814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687ad46596f06c934001fa6d7bea3d1508b0bb616cffb71004efd5bada56884f`  
		Last Modified: Tue, 13 Jan 2026 03:57:05 GMT  
		Size: 64.5 MB (64479462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4727da870f03e6f8c085d56b63f289deebc7820ce9cea1dfb4d546be2703fab6`  
		Last Modified: Mon, 02 Feb 2026 19:22:33 GMT  
		Size: 3.2 KB (3247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c551717c2744d9daa857d97323b12dcd0dcbce3074876c181a8ef8d1f1b382f`  
		Last Modified: Mon, 02 Feb 2026 19:22:35 GMT  
		Size: 38.9 MB (38922135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.01-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:75899282e154f4e29fff89eb6739bb76141d253caa2928386799ea50ca6d3c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffcbc5a83761f2509328687b471a77c25135ea3f6cfacc2e3b7f01419412c2e2`

```dockerfile
```

-	Layers:
	-	`sha256:dcfbac8ce74924630cd9121f893ba6380cec2097939e84df466335750917a90b`  
		Last Modified: Mon, 02 Feb 2026 19:22:34 GMT  
		Size: 8.0 MB (7974840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8403fe7b8662ef48e4d9b67d47e6670b90f784b13d4b4375eb01933edae5bb96`  
		Last Modified: Mon, 02 Feb 2026 19:22:33 GMT  
		Size: 12.8 KB (12798 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2026.01-trixie`

```console
$ docker pull rakudo-star@sha256:e953a3640baf3e0ce26dbadb6da2b650a4f969988774994c778b514d3b1a96d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2026.01-trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:132659830b6493199cc9a209b0e4fe1e9ecb4bdfb121b0ee6172364bcb40898c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183601809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0e6311d1231f93fa0f60c69c548f15624bfe2ca7b58f57000bd500655baffc`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 02 Feb 2026 19:00:52 GMT
MAINTAINER AntonOks
# Mon, 02 Feb 2026 19:00:52 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 02 Feb 2026 19:00:52 GMT
ARG rakudo_version=2026.01-01
# Mon, 02 Feb 2026 19:00:52 GMT
ENV rakudo_version=2026.01-01
# Mon, 02 Feb 2026 19:15:00 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 02 Feb 2026 19:15:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 02 Feb 2026 19:15:00 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e18c5e1c15ff34b31f1443e9327b69daaa0c1bd65a23846328fc3738c7f8f1`  
		Last Modified: Tue, 13 Jan 2026 02:11:12 GMT  
		Size: 25.6 MB (25613410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be442a7e0d6f290b909f8da51840566e06ab51bfbea277c70fbda26c44c8259d`  
		Last Modified: Tue, 13 Jan 2026 03:54:29 GMT  
		Size: 67.8 MB (67786776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d87016bf67ecdecfb422c85c03a6f73c04bcb842d684d495da329eb1e88d6fa`  
		Last Modified: Mon, 02 Feb 2026 19:15:15 GMT  
		Size: 3.2 KB (3245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad491ee8bff96edcb80b5bd2dce4f4895d1d0f7b5ce8e121804cf562f39fa7b`  
		Last Modified: Mon, 02 Feb 2026 19:15:17 GMT  
		Size: 40.9 MB (40912757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.01-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:1d24426d1e1f4557dd0545e160ef490d66593c6a13d5d8e6314ab10a897b5f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d944fa40bfb62d6c8b5285fd5c7f2a94b3ccfdf30570b3c138615a2d82b120`

```dockerfile
```

-	Layers:
	-	`sha256:6af3cb1d9cc850285218aba4281669a18f39181b925003ee6d7a78b28684075d`  
		Last Modified: Mon, 02 Feb 2026 19:15:16 GMT  
		Size: 7.8 MB (7770538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f3bfee5c0b9576cf0c0b8c25e33504e76aedd2aceca83e5c63e5432bdf1bff9`  
		Last Modified: Mon, 02 Feb 2026 19:15:15 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2026.01-trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:7766c73251b876521f70c6b86d1efb4b07c99d2ed8587e65ed1eeeb1ad926742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.2 MB (181208547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c196c35b902894b8bc1e017719d5de87ff5a12ba87c6e91f16c71d5ebf5c2c8`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:15:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:58:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 02 Feb 2026 18:58:42 GMT
MAINTAINER AntonOks
# Mon, 02 Feb 2026 18:58:42 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 02 Feb 2026 18:58:42 GMT
ARG rakudo_version=2026.01-01
# Mon, 02 Feb 2026 18:58:42 GMT
ENV rakudo_version=2026.01-01
# Mon, 02 Feb 2026 19:17:33 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 02 Feb 2026 19:17:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 02 Feb 2026 19:17:33 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:42 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d5b6b6766fd729045e2e7d0396d1f61fe41c612d4aef6bb3bf5ea7db12ae2`  
		Last Modified: Tue, 13 Jan 2026 02:15:36 GMT  
		Size: 25.0 MB (25022636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b629762372f548de0ebccf01b8e80ae5ce251dfd36aef6fc3ae8d963493edf`  
		Last Modified: Tue, 13 Jan 2026 03:58:39 GMT  
		Size: 67.6 MB (67591513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80142398193fae0091ca23e1f37c520447224fc6bf940182ff0cc0cd436e8cbf`  
		Last Modified: Mon, 02 Feb 2026 19:17:49 GMT  
		Size: 3.2 KB (3244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e08c3cd59a60595e114e92a47f18dadf534b8f422056a4db4ecbf775dde025`  
		Last Modified: Mon, 02 Feb 2026 19:17:50 GMT  
		Size: 38.9 MB (38943071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.01-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:22e7334693376af858b5a6c4e182b7bda8b643454ff42f3fb19577a9252b41c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7791312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8d0981284706891d7288aa283dd244c117366055c108a8b6df78cde120933b`

```dockerfile
```

-	Layers:
	-	`sha256:048ff38cb269d6c7de974e9141e625922132b7858dfe8c4f532de532ad3cf16f`  
		Last Modified: Mon, 02 Feb 2026 19:17:49 GMT  
		Size: 7.8 MB (7778213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c0ccfd2671467439f9620004c1e766db351188dad5be4ea3219da700871fe43`  
		Last Modified: Mon, 02 Feb 2026 19:17:49 GMT  
		Size: 13.1 KB (13099 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:78a228970ec5e9b42567b9d6da6629b1a49c3f6175f2e7a52b1afdbdaef0b31f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:a5bff11023898fb0a4aea0041a2914ae3088ab11afd6965cb5fa4e8382531b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51337346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad9dfeb15cf9dd0010a9ddd7e4938e03a6c544adb4a84edc2b3ebf14219bbe3f`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:03:04 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Mon, 02 Feb 2026 19:19:20 GMT
ARG rakudo_version=2026.01-01
# Mon, 02 Feb 2026 19:19:20 GMT
ENV rakudo_version=2026.01-01
# Mon, 02 Feb 2026 19:19:20 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Mon, 02 Feb 2026 19:19:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 02 Feb 2026 19:19:20 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3060884c0be28f953f468c7201d683ba6c0e82dddfc2564c09b2d3b821b4e4fb`  
		Last Modified: Mon, 02 Feb 2026 19:19:31 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe45a1b0764dd266b786344adcb3b4c60c26489d59bdf104692f0849be7c390c`  
		Last Modified: Mon, 02 Feb 2026 19:19:36 GMT  
		Size: 47.5 MB (47474577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:4658d3cab6fd635f2f098ac62c80fcda5ce29fc291cf7e04be980103cf93a655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 KB (198691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5115d4e0288db5efbf0f47419b95453d7567d45a1c64368a45ad162f8ed98d33`

```dockerfile
```

-	Layers:
	-	`sha256:cbd4c48955e5af20ebde87c4430550e568b58e1e4da10059a9e7a37b8991b3b5`  
		Last Modified: Mon, 02 Feb 2026 19:19:31 GMT  
		Size: 187.0 KB (186973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bd9039c43e0e55fadf6c78efbca2ca8533cfb57e7ac6a2962c6cc8d85aeb6ee`  
		Last Modified: Mon, 02 Feb 2026 19:19:31 GMT  
		Size: 11.7 KB (11718 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:e23968cc99cf3d7329dffb6df4a788bbff56e8660ba05b60140cb3dc85415aef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51410918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44523c43bffe91994ab0d41cac40b9586c81063423cf08a6095b4b47039f3df`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 02 Feb 2026 19:03:53 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Mon, 02 Feb 2026 19:23:15 GMT
ARG rakudo_version=2026.01-01
# Mon, 02 Feb 2026 19:23:15 GMT
ENV rakudo_version=2026.01-01
# Mon, 02 Feb 2026 19:23:15 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Mon, 02 Feb 2026 19:23:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 02 Feb 2026 19:23:15 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637aa627dfc01bebed15028112f215606ab0f1cd1d25c2a41fdd2ab88fc60530`  
		Last Modified: Mon, 02 Feb 2026 19:23:27 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52008d4f177e3efc234c3aaabeaf66f73e9add81659a303f773a078438c24ee`  
		Last Modified: Mon, 02 Feb 2026 19:23:28 GMT  
		Size: 47.2 MB (47212880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:212cd58719d10575eec5bbc600a315b36c9171b8d70d6117876511f7caa74d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 KB (198168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588030a4c73d35971132596be85090e56b1d035c0f1fdc39cabcb3371f47e6ec`

```dockerfile
```

-	Layers:
	-	`sha256:f57e8b7aa80eafc12962eb9f7d1a3d01a9e49ce3dd50381059874a3017cd2e83`  
		Last Modified: Mon, 02 Feb 2026 19:23:27 GMT  
		Size: 186.4 KB (186355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ee180b9438495f5dd822ac0813970d7a53c6fc36cc9b2cf00d14ecfa17f2b9b`  
		Last Modified: Mon, 02 Feb 2026 19:23:27 GMT  
		Size: 11.8 KB (11813 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:bookworm`

```console
$ docker pull rakudo-star@sha256:a2edc259f9c14e5ed81276da46960acb5694c32c7369b64c552d4c2e081d9f4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:9aa53c7ab51f45c64c31c9b42932c886d0cd5b9cf74f98d8b27daea84884a595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177809492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d015be3534e46fae29d8c77993337cd21a4d2ccba5a4869b64468f150793f1ce`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:53:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Feb 2026 19:02:51 GMT
MAINTAINER Rob Hoelz
# Mon, 02 Feb 2026 19:02:51 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 02 Feb 2026 19:02:51 GMT
ARG rakudo_version=2026.01-01
# Mon, 02 Feb 2026 19:02:51 GMT
ENV rakudo_version=2026.01-01
# Mon, 02 Feb 2026 19:15:55 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 02 Feb 2026 19:15:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 02 Feb 2026 19:15:55 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1872fa12cc6b1145803f1a0679ca26cc65fa1b4e0ee389bfb30267594736b6`  
		Last Modified: Tue, 13 Jan 2026 03:53:27 GMT  
		Size: 64.4 MB (64395833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb84c343193d87e30e6c44b8214db4fb8233999f647f28e9e501bc0a3b123533`  
		Last Modified: Mon, 02 Feb 2026 19:16:10 GMT  
		Size: 3.2 KB (3243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d05b3c70d33048ed2fbfa2b4ee89f6e300a3f8aeeb25801a928950492d3df0f`  
		Last Modified: Mon, 02 Feb 2026 19:16:12 GMT  
		Size: 40.9 MB (40891927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:0bfd5ca308a9a7453bb1f609d377a74109df04272580d502a1143551446c0d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d7e1d86570f972e2d0345aba7bca198dadcc8365ba01ea330d751d4c70a22f`

```dockerfile
```

-	Layers:
	-	`sha256:c643143c4971fa54aaecf85c2c78daec5e967c7e67664335423f3a2dbc6e8b52`  
		Last Modified: Mon, 02 Feb 2026 19:16:11 GMT  
		Size: 8.0 MB (7968447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e72c8492f948f827089c144856eb5644979cce4edf3a2f4222e8b71b7fd8978f`  
		Last Modified: Mon, 02 Feb 2026 19:16:10 GMT  
		Size: 12.7 KB (12702 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:55829a31ccf62ae3c1558965f6c321f71fc050ad982c271b0f5daf05cf563f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175375730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023a7efaab8ae35b16ba5b7389dac50708a3810d8a6a43e58a73668b7f8b7428`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:56:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Feb 2026 19:03:40 GMT
MAINTAINER Rob Hoelz
# Mon, 02 Feb 2026 19:03:40 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 02 Feb 2026 19:03:40 GMT
ARG rakudo_version=2026.01-01
# Mon, 02 Feb 2026 19:03:40 GMT
ENV rakudo_version=2026.01-01
# Mon, 02 Feb 2026 19:22:17 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 02 Feb 2026 19:22:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 02 Feb 2026 19:22:17 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c713ab317dd7f302a6ff5a345af5b61cddc864fca2d96a23e6ef3c90a6657`  
		Last Modified: Tue, 13 Jan 2026 02:12:45 GMT  
		Size: 23.6 MB (23604814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687ad46596f06c934001fa6d7bea3d1508b0bb616cffb71004efd5bada56884f`  
		Last Modified: Tue, 13 Jan 2026 03:57:05 GMT  
		Size: 64.5 MB (64479462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4727da870f03e6f8c085d56b63f289deebc7820ce9cea1dfb4d546be2703fab6`  
		Last Modified: Mon, 02 Feb 2026 19:22:33 GMT  
		Size: 3.2 KB (3247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c551717c2744d9daa857d97323b12dcd0dcbce3074876c181a8ef8d1f1b382f`  
		Last Modified: Mon, 02 Feb 2026 19:22:35 GMT  
		Size: 38.9 MB (38922135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:75899282e154f4e29fff89eb6739bb76141d253caa2928386799ea50ca6d3c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffcbc5a83761f2509328687b471a77c25135ea3f6cfacc2e3b7f01419412c2e2`

```dockerfile
```

-	Layers:
	-	`sha256:dcfbac8ce74924630cd9121f893ba6380cec2097939e84df466335750917a90b`  
		Last Modified: Mon, 02 Feb 2026 19:22:34 GMT  
		Size: 8.0 MB (7974840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8403fe7b8662ef48e4d9b67d47e6670b90f784b13d4b4375eb01933edae5bb96`  
		Last Modified: Mon, 02 Feb 2026 19:22:33 GMT  
		Size: 12.8 KB (12798 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:e953a3640baf3e0ce26dbadb6da2b650a4f969988774994c778b514d3b1a96d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:132659830b6493199cc9a209b0e4fe1e9ecb4bdfb121b0ee6172364bcb40898c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183601809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0e6311d1231f93fa0f60c69c548f15624bfe2ca7b58f57000bd500655baffc`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 02 Feb 2026 19:00:52 GMT
MAINTAINER AntonOks
# Mon, 02 Feb 2026 19:00:52 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 02 Feb 2026 19:00:52 GMT
ARG rakudo_version=2026.01-01
# Mon, 02 Feb 2026 19:00:52 GMT
ENV rakudo_version=2026.01-01
# Mon, 02 Feb 2026 19:15:00 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 02 Feb 2026 19:15:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 02 Feb 2026 19:15:00 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e18c5e1c15ff34b31f1443e9327b69daaa0c1bd65a23846328fc3738c7f8f1`  
		Last Modified: Tue, 13 Jan 2026 02:11:12 GMT  
		Size: 25.6 MB (25613410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be442a7e0d6f290b909f8da51840566e06ab51bfbea277c70fbda26c44c8259d`  
		Last Modified: Tue, 13 Jan 2026 03:54:29 GMT  
		Size: 67.8 MB (67786776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d87016bf67ecdecfb422c85c03a6f73c04bcb842d684d495da329eb1e88d6fa`  
		Last Modified: Mon, 02 Feb 2026 19:15:15 GMT  
		Size: 3.2 KB (3245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad491ee8bff96edcb80b5bd2dce4f4895d1d0f7b5ce8e121804cf562f39fa7b`  
		Last Modified: Mon, 02 Feb 2026 19:15:17 GMT  
		Size: 40.9 MB (40912757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:1d24426d1e1f4557dd0545e160ef490d66593c6a13d5d8e6314ab10a897b5f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d944fa40bfb62d6c8b5285fd5c7f2a94b3ccfdf30570b3c138615a2d82b120`

```dockerfile
```

-	Layers:
	-	`sha256:6af3cb1d9cc850285218aba4281669a18f39181b925003ee6d7a78b28684075d`  
		Last Modified: Mon, 02 Feb 2026 19:15:16 GMT  
		Size: 7.8 MB (7770538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f3bfee5c0b9576cf0c0b8c25e33504e76aedd2aceca83e5c63e5432bdf1bff9`  
		Last Modified: Mon, 02 Feb 2026 19:15:15 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:7766c73251b876521f70c6b86d1efb4b07c99d2ed8587e65ed1eeeb1ad926742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.2 MB (181208547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c196c35b902894b8bc1e017719d5de87ff5a12ba87c6e91f16c71d5ebf5c2c8`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:15:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:58:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 02 Feb 2026 18:58:42 GMT
MAINTAINER AntonOks
# Mon, 02 Feb 2026 18:58:42 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 02 Feb 2026 18:58:42 GMT
ARG rakudo_version=2026.01-01
# Mon, 02 Feb 2026 18:58:42 GMT
ENV rakudo_version=2026.01-01
# Mon, 02 Feb 2026 19:17:33 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 02 Feb 2026 19:17:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 02 Feb 2026 19:17:33 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:42 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d5b6b6766fd729045e2e7d0396d1f61fe41c612d4aef6bb3bf5ea7db12ae2`  
		Last Modified: Tue, 13 Jan 2026 02:15:36 GMT  
		Size: 25.0 MB (25022636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b629762372f548de0ebccf01b8e80ae5ce251dfd36aef6fc3ae8d963493edf`  
		Last Modified: Tue, 13 Jan 2026 03:58:39 GMT  
		Size: 67.6 MB (67591513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80142398193fae0091ca23e1f37c520447224fc6bf940182ff0cc0cd436e8cbf`  
		Last Modified: Mon, 02 Feb 2026 19:17:49 GMT  
		Size: 3.2 KB (3244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e08c3cd59a60595e114e92a47f18dadf534b8f422056a4db4ecbf775dde025`  
		Last Modified: Mon, 02 Feb 2026 19:17:50 GMT  
		Size: 38.9 MB (38943071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:22e7334693376af858b5a6c4e182b7bda8b643454ff42f3fb19577a9252b41c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7791312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8d0981284706891d7288aa283dd244c117366055c108a8b6df78cde120933b`

```dockerfile
```

-	Layers:
	-	`sha256:048ff38cb269d6c7de974e9141e625922132b7858dfe8c4f532de532ad3cf16f`  
		Last Modified: Mon, 02 Feb 2026 19:17:49 GMT  
		Size: 7.8 MB (7778213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c0ccfd2671467439f9620004c1e766db351188dad5be4ea3219da700871fe43`  
		Last Modified: Mon, 02 Feb 2026 19:17:49 GMT  
		Size: 13.1 KB (13099 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:trixie`

```console
$ docker pull rakudo-star@sha256:e953a3640baf3e0ce26dbadb6da2b650a4f969988774994c778b514d3b1a96d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:132659830b6493199cc9a209b0e4fe1e9ecb4bdfb121b0ee6172364bcb40898c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183601809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0e6311d1231f93fa0f60c69c548f15624bfe2ca7b58f57000bd500655baffc`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 02 Feb 2026 19:00:52 GMT
MAINTAINER AntonOks
# Mon, 02 Feb 2026 19:00:52 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 02 Feb 2026 19:00:52 GMT
ARG rakudo_version=2026.01-01
# Mon, 02 Feb 2026 19:00:52 GMT
ENV rakudo_version=2026.01-01
# Mon, 02 Feb 2026 19:15:00 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 02 Feb 2026 19:15:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 02 Feb 2026 19:15:00 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e18c5e1c15ff34b31f1443e9327b69daaa0c1bd65a23846328fc3738c7f8f1`  
		Last Modified: Tue, 13 Jan 2026 02:11:12 GMT  
		Size: 25.6 MB (25613410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be442a7e0d6f290b909f8da51840566e06ab51bfbea277c70fbda26c44c8259d`  
		Last Modified: Tue, 13 Jan 2026 03:54:29 GMT  
		Size: 67.8 MB (67786776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d87016bf67ecdecfb422c85c03a6f73c04bcb842d684d495da329eb1e88d6fa`  
		Last Modified: Mon, 02 Feb 2026 19:15:15 GMT  
		Size: 3.2 KB (3245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad491ee8bff96edcb80b5bd2dce4f4895d1d0f7b5ce8e121804cf562f39fa7b`  
		Last Modified: Mon, 02 Feb 2026 19:15:17 GMT  
		Size: 40.9 MB (40912757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:1d24426d1e1f4557dd0545e160ef490d66593c6a13d5d8e6314ab10a897b5f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d944fa40bfb62d6c8b5285fd5c7f2a94b3ccfdf30570b3c138615a2d82b120`

```dockerfile
```

-	Layers:
	-	`sha256:6af3cb1d9cc850285218aba4281669a18f39181b925003ee6d7a78b28684075d`  
		Last Modified: Mon, 02 Feb 2026 19:15:16 GMT  
		Size: 7.8 MB (7770538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f3bfee5c0b9576cf0c0b8c25e33504e76aedd2aceca83e5c63e5432bdf1bff9`  
		Last Modified: Mon, 02 Feb 2026 19:15:15 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:7766c73251b876521f70c6b86d1efb4b07c99d2ed8587e65ed1eeeb1ad926742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.2 MB (181208547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c196c35b902894b8bc1e017719d5de87ff5a12ba87c6e91f16c71d5ebf5c2c8`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:15:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:58:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 02 Feb 2026 18:58:42 GMT
MAINTAINER AntonOks
# Mon, 02 Feb 2026 18:58:42 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 02 Feb 2026 18:58:42 GMT
ARG rakudo_version=2026.01-01
# Mon, 02 Feb 2026 18:58:42 GMT
ENV rakudo_version=2026.01-01
# Mon, 02 Feb 2026 19:17:33 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 02 Feb 2026 19:17:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 02 Feb 2026 19:17:33 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:42 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d5b6b6766fd729045e2e7d0396d1f61fe41c612d4aef6bb3bf5ea7db12ae2`  
		Last Modified: Tue, 13 Jan 2026 02:15:36 GMT  
		Size: 25.0 MB (25022636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b629762372f548de0ebccf01b8e80ae5ce251dfd36aef6fc3ae8d963493edf`  
		Last Modified: Tue, 13 Jan 2026 03:58:39 GMT  
		Size: 67.6 MB (67591513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80142398193fae0091ca23e1f37c520447224fc6bf940182ff0cc0cd436e8cbf`  
		Last Modified: Mon, 02 Feb 2026 19:17:49 GMT  
		Size: 3.2 KB (3244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e08c3cd59a60595e114e92a47f18dadf534b8f422056a4db4ecbf775dde025`  
		Last Modified: Mon, 02 Feb 2026 19:17:50 GMT  
		Size: 38.9 MB (38943071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:22e7334693376af858b5a6c4e182b7bda8b643454ff42f3fb19577a9252b41c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7791312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8d0981284706891d7288aa283dd244c117366055c108a8b6df78cde120933b`

```dockerfile
```

-	Layers:
	-	`sha256:048ff38cb269d6c7de974e9141e625922132b7858dfe8c4f532de532ad3cf16f`  
		Last Modified: Mon, 02 Feb 2026 19:17:49 GMT  
		Size: 7.8 MB (7778213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c0ccfd2671467439f9620004c1e766db351188dad5be4ea3219da700871fe43`  
		Last Modified: Mon, 02 Feb 2026 19:17:49 GMT  
		Size: 13.1 KB (13099 bytes)  
		MIME: application/vnd.in-toto+json
