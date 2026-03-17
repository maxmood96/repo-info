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
$ docker pull rakudo-star@sha256:dcf981c4b3e5e3d8c1861fa90e3423e8fa68860d731563f6b8d43d6f9d689a5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2026.01-bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:119b6bb6988b2d8cd9f98998e827d31653703af405fd7ff928b686b4acf4f65b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.0 MB (177961578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9027d9d486fddff7c06a3963a89aba389a3f8308da6e6f29a5761b0dba076abf`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:24:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:22:49 GMT
MAINTAINER Rob Hoelz
# Tue, 17 Mar 2026 00:22:49 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 17 Mar 2026 00:22:49 GMT
ARG rakudo_version=2026.01-01
# Tue, 17 Mar 2026 00:22:49 GMT
ENV rakudo_version=2026.01-01
# Tue, 17 Mar 2026 00:37:23 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Mar 2026 00:37:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 17 Mar 2026 00:37:23 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3468d221545a43d2151f3977695a31857f9342ba842627d03c9fa1b2ae02`  
		Last Modified: Mon, 16 Mar 2026 22:37:09 GMT  
		Size: 24.0 MB (24038304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf051f1897bf7109af670b243c7791c62723fc1ebbfa516af2522da6c8c99a9`  
		Last Modified: Mon, 16 Mar 2026 23:25:05 GMT  
		Size: 64.4 MB (64395521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1717b53a0b77450b8db76ee2d3c9640a83c026931a62f60c150a98302f3f159`  
		Last Modified: Tue, 17 Mar 2026 00:37:37 GMT  
		Size: 3.2 KB (3239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a8d11db0b910d7ccaec5a8771a09d936e4f3654aa9a1625299fda5e4d1726b`  
		Last Modified: Tue, 17 Mar 2026 00:37:39 GMT  
		Size: 41.0 MB (41035930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.01-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:b0ccfb3abf4043d4fc29a955dfcbe3887081f1e84e19496922b6fa8c8896d1a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c6163f8834c9807816c33f392699ee95c5b7bcb460cfa4d326309acad343bb`

```dockerfile
```

-	Layers:
	-	`sha256:a11904c0db01abae8ea54224ef6c1c58335867a8f4b42105c654338638799b74`  
		Last Modified: Tue, 17 Mar 2026 00:37:38 GMT  
		Size: 8.0 MB (7968447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22a558a9b2ada05737dbe011586308b5ffcb48cb49df53b9f2d7d835010223d4`  
		Last Modified: Tue, 17 Mar 2026 00:37:37 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2026.01-bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:c96e603b97a19e873e8fdfaec56ff3d6203277965aa2d1d5c87f457e9fff7a53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175480397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e547ecc8837f91a909546759e92b8e06bc0148a711b03a1912238090aeed2e`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:30:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:22:39 GMT
MAINTAINER Rob Hoelz
# Tue, 17 Mar 2026 00:22:39 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 17 Mar 2026 00:22:39 GMT
ARG rakudo_version=2026.01-01
# Tue, 17 Mar 2026 00:22:39 GMT
ENV rakudo_version=2026.01-01
# Tue, 17 Mar 2026 00:41:25 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Mar 2026 00:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 17 Mar 2026 00:41:25 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbce225727d69d170353500d8834770da849cbdcea48de37e492fe14ef880d0`  
		Last Modified: Mon, 16 Mar 2026 22:39:28 GMT  
		Size: 23.6 MB (23604701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda59add442110ab916af1231a98d110e965b9b107829a3f0920d6789fa955d0`  
		Last Modified: Mon, 16 Mar 2026 23:30:22 GMT  
		Size: 64.5 MB (64479442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24339ca786a72babf92faa3c15e6497881fc0689c6bf17fab8b783ccaecbf451`  
		Last Modified: Tue, 17 Mar 2026 00:41:40 GMT  
		Size: 3.2 KB (3238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5d0bc6513ba62c20ce56bcd7f2df9cfe3c5fb4f8fcc2b10fa2de11f0a3ccbb`  
		Last Modified: Tue, 17 Mar 2026 00:41:41 GMT  
		Size: 39.0 MB (39019984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.01-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:2466c61ec897475181d791858d411ba8092ef119b539b91f6eb774e0a027ea5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb5a950358b1a67d0c927b515ada7448d0e1ef1396d209b73341e580f54ea501`

```dockerfile
```

-	Layers:
	-	`sha256:e247162bdfb1892e97b87a20490de9d8a1e6a0939d2e7907a6672bb69652e73a`  
		Last Modified: Tue, 17 Mar 2026 00:41:40 GMT  
		Size: 8.0 MB (7974840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a18f1de951f5ab150db90ba4d5b581a1735e3a800178ee6c8cfc4ac1974e2cf`  
		Last Modified: Tue, 17 Mar 2026 00:41:40 GMT  
		Size: 12.8 KB (12798 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2026.01-trixie`

```console
$ docker pull rakudo-star@sha256:e87a2188e14e6e31bdd385ec16fcb79c29d324c28e08f48700524a51cfd0ce25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2026.01-trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:242e293e27620ae1811a90000fe5f517a74340ed8f35910be70302f602c69f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183743461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd10bfbf304ceca76f376734018240301e37c4c223963a89ae7819711fb78d8`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:38:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:25:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 00:22:37 GMT
MAINTAINER AntonOks
# Tue, 17 Mar 2026 00:22:37 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 17 Mar 2026 00:22:37 GMT
ARG rakudo_version=2026.01-01
# Tue, 17 Mar 2026 00:22:37 GMT
ENV rakudo_version=2026.01-01
# Tue, 17 Mar 2026 00:37:55 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Mar 2026 00:37:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 17 Mar 2026 00:37:55 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b012eb15dff0bce418c03ec940325aee6aa4300d771c325728855697e620c63a`  
		Last Modified: Mon, 16 Mar 2026 22:38:25 GMT  
		Size: 25.6 MB (25621715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3a0e7d77f0c84203cab438fcf345647c8121bbd80506a3c692f8608a14c4f4`  
		Last Modified: Mon, 16 Mar 2026 23:25:57 GMT  
		Size: 67.8 MB (67780758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe173fd798975c233535c1d36f29566c80794faf9f14eedc56528e614ef58c1a`  
		Last Modified: Tue, 17 Mar 2026 00:38:09 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790207741ea5ac8705ec7a65d78c95cc9eab4986af23fbd283f86c4995819a40`  
		Last Modified: Tue, 17 Mar 2026 00:38:10 GMT  
		Size: 41.0 MB (41040221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.01-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:435ef7c0a62993e4a5a7181b736eed0eee89ef62dc312ff7b7a6ea5a94ba8fc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376e9ea7242ca849e93320e7f7811ae3fe2a62a9216a80292d6ef80b5ee2409e`

```dockerfile
```

-	Layers:
	-	`sha256:1fdf4497370e9acfa7d43291b4f49e75f40253fb393977acfe8537fd69edd086`  
		Last Modified: Tue, 17 Mar 2026 00:38:09 GMT  
		Size: 7.8 MB (7770612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:093ce78a4792ef76c8f885fac4e98f86b927fb8eed2eed83e72d3c431fa7c3b2`  
		Last Modified: Tue, 17 Mar 2026 00:38:09 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2026.01-trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:e5e11177ea401e22bbda100080e500af1e25ac4f162885df1ddec8d551255b49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181362554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d965267ccb4f41b42dd350ff83e87a1004e646dab0587f752d9a2a13232560ef`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:30:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 00:21:55 GMT
MAINTAINER AntonOks
# Tue, 17 Mar 2026 00:21:55 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 17 Mar 2026 00:21:55 GMT
ARG rakudo_version=2026.01-01
# Tue, 17 Mar 2026 00:21:55 GMT
ENV rakudo_version=2026.01-01
# Tue, 17 Mar 2026 00:42:11 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Mar 2026 00:42:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 17 Mar 2026 00:42:11 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6778b62bd97b31237948877e89abc29ad2b2c003f3b965027457c8c90d4f44e0`  
		Last Modified: Mon, 16 Mar 2026 22:40:45 GMT  
		Size: 25.0 MB (25023728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16813bdedcf0a1acbd78336c5bed6fbfaee2674574408140ba7e896cd49cb95`  
		Last Modified: Mon, 16 Mar 2026 23:31:00 GMT  
		Size: 67.6 MB (67584568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe50c8556efff3e8339683215e49c2b8bd823548744c2731d13bc31b6f1b5ff8`  
		Last Modified: Tue, 17 Mar 2026 00:42:26 GMT  
		Size: 3.2 KB (3238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0759562ba69647c92c9661698c14f541457f66ddb59825abd525f8c5c1531ff`  
		Last Modified: Tue, 17 Mar 2026 00:42:27 GMT  
		Size: 39.1 MB (39086067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.01-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:26bb425112ae86b19ce519c58dda368250db74e77b576b2114af3d98fa584474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7791387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8044903330ef97bb4b440b206fc8277c8818179d2d9afe7e37e28c11ca196c17`

```dockerfile
```

-	Layers:
	-	`sha256:f6ca11526cc9438cc23b976497f452e453ee7494598206c0c259477fe66a3aaa`  
		Last Modified: Tue, 17 Mar 2026 00:42:26 GMT  
		Size: 7.8 MB (7778287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:637053d51c1848fb19d128eba365be192dc29d5fb848e1856008d04acda78518`  
		Last Modified: Tue, 17 Mar 2026 00:42:26 GMT  
		Size: 13.1 KB (13100 bytes)  
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
$ docker pull rakudo-star@sha256:dcf981c4b3e5e3d8c1861fa90e3423e8fa68860d731563f6b8d43d6f9d689a5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:119b6bb6988b2d8cd9f98998e827d31653703af405fd7ff928b686b4acf4f65b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.0 MB (177961578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9027d9d486fddff7c06a3963a89aba389a3f8308da6e6f29a5761b0dba076abf`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:24:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:22:49 GMT
MAINTAINER Rob Hoelz
# Tue, 17 Mar 2026 00:22:49 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 17 Mar 2026 00:22:49 GMT
ARG rakudo_version=2026.01-01
# Tue, 17 Mar 2026 00:22:49 GMT
ENV rakudo_version=2026.01-01
# Tue, 17 Mar 2026 00:37:23 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Mar 2026 00:37:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 17 Mar 2026 00:37:23 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3468d221545a43d2151f3977695a31857f9342ba842627d03c9fa1b2ae02`  
		Last Modified: Mon, 16 Mar 2026 22:37:09 GMT  
		Size: 24.0 MB (24038304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf051f1897bf7109af670b243c7791c62723fc1ebbfa516af2522da6c8c99a9`  
		Last Modified: Mon, 16 Mar 2026 23:25:05 GMT  
		Size: 64.4 MB (64395521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1717b53a0b77450b8db76ee2d3c9640a83c026931a62f60c150a98302f3f159`  
		Last Modified: Tue, 17 Mar 2026 00:37:37 GMT  
		Size: 3.2 KB (3239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a8d11db0b910d7ccaec5a8771a09d936e4f3654aa9a1625299fda5e4d1726b`  
		Last Modified: Tue, 17 Mar 2026 00:37:39 GMT  
		Size: 41.0 MB (41035930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:b0ccfb3abf4043d4fc29a955dfcbe3887081f1e84e19496922b6fa8c8896d1a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c6163f8834c9807816c33f392699ee95c5b7bcb460cfa4d326309acad343bb`

```dockerfile
```

-	Layers:
	-	`sha256:a11904c0db01abae8ea54224ef6c1c58335867a8f4b42105c654338638799b74`  
		Last Modified: Tue, 17 Mar 2026 00:37:38 GMT  
		Size: 8.0 MB (7968447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22a558a9b2ada05737dbe011586308b5ffcb48cb49df53b9f2d7d835010223d4`  
		Last Modified: Tue, 17 Mar 2026 00:37:37 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:c96e603b97a19e873e8fdfaec56ff3d6203277965aa2d1d5c87f457e9fff7a53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175480397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e547ecc8837f91a909546759e92b8e06bc0148a711b03a1912238090aeed2e`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:30:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:22:39 GMT
MAINTAINER Rob Hoelz
# Tue, 17 Mar 2026 00:22:39 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 17 Mar 2026 00:22:39 GMT
ARG rakudo_version=2026.01-01
# Tue, 17 Mar 2026 00:22:39 GMT
ENV rakudo_version=2026.01-01
# Tue, 17 Mar 2026 00:41:25 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Mar 2026 00:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 17 Mar 2026 00:41:25 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbce225727d69d170353500d8834770da849cbdcea48de37e492fe14ef880d0`  
		Last Modified: Mon, 16 Mar 2026 22:39:28 GMT  
		Size: 23.6 MB (23604701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda59add442110ab916af1231a98d110e965b9b107829a3f0920d6789fa955d0`  
		Last Modified: Mon, 16 Mar 2026 23:30:22 GMT  
		Size: 64.5 MB (64479442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24339ca786a72babf92faa3c15e6497881fc0689c6bf17fab8b783ccaecbf451`  
		Last Modified: Tue, 17 Mar 2026 00:41:40 GMT  
		Size: 3.2 KB (3238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5d0bc6513ba62c20ce56bcd7f2df9cfe3c5fb4f8fcc2b10fa2de11f0a3ccbb`  
		Last Modified: Tue, 17 Mar 2026 00:41:41 GMT  
		Size: 39.0 MB (39019984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:2466c61ec897475181d791858d411ba8092ef119b539b91f6eb774e0a027ea5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb5a950358b1a67d0c927b515ada7448d0e1ef1396d209b73341e580f54ea501`

```dockerfile
```

-	Layers:
	-	`sha256:e247162bdfb1892e97b87a20490de9d8a1e6a0939d2e7907a6672bb69652e73a`  
		Last Modified: Tue, 17 Mar 2026 00:41:40 GMT  
		Size: 8.0 MB (7974840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a18f1de951f5ab150db90ba4d5b581a1735e3a800178ee6c8cfc4ac1974e2cf`  
		Last Modified: Tue, 17 Mar 2026 00:41:40 GMT  
		Size: 12.8 KB (12798 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:e87a2188e14e6e31bdd385ec16fcb79c29d324c28e08f48700524a51cfd0ce25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:242e293e27620ae1811a90000fe5f517a74340ed8f35910be70302f602c69f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183743461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd10bfbf304ceca76f376734018240301e37c4c223963a89ae7819711fb78d8`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:38:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:25:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 00:22:37 GMT
MAINTAINER AntonOks
# Tue, 17 Mar 2026 00:22:37 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 17 Mar 2026 00:22:37 GMT
ARG rakudo_version=2026.01-01
# Tue, 17 Mar 2026 00:22:37 GMT
ENV rakudo_version=2026.01-01
# Tue, 17 Mar 2026 00:37:55 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Mar 2026 00:37:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 17 Mar 2026 00:37:55 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b012eb15dff0bce418c03ec940325aee6aa4300d771c325728855697e620c63a`  
		Last Modified: Mon, 16 Mar 2026 22:38:25 GMT  
		Size: 25.6 MB (25621715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3a0e7d77f0c84203cab438fcf345647c8121bbd80506a3c692f8608a14c4f4`  
		Last Modified: Mon, 16 Mar 2026 23:25:57 GMT  
		Size: 67.8 MB (67780758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe173fd798975c233535c1d36f29566c80794faf9f14eedc56528e614ef58c1a`  
		Last Modified: Tue, 17 Mar 2026 00:38:09 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790207741ea5ac8705ec7a65d78c95cc9eab4986af23fbd283f86c4995819a40`  
		Last Modified: Tue, 17 Mar 2026 00:38:10 GMT  
		Size: 41.0 MB (41040221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:435ef7c0a62993e4a5a7181b736eed0eee89ef62dc312ff7b7a6ea5a94ba8fc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376e9ea7242ca849e93320e7f7811ae3fe2a62a9216a80292d6ef80b5ee2409e`

```dockerfile
```

-	Layers:
	-	`sha256:1fdf4497370e9acfa7d43291b4f49e75f40253fb393977acfe8537fd69edd086`  
		Last Modified: Tue, 17 Mar 2026 00:38:09 GMT  
		Size: 7.8 MB (7770612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:093ce78a4792ef76c8f885fac4e98f86b927fb8eed2eed83e72d3c431fa7c3b2`  
		Last Modified: Tue, 17 Mar 2026 00:38:09 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:e5e11177ea401e22bbda100080e500af1e25ac4f162885df1ddec8d551255b49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181362554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d965267ccb4f41b42dd350ff83e87a1004e646dab0587f752d9a2a13232560ef`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:30:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 00:21:55 GMT
MAINTAINER AntonOks
# Tue, 17 Mar 2026 00:21:55 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 17 Mar 2026 00:21:55 GMT
ARG rakudo_version=2026.01-01
# Tue, 17 Mar 2026 00:21:55 GMT
ENV rakudo_version=2026.01-01
# Tue, 17 Mar 2026 00:42:11 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Mar 2026 00:42:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 17 Mar 2026 00:42:11 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6778b62bd97b31237948877e89abc29ad2b2c003f3b965027457c8c90d4f44e0`  
		Last Modified: Mon, 16 Mar 2026 22:40:45 GMT  
		Size: 25.0 MB (25023728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16813bdedcf0a1acbd78336c5bed6fbfaee2674574408140ba7e896cd49cb95`  
		Last Modified: Mon, 16 Mar 2026 23:31:00 GMT  
		Size: 67.6 MB (67584568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe50c8556efff3e8339683215e49c2b8bd823548744c2731d13bc31b6f1b5ff8`  
		Last Modified: Tue, 17 Mar 2026 00:42:26 GMT  
		Size: 3.2 KB (3238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0759562ba69647c92c9661698c14f541457f66ddb59825abd525f8c5c1531ff`  
		Last Modified: Tue, 17 Mar 2026 00:42:27 GMT  
		Size: 39.1 MB (39086067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:26bb425112ae86b19ce519c58dda368250db74e77b576b2114af3d98fa584474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7791387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8044903330ef97bb4b440b206fc8277c8818179d2d9afe7e37e28c11ca196c17`

```dockerfile
```

-	Layers:
	-	`sha256:f6ca11526cc9438cc23b976497f452e453ee7494598206c0c259477fe66a3aaa`  
		Last Modified: Tue, 17 Mar 2026 00:42:26 GMT  
		Size: 7.8 MB (7778287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:637053d51c1848fb19d128eba365be192dc29d5fb848e1856008d04acda78518`  
		Last Modified: Tue, 17 Mar 2026 00:42:26 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:trixie`

```console
$ docker pull rakudo-star@sha256:e87a2188e14e6e31bdd385ec16fcb79c29d324c28e08f48700524a51cfd0ce25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:242e293e27620ae1811a90000fe5f517a74340ed8f35910be70302f602c69f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183743461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd10bfbf304ceca76f376734018240301e37c4c223963a89ae7819711fb78d8`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:38:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:25:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 00:22:37 GMT
MAINTAINER AntonOks
# Tue, 17 Mar 2026 00:22:37 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 17 Mar 2026 00:22:37 GMT
ARG rakudo_version=2026.01-01
# Tue, 17 Mar 2026 00:22:37 GMT
ENV rakudo_version=2026.01-01
# Tue, 17 Mar 2026 00:37:55 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Mar 2026 00:37:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 17 Mar 2026 00:37:55 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b012eb15dff0bce418c03ec940325aee6aa4300d771c325728855697e620c63a`  
		Last Modified: Mon, 16 Mar 2026 22:38:25 GMT  
		Size: 25.6 MB (25621715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3a0e7d77f0c84203cab438fcf345647c8121bbd80506a3c692f8608a14c4f4`  
		Last Modified: Mon, 16 Mar 2026 23:25:57 GMT  
		Size: 67.8 MB (67780758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe173fd798975c233535c1d36f29566c80794faf9f14eedc56528e614ef58c1a`  
		Last Modified: Tue, 17 Mar 2026 00:38:09 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790207741ea5ac8705ec7a65d78c95cc9eab4986af23fbd283f86c4995819a40`  
		Last Modified: Tue, 17 Mar 2026 00:38:10 GMT  
		Size: 41.0 MB (41040221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:435ef7c0a62993e4a5a7181b736eed0eee89ef62dc312ff7b7a6ea5a94ba8fc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376e9ea7242ca849e93320e7f7811ae3fe2a62a9216a80292d6ef80b5ee2409e`

```dockerfile
```

-	Layers:
	-	`sha256:1fdf4497370e9acfa7d43291b4f49e75f40253fb393977acfe8537fd69edd086`  
		Last Modified: Tue, 17 Mar 2026 00:38:09 GMT  
		Size: 7.8 MB (7770612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:093ce78a4792ef76c8f885fac4e98f86b927fb8eed2eed83e72d3c431fa7c3b2`  
		Last Modified: Tue, 17 Mar 2026 00:38:09 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:e5e11177ea401e22bbda100080e500af1e25ac4f162885df1ddec8d551255b49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181362554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d965267ccb4f41b42dd350ff83e87a1004e646dab0587f752d9a2a13232560ef`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:30:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 00:21:55 GMT
MAINTAINER AntonOks
# Tue, 17 Mar 2026 00:21:55 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 17 Mar 2026 00:21:55 GMT
ARG rakudo_version=2026.01-01
# Tue, 17 Mar 2026 00:21:55 GMT
ENV rakudo_version=2026.01-01
# Tue, 17 Mar 2026 00:42:11 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Mar 2026 00:42:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 17 Mar 2026 00:42:11 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6778b62bd97b31237948877e89abc29ad2b2c003f3b965027457c8c90d4f44e0`  
		Last Modified: Mon, 16 Mar 2026 22:40:45 GMT  
		Size: 25.0 MB (25023728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16813bdedcf0a1acbd78336c5bed6fbfaee2674574408140ba7e896cd49cb95`  
		Last Modified: Mon, 16 Mar 2026 23:31:00 GMT  
		Size: 67.6 MB (67584568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe50c8556efff3e8339683215e49c2b8bd823548744c2731d13bc31b6f1b5ff8`  
		Last Modified: Tue, 17 Mar 2026 00:42:26 GMT  
		Size: 3.2 KB (3238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0759562ba69647c92c9661698c14f541457f66ddb59825abd525f8c5c1531ff`  
		Last Modified: Tue, 17 Mar 2026 00:42:27 GMT  
		Size: 39.1 MB (39086067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:26bb425112ae86b19ce519c58dda368250db74e77b576b2114af3d98fa584474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7791387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8044903330ef97bb4b440b206fc8277c8818179d2d9afe7e37e28c11ca196c17`

```dockerfile
```

-	Layers:
	-	`sha256:f6ca11526cc9438cc23b976497f452e453ee7494598206c0c259477fe66a3aaa`  
		Last Modified: Tue, 17 Mar 2026 00:42:26 GMT  
		Size: 7.8 MB (7778287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:637053d51c1848fb19d128eba365be192dc29d5fb848e1856008d04acda78518`  
		Last Modified: Tue, 17 Mar 2026 00:42:26 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json
