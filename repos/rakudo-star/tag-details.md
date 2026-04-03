<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rakudo-star`

-	[`rakudo-star:2026.02-alpine`](#rakudo-star202602-alpine)
-	[`rakudo-star:2026.02-bookworm`](#rakudo-star202602-bookworm)
-	[`rakudo-star:2026.02-trixie`](#rakudo-star202602-trixie)
-	[`rakudo-star:alpine`](#rakudo-staralpine)
-	[`rakudo-star:bookworm`](#rakudo-starbookworm)
-	[`rakudo-star:trixie`](#rakudo-startrixie)

## `rakudo-star:2026.02-alpine`

```console
$ docker pull rakudo-star@sha256:7ac96f5ac81916e6dfd1ee9c10d8272ac5197fbdb9ce41483a0775b058f76eb7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2026.02-alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:65f7307239605bfd5b3dbaa102a7ee2c1276e6f553e543c0c343f4a7f7463dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51384463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4866304546cd1c6d056b4d5e205407d4abaa3e015ad0ef0a105d8555849752f2`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:50:37 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Fri, 03 Apr 2026 17:04:33 GMT
ARG rakudo_version=2026.02-01
# Fri, 03 Apr 2026 17:04:33 GMT
ENV rakudo_version=2026.02-01
# Fri, 03 Apr 2026 17:04:33 GMT
# ARGS: rakudo_version=2026.02-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Fri, 03 Apr 2026 17:04:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Fri, 03 Apr 2026 17:04:33 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4dfe11419645f5381d5b113703e58c96e93c1583ea3b5ce5a9ff48f099d4dc`  
		Last Modified: Fri, 03 Apr 2026 17:04:43 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f622723c230a5fa4f037307e3dd4016873a120b69efbbcc075c22dc7ba4931d2`  
		Last Modified: Fri, 03 Apr 2026 17:04:44 GMT  
		Size: 47.5 MB (47521695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.02-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:4c64b12be6b7987c10efc78e4172a319f6cdf3eac12378fcdb1395cc242c07c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 KB (198691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dce5d63c7f6bf5bf6bc05b7e8f05d11f448e7054206be674f185b75e78b175a`

```dockerfile
```

