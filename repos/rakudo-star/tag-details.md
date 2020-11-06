<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rakudo-star`

-	[`rakudo-star:2020.10`](#rakudo-star202010)
-	[`rakudo-star:2020.10-alpine`](#rakudo-star202010-alpine)
-	[`rakudo-star:alpine`](#rakudo-staralpine)
-	[`rakudo-star:latest`](#rakudo-starlatest)

## `rakudo-star:2020.10`

```console
$ docker pull rakudo-star@sha256:86234b35b9a7613b9b725642a94e6eeff6dabcf372eee631f15fe7f6c083fee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rakudo-star:2020.10` - linux; amd64

```console
$ docker pull rakudo-star@sha256:0cf3342741eb8b177cf5c1488fbea5eb4d74043648378243cbc0964ebc4be29a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.1 MB (160067596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:757eacab50b40e8136e2d3693752c19b8f6add9a95d1dc07a75aa6c3d751dc91`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 13 Oct 2020 01:38:30 GMT
ADD file:6627ad39ea0cb9fcb212342326d14efaff51aece1fd0dc16d5bbcaa25d858622 in / 
# Tue, 13 Oct 2020 01:38:30 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:14:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:14:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:15:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 14 Oct 2020 04:27:59 GMT
MAINTAINER Rob Hoelz
# Wed, 14 Oct 2020 04:27:59 GMT
RUN groupadd -r raku && useradd -r -g raku raku
# Fri, 06 Nov 2020 22:22:38 GMT
ARG rakudo_version=2020.10
# Fri, 06 Nov 2020 22:22:39 GMT
ENV rakudo_version=2020.10
# Fri, 06 Nov 2020 22:32:29 GMT
RUN buildDeps='         gcc         libc6-dev         libencode-perl         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -x     && export GNUPGHOME="$tmpdir"     && apt-get update     && apt-get --yes install --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps
# Fri, 06 Nov 2020 22:32:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/site/bin
# Fri, 06 Nov 2020 22:32:30 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:e4c3d3e4f7b024979a1c12daa4073f6353b2ba92d96418bc90451994927c9bff`  
		Last Modified: Tue, 13 Oct 2020 01:48:02 GMT  
		Size: 50.4 MB (50395978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101c41d0463bc77661fb3343235b16d536a92d2efb687046164d413e51bd4fc4`  
		Last Modified: Tue, 13 Oct 2020 02:28:35 GMT  
		Size: 7.8 MB (7811737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8275efcd805f9905d7def23603618236284b0be6b9e47455c638fbfb03fa9208`  
		Last Modified: Tue, 13 Oct 2020 02:28:35 GMT  
		Size: 10.0 MB (9996326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751620502a7a2905067c2f32d4982fb9b310b9808670ce82c0e2b40f5307a3ee`  
		Last Modified: Tue, 13 Oct 2020 02:28:53 GMT  
		Size: 51.8 MB (51829492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a507362ec7a5ae27c5c07857921eca55ed2c4e270e4b12ad9905770da2f705`  
		Last Modified: Wed, 14 Oct 2020 04:40:33 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b817222cf1b4c8fcbfbf29484a802ba88e7ae88449a74f1673aaf0129849d333`  
		Last Modified: Fri, 06 Nov 2020 22:44:11 GMT  
		Size: 40.0 MB (40032308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rakudo-star:2020.10-alpine`

```console
$ docker pull rakudo-star@sha256:bd10efa98144be262537f20ae271da515b8ba42b01d63f115fbcc93360e3c0b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rakudo-star:2020.10-alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:185e129596490f9648ecd17c147069cb0fb6ac5c88ebd9700e3f9c29459e3047
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42505492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee71c4c9d6dd159035d0def22729e461050195e4b9acc7c64f618f1592f0b485`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Fri, 06 Nov 2020 22:32:49 GMT
RUN addgroup -S raku && adduser -S raku -G raku
# Fri, 06 Nov 2020 22:32:49 GMT
ARG rakudo_version=2020.10
# Fri, 06 Nov 2020 22:32:49 GMT
ENV rakudo_version=2020.10
# Fri, 06 Nov 2020 22:43:53 GMT
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl         perl-encode     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -x     && export GNUPGHOME="$tmpdir"     && apk add --no-cache --virtual .build-deps $buildDeps     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del .build-deps
# Fri, 06 Nov 2020 22:43:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/site/bin
# Fri, 06 Nov 2020 22:43:54 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406cfbc4ad756e663752335e88cabb755c8d030849d683c60669928705b16abe`  
		Last Modified: Fri, 06 Nov 2020 22:44:16 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98383171d5c236fb0d35f7b1f683d7dc1ce0aa2ecdb285b11d327d00dde4fad5`  
		Last Modified: Fri, 06 Nov 2020 22:44:25 GMT  
		Size: 39.7 MB (39707402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:7d1769dcc2efd86eaff6383894714a32f799f0360b51a776821ab0a4f43e3cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:185e129596490f9648ecd17c147069cb0fb6ac5c88ebd9700e3f9c29459e3047
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42505492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee71c4c9d6dd159035d0def22729e461050195e4b9acc7c64f618f1592f0b485`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Fri, 06 Nov 2020 22:32:49 GMT
RUN addgroup -S raku && adduser -S raku -G raku
# Fri, 06 Nov 2020 22:32:49 GMT
ARG rakudo_version=2020.10
# Fri, 06 Nov 2020 22:32:49 GMT
ENV rakudo_version=2020.10
# Fri, 06 Nov 2020 22:43:53 GMT
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl         perl-encode     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -x     && export GNUPGHOME="$tmpdir"     && apk add --no-cache --virtual .build-deps $buildDeps     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del .build-deps
# Fri, 06 Nov 2020 22:43:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/site/bin
# Fri, 06 Nov 2020 22:43:54 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406cfbc4ad756e663752335e88cabb755c8d030849d683c60669928705b16abe`  
		Last Modified: Fri, 06 Nov 2020 22:44:16 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98383171d5c236fb0d35f7b1f683d7dc1ce0aa2ecdb285b11d327d00dde4fad5`  
		Last Modified: Fri, 06 Nov 2020 22:44:25 GMT  
		Size: 39.7 MB (39707402 bytes)  
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
$ docker pull rakudo-star@sha256:add0db1ab8a7a8413b4376ccb6327b838b2ed67b01a56f21231b152056cd9a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:0cf3342741eb8b177cf5c1488fbea5eb4d74043648378243cbc0964ebc4be29a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.1 MB (160067596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:757eacab50b40e8136e2d3693752c19b8f6add9a95d1dc07a75aa6c3d751dc91`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 13 Oct 2020 01:38:30 GMT
ADD file:6627ad39ea0cb9fcb212342326d14efaff51aece1fd0dc16d5bbcaa25d858622 in / 
# Tue, 13 Oct 2020 01:38:30 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:14:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:14:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:15:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 14 Oct 2020 04:27:59 GMT
MAINTAINER Rob Hoelz
# Wed, 14 Oct 2020 04:27:59 GMT
RUN groupadd -r raku && useradd -r -g raku raku
# Fri, 06 Nov 2020 22:22:38 GMT
ARG rakudo_version=2020.10
# Fri, 06 Nov 2020 22:22:39 GMT
ENV rakudo_version=2020.10
# Fri, 06 Nov 2020 22:32:29 GMT
RUN buildDeps='         gcc         libc6-dev         libencode-perl         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -x     && export GNUPGHOME="$tmpdir"     && apt-get update     && apt-get --yes install --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps
# Fri, 06 Nov 2020 22:32:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/site/bin
# Fri, 06 Nov 2020 22:32:30 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:e4c3d3e4f7b024979a1c12daa4073f6353b2ba92d96418bc90451994927c9bff`  
		Last Modified: Tue, 13 Oct 2020 01:48:02 GMT  
		Size: 50.4 MB (50395978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101c41d0463bc77661fb3343235b16d536a92d2efb687046164d413e51bd4fc4`  
		Last Modified: Tue, 13 Oct 2020 02:28:35 GMT  
		Size: 7.8 MB (7811737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8275efcd805f9905d7def23603618236284b0be6b9e47455c638fbfb03fa9208`  
		Last Modified: Tue, 13 Oct 2020 02:28:35 GMT  
		Size: 10.0 MB (9996326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751620502a7a2905067c2f32d4982fb9b310b9808670ce82c0e2b40f5307a3ee`  
		Last Modified: Tue, 13 Oct 2020 02:28:53 GMT  
		Size: 51.8 MB (51829492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a507362ec7a5ae27c5c07857921eca55ed2c4e270e4b12ad9905770da2f705`  
		Last Modified: Wed, 14 Oct 2020 04:40:33 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b817222cf1b4c8fcbfbf29484a802ba88e7ae88449a74f1673aaf0129849d333`  
		Last Modified: Fri, 06 Nov 2020 22:44:11 GMT  
		Size: 40.0 MB (40032308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:e2853030a9625a26fe1342e5148659daacda3d31d88e9b82169a1819ee7259d0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148413360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2fd8af940641074835ad6ee58b79aa39b3e549b06baa9841c2865b568ec0f0`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 13 Oct 2020 01:40:40 GMT
ADD file:7a9016f6c75910c392bbea2cb9e146d1eba3942cdfd666a44004c79951c5d46f in / 
# Tue, 13 Oct 2020 01:40:45 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:32:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:33:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:33:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 06 Nov 2020 04:50:21 GMT
MAINTAINER Rob Hoelz
# Fri, 06 Nov 2020 04:50:24 GMT
RUN groupadd -r raku && useradd -r -g raku raku
# Fri, 06 Nov 2020 04:50:25 GMT
ARG rakudo_version=2020.01
# Fri, 06 Nov 2020 04:50:25 GMT
ENV rakudo_version=2020.01
# Fri, 06 Nov 2020 05:16:06 GMT
RUN buildDeps='         gcc         libc6-dev         libencode-perl         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='ECF8B611205B447E091246AF959E3D6197190DD5 7A6C9EB8809CFEAF0ED4E09F18C438E6FF24326D B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -x     && export GNUPGHOME="$tmpdir"     && apt-get update     && apt-get --yes install --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && perl Configure.pl --prefix=/usr --gen-moar         && make install     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps
# Fri, 06 Nov 2020 05:16:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/site/bin
# Fri, 06 Nov 2020 05:16:08 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:04aacb10cb67f5fa248646a0ac9f40af5a6d3b0dbef65505bb7766bed6bf4885`  
		Last Modified: Tue, 13 Oct 2020 01:47:53 GMT  
		Size: 49.2 MB (49175405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136d6e4f4b17bdbefbe60820da5f5711a26d31c075dc69bcaf9b077d7d29262d`  
		Last Modified: Tue, 13 Oct 2020 02:47:32 GMT  
		Size: 7.7 MB (7681432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28db65b8364fc73072a0d5b51199cc9c6b108b4229d92e784b92ae67898dd0bd`  
		Last Modified: Tue, 13 Oct 2020 02:47:32 GMT  
		Size: 10.0 MB (9983936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff74fb95e95674d2f0c26f446a2cb7c0ee055d78182a9d61e1578c64c171f2b4`  
		Last Modified: Tue, 13 Oct 2020 02:48:00 GMT  
		Size: 52.2 MB (52163324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05feb6454a5939545e2055e2b9822799fb1d461993e9b953094fa6fb46a981c`  
		Last Modified: Fri, 06 Nov 2020 05:16:32 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbc40abf66c1f587ac5ab640e5dd416abdadb50ec34677492bfcf868aa97536`  
		Last Modified: Fri, 06 Nov 2020 05:16:43 GMT  
		Size: 29.4 MB (29407499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
