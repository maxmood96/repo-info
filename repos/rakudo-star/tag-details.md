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
$ docker pull rakudo-star@sha256:477868dda34169df69119cd436d1686d4dadae39d4b682ccde06dd8f3b42ac7b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2026.03-bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:6da4b186fcbb3597d995666c1fe9d6430be425ca5a23ba5f4ddc31133bdca7d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179128660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc3e9343b22091dc76c33a264201789fb76adc8819e500660f9b6e3a05fb871`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:42:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 21:47:40 GMT
MAINTAINER Rob Hoelz
# Mon, 13 Apr 2026 21:47:40 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 13 Apr 2026 21:47:40 GMT
ARG rakudo_version=2026.03-01
# Mon, 13 Apr 2026 21:47:40 GMT
ENV rakudo_version=2026.03-01
# Mon, 13 Apr 2026 22:02:16 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 13 Apr 2026 22:02:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 13 Apr 2026 22:02:16 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3414b1d6b49c54c305584faac46aad75c67644cf4f8495e8145206d28e416`  
		Last Modified: Tue, 07 Apr 2026 01:47:02 GMT  
		Size: 24.0 MB (24038269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de73ef470b7b271fede6f98a4c8376971bd059ce04ebc13b9f86e34e534b89ae`  
		Last Modified: Tue, 07 Apr 2026 02:43:01 GMT  
		Size: 64.4 MB (64396012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c8344afd9052e6f36f782bda78f65c2b71f84b9b0560a16ddf769debbf3575`  
		Last Modified: Mon, 13 Apr 2026 22:02:31 GMT  
		Size: 3.2 KB (3244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866618fc64df1c6a777283b5bd77f9bc17a9af3a079299bc5ce35431ecbb7b94`  
		Last Modified: Mon, 13 Apr 2026 22:02:33 GMT  
		Size: 42.2 MB (42202312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.03-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:311588993d729c59489197740c5b2c0c0cb3bf3a2ed7d2f3699d1c3a9f272e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4390640ace98027cd516dfe459fd1b5a62418d957c1432e0e55c7147aeb41bb3`

```dockerfile
```

-	Layers:
	-	`sha256:f20109be9561d544badb49f168a5c5f0f1858ed9fb48f30f76ac9bc7b0bf2035`  
		Last Modified: Mon, 13 Apr 2026 22:02:32 GMT  
		Size: 8.0 MB (7968447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26d6bfd680b5aa3beb4384da7f28fae233dadcadb15657d0eaa3512ab67d62e9`  
		Last Modified: Mon, 13 Apr 2026 22:02:31 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2026.03-bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:85d41733339a291c83c41631cf4cea7b2720b4065790a50f95d8e44fdbbce13c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176698140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe295060167058063fa7164ae2a902d0e0830bb5d2e1f8f699a8003f344df14`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:42:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 03:19:19 GMT
MAINTAINER Rob Hoelz
# Wed, 22 Apr 2026 03:19:19 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Wed, 22 Apr 2026 03:19:19 GMT
ARG rakudo_version=2026.03-01
# Wed, 22 Apr 2026 03:19:19 GMT
ENV rakudo_version=2026.03-01
# Wed, 22 Apr 2026 03:39:16 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 03:39:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 22 Apr 2026 03:39:16 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb7bd28fbdfe678a7f45878b7b1c07dbbc0fa7753b0312aa8fd049667a9e137`  
		Last Modified: Wed, 22 Apr 2026 01:43:06 GMT  
		Size: 23.6 MB (23609423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d07e8492bcee46202f5eae3e3010a470acc5139840e6d14556aefa3fc355f`  
		Last Modified: Wed, 22 Apr 2026 02:32:24 GMT  
		Size: 64.5 MB (64479606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd9ddd9942128d4292a02742e191ee9f2b68262789b1535ff18abbdb4404d4b`  
		Last Modified: Wed, 22 Apr 2026 03:39:31 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa9959ea151b5cc40210b49f90d1f167cbfd39a3f06363b2041c69acd87abb1`  
		Last Modified: Wed, 22 Apr 2026 03:39:32 GMT  
		Size: 40.2 MB (40232803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.03-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:8b1fea3389c927eff5b255015d71110e153fc2dd23f39cab9c50a25707642c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a26381b05f67618f5447122f803ef201e8edba352655c0c989c1a73b4573c09`

```dockerfile
```

-	Layers:
	-	`sha256:fa0c422bed7e4ea5c2772d2870c751d4db5078d5b9cf7c23738ea3837e744c48`  
		Last Modified: Wed, 22 Apr 2026 03:39:31 GMT  
		Size: 8.0 MB (7974840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60709cd4fd5dc24cd803b2c6e40085d22f9a0cdae87383b778085f4a0d6a4612`  
		Last Modified: Wed, 22 Apr 2026 03:39:31 GMT  
		Size: 12.8 KB (12797 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2026.03-trixie`

```console
$ docker pull rakudo-star@sha256:853c76e2b00100128d15610a17235b5f3e1ea0a5a22ab752bb0ca616decedb2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2026.03-trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:7799bfcd9f47feabcd1d1faf9766a33f400ccc95672d1e7d3ff3797a91ab7420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184864582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee335f6c4e49b431ebaf55bf84401e9be8ccd75e6f03c2b4fed36faa19562b9e`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:45:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:15:15 GMT
MAINTAINER AntonOks
# Wed, 22 Apr 2026 05:15:15 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Wed, 22 Apr 2026 05:15:15 GMT
ARG rakudo_version=2026.03-01
# Wed, 22 Apr 2026 05:15:15 GMT
ENV rakudo_version=2026.03-01
# Wed, 22 Apr 2026 05:29:28 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 05:29:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 22 Apr 2026 05:29:28 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5467f93954cfe1451f4333422086d00bd066cf33f42112b531804ffe06f0a929`  
		Last Modified: Wed, 22 Apr 2026 01:39:50 GMT  
		Size: 25.6 MB (25622443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d12c8f3f3fbb5bd2b8369adf3213e09d6b33f975462543ddfece85b2fe85e5`  
		Last Modified: Wed, 22 Apr 2026 04:45:50 GMT  
		Size: 67.8 MB (67790089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c06b142db6567c3c4208041d15bfdec47ca6d54e39ff5f25f6eebad4df99bb`  
		Last Modified: Wed, 22 Apr 2026 05:29:41 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5dded8e990040ceb68e219964be8cc38bcc7f0dcd7aa47cc9374a8aebd138c0`  
		Last Modified: Wed, 22 Apr 2026 05:29:43 GMT  
		Size: 42.1 MB (42146711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.03-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:a40d688f2395cea856c9e5b7e8fac9fb87d8c0df649febed037ba5bdfe6bd9ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a69d928e0bb06b26371a73243f36ee4ab97eb821026b58e92f3860483d7f760`

```dockerfile
```

-	Layers:
	-	`sha256:9caa78aeb132c46309812dd13056d27b00a705f26b9233f28a3391f314aaac01`  
		Last Modified: Wed, 22 Apr 2026 05:29:42 GMT  
		Size: 7.8 MB (7770666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:922c7d09fda53e4cea9255584a75815b224cf2bbfc2fd1dfdd379893cee5acd5`  
		Last Modified: Wed, 22 Apr 2026 05:29:41 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2026.03-trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:3b8b90e7ef2932d52579c2a135bbb6eab236b2a982641d6ee1add03fa126c634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182553211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882416f9241792ebd791e98b58ce9705f6e08d6224fd7e920c80fb1b99a5003c`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:43:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:32:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:19:17 GMT
MAINTAINER AntonOks
# Wed, 22 Apr 2026 03:19:17 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Wed, 22 Apr 2026 03:19:17 GMT
ARG rakudo_version=2026.03-01
# Wed, 22 Apr 2026 03:19:17 GMT
ENV rakudo_version=2026.03-01
# Wed, 22 Apr 2026 03:40:12 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 03:40:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 22 Apr 2026 03:40:12 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705f67984ab3d0b84dba0bf1b9e75bc42547713ab962aa5b392bacb0e61fa68b`  
		Last Modified: Wed, 22 Apr 2026 01:43:34 GMT  
		Size: 25.0 MB (25023409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c17e454c787ef19107fbea0250c33a4b6ca95fe0319ad68539a7bae9d9cad57`  
		Last Modified: Wed, 22 Apr 2026 02:32:52 GMT  
		Size: 67.6 MB (67584735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb58dc02113709e73b4e29c7ba564694d0ae46e265cef14510f2e6d18f0217e`  
		Last Modified: Wed, 22 Apr 2026 03:40:27 GMT  
		Size: 3.2 KB (3236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ce4f6e70807f9d2227e8a744c543da971dc09f193b7072bf3388ae65b0020e`  
		Last Modified: Wed, 22 Apr 2026 03:40:28 GMT  
		Size: 40.3 MB (40272586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.03-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:0bdb790ad8fe5f5d2be867ff2fbb269b1fb7065845918ecd54216f436d5c2bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7791441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2cfaeb2a7b9c71012f4ea167557443febb6cd30e94bfe9508e43bcf892fee1`

```dockerfile
```

-	Layers:
	-	`sha256:f9c8e949e3fe54ebef78602f3cc1e3f34836184f63ebad8767850bb798097c52`  
		Last Modified: Wed, 22 Apr 2026 03:40:27 GMT  
		Size: 7.8 MB (7778341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1a39a1db0c8afa73cbfc92a4322479112a27bd780139ef5ddb5b51966e02c14`  
		Last Modified: Wed, 22 Apr 2026 03:40:27 GMT  
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
$ docker pull rakudo-star@sha256:477868dda34169df69119cd436d1686d4dadae39d4b682ccde06dd8f3b42ac7b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:6da4b186fcbb3597d995666c1fe9d6430be425ca5a23ba5f4ddc31133bdca7d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179128660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc3e9343b22091dc76c33a264201789fb76adc8819e500660f9b6e3a05fb871`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:42:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 21:47:40 GMT
MAINTAINER Rob Hoelz
# Mon, 13 Apr 2026 21:47:40 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 13 Apr 2026 21:47:40 GMT
ARG rakudo_version=2026.03-01
# Mon, 13 Apr 2026 21:47:40 GMT
ENV rakudo_version=2026.03-01
# Mon, 13 Apr 2026 22:02:16 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 13 Apr 2026 22:02:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 13 Apr 2026 22:02:16 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3414b1d6b49c54c305584faac46aad75c67644cf4f8495e8145206d28e416`  
		Last Modified: Tue, 07 Apr 2026 01:47:02 GMT  
		Size: 24.0 MB (24038269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de73ef470b7b271fede6f98a4c8376971bd059ce04ebc13b9f86e34e534b89ae`  
		Last Modified: Tue, 07 Apr 2026 02:43:01 GMT  
		Size: 64.4 MB (64396012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c8344afd9052e6f36f782bda78f65c2b71f84b9b0560a16ddf769debbf3575`  
		Last Modified: Mon, 13 Apr 2026 22:02:31 GMT  
		Size: 3.2 KB (3244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866618fc64df1c6a777283b5bd77f9bc17a9af3a079299bc5ce35431ecbb7b94`  
		Last Modified: Mon, 13 Apr 2026 22:02:33 GMT  
		Size: 42.2 MB (42202312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:311588993d729c59489197740c5b2c0c0cb3bf3a2ed7d2f3699d1c3a9f272e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4390640ace98027cd516dfe459fd1b5a62418d957c1432e0e55c7147aeb41bb3`

```dockerfile
```

-	Layers:
	-	`sha256:f20109be9561d544badb49f168a5c5f0f1858ed9fb48f30f76ac9bc7b0bf2035`  
		Last Modified: Mon, 13 Apr 2026 22:02:32 GMT  
		Size: 8.0 MB (7968447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26d6bfd680b5aa3beb4384da7f28fae233dadcadb15657d0eaa3512ab67d62e9`  
		Last Modified: Mon, 13 Apr 2026 22:02:31 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:85d41733339a291c83c41631cf4cea7b2720b4065790a50f95d8e44fdbbce13c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176698140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe295060167058063fa7164ae2a902d0e0830bb5d2e1f8f699a8003f344df14`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:42:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 03:19:19 GMT
MAINTAINER Rob Hoelz
# Wed, 22 Apr 2026 03:19:19 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Wed, 22 Apr 2026 03:19:19 GMT
ARG rakudo_version=2026.03-01
# Wed, 22 Apr 2026 03:19:19 GMT
ENV rakudo_version=2026.03-01
# Wed, 22 Apr 2026 03:39:16 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 03:39:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 22 Apr 2026 03:39:16 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb7bd28fbdfe678a7f45878b7b1c07dbbc0fa7753b0312aa8fd049667a9e137`  
		Last Modified: Wed, 22 Apr 2026 01:43:06 GMT  
		Size: 23.6 MB (23609423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d07e8492bcee46202f5eae3e3010a470acc5139840e6d14556aefa3fc355f`  
		Last Modified: Wed, 22 Apr 2026 02:32:24 GMT  
		Size: 64.5 MB (64479606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd9ddd9942128d4292a02742e191ee9f2b68262789b1535ff18abbdb4404d4b`  
		Last Modified: Wed, 22 Apr 2026 03:39:31 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa9959ea151b5cc40210b49f90d1f167cbfd39a3f06363b2041c69acd87abb1`  
		Last Modified: Wed, 22 Apr 2026 03:39:32 GMT  
		Size: 40.2 MB (40232803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:8b1fea3389c927eff5b255015d71110e153fc2dd23f39cab9c50a25707642c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a26381b05f67618f5447122f803ef201e8edba352655c0c989c1a73b4573c09`

```dockerfile
```

-	Layers:
	-	`sha256:fa0c422bed7e4ea5c2772d2870c751d4db5078d5b9cf7c23738ea3837e744c48`  
		Last Modified: Wed, 22 Apr 2026 03:39:31 GMT  
		Size: 8.0 MB (7974840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60709cd4fd5dc24cd803b2c6e40085d22f9a0cdae87383b778085f4a0d6a4612`  
		Last Modified: Wed, 22 Apr 2026 03:39:31 GMT  
		Size: 12.8 KB (12797 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:853c76e2b00100128d15610a17235b5f3e1ea0a5a22ab752bb0ca616decedb2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:7799bfcd9f47feabcd1d1faf9766a33f400ccc95672d1e7d3ff3797a91ab7420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184864582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee335f6c4e49b431ebaf55bf84401e9be8ccd75e6f03c2b4fed36faa19562b9e`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:45:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:15:15 GMT
MAINTAINER AntonOks
# Wed, 22 Apr 2026 05:15:15 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Wed, 22 Apr 2026 05:15:15 GMT
ARG rakudo_version=2026.03-01
# Wed, 22 Apr 2026 05:15:15 GMT
ENV rakudo_version=2026.03-01
# Wed, 22 Apr 2026 05:29:28 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 05:29:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 22 Apr 2026 05:29:28 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5467f93954cfe1451f4333422086d00bd066cf33f42112b531804ffe06f0a929`  
		Last Modified: Wed, 22 Apr 2026 01:39:50 GMT  
		Size: 25.6 MB (25622443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d12c8f3f3fbb5bd2b8369adf3213e09d6b33f975462543ddfece85b2fe85e5`  
		Last Modified: Wed, 22 Apr 2026 04:45:50 GMT  
		Size: 67.8 MB (67790089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c06b142db6567c3c4208041d15bfdec47ca6d54e39ff5f25f6eebad4df99bb`  
		Last Modified: Wed, 22 Apr 2026 05:29:41 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5dded8e990040ceb68e219964be8cc38bcc7f0dcd7aa47cc9374a8aebd138c0`  
		Last Modified: Wed, 22 Apr 2026 05:29:43 GMT  
		Size: 42.1 MB (42146711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:a40d688f2395cea856c9e5b7e8fac9fb87d8c0df649febed037ba5bdfe6bd9ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a69d928e0bb06b26371a73243f36ee4ab97eb821026b58e92f3860483d7f760`

```dockerfile
```

-	Layers:
	-	`sha256:9caa78aeb132c46309812dd13056d27b00a705f26b9233f28a3391f314aaac01`  
		Last Modified: Wed, 22 Apr 2026 05:29:42 GMT  
		Size: 7.8 MB (7770666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:922c7d09fda53e4cea9255584a75815b224cf2bbfc2fd1dfdd379893cee5acd5`  
		Last Modified: Wed, 22 Apr 2026 05:29:41 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:3b8b90e7ef2932d52579c2a135bbb6eab236b2a982641d6ee1add03fa126c634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182553211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882416f9241792ebd791e98b58ce9705f6e08d6224fd7e920c80fb1b99a5003c`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:43:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:32:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:19:17 GMT
MAINTAINER AntonOks
# Wed, 22 Apr 2026 03:19:17 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Wed, 22 Apr 2026 03:19:17 GMT
ARG rakudo_version=2026.03-01
# Wed, 22 Apr 2026 03:19:17 GMT
ENV rakudo_version=2026.03-01
# Wed, 22 Apr 2026 03:40:12 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 03:40:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 22 Apr 2026 03:40:12 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705f67984ab3d0b84dba0bf1b9e75bc42547713ab962aa5b392bacb0e61fa68b`  
		Last Modified: Wed, 22 Apr 2026 01:43:34 GMT  
		Size: 25.0 MB (25023409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c17e454c787ef19107fbea0250c33a4b6ca95fe0319ad68539a7bae9d9cad57`  
		Last Modified: Wed, 22 Apr 2026 02:32:52 GMT  
		Size: 67.6 MB (67584735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb58dc02113709e73b4e29c7ba564694d0ae46e265cef14510f2e6d18f0217e`  
		Last Modified: Wed, 22 Apr 2026 03:40:27 GMT  
		Size: 3.2 KB (3236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ce4f6e70807f9d2227e8a744c543da971dc09f193b7072bf3388ae65b0020e`  
		Last Modified: Wed, 22 Apr 2026 03:40:28 GMT  
		Size: 40.3 MB (40272586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:0bdb790ad8fe5f5d2be867ff2fbb269b1fb7065845918ecd54216f436d5c2bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7791441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2cfaeb2a7b9c71012f4ea167557443febb6cd30e94bfe9508e43bcf892fee1`

```dockerfile
```

-	Layers:
	-	`sha256:f9c8e949e3fe54ebef78602f3cc1e3f34836184f63ebad8767850bb798097c52`  
		Last Modified: Wed, 22 Apr 2026 03:40:27 GMT  
		Size: 7.8 MB (7778341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1a39a1db0c8afa73cbfc92a4322479112a27bd780139ef5ddb5b51966e02c14`  
		Last Modified: Wed, 22 Apr 2026 03:40:27 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:trixie`

```console
$ docker pull rakudo-star@sha256:853c76e2b00100128d15610a17235b5f3e1ea0a5a22ab752bb0ca616decedb2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:7799bfcd9f47feabcd1d1faf9766a33f400ccc95672d1e7d3ff3797a91ab7420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184864582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee335f6c4e49b431ebaf55bf84401e9be8ccd75e6f03c2b4fed36faa19562b9e`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:45:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:15:15 GMT
MAINTAINER AntonOks
# Wed, 22 Apr 2026 05:15:15 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Wed, 22 Apr 2026 05:15:15 GMT
ARG rakudo_version=2026.03-01
# Wed, 22 Apr 2026 05:15:15 GMT
ENV rakudo_version=2026.03-01
# Wed, 22 Apr 2026 05:29:28 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 05:29:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 22 Apr 2026 05:29:28 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5467f93954cfe1451f4333422086d00bd066cf33f42112b531804ffe06f0a929`  
		Last Modified: Wed, 22 Apr 2026 01:39:50 GMT  
		Size: 25.6 MB (25622443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d12c8f3f3fbb5bd2b8369adf3213e09d6b33f975462543ddfece85b2fe85e5`  
		Last Modified: Wed, 22 Apr 2026 04:45:50 GMT  
		Size: 67.8 MB (67790089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c06b142db6567c3c4208041d15bfdec47ca6d54e39ff5f25f6eebad4df99bb`  
		Last Modified: Wed, 22 Apr 2026 05:29:41 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5dded8e990040ceb68e219964be8cc38bcc7f0dcd7aa47cc9374a8aebd138c0`  
		Last Modified: Wed, 22 Apr 2026 05:29:43 GMT  
		Size: 42.1 MB (42146711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:a40d688f2395cea856c9e5b7e8fac9fb87d8c0df649febed037ba5bdfe6bd9ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a69d928e0bb06b26371a73243f36ee4ab97eb821026b58e92f3860483d7f760`

```dockerfile
```

-	Layers:
	-	`sha256:9caa78aeb132c46309812dd13056d27b00a705f26b9233f28a3391f314aaac01`  
		Last Modified: Wed, 22 Apr 2026 05:29:42 GMT  
		Size: 7.8 MB (7770666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:922c7d09fda53e4cea9255584a75815b224cf2bbfc2fd1dfdd379893cee5acd5`  
		Last Modified: Wed, 22 Apr 2026 05:29:41 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:3b8b90e7ef2932d52579c2a135bbb6eab236b2a982641d6ee1add03fa126c634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182553211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882416f9241792ebd791e98b58ce9705f6e08d6224fd7e920c80fb1b99a5003c`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:43:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:32:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:19:17 GMT
MAINTAINER AntonOks
# Wed, 22 Apr 2026 03:19:17 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Wed, 22 Apr 2026 03:19:17 GMT
ARG rakudo_version=2026.03-01
# Wed, 22 Apr 2026 03:19:17 GMT
ENV rakudo_version=2026.03-01
# Wed, 22 Apr 2026 03:40:12 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 03:40:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 22 Apr 2026 03:40:12 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705f67984ab3d0b84dba0bf1b9e75bc42547713ab962aa5b392bacb0e61fa68b`  
		Last Modified: Wed, 22 Apr 2026 01:43:34 GMT  
		Size: 25.0 MB (25023409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c17e454c787ef19107fbea0250c33a4b6ca95fe0319ad68539a7bae9d9cad57`  
		Last Modified: Wed, 22 Apr 2026 02:32:52 GMT  
		Size: 67.6 MB (67584735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb58dc02113709e73b4e29c7ba564694d0ae46e265cef14510f2e6d18f0217e`  
		Last Modified: Wed, 22 Apr 2026 03:40:27 GMT  
		Size: 3.2 KB (3236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ce4f6e70807f9d2227e8a744c543da971dc09f193b7072bf3388ae65b0020e`  
		Last Modified: Wed, 22 Apr 2026 03:40:28 GMT  
		Size: 40.3 MB (40272586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:0bdb790ad8fe5f5d2be867ff2fbb269b1fb7065845918ecd54216f436d5c2bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7791441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2cfaeb2a7b9c71012f4ea167557443febb6cd30e94bfe9508e43bcf892fee1`

```dockerfile
```

-	Layers:
	-	`sha256:f9c8e949e3fe54ebef78602f3cc1e3f34836184f63ebad8767850bb798097c52`  
		Last Modified: Wed, 22 Apr 2026 03:40:27 GMT  
		Size: 7.8 MB (7778341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1a39a1db0c8afa73cbfc92a4322479112a27bd780139ef5ddb5b51966e02c14`  
		Last Modified: Wed, 22 Apr 2026 03:40:27 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json
