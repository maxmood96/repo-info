## `irssi:alpine`

```console
$ docker pull irssi@sha256:b1f71ebbcc60cfe347d5ff10c892daf15e33660dbb4970d416d7ea9ca9463562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `irssi:alpine` - linux; amd64

```console
$ docker pull irssi@sha256:6f155185a9910969212aaa20048910405c719366e2a96066a673d63f2ff8dfb9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18636192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5e01025e17df3698ef23de49fcab9568d7136952e0cca39cf883603971b272`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 28 Jan 2021 23:19:38 GMT
ADD file:0e2d487cd80773e947c8aae6daad3d565b7bb019a954af2b8bff188681c00d81 in / 
# Thu, 28 Jan 2021 23:19:38 GMT
CMD ["/bin/sh"]
# Fri, 12 Feb 2021 02:21:49 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Fri, 12 Feb 2021 02:21:49 GMT
ENV HOME=/home/user
# Fri, 12 Feb 2021 02:21:50 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Fri, 12 Feb 2021 02:21:50 GMT
ENV LANG=C.UTF-8
# Fri, 12 Feb 2021 02:21:50 GMT
ENV IRSSI_VERSION=1.2.2
# Fri, 12 Feb 2021 02:22:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		automake 		coreutils 		dpkg-dev dpkg 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		make 		ncurses-dev 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-true-color 		--with-bot 		--with-proxy 		--with-socks 	; 	make -j "$(nproc)"; 	make install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Fri, 12 Feb 2021 02:22:43 GMT
WORKDIR /home/user
# Fri, 12 Feb 2021 02:22:43 GMT
USER user
# Fri, 12 Feb 2021 02:22:44 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4c0d98bf9879488e0407f897d9dd4bf758555a78e39675e72b5124ccf12c2580`  
		Last Modified: Thu, 28 Jan 2021 23:20:08 GMT  
		Size: 2.8 MB (2811321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e9195ef07e8ce96840069ea52b95743ba4e95c933b6c5aafc91148fb4721f44`  
		Last Modified: Fri, 12 Feb 2021 02:23:03 GMT  
		Size: 9.5 MB (9546138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d8535849319e138c31afbe4b9cb3d1b7d68f972783f0eae615623b4f590261`  
		Last Modified: Fri, 12 Feb 2021 02:23:01 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5e2e93832b2db8f3b88719edc11ed0375635931b550d8be30680601dd4d2ef`  
		Last Modified: Fri, 12 Feb 2021 02:23:02 GMT  
		Size: 6.3 MB (6277489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:1f5c7f3acf830fde5a0b1b2a03c8d4c241c16f80075fa9354eee2fedcda705e7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17380720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71696b9d35a21e30b8716ccac8b96700bd5f52f029875b05bbae25c07cf2482a`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:24:35 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Wed, 17 Feb 2021 21:24:36 GMT
ENV HOME=/home/user
# Wed, 17 Feb 2021 21:24:39 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Wed, 17 Feb 2021 21:24:40 GMT
ENV LANG=C.UTF-8
# Wed, 17 Feb 2021 21:24:41 GMT
ENV IRSSI_VERSION=1.2.2
# Wed, 17 Feb 2021 21:25:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		automake 		coreutils 		dpkg-dev dpkg 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		make 		ncurses-dev 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-true-color 		--with-bot 		--with-proxy 		--with-socks 	; 	make -j "$(nproc)"; 	make install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Wed, 17 Feb 2021 21:25:34 GMT
WORKDIR /home/user
# Wed, 17 Feb 2021 21:25:35 GMT
USER user
# Wed, 17 Feb 2021 21:25:36 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ff4c5d9d970b7aea5a3154a048a8dffdecaa2ba25b1ca324fe17c97846b341`  
		Last Modified: Wed, 17 Feb 2021 21:25:58 GMT  
		Size: 8.8 MB (8779079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762491e3840e0e26a34e0b701ff53443ad7810f8597293077dc34d419566d287`  
		Last Modified: Wed, 17 Feb 2021 21:25:54 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8ff637f1f0558e9446a89673d71ef57ac31f70c30723de693a929ae08bef99`  
		Last Modified: Wed, 17 Feb 2021 21:25:56 GMT  
		Size: 6.0 MB (5978332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:98e9d26dba6b9d04ea95eb1c4db163a2e49b7f382231f090c359f4a2e62c0bb9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16827140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7008468a20016e3e36be26bfef0107ff0772b2b1cb411175dbd3ff7ce17ccfc`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:56:44 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Wed, 17 Feb 2021 21:56:46 GMT
ENV HOME=/home/user
# Wed, 17 Feb 2021 21:57:09 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Wed, 17 Feb 2021 21:57:15 GMT
ENV LANG=C.UTF-8
# Wed, 17 Feb 2021 21:57:19 GMT
ENV IRSSI_VERSION=1.2.2
# Wed, 17 Feb 2021 21:59:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		automake 		coreutils 		dpkg-dev dpkg 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		make 		ncurses-dev 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-true-color 		--with-bot 		--with-proxy 		--with-socks 	; 	make -j "$(nproc)"; 	make install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Wed, 17 Feb 2021 21:59:18 GMT
WORKDIR /home/user
# Wed, 17 Feb 2021 21:59:22 GMT
USER user
# Wed, 17 Feb 2021 21:59:27 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2fd61c3640b29fa2c56636a6beaba35f3feeaccdc0aa8f1b840d41e57d6567b`  
		Last Modified: Wed, 17 Feb 2021 22:00:02 GMT  
		Size: 8.6 MB (8630384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a207f2622f75244aef8808929a788c81bf2275a3a71b65b250ff28d176b528`  
		Last Modified: Wed, 17 Feb 2021 21:59:55 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38dc3cd80a9a70577dd247b0106d4642e934647618cbdde5dbd869111220070d`  
		Last Modified: Wed, 17 Feb 2021 22:00:02 GMT  
		Size: 5.8 MB (5771592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:3b9041124ac4d90b6fca2a0b7e2394b45dbc395bad1dba33697706f602368083
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18483592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e478282eb524a3206e9cc38f551d08878bcec7cab3eaf0c0e26371dd284e40`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 28 Jan 2021 23:39:33 GMT
ADD file:fecabe41deaeb72acdd63023566d87ae48b013ef80c97fdd993b55d6c727da93 in / 
# Thu, 28 Jan 2021 23:39:34 GMT
CMD ["/bin/sh"]
# Fri, 12 Feb 2021 02:42:59 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Fri, 12 Feb 2021 02:43:01 GMT
ENV HOME=/home/user
# Fri, 12 Feb 2021 02:43:03 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Fri, 12 Feb 2021 02:43:04 GMT
ENV LANG=C.UTF-8
# Fri, 12 Feb 2021 02:43:05 GMT
ENV IRSSI_VERSION=1.2.2
# Fri, 12 Feb 2021 02:43:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		automake 		coreutils 		dpkg-dev dpkg 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		make 		ncurses-dev 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-true-color 		--with-bot 		--with-proxy 		--with-socks 	; 	make -j "$(nproc)"; 	make install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Fri, 12 Feb 2021 02:43:53 GMT
WORKDIR /home/user
# Fri, 12 Feb 2021 02:43:53 GMT
USER user
# Fri, 12 Feb 2021 02:43:54 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2914792bc417803b2106001990194cc00cdd4b6fd97cd21a368f26148bc8e722`  
		Last Modified: Thu, 28 Jan 2021 23:40:10 GMT  
		Size: 2.7 MB (2711261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1472be30a9c004f7572fa2ea158640b79968100f2315d8e360aa93af7e0ac6ec`  
		Last Modified: Fri, 12 Feb 2021 02:44:16 GMT  
		Size: 9.5 MB (9542244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be9ff8abf426fb845619acdb1a33f5eb5e350caa2cf190408b1ef8e0b24fc5c`  
		Last Modified: Fri, 12 Feb 2021 02:44:13 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:166c8668e79dc504a5684693fd3b134639984128b42a0773f2fa5cd9e232698a`  
		Last Modified: Fri, 12 Feb 2021 02:44:14 GMT  
		Size: 6.2 MB (6228816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; 386

```console
$ docker pull irssi@sha256:3eb3e9d9632f9141e74c26a33e48d845c1c6d125db99aba5e822698f8f6bbc69
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17696674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5218d4e5fa8450c7411955b9ba93511e93b2eacc878b57a8159a04a169191fa7`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 28 Jan 2021 23:38:31 GMT
ADD file:c0e9ea135d66ad6504c77915a7a48b3bead60892d155d3258b746cb4945981c0 in / 
# Thu, 28 Jan 2021 23:38:31 GMT
CMD ["/bin/sh"]
# Fri, 12 Feb 2021 02:40:53 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Fri, 12 Feb 2021 02:40:53 GMT
ENV HOME=/home/user
# Fri, 12 Feb 2021 02:40:54 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Fri, 12 Feb 2021 02:40:54 GMT
ENV LANG=C.UTF-8
# Fri, 12 Feb 2021 02:40:54 GMT
ENV IRSSI_VERSION=1.2.2
# Fri, 12 Feb 2021 02:41:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		automake 		coreutils 		dpkg-dev dpkg 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		make 		ncurses-dev 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-true-color 		--with-bot 		--with-proxy 		--with-socks 	; 	make -j "$(nproc)"; 	make install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Fri, 12 Feb 2021 02:41:54 GMT
WORKDIR /home/user
# Fri, 12 Feb 2021 02:41:54 GMT
USER user
# Fri, 12 Feb 2021 02:41:54 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3fea00a81341ce917db671eb3ad24ef5750cb6928b7f760e3ce4dab619eeb1fa`  
		Last Modified: Thu, 28 Jan 2021 23:39:02 GMT  
		Size: 2.8 MB (2817627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e2567f275f1580b3a666d72f9fd68f0624463b51d3efb4d0ca32220140480f`  
		Last Modified: Fri, 12 Feb 2021 02:42:19 GMT  
		Size: 8.9 MB (8912699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1cf744978f6b257e75f0d9f8d485cc009c002a68fbfd09d2c86682e295a55ca`  
		Last Modified: Fri, 12 Feb 2021 02:42:15 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c24e57c1812de51612f3a7d46b191b5335b7aa8c7453d615fc0aa626654737`  
		Last Modified: Fri, 12 Feb 2021 02:42:22 GMT  
		Size: 6.0 MB (5965103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:d311dab78fc85b3da27d037bd147a456f46668231c4e1638a68791a6583803e9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18936606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d89ab620811ed1d73742b91c14b60c97ba0792d521e62ac8c2e60362356a222`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 28 Jan 2021 23:55:50 GMT
ADD file:b14fd5f3f7fcd16e2b4ec6932d3e9c07c7400c577cee5fdcb88b0795a70a7bfb in / 
# Thu, 28 Jan 2021 23:55:52 GMT
CMD ["/bin/sh"]
# Fri, 12 Feb 2021 02:22:51 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Fri, 12 Feb 2021 02:22:57 GMT
ENV HOME=/home/user
# Fri, 12 Feb 2021 02:23:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Fri, 12 Feb 2021 02:23:20 GMT
ENV LANG=C.UTF-8
# Fri, 12 Feb 2021 02:23:28 GMT
ENV IRSSI_VERSION=1.2.2
# Fri, 12 Feb 2021 02:24:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		automake 		coreutils 		dpkg-dev dpkg 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		make 		ncurses-dev 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-true-color 		--with-bot 		--with-proxy 		--with-socks 	; 	make -j "$(nproc)"; 	make install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Fri, 12 Feb 2021 02:24:38 GMT
WORKDIR /home/user
# Fri, 12 Feb 2021 02:24:41 GMT
USER user
# Fri, 12 Feb 2021 02:24:47 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f3b94a1d8d591af02f1b419642bee91066ecbb9c65099d6903deed310fd1c2ff`  
		Last Modified: Thu, 28 Jan 2021 23:56:32 GMT  
		Size: 2.8 MB (2812517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1350879e766a79b2700ba308c8723d6062ba50e73770b955b3c7eaa85d71f0c4`  
		Last Modified: Fri, 12 Feb 2021 02:25:16 GMT  
		Size: 9.6 MB (9642136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d400834332386f797f1b7d0efbb74ccf52781cf43800e6d216531c559034030`  
		Last Modified: Fri, 12 Feb 2021 02:25:14 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8df220e5e651e0e7237d472b3e06378faf13942fc99a530aeaf5a827cec8d3`  
		Last Modified: Fri, 12 Feb 2021 02:25:15 GMT  
		Size: 6.5 MB (6480679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; s390x

```console
$ docker pull irssi@sha256:bb161a5f89c42d7993ae06e05469df5c2eedbb3dca696493e7c99b92c8ec514e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18849592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f41bb9023f99c5f41ab97ed1136f66f1ae78bdd04af43579ed469d90316ba0`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 21:45:50 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Wed, 17 Feb 2021 21:45:53 GMT
ENV HOME=/home/user
# Wed, 17 Feb 2021 21:45:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Wed, 17 Feb 2021 21:45:56 GMT
ENV LANG=C.UTF-8
# Wed, 17 Feb 2021 21:45:56 GMT
ENV IRSSI_VERSION=1.2.2
# Wed, 17 Feb 2021 21:47:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		automake 		coreutils 		dpkg-dev dpkg 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		make 		ncurses-dev 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-true-color 		--with-bot 		--with-proxy 		--with-socks 	; 	make -j "$(nproc)"; 	make install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Wed, 17 Feb 2021 21:47:19 GMT
WORKDIR /home/user
# Wed, 17 Feb 2021 21:47:20 GMT
USER user
# Wed, 17 Feb 2021 21:47:20 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431c6777b2e72ebd239ef29f3af5bf3d5a0e20ef56f8555bd1d6755fafc88ffd`  
		Last Modified: Wed, 17 Feb 2021 21:47:46 GMT  
		Size: 10.0 MB (9983485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77dd0d64dafd0e587a28096db40881c63cf90c507b5d3ef6ad95545c2802949e`  
		Last Modified: Wed, 17 Feb 2021 21:47:43 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d3dfea215a6802694908be57e3e737fe63e9897a13f70f22007fd537cf50351`  
		Last Modified: Wed, 17 Feb 2021 21:47:45 GMT  
		Size: 6.3 MB (6262456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
