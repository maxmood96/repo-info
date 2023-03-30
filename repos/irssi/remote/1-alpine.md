## `irssi:1-alpine`

```console
$ docker pull irssi@sha256:8dd7df30d2df3e05cc51f37e54da2e8967f29e6a50d9cbaf883beeeba870b555
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

### `irssi:1-alpine` - linux; amd64

```console
$ docker pull irssi@sha256:082299a485cd735ffb5f076ccac5b76b016ea8146cca12cf0e80d52f953d6e4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17472871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b264b3e317b214d1ec23e3c608baf1e7a2558cee564c13710b42752735a4741`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:28 GMT
ADD file:970e6b2578ef73457ffed1189e8ba128b0211cabd3174b8c7d3afd8fb58ad614 in / 
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 22:03:34 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Wed, 29 Mar 2023 22:03:34 GMT
ENV HOME=/home/user
# Wed, 29 Mar 2023 22:03:34 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Wed, 29 Mar 2023 22:03:34 GMT
ENV LANG=C.UTF-8
# Wed, 29 Mar 2023 22:03:34 GMT
ENV IRSSI_VERSION=1.4.3
# Wed, 29 Mar 2023 22:03:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Wed, 29 Mar 2023 22:03:55 GMT
WORKDIR /home/user
# Wed, 29 Mar 2023 22:03:55 GMT
USER user
# Wed, 29 Mar 2023 22:03:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:91d30c5bc19582de1415b18f1ec5bcbf52a558b62cf6cc201c9669df9f748c22`  
		Last Modified: Wed, 29 Mar 2023 18:20:09 GMT  
		Size: 2.8 MB (2807803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09911801585d7e9189254b5d98e67a35a8209f226a67e6174b94d432307d820e`  
		Last Modified: Wed, 29 Mar 2023 22:04:11 GMT  
		Size: 9.6 MB (9641385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af57762370f3d2cb5399208d23f4d32cb3b197241654b4061c46ed30fcdd6a07`  
		Last Modified: Wed, 29 Mar 2023 22:04:09 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498d38f93729936ba60894a2040cb31e4f127ea13203a386bfbcc306bccd04c9`  
		Last Modified: Wed, 29 Mar 2023 22:04:10 GMT  
		Size: 5.0 MB (5022398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:b8699e2c266aa530cf7c4886d0f059db07f0aa53342b0fce36f43c7a407ffc33
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16404172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8304e45668335f402b2b6a4d3e53eaf181eecaa98abf4b72f58cc7bf02261d0`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:11 GMT
ADD file:c5e68ad58a515830d33f20488adffa6af47be2e332543c747b8931cab7444e59 in / 
# Wed, 29 Mar 2023 18:01:11 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:25:08 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Wed, 29 Mar 2023 19:25:09 GMT
ENV HOME=/home/user
# Wed, 29 Mar 2023 19:25:09 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Wed, 29 Mar 2023 19:25:09 GMT
ENV LANG=C.UTF-8
# Wed, 29 Mar 2023 19:25:09 GMT
ENV IRSSI_VERSION=1.4.3
# Wed, 29 Mar 2023 19:25:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Wed, 29 Mar 2023 19:25:28 GMT
WORKDIR /home/user
# Wed, 29 Mar 2023 19:25:29 GMT
USER user
# Wed, 29 Mar 2023 19:25:29 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c4ddbcc13e08e4ef30f810d8afad41fd6994bd8af7d37746d0ea33d8813968fc`  
		Last Modified: Wed, 29 Mar 2023 18:02:04 GMT  
		Size: 2.6 MB (2616846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb605cb2a45e966965b577a4ea07f18a5a8579d7ae173449829f2b2d876b8d4`  
		Last Modified: Wed, 29 Mar 2023 19:25:43 GMT  
		Size: 8.9 MB (8871530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce8e2ffac3a746e7f6c45a65deca675e539e8b259af541e753766a377cb02b3`  
		Last Modified: Wed, 29 Mar 2023 19:25:41 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d922509de6a17dd6c080db072603d096847433dafac7f8eced51c4eee97a5595`  
		Last Modified: Wed, 29 Mar 2023 19:25:42 GMT  
		Size: 4.9 MB (4914511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:6bb805ba06aeef2aa80a48293f9b2d9f511c01bd2d7df583e7722cdf3084cc85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15833303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c59bfea79874dbb3be9383225c28a5a6a9322c1549a067406039f282bd9fa8`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 29 Mar 2023 18:04:21 GMT
ADD file:68992157dbe7c3a454c26656c7bcb497794c1008ead5e078b2928ce165cd65cd in / 
# Wed, 29 Mar 2023 18:04:21 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:20:08 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Wed, 29 Mar 2023 19:20:08 GMT
ENV HOME=/home/user
# Wed, 29 Mar 2023 19:20:08 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Wed, 29 Mar 2023 19:20:09 GMT
ENV LANG=C.UTF-8
# Wed, 29 Mar 2023 19:20:09 GMT
ENV IRSSI_VERSION=1.4.3
# Wed, 29 Mar 2023 19:20:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Wed, 29 Mar 2023 19:20:26 GMT
WORKDIR /home/user
# Wed, 29 Mar 2023 19:20:26 GMT
USER user
# Wed, 29 Mar 2023 19:20:27 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d378ffb313542b797defad9ec843de710c353f40e17e124e74f7e874971429ee`  
		Last Modified: Wed, 29 Mar 2023 18:07:08 GMT  
		Size: 2.4 MB (2420546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b48f1c39711cf0fd4070d46a27cb283604416e2c2191ab32eef0320144afe6d`  
		Last Modified: Wed, 29 Mar 2023 19:22:38 GMT  
		Size: 8.7 MB (8718311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f05b4fa9e9a55db72158c5b49091b7577235330d765a8512049ad668afa137`  
		Last Modified: Wed, 29 Mar 2023 19:22:36 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc5851d93e0e2d33fc8a601b37d399ef36c53af07009634a7de320c8da8ca1e`  
		Last Modified: Wed, 29 Mar 2023 19:22:37 GMT  
		Size: 4.7 MB (4693166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:bf5c28cc6a74de11b27e0da808cbe01c369ddfacb14139d1406104a1d6781605
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17241651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d155a800c057aeb27e81980fd04b43643ae812c21702c5d822dbf9101b08d31`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:20 GMT
ADD file:a6a2f69b60d7d27bc6e2b9b7e9910dabdc3f5e3702c2345d26a7dc8c603ae595 in / 
# Wed, 29 Mar 2023 17:39:20 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 05:52:35 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Thu, 30 Mar 2023 05:52:35 GMT
ENV HOME=/home/user
# Thu, 30 Mar 2023 05:52:35 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Thu, 30 Mar 2023 05:52:36 GMT
ENV LANG=C.UTF-8
# Thu, 30 Mar 2023 05:52:36 GMT
ENV IRSSI_VERSION=1.4.3
# Thu, 30 Mar 2023 05:52:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Thu, 30 Mar 2023 05:52:50 GMT
WORKDIR /home/user
# Thu, 30 Mar 2023 05:52:50 GMT
USER user
# Thu, 30 Mar 2023 05:52:50 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:547446be3368f442c50ff95e2a2a9c85110b6b41bbb3c75b7e5ebb115f478b57`  
		Last Modified: Wed, 29 Mar 2023 17:39:56 GMT  
		Size: 2.7 MB (2709344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078f62fc1f9e697de935d5e85459800e062a59191dff048cbfab6756a49088e1`  
		Last Modified: Thu, 30 Mar 2023 05:53:02 GMT  
		Size: 9.6 MB (9623573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16144b670351984e90b29eb764f1123de310a42ed40bdc8561f01e0ddc4b972b`  
		Last Modified: Thu, 30 Mar 2023 05:53:00 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c017955d3479154eb941c70645b33bc3962953f5c04ec5d2a174b8ed83fe102d`  
		Last Modified: Thu, 30 Mar 2023 05:53:01 GMT  
		Size: 4.9 MB (4907451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1-alpine` - linux; 386

```console
$ docker pull irssi@sha256:55299f002323bde689f031a549a0412f5e005964d7a3037114adeb2d54f5715f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16916717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf51c85b6714acbe05b212aff5536baa26893df1d621fe7d721572422eae0133`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:33 GMT
ADD file:c9d37b1a7eee54b1a8c1ebde284829510ec289f7b7db2c16059b26f01b416fe0 in / 
# Wed, 29 Mar 2023 17:38:33 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:18:50 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Wed, 29 Mar 2023 19:18:50 GMT
ENV HOME=/home/user
# Wed, 29 Mar 2023 19:18:51 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Wed, 29 Mar 2023 19:18:51 GMT
ENV LANG=C.UTF-8
# Wed, 29 Mar 2023 19:18:51 GMT
ENV IRSSI_VERSION=1.4.3
# Wed, 29 Mar 2023 19:19:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Wed, 29 Mar 2023 19:19:31 GMT
WORKDIR /home/user
# Wed, 29 Mar 2023 19:19:31 GMT
USER user
# Wed, 29 Mar 2023 19:19:31 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:dea45757091f21722aec41fb20845e57a04f4bb8c199531491f1dc070480a574`  
		Last Modified: Wed, 29 Mar 2023 17:39:11 GMT  
		Size: 2.8 MB (2810814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c42f84a04453ba7baeca135a7a645e355dc290e25fc6e660419fa9eb718951a`  
		Last Modified: Wed, 29 Mar 2023 19:19:53 GMT  
		Size: 9.0 MB (9004215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf75b313960f16ab6a3bab768ba24f9e771f088acd1f4276154ab8ecd32d29d`  
		Last Modified: Wed, 29 Mar 2023 19:19:50 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511d3db68bb9e82b26086ac8aa74d208389376615383213ec7900b95f718b1e2`  
		Last Modified: Wed, 29 Mar 2023 19:19:51 GMT  
		Size: 5.1 MB (5100405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:2f852e0291e1f539f4c104b145a0aeecd9d3d019187dde7c984e0f97f7b4726b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17655487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8aac49ed0c02d21090c9fcba965943b2cb91f0c09083172da64a4b1a0606fd`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 29 Mar 2023 18:16:34 GMT
ADD file:00a20a25a46ff8ebd9bc78b5b8c6fc5b1dc8ae73d5a42048fa5769a2b2e717c7 in / 
# Wed, 29 Mar 2023 18:16:34 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 05:45:28 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Thu, 30 Mar 2023 05:45:29 GMT
ENV HOME=/home/user
# Thu, 30 Mar 2023 05:45:30 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Thu, 30 Mar 2023 05:45:30 GMT
ENV LANG=C.UTF-8
# Thu, 30 Mar 2023 05:45:31 GMT
ENV IRSSI_VERSION=1.4.3
# Thu, 30 Mar 2023 05:45:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Thu, 30 Mar 2023 05:45:58 GMT
WORKDIR /home/user
# Thu, 30 Mar 2023 05:45:58 GMT
USER user
# Thu, 30 Mar 2023 05:45:58 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d80736dee7a63492583c90bab1ab07f987ed5e10dfb16fd3f025df3a2d65f1c6`  
		Last Modified: Wed, 29 Mar 2023 18:17:28 GMT  
		Size: 2.8 MB (2804670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7d43ca3ca18a4d576b046189e40c553ea031abdb6f5e2f9f01d2c17daf6b32`  
		Last Modified: Thu, 30 Mar 2023 05:46:21 GMT  
		Size: 9.7 MB (9733846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecd438304f642334eadc75edbe6e60a4f8eec5c73d1d6f6244e7d901dffb6849`  
		Last Modified: Thu, 30 Mar 2023 05:46:18 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f4355b262c288c59e205e3a5257a83ee4b9844f42a30c0b9b6ef26c5fbcac2`  
		Last Modified: Thu, 30 Mar 2023 05:46:19 GMT  
		Size: 5.1 MB (5115688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:2e60e6e239481450d54db34d86510c666412f2707203f468e64352ffe3e9beea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17704051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c9949e1344fe9af302ed763b04ad9d1fca84e80dd4f0b6455115f95461bd62`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 29 Mar 2023 17:42:02 GMT
ADD file:6c3b2d8f192a3a12e6df8bc7130bbc723b1a39aa71809d23b15cf80bc5135096 in / 
# Wed, 29 Mar 2023 17:42:02 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 18:47:06 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Wed, 29 Mar 2023 18:47:07 GMT
ENV HOME=/home/user
# Wed, 29 Mar 2023 18:47:07 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Wed, 29 Mar 2023 18:47:07 GMT
ENV LANG=C.UTF-8
# Wed, 29 Mar 2023 18:47:07 GMT
ENV IRSSI_VERSION=1.4.3
# Wed, 29 Mar 2023 18:47:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Wed, 29 Mar 2023 18:47:29 GMT
WORKDIR /home/user
# Wed, 29 Mar 2023 18:47:30 GMT
USER user
# Wed, 29 Mar 2023 18:47:30 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:95cbbfdf0c760cbcde91603c8eee15ec60d4aa5f874b4a538babcd2df1709174`  
		Last Modified: Wed, 29 Mar 2023 17:42:37 GMT  
		Size: 2.6 MB (2593389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c03195f7041f32a296c69af1282b626f998bc2dbefe179029374aba4b33a8e`  
		Last Modified: Wed, 29 Mar 2023 18:47:51 GMT  
		Size: 10.1 MB (10079011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144be28453822317c17c0cb1711ca490599a6e30f212d0c3aa3d8f59f45091f6`  
		Last Modified: Wed, 29 Mar 2023 18:47:49 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f976c958bb772c9bb3bb1e4c6c9d983ee4a8553b914ddf4985106426914139bb`  
		Last Modified: Wed, 29 Mar 2023 18:47:50 GMT  
		Size: 5.0 MB (5030367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
