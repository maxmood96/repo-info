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
$ docker pull rakudo-star@sha256:e07888cf563040648f3276c9a1de410e77b013921c5df0c81ba5261943473e35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2026.01-bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:6c92a86b586e15724d82bb65d07b554101290c746d453ff619a991752ab8c686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177941012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe42dadb31807624141cf42211a738d87c5e954a2d3555cd27178570f20bd3f`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:03:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:42:06 GMT
MAINTAINER Rob Hoelz
# Tue, 24 Feb 2026 20:42:06 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 24 Feb 2026 20:42:06 GMT
ARG rakudo_version=2026.01-01
# Tue, 24 Feb 2026 20:42:06 GMT
ENV rakudo_version=2026.01-01
# Tue, 24 Feb 2026 20:55:14 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 20:55:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 24 Feb 2026 20:55:14 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa27031269f0a970255d56a9e793fc2a9d6bb091463cd5e632af4ae274881601`  
		Last Modified: Tue, 24 Feb 2026 20:03:49 GMT  
		Size: 64.4 MB (64395853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0cb6749902567cac6d03be626f17a6413f5e4a380972a5af57ef2f0084cd56`  
		Last Modified: Tue, 24 Feb 2026 20:55:27 GMT  
		Size: 3.2 KB (3238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611b5781bff0edfb56382588536700e10a2e0be0e4bb6352703c0a5a4120209a`  
		Last Modified: Tue, 24 Feb 2026 20:55:28 GMT  
		Size: 41.0 MB (41014694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.01-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:4d5dce5844e9fb9dd8cf25c9c0feb0d0a3863dc49ea30aa84286a09009ad17d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79df3b26b9465df992be43c7e6aac12f0d9c56fbca2dd8068448cbcf861ae64`

```dockerfile
```

-	Layers:
	-	`sha256:9fa361119b10e65b5b2a0d65e180d765f657b886fb3bc83ba150db41677bc193`  
		Last Modified: Tue, 24 Feb 2026 20:55:27 GMT  
		Size: 8.0 MB (7968447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:440f07b97eb32e236c20f29c7e29acb83eb032bbb3d60da95188a97e697f77a1`  
		Last Modified: Tue, 24 Feb 2026 20:55:27 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2026.01-bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:0a99a97a658cc5e0235a5ae99c886548b60ae6c1e5a0a2c4ff0f994c94cd0ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175504671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f7b1d948a8e5a45f57d6a3cfdf4f44788bab72e48d14dcce6781326ef937656`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:14:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:33:29 GMT
MAINTAINER Rob Hoelz
# Tue, 24 Feb 2026 21:33:29 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 24 Feb 2026 21:33:29 GMT
ARG rakudo_version=2026.01-01
# Tue, 24 Feb 2026 21:33:29 GMT
ENV rakudo_version=2026.01-01
# Tue, 24 Feb 2026 21:53:27 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 21:53:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 24 Feb 2026 21:53:27 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443d4217b87aad21c6acb58313c9038eb24571a4e9f81de2463aaf19d403a640`  
		Last Modified: Tue, 24 Feb 2026 19:24:13 GMT  
		Size: 23.6 MB (23604736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d27b842bb73f4af595ce58848c4c53ae713ca5c649636d25b483ca63bccc52`  
		Last Modified: Tue, 24 Feb 2026 20:14:46 GMT  
		Size: 64.5 MB (64479406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e88e002c8fe052dc7e362524df55a04dfef5b0e5625d1d9422ff6f37e857ff`  
		Last Modified: Tue, 24 Feb 2026 21:53:42 GMT  
		Size: 3.2 KB (3238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026eb2954984506fff995ed957bd0c2e7dd0f0499d18c9c829cc9873212b0366`  
		Last Modified: Tue, 24 Feb 2026 21:53:44 GMT  
		Size: 39.0 MB (39044081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.01-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:0996c594e85e035208453b7574ffcc304a85ad31ce45efbd9aa09992250ba444
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d19f0a3dc16af9a3fcff00be54699e9afd4eb8734dc9ff368c0fb9da5022c08`

```dockerfile
```

-	Layers:
	-	`sha256:b3f709b64cb707ca2f29dfe8a616b6274e447a59249c50f61d2ad3b0ccbbdc3b`  
		Last Modified: Tue, 24 Feb 2026 21:53:43 GMT  
		Size: 8.0 MB (7974840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f745f7daba9612e85227c91cfc8f7395094fc2081f6ede7f66cf6d00c6a70431`  
		Last Modified: Tue, 24 Feb 2026 21:53:42 GMT  
		Size: 12.8 KB (12797 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2026.01-trixie`

```console
$ docker pull rakudo-star@sha256:4fad5613619d935065b5e98acf6872ddcf921c514421489170211e17487eae9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2026.01-trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:e6a4a31f04a4a30ca26e525cb28f56ceb95ad350103ebc5f7316c2ede13a858c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183726082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb90e860d4128bcb9cc96754a5cac41376723f14af587e896cdfa9bc365ce142`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:04:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:41:31 GMT
MAINTAINER AntonOks
# Tue, 24 Feb 2026 20:41:31 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 24 Feb 2026 20:41:31 GMT
ARG rakudo_version=2026.01-01
# Tue, 24 Feb 2026 20:41:31 GMT
ENV rakudo_version=2026.01-01
# Tue, 24 Feb 2026 20:56:07 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 20:56:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 24 Feb 2026 20:56:07 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed881fbf1b07b42dd470cd5b56a8feb684d60879c6f8028a9e7a8715e0e72361`  
		Last Modified: Tue, 24 Feb 2026 19:20:17 GMT  
		Size: 25.6 MB (25614562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da421ddeb655bdfb3960e490b39373b0d1351e3eaba61d01978107920638392`  
		Last Modified: Tue, 24 Feb 2026 20:04:27 GMT  
		Size: 67.8 MB (67778971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a5dd9f1ea8eeda6f9bbd82467377582d49a9654af4f000c9452f6851504099`  
		Last Modified: Tue, 24 Feb 2026 20:56:21 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e72ac401f82f8ebc99b9237acc7131b59339b389a974030d14060fb949792c1`  
		Last Modified: Tue, 24 Feb 2026 20:56:22 GMT  
		Size: 41.0 MB (41036188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.01-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:3f6fdb060d4c3279fe2fb00f9bee8e0d8b35f590eb2d0322f085cbf42a3f9c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c7565c637d83d883d4bb069cc61ffebb979a8e4972b55109a648a5f9dce4547`

```dockerfile
```

-	Layers:
	-	`sha256:7b586f98a4197e1ff9985ff0e03eccc62abd4edd9bc804f5e6d6550351af7d03`  
		Last Modified: Tue, 24 Feb 2026 20:56:21 GMT  
		Size: 7.8 MB (7770538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecbcb2a4ea49e947417c5725eec704974988c54c550fef84fbc075ea561ee4cf`  
		Last Modified: Tue, 24 Feb 2026 20:56:21 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2026.01-trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:f494333ff3fb7184cdabd201443641a887715127d9e2ced89e33966600962b80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.3 MB (181326480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec7c7c672d5408e03382427e842bef696f19c2131d248f65564b0794a76421e`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:24:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:14:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 21:33:10 GMT
MAINTAINER AntonOks
# Tue, 24 Feb 2026 21:33:10 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 24 Feb 2026 21:33:10 GMT
ARG rakudo_version=2026.01-01
# Tue, 24 Feb 2026 21:33:10 GMT
ENV rakudo_version=2026.01-01
# Tue, 24 Feb 2026 21:51:40 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 21:51:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 24 Feb 2026 21:51:40 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95da832d1713c4ed161275cd40c4161680fbdd97c6faf23e71654d26bb2e58d6`  
		Last Modified: Tue, 24 Feb 2026 19:25:09 GMT  
		Size: 25.0 MB (25023493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c46eec5989abc098640d80ee9b97658d4487864f3268219dadc63c0a047866`  
		Last Modified: Tue, 24 Feb 2026 20:15:09 GMT  
		Size: 67.6 MB (67585551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d1ed4489cd9c9fa6ceafe2da92c08d884dd1f14669679f97a2489e8a94e640`  
		Last Modified: Tue, 24 Feb 2026 21:51:55 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695b3a266e3b8d592d861209abb74e8feb199943a86ae0d3c4a2d2ab3accf3ad`  
		Last Modified: Tue, 24 Feb 2026 21:51:56 GMT  
		Size: 39.1 MB (39062028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.01-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:f91f79b0317256dc72579c19319156ccccc18db64923451a147bcc459f3e8af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7791313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63547eb772f2cee140241f4029e61b630ae431b3dc0ee951b17a6b0db497c16`

```dockerfile
```

-	Layers:
	-	`sha256:84f660932f2c8c79a337000de11d5e923abb10813dbf2ad0a0d76ca684c31ab7`  
		Last Modified: Tue, 24 Feb 2026 21:51:56 GMT  
		Size: 7.8 MB (7778213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a08673963cb439ea169f0274c90b2d35dc7d0b6d028dd76007417eb1189c2906`  
		Last Modified: Tue, 24 Feb 2026 21:51:55 GMT  
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
$ docker pull rakudo-star@sha256:e07888cf563040648f3276c9a1de410e77b013921c5df0c81ba5261943473e35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:6c92a86b586e15724d82bb65d07b554101290c746d453ff619a991752ab8c686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177941012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe42dadb31807624141cf42211a738d87c5e954a2d3555cd27178570f20bd3f`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:03:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:42:06 GMT
MAINTAINER Rob Hoelz
# Tue, 24 Feb 2026 20:42:06 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 24 Feb 2026 20:42:06 GMT
ARG rakudo_version=2026.01-01
# Tue, 24 Feb 2026 20:42:06 GMT
ENV rakudo_version=2026.01-01
# Tue, 24 Feb 2026 20:55:14 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 20:55:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 24 Feb 2026 20:55:14 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa27031269f0a970255d56a9e793fc2a9d6bb091463cd5e632af4ae274881601`  
		Last Modified: Tue, 24 Feb 2026 20:03:49 GMT  
		Size: 64.4 MB (64395853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0cb6749902567cac6d03be626f17a6413f5e4a380972a5af57ef2f0084cd56`  
		Last Modified: Tue, 24 Feb 2026 20:55:27 GMT  
		Size: 3.2 KB (3238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611b5781bff0edfb56382588536700e10a2e0be0e4bb6352703c0a5a4120209a`  
		Last Modified: Tue, 24 Feb 2026 20:55:28 GMT  
		Size: 41.0 MB (41014694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:4d5dce5844e9fb9dd8cf25c9c0feb0d0a3863dc49ea30aa84286a09009ad17d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79df3b26b9465df992be43c7e6aac12f0d9c56fbca2dd8068448cbcf861ae64`

```dockerfile
```

-	Layers:
	-	`sha256:9fa361119b10e65b5b2a0d65e180d765f657b886fb3bc83ba150db41677bc193`  
		Last Modified: Tue, 24 Feb 2026 20:55:27 GMT  
		Size: 8.0 MB (7968447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:440f07b97eb32e236c20f29c7e29acb83eb032bbb3d60da95188a97e697f77a1`  
		Last Modified: Tue, 24 Feb 2026 20:55:27 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:0a99a97a658cc5e0235a5ae99c886548b60ae6c1e5a0a2c4ff0f994c94cd0ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175504671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f7b1d948a8e5a45f57d6a3cfdf4f44788bab72e48d14dcce6781326ef937656`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:14:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:33:29 GMT
MAINTAINER Rob Hoelz
# Tue, 24 Feb 2026 21:33:29 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 24 Feb 2026 21:33:29 GMT
ARG rakudo_version=2026.01-01
# Tue, 24 Feb 2026 21:33:29 GMT
ENV rakudo_version=2026.01-01
# Tue, 24 Feb 2026 21:53:27 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 21:53:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 24 Feb 2026 21:53:27 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443d4217b87aad21c6acb58313c9038eb24571a4e9f81de2463aaf19d403a640`  
		Last Modified: Tue, 24 Feb 2026 19:24:13 GMT  
		Size: 23.6 MB (23604736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d27b842bb73f4af595ce58848c4c53ae713ca5c649636d25b483ca63bccc52`  
		Last Modified: Tue, 24 Feb 2026 20:14:46 GMT  
		Size: 64.5 MB (64479406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e88e002c8fe052dc7e362524df55a04dfef5b0e5625d1d9422ff6f37e857ff`  
		Last Modified: Tue, 24 Feb 2026 21:53:42 GMT  
		Size: 3.2 KB (3238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026eb2954984506fff995ed957bd0c2e7dd0f0499d18c9c829cc9873212b0366`  
		Last Modified: Tue, 24 Feb 2026 21:53:44 GMT  
		Size: 39.0 MB (39044081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:0996c594e85e035208453b7574ffcc304a85ad31ce45efbd9aa09992250ba444
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d19f0a3dc16af9a3fcff00be54699e9afd4eb8734dc9ff368c0fb9da5022c08`

```dockerfile
```

-	Layers:
	-	`sha256:b3f709b64cb707ca2f29dfe8a616b6274e447a59249c50f61d2ad3b0ccbbdc3b`  
		Last Modified: Tue, 24 Feb 2026 21:53:43 GMT  
		Size: 8.0 MB (7974840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f745f7daba9612e85227c91cfc8f7395094fc2081f6ede7f66cf6d00c6a70431`  
		Last Modified: Tue, 24 Feb 2026 21:53:42 GMT  
		Size: 12.8 KB (12797 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:4fad5613619d935065b5e98acf6872ddcf921c514421489170211e17487eae9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:e6a4a31f04a4a30ca26e525cb28f56ceb95ad350103ebc5f7316c2ede13a858c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183726082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb90e860d4128bcb9cc96754a5cac41376723f14af587e896cdfa9bc365ce142`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:04:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:41:31 GMT
MAINTAINER AntonOks
# Tue, 24 Feb 2026 20:41:31 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 24 Feb 2026 20:41:31 GMT
ARG rakudo_version=2026.01-01
# Tue, 24 Feb 2026 20:41:31 GMT
ENV rakudo_version=2026.01-01
# Tue, 24 Feb 2026 20:56:07 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 20:56:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 24 Feb 2026 20:56:07 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed881fbf1b07b42dd470cd5b56a8feb684d60879c6f8028a9e7a8715e0e72361`  
		Last Modified: Tue, 24 Feb 2026 19:20:17 GMT  
		Size: 25.6 MB (25614562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da421ddeb655bdfb3960e490b39373b0d1351e3eaba61d01978107920638392`  
		Last Modified: Tue, 24 Feb 2026 20:04:27 GMT  
		Size: 67.8 MB (67778971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a5dd9f1ea8eeda6f9bbd82467377582d49a9654af4f000c9452f6851504099`  
		Last Modified: Tue, 24 Feb 2026 20:56:21 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e72ac401f82f8ebc99b9237acc7131b59339b389a974030d14060fb949792c1`  
		Last Modified: Tue, 24 Feb 2026 20:56:22 GMT  
		Size: 41.0 MB (41036188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:3f6fdb060d4c3279fe2fb00f9bee8e0d8b35f590eb2d0322f085cbf42a3f9c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c7565c637d83d883d4bb069cc61ffebb979a8e4972b55109a648a5f9dce4547`

```dockerfile
```

-	Layers:
	-	`sha256:7b586f98a4197e1ff9985ff0e03eccc62abd4edd9bc804f5e6d6550351af7d03`  
		Last Modified: Tue, 24 Feb 2026 20:56:21 GMT  
		Size: 7.8 MB (7770538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecbcb2a4ea49e947417c5725eec704974988c54c550fef84fbc075ea561ee4cf`  
		Last Modified: Tue, 24 Feb 2026 20:56:21 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:f494333ff3fb7184cdabd201443641a887715127d9e2ced89e33966600962b80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.3 MB (181326480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec7c7c672d5408e03382427e842bef696f19c2131d248f65564b0794a76421e`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:24:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:14:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 21:33:10 GMT
MAINTAINER AntonOks
# Tue, 24 Feb 2026 21:33:10 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 24 Feb 2026 21:33:10 GMT
ARG rakudo_version=2026.01-01
# Tue, 24 Feb 2026 21:33:10 GMT
ENV rakudo_version=2026.01-01
# Tue, 24 Feb 2026 21:51:40 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 21:51:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 24 Feb 2026 21:51:40 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95da832d1713c4ed161275cd40c4161680fbdd97c6faf23e71654d26bb2e58d6`  
		Last Modified: Tue, 24 Feb 2026 19:25:09 GMT  
		Size: 25.0 MB (25023493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c46eec5989abc098640d80ee9b97658d4487864f3268219dadc63c0a047866`  
		Last Modified: Tue, 24 Feb 2026 20:15:09 GMT  
		Size: 67.6 MB (67585551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d1ed4489cd9c9fa6ceafe2da92c08d884dd1f14669679f97a2489e8a94e640`  
		Last Modified: Tue, 24 Feb 2026 21:51:55 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695b3a266e3b8d592d861209abb74e8feb199943a86ae0d3c4a2d2ab3accf3ad`  
		Last Modified: Tue, 24 Feb 2026 21:51:56 GMT  
		Size: 39.1 MB (39062028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:f91f79b0317256dc72579c19319156ccccc18db64923451a147bcc459f3e8af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7791313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63547eb772f2cee140241f4029e61b630ae431b3dc0ee951b17a6b0db497c16`

```dockerfile
```

-	Layers:
	-	`sha256:84f660932f2c8c79a337000de11d5e923abb10813dbf2ad0a0d76ca684c31ab7`  
		Last Modified: Tue, 24 Feb 2026 21:51:56 GMT  
		Size: 7.8 MB (7778213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a08673963cb439ea169f0274c90b2d35dc7d0b6d028dd76007417eb1189c2906`  
		Last Modified: Tue, 24 Feb 2026 21:51:55 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:trixie`

```console
$ docker pull rakudo-star@sha256:4fad5613619d935065b5e98acf6872ddcf921c514421489170211e17487eae9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:e6a4a31f04a4a30ca26e525cb28f56ceb95ad350103ebc5f7316c2ede13a858c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183726082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb90e860d4128bcb9cc96754a5cac41376723f14af587e896cdfa9bc365ce142`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:04:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:41:31 GMT
MAINTAINER AntonOks
# Tue, 24 Feb 2026 20:41:31 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 24 Feb 2026 20:41:31 GMT
ARG rakudo_version=2026.01-01
# Tue, 24 Feb 2026 20:41:31 GMT
ENV rakudo_version=2026.01-01
# Tue, 24 Feb 2026 20:56:07 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 20:56:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 24 Feb 2026 20:56:07 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed881fbf1b07b42dd470cd5b56a8feb684d60879c6f8028a9e7a8715e0e72361`  
		Last Modified: Tue, 24 Feb 2026 19:20:17 GMT  
		Size: 25.6 MB (25614562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da421ddeb655bdfb3960e490b39373b0d1351e3eaba61d01978107920638392`  
		Last Modified: Tue, 24 Feb 2026 20:04:27 GMT  
		Size: 67.8 MB (67778971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a5dd9f1ea8eeda6f9bbd82467377582d49a9654af4f000c9452f6851504099`  
		Last Modified: Tue, 24 Feb 2026 20:56:21 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e72ac401f82f8ebc99b9237acc7131b59339b389a974030d14060fb949792c1`  
		Last Modified: Tue, 24 Feb 2026 20:56:22 GMT  
		Size: 41.0 MB (41036188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:3f6fdb060d4c3279fe2fb00f9bee8e0d8b35f590eb2d0322f085cbf42a3f9c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c7565c637d83d883d4bb069cc61ffebb979a8e4972b55109a648a5f9dce4547`

```dockerfile
```

-	Layers:
	-	`sha256:7b586f98a4197e1ff9985ff0e03eccc62abd4edd9bc804f5e6d6550351af7d03`  
		Last Modified: Tue, 24 Feb 2026 20:56:21 GMT  
		Size: 7.8 MB (7770538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecbcb2a4ea49e947417c5725eec704974988c54c550fef84fbc075ea561ee4cf`  
		Last Modified: Tue, 24 Feb 2026 20:56:21 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:f494333ff3fb7184cdabd201443641a887715127d9e2ced89e33966600962b80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.3 MB (181326480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec7c7c672d5408e03382427e842bef696f19c2131d248f65564b0794a76421e`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:24:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:14:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 21:33:10 GMT
MAINTAINER AntonOks
# Tue, 24 Feb 2026 21:33:10 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 24 Feb 2026 21:33:10 GMT
ARG rakudo_version=2026.01-01
# Tue, 24 Feb 2026 21:33:10 GMT
ENV rakudo_version=2026.01-01
# Tue, 24 Feb 2026 21:51:40 GMT
# ARGS: rakudo_version=2026.01-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 24 Feb 2026 21:51:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 24 Feb 2026 21:51:40 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95da832d1713c4ed161275cd40c4161680fbdd97c6faf23e71654d26bb2e58d6`  
		Last Modified: Tue, 24 Feb 2026 19:25:09 GMT  
		Size: 25.0 MB (25023493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c46eec5989abc098640d80ee9b97658d4487864f3268219dadc63c0a047866`  
		Last Modified: Tue, 24 Feb 2026 20:15:09 GMT  
		Size: 67.6 MB (67585551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d1ed4489cd9c9fa6ceafe2da92c08d884dd1f14669679f97a2489e8a94e640`  
		Last Modified: Tue, 24 Feb 2026 21:51:55 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695b3a266e3b8d592d861209abb74e8feb199943a86ae0d3c4a2d2ab3accf3ad`  
		Last Modified: Tue, 24 Feb 2026 21:51:56 GMT  
		Size: 39.1 MB (39062028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:f91f79b0317256dc72579c19319156ccccc18db64923451a147bcc459f3e8af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7791313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63547eb772f2cee140241f4029e61b630ae431b3dc0ee951b17a6b0db497c16`

```dockerfile
```

-	Layers:
	-	`sha256:84f660932f2c8c79a337000de11d5e923abb10813dbf2ad0a0d76ca684c31ab7`  
		Last Modified: Tue, 24 Feb 2026 21:51:56 GMT  
		Size: 7.8 MB (7778213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a08673963cb439ea169f0274c90b2d35dc7d0b6d028dd76007417eb1189c2906`  
		Last Modified: Tue, 24 Feb 2026 21:51:55 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json
