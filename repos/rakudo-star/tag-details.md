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
$ docker pull rakudo-star@sha256:811bf42f560bf09a28500665556724e5f6cafdbd779295e939346d718b34c8c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2026.03-bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:50c806a10afa0a7d5ef153aad5c8eb1d1bb3c28fea7b630e65e52c1edf869bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.2 MB (179174934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60fe25ed908da98ea95700a9236bee422b35ea1afc098ee0d7c4b4b0cad0b6ac`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:19:52 GMT
MAINTAINER Rob Hoelz
# Fri, 08 May 2026 21:19:52 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Fri, 08 May 2026 21:19:52 GMT
ARG rakudo_version=2026.03-01
# Fri, 08 May 2026 21:19:52 GMT
ENV rakudo_version=2026.03-01
# Fri, 08 May 2026 21:36:08 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 21:36:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Fri, 08 May 2026 21:36:08 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0869e5c4dac5849d3555a38db741288a16528478145da8dcb95b8dba2464d55d`  
		Last Modified: Fri, 08 May 2026 20:26:25 GMT  
		Size: 64.4 MB (64397036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f954b518f588312517f28e20327abec13582880777509e3a82d6b0bc2f4d94`  
		Last Modified: Fri, 08 May 2026 21:36:22 GMT  
		Size: 3.2 KB (3244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915f308a59b3d70acbec66c84c3bca1b2b0cd345dceebe5ea5018cc9daf3cbb2`  
		Last Modified: Fri, 08 May 2026 21:36:24 GMT  
		Size: 42.2 MB (42243798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.03-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:e0fffc5c01c7a279d7d56446ec73bd4d891c1e3e65359014829b48f40ebe7a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a8ea5c07249ff83cb25b20fb419783a3c21b07f81b2492ebd8adcc0097b61d`

```dockerfile
```

-	Layers:
	-	`sha256:db12d36070da5315141ac60c902c7da121e18dda05bd8be7abb962196060d3f0`  
		Last Modified: Fri, 08 May 2026 21:36:23 GMT  
		Size: 8.0 MB (7968447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fbb171494a541a1221e5a85bfe47b5de90dea011ac7aa0da05ddb61fd59abc0`  
		Last Modified: Fri, 08 May 2026 21:36:22 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2026.03-bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:8126b1128cff1d8f9abfd34f968b113d65a50a84f8671f37af4a7d5cbfd2b881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176718072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8560ac6c4092839aad5173a1ccc5031877df19bb41841d55b6813f42f069a610`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:31:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:20:32 GMT
MAINTAINER Rob Hoelz
# Fri, 08 May 2026 21:20:32 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Fri, 08 May 2026 21:20:32 GMT
ARG rakudo_version=2026.03-01
# Fri, 08 May 2026 21:20:32 GMT
ENV rakudo_version=2026.03-01
# Fri, 08 May 2026 21:40:22 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 21:40:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Fri, 08 May 2026 21:40:22 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f56578c9577bd69a05b2319baacd770a986ae61a8568047ddd91db1a1893b4`  
		Last Modified: Fri, 08 May 2026 19:42:30 GMT  
		Size: 23.6 MB (23609357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd5c3bf1fab727b805a2f735f33789c10938680bdeb2f8922a44aa2738df91f`  
		Last Modified: Fri, 08 May 2026 20:32:11 GMT  
		Size: 64.5 MB (64479741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4b96e5b48c46c2cf2dc3cca656850c57ea041540d0b02915ab752c4a4869b4`  
		Last Modified: Fri, 08 May 2026 21:40:37 GMT  
		Size: 3.2 KB (3243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b078b725c68988ab7b550c2e796c0f8c258d168d612dd57d6f23c3c299eaa866`  
		Last Modified: Fri, 08 May 2026 21:40:39 GMT  
		Size: 40.3 MB (40252581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.03-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:18d0c25748ccab282fdeeaa68cfccb03d753e36accb61b32fe5c2ce9b5be8b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70eab49d26402bffe796fdc6a77bf3b8956a234801cafdc3a6a77523e2fd7d65`

```dockerfile
```

-	Layers:
	-	`sha256:a028daf4443ff62384fdcb0f47bea9b2e56b84bb401a8fc0e4b235460549f894`  
		Last Modified: Fri, 08 May 2026 21:40:38 GMT  
		Size: 8.0 MB (7974840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36fc0888faf084e8c38943b57273357ca085b8f272c97699c2e464528b11c9b7`  
		Last Modified: Fri, 08 May 2026 21:40:37 GMT  
		Size: 12.8 KB (12798 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2026.03-trixie`

```console
$ docker pull rakudo-star@sha256:8fa52e07957af55cd0dc7df314bdc24bf1dcb5a66045554ae7821c8684c01aae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2026.03-trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:becc95dff92662eab5470178f38f4e68c66ad33985c2867797af5f976c084e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (184976515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752c06859dabaaef9d2dd62ea7b20f2a21b61f0d61e59f97addfac3333617cd1`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:40:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:26:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:19:36 GMT
MAINTAINER AntonOks
# Fri, 08 May 2026 21:19:36 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Fri, 08 May 2026 21:19:36 GMT
ARG rakudo_version=2026.03-01
# Fri, 08 May 2026 21:19:36 GMT
ENV rakudo_version=2026.03-01
# Fri, 08 May 2026 21:35:27 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 21:35:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Fri, 08 May 2026 21:35:27 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf6c0a95e34418907d5abfe604d08c5cc6bf9d689943856fcd842eb2be82c6c`  
		Last Modified: Fri, 08 May 2026 19:40:57 GMT  
		Size: 25.6 MB (25623106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a92b93bf7181c9d6b4525236a1a2fec85dc591d4deee481e828e707853f42c`  
		Last Modified: Fri, 08 May 2026 20:27:02 GMT  
		Size: 67.8 MB (67789206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46240e81cf02e288be339f64f94dcf8bf7ddc00ea0b0624bc56db109113d2e6`  
		Last Modified: Fri, 08 May 2026 21:35:41 GMT  
		Size: 3.2 KB (3243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d69b8e298bfac72d48946b3adf1fd8c3ba2d9aaf42c301c0e18e9bdc4c6a256`  
		Last Modified: Fri, 08 May 2026 21:35:42 GMT  
		Size: 42.3 MB (42258640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.03-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:5bd74c7bb6d99ee3e42787c4624b0a90afe8e158249d4840cf2a9a956a87e3d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:451fdc2f83a32e2f764bfaf3305a84f55103c914e5d59960fafa2431a4d8b430`

```dockerfile
```

-	Layers:
	-	`sha256:56cd30df74aabaf94c2aa85e77474cf89457156fe9bfc6f8f2fba50a58e015e9`  
		Last Modified: Fri, 08 May 2026 21:35:41 GMT  
		Size: 7.8 MB (7770666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a30ef50d81c9784fb53290e22ce97f39df612fec9a1c00e38b6289d842d9587a`  
		Last Modified: Fri, 08 May 2026 21:35:41 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2026.03-trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:dee7fb4ecab2e1d9334fe442680c58607dc92ea0b0a54a1386fcf66cd98b86a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182557585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3def38ef5c552e78674daa05109c10bc7b4b9f77b6fe6a7732c3010cd65c9c7`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:42:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:19:38 GMT
MAINTAINER AntonOks
# Fri, 08 May 2026 21:19:38 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Fri, 08 May 2026 21:19:38 GMT
ARG rakudo_version=2026.03-01
# Fri, 08 May 2026 21:19:38 GMT
ENV rakudo_version=2026.03-01
# Fri, 08 May 2026 21:39:53 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 21:39:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Fri, 08 May 2026 21:39:53 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6968d8edb06bcdaf22846e8626a2500d70d68bae3413bca896fefe955e2a6ef0`  
		Last Modified: Fri, 08 May 2026 19:42:46 GMT  
		Size: 25.0 MB (25023476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc880ef5fbb726989fb57630c05c39cfe57a36a9f03c5b86a2d51c9c86ed66f2`  
		Last Modified: Fri, 08 May 2026 20:32:42 GMT  
		Size: 67.6 MB (67592055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d944f36e8d4737c299105fd017ba91ba09672d464f7eef4eb9cba7ba964b84a5`  
		Last Modified: Fri, 08 May 2026 21:40:08 GMT  
		Size: 3.2 KB (3243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6eeede9eacb1facb6d0661f8c30fba4020b7f3418c486bd58018b93f84c009`  
		Last Modified: Fri, 08 May 2026 21:40:10 GMT  
		Size: 40.3 MB (40269366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.03-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:32ccb461388015d98105e4686b54f68f3f43dd239085cf48fdbbf5f3c98cdd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7791441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c058b821f308233406eb7a0f952f31df392d7c5d0afcbd300853d1269c64ac9b`

```dockerfile
```

-	Layers:
	-	`sha256:c64fb2df571d20d6f12cfdf8883932c5bd26aedafab5008a5b3ff5a1ec8f521f`  
		Last Modified: Fri, 08 May 2026 21:40:09 GMT  
		Size: 7.8 MB (7778341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0de358beba4bf91db65e0d7dcb26181b827fe6146187d6fae4bedb81eb141b70`  
		Last Modified: Fri, 08 May 2026 21:40:08 GMT  
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
$ docker pull rakudo-star@sha256:811bf42f560bf09a28500665556724e5f6cafdbd779295e939346d718b34c8c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:50c806a10afa0a7d5ef153aad5c8eb1d1bb3c28fea7b630e65e52c1edf869bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.2 MB (179174934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60fe25ed908da98ea95700a9236bee422b35ea1afc098ee0d7c4b4b0cad0b6ac`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:19:52 GMT
MAINTAINER Rob Hoelz
# Fri, 08 May 2026 21:19:52 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Fri, 08 May 2026 21:19:52 GMT
ARG rakudo_version=2026.03-01
# Fri, 08 May 2026 21:19:52 GMT
ENV rakudo_version=2026.03-01
# Fri, 08 May 2026 21:36:08 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 21:36:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Fri, 08 May 2026 21:36:08 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0869e5c4dac5849d3555a38db741288a16528478145da8dcb95b8dba2464d55d`  
		Last Modified: Fri, 08 May 2026 20:26:25 GMT  
		Size: 64.4 MB (64397036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f954b518f588312517f28e20327abec13582880777509e3a82d6b0bc2f4d94`  
		Last Modified: Fri, 08 May 2026 21:36:22 GMT  
		Size: 3.2 KB (3244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915f308a59b3d70acbec66c84c3bca1b2b0cd345dceebe5ea5018cc9daf3cbb2`  
		Last Modified: Fri, 08 May 2026 21:36:24 GMT  
		Size: 42.2 MB (42243798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:e0fffc5c01c7a279d7d56446ec73bd4d891c1e3e65359014829b48f40ebe7a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a8ea5c07249ff83cb25b20fb419783a3c21b07f81b2492ebd8adcc0097b61d`

```dockerfile
```

-	Layers:
	-	`sha256:db12d36070da5315141ac60c902c7da121e18dda05bd8be7abb962196060d3f0`  
		Last Modified: Fri, 08 May 2026 21:36:23 GMT  
		Size: 8.0 MB (7968447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fbb171494a541a1221e5a85bfe47b5de90dea011ac7aa0da05ddb61fd59abc0`  
		Last Modified: Fri, 08 May 2026 21:36:22 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:8126b1128cff1d8f9abfd34f968b113d65a50a84f8671f37af4a7d5cbfd2b881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176718072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8560ac6c4092839aad5173a1ccc5031877df19bb41841d55b6813f42f069a610`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:31:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:20:32 GMT
MAINTAINER Rob Hoelz
# Fri, 08 May 2026 21:20:32 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Fri, 08 May 2026 21:20:32 GMT
ARG rakudo_version=2026.03-01
# Fri, 08 May 2026 21:20:32 GMT
ENV rakudo_version=2026.03-01
# Fri, 08 May 2026 21:40:22 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 21:40:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Fri, 08 May 2026 21:40:22 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f56578c9577bd69a05b2319baacd770a986ae61a8568047ddd91db1a1893b4`  
		Last Modified: Fri, 08 May 2026 19:42:30 GMT  
		Size: 23.6 MB (23609357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd5c3bf1fab727b805a2f735f33789c10938680bdeb2f8922a44aa2738df91f`  
		Last Modified: Fri, 08 May 2026 20:32:11 GMT  
		Size: 64.5 MB (64479741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4b96e5b48c46c2cf2dc3cca656850c57ea041540d0b02915ab752c4a4869b4`  
		Last Modified: Fri, 08 May 2026 21:40:37 GMT  
		Size: 3.2 KB (3243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b078b725c68988ab7b550c2e796c0f8c258d168d612dd57d6f23c3c299eaa866`  
		Last Modified: Fri, 08 May 2026 21:40:39 GMT  
		Size: 40.3 MB (40252581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:18d0c25748ccab282fdeeaa68cfccb03d753e36accb61b32fe5c2ce9b5be8b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70eab49d26402bffe796fdc6a77bf3b8956a234801cafdc3a6a77523e2fd7d65`

```dockerfile
```

-	Layers:
	-	`sha256:a028daf4443ff62384fdcb0f47bea9b2e56b84bb401a8fc0e4b235460549f894`  
		Last Modified: Fri, 08 May 2026 21:40:38 GMT  
		Size: 8.0 MB (7974840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36fc0888faf084e8c38943b57273357ca085b8f272c97699c2e464528b11c9b7`  
		Last Modified: Fri, 08 May 2026 21:40:37 GMT  
		Size: 12.8 KB (12798 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:8fa52e07957af55cd0dc7df314bdc24bf1dcb5a66045554ae7821c8684c01aae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:becc95dff92662eab5470178f38f4e68c66ad33985c2867797af5f976c084e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (184976515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752c06859dabaaef9d2dd62ea7b20f2a21b61f0d61e59f97addfac3333617cd1`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:40:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:26:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:19:36 GMT
MAINTAINER AntonOks
# Fri, 08 May 2026 21:19:36 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Fri, 08 May 2026 21:19:36 GMT
ARG rakudo_version=2026.03-01
# Fri, 08 May 2026 21:19:36 GMT
ENV rakudo_version=2026.03-01
# Fri, 08 May 2026 21:35:27 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 21:35:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Fri, 08 May 2026 21:35:27 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf6c0a95e34418907d5abfe604d08c5cc6bf9d689943856fcd842eb2be82c6c`  
		Last Modified: Fri, 08 May 2026 19:40:57 GMT  
		Size: 25.6 MB (25623106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a92b93bf7181c9d6b4525236a1a2fec85dc591d4deee481e828e707853f42c`  
		Last Modified: Fri, 08 May 2026 20:27:02 GMT  
		Size: 67.8 MB (67789206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46240e81cf02e288be339f64f94dcf8bf7ddc00ea0b0624bc56db109113d2e6`  
		Last Modified: Fri, 08 May 2026 21:35:41 GMT  
		Size: 3.2 KB (3243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d69b8e298bfac72d48946b3adf1fd8c3ba2d9aaf42c301c0e18e9bdc4c6a256`  
		Last Modified: Fri, 08 May 2026 21:35:42 GMT  
		Size: 42.3 MB (42258640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:5bd74c7bb6d99ee3e42787c4624b0a90afe8e158249d4840cf2a9a956a87e3d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:451fdc2f83a32e2f764bfaf3305a84f55103c914e5d59960fafa2431a4d8b430`

```dockerfile
```

-	Layers:
	-	`sha256:56cd30df74aabaf94c2aa85e77474cf89457156fe9bfc6f8f2fba50a58e015e9`  
		Last Modified: Fri, 08 May 2026 21:35:41 GMT  
		Size: 7.8 MB (7770666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a30ef50d81c9784fb53290e22ce97f39df612fec9a1c00e38b6289d842d9587a`  
		Last Modified: Fri, 08 May 2026 21:35:41 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:dee7fb4ecab2e1d9334fe442680c58607dc92ea0b0a54a1386fcf66cd98b86a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182557585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3def38ef5c552e78674daa05109c10bc7b4b9f77b6fe6a7732c3010cd65c9c7`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:42:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:19:38 GMT
MAINTAINER AntonOks
# Fri, 08 May 2026 21:19:38 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Fri, 08 May 2026 21:19:38 GMT
ARG rakudo_version=2026.03-01
# Fri, 08 May 2026 21:19:38 GMT
ENV rakudo_version=2026.03-01
# Fri, 08 May 2026 21:39:53 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 21:39:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Fri, 08 May 2026 21:39:53 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6968d8edb06bcdaf22846e8626a2500d70d68bae3413bca896fefe955e2a6ef0`  
		Last Modified: Fri, 08 May 2026 19:42:46 GMT  
		Size: 25.0 MB (25023476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc880ef5fbb726989fb57630c05c39cfe57a36a9f03c5b86a2d51c9c86ed66f2`  
		Last Modified: Fri, 08 May 2026 20:32:42 GMT  
		Size: 67.6 MB (67592055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d944f36e8d4737c299105fd017ba91ba09672d464f7eef4eb9cba7ba964b84a5`  
		Last Modified: Fri, 08 May 2026 21:40:08 GMT  
		Size: 3.2 KB (3243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6eeede9eacb1facb6d0661f8c30fba4020b7f3418c486bd58018b93f84c009`  
		Last Modified: Fri, 08 May 2026 21:40:10 GMT  
		Size: 40.3 MB (40269366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:32ccb461388015d98105e4686b54f68f3f43dd239085cf48fdbbf5f3c98cdd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7791441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c058b821f308233406eb7a0f952f31df392d7c5d0afcbd300853d1269c64ac9b`

```dockerfile
```

-	Layers:
	-	`sha256:c64fb2df571d20d6f12cfdf8883932c5bd26aedafab5008a5b3ff5a1ec8f521f`  
		Last Modified: Fri, 08 May 2026 21:40:09 GMT  
		Size: 7.8 MB (7778341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0de358beba4bf91db65e0d7dcb26181b827fe6146187d6fae4bedb81eb141b70`  
		Last Modified: Fri, 08 May 2026 21:40:08 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:trixie`

```console
$ docker pull rakudo-star@sha256:8fa52e07957af55cd0dc7df314bdc24bf1dcb5a66045554ae7821c8684c01aae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:becc95dff92662eab5470178f38f4e68c66ad33985c2867797af5f976c084e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (184976515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752c06859dabaaef9d2dd62ea7b20f2a21b61f0d61e59f97addfac3333617cd1`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:40:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:26:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:19:36 GMT
MAINTAINER AntonOks
# Fri, 08 May 2026 21:19:36 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Fri, 08 May 2026 21:19:36 GMT
ARG rakudo_version=2026.03-01
# Fri, 08 May 2026 21:19:36 GMT
ENV rakudo_version=2026.03-01
# Fri, 08 May 2026 21:35:27 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 21:35:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Fri, 08 May 2026 21:35:27 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf6c0a95e34418907d5abfe604d08c5cc6bf9d689943856fcd842eb2be82c6c`  
		Last Modified: Fri, 08 May 2026 19:40:57 GMT  
		Size: 25.6 MB (25623106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a92b93bf7181c9d6b4525236a1a2fec85dc591d4deee481e828e707853f42c`  
		Last Modified: Fri, 08 May 2026 20:27:02 GMT  
		Size: 67.8 MB (67789206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46240e81cf02e288be339f64f94dcf8bf7ddc00ea0b0624bc56db109113d2e6`  
		Last Modified: Fri, 08 May 2026 21:35:41 GMT  
		Size: 3.2 KB (3243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d69b8e298bfac72d48946b3adf1fd8c3ba2d9aaf42c301c0e18e9bdc4c6a256`  
		Last Modified: Fri, 08 May 2026 21:35:42 GMT  
		Size: 42.3 MB (42258640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:5bd74c7bb6d99ee3e42787c4624b0a90afe8e158249d4840cf2a9a956a87e3d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:451fdc2f83a32e2f764bfaf3305a84f55103c914e5d59960fafa2431a4d8b430`

```dockerfile
```

-	Layers:
	-	`sha256:56cd30df74aabaf94c2aa85e77474cf89457156fe9bfc6f8f2fba50a58e015e9`  
		Last Modified: Fri, 08 May 2026 21:35:41 GMT  
		Size: 7.8 MB (7770666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a30ef50d81c9784fb53290e22ce97f39df612fec9a1c00e38b6289d842d9587a`  
		Last Modified: Fri, 08 May 2026 21:35:41 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:dee7fb4ecab2e1d9334fe442680c58607dc92ea0b0a54a1386fcf66cd98b86a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182557585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3def38ef5c552e78674daa05109c10bc7b4b9f77b6fe6a7732c3010cd65c9c7`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:42:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:19:38 GMT
MAINTAINER AntonOks
# Fri, 08 May 2026 21:19:38 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Fri, 08 May 2026 21:19:38 GMT
ARG rakudo_version=2026.03-01
# Fri, 08 May 2026 21:19:38 GMT
ENV rakudo_version=2026.03-01
# Fri, 08 May 2026 21:39:53 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 08 May 2026 21:39:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Fri, 08 May 2026 21:39:53 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6968d8edb06bcdaf22846e8626a2500d70d68bae3413bca896fefe955e2a6ef0`  
		Last Modified: Fri, 08 May 2026 19:42:46 GMT  
		Size: 25.0 MB (25023476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc880ef5fbb726989fb57630c05c39cfe57a36a9f03c5b86a2d51c9c86ed66f2`  
		Last Modified: Fri, 08 May 2026 20:32:42 GMT  
		Size: 67.6 MB (67592055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d944f36e8d4737c299105fd017ba91ba09672d464f7eef4eb9cba7ba964b84a5`  
		Last Modified: Fri, 08 May 2026 21:40:08 GMT  
		Size: 3.2 KB (3243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6eeede9eacb1facb6d0661f8c30fba4020b7f3418c486bd58018b93f84c009`  
		Last Modified: Fri, 08 May 2026 21:40:10 GMT  
		Size: 40.3 MB (40269366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:32ccb461388015d98105e4686b54f68f3f43dd239085cf48fdbbf5f3c98cdd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7791441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c058b821f308233406eb7a0f952f31df392d7c5d0afcbd300853d1269c64ac9b`

```dockerfile
```

-	Layers:
	-	`sha256:c64fb2df571d20d6f12cfdf8883932c5bd26aedafab5008a5b3ff5a1ec8f521f`  
		Last Modified: Fri, 08 May 2026 21:40:09 GMT  
		Size: 7.8 MB (7778341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0de358beba4bf91db65e0d7dcb26181b827fe6146187d6fae4bedb81eb141b70`  
		Last Modified: Fri, 08 May 2026 21:40:08 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json
