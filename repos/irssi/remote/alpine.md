## `irssi:alpine`

```console
$ docker pull irssi@sha256:d499a09763fa3bceaa896e3832af85d6d529dfeda6a3138ddd3f279e22b376bd
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
$ docker pull irssi@sha256:d17bbad47491f5826e8e1525ab8d9b1456d88ff7eed7192ddda3d4b602d3b2ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19053044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0c37fb1f6a602950cfc3b150083d9cfaaeff699af568fc198d295108cb9631`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 May 2022 19:19:30 GMT
ADD file:8e81116368669ed3dd361bc898d61bff249f524139a239fdaf3ec46869a39921 in / 
# Mon, 23 May 2022 19:19:31 GMT
CMD ["/bin/sh"]
# Mon, 13 Jun 2022 19:50:26 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 13 Jun 2022 19:50:27 GMT
ENV HOME=/home/user
# Mon, 13 Jun 2022 19:50:27 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 13 Jun 2022 19:50:27 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 19:31:48 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 19:32:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 18 Jul 2022 19:32:11 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 19:32:11 GMT
USER user
# Mon, 18 Jul 2022 19:32:11 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2408cc74d12b6cd092bb8b516ba7d5e290f485d3eb9672efc00f0583730179e8`  
		Last Modified: Mon, 23 May 2022 19:09:38 GMT  
		Size: 2.8 MB (2798889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a560d9327c7ec9237ffdc0c14fab68c118b3c4f96082cf728bf4adaac758f73`  
		Last Modified: Mon, 13 Jun 2022 19:51:35 GMT  
		Size: 9.6 MB (9635226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5cf8356e2a173d9862dd806bc61eadbd3d3a348a45f1cc5e5b9f142d38d1a8`  
		Last Modified: Mon, 13 Jun 2022 19:51:33 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93210a21a541763580602ab316b52b3dfa5b7caeacc7218480db0a3adb22a4eb`  
		Last Modified: Mon, 18 Jul 2022 19:32:44 GMT  
		Size: 6.6 MB (6617644 bytes)  
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
$ docker pull irssi@sha256:7726b670a7075eb493678469422e169667df6aab527e51cfaa879cda7f5062cc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15814593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64832f2b21baf5ec2006706a9cf25927c0a2a416d508ab5593ece2a7d00c258`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 Jul 2022 21:24:47 GMT
ADD file:68590e866bc6db27ad54d23de7dd275d0389cb86e4e6291a1243fcc234f2f7a1 in / 
# Mon, 18 Jul 2022 21:24:47 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 21:46:46 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 18 Jul 2022 21:46:47 GMT
ENV HOME=/home/user
# Mon, 18 Jul 2022 21:46:49 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 18 Jul 2022 21:46:49 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 21:46:50 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 21:47:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 18 Jul 2022 21:47:14 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 21:47:14 GMT
USER user
# Mon, 18 Jul 2022 21:47:14 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a6b45ace95f42a930d15c33679ab9c85d46019b7e73954cadc73bb9ba176509b`  
		Last Modified: Mon, 18 Jul 2022 19:08:56 GMT  
		Size: 2.4 MB (2412307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9e1dca7051a20a401a3d84f96da71dd867a9ee0e24f1a7f09677de75d53140`  
		Last Modified: Mon, 18 Jul 2022 21:48:15 GMT  
		Size: 8.7 MB (8708216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0f6db8c54d3924f3e78936c4066057027d8b3bd0a10af466cfc216a9ef6d2b`  
		Last Modified: Mon, 18 Jul 2022 21:48:07 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4987ffc8bc6cbb769df4dd941574de6d0a30766e1d35d371c5ed45aeba785b`  
		Last Modified: Mon, 18 Jul 2022 21:48:10 GMT  
		Size: 4.7 MB (4692786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:1a144b7297bd5fa738e4b2c6ccaa92e9cf1ba5d478de7fb7ddd5016784dd6679
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18691044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8b7b441dd2edbe7d661c2a595e94f38063856a7cbef746febef212905735aa`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 May 2022 19:39:22 GMT
ADD file:3ae36c6c4a1fc43157692da97c6c4fa6c3d0189ba82e2bef7f5aaf4a5e083f18 in / 
# Mon, 23 May 2022 19:39:22 GMT
CMD ["/bin/sh"]
# Mon, 13 Jun 2022 20:23:39 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 13 Jun 2022 20:23:39 GMT
ENV HOME=/home/user
# Mon, 13 Jun 2022 20:23:40 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 13 Jun 2022 20:23:41 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 18:49:18 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 18:49:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 18 Jul 2022 18:49:37 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 18:49:38 GMT
USER user
# Mon, 18 Jul 2022 18:49:39 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b3c136eddcbf2003d3180787cef00f39d46b9fd9e4623178282ad6a8d63ad3b0`  
		Last Modified: Mon, 23 May 2022 19:08:34 GMT  
		Size: 2.7 MB (2694464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df0326bfe3101294ae401c713084eba32047bac8d67f9d513ba125184ebdeab`  
		Last Modified: Mon, 13 Jun 2022 20:24:54 GMT  
		Size: 9.6 MB (9614164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab20c2c5fdaab414b403e89ab87d1e9150f146c59a654d908bf59de00754098c`  
		Last Modified: Mon, 13 Jun 2022 20:24:52 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7aab38e8fd1fe53325b3016e80b3373c0212d8ea7b3eee9d35c294a8e658ba5`  
		Last Modified: Mon, 18 Jul 2022 18:50:22 GMT  
		Size: 6.4 MB (6381158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; 386

```console
$ docker pull irssi@sha256:cb377bddeaa0f32f50bec41afb14efa635b8b275cd8dc27d29b9eb84278b07cd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16895156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89892b7d6a7e9cf4b9c20eaddfcfb4b60dfd2d3baf63e25ed682b85da30d9f9b`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 Jul 2022 20:38:19 GMT
ADD file:be69b7550bf861d8fb12bdbe1edf3a0d2519a6a4da61bd04858b6258ffbf48a7 in / 
# Mon, 18 Jul 2022 20:38:19 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 21:22:34 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 18 Jul 2022 21:22:34 GMT
ENV HOME=/home/user
# Mon, 18 Jul 2022 21:22:35 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 18 Jul 2022 21:22:36 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 21:22:37 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 21:22:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 18 Jul 2022 21:22:58 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 21:22:59 GMT
USER user
# Mon, 18 Jul 2022 21:23:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5d7f927419794ebb7496ac38b0659686317b2d2fac7252a4a0d40d43d5fdd662`  
		Last Modified: Mon, 18 Jul 2022 19:09:22 GMT  
		Size: 2.8 MB (2802334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2145e9491f9798ce6ba6a51e68ca96b186ad6ba788f3c69c1b1b154ad56a7e1a`  
		Last Modified: Mon, 18 Jul 2022 21:23:31 GMT  
		Size: 9.0 MB (8992480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d16a63cb4fb487e02f956e04140855533c28e2ee5e908cec5ea8a2468d6da3b`  
		Last Modified: Mon, 18 Jul 2022 21:23:29 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7d0ef11d7b29e8d2ec1207dc213657f05c112333cfe74b1e705a57a4df207e`  
		Last Modified: Mon, 18 Jul 2022 21:23:29 GMT  
		Size: 5.1 MB (5099084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:a9fb5fe7d2690db216626fbe721079fc3876b49c95d65865d6619652afe856da
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19155180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8220eb931b94ed838fab3d87fd63b138a4482392f2f169ca36d5ab9b9e49fc4`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 May 2022 19:16:51 GMT
ADD file:6a5450c8a7cee3ceda59e7cb350c54df4139b0f7b7cf49c8b31bb9c01646c3cd in / 
# Mon, 23 May 2022 19:16:53 GMT
CMD ["/bin/sh"]
# Mon, 13 Jun 2022 23:14:25 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 13 Jun 2022 23:14:43 GMT
ENV HOME=/home/user
# Mon, 13 Jun 2022 23:14:54 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 13 Jun 2022 23:14:56 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 21:06:01 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 21:06:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 18 Jul 2022 21:06:49 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 21:06:52 GMT
USER user
# Mon, 18 Jul 2022 21:06:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d3deabf2a506ef6f5fa7c2a68bf27047574cef9908b30a97ff2d01ae539b089a`  
		Last Modified: Mon, 23 May 2022 19:09:13 GMT  
		Size: 2.8 MB (2789745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add35b7a4f86cc3945395519a210218c4dba779c4156808a76c67f2b6e20d3cb`  
		Last Modified: Mon, 13 Jun 2022 23:16:38 GMT  
		Size: 9.7 MB (9719680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bec80f7d521a91ee5a34b351f337e96c9f4deca03a7aafa190942d7a04cb536`  
		Last Modified: Mon, 13 Jun 2022 23:16:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22bf4aba5775615ee4073b98fabef759a96d576461a19b3f231ebc3e12edf9f1`  
		Last Modified: Mon, 18 Jul 2022 21:07:54 GMT  
		Size: 6.6 MB (6644469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; s390x

```console
$ docker pull irssi@sha256:c951571e9f532032314e8dbc4a27642e5aa5d4f8b8aac1cc46f32e03753765b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (19000975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c5f065bd013fd4e025ddf2c4b3a96f0cf81f8dc3f9f1de5179a9bd76e5769c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 May 2022 19:41:59 GMT
ADD file:e1852d8ef555a0d3ef6d0b74a898720c82bb9f491430b06a0dd0499497ce118e in / 
# Mon, 23 May 2022 19:42:10 GMT
CMD ["/bin/sh"]
# Mon, 13 Jun 2022 20:37:11 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 13 Jun 2022 20:37:12 GMT
ENV HOME=/home/user
# Mon, 13 Jun 2022 20:37:13 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 13 Jun 2022 20:37:13 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 19:50:49 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 19:51:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 18 Jul 2022 19:51:21 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 19:51:22 GMT
USER user
# Mon, 18 Jul 2022 19:51:23 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:af1ac1a73384e058591d04d19bc05a06781cc32d52d4593b468d6cb95eda9858`  
		Last Modified: Mon, 23 May 2022 19:43:36 GMT  
		Size: 2.6 MB (2580494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8ce5afc179fecb50a185a15e9da7fadbb998c0a176a3184c2a469300a0e6ed`  
		Last Modified: Mon, 13 Jun 2022 20:38:25 GMT  
		Size: 10.1 MB (10054673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f78014fdf3530a88cb1fcb23f00ec5d13af184e82e7a1ff33579e22002c0a78`  
		Last Modified: Mon, 13 Jun 2022 20:38:23 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81162e071b28adcf3e33286dadab246430966b16d6f65e177cc0ccd912cb810d`  
		Last Modified: Mon, 18 Jul 2022 19:52:07 GMT  
		Size: 6.4 MB (6364524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
