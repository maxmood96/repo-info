<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rakudo-star`

-	[`rakudo-star:2020.01`](#rakudo-star202001)
-	[`rakudo-star:2020.01-alpine`](#rakudo-star202001-alpine)
-	[`rakudo-star:alpine`](#rakudo-staralpine)
-	[`rakudo-star:latest`](#rakudo-starlatest)

## `rakudo-star:2020.01`

```console
$ docker pull rakudo-star@sha256:29b1f51ac91075b9358604667e254a838d87072845ea70eeb81cfa9bfe04e551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `rakudo-star:2020.01` - linux; amd64

```console
$ docker pull rakudo-star@sha256:a5ffb8019f165e235d558f49dd4791462a0c07d3845b4ba1e92aaf54f4df19cc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (149989359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a302cb1f57b0a61a4dbb5188bf4dba0c808086717972897c6a231a679e88231`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:50:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 29 Apr 2020 02:31:56 GMT
MAINTAINER Rob Hoelz
# Wed, 29 Apr 2020 02:31:57 GMT
RUN groupadd -r raku && useradd -r -g raku raku
# Wed, 29 Apr 2020 02:31:57 GMT
ARG rakudo_version=2020.01
# Wed, 29 Apr 2020 02:31:58 GMT
ENV rakudo_version=2020.01
# Wed, 29 Apr 2020 02:47:07 GMT
RUN buildDeps='         gcc         libc6-dev         libencode-perl         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='ECF8B611205B447E091246AF959E3D6197190DD5 7A6C9EB8809CFEAF0ED4E09F18C438E6FF24326D B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -x     && export GNUPGHOME="$tmpdir"     && apt-get update     && apt-get --yes install --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && perl Configure.pl --prefix=/usr --gen-moar         && make install     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps
# Wed, 29 Apr 2020 02:47:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/site/bin
# Wed, 29 Apr 2020 02:47:08 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e27dc593d49a6d728dfe36976cb1469e076fbf3611e501fd030308cd212a80`  
		Last Modified: Thu, 23 Apr 2020 01:03:03 GMT  
		Size: 51.8 MB (51826941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2902f6f4aa3b0d78f3a2ca95ca889fb8319ea50c2c84452854e13e4fc6fa2fdd`  
		Last Modified: Wed, 29 Apr 2020 03:12:09 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f02acc9df549fa80e89ff0164afe84aabf3e9a13df84b79d530609a6b3b1e3d`  
		Last Modified: Wed, 29 Apr 2020 03:12:19 GMT  
		Size: 30.0 MB (29969327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rakudo-star:2020.01` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:bf3057b00d557c44494e918913f4c591ee10e39ecdfb40982e396eaca2976c04
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148725788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f27425a7ea22c3cf20aab0829e73a0027c1502f5319312efb61734db2910888b`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 23 Apr 2020 00:54:22 GMT
ADD file:c49818672222185a0a985a8511744bd524fce453bddb137364d79a793dc5740f in / 
# Thu, 23 Apr 2020 00:54:26 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:37:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 03:38:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 03:39:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 29 Apr 2020 03:34:31 GMT
MAINTAINER Rob Hoelz
# Wed, 29 Apr 2020 03:34:41 GMT
RUN groupadd -r raku && useradd -r -g raku raku
# Wed, 29 Apr 2020 03:34:47 GMT
ARG rakudo_version=2020.01
# Wed, 29 Apr 2020 03:34:48 GMT
ENV rakudo_version=2020.01
# Wed, 29 Apr 2020 04:02:29 GMT
RUN buildDeps='         gcc         libc6-dev         libencode-perl         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='ECF8B611205B447E091246AF959E3D6197190DD5 7A6C9EB8809CFEAF0ED4E09F18C438E6FF24326D B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -x     && export GNUPGHOME="$tmpdir"     && apt-get update     && apt-get --yes install --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && perl Configure.pl --prefix=/usr --gen-moar         && make install     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps
# Wed, 29 Apr 2020 04:02:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/site/bin
# Wed, 29 Apr 2020 04:02:34 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6243ff87266a170a3ad584d6c9c13f9b93c3aa84bded170c0040480f6c4e4170`  
		Last Modified: Thu, 23 Apr 2020 01:03:05 GMT  
		Size: 49.2 MB (49169698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0e7aea31e932e05b2ceba046f4e670116c0e81cfc82ca24a86a41afe7f0f98`  
		Last Modified: Thu, 23 Apr 2020 03:51:42 GMT  
		Size: 7.7 MB (7681533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ee43f3d2cbd321b8fb1657fed3947ec55776292d85377636a5fd3188d42662`  
		Last Modified: Thu, 23 Apr 2020 03:51:42 GMT  
		Size: 10.0 MB (9983945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bac10972135477f10794c7cecd0815eb04e84c70622089fc585b9622b1fabd9`  
		Last Modified: Thu, 23 Apr 2020 03:52:09 GMT  
		Size: 52.2 MB (52156992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db9670c04a1daa851cb6caadf6df6ebf0ceaab72faab5f6e6426e4f7c36f80c5`  
		Last Modified: Wed, 29 Apr 2020 04:15:13 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:169f1fdfbccb2c78eda5ebd69b7cf678261eace860fccac8ce130deb576c52ad`  
		Last Modified: Wed, 29 Apr 2020 04:15:25 GMT  
		Size: 29.7 MB (29731854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rakudo-star:2020.01-alpine`

```console
$ docker pull rakudo-star@sha256:d11cf8125f0d8808a7aa61d9ff05020f91bf25ccb8cd3b2722bfe0a3c5f77224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `rakudo-star:2020.01-alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:7582bde23313a17fe3f6c1959b46bbc3622432a8780530c2c4a2d7f5816e70df
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32447489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad4d6fbb74669b5b30726c2d599070fa83ba4868e262437469085efb6b3a0ea`
-	Default Command: `["raku"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:21 GMT
ADD file:66a440394c2442570f1f060e25c86613cb2d88a8af0c71c5a4154b3570e9a805 in / 
# Fri, 24 Apr 2020 01:05:21 GMT
CMD ["/bin/sh"]
# Wed, 29 Apr 2020 02:47:29 GMT
RUN addgroup -S raku && adduser -S raku -G raku
# Wed, 29 Apr 2020 02:47:29 GMT
ARG rakudo_version=2020.01
# Wed, 29 Apr 2020 02:47:29 GMT
ENV rakudo_version=2020.01
# Wed, 29 Apr 2020 03:11:59 GMT
RUN buildDeps='         gnupg         perl         perl-encode         gcc         libc-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='ECF8B611205B447E091246AF959E3D6197190DD5 7A6C9EB8809CFEAF0ED4E09F18C438E6FF24326D B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -x     && export GNUPGHOME="$tmpdir"     && apk add --no-cache --virtual .build-deps $buildDeps     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && perl Configure.pl --prefix=/usr --gen-moar         && make install     )     && rm -rf $tmpdir     && apk del .build-deps
# Wed, 29 Apr 2020 03:11:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/site/bin
# Wed, 29 Apr 2020 03:11:59 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:21c83c5242199776c232920ddb58cfa2a46b17e42ed831ca9001c8dbc532d22d`  
		Last Modified: Fri, 24 Apr 2020 01:06:07 GMT  
		Size: 2.8 MB (2795580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1309bc98d8d6bdf032bd788330f6a9b9829fae2ad0f22bfb0c70ccaa8cfa1f`  
		Last Modified: Wed, 29 Apr 2020 03:12:25 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ea977c03cd2ea114dada822df05948d13976d63d5f6c534a493927a71e64a8`  
		Last Modified: Wed, 29 Apr 2020 03:12:35 GMT  
		Size: 29.7 MB (29650653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rakudo-star:2020.01-alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:221ea7fd1fb65e9517d5e51d6831ab9a509b7ec45d855f87f6b9067fb83748ca
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 MB (31939635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1cc87342dbf7e66e1a629ba23269b90e12680d99df3f7d5275abd36923d7d95`
-	Default Command: `["raku"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:52 GMT
ADD file:75529f7e83edb6d0457a3b8bbfe33d4e3a12f339c5ace517d0f52dbedd9a146b in / 
# Fri, 24 Apr 2020 00:14:53 GMT
CMD ["/bin/sh"]
# Wed, 29 Apr 2020 04:02:56 GMT
RUN addgroup -S raku && adduser -S raku -G raku
# Wed, 29 Apr 2020 04:02:57 GMT
ARG rakudo_version=2020.01
# Wed, 29 Apr 2020 04:02:58 GMT
ENV rakudo_version=2020.01
# Wed, 29 Apr 2020 06:03:13 GMT
RUN buildDeps='         gnupg         perl         perl-encode         gcc         libc-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='ECF8B611205B447E091246AF959E3D6197190DD5 7A6C9EB8809CFEAF0ED4E09F18C438E6FF24326D B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -x     && export GNUPGHOME="$tmpdir"     && apk add --no-cache --virtual .build-deps $buildDeps     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && perl Configure.pl --prefix=/usr --gen-moar         && make install     )     && rm -rf $tmpdir     && apk del .build-deps
# Wed, 29 Apr 2020 06:03:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/site/bin
# Wed, 29 Apr 2020 06:03:16 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:b038bcb63e9c8905cc879c957302f686a9b43f24a18dcfc4186ab236ddf04cad`  
		Last Modified: Fri, 24 Apr 2020 00:15:54 GMT  
		Size: 2.7 MB (2718734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a84906ed6937a6e0af1caf5edb5e8c4970a4717f4e68c82a4fb947abd8ad150`  
		Last Modified: Wed, 29 Apr 2020 06:03:40 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e4fdfa66c93b748ea85652aa2a5178dd5766f9ccc347b84f1930c3f66f8ee5`  
		Last Modified: Wed, 29 Apr 2020 06:03:52 GMT  
		Size: 29.2 MB (29219615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:d11cf8125f0d8808a7aa61d9ff05020f91bf25ccb8cd3b2722bfe0a3c5f77224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:7582bde23313a17fe3f6c1959b46bbc3622432a8780530c2c4a2d7f5816e70df
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32447489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad4d6fbb74669b5b30726c2d599070fa83ba4868e262437469085efb6b3a0ea`
-	Default Command: `["raku"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:21 GMT
ADD file:66a440394c2442570f1f060e25c86613cb2d88a8af0c71c5a4154b3570e9a805 in / 
# Fri, 24 Apr 2020 01:05:21 GMT
CMD ["/bin/sh"]
# Wed, 29 Apr 2020 02:47:29 GMT
RUN addgroup -S raku && adduser -S raku -G raku
# Wed, 29 Apr 2020 02:47:29 GMT
ARG rakudo_version=2020.01
# Wed, 29 Apr 2020 02:47:29 GMT
ENV rakudo_version=2020.01
# Wed, 29 Apr 2020 03:11:59 GMT
RUN buildDeps='         gnupg         perl         perl-encode         gcc         libc-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='ECF8B611205B447E091246AF959E3D6197190DD5 7A6C9EB8809CFEAF0ED4E09F18C438E6FF24326D B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -x     && export GNUPGHOME="$tmpdir"     && apk add --no-cache --virtual .build-deps $buildDeps     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && perl Configure.pl --prefix=/usr --gen-moar         && make install     )     && rm -rf $tmpdir     && apk del .build-deps
# Wed, 29 Apr 2020 03:11:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/site/bin
# Wed, 29 Apr 2020 03:11:59 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:21c83c5242199776c232920ddb58cfa2a46b17e42ed831ca9001c8dbc532d22d`  
		Last Modified: Fri, 24 Apr 2020 01:06:07 GMT  
		Size: 2.8 MB (2795580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1309bc98d8d6bdf032bd788330f6a9b9829fae2ad0f22bfb0c70ccaa8cfa1f`  
		Last Modified: Wed, 29 Apr 2020 03:12:25 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ea977c03cd2ea114dada822df05948d13976d63d5f6c534a493927a71e64a8`  
		Last Modified: Wed, 29 Apr 2020 03:12:35 GMT  
		Size: 29.7 MB (29650653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:221ea7fd1fb65e9517d5e51d6831ab9a509b7ec45d855f87f6b9067fb83748ca
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 MB (31939635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1cc87342dbf7e66e1a629ba23269b90e12680d99df3f7d5275abd36923d7d95`
-	Default Command: `["raku"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:52 GMT
ADD file:75529f7e83edb6d0457a3b8bbfe33d4e3a12f339c5ace517d0f52dbedd9a146b in / 
# Fri, 24 Apr 2020 00:14:53 GMT
CMD ["/bin/sh"]
# Wed, 29 Apr 2020 04:02:56 GMT
RUN addgroup -S raku && adduser -S raku -G raku
# Wed, 29 Apr 2020 04:02:57 GMT
ARG rakudo_version=2020.01
# Wed, 29 Apr 2020 04:02:58 GMT
ENV rakudo_version=2020.01
# Wed, 29 Apr 2020 06:03:13 GMT
RUN buildDeps='         gnupg         perl         perl-encode         gcc         libc-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='ECF8B611205B447E091246AF959E3D6197190DD5 7A6C9EB8809CFEAF0ED4E09F18C438E6FF24326D B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -x     && export GNUPGHOME="$tmpdir"     && apk add --no-cache --virtual .build-deps $buildDeps     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && perl Configure.pl --prefix=/usr --gen-moar         && make install     )     && rm -rf $tmpdir     && apk del .build-deps
# Wed, 29 Apr 2020 06:03:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/site/bin
# Wed, 29 Apr 2020 06:03:16 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:b038bcb63e9c8905cc879c957302f686a9b43f24a18dcfc4186ab236ddf04cad`  
		Last Modified: Fri, 24 Apr 2020 00:15:54 GMT  
		Size: 2.7 MB (2718734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a84906ed6937a6e0af1caf5edb5e8c4970a4717f4e68c82a4fb947abd8ad150`  
		Last Modified: Wed, 29 Apr 2020 06:03:40 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e4fdfa66c93b748ea85652aa2a5178dd5766f9ccc347b84f1930c3f66f8ee5`  
		Last Modified: Wed, 29 Apr 2020 06:03:52 GMT  
		Size: 29.2 MB (29219615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:29b1f51ac91075b9358604667e254a838d87072845ea70eeb81cfa9bfe04e551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:a5ffb8019f165e235d558f49dd4791462a0c07d3845b4ba1e92aaf54f4df19cc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (149989359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a302cb1f57b0a61a4dbb5188bf4dba0c808086717972897c6a231a679e88231`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:50:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 29 Apr 2020 02:31:56 GMT
MAINTAINER Rob Hoelz
# Wed, 29 Apr 2020 02:31:57 GMT
RUN groupadd -r raku && useradd -r -g raku raku
# Wed, 29 Apr 2020 02:31:57 GMT
ARG rakudo_version=2020.01
# Wed, 29 Apr 2020 02:31:58 GMT
ENV rakudo_version=2020.01
# Wed, 29 Apr 2020 02:47:07 GMT
RUN buildDeps='         gcc         libc6-dev         libencode-perl         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='ECF8B611205B447E091246AF959E3D6197190DD5 7A6C9EB8809CFEAF0ED4E09F18C438E6FF24326D B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -x     && export GNUPGHOME="$tmpdir"     && apt-get update     && apt-get --yes install --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && perl Configure.pl --prefix=/usr --gen-moar         && make install     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps
# Wed, 29 Apr 2020 02:47:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/site/bin
# Wed, 29 Apr 2020 02:47:08 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e27dc593d49a6d728dfe36976cb1469e076fbf3611e501fd030308cd212a80`  
		Last Modified: Thu, 23 Apr 2020 01:03:03 GMT  
		Size: 51.8 MB (51826941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2902f6f4aa3b0d78f3a2ca95ca889fb8319ea50c2c84452854e13e4fc6fa2fdd`  
		Last Modified: Wed, 29 Apr 2020 03:12:09 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f02acc9df549fa80e89ff0164afe84aabf3e9a13df84b79d530609a6b3b1e3d`  
		Last Modified: Wed, 29 Apr 2020 03:12:19 GMT  
		Size: 30.0 MB (29969327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:bf3057b00d557c44494e918913f4c591ee10e39ecdfb40982e396eaca2976c04
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148725788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f27425a7ea22c3cf20aab0829e73a0027c1502f5319312efb61734db2910888b`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 23 Apr 2020 00:54:22 GMT
ADD file:c49818672222185a0a985a8511744bd524fce453bddb137364d79a793dc5740f in / 
# Thu, 23 Apr 2020 00:54:26 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:37:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 03:38:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 03:39:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 29 Apr 2020 03:34:31 GMT
MAINTAINER Rob Hoelz
# Wed, 29 Apr 2020 03:34:41 GMT
RUN groupadd -r raku && useradd -r -g raku raku
# Wed, 29 Apr 2020 03:34:47 GMT
ARG rakudo_version=2020.01
# Wed, 29 Apr 2020 03:34:48 GMT
ENV rakudo_version=2020.01
# Wed, 29 Apr 2020 04:02:29 GMT
RUN buildDeps='         gcc         libc6-dev         libencode-perl         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='ECF8B611205B447E091246AF959E3D6197190DD5 7A6C9EB8809CFEAF0ED4E09F18C438E6FF24326D B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -x     && export GNUPGHOME="$tmpdir"     && apt-get update     && apt-get --yes install --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && perl Configure.pl --prefix=/usr --gen-moar         && make install     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps
# Wed, 29 Apr 2020 04:02:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/site/bin
# Wed, 29 Apr 2020 04:02:34 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6243ff87266a170a3ad584d6c9c13f9b93c3aa84bded170c0040480f6c4e4170`  
		Last Modified: Thu, 23 Apr 2020 01:03:05 GMT  
		Size: 49.2 MB (49169698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0e7aea31e932e05b2ceba046f4e670116c0e81cfc82ca24a86a41afe7f0f98`  
		Last Modified: Thu, 23 Apr 2020 03:51:42 GMT  
		Size: 7.7 MB (7681533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ee43f3d2cbd321b8fb1657fed3947ec55776292d85377636a5fd3188d42662`  
		Last Modified: Thu, 23 Apr 2020 03:51:42 GMT  
		Size: 10.0 MB (9983945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bac10972135477f10794c7cecd0815eb04e84c70622089fc585b9622b1fabd9`  
		Last Modified: Thu, 23 Apr 2020 03:52:09 GMT  
		Size: 52.2 MB (52156992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db9670c04a1daa851cb6caadf6df6ebf0ceaab72faab5f6e6426e4f7c36f80c5`  
		Last Modified: Wed, 29 Apr 2020 04:15:13 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:169f1fdfbccb2c78eda5ebd69b7cf678261eace860fccac8ce130deb576c52ad`  
		Last Modified: Wed, 29 Apr 2020 04:15:25 GMT  
		Size: 29.7 MB (29731854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
