## `irssi:alpine3.21`

```console
$ docker pull irssi@sha256:55940669ca5f3eed0516d771aaeac2d308988b4b1d989e0f8911dbb32c2832ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `irssi:alpine3.21` - linux; amd64

```console
$ docker pull irssi@sha256:336fb0bf260ee2609812f5e34bb4cd3442beff2447ba8c1239f0812b91efd273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19993690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd16baceee58bda22459c0a0de2ea70260fee3c0b1b3d0e85683e2059628cc70`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:52:22 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
ENV HOME=/home/user
# Fri, 13 Dec 2024 00:52:22 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 00:52:22 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 13 Dec 2024 00:52:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
WORKDIR /home/user
# Fri, 13 Dec 2024 00:52:22 GMT
USER user
# Fri, 13 Dec 2024 00:52:22 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7384aba53677d626a575e3d536998a02838ebb3f712f32bc84d3197c70a6e43f`  
		Last Modified: Fri, 13 Dec 2024 01:29:47 GMT  
		Size: 10.4 MB (10404708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b86539435864a6adf5d2968e1d5b97f4dc8729b51c000e2161a61ca55367e04`  
		Last Modified: Fri, 13 Dec 2024 01:29:46 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d684d37c3541133b8cc2fd9df4da32116d9537d0e2fbd1a3ad2cb1a29ef1d80`  
		Last Modified: Fri, 13 Dec 2024 01:29:46 GMT  
		Size: 5.9 MB (5943540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:4a64fbe1446cd2b03ef3f262750ff401046f11afbe915a7c21c18d5167787a4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1289203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fdbb8de2ecb693d28f44049cb9f0138760351aa11ebf5c75483555f2abb56ff`

```dockerfile
```

-	Layers:
	-	`sha256:09d0d372eda010f730a8f4f082054946ce3c27efd81c70a38a99ced582f28366`  
		Last Modified: Fri, 13 Dec 2024 01:29:46 GMT  
		Size: 1.3 MB (1271661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a41ff1f577c7f72ba0b2a5c4a318b464d765c5d476d17fc80f1c27ae4229f5e`  
		Last Modified: Fri, 13 Dec 2024 01:29:46 GMT  
		Size: 17.5 KB (17542 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; arm variant v6

```console
$ docker pull irssi@sha256:c6b4ca6582d4e3c344b4e20351cb4d3f455b8e2b0e505436cae13714fd2a16c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18769072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f315c7209a682f5f61df30d9b5bb2b0e556b7b3995a469ada17df9d7f333bec5`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:52:22 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
ENV HOME=/home/user
# Fri, 13 Dec 2024 00:52:22 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 00:52:22 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 13 Dec 2024 00:52:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
WORKDIR /home/user
# Fri, 13 Dec 2024 00:52:22 GMT
USER user
# Fri, 13 Dec 2024 00:52:22 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499df35117ba582f903dfc60fda67a437d0c6f15681d32dac6b3e1a95211c28f`  
		Size: 9.6 MB (9622905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf94c9d5ff47153bf82dd5c310f19a4882639a1f5452174ce636d8a513790209`  
		Last Modified: Fri, 13 Dec 2024 01:48:09 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3288207417d553cc2f9cbd91ebac1d352a9599c713b8cd6b68a0b411c741df`  
		Last Modified: Fri, 13 Dec 2024 01:48:09 GMT  
		Size: 5.8 MB (5777988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:85d2671543af0489961dccd982c049ffdbb8c2f4c313d1c675caea017f8f6261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57a86094b33eea4d0b093140276bc5046ab7e42545a5afded5de5177aa893d3`

```dockerfile
```

-	Layers:
	-	`sha256:dfbcc55b782bc745d8debc81d7207d9a86afd71070e485d376825c8b5010ac9d`  
		Last Modified: Fri, 13 Dec 2024 01:48:09 GMT  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; arm variant v7

```console
$ docker pull irssi@sha256:21838377030b4a7343e5d162ea0695e4aa095b29763b34e318a3173035c1c2fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18094444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0203da06376bc244d08b1894bf91ab9f14a722caaec0dd99df802f3c76b05ed`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:52:22 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
ENV HOME=/home/user
# Fri, 13 Dec 2024 00:52:22 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 00:52:22 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 13 Dec 2024 00:52:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
WORKDIR /home/user
# Fri, 13 Dec 2024 00:52:22 GMT
USER user
# Fri, 13 Dec 2024 00:52:22 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c145b437881bf74fb6d3b92f9ecc04283362bd61dff7053e7b6875f8d5f39e`  
		Size: 9.5 MB (9453360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244d70019cc89783e5b1ad54dbbfe1109499d827e3a4c907245e7779c9a683d1`  
		Last Modified: Fri, 13 Dec 2024 01:51:11 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57aec11ab6e789ed42645dcba9d63e37c6d92cabe112eae3cfbdc6c4ed26d6bb`  
		Last Modified: Fri, 13 Dec 2024 01:51:11 GMT  
		Size: 5.5 MB (5540051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:b6f604e833c0207a1cea157a5f013ba9604ce162d9d8775a03f7e28c7dba5dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1292218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:225ccfcc61ab239a998f506ac5d0bf16cf2625d357c015daf8f4df25e602fade`

```dockerfile
```

-	Layers:
	-	`sha256:7a5e900c308b985962c66cf148d05645cd8f4198b43bc14ecad018e7a3f7f6ce`  
		Last Modified: Fri, 13 Dec 2024 01:51:11 GMT  
		Size: 1.3 MB (1274545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69443020b375c5f17fddbc5363ef3ecd63ddf0fd78693a3bc04c247b5cfd2053`  
		Last Modified: Fri, 13 Dec 2024 01:51:10 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:6ada86b02773224700057c60d7eb83a11617458fb28fc710e2a63ac8558fa452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20185886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b10b7c5c21b638dcb23a95ba145e117c8e6215181885edbd01432f51b5a1d2fd`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:52:22 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
ENV HOME=/home/user
# Fri, 13 Dec 2024 00:52:22 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 00:52:22 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 13 Dec 2024 00:52:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
WORKDIR /home/user
# Fri, 13 Dec 2024 00:52:22 GMT
USER user
# Fri, 13 Dec 2024 00:52:22 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77d23ee02b015183139fb7fd8378af60c7665eb5271a0d54e2ed06639286375`  
		Size: 10.4 MB (10370379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c9550ec800d0c24b3469f08ec0175c2337a8d8ad61d67f560adb928c15b145`  
		Last Modified: Fri, 13 Dec 2024 01:52:25 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2946d7bddd02f0170a4031b6ef7d0f4d9cfaecf3bd69a51e9b313c2e6c81e7bf`  
		Last Modified: Fri, 13 Dec 2024 01:52:26 GMT  
		Size: 5.8 MB (5821322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:1c369be4050536d381d3e13ab8a70ef7848003971d42ff83311f1eb604f78da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1289490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b93dbc99bac78e3ae3910d4997957cbd430a69f7b3baef85e8521a1e3a18a985`

```dockerfile
```

-	Layers:
	-	`sha256:cc3de9230c6c250d9a9588f8f725d8a025bf67b9c8753e28c3866802354cfcce`  
		Size: 1.3 MB (1271765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a16708cd0048952747a0e28bef0ea18748e1f88bf26018f496deb8fc1ed1f28`  
		Last Modified: Fri, 13 Dec 2024 01:52:25 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; 386

```console
$ docker pull irssi@sha256:bb3d8fd72f150a2f0e3db53bd52d20a0b1970416dc9ec58bb271ae3a9a592348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19458634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c19afc33dc9c04a7475c9aed56e986f8289313df089141784c1bc744cf494635`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:52:22 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
ENV HOME=/home/user
# Fri, 13 Dec 2024 00:52:22 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 00:52:22 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 13 Dec 2024 00:52:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
WORKDIR /home/user
# Fri, 13 Dec 2024 00:52:22 GMT
USER user
# Fri, 13 Dec 2024 00:52:22 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d77e1fb5542f4b07e742d60eaa6c16d3f44cb9569f4778bb1547b3c6beb2ab`  
		Last Modified: Fri, 13 Dec 2024 01:29:55 GMT  
		Size: 10.0 MB (9959220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373238acbe738092213578f6358228cc9554a9e0c74664ccf55e8717d017b063`  
		Last Modified: Fri, 13 Dec 2024 01:29:54 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8f40e395c3e6cad56cfa66cf1cb29f4009d2cbd44738287723f332f0767d3b`  
		Last Modified: Fri, 13 Dec 2024 01:29:55 GMT  
		Size: 6.0 MB (6032334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:7e40f31093e7f0aa84dfc77fe227421df60b811b0bc1aa6d81063f8b2d1235dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1289099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea59ac9c71a643c18dd066de50e7c80728b5aef7495457002b6bcc95f834dc6`

```dockerfile
```

-	Layers:
	-	`sha256:f73cd654305fd3e6dd381277d76c77d07e314ba6978dc1bdfd88a7f2415eb868`  
		Last Modified: Fri, 13 Dec 2024 01:29:54 GMT  
		Size: 1.3 MB (1271616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a6079d9cee762d04f1ba773ab234c5ad003e1723744e7a2f723800a88c1f81a`  
		Last Modified: Fri, 13 Dec 2024 01:29:54 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; ppc64le

```console
$ docker pull irssi@sha256:f0fa68e5bdfb8db76d0c44c5a68a3262b7d6a808bdf5e0eae91ea07ff15f2d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20374240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d603a0156008df0a328848799147982e79d5c4e09b67e6c8025af363598eea1`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:52:22 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
ENV HOME=/home/user
# Fri, 13 Dec 2024 00:52:22 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 00:52:22 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 13 Dec 2024 00:52:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
WORKDIR /home/user
# Fri, 13 Dec 2024 00:52:22 GMT
USER user
# Fri, 13 Dec 2024 00:52:22 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23014e0fedcb97624d76b0320ebe656c617ea68b84d72f76654793c0ea6a1d66`  
		Last Modified: Fri, 13 Dec 2024 01:53:54 GMT  
		Size: 10.6 MB (10590422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15523ac6ddf6eba8d3008449697b3ebd3693b49b6d337d7219732bfc68d4465`  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806bc2c2c80b504f37c15764856ed4c0c1418adfaa4c4126ced659e67ec1158e`  
		Last Modified: Fri, 13 Dec 2024 01:53:54 GMT  
		Size: 6.2 MB (6205711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:0efd745b8c7a15f7eb115eb562f9fe88896e514a60a36f17dabbce79d6c883b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1287380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3451366c6cfebbaf9ad054a7bc9968983beea80f5843f11976f9ca2b8730c148`

```dockerfile
```

-	Layers:
	-	`sha256:e8c0eb6107ec88af989fcb3b86cd61226f25084f974522383047a4db27ba2ed6`  
		Last Modified: Fri, 13 Dec 2024 01:53:54 GMT  
		Size: 1.3 MB (1269765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cdfcaf0bd9d17f6100dc20f86273e3ce572e48cee89e60d2c7c8097566ec794`  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; riscv64

```console
$ docker pull irssi@sha256:dff7b93f11deeb1a8023b02b136481f61f65be04739511a558b9e9bb65e480b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19160536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:149d1f9424a87085b8c96df94c7efc420e5508a57d79fefb29a9069a3222851d`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:52:22 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
ENV HOME=/home/user
# Fri, 13 Dec 2024 00:52:22 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 00:52:22 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 13 Dec 2024 00:52:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
WORKDIR /home/user
# Fri, 13 Dec 2024 00:52:22 GMT
USER user
# Fri, 13 Dec 2024 00:52:22 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea49ffce234460a182b928db174ef87cdae434a6dd60e1616174604faa8fe2d6`  
		Last Modified: Fri, 13 Dec 2024 19:41:00 GMT  
		Size: 9.8 MB (9847840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5184bc12270538b77c634d56124ffb50fc79f3dac904754caafa45336e34b500`  
		Last Modified: Fri, 13 Dec 2024 19:40:58 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa292ed70b91ec6be201c053e89be52d89c295c7064efdc9bc3152a207ddde1c`  
		Last Modified: Fri, 13 Dec 2024 19:40:59 GMT  
		Size: 6.0 MB (5957677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:db0a742075935e7db2fae698596bc2c6d6c58a8fba1191a3381227430bd5660b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1287372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:199f2e38c54c656a48fcc30ae398d8d798b4bb1f866306e867e8cb6824d562a0`

```dockerfile
```

-	Layers:
	-	`sha256:6e4862a5a0a88b7fc9c096bbd37ae64fac35cf800dfd4586f40fb25082f168c0`  
		Last Modified: Fri, 13 Dec 2024 19:40:59 GMT  
		Size: 1.3 MB (1269761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a1f594d2217e6c242a3cc1f280e0b02a545f9b7c6989743ba3da3724ca352a8`  
		Last Modified: Fri, 13 Dec 2024 19:40:58 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; s390x

```console
$ docker pull irssi@sha256:37a93b1e5db028de477c6f26854870b303d55a60c7135859a5e61cb1fb4fbcec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20538181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753dd51177e51164a6fb1ff8c23dcc77e5f07c8e46a0ea01e7d5a6346064e3f1`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:52:22 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
ENV HOME=/home/user
# Fri, 13 Dec 2024 00:52:22 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 00:52:22 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 13 Dec 2024 00:52:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
WORKDIR /home/user
# Fri, 13 Dec 2024 00:52:22 GMT
USER user
# Fri, 13 Dec 2024 00:52:22 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af769ac45497c8811c152c93d94b62b05ab1aa3cf40f2b01310ba64a0bfc05af`  
		Last Modified: Fri, 13 Dec 2024 02:34:14 GMT  
		Size: 11.0 MB (10968385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9765ad6f8d69318fce5c29dbc5d84ebcaa8f5bf2ea81c77faf2ef8218cd83e`  
		Last Modified: Fri, 13 Dec 2024 02:34:14 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e5d8db4c89dfce60c5033b8e492cfb142b0542ffd4507f091ca24e04f1de83`  
		Last Modified: Fri, 13 Dec 2024 02:34:15 GMT  
		Size: 6.1 MB (6099277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:1ec1331ef5d60413daa5c96e9f69729cdad193ed68abc71df6c01f8cdf2ff48c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1287250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0be189695feb46167635577d2e9462883ff82412b3e0cbbcb4ffe50153ec736`

```dockerfile
```

-	Layers:
	-	`sha256:e37f236d30594840a3572d6bb4fe0ceb133577435f112d227200885e5879a811`  
		Last Modified: Fri, 13 Dec 2024 02:34:14 GMT  
		Size: 1.3 MB (1269707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0221ba14df94a82a6ca51b6bc4f05d23002da11880315ff00f7a9fbbdb1857d4`  
		Last Modified: Fri, 13 Dec 2024 02:34:14 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json
