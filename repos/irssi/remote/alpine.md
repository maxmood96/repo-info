## `irssi:alpine`

```console
$ docker pull irssi@sha256:62ac933c644046c5f409be773e05af5ecca879a33b0d732f6618b8052ea69aca
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
$ docker pull irssi@sha256:e81de68bf0b471e0b77ad913541a1f32206fcb8c80fac98a0d9d1350478ac605
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18658093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dead0fe2265236caa74a87944b897072c3db257ea60dcd26ad0f8c8a0a57695`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:21:09 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Sat, 13 Nov 2021 06:21:09 GMT
ENV HOME=/home/user
# Sat, 13 Nov 2021 06:21:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Sat, 13 Nov 2021 06:21:10 GMT
ENV LANG=C.UTF-8
# Sat, 13 Nov 2021 06:21:10 GMT
ENV IRSSI_VERSION=1.2.3
# Sat, 26 Feb 2022 02:42:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		automake 		coreutils 		dpkg-dev dpkg 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		make 		ncurses-dev 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-true-color 		--with-bot 		--with-proxy 		--with-socks 	; 	make -j "$(nproc)"; 	make install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Sat, 26 Feb 2022 02:42:56 GMT
WORKDIR /home/user
# Sat, 26 Feb 2022 02:42:56 GMT
USER user
# Sat, 26 Feb 2022 02:42:56 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce5baac574d8b4271c82fa64dcdd49fa857685442591bb2a9088f4a17aa326d`  
		Last Modified: Sat, 13 Nov 2021 06:22:31 GMT  
		Size: 9.5 MB (9546893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6a10ef4b17c6ffd971ee996f3f9f1f835f466b8f8bf05e5f6d7b8e11bdf3e0`  
		Last Modified: Sat, 13 Nov 2021 06:22:28 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c805e6f5481d38ada6303ac8752840cc587fd0cb676315c10e5c3b97f6dda3e0`  
		Last Modified: Sat, 26 Feb 2022 02:43:33 GMT  
		Size: 6.3 MB (6287505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:f47d5355f67178d363007d5ceb085dc5c31a7474d8dd3717e7a49d016b60d623
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17399747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4440bf00c51e7e1118c662cdcc138a9fc2eb71c6412c3e599195855da1833f5`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 03:07:25 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Sat, 13 Nov 2021 03:07:26 GMT
ENV HOME=/home/user
# Sat, 13 Nov 2021 03:07:27 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Sat, 13 Nov 2021 03:07:28 GMT
ENV LANG=C.UTF-8
# Sat, 13 Nov 2021 03:07:28 GMT
ENV IRSSI_VERSION=1.2.3
# Sat, 26 Feb 2022 00:50:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		automake 		coreutils 		dpkg-dev dpkg 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		make 		ncurses-dev 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-true-color 		--with-bot 		--with-proxy 		--with-socks 	; 	make -j "$(nproc)"; 	make install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Sat, 26 Feb 2022 00:50:54 GMT
WORKDIR /home/user
# Sat, 26 Feb 2022 00:50:55 GMT
USER user
# Sat, 26 Feb 2022 00:50:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e18644b7db2c0521d7b46f9a0ad2bbef1e78c4441a4eb4edd2e471d076617e`  
		Last Modified: Sat, 13 Nov 2021 03:09:18 GMT  
		Size: 8.8 MB (8777945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47719028b3d12f241ef81a872a66d640d50374d5c7b7ada4dea7a5d4f8d628b9`  
		Last Modified: Sat, 13 Nov 2021 03:09:12 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c9f2e6dd64e4cf27098cee126ac7e8d3fd7da82e492cd105a0855f350e1d5e`  
		Last Modified: Sat, 26 Feb 2022 00:51:30 GMT  
		Size: 6.0 MB (5987187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:39fd318eba9bfe402c70dbb1658cc83d2008473a2bf7c6640ffcbf0f4cab5410
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16843546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80cf593f5cd7256f7f600c886f639c64a7fef945a7476ac8f235f315f2834f7f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:54 GMT
ADD file:a13993855beba2267575c54a0c6707ddda85d238e697a81046a8b1c1a34df054 in / 
# Fri, 12 Nov 2021 16:57:54 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 10:53:57 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Sat, 13 Nov 2021 10:53:58 GMT
ENV HOME=/home/user
# Sat, 13 Nov 2021 10:54:01 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Sat, 13 Nov 2021 10:54:02 GMT
ENV LANG=C.UTF-8
# Sat, 13 Nov 2021 10:54:02 GMT
ENV IRSSI_VERSION=1.2.3
# Sat, 13 Nov 2021 10:55:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		automake 		coreutils 		dpkg-dev dpkg 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		make 		ncurses-dev 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-true-color 		--with-bot 		--with-proxy 		--with-socks 	; 	make -j "$(nproc)"; 	make install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Sat, 13 Nov 2021 10:55:27 GMT
WORKDIR /home/user
# Sat, 13 Nov 2021 10:55:27 GMT
USER user
# Sat, 13 Nov 2021 10:55:28 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:767c1b67bc22761376676021ea5a310e7a7d1344b7a017bb8ede1a202340dbaf`  
		Last Modified: Fri, 12 Nov 2021 16:59:54 GMT  
		Size: 2.4 MB (2436506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf65fbf3cfd284ebb1b6bcbb3f5aeb9c90f25a8ef76be7e8626b4de4cbc9d12f`  
		Last Modified: Sat, 13 Nov 2021 10:56:37 GMT  
		Size: 8.6 MB (8630841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb323d0bda53eaa67141782bb2c816d1ee006b00a1834b70ab92d64c7bf823ed`  
		Last Modified: Sat, 13 Nov 2021 10:56:32 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d23d9d27bff57b2dbc2a08da74408f29dc954f150b5886a7e982dbfa160800`  
		Last Modified: Sat, 13 Nov 2021 10:56:35 GMT  
		Size: 5.8 MB (5774928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:237a3fb28d0d750071b6920a2ccc32afab7b574fc1a31deb71006cc8820b50de
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18493717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43e7f354df530cf5903915bf52cff862c5931681cd9d85b24b826e77a9a3998f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:27:36 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Sat, 13 Nov 2021 06:27:37 GMT
ENV HOME=/home/user
# Sat, 13 Nov 2021 06:27:38 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Sat, 13 Nov 2021 06:27:39 GMT
ENV LANG=C.UTF-8
# Sat, 13 Nov 2021 06:27:40 GMT
ENV IRSSI_VERSION=1.2.3
# Sat, 13 Nov 2021 06:28:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		automake 		coreutils 		dpkg-dev dpkg 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		make 		ncurses-dev 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-true-color 		--with-bot 		--with-proxy 		--with-socks 	; 	make -j "$(nproc)"; 	make install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Sat, 13 Nov 2021 06:28:27 GMT
WORKDIR /home/user
# Sat, 13 Nov 2021 06:28:28 GMT
USER user
# Sat, 13 Nov 2021 06:28:29 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e152f8af96423f066d9e00e70b1fbbc96e94dbf4c98f075c6b7117135d97be4b`  
		Last Modified: Sat, 13 Nov 2021 06:29:25 GMT  
		Size: 9.5 MB (9543545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6065fe2276d0eabc118421590a0496be4176b2ecb15421a8798cfd55ea4ff0eb`  
		Last Modified: Sat, 13 Nov 2021 06:29:23 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39cb7b7de97a12a3eb299292e27a79d7e76bb96fd8eef37dc3d046620f92fb67`  
		Last Modified: Sat, 13 Nov 2021 06:29:24 GMT  
		Size: 6.2 MB (6229287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; 386

```console
$ docker pull irssi@sha256:e1533792e9821046cba4fd97ad160b36c6943d86078fde47a356e79b1184755a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17711979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1216a4299c56d5ac15112c6e1df985afef515bf2dbaeaa74ac5b8479b4080fbf`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 04:44:05 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Sat, 13 Nov 2021 04:44:06 GMT
ENV HOME=/home/user
# Sat, 13 Nov 2021 04:44:07 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Sat, 13 Nov 2021 04:44:07 GMT
ENV LANG=C.UTF-8
# Sat, 13 Nov 2021 04:44:07 GMT
ENV IRSSI_VERSION=1.2.3
# Sat, 13 Nov 2021 04:45:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		automake 		coreutils 		dpkg-dev dpkg 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		make 		ncurses-dev 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-true-color 		--with-bot 		--with-proxy 		--with-socks 	; 	make -j "$(nproc)"; 	make install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Sat, 13 Nov 2021 04:45:13 GMT
WORKDIR /home/user
# Sat, 13 Nov 2021 04:45:13 GMT
USER user
# Sat, 13 Nov 2021 04:45:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75fb5374975ca920199ffda46b9a54fba11dd5eda1e231d1586fd28b00bfab55`  
		Last Modified: Sat, 13 Nov 2021 04:45:58 GMT  
		Size: 8.9 MB (8914326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bda351aa4adae26d595a83d58109f6b9e63f43b0ef135c5c65ae3d27207425`  
		Last Modified: Sat, 13 Nov 2021 04:45:53 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19698f734fdb7985e49d87a08629d95fecae4a127bcb935a6cb36b5e2f1eed82`  
		Last Modified: Sat, 13 Nov 2021 04:45:56 GMT  
		Size: 6.0 MB (5967572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:256febb4e88caa7803e51f3bc7bc6d08a2ee593d903986b0048bb9f2a3adf1dd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (18956324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c7163a5875310136dafbc963f6cd5ff2f3e2a661335157c1122fab4bbd8b961`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 12 Nov 2021 21:18:25 GMT
ADD file:f7216323de17450e653f77c86d2c1e2e8ec01e1133e93f29c515761b3e9d8f7d in / 
# Fri, 12 Nov 2021 21:18:28 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 15:17:21 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Sat, 13 Nov 2021 15:17:25 GMT
ENV HOME=/home/user
# Sat, 13 Nov 2021 15:17:37 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Sat, 13 Nov 2021 15:17:39 GMT
ENV LANG=C.UTF-8
# Sat, 13 Nov 2021 15:17:41 GMT
ENV IRSSI_VERSION=1.2.3
# Sat, 26 Feb 2022 07:41:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		automake 		coreutils 		dpkg-dev dpkg 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		make 		ncurses-dev 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-true-color 		--with-bot 		--with-proxy 		--with-socks 	; 	make -j "$(nproc)"; 	make install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Sat, 26 Feb 2022 07:41:20 GMT
WORKDIR /home/user
# Sat, 26 Feb 2022 07:41:23 GMT
USER user
# Sat, 26 Feb 2022 07:41:29 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6729720a3e6b58511df148134bb67d786ad90f9fce1c02ba5bbfd31f33055fbe`  
		Last Modified: Fri, 12 Nov 2021 21:19:49 GMT  
		Size: 2.8 MB (2820517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5c3bca0019540f7fc24b101be6d560cac83a81f1b6cda2b2fd1dcb4400c6e7`  
		Last Modified: Sat, 13 Nov 2021 15:19:52 GMT  
		Size: 9.6 MB (9642236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2dbb74b4ba4c2dc34b3813acf99e0b991bcdb045c4404168d74feb0a7d550f8`  
		Last Modified: Sat, 13 Nov 2021 15:19:50 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b020c19f58e52afc93f0a890fe6012615a585c053cb4cf0da4571f3eb92ac642`  
		Last Modified: Sat, 26 Feb 2022 07:42:26 GMT  
		Size: 6.5 MB (6492301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; s390x

```console
$ docker pull irssi@sha256:50bdb230f1994347e42ae29828177ee13eaaecb603ee60b6a9d294ea0b7d7aa7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18872134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2a07a0958db17c3a111679879c59fd06187e002b2f6b0fa605868f44f821b9`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 12 Nov 2021 16:41:44 GMT
ADD file:637f327c9b07758709ef7dbc42eb472c888d221acde89b1c3775553864334d5c in / 
# Fri, 12 Nov 2021 16:41:44 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:46:37 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Fri, 12 Nov 2021 21:46:38 GMT
ENV HOME=/home/user
# Fri, 12 Nov 2021 21:46:38 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Fri, 12 Nov 2021 21:46:39 GMT
ENV LANG=C.UTF-8
# Fri, 12 Nov 2021 21:46:39 GMT
ENV IRSSI_VERSION=1.2.3
# Sat, 26 Feb 2022 00:44:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		autoconf 		automake 		coreutils 		dpkg-dev dpkg 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		make 		ncurses-dev 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-true-color 		--with-bot 		--with-proxy 		--with-socks 	; 	make -j "$(nproc)"; 	make install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Sat, 26 Feb 2022 00:44:16 GMT
WORKDIR /home/user
# Sat, 26 Feb 2022 00:44:16 GMT
USER user
# Sat, 26 Feb 2022 00:44:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b872f056719bde6e6722091afb2a3376d720c69c142b91ac352050080dd79615`  
		Last Modified: Fri, 12 Nov 2021 16:42:54 GMT  
		Size: 2.6 MB (2611155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dbee0262fb10c6ee826cdf9ad391574e205886b3ecbe48df9d7faefc8631395`  
		Last Modified: Fri, 12 Nov 2021 21:47:46 GMT  
		Size: 10.0 MB (9982759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d313f2224226336843ad5b4eed2dc03c80a76d54cb049248fa3ce29f7b17f6fe`  
		Last Modified: Fri, 12 Nov 2021 21:47:44 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647b0b24f0a4c27c905b049227cf6d0f7f4c0626fee67a796e2a2a5f234a9632`  
		Last Modified: Sat, 26 Feb 2022 00:44:58 GMT  
		Size: 6.3 MB (6276948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
