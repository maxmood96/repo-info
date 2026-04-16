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
$ docker pull rakudo-star@sha256:9396a7dce9c6de74b99ea0d816877e6200c7f329fd30ff83703bc546a576a539
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
$ docker pull rakudo-star@sha256:4e04b37601f402b4e88993bc2eb68e7a9795dbe876af3ad3006da238a7d2a82f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.6 MB (176585306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e15667282f4e74dc1287243fb44ee34559041283843a6b427a646469108fdef`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:52:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 21:52:08 GMT
MAINTAINER Rob Hoelz
# Mon, 13 Apr 2026 21:52:08 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 13 Apr 2026 21:52:08 GMT
ARG rakudo_version=2026.03-01
# Mon, 13 Apr 2026 21:52:08 GMT
ENV rakudo_version=2026.03-01
# Mon, 13 Apr 2026 22:11:31 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 13 Apr 2026 22:11:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 13 Apr 2026 22:11:31 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af98f0879b367460715b477e9118922ba24f17d9a4ad8d70e595a9c4cf56990`  
		Last Modified: Tue, 07 Apr 2026 01:49:50 GMT  
		Size: 23.6 MB (23604705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b913dee6e116304b9bb2391ef8aedbb1f5ee16d167338920c7609a48bdd772`  
		Last Modified: Tue, 07 Apr 2026 02:53:06 GMT  
		Size: 64.5 MB (64479508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffce43d2458fb47b231039b561235bd56bc487151927f2b0b4c79969d22f82f`  
		Last Modified: Mon, 13 Apr 2026 22:11:47 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1409dd3fcf729b3d1aad4f5110f6be893edac1fb2ee1166b7223fafad6ce857`  
		Last Modified: Mon, 13 Apr 2026 22:11:48 GMT  
		Size: 40.1 MB (40124591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.03-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:976d57ed7c27cedc3e16e7d08e282620f75d3cc7400321a91234ba5c70b45876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2141c02b149bbef32424b05099a68e84c44e9de3c8eb46cccee94b75151a4dd9`

```dockerfile
```

-	Layers:
	-	`sha256:7356f24167bbff79f6d1da52007ee3d4005a5e14759ba2581724a09a4f0da38a`  
		Last Modified: Mon, 13 Apr 2026 22:11:47 GMT  
		Size: 8.0 MB (7974840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b89d5cdf72bf53de89d17966b715b312166fedac22d9e3fa24e42213227cfb51`  
		Last Modified: Mon, 13 Apr 2026 22:11:47 GMT  
		Size: 12.8 KB (12798 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2026.03-trixie`

```console
$ docker pull rakudo-star@sha256:ffcecd0daa42e80c3029f7217880738f4672e367994eb783757dd212682f511e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2026.03-trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:5e1e118e6a35dbdabc871e830c8c01f1d7d66b22facc826194ec56e73cfe7e34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184922881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37db924fe4a2130930163b00a4f5d8d16673d68ff4938ea6eec977ab2e0ebcb2`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:47:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:43:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 13 Apr 2026 21:46:44 GMT
MAINTAINER AntonOks
# Mon, 13 Apr 2026 21:46:44 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 13 Apr 2026 21:46:44 GMT
ARG rakudo_version=2026.03-01
# Mon, 13 Apr 2026 21:46:44 GMT
ENV rakudo_version=2026.03-01
# Mon, 13 Apr 2026 22:03:24 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 13 Apr 2026 22:03:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 13 Apr 2026 22:03:24 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33970743aee750df25f6c661132b7401c8fefe930e5f4803f4c8b6f567a6b55`  
		Last Modified: Tue, 07 Apr 2026 01:47:22 GMT  
		Size: 25.6 MB (25621678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5397da1d1537c4d725f3090c5688a582e14eeaf7743d75d9b38bad1649554987`  
		Last Modified: Tue, 07 Apr 2026 02:43:39 GMT  
		Size: 67.8 MB (67780708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a228dbe2677612d82ede2d95e3fd39f0eeaaf48d21f520e05acd9678284e07`  
		Last Modified: Mon, 13 Apr 2026 22:03:40 GMT  
		Size: 3.2 KB (3242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f78573956e12245067b2f4a1cf234374971d2b49e255ffd367d72a732a7c496`  
		Last Modified: Mon, 13 Apr 2026 22:03:41 GMT  
		Size: 42.2 MB (42219420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.03-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:a24706ca16d7bd9aac21a6bf15356d9b789dad7ea588c309e9009814dac2ed2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d214e5e5102dab9979168e0140ebe0f76732a8f7fd91391914214e97f11ff88`

```dockerfile
```

-	Layers:
	-	`sha256:40fb6bb1ec03c39ed29aa412af130c06e4a62971c674bcc264009bdb8aace792`  
		Last Modified: Mon, 13 Apr 2026 22:03:40 GMT  
		Size: 7.8 MB (7770612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a5aed902d99f75c9361979fede6894f8e119ba2dd3d5b928aa2280eebb8d29`  
		Last Modified: Mon, 13 Apr 2026 22:03:40 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2026.03-trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:6e59b113072012af6ab89a8150083cda2cdf9a4e7e990fc1bc309f08a00247dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182509485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e55c610f5f82eddcca8e92f3d1443646f0b633aad85ae7b40b7b5a8556f4e81`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:50:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:53:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 13 Apr 2026 21:51:48 GMT
MAINTAINER AntonOks
# Mon, 13 Apr 2026 21:51:48 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 13 Apr 2026 21:51:48 GMT
ARG rakudo_version=2026.03-01
# Mon, 13 Apr 2026 21:51:48 GMT
ENV rakudo_version=2026.03-01
# Mon, 13 Apr 2026 22:12:28 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 13 Apr 2026 22:12:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 13 Apr 2026 22:12:28 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277ee5883c1f173b0485b465221ddea5443b64c95935146f0bb3655baee3647d`  
		Last Modified: Tue, 07 Apr 2026 01:50:26 GMT  
		Size: 25.0 MB (25023654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6084ed286765ee022e8f8d9df76b9a2bd97a3224c379e905079f3bb11e1e48ca`  
		Last Modified: Tue, 07 Apr 2026 02:54:15 GMT  
		Size: 67.6 MB (67591915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29e6a5f08d5483c8a75ce08d32a0353f4459e4e076c4b2136103d1060959b8a`  
		Last Modified: Mon, 13 Apr 2026 22:12:45 GMT  
		Size: 3.2 KB (3241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b3e3bc1e45ec09da0459321b6873dd20351709947976bbd53e7ebcc8102a95`  
		Last Modified: Mon, 13 Apr 2026 22:12:46 GMT  
		Size: 40.2 MB (40225419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.03-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:3106a4b9e0fc67399c1acaa57821a81b8716c8f2d09116e1da80cfdbb12865d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7791387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419598772e5c8659634129aee7a7444fbb0b6a326c6f6a48cf2dd1235dd2be24`

```dockerfile
```

-	Layers:
	-	`sha256:8cb1fce8f5cc1838f24848952a5b4deed994260f446534db023686a40f76d944`  
		Last Modified: Mon, 13 Apr 2026 22:12:45 GMT  
		Size: 7.8 MB (7778287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10c762ea4900845eeb8385a9105369f7ce11d7b9ed78cc2d2820cf647d32e469`  
		Last Modified: Mon, 13 Apr 2026 22:12:45 GMT  
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
$ docker pull rakudo-star@sha256:9396a7dce9c6de74b99ea0d816877e6200c7f329fd30ff83703bc546a576a539
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
$ docker pull rakudo-star@sha256:4e04b37601f402b4e88993bc2eb68e7a9795dbe876af3ad3006da238a7d2a82f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.6 MB (176585306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e15667282f4e74dc1287243fb44ee34559041283843a6b427a646469108fdef`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:52:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 21:52:08 GMT
MAINTAINER Rob Hoelz
# Mon, 13 Apr 2026 21:52:08 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 13 Apr 2026 21:52:08 GMT
ARG rakudo_version=2026.03-01
# Mon, 13 Apr 2026 21:52:08 GMT
ENV rakudo_version=2026.03-01
# Mon, 13 Apr 2026 22:11:31 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 13 Apr 2026 22:11:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 13 Apr 2026 22:11:31 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af98f0879b367460715b477e9118922ba24f17d9a4ad8d70e595a9c4cf56990`  
		Last Modified: Tue, 07 Apr 2026 01:49:50 GMT  
		Size: 23.6 MB (23604705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b913dee6e116304b9bb2391ef8aedbb1f5ee16d167338920c7609a48bdd772`  
		Last Modified: Tue, 07 Apr 2026 02:53:06 GMT  
		Size: 64.5 MB (64479508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffce43d2458fb47b231039b561235bd56bc487151927f2b0b4c79969d22f82f`  
		Last Modified: Mon, 13 Apr 2026 22:11:47 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1409dd3fcf729b3d1aad4f5110f6be893edac1fb2ee1166b7223fafad6ce857`  
		Last Modified: Mon, 13 Apr 2026 22:11:48 GMT  
		Size: 40.1 MB (40124591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:976d57ed7c27cedc3e16e7d08e282620f75d3cc7400321a91234ba5c70b45876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2141c02b149bbef32424b05099a68e84c44e9de3c8eb46cccee94b75151a4dd9`

```dockerfile
```

-	Layers:
	-	`sha256:7356f24167bbff79f6d1da52007ee3d4005a5e14759ba2581724a09a4f0da38a`  
		Last Modified: Mon, 13 Apr 2026 22:11:47 GMT  
		Size: 8.0 MB (7974840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b89d5cdf72bf53de89d17966b715b312166fedac22d9e3fa24e42213227cfb51`  
		Last Modified: Mon, 13 Apr 2026 22:11:47 GMT  
		Size: 12.8 KB (12798 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:ffcecd0daa42e80c3029f7217880738f4672e367994eb783757dd212682f511e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:5e1e118e6a35dbdabc871e830c8c01f1d7d66b22facc826194ec56e73cfe7e34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184922881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37db924fe4a2130930163b00a4f5d8d16673d68ff4938ea6eec977ab2e0ebcb2`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:47:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:43:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 13 Apr 2026 21:46:44 GMT
MAINTAINER AntonOks
# Mon, 13 Apr 2026 21:46:44 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 13 Apr 2026 21:46:44 GMT
ARG rakudo_version=2026.03-01
# Mon, 13 Apr 2026 21:46:44 GMT
ENV rakudo_version=2026.03-01
# Mon, 13 Apr 2026 22:03:24 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 13 Apr 2026 22:03:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 13 Apr 2026 22:03:24 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33970743aee750df25f6c661132b7401c8fefe930e5f4803f4c8b6f567a6b55`  
		Last Modified: Tue, 07 Apr 2026 01:47:22 GMT  
		Size: 25.6 MB (25621678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5397da1d1537c4d725f3090c5688a582e14eeaf7743d75d9b38bad1649554987`  
		Last Modified: Tue, 07 Apr 2026 02:43:39 GMT  
		Size: 67.8 MB (67780708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a228dbe2677612d82ede2d95e3fd39f0eeaaf48d21f520e05acd9678284e07`  
		Last Modified: Mon, 13 Apr 2026 22:03:40 GMT  
		Size: 3.2 KB (3242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f78573956e12245067b2f4a1cf234374971d2b49e255ffd367d72a732a7c496`  
		Last Modified: Mon, 13 Apr 2026 22:03:41 GMT  
		Size: 42.2 MB (42219420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:a24706ca16d7bd9aac21a6bf15356d9b789dad7ea588c309e9009814dac2ed2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d214e5e5102dab9979168e0140ebe0f76732a8f7fd91391914214e97f11ff88`

```dockerfile
```

-	Layers:
	-	`sha256:40fb6bb1ec03c39ed29aa412af130c06e4a62971c674bcc264009bdb8aace792`  
		Last Modified: Mon, 13 Apr 2026 22:03:40 GMT  
		Size: 7.8 MB (7770612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a5aed902d99f75c9361979fede6894f8e119ba2dd3d5b928aa2280eebb8d29`  
		Last Modified: Mon, 13 Apr 2026 22:03:40 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:6e59b113072012af6ab89a8150083cda2cdf9a4e7e990fc1bc309f08a00247dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182509485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e55c610f5f82eddcca8e92f3d1443646f0b633aad85ae7b40b7b5a8556f4e81`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:50:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:53:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 13 Apr 2026 21:51:48 GMT
MAINTAINER AntonOks
# Mon, 13 Apr 2026 21:51:48 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 13 Apr 2026 21:51:48 GMT
ARG rakudo_version=2026.03-01
# Mon, 13 Apr 2026 21:51:48 GMT
ENV rakudo_version=2026.03-01
# Mon, 13 Apr 2026 22:12:28 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 13 Apr 2026 22:12:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 13 Apr 2026 22:12:28 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277ee5883c1f173b0485b465221ddea5443b64c95935146f0bb3655baee3647d`  
		Last Modified: Tue, 07 Apr 2026 01:50:26 GMT  
		Size: 25.0 MB (25023654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6084ed286765ee022e8f8d9df76b9a2bd97a3224c379e905079f3bb11e1e48ca`  
		Last Modified: Tue, 07 Apr 2026 02:54:15 GMT  
		Size: 67.6 MB (67591915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29e6a5f08d5483c8a75ce08d32a0353f4459e4e076c4b2136103d1060959b8a`  
		Last Modified: Mon, 13 Apr 2026 22:12:45 GMT  
		Size: 3.2 KB (3241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b3e3bc1e45ec09da0459321b6873dd20351709947976bbd53e7ebcc8102a95`  
		Last Modified: Mon, 13 Apr 2026 22:12:46 GMT  
		Size: 40.2 MB (40225419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:latest` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:3106a4b9e0fc67399c1acaa57821a81b8716c8f2d09116e1da80cfdbb12865d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7791387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419598772e5c8659634129aee7a7444fbb0b6a326c6f6a48cf2dd1235dd2be24`

```dockerfile
```

-	Layers:
	-	`sha256:8cb1fce8f5cc1838f24848952a5b4deed994260f446534db023686a40f76d944`  
		Last Modified: Mon, 13 Apr 2026 22:12:45 GMT  
		Size: 7.8 MB (7778287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10c762ea4900845eeb8385a9105369f7ce11d7b9ed78cc2d2820cf647d32e469`  
		Last Modified: Mon, 13 Apr 2026 22:12:45 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:trixie`

```console
$ docker pull rakudo-star@sha256:ffcecd0daa42e80c3029f7217880738f4672e367994eb783757dd212682f511e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:5e1e118e6a35dbdabc871e830c8c01f1d7d66b22facc826194ec56e73cfe7e34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184922881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37db924fe4a2130930163b00a4f5d8d16673d68ff4938ea6eec977ab2e0ebcb2`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:47:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:43:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 13 Apr 2026 21:46:44 GMT
MAINTAINER AntonOks
# Mon, 13 Apr 2026 21:46:44 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 13 Apr 2026 21:46:44 GMT
ARG rakudo_version=2026.03-01
# Mon, 13 Apr 2026 21:46:44 GMT
ENV rakudo_version=2026.03-01
# Mon, 13 Apr 2026 22:03:24 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 13 Apr 2026 22:03:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 13 Apr 2026 22:03:24 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33970743aee750df25f6c661132b7401c8fefe930e5f4803f4c8b6f567a6b55`  
		Last Modified: Tue, 07 Apr 2026 01:47:22 GMT  
		Size: 25.6 MB (25621678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5397da1d1537c4d725f3090c5688a582e14eeaf7743d75d9b38bad1649554987`  
		Last Modified: Tue, 07 Apr 2026 02:43:39 GMT  
		Size: 67.8 MB (67780708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a228dbe2677612d82ede2d95e3fd39f0eeaaf48d21f520e05acd9678284e07`  
		Last Modified: Mon, 13 Apr 2026 22:03:40 GMT  
		Size: 3.2 KB (3242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f78573956e12245067b2f4a1cf234374971d2b49e255ffd367d72a732a7c496`  
		Last Modified: Mon, 13 Apr 2026 22:03:41 GMT  
		Size: 42.2 MB (42219420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:a24706ca16d7bd9aac21a6bf15356d9b789dad7ea588c309e9009814dac2ed2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d214e5e5102dab9979168e0140ebe0f76732a8f7fd91391914214e97f11ff88`

```dockerfile
```

-	Layers:
	-	`sha256:40fb6bb1ec03c39ed29aa412af130c06e4a62971c674bcc264009bdb8aace792`  
		Last Modified: Mon, 13 Apr 2026 22:03:40 GMT  
		Size: 7.8 MB (7770612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a5aed902d99f75c9361979fede6894f8e119ba2dd3d5b928aa2280eebb8d29`  
		Last Modified: Mon, 13 Apr 2026 22:03:40 GMT  
		Size: 13.0 KB (12993 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:6e59b113072012af6ab89a8150083cda2cdf9a4e7e990fc1bc309f08a00247dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182509485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e55c610f5f82eddcca8e92f3d1443646f0b633aad85ae7b40b7b5a8556f4e81`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:50:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:53:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 13 Apr 2026 21:51:48 GMT
MAINTAINER AntonOks
# Mon, 13 Apr 2026 21:51:48 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Mon, 13 Apr 2026 21:51:48 GMT
ARG rakudo_version=2026.03-01
# Mon, 13 Apr 2026 21:51:48 GMT
ENV rakudo_version=2026.03-01
# Mon, 13 Apr 2026 22:12:28 GMT
# ARGS: rakudo_version=2026.03-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 13 Apr 2026 22:12:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Mon, 13 Apr 2026 22:12:28 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277ee5883c1f173b0485b465221ddea5443b64c95935146f0bb3655baee3647d`  
		Last Modified: Tue, 07 Apr 2026 01:50:26 GMT  
		Size: 25.0 MB (25023654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6084ed286765ee022e8f8d9df76b9a2bd97a3224c379e905079f3bb11e1e48ca`  
		Last Modified: Tue, 07 Apr 2026 02:54:15 GMT  
		Size: 67.6 MB (67591915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29e6a5f08d5483c8a75ce08d32a0353f4459e4e076c4b2136103d1060959b8a`  
		Last Modified: Mon, 13 Apr 2026 22:12:45 GMT  
		Size: 3.2 KB (3241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b3e3bc1e45ec09da0459321b6873dd20351709947976bbd53e7ebcc8102a95`  
		Last Modified: Mon, 13 Apr 2026 22:12:46 GMT  
		Size: 40.2 MB (40225419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:3106a4b9e0fc67399c1acaa57821a81b8716c8f2d09116e1da80cfdbb12865d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7791387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419598772e5c8659634129aee7a7444fbb0b6a326c6f6a48cf2dd1235dd2be24`

```dockerfile
```

-	Layers:
	-	`sha256:8cb1fce8f5cc1838f24848952a5b4deed994260f446534db023686a40f76d944`  
		Last Modified: Mon, 13 Apr 2026 22:12:45 GMT  
		Size: 7.8 MB (7778287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10c762ea4900845eeb8385a9105369f7ce11d7b9ed78cc2d2820cf647d32e469`  
		Last Modified: Mon, 13 Apr 2026 22:12:45 GMT  
		Size: 13.1 KB (13100 bytes)  
		MIME: application/vnd.in-toto+json
