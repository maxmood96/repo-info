## `irssi:alpine`

```console
$ docker pull irssi@sha256:de5ef2125bf0cebc155c6ea8918e436e20bafefb65204e43f44174283de8ec05
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
$ docker pull irssi@sha256:1ee6ea9617f00ef85aec02096aeee93e253c1fce4f559a3739175f1412110887
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18840008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7066a07c9e35db2f3641c82d1b1599ebb7ecfbba2d78659f3093927b81c6f9`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:07:22 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Thu, 28 Sep 2023 23:07:22 GMT
ENV HOME=/home/user
# Thu, 28 Sep 2023 23:07:23 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Thu, 28 Sep 2023 23:07:23 GMT
ENV LANG=C.UTF-8
# Fri, 06 Oct 2023 20:05:43 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 06 Oct 2023 20:06:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Fri, 06 Oct 2023 20:06:02 GMT
WORKDIR /home/user
# Fri, 06 Oct 2023 20:06:02 GMT
USER user
# Fri, 06 Oct 2023 20:06:02 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af553cbaa1665f3df3ff9ed6df3fc8fdeef915391198875444aee02cb0f1dba`  
		Last Modified: Thu, 28 Sep 2023 23:08:01 GMT  
		Size: 9.6 MB (9638068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:475821153744984a56837800be5e45c520da1740ad0e9e56b1a27abb64ab5677`  
		Last Modified: Thu, 28 Sep 2023 23:07:59 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6870b695db89ae46f18ed0a5ea51ba2cb82240d1c5b1c5219a7030798a3f67`  
		Last Modified: Fri, 06 Oct 2023 20:06:47 GMT  
		Size: 5.8 MB (5798688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:669d619d8edfe2681c4ac13ac5feec1996e7453c842461a6f42b44e3420c68be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17664736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfec5f4b576746c72f38383deb43d865442459b8ca2e40a74a5190e7eb6e22e2`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:28:20 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Sat, 21 Oct 2023 00:28:20 GMT
ENV HOME=/home/user
# Sat, 21 Oct 2023 00:28:21 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Sat, 21 Oct 2023 00:28:21 GMT
ENV LANG=C.UTF-8
# Sat, 21 Oct 2023 00:28:21 GMT
ENV IRSSI_VERSION=1.4.5
# Sat, 21 Oct 2023 00:28:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Sat, 21 Oct 2023 00:28:41 GMT
WORKDIR /home/user
# Sat, 21 Oct 2023 00:28:41 GMT
USER user
# Sat, 21 Oct 2023 00:28:42 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d55fb6504fd81f0e7c6623487aa62c5b78561b01c749beb44a83c29f6b01e14`  
		Last Modified: Sat, 21 Oct 2023 00:28:53 GMT  
		Size: 8.9 MB (8873688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9a2d40b1b5ac6b6bfc84a45386ac82f09a84519bd446a97a77b8a1d2c8e695`  
		Last Modified: Sat, 21 Oct 2023 00:28:51 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17fe7619eb2565acf1133a250e1b9e17ec3f460a5bf0382bad047e42c900f8ac`  
		Last Modified: Sat, 21 Oct 2023 00:28:52 GMT  
		Size: 5.6 MB (5644472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:c6d6d585a6c51b60051f65f9cdc0136bf13f5055b5297b0417b22a2ae3903ca0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16994909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be928507127978ad8b0546cd2d61079dc12cde36fac93cd44b38bfde8da7ab6`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:52:05 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Sat, 21 Oct 2023 00:52:05 GMT
ENV HOME=/home/user
# Sat, 21 Oct 2023 00:52:06 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Sat, 21 Oct 2023 00:52:06 GMT
ENV LANG=C.UTF-8
# Sat, 21 Oct 2023 00:52:06 GMT
ENV IRSSI_VERSION=1.4.5
# Sat, 21 Oct 2023 00:52:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Sat, 21 Oct 2023 00:52:22 GMT
WORKDIR /home/user
# Sat, 21 Oct 2023 00:52:22 GMT
USER user
# Sat, 21 Oct 2023 00:52:22 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc98cc9942c2f26a7b67b5f090312df51352ce21bb480db3089968ef5d931cce`  
		Last Modified: Sat, 21 Oct 2023 00:52:45 GMT  
		Size: 8.7 MB (8713792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd52a443d0cc7fb7c5c805749f6a1b41bc351217144cd216181709f6f8ac77ac`  
		Last Modified: Sat, 21 Oct 2023 00:52:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab1fca5a554797d7d71a56eaa3b77c331d3682ae9452eb5e6ed560e24b32820`  
		Last Modified: Sat, 21 Oct 2023 00:52:44 GMT  
		Size: 5.4 MB (5379926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:8e84ebd4f06676afeeff5d3df76c54b494e9225ad08af34c22405bbb1dfac624
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18715109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4acd348d9659d9e55521ba8e049504b24acb95e989e3c60ef45ce22819d3201c`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 21:57:36 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Thu, 28 Sep 2023 21:57:36 GMT
ENV HOME=/home/user
# Thu, 28 Sep 2023 21:57:36 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Thu, 28 Sep 2023 21:57:36 GMT
ENV LANG=C.UTF-8
# Fri, 06 Oct 2023 18:51:05 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 06 Oct 2023 18:51:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Fri, 06 Oct 2023 18:51:19 GMT
WORKDIR /home/user
# Fri, 06 Oct 2023 18:51:19 GMT
USER user
# Fri, 06 Oct 2023 18:51:19 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb98c09201d772cdbd8ebf3b77e3767ba0112bb407e3fa992d4a5e162065862`  
		Last Modified: Thu, 28 Sep 2023 21:58:15 GMT  
		Size: 9.7 MB (9667003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3eb447534379436f487e6d6e2a8bfe8d3f4a55aaf3e65cd8c162ce04b733398`  
		Last Modified: Thu, 28 Sep 2023 21:58:14 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8285f819417a3875bfc576dd902248316d6bc296fa13316b6e8b1a5193ee0005`  
		Last Modified: Fri, 06 Oct 2023 18:51:59 GMT  
		Size: 5.7 MB (5714992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; 386

```console
$ docker pull irssi@sha256:10a2f7e3da4f7b5d50afd23be8aea339f3d1a4ab0ae47a2b6a712572d1cefdcb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17949812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5521337ea42656e0519d4b176a333f870ff08f83fbe13b36debe39a8317e315`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 28 Sep 2023 20:38:19 GMT
ADD file:8402753f294e403e92353bd65c86a6428c960be5116c0a15484b663a84f66fcd in / 
# Thu, 28 Sep 2023 20:38:20 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 01:13:36 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Sat, 21 Oct 2023 01:13:36 GMT
ENV HOME=/home/user
# Sat, 21 Oct 2023 01:13:36 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Sat, 21 Oct 2023 01:13:37 GMT
ENV LANG=C.UTF-8
# Sat, 21 Oct 2023 01:13:37 GMT
ENV IRSSI_VERSION=1.4.5
# Sat, 21 Oct 2023 01:14:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Sat, 21 Oct 2023 01:14:10 GMT
WORKDIR /home/user
# Sat, 21 Oct 2023 01:14:10 GMT
USER user
# Sat, 21 Oct 2023 01:14:11 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:dc95107ad2a031a015320bb397f73ec151d738127175b31ad643120697dc7e90`  
		Last Modified: Thu, 28 Sep 2023 20:39:32 GMT  
		Size: 3.2 MB (3235757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469f51955af617b8fe3b7664ff5a864bbf719ecb6fa0dc4e96f61b2ccd738a55`  
		Last Modified: Sat, 21 Oct 2023 01:14:37 GMT  
		Size: 8.9 MB (8896532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ac079b8db6bffdb217008552d5f764995b627666a6666ef4acabee2123a7b8`  
		Last Modified: Sat, 21 Oct 2023 01:14:34 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59be0afc275620a1e5b9b87213d6ff7deeedc4c8c9220ce7eb985d5f7a2d79f`  
		Last Modified: Sat, 21 Oct 2023 01:14:36 GMT  
		Size: 5.8 MB (5816238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:dbc320a9086195da2680bc4cf935011676350719e142d546fd6481e19cc54993
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19107908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd39641bdb2a9ab56a6bc7e82024b3b2af490347fd5416cea36ed9aaf094cd9`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 28 Sep 2023 21:22:20 GMT
ADD file:a720acb99214334c501363d564d8cae9b90d062ccf8a24a5ba1c831545b783dd in / 
# Thu, 28 Sep 2023 21:22:21 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:37:49 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Sat, 21 Oct 2023 00:37:50 GMT
ENV HOME=/home/user
# Sat, 21 Oct 2023 00:37:51 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Sat, 21 Oct 2023 00:37:51 GMT
ENV LANG=C.UTF-8
# Sat, 21 Oct 2023 00:37:51 GMT
ENV IRSSI_VERSION=1.4.5
# Sat, 21 Oct 2023 00:38:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Sat, 21 Oct 2023 00:38:09 GMT
WORKDIR /home/user
# Sat, 21 Oct 2023 00:38:09 GMT
USER user
# Sat, 21 Oct 2023 00:38:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cd37f9856024d6685ac0233823aded690551c5872d6a27699a96c6a479d20f6f`  
		Last Modified: Thu, 28 Sep 2023 21:23:43 GMT  
		Size: 3.3 MB (3346508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ffddccb3efcbf8be2ccdc8e955d416138caeb1b6e4ad22c77c70c14c63412e`  
		Last Modified: Sat, 21 Oct 2023 00:38:27 GMT  
		Size: 9.7 MB (9727207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f11b5d5a4ccf174cd360b852e73f56ffd9d3110f56cc3ce1918f33690224d8`  
		Last Modified: Sat, 21 Oct 2023 00:38:25 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be7e1a7f5bc3f5725506aa72399261389527f19d434b1f7aaf6ca1b0f0e39262`  
		Last Modified: Sat, 21 Oct 2023 00:38:26 GMT  
		Size: 6.0 MB (6032907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; s390x

```console
$ docker pull irssi@sha256:193fd7ae38af58ed0b2178ff24e9d2ed3f9743ef85a728d3e884dcb8827853c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19110933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:322879eed395ebe6f64d1550cc35dd1225368e0cf2cb7df129c2b5ea7a34f007`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:33:59 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Sat, 21 Oct 2023 00:34:01 GMT
ENV HOME=/home/user
# Sat, 21 Oct 2023 00:34:01 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Sat, 21 Oct 2023 00:34:01 GMT
ENV LANG=C.UTF-8
# Sat, 21 Oct 2023 00:34:02 GMT
ENV IRSSI_VERSION=1.4.5
# Sat, 21 Oct 2023 00:34:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Sat, 21 Oct 2023 00:34:22 GMT
WORKDIR /home/user
# Sat, 21 Oct 2023 00:34:22 GMT
USER user
# Sat, 21 Oct 2023 00:34:22 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b273a1445581c4c7dea161e850b4a3f620152efa960fbdf99c80bbe7673dc2`  
		Last Modified: Sat, 21 Oct 2023 00:34:49 GMT  
		Size: 10.1 MB (10079030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f26b188f47f68394fc4109ff18407816957aba0cd17288e3bb4b22cd7b157f`  
		Last Modified: Sat, 21 Oct 2023 00:34:47 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc0e23c0b83a3b4eee71e6e3c3912e01d5d4ceb690808bebc4a0f701f2712ad`  
		Last Modified: Sat, 21 Oct 2023 00:34:48 GMT  
		Size: 5.8 MB (5815515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
