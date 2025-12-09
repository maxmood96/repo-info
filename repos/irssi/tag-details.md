<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `irssi`

-	[`irssi:1`](#irssi1)
-	[`irssi:1-alpine`](#irssi1-alpine)
-	[`irssi:1-alpine3.23`](#irssi1-alpine323)
-	[`irssi:1-trixie`](#irssi1-trixie)
-	[`irssi:1.4`](#irssi14)
-	[`irssi:1.4-alpine`](#irssi14-alpine)
-	[`irssi:1.4-alpine3.23`](#irssi14-alpine323)
-	[`irssi:1.4-trixie`](#irssi14-trixie)
-	[`irssi:1.4.5`](#irssi145)
-	[`irssi:1.4.5-alpine`](#irssi145-alpine)
-	[`irssi:1.4.5-alpine3.23`](#irssi145-alpine323)
-	[`irssi:1.4.5-trixie`](#irssi145-trixie)
-	[`irssi:alpine`](#irssialpine)
-	[`irssi:alpine3.23`](#irssialpine323)
-	[`irssi:latest`](#irssilatest)
-	[`irssi:trixie`](#irssitrixie)

## `irssi:1`

```console
$ docker pull irssi@sha256:19043dddac4df97572295eb4df56b6e5e8d1244a09ece798931a7e728e2099b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
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

### `irssi:1` - linux; amd64

```console
$ docker pull irssi@sha256:ba548a27a12441efe110f9a056e793d722bda4a4eb13a3ceea8bf8d2d5ac1e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53869300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ebb967af1ef6016f39c7253143525ae93880628cdbc3e189772a2d029fc1a25`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:37:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:37:12 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:37:12 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:37:12 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:37:12 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:37:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:37:51 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:37:51 GMT
USER user
# Mon, 08 Dec 2025 22:37:51 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae9ff25045243dc27c083564f101c73527fab1e4d6de25faafe1d20c6993d0f`  
		Last Modified: Mon, 08 Dec 2025 22:38:10 GMT  
		Size: 19.2 MB (19222767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cff4c278980a41219ced1054076473f352a9ab538703fdb0508673575901de`  
		Last Modified: Mon, 08 Dec 2025 22:38:08 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6979d38c29179b5f4797ac48f3389f2044fb0312d0cd3b7f7fe377d41762cf9c`  
		Last Modified: Mon, 08 Dec 2025 22:38:08 GMT  
		Size: 4.9 MB (4866682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:2c34f0b8bd4789c746b87fcefbeca5053bc49367fbe0106f8c1f2c5df4510d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aec691ef1c3f8b1f097d426de19c51fc9a39bcd3002cf27303c6ea181155e87`

```dockerfile
```

-	Layers:
	-	`sha256:ea7448fd69d2025a02fa3773b13695b9ecaa34efd8cc5b223bd340a6a20bb280`  
		Last Modified: Tue, 09 Dec 2025 00:01:32 GMT  
		Size: 5.6 MB (5588377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15055f679734606495e25ae5c7b68d5ee1ec2609bfbca41b8eccfdc0431ef6dd`  
		Last Modified: Tue, 09 Dec 2025 00:01:32 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v5

```console
$ docker pull irssi@sha256:605f1644cbe09985d1b0a7159e6a3645cacce33a561adb3eb3994e2bb9fe1118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50943555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d5500fde47056d160fcf131159d65be22e1cce50911f44d2f5be15fc113c99`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:33:53 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:33:53 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:33:53 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:33:53 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:34:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:34:44 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:34:44 GMT
USER user
# Mon, 08 Dec 2025 22:34:44 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209b020e9b6936d49088aeb2fe32da563e0dc7240b53e7a4f55a0064bcc57dbb`  
		Last Modified: Mon, 08 Dec 2025 22:35:02 GMT  
		Size: 18.3 MB (18286366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e546d6b1c1001d996e09271aa06076bbf5076bf4c0f1a64a5a76db18e6351b32`  
		Last Modified: Mon, 08 Dec 2025 22:34:59 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c1c60a78876ca8d26fa893a37ff13080f097555eea972e3e45e59d912f5e9c`  
		Last Modified: Mon, 08 Dec 2025 22:35:00 GMT  
		Size: 4.7 MB (4709641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:42ce2f56fd00643a382954ddf368a7ad26f88a053b4a557aa1112ed9de67aac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192e3247c9d1fd1e403f1da43c465327ebe5a123a9caf785ea53b5dd0388c5cb`

```dockerfile
```

-	Layers:
	-	`sha256:dbd5f23d6f6d5ab003eddef0af01a8a8b66fac74afe90d0faa97afa2b0a581d2`  
		Last Modified: Tue, 09 Dec 2025 00:01:40 GMT  
		Size: 5.6 MB (5585926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:401ba355602555e19652809e181e8fc4d172d2140c0c17f0781b909a2bff847e`  
		Last Modified: Tue, 09 Dec 2025 00:01:41 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v7

```console
$ docker pull irssi@sha256:90bf141f8448f931b78a4759623391882ba8d3d0520b3770b063ea80daf29ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48681035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d9f126abb644aa91708596fe16f433c339727d7b73386dc26994eb1d0119af6`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:36:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:36:55 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:36:55 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:36:55 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:36:55 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:37:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:37:36 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:37:36 GMT
USER user
# Mon, 08 Dec 2025 22:37:36 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea7a0e9121517502a0452fd53a68bbbf3e120ea0391f4616c22058f3ffe83a6`  
		Last Modified: Mon, 08 Dec 2025 22:37:54 GMT  
		Size: 17.9 MB (17909125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a98b78793ec14ceabf793c4778fa9c59358545e4604a1c0b15bb6bd21bd755`  
		Last Modified: Mon, 08 Dec 2025 22:37:52 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c7e9fbcbad6965518fd24946faf5855bd7c2b9dbb7a8632a912292a76f391b`  
		Last Modified: Mon, 08 Dec 2025 22:37:53 GMT  
		Size: 4.6 MB (4558538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:529cccf10215bb411a271b196fe666e44db36c0c88bc62b754ae778cc278ef86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5070cb3b050937bc197ae388f5989122c8e4fc9558708e5cd01f7eb53047ec85`

```dockerfile
```

-	Layers:
	-	`sha256:82a650d25d6be9c0ec73d583a9bfbb7e4cdf26f7eac9d4a2c0b9165043d1c3b1`  
		Last Modified: Tue, 09 Dec 2025 00:01:47 GMT  
		Size: 5.6 MB (5588948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b12cb7447938f917d5345ecf33832b856ff04c97a5f9c2213b71e0a7d45d3fcc`  
		Last Modified: Tue, 09 Dec 2025 00:01:47 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:4ad94477cda90ae8d3d4d47ed0c1a58d162ca780cbc21e1e356ae833c2c9af51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53972792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6123fcf7ac4efb210283b7fab07ab5e1f866bcfa7ad8dbd2186bd66c2f88d4b2`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:35:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:35:56 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:35:56 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:35:56 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:35:56 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:36:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:36:32 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:36:32 GMT
USER user
# Mon, 08 Dec 2025 22:36:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271cd4b9332a86de31690e94a837946ec81b376cf3b99b9ec078b9997ebfc4e7`  
		Last Modified: Mon, 08 Dec 2025 22:36:51 GMT  
		Size: 19.0 MB (19049077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f51515c1d0d0bdda82745487e18f18f85d1a6999f3c82ff517039ed8c01ae9`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae317866ab39c091f9ece44d604dc3317877b2ed386b1ff38dcf25d62707f6e`  
		Last Modified: Mon, 08 Dec 2025 22:36:50 GMT  
		Size: 4.8 MB (4781724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:8a9848973ad593c402ad00791b8debf829808115d9215d351a4d092da9efdfb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e8e14ea45e56f1a280745e4215d6b09bf3bbe98d77d25ed701e1833b69db94`

```dockerfile
```

-	Layers:
	-	`sha256:833298ea4b4e32cd4be350f01f29cc972db0aa5f1e1b52c229e9611870f9d81d`  
		Last Modified: Tue, 09 Dec 2025 00:01:51 GMT  
		Size: 5.6 MB (5594861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12ec53196ee839e1d4fc9f760637572995c6cf92c75585cdf8a0ddebd72fd86a`  
		Last Modified: Tue, 09 Dec 2025 00:01:52 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; 386

```console
$ docker pull irssi@sha256:e3cb55074f79f7accb3186e087c8bcfbe5fb81bafed6b3843bbb182b831c2271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede6324a485fc1c56152548ccc95aa525d3e6298b82206a635b9e5bb2c43a274`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:34:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:34:50 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:34:50 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:34:50 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:34:50 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:35:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:35:33 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:35:33 GMT
USER user
# Mon, 08 Dec 2025 22:35:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92779a84b492a0e3f9b30abe3ba2c3f3c75f5f8bac0be5b3ec6f1d2151769a81`  
		Last Modified: Mon, 08 Dec 2025 22:35:51 GMT  
		Size: 18.7 MB (18740473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9e00516c012835613d2d6c24e48eca1db4092e2ae02a5557ef978565a9087b`  
		Last Modified: Mon, 08 Dec 2025 22:35:49 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380f851f46dcf6024e273c5690f4de14d4837fe4c9e173048edc3844675aefad`  
		Last Modified: Mon, 08 Dec 2025 22:35:49 GMT  
		Size: 4.9 MB (4868342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:0e026c9c8b43f1e4b3f0cf84c29441b70414ab67d248c56ebf7607efd867af5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c110c8c5132d6b986eca5007cb21a2921c655197298f96c1e6e3fe1d975295ce`

```dockerfile
```

-	Layers:
	-	`sha256:290278e5fa9964615268f167ae0917568dd48529eb40cb0fe4b7b6b4fd6db490`  
		Last Modified: Tue, 09 Dec 2025 00:01:57 GMT  
		Size: 5.6 MB (5584500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b86870229139d3e4a5b2f5fb461a45c930f312a775c5a1c86c120a2616479b3`  
		Last Modified: Tue, 09 Dec 2025 00:01:58 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; ppc64le

```console
$ docker pull irssi@sha256:93ea18bd78c1073049928098da83c8d7489f034eb6e93242c329dd6ac2f1928b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58240744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5496783653403c6d012d80f5d9f8c7a75a1093b7a1752b8fe2f67c024d71ba30`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:28:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:28:22 GMT
ENV HOME=/home/user
# Tue, 09 Dec 2025 00:28:22 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 09 Dec 2025 00:28:22 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 00:28:22 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 09 Dec 2025 00:30:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 09 Dec 2025 00:30:05 GMT
WORKDIR /home/user
# Tue, 09 Dec 2025 00:30:05 GMT
USER user
# Tue, 09 Dec 2025 00:30:05 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d43ff5db3e76c55de7b73205ca86bac1121de5d0f0c442c6d1fab408d40dbc4`  
		Last Modified: Tue, 09 Dec 2025 00:30:40 GMT  
		Size: 19.5 MB (19543101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20fac790531c01e08ec11e7ea8e6c78bc9732c6dd506329349609d5c47ea56b`  
		Last Modified: Tue, 09 Dec 2025 00:30:38 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e4e19b419b36bd43d3ecbb483048af4910c11c8ed72f86585d17de6a3cf367`  
		Last Modified: Tue, 09 Dec 2025 00:30:41 GMT  
		Size: 5.1 MB (5097391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:fe0f1b60af0b886246c9c854bfba7d6c86f3a936171bfe3afcb3fe3e72177db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aaaf9080eb40d58b04f0eb1b35aacf665d2ab2db092955824c8a40ab7b15d85`

```dockerfile
```

-	Layers:
	-	`sha256:e4b1401322d5b02c67c73ad0a132014ff5d6ebe1d604dbeb9595a74e83201f93`  
		Last Modified: Tue, 09 Dec 2025 02:59:59 GMT  
		Size: 5.6 MB (5595408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e74c10f22046f87919aa9d2d4f9fc0afaed79b0bdbbaad1bf79c689583b0b1c`  
		Last Modified: Tue, 09 Dec 2025 03:00:00 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; riscv64

```console
$ docker pull irssi@sha256:0a17bc9dc7f1ede0aae4d4035aa269c39fdd3ad059158a3c6a569fa2bf7da8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51686196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e6a1bc4c5ae216cf035ec48b010768259be2a066ee4ef066bcb9c32d445e4d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 10:01:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:01:44 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 10:01:44 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 10:01:44 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 10:01:44 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 10:08:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 10:08:36 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 10:08:36 GMT
USER user
# Tue, 18 Nov 2025 10:08:36 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afef2a7493fa326b06e464e36f2a79568e4c5c265515366e193165f0b4d284e`  
		Last Modified: Tue, 18 Nov 2025 10:10:42 GMT  
		Size: 18.5 MB (18549074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f026bbe28877d1917f647dacffd37172e95435e1c7e9fbe30a62986bb72cd62b`  
		Last Modified: Tue, 18 Nov 2025 10:10:41 GMT  
		Size: 3.3 KB (3337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3d248f54be38451080b4d25093d9df5c1c9efe1175c3cf58494a7e0fd7fe62`  
		Last Modified: Tue, 18 Nov 2025 10:10:41 GMT  
		Size: 4.9 MB (4860627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:7b01cdd2258dc9fd9266a05e6cbd264f72886699285f27da4dcfa624dcb82f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afb4ae2e3561846a1f14e41a61390911210a0c9ea6b4f9bace7ef57ca7a1303`

```dockerfile
```

-	Layers:
	-	`sha256:5044523627d968ee0b87912ad5e86b6f374ff85ef9a7878ae77c52dcf5581421`  
		Last Modified: Tue, 18 Nov 2025 18:00:24 GMT  
		Size: 5.6 MB (5579680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43863609ed306f6a1f2ac385d2c41ef9efb115640066a4bb3b02043bb96f7158`  
		Last Modified: Tue, 18 Nov 2025 18:00:25 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; s390x

```console
$ docker pull irssi@sha256:79ceeb6e5f00cadefc5098892f4fdd847c8a6c7147214049af36f2988eb63701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54503098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4447f6a16ef4660d5cc882de4451987df832e0221f3c9198582f5041d9e484`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:33:35 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:33:35 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:33:35 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:33:35 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:34:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:34:10 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:34:10 GMT
USER user
# Mon, 08 Dec 2025 22:34:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a68582eda8cf9c795e8fac7bd4a06d7b4cf05bcce0b996577a486d0e34b56c`  
		Last Modified: Mon, 08 Dec 2025 22:34:33 GMT  
		Size: 19.8 MB (19759448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea7a5c770aac1d19a49e32bddbb9b474dd2746e7821d20791e1b80abfa3b5a3`  
		Last Modified: Mon, 08 Dec 2025 22:34:31 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fe49ac5d532203fa75223786c8c8ef7f78fbdeff8227abdab3b6e08125de53`  
		Last Modified: Mon, 08 Dec 2025 22:34:32 GMT  
		Size: 4.9 MB (4905890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:afc0d5563715a205bdbf09adfb0dcb772d44ec5f9f64be619112ea71bef71370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb41a3e51a7b6c277c4898dede97241725067c20506fcd3897eb9a2fa33ef8fc`

```dockerfile
```

-	Layers:
	-	`sha256:9292a924a5f71b0700ea789b79e1a8bf1256af5aae51b422283563c1fa34bf6e`  
		Last Modified: Tue, 09 Dec 2025 00:02:15 GMT  
		Size: 5.6 MB (5589282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff40bc8ca1364bffe8c60be1df3e2bffedbd27bb8dbcf6db778c754320ccf6e`  
		Last Modified: Tue, 09 Dec 2025 00:02:16 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine`

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

### `irssi:1-alpine` - linux; amd64

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

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

### `irssi:1-alpine` - linux; arm variant v6

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

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

### `irssi:1-alpine` - linux; arm variant v7

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

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

### `irssi:1-alpine` - linux; arm64 variant v8

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

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

### `irssi:1-alpine` - linux; 386

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

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

### `irssi:1-alpine` - linux; ppc64le

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

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

### `irssi:1-alpine` - linux; riscv64

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

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

### `irssi:1-alpine` - linux; s390x

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

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

## `irssi:1-alpine3.23`

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

### `irssi:1-alpine3.23` - linux; amd64

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

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

### `irssi:1-alpine3.23` - linux; arm variant v6

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

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

### `irssi:1-alpine3.23` - linux; arm variant v7

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

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

### `irssi:1-alpine3.23` - linux; arm64 variant v8

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

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

### `irssi:1-alpine3.23` - linux; 386

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

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

### `irssi:1-alpine3.23` - linux; ppc64le

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

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

### `irssi:1-alpine3.23` - linux; riscv64

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

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

### `irssi:1-alpine3.23` - linux; s390x

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

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

## `irssi:1-trixie`

```console
$ docker pull irssi@sha256:19043dddac4df97572295eb4df56b6e5e8d1244a09ece798931a7e728e2099b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
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

### `irssi:1-trixie` - linux; amd64

```console
$ docker pull irssi@sha256:ba548a27a12441efe110f9a056e793d722bda4a4eb13a3ceea8bf8d2d5ac1e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53869300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ebb967af1ef6016f39c7253143525ae93880628cdbc3e189772a2d029fc1a25`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:37:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:37:12 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:37:12 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:37:12 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:37:12 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:37:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:37:51 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:37:51 GMT
USER user
# Mon, 08 Dec 2025 22:37:51 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae9ff25045243dc27c083564f101c73527fab1e4d6de25faafe1d20c6993d0f`  
		Last Modified: Mon, 08 Dec 2025 22:38:10 GMT  
		Size: 19.2 MB (19222767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cff4c278980a41219ced1054076473f352a9ab538703fdb0508673575901de`  
		Last Modified: Mon, 08 Dec 2025 22:38:08 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6979d38c29179b5f4797ac48f3389f2044fb0312d0cd3b7f7fe377d41762cf9c`  
		Last Modified: Mon, 08 Dec 2025 22:38:08 GMT  
		Size: 4.9 MB (4866682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:2c34f0b8bd4789c746b87fcefbeca5053bc49367fbe0106f8c1f2c5df4510d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aec691ef1c3f8b1f097d426de19c51fc9a39bcd3002cf27303c6ea181155e87`

```dockerfile
```

-	Layers:
	-	`sha256:ea7448fd69d2025a02fa3773b13695b9ecaa34efd8cc5b223bd340a6a20bb280`  
		Last Modified: Tue, 09 Dec 2025 00:01:32 GMT  
		Size: 5.6 MB (5588377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15055f679734606495e25ae5c7b68d5ee1ec2609bfbca41b8eccfdc0431ef6dd`  
		Last Modified: Tue, 09 Dec 2025 00:01:32 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:605f1644cbe09985d1b0a7159e6a3645cacce33a561adb3eb3994e2bb9fe1118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50943555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d5500fde47056d160fcf131159d65be22e1cce50911f44d2f5be15fc113c99`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:33:53 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:33:53 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:33:53 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:33:53 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:34:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:34:44 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:34:44 GMT
USER user
# Mon, 08 Dec 2025 22:34:44 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209b020e9b6936d49088aeb2fe32da563e0dc7240b53e7a4f55a0064bcc57dbb`  
		Last Modified: Mon, 08 Dec 2025 22:35:02 GMT  
		Size: 18.3 MB (18286366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e546d6b1c1001d996e09271aa06076bbf5076bf4c0f1a64a5a76db18e6351b32`  
		Last Modified: Mon, 08 Dec 2025 22:34:59 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c1c60a78876ca8d26fa893a37ff13080f097555eea972e3e45e59d912f5e9c`  
		Last Modified: Mon, 08 Dec 2025 22:35:00 GMT  
		Size: 4.7 MB (4709641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:42ce2f56fd00643a382954ddf368a7ad26f88a053b4a557aa1112ed9de67aac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192e3247c9d1fd1e403f1da43c465327ebe5a123a9caf785ea53b5dd0388c5cb`

```dockerfile
```

-	Layers:
	-	`sha256:dbd5f23d6f6d5ab003eddef0af01a8a8b66fac74afe90d0faa97afa2b0a581d2`  
		Last Modified: Tue, 09 Dec 2025 00:01:40 GMT  
		Size: 5.6 MB (5585926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:401ba355602555e19652809e181e8fc4d172d2140c0c17f0781b909a2bff847e`  
		Last Modified: Tue, 09 Dec 2025 00:01:41 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:90bf141f8448f931b78a4759623391882ba8d3d0520b3770b063ea80daf29ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48681035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d9f126abb644aa91708596fe16f433c339727d7b73386dc26994eb1d0119af6`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:36:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:36:55 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:36:55 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:36:55 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:36:55 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:37:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:37:36 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:37:36 GMT
USER user
# Mon, 08 Dec 2025 22:37:36 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea7a0e9121517502a0452fd53a68bbbf3e120ea0391f4616c22058f3ffe83a6`  
		Last Modified: Mon, 08 Dec 2025 22:37:54 GMT  
		Size: 17.9 MB (17909125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a98b78793ec14ceabf793c4778fa9c59358545e4604a1c0b15bb6bd21bd755`  
		Last Modified: Mon, 08 Dec 2025 22:37:52 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c7e9fbcbad6965518fd24946faf5855bd7c2b9dbb7a8632a912292a76f391b`  
		Last Modified: Mon, 08 Dec 2025 22:37:53 GMT  
		Size: 4.6 MB (4558538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:529cccf10215bb411a271b196fe666e44db36c0c88bc62b754ae778cc278ef86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5070cb3b050937bc197ae388f5989122c8e4fc9558708e5cd01f7eb53047ec85`

```dockerfile
```

-	Layers:
	-	`sha256:82a650d25d6be9c0ec73d583a9bfbb7e4cdf26f7eac9d4a2c0b9165043d1c3b1`  
		Last Modified: Tue, 09 Dec 2025 00:01:47 GMT  
		Size: 5.6 MB (5588948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b12cb7447938f917d5345ecf33832b856ff04c97a5f9c2213b71e0a7d45d3fcc`  
		Last Modified: Tue, 09 Dec 2025 00:01:47 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:4ad94477cda90ae8d3d4d47ed0c1a58d162ca780cbc21e1e356ae833c2c9af51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53972792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6123fcf7ac4efb210283b7fab07ab5e1f866bcfa7ad8dbd2186bd66c2f88d4b2`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:35:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:35:56 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:35:56 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:35:56 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:35:56 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:36:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:36:32 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:36:32 GMT
USER user
# Mon, 08 Dec 2025 22:36:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271cd4b9332a86de31690e94a837946ec81b376cf3b99b9ec078b9997ebfc4e7`  
		Last Modified: Mon, 08 Dec 2025 22:36:51 GMT  
		Size: 19.0 MB (19049077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f51515c1d0d0bdda82745487e18f18f85d1a6999f3c82ff517039ed8c01ae9`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae317866ab39c091f9ece44d604dc3317877b2ed386b1ff38dcf25d62707f6e`  
		Last Modified: Mon, 08 Dec 2025 22:36:50 GMT  
		Size: 4.8 MB (4781724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:8a9848973ad593c402ad00791b8debf829808115d9215d351a4d092da9efdfb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e8e14ea45e56f1a280745e4215d6b09bf3bbe98d77d25ed701e1833b69db94`

```dockerfile
```

-	Layers:
	-	`sha256:833298ea4b4e32cd4be350f01f29cc972db0aa5f1e1b52c229e9611870f9d81d`  
		Last Modified: Tue, 09 Dec 2025 00:01:51 GMT  
		Size: 5.6 MB (5594861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12ec53196ee839e1d4fc9f760637572995c6cf92c75585cdf8a0ddebd72fd86a`  
		Last Modified: Tue, 09 Dec 2025 00:01:52 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; 386

```console
$ docker pull irssi@sha256:e3cb55074f79f7accb3186e087c8bcfbe5fb81bafed6b3843bbb182b831c2271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede6324a485fc1c56152548ccc95aa525d3e6298b82206a635b9e5bb2c43a274`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:34:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:34:50 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:34:50 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:34:50 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:34:50 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:35:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:35:33 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:35:33 GMT
USER user
# Mon, 08 Dec 2025 22:35:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92779a84b492a0e3f9b30abe3ba2c3f3c75f5f8bac0be5b3ec6f1d2151769a81`  
		Last Modified: Mon, 08 Dec 2025 22:35:51 GMT  
		Size: 18.7 MB (18740473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9e00516c012835613d2d6c24e48eca1db4092e2ae02a5557ef978565a9087b`  
		Last Modified: Mon, 08 Dec 2025 22:35:49 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380f851f46dcf6024e273c5690f4de14d4837fe4c9e173048edc3844675aefad`  
		Last Modified: Mon, 08 Dec 2025 22:35:49 GMT  
		Size: 4.9 MB (4868342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:0e026c9c8b43f1e4b3f0cf84c29441b70414ab67d248c56ebf7607efd867af5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c110c8c5132d6b986eca5007cb21a2921c655197298f96c1e6e3fe1d975295ce`

```dockerfile
```

-	Layers:
	-	`sha256:290278e5fa9964615268f167ae0917568dd48529eb40cb0fe4b7b6b4fd6db490`  
		Last Modified: Tue, 09 Dec 2025 00:01:57 GMT  
		Size: 5.6 MB (5584500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b86870229139d3e4a5b2f5fb461a45c930f312a775c5a1c86c120a2616479b3`  
		Last Modified: Tue, 09 Dec 2025 00:01:58 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:93ea18bd78c1073049928098da83c8d7489f034eb6e93242c329dd6ac2f1928b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58240744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5496783653403c6d012d80f5d9f8c7a75a1093b7a1752b8fe2f67c024d71ba30`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:28:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:28:22 GMT
ENV HOME=/home/user
# Tue, 09 Dec 2025 00:28:22 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 09 Dec 2025 00:28:22 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 00:28:22 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 09 Dec 2025 00:30:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 09 Dec 2025 00:30:05 GMT
WORKDIR /home/user
# Tue, 09 Dec 2025 00:30:05 GMT
USER user
# Tue, 09 Dec 2025 00:30:05 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d43ff5db3e76c55de7b73205ca86bac1121de5d0f0c442c6d1fab408d40dbc4`  
		Last Modified: Tue, 09 Dec 2025 00:30:40 GMT  
		Size: 19.5 MB (19543101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20fac790531c01e08ec11e7ea8e6c78bc9732c6dd506329349609d5c47ea56b`  
		Last Modified: Tue, 09 Dec 2025 00:30:38 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e4e19b419b36bd43d3ecbb483048af4910c11c8ed72f86585d17de6a3cf367`  
		Last Modified: Tue, 09 Dec 2025 00:30:41 GMT  
		Size: 5.1 MB (5097391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:fe0f1b60af0b886246c9c854bfba7d6c86f3a936171bfe3afcb3fe3e72177db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aaaf9080eb40d58b04f0eb1b35aacf665d2ab2db092955824c8a40ab7b15d85`

```dockerfile
```

-	Layers:
	-	`sha256:e4b1401322d5b02c67c73ad0a132014ff5d6ebe1d604dbeb9595a74e83201f93`  
		Last Modified: Tue, 09 Dec 2025 02:59:59 GMT  
		Size: 5.6 MB (5595408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e74c10f22046f87919aa9d2d4f9fc0afaed79b0bdbbaad1bf79c689583b0b1c`  
		Last Modified: Tue, 09 Dec 2025 03:00:00 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:0a17bc9dc7f1ede0aae4d4035aa269c39fdd3ad059158a3c6a569fa2bf7da8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51686196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e6a1bc4c5ae216cf035ec48b010768259be2a066ee4ef066bcb9c32d445e4d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 10:01:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:01:44 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 10:01:44 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 10:01:44 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 10:01:44 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 10:08:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 10:08:36 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 10:08:36 GMT
USER user
# Tue, 18 Nov 2025 10:08:36 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afef2a7493fa326b06e464e36f2a79568e4c5c265515366e193165f0b4d284e`  
		Last Modified: Tue, 18 Nov 2025 10:10:42 GMT  
		Size: 18.5 MB (18549074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f026bbe28877d1917f647dacffd37172e95435e1c7e9fbe30a62986bb72cd62b`  
		Last Modified: Tue, 18 Nov 2025 10:10:41 GMT  
		Size: 3.3 KB (3337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3d248f54be38451080b4d25093d9df5c1c9efe1175c3cf58494a7e0fd7fe62`  
		Last Modified: Tue, 18 Nov 2025 10:10:41 GMT  
		Size: 4.9 MB (4860627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:7b01cdd2258dc9fd9266a05e6cbd264f72886699285f27da4dcfa624dcb82f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afb4ae2e3561846a1f14e41a61390911210a0c9ea6b4f9bace7ef57ca7a1303`

```dockerfile
```

-	Layers:
	-	`sha256:5044523627d968ee0b87912ad5e86b6f374ff85ef9a7878ae77c52dcf5581421`  
		Last Modified: Tue, 18 Nov 2025 18:00:24 GMT  
		Size: 5.6 MB (5579680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43863609ed306f6a1f2ac385d2c41ef9efb115640066a4bb3b02043bb96f7158`  
		Last Modified: Tue, 18 Nov 2025 18:00:25 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; s390x

```console
$ docker pull irssi@sha256:79ceeb6e5f00cadefc5098892f4fdd847c8a6c7147214049af36f2988eb63701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54503098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4447f6a16ef4660d5cc882de4451987df832e0221f3c9198582f5041d9e484`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:33:35 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:33:35 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:33:35 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:33:35 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:34:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:34:10 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:34:10 GMT
USER user
# Mon, 08 Dec 2025 22:34:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a68582eda8cf9c795e8fac7bd4a06d7b4cf05bcce0b996577a486d0e34b56c`  
		Last Modified: Mon, 08 Dec 2025 22:34:33 GMT  
		Size: 19.8 MB (19759448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea7a5c770aac1d19a49e32bddbb9b474dd2746e7821d20791e1b80abfa3b5a3`  
		Last Modified: Mon, 08 Dec 2025 22:34:31 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fe49ac5d532203fa75223786c8c8ef7f78fbdeff8227abdab3b6e08125de53`  
		Last Modified: Mon, 08 Dec 2025 22:34:32 GMT  
		Size: 4.9 MB (4905890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:afc0d5563715a205bdbf09adfb0dcb772d44ec5f9f64be619112ea71bef71370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb41a3e51a7b6c277c4898dede97241725067c20506fcd3897eb9a2fa33ef8fc`

```dockerfile
```

-	Layers:
	-	`sha256:9292a924a5f71b0700ea789b79e1a8bf1256af5aae51b422283563c1fa34bf6e`  
		Last Modified: Tue, 09 Dec 2025 00:02:15 GMT  
		Size: 5.6 MB (5589282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff40bc8ca1364bffe8c60be1df3e2bffedbd27bb8dbcf6db778c754320ccf6e`  
		Last Modified: Tue, 09 Dec 2025 00:02:16 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4`

```console
$ docker pull irssi@sha256:19043dddac4df97572295eb4df56b6e5e8d1244a09ece798931a7e728e2099b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
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

### `irssi:1.4` - linux; amd64

```console
$ docker pull irssi@sha256:ba548a27a12441efe110f9a056e793d722bda4a4eb13a3ceea8bf8d2d5ac1e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53869300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ebb967af1ef6016f39c7253143525ae93880628cdbc3e189772a2d029fc1a25`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:37:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:37:12 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:37:12 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:37:12 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:37:12 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:37:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:37:51 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:37:51 GMT
USER user
# Mon, 08 Dec 2025 22:37:51 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae9ff25045243dc27c083564f101c73527fab1e4d6de25faafe1d20c6993d0f`  
		Last Modified: Mon, 08 Dec 2025 22:38:10 GMT  
		Size: 19.2 MB (19222767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cff4c278980a41219ced1054076473f352a9ab538703fdb0508673575901de`  
		Last Modified: Mon, 08 Dec 2025 22:38:08 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6979d38c29179b5f4797ac48f3389f2044fb0312d0cd3b7f7fe377d41762cf9c`  
		Last Modified: Mon, 08 Dec 2025 22:38:08 GMT  
		Size: 4.9 MB (4866682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:2c34f0b8bd4789c746b87fcefbeca5053bc49367fbe0106f8c1f2c5df4510d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aec691ef1c3f8b1f097d426de19c51fc9a39bcd3002cf27303c6ea181155e87`

```dockerfile
```

-	Layers:
	-	`sha256:ea7448fd69d2025a02fa3773b13695b9ecaa34efd8cc5b223bd340a6a20bb280`  
		Last Modified: Tue, 09 Dec 2025 00:01:32 GMT  
		Size: 5.6 MB (5588377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15055f679734606495e25ae5c7b68d5ee1ec2609bfbca41b8eccfdc0431ef6dd`  
		Last Modified: Tue, 09 Dec 2025 00:01:32 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v5

```console
$ docker pull irssi@sha256:605f1644cbe09985d1b0a7159e6a3645cacce33a561adb3eb3994e2bb9fe1118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50943555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d5500fde47056d160fcf131159d65be22e1cce50911f44d2f5be15fc113c99`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:33:53 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:33:53 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:33:53 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:33:53 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:34:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:34:44 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:34:44 GMT
USER user
# Mon, 08 Dec 2025 22:34:44 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209b020e9b6936d49088aeb2fe32da563e0dc7240b53e7a4f55a0064bcc57dbb`  
		Last Modified: Mon, 08 Dec 2025 22:35:02 GMT  
		Size: 18.3 MB (18286366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e546d6b1c1001d996e09271aa06076bbf5076bf4c0f1a64a5a76db18e6351b32`  
		Last Modified: Mon, 08 Dec 2025 22:34:59 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c1c60a78876ca8d26fa893a37ff13080f097555eea972e3e45e59d912f5e9c`  
		Last Modified: Mon, 08 Dec 2025 22:35:00 GMT  
		Size: 4.7 MB (4709641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:42ce2f56fd00643a382954ddf368a7ad26f88a053b4a557aa1112ed9de67aac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192e3247c9d1fd1e403f1da43c465327ebe5a123a9caf785ea53b5dd0388c5cb`

```dockerfile
```

-	Layers:
	-	`sha256:dbd5f23d6f6d5ab003eddef0af01a8a8b66fac74afe90d0faa97afa2b0a581d2`  
		Last Modified: Tue, 09 Dec 2025 00:01:40 GMT  
		Size: 5.6 MB (5585926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:401ba355602555e19652809e181e8fc4d172d2140c0c17f0781b909a2bff847e`  
		Last Modified: Tue, 09 Dec 2025 00:01:41 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v7

```console
$ docker pull irssi@sha256:90bf141f8448f931b78a4759623391882ba8d3d0520b3770b063ea80daf29ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48681035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d9f126abb644aa91708596fe16f433c339727d7b73386dc26994eb1d0119af6`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:36:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:36:55 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:36:55 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:36:55 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:36:55 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:37:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:37:36 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:37:36 GMT
USER user
# Mon, 08 Dec 2025 22:37:36 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea7a0e9121517502a0452fd53a68bbbf3e120ea0391f4616c22058f3ffe83a6`  
		Last Modified: Mon, 08 Dec 2025 22:37:54 GMT  
		Size: 17.9 MB (17909125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a98b78793ec14ceabf793c4778fa9c59358545e4604a1c0b15bb6bd21bd755`  
		Last Modified: Mon, 08 Dec 2025 22:37:52 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c7e9fbcbad6965518fd24946faf5855bd7c2b9dbb7a8632a912292a76f391b`  
		Last Modified: Mon, 08 Dec 2025 22:37:53 GMT  
		Size: 4.6 MB (4558538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:529cccf10215bb411a271b196fe666e44db36c0c88bc62b754ae778cc278ef86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5070cb3b050937bc197ae388f5989122c8e4fc9558708e5cd01f7eb53047ec85`

```dockerfile
```

-	Layers:
	-	`sha256:82a650d25d6be9c0ec73d583a9bfbb7e4cdf26f7eac9d4a2c0b9165043d1c3b1`  
		Last Modified: Tue, 09 Dec 2025 00:01:47 GMT  
		Size: 5.6 MB (5588948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b12cb7447938f917d5345ecf33832b856ff04c97a5f9c2213b71e0a7d45d3fcc`  
		Last Modified: Tue, 09 Dec 2025 00:01:47 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:4ad94477cda90ae8d3d4d47ed0c1a58d162ca780cbc21e1e356ae833c2c9af51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53972792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6123fcf7ac4efb210283b7fab07ab5e1f866bcfa7ad8dbd2186bd66c2f88d4b2`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:35:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:35:56 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:35:56 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:35:56 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:35:56 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:36:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:36:32 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:36:32 GMT
USER user
# Mon, 08 Dec 2025 22:36:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271cd4b9332a86de31690e94a837946ec81b376cf3b99b9ec078b9997ebfc4e7`  
		Last Modified: Mon, 08 Dec 2025 22:36:51 GMT  
		Size: 19.0 MB (19049077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f51515c1d0d0bdda82745487e18f18f85d1a6999f3c82ff517039ed8c01ae9`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae317866ab39c091f9ece44d604dc3317877b2ed386b1ff38dcf25d62707f6e`  
		Last Modified: Mon, 08 Dec 2025 22:36:50 GMT  
		Size: 4.8 MB (4781724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:8a9848973ad593c402ad00791b8debf829808115d9215d351a4d092da9efdfb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e8e14ea45e56f1a280745e4215d6b09bf3bbe98d77d25ed701e1833b69db94`

```dockerfile
```

-	Layers:
	-	`sha256:833298ea4b4e32cd4be350f01f29cc972db0aa5f1e1b52c229e9611870f9d81d`  
		Last Modified: Tue, 09 Dec 2025 00:01:51 GMT  
		Size: 5.6 MB (5594861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12ec53196ee839e1d4fc9f760637572995c6cf92c75585cdf8a0ddebd72fd86a`  
		Last Modified: Tue, 09 Dec 2025 00:01:52 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; 386

```console
$ docker pull irssi@sha256:e3cb55074f79f7accb3186e087c8bcfbe5fb81bafed6b3843bbb182b831c2271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede6324a485fc1c56152548ccc95aa525d3e6298b82206a635b9e5bb2c43a274`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:34:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:34:50 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:34:50 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:34:50 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:34:50 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:35:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:35:33 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:35:33 GMT
USER user
# Mon, 08 Dec 2025 22:35:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92779a84b492a0e3f9b30abe3ba2c3f3c75f5f8bac0be5b3ec6f1d2151769a81`  
		Last Modified: Mon, 08 Dec 2025 22:35:51 GMT  
		Size: 18.7 MB (18740473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9e00516c012835613d2d6c24e48eca1db4092e2ae02a5557ef978565a9087b`  
		Last Modified: Mon, 08 Dec 2025 22:35:49 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380f851f46dcf6024e273c5690f4de14d4837fe4c9e173048edc3844675aefad`  
		Last Modified: Mon, 08 Dec 2025 22:35:49 GMT  
		Size: 4.9 MB (4868342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:0e026c9c8b43f1e4b3f0cf84c29441b70414ab67d248c56ebf7607efd867af5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c110c8c5132d6b986eca5007cb21a2921c655197298f96c1e6e3fe1d975295ce`

```dockerfile
```

-	Layers:
	-	`sha256:290278e5fa9964615268f167ae0917568dd48529eb40cb0fe4b7b6b4fd6db490`  
		Last Modified: Tue, 09 Dec 2025 00:01:57 GMT  
		Size: 5.6 MB (5584500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b86870229139d3e4a5b2f5fb461a45c930f312a775c5a1c86c120a2616479b3`  
		Last Modified: Tue, 09 Dec 2025 00:01:58 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; ppc64le

```console
$ docker pull irssi@sha256:93ea18bd78c1073049928098da83c8d7489f034eb6e93242c329dd6ac2f1928b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58240744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5496783653403c6d012d80f5d9f8c7a75a1093b7a1752b8fe2f67c024d71ba30`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:28:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:28:22 GMT
ENV HOME=/home/user
# Tue, 09 Dec 2025 00:28:22 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 09 Dec 2025 00:28:22 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 00:28:22 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 09 Dec 2025 00:30:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 09 Dec 2025 00:30:05 GMT
WORKDIR /home/user
# Tue, 09 Dec 2025 00:30:05 GMT
USER user
# Tue, 09 Dec 2025 00:30:05 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d43ff5db3e76c55de7b73205ca86bac1121de5d0f0c442c6d1fab408d40dbc4`  
		Last Modified: Tue, 09 Dec 2025 00:30:40 GMT  
		Size: 19.5 MB (19543101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20fac790531c01e08ec11e7ea8e6c78bc9732c6dd506329349609d5c47ea56b`  
		Last Modified: Tue, 09 Dec 2025 00:30:38 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e4e19b419b36bd43d3ecbb483048af4910c11c8ed72f86585d17de6a3cf367`  
		Last Modified: Tue, 09 Dec 2025 00:30:41 GMT  
		Size: 5.1 MB (5097391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:fe0f1b60af0b886246c9c854bfba7d6c86f3a936171bfe3afcb3fe3e72177db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aaaf9080eb40d58b04f0eb1b35aacf665d2ab2db092955824c8a40ab7b15d85`

```dockerfile
```

-	Layers:
	-	`sha256:e4b1401322d5b02c67c73ad0a132014ff5d6ebe1d604dbeb9595a74e83201f93`  
		Last Modified: Tue, 09 Dec 2025 02:59:59 GMT  
		Size: 5.6 MB (5595408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e74c10f22046f87919aa9d2d4f9fc0afaed79b0bdbbaad1bf79c689583b0b1c`  
		Last Modified: Tue, 09 Dec 2025 03:00:00 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; riscv64

```console
$ docker pull irssi@sha256:0a17bc9dc7f1ede0aae4d4035aa269c39fdd3ad059158a3c6a569fa2bf7da8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51686196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e6a1bc4c5ae216cf035ec48b010768259be2a066ee4ef066bcb9c32d445e4d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 10:01:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:01:44 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 10:01:44 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 10:01:44 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 10:01:44 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 10:08:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 10:08:36 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 10:08:36 GMT
USER user
# Tue, 18 Nov 2025 10:08:36 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afef2a7493fa326b06e464e36f2a79568e4c5c265515366e193165f0b4d284e`  
		Last Modified: Tue, 18 Nov 2025 10:10:42 GMT  
		Size: 18.5 MB (18549074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f026bbe28877d1917f647dacffd37172e95435e1c7e9fbe30a62986bb72cd62b`  
		Last Modified: Tue, 18 Nov 2025 10:10:41 GMT  
		Size: 3.3 KB (3337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3d248f54be38451080b4d25093d9df5c1c9efe1175c3cf58494a7e0fd7fe62`  
		Last Modified: Tue, 18 Nov 2025 10:10:41 GMT  
		Size: 4.9 MB (4860627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:7b01cdd2258dc9fd9266a05e6cbd264f72886699285f27da4dcfa624dcb82f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afb4ae2e3561846a1f14e41a61390911210a0c9ea6b4f9bace7ef57ca7a1303`

```dockerfile
```

-	Layers:
	-	`sha256:5044523627d968ee0b87912ad5e86b6f374ff85ef9a7878ae77c52dcf5581421`  
		Last Modified: Tue, 18 Nov 2025 18:00:24 GMT  
		Size: 5.6 MB (5579680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43863609ed306f6a1f2ac385d2c41ef9efb115640066a4bb3b02043bb96f7158`  
		Last Modified: Tue, 18 Nov 2025 18:00:25 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; s390x

```console
$ docker pull irssi@sha256:79ceeb6e5f00cadefc5098892f4fdd847c8a6c7147214049af36f2988eb63701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54503098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4447f6a16ef4660d5cc882de4451987df832e0221f3c9198582f5041d9e484`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:33:35 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:33:35 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:33:35 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:33:35 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:34:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:34:10 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:34:10 GMT
USER user
# Mon, 08 Dec 2025 22:34:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a68582eda8cf9c795e8fac7bd4a06d7b4cf05bcce0b996577a486d0e34b56c`  
		Last Modified: Mon, 08 Dec 2025 22:34:33 GMT  
		Size: 19.8 MB (19759448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea7a5c770aac1d19a49e32bddbb9b474dd2746e7821d20791e1b80abfa3b5a3`  
		Last Modified: Mon, 08 Dec 2025 22:34:31 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fe49ac5d532203fa75223786c8c8ef7f78fbdeff8227abdab3b6e08125de53`  
		Last Modified: Mon, 08 Dec 2025 22:34:32 GMT  
		Size: 4.9 MB (4905890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:afc0d5563715a205bdbf09adfb0dcb772d44ec5f9f64be619112ea71bef71370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb41a3e51a7b6c277c4898dede97241725067c20506fcd3897eb9a2fa33ef8fc`

```dockerfile
```

-	Layers:
	-	`sha256:9292a924a5f71b0700ea789b79e1a8bf1256af5aae51b422283563c1fa34bf6e`  
		Last Modified: Tue, 09 Dec 2025 00:02:15 GMT  
		Size: 5.6 MB (5589282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff40bc8ca1364bffe8c60be1df3e2bffedbd27bb8dbcf6db778c754320ccf6e`  
		Last Modified: Tue, 09 Dec 2025 00:02:16 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine`

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

### `irssi:1.4-alpine` - linux; amd64

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

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

### `irssi:1.4-alpine` - linux; arm variant v6

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

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

### `irssi:1.4-alpine` - linux; arm variant v7

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

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

### `irssi:1.4-alpine` - linux; arm64 variant v8

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

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

### `irssi:1.4-alpine` - linux; 386

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

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

### `irssi:1.4-alpine` - linux; ppc64le

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

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

### `irssi:1.4-alpine` - linux; riscv64

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

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

### `irssi:1.4-alpine` - linux; s390x

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

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

## `irssi:1.4-alpine3.23`

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

### `irssi:1.4-alpine3.23` - linux; amd64

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

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

### `irssi:1.4-alpine3.23` - linux; arm variant v6

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

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

### `irssi:1.4-alpine3.23` - linux; arm variant v7

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

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

### `irssi:1.4-alpine3.23` - linux; arm64 variant v8

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

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

### `irssi:1.4-alpine3.23` - linux; 386

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

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

### `irssi:1.4-alpine3.23` - linux; ppc64le

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

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

### `irssi:1.4-alpine3.23` - linux; riscv64

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

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

### `irssi:1.4-alpine3.23` - linux; s390x

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

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

## `irssi:1.4-trixie`

```console
$ docker pull irssi@sha256:19043dddac4df97572295eb4df56b6e5e8d1244a09ece798931a7e728e2099b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
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

### `irssi:1.4-trixie` - linux; amd64

```console
$ docker pull irssi@sha256:ba548a27a12441efe110f9a056e793d722bda4a4eb13a3ceea8bf8d2d5ac1e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53869300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ebb967af1ef6016f39c7253143525ae93880628cdbc3e189772a2d029fc1a25`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:37:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:37:12 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:37:12 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:37:12 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:37:12 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:37:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:37:51 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:37:51 GMT
USER user
# Mon, 08 Dec 2025 22:37:51 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae9ff25045243dc27c083564f101c73527fab1e4d6de25faafe1d20c6993d0f`  
		Last Modified: Mon, 08 Dec 2025 22:38:10 GMT  
		Size: 19.2 MB (19222767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cff4c278980a41219ced1054076473f352a9ab538703fdb0508673575901de`  
		Last Modified: Mon, 08 Dec 2025 22:38:08 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6979d38c29179b5f4797ac48f3389f2044fb0312d0cd3b7f7fe377d41762cf9c`  
		Last Modified: Mon, 08 Dec 2025 22:38:08 GMT  
		Size: 4.9 MB (4866682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:2c34f0b8bd4789c746b87fcefbeca5053bc49367fbe0106f8c1f2c5df4510d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aec691ef1c3f8b1f097d426de19c51fc9a39bcd3002cf27303c6ea181155e87`

```dockerfile
```

-	Layers:
	-	`sha256:ea7448fd69d2025a02fa3773b13695b9ecaa34efd8cc5b223bd340a6a20bb280`  
		Last Modified: Tue, 09 Dec 2025 00:01:32 GMT  
		Size: 5.6 MB (5588377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15055f679734606495e25ae5c7b68d5ee1ec2609bfbca41b8eccfdc0431ef6dd`  
		Last Modified: Tue, 09 Dec 2025 00:01:32 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:605f1644cbe09985d1b0a7159e6a3645cacce33a561adb3eb3994e2bb9fe1118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50943555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d5500fde47056d160fcf131159d65be22e1cce50911f44d2f5be15fc113c99`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:33:53 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:33:53 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:33:53 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:33:53 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:34:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:34:44 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:34:44 GMT
USER user
# Mon, 08 Dec 2025 22:34:44 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209b020e9b6936d49088aeb2fe32da563e0dc7240b53e7a4f55a0064bcc57dbb`  
		Last Modified: Mon, 08 Dec 2025 22:35:02 GMT  
		Size: 18.3 MB (18286366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e546d6b1c1001d996e09271aa06076bbf5076bf4c0f1a64a5a76db18e6351b32`  
		Last Modified: Mon, 08 Dec 2025 22:34:59 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c1c60a78876ca8d26fa893a37ff13080f097555eea972e3e45e59d912f5e9c`  
		Last Modified: Mon, 08 Dec 2025 22:35:00 GMT  
		Size: 4.7 MB (4709641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:42ce2f56fd00643a382954ddf368a7ad26f88a053b4a557aa1112ed9de67aac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192e3247c9d1fd1e403f1da43c465327ebe5a123a9caf785ea53b5dd0388c5cb`

```dockerfile
```

-	Layers:
	-	`sha256:dbd5f23d6f6d5ab003eddef0af01a8a8b66fac74afe90d0faa97afa2b0a581d2`  
		Last Modified: Tue, 09 Dec 2025 00:01:40 GMT  
		Size: 5.6 MB (5585926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:401ba355602555e19652809e181e8fc4d172d2140c0c17f0781b909a2bff847e`  
		Last Modified: Tue, 09 Dec 2025 00:01:41 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:90bf141f8448f931b78a4759623391882ba8d3d0520b3770b063ea80daf29ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48681035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d9f126abb644aa91708596fe16f433c339727d7b73386dc26994eb1d0119af6`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:36:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:36:55 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:36:55 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:36:55 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:36:55 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:37:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:37:36 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:37:36 GMT
USER user
# Mon, 08 Dec 2025 22:37:36 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea7a0e9121517502a0452fd53a68bbbf3e120ea0391f4616c22058f3ffe83a6`  
		Last Modified: Mon, 08 Dec 2025 22:37:54 GMT  
		Size: 17.9 MB (17909125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a98b78793ec14ceabf793c4778fa9c59358545e4604a1c0b15bb6bd21bd755`  
		Last Modified: Mon, 08 Dec 2025 22:37:52 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c7e9fbcbad6965518fd24946faf5855bd7c2b9dbb7a8632a912292a76f391b`  
		Last Modified: Mon, 08 Dec 2025 22:37:53 GMT  
		Size: 4.6 MB (4558538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:529cccf10215bb411a271b196fe666e44db36c0c88bc62b754ae778cc278ef86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5070cb3b050937bc197ae388f5989122c8e4fc9558708e5cd01f7eb53047ec85`

```dockerfile
```

-	Layers:
	-	`sha256:82a650d25d6be9c0ec73d583a9bfbb7e4cdf26f7eac9d4a2c0b9165043d1c3b1`  
		Last Modified: Tue, 09 Dec 2025 00:01:47 GMT  
		Size: 5.6 MB (5588948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b12cb7447938f917d5345ecf33832b856ff04c97a5f9c2213b71e0a7d45d3fcc`  
		Last Modified: Tue, 09 Dec 2025 00:01:47 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:4ad94477cda90ae8d3d4d47ed0c1a58d162ca780cbc21e1e356ae833c2c9af51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53972792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6123fcf7ac4efb210283b7fab07ab5e1f866bcfa7ad8dbd2186bd66c2f88d4b2`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:35:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:35:56 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:35:56 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:35:56 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:35:56 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:36:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:36:32 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:36:32 GMT
USER user
# Mon, 08 Dec 2025 22:36:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271cd4b9332a86de31690e94a837946ec81b376cf3b99b9ec078b9997ebfc4e7`  
		Last Modified: Mon, 08 Dec 2025 22:36:51 GMT  
		Size: 19.0 MB (19049077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f51515c1d0d0bdda82745487e18f18f85d1a6999f3c82ff517039ed8c01ae9`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae317866ab39c091f9ece44d604dc3317877b2ed386b1ff38dcf25d62707f6e`  
		Last Modified: Mon, 08 Dec 2025 22:36:50 GMT  
		Size: 4.8 MB (4781724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:8a9848973ad593c402ad00791b8debf829808115d9215d351a4d092da9efdfb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e8e14ea45e56f1a280745e4215d6b09bf3bbe98d77d25ed701e1833b69db94`

```dockerfile
```

-	Layers:
	-	`sha256:833298ea4b4e32cd4be350f01f29cc972db0aa5f1e1b52c229e9611870f9d81d`  
		Last Modified: Tue, 09 Dec 2025 00:01:51 GMT  
		Size: 5.6 MB (5594861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12ec53196ee839e1d4fc9f760637572995c6cf92c75585cdf8a0ddebd72fd86a`  
		Last Modified: Tue, 09 Dec 2025 00:01:52 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; 386

```console
$ docker pull irssi@sha256:e3cb55074f79f7accb3186e087c8bcfbe5fb81bafed6b3843bbb182b831c2271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede6324a485fc1c56152548ccc95aa525d3e6298b82206a635b9e5bb2c43a274`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:34:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:34:50 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:34:50 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:34:50 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:34:50 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:35:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:35:33 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:35:33 GMT
USER user
# Mon, 08 Dec 2025 22:35:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92779a84b492a0e3f9b30abe3ba2c3f3c75f5f8bac0be5b3ec6f1d2151769a81`  
		Last Modified: Mon, 08 Dec 2025 22:35:51 GMT  
		Size: 18.7 MB (18740473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9e00516c012835613d2d6c24e48eca1db4092e2ae02a5557ef978565a9087b`  
		Last Modified: Mon, 08 Dec 2025 22:35:49 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380f851f46dcf6024e273c5690f4de14d4837fe4c9e173048edc3844675aefad`  
		Last Modified: Mon, 08 Dec 2025 22:35:49 GMT  
		Size: 4.9 MB (4868342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:0e026c9c8b43f1e4b3f0cf84c29441b70414ab67d248c56ebf7607efd867af5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c110c8c5132d6b986eca5007cb21a2921c655197298f96c1e6e3fe1d975295ce`

```dockerfile
```

-	Layers:
	-	`sha256:290278e5fa9964615268f167ae0917568dd48529eb40cb0fe4b7b6b4fd6db490`  
		Last Modified: Tue, 09 Dec 2025 00:01:57 GMT  
		Size: 5.6 MB (5584500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b86870229139d3e4a5b2f5fb461a45c930f312a775c5a1c86c120a2616479b3`  
		Last Modified: Tue, 09 Dec 2025 00:01:58 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:93ea18bd78c1073049928098da83c8d7489f034eb6e93242c329dd6ac2f1928b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58240744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5496783653403c6d012d80f5d9f8c7a75a1093b7a1752b8fe2f67c024d71ba30`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:28:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:28:22 GMT
ENV HOME=/home/user
# Tue, 09 Dec 2025 00:28:22 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 09 Dec 2025 00:28:22 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 00:28:22 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 09 Dec 2025 00:30:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 09 Dec 2025 00:30:05 GMT
WORKDIR /home/user
# Tue, 09 Dec 2025 00:30:05 GMT
USER user
# Tue, 09 Dec 2025 00:30:05 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d43ff5db3e76c55de7b73205ca86bac1121de5d0f0c442c6d1fab408d40dbc4`  
		Last Modified: Tue, 09 Dec 2025 00:30:40 GMT  
		Size: 19.5 MB (19543101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20fac790531c01e08ec11e7ea8e6c78bc9732c6dd506329349609d5c47ea56b`  
		Last Modified: Tue, 09 Dec 2025 00:30:38 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e4e19b419b36bd43d3ecbb483048af4910c11c8ed72f86585d17de6a3cf367`  
		Last Modified: Tue, 09 Dec 2025 00:30:41 GMT  
		Size: 5.1 MB (5097391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:fe0f1b60af0b886246c9c854bfba7d6c86f3a936171bfe3afcb3fe3e72177db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aaaf9080eb40d58b04f0eb1b35aacf665d2ab2db092955824c8a40ab7b15d85`

```dockerfile
```

-	Layers:
	-	`sha256:e4b1401322d5b02c67c73ad0a132014ff5d6ebe1d604dbeb9595a74e83201f93`  
		Last Modified: Tue, 09 Dec 2025 02:59:59 GMT  
		Size: 5.6 MB (5595408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e74c10f22046f87919aa9d2d4f9fc0afaed79b0bdbbaad1bf79c689583b0b1c`  
		Last Modified: Tue, 09 Dec 2025 03:00:00 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:0a17bc9dc7f1ede0aae4d4035aa269c39fdd3ad059158a3c6a569fa2bf7da8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51686196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e6a1bc4c5ae216cf035ec48b010768259be2a066ee4ef066bcb9c32d445e4d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 10:01:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:01:44 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 10:01:44 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 10:01:44 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 10:01:44 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 10:08:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 10:08:36 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 10:08:36 GMT
USER user
# Tue, 18 Nov 2025 10:08:36 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afef2a7493fa326b06e464e36f2a79568e4c5c265515366e193165f0b4d284e`  
		Last Modified: Tue, 18 Nov 2025 10:10:42 GMT  
		Size: 18.5 MB (18549074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f026bbe28877d1917f647dacffd37172e95435e1c7e9fbe30a62986bb72cd62b`  
		Last Modified: Tue, 18 Nov 2025 10:10:41 GMT  
		Size: 3.3 KB (3337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3d248f54be38451080b4d25093d9df5c1c9efe1175c3cf58494a7e0fd7fe62`  
		Last Modified: Tue, 18 Nov 2025 10:10:41 GMT  
		Size: 4.9 MB (4860627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:7b01cdd2258dc9fd9266a05e6cbd264f72886699285f27da4dcfa624dcb82f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afb4ae2e3561846a1f14e41a61390911210a0c9ea6b4f9bace7ef57ca7a1303`

```dockerfile
```

-	Layers:
	-	`sha256:5044523627d968ee0b87912ad5e86b6f374ff85ef9a7878ae77c52dcf5581421`  
		Last Modified: Tue, 18 Nov 2025 18:00:24 GMT  
		Size: 5.6 MB (5579680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43863609ed306f6a1f2ac385d2c41ef9efb115640066a4bb3b02043bb96f7158`  
		Last Modified: Tue, 18 Nov 2025 18:00:25 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; s390x

```console
$ docker pull irssi@sha256:79ceeb6e5f00cadefc5098892f4fdd847c8a6c7147214049af36f2988eb63701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54503098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4447f6a16ef4660d5cc882de4451987df832e0221f3c9198582f5041d9e484`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:33:35 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:33:35 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:33:35 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:33:35 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:34:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:34:10 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:34:10 GMT
USER user
# Mon, 08 Dec 2025 22:34:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a68582eda8cf9c795e8fac7bd4a06d7b4cf05bcce0b996577a486d0e34b56c`  
		Last Modified: Mon, 08 Dec 2025 22:34:33 GMT  
		Size: 19.8 MB (19759448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea7a5c770aac1d19a49e32bddbb9b474dd2746e7821d20791e1b80abfa3b5a3`  
		Last Modified: Mon, 08 Dec 2025 22:34:31 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fe49ac5d532203fa75223786c8c8ef7f78fbdeff8227abdab3b6e08125de53`  
		Last Modified: Mon, 08 Dec 2025 22:34:32 GMT  
		Size: 4.9 MB (4905890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:afc0d5563715a205bdbf09adfb0dcb772d44ec5f9f64be619112ea71bef71370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb41a3e51a7b6c277c4898dede97241725067c20506fcd3897eb9a2fa33ef8fc`

```dockerfile
```

-	Layers:
	-	`sha256:9292a924a5f71b0700ea789b79e1a8bf1256af5aae51b422283563c1fa34bf6e`  
		Last Modified: Tue, 09 Dec 2025 00:02:15 GMT  
		Size: 5.6 MB (5589282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff40bc8ca1364bffe8c60be1df3e2bffedbd27bb8dbcf6db778c754320ccf6e`  
		Last Modified: Tue, 09 Dec 2025 00:02:16 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5`

```console
$ docker pull irssi@sha256:19043dddac4df97572295eb4df56b6e5e8d1244a09ece798931a7e728e2099b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
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

### `irssi:1.4.5` - linux; amd64

```console
$ docker pull irssi@sha256:ba548a27a12441efe110f9a056e793d722bda4a4eb13a3ceea8bf8d2d5ac1e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53869300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ebb967af1ef6016f39c7253143525ae93880628cdbc3e189772a2d029fc1a25`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:37:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:37:12 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:37:12 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:37:12 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:37:12 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:37:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:37:51 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:37:51 GMT
USER user
# Mon, 08 Dec 2025 22:37:51 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae9ff25045243dc27c083564f101c73527fab1e4d6de25faafe1d20c6993d0f`  
		Last Modified: Mon, 08 Dec 2025 22:38:10 GMT  
		Size: 19.2 MB (19222767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cff4c278980a41219ced1054076473f352a9ab538703fdb0508673575901de`  
		Last Modified: Mon, 08 Dec 2025 22:38:08 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6979d38c29179b5f4797ac48f3389f2044fb0312d0cd3b7f7fe377d41762cf9c`  
		Last Modified: Mon, 08 Dec 2025 22:38:08 GMT  
		Size: 4.9 MB (4866682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:2c34f0b8bd4789c746b87fcefbeca5053bc49367fbe0106f8c1f2c5df4510d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aec691ef1c3f8b1f097d426de19c51fc9a39bcd3002cf27303c6ea181155e87`

```dockerfile
```

-	Layers:
	-	`sha256:ea7448fd69d2025a02fa3773b13695b9ecaa34efd8cc5b223bd340a6a20bb280`  
		Last Modified: Tue, 09 Dec 2025 00:01:32 GMT  
		Size: 5.6 MB (5588377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15055f679734606495e25ae5c7b68d5ee1ec2609bfbca41b8eccfdc0431ef6dd`  
		Last Modified: Tue, 09 Dec 2025 00:01:32 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v5

```console
$ docker pull irssi@sha256:605f1644cbe09985d1b0a7159e6a3645cacce33a561adb3eb3994e2bb9fe1118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50943555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d5500fde47056d160fcf131159d65be22e1cce50911f44d2f5be15fc113c99`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:33:53 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:33:53 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:33:53 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:33:53 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:34:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:34:44 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:34:44 GMT
USER user
# Mon, 08 Dec 2025 22:34:44 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209b020e9b6936d49088aeb2fe32da563e0dc7240b53e7a4f55a0064bcc57dbb`  
		Last Modified: Mon, 08 Dec 2025 22:35:02 GMT  
		Size: 18.3 MB (18286366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e546d6b1c1001d996e09271aa06076bbf5076bf4c0f1a64a5a76db18e6351b32`  
		Last Modified: Mon, 08 Dec 2025 22:34:59 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c1c60a78876ca8d26fa893a37ff13080f097555eea972e3e45e59d912f5e9c`  
		Last Modified: Mon, 08 Dec 2025 22:35:00 GMT  
		Size: 4.7 MB (4709641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:42ce2f56fd00643a382954ddf368a7ad26f88a053b4a557aa1112ed9de67aac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192e3247c9d1fd1e403f1da43c465327ebe5a123a9caf785ea53b5dd0388c5cb`

```dockerfile
```

-	Layers:
	-	`sha256:dbd5f23d6f6d5ab003eddef0af01a8a8b66fac74afe90d0faa97afa2b0a581d2`  
		Last Modified: Tue, 09 Dec 2025 00:01:40 GMT  
		Size: 5.6 MB (5585926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:401ba355602555e19652809e181e8fc4d172d2140c0c17f0781b909a2bff847e`  
		Last Modified: Tue, 09 Dec 2025 00:01:41 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v7

```console
$ docker pull irssi@sha256:90bf141f8448f931b78a4759623391882ba8d3d0520b3770b063ea80daf29ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48681035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d9f126abb644aa91708596fe16f433c339727d7b73386dc26994eb1d0119af6`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:36:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:36:55 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:36:55 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:36:55 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:36:55 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:37:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:37:36 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:37:36 GMT
USER user
# Mon, 08 Dec 2025 22:37:36 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea7a0e9121517502a0452fd53a68bbbf3e120ea0391f4616c22058f3ffe83a6`  
		Last Modified: Mon, 08 Dec 2025 22:37:54 GMT  
		Size: 17.9 MB (17909125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a98b78793ec14ceabf793c4778fa9c59358545e4604a1c0b15bb6bd21bd755`  
		Last Modified: Mon, 08 Dec 2025 22:37:52 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c7e9fbcbad6965518fd24946faf5855bd7c2b9dbb7a8632a912292a76f391b`  
		Last Modified: Mon, 08 Dec 2025 22:37:53 GMT  
		Size: 4.6 MB (4558538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:529cccf10215bb411a271b196fe666e44db36c0c88bc62b754ae778cc278ef86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5070cb3b050937bc197ae388f5989122c8e4fc9558708e5cd01f7eb53047ec85`

```dockerfile
```

-	Layers:
	-	`sha256:82a650d25d6be9c0ec73d583a9bfbb7e4cdf26f7eac9d4a2c0b9165043d1c3b1`  
		Last Modified: Tue, 09 Dec 2025 00:01:47 GMT  
		Size: 5.6 MB (5588948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b12cb7447938f917d5345ecf33832b856ff04c97a5f9c2213b71e0a7d45d3fcc`  
		Last Modified: Tue, 09 Dec 2025 00:01:47 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:4ad94477cda90ae8d3d4d47ed0c1a58d162ca780cbc21e1e356ae833c2c9af51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53972792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6123fcf7ac4efb210283b7fab07ab5e1f866bcfa7ad8dbd2186bd66c2f88d4b2`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:35:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:35:56 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:35:56 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:35:56 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:35:56 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:36:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:36:32 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:36:32 GMT
USER user
# Mon, 08 Dec 2025 22:36:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271cd4b9332a86de31690e94a837946ec81b376cf3b99b9ec078b9997ebfc4e7`  
		Last Modified: Mon, 08 Dec 2025 22:36:51 GMT  
		Size: 19.0 MB (19049077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f51515c1d0d0bdda82745487e18f18f85d1a6999f3c82ff517039ed8c01ae9`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae317866ab39c091f9ece44d604dc3317877b2ed386b1ff38dcf25d62707f6e`  
		Last Modified: Mon, 08 Dec 2025 22:36:50 GMT  
		Size: 4.8 MB (4781724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:8a9848973ad593c402ad00791b8debf829808115d9215d351a4d092da9efdfb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e8e14ea45e56f1a280745e4215d6b09bf3bbe98d77d25ed701e1833b69db94`

```dockerfile
```

-	Layers:
	-	`sha256:833298ea4b4e32cd4be350f01f29cc972db0aa5f1e1b52c229e9611870f9d81d`  
		Last Modified: Tue, 09 Dec 2025 00:01:51 GMT  
		Size: 5.6 MB (5594861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12ec53196ee839e1d4fc9f760637572995c6cf92c75585cdf8a0ddebd72fd86a`  
		Last Modified: Tue, 09 Dec 2025 00:01:52 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; 386

```console
$ docker pull irssi@sha256:e3cb55074f79f7accb3186e087c8bcfbe5fb81bafed6b3843bbb182b831c2271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede6324a485fc1c56152548ccc95aa525d3e6298b82206a635b9e5bb2c43a274`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:34:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:34:50 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:34:50 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:34:50 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:34:50 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:35:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:35:33 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:35:33 GMT
USER user
# Mon, 08 Dec 2025 22:35:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92779a84b492a0e3f9b30abe3ba2c3f3c75f5f8bac0be5b3ec6f1d2151769a81`  
		Last Modified: Mon, 08 Dec 2025 22:35:51 GMT  
		Size: 18.7 MB (18740473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9e00516c012835613d2d6c24e48eca1db4092e2ae02a5557ef978565a9087b`  
		Last Modified: Mon, 08 Dec 2025 22:35:49 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380f851f46dcf6024e273c5690f4de14d4837fe4c9e173048edc3844675aefad`  
		Last Modified: Mon, 08 Dec 2025 22:35:49 GMT  
		Size: 4.9 MB (4868342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:0e026c9c8b43f1e4b3f0cf84c29441b70414ab67d248c56ebf7607efd867af5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c110c8c5132d6b986eca5007cb21a2921c655197298f96c1e6e3fe1d975295ce`

```dockerfile
```

-	Layers:
	-	`sha256:290278e5fa9964615268f167ae0917568dd48529eb40cb0fe4b7b6b4fd6db490`  
		Last Modified: Tue, 09 Dec 2025 00:01:57 GMT  
		Size: 5.6 MB (5584500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b86870229139d3e4a5b2f5fb461a45c930f312a775c5a1c86c120a2616479b3`  
		Last Modified: Tue, 09 Dec 2025 00:01:58 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; ppc64le

```console
$ docker pull irssi@sha256:93ea18bd78c1073049928098da83c8d7489f034eb6e93242c329dd6ac2f1928b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58240744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5496783653403c6d012d80f5d9f8c7a75a1093b7a1752b8fe2f67c024d71ba30`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:28:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:28:22 GMT
ENV HOME=/home/user
# Tue, 09 Dec 2025 00:28:22 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 09 Dec 2025 00:28:22 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 00:28:22 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 09 Dec 2025 00:30:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 09 Dec 2025 00:30:05 GMT
WORKDIR /home/user
# Tue, 09 Dec 2025 00:30:05 GMT
USER user
# Tue, 09 Dec 2025 00:30:05 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d43ff5db3e76c55de7b73205ca86bac1121de5d0f0c442c6d1fab408d40dbc4`  
		Last Modified: Tue, 09 Dec 2025 00:30:40 GMT  
		Size: 19.5 MB (19543101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20fac790531c01e08ec11e7ea8e6c78bc9732c6dd506329349609d5c47ea56b`  
		Last Modified: Tue, 09 Dec 2025 00:30:38 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e4e19b419b36bd43d3ecbb483048af4910c11c8ed72f86585d17de6a3cf367`  
		Last Modified: Tue, 09 Dec 2025 00:30:41 GMT  
		Size: 5.1 MB (5097391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:fe0f1b60af0b886246c9c854bfba7d6c86f3a936171bfe3afcb3fe3e72177db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aaaf9080eb40d58b04f0eb1b35aacf665d2ab2db092955824c8a40ab7b15d85`

```dockerfile
```

-	Layers:
	-	`sha256:e4b1401322d5b02c67c73ad0a132014ff5d6ebe1d604dbeb9595a74e83201f93`  
		Last Modified: Tue, 09 Dec 2025 02:59:59 GMT  
		Size: 5.6 MB (5595408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e74c10f22046f87919aa9d2d4f9fc0afaed79b0bdbbaad1bf79c689583b0b1c`  
		Last Modified: Tue, 09 Dec 2025 03:00:00 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; riscv64

```console
$ docker pull irssi@sha256:0a17bc9dc7f1ede0aae4d4035aa269c39fdd3ad059158a3c6a569fa2bf7da8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51686196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e6a1bc4c5ae216cf035ec48b010768259be2a066ee4ef066bcb9c32d445e4d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 10:01:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:01:44 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 10:01:44 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 10:01:44 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 10:01:44 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 10:08:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 10:08:36 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 10:08:36 GMT
USER user
# Tue, 18 Nov 2025 10:08:36 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afef2a7493fa326b06e464e36f2a79568e4c5c265515366e193165f0b4d284e`  
		Last Modified: Tue, 18 Nov 2025 10:10:42 GMT  
		Size: 18.5 MB (18549074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f026bbe28877d1917f647dacffd37172e95435e1c7e9fbe30a62986bb72cd62b`  
		Last Modified: Tue, 18 Nov 2025 10:10:41 GMT  
		Size: 3.3 KB (3337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3d248f54be38451080b4d25093d9df5c1c9efe1175c3cf58494a7e0fd7fe62`  
		Last Modified: Tue, 18 Nov 2025 10:10:41 GMT  
		Size: 4.9 MB (4860627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:7b01cdd2258dc9fd9266a05e6cbd264f72886699285f27da4dcfa624dcb82f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afb4ae2e3561846a1f14e41a61390911210a0c9ea6b4f9bace7ef57ca7a1303`

```dockerfile
```

-	Layers:
	-	`sha256:5044523627d968ee0b87912ad5e86b6f374ff85ef9a7878ae77c52dcf5581421`  
		Last Modified: Tue, 18 Nov 2025 18:00:24 GMT  
		Size: 5.6 MB (5579680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43863609ed306f6a1f2ac385d2c41ef9efb115640066a4bb3b02043bb96f7158`  
		Last Modified: Tue, 18 Nov 2025 18:00:25 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; s390x

```console
$ docker pull irssi@sha256:79ceeb6e5f00cadefc5098892f4fdd847c8a6c7147214049af36f2988eb63701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54503098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4447f6a16ef4660d5cc882de4451987df832e0221f3c9198582f5041d9e484`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:33:35 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:33:35 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:33:35 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:33:35 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:34:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:34:10 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:34:10 GMT
USER user
# Mon, 08 Dec 2025 22:34:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a68582eda8cf9c795e8fac7bd4a06d7b4cf05bcce0b996577a486d0e34b56c`  
		Last Modified: Mon, 08 Dec 2025 22:34:33 GMT  
		Size: 19.8 MB (19759448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea7a5c770aac1d19a49e32bddbb9b474dd2746e7821d20791e1b80abfa3b5a3`  
		Last Modified: Mon, 08 Dec 2025 22:34:31 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fe49ac5d532203fa75223786c8c8ef7f78fbdeff8227abdab3b6e08125de53`  
		Last Modified: Mon, 08 Dec 2025 22:34:32 GMT  
		Size: 4.9 MB (4905890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:afc0d5563715a205bdbf09adfb0dcb772d44ec5f9f64be619112ea71bef71370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb41a3e51a7b6c277c4898dede97241725067c20506fcd3897eb9a2fa33ef8fc`

```dockerfile
```

-	Layers:
	-	`sha256:9292a924a5f71b0700ea789b79e1a8bf1256af5aae51b422283563c1fa34bf6e`  
		Last Modified: Tue, 09 Dec 2025 00:02:15 GMT  
		Size: 5.6 MB (5589282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff40bc8ca1364bffe8c60be1df3e2bffedbd27bb8dbcf6db778c754320ccf6e`  
		Last Modified: Tue, 09 Dec 2025 00:02:16 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine`

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

### `irssi:1.4.5-alpine` - linux; amd64

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

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

### `irssi:1.4.5-alpine` - linux; arm variant v6

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

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

### `irssi:1.4.5-alpine` - linux; arm variant v7

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

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

### `irssi:1.4.5-alpine` - linux; arm64 variant v8

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

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

### `irssi:1.4.5-alpine` - linux; 386

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

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

### `irssi:1.4.5-alpine` - linux; ppc64le

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

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

### `irssi:1.4.5-alpine` - linux; riscv64

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

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

### `irssi:1.4.5-alpine` - linux; s390x

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

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

## `irssi:1.4.5-alpine3.23`

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

### `irssi:1.4.5-alpine3.23` - linux; amd64

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

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

### `irssi:1.4.5-alpine3.23` - linux; arm variant v6

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

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

### `irssi:1.4.5-alpine3.23` - linux; arm variant v7

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

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

### `irssi:1.4.5-alpine3.23` - linux; arm64 variant v8

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

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

### `irssi:1.4.5-alpine3.23` - linux; 386

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

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

### `irssi:1.4.5-alpine3.23` - linux; ppc64le

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

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

### `irssi:1.4.5-alpine3.23` - linux; riscv64

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

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

### `irssi:1.4.5-alpine3.23` - linux; s390x

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

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

## `irssi:1.4.5-trixie`

```console
$ docker pull irssi@sha256:19043dddac4df97572295eb4df56b6e5e8d1244a09ece798931a7e728e2099b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
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

### `irssi:1.4.5-trixie` - linux; amd64

```console
$ docker pull irssi@sha256:ba548a27a12441efe110f9a056e793d722bda4a4eb13a3ceea8bf8d2d5ac1e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53869300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ebb967af1ef6016f39c7253143525ae93880628cdbc3e189772a2d029fc1a25`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:37:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:37:12 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:37:12 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:37:12 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:37:12 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:37:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:37:51 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:37:51 GMT
USER user
# Mon, 08 Dec 2025 22:37:51 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae9ff25045243dc27c083564f101c73527fab1e4d6de25faafe1d20c6993d0f`  
		Last Modified: Mon, 08 Dec 2025 22:38:10 GMT  
		Size: 19.2 MB (19222767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cff4c278980a41219ced1054076473f352a9ab538703fdb0508673575901de`  
		Last Modified: Mon, 08 Dec 2025 22:38:08 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6979d38c29179b5f4797ac48f3389f2044fb0312d0cd3b7f7fe377d41762cf9c`  
		Last Modified: Mon, 08 Dec 2025 22:38:08 GMT  
		Size: 4.9 MB (4866682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:2c34f0b8bd4789c746b87fcefbeca5053bc49367fbe0106f8c1f2c5df4510d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aec691ef1c3f8b1f097d426de19c51fc9a39bcd3002cf27303c6ea181155e87`

```dockerfile
```

-	Layers:
	-	`sha256:ea7448fd69d2025a02fa3773b13695b9ecaa34efd8cc5b223bd340a6a20bb280`  
		Last Modified: Tue, 09 Dec 2025 00:01:32 GMT  
		Size: 5.6 MB (5588377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15055f679734606495e25ae5c7b68d5ee1ec2609bfbca41b8eccfdc0431ef6dd`  
		Last Modified: Tue, 09 Dec 2025 00:01:32 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:605f1644cbe09985d1b0a7159e6a3645cacce33a561adb3eb3994e2bb9fe1118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50943555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d5500fde47056d160fcf131159d65be22e1cce50911f44d2f5be15fc113c99`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:33:53 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:33:53 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:33:53 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:33:53 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:34:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:34:44 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:34:44 GMT
USER user
# Mon, 08 Dec 2025 22:34:44 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209b020e9b6936d49088aeb2fe32da563e0dc7240b53e7a4f55a0064bcc57dbb`  
		Last Modified: Mon, 08 Dec 2025 22:35:02 GMT  
		Size: 18.3 MB (18286366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e546d6b1c1001d996e09271aa06076bbf5076bf4c0f1a64a5a76db18e6351b32`  
		Last Modified: Mon, 08 Dec 2025 22:34:59 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c1c60a78876ca8d26fa893a37ff13080f097555eea972e3e45e59d912f5e9c`  
		Last Modified: Mon, 08 Dec 2025 22:35:00 GMT  
		Size: 4.7 MB (4709641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:42ce2f56fd00643a382954ddf368a7ad26f88a053b4a557aa1112ed9de67aac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192e3247c9d1fd1e403f1da43c465327ebe5a123a9caf785ea53b5dd0388c5cb`

```dockerfile
```

-	Layers:
	-	`sha256:dbd5f23d6f6d5ab003eddef0af01a8a8b66fac74afe90d0faa97afa2b0a581d2`  
		Last Modified: Tue, 09 Dec 2025 00:01:40 GMT  
		Size: 5.6 MB (5585926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:401ba355602555e19652809e181e8fc4d172d2140c0c17f0781b909a2bff847e`  
		Last Modified: Tue, 09 Dec 2025 00:01:41 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:90bf141f8448f931b78a4759623391882ba8d3d0520b3770b063ea80daf29ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48681035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d9f126abb644aa91708596fe16f433c339727d7b73386dc26994eb1d0119af6`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:36:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:36:55 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:36:55 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:36:55 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:36:55 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:37:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:37:36 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:37:36 GMT
USER user
# Mon, 08 Dec 2025 22:37:36 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea7a0e9121517502a0452fd53a68bbbf3e120ea0391f4616c22058f3ffe83a6`  
		Last Modified: Mon, 08 Dec 2025 22:37:54 GMT  
		Size: 17.9 MB (17909125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a98b78793ec14ceabf793c4778fa9c59358545e4604a1c0b15bb6bd21bd755`  
		Last Modified: Mon, 08 Dec 2025 22:37:52 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c7e9fbcbad6965518fd24946faf5855bd7c2b9dbb7a8632a912292a76f391b`  
		Last Modified: Mon, 08 Dec 2025 22:37:53 GMT  
		Size: 4.6 MB (4558538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:529cccf10215bb411a271b196fe666e44db36c0c88bc62b754ae778cc278ef86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5070cb3b050937bc197ae388f5989122c8e4fc9558708e5cd01f7eb53047ec85`

```dockerfile
```

-	Layers:
	-	`sha256:82a650d25d6be9c0ec73d583a9bfbb7e4cdf26f7eac9d4a2c0b9165043d1c3b1`  
		Last Modified: Tue, 09 Dec 2025 00:01:47 GMT  
		Size: 5.6 MB (5588948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b12cb7447938f917d5345ecf33832b856ff04c97a5f9c2213b71e0a7d45d3fcc`  
		Last Modified: Tue, 09 Dec 2025 00:01:47 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:4ad94477cda90ae8d3d4d47ed0c1a58d162ca780cbc21e1e356ae833c2c9af51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53972792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6123fcf7ac4efb210283b7fab07ab5e1f866bcfa7ad8dbd2186bd66c2f88d4b2`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:35:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:35:56 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:35:56 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:35:56 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:35:56 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:36:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:36:32 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:36:32 GMT
USER user
# Mon, 08 Dec 2025 22:36:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271cd4b9332a86de31690e94a837946ec81b376cf3b99b9ec078b9997ebfc4e7`  
		Last Modified: Mon, 08 Dec 2025 22:36:51 GMT  
		Size: 19.0 MB (19049077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f51515c1d0d0bdda82745487e18f18f85d1a6999f3c82ff517039ed8c01ae9`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae317866ab39c091f9ece44d604dc3317877b2ed386b1ff38dcf25d62707f6e`  
		Last Modified: Mon, 08 Dec 2025 22:36:50 GMT  
		Size: 4.8 MB (4781724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:8a9848973ad593c402ad00791b8debf829808115d9215d351a4d092da9efdfb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e8e14ea45e56f1a280745e4215d6b09bf3bbe98d77d25ed701e1833b69db94`

```dockerfile
```

-	Layers:
	-	`sha256:833298ea4b4e32cd4be350f01f29cc972db0aa5f1e1b52c229e9611870f9d81d`  
		Last Modified: Tue, 09 Dec 2025 00:01:51 GMT  
		Size: 5.6 MB (5594861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12ec53196ee839e1d4fc9f760637572995c6cf92c75585cdf8a0ddebd72fd86a`  
		Last Modified: Tue, 09 Dec 2025 00:01:52 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; 386

```console
$ docker pull irssi@sha256:e3cb55074f79f7accb3186e087c8bcfbe5fb81bafed6b3843bbb182b831c2271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede6324a485fc1c56152548ccc95aa525d3e6298b82206a635b9e5bb2c43a274`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:34:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:34:50 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:34:50 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:34:50 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:34:50 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:35:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:35:33 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:35:33 GMT
USER user
# Mon, 08 Dec 2025 22:35:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92779a84b492a0e3f9b30abe3ba2c3f3c75f5f8bac0be5b3ec6f1d2151769a81`  
		Last Modified: Mon, 08 Dec 2025 22:35:51 GMT  
		Size: 18.7 MB (18740473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9e00516c012835613d2d6c24e48eca1db4092e2ae02a5557ef978565a9087b`  
		Last Modified: Mon, 08 Dec 2025 22:35:49 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380f851f46dcf6024e273c5690f4de14d4837fe4c9e173048edc3844675aefad`  
		Last Modified: Mon, 08 Dec 2025 22:35:49 GMT  
		Size: 4.9 MB (4868342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:0e026c9c8b43f1e4b3f0cf84c29441b70414ab67d248c56ebf7607efd867af5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c110c8c5132d6b986eca5007cb21a2921c655197298f96c1e6e3fe1d975295ce`

```dockerfile
```

-	Layers:
	-	`sha256:290278e5fa9964615268f167ae0917568dd48529eb40cb0fe4b7b6b4fd6db490`  
		Last Modified: Tue, 09 Dec 2025 00:01:57 GMT  
		Size: 5.6 MB (5584500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b86870229139d3e4a5b2f5fb461a45c930f312a775c5a1c86c120a2616479b3`  
		Last Modified: Tue, 09 Dec 2025 00:01:58 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:93ea18bd78c1073049928098da83c8d7489f034eb6e93242c329dd6ac2f1928b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58240744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5496783653403c6d012d80f5d9f8c7a75a1093b7a1752b8fe2f67c024d71ba30`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:28:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:28:22 GMT
ENV HOME=/home/user
# Tue, 09 Dec 2025 00:28:22 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 09 Dec 2025 00:28:22 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 00:28:22 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 09 Dec 2025 00:30:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 09 Dec 2025 00:30:05 GMT
WORKDIR /home/user
# Tue, 09 Dec 2025 00:30:05 GMT
USER user
# Tue, 09 Dec 2025 00:30:05 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d43ff5db3e76c55de7b73205ca86bac1121de5d0f0c442c6d1fab408d40dbc4`  
		Last Modified: Tue, 09 Dec 2025 00:30:40 GMT  
		Size: 19.5 MB (19543101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20fac790531c01e08ec11e7ea8e6c78bc9732c6dd506329349609d5c47ea56b`  
		Last Modified: Tue, 09 Dec 2025 00:30:38 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e4e19b419b36bd43d3ecbb483048af4910c11c8ed72f86585d17de6a3cf367`  
		Last Modified: Tue, 09 Dec 2025 00:30:41 GMT  
		Size: 5.1 MB (5097391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:fe0f1b60af0b886246c9c854bfba7d6c86f3a936171bfe3afcb3fe3e72177db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aaaf9080eb40d58b04f0eb1b35aacf665d2ab2db092955824c8a40ab7b15d85`

```dockerfile
```

-	Layers:
	-	`sha256:e4b1401322d5b02c67c73ad0a132014ff5d6ebe1d604dbeb9595a74e83201f93`  
		Last Modified: Tue, 09 Dec 2025 02:59:59 GMT  
		Size: 5.6 MB (5595408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e74c10f22046f87919aa9d2d4f9fc0afaed79b0bdbbaad1bf79c689583b0b1c`  
		Last Modified: Tue, 09 Dec 2025 03:00:00 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:0a17bc9dc7f1ede0aae4d4035aa269c39fdd3ad059158a3c6a569fa2bf7da8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51686196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e6a1bc4c5ae216cf035ec48b010768259be2a066ee4ef066bcb9c32d445e4d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 10:01:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:01:44 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 10:01:44 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 10:01:44 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 10:01:44 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 10:08:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 10:08:36 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 10:08:36 GMT
USER user
# Tue, 18 Nov 2025 10:08:36 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afef2a7493fa326b06e464e36f2a79568e4c5c265515366e193165f0b4d284e`  
		Last Modified: Tue, 18 Nov 2025 10:10:42 GMT  
		Size: 18.5 MB (18549074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f026bbe28877d1917f647dacffd37172e95435e1c7e9fbe30a62986bb72cd62b`  
		Last Modified: Tue, 18 Nov 2025 10:10:41 GMT  
		Size: 3.3 KB (3337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3d248f54be38451080b4d25093d9df5c1c9efe1175c3cf58494a7e0fd7fe62`  
		Last Modified: Tue, 18 Nov 2025 10:10:41 GMT  
		Size: 4.9 MB (4860627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:7b01cdd2258dc9fd9266a05e6cbd264f72886699285f27da4dcfa624dcb82f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afb4ae2e3561846a1f14e41a61390911210a0c9ea6b4f9bace7ef57ca7a1303`

```dockerfile
```

-	Layers:
	-	`sha256:5044523627d968ee0b87912ad5e86b6f374ff85ef9a7878ae77c52dcf5581421`  
		Last Modified: Tue, 18 Nov 2025 18:00:24 GMT  
		Size: 5.6 MB (5579680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43863609ed306f6a1f2ac385d2c41ef9efb115640066a4bb3b02043bb96f7158`  
		Last Modified: Tue, 18 Nov 2025 18:00:25 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; s390x

```console
$ docker pull irssi@sha256:79ceeb6e5f00cadefc5098892f4fdd847c8a6c7147214049af36f2988eb63701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54503098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4447f6a16ef4660d5cc882de4451987df832e0221f3c9198582f5041d9e484`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:33:35 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:33:35 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:33:35 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:33:35 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:34:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:34:10 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:34:10 GMT
USER user
# Mon, 08 Dec 2025 22:34:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a68582eda8cf9c795e8fac7bd4a06d7b4cf05bcce0b996577a486d0e34b56c`  
		Last Modified: Mon, 08 Dec 2025 22:34:33 GMT  
		Size: 19.8 MB (19759448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea7a5c770aac1d19a49e32bddbb9b474dd2746e7821d20791e1b80abfa3b5a3`  
		Last Modified: Mon, 08 Dec 2025 22:34:31 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fe49ac5d532203fa75223786c8c8ef7f78fbdeff8227abdab3b6e08125de53`  
		Last Modified: Mon, 08 Dec 2025 22:34:32 GMT  
		Size: 4.9 MB (4905890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:afc0d5563715a205bdbf09adfb0dcb772d44ec5f9f64be619112ea71bef71370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb41a3e51a7b6c277c4898dede97241725067c20506fcd3897eb9a2fa33ef8fc`

```dockerfile
```

-	Layers:
	-	`sha256:9292a924a5f71b0700ea789b79e1a8bf1256af5aae51b422283563c1fa34bf6e`  
		Last Modified: Tue, 09 Dec 2025 00:02:15 GMT  
		Size: 5.6 MB (5589282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff40bc8ca1364bffe8c60be1df3e2bffedbd27bb8dbcf6db778c754320ccf6e`  
		Last Modified: Tue, 09 Dec 2025 00:02:16 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
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

## `irssi:alpine3.23`

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

### `irssi:alpine3.23` - linux; amd64

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

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

### `irssi:alpine3.23` - linux; arm variant v6

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

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

### `irssi:alpine3.23` - linux; arm variant v7

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

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

### `irssi:alpine3.23` - linux; arm64 variant v8

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

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

### `irssi:alpine3.23` - linux; 386

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

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

### `irssi:alpine3.23` - linux; ppc64le

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

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

### `irssi:alpine3.23` - linux; riscv64

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

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

### `irssi:alpine3.23` - linux; s390x

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

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

## `irssi:latest`

```console
$ docker pull irssi@sha256:19043dddac4df97572295eb4df56b6e5e8d1244a09ece798931a7e728e2099b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
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

### `irssi:latest` - linux; amd64

```console
$ docker pull irssi@sha256:ba548a27a12441efe110f9a056e793d722bda4a4eb13a3ceea8bf8d2d5ac1e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53869300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ebb967af1ef6016f39c7253143525ae93880628cdbc3e189772a2d029fc1a25`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:37:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:37:12 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:37:12 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:37:12 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:37:12 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:37:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:37:51 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:37:51 GMT
USER user
# Mon, 08 Dec 2025 22:37:51 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae9ff25045243dc27c083564f101c73527fab1e4d6de25faafe1d20c6993d0f`  
		Last Modified: Mon, 08 Dec 2025 22:38:10 GMT  
		Size: 19.2 MB (19222767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cff4c278980a41219ced1054076473f352a9ab538703fdb0508673575901de`  
		Last Modified: Mon, 08 Dec 2025 22:38:08 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6979d38c29179b5f4797ac48f3389f2044fb0312d0cd3b7f7fe377d41762cf9c`  
		Last Modified: Mon, 08 Dec 2025 22:38:08 GMT  
		Size: 4.9 MB (4866682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:2c34f0b8bd4789c746b87fcefbeca5053bc49367fbe0106f8c1f2c5df4510d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aec691ef1c3f8b1f097d426de19c51fc9a39bcd3002cf27303c6ea181155e87`

```dockerfile
```

-	Layers:
	-	`sha256:ea7448fd69d2025a02fa3773b13695b9ecaa34efd8cc5b223bd340a6a20bb280`  
		Last Modified: Tue, 09 Dec 2025 00:01:32 GMT  
		Size: 5.6 MB (5588377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15055f679734606495e25ae5c7b68d5ee1ec2609bfbca41b8eccfdc0431ef6dd`  
		Last Modified: Tue, 09 Dec 2025 00:01:32 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v5

```console
$ docker pull irssi@sha256:605f1644cbe09985d1b0a7159e6a3645cacce33a561adb3eb3994e2bb9fe1118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50943555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d5500fde47056d160fcf131159d65be22e1cce50911f44d2f5be15fc113c99`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:33:53 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:33:53 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:33:53 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:33:53 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:34:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:34:44 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:34:44 GMT
USER user
# Mon, 08 Dec 2025 22:34:44 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209b020e9b6936d49088aeb2fe32da563e0dc7240b53e7a4f55a0064bcc57dbb`  
		Last Modified: Mon, 08 Dec 2025 22:35:02 GMT  
		Size: 18.3 MB (18286366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e546d6b1c1001d996e09271aa06076bbf5076bf4c0f1a64a5a76db18e6351b32`  
		Last Modified: Mon, 08 Dec 2025 22:34:59 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c1c60a78876ca8d26fa893a37ff13080f097555eea972e3e45e59d912f5e9c`  
		Last Modified: Mon, 08 Dec 2025 22:35:00 GMT  
		Size: 4.7 MB (4709641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:42ce2f56fd00643a382954ddf368a7ad26f88a053b4a557aa1112ed9de67aac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192e3247c9d1fd1e403f1da43c465327ebe5a123a9caf785ea53b5dd0388c5cb`

```dockerfile
```

-	Layers:
	-	`sha256:dbd5f23d6f6d5ab003eddef0af01a8a8b66fac74afe90d0faa97afa2b0a581d2`  
		Last Modified: Tue, 09 Dec 2025 00:01:40 GMT  
		Size: 5.6 MB (5585926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:401ba355602555e19652809e181e8fc4d172d2140c0c17f0781b909a2bff847e`  
		Last Modified: Tue, 09 Dec 2025 00:01:41 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v7

```console
$ docker pull irssi@sha256:90bf141f8448f931b78a4759623391882ba8d3d0520b3770b063ea80daf29ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48681035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d9f126abb644aa91708596fe16f433c339727d7b73386dc26994eb1d0119af6`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:36:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:36:55 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:36:55 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:36:55 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:36:55 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:37:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:37:36 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:37:36 GMT
USER user
# Mon, 08 Dec 2025 22:37:36 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea7a0e9121517502a0452fd53a68bbbf3e120ea0391f4616c22058f3ffe83a6`  
		Last Modified: Mon, 08 Dec 2025 22:37:54 GMT  
		Size: 17.9 MB (17909125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a98b78793ec14ceabf793c4778fa9c59358545e4604a1c0b15bb6bd21bd755`  
		Last Modified: Mon, 08 Dec 2025 22:37:52 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c7e9fbcbad6965518fd24946faf5855bd7c2b9dbb7a8632a912292a76f391b`  
		Last Modified: Mon, 08 Dec 2025 22:37:53 GMT  
		Size: 4.6 MB (4558538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:529cccf10215bb411a271b196fe666e44db36c0c88bc62b754ae778cc278ef86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5070cb3b050937bc197ae388f5989122c8e4fc9558708e5cd01f7eb53047ec85`

```dockerfile
```

-	Layers:
	-	`sha256:82a650d25d6be9c0ec73d583a9bfbb7e4cdf26f7eac9d4a2c0b9165043d1c3b1`  
		Last Modified: Tue, 09 Dec 2025 00:01:47 GMT  
		Size: 5.6 MB (5588948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b12cb7447938f917d5345ecf33832b856ff04c97a5f9c2213b71e0a7d45d3fcc`  
		Last Modified: Tue, 09 Dec 2025 00:01:47 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:4ad94477cda90ae8d3d4d47ed0c1a58d162ca780cbc21e1e356ae833c2c9af51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53972792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6123fcf7ac4efb210283b7fab07ab5e1f866bcfa7ad8dbd2186bd66c2f88d4b2`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:35:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:35:56 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:35:56 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:35:56 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:35:56 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:36:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:36:32 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:36:32 GMT
USER user
# Mon, 08 Dec 2025 22:36:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271cd4b9332a86de31690e94a837946ec81b376cf3b99b9ec078b9997ebfc4e7`  
		Last Modified: Mon, 08 Dec 2025 22:36:51 GMT  
		Size: 19.0 MB (19049077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f51515c1d0d0bdda82745487e18f18f85d1a6999f3c82ff517039ed8c01ae9`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae317866ab39c091f9ece44d604dc3317877b2ed386b1ff38dcf25d62707f6e`  
		Last Modified: Mon, 08 Dec 2025 22:36:50 GMT  
		Size: 4.8 MB (4781724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:8a9848973ad593c402ad00791b8debf829808115d9215d351a4d092da9efdfb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e8e14ea45e56f1a280745e4215d6b09bf3bbe98d77d25ed701e1833b69db94`

```dockerfile
```

-	Layers:
	-	`sha256:833298ea4b4e32cd4be350f01f29cc972db0aa5f1e1b52c229e9611870f9d81d`  
		Last Modified: Tue, 09 Dec 2025 00:01:51 GMT  
		Size: 5.6 MB (5594861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12ec53196ee839e1d4fc9f760637572995c6cf92c75585cdf8a0ddebd72fd86a`  
		Last Modified: Tue, 09 Dec 2025 00:01:52 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; 386

```console
$ docker pull irssi@sha256:e3cb55074f79f7accb3186e087c8bcfbe5fb81bafed6b3843bbb182b831c2271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede6324a485fc1c56152548ccc95aa525d3e6298b82206a635b9e5bb2c43a274`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:34:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:34:50 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:34:50 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:34:50 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:34:50 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:35:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:35:33 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:35:33 GMT
USER user
# Mon, 08 Dec 2025 22:35:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92779a84b492a0e3f9b30abe3ba2c3f3c75f5f8bac0be5b3ec6f1d2151769a81`  
		Last Modified: Mon, 08 Dec 2025 22:35:51 GMT  
		Size: 18.7 MB (18740473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9e00516c012835613d2d6c24e48eca1db4092e2ae02a5557ef978565a9087b`  
		Last Modified: Mon, 08 Dec 2025 22:35:49 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380f851f46dcf6024e273c5690f4de14d4837fe4c9e173048edc3844675aefad`  
		Last Modified: Mon, 08 Dec 2025 22:35:49 GMT  
		Size: 4.9 MB (4868342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:0e026c9c8b43f1e4b3f0cf84c29441b70414ab67d248c56ebf7607efd867af5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c110c8c5132d6b986eca5007cb21a2921c655197298f96c1e6e3fe1d975295ce`

```dockerfile
```

-	Layers:
	-	`sha256:290278e5fa9964615268f167ae0917568dd48529eb40cb0fe4b7b6b4fd6db490`  
		Last Modified: Tue, 09 Dec 2025 00:01:57 GMT  
		Size: 5.6 MB (5584500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b86870229139d3e4a5b2f5fb461a45c930f312a775c5a1c86c120a2616479b3`  
		Last Modified: Tue, 09 Dec 2025 00:01:58 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; ppc64le

```console
$ docker pull irssi@sha256:93ea18bd78c1073049928098da83c8d7489f034eb6e93242c329dd6ac2f1928b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58240744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5496783653403c6d012d80f5d9f8c7a75a1093b7a1752b8fe2f67c024d71ba30`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:28:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:28:22 GMT
ENV HOME=/home/user
# Tue, 09 Dec 2025 00:28:22 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 09 Dec 2025 00:28:22 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 00:28:22 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 09 Dec 2025 00:30:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 09 Dec 2025 00:30:05 GMT
WORKDIR /home/user
# Tue, 09 Dec 2025 00:30:05 GMT
USER user
# Tue, 09 Dec 2025 00:30:05 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d43ff5db3e76c55de7b73205ca86bac1121de5d0f0c442c6d1fab408d40dbc4`  
		Last Modified: Tue, 09 Dec 2025 00:30:40 GMT  
		Size: 19.5 MB (19543101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20fac790531c01e08ec11e7ea8e6c78bc9732c6dd506329349609d5c47ea56b`  
		Last Modified: Tue, 09 Dec 2025 00:30:38 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e4e19b419b36bd43d3ecbb483048af4910c11c8ed72f86585d17de6a3cf367`  
		Last Modified: Tue, 09 Dec 2025 00:30:41 GMT  
		Size: 5.1 MB (5097391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:fe0f1b60af0b886246c9c854bfba7d6c86f3a936171bfe3afcb3fe3e72177db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aaaf9080eb40d58b04f0eb1b35aacf665d2ab2db092955824c8a40ab7b15d85`

```dockerfile
```

-	Layers:
	-	`sha256:e4b1401322d5b02c67c73ad0a132014ff5d6ebe1d604dbeb9595a74e83201f93`  
		Last Modified: Tue, 09 Dec 2025 02:59:59 GMT  
		Size: 5.6 MB (5595408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e74c10f22046f87919aa9d2d4f9fc0afaed79b0bdbbaad1bf79c689583b0b1c`  
		Last Modified: Tue, 09 Dec 2025 03:00:00 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; riscv64

```console
$ docker pull irssi@sha256:0a17bc9dc7f1ede0aae4d4035aa269c39fdd3ad059158a3c6a569fa2bf7da8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51686196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e6a1bc4c5ae216cf035ec48b010768259be2a066ee4ef066bcb9c32d445e4d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 10:01:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:01:44 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 10:01:44 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 10:01:44 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 10:01:44 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 10:08:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 10:08:36 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 10:08:36 GMT
USER user
# Tue, 18 Nov 2025 10:08:36 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afef2a7493fa326b06e464e36f2a79568e4c5c265515366e193165f0b4d284e`  
		Last Modified: Tue, 18 Nov 2025 10:10:42 GMT  
		Size: 18.5 MB (18549074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f026bbe28877d1917f647dacffd37172e95435e1c7e9fbe30a62986bb72cd62b`  
		Last Modified: Tue, 18 Nov 2025 10:10:41 GMT  
		Size: 3.3 KB (3337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3d248f54be38451080b4d25093d9df5c1c9efe1175c3cf58494a7e0fd7fe62`  
		Last Modified: Tue, 18 Nov 2025 10:10:41 GMT  
		Size: 4.9 MB (4860627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:7b01cdd2258dc9fd9266a05e6cbd264f72886699285f27da4dcfa624dcb82f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afb4ae2e3561846a1f14e41a61390911210a0c9ea6b4f9bace7ef57ca7a1303`

```dockerfile
```

-	Layers:
	-	`sha256:5044523627d968ee0b87912ad5e86b6f374ff85ef9a7878ae77c52dcf5581421`  
		Last Modified: Tue, 18 Nov 2025 18:00:24 GMT  
		Size: 5.6 MB (5579680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43863609ed306f6a1f2ac385d2c41ef9efb115640066a4bb3b02043bb96f7158`  
		Last Modified: Tue, 18 Nov 2025 18:00:25 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; s390x

```console
$ docker pull irssi@sha256:79ceeb6e5f00cadefc5098892f4fdd847c8a6c7147214049af36f2988eb63701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54503098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4447f6a16ef4660d5cc882de4451987df832e0221f3c9198582f5041d9e484`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:33:35 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:33:35 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:33:35 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:33:35 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:34:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:34:10 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:34:10 GMT
USER user
# Mon, 08 Dec 2025 22:34:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a68582eda8cf9c795e8fac7bd4a06d7b4cf05bcce0b996577a486d0e34b56c`  
		Last Modified: Mon, 08 Dec 2025 22:34:33 GMT  
		Size: 19.8 MB (19759448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea7a5c770aac1d19a49e32bddbb9b474dd2746e7821d20791e1b80abfa3b5a3`  
		Last Modified: Mon, 08 Dec 2025 22:34:31 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fe49ac5d532203fa75223786c8c8ef7f78fbdeff8227abdab3b6e08125de53`  
		Last Modified: Mon, 08 Dec 2025 22:34:32 GMT  
		Size: 4.9 MB (4905890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:afc0d5563715a205bdbf09adfb0dcb772d44ec5f9f64be619112ea71bef71370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb41a3e51a7b6c277c4898dede97241725067c20506fcd3897eb9a2fa33ef8fc`

```dockerfile
```

-	Layers:
	-	`sha256:9292a924a5f71b0700ea789b79e1a8bf1256af5aae51b422283563c1fa34bf6e`  
		Last Modified: Tue, 09 Dec 2025 00:02:15 GMT  
		Size: 5.6 MB (5589282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff40bc8ca1364bffe8c60be1df3e2bffedbd27bb8dbcf6db778c754320ccf6e`  
		Last Modified: Tue, 09 Dec 2025 00:02:16 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:trixie`

```console
$ docker pull irssi@sha256:19043dddac4df97572295eb4df56b6e5e8d1244a09ece798931a7e728e2099b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
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

### `irssi:trixie` - linux; amd64

```console
$ docker pull irssi@sha256:ba548a27a12441efe110f9a056e793d722bda4a4eb13a3ceea8bf8d2d5ac1e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53869300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ebb967af1ef6016f39c7253143525ae93880628cdbc3e189772a2d029fc1a25`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:37:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:37:12 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:37:12 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:37:12 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:37:12 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:37:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:37:51 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:37:51 GMT
USER user
# Mon, 08 Dec 2025 22:37:51 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae9ff25045243dc27c083564f101c73527fab1e4d6de25faafe1d20c6993d0f`  
		Last Modified: Mon, 08 Dec 2025 22:38:10 GMT  
		Size: 19.2 MB (19222767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cff4c278980a41219ced1054076473f352a9ab538703fdb0508673575901de`  
		Last Modified: Mon, 08 Dec 2025 22:38:08 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6979d38c29179b5f4797ac48f3389f2044fb0312d0cd3b7f7fe377d41762cf9c`  
		Last Modified: Mon, 08 Dec 2025 22:38:08 GMT  
		Size: 4.9 MB (4866682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:2c34f0b8bd4789c746b87fcefbeca5053bc49367fbe0106f8c1f2c5df4510d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aec691ef1c3f8b1f097d426de19c51fc9a39bcd3002cf27303c6ea181155e87`

```dockerfile
```

-	Layers:
	-	`sha256:ea7448fd69d2025a02fa3773b13695b9ecaa34efd8cc5b223bd340a6a20bb280`  
		Last Modified: Tue, 09 Dec 2025 00:01:32 GMT  
		Size: 5.6 MB (5588377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15055f679734606495e25ae5c7b68d5ee1ec2609bfbca41b8eccfdc0431ef6dd`  
		Last Modified: Tue, 09 Dec 2025 00:01:32 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:605f1644cbe09985d1b0a7159e6a3645cacce33a561adb3eb3994e2bb9fe1118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50943555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d5500fde47056d160fcf131159d65be22e1cce50911f44d2f5be15fc113c99`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:33:53 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:33:53 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:33:53 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:33:53 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:34:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:34:44 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:34:44 GMT
USER user
# Mon, 08 Dec 2025 22:34:44 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209b020e9b6936d49088aeb2fe32da563e0dc7240b53e7a4f55a0064bcc57dbb`  
		Last Modified: Mon, 08 Dec 2025 22:35:02 GMT  
		Size: 18.3 MB (18286366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e546d6b1c1001d996e09271aa06076bbf5076bf4c0f1a64a5a76db18e6351b32`  
		Last Modified: Mon, 08 Dec 2025 22:34:59 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c1c60a78876ca8d26fa893a37ff13080f097555eea972e3e45e59d912f5e9c`  
		Last Modified: Mon, 08 Dec 2025 22:35:00 GMT  
		Size: 4.7 MB (4709641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:42ce2f56fd00643a382954ddf368a7ad26f88a053b4a557aa1112ed9de67aac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192e3247c9d1fd1e403f1da43c465327ebe5a123a9caf785ea53b5dd0388c5cb`

```dockerfile
```

-	Layers:
	-	`sha256:dbd5f23d6f6d5ab003eddef0af01a8a8b66fac74afe90d0faa97afa2b0a581d2`  
		Last Modified: Tue, 09 Dec 2025 00:01:40 GMT  
		Size: 5.6 MB (5585926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:401ba355602555e19652809e181e8fc4d172d2140c0c17f0781b909a2bff847e`  
		Last Modified: Tue, 09 Dec 2025 00:01:41 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:90bf141f8448f931b78a4759623391882ba8d3d0520b3770b063ea80daf29ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48681035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d9f126abb644aa91708596fe16f433c339727d7b73386dc26994eb1d0119af6`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:36:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:36:55 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:36:55 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:36:55 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:36:55 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:37:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:37:36 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:37:36 GMT
USER user
# Mon, 08 Dec 2025 22:37:36 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea7a0e9121517502a0452fd53a68bbbf3e120ea0391f4616c22058f3ffe83a6`  
		Last Modified: Mon, 08 Dec 2025 22:37:54 GMT  
		Size: 17.9 MB (17909125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a98b78793ec14ceabf793c4778fa9c59358545e4604a1c0b15bb6bd21bd755`  
		Last Modified: Mon, 08 Dec 2025 22:37:52 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c7e9fbcbad6965518fd24946faf5855bd7c2b9dbb7a8632a912292a76f391b`  
		Last Modified: Mon, 08 Dec 2025 22:37:53 GMT  
		Size: 4.6 MB (4558538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:529cccf10215bb411a271b196fe666e44db36c0c88bc62b754ae778cc278ef86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5070cb3b050937bc197ae388f5989122c8e4fc9558708e5cd01f7eb53047ec85`

```dockerfile
```

-	Layers:
	-	`sha256:82a650d25d6be9c0ec73d583a9bfbb7e4cdf26f7eac9d4a2c0b9165043d1c3b1`  
		Last Modified: Tue, 09 Dec 2025 00:01:47 GMT  
		Size: 5.6 MB (5588948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b12cb7447938f917d5345ecf33832b856ff04c97a5f9c2213b71e0a7d45d3fcc`  
		Last Modified: Tue, 09 Dec 2025 00:01:47 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:4ad94477cda90ae8d3d4d47ed0c1a58d162ca780cbc21e1e356ae833c2c9af51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53972792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6123fcf7ac4efb210283b7fab07ab5e1f866bcfa7ad8dbd2186bd66c2f88d4b2`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:35:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:35:56 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:35:56 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:35:56 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:35:56 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:36:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:36:32 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:36:32 GMT
USER user
# Mon, 08 Dec 2025 22:36:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271cd4b9332a86de31690e94a837946ec81b376cf3b99b9ec078b9997ebfc4e7`  
		Last Modified: Mon, 08 Dec 2025 22:36:51 GMT  
		Size: 19.0 MB (19049077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f51515c1d0d0bdda82745487e18f18f85d1a6999f3c82ff517039ed8c01ae9`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae317866ab39c091f9ece44d604dc3317877b2ed386b1ff38dcf25d62707f6e`  
		Last Modified: Mon, 08 Dec 2025 22:36:50 GMT  
		Size: 4.8 MB (4781724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:8a9848973ad593c402ad00791b8debf829808115d9215d351a4d092da9efdfb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e8e14ea45e56f1a280745e4215d6b09bf3bbe98d77d25ed701e1833b69db94`

```dockerfile
```

-	Layers:
	-	`sha256:833298ea4b4e32cd4be350f01f29cc972db0aa5f1e1b52c229e9611870f9d81d`  
		Last Modified: Tue, 09 Dec 2025 00:01:51 GMT  
		Size: 5.6 MB (5594861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12ec53196ee839e1d4fc9f760637572995c6cf92c75585cdf8a0ddebd72fd86a`  
		Last Modified: Tue, 09 Dec 2025 00:01:52 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; 386

```console
$ docker pull irssi@sha256:e3cb55074f79f7accb3186e087c8bcfbe5fb81bafed6b3843bbb182b831c2271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede6324a485fc1c56152548ccc95aa525d3e6298b82206a635b9e5bb2c43a274`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:34:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:34:50 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:34:50 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:34:50 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:34:50 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:35:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:35:33 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:35:33 GMT
USER user
# Mon, 08 Dec 2025 22:35:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92779a84b492a0e3f9b30abe3ba2c3f3c75f5f8bac0be5b3ec6f1d2151769a81`  
		Last Modified: Mon, 08 Dec 2025 22:35:51 GMT  
		Size: 18.7 MB (18740473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9e00516c012835613d2d6c24e48eca1db4092e2ae02a5557ef978565a9087b`  
		Last Modified: Mon, 08 Dec 2025 22:35:49 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380f851f46dcf6024e273c5690f4de14d4837fe4c9e173048edc3844675aefad`  
		Last Modified: Mon, 08 Dec 2025 22:35:49 GMT  
		Size: 4.9 MB (4868342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:0e026c9c8b43f1e4b3f0cf84c29441b70414ab67d248c56ebf7607efd867af5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c110c8c5132d6b986eca5007cb21a2921c655197298f96c1e6e3fe1d975295ce`

```dockerfile
```

-	Layers:
	-	`sha256:290278e5fa9964615268f167ae0917568dd48529eb40cb0fe4b7b6b4fd6db490`  
		Last Modified: Tue, 09 Dec 2025 00:01:57 GMT  
		Size: 5.6 MB (5584500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b86870229139d3e4a5b2f5fb461a45c930f312a775c5a1c86c120a2616479b3`  
		Last Modified: Tue, 09 Dec 2025 00:01:58 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:93ea18bd78c1073049928098da83c8d7489f034eb6e93242c329dd6ac2f1928b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58240744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5496783653403c6d012d80f5d9f8c7a75a1093b7a1752b8fe2f67c024d71ba30`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:28:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:28:22 GMT
ENV HOME=/home/user
# Tue, 09 Dec 2025 00:28:22 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 09 Dec 2025 00:28:22 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 00:28:22 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 09 Dec 2025 00:30:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 09 Dec 2025 00:30:05 GMT
WORKDIR /home/user
# Tue, 09 Dec 2025 00:30:05 GMT
USER user
# Tue, 09 Dec 2025 00:30:05 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d43ff5db3e76c55de7b73205ca86bac1121de5d0f0c442c6d1fab408d40dbc4`  
		Last Modified: Tue, 09 Dec 2025 00:30:40 GMT  
		Size: 19.5 MB (19543101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20fac790531c01e08ec11e7ea8e6c78bc9732c6dd506329349609d5c47ea56b`  
		Last Modified: Tue, 09 Dec 2025 00:30:38 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e4e19b419b36bd43d3ecbb483048af4910c11c8ed72f86585d17de6a3cf367`  
		Last Modified: Tue, 09 Dec 2025 00:30:41 GMT  
		Size: 5.1 MB (5097391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:fe0f1b60af0b886246c9c854bfba7d6c86f3a936171bfe3afcb3fe3e72177db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aaaf9080eb40d58b04f0eb1b35aacf665d2ab2db092955824c8a40ab7b15d85`

```dockerfile
```

-	Layers:
	-	`sha256:e4b1401322d5b02c67c73ad0a132014ff5d6ebe1d604dbeb9595a74e83201f93`  
		Last Modified: Tue, 09 Dec 2025 02:59:59 GMT  
		Size: 5.6 MB (5595408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e74c10f22046f87919aa9d2d4f9fc0afaed79b0bdbbaad1bf79c689583b0b1c`  
		Last Modified: Tue, 09 Dec 2025 03:00:00 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:0a17bc9dc7f1ede0aae4d4035aa269c39fdd3ad059158a3c6a569fa2bf7da8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51686196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e6a1bc4c5ae216cf035ec48b010768259be2a066ee4ef066bcb9c32d445e4d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 10:01:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:01:44 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 10:01:44 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 10:01:44 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 10:01:44 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 10:08:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 10:08:36 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 10:08:36 GMT
USER user
# Tue, 18 Nov 2025 10:08:36 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afef2a7493fa326b06e464e36f2a79568e4c5c265515366e193165f0b4d284e`  
		Last Modified: Tue, 18 Nov 2025 10:10:42 GMT  
		Size: 18.5 MB (18549074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f026bbe28877d1917f647dacffd37172e95435e1c7e9fbe30a62986bb72cd62b`  
		Last Modified: Tue, 18 Nov 2025 10:10:41 GMT  
		Size: 3.3 KB (3337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3d248f54be38451080b4d25093d9df5c1c9efe1175c3cf58494a7e0fd7fe62`  
		Last Modified: Tue, 18 Nov 2025 10:10:41 GMT  
		Size: 4.9 MB (4860627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:7b01cdd2258dc9fd9266a05e6cbd264f72886699285f27da4dcfa624dcb82f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afb4ae2e3561846a1f14e41a61390911210a0c9ea6b4f9bace7ef57ca7a1303`

```dockerfile
```

-	Layers:
	-	`sha256:5044523627d968ee0b87912ad5e86b6f374ff85ef9a7878ae77c52dcf5581421`  
		Last Modified: Tue, 18 Nov 2025 18:00:24 GMT  
		Size: 5.6 MB (5579680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43863609ed306f6a1f2ac385d2c41ef9efb115640066a4bb3b02043bb96f7158`  
		Last Modified: Tue, 18 Nov 2025 18:00:25 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; s390x

```console
$ docker pull irssi@sha256:79ceeb6e5f00cadefc5098892f4fdd847c8a6c7147214049af36f2988eb63701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54503098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4447f6a16ef4660d5cc882de4451987df832e0221f3c9198582f5041d9e484`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:33:35 GMT
ENV HOME=/home/user
# Mon, 08 Dec 2025 22:33:35 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 08 Dec 2025 22:33:35 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 22:33:35 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 08 Dec 2025 22:34:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 08 Dec 2025 22:34:10 GMT
WORKDIR /home/user
# Mon, 08 Dec 2025 22:34:10 GMT
USER user
# Mon, 08 Dec 2025 22:34:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a68582eda8cf9c795e8fac7bd4a06d7b4cf05bcce0b996577a486d0e34b56c`  
		Last Modified: Mon, 08 Dec 2025 22:34:33 GMT  
		Size: 19.8 MB (19759448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea7a5c770aac1d19a49e32bddbb9b474dd2746e7821d20791e1b80abfa3b5a3`  
		Last Modified: Mon, 08 Dec 2025 22:34:31 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fe49ac5d532203fa75223786c8c8ef7f78fbdeff8227abdab3b6e08125de53`  
		Last Modified: Mon, 08 Dec 2025 22:34:32 GMT  
		Size: 4.9 MB (4905890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:afc0d5563715a205bdbf09adfb0dcb772d44ec5f9f64be619112ea71bef71370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb41a3e51a7b6c277c4898dede97241725067c20506fcd3897eb9a2fa33ef8fc`

```dockerfile
```

-	Layers:
	-	`sha256:9292a924a5f71b0700ea789b79e1a8bf1256af5aae51b422283563c1fa34bf6e`  
		Last Modified: Tue, 09 Dec 2025 00:02:15 GMT  
		Size: 5.6 MB (5589282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff40bc8ca1364bffe8c60be1df3e2bffedbd27bb8dbcf6db778c754320ccf6e`  
		Last Modified: Tue, 09 Dec 2025 00:02:16 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json
