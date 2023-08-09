## `irssi:alpine3.18`

```console
$ docker pull irssi@sha256:4b3f28dc4522bb0209ba4529ac626d879cad45d64d0d76929ff32302b4a88476
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

### `irssi:alpine3.18` - linux; amd64

```console
$ docker pull irssi@sha256:c690fea8bc556b0265eaa9e04df77fa346d293901ac5a6f959e67bec9889040c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18443867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2435905e4f254e973d6085f275b28e242db9432e514b21128416e06b6a6bed0`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 01:58:28 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Wed, 09 Aug 2023 01:58:28 GMT
ENV HOME=/home/user
# Wed, 09 Aug 2023 01:58:29 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Wed, 09 Aug 2023 01:58:29 GMT
ENV LANG=C.UTF-8
# Wed, 09 Aug 2023 01:58:29 GMT
ENV IRSSI_VERSION=1.4.4
# Wed, 09 Aug 2023 01:58:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Wed, 09 Aug 2023 01:58:47 GMT
WORKDIR /home/user
# Wed, 09 Aug 2023 01:58:48 GMT
USER user
# Wed, 09 Aug 2023 01:58:48 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c299710b1ab87afb1f6ac87939396c65b60fb195aa8c33e0ae562c629986c7`  
		Last Modified: Wed, 09 Aug 2023 01:59:04 GMT  
		Size: 9.6 MB (9637852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e307a0c834c1c97f259ca36d85dd3278bc4f74f67d22db0715c5b13b4b26a22`  
		Last Modified: Wed, 09 Aug 2023 01:59:03 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9059412d3fb1532142f10e8250eff86f1083a4c307e663436ddf4389937bb8`  
		Last Modified: Wed, 09 Aug 2023 01:59:03 GMT  
		Size: 5.4 MB (5403118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine3.18` - linux; arm variant v6

```console
$ docker pull irssi@sha256:86f161b1a624031dc9cb2d2907e708e6f782455857cfe4e68d89fa3ea811968a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17263392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c64b1e9863f823f30379e8b1ba927de7209b57dd7a59e8c7daec0ca6821467`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 20:43:12 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Tue, 08 Aug 2023 20:43:12 GMT
ENV HOME=/home/user
# Tue, 08 Aug 2023 20:43:12 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 08 Aug 2023 20:43:12 GMT
ENV LANG=C.UTF-8
# Tue, 08 Aug 2023 20:43:12 GMT
ENV IRSSI_VERSION=1.4.4
# Tue, 08 Aug 2023 20:43:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Tue, 08 Aug 2023 20:43:35 GMT
WORKDIR /home/user
# Tue, 08 Aug 2023 20:43:35 GMT
USER user
# Tue, 08 Aug 2023 20:43:35 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c56a1bcfc7afff7a5a1b4036b47ca4c083194105cf9f0bf9916e8f01a99ffd1`  
		Last Modified: Tue, 08 Aug 2023 20:43:49 GMT  
		Size: 8.9 MB (8873581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ea04311041fd0322313bc225f454e1c159427e0ef152a8b405896600b8a473`  
		Last Modified: Tue, 08 Aug 2023 20:43:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2944242a4505d59c2fbf20afa30bd2e588a01bf6a9785ab3c8a470a597b4172`  
		Last Modified: Tue, 08 Aug 2023 20:43:48 GMT  
		Size: 5.2 MB (5243720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine3.18` - linux; arm variant v7

```console
$ docker pull irssi@sha256:39b31754b9607eb4e40ba490b5ae796dc050555cd971df5f147971f98bec2c2e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16622956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a425c83559c38fd9ea04fed3dac60c590bf233aea6eafce96946682652757b`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:25 GMT
ADD file:e3f56488d3d3bb67729714db13ddadf6652e7efb5281cfc7010d3e71f9d6607f in / 
# Mon, 07 Aug 2023 19:57:25 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 01:18:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Tue, 08 Aug 2023 01:18:32 GMT
ENV HOME=/home/user
# Tue, 08 Aug 2023 01:18:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 08 Aug 2023 01:18:32 GMT
ENV LANG=C.UTF-8
# Tue, 08 Aug 2023 01:18:32 GMT
ENV IRSSI_VERSION=1.4.4
# Tue, 08 Aug 2023 01:18:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Tue, 08 Aug 2023 01:18:49 GMT
WORKDIR /home/user
# Tue, 08 Aug 2023 01:18:49 GMT
USER user
# Tue, 08 Aug 2023 01:18:49 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f8dec92eec42224ef9e6ca9c6207ea6b9195dcf93d06bd5ceff0f814b62bf064`  
		Last Modified: Mon, 07 Aug 2023 19:57:55 GMT  
		Size: 2.9 MB (2899480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50072b4c9927347770448dba84676c4165e9810f8c7e8d5167049698e97e379e`  
		Last Modified: Tue, 08 Aug 2023 01:19:13 GMT  
		Size: 8.7 MB (8713691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c42151aa91c6c6334c01ecae667b1b758cb1729f97bda99ed99a4902ff2180e`  
		Last Modified: Tue, 08 Aug 2023 01:19:11 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca598d51edc21ae9f5780c6d6bbea24c6805c906019921d7cca80767ba4342f`  
		Last Modified: Tue, 08 Aug 2023 01:19:12 GMT  
		Size: 5.0 MB (5008501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine3.18` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:c1afe9e272a1d25be415aa825a334e632f7134f5e6080c7062f70557c084e5fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18307238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1269e8338be18c300103717e0e15067aa9ed56aff66b74e6547b28570817428b`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:19 GMT
ADD file:b2e7eaa7e41f08853dbe08d84439a7f9fd32fc58c3aa1e298f3f60343b2b683a in / 
# Mon, 07 Aug 2023 19:39:19 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 00:46:56 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Wed, 09 Aug 2023 00:46:57 GMT
ENV HOME=/home/user
# Wed, 09 Aug 2023 00:46:57 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Wed, 09 Aug 2023 00:46:57 GMT
ENV LANG=C.UTF-8
# Wed, 09 Aug 2023 00:46:57 GMT
ENV IRSSI_VERSION=1.4.4
# Wed, 09 Aug 2023 00:47:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Wed, 09 Aug 2023 00:47:10 GMT
WORKDIR /home/user
# Wed, 09 Aug 2023 00:47:10 GMT
USER user
# Wed, 09 Aug 2023 00:47:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9fda8d8052c61740409c4bea888859c141fd8cc3f58ac61943144ff6d1681b2d`  
		Last Modified: Mon, 07 Aug 2023 19:39:45 GMT  
		Size: 3.3 MB (3330767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c221b7124bd609cc0c88ee0a922bcd069bd815af11716e5243f1ac807ea131ce`  
		Last Modified: Wed, 09 Aug 2023 00:47:29 GMT  
		Size: 9.7 MB (9666001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0910e7692c8bdf0a7ec277037abddbb55586b0f3b47db19b964d649cd4eb28d3`  
		Last Modified: Wed, 09 Aug 2023 00:47:28 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9c677e4615a51bf7be3968d0289ad797beb3924a3f1c9f34f868db8b08d7af`  
		Last Modified: Wed, 09 Aug 2023 00:47:28 GMT  
		Size: 5.3 MB (5309189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine3.18` - linux; 386

```console
$ docker pull irssi@sha256:0db563ef1d4943e099d9b94c6d3a5373f9d609015588878e7ef5a534f6f7892e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17545633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9685d5c50bd27f896c7a71a716392d71c14abdd0b147821f10d6b43b460f82fa`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:26 GMT
ADD file:4b33c52e11b19fde30197c62ead0b77bde28d34edaa08346a5302cd892d3cebe in / 
# Mon, 07 Aug 2023 19:38:27 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 21:44:50 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 07 Aug 2023 21:44:50 GMT
ENV HOME=/home/user
# Mon, 07 Aug 2023 21:44:50 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 07 Aug 2023 21:44:50 GMT
ENV LANG=C.UTF-8
# Mon, 07 Aug 2023 21:44:50 GMT
ENV IRSSI_VERSION=1.4.4
# Mon, 07 Aug 2023 21:45:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 07 Aug 2023 21:45:24 GMT
WORKDIR /home/user
# Mon, 07 Aug 2023 21:45:24 GMT
USER user
# Mon, 07 Aug 2023 21:45:24 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:95dc695758361a4038a2d9026959d72e1f531114edb0341be7ce47d912ef069e`  
		Last Modified: Mon, 07 Aug 2023 19:38:56 GMT  
		Size: 3.2 MB (3235144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046b2528594cd9fc777d0153d709fb2809d8b44f8c99420ff232919922d33053`  
		Last Modified: Mon, 07 Aug 2023 21:45:51 GMT  
		Size: 8.9 MB (8896294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b9a58d32089d32752297064b4653251abf366ea9158a7abc0b90b15ceee675`  
		Last Modified: Mon, 07 Aug 2023 21:45:48 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca72c81c6201ee5c211d024845b1b6f7075f4e89132dfb205d68e8a03c277947`  
		Last Modified: Mon, 07 Aug 2023 21:45:50 GMT  
		Size: 5.4 MB (5412910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine3.18` - linux; ppc64le

```console
$ docker pull irssi@sha256:f8e8ee83d966507b0fea53462b618401b83daf7f523ddfcbf02ecab0daa79d33
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18706016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c95884f1cff2c5b774e56fc9ef56bdb289893205f4b7095309f0875c1dfd97`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:25 GMT
ADD file:b8cf7516cdf9487d9347da0b5b5e3a6f65f24ebcdcadf81f430adb2b2664f2d1 in / 
# Mon, 07 Aug 2023 20:16:26 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 01:04:07 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Tue, 08 Aug 2023 01:04:10 GMT
ENV HOME=/home/user
# Tue, 08 Aug 2023 01:04:13 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 08 Aug 2023 01:04:13 GMT
ENV LANG=C.UTF-8
# Tue, 08 Aug 2023 01:04:14 GMT
ENV IRSSI_VERSION=1.4.4
# Tue, 08 Aug 2023 01:04:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Tue, 08 Aug 2023 01:04:40 GMT
WORKDIR /home/user
# Tue, 08 Aug 2023 01:04:42 GMT
USER user
# Tue, 08 Aug 2023 01:04:44 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:55353ca330e9474ce7b858eca6842bb540ef4a70b2981c2ed47eefb9ef4253ad`  
		Last Modified: Mon, 07 Aug 2023 20:17:20 GMT  
		Size: 3.3 MB (3346251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03fb6d6b3d88160311a208a89abce6a55248b5806df64524162295110f7fe85`  
		Last Modified: Tue, 08 Aug 2023 01:05:26 GMT  
		Size: 9.7 MB (9726946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dd339118965df2c5c58f96440da6daf2ca178448b019c2646e1aa6c618ea2b`  
		Last Modified: Tue, 08 Aug 2023 01:05:23 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8adb7c2a30ee10ee6d4ba10643644281a19908dee300bbeeb1683620eee9396f`  
		Last Modified: Tue, 08 Aug 2023 01:05:24 GMT  
		Size: 5.6 MB (5631536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine3.18` - linux; s390x

```console
$ docker pull irssi@sha256:18a16ccf400d1703510731058f8fa96ac4e12fc2f3a69182ba0992e8aac09772
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18701981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:974c8c6125900610e54c7c70bfc633a88d8f6ab68d95460cee662e84b3742ff0`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 07 Aug 2023 19:41:54 GMT
ADD file:b57ea5bba3c986df3471f3ea27443a9a4b19d40c46f9fbca8bb6077b399725aa in / 
# Mon, 07 Aug 2023 19:41:55 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:34:00 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 07 Aug 2023 20:34:02 GMT
ENV HOME=/home/user
# Mon, 07 Aug 2023 20:34:03 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 07 Aug 2023 20:34:04 GMT
ENV LANG=C.UTF-8
# Mon, 07 Aug 2023 20:34:04 GMT
ENV IRSSI_VERSION=1.4.4
# Mon, 07 Aug 2023 20:34:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 07 Aug 2023 20:34:25 GMT
WORKDIR /home/user
# Mon, 07 Aug 2023 20:34:25 GMT
USER user
# Mon, 07 Aug 2023 20:34:25 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8bed2eae372fe236061920d89ae1ce89695a12df84989113bcc7ce4bd9774456`  
		Last Modified: Mon, 07 Aug 2023 19:42:39 GMT  
		Size: 3.2 MB (3214195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac529dad188f0aa87b371b0436c2c5069d189ea8aa8a91cff51a6d65f6345af7`  
		Last Modified: Mon, 07 Aug 2023 20:34:55 GMT  
		Size: 10.1 MB (10078915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5671f425cf9f2932a941fdd2470f63eecc9f4838ef35aa0eeecc96fc1c7a7ddc`  
		Last Modified: Mon, 07 Aug 2023 20:34:53 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d6fcd32d935e7ccc5e845731384b2f627fbc1db6521e0146b91d0193536067`  
		Last Modified: Mon, 07 Aug 2023 20:34:54 GMT  
		Size: 5.4 MB (5407590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
