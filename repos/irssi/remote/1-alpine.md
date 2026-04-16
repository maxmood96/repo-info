## `irssi:1-alpine`

```console
$ docker pull irssi@sha256:7c2ee0882bf007852a20867f9913437ae6657fd03a331e7a77e133726ff69944
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

### `irssi:1-alpine` - linux; amd64

```console
$ docker pull irssi@sha256:dc5df1b58e5b65a3a759880c5e85d4a3f9b00101c8714c1c641b6cc9238acaa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20786977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288090f6d91eede7d4eeff9b23bc23af786c37eeadccb13bd6f3ef9437ce4336`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:42 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:17:42 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:17:42 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:17:42 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:17:42 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:17:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:17:54 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:17:54 GMT
USER user
# Wed, 15 Apr 2026 20:17:54 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08c5acb2b8849dfbc3ab7dac250bb75028f186bb6733ad7177b937b31f273b8`  
		Last Modified: Wed, 15 Apr 2026 20:18:01 GMT  
		Size: 10.9 MB (10858235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e7a3bff3ec07d78843e225a8924e151e5daea035461282480b5aa821e6705c`  
		Last Modified: Wed, 15 Apr 2026 20:18:00 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0cf822c89aa3e74cb489830e51d76afc9215694e4c95d4ff6b22e5982f04c4`  
		Last Modified: Wed, 15 Apr 2026 20:18:01 GMT  
		Size: 6.1 MB (6063568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:bf8012819911dfaf56515374f681f893249b0db11ddd7bea57fa25dc0a2d09d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1324284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaae6d9d2d8688519f9df33930928011c4010b1179c24d66b7d4b44adda0a44d`

```dockerfile
```

-	Layers:
	-	`sha256:a6f70f031073a0bee5df5e94871c9c0e0c72ea88c339f9eb2a86e4dc33ac5ab9`  
		Last Modified: Wed, 15 Apr 2026 20:18:01 GMT  
		Size: 1.3 MB (1306784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c573c6f83781d7801716b88a5047725f6e4c824b5986b91bb98255f8a226a1c9`  
		Last Modified: Wed, 15 Apr 2026 20:18:00 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:32a993e3ad9b91e98d7f9d895a4c4b5e2b10818f155823c0654cab147d4e8b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19538989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca1094867198ce0d1a87bf43e35e11da52d537622882aff5f2c2f6b54d9b6c2`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:52 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:17:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:17:52 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:18:09 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:18:09 GMT
USER user
# Wed, 15 Apr 2026 20:18:09 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3b91abb913ea5e552d7b0c7347de9ef0c668c74007f3f8d596df4b3285a230`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 10.1 MB (10072770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e1c8790e4fb41f6ece159618adf742aca7b1b3bfb4006b649fa173b52e5d9c`  
		Last Modified: Wed, 15 Apr 2026 20:18:14 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8bc551d614897c5e1f37a1639b18294245230dd66a0c33dc9838839592eadb`  
		Last Modified: Wed, 15 Apr 2026 20:18:14 GMT  
		Size: 5.9 MB (5893373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:f8d5c8034900c66929ae9c22c2b9b1faea245ac7317a6866630af08bacf312e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d310f9907d9f56f5894b2b06bc4efc44434c529351c08426b2cb7dd2074aaab5`

```dockerfile
```

-	Layers:
	-	`sha256:3c700ec9d42a320334d5e286c3c876a4cf0a7152772e7bdcc8d35701849b271f`  
		Last Modified: Wed, 15 Apr 2026 20:18:14 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:8400cca8ce894ce77a70da43d520c1240eddff2930763ffc0372799c186d9121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18831804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ebe844c4e6342061059fcd093f14ed4b366024bff88c6f71a52dfeb7965d7a2`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:53 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:17:53 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:17:53 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:17:53 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:17:53 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:18:08 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:18:08 GMT
USER user
# Wed, 15 Apr 2026 20:18:08 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79dec2323c1b616d1815d215235e7214217786ae0cdec9018d33e3353158ebd`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 9.9 MB (9904377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef3d3e089ce4f1f0cdea10454197d4b856179f93b0881b1fbbb2f6d7bbe9752`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e9cf0ea2e20131d951f7eb3c8e90d027f05753b06a06284adfc24591741c25`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 5.6 MB (5643320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:64e02ba7169fe7427d2a843f819239f3bb4c285582557fc4bb8e8f9e9fba3d9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ba9b7cba5ebc56e832b06d9991bcfde287164a0487b199f6ae9318ed139db8`

```dockerfile
```

-	Layers:
	-	`sha256:1013866b449ede3436fa97b85a19bea88d8cbbfe27f2a350005e2b95631571a5`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 1.3 MB (1309192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cea2f3499ce7de5710ce312145acb7bae5b22bdfcf5875b6a84b6aefae38443a`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 17.6 KB (17632 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:7b9894af2ad3e75a6b5e643c310b097562a2a87c60247f4c0de46b219a0ea5de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20932992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b723908ef497f2f1786ea7c7a4b275b9864bd678863136e6a6c6ae49f5c87e0`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:03 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:16:03 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:16:03 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:16:03 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:16:03 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:16:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:16:17 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:16:17 GMT
USER user
# Wed, 15 Apr 2026 20:16:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3764ce07cb9fb07911422ef3e80f2f06c0f31c885113098ec8b13c160905b584`  
		Last Modified: Wed, 15 Apr 2026 20:16:24 GMT  
		Size: 10.8 MB (10795637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1634788c728d67c110d9d4e0c15ae13b2e6b7a80a77ff3a878345213d581ce`  
		Last Modified: Wed, 15 Apr 2026 20:16:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e07c53b7b681fdb25c1b58692718b42d2cc2b31317e0ece3b3c0c380d809367`  
		Last Modified: Wed, 15 Apr 2026 20:16:24 GMT  
		Size: 5.9 MB (5936500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:52701cb1c00bb28d537acde50c49ef4784ec8a482bdd8478cce4e7bd572ee4b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2179829906c4a8910ab9e20abad2f943a493fca28c0be75620b92566a742e914`

```dockerfile
```

-	Layers:
	-	`sha256:dfcef6d50e20c567b12b21284967f6ae37c8a2073fd8fe387f4aec8cb1483826`  
		Last Modified: Wed, 15 Apr 2026 20:16:24 GMT  
		Size: 1.3 MB (1306238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62d84bee390fe98a360de40e03f2681e268921c47765fa679b33ee75fc08b6af`  
		Last Modified: Wed, 15 Apr 2026 20:16:23 GMT  
		Size: 17.7 KB (17681 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; 386

```console
$ docker pull irssi@sha256:b3be93716c332caea0efd0046cc0e1bec7c1869fca4821e1789e1042607652c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20226813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9806f375f632e375cc393636cd0cf194e1417b55dc702350b1c7e989df95f3bf`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:20:48 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 22:20:48 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 22:20:48 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 22:20:48 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 22:20:48 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 22:21:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 22:21:06 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 22:21:06 GMT
USER user
# Wed, 15 Apr 2026 22:21:06 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1b20561f93fbd784885928a7bdc5496cc351d13ba590d7677906e332db7dfe`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 10.4 MB (10390987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2899b7c728e3786919f78f216c3cc06314662cc7a39aaa46d5a6e52c3df73c`  
		Last Modified: Wed, 15 Apr 2026 22:21:12 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955bacd8728c20067a5cc2b25b87df5ffbc903b6a939de5d0a9c75d647d9fb98`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 6.1 MB (6144398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:93ce05abd87b658f33a303d2ff604976901153ce174e9016ab35726d3014bca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1324183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73fbdcfd6a9387c03db734beaaffcb335ed9ab7289b8e1ea3b676578476a5388`

```dockerfile
```

-	Layers:
	-	`sha256:4ceae1c6bf79b1c1e63914818f6673c06d6ab4174d52fb1f3b7cc2ee1f8ba46b`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 1.3 MB (1306739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d62bef2452b6c6f240a0ca80a588c10c66294d389ea7f48156bf1ed1a446dabf`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:254afdc9663a28ee737288f82d016a19889a7c8754baae69395f2d17bfaff029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21274213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2263772125383f143b80e6be1c94a04db51de28777edaf65099fe747f8e9786`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:51 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:16:52 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:16:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:16:52 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:16:52 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:17:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:17:14 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:17:14 GMT
USER user
# Wed, 15 Apr 2026 20:17:14 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb8acfc73a055a737970c574659149b8b5011cb66a2471181b70b4545ab061d`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 11.1 MB (11080147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04cc343afa57def6717e37a31ebd9c0a3f96cdaab4fcd6fb77fe09d0928a4f60`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2ee35f7d08e3f891969387cf3d54ce04ad6f25b577b354c9dc65861976e82d`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 6.4 MB (6362152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:dd670c211672c1ff7f437ac9de7554f3bb7d5b31aee4bc25d2f6daac8ada855e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c8985b9021b635d6db90b26530a7142ef977f9ab6b5ee00d73682132aac50f`

```dockerfile
```

-	Layers:
	-	`sha256:61c46e29cea49bdaeb4579b4b32f590dd09ade9f7babb0e92937336be2369626`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 1.3 MB (1306191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e04b155fa69a2f233568615ccf2b447061dba7c85665b73d2f8d13b51f17df5e`  
		Last Modified: Wed, 15 Apr 2026 20:17:28 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:bfb4fc15f5ed90f67fd76e60601a679aceee8d624a9cebb62c3467a053497187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19943959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77108e163255a50f7eb48818727d6199fa18870afa211283ed5c516f65705898`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 23:40:39 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 23:40:40 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 23:40:40 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 23:40:40 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 23:40:40 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 23:44:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 23:44:28 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 23:44:28 GMT
USER user
# Wed, 15 Apr 2026 23:44:28 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3876ea28a626875613089e4c0154d886493d2978e5878febd20db5b52b40d2`  
		Last Modified: Wed, 15 Apr 2026 23:45:31 GMT  
		Size: 10.3 MB (10291169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa98a76790d03a8cc0c25f479195b0c473c021cd143d9fb33022b3e6e2c094d`  
		Last Modified: Wed, 15 Apr 2026 23:45:29 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bf07524a0c6cd9050b930be06bdb1518111677f61a8f28dd8ad0ec0184265c`  
		Last Modified: Wed, 15 Apr 2026 23:45:31 GMT  
		Size: 6.1 MB (6064142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:4cc92eb4b78ca33cac771f363db2ae54762f45f6e734f21a4e01790bcc4daae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9918ab08cc9d848fb7ce9c1ffc1a4ea4e331f579f7c7128a7dc421f604281899`

```dockerfile
```

-	Layers:
	-	`sha256:711cf3d984876c007cd510a22a7ada0bf35ea70a789e863e81db69d9e382a1c8`  
		Last Modified: Wed, 15 Apr 2026 23:45:29 GMT  
		Size: 1.3 MB (1306187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c69a7d6857546446e8284d168ca983d23255b2a89e9403e525b1ecdfa308d70`  
		Last Modified: Wed, 15 Apr 2026 23:45:28 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:3c8ece34a2fcdfcfe9d06fcb0c9cecb6620f3df146180789497f2f60e6ec9cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21334454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424937e538e09808772e1c933bdfc98f7e1246703af88eeb73a8546ff78898ca`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:14:38 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:14:38 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:14:38 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:14:38 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:14:38 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:15:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:15:00 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:15:00 GMT
USER user
# Wed, 15 Apr 2026 20:15:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039c6078db85a63371a551471eed0c3ca92837a3efae9929f759f4f2ab304005`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 11.4 MB (11403564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c23488248c4834815a024dac0287469c4e0c3f509e1d6601dad9ebba3ae064`  
		Last Modified: Wed, 15 Apr 2026 20:15:15 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9692f8d5135249c4b910046ab77a1a059df863ff0a74b77329ad64f860e74aae`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 6.2 MB (6203373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:90fa0fa19724af68aca64e6da748c22d2673878a7982be79fbcd5e5457ff42ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18dfc948454050fdc29c101ca6089e0da0689c3259f3e6903686df6ea40ece0c`

```dockerfile
```

-	Layers:
	-	`sha256:8bee6112489a71896cbc2c463f534c78d0bda9c15d98e590ca17ab900f0a7661`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 1.3 MB (1306133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11e2ba4990565e2b2c96183c5443f41b0a2c2c8e498c6bcb7d6e476180234cef`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 17.5 KB (17499 bytes)  
		MIME: application/vnd.in-toto+json
