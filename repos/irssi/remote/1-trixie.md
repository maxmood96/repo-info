## `irssi:1-trixie`

```console
$ docker pull irssi@sha256:ab83c608a92f414b510d1aeac4b1985a65984a31cc112b16e6175d6af6e6fc5a
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
$ docker pull irssi@sha256:7398896e76791c8a6f48e6889aba16682fedd1f0bc2bd75caa6574b0c830c02e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53864209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e64037afadf0707edd5aa3ae820bbcafc272a9a8fda110fbb21d9c38bd2d81e`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
ENV HOME=/home/user
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
ENV LANG=C.UTF-8
# Mon, 11 Aug 2025 16:45:42 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
WORKDIR /home/user
# Mon, 11 Aug 2025 16:45:42 GMT
USER user
# Mon, 11 Aug 2025 16:45:42 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d21d8d3cefb0fe84f6ca62dd5d78babca5d7b39c11aa94c40ad48fb6934570`  
		Last Modified: Tue, 12 Aug 2025 23:39:52 GMT  
		Size: 19.2 MB (19222065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5679b3451c3570bbd8906ee0b35c8f5c788391d90491bca6128a45c588af5ecc`  
		Last Modified: Tue, 12 Aug 2025 23:39:49 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a4c47be8e074821b3e68fca234af7ff0f5eb77df9fef15971d80a476892563`  
		Last Modified: Tue, 12 Aug 2025 23:39:51 GMT  
		Size: 4.9 MB (4865503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:6b0226923177745f4441d07b02ce108a962bdc2492f796b4e3de0641416af362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5606143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd017519672cb4e40abfa5e7015b834dac029e18d21e7c745daa039d26a37bc`

```dockerfile
```

-	Layers:
	-	`sha256:7b54864f671846a7a3a3d0f65f87ecfa0f2fb3da02d79743eda30c7ec0412cea`  
		Last Modified: Wed, 13 Aug 2025 01:59:23 GMT  
		Size: 5.6 MB (5587449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8772d8c3f9f671c1882b92127e351b6673fc88caacdf580c6ad6a24bb700f061`  
		Last Modified: Wed, 13 Aug 2025 01:59:24 GMT  
		Size: 18.7 KB (18694 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:d5ab016b397e9ce6bf2df4586aeefeec8b1cefbbafb87b9a506541fff4753334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50940618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71aca4a28dca9c5ddc3d27e484fad1a7e5935bc471f45de0d168e90a6c214ff5`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1754870400'
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
ENV HOME=/home/user
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
ENV LANG=C.UTF-8
# Mon, 11 Aug 2025 16:45:42 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
WORKDIR /home/user
# Mon, 11 Aug 2025 16:45:42 GMT
USER user
# Mon, 11 Aug 2025 16:45:42 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:498399880872f14c562c46bd2a1ef4cfcf3c2a1453514ff0d0f6b7d89f8010dd`  
		Last Modified: Tue, 12 Aug 2025 22:02:01 GMT  
		Size: 27.9 MB (27941706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346378d648b66fbf52966025f8faef2a14fe8188d748fcf1615e4f4bd9ff60ff`  
		Last Modified: Wed, 13 Aug 2025 01:43:50 GMT  
		Size: 18.3 MB (18286531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6cd40c73b4f14aa0bcabf0af3ba3aa1eede7225a5fb7eef3d5bceb21aa908c`  
		Last Modified: Wed, 13 Aug 2025 01:43:50 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90353c15119d833de35cf3d659b9b4f33b0de474fd9ce5cbe67af83221b8c704`  
		Last Modified: Wed, 13 Aug 2025 01:43:51 GMT  
		Size: 4.7 MB (4709021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:2aea0ec5cc053f19d16e8177ee7b3c3d32951ac0420081ace40824199bf96519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875ca5cb54e72995b309cccc5cbf8b0b5900076f8fa5cfd966e91c1b8a03ad40`

```dockerfile
```

-	Layers:
	-	`sha256:554142e0e5ec7d84326960989c636400ba006769fd4961d01df058d44547173e`  
		Last Modified: Wed, 13 Aug 2025 04:59:27 GMT  
		Size: 5.6 MB (5584998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b34a0ebd0ea275cb4870ebae6b66c1e3d6449009de56d256f062115a65a46102`  
		Last Modified: Wed, 13 Aug 2025 04:59:29 GMT  
		Size: 18.8 KB (18828 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:0ccb1f67c7bd46cc5a4b82c28afa8725deafab8d244b1154b48e4fb3c98f4e20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48677120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1282e9d931841daf278b717f6bd4c607d44f654742ec2e2f67f6702ec60d706d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
ENV HOME=/home/user
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
ENV LANG=C.UTF-8
# Mon, 11 Aug 2025 16:45:42 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
WORKDIR /home/user
# Mon, 11 Aug 2025 16:45:42 GMT
USER user
# Mon, 11 Aug 2025 16:45:42 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5cab0fd36e22f3167d8ac088b006dba1f05adbb31743844cb18fbc8fbfe9d7`  
		Last Modified: Wed, 13 Aug 2025 02:54:47 GMT  
		Size: 17.9 MB (17909029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68e1ccd7a69ea7968427bc483f01df9dcd5bcc72f2293db2789832e41d6a919`  
		Last Modified: Wed, 13 Aug 2025 02:54:44 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1483c283b534fa8bb61e9286056251fd474ff0520bc04620cc871e495dc519e3`  
		Last Modified: Wed, 13 Aug 2025 02:54:45 GMT  
		Size: 4.6 MB (4557246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:d39162439acd085300078ee02e583f26178e1798b83158a3e7bb1cf13b0dcb4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5606847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7025f32fa29df7f099705370fef3c82b792d72cc2d0b7fb679120d168a3d77a`

```dockerfile
```

-	Layers:
	-	`sha256:062e6545743d03225a3a08c7ba38836f8d71bc1799ecba0d2fcb9f0f9533aa13`  
		Last Modified: Wed, 13 Aug 2025 04:59:34 GMT  
		Size: 5.6 MB (5588020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7735c105059cadbbf5083bf4b575cc53a303e68162c869b5d367585f06aff5c`  
		Last Modified: Wed, 13 Aug 2025 04:59:35 GMT  
		Size: 18.8 KB (18827 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:09f56fe9e8eec76e437d704b4a4e8679391fc039412d217574d1bb0205138681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53969818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb2244ea65f88d49d996e543b798865c6da0a59bb4d6cfb2870e52ad4a48f7a`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
ENV HOME=/home/user
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
ENV LANG=C.UTF-8
# Mon, 11 Aug 2025 16:45:42 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
WORKDIR /home/user
# Mon, 11 Aug 2025 16:45:42 GMT
USER user
# Mon, 11 Aug 2025 16:45:42 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0caf570426750d4bdde7e97f1a851b6b588e80e1cb23ae974edaaa18bcec44a4`  
		Last Modified: Wed, 13 Aug 2025 03:01:35 GMT  
		Size: 19.0 MB (19049336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa50cc87bfbaeb5a6fff385230a401697b01e2afb4814ed21acfbd5985b47c58`  
		Last Modified: Wed, 13 Aug 2025 03:01:30 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b104a5eb5efd32f33f98477372f5539b17e32cb1a336f9166b72556353561af8`  
		Last Modified: Wed, 13 Aug 2025 03:01:34 GMT  
		Size: 4.8 MB (4781076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:92db2d4f59409a60217a3d6d51590e5e1768fb2fd63ce5ef5ee764110b36389d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5612808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eef665875f85efda2db45558a87501258adcdf531d105bf11560f15f27c2d1b`

```dockerfile
```

-	Layers:
	-	`sha256:7d0ba1b8d5613eac99b67a4f02099ad92832153acbd64f601fbf84f67f1a0ce0`  
		Last Modified: Wed, 13 Aug 2025 04:59:40 GMT  
		Size: 5.6 MB (5593933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:134f2dafdcf5ccbecc4181b5369026caf9716e7b9ab17f3cc5f4fff3dfc18c08`  
		Last Modified: Wed, 13 Aug 2025 04:59:41 GMT  
		Size: 18.9 KB (18875 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; 386

```console
$ docker pull irssi@sha256:2b8510fdd6303c8478599177a6a7291e7e385b8d15f9f1826c5c17624db6b1d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54900489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822998f9da5d1b7c9e4691dbede7c052c47928b1176b7bf6fa6e1a9e0b7b3dcd`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
ENV HOME=/home/user
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
ENV LANG=C.UTF-8
# Mon, 11 Aug 2025 16:45:42 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
WORKDIR /home/user
# Mon, 11 Aug 2025 16:45:42 GMT
USER user
# Mon, 11 Aug 2025 16:45:42 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c1bd8fc9bf23f24f7cadec63470bb3ffff07e9fdef38fba1c0085a7c80f5832`  
		Last Modified: Tue, 12 Aug 2025 23:39:52 GMT  
		Size: 18.7 MB (18740603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc00f7a892d0a3480b837cc5a7355d23008438aee7c63557c990bd04018e81b9`  
		Last Modified: Tue, 12 Aug 2025 23:39:51 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00bde766b54345f633730cd03c1e7ad0c5d832acd6db3cf4f413397d394747a`  
		Last Modified: Tue, 12 Aug 2025 23:39:51 GMT  
		Size: 4.9 MB (4867148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:63e63227fa4473402dd6f72d5b37d827547421177251cc0f387eb3fa5fa59b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5602210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9fe3d3d47c41f9e11cce28818a965cd3a28d869c83e4f56343ab3c54520b31`

```dockerfile
```

-	Layers:
	-	`sha256:449c7eb5bd8c28ff89a7b76264c894722a6c06ab9114e7e17e66194ca6cf5ae6`  
		Last Modified: Wed, 13 Aug 2025 01:59:30 GMT  
		Size: 5.6 MB (5583572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbdc6373690f65476a7ffe871888f71d6cbb268277b6dd957d2adc153640b22c`  
		Last Modified: Wed, 13 Aug 2025 01:59:31 GMT  
		Size: 18.6 KB (18638 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:705ccb42665fc24e5711ab6cd641eff4d7bc378efe699551833304c8ebeb6732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58236332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea01c27ec2a2039845a2282bad750b2f4c945ed1b593220b3815253a6d09c3c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
ENV HOME=/home/user
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
ENV LANG=C.UTF-8
# Mon, 11 Aug 2025 16:45:42 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
WORKDIR /home/user
# Mon, 11 Aug 2025 16:45:42 GMT
USER user
# Mon, 11 Aug 2025 16:45:42 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6dbfed38402c3a6ae343a7b5e3e24084ae658429f5614f9cae88c8015912456`  
		Last Modified: Wed, 13 Aug 2025 04:51:37 GMT  
		Size: 19.5 MB (19542289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5f8cdcdba2d7ba10e7ff856b3acfd6ec341449c10a06cbb575b483df57a013`  
		Last Modified: Wed, 13 Aug 2025 04:51:35 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a2185018bd61c39e5fe09233abb78c4683039cd391a9518ebb9bbbbde74fcc`  
		Last Modified: Wed, 13 Aug 2025 04:51:35 GMT  
		Size: 5.1 MB (5096472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:b449ceb38fe35b9d3b2f055b14cf9baef635a968d376873e2cf07bc9c12da586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed63e8a709805dad274fc48f7842373bdae60468daef8f69a525ba56130b86b4`

```dockerfile
```

-	Layers:
	-	`sha256:c9e7ec3164cea82c44e5e4a7e2ce5dcbaf21681e539ac7f520663b5f18be113e`  
		Last Modified: Wed, 13 Aug 2025 07:59:38 GMT  
		Size: 5.6 MB (5594480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53c52d1829e7dc1e1420162de6c9fae2228d10f461732fa93df28e21e87b0c55`  
		Last Modified: Wed, 13 Aug 2025 07:59:39 GMT  
		Size: 18.8 KB (18766 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:8f8637fe913064cfbc2fa2bb1cb4d66ad28ee1a935d1238125764c4a4e763240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51683694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ca37ec8afd9d241d622fe15c2a65ebe38aa0a39d2fec0b43066f6fcec0a90e`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
ENV HOME=/home/user
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
ENV LANG=C.UTF-8
# Mon, 11 Aug 2025 16:45:42 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
WORKDIR /home/user
# Mon, 11 Aug 2025 16:45:42 GMT
USER user
# Mon, 11 Aug 2025 16:45:42 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c06a3222e88ed840b1ac200e6df35a4a10c8f3a01b74a7367f2e7c64acedc8`  
		Last Modified: Wed, 13 Aug 2025 11:02:32 GMT  
		Size: 18.5 MB (18548816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8491db56a2d24536096f4792720b8538dceecbd4652a0a13b8b41d11f5a94811`  
		Last Modified: Wed, 13 Aug 2025 10:18:42 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dec5c0bd1a94b2c01b2b10b2240f03e88b0e3366bce402601a13c24b233ff8d`  
		Last Modified: Wed, 13 Aug 2025 10:18:49 GMT  
		Size: 4.9 MB (4859896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:29c57a7dd85bc4c527b4fda41ff482bba414e48cd3894dde90806188a669a88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5597518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:587eae02f903180e82164e4ffd9c42e981e35d70d66cdb4e1989c41f649f69f0`

```dockerfile
```

-	Layers:
	-	`sha256:4128ec00f64a84c3499b73eb7bbc428b797429fb8e0f9c6f9fbbb474f27f1b39`  
		Last Modified: Wed, 13 Aug 2025 10:59:44 GMT  
		Size: 5.6 MB (5578752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2a9dc47f7df355b3fcca7036b52393f544e0dc74d7bafd2cb13271318213f49`  
		Last Modified: Wed, 13 Aug 2025 10:59:45 GMT  
		Size: 18.8 KB (18766 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; s390x

```console
$ docker pull irssi@sha256:0ccbfc14fb203c6ef64b3942fd89d870c3218fd330d22cde57871d1fe714c348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54501611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c5c34670b2808a7759c7b99e019715dbcc5978432f59d746664f61be0422ac5`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
ENV HOME=/home/user
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
ENV LANG=C.UTF-8
# Mon, 11 Aug 2025 16:45:42 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
WORKDIR /home/user
# Mon, 11 Aug 2025 16:45:42 GMT
USER user
# Mon, 11 Aug 2025 16:45:42 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9af2d640947b3989224e40b9c677a7b69352d3b0dd06e006228434f4a33455`  
		Last Modified: Wed, 13 Aug 2025 09:16:50 GMT  
		Size: 19.8 MB (19759763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff3954c8bf0576d3bd8613d36d27eedf8a50a9b777b3e3424964d00a27856830`  
		Last Modified: Wed, 13 Aug 2025 08:19:57 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70745ffb0cc42b83c048dedfcedc881d28b2accfbda3893e1600fc95f921c9c5`  
		Last Modified: Wed, 13 Aug 2025 08:20:01 GMT  
		Size: 4.9 MB (4905431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:dbc2e7f8e087aac6d433704238987b47849774d2aeff6d214c18a7ccb79f7705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af489dab1c7c89c5787fee00d6484b05fdfc06fb261968fef887b5fb63d83505`

```dockerfile
```

-	Layers:
	-	`sha256:4437b31003a27e750a587dafd7a0ca6ed6c061fe8a5291eec41a0cc26832dae5`  
		Last Modified: Wed, 13 Aug 2025 10:59:50 GMT  
		Size: 5.6 MB (5588354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02080434bcbb3745c80a050953b233f149f067098ab91dbb1904153dfb20e859`  
		Last Modified: Wed, 13 Aug 2025 10:59:51 GMT  
		Size: 18.7 KB (18694 bytes)  
		MIME: application/vnd.in-toto+json
