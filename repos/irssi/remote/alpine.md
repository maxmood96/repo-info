## `irssi:alpine`

```console
$ docker pull irssi@sha256:b404269638b505c913a02979a9f253a8e9e904e585c6bb3011b7afbc06908340
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
$ docker pull irssi@sha256:bac3d5c9afaa50fa166d54e4f8a6b82f8519d5f41f60e154925a961f498c67cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18451924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18b85f03e9dae76ebfd3a15dd2180db03fc5728ce1980f8ae072a7fbbdc15f3`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:28:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Fri, 01 Dec 2023 05:28:32 GMT
ENV HOME=/home/user
# Fri, 01 Dec 2023 05:28:33 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Fri, 01 Dec 2023 05:28:33 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 05:28:33 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 01 Dec 2023 05:28:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Fri, 01 Dec 2023 05:28:52 GMT
WORKDIR /home/user
# Fri, 01 Dec 2023 05:28:52 GMT
USER user
# Fri, 01 Dec 2023 05:28:52 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2253ad6954238459aeb69a5812221ad8d0a9cf6473cb145f43ec969741e3f7c`  
		Last Modified: Fri, 01 Dec 2023 05:29:12 GMT  
		Size: 9.6 MB (9645529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027edf83d9867e80bd5e7041a3da7cbbd50027d7f1e9018f1174b20ca77aea09`  
		Last Modified: Fri, 01 Dec 2023 05:29:10 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf95bf3609411e5c119950c792cabbb3c647eb384dafacbce7a70a601533c44`  
		Last Modified: Fri, 01 Dec 2023 05:29:11 GMT  
		Size: 5.4 MB (5402689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:51601527f7062d912289288c810b48a9d00b3922cef2a58b04787672ff913d07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17271200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3301b14e65fec26ab44af0807bbcd5ac7cfb9230618a31edcde72367a83b21da`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 01:09:50 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Fri, 01 Dec 2023 01:09:50 GMT
ENV HOME=/home/user
# Fri, 01 Dec 2023 01:09:51 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Fri, 01 Dec 2023 01:09:51 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 01:09:51 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 01 Dec 2023 01:10:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Fri, 01 Dec 2023 01:10:08 GMT
WORKDIR /home/user
# Fri, 01 Dec 2023 01:10:08 GMT
USER user
# Fri, 01 Dec 2023 01:10:08 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0389ed6f59ff0e95c3c6c4566157405d8b3bb4b5a827a5a1fd24edf934393c`  
		Last Modified: Fri, 01 Dec 2023 01:10:22 GMT  
		Size: 8.9 MB (8880077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4039f2bf7cbc0fa8f9a5e8a20f20a5035b388d7a42a95d9d6f0a3a58446eed`  
		Last Modified: Fri, 01 Dec 2023 01:10:19 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184e5e97ecd8a9cf4081a03b9f6a83022561e425f3294a0d09c345420c858123`  
		Last Modified: Fri, 01 Dec 2023 01:10:21 GMT  
		Size: 5.2 MB (5242968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:6ff758c9743e67bc2781d127b56339f483bfbb1251763d398a335d3a95ae9744
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16630768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ba268037301e762641733ac31d7ab82c0538e3658cc00205b6ca74c23bb5332`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:41:57 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Fri, 01 Dec 2023 08:41:57 GMT
ENV HOME=/home/user
# Fri, 01 Dec 2023 08:41:57 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Fri, 01 Dec 2023 08:41:57 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 08:41:57 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 01 Dec 2023 08:42:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Fri, 01 Dec 2023 08:42:12 GMT
WORKDIR /home/user
# Fri, 01 Dec 2023 08:42:12 GMT
USER user
# Fri, 01 Dec 2023 08:42:12 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505553baa092b1ac5dc9c2a961456e9728d5bfe4d15f5a93644f58c1a0c75d14`  
		Last Modified: Fri, 01 Dec 2023 08:42:31 GMT  
		Size: 8.7 MB (8721323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc7d412e24534e4f0eebe098495c5878f5184667c4180f22eb8b50bff5d78cf`  
		Last Modified: Fri, 01 Dec 2023 08:42:29 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d25439b4dd4f4d92fd4be67af55606656fd511d66a1f63715b0dd6d2eeab5b`  
		Last Modified: Fri, 01 Dec 2023 08:42:30 GMT  
		Size: 5.0 MB (5007154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:444032f59c771f9f8ecc9f1374f55b4f94016696d5e58a0931e61ae604748369
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18316372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03091ab8bcbd9db84ead2d162e748af025192b4ebc302c6a42bd11b034e026b`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 09:37:23 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Fri, 01 Dec 2023 09:37:23 GMT
ENV HOME=/home/user
# Fri, 01 Dec 2023 09:37:24 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Fri, 01 Dec 2023 09:37:24 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 09:37:24 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 01 Dec 2023 09:37:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Fri, 01 Dec 2023 09:37:36 GMT
WORKDIR /home/user
# Fri, 01 Dec 2023 09:37:36 GMT
USER user
# Fri, 01 Dec 2023 09:37:36 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408050d673681e97a81fefc3f0d62dc535741ab369d0f890dfd492fea579fc73`  
		Last Modified: Fri, 01 Dec 2023 09:37:55 GMT  
		Size: 9.7 MB (9672911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b351c7a82544307a7a55c5daa20a529cd389facb270805cea95b2040f8b864`  
		Last Modified: Fri, 01 Dec 2023 09:37:53 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad688b9a5733e1a4e2feaddf0a4ae2395f72b5d718efc48685befed72ad2d440`  
		Last Modified: Fri, 01 Dec 2023 09:37:54 GMT  
		Size: 5.3 MB (5309143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; 386

```console
$ docker pull irssi@sha256:cb5e5eb3ce2e5c8a080af15a2414c7078412473c44bfe7c15196f957fdd3931b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17557886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e422f2a321a825ce4ac90dad135af83afa3ee86cd59d10d667a313c1b2ec35a7`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 01 Dec 2023 02:03:44 GMT
ADD file:92902088cd15ed8f5dca2f7fc6570fb4e4824fac8b09e091c88e96bbd0ca814b in / 
# Fri, 01 Dec 2023 02:03:44 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 09:02:03 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Fri, 01 Dec 2023 09:02:03 GMT
ENV HOME=/home/user
# Fri, 01 Dec 2023 09:02:03 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Fri, 01 Dec 2023 09:02:04 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 09:02:04 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 01 Dec 2023 09:02:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Fri, 01 Dec 2023 09:02:38 GMT
WORKDIR /home/user
# Fri, 01 Dec 2023 09:02:38 GMT
USER user
# Fri, 01 Dec 2023 09:02:38 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4966a8bd129b0a6adf93dc295a8fbe8f665d3194a684a5ce199c1c3596dbf3d9`  
		Last Modified: Fri, 01 Dec 2023 02:04:18 GMT  
		Size: 3.2 MB (3238831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c194fdb04cb3e17be198ec377fafeb3f5716927ef33b40df425a942b4f3f7e50`  
		Last Modified: Fri, 01 Dec 2023 09:03:00 GMT  
		Size: 8.9 MB (8904478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc41f0a0151cdbeed763c916854e38b017669921f3a79d0554e77543dcb09acb`  
		Last Modified: Fri, 01 Dec 2023 09:02:57 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5a928454e9d9ee194c2842f26954fc39b31e235b0de4f542f9acc45af1737f`  
		Last Modified: Fri, 01 Dec 2023 09:02:58 GMT  
		Size: 5.4 MB (5413293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:e3eba53096e51def6997bdc72c51cf88f0019645321ee59bdd20b49b4236a617
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18717510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:890fc74fc94817011bde8d06e7b449e6407828cbbff17d07e69de027ad3d77f4`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:04:09 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Fri, 01 Dec 2023 05:04:12 GMT
ENV HOME=/home/user
# Fri, 01 Dec 2023 05:04:20 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Fri, 01 Dec 2023 05:04:21 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 05:04:21 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 01 Dec 2023 05:04:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Fri, 01 Dec 2023 05:04:59 GMT
WORKDIR /home/user
# Fri, 01 Dec 2023 05:05:00 GMT
USER user
# Fri, 01 Dec 2023 05:05:02 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5afc2e0a7e24376eade504bc1d0aee8fa44d1b246f3121de324296a57c0ff25d`  
		Last Modified: Fri, 01 Dec 2023 05:05:36 GMT  
		Size: 9.7 MB (9736497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04ef92e3c12ead968e636f09604f92720ce8750a3a7f114277c2ef6764219b6`  
		Last Modified: Fri, 01 Dec 2023 05:05:34 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce0f8ba67064d14f75d9e13652d96ba1e13e489eff4d5617c0e503e25106009`  
		Last Modified: Fri, 01 Dec 2023 05:05:35 GMT  
		Size: 5.6 MB (5631406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; s390x

```console
$ docker pull irssi@sha256:2f5751ebf70dce38c6c48dc4a4e7f72bdae9824a0da9b3b95c277c755139592c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18708403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30063d82b1a526f916c2be961b95561fad91acd4ecfa2942d616740be6105a20`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:08 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Thu, 30 Nov 2023 22:42:09 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:13:12 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Fri, 01 Dec 2023 08:13:13 GMT
ENV HOME=/home/user
# Fri, 01 Dec 2023 08:13:13 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Fri, 01 Dec 2023 08:13:14 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 08:13:14 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 01 Dec 2023 08:13:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Fri, 01 Dec 2023 08:13:35 GMT
WORKDIR /home/user
# Fri, 01 Dec 2023 08:13:35 GMT
USER user
# Fri, 01 Dec 2023 08:13:36 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c64be9d9a3f22087e689a8436399a73b9fb1f76114c8c4b5740080a6d178c9b`  
		Last Modified: Fri, 01 Dec 2023 08:14:02 GMT  
		Size: 10.1 MB (10083001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403430efaca857233fd4cc970775e8fb9b2bfa68899058f8046852bf2a25be16`  
		Last Modified: Fri, 01 Dec 2023 08:13:59 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9630989fe7d8e6fcb8d2886d67968d8118d654dbaa9787a1e4050fe5d293e589`  
		Last Modified: Fri, 01 Dec 2023 08:14:00 GMT  
		Size: 5.4 MB (5406662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
