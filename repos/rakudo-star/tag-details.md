<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rakudo-star`

-	[`rakudo-star:2026.03-alpine`](#rakudo-star202603-alpine)
-	[`rakudo-star:2026.03-bookworm`](#rakudo-star202603-bookworm)
-	[`rakudo-star:2026.03-trixie`](#rakudo-star202603-trixie)
-	[`rakudo-star:alpine`](#rakudo-staralpine)
-	[`rakudo-star:bookworm`](#rakudo-starbookworm)
-	[`rakudo-star:latest`](#rakudo-starlatest)
-	[`rakudo-star:trixie`](#rakudo-startrixie)

## `rakudo-star:2026.03-alpine`

```console
$ docker pull rakudo-star@sha256:71b0de1ce70879c6f12585086cc01bd01421a75b108389a805de96b37212ff33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2026.03-alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:7aa0628d0b1a583e1b90866106715e1ef223a6e0f32fb30deddc953505334412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52665660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86499ffcf77fdcf740a18cf389d0e2c0eb446e0665da8ae8132cf9a10ea5b65e`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:53:03 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Wed, 15 Apr 2026 21:10:32 GMT
ARG rakudo_version=2026.03-01
# Wed, 15 Apr 2026 21:10:32 GMT
ENV rakudo_version=2026.03-01
# Wed, 15 Apr 2026 21:10:32 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Wed, 15 Apr 2026 21:10:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 15 Apr 2026 21:10:32 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee98c68fca1fa970b30bcd494032418ea2d11bedab8f79d2a603699ed769ddb`  
		Last Modified: Wed, 15 Apr 2026 21:10:43 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a458dad0f26aa20a313acbacc31b6726e4227f1ec4db1c951f0e34b74e5a7d`  
		Last Modified: Wed, 15 Apr 2026 21:10:45 GMT  
		Size: 48.8 MB (48800525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.03-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:34b9f0c1780077e0a2ec20ca2e496886306e80f4ae9c18f493b38e09f24bcf05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 KB (198718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9305c952925e9a739edb860c7119906457b3d253274a7be2d8b9aea23db0bda3`

```dockerfile
```