-	Layers:
	-	`sha256:497f7c79200bc4d0c9f18ee1a45fcdda3b247e2f98bb10c2f0fa2637b8667546`  
		Last Modified: Fri, 03 Apr 2026 17:04:43 GMT  
		Size: 187.0 KB (186973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:364dad5c259fe66d1cf7264ffde2ad6fbf7922518189ed5f5d915bbde498f567`  
		Last Modified: Fri, 03 Apr 2026 17:04:43 GMT  
		Size: 11.7 KB (11718 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2026.02-alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:a22e4c3a07cedb3d352e1a027d96166ac52b8db7d934bb8bf15f255a9311355d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51470933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4427788d5f0bc0670e1e8c2776ff1d32999ecd06a2a36b9f5be80cf28daedf39`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:51:02 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Fri, 03 Apr 2026 17:12:02 GMT
ARG rakudo_version=2026.02-01
# Fri, 03 Apr 2026 17:12:02 GMT
ENV rakudo_version=2026.02-01
# Fri, 03 Apr 2026 17:12:02 GMT
# ARGS: rakudo_version=2026.02-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Fri, 03 Apr 2026 17:12:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Fri, 03 Apr 2026 17:12:02 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037a4159d66f13abdb14f3b4cba9429d2d3d44b7532889dcd0c54b8d0119025e`  
		Last Modified: Fri, 03 Apr 2026 17:12:14 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92489c94330b78a9754640b3b1ea4dc80d4f85ea127b47246570e86134e5b886`  
		Last Modified: Fri, 03 Apr 2026 17:12:15 GMT  
		Size: 47.3 MB (47272896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.02-alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:1a239fd58a86afb775ecc7cf9ae030104ab8d9be05082a58f114dec73d2accb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 KB (198168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d1821c09ef93b59dea2f66acf34839f644b58e6e6f8c9057b4361cc610c81e`

```dockerfile
```

-	Layers:
	-	`sha256:c7db9d1917c097cd9834e10bcde2e911f0db9cefe3a2ab364bbcbff1256f6f46`  
		Last Modified: Fri, 03 Apr 2026 17:12:14 GMT  
		Size: 186.4 KB (186355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0937fe8e1d49296519b3c32532aad91600401e75c5beb98e3de763996192770d`  
		Last Modified: Fri, 03 Apr 2026 17:12:14 GMT  
		Size: 11.8 KB (11813 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2026.02-bookworm`

```console
$ docker pull rakudo-star@sha256:e772efdb1cee5bc16120dd1eac7b7c991273139f46cdd6cb01f4d398310da696
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2026.02-bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:6cb12985fb14baba6fa14b5de550c45b886b980121aaf1aec69205a118bdcdb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177873498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e81e92082698f25c445ff8f6ea38fadff816559d3c7bcc02f9b2e52002a26e06`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:24:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 16:48:06 GMT
MAINTAINER Rob Hoelz
# Fri, 03 Apr 2026 16:48:06 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Fri, 03 Apr 2026 16:48:06 GMT
ARG rakudo_version=2026.02-01
# Fri, 03 Apr 2026 16:48:06 GMT
ENV rakudo_version=2026.02-01
# Fri, 03 Apr 2026 17:02:15 GMT
# ARGS: rakudo_version=2026.02-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 03 Apr 2026 17:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Fri, 03 Apr 2026 17:02:15 GMT
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
	-	`sha256:d85dbd65be1a9b40f924d04056f30bcc55074df685b90257d274d03b092c5d44`  
		Last Modified: Fri, 03 Apr 2026 17:02:30 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9ab3d37ba50c3637b9ffea4ce09d85353c534f35ca8f39a51f4233f43e25db`  
		Last Modified: Fri, 03 Apr 2026 17:02:31 GMT  
		Size: 40.9 MB (40947849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.02-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:76fe2632e77396f3f9cd4bfe7dc571438e65381bdd5c399faeb7e863fb6a9c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1d0ab4457a6835d30cf13b71aee477e3b4ded05e580c5975f2c028555b5101`

```dockerfile
```

-	Layers:
	-	`sha256:78ac7e5a2a3f08b233647b2face76315adce26236b5e79563958dc984354b546`  
		Last Modified: Fri, 03 Apr 2026 17:02:30 GMT  
		Size: 8.0 MB (7968447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4f07244960553fa44395fdf054b23b15673aaa10b2fa8c139ec8c390446ee87`  
		Last Modified: Fri, 03 Apr 2026 17:02:30 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2026.02-bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:871489e37db792c44e104fe89c52b07aa0fb7bfe6d8f26c0dd6f12b043d85fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175445090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38c981f7309c401832c35af77e5476295da6447d95fcba3ff6f8fd2596980d7b`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:30:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 16:49:14 GMT
MAINTAINER Rob Hoelz
# Fri, 03 Apr 2026 16:49:14 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Fri, 03 Apr 2026 16:49:14 GMT
ARG rakudo_version=2026.02-01
# Fri, 03 Apr 2026 16:49:14 GMT
ENV rakudo_version=2026.02-01
# Fri, 03 Apr 2026 17:07:56 GMT
# ARGS: rakudo_version=2026.02-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 03 Apr 2026 17:07:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Fri, 03 Apr 2026 17:07:56 GMT
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
	-	`sha256:563abae6eac1536b47743a8713ce934275f51a82cc7e645eff4370f137a787a4`  
		Last Modified: Fri, 03 Apr 2026 17:08:11 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0d1570e5b76bfe3b559e53dd0b3a631cbe6da79d956adbbbc4e655b815ea95`  
		Last Modified: Fri, 03 Apr 2026 17:08:13 GMT  
		Size: 39.0 MB (38984675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.02-bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:d8837b170d1d8dd99763e2917d582e482950a7d8e2ec15e30d6515137410765c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c4f1e4732b5f8bd8b7331083e8eccde5d3b9fbffa7e25d00fe67d63ab79d197`

```dockerfile
```

-	Layers:
	-	`sha256:aa4fddb3ebc2fcf40e5378315f866a596cb64234f29e91575f0a1d8bc8a5a493`  
		Last Modified: Fri, 03 Apr 2026 17:08:12 GMT  
		Size: 8.0 MB (7974840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:677ec8bf12b1a2399adb404d81227794ea3e56c6dad6ad7318275377ef2c4aac`  
		Last Modified: Fri, 03 Apr 2026 17:08:12 GMT  
		Size: 12.8 KB (12798 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:2026.02-trixie`

```console
$ docker pull rakudo-star@sha256:146bbcc1beb84f509d169d2777ed873c519364b542873553d1cea96a009a90c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:2026.02-trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:b86610468fc307c09289dee6e0e42b1c1a0757e394d12dd6809429a960bd3cdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183674684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427b75a5d505332a08c4dc8b60c5bfdeada105e02b930d9c39472103caaa44ad`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:38:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:25:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 03 Apr 2026 16:48:02 GMT
MAINTAINER AntonOks
# Fri, 03 Apr 2026 16:48:02 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Fri, 03 Apr 2026 16:48:02 GMT
ARG rakudo_version=2026.02-01
# Fri, 03 Apr 2026 16:48:02 GMT
ENV rakudo_version=2026.02-01
# Fri, 03 Apr 2026 17:02:30 GMT
# ARGS: rakudo_version=2026.02-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 03 Apr 2026 17:02:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Fri, 03 Apr 2026 17:02:30 GMT
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
	-	`sha256:057dd72c0508b5b843429b514063317ec0b8a34fab30981bfd832f1ab2dc6181`  
		Last Modified: Fri, 03 Apr 2026 17:02:45 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b94f60fda7cf700b36b1853419cfcbee307e31f6fc498d664e144baefe2658`  
		Last Modified: Fri, 03 Apr 2026 17:02:46 GMT  
		Size: 41.0 MB (40971441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.02-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:033421dbd2b87777bdde49c7349381cf9bb9fb3f4f139bcc2dc0807e151b6fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980f56dad88ff63bf2e02fd15a5782f228bad7bfae6feb532b1bf47f9706498d`

```dockerfile
```

-	Layers:
	-	`sha256:eade7d07912a683a27aa9d6d7d8beafe0ba9520f3677fff4d7de425983c6600a`  
		Last Modified: Fri, 03 Apr 2026 17:02:46 GMT  
		Size: 7.8 MB (7770304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dea1ec642db9331e451ee1b64782b127d8423a8b68241f990bca189ffd7ea000`  
		Last Modified: Fri, 03 Apr 2026 17:02:45 GMT  
		Size: 12.7 KB (12685 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:2026.02-trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:d5c6f9514810d4916a72a56e49d69bba768d320d64ab86c56b771911808ae586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.3 MB (181282614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:269d0a7b7269d31d277589719549d4fd39de05bca1e7ed5788fc28186d875dba`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:30:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 03 Apr 2026 16:48:42 GMT
MAINTAINER AntonOks
# Fri, 03 Apr 2026 16:48:42 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Fri, 03 Apr 2026 16:48:42 GMT
ARG rakudo_version=2026.02-01
# Fri, 03 Apr 2026 16:48:42 GMT
ENV rakudo_version=2026.02-01
# Fri, 03 Apr 2026 17:08:19 GMT
# ARGS: rakudo_version=2026.02-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 03 Apr 2026 17:08:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Fri, 03 Apr 2026 17:08:19 GMT
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
	-	`sha256:ae1131783f546848fafb465101404a0fd847156698c68062ed85837e8acb8574`  
		Last Modified: Fri, 03 Apr 2026 17:08:35 GMT  
		Size: 3.2 KB (3245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c93828b0f63386d7951699cac0832c05942eb6cbd094f16addf2500c1a485d0`  
		Last Modified: Fri, 03 Apr 2026 17:08:37 GMT  
		Size: 39.0 MB (39006120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:2026.02-trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:cd9cd59d881f3b7abf9f5a8d7e6e4429673c2b0ddd202851b8de32e2357bd6a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd775206cac4f8ca587e23038a30f8645127ff4ea6d0af1b4c633ddcc20105f`

```dockerfile
```

-	Layers:
	-	`sha256:7f2fbe656fc8d72c70f64b12aadff23310fe61889b435af7fd672f9f2d9779ae`  
		Last Modified: Fri, 03 Apr 2026 17:08:36 GMT  
		Size: 7.8 MB (7777967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b70be210d8025c56fd62595311f6219d71c6ce24a6119d15e12c8b498c481ec4`  
		Last Modified: Fri, 03 Apr 2026 17:08:35 GMT  
		Size: 12.8 KB (12779 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:7ac96f5ac81916e6dfd1ee9c10d8272ac5197fbdb9ce41483a0775b058f76eb7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:65f7307239605bfd5b3dbaa102a7ee2c1276e6f553e543c0c343f4a7f7463dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51384463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4866304546cd1c6d056b4d5e205407d4abaa3e015ad0ef0a105d8555849752f2`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:50:37 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Fri, 03 Apr 2026 17:04:33 GMT
ARG rakudo_version=2026.02-01
# Fri, 03 Apr 2026 17:04:33 GMT
ENV rakudo_version=2026.02-01
# Fri, 03 Apr 2026 17:04:33 GMT
# ARGS: rakudo_version=2026.02-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Fri, 03 Apr 2026 17:04:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Fri, 03 Apr 2026 17:04:33 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4dfe11419645f5381d5b113703e58c96e93c1583ea3b5ce5a9ff48f099d4dc`  
		Last Modified: Fri, 03 Apr 2026 17:04:43 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f622723c230a5fa4f037307e3dd4016873a120b69efbbcc075c22dc7ba4931d2`  
		Last Modified: Fri, 03 Apr 2026 17:04:44 GMT  
		Size: 47.5 MB (47521695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:4c64b12be6b7987c10efc78e4172a319f6cdf3eac12378fcdb1395cc242c07c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 KB (198691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dce5d63c7f6bf5bf6bc05b7e8f05d11f448e7054206be674f185b75e78b175a`

```dockerfile
```

-	Layers:
	-	`sha256:497f7c79200bc4d0c9f18ee1a45fcdda3b247e2f98bb10c2f0fa2637b8667546`  
		Last Modified: Fri, 03 Apr 2026 17:04:43 GMT  
		Size: 187.0 KB (186973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:364dad5c259fe66d1cf7264ffde2ad6fbf7922518189ed5f5d915bbde498f567`  
		Last Modified: Fri, 03 Apr 2026 17:04:43 GMT  
		Size: 11.7 KB (11718 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:a22e4c3a07cedb3d352e1a027d96166ac52b8db7d934bb8bf15f255a9311355d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51470933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4427788d5f0bc0670e1e8c2776ff1d32999ecd06a2a36b9f5be80cf28daedf39`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Fri, 03 Apr 2026 16:51:02 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Fri, 03 Apr 2026 17:12:02 GMT
ARG rakudo_version=2026.02-01
# Fri, 03 Apr 2026 17:12:02 GMT
ENV rakudo_version=2026.02-01
# Fri, 03 Apr 2026 17:12:02 GMT
# ARGS: rakudo_version=2026.02-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline git     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Fri, 03 Apr 2026 17:12:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Fri, 03 Apr 2026 17:12:02 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037a4159d66f13abdb14f3b4cba9429d2d3d44b7532889dcd0c54b8d0119025e`  
		Last Modified: Fri, 03 Apr 2026 17:12:14 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92489c94330b78a9754640b3b1ea4dc80d4f85ea127b47246570e86134e5b886`  
		Last Modified: Fri, 03 Apr 2026 17:12:15 GMT  
		Size: 47.3 MB (47272896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:1a239fd58a86afb775ecc7cf9ae030104ab8d9be05082a58f114dec73d2accb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 KB (198168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d1821c09ef93b59dea2f66acf34839f644b58e6e6f8c9057b4361cc610c81e`

```dockerfile
```

-	Layers:
	-	`sha256:c7db9d1917c097cd9834e10bcde2e911f0db9cefe3a2ab364bbcbff1256f6f46`  
		Last Modified: Fri, 03 Apr 2026 17:12:14 GMT  
		Size: 186.4 KB (186355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0937fe8e1d49296519b3c32532aad91600401e75c5beb98e3de763996192770d`  
		Last Modified: Fri, 03 Apr 2026 17:12:14 GMT  
		Size: 11.8 KB (11813 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:bookworm`

```console
$ docker pull rakudo-star@sha256:e772efdb1cee5bc16120dd1eac7b7c991273139f46cdd6cb01f4d398310da696
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:6cb12985fb14baba6fa14b5de550c45b886b980121aaf1aec69205a118bdcdb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177873498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e81e92082698f25c445ff8f6ea38fadff816559d3c7bcc02f9b2e52002a26e06`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:24:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 16:48:06 GMT
MAINTAINER Rob Hoelz
# Fri, 03 Apr 2026 16:48:06 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Fri, 03 Apr 2026 16:48:06 GMT
ARG rakudo_version=2026.02-01
# Fri, 03 Apr 2026 16:48:06 GMT
ENV rakudo_version=2026.02-01
# Fri, 03 Apr 2026 17:02:15 GMT
# ARGS: rakudo_version=2026.02-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 03 Apr 2026 17:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Fri, 03 Apr 2026 17:02:15 GMT
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
	-	`sha256:d85dbd65be1a9b40f924d04056f30bcc55074df685b90257d274d03b092c5d44`  
		Last Modified: Fri, 03 Apr 2026 17:02:30 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9ab3d37ba50c3637b9ffea4ce09d85353c534f35ca8f39a51f4233f43e25db`  
		Last Modified: Fri, 03 Apr 2026 17:02:31 GMT  
		Size: 40.9 MB (40947849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:76fe2632e77396f3f9cd4bfe7dc571438e65381bdd5c399faeb7e863fb6a9c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1d0ab4457a6835d30cf13b71aee477e3b4ded05e580c5975f2c028555b5101`

```dockerfile
```

-	Layers:
	-	`sha256:78ac7e5a2a3f08b233647b2face76315adce26236b5e79563958dc984354b546`  
		Last Modified: Fri, 03 Apr 2026 17:02:30 GMT  
		Size: 8.0 MB (7968447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4f07244960553fa44395fdf054b23b15673aaa10b2fa8c139ec8c390446ee87`  
		Last Modified: Fri, 03 Apr 2026 17:02:30 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:871489e37db792c44e104fe89c52b07aa0fb7bfe6d8f26c0dd6f12b043d85fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175445090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38c981f7309c401832c35af77e5476295da6447d95fcba3ff6f8fd2596980d7b`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:30:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Apr 2026 16:49:14 GMT
MAINTAINER Rob Hoelz
# Fri, 03 Apr 2026 16:49:14 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Fri, 03 Apr 2026 16:49:14 GMT
ARG rakudo_version=2026.02-01
# Fri, 03 Apr 2026 16:49:14 GMT
ENV rakudo_version=2026.02-01
# Fri, 03 Apr 2026 17:07:56 GMT
# ARGS: rakudo_version=2026.02-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 03 Apr 2026 17:07:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Fri, 03 Apr 2026 17:07:56 GMT
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
	-	`sha256:563abae6eac1536b47743a8713ce934275f51a82cc7e645eff4370f137a787a4`  
		Last Modified: Fri, 03 Apr 2026 17:08:11 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0d1570e5b76bfe3b559e53dd0b3a631cbe6da79d956adbbbc4e655b815ea95`  
		Last Modified: Fri, 03 Apr 2026 17:08:13 GMT  
		Size: 39.0 MB (38984675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:d8837b170d1d8dd99763e2917d582e482950a7d8e2ec15e30d6515137410765c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c4f1e4732b5f8bd8b7331083e8eccde5d3b9fbffa7e25d00fe67d63ab79d197`

```dockerfile
```

-	Layers:
	-	`sha256:aa4fddb3ebc2fcf40e5378315f866a596cb64234f29e91575f0a1d8bc8a5a493`  
		Last Modified: Fri, 03 Apr 2026 17:08:12 GMT  
		Size: 8.0 MB (7974840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:677ec8bf12b1a2399adb404d81227794ea3e56c6dad6ad7318275377ef2c4aac`  
		Last Modified: Fri, 03 Apr 2026 17:08:12 GMT  
		Size: 12.8 KB (12798 bytes)  
		MIME: application/vnd.in-toto+json

## `rakudo-star:trixie`

```console
$ docker pull rakudo-star@sha256:146bbcc1beb84f509d169d2777ed873c519364b542873553d1cea96a009a90c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:b86610468fc307c09289dee6e0e42b1c1a0757e394d12dd6809429a960bd3cdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183674684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427b75a5d505332a08c4dc8b60c5bfdeada105e02b930d9c39472103caaa44ad`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:38:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:25:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 03 Apr 2026 16:48:02 GMT
MAINTAINER AntonOks
# Fri, 03 Apr 2026 16:48:02 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Fri, 03 Apr 2026 16:48:02 GMT
ARG rakudo_version=2026.02-01
# Fri, 03 Apr 2026 16:48:02 GMT
ENV rakudo_version=2026.02-01
# Fri, 03 Apr 2026 17:02:30 GMT
# ARGS: rakudo_version=2026.02-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 03 Apr 2026 17:02:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Fri, 03 Apr 2026 17:02:30 GMT
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
	-	`sha256:057dd72c0508b5b843429b514063317ec0b8a34fab30981bfd832f1ab2dc6181`  
		Last Modified: Fri, 03 Apr 2026 17:02:45 GMT  
		Size: 3.2 KB (3240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b94f60fda7cf700b36b1853419cfcbee307e31f6fc498d664e144baefe2658`  
		Last Modified: Fri, 03 Apr 2026 17:02:46 GMT  
		Size: 41.0 MB (40971441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:033421dbd2b87777bdde49c7349381cf9bb9fb3f4f139bcc2dc0807e151b6fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980f56dad88ff63bf2e02fd15a5782f228bad7bfae6feb532b1bf47f9706498d`

```dockerfile
```

-	Layers:
	-	`sha256:eade7d07912a683a27aa9d6d7d8beafe0ba9520f3677fff4d7de425983c6600a`  
		Last Modified: Fri, 03 Apr 2026 17:02:46 GMT  
		Size: 7.8 MB (7770304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dea1ec642db9331e451ee1b64782b127d8423a8b68241f990bca189ffd7ea000`  
		Last Modified: Fri, 03 Apr 2026 17:02:45 GMT  
		Size: 12.7 KB (12685 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:d5c6f9514810d4916a72a56e49d69bba768d320d64ab86c56b771911808ae586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.3 MB (181282614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:269d0a7b7269d31d277589719549d4fd39de05bca1e7ed5788fc28186d875dba`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:30:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 03 Apr 2026 16:48:42 GMT
MAINTAINER AntonOks
# Fri, 03 Apr 2026 16:48:42 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Fri, 03 Apr 2026 16:48:42 GMT
ARG rakudo_version=2026.02-01
# Fri, 03 Apr 2026 16:48:42 GMT
ENV rakudo_version=2026.02-01
# Fri, 03 Apr 2026 17:08:19 GMT
# ARGS: rakudo_version=2026.02-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 03 Apr 2026 17:08:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Fri, 03 Apr 2026 17:08:19 GMT
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
	-	`sha256:ae1131783f546848fafb465101404a0fd847156698c68062ed85837e8acb8574`  
		Last Modified: Fri, 03 Apr 2026 17:08:35 GMT  
		Size: 3.2 KB (3245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c93828b0f63386d7951699cac0832c05942eb6cbd094f16addf2500c1a485d0`  
		Last Modified: Fri, 03 Apr 2026 17:08:37 GMT  
		Size: 39.0 MB (39006120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:cd9cd59d881f3b7abf9f5a8d7e6e4429673c2b0ddd202851b8de32e2357bd6a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd775206cac4f8ca587e23038a30f8645127ff4ea6d0af1b4c633ddcc20105f`

```dockerfile
```

-	Layers:
	-	`sha256:7f2fbe656fc8d72c70f64b12aadff23310fe61889b435af7fd672f9f2d9779ae`  
		Last Modified: Fri, 03 Apr 2026 17:08:36 GMT  
		Size: 7.8 MB (7777967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b70be210d8025c56fd62595311f6219d71c6ce24a6119d15e12c8b498c481ec4`  
		Last Modified: Fri, 03 Apr 2026 17:08:35 GMT  
		Size: 12.8 KB (12779 bytes)  
		MIME: application/vnd.in-toto+json
