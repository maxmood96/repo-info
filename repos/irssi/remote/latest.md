## `irssi:latest`

```console
$ docker pull irssi@sha256:f23fbb8b1fa045eadf3b2acd06587865d811920c47a28ced47c6071348cf06d8
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
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
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
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
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
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
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
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
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
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
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
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
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
$ docker pull irssi@sha256:5fd8253717644b6270733622a97e41917f283621faeec759b246947adf77fedd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51686162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d03f27678d2b4ef07cdf436afe2205763c4160acd7830d823ba80cff8cce64d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 05:21:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 05:21:42 GMT
ENV HOME=/home/user
# Tue, 09 Dec 2025 05:21:42 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 09 Dec 2025 05:21:42 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 05:21:42 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 09 Dec 2025 05:28:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 09 Dec 2025 05:28:28 GMT
WORKDIR /home/user
# Tue, 09 Dec 2025 05:28:28 GMT
USER user
# Tue, 09 Dec 2025 05:28:28 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48378c4787aa0d9913ef1d060d4364edfd92d4e9543c5a9ddc8912e93dfd14e7`  
		Last Modified: Tue, 09 Dec 2025 05:30:30 GMT  
		Size: 18.5 MB (18549064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c877858540b876651157ef02a27381885fe9b00e248261583f50ba42dd3f46f`  
		Last Modified: Tue, 09 Dec 2025 05:30:29 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5407114727f79e076f4a8eac0a5270cf3d2e1eaefbb1ea46fd97a944eb47d8f`  
		Last Modified: Tue, 09 Dec 2025 05:30:30 GMT  
		Size: 4.9 MB (4860579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:1b92fd8833f5dd070657c1ec551487f7908d41f8c197a02d2c94c0be1cf88fdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3749a78e7479d9c96e755a69156fecadccf437bf71397e86766b831e6d90ca88`

```dockerfile
```

-	Layers:
	-	`sha256:795aa680729a190646d3d49c4585f4d5c1d1de9b667004cfee4edb5fc9a40095`  
		Last Modified: Tue, 09 Dec 2025 08:59:45 GMT  
		Size: 5.6 MB (5579680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee3a97a13316932827a6a4f79029ac46bdd1f33c61cd3cfa84546bbfb396c0cf`  
		Last Modified: Tue, 09 Dec 2025 08:59:46 GMT  
		Size: 18.7 KB (18723 bytes)  
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
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
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