-	Layers:
	-	`sha256:6529c149c158b9dd00064e5e412cab9d4e482d07bad94363401cb8f1e3c079ce`  
		Last Modified: Wed, 15 Apr 2026 21:10:43 GMT  
		Size: 187.0 KB (187001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:930779c51180105b4cf0717bb42f9a75cc1b5fa76f446d14d0587ad5be29cdf4`  
		Last Modified: Wed, 15 Apr 2026 21:10:43 GMT  
		Size: 11.7 KB (11717 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2026.03-alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:b246f0fa08554f866262d82434ed1d91be5a464858dee19c9e801893d4cb9bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52732464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc0e0fd9701fbc774f4db604c387dbb3d2c58ab6718e2199049dfdea78eef44`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:59:41 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Wed, 15 Apr 2026 21:20:04 GMT
ARG rakudo_version=2026.03-01
# Wed, 15 Apr 2026 21:20:04 GMT
ENV rakudo_version=2026.03-01
# Wed, 15 Apr 2026 21:20:04 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Wed, 15 Apr 2026 21:20:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 15 Apr 2026 21:20:04 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83697b754b185d3e5cd3643c95a6c53675b136cb600995bf966ae44eed43a7f0`  
		Last Modified: Wed, 15 Apr 2026 21:20:16 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3647707710c7794999ead460f620a06d0d30e1ef762485b28d2f6dafaee19eb`  
		Last Modified: Wed, 15 Apr 2026 21:20:17 GMT  
		Size: 48.5 MB (48531649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.03-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:105ff67cd14d36334ef6715ae7cb4e5eb8b11b3ac69b2354bde1bb0aab8b6dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 KB (198196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d88f1a6237aad331d492b369e2380a0f9a55e949e20ed6109e5ad5950af8053b`

```dockerfile
```

-	Layers:
	-	`sha256:f943a3d2d8231744298f6a5a6462438b4e3f385010d208a3eddfdaf0dafd31f9`  
		Last Modified: Wed, 15 Apr 2026 21:20:16 GMT  
		Size: 186.4 KB (186383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1afd60289ce1461274e4e5ff2fe64000a8bbe9b4717241e36ede85ed5bb7492`  
		Last Modified: Wed, 15 Apr 2026 21:20:16 GMT  
		Size: 11.8 KB (11813 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2026.03-bookworm`

```console
$ docker pull rakudo-star@sha256:06ef8ec097c6592b8080c2b13c11d3004a358d964760299c07151c19359f5df4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2026.03-bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:7de6be39bf186e6563c7df23b2a3e5f653f4a78d17d4336a1895ce31f6eb7ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.2 MB (179207237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7183cad597e1b270843dbb7dac99cd87c78d831529b942f938d3b274ade39f00`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:17:48 GMT
MAINTAINER Rob Hoelz
# Wed, 20 May 2026 01:17:48 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Wed, 20 May 2026 01:17:48 GMT
ARG rakudo_version=2026.03-01
# Wed, 20 May 2026 01:17:48 GMT
ENV rakudo_version=2026.03-01
# Wed, 20 May 2026 01:35:21 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 20 May 2026 01:35:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 20 May 2026 01:35:21 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a234579dfb0d2a4c7e869bc6c39c06f306aa019f90ec3e79f682671badaeb4f3`  
		Last Modified: Wed, 20 May 2026 00:26:20 GMT  
		Size: 64.4 MB (64404451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa9e1ed62d1a2b5c8a006b91e2cfec6c234d1bfb20a80fb6fadd8782ff34205`  
		Last Modified: Wed, 20 May 2026 01:35:35 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e66a22c6e2e18ef08a22ad402278980a00c2b82a46d8b4505fd45ea6e321d8b`  
		Last Modified: Wed, 20 May 2026 01:35:37 GMT  
		Size: 42.3 MB (42260740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.03-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:bdee54e2758e904e9dd9287f0a8dacdf40e5da1ae9b7ccd0562d70fb2c394b0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd56cfd53cd90d1f72f3b9d83f3b602e32de3df901d469636442ae41c613d280`

```dockerfile
```

-	Layers:
	-	`sha256:9cfa43c350e509b638aa4fc9fa6f9a7972f352946dfe35aff284da8f15f80115`  
		Last Modified: Wed, 20 May 2026 01:35:36 GMT  
		Size: 8.0 MB (7968469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6725920fbf99229bb0d0f639ddfe62c7a6490d22e24d569436d53f014f61469c`  
		Last Modified: Wed, 20 May 2026 01:35:36 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2026.03-bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:1abc370570a269136227dc51b3e28354421ec1ca918882db09db4a997584927a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176745246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdfaf60ff8c386577acf039c6c5c271618294a3b7c9fcd83788afd1321f5c578`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:18:31 GMT
MAINTAINER Rob Hoelz
# Wed, 20 May 2026 01:18:31 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Wed, 20 May 2026 01:18:31 GMT
ARG rakudo_version=2026.03-01
# Wed, 20 May 2026 01:18:31 GMT
ENV rakudo_version=2026.03-01
# Wed, 20 May 2026 01:40:11 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 20 May 2026 01:40:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 20 May 2026 01:40:11 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3daebbc198bd7b84bdd72840d7f4ded251896f03b9a9f880894e95e926bc543`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 23.6 MB (23613394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c669ec0346d48159cb837d6257098593cd53e61de677d9c0426474d36e1c5e`  
		Last Modified: Wed, 20 May 2026 00:27:16 GMT  
		Size: 64.5 MB (64487655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8d58c84cc7c70bdc8bae0194bf29f3d91c0ee0a3eb12a28d3b4a6b23b6ea85`  
		Last Modified: Wed, 20 May 2026 01:40:26 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635cf77ab180fe31092f29408e53e5a9332097ad1f5c1a9b14a2aeb6aa29195c`  
		Last Modified: Wed, 20 May 2026 01:40:28 GMT  
		Size: 40.3 MB (40261528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.03-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:c2c3f686ad7c93a0a2ef02ea3828b140a2a69a8a84308c4088cfce5a60cf9b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f842b4e1edc00468fb458b32fab00137e8a3dd4466fc3e9413b4343eb38e76f`

```dockerfile
```

-	Layers:
	-	`sha256:70dc6fba4295dcfcc71b458c1d854a3b1f86b371939b7d4945a9b59a5f7f37cc`  
		Last Modified: Wed, 20 May 2026 01:40:27 GMT  
		Size: 8.0 MB (7974862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e549d5f20adf24258b84d6de791af46d94b2202cd155d016049584c09d4fee50`  
		Last Modified: Wed, 20 May 2026 01:40:26 GMT  
		Size: 12.8 KB (12798 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2026.03-trixie`

```console
$ docker pull rakudo-star@sha256:d0ded55394c33c5c981eab3d316f9125553fee4a0f7e8744e82b7f2d5e78b399
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2026.03-trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:a5db8c5546a9bf772884c217d6f58ff2655dd7dddcce853bd0afc089024a0c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185001475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e235f8172f1db249661eb65b983ee7b804f0a605d3bf83884691bb61ec3dfdff`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:17:38 GMT
MAINTAINER AntonOks
# Wed, 20 May 2026 01:17:38 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Wed, 20 May 2026 01:17:38 GMT
ARG rakudo_version=2026.03-01
# Wed, 20 May 2026 01:17:38 GMT
ENV rakudo_version=2026.03-01
# Wed, 20 May 2026 01:34:12 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 20 May 2026 01:34:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 20 May 2026 01:34:12 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7504cd2818ce40ac76c17886a03dff25ef0aa06ff6125bf0f0c7302cdc6471`  
		Last Modified: Tue, 19 May 2026 23:23:34 GMT  
		Size: 25.6 MB (25633915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53089dca50590292ecc77bf803152a5799650e734717e4b706cb812a02073ba`  
		Last Modified: Wed, 20 May 2026 00:26:48 GMT  
		Size: 67.8 MB (67777732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80607773a759902698ec0cf0e10e9da74c8fec8600e897dd0d797640a8d43289`  
		Last Modified: Wed, 20 May 2026 01:34:27 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a545e4e9cef0f98ea91a02d9353066d60795f5c7148a00c456565202f9d39f1`  
		Last Modified: Wed, 20 May 2026 01:34:28 GMT  
		Size: 42.3 MB (42275965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.03-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:b8d9720544b8579958f2d506853810431859b3015ba612506e4fdd2c98bbbdad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be136192959832f739f7038ee624e566f1e5fc55145602eff71e677a0bad0e2f`

```dockerfile
```

-	Layers:
	-	`sha256:45681b8ec93bdda21c74edc2fcf9abaea31dd877f07579176d589bf86d203bd3`  
		Last Modified: Wed, 20 May 2026 01:34:27 GMT  
		Size: 7.8 MB (7770816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4742c2a063641ea363ab07e0d07d0471a7144c88f8de15d64633f7b638b8638e`  
		Last Modified: Wed, 20 May 2026 01:34:27 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2026.03-trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:ccd3cde3b3b0ab86674ce234601a09f0497ee19cd2db420af00a4822c39fa0b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182575813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4c935a370b4c3e919d83b00af34b9f1b21ebb20c32afc63c545279dc9655ce`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:27:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:27:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:17:57 GMT
MAINTAINER AntonOks
# Wed, 20 May 2026 01:17:57 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Wed, 20 May 2026 01:17:57 GMT
ARG rakudo_version=2026.03-01
# Wed, 20 May 2026 01:17:57 GMT
ENV rakudo_version=2026.03-01
# Wed, 20 May 2026 01:37:35 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 20 May 2026 01:37:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 20 May 2026 01:37:35 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28313c8eaf165ac06f26bda4877768677cf5e44e5c61ec169a81b436b2e985b`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 25.0 MB (25025606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39feea71264a587b284d92fded7754becc4682529629dd95c8bc3dd25a948a27`  
		Last Modified: Wed, 20 May 2026 00:27:52 GMT  
		Size: 67.6 MB (67592849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3069e913afb301820f3287b1aaeb6333296bfb8d622c88f851dcf6c38ed9480`  
		Last Modified: Wed, 20 May 2026 01:37:50 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0266231e82e884294c5a8205e13d1880ff188f73f6167cadd931cbd3e0523b`  
		Last Modified: Wed, 20 May 2026 01:37:52 GMT  
		Size: 40.3 MB (40281898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.03-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:6466072a9135ac916eac9efb849ed2427893887f31b3a5424447e7e421100e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3537f7f6df5ce7c38ecf4d28c44f1442099095cf51a65fa2dd6c7b3eab4c7d`

```dockerfile
```

-	Layers:
	-	`sha256:ac7e39d6c3ac29c1b181bd3b0de881a3901d99c74c9ddcd10c9fcb6b25f5ab65`  
		Last Modified: Wed, 20 May 2026 01:37:51 GMT  
		Size: 7.8 MB (7777854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcbb83e93fe5d19fb6c866ed79b54e169dbc586a17bdefaf9386062d5b5204a1`  
		Last Modified: Wed, 20 May 2026 01:37:50 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:71b0de1ce70879c6f12585086cc01bd01421a75b108389a805de96b37212ff33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:7aa0628d0b1a583e1b90866106715e1ef223a6e0f32fb30deddc953505334412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52665660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86499ffcf77fdcf740a18cf389d0e2c0eb446e0665da8ae8132cf9a10ea5b65e`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:53:03 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Wed, 15 Apr 2026 21:10:32 GMT
ARG rakudo_version=2026.03-01
# Wed, 15 Apr 2026 21:10:32 GMT
ENV rakudo_version=2026.03-01
# Wed, 15 Apr 2026 21:10:32 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Wed, 15 Apr 2026 21:10:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 15 Apr 2026 21:10:32 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee98c68fca1fa970b30bcd494032418ea2d11bedab8f79d2a603699ed769ddb`  
		Last Modified: Wed, 15 Apr 2026 21:10:43 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a458dad0f26aa20a313acbacc31b6726e4227f1ec4db1c951f0e34b74e5a7d`  
		Last Modified: Wed, 15 Apr 2026 21:10:45 GMT  
		Size: 48.8 MB (48800525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:34b9f0c1780077e0a2ec20ca2e496886306e80f4ae9c18f493b38e09f24bcf05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 KB (198718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9305c952925e9a739edb860c7119906457b3d253274a7be2d8b9aea23db0bda3`

```dockerfile
```

-	Layers:
	-	`sha256:6529c149c158b9dd00064e5e412cab9d4e482d07bad94363401cb8f1e3c079ce`  
		Last Modified: Wed, 15 Apr 2026 21:10:43 GMT  
		Size: 187.0 KB (187001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:930779c51180105b4cf0717bb42f9a75cc1b5fa76f446d14d0587ad5be29cdf4`  
		Last Modified: Wed, 15 Apr 2026 21:10:43 GMT  
		Size: 11.7 KB (11717 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:b246f0fa08554f866262d82434ed1d91be5a464858dee19c9e801893d4cb9bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52732464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc0e0fd9701fbc774f4db604c387dbb3d2c58ab6718e2199049dfdea78eef44`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:59:41 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Wed, 15 Apr 2026 21:20:04 GMT
ARG rakudo_version=2026.03-01
# Wed, 15 Apr 2026 21:20:04 GMT
ENV rakudo_version=2026.03-01
# Wed, 15 Apr 2026 21:20:04 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Wed, 15 Apr 2026 21:20:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 15 Apr 2026 21:20:04 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83697b754b185d3e5cd3643c95a6c53675b136cb600995bf966ae44eed43a7f0`  
		Last Modified: Wed, 15 Apr 2026 21:20:16 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3647707710c7794999ead460f620a06d0d30e1ef762485b28d2f6dafaee19eb`  
		Last Modified: Wed, 15 Apr 2026 21:20:17 GMT  
		Size: 48.5 MB (48531649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:105ff67cd14d36334ef6715ae7cb4e5eb8b11b3ac69b2354bde1bb0aab8b6dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 KB (198196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d88f1a6237aad331d492b369e2380a0f9a55e949e20ed6109e5ad5950af8053b`

```dockerfile
```

-	Layers:
	-	`sha256:f943a3d2d8231744298f6a5a6462438b4e3f385010d208a3eddfdaf0dafd31f9`  
		Last Modified: Wed, 15 Apr 2026 21:20:16 GMT  
		Size: 186.4 KB (186383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1afd60289ce1461274e4e5ff2fe64000a8bbe9b4717241e36ede85ed5bb7492`  
		Last Modified: Wed, 15 Apr 2026 21:20:16 GMT  
		Size: 11.8 KB (11813 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:bookworm`

```console
$ docker pull rakudo-star@sha256:06ef8ec097c6592b8080c2b13c11d3004a358d964760299c07151c19359f5df4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:7de6be39bf186e6563c7df23b2a3e5f653f4a78d17d4336a1895ce31f6eb7ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.2 MB (179207237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7183cad597e1b270843dbb7dac99cd87c78d831529b942f938d3b274ade39f00`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:17:48 GMT
MAINTAINER Rob Hoelz
# Wed, 20 May 2026 01:17:48 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Wed, 20 May 2026 01:17:48 GMT
ARG rakudo_version=2026.03-01
# Wed, 20 May 2026 01:17:48 GMT
ENV rakudo_version=2026.03-01
# Wed, 20 May 2026 01:35:21 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 20 May 2026 01:35:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 20 May 2026 01:35:21 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a234579dfb0d2a4c7e869bc6c39c06f306aa019f90ec3e79f682671badaeb4f3`  
		Last Modified: Wed, 20 May 2026 00:26:20 GMT  
		Size: 64.4 MB (64404451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa9e1ed62d1a2b5c8a006b91e2cfec6c234d1bfb20a80fb6fadd8782ff34205`  
		Last Modified: Wed, 20 May 2026 01:35:35 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e66a22c6e2e18ef08a22ad402278980a00c2b82a46d8b4505fd45ea6e321d8b`  
		Last Modified: Wed, 20 May 2026 01:35:37 GMT  
		Size: 42.3 MB (42260740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:bdee54e2758e904e9dd9287f0a8dacdf40e5da1ae9b7ccd0562d70fb2c394b0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd56cfd53cd90d1f72f3b9d83f3b602e32de3df901d469636442ae41c613d280`

```dockerfile
```

-	Layers:
	-	`sha256:9cfa43c350e509b638aa4fc9fa6f9a7972f352946dfe35aff284da8f15f80115`  
		Last Modified: Wed, 20 May 2026 01:35:36 GMT  
		Size: 8.0 MB (7968469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6725920fbf99229bb0d0f639ddfe62c7a6490d22e24d569436d53f014f61469c`  
		Last Modified: Wed, 20 May 2026 01:35:36 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:1abc370570a269136227dc51b3e28354421ec1ca918882db09db4a997584927a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176745246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdfaf60ff8c386577acf039c6c5c271618294a3b7c9fcd83788afd1321f5c578`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:18:31 GMT
MAINTAINER Rob Hoelz
# Wed, 20 May 2026 01:18:31 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Wed, 20 May 2026 01:18:31 GMT
ARG rakudo_version=2026.03-01
# Wed, 20 May 2026 01:18:31 GMT
ENV rakudo_version=2026.03-01
# Wed, 20 May 2026 01:40:11 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 20 May 2026 01:40:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 20 May 2026 01:40:11 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3daebbc198bd7b84bdd72840d7f4ded251896f03b9a9f880894e95e926bc543`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 23.6 MB (23613394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c669ec0346d48159cb837d6257098593cd53e61de677d9c0426474d36e1c5e`  
		Last Modified: Wed, 20 May 2026 00:27:16 GMT  
		Size: 64.5 MB (64487655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8d58c84cc7c70bdc8bae0194bf29f3d91c0ee0a3eb12a28d3b4a6b23b6ea85`  
		Last Modified: Wed, 20 May 2026 01:40:26 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635cf77ab180fe31092f29408e53e5a9332097ad1f5c1a9b14a2aeb6aa29195c`  
		Last Modified: Wed, 20 May 2026 01:40:28 GMT  
		Size: 40.3 MB (40261528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:c2c3f686ad7c93a0a2ef02ea3828b140a2a69a8a84308c4088cfce5a60cf9b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f842b4e1edc00468fb458b32fab00137e8a3dd4466fc3e9413b4343eb38e76f`

```dockerfile
```

-	Layers:
	-	`sha256:70dc6fba4295dcfcc71b458c1d854a3b1f86b371939b7d4945a9b59a5f7f37cc`  
		Last Modified: Wed, 20 May 2026 01:40:27 GMT  
		Size: 8.0 MB (7974862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e549d5f20adf24258b84d6de791af46d94b2202cd155d016049584c09d4fee50`  
		Last Modified: Wed, 20 May 2026 01:40:26 GMT  
		Size: 12.8 KB (12798 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:d0ded55394c33c5c981eab3d316f9125553fee4a0f7e8744e82b7f2d5e78b399
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:a5db8c5546a9bf772884c217d6f58ff2655dd7dddcce853bd0afc089024a0c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185001475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e235f8172f1db249661eb65b983ee7b804f0a605d3bf83884691bb61ec3dfdff`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:17:38 GMT
MAINTAINER AntonOks
# Wed, 20 May 2026 01:17:38 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Wed, 20 May 2026 01:17:38 GMT
ARG rakudo_version=2026.03-01
# Wed, 20 May 2026 01:17:38 GMT
ENV rakudo_version=2026.03-01
# Wed, 20 May 2026 01:34:12 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 20 May 2026 01:34:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 20 May 2026 01:34:12 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7504cd2818ce40ac76c17886a03dff25ef0aa06ff6125bf0f0c7302cdc6471`  
		Last Modified: Tue, 19 May 2026 23:23:34 GMT  
		Size: 25.6 MB (25633915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53089dca50590292ecc77bf803152a5799650e734717e4b706cb812a02073ba`  
		Last Modified: Wed, 20 May 2026 00:26:48 GMT  
		Size: 67.8 MB (67777732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80607773a759902698ec0cf0e10e9da74c8fec8600e897dd0d797640a8d43289`  
		Last Modified: Wed, 20 May 2026 01:34:27 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a545e4e9cef0f98ea91a02d9353066d60795f5c7148a00c456565202f9d39f1`  
		Last Modified: Wed, 20 May 2026 01:34:28 GMT  
		Size: 42.3 MB (42275965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:b8d9720544b8579958f2d506853810431859b3015ba612506e4fdd2c98bbbdad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be136192959832f739f7038ee624e566f1e5fc55145602eff71e677a0bad0e2f`

```dockerfile
```

-	Layers:
	-	`sha256:45681b8ec93bdda21c74edc2fcf9abaea31dd877f07579176d589bf86d203bd3`  
		Last Modified: Wed, 20 May 2026 01:34:27 GMT  
		Size: 7.8 MB (7770816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4742c2a063641ea363ab07e0d07d0471a7144c88f8de15d64633f7b638b8638e`  
		Last Modified: Wed, 20 May 2026 01:34:27 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:ccd3cde3b3b0ab86674ce234601a09f0497ee19cd2db420af00a4822c39fa0b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182575813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4c935a370b4c3e919d83b00af34b9f1b21ebb20c32afc63c545279dc9655ce`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:27:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:27:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:17:57 GMT
MAINTAINER AntonOks
# Wed, 20 May 2026 01:17:57 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Wed, 20 May 2026 01:17:57 GMT
ARG rakudo_version=2026.03-01
# Wed, 20 May 2026 01:17:57 GMT
ENV rakudo_version=2026.03-01
# Wed, 20 May 2026 01:37:35 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 20 May 2026 01:37:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 20 May 2026 01:37:35 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28313c8eaf165ac06f26bda4877768677cf5e44e5c61ec169a81b436b2e985b`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 25.0 MB (25025606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39feea71264a587b284d92fded7754becc4682529629dd95c8bc3dd25a948a27`  
		Last Modified: Wed, 20 May 2026 00:27:52 GMT  
		Size: 67.6 MB (67592849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3069e913afb301820f3287b1aaeb6333296bfb8d622c88f851dcf6c38ed9480`  
		Last Modified: Wed, 20 May 2026 01:37:50 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0266231e82e884294c5a8205e13d1880ff188f73f6167cadd931cbd3e0523b`  
		Last Modified: Wed, 20 May 2026 01:37:52 GMT  
		Size: 40.3 MB (40281898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:6466072a9135ac916eac9efb849ed2427893887f31b3a5424447e7e421100e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3537f7f6df5ce7c38ecf4d28c44f1442099095cf51a65fa2dd6c7b3eab4c7d`

```dockerfile
```

-	Layers:
	-	`sha256:ac7e39d6c3ac29c1b181bd3b0de881a3901d99c74c9ddcd10c9fcb6b25f5ab65`  
		Last Modified: Wed, 20 May 2026 01:37:51 GMT  
		Size: 7.8 MB (7777854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcbb83e93fe5d19fb6c866ed79b54e169dbc586a17bdefaf9386062d5b5204a1`  
		Last Modified: Wed, 20 May 2026 01:37:50 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:trixie`

```console
$ docker pull rakudo-star@sha256:d0ded55394c33c5c981eab3d316f9125553fee4a0f7e8744e82b7f2d5e78b399
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:a5db8c5546a9bf772884c217d6f58ff2655dd7dddcce853bd0afc089024a0c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185001475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e235f8172f1db249661eb65b983ee7b804f0a605d3bf83884691bb61ec3dfdff`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:17:38 GMT
MAINTAINER AntonOks
# Wed, 20 May 2026 01:17:38 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Wed, 20 May 2026 01:17:38 GMT
ARG rakudo_version=2026.03-01
# Wed, 20 May 2026 01:17:38 GMT
ENV rakudo_version=2026.03-01
# Wed, 20 May 2026 01:34:12 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 20 May 2026 01:34:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 20 May 2026 01:34:12 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7504cd2818ce40ac76c17886a03dff25ef0aa06ff6125bf0f0c7302cdc6471`  
		Last Modified: Tue, 19 May 2026 23:23:34 GMT  
		Size: 25.6 MB (25633915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53089dca50590292ecc77bf803152a5799650e734717e4b706cb812a02073ba`  
		Last Modified: Wed, 20 May 2026 00:26:48 GMT  
		Size: 67.8 MB (67777732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80607773a759902698ec0cf0e10e9da74c8fec8600e897dd0d797640a8d43289`  
		Last Modified: Wed, 20 May 2026 01:34:27 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a545e4e9cef0f98ea91a02d9353066d60795f5c7148a00c456565202f9d39f1`  
		Last Modified: Wed, 20 May 2026 01:34:28 GMT  
		Size: 42.3 MB (42275965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:b8d9720544b8579958f2d506853810431859b3015ba612506e4fdd2c98bbbdad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be136192959832f739f7038ee624e566f1e5fc55145602eff71e677a0bad0e2f`

```dockerfile
```

-	Layers:
	-	`sha256:45681b8ec93bdda21c74edc2fcf9abaea31dd877f07579176d589bf86d203bd3`  
		Last Modified: Wed, 20 May 2026 01:34:27 GMT  
		Size: 7.8 MB (7770816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4742c2a063641ea363ab07e0d07d0471a7144c88f8de15d64633f7b638b8638e`  
		Last Modified: Wed, 20 May 2026 01:34:27 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:ccd3cde3b3b0ab86674ce234601a09f0497ee19cd2db420af00a4822c39fa0b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182575813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4c935a370b4c3e919d83b00af34b9f1b21ebb20c32afc63c545279dc9655ce`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:27:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:27:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:17:57 GMT
MAINTAINER AntonOks
# Wed, 20 May 2026 01:17:57 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Wed, 20 May 2026 01:17:57 GMT
ARG rakudo_version=2026.03-01
# Wed, 20 May 2026 01:17:57 GMT
ENV rakudo_version=2026.03-01
# Wed, 20 May 2026 01:37:35 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 20 May 2026 01:37:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 20 May 2026 01:37:35 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28313c8eaf165ac06f26bda4877768677cf5e44e5c61ec169a81b436b2e985b`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 25.0 MB (25025606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39feea71264a587b284d92fded7754becc4682529629dd95c8bc3dd25a948a27`  
		Last Modified: Wed, 20 May 2026 00:27:52 GMT  
		Size: 67.6 MB (67592849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3069e913afb301820f3287b1aaeb6333296bfb8d622c88f851dcf6c38ed9480`  
		Last Modified: Wed, 20 May 2026 01:37:50 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0266231e82e884294c5a8205e13d1880ff188f73f6167cadd931cbd3e0523b`  
		Last Modified: Wed, 20 May 2026 01:37:52 GMT  
		Size: 40.3 MB (40281898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:6466072a9135ac916eac9efb849ed2427893887f31b3a5424447e7e421100e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3537f7f6df5ce7c38ecf4d28c44f1442099095cf51a65fa2dd6c7b3eab4c7d`

```dockerfile
```

-	Layers:
	-	`sha256:ac7e39d6c3ac29c1b181bd3b0de881a3901d99c74c9ddcd10c9fcb6b25f5ab65`  
		Last Modified: Wed, 20 May 2026 01:37:51 GMT  
		Size: 7.8 MB (7777854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcbb83e93fe5d19fb6c866ed79b54e169dbc586a17bdefaf9386062d5b5204a1`  
		Last Modified: Wed, 20 May 2026 01:37:50 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json
