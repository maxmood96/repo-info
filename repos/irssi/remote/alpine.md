## `irssi:alpine`

```console
$ docker pull irssi@sha256:9abb791afa484b4b3144018d2cd798b3dbe5688516d771210099bf619324e129
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

### `irssi:alpine` - linux; amd64

```console
$ docker pull irssi@sha256:79efb9e01efac0d1d1a5f225bd570bde558b5fed49f147eeb0c8bcf427f51bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20781281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a68443653df5b42be54eb83627f652ad3bfa6584732d97fba8f1769b11a2903`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 21:11:48 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 04 Dec 2025 21:11:48 GMT
ENV HOME=/home/user
# Thu, 04 Dec 2025 21:11:48 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 04 Dec 2025 21:11:48 GMT
ENV LANG=C.UTF-8
# Thu, 04 Dec 2025 21:11:48 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 04 Dec 2025 21:12:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 04 Dec 2025 21:12:01 GMT
WORKDIR /home/user
# Thu, 04 Dec 2025 21:12:01 GMT
USER user
# Thu, 04 Dec 2025 21:12:01 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24fa260809d9cf5463ec91affa612416596810d1c3d238a93a6bcee207f2c258`  
		Last Modified: Thu, 04 Dec 2025 21:12:28 GMT  
		Size: 10.9 MB (10857914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6259b533c9268650af74d632dea91c9804f432a3ba18f78205b22f49cf1668df`  
		Last Modified: Thu, 04 Dec 2025 21:12:27 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b3619b1955c16ada90f9a87e4574e132ece333124b43e37f4b04d991fce8cd`  
		Last Modified: Thu, 04 Dec 2025 21:12:28 GMT  
		Size: 6.1 MB (6063068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:e2f49780d95472e16b74402530ab1419b5bed69c32f1ecd6f7bb75e9198fd563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b61f249f14b597f69ad67bfd38873cac2dc7d10b825eb670de61d2c95b1cf819`

```dockerfile
```

-	Layers:
	-	`sha256:50b01be0a02be9648fe0cd60b67bc02abe2115de1e7e7c6995f6b0612d2e526f`  
		Last Modified: Thu, 04 Dec 2025 23:59:49 GMT  
		Size: 1.3 MB (1308739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e13bdb06554bf5bb3bff339d99263a06d1292ea0cfe2be65631625079abb9916`  
		Last Modified: Thu, 04 Dec 2025 23:59:50 GMT  
		Size: 17.5 KB (17499 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:9145387d5ee72fd4bb653359de5576dce8f0f662b7c188bcac72f6509f57d703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19537337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51a6bbf18db15f35e87356cf2355a347b861e1998a8d683a45ada212347ec9e1`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 21:11:42 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 04 Dec 2025 21:11:42 GMT
ENV HOME=/home/user
# Thu, 04 Dec 2025 21:11:42 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 04 Dec 2025 21:11:42 GMT
ENV LANG=C.UTF-8
# Thu, 04 Dec 2025 21:11:42 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 04 Dec 2025 21:12:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 04 Dec 2025 21:12:01 GMT
WORKDIR /home/user
# Thu, 04 Dec 2025 21:12:01 GMT
USER user
# Thu, 04 Dec 2025 21:12:01 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602920dff7d7b6fb01ece900a97cb395060a299bcc43f34970501d319adff6a0`  
		Last Modified: Thu, 04 Dec 2025 21:12:17 GMT  
		Size: 10.1 MB (10075552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e501552b50d5e83730bd6dc91e0ac578aded351a70d8b086facdc3dac5bf12ef`  
		Last Modified: Thu, 04 Dec 2025 21:12:15 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da3bef7fe89788b53b2417a0cf2f9ff1792a7288acf85ae4a7b034518564eee`  
		Last Modified: Thu, 04 Dec 2025 21:12:16 GMT  
		Size: 5.9 MB (5892906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:46d88f2f3252f1fb8ab82831e11aa6c39953ae9253cf7ebc6454c252942528fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f9f52a0053fb0e18f3b3e5178faab9ad8cad392521cb3ba8c4705e041ee44d`

```dockerfile
```

-	Layers:
	-	`sha256:3e89352384f64d60603ac440b628397387f63cd07de6cdafc27148393a3cf529`  
		Last Modified: Thu, 04 Dec 2025 23:59:53 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:1b8f5e99294e7a1d3e755a581820b627073238439f6668926f9090661017766c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18825086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:330c8d49fed423f1d3285e26e8a2e2d54f4334085950032d617c540120c2452f`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 21:11:58 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 04 Dec 2025 21:11:58 GMT
ENV HOME=/home/user
# Thu, 04 Dec 2025 21:11:58 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 04 Dec 2025 21:11:58 GMT
ENV LANG=C.UTF-8
# Thu, 04 Dec 2025 21:11:58 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 04 Dec 2025 21:12:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 04 Dec 2025 21:12:13 GMT
WORKDIR /home/user
# Thu, 04 Dec 2025 21:12:13 GMT
USER user
# Thu, 04 Dec 2025 21:12:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e690a6ab730fd8cc183f316c2fd0dd8b5027b545bcbbfa41712d817592fe50e8`  
		Last Modified: Thu, 04 Dec 2025 21:12:34 GMT  
		Size: 9.9 MB (9902443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d1dd6ae30fc398585b44251f00a6c6a059dd1b09c7c0444ee729e5693ab071`  
		Last Modified: Thu, 04 Dec 2025 21:12:34 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf59b7441f43312089986e774c984d3b27b0843cfae31e5d06c6f745fdd98cf6`  
		Last Modified: Thu, 04 Dec 2025 21:12:34 GMT  
		Size: 5.6 MB (5643194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:147e0e155fa87f35716fdc1d450f0951aa18e19416b6b71a4302a93293caa86e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1328781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ceefe792cb50642bc8ac1962c3b10b6b8a082488da75e7d7b22523cec89eed`

```dockerfile
```

-	Layers:
	-	`sha256:e0aed9ab672358aa900b45073c11e8ac8922a0b47b4c73358ef2c6ef1212537d`  
		Last Modified: Thu, 04 Dec 2025 23:59:56 GMT  
		Size: 1.3 MB (1311147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31b3b0e812607f99b01e0e890cf4f504a9be72d6a28ede8f5bf68b0c3a58dc0d`  
		Last Modified: Thu, 04 Dec 2025 23:59:57 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:8e438800eb2ff8849e05c6a68400420c1e517c4125c6c0c65d12903bd3df75e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20925214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b695a5184d69482a7155a9a1d40ec88fc67d059b188e52b12a18694fa8073f9a`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 21:12:05 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 04 Dec 2025 21:12:06 GMT
ENV HOME=/home/user
# Thu, 04 Dec 2025 21:12:06 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 04 Dec 2025 21:12:06 GMT
ENV LANG=C.UTF-8
# Thu, 04 Dec 2025 21:12:06 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 04 Dec 2025 21:12:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 04 Dec 2025 21:12:18 GMT
WORKDIR /home/user
# Thu, 04 Dec 2025 21:12:18 GMT
USER user
# Thu, 04 Dec 2025 21:12:18 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf4f7615786f885ecd7d8a65c53193770c5e8838be874c0e352234997dfdbda`  
		Last Modified: Thu, 04 Dec 2025 21:12:47 GMT  
		Size: 10.8 MB (10792784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311efc7a3452cf16c7ddf0328230a6748d62f6150b95f8b8e1e2faa5823e920c`  
		Last Modified: Thu, 04 Dec 2025 21:12:44 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3360d9175d50908c8f955f1d2d2e9b3d537df5aa83925889bc827644227e4f44`  
		Last Modified: Thu, 04 Dec 2025 21:12:45 GMT  
		Size: 5.9 MB (5936246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:5cb068e93ece9bf2d27f829b13188247f131d37949bffbef1e32f9b420c1995b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0dfb4a3e1fa431ddde8cb04e1d30c762f55d79363b133abeb8da755a2dfbba`

```dockerfile
```

-	Layers:
	-	`sha256:68810644a1bde26ea40316c2082eaa350a6f207c830b3ea59a56b5f517af0766`  
		Last Modified: Fri, 05 Dec 2025 00:00:00 GMT  
		Size: 1.3 MB (1308193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff7c66ca22bfe5ffaa94573d2ea734ea9ffa631be83ec439d1224bb0f49aa66e`  
		Last Modified: Fri, 05 Dec 2025 00:00:01 GMT  
		Size: 17.7 KB (17682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; 386

```console
$ docker pull irssi@sha256:c0bee0c5eb8325950f87e9195512d5261894b9ce2048096029c3882413a69a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20224576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66858948c02037ea29334d9368264a968ed1356c09229bfc26fa3454cbdbc3e`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 21:11:59 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 04 Dec 2025 21:11:59 GMT
ENV HOME=/home/user
# Thu, 04 Dec 2025 21:11:59 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 04 Dec 2025 21:11:59 GMT
ENV LANG=C.UTF-8
# Thu, 04 Dec 2025 21:11:59 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 04 Dec 2025 21:12:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 04 Dec 2025 21:12:17 GMT
WORKDIR /home/user
# Thu, 04 Dec 2025 21:12:17 GMT
USER user
# Thu, 04 Dec 2025 21:12:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3527b4f952d5950d8caa74dc0d1759215000f2f0a195344f0239c7e2805fe2fc`  
		Last Modified: Wed, 03 Dec 2025 19:30:41 GMT  
		Size: 3.7 MB (3685856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f9ccaf24beeba4455f739496ce8bff12775d46b447a53b8c7a6646f5f6e575`  
		Last Modified: Thu, 04 Dec 2025 21:12:45 GMT  
		Size: 10.4 MB (10393635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7caba418e8b8e55d5dbe7ea5a941ac0daa259fa75a04c95cf41f928eb2b4046`  
		Last Modified: Thu, 04 Dec 2025 21:12:45 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afebaa2811e97d16b1d28e05788a2726b17cd46fde225ab4edb9b2f084f8cbef`  
		Last Modified: Thu, 04 Dec 2025 21:12:46 GMT  
		Size: 6.1 MB (6144101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:ebb7b40291ee096b7c1a8164ee1ba33fb27b4c4519afcbad51c4c380ea6d98cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf6dbd2af1498c3d7a1ee3533cbc11fc8b8d2f6ec3c7e63bb3bd041adff599d`

```dockerfile
```

-	Layers:
	-	`sha256:c41ded1f485b11811fb71817e1c8c31b636d6e28214e4136e718fc0b09cc21fc`  
		Last Modified: Fri, 05 Dec 2025 00:00:12 GMT  
		Size: 1.3 MB (1308694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24293e335f121711abdca45e94004614209845dac3a95d100f6a54082b37d0ba`  
		Last Modified: Fri, 05 Dec 2025 00:00:13 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:0f1628405a73324c6ed803e6cfd28a9f6e938f148e9648283f2ea920c25b0412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21269753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beef4873975a264c13a0d691cda7a687a378e79f3ab398a7b3ecb10a84963a0b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 21:11:07 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 04 Dec 2025 21:11:08 GMT
ENV HOME=/home/user
# Thu, 04 Dec 2025 21:11:08 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 04 Dec 2025 21:11:08 GMT
ENV LANG=C.UTF-8
# Thu, 04 Dec 2025 21:11:08 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 04 Dec 2025 21:11:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 04 Dec 2025 21:11:35 GMT
WORKDIR /home/user
# Thu, 04 Dec 2025 21:11:35 GMT
USER user
# Thu, 04 Dec 2025 21:11:35 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9905f119264b8ccef15280ffa7c050fc9bb03f777fb151bab2c9ff1296db54a5`  
		Last Modified: Thu, 04 Dec 2025 21:12:06 GMT  
		Size: 11.1 MB (11079705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c04c0f90cd8237ce493465a9e31d48ed6faab0f95240ca2d438886a8b8a20e6`  
		Last Modified: Thu, 04 Dec 2025 21:12:05 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c74d7d37f0dc728b1779021b2ef680c3bf1b1c34cd4a603e614e544806c2621`  
		Last Modified: Thu, 04 Dec 2025 21:12:06 GMT  
		Size: 6.4 MB (6362047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:a5e9e5db611970b00899f2c6d9b87707a4898d01e80402525bb5d359834407c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a7a5c4c319d6d99528a01c0d28968033a5272dec5dd29d5d4675be20c9f6d4`

```dockerfile
```

-	Layers:
	-	`sha256:88187f93cc7d864bab30c53d306252ac8f6a97caee765a0c0113d19e6255dcac`  
		Last Modified: Fri, 05 Dec 2025 00:00:17 GMT  
		Size: 1.3 MB (1308146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6bd61dabe0b6bd38aefe1101a7e4ad37e9c7788c8525077cf77ddba8f924cc8`  
		Last Modified: Fri, 05 Dec 2025 00:00:18 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:b51c6dd96d591d049fd831c218d1b0067e833232347979d875e6b553dbb55dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19940645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:950ddd46f3defc3af429d60be35120e2c88d8412ad26308084c4b0e512fe07d4`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Fri, 05 Dec 2025 02:23:19 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 05 Dec 2025 02:23:20 GMT
ENV HOME=/home/user
# Fri, 05 Dec 2025 02:23:20 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Dec 2025 02:23:20 GMT
ENV LANG=C.UTF-8
# Fri, 05 Dec 2025 02:23:20 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Dec 2025 02:27:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 05 Dec 2025 02:27:11 GMT
WORKDIR /home/user
# Fri, 05 Dec 2025 02:27:11 GMT
USER user
# Fri, 05 Dec 2025 02:27:11 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2433c7ad7b3646a740a7eae28741a65c17ddefb633720b81c0ad01930564940`  
		Last Modified: Fri, 05 Dec 2025 02:28:12 GMT  
		Size: 10.3 MB (10291935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74200693db2c71da95a13b4ce82d1d83ef41bdc712e3b64488a69928d6dbf225`  
		Last Modified: Fri, 05 Dec 2025 02:28:09 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63946db1d94babbacf79d6f59ca8dcdfb7ac9837b2a8832a1de71a1d0c7cfcbb`  
		Last Modified: Fri, 05 Dec 2025 02:28:10 GMT  
		Size: 6.1 MB (6064207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:806bf6472ab9376ae91ff7a3fff3b59307151f22497af2b96110e8ca13ecd9d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d115ddff3738ea92b66b3a384b196554820888fd0d431bd5d9b9260d26797eea`

```dockerfile
```

-	Layers:
	-	`sha256:bc5fd96d52fb45ce4ae0dba6ff0a117c6e3c99b311642d5619242f0d7c096ed9`  
		Last Modified: Fri, 05 Dec 2025 05:59:41 GMT  
		Size: 1.3 MB (1308142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:365607a9c3c292b36bde1aa841851b924c3a341d76ca262ec76ca3fb6fbaff0c`  
		Last Modified: Fri, 05 Dec 2025 05:59:43 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; s390x

```console
$ docker pull irssi@sha256:e12e758bc5aa9a99981c4d2688b16f61c2a0e7ed34020c5e14299218983dec27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21332926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2c43034c5ede74a33f9a9fd008146d029308e1d82ff91eebc47d705aa0e6be9`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 21:11:11 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 04 Dec 2025 21:11:12 GMT
ENV HOME=/home/user
# Thu, 04 Dec 2025 21:11:12 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 04 Dec 2025 21:11:12 GMT
ENV LANG=C.UTF-8
# Thu, 04 Dec 2025 21:11:12 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 04 Dec 2025 21:11:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 04 Dec 2025 21:12:03 GMT
WORKDIR /home/user
# Thu, 04 Dec 2025 21:12:03 GMT
USER user
# Thu, 04 Dec 2025 21:12:03 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bbe1294bf0a9dfd59f3d5a77e576938b23fa2cb4172e5002f7bfa79b7a2aba`  
		Last Modified: Thu, 04 Dec 2025 21:13:06 GMT  
		Size: 11.4 MB (11404890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51597b97e50cb63e1d686a257b41981c6d2c082665a14361864231d31a3b0355`  
		Last Modified: Thu, 04 Dec 2025 21:13:05 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9db9be19ab701b40ff18f74c6c2fc270801230c588b5631a90565c2c96f8a6`  
		Last Modified: Thu, 04 Dec 2025 21:13:06 GMT  
		Size: 6.2 MB (6203243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:f112609f6390c8de823800c4b28ef46aae8abfec9bc8d7d934e291e69d236b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09e61d06c61275ece3ef74e19ae1ded709b228b73759e6b5c02ea338d595455`

```dockerfile
```

-	Layers:
	-	`sha256:c131707d8746e565e070eba0c8be606d40a3d2478f3e54a5d39e7ac77e5c77b8`  
		Last Modified: Fri, 05 Dec 2025 00:00:22 GMT  
		Size: 1.3 MB (1308088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef01364ad69e574266d1ab766919f6791a04e91afdbec4bedec87461d560535f`  
		Last Modified: Fri, 05 Dec 2025 00:00:23 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json
