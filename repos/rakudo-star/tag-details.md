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

**does not exist** (yet?)

## `rakudo-star:2026.03-bookworm`

**does not exist** (yet?)

## `rakudo-star:2026.03-trixie`

**does not exist** (yet?)

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
$ docker pull rakudo-star@sha256:540bd5850193c5e415ed66818813f74678e855fd20c4f9f89a96c77bbcfdfbd9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:bookworm` - linux; amd64

```console
$ docker pull rakudo-star@sha256:165bdca84baafedb8296a677de54a01f56ff8113ca9f58a05919fd72ed5c7d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177869160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a30e58a712e21528db818a04922513e992fd78c9bea978b4070368906ae1da2d`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:42:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:26:43 GMT
MAINTAINER Rob Hoelz
# Tue, 07 Apr 2026 03:26:43 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 07 Apr 2026 03:26:43 GMT
ARG rakudo_version=2026.02-01
# Tue, 07 Apr 2026 03:26:43 GMT
ENV rakudo_version=2026.02-01
# Tue, 07 Apr 2026 03:40:48 GMT
# ARGS: rakudo_version=2026.02-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 03:40:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 07 Apr 2026 03:40:48 GMT
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
	-	`sha256:46dea75998994c6e0a361484aa9f7f809eb916977c34611c6c9bcfab3d89761b`  
		Last Modified: Tue, 07 Apr 2026 03:41:08 GMT  
		Size: 3.2 KB (3239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae641c988c9e638bcd41fea181591a2e49ad86e01ec869201dbf650fcab8d47`  
		Last Modified: Tue, 07 Apr 2026 03:41:09 GMT  
		Size: 40.9 MB (40942817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:d8ff92077bb5bb8b91c58ef090dc9ba04f796e7bb3e1cfe063444dc676380cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56d328ff76f199ac876a40302b20074eba7380b001ced75a22790606e7ad1563`

```dockerfile
```

-	Layers:
	-	`sha256:cc9497c8ec5c6311b5bcb68545133317aba942163e351fc379ffed79ade58b31`  
		Last Modified: Tue, 07 Apr 2026 03:41:08 GMT  
		Size: 8.0 MB (7968447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70e8ca3a166091ae68bd8887f67bbb50c1521b4bd40d4d60c44b93212cd41c7e`  
		Last Modified: Tue, 07 Apr 2026 03:41:08 GMT  
		Size: 12.7 KB (12703 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:bookworm` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:925ac9a3acf3584eda680eec333ca797506f16f2296e7b91a8296a1c9c1c31fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175458839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd87dc47fcb6bccd64e7c546488ef65535fdff32d1b557e0c547d43df2901a6a`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:52:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:38:42 GMT
MAINTAINER Rob Hoelz
# Tue, 07 Apr 2026 03:38:42 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 07 Apr 2026 03:38:42 GMT
ARG rakudo_version=2026.02-01
# Tue, 07 Apr 2026 03:38:42 GMT
ENV rakudo_version=2026.02-01
# Tue, 07 Apr 2026 03:58:22 GMT
# ARGS: rakudo_version=2026.02-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 03:58:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 07 Apr 2026 03:58:22 GMT
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
	-	`sha256:5776a4df8ff97868f954e77fcc8f57df7d92eb81a0acd2af44818089c52df2af`  
		Last Modified: Tue, 07 Apr 2026 03:58:40 GMT  
		Size: 3.2 KB (3241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93926fbeece0016b3dfa7a27a5aa7bfa1398bc2e4df00efb1dd0ba3b15013c2c`  
		Last Modified: Tue, 07 Apr 2026 03:58:41 GMT  
		Size: 39.0 MB (38998123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:bookworm` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:6dd89c1d4a9ef073f41c7de1767a3cc08abcb4d6fc1d4978d64a031e0a23d443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce698d1825464b472449eb82b676afab644d52fe331a2377318c64d9120fd613`

```dockerfile
```

-	Layers:
	-	`sha256:5178d36d146d03d5028144567b83887583e055d47a2ada29ee9ee664e2b76340`  
		Last Modified: Tue, 07 Apr 2026 03:58:40 GMT  
		Size: 8.0 MB (7974840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30a8d98c42a0fdab869c4234e45e0d894e7b161c7355e8fc9537caa16298c5b5`  
		Last Modified: Tue, 07 Apr 2026 03:58:40 GMT  
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
$ docker pull rakudo-star@sha256:d61f9353a8091955fbeb493d728f48a00c02fbe6322058e5438731ec7a4cd61a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:trixie` - linux; amd64

```console
$ docker pull rakudo-star@sha256:23101a16105f652d19844b48b6c43174ab0be3d6e259e0b5ec48de4e80a9caae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183669958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6212dab6d87fb18387d387f1cc742eb0dba25c59745fc3f050a2d012d699fc9`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:47:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:43:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:26:38 GMT
MAINTAINER AntonOks
# Tue, 07 Apr 2026 03:26:38 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 07 Apr 2026 03:26:38 GMT
ARG rakudo_version=2026.02-01
# Tue, 07 Apr 2026 03:26:38 GMT
ENV rakudo_version=2026.02-01
# Tue, 07 Apr 2026 03:41:31 GMT
# ARGS: rakudo_version=2026.02-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 03:41:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 07 Apr 2026 03:41:31 GMT
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
	-	`sha256:d57257cc462fa158485ef8936cd001a9943d468b402767efa82318d2028e6c91`  
		Last Modified: Tue, 07 Apr 2026 03:41:54 GMT  
		Size: 3.2 KB (3244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2492036ef8b49a1d58934bcbdc738b245ebd52a46460367bfef2f1f8100e5188`  
		Last Modified: Tue, 07 Apr 2026 03:41:56 GMT  
		Size: 41.0 MB (40966495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:591e75b5f0b6537d2180e7d1a582affa1ed347a659fe586e37b8a7a8120c42f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab85bfa57736b9c3245d1338d86f6bb4778d5e0de329e6a94ae01fb207f45ab`

```dockerfile
```

-	Layers:
	-	`sha256:20706ef706724d170da8fc89fb063e896e8f0d302d627ee96484a3a075aa4efe`  
		Last Modified: Tue, 07 Apr 2026 03:41:55 GMT  
		Size: 7.8 MB (7770304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a012bcbfd00716b658df4d3f2f0efa995c4681589b7955519694c5ed5b02ce06`  
		Last Modified: Tue, 07 Apr 2026 03:41:55 GMT  
		Size: 12.7 KB (12685 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:trixie` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:8c08e943da1e75067e48d29eb62016d4767a67c36f79c895b2ec0d8fd3a48c89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.3 MB (181299328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c354eeb17bec78712e460b0772e2e20a36dbe5047479e15d149ec24d9599da`
-	Default Command: `["raku"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:50:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:53:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:38:41 GMT
MAINTAINER AntonOks
# Tue, 07 Apr 2026 03:38:41 GMT
RUN groupadd -r raku && useradd -m -r -g raku raku # buildkit
# Tue, 07 Apr 2026 03:38:41 GMT
ARG rakudo_version=2026.02-01
# Tue, 07 Apr 2026 03:38:41 GMT
ENV rakudo_version=2026.02-01
# Tue, 07 Apr 2026 03:59:16 GMT
# ARGS: rakudo_version=2026.02-01
RUN buildDeps='         gcc         libc6-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir/gnupg"     && mkdir $GNUPGHOME     && apt-get update     && apt-get install -y --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && curl -fsSL $pubkeyurl -o ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 03:59:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Tue, 07 Apr 2026 03:59:16 GMT
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
	-	`sha256:c46650357223e61e94f7bb3c68d8e9cf2287be7baa477bb9440b1f7189998d40`  
		Last Modified: Tue, 07 Apr 2026 03:59:32 GMT  
		Size: 3.2 KB (3241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb9a4a6428e8db5658a620e9299ee1221deb67b6dde6db6e8e0c3f993ab19f2`  
		Last Modified: Tue, 07 Apr 2026 03:59:33 GMT  
		Size: 39.0 MB (39015262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:trixie` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:745f8649a74da9b0ce4dae5db94a181fa1db09ff8a8ec7ef1a568c7ab2f99e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7790747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7027998df555dcf27f3e6c4529e901263ace61d3b9dc1e221844e22e12b25ae`

```dockerfile
```

-	Layers:
	-	`sha256:41479ffb9744a5ff5c316b85d3746447f03b4a3cd485dc89e35d35def4793b87`  
		Last Modified: Tue, 07 Apr 2026 03:59:32 GMT  
		Size: 7.8 MB (7777967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b88e25a2da8d045158cbbfd4ad652329cba4140ef9f5133c07780565cb37df68`  
		Last Modified: Tue, 07 Apr 2026 03:59:32 GMT  
		Size: 12.8 KB (12780 bytes)  
		MIME: application/vnd.in-toto+json
