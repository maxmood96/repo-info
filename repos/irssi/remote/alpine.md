## `irssi:alpine`

```console
$ docker pull irssi@sha256:32f16e040050491dc00e7f85e7c0b9126881b0374de4a319009d12fd7cce75b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `irssi:alpine` - linux; amd64

```console
$ docker pull irssi@sha256:ea6dd4cae5a87901d6561c4ec5905383f0ffd31dc072862ec3bfc9f52be51bdb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17470544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbdbd57b8e8f3d61feff52c3dd0e4a77b86c8ab0a60db7f5dd4f0b499ca1a9a6`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:41:24 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Tue, 09 Aug 2022 20:41:24 GMT
ENV HOME=/home/user
# Tue, 09 Aug 2022 20:41:25 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 09 Aug 2022 20:41:25 GMT
ENV LANG=C.UTF-8
# Tue, 09 Aug 2022 20:41:25 GMT
ENV IRSSI_VERSION=1.4.2
# Tue, 09 Aug 2022 20:41:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Tue, 09 Aug 2022 20:41:46 GMT
WORKDIR /home/user
# Tue, 09 Aug 2022 20:41:46 GMT
USER user
# Tue, 09 Aug 2022 20:41:46 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5d9a1c4c1f2ab14d46764ffc31eacb8ad8867425565610eddb4a37b96506dd`  
		Last Modified: Tue, 09 Aug 2022 20:42:05 GMT  
		Size: 9.6 MB (9641367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb63d9e300689b98b6818bc75a9d0f1240542f26918d5f03ee59744ca49b83c1`  
		Last Modified: Tue, 09 Aug 2022 20:42:05 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b9c190fc124c2012dca28f7fc3ac3c5efe9c138a52834b623b8bd71ac1a44a`  
		Last Modified: Tue, 09 Aug 2022 20:42:06 GMT  
		Size: 5.0 MB (5021842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:3a494d4239afb464641516da33a1ac5641f0b315b22fa104eac28aa0a72f9c28
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16382978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb33fdc30a24d339ba9656ee8df90546bae6308ff1b070dcc65098a1ff78e4dc`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 Jul 2022 19:49:37 GMT
ADD file:7a20333469e71664904a0cb8f61613250f2bd092b4a27bfa7bbae1dc7e21b7ed in / 
# Mon, 18 Jul 2022 19:49:37 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 21:02:43 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 18 Jul 2022 21:02:44 GMT
ENV HOME=/home/user
# Mon, 18 Jul 2022 21:02:46 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 18 Jul 2022 21:02:46 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 21:02:46 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 21:03:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 18 Jul 2022 21:03:20 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 21:03:21 GMT
USER user
# Mon, 18 Jul 2022 21:03:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b7885075fcd06a866d12dfd56eb704045eaadbd22dc03a224cd98715be566677`  
		Last Modified: Mon, 18 Jul 2022 19:08:42 GMT  
		Size: 2.6 MB (2606431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead05fb861289a3112d85fde030e8569e9a7dc8dd23508fe65d82f88ee0b12a3`  
		Last Modified: Mon, 18 Jul 2022 21:04:05 GMT  
		Size: 8.9 MB (8861206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86cdcb4e11581d3551b521decf6e7d4a73ad09f615896b0723f46ed075ef77e2`  
		Last Modified: Mon, 18 Jul 2022 21:03:57 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5685ef9768727bd6b69beb5438e3f2f0dd1cc972b33dfe398ca9f2fc28a2e6c3`  
		Last Modified: Mon, 18 Jul 2022 21:04:01 GMT  
		Size: 4.9 MB (4914057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:8b159bfe44ef61fe32554d34ea779177ff1e120d3cc57a538bc2d7015bfe861f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15829370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16323f4996b0a0df0c382fea80261be6277dda0c12eb1c60f95c396c296a786d`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 19:32:59 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Tue, 09 Aug 2022 19:32:59 GMT
ENV HOME=/home/user
# Tue, 09 Aug 2022 19:33:00 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 09 Aug 2022 19:33:00 GMT
ENV LANG=C.UTF-8
# Tue, 09 Aug 2022 19:33:00 GMT
ENV IRSSI_VERSION=1.4.2
# Tue, 09 Aug 2022 19:33:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Tue, 09 Aug 2022 19:33:52 GMT
WORKDIR /home/user
# Tue, 09 Aug 2022 19:33:52 GMT
USER user
# Tue, 09 Aug 2022 19:33:52 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08850f489e1f601ce2f8dccdba25847795fc54b3dcb55ba107f95cc3f0123c36`  
		Last Modified: Tue, 09 Aug 2022 19:34:37 GMT  
		Size: 8.7 MB (8718306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffe35cbcde0da632c5c0fcc26e3b31b10faaa0874d87de116244514f90f8c0e`  
		Last Modified: Tue, 09 Aug 2022 19:34:34 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa13f0efee7ddc81731da64d4d1c922ab8853f146bf3e306e18c059f5a7bfda`  
		Last Modified: Tue, 09 Aug 2022 19:34:36 GMT  
		Size: 4.7 MB (4692715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:5f850f4ffcb0ababe2a456df3f3a27bd2f9cce6c5b76c2c403d1237dfc3c96a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17237743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ab0c573bef0378b6c1ecd6f732d1e6fc5da398e2a7b83ae38453d43eeb9cb1`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:41:15 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Tue, 09 Aug 2022 20:41:16 GMT
ENV HOME=/home/user
# Tue, 09 Aug 2022 20:41:17 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 09 Aug 2022 20:41:18 GMT
ENV LANG=C.UTF-8
# Tue, 09 Aug 2022 20:41:19 GMT
ENV IRSSI_VERSION=1.4.2
# Tue, 09 Aug 2022 20:41:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Tue, 09 Aug 2022 20:41:38 GMT
WORKDIR /home/user
# Tue, 09 Aug 2022 20:41:39 GMT
USER user
# Tue, 09 Aug 2022 20:41:40 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f71300e5989b171ff91b55662b5c6e60fccf216a94e2dc523fb031c0bd2f2d`  
		Last Modified: Tue, 09 Aug 2022 20:42:08 GMT  
		Size: 9.6 MB (9622410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1865821a3671b3a1c2071d9304bb84bd275ae43c8b888fce5b2aa36a468f1686`  
		Last Modified: Tue, 09 Aug 2022 20:42:06 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080c6a619db387601df0d0ecd28d2259a06d26d4c410545736f2f473094e99a6`  
		Last Modified: Tue, 09 Aug 2022 20:42:07 GMT  
		Size: 4.9 MB (4906415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; 386

```console
$ docker pull irssi@sha256:6ed3028eb1909171f0f91a347ae155d04518b668de604dfa934052b72917d244
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16910572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a782321883e16ef8a4f3c93dce0d7e3f828b0b9fc0b011a31a0baeacc0caae`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 00:22:48 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Wed, 10 Aug 2022 00:22:49 GMT
ENV HOME=/home/user
# Wed, 10 Aug 2022 00:22:50 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Wed, 10 Aug 2022 00:22:51 GMT
ENV LANG=C.UTF-8
# Wed, 10 Aug 2022 00:22:52 GMT
ENV IRSSI_VERSION=1.4.2
# Wed, 10 Aug 2022 00:23:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Wed, 10 Aug 2022 00:23:13 GMT
WORKDIR /home/user
# Wed, 10 Aug 2022 00:23:14 GMT
USER user
# Wed, 10 Aug 2022 00:23:15 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978744516fa560e1c271bf8db3148e97ccde460713e502f8833989dfd642d5a1`  
		Last Modified: Wed, 10 Aug 2022 00:23:47 GMT  
		Size: 9.0 MB (9002955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4f72cf94df8e4f8de5d6d3b4997a3082e65894bc4a91137b1579fd4e4f02f2`  
		Last Modified: Wed, 10 Aug 2022 00:23:45 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22750e7e8147aff248d9c1a3b4b387ecaedba31a726ee7f9a1309cf6a34a5081`  
		Last Modified: Wed, 10 Aug 2022 00:23:46 GMT  
		Size: 5.1 MB (5099240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:1a5f3f068371c638326b4b99fee9bcea0d960bfcd57bc9744a00b26c611b6845
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17653661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd9d71d369cea216022e65e47ff44fa8eeea4c3efe3cba5141ccfb8d5c22b483`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:09 GMT
ADD file:66b351666e41834033d334aeb3dc6998dea77aa22e8e254028c923fee67a41a8 in / 
# Tue, 09 Aug 2022 17:17:10 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Tue, 09 Aug 2022 18:46:41 GMT
ENV HOME=/home/user
# Tue, 09 Aug 2022 18:46:42 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 09 Aug 2022 18:46:43 GMT
ENV LANG=C.UTF-8
# Tue, 09 Aug 2022 18:46:43 GMT
ENV IRSSI_VERSION=1.4.2
# Tue, 09 Aug 2022 18:47:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Tue, 09 Aug 2022 18:47:11 GMT
WORKDIR /home/user
# Tue, 09 Aug 2022 18:47:11 GMT
USER user
# Tue, 09 Aug 2022 18:47:11 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c79e5d1a8c89b87020a754c8a5c8370faaa37bfb5bca1d8af66770d522ef1caf`  
		Last Modified: Tue, 09 Aug 2022 17:18:26 GMT  
		Size: 2.8 MB (2803320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c57991f4206038524a4bddff6977cdb787830ff801f4eec780f96cd71882ae2`  
		Last Modified: Tue, 09 Aug 2022 18:47:44 GMT  
		Size: 9.7 MB (9733766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6607afe69f399563a6af6716005e0c00534c535f907afa7ebd0640b067743527`  
		Last Modified: Tue, 09 Aug 2022 18:47:40 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54fd143b8ec26961c67226fc801bda07f0f072ec60f57ac2968b6cffeb9e1c4b`  
		Last Modified: Tue, 09 Aug 2022 18:47:42 GMT  
		Size: 5.1 MB (5115292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; s390x

```console
$ docker pull irssi@sha256:7154308b12b2df03369f01f2870ef87cca6c81f07dcd756dfb475df3d405fe4a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17700482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316be5f59a3520b319fac3924c1742e959a5ddc7e1c52e1056ac29beb4f8a7c5`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 19:09:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Tue, 09 Aug 2022 19:09:55 GMT
ENV HOME=/home/user
# Tue, 09 Aug 2022 19:09:56 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 09 Aug 2022 19:09:56 GMT
ENV LANG=C.UTF-8
# Tue, 09 Aug 2022 19:09:56 GMT
ENV IRSSI_VERSION=1.4.2
# Tue, 09 Aug 2022 19:10:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Tue, 09 Aug 2022 19:10:16 GMT
WORKDIR /home/user
# Tue, 09 Aug 2022 19:10:16 GMT
USER user
# Tue, 09 Aug 2022 19:10:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:397bf195fe3fcd3305c8fc52aca185c710447ed85cea20e39fbe44d1bfa29a52`  
		Last Modified: Tue, 09 Aug 2022 19:10:48 GMT  
		Size: 10.1 MB (10078568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0a54068010fe482bca0eaa0c4dcad321f4e2364a0b993da60bb0a7be54ba62`  
		Last Modified: Tue, 09 Aug 2022 19:10:46 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2e3c693e69e0ec940fb8c074ef90c5b6a37d65f58970fb54a46322648fe1f8`  
		Last Modified: Tue, 09 Aug 2022 19:10:47 GMT  
		Size: 5.0 MB (5030034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
