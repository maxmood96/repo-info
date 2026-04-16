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
