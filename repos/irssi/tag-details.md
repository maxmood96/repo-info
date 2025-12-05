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
$ docker pull irssi@sha256:f16b9ab6967270a5b2d0745b7f6b9233f6226b9866de8e46ab3f67f20167dde3
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
$ docker pull irssi@sha256:1c3ad0c692729985069dc605f6970c498536ff77cdc28731957a9981bb5cc69d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53869276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d8b5071dd14f9cc7babdbbb92be355488770afbb4baa1dd4193f835544e54d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:18:09 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 04:18:09 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 04:18:09 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:18:09 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 04:18:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 04:18:46 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 04:18:46 GMT
USER user
# Tue, 18 Nov 2025 04:18:46 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3defe69b9d42ee331ee4997997e0b6950a228ac42a28acb744b2a217802984`  
		Last Modified: Tue, 18 Nov 2025 04:19:08 GMT  
		Size: 19.2 MB (19222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d261d2d2be0daf5812e199043e646cd3b38c72c6a85a46d1aa2664afbbfdab`  
		Last Modified: Tue, 18 Nov 2025 04:19:07 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fb0ce4ebcc67d4eb7b0fd5a6f142adedb46b4a4b5c9f752bb3663092160fd4`  
		Last Modified: Tue, 18 Nov 2025 04:19:07 GMT  
		Size: 4.9 MB (4866605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:22bdb7c49ddfaba85497f04c9d268938716f3b3352fe24378d933a7732e8d145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d4070dfa4342b3ae917c1f765452b8b31cbfe6c04864d806db24d761ba3c65`

```dockerfile
```

-	Layers:
	-	`sha256:5234daf2a71968c25322c71bfea4cdc75082624fc15fcfa85f68596c0e1e8722`  
		Last Modified: Tue, 18 Nov 2025 06:01:31 GMT  
		Size: 5.6 MB (5588377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef6a5104b772e5ddb76df8ed09e14d2aaf8f4757fd03c65a00ce68904337b081`  
		Last Modified: Tue, 18 Nov 2025 06:01:32 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v5

```console
$ docker pull irssi@sha256:3bfeabfea3f173a6eef66224244f7c8ab79162e4b3e3454b5d7b951b699e6d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50944118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce561de65d9ced729b270243f33a9fe650e7088512ea128954c48a408518f61`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:22:31 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:22:31 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:22:31 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:22:31 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:23:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:23:21 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:23:21 GMT
USER user
# Tue, 18 Nov 2025 02:23:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e77346f90948edf43f33edec1b3c918cc8196b58e71fc74d47eb901d26a7c88`  
		Last Modified: Tue, 18 Nov 2025 02:23:39 GMT  
		Size: 18.3 MB (18286955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab20fff4d4c2bb97e0fc743edd41339f9e7f2db5706f958f8419de0227c19fa9`  
		Last Modified: Tue, 18 Nov 2025 02:23:38 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3deede23e33150dccc8ce32f23f864d2a100697bb5c3f5f0d51414ec4913c97f`  
		Last Modified: Tue, 18 Nov 2025 02:23:38 GMT  
		Size: 4.7 MB (4709653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:92486d0301f23f7f5fef04e23a1038f9c9c424a3a47ade435591fdd52853f380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a1456fb2be5b0b7cdc491b833efa2a0ceb4796c5c761a82e6ef643577401e6`

```dockerfile
```

-	Layers:
	-	`sha256:6273392ed72e310ca2593fd6731c533c6f636ed1289f29f728e45fc25e8d45b3`  
		Last Modified: Tue, 18 Nov 2025 06:01:44 GMT  
		Size: 5.6 MB (5585926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c338421356fba9d226382ee2864822813fdd13c90654bd98562c53392aa9884f`  
		Last Modified: Tue, 18 Nov 2025 06:01:44 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v7

```console
$ docker pull irssi@sha256:6206945589cb5f70880eb627ea43ce5e83dc6b09e69ad976fc69ec0a8a671e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48681442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e2dfadf9b6f72f29f6e28ff5885e16008ea991da97c386c12c6effd41ef773`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:24:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:24:00 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:24:00 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:24:00 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:24:00 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:24:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:24:41 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:24:41 GMT
USER user
# Tue, 18 Nov 2025 02:24:41 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07012b32f4cdf9145076ab6689e96bf750c40d6358ddc6b3d983ed86522093b2`  
		Last Modified: Tue, 18 Nov 2025 02:25:00 GMT  
		Size: 17.9 MB (17909541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c317eec7c88d4aa0563b4acdfa018d18e2244d1cd4faaa808233aad6ed8c4eef`  
		Last Modified: Tue, 18 Nov 2025 02:24:57 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999e397c097f4a4f9d07fc0ad13a259eb1c5dc9952ad435619e84f81acd7aa5a`  
		Last Modified: Tue, 18 Nov 2025 02:24:57 GMT  
		Size: 4.6 MB (4558582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:2807406dbaf53bd4128387747c9380192177098c869b02c4fbc0e079734b4a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912225e9dca4300bbd0be1c71db46f637c20bb0ae39dd56905152d9fd37712e7`

```dockerfile
```

-	Layers:
	-	`sha256:826b1dd7affc3defc30e532bafe21b81af9274fe59f9cb13bc8880b266566410`  
		Last Modified: Tue, 18 Nov 2025 06:01:49 GMT  
		Size: 5.6 MB (5588948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caba9a457c37510c70d5629f0b91ebfec1b4e1fddabcf69e4581cc62b8efbdf9`  
		Last Modified: Tue, 18 Nov 2025 06:01:51 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:0ca154f240d8e55d9139562ed162f6d09ed917369e5d3ac0ef11f4277868a144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53972828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494da41086e91ed2e2a5b5a81ed84f81af0313ded1a6a19ca4935a9ed697e260`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:19:36 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:19:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:19:36 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:19:36 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:20:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:20:13 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:20:13 GMT
USER user
# Tue, 18 Nov 2025 02:20:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a619a9a2c5679b92c7e4905e08f05810e02f68d89d06b10524e21d2583f4ab16`  
		Last Modified: Tue, 18 Nov 2025 02:20:32 GMT  
		Size: 19.0 MB (19049113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494e61b822c7885405295c0e02e3d6f750e57594294fe2d8b997a0632065745d`  
		Last Modified: Tue, 18 Nov 2025 02:20:30 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84635b25a37fcbf6ec3700e051e040f70178ad0e6880c9c76aeef1ebcfdf275`  
		Last Modified: Tue, 18 Nov 2025 02:20:30 GMT  
		Size: 4.8 MB (4781743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:6b955f8723ba03a2a30061c1a89c6af489d1442317213524c5594663f9d28695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b845fa96792ab508c1cabce079cc6822b4d3ed51f4ff9cc1486fb4becdb2b9`

```dockerfile
```

-	Layers:
	-	`sha256:1e1288c631711328c43fbd795987044f9c19d6d7ca488586f7d48b2d1bbf9fc9`  
		Last Modified: Tue, 18 Nov 2025 06:01:56 GMT  
		Size: 5.6 MB (5594861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3627aff8962b25f0eb1a595d760c047d53573e5a83de81ffd5ee43ffde3e283f`  
		Last Modified: Tue, 18 Nov 2025 06:01:57 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; 386

```console
$ docker pull irssi@sha256:9ca8e0716038e4dbc489c402c36d6bdc49bb1c6dc80a6050371e0ebb63798b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afefadafe5f8e789fb22f477834b8855758beefa989deb19c7f4e79699e5e89`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:16:34 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:16:34 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:16:34 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:16:34 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:17:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:17:16 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:17:16 GMT
USER user
# Tue, 18 Nov 2025 02:17:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c2fb43e1b281a402bf774cd8bde6070d229add5d03c870cbfe7c8e16f2cbb7`  
		Last Modified: Tue, 18 Nov 2025 02:17:34 GMT  
		Size: 18.7 MB (18740862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6997edee7df4e50b70fa845f324ec76992912dec560143cbead27a7aec43803b`  
		Last Modified: Tue, 18 Nov 2025 02:17:33 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4a3e4cae20c6dc7e982f2a19aa8de8e2b641b6bcc81e72f1bef2930dca363d`  
		Last Modified: Tue, 18 Nov 2025 02:17:34 GMT  
		Size: 4.9 MB (4868298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:59d4050c0c1cd29128be910eccf5ea2a035052b836f46e045244c9f64fa4298c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1003b498f9e79e27d0402d3e70dfc68a8d4f2e5fb76327ddf0d269848f164933`

```dockerfile
```

-	Layers:
	-	`sha256:dae334eb70cbeb2210f0f00af9826de6e0af19a4045d45c351ccd063c967c44c`  
		Last Modified: Tue, 18 Nov 2025 06:02:04 GMT  
		Size: 5.6 MB (5584500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48f17fc2c6b6001ffa3a573775d2cbcfc57f6836267cf4f7578260842ada1b7`  
		Last Modified: Tue, 18 Nov 2025 06:02:05 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; ppc64le

```console
$ docker pull irssi@sha256:459fe708abbb929ace6e5502ac492cb132f84c0e1b80e5a3dd662a7d98b6470e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58240238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72533238806364f21d117ef1051d9f72e86e6063d9c6683bc210cea47127bda`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:03:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 15:03:14 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 15:03:14 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 15:03:14 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 15:03:14 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 15:04:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 15:04:50 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 15:04:50 GMT
USER user
# Tue, 18 Nov 2025 15:04:50 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f858dd24ce7b2766334f11cb720c162ec10dcc1115c24b7c5a2cb933f4732e`  
		Last Modified: Tue, 18 Nov 2025 15:05:24 GMT  
		Size: 19.5 MB (19542803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7e87e68a0f54b41f554a220560c01fae4bca1b4bb4b83336d6c6110f750186`  
		Last Modified: Tue, 18 Nov 2025 15:05:23 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab575b18effe508097b5d8936201a72cd903f95c5c055af70a652fee9591f15f`  
		Last Modified: Tue, 18 Nov 2025 15:05:23 GMT  
		Size: 5.1 MB (5097211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:43823b3c76d194b48bf19fd79dde879a47f65352dc638bc93f743de8b5863b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b0fd9dbba87f1d0495d3f376c23a11766edc9e180c9c6afddfacb7df1cbe76`

```dockerfile
```

-	Layers:
	-	`sha256:ebbbdb938672f1b98a9abf9c0267764349f2261c7295ea777971571c28ac293f`  
		Last Modified: Tue, 18 Nov 2025 18:00:17 GMT  
		Size: 5.6 MB (5595408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ae083b6d0624ff996d976b7dfead8f215b20de9aedc3bef84697341f367a4d3`  
		Last Modified: Tue, 18 Nov 2025 18:00:18 GMT  
		Size: 18.7 KB (18723 bytes)  
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
$ docker pull irssi@sha256:da93e9283b14d1092e451a797eb231f916c62509d64042a7ed65617b6ab9c487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54503019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6b5c6cf33fd166afa65862c57464a7a99d44516a592d7093c9c71058d5008c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:17:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:58 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:17:58 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:17:58 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:17:58 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:18:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:18:33 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:18:33 GMT
USER user
# Tue, 18 Nov 2025 02:18:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bce4907214a18511e7c1676f0b93794fa538b6672045daa187e1c681bbd9019`  
		Last Modified: Tue, 18 Nov 2025 02:18:55 GMT  
		Size: 19.8 MB (19759415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dca431fe704652eca13f122842a6232de3a88619e75b4585c55d73ab6784b33`  
		Last Modified: Tue, 18 Nov 2025 02:18:52 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12fa892c886e7110c8b36d26e5b06c87bdfad4dab6e9bf9b746c2887bce206f`  
		Last Modified: Tue, 18 Nov 2025 02:18:53 GMT  
		Size: 4.9 MB (4905870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:9921bed642cdddc5b883e960fbb4efa54a43817af46e8c05c8c59611062a6056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babbc467c5248e09f8d3d0710512a06a92fbd5173a81414b551f82cab3d5d0d3`

```dockerfile
```

-	Layers:
	-	`sha256:a1fee033f27a53ca8a99d5789a2cf1a16782bef7f265384856e2f9c62104fc55`  
		Last Modified: Tue, 18 Nov 2025 06:02:18 GMT  
		Size: 5.6 MB (5589282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd54ab02d147f06764006021d0881cd166981d03206bbcbfdca3215249d036e1`  
		Last Modified: Tue, 18 Nov 2025 06:02:19 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine`

```console
$ docker pull irssi@sha256:a9f4d6de38d69a4ba0ab97a6f43836134df1ffd4290e4a244596c34b80554604
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
$ docker pull irssi@sha256:af936cabadda0c93ca3a229f630f7a5f4888f182b0cbb68edba78dbfaf1dd897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19342220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6546997bb677e945cd6914f29dcdd5d93b42fce0ffcc5b7109c0829285bcea25`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90056e842713293c53c6dce4290bfbd298df758358806bd5d3bec46230a89716`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 9.8 MB (9840947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c83cc5e93d426e4646d9cce9fdd7a659215fc178d82320a85f6c6e13ce0939`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1486e128aa6ab32a4665c7cdcb3ed936f18c1e8bf06a7a4d7414222f0a89ac9`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 6.0 MB (5985049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:7bdbcb1c990676d35120b16117a0adacceb673203918e2e310ce5e5bb9f8ef01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1819ad33d43cee11f7584b364a2e91ced1b9b8229dea8fc4e7bf7cad969bfe7`

```dockerfile
```

-	Layers:
	-	`sha256:0191fc70832b0a543dfdac6c4787f835b7dd8fd57d9e0b7c1a864173c00c5b5a`  
		Last Modified: Thu, 09 Oct 2025 07:59:31 GMT  
		Size: 1.3 MB (1268771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:101fedb5dfade0a1d32aed1260a2c4e061defe2886d8bccdd1cabcc4f65ab848`  
		Last Modified: Thu, 09 Oct 2025 07:59:32 GMT  
		Size: 17.6 KB (17611 bytes)  
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
$ docker pull irssi@sha256:3628d0d0b7185364f7bfc20971afa71df0c98f15e734b4f7199ce9339663e4ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
$ docker pull irssi@sha256:f16b9ab6967270a5b2d0745b7f6b9233f6226b9866de8e46ab3f67f20167dde3
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
$ docker pull irssi@sha256:1c3ad0c692729985069dc605f6970c498536ff77cdc28731957a9981bb5cc69d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53869276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d8b5071dd14f9cc7babdbbb92be355488770afbb4baa1dd4193f835544e54d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:18:09 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 04:18:09 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 04:18:09 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:18:09 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 04:18:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 04:18:46 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 04:18:46 GMT
USER user
# Tue, 18 Nov 2025 04:18:46 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3defe69b9d42ee331ee4997997e0b6950a228ac42a28acb744b2a217802984`  
		Last Modified: Tue, 18 Nov 2025 04:19:08 GMT  
		Size: 19.2 MB (19222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d261d2d2be0daf5812e199043e646cd3b38c72c6a85a46d1aa2664afbbfdab`  
		Last Modified: Tue, 18 Nov 2025 04:19:07 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fb0ce4ebcc67d4eb7b0fd5a6f142adedb46b4a4b5c9f752bb3663092160fd4`  
		Last Modified: Tue, 18 Nov 2025 04:19:07 GMT  
		Size: 4.9 MB (4866605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:22bdb7c49ddfaba85497f04c9d268938716f3b3352fe24378d933a7732e8d145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d4070dfa4342b3ae917c1f765452b8b31cbfe6c04864d806db24d761ba3c65`

```dockerfile
```

-	Layers:
	-	`sha256:5234daf2a71968c25322c71bfea4cdc75082624fc15fcfa85f68596c0e1e8722`  
		Last Modified: Tue, 18 Nov 2025 06:01:31 GMT  
		Size: 5.6 MB (5588377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef6a5104b772e5ddb76df8ed09e14d2aaf8f4757fd03c65a00ce68904337b081`  
		Last Modified: Tue, 18 Nov 2025 06:01:32 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:3bfeabfea3f173a6eef66224244f7c8ab79162e4b3e3454b5d7b951b699e6d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50944118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce561de65d9ced729b270243f33a9fe650e7088512ea128954c48a408518f61`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:22:31 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:22:31 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:22:31 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:22:31 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:23:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:23:21 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:23:21 GMT
USER user
# Tue, 18 Nov 2025 02:23:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e77346f90948edf43f33edec1b3c918cc8196b58e71fc74d47eb901d26a7c88`  
		Last Modified: Tue, 18 Nov 2025 02:23:39 GMT  
		Size: 18.3 MB (18286955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab20fff4d4c2bb97e0fc743edd41339f9e7f2db5706f958f8419de0227c19fa9`  
		Last Modified: Tue, 18 Nov 2025 02:23:38 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3deede23e33150dccc8ce32f23f864d2a100697bb5c3f5f0d51414ec4913c97f`  
		Last Modified: Tue, 18 Nov 2025 02:23:38 GMT  
		Size: 4.7 MB (4709653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:92486d0301f23f7f5fef04e23a1038f9c9c424a3a47ade435591fdd52853f380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a1456fb2be5b0b7cdc491b833efa2a0ceb4796c5c761a82e6ef643577401e6`

```dockerfile
```

-	Layers:
	-	`sha256:6273392ed72e310ca2593fd6731c533c6f636ed1289f29f728e45fc25e8d45b3`  
		Last Modified: Tue, 18 Nov 2025 06:01:44 GMT  
		Size: 5.6 MB (5585926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c338421356fba9d226382ee2864822813fdd13c90654bd98562c53392aa9884f`  
		Last Modified: Tue, 18 Nov 2025 06:01:44 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:6206945589cb5f70880eb627ea43ce5e83dc6b09e69ad976fc69ec0a8a671e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48681442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e2dfadf9b6f72f29f6e28ff5885e16008ea991da97c386c12c6effd41ef773`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:24:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:24:00 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:24:00 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:24:00 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:24:00 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:24:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:24:41 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:24:41 GMT
USER user
# Tue, 18 Nov 2025 02:24:41 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07012b32f4cdf9145076ab6689e96bf750c40d6358ddc6b3d983ed86522093b2`  
		Last Modified: Tue, 18 Nov 2025 02:25:00 GMT  
		Size: 17.9 MB (17909541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c317eec7c88d4aa0563b4acdfa018d18e2244d1cd4faaa808233aad6ed8c4eef`  
		Last Modified: Tue, 18 Nov 2025 02:24:57 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999e397c097f4a4f9d07fc0ad13a259eb1c5dc9952ad435619e84f81acd7aa5a`  
		Last Modified: Tue, 18 Nov 2025 02:24:57 GMT  
		Size: 4.6 MB (4558582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:2807406dbaf53bd4128387747c9380192177098c869b02c4fbc0e079734b4a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912225e9dca4300bbd0be1c71db46f637c20bb0ae39dd56905152d9fd37712e7`

```dockerfile
```

-	Layers:
	-	`sha256:826b1dd7affc3defc30e532bafe21b81af9274fe59f9cb13bc8880b266566410`  
		Last Modified: Tue, 18 Nov 2025 06:01:49 GMT  
		Size: 5.6 MB (5588948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caba9a457c37510c70d5629f0b91ebfec1b4e1fddabcf69e4581cc62b8efbdf9`  
		Last Modified: Tue, 18 Nov 2025 06:01:51 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:0ca154f240d8e55d9139562ed162f6d09ed917369e5d3ac0ef11f4277868a144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53972828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494da41086e91ed2e2a5b5a81ed84f81af0313ded1a6a19ca4935a9ed697e260`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:19:36 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:19:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:19:36 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:19:36 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:20:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:20:13 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:20:13 GMT
USER user
# Tue, 18 Nov 2025 02:20:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a619a9a2c5679b92c7e4905e08f05810e02f68d89d06b10524e21d2583f4ab16`  
		Last Modified: Tue, 18 Nov 2025 02:20:32 GMT  
		Size: 19.0 MB (19049113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494e61b822c7885405295c0e02e3d6f750e57594294fe2d8b997a0632065745d`  
		Last Modified: Tue, 18 Nov 2025 02:20:30 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84635b25a37fcbf6ec3700e051e040f70178ad0e6880c9c76aeef1ebcfdf275`  
		Last Modified: Tue, 18 Nov 2025 02:20:30 GMT  
		Size: 4.8 MB (4781743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:6b955f8723ba03a2a30061c1a89c6af489d1442317213524c5594663f9d28695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b845fa96792ab508c1cabce079cc6822b4d3ed51f4ff9cc1486fb4becdb2b9`

```dockerfile
```

-	Layers:
	-	`sha256:1e1288c631711328c43fbd795987044f9c19d6d7ca488586f7d48b2d1bbf9fc9`  
		Last Modified: Tue, 18 Nov 2025 06:01:56 GMT  
		Size: 5.6 MB (5594861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3627aff8962b25f0eb1a595d760c047d53573e5a83de81ffd5ee43ffde3e283f`  
		Last Modified: Tue, 18 Nov 2025 06:01:57 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; 386

```console
$ docker pull irssi@sha256:9ca8e0716038e4dbc489c402c36d6bdc49bb1c6dc80a6050371e0ebb63798b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afefadafe5f8e789fb22f477834b8855758beefa989deb19c7f4e79699e5e89`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:16:34 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:16:34 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:16:34 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:16:34 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:17:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:17:16 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:17:16 GMT
USER user
# Tue, 18 Nov 2025 02:17:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c2fb43e1b281a402bf774cd8bde6070d229add5d03c870cbfe7c8e16f2cbb7`  
		Last Modified: Tue, 18 Nov 2025 02:17:34 GMT  
		Size: 18.7 MB (18740862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6997edee7df4e50b70fa845f324ec76992912dec560143cbead27a7aec43803b`  
		Last Modified: Tue, 18 Nov 2025 02:17:33 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4a3e4cae20c6dc7e982f2a19aa8de8e2b641b6bcc81e72f1bef2930dca363d`  
		Last Modified: Tue, 18 Nov 2025 02:17:34 GMT  
		Size: 4.9 MB (4868298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:59d4050c0c1cd29128be910eccf5ea2a035052b836f46e045244c9f64fa4298c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1003b498f9e79e27d0402d3e70dfc68a8d4f2e5fb76327ddf0d269848f164933`

```dockerfile
```

-	Layers:
	-	`sha256:dae334eb70cbeb2210f0f00af9826de6e0af19a4045d45c351ccd063c967c44c`  
		Last Modified: Tue, 18 Nov 2025 06:02:04 GMT  
		Size: 5.6 MB (5584500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48f17fc2c6b6001ffa3a573775d2cbcfc57f6836267cf4f7578260842ada1b7`  
		Last Modified: Tue, 18 Nov 2025 06:02:05 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:459fe708abbb929ace6e5502ac492cb132f84c0e1b80e5a3dd662a7d98b6470e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58240238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72533238806364f21d117ef1051d9f72e86e6063d9c6683bc210cea47127bda`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:03:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 15:03:14 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 15:03:14 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 15:03:14 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 15:03:14 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 15:04:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 15:04:50 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 15:04:50 GMT
USER user
# Tue, 18 Nov 2025 15:04:50 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f858dd24ce7b2766334f11cb720c162ec10dcc1115c24b7c5a2cb933f4732e`  
		Last Modified: Tue, 18 Nov 2025 15:05:24 GMT  
		Size: 19.5 MB (19542803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7e87e68a0f54b41f554a220560c01fae4bca1b4bb4b83336d6c6110f750186`  
		Last Modified: Tue, 18 Nov 2025 15:05:23 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab575b18effe508097b5d8936201a72cd903f95c5c055af70a652fee9591f15f`  
		Last Modified: Tue, 18 Nov 2025 15:05:23 GMT  
		Size: 5.1 MB (5097211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:43823b3c76d194b48bf19fd79dde879a47f65352dc638bc93f743de8b5863b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b0fd9dbba87f1d0495d3f376c23a11766edc9e180c9c6afddfacb7df1cbe76`

```dockerfile
```

-	Layers:
	-	`sha256:ebbbdb938672f1b98a9abf9c0267764349f2261c7295ea777971571c28ac293f`  
		Last Modified: Tue, 18 Nov 2025 18:00:17 GMT  
		Size: 5.6 MB (5595408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ae083b6d0624ff996d976b7dfead8f215b20de9aedc3bef84697341f367a4d3`  
		Last Modified: Tue, 18 Nov 2025 18:00:18 GMT  
		Size: 18.7 KB (18723 bytes)  
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
$ docker pull irssi@sha256:da93e9283b14d1092e451a797eb231f916c62509d64042a7ed65617b6ab9c487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54503019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6b5c6cf33fd166afa65862c57464a7a99d44516a592d7093c9c71058d5008c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:17:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:58 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:17:58 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:17:58 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:17:58 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:18:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:18:33 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:18:33 GMT
USER user
# Tue, 18 Nov 2025 02:18:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bce4907214a18511e7c1676f0b93794fa538b6672045daa187e1c681bbd9019`  
		Last Modified: Tue, 18 Nov 2025 02:18:55 GMT  
		Size: 19.8 MB (19759415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dca431fe704652eca13f122842a6232de3a88619e75b4585c55d73ab6784b33`  
		Last Modified: Tue, 18 Nov 2025 02:18:52 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12fa892c886e7110c8b36d26e5b06c87bdfad4dab6e9bf9b746c2887bce206f`  
		Last Modified: Tue, 18 Nov 2025 02:18:53 GMT  
		Size: 4.9 MB (4905870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:9921bed642cdddc5b883e960fbb4efa54a43817af46e8c05c8c59611062a6056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babbc467c5248e09f8d3d0710512a06a92fbd5173a81414b551f82cab3d5d0d3`

```dockerfile
```

-	Layers:
	-	`sha256:a1fee033f27a53ca8a99d5789a2cf1a16782bef7f265384856e2f9c62104fc55`  
		Last Modified: Tue, 18 Nov 2025 06:02:18 GMT  
		Size: 5.6 MB (5589282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd54ab02d147f06764006021d0881cd166981d03206bbcbfdca3215249d036e1`  
		Last Modified: Tue, 18 Nov 2025 06:02:19 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4`

```console
$ docker pull irssi@sha256:f16b9ab6967270a5b2d0745b7f6b9233f6226b9866de8e46ab3f67f20167dde3
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
$ docker pull irssi@sha256:1c3ad0c692729985069dc605f6970c498536ff77cdc28731957a9981bb5cc69d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53869276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d8b5071dd14f9cc7babdbbb92be355488770afbb4baa1dd4193f835544e54d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:18:09 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 04:18:09 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 04:18:09 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:18:09 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 04:18:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 04:18:46 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 04:18:46 GMT
USER user
# Tue, 18 Nov 2025 04:18:46 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3defe69b9d42ee331ee4997997e0b6950a228ac42a28acb744b2a217802984`  
		Last Modified: Tue, 18 Nov 2025 04:19:08 GMT  
		Size: 19.2 MB (19222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d261d2d2be0daf5812e199043e646cd3b38c72c6a85a46d1aa2664afbbfdab`  
		Last Modified: Tue, 18 Nov 2025 04:19:07 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fb0ce4ebcc67d4eb7b0fd5a6f142adedb46b4a4b5c9f752bb3663092160fd4`  
		Last Modified: Tue, 18 Nov 2025 04:19:07 GMT  
		Size: 4.9 MB (4866605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:22bdb7c49ddfaba85497f04c9d268938716f3b3352fe24378d933a7732e8d145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d4070dfa4342b3ae917c1f765452b8b31cbfe6c04864d806db24d761ba3c65`

```dockerfile
```

-	Layers:
	-	`sha256:5234daf2a71968c25322c71bfea4cdc75082624fc15fcfa85f68596c0e1e8722`  
		Last Modified: Tue, 18 Nov 2025 06:01:31 GMT  
		Size: 5.6 MB (5588377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef6a5104b772e5ddb76df8ed09e14d2aaf8f4757fd03c65a00ce68904337b081`  
		Last Modified: Tue, 18 Nov 2025 06:01:32 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v5

```console
$ docker pull irssi@sha256:3bfeabfea3f173a6eef66224244f7c8ab79162e4b3e3454b5d7b951b699e6d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50944118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce561de65d9ced729b270243f33a9fe650e7088512ea128954c48a408518f61`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:22:31 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:22:31 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:22:31 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:22:31 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:23:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:23:21 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:23:21 GMT
USER user
# Tue, 18 Nov 2025 02:23:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e77346f90948edf43f33edec1b3c918cc8196b58e71fc74d47eb901d26a7c88`  
		Last Modified: Tue, 18 Nov 2025 02:23:39 GMT  
		Size: 18.3 MB (18286955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab20fff4d4c2bb97e0fc743edd41339f9e7f2db5706f958f8419de0227c19fa9`  
		Last Modified: Tue, 18 Nov 2025 02:23:38 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3deede23e33150dccc8ce32f23f864d2a100697bb5c3f5f0d51414ec4913c97f`  
		Last Modified: Tue, 18 Nov 2025 02:23:38 GMT  
		Size: 4.7 MB (4709653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:92486d0301f23f7f5fef04e23a1038f9c9c424a3a47ade435591fdd52853f380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a1456fb2be5b0b7cdc491b833efa2a0ceb4796c5c761a82e6ef643577401e6`

```dockerfile
```

-	Layers:
	-	`sha256:6273392ed72e310ca2593fd6731c533c6f636ed1289f29f728e45fc25e8d45b3`  
		Last Modified: Tue, 18 Nov 2025 06:01:44 GMT  
		Size: 5.6 MB (5585926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c338421356fba9d226382ee2864822813fdd13c90654bd98562c53392aa9884f`  
		Last Modified: Tue, 18 Nov 2025 06:01:44 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v7

```console
$ docker pull irssi@sha256:6206945589cb5f70880eb627ea43ce5e83dc6b09e69ad976fc69ec0a8a671e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48681442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e2dfadf9b6f72f29f6e28ff5885e16008ea991da97c386c12c6effd41ef773`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:24:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:24:00 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:24:00 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:24:00 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:24:00 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:24:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:24:41 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:24:41 GMT
USER user
# Tue, 18 Nov 2025 02:24:41 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07012b32f4cdf9145076ab6689e96bf750c40d6358ddc6b3d983ed86522093b2`  
		Last Modified: Tue, 18 Nov 2025 02:25:00 GMT  
		Size: 17.9 MB (17909541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c317eec7c88d4aa0563b4acdfa018d18e2244d1cd4faaa808233aad6ed8c4eef`  
		Last Modified: Tue, 18 Nov 2025 02:24:57 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999e397c097f4a4f9d07fc0ad13a259eb1c5dc9952ad435619e84f81acd7aa5a`  
		Last Modified: Tue, 18 Nov 2025 02:24:57 GMT  
		Size: 4.6 MB (4558582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:2807406dbaf53bd4128387747c9380192177098c869b02c4fbc0e079734b4a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912225e9dca4300bbd0be1c71db46f637c20bb0ae39dd56905152d9fd37712e7`

```dockerfile
```

-	Layers:
	-	`sha256:826b1dd7affc3defc30e532bafe21b81af9274fe59f9cb13bc8880b266566410`  
		Last Modified: Tue, 18 Nov 2025 06:01:49 GMT  
		Size: 5.6 MB (5588948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caba9a457c37510c70d5629f0b91ebfec1b4e1fddabcf69e4581cc62b8efbdf9`  
		Last Modified: Tue, 18 Nov 2025 06:01:51 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:0ca154f240d8e55d9139562ed162f6d09ed917369e5d3ac0ef11f4277868a144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53972828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494da41086e91ed2e2a5b5a81ed84f81af0313ded1a6a19ca4935a9ed697e260`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:19:36 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:19:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:19:36 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:19:36 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:20:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:20:13 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:20:13 GMT
USER user
# Tue, 18 Nov 2025 02:20:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a619a9a2c5679b92c7e4905e08f05810e02f68d89d06b10524e21d2583f4ab16`  
		Last Modified: Tue, 18 Nov 2025 02:20:32 GMT  
		Size: 19.0 MB (19049113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494e61b822c7885405295c0e02e3d6f750e57594294fe2d8b997a0632065745d`  
		Last Modified: Tue, 18 Nov 2025 02:20:30 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84635b25a37fcbf6ec3700e051e040f70178ad0e6880c9c76aeef1ebcfdf275`  
		Last Modified: Tue, 18 Nov 2025 02:20:30 GMT  
		Size: 4.8 MB (4781743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:6b955f8723ba03a2a30061c1a89c6af489d1442317213524c5594663f9d28695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b845fa96792ab508c1cabce079cc6822b4d3ed51f4ff9cc1486fb4becdb2b9`

```dockerfile
```

-	Layers:
	-	`sha256:1e1288c631711328c43fbd795987044f9c19d6d7ca488586f7d48b2d1bbf9fc9`  
		Last Modified: Tue, 18 Nov 2025 06:01:56 GMT  
		Size: 5.6 MB (5594861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3627aff8962b25f0eb1a595d760c047d53573e5a83de81ffd5ee43ffde3e283f`  
		Last Modified: Tue, 18 Nov 2025 06:01:57 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; 386

```console
$ docker pull irssi@sha256:9ca8e0716038e4dbc489c402c36d6bdc49bb1c6dc80a6050371e0ebb63798b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afefadafe5f8e789fb22f477834b8855758beefa989deb19c7f4e79699e5e89`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:16:34 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:16:34 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:16:34 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:16:34 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:17:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:17:16 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:17:16 GMT
USER user
# Tue, 18 Nov 2025 02:17:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c2fb43e1b281a402bf774cd8bde6070d229add5d03c870cbfe7c8e16f2cbb7`  
		Last Modified: Tue, 18 Nov 2025 02:17:34 GMT  
		Size: 18.7 MB (18740862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6997edee7df4e50b70fa845f324ec76992912dec560143cbead27a7aec43803b`  
		Last Modified: Tue, 18 Nov 2025 02:17:33 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4a3e4cae20c6dc7e982f2a19aa8de8e2b641b6bcc81e72f1bef2930dca363d`  
		Last Modified: Tue, 18 Nov 2025 02:17:34 GMT  
		Size: 4.9 MB (4868298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:59d4050c0c1cd29128be910eccf5ea2a035052b836f46e045244c9f64fa4298c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1003b498f9e79e27d0402d3e70dfc68a8d4f2e5fb76327ddf0d269848f164933`

```dockerfile
```

-	Layers:
	-	`sha256:dae334eb70cbeb2210f0f00af9826de6e0af19a4045d45c351ccd063c967c44c`  
		Last Modified: Tue, 18 Nov 2025 06:02:04 GMT  
		Size: 5.6 MB (5584500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48f17fc2c6b6001ffa3a573775d2cbcfc57f6836267cf4f7578260842ada1b7`  
		Last Modified: Tue, 18 Nov 2025 06:02:05 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; ppc64le

```console
$ docker pull irssi@sha256:459fe708abbb929ace6e5502ac492cb132f84c0e1b80e5a3dd662a7d98b6470e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58240238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72533238806364f21d117ef1051d9f72e86e6063d9c6683bc210cea47127bda`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:03:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 15:03:14 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 15:03:14 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 15:03:14 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 15:03:14 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 15:04:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 15:04:50 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 15:04:50 GMT
USER user
# Tue, 18 Nov 2025 15:04:50 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f858dd24ce7b2766334f11cb720c162ec10dcc1115c24b7c5a2cb933f4732e`  
		Last Modified: Tue, 18 Nov 2025 15:05:24 GMT  
		Size: 19.5 MB (19542803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7e87e68a0f54b41f554a220560c01fae4bca1b4bb4b83336d6c6110f750186`  
		Last Modified: Tue, 18 Nov 2025 15:05:23 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab575b18effe508097b5d8936201a72cd903f95c5c055af70a652fee9591f15f`  
		Last Modified: Tue, 18 Nov 2025 15:05:23 GMT  
		Size: 5.1 MB (5097211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:43823b3c76d194b48bf19fd79dde879a47f65352dc638bc93f743de8b5863b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b0fd9dbba87f1d0495d3f376c23a11766edc9e180c9c6afddfacb7df1cbe76`

```dockerfile
```

-	Layers:
	-	`sha256:ebbbdb938672f1b98a9abf9c0267764349f2261c7295ea777971571c28ac293f`  
		Last Modified: Tue, 18 Nov 2025 18:00:17 GMT  
		Size: 5.6 MB (5595408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ae083b6d0624ff996d976b7dfead8f215b20de9aedc3bef84697341f367a4d3`  
		Last Modified: Tue, 18 Nov 2025 18:00:18 GMT  
		Size: 18.7 KB (18723 bytes)  
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
$ docker pull irssi@sha256:da93e9283b14d1092e451a797eb231f916c62509d64042a7ed65617b6ab9c487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54503019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6b5c6cf33fd166afa65862c57464a7a99d44516a592d7093c9c71058d5008c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:17:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:58 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:17:58 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:17:58 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:17:58 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:18:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:18:33 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:18:33 GMT
USER user
# Tue, 18 Nov 2025 02:18:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bce4907214a18511e7c1676f0b93794fa538b6672045daa187e1c681bbd9019`  
		Last Modified: Tue, 18 Nov 2025 02:18:55 GMT  
		Size: 19.8 MB (19759415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dca431fe704652eca13f122842a6232de3a88619e75b4585c55d73ab6784b33`  
		Last Modified: Tue, 18 Nov 2025 02:18:52 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12fa892c886e7110c8b36d26e5b06c87bdfad4dab6e9bf9b746c2887bce206f`  
		Last Modified: Tue, 18 Nov 2025 02:18:53 GMT  
		Size: 4.9 MB (4905870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:9921bed642cdddc5b883e960fbb4efa54a43817af46e8c05c8c59611062a6056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babbc467c5248e09f8d3d0710512a06a92fbd5173a81414b551f82cab3d5d0d3`

```dockerfile
```

-	Layers:
	-	`sha256:a1fee033f27a53ca8a99d5789a2cf1a16782bef7f265384856e2f9c62104fc55`  
		Last Modified: Tue, 18 Nov 2025 06:02:18 GMT  
		Size: 5.6 MB (5589282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd54ab02d147f06764006021d0881cd166981d03206bbcbfdca3215249d036e1`  
		Last Modified: Tue, 18 Nov 2025 06:02:19 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine`

```console
$ docker pull irssi@sha256:a9f4d6de38d69a4ba0ab97a6f43836134df1ffd4290e4a244596c34b80554604
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
$ docker pull irssi@sha256:af936cabadda0c93ca3a229f630f7a5f4888f182b0cbb68edba78dbfaf1dd897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19342220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6546997bb677e945cd6914f29dcdd5d93b42fce0ffcc5b7109c0829285bcea25`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90056e842713293c53c6dce4290bfbd298df758358806bd5d3bec46230a89716`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 9.8 MB (9840947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c83cc5e93d426e4646d9cce9fdd7a659215fc178d82320a85f6c6e13ce0939`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1486e128aa6ab32a4665c7cdcb3ed936f18c1e8bf06a7a4d7414222f0a89ac9`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 6.0 MB (5985049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:7bdbcb1c990676d35120b16117a0adacceb673203918e2e310ce5e5bb9f8ef01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1819ad33d43cee11f7584b364a2e91ced1b9b8229dea8fc4e7bf7cad969bfe7`

```dockerfile
```

-	Layers:
	-	`sha256:0191fc70832b0a543dfdac6c4787f835b7dd8fd57d9e0b7c1a864173c00c5b5a`  
		Last Modified: Thu, 09 Oct 2025 07:59:31 GMT  
		Size: 1.3 MB (1268771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:101fedb5dfade0a1d32aed1260a2c4e061defe2886d8bccdd1cabcc4f65ab848`  
		Last Modified: Thu, 09 Oct 2025 07:59:32 GMT  
		Size: 17.6 KB (17611 bytes)  
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
$ docker pull irssi@sha256:3628d0d0b7185364f7bfc20971afa71df0c98f15e734b4f7199ce9339663e4ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
$ docker pull irssi@sha256:f16b9ab6967270a5b2d0745b7f6b9233f6226b9866de8e46ab3f67f20167dde3
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
$ docker pull irssi@sha256:1c3ad0c692729985069dc605f6970c498536ff77cdc28731957a9981bb5cc69d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53869276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d8b5071dd14f9cc7babdbbb92be355488770afbb4baa1dd4193f835544e54d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:18:09 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 04:18:09 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 04:18:09 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:18:09 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 04:18:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 04:18:46 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 04:18:46 GMT
USER user
# Tue, 18 Nov 2025 04:18:46 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3defe69b9d42ee331ee4997997e0b6950a228ac42a28acb744b2a217802984`  
		Last Modified: Tue, 18 Nov 2025 04:19:08 GMT  
		Size: 19.2 MB (19222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d261d2d2be0daf5812e199043e646cd3b38c72c6a85a46d1aa2664afbbfdab`  
		Last Modified: Tue, 18 Nov 2025 04:19:07 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fb0ce4ebcc67d4eb7b0fd5a6f142adedb46b4a4b5c9f752bb3663092160fd4`  
		Last Modified: Tue, 18 Nov 2025 04:19:07 GMT  
		Size: 4.9 MB (4866605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:22bdb7c49ddfaba85497f04c9d268938716f3b3352fe24378d933a7732e8d145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d4070dfa4342b3ae917c1f765452b8b31cbfe6c04864d806db24d761ba3c65`

```dockerfile
```

-	Layers:
	-	`sha256:5234daf2a71968c25322c71bfea4cdc75082624fc15fcfa85f68596c0e1e8722`  
		Last Modified: Tue, 18 Nov 2025 06:01:31 GMT  
		Size: 5.6 MB (5588377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef6a5104b772e5ddb76df8ed09e14d2aaf8f4757fd03c65a00ce68904337b081`  
		Last Modified: Tue, 18 Nov 2025 06:01:32 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:3bfeabfea3f173a6eef66224244f7c8ab79162e4b3e3454b5d7b951b699e6d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50944118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce561de65d9ced729b270243f33a9fe650e7088512ea128954c48a408518f61`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:22:31 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:22:31 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:22:31 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:22:31 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:23:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:23:21 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:23:21 GMT
USER user
# Tue, 18 Nov 2025 02:23:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e77346f90948edf43f33edec1b3c918cc8196b58e71fc74d47eb901d26a7c88`  
		Last Modified: Tue, 18 Nov 2025 02:23:39 GMT  
		Size: 18.3 MB (18286955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab20fff4d4c2bb97e0fc743edd41339f9e7f2db5706f958f8419de0227c19fa9`  
		Last Modified: Tue, 18 Nov 2025 02:23:38 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3deede23e33150dccc8ce32f23f864d2a100697bb5c3f5f0d51414ec4913c97f`  
		Last Modified: Tue, 18 Nov 2025 02:23:38 GMT  
		Size: 4.7 MB (4709653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:92486d0301f23f7f5fef04e23a1038f9c9c424a3a47ade435591fdd52853f380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a1456fb2be5b0b7cdc491b833efa2a0ceb4796c5c761a82e6ef643577401e6`

```dockerfile
```

-	Layers:
	-	`sha256:6273392ed72e310ca2593fd6731c533c6f636ed1289f29f728e45fc25e8d45b3`  
		Last Modified: Tue, 18 Nov 2025 06:01:44 GMT  
		Size: 5.6 MB (5585926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c338421356fba9d226382ee2864822813fdd13c90654bd98562c53392aa9884f`  
		Last Modified: Tue, 18 Nov 2025 06:01:44 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:6206945589cb5f70880eb627ea43ce5e83dc6b09e69ad976fc69ec0a8a671e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48681442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e2dfadf9b6f72f29f6e28ff5885e16008ea991da97c386c12c6effd41ef773`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:24:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:24:00 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:24:00 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:24:00 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:24:00 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:24:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:24:41 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:24:41 GMT
USER user
# Tue, 18 Nov 2025 02:24:41 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07012b32f4cdf9145076ab6689e96bf750c40d6358ddc6b3d983ed86522093b2`  
		Last Modified: Tue, 18 Nov 2025 02:25:00 GMT  
		Size: 17.9 MB (17909541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c317eec7c88d4aa0563b4acdfa018d18e2244d1cd4faaa808233aad6ed8c4eef`  
		Last Modified: Tue, 18 Nov 2025 02:24:57 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999e397c097f4a4f9d07fc0ad13a259eb1c5dc9952ad435619e84f81acd7aa5a`  
		Last Modified: Tue, 18 Nov 2025 02:24:57 GMT  
		Size: 4.6 MB (4558582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:2807406dbaf53bd4128387747c9380192177098c869b02c4fbc0e079734b4a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912225e9dca4300bbd0be1c71db46f637c20bb0ae39dd56905152d9fd37712e7`

```dockerfile
```

-	Layers:
	-	`sha256:826b1dd7affc3defc30e532bafe21b81af9274fe59f9cb13bc8880b266566410`  
		Last Modified: Tue, 18 Nov 2025 06:01:49 GMT  
		Size: 5.6 MB (5588948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caba9a457c37510c70d5629f0b91ebfec1b4e1fddabcf69e4581cc62b8efbdf9`  
		Last Modified: Tue, 18 Nov 2025 06:01:51 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:0ca154f240d8e55d9139562ed162f6d09ed917369e5d3ac0ef11f4277868a144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53972828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494da41086e91ed2e2a5b5a81ed84f81af0313ded1a6a19ca4935a9ed697e260`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:19:36 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:19:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:19:36 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:19:36 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:20:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:20:13 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:20:13 GMT
USER user
# Tue, 18 Nov 2025 02:20:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a619a9a2c5679b92c7e4905e08f05810e02f68d89d06b10524e21d2583f4ab16`  
		Last Modified: Tue, 18 Nov 2025 02:20:32 GMT  
		Size: 19.0 MB (19049113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494e61b822c7885405295c0e02e3d6f750e57594294fe2d8b997a0632065745d`  
		Last Modified: Tue, 18 Nov 2025 02:20:30 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84635b25a37fcbf6ec3700e051e040f70178ad0e6880c9c76aeef1ebcfdf275`  
		Last Modified: Tue, 18 Nov 2025 02:20:30 GMT  
		Size: 4.8 MB (4781743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:6b955f8723ba03a2a30061c1a89c6af489d1442317213524c5594663f9d28695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b845fa96792ab508c1cabce079cc6822b4d3ed51f4ff9cc1486fb4becdb2b9`

```dockerfile
```

-	Layers:
	-	`sha256:1e1288c631711328c43fbd795987044f9c19d6d7ca488586f7d48b2d1bbf9fc9`  
		Last Modified: Tue, 18 Nov 2025 06:01:56 GMT  
		Size: 5.6 MB (5594861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3627aff8962b25f0eb1a595d760c047d53573e5a83de81ffd5ee43ffde3e283f`  
		Last Modified: Tue, 18 Nov 2025 06:01:57 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; 386

```console
$ docker pull irssi@sha256:9ca8e0716038e4dbc489c402c36d6bdc49bb1c6dc80a6050371e0ebb63798b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afefadafe5f8e789fb22f477834b8855758beefa989deb19c7f4e79699e5e89`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:16:34 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:16:34 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:16:34 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:16:34 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:17:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:17:16 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:17:16 GMT
USER user
# Tue, 18 Nov 2025 02:17:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c2fb43e1b281a402bf774cd8bde6070d229add5d03c870cbfe7c8e16f2cbb7`  
		Last Modified: Tue, 18 Nov 2025 02:17:34 GMT  
		Size: 18.7 MB (18740862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6997edee7df4e50b70fa845f324ec76992912dec560143cbead27a7aec43803b`  
		Last Modified: Tue, 18 Nov 2025 02:17:33 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4a3e4cae20c6dc7e982f2a19aa8de8e2b641b6bcc81e72f1bef2930dca363d`  
		Last Modified: Tue, 18 Nov 2025 02:17:34 GMT  
		Size: 4.9 MB (4868298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:59d4050c0c1cd29128be910eccf5ea2a035052b836f46e045244c9f64fa4298c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1003b498f9e79e27d0402d3e70dfc68a8d4f2e5fb76327ddf0d269848f164933`

```dockerfile
```

-	Layers:
	-	`sha256:dae334eb70cbeb2210f0f00af9826de6e0af19a4045d45c351ccd063c967c44c`  
		Last Modified: Tue, 18 Nov 2025 06:02:04 GMT  
		Size: 5.6 MB (5584500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48f17fc2c6b6001ffa3a573775d2cbcfc57f6836267cf4f7578260842ada1b7`  
		Last Modified: Tue, 18 Nov 2025 06:02:05 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:459fe708abbb929ace6e5502ac492cb132f84c0e1b80e5a3dd662a7d98b6470e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58240238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72533238806364f21d117ef1051d9f72e86e6063d9c6683bc210cea47127bda`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:03:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 15:03:14 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 15:03:14 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 15:03:14 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 15:03:14 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 15:04:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 15:04:50 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 15:04:50 GMT
USER user
# Tue, 18 Nov 2025 15:04:50 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f858dd24ce7b2766334f11cb720c162ec10dcc1115c24b7c5a2cb933f4732e`  
		Last Modified: Tue, 18 Nov 2025 15:05:24 GMT  
		Size: 19.5 MB (19542803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7e87e68a0f54b41f554a220560c01fae4bca1b4bb4b83336d6c6110f750186`  
		Last Modified: Tue, 18 Nov 2025 15:05:23 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab575b18effe508097b5d8936201a72cd903f95c5c055af70a652fee9591f15f`  
		Last Modified: Tue, 18 Nov 2025 15:05:23 GMT  
		Size: 5.1 MB (5097211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:43823b3c76d194b48bf19fd79dde879a47f65352dc638bc93f743de8b5863b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b0fd9dbba87f1d0495d3f376c23a11766edc9e180c9c6afddfacb7df1cbe76`

```dockerfile
```

-	Layers:
	-	`sha256:ebbbdb938672f1b98a9abf9c0267764349f2261c7295ea777971571c28ac293f`  
		Last Modified: Tue, 18 Nov 2025 18:00:17 GMT  
		Size: 5.6 MB (5595408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ae083b6d0624ff996d976b7dfead8f215b20de9aedc3bef84697341f367a4d3`  
		Last Modified: Tue, 18 Nov 2025 18:00:18 GMT  
		Size: 18.7 KB (18723 bytes)  
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
$ docker pull irssi@sha256:da93e9283b14d1092e451a797eb231f916c62509d64042a7ed65617b6ab9c487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54503019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6b5c6cf33fd166afa65862c57464a7a99d44516a592d7093c9c71058d5008c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:17:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:58 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:17:58 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:17:58 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:17:58 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:18:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:18:33 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:18:33 GMT
USER user
# Tue, 18 Nov 2025 02:18:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bce4907214a18511e7c1676f0b93794fa538b6672045daa187e1c681bbd9019`  
		Last Modified: Tue, 18 Nov 2025 02:18:55 GMT  
		Size: 19.8 MB (19759415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dca431fe704652eca13f122842a6232de3a88619e75b4585c55d73ab6784b33`  
		Last Modified: Tue, 18 Nov 2025 02:18:52 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12fa892c886e7110c8b36d26e5b06c87bdfad4dab6e9bf9b746c2887bce206f`  
		Last Modified: Tue, 18 Nov 2025 02:18:53 GMT  
		Size: 4.9 MB (4905870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:9921bed642cdddc5b883e960fbb4efa54a43817af46e8c05c8c59611062a6056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babbc467c5248e09f8d3d0710512a06a92fbd5173a81414b551f82cab3d5d0d3`

```dockerfile
```

-	Layers:
	-	`sha256:a1fee033f27a53ca8a99d5789a2cf1a16782bef7f265384856e2f9c62104fc55`  
		Last Modified: Tue, 18 Nov 2025 06:02:18 GMT  
		Size: 5.6 MB (5589282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd54ab02d147f06764006021d0881cd166981d03206bbcbfdca3215249d036e1`  
		Last Modified: Tue, 18 Nov 2025 06:02:19 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5`

```console
$ docker pull irssi@sha256:f16b9ab6967270a5b2d0745b7f6b9233f6226b9866de8e46ab3f67f20167dde3
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
$ docker pull irssi@sha256:1c3ad0c692729985069dc605f6970c498536ff77cdc28731957a9981bb5cc69d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53869276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d8b5071dd14f9cc7babdbbb92be355488770afbb4baa1dd4193f835544e54d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:18:09 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 04:18:09 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 04:18:09 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:18:09 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 04:18:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 04:18:46 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 04:18:46 GMT
USER user
# Tue, 18 Nov 2025 04:18:46 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3defe69b9d42ee331ee4997997e0b6950a228ac42a28acb744b2a217802984`  
		Last Modified: Tue, 18 Nov 2025 04:19:08 GMT  
		Size: 19.2 MB (19222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d261d2d2be0daf5812e199043e646cd3b38c72c6a85a46d1aa2664afbbfdab`  
		Last Modified: Tue, 18 Nov 2025 04:19:07 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fb0ce4ebcc67d4eb7b0fd5a6f142adedb46b4a4b5c9f752bb3663092160fd4`  
		Last Modified: Tue, 18 Nov 2025 04:19:07 GMT  
		Size: 4.9 MB (4866605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:22bdb7c49ddfaba85497f04c9d268938716f3b3352fe24378d933a7732e8d145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d4070dfa4342b3ae917c1f765452b8b31cbfe6c04864d806db24d761ba3c65`

```dockerfile
```

-	Layers:
	-	`sha256:5234daf2a71968c25322c71bfea4cdc75082624fc15fcfa85f68596c0e1e8722`  
		Last Modified: Tue, 18 Nov 2025 06:01:31 GMT  
		Size: 5.6 MB (5588377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef6a5104b772e5ddb76df8ed09e14d2aaf8f4757fd03c65a00ce68904337b081`  
		Last Modified: Tue, 18 Nov 2025 06:01:32 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v5

```console
$ docker pull irssi@sha256:3bfeabfea3f173a6eef66224244f7c8ab79162e4b3e3454b5d7b951b699e6d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50944118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce561de65d9ced729b270243f33a9fe650e7088512ea128954c48a408518f61`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:22:31 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:22:31 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:22:31 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:22:31 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:23:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:23:21 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:23:21 GMT
USER user
# Tue, 18 Nov 2025 02:23:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e77346f90948edf43f33edec1b3c918cc8196b58e71fc74d47eb901d26a7c88`  
		Last Modified: Tue, 18 Nov 2025 02:23:39 GMT  
		Size: 18.3 MB (18286955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab20fff4d4c2bb97e0fc743edd41339f9e7f2db5706f958f8419de0227c19fa9`  
		Last Modified: Tue, 18 Nov 2025 02:23:38 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3deede23e33150dccc8ce32f23f864d2a100697bb5c3f5f0d51414ec4913c97f`  
		Last Modified: Tue, 18 Nov 2025 02:23:38 GMT  
		Size: 4.7 MB (4709653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:92486d0301f23f7f5fef04e23a1038f9c9c424a3a47ade435591fdd52853f380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a1456fb2be5b0b7cdc491b833efa2a0ceb4796c5c761a82e6ef643577401e6`

```dockerfile
```

-	Layers:
	-	`sha256:6273392ed72e310ca2593fd6731c533c6f636ed1289f29f728e45fc25e8d45b3`  
		Last Modified: Tue, 18 Nov 2025 06:01:44 GMT  
		Size: 5.6 MB (5585926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c338421356fba9d226382ee2864822813fdd13c90654bd98562c53392aa9884f`  
		Last Modified: Tue, 18 Nov 2025 06:01:44 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v7

```console
$ docker pull irssi@sha256:6206945589cb5f70880eb627ea43ce5e83dc6b09e69ad976fc69ec0a8a671e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48681442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e2dfadf9b6f72f29f6e28ff5885e16008ea991da97c386c12c6effd41ef773`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:24:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:24:00 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:24:00 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:24:00 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:24:00 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:24:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:24:41 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:24:41 GMT
USER user
# Tue, 18 Nov 2025 02:24:41 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07012b32f4cdf9145076ab6689e96bf750c40d6358ddc6b3d983ed86522093b2`  
		Last Modified: Tue, 18 Nov 2025 02:25:00 GMT  
		Size: 17.9 MB (17909541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c317eec7c88d4aa0563b4acdfa018d18e2244d1cd4faaa808233aad6ed8c4eef`  
		Last Modified: Tue, 18 Nov 2025 02:24:57 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999e397c097f4a4f9d07fc0ad13a259eb1c5dc9952ad435619e84f81acd7aa5a`  
		Last Modified: Tue, 18 Nov 2025 02:24:57 GMT  
		Size: 4.6 MB (4558582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:2807406dbaf53bd4128387747c9380192177098c869b02c4fbc0e079734b4a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912225e9dca4300bbd0be1c71db46f637c20bb0ae39dd56905152d9fd37712e7`

```dockerfile
```

-	Layers:
	-	`sha256:826b1dd7affc3defc30e532bafe21b81af9274fe59f9cb13bc8880b266566410`  
		Last Modified: Tue, 18 Nov 2025 06:01:49 GMT  
		Size: 5.6 MB (5588948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caba9a457c37510c70d5629f0b91ebfec1b4e1fddabcf69e4581cc62b8efbdf9`  
		Last Modified: Tue, 18 Nov 2025 06:01:51 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:0ca154f240d8e55d9139562ed162f6d09ed917369e5d3ac0ef11f4277868a144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53972828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494da41086e91ed2e2a5b5a81ed84f81af0313ded1a6a19ca4935a9ed697e260`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:19:36 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:19:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:19:36 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:19:36 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:20:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:20:13 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:20:13 GMT
USER user
# Tue, 18 Nov 2025 02:20:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a619a9a2c5679b92c7e4905e08f05810e02f68d89d06b10524e21d2583f4ab16`  
		Last Modified: Tue, 18 Nov 2025 02:20:32 GMT  
		Size: 19.0 MB (19049113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494e61b822c7885405295c0e02e3d6f750e57594294fe2d8b997a0632065745d`  
		Last Modified: Tue, 18 Nov 2025 02:20:30 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84635b25a37fcbf6ec3700e051e040f70178ad0e6880c9c76aeef1ebcfdf275`  
		Last Modified: Tue, 18 Nov 2025 02:20:30 GMT  
		Size: 4.8 MB (4781743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:6b955f8723ba03a2a30061c1a89c6af489d1442317213524c5594663f9d28695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b845fa96792ab508c1cabce079cc6822b4d3ed51f4ff9cc1486fb4becdb2b9`

```dockerfile
```

-	Layers:
	-	`sha256:1e1288c631711328c43fbd795987044f9c19d6d7ca488586f7d48b2d1bbf9fc9`  
		Last Modified: Tue, 18 Nov 2025 06:01:56 GMT  
		Size: 5.6 MB (5594861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3627aff8962b25f0eb1a595d760c047d53573e5a83de81ffd5ee43ffde3e283f`  
		Last Modified: Tue, 18 Nov 2025 06:01:57 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; 386

```console
$ docker pull irssi@sha256:9ca8e0716038e4dbc489c402c36d6bdc49bb1c6dc80a6050371e0ebb63798b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afefadafe5f8e789fb22f477834b8855758beefa989deb19c7f4e79699e5e89`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:16:34 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:16:34 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:16:34 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:16:34 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:17:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:17:16 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:17:16 GMT
USER user
# Tue, 18 Nov 2025 02:17:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c2fb43e1b281a402bf774cd8bde6070d229add5d03c870cbfe7c8e16f2cbb7`  
		Last Modified: Tue, 18 Nov 2025 02:17:34 GMT  
		Size: 18.7 MB (18740862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6997edee7df4e50b70fa845f324ec76992912dec560143cbead27a7aec43803b`  
		Last Modified: Tue, 18 Nov 2025 02:17:33 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4a3e4cae20c6dc7e982f2a19aa8de8e2b641b6bcc81e72f1bef2930dca363d`  
		Last Modified: Tue, 18 Nov 2025 02:17:34 GMT  
		Size: 4.9 MB (4868298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:59d4050c0c1cd29128be910eccf5ea2a035052b836f46e045244c9f64fa4298c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1003b498f9e79e27d0402d3e70dfc68a8d4f2e5fb76327ddf0d269848f164933`

```dockerfile
```

-	Layers:
	-	`sha256:dae334eb70cbeb2210f0f00af9826de6e0af19a4045d45c351ccd063c967c44c`  
		Last Modified: Tue, 18 Nov 2025 06:02:04 GMT  
		Size: 5.6 MB (5584500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48f17fc2c6b6001ffa3a573775d2cbcfc57f6836267cf4f7578260842ada1b7`  
		Last Modified: Tue, 18 Nov 2025 06:02:05 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; ppc64le

```console
$ docker pull irssi@sha256:459fe708abbb929ace6e5502ac492cb132f84c0e1b80e5a3dd662a7d98b6470e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58240238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72533238806364f21d117ef1051d9f72e86e6063d9c6683bc210cea47127bda`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:03:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 15:03:14 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 15:03:14 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 15:03:14 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 15:03:14 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 15:04:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 15:04:50 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 15:04:50 GMT
USER user
# Tue, 18 Nov 2025 15:04:50 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f858dd24ce7b2766334f11cb720c162ec10dcc1115c24b7c5a2cb933f4732e`  
		Last Modified: Tue, 18 Nov 2025 15:05:24 GMT  
		Size: 19.5 MB (19542803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7e87e68a0f54b41f554a220560c01fae4bca1b4bb4b83336d6c6110f750186`  
		Last Modified: Tue, 18 Nov 2025 15:05:23 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab575b18effe508097b5d8936201a72cd903f95c5c055af70a652fee9591f15f`  
		Last Modified: Tue, 18 Nov 2025 15:05:23 GMT  
		Size: 5.1 MB (5097211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:43823b3c76d194b48bf19fd79dde879a47f65352dc638bc93f743de8b5863b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b0fd9dbba87f1d0495d3f376c23a11766edc9e180c9c6afddfacb7df1cbe76`

```dockerfile
```

-	Layers:
	-	`sha256:ebbbdb938672f1b98a9abf9c0267764349f2261c7295ea777971571c28ac293f`  
		Last Modified: Tue, 18 Nov 2025 18:00:17 GMT  
		Size: 5.6 MB (5595408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ae083b6d0624ff996d976b7dfead8f215b20de9aedc3bef84697341f367a4d3`  
		Last Modified: Tue, 18 Nov 2025 18:00:18 GMT  
		Size: 18.7 KB (18723 bytes)  
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
$ docker pull irssi@sha256:da93e9283b14d1092e451a797eb231f916c62509d64042a7ed65617b6ab9c487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54503019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6b5c6cf33fd166afa65862c57464a7a99d44516a592d7093c9c71058d5008c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:17:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:58 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:17:58 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:17:58 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:17:58 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:18:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:18:33 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:18:33 GMT
USER user
# Tue, 18 Nov 2025 02:18:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bce4907214a18511e7c1676f0b93794fa538b6672045daa187e1c681bbd9019`  
		Last Modified: Tue, 18 Nov 2025 02:18:55 GMT  
		Size: 19.8 MB (19759415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dca431fe704652eca13f122842a6232de3a88619e75b4585c55d73ab6784b33`  
		Last Modified: Tue, 18 Nov 2025 02:18:52 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12fa892c886e7110c8b36d26e5b06c87bdfad4dab6e9bf9b746c2887bce206f`  
		Last Modified: Tue, 18 Nov 2025 02:18:53 GMT  
		Size: 4.9 MB (4905870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:9921bed642cdddc5b883e960fbb4efa54a43817af46e8c05c8c59611062a6056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babbc467c5248e09f8d3d0710512a06a92fbd5173a81414b551f82cab3d5d0d3`

```dockerfile
```

-	Layers:
	-	`sha256:a1fee033f27a53ca8a99d5789a2cf1a16782bef7f265384856e2f9c62104fc55`  
		Last Modified: Tue, 18 Nov 2025 06:02:18 GMT  
		Size: 5.6 MB (5589282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd54ab02d147f06764006021d0881cd166981d03206bbcbfdca3215249d036e1`  
		Last Modified: Tue, 18 Nov 2025 06:02:19 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine`

```console
$ docker pull irssi@sha256:a9f4d6de38d69a4ba0ab97a6f43836134df1ffd4290e4a244596c34b80554604
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
$ docker pull irssi@sha256:af936cabadda0c93ca3a229f630f7a5f4888f182b0cbb68edba78dbfaf1dd897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19342220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6546997bb677e945cd6914f29dcdd5d93b42fce0ffcc5b7109c0829285bcea25`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90056e842713293c53c6dce4290bfbd298df758358806bd5d3bec46230a89716`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 9.8 MB (9840947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c83cc5e93d426e4646d9cce9fdd7a659215fc178d82320a85f6c6e13ce0939`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1486e128aa6ab32a4665c7cdcb3ed936f18c1e8bf06a7a4d7414222f0a89ac9`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 6.0 MB (5985049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:7bdbcb1c990676d35120b16117a0adacceb673203918e2e310ce5e5bb9f8ef01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1819ad33d43cee11f7584b364a2e91ced1b9b8229dea8fc4e7bf7cad969bfe7`

```dockerfile
```

-	Layers:
	-	`sha256:0191fc70832b0a543dfdac6c4787f835b7dd8fd57d9e0b7c1a864173c00c5b5a`  
		Last Modified: Thu, 09 Oct 2025 07:59:31 GMT  
		Size: 1.3 MB (1268771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:101fedb5dfade0a1d32aed1260a2c4e061defe2886d8bccdd1cabcc4f65ab848`  
		Last Modified: Thu, 09 Oct 2025 07:59:32 GMT  
		Size: 17.6 KB (17611 bytes)  
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
$ docker pull irssi@sha256:3628d0d0b7185364f7bfc20971afa71df0c98f15e734b4f7199ce9339663e4ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
$ docker pull irssi@sha256:f16b9ab6967270a5b2d0745b7f6b9233f6226b9866de8e46ab3f67f20167dde3
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
$ docker pull irssi@sha256:1c3ad0c692729985069dc605f6970c498536ff77cdc28731957a9981bb5cc69d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53869276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d8b5071dd14f9cc7babdbbb92be355488770afbb4baa1dd4193f835544e54d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:18:09 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 04:18:09 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 04:18:09 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:18:09 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 04:18:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 04:18:46 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 04:18:46 GMT
USER user
# Tue, 18 Nov 2025 04:18:46 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3defe69b9d42ee331ee4997997e0b6950a228ac42a28acb744b2a217802984`  
		Last Modified: Tue, 18 Nov 2025 04:19:08 GMT  
		Size: 19.2 MB (19222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d261d2d2be0daf5812e199043e646cd3b38c72c6a85a46d1aa2664afbbfdab`  
		Last Modified: Tue, 18 Nov 2025 04:19:07 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fb0ce4ebcc67d4eb7b0fd5a6f142adedb46b4a4b5c9f752bb3663092160fd4`  
		Last Modified: Tue, 18 Nov 2025 04:19:07 GMT  
		Size: 4.9 MB (4866605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:22bdb7c49ddfaba85497f04c9d268938716f3b3352fe24378d933a7732e8d145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d4070dfa4342b3ae917c1f765452b8b31cbfe6c04864d806db24d761ba3c65`

```dockerfile
```

-	Layers:
	-	`sha256:5234daf2a71968c25322c71bfea4cdc75082624fc15fcfa85f68596c0e1e8722`  
		Last Modified: Tue, 18 Nov 2025 06:01:31 GMT  
		Size: 5.6 MB (5588377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef6a5104b772e5ddb76df8ed09e14d2aaf8f4757fd03c65a00ce68904337b081`  
		Last Modified: Tue, 18 Nov 2025 06:01:32 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:3bfeabfea3f173a6eef66224244f7c8ab79162e4b3e3454b5d7b951b699e6d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50944118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce561de65d9ced729b270243f33a9fe650e7088512ea128954c48a408518f61`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:22:31 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:22:31 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:22:31 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:22:31 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:23:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:23:21 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:23:21 GMT
USER user
# Tue, 18 Nov 2025 02:23:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e77346f90948edf43f33edec1b3c918cc8196b58e71fc74d47eb901d26a7c88`  
		Last Modified: Tue, 18 Nov 2025 02:23:39 GMT  
		Size: 18.3 MB (18286955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab20fff4d4c2bb97e0fc743edd41339f9e7f2db5706f958f8419de0227c19fa9`  
		Last Modified: Tue, 18 Nov 2025 02:23:38 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3deede23e33150dccc8ce32f23f864d2a100697bb5c3f5f0d51414ec4913c97f`  
		Last Modified: Tue, 18 Nov 2025 02:23:38 GMT  
		Size: 4.7 MB (4709653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:92486d0301f23f7f5fef04e23a1038f9c9c424a3a47ade435591fdd52853f380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a1456fb2be5b0b7cdc491b833efa2a0ceb4796c5c761a82e6ef643577401e6`

```dockerfile
```

-	Layers:
	-	`sha256:6273392ed72e310ca2593fd6731c533c6f636ed1289f29f728e45fc25e8d45b3`  
		Last Modified: Tue, 18 Nov 2025 06:01:44 GMT  
		Size: 5.6 MB (5585926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c338421356fba9d226382ee2864822813fdd13c90654bd98562c53392aa9884f`  
		Last Modified: Tue, 18 Nov 2025 06:01:44 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:6206945589cb5f70880eb627ea43ce5e83dc6b09e69ad976fc69ec0a8a671e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48681442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e2dfadf9b6f72f29f6e28ff5885e16008ea991da97c386c12c6effd41ef773`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:24:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:24:00 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:24:00 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:24:00 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:24:00 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:24:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:24:41 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:24:41 GMT
USER user
# Tue, 18 Nov 2025 02:24:41 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07012b32f4cdf9145076ab6689e96bf750c40d6358ddc6b3d983ed86522093b2`  
		Last Modified: Tue, 18 Nov 2025 02:25:00 GMT  
		Size: 17.9 MB (17909541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c317eec7c88d4aa0563b4acdfa018d18e2244d1cd4faaa808233aad6ed8c4eef`  
		Last Modified: Tue, 18 Nov 2025 02:24:57 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999e397c097f4a4f9d07fc0ad13a259eb1c5dc9952ad435619e84f81acd7aa5a`  
		Last Modified: Tue, 18 Nov 2025 02:24:57 GMT  
		Size: 4.6 MB (4558582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:2807406dbaf53bd4128387747c9380192177098c869b02c4fbc0e079734b4a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912225e9dca4300bbd0be1c71db46f637c20bb0ae39dd56905152d9fd37712e7`

```dockerfile
```

-	Layers:
	-	`sha256:826b1dd7affc3defc30e532bafe21b81af9274fe59f9cb13bc8880b266566410`  
		Last Modified: Tue, 18 Nov 2025 06:01:49 GMT  
		Size: 5.6 MB (5588948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caba9a457c37510c70d5629f0b91ebfec1b4e1fddabcf69e4581cc62b8efbdf9`  
		Last Modified: Tue, 18 Nov 2025 06:01:51 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:0ca154f240d8e55d9139562ed162f6d09ed917369e5d3ac0ef11f4277868a144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53972828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494da41086e91ed2e2a5b5a81ed84f81af0313ded1a6a19ca4935a9ed697e260`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:19:36 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:19:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:19:36 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:19:36 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:20:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:20:13 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:20:13 GMT
USER user
# Tue, 18 Nov 2025 02:20:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a619a9a2c5679b92c7e4905e08f05810e02f68d89d06b10524e21d2583f4ab16`  
		Last Modified: Tue, 18 Nov 2025 02:20:32 GMT  
		Size: 19.0 MB (19049113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494e61b822c7885405295c0e02e3d6f750e57594294fe2d8b997a0632065745d`  
		Last Modified: Tue, 18 Nov 2025 02:20:30 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84635b25a37fcbf6ec3700e051e040f70178ad0e6880c9c76aeef1ebcfdf275`  
		Last Modified: Tue, 18 Nov 2025 02:20:30 GMT  
		Size: 4.8 MB (4781743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:6b955f8723ba03a2a30061c1a89c6af489d1442317213524c5594663f9d28695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b845fa96792ab508c1cabce079cc6822b4d3ed51f4ff9cc1486fb4becdb2b9`

```dockerfile
```

-	Layers:
	-	`sha256:1e1288c631711328c43fbd795987044f9c19d6d7ca488586f7d48b2d1bbf9fc9`  
		Last Modified: Tue, 18 Nov 2025 06:01:56 GMT  
		Size: 5.6 MB (5594861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3627aff8962b25f0eb1a595d760c047d53573e5a83de81ffd5ee43ffde3e283f`  
		Last Modified: Tue, 18 Nov 2025 06:01:57 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; 386

```console
$ docker pull irssi@sha256:9ca8e0716038e4dbc489c402c36d6bdc49bb1c6dc80a6050371e0ebb63798b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afefadafe5f8e789fb22f477834b8855758beefa989deb19c7f4e79699e5e89`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:16:34 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:16:34 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:16:34 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:16:34 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:17:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:17:16 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:17:16 GMT
USER user
# Tue, 18 Nov 2025 02:17:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c2fb43e1b281a402bf774cd8bde6070d229add5d03c870cbfe7c8e16f2cbb7`  
		Last Modified: Tue, 18 Nov 2025 02:17:34 GMT  
		Size: 18.7 MB (18740862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6997edee7df4e50b70fa845f324ec76992912dec560143cbead27a7aec43803b`  
		Last Modified: Tue, 18 Nov 2025 02:17:33 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4a3e4cae20c6dc7e982f2a19aa8de8e2b641b6bcc81e72f1bef2930dca363d`  
		Last Modified: Tue, 18 Nov 2025 02:17:34 GMT  
		Size: 4.9 MB (4868298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:59d4050c0c1cd29128be910eccf5ea2a035052b836f46e045244c9f64fa4298c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1003b498f9e79e27d0402d3e70dfc68a8d4f2e5fb76327ddf0d269848f164933`

```dockerfile
```

-	Layers:
	-	`sha256:dae334eb70cbeb2210f0f00af9826de6e0af19a4045d45c351ccd063c967c44c`  
		Last Modified: Tue, 18 Nov 2025 06:02:04 GMT  
		Size: 5.6 MB (5584500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48f17fc2c6b6001ffa3a573775d2cbcfc57f6836267cf4f7578260842ada1b7`  
		Last Modified: Tue, 18 Nov 2025 06:02:05 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:459fe708abbb929ace6e5502ac492cb132f84c0e1b80e5a3dd662a7d98b6470e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58240238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72533238806364f21d117ef1051d9f72e86e6063d9c6683bc210cea47127bda`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:03:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 15:03:14 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 15:03:14 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 15:03:14 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 15:03:14 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 15:04:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 15:04:50 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 15:04:50 GMT
USER user
# Tue, 18 Nov 2025 15:04:50 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f858dd24ce7b2766334f11cb720c162ec10dcc1115c24b7c5a2cb933f4732e`  
		Last Modified: Tue, 18 Nov 2025 15:05:24 GMT  
		Size: 19.5 MB (19542803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7e87e68a0f54b41f554a220560c01fae4bca1b4bb4b83336d6c6110f750186`  
		Last Modified: Tue, 18 Nov 2025 15:05:23 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab575b18effe508097b5d8936201a72cd903f95c5c055af70a652fee9591f15f`  
		Last Modified: Tue, 18 Nov 2025 15:05:23 GMT  
		Size: 5.1 MB (5097211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:43823b3c76d194b48bf19fd79dde879a47f65352dc638bc93f743de8b5863b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b0fd9dbba87f1d0495d3f376c23a11766edc9e180c9c6afddfacb7df1cbe76`

```dockerfile
```

-	Layers:
	-	`sha256:ebbbdb938672f1b98a9abf9c0267764349f2261c7295ea777971571c28ac293f`  
		Last Modified: Tue, 18 Nov 2025 18:00:17 GMT  
		Size: 5.6 MB (5595408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ae083b6d0624ff996d976b7dfead8f215b20de9aedc3bef84697341f367a4d3`  
		Last Modified: Tue, 18 Nov 2025 18:00:18 GMT  
		Size: 18.7 KB (18723 bytes)  
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
$ docker pull irssi@sha256:da93e9283b14d1092e451a797eb231f916c62509d64042a7ed65617b6ab9c487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54503019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6b5c6cf33fd166afa65862c57464a7a99d44516a592d7093c9c71058d5008c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:17:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:58 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:17:58 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:17:58 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:17:58 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:18:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:18:33 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:18:33 GMT
USER user
# Tue, 18 Nov 2025 02:18:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bce4907214a18511e7c1676f0b93794fa538b6672045daa187e1c681bbd9019`  
		Last Modified: Tue, 18 Nov 2025 02:18:55 GMT  
		Size: 19.8 MB (19759415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dca431fe704652eca13f122842a6232de3a88619e75b4585c55d73ab6784b33`  
		Last Modified: Tue, 18 Nov 2025 02:18:52 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12fa892c886e7110c8b36d26e5b06c87bdfad4dab6e9bf9b746c2887bce206f`  
		Last Modified: Tue, 18 Nov 2025 02:18:53 GMT  
		Size: 4.9 MB (4905870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:9921bed642cdddc5b883e960fbb4efa54a43817af46e8c05c8c59611062a6056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babbc467c5248e09f8d3d0710512a06a92fbd5173a81414b551f82cab3d5d0d3`

```dockerfile
```

-	Layers:
	-	`sha256:a1fee033f27a53ca8a99d5789a2cf1a16782bef7f265384856e2f9c62104fc55`  
		Last Modified: Tue, 18 Nov 2025 06:02:18 GMT  
		Size: 5.6 MB (5589282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd54ab02d147f06764006021d0881cd166981d03206bbcbfdca3215249d036e1`  
		Last Modified: Tue, 18 Nov 2025 06:02:19 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine`

```console
$ docker pull irssi@sha256:a9f4d6de38d69a4ba0ab97a6f43836134df1ffd4290e4a244596c34b80554604
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
$ docker pull irssi@sha256:af936cabadda0c93ca3a229f630f7a5f4888f182b0cbb68edba78dbfaf1dd897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19342220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6546997bb677e945cd6914f29dcdd5d93b42fce0ffcc5b7109c0829285bcea25`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 21:14:55 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90056e842713293c53c6dce4290bfbd298df758358806bd5d3bec46230a89716`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 9.8 MB (9840947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c83cc5e93d426e4646d9cce9fdd7a659215fc178d82320a85f6c6e13ce0939`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1486e128aa6ab32a4665c7cdcb3ed936f18c1e8bf06a7a4d7414222f0a89ac9`  
		Last Modified: Thu, 09 Oct 2025 04:40:05 GMT  
		Size: 6.0 MB (5985049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:7bdbcb1c990676d35120b16117a0adacceb673203918e2e310ce5e5bb9f8ef01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1819ad33d43cee11f7584b364a2e91ced1b9b8229dea8fc4e7bf7cad969bfe7`

```dockerfile
```

-	Layers:
	-	`sha256:0191fc70832b0a543dfdac6c4787f835b7dd8fd57d9e0b7c1a864173c00c5b5a`  
		Last Modified: Thu, 09 Oct 2025 07:59:31 GMT  
		Size: 1.3 MB (1268771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:101fedb5dfade0a1d32aed1260a2c4e061defe2886d8bccdd1cabcc4f65ab848`  
		Last Modified: Thu, 09 Oct 2025 07:59:32 GMT  
		Size: 17.6 KB (17611 bytes)  
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
$ docker pull irssi@sha256:3628d0d0b7185364f7bfc20971afa71df0c98f15e734b4f7199ce9339663e4ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
$ docker pull irssi@sha256:f16b9ab6967270a5b2d0745b7f6b9233f6226b9866de8e46ab3f67f20167dde3
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
$ docker pull irssi@sha256:1c3ad0c692729985069dc605f6970c498536ff77cdc28731957a9981bb5cc69d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53869276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d8b5071dd14f9cc7babdbbb92be355488770afbb4baa1dd4193f835544e54d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:18:09 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 04:18:09 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 04:18:09 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:18:09 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 04:18:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 04:18:46 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 04:18:46 GMT
USER user
# Tue, 18 Nov 2025 04:18:46 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3defe69b9d42ee331ee4997997e0b6950a228ac42a28acb744b2a217802984`  
		Last Modified: Tue, 18 Nov 2025 04:19:08 GMT  
		Size: 19.2 MB (19222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d261d2d2be0daf5812e199043e646cd3b38c72c6a85a46d1aa2664afbbfdab`  
		Last Modified: Tue, 18 Nov 2025 04:19:07 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fb0ce4ebcc67d4eb7b0fd5a6f142adedb46b4a4b5c9f752bb3663092160fd4`  
		Last Modified: Tue, 18 Nov 2025 04:19:07 GMT  
		Size: 4.9 MB (4866605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:22bdb7c49ddfaba85497f04c9d268938716f3b3352fe24378d933a7732e8d145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d4070dfa4342b3ae917c1f765452b8b31cbfe6c04864d806db24d761ba3c65`

```dockerfile
```

-	Layers:
	-	`sha256:5234daf2a71968c25322c71bfea4cdc75082624fc15fcfa85f68596c0e1e8722`  
		Last Modified: Tue, 18 Nov 2025 06:01:31 GMT  
		Size: 5.6 MB (5588377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef6a5104b772e5ddb76df8ed09e14d2aaf8f4757fd03c65a00ce68904337b081`  
		Last Modified: Tue, 18 Nov 2025 06:01:32 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v5

```console
$ docker pull irssi@sha256:3bfeabfea3f173a6eef66224244f7c8ab79162e4b3e3454b5d7b951b699e6d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50944118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce561de65d9ced729b270243f33a9fe650e7088512ea128954c48a408518f61`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:22:31 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:22:31 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:22:31 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:22:31 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:23:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:23:21 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:23:21 GMT
USER user
# Tue, 18 Nov 2025 02:23:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e77346f90948edf43f33edec1b3c918cc8196b58e71fc74d47eb901d26a7c88`  
		Last Modified: Tue, 18 Nov 2025 02:23:39 GMT  
		Size: 18.3 MB (18286955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab20fff4d4c2bb97e0fc743edd41339f9e7f2db5706f958f8419de0227c19fa9`  
		Last Modified: Tue, 18 Nov 2025 02:23:38 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3deede23e33150dccc8ce32f23f864d2a100697bb5c3f5f0d51414ec4913c97f`  
		Last Modified: Tue, 18 Nov 2025 02:23:38 GMT  
		Size: 4.7 MB (4709653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:92486d0301f23f7f5fef04e23a1038f9c9c424a3a47ade435591fdd52853f380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a1456fb2be5b0b7cdc491b833efa2a0ceb4796c5c761a82e6ef643577401e6`

```dockerfile
```

-	Layers:
	-	`sha256:6273392ed72e310ca2593fd6731c533c6f636ed1289f29f728e45fc25e8d45b3`  
		Last Modified: Tue, 18 Nov 2025 06:01:44 GMT  
		Size: 5.6 MB (5585926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c338421356fba9d226382ee2864822813fdd13c90654bd98562c53392aa9884f`  
		Last Modified: Tue, 18 Nov 2025 06:01:44 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v7

```console
$ docker pull irssi@sha256:6206945589cb5f70880eb627ea43ce5e83dc6b09e69ad976fc69ec0a8a671e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48681442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e2dfadf9b6f72f29f6e28ff5885e16008ea991da97c386c12c6effd41ef773`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:24:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:24:00 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:24:00 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:24:00 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:24:00 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:24:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:24:41 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:24:41 GMT
USER user
# Tue, 18 Nov 2025 02:24:41 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07012b32f4cdf9145076ab6689e96bf750c40d6358ddc6b3d983ed86522093b2`  
		Last Modified: Tue, 18 Nov 2025 02:25:00 GMT  
		Size: 17.9 MB (17909541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c317eec7c88d4aa0563b4acdfa018d18e2244d1cd4faaa808233aad6ed8c4eef`  
		Last Modified: Tue, 18 Nov 2025 02:24:57 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999e397c097f4a4f9d07fc0ad13a259eb1c5dc9952ad435619e84f81acd7aa5a`  
		Last Modified: Tue, 18 Nov 2025 02:24:57 GMT  
		Size: 4.6 MB (4558582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:2807406dbaf53bd4128387747c9380192177098c869b02c4fbc0e079734b4a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912225e9dca4300bbd0be1c71db46f637c20bb0ae39dd56905152d9fd37712e7`

```dockerfile
```

-	Layers:
	-	`sha256:826b1dd7affc3defc30e532bafe21b81af9274fe59f9cb13bc8880b266566410`  
		Last Modified: Tue, 18 Nov 2025 06:01:49 GMT  
		Size: 5.6 MB (5588948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caba9a457c37510c70d5629f0b91ebfec1b4e1fddabcf69e4581cc62b8efbdf9`  
		Last Modified: Tue, 18 Nov 2025 06:01:51 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:0ca154f240d8e55d9139562ed162f6d09ed917369e5d3ac0ef11f4277868a144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53972828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494da41086e91ed2e2a5b5a81ed84f81af0313ded1a6a19ca4935a9ed697e260`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:19:36 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:19:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:19:36 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:19:36 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:20:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:20:13 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:20:13 GMT
USER user
# Tue, 18 Nov 2025 02:20:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a619a9a2c5679b92c7e4905e08f05810e02f68d89d06b10524e21d2583f4ab16`  
		Last Modified: Tue, 18 Nov 2025 02:20:32 GMT  
		Size: 19.0 MB (19049113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494e61b822c7885405295c0e02e3d6f750e57594294fe2d8b997a0632065745d`  
		Last Modified: Tue, 18 Nov 2025 02:20:30 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84635b25a37fcbf6ec3700e051e040f70178ad0e6880c9c76aeef1ebcfdf275`  
		Last Modified: Tue, 18 Nov 2025 02:20:30 GMT  
		Size: 4.8 MB (4781743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:6b955f8723ba03a2a30061c1a89c6af489d1442317213524c5594663f9d28695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b845fa96792ab508c1cabce079cc6822b4d3ed51f4ff9cc1486fb4becdb2b9`

```dockerfile
```

-	Layers:
	-	`sha256:1e1288c631711328c43fbd795987044f9c19d6d7ca488586f7d48b2d1bbf9fc9`  
		Last Modified: Tue, 18 Nov 2025 06:01:56 GMT  
		Size: 5.6 MB (5594861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3627aff8962b25f0eb1a595d760c047d53573e5a83de81ffd5ee43ffde3e283f`  
		Last Modified: Tue, 18 Nov 2025 06:01:57 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; 386

```console
$ docker pull irssi@sha256:9ca8e0716038e4dbc489c402c36d6bdc49bb1c6dc80a6050371e0ebb63798b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afefadafe5f8e789fb22f477834b8855758beefa989deb19c7f4e79699e5e89`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:16:34 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:16:34 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:16:34 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:16:34 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:17:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:17:16 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:17:16 GMT
USER user
# Tue, 18 Nov 2025 02:17:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c2fb43e1b281a402bf774cd8bde6070d229add5d03c870cbfe7c8e16f2cbb7`  
		Last Modified: Tue, 18 Nov 2025 02:17:34 GMT  
		Size: 18.7 MB (18740862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6997edee7df4e50b70fa845f324ec76992912dec560143cbead27a7aec43803b`  
		Last Modified: Tue, 18 Nov 2025 02:17:33 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4a3e4cae20c6dc7e982f2a19aa8de8e2b641b6bcc81e72f1bef2930dca363d`  
		Last Modified: Tue, 18 Nov 2025 02:17:34 GMT  
		Size: 4.9 MB (4868298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:59d4050c0c1cd29128be910eccf5ea2a035052b836f46e045244c9f64fa4298c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1003b498f9e79e27d0402d3e70dfc68a8d4f2e5fb76327ddf0d269848f164933`

```dockerfile
```

-	Layers:
	-	`sha256:dae334eb70cbeb2210f0f00af9826de6e0af19a4045d45c351ccd063c967c44c`  
		Last Modified: Tue, 18 Nov 2025 06:02:04 GMT  
		Size: 5.6 MB (5584500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48f17fc2c6b6001ffa3a573775d2cbcfc57f6836267cf4f7578260842ada1b7`  
		Last Modified: Tue, 18 Nov 2025 06:02:05 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; ppc64le

```console
$ docker pull irssi@sha256:459fe708abbb929ace6e5502ac492cb132f84c0e1b80e5a3dd662a7d98b6470e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58240238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72533238806364f21d117ef1051d9f72e86e6063d9c6683bc210cea47127bda`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:03:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 15:03:14 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 15:03:14 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 15:03:14 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 15:03:14 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 15:04:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 15:04:50 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 15:04:50 GMT
USER user
# Tue, 18 Nov 2025 15:04:50 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f858dd24ce7b2766334f11cb720c162ec10dcc1115c24b7c5a2cb933f4732e`  
		Last Modified: Tue, 18 Nov 2025 15:05:24 GMT  
		Size: 19.5 MB (19542803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7e87e68a0f54b41f554a220560c01fae4bca1b4bb4b83336d6c6110f750186`  
		Last Modified: Tue, 18 Nov 2025 15:05:23 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab575b18effe508097b5d8936201a72cd903f95c5c055af70a652fee9591f15f`  
		Last Modified: Tue, 18 Nov 2025 15:05:23 GMT  
		Size: 5.1 MB (5097211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:43823b3c76d194b48bf19fd79dde879a47f65352dc638bc93f743de8b5863b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b0fd9dbba87f1d0495d3f376c23a11766edc9e180c9c6afddfacb7df1cbe76`

```dockerfile
```

-	Layers:
	-	`sha256:ebbbdb938672f1b98a9abf9c0267764349f2261c7295ea777971571c28ac293f`  
		Last Modified: Tue, 18 Nov 2025 18:00:17 GMT  
		Size: 5.6 MB (5595408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ae083b6d0624ff996d976b7dfead8f215b20de9aedc3bef84697341f367a4d3`  
		Last Modified: Tue, 18 Nov 2025 18:00:18 GMT  
		Size: 18.7 KB (18723 bytes)  
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
$ docker pull irssi@sha256:da93e9283b14d1092e451a797eb231f916c62509d64042a7ed65617b6ab9c487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54503019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6b5c6cf33fd166afa65862c57464a7a99d44516a592d7093c9c71058d5008c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:17:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:58 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:17:58 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:17:58 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:17:58 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:18:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:18:33 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:18:33 GMT
USER user
# Tue, 18 Nov 2025 02:18:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bce4907214a18511e7c1676f0b93794fa538b6672045daa187e1c681bbd9019`  
		Last Modified: Tue, 18 Nov 2025 02:18:55 GMT  
		Size: 19.8 MB (19759415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dca431fe704652eca13f122842a6232de3a88619e75b4585c55d73ab6784b33`  
		Last Modified: Tue, 18 Nov 2025 02:18:52 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12fa892c886e7110c8b36d26e5b06c87bdfad4dab6e9bf9b746c2887bce206f`  
		Last Modified: Tue, 18 Nov 2025 02:18:53 GMT  
		Size: 4.9 MB (4905870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:9921bed642cdddc5b883e960fbb4efa54a43817af46e8c05c8c59611062a6056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babbc467c5248e09f8d3d0710512a06a92fbd5173a81414b551f82cab3d5d0d3`

```dockerfile
```

-	Layers:
	-	`sha256:a1fee033f27a53ca8a99d5789a2cf1a16782bef7f265384856e2f9c62104fc55`  
		Last Modified: Tue, 18 Nov 2025 06:02:18 GMT  
		Size: 5.6 MB (5589282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd54ab02d147f06764006021d0881cd166981d03206bbcbfdca3215249d036e1`  
		Last Modified: Tue, 18 Nov 2025 06:02:19 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:trixie`

```console
$ docker pull irssi@sha256:f16b9ab6967270a5b2d0745b7f6b9233f6226b9866de8e46ab3f67f20167dde3
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
$ docker pull irssi@sha256:1c3ad0c692729985069dc605f6970c498536ff77cdc28731957a9981bb5cc69d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53869276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d8b5071dd14f9cc7babdbbb92be355488770afbb4baa1dd4193f835544e54d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:18:09 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 04:18:09 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 04:18:09 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:18:09 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 04:18:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 04:18:46 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 04:18:46 GMT
USER user
# Tue, 18 Nov 2025 04:18:46 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3defe69b9d42ee331ee4997997e0b6950a228ac42a28acb744b2a217802984`  
		Last Modified: Tue, 18 Nov 2025 04:19:08 GMT  
		Size: 19.2 MB (19222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d261d2d2be0daf5812e199043e646cd3b38c72c6a85a46d1aa2664afbbfdab`  
		Last Modified: Tue, 18 Nov 2025 04:19:07 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fb0ce4ebcc67d4eb7b0fd5a6f142adedb46b4a4b5c9f752bb3663092160fd4`  
		Last Modified: Tue, 18 Nov 2025 04:19:07 GMT  
		Size: 4.9 MB (4866605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:22bdb7c49ddfaba85497f04c9d268938716f3b3352fe24378d933a7732e8d145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d4070dfa4342b3ae917c1f765452b8b31cbfe6c04864d806db24d761ba3c65`

```dockerfile
```

-	Layers:
	-	`sha256:5234daf2a71968c25322c71bfea4cdc75082624fc15fcfa85f68596c0e1e8722`  
		Last Modified: Tue, 18 Nov 2025 06:01:31 GMT  
		Size: 5.6 MB (5588377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef6a5104b772e5ddb76df8ed09e14d2aaf8f4757fd03c65a00ce68904337b081`  
		Last Modified: Tue, 18 Nov 2025 06:01:32 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:3bfeabfea3f173a6eef66224244f7c8ab79162e4b3e3454b5d7b951b699e6d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50944118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce561de65d9ced729b270243f33a9fe650e7088512ea128954c48a408518f61`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:22:31 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:22:31 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:22:31 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:22:31 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:23:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:23:21 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:23:21 GMT
USER user
# Tue, 18 Nov 2025 02:23:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e77346f90948edf43f33edec1b3c918cc8196b58e71fc74d47eb901d26a7c88`  
		Last Modified: Tue, 18 Nov 2025 02:23:39 GMT  
		Size: 18.3 MB (18286955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab20fff4d4c2bb97e0fc743edd41339f9e7f2db5706f958f8419de0227c19fa9`  
		Last Modified: Tue, 18 Nov 2025 02:23:38 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3deede23e33150dccc8ce32f23f864d2a100697bb5c3f5f0d51414ec4913c97f`  
		Last Modified: Tue, 18 Nov 2025 02:23:38 GMT  
		Size: 4.7 MB (4709653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:92486d0301f23f7f5fef04e23a1038f9c9c424a3a47ade435591fdd52853f380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a1456fb2be5b0b7cdc491b833efa2a0ceb4796c5c761a82e6ef643577401e6`

```dockerfile
```

-	Layers:
	-	`sha256:6273392ed72e310ca2593fd6731c533c6f636ed1289f29f728e45fc25e8d45b3`  
		Last Modified: Tue, 18 Nov 2025 06:01:44 GMT  
		Size: 5.6 MB (5585926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c338421356fba9d226382ee2864822813fdd13c90654bd98562c53392aa9884f`  
		Last Modified: Tue, 18 Nov 2025 06:01:44 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:6206945589cb5f70880eb627ea43ce5e83dc6b09e69ad976fc69ec0a8a671e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48681442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e2dfadf9b6f72f29f6e28ff5885e16008ea991da97c386c12c6effd41ef773`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:24:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:24:00 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:24:00 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:24:00 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:24:00 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:24:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:24:41 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:24:41 GMT
USER user
# Tue, 18 Nov 2025 02:24:41 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07012b32f4cdf9145076ab6689e96bf750c40d6358ddc6b3d983ed86522093b2`  
		Last Modified: Tue, 18 Nov 2025 02:25:00 GMT  
		Size: 17.9 MB (17909541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c317eec7c88d4aa0563b4acdfa018d18e2244d1cd4faaa808233aad6ed8c4eef`  
		Last Modified: Tue, 18 Nov 2025 02:24:57 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999e397c097f4a4f9d07fc0ad13a259eb1c5dc9952ad435619e84f81acd7aa5a`  
		Last Modified: Tue, 18 Nov 2025 02:24:57 GMT  
		Size: 4.6 MB (4558582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:2807406dbaf53bd4128387747c9380192177098c869b02c4fbc0e079734b4a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912225e9dca4300bbd0be1c71db46f637c20bb0ae39dd56905152d9fd37712e7`

```dockerfile
```

-	Layers:
	-	`sha256:826b1dd7affc3defc30e532bafe21b81af9274fe59f9cb13bc8880b266566410`  
		Last Modified: Tue, 18 Nov 2025 06:01:49 GMT  
		Size: 5.6 MB (5588948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caba9a457c37510c70d5629f0b91ebfec1b4e1fddabcf69e4581cc62b8efbdf9`  
		Last Modified: Tue, 18 Nov 2025 06:01:51 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:0ca154f240d8e55d9139562ed162f6d09ed917369e5d3ac0ef11f4277868a144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53972828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494da41086e91ed2e2a5b5a81ed84f81af0313ded1a6a19ca4935a9ed697e260`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:19:36 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:19:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:19:36 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:19:36 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:20:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:20:13 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:20:13 GMT
USER user
# Tue, 18 Nov 2025 02:20:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a619a9a2c5679b92c7e4905e08f05810e02f68d89d06b10524e21d2583f4ab16`  
		Last Modified: Tue, 18 Nov 2025 02:20:32 GMT  
		Size: 19.0 MB (19049113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494e61b822c7885405295c0e02e3d6f750e57594294fe2d8b997a0632065745d`  
		Last Modified: Tue, 18 Nov 2025 02:20:30 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84635b25a37fcbf6ec3700e051e040f70178ad0e6880c9c76aeef1ebcfdf275`  
		Last Modified: Tue, 18 Nov 2025 02:20:30 GMT  
		Size: 4.8 MB (4781743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:6b955f8723ba03a2a30061c1a89c6af489d1442317213524c5594663f9d28695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b845fa96792ab508c1cabce079cc6822b4d3ed51f4ff9cc1486fb4becdb2b9`

```dockerfile
```

-	Layers:
	-	`sha256:1e1288c631711328c43fbd795987044f9c19d6d7ca488586f7d48b2d1bbf9fc9`  
		Last Modified: Tue, 18 Nov 2025 06:01:56 GMT  
		Size: 5.6 MB (5594861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3627aff8962b25f0eb1a595d760c047d53573e5a83de81ffd5ee43ffde3e283f`  
		Last Modified: Tue, 18 Nov 2025 06:01:57 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; 386

```console
$ docker pull irssi@sha256:9ca8e0716038e4dbc489c402c36d6bdc49bb1c6dc80a6050371e0ebb63798b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afefadafe5f8e789fb22f477834b8855758beefa989deb19c7f4e79699e5e89`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:16:34 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:16:34 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:16:34 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:16:34 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:17:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:17:16 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:17:16 GMT
USER user
# Tue, 18 Nov 2025 02:17:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c2fb43e1b281a402bf774cd8bde6070d229add5d03c870cbfe7c8e16f2cbb7`  
		Last Modified: Tue, 18 Nov 2025 02:17:34 GMT  
		Size: 18.7 MB (18740862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6997edee7df4e50b70fa845f324ec76992912dec560143cbead27a7aec43803b`  
		Last Modified: Tue, 18 Nov 2025 02:17:33 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4a3e4cae20c6dc7e982f2a19aa8de8e2b641b6bcc81e72f1bef2930dca363d`  
		Last Modified: Tue, 18 Nov 2025 02:17:34 GMT  
		Size: 4.9 MB (4868298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:59d4050c0c1cd29128be910eccf5ea2a035052b836f46e045244c9f64fa4298c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1003b498f9e79e27d0402d3e70dfc68a8d4f2e5fb76327ddf0d269848f164933`

```dockerfile
```

-	Layers:
	-	`sha256:dae334eb70cbeb2210f0f00af9826de6e0af19a4045d45c351ccd063c967c44c`  
		Last Modified: Tue, 18 Nov 2025 06:02:04 GMT  
		Size: 5.6 MB (5584500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48f17fc2c6b6001ffa3a573775d2cbcfc57f6836267cf4f7578260842ada1b7`  
		Last Modified: Tue, 18 Nov 2025 06:02:05 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:459fe708abbb929ace6e5502ac492cb132f84c0e1b80e5a3dd662a7d98b6470e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58240238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72533238806364f21d117ef1051d9f72e86e6063d9c6683bc210cea47127bda`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 15:03:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 15:03:14 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 15:03:14 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 15:03:14 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 15:03:14 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 15:04:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 15:04:50 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 15:04:50 GMT
USER user
# Tue, 18 Nov 2025 15:04:50 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f858dd24ce7b2766334f11cb720c162ec10dcc1115c24b7c5a2cb933f4732e`  
		Last Modified: Tue, 18 Nov 2025 15:05:24 GMT  
		Size: 19.5 MB (19542803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7e87e68a0f54b41f554a220560c01fae4bca1b4bb4b83336d6c6110f750186`  
		Last Modified: Tue, 18 Nov 2025 15:05:23 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab575b18effe508097b5d8936201a72cd903f95c5c055af70a652fee9591f15f`  
		Last Modified: Tue, 18 Nov 2025 15:05:23 GMT  
		Size: 5.1 MB (5097211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:43823b3c76d194b48bf19fd79dde879a47f65352dc638bc93f743de8b5863b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b0fd9dbba87f1d0495d3f376c23a11766edc9e180c9c6afddfacb7df1cbe76`

```dockerfile
```

-	Layers:
	-	`sha256:ebbbdb938672f1b98a9abf9c0267764349f2261c7295ea777971571c28ac293f`  
		Last Modified: Tue, 18 Nov 2025 18:00:17 GMT  
		Size: 5.6 MB (5595408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ae083b6d0624ff996d976b7dfead8f215b20de9aedc3bef84697341f367a4d3`  
		Last Modified: Tue, 18 Nov 2025 18:00:18 GMT  
		Size: 18.7 KB (18723 bytes)  
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
$ docker pull irssi@sha256:da93e9283b14d1092e451a797eb231f916c62509d64042a7ed65617b6ab9c487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54503019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6b5c6cf33fd166afa65862c57464a7a99d44516a592d7093c9c71058d5008c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:17:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:58 GMT
ENV HOME=/home/user
# Tue, 18 Nov 2025 02:17:58 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 18 Nov 2025 02:17:58 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:17:58 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 18 Nov 2025 02:18:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 18 Nov 2025 02:18:33 GMT
WORKDIR /home/user
# Tue, 18 Nov 2025 02:18:33 GMT
USER user
# Tue, 18 Nov 2025 02:18:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bce4907214a18511e7c1676f0b93794fa538b6672045daa187e1c681bbd9019`  
		Last Modified: Tue, 18 Nov 2025 02:18:55 GMT  
		Size: 19.8 MB (19759415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dca431fe704652eca13f122842a6232de3a88619e75b4585c55d73ab6784b33`  
		Last Modified: Tue, 18 Nov 2025 02:18:52 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12fa892c886e7110c8b36d26e5b06c87bdfad4dab6e9bf9b746c2887bce206f`  
		Last Modified: Tue, 18 Nov 2025 02:18:53 GMT  
		Size: 4.9 MB (4905870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:9921bed642cdddc5b883e960fbb4efa54a43817af46e8c05c8c59611062a6056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babbc467c5248e09f8d3d0710512a06a92fbd5173a81414b551f82cab3d5d0d3`

```dockerfile
```

-	Layers:
	-	`sha256:a1fee033f27a53ca8a99d5789a2cf1a16782bef7f265384856e2f9c62104fc55`  
		Last Modified: Tue, 18 Nov 2025 06:02:18 GMT  
		Size: 5.6 MB (5589282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd54ab02d147f06764006021d0881cd166981d03206bbcbfdca3215249d036e1`  
		Last Modified: Tue, 18 Nov 2025 06:02:19 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json
