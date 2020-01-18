## `irssi:alpine`

```console
$ docker pull irssi@sha256:c931767a16efd36378129640a7a6462c93d907acd674c8633146c50b5cfe4e78
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
$ docker pull irssi@sha256:d498b383253d36eb8d5564b9003784807bf61a6c95f5f5efea9a8a1ca53db813
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20839887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef7ddf5fad77d0cbc4d848089a74098336df710d119fc9059bbd8199ca38d36`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 24 Dec 2019 19:20:12 GMT
ADD file:36fdc8cb08228a87093fb227736f4ce1d4d6c15366326dea541fbbd863976ee5 in / 
# Tue, 24 Dec 2019 19:20:12 GMT
CMD ["/bin/sh"]
# Mon, 30 Dec 2019 22:21:11 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 30 Dec 2019 22:21:11 GMT
ENV HOME=/home/user
# Mon, 30 Dec 2019 22:21:12 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 30 Dec 2019 22:21:12 GMT
ENV LANG=C.UTF-8
# Mon, 30 Dec 2019 22:21:12 GMT
ENV IRSSI_VERSION=1.2.2
# Mon, 30 Dec 2019 22:21:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		automake 		coreutils 		dpkg-dev dpkg 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		make 		ncurses-dev 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-true-color 		--with-bot 		--with-proxy 		--with-socks 	; 	make -j "$(nproc)"; 	make install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 30 Dec 2019 22:21:55 GMT
WORKDIR /home/user
# Mon, 30 Dec 2019 22:21:55 GMT
USER user
# Mon, 30 Dec 2019 22:21:56 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e6b0cf9c0882fb079c9d35361d12ff4691f916b6d825061247d1bd0b26d7cf3f`  
		Last Modified: Tue, 24 Dec 2019 19:20:40 GMT  
		Size: 2.8 MB (2801778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02efda7cb3f2ba7e78335ff88f8af0583f3d7bd83d881203400353fd4e7d1aad`  
		Last Modified: Mon, 30 Dec 2019 22:22:18 GMT  
		Size: 9.4 MB (9422617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:763a8f604cd845bfe10ad1e1d26d0a495af238989879d28ad31bbbbf97c841df`  
		Last Modified: Mon, 30 Dec 2019 22:22:16 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e9ea64f8456d0e5858d10d08b5232c1278cd14d564b88ac279cef7ddd454dd7`  
		Last Modified: Mon, 30 Dec 2019 22:22:18 GMT  
		Size: 8.6 MB (8614252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:342b2c19ea74b251a8c406ff065393a1826ac54052946813237158beea60ddfb
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19363564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9260d7ed17bd0aa35c4da740d6f224880fcc65b175e242e816b586e973b33db0`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 24 Dec 2019 18:49:41 GMT
ADD file:c4f944e24d0f2e758363506e8b98b3b53973ec18dd4dd23da3f09520ef22c65c in / 
# Tue, 24 Dec 2019 18:49:42 GMT
CMD ["/bin/sh"]
# Mon, 30 Dec 2019 22:50:56 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 30 Dec 2019 22:51:02 GMT
ENV HOME=/home/user
# Mon, 30 Dec 2019 22:51:08 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 30 Dec 2019 22:51:10 GMT
ENV LANG=C.UTF-8
# Mon, 30 Dec 2019 22:51:13 GMT
ENV IRSSI_VERSION=1.2.2
# Mon, 30 Dec 2019 22:52:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		automake 		coreutils 		dpkg-dev dpkg 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		make 		ncurses-dev 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-true-color 		--with-bot 		--with-proxy 		--with-socks 	; 	make -j "$(nproc)"; 	make install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 30 Dec 2019 22:52:18 GMT
WORKDIR /home/user
# Mon, 30 Dec 2019 22:52:19 GMT
USER user
# Mon, 30 Dec 2019 22:52:19 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:546eec1e02ac5f4494868d8b22e8ced00773a2fba8e25b3edd30002889874299`  
		Last Modified: Tue, 24 Dec 2019 18:50:07 GMT  
		Size: 2.6 MB (2612021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e096f7e647acbccc301b850346b30db145dbc810757f233bbd4b9203c86d77a1`  
		Last Modified: Mon, 30 Dec 2019 22:52:36 GMT  
		Size: 8.7 MB (8665185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e252d91ac1eeb24eda441bc7025af739933267533fccbb1f5aca50534a8536`  
		Last Modified: Mon, 30 Dec 2019 22:52:32 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a7f820d727394e1780cfbc82d9c6cbb3b358c303cc6374fdf02405a913329b`  
		Last Modified: Mon, 30 Dec 2019 22:52:35 GMT  
		Size: 8.1 MB (8085085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:5323826e1334be7f0aa23dd153c0a9027eda69db5e37680e91190d9a7fbffdaf
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18734230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd1c12aeeb43dc43b9c31e0bd6108d283edb34f70c5d74b0c48c0af2f8dd92c3`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 24 Dec 2019 18:59:09 GMT
ADD file:caf7ca25875eddd2bfa2d1e56663bb52d278a85f6ee1314f9ccf01dc4da8070a in / 
# Tue, 24 Dec 2019 18:59:10 GMT
CMD ["/bin/sh"]
# Mon, 30 Dec 2019 23:04:54 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 30 Dec 2019 23:04:56 GMT
ENV HOME=/home/user
# Mon, 30 Dec 2019 23:04:58 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 30 Dec 2019 23:04:59 GMT
ENV LANG=C.UTF-8
# Mon, 30 Dec 2019 23:04:59 GMT
ENV IRSSI_VERSION=1.2.2
# Mon, 30 Dec 2019 23:05:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		automake 		coreutils 		dpkg-dev dpkg 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		make 		ncurses-dev 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-true-color 		--with-bot 		--with-proxy 		--with-socks 	; 	make -j "$(nproc)"; 	make install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 30 Dec 2019 23:05:41 GMT
WORKDIR /home/user
# Mon, 30 Dec 2019 23:05:41 GMT
USER user
# Mon, 30 Dec 2019 23:05:42 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3922e475e500b2739b5e74787fc80622853325822f71f8bd3de7e5b09654d60f`  
		Last Modified: Tue, 24 Dec 2019 18:59:33 GMT  
		Size: 2.4 MB (2416691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4247b9ca99628bec17c3dd6184c29f6c8317ecc6882147a77dff862db7e444f`  
		Last Modified: Mon, 30 Dec 2019 23:06:29 GMT  
		Size: 8.5 MB (8516102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45951496c3bb5ad5cc1b8c18982ed20a9ace397251c384a2c24dbfb8996903b`  
		Last Modified: Mon, 30 Dec 2019 23:06:25 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eaf6e100e70ae4aab07dc3f7ece6be2b1cfd56d0d32090adea34b868712cfb0`  
		Last Modified: Mon, 30 Dec 2019 23:06:28 GMT  
		Size: 7.8 MB (7800167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:207c264f04e366c5bd1fb958a98a72b995af1ef534d9f0023bc03eaac2f84346
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19140791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d45b6d8eff3e11e1532c225b72d6e2948edcff1a40672f0f16c62f72c1014ae`
-	Default Command: `["irssi"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 02:15:17 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Sat, 18 Jan 2020 02:15:20 GMT
ENV HOME=/home/user
# Sat, 18 Jan 2020 02:15:26 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Sat, 18 Jan 2020 02:15:28 GMT
ENV LANG=C.UTF-8
# Sat, 18 Jan 2020 02:15:30 GMT
ENV IRSSI_VERSION=1.2.2
# Sat, 18 Jan 2020 02:16:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		automake 		coreutils 		dpkg-dev dpkg 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		make 		ncurses-dev 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-true-color 		--with-bot 		--with-proxy 		--with-socks 	; 	make -j "$(nproc)"; 	make install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Sat, 18 Jan 2020 02:16:42 GMT
WORKDIR /home/user
# Sat, 18 Jan 2020 02:16:44 GMT
USER user
# Sat, 18 Jan 2020 02:16:45 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69e852f652474e05d47f735b6cd5f72da8c34afad334b50738688b19b0a4db4`  
		Last Modified: Sat, 18 Jan 2020 02:17:06 GMT  
		Size: 9.4 MB (9425621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6def3b6ee199ce1adf97bb4eeaa035b672219b0ee8b530d9d64d8cbade20bdd3`  
		Last Modified: Sat, 18 Jan 2020 02:17:02 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73860e239366f5942b9248b359261d13cc9f5f3bcfdf519862444ed2311678f1`  
		Last Modified: Sat, 18 Jan 2020 02:17:05 GMT  
		Size: 7.0 MB (6990825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; 386

```console
$ docker pull irssi@sha256:06ceaa49272143bc576a7ba5152770993749081dcf137f1fb1eb2013782a9651
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19947359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd9498f6332d6dd2090dfa8ea6ebd973aae9d1ed9ae4c972432518e7e04603b`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 24 Dec 2019 19:38:57 GMT
ADD file:d0127a9692e8445993a88163cb741dbb23fa25436dd65289e76b08484264b397 in / 
# Tue, 24 Dec 2019 19:38:57 GMT
CMD ["/bin/sh"]
# Mon, 30 Dec 2019 22:40:08 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 30 Dec 2019 22:40:09 GMT
ENV HOME=/home/user
# Mon, 30 Dec 2019 22:40:09 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 30 Dec 2019 22:40:10 GMT
ENV LANG=C.UTF-8
# Mon, 30 Dec 2019 22:40:10 GMT
ENV IRSSI_VERSION=1.2.2
# Mon, 30 Dec 2019 22:40:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		automake 		coreutils 		dpkg-dev dpkg 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		make 		ncurses-dev 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-true-color 		--with-bot 		--with-proxy 		--with-socks 	; 	make -j "$(nproc)"; 	make install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 30 Dec 2019 22:40:58 GMT
WORKDIR /home/user
# Mon, 30 Dec 2019 22:40:58 GMT
USER user
# Mon, 30 Dec 2019 22:40:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:57bbc6f150623b3e4f01930af4ab2efa6ed5df02319341a08b1ce0bbd7e4afdf`  
		Last Modified: Tue, 24 Dec 2019 19:39:19 GMT  
		Size: 2.8 MB (2805146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff76006f62081ce832038868fe5b0b60ceed2187a08ed77ee36104006fbba791`  
		Last Modified: Mon, 30 Dec 2019 22:41:28 GMT  
		Size: 8.8 MB (8795524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db6f9ad44fed6961e6e5583a2858d76ed51e909d36e5f56257c2c3f01ec9aa3`  
		Last Modified: Mon, 30 Dec 2019 22:41:25 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbbf684b8369fac0090667874a96aa8959617cdf6f3e2efd898b900ee2271f00`  
		Last Modified: Mon, 30 Dec 2019 22:41:28 GMT  
		Size: 8.3 MB (8345445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:cf87f98694a743ce1910ccf873a30b1e39f73ba9ba67c8053f6570edfaf2d734
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21118083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d21cfedadc16ec97b2c8c03f6e7bdeed571110c27d0df1330f633347594e6731`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 24 Dec 2019 19:28:37 GMT
ADD file:4d85451a651e236d899cd849617594eb6babf24079f9b2269134ad06d89bdecc in / 
# Tue, 24 Dec 2019 19:28:38 GMT
CMD ["/bin/sh"]
# Mon, 30 Dec 2019 22:23:49 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 30 Dec 2019 22:23:53 GMT
ENV HOME=/home/user
# Mon, 30 Dec 2019 22:24:00 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 30 Dec 2019 22:24:03 GMT
ENV LANG=C.UTF-8
# Mon, 30 Dec 2019 22:24:06 GMT
ENV IRSSI_VERSION=1.2.2
# Mon, 30 Dec 2019 22:25:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		automake 		coreutils 		dpkg-dev dpkg 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		make 		ncurses-dev 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-true-color 		--with-bot 		--with-proxy 		--with-socks 	; 	make -j "$(nproc)"; 	make install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 30 Dec 2019 22:25:05 GMT
WORKDIR /home/user
# Mon, 30 Dec 2019 22:25:07 GMT
USER user
# Mon, 30 Dec 2019 22:25:11 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a5dee701e1e87430161d8fce67e77ee5e132bdbafe165c52490a36df654c7660`  
		Last Modified: Tue, 24 Dec 2019 19:29:09 GMT  
		Size: 2.8 MB (2816482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793246a6858f16478d9669ddda5318daf2a7be058d448071d46c0311a5781bc3`  
		Last Modified: Mon, 30 Dec 2019 22:26:00 GMT  
		Size: 9.5 MB (9521140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee975bdd87c45a12edada8731f15a13214fe92ea1844cba6e4358ed4115a4496`  
		Last Modified: Mon, 30 Dec 2019 22:25:56 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9369c932bfaa3e22e067b1ac7961c8c22e942db0997c9618c2fa6e4430f3361c`  
		Last Modified: Mon, 30 Dec 2019 22:26:00 GMT  
		Size: 8.8 MB (8779188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; s390x

```console
$ docker pull irssi@sha256:743262e0cf05ee5125863b88cda7b7377c3062926189f5e02a2b42df784f2cb2
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19412058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ccf5f5bf85e76d9796ebb1c43c0e0bdf44eda4060d07dcb03f2ad6d9c96c1e5`
-	Default Command: `["irssi"]`

```dockerfile
# Sat, 18 Jan 2020 01:41:33 GMT
ADD file:a6f8b7d4ba199527053ef1ac710b5e318135cb6903cb9ad6fae4fe42e6ad0bf7 in / 
# Sat, 18 Jan 2020 01:41:33 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 02:18:41 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Sat, 18 Jan 2020 02:18:42 GMT
ENV HOME=/home/user
# Sat, 18 Jan 2020 02:18:42 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Sat, 18 Jan 2020 02:18:43 GMT
ENV LANG=C.UTF-8
# Sat, 18 Jan 2020 02:18:43 GMT
ENV IRSSI_VERSION=1.2.2
# Sat, 18 Jan 2020 02:19:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		automake 		coreutils 		dpkg-dev dpkg 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		make 		ncurses-dev 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-true-color 		--with-bot 		--with-proxy 		--with-socks 	; 	make -j "$(nproc)"; 	make install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Sat, 18 Jan 2020 02:19:07 GMT
WORKDIR /home/user
# Sat, 18 Jan 2020 02:19:07 GMT
USER user
# Sat, 18 Jan 2020 02:19:07 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:176bad61a3a435da03ec603d2bd8f7a69286d92f21f447b17f21f0bc4e085bde`  
		Last Modified: Sat, 18 Jan 2020 01:41:59 GMT  
		Size: 2.6 MB (2582031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e137b1edc1565268f2019b28a1283c2b36e957c2009bb8ae076a030a13cb509`  
		Last Modified: Sat, 18 Jan 2020 02:19:21 GMT  
		Size: 9.8 MB (9834358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b03d27ba39922c28999efffd37fba89df9b0a24245f1a6512c36d8addc6d77`  
		Last Modified: Sat, 18 Jan 2020 02:19:20 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4f0c62b30ce5b338a1a15eae2c2181316c105dd21264175c162f3ae6c511f3`  
		Last Modified: Sat, 18 Jan 2020 02:19:21 GMT  
		Size: 7.0 MB (6994424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
