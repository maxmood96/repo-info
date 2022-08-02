<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `irssi`

-	[`irssi:1`](#irssi1)
-	[`irssi:1-alpine`](#irssi1-alpine)
-	[`irssi:1.4`](#irssi14)
-	[`irssi:1.4-alpine`](#irssi14-alpine)
-	[`irssi:1.4.2`](#irssi142)
-	[`irssi:1.4.2-alpine`](#irssi142-alpine)
-	[`irssi:alpine`](#irssialpine)
-	[`irssi:latest`](#irssilatest)

## `irssi:1`

```console
$ docker pull irssi@sha256:6c1fac3ca2e9ecdabbc9187638b5106d56be577b5c60a5d3a1e2d1edb269c0f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `irssi:1` - linux; amd64

```console
$ docker pull irssi@sha256:4d0a57587f583ae57ba90633678591956501c95dbc1cd6703a8e8a4790577e2d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51343672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba512ed38aa173d1e69a89d5f49352ad0b61efaf7d3f7c542c627b03cdcfb0ef`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 04:33:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 04:33:52 GMT
ENV HOME=/home/user
# Tue, 12 Jul 2022 04:33:53 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 12 Jul 2022 04:33:53 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 19:31:00 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 19:31:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dirmngr 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Mon, 18 Jul 2022 19:31:39 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 19:31:39 GMT
USER user
# Mon, 18 Jul 2022 19:31:39 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:461246efe0a75316d99afdbf348f7063b57b0caeee8daab775f1f08152ea36f4`  
		Last Modified: Tue, 12 Jul 2022 01:24:34 GMT  
		Size: 31.4 MB (31366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e79e09cff439b97f521fe2a06f622f78563e7fa21992fac5121edd4d4cfdff7`  
		Last Modified: Tue, 12 Jul 2022 04:34:55 GMT  
		Size: 15.5 MB (15497990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de2a42942ce691111b16112e95781a9a4c0fad8e02d80fa30ad655226332107`  
		Last Modified: Tue, 12 Jul 2022 04:34:52 GMT  
		Size: 4.2 KB (4203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3a67937f3d44395a92dcfaabe40094a4d8fef1ba55683cdedea2d380c6d326`  
		Last Modified: Mon, 18 Jul 2022 19:32:29 GMT  
		Size: 4.5 MB (4474869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1` - linux; arm variant v5

```console
$ docker pull irssi@sha256:cbaecb7e5ce27a9f92f733f7d03bfc8b5a0a43ee3114f6bacafad16f03f8207a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47909536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ffc892412aa787e4af6555c04156ee5c4e13d354e8d87876b73144e97ea2954`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:10 GMT
ADD file:4cd2f95737fd3007912428eeac56036c9e67e989e66cec08a8be99da47f88494 in / 
# Tue, 02 Aug 2022 00:49:10 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:56:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:56:56 GMT
ENV HOME=/home/user
# Tue, 02 Aug 2022 01:56:57 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 02 Aug 2022 01:56:57 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 01:56:57 GMT
ENV IRSSI_VERSION=1.4.2
# Tue, 02 Aug 2022 01:57:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dirmngr 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Tue, 02 Aug 2022 01:57:52 GMT
WORKDIR /home/user
# Tue, 02 Aug 2022 01:57:52 GMT
USER user
# Tue, 02 Aug 2022 01:57:52 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5890b0ca6af5e8467a488e68716691950496a8f247d0495c2d595ddcb1893aff`  
		Last Modified: Tue, 02 Aug 2022 00:56:06 GMT  
		Size: 28.9 MB (28905515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b96885e167027fcb6391bfc0fda996e4c68280b656a669066fbca6ee32f57c`  
		Last Modified: Tue, 02 Aug 2022 01:58:20 GMT  
		Size: 14.7 MB (14674073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b78241a104470ed2f1128a082f2f65560bf86cf724fa5df219dbdf00d2faa0`  
		Last Modified: Tue, 02 Aug 2022 01:58:15 GMT  
		Size: 4.2 KB (4190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72eefd5a1fe1c338236141cea2f58baa3efd6d80e1d1c7043ed996e975a96ac`  
		Last Modified: Tue, 02 Aug 2022 01:58:16 GMT  
		Size: 4.3 MB (4325758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1` - linux; arm variant v7

```console
$ docker pull irssi@sha256:e921634c5488eab60d5f3bb71deaf4120a440291f0be93ee8379aba27b415e9f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45176825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f99154c23f142ad6e7a9f37ecd8062dceea9d74ff0edd51b490fc8e937b82ff`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Jul 2022 00:59:54 GMT
ADD file:ae890621b36ff6e27364bb7316b5bd4319a820ddf7e65565c6201eb11d70fde9 in / 
# Tue, 12 Jul 2022 00:59:55 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 06:34:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 06:34:28 GMT
ENV HOME=/home/user
# Tue, 12 Jul 2022 06:34:30 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 12 Jul 2022 06:34:30 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 20:17:40 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 20:18:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dirmngr 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Mon, 18 Jul 2022 20:18:49 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 20:18:49 GMT
USER user
# Mon, 18 Jul 2022 20:18:50 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:314cda9d0ef2282082d2bd0efd7659e0d9edb3ceae8e7919d990bcf95cbb3d2b`  
		Last Modified: Tue, 12 Jul 2022 01:12:37 GMT  
		Size: 26.6 MB (26560559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ca7959cb389c6a5178f433269da0b2c6c8474f8d44d9e40a3869ac96588d4d`  
		Last Modified: Tue, 12 Jul 2022 06:36:58 GMT  
		Size: 14.4 MB (14424292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976f86f89cadf992f0b4055818f123826998345af9b5f5940d0bc653a2427057`  
		Last Modified: Tue, 12 Jul 2022 06:36:43 GMT  
		Size: 4.2 KB (4188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419495c1f261eea969d0d2028dc1d47a5b2f7dd668f9f481a728a8b665085a0a`  
		Last Modified: Mon, 18 Jul 2022 20:20:19 GMT  
		Size: 4.2 MB (4187786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:2d22ed2ec5237ace63ed06ac97c4d4a20e21c76708fadc56fc6c0a3962626605
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49603297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2913f649550379e0daaad94fb55a90e376e9be33556c8052e9d6460df2fad579`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:34 GMT
ADD file:f3a33075f4c3324c6a634ef37a1965ddd5606b4449c0f5909ce18eeb8268b612 in / 
# Tue, 12 Jul 2022 00:40:35 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 03:58:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 03:58:01 GMT
ENV HOME=/home/user
# Tue, 12 Jul 2022 03:58:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 12 Jul 2022 03:58:03 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 18:48:35 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 18:49:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dirmngr 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Mon, 18 Jul 2022 18:49:06 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 18:49:07 GMT
USER user
# Mon, 18 Jul 2022 18:49:08 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:60197a4c18d4b386d371cf39d01c48e98c357bba06da0b070a3c1f75006fd838`  
		Last Modified: Tue, 12 Jul 2022 00:46:13 GMT  
		Size: 30.1 MB (30054226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31d5df8c69c5980350d19a5ffb57504867950d6e5b8c3a6f11080af3e3a0c38`  
		Last Modified: Tue, 12 Jul 2022 03:59:16 GMT  
		Size: 15.4 MB (15377261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b76490db37eaebc94203a05f902096f75ed24cf7a086628cafc39dc7769bbf`  
		Last Modified: Tue, 12 Jul 2022 03:59:13 GMT  
		Size: 4.1 KB (4067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ccc8bb291efc3aa7242c0d8b4780541f2d9603daf68e756cdf6f635b29b4f4`  
		Last Modified: Mon, 18 Jul 2022 18:50:05 GMT  
		Size: 4.2 MB (4167743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1` - linux; 386

```console
$ docker pull irssi@sha256:6c4957ff125a55b1b7681b5dcff90a8b3038362e2a8e4153879db7a2be28b1c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51679954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50aea866fe6b1bbdd4191e840834c20db4a10eb7bd0c9578c2b83f18f0825eb0`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 02 Aug 2022 00:39:20 GMT
ADD file:f771e2286465694126158821089d801c7296376be2a56189e6041a15d2fe79f5 in / 
# Tue, 02 Aug 2022 00:39:21 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 03:10:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 03:10:20 GMT
ENV HOME=/home/user
# Tue, 02 Aug 2022 03:10:20 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 02 Aug 2022 03:10:21 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 03:10:22 GMT
ENV IRSSI_VERSION=1.4.2
# Tue, 02 Aug 2022 03:10:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dirmngr 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Tue, 02 Aug 2022 03:11:00 GMT
WORKDIR /home/user
# Tue, 02 Aug 2022 03:11:01 GMT
USER user
# Tue, 02 Aug 2022 03:11:02 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:90eb7f0ce9f33cf5dcd67d54c2fa606186dbaa5f95b6046f36145097267f9e53`  
		Last Modified: Tue, 02 Aug 2022 00:45:14 GMT  
		Size: 32.4 MB (32374054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e807876191c36c0343701cbf9f2866e857910c0bb70333fa34a0d8b7bc512b`  
		Last Modified: Tue, 02 Aug 2022 03:11:36 GMT  
		Size: 15.0 MB (15031673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e042e29265be416ef65d312aeebbf008b8a29b1ed9c1351486c336b91a11d4`  
		Last Modified: Tue, 02 Aug 2022 03:11:33 GMT  
		Size: 4.1 KB (4053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac3539df7150f2d647d38ae218b76d52ba34303d339bf960aa2fe6c5a8b441e`  
		Last Modified: Tue, 02 Aug 2022 03:11:33 GMT  
		Size: 4.3 MB (4270174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1` - linux; mips64le

```console
$ docker pull irssi@sha256:5e0bf0828437d767db40431686c24d975b9601b8360a8164074769d9d13c6acf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48617509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556eed7be91d94dbe25d160fa495d39f69c1add07bb664e33c473f458f9a3dd1`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 02 Aug 2022 01:10:34 GMT
ADD file:6dc22a1e5b5fcf23f2549406ddcc45c4e244f46e21eafa881de81fa87438e5d8 in / 
# Tue, 02 Aug 2022 01:10:38 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 03:17:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 03:17:38 GMT
ENV HOME=/home/user
# Tue, 02 Aug 2022 03:17:45 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 02 Aug 2022 03:17:48 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 03:17:51 GMT
ENV IRSSI_VERSION=1.4.2
# Tue, 02 Aug 2022 03:21:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dirmngr 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Tue, 02 Aug 2022 03:21:45 GMT
WORKDIR /home/user
# Tue, 02 Aug 2022 03:21:49 GMT
USER user
# Tue, 02 Aug 2022 03:21:52 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:88350749a27614c791450c256b051f023d81cdd256211274b1efac493779d2be`  
		Last Modified: Tue, 02 Aug 2022 01:21:02 GMT  
		Size: 29.6 MB (29628964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32415daee5708ee92f8f0d8cbb82cc3e0aba17931f1daa2fe19a06b38d6b4b3`  
		Last Modified: Tue, 02 Aug 2022 03:22:25 GMT  
		Size: 14.7 MB (14668257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31be73626d6aa213ab20d502e69c5545c4ef2147bcacdb751040c739cc9c28f`  
		Last Modified: Tue, 02 Aug 2022 03:22:11 GMT  
		Size: 4.1 KB (4066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848b6bffac840f3f64795049e1548ebc7769ce9475b3921d0cd85176dd664465`  
		Last Modified: Tue, 02 Aug 2022 03:22:15 GMT  
		Size: 4.3 MB (4316222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1` - linux; ppc64le

```console
$ docker pull irssi@sha256:a8e6205e8016bdc0cd109de6ed6e9d007b72c466be63523b492adeecc53f5433
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55758440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a96be9146d164ac0e9f7bfc663cc6e3e4d13b1d64bc9f0eef34643e6ac4eb72`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Jul 2022 01:25:28 GMT
ADD file:9e1afe48f40d94f879aefb12a7e68da2f0772d701e95b8219bd1f79a83e1933a in / 
# Tue, 12 Jul 2022 01:25:32 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 06:02:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 06:02:16 GMT
ENV HOME=/home/user
# Tue, 12 Jul 2022 06:02:24 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 12 Jul 2022 06:02:27 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 20:59:07 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 21:05:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dirmngr 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Mon, 18 Jul 2022 21:05:29 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 21:05:34 GMT
USER user
# Mon, 18 Jul 2022 21:05:39 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:bd3d68d1ce583727f6378a16916795b955cc0ad39e0ebe754a26007ef54744fa`  
		Last Modified: Tue, 12 Jul 2022 01:36:03 GMT  
		Size: 35.3 MB (35272500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39e75ba095c6987e0fca8686cbac241d72e4b34526b2312618405b4b0feba71`  
		Last Modified: Tue, 12 Jul 2022 06:07:46 GMT  
		Size: 15.8 MB (15797793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3029a04938ed8ac96ce82eea145146851d02beccd82d19f3af82573e0a00f41a`  
		Last Modified: Tue, 12 Jul 2022 06:07:41 GMT  
		Size: 4.2 KB (4216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3650334413d621df83d25ff4038e0c1ac603ce5ef7d064a444887e524b546e`  
		Last Modified: Mon, 18 Jul 2022 21:07:33 GMT  
		Size: 4.7 MB (4683931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1` - linux; s390x

```console
$ docker pull irssi@sha256:c664751349154e1ce063ab587bf63b9f363867f57ae9c1edb8da99dc42b3fe4a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50192142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2485b9e0e2067eb44ac6ef1a366099a1d3f9f29d553bfbe09dc44ef7dae829e`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 02 Aug 2022 00:42:27 GMT
ADD file:c2afc8990930846fbe7c99bfdfe9ea562c75feb6e3c9122431f7c9f8b5e51a7f in / 
# Tue, 02 Aug 2022 00:42:29 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 02:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 02:35:29 GMT
ENV HOME=/home/user
# Tue, 02 Aug 2022 02:35:30 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 02 Aug 2022 02:35:30 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 02:35:30 GMT
ENV IRSSI_VERSION=1.4.2
# Tue, 02 Aug 2022 02:35:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dirmngr 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Tue, 02 Aug 2022 02:35:57 GMT
WORKDIR /home/user
# Tue, 02 Aug 2022 02:35:57 GMT
USER user
# Tue, 02 Aug 2022 02:35:57 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:026d311d0716db60eba0572ea784c21031f420960510cebcc383dc53949b4db8`  
		Last Modified: Tue, 02 Aug 2022 00:48:01 GMT  
		Size: 29.6 MB (29640259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813471a33007d06aacc4cbaf7aff38415e1205c5fee4edd8e2c0f2bfebd0d8f2`  
		Last Modified: Tue, 02 Aug 2022 02:36:36 GMT  
		Size: 15.8 MB (15796925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecee3a36c2c868b4cf52323b6be62201a59b371d017e3336960cb20cb2ff679`  
		Last Modified: Tue, 02 Aug 2022 02:36:33 GMT  
		Size: 4.2 KB (4208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e622d653a1f908ca86a2ecd33d0381d0bcafee70c2badfa9733d02eca0a6901d`  
		Last Modified: Tue, 02 Aug 2022 02:36:33 GMT  
		Size: 4.8 MB (4750750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `irssi:1-alpine`

```console
$ docker pull irssi@sha256:854de1a51b99067ebb0100a67c6e13673d2fbdd5eb9a7b4b77484c65fc3cd0ad
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

### `irssi:1-alpine` - linux; amd64

```console
$ docker pull irssi@sha256:f3c10f861f7d988f12d99c084634ebbcaa0ee7554709b4cbeda8c0ffe5f7511e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17457462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f85f9670eee79491099fe67fa0e6ffc8d1f9222f94eac0129863c809506224`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 00:23:35 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Tue, 19 Jul 2022 00:23:35 GMT
ENV HOME=/home/user
# Tue, 19 Jul 2022 00:23:35 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 19 Jul 2022 00:23:36 GMT
ENV LANG=C.UTF-8
# Tue, 19 Jul 2022 00:23:36 GMT
ENV IRSSI_VERSION=1.4.2
# Tue, 19 Jul 2022 00:23:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Tue, 19 Jul 2022 00:23:58 GMT
WORKDIR /home/user
# Tue, 19 Jul 2022 00:23:58 GMT
USER user
# Tue, 19 Jul 2022 00:23:58 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b5bbd7de7a34116522b4918981e9d13d9f16810a588b74d764c886ca66f286`  
		Last Modified: Tue, 19 Jul 2022 00:24:16 GMT  
		Size: 9.6 MB (9635582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3125246c3b589cd814d841704f2635efc959d690c1baf7949f9bca0fdb5185a`  
		Last Modified: Tue, 19 Jul 2022 00:24:14 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912b4d23111a9384a40ebe73bb55898ab8cd45d79416b35411328fa809c814c0`  
		Last Modified: Tue, 19 Jul 2022 00:24:15 GMT  
		Size: 5.0 MB (5021792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:3a494d4239afb464641516da33a1ac5641f0b315b22fa104eac28aa0a72f9c28
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16382978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb33fdc30a24d339ba9656ee8df90546bae6308ff1b070dcc65098a1ff78e4dc`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 Jul 2022 19:49:37 GMT
ADD file:7a20333469e71664904a0cb8f61613250f2bd092b4a27bfa7bbae1dc7e21b7ed in / 
# Mon, 18 Jul 2022 19:49:37 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 21:02:43 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 18 Jul 2022 21:02:44 GMT
ENV HOME=/home/user
# Mon, 18 Jul 2022 21:02:46 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 18 Jul 2022 21:02:46 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 21:02:46 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 21:03:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 18 Jul 2022 21:03:20 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 21:03:21 GMT
USER user
# Mon, 18 Jul 2022 21:03:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b7885075fcd06a866d12dfd56eb704045eaadbd22dc03a224cd98715be566677`  
		Last Modified: Mon, 18 Jul 2022 19:08:42 GMT  
		Size: 2.6 MB (2606431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead05fb861289a3112d85fde030e8569e9a7dc8dd23508fe65d82f88ee0b12a3`  
		Last Modified: Mon, 18 Jul 2022 21:04:05 GMT  
		Size: 8.9 MB (8861206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86cdcb4e11581d3551b521decf6e7d4a73ad09f615896b0723f46ed075ef77e2`  
		Last Modified: Mon, 18 Jul 2022 21:03:57 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5685ef9768727bd6b69beb5438e3f2f0dd1cc972b33dfe398ca9f2fc28a2e6c3`  
		Last Modified: Mon, 18 Jul 2022 21:04:01 GMT  
		Size: 4.9 MB (4914057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:7726b670a7075eb493678469422e169667df6aab527e51cfaa879cda7f5062cc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15814593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64832f2b21baf5ec2006706a9cf25927c0a2a416d508ab5593ece2a7d00c258`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 Jul 2022 21:24:47 GMT
ADD file:68590e866bc6db27ad54d23de7dd275d0389cb86e4e6291a1243fcc234f2f7a1 in / 
# Mon, 18 Jul 2022 21:24:47 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 21:46:46 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 18 Jul 2022 21:46:47 GMT
ENV HOME=/home/user
# Mon, 18 Jul 2022 21:46:49 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 18 Jul 2022 21:46:49 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 21:46:50 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 21:47:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 18 Jul 2022 21:47:14 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 21:47:14 GMT
USER user
# Mon, 18 Jul 2022 21:47:14 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a6b45ace95f42a930d15c33679ab9c85d46019b7e73954cadc73bb9ba176509b`  
		Last Modified: Mon, 18 Jul 2022 19:08:56 GMT  
		Size: 2.4 MB (2412307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9e1dca7051a20a401a3d84f96da71dd867a9ee0e24f1a7f09677de75d53140`  
		Last Modified: Mon, 18 Jul 2022 21:48:15 GMT  
		Size: 8.7 MB (8708216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0f6db8c54d3924f3e78936c4066057027d8b3bd0a10af466cfc216a9ef6d2b`  
		Last Modified: Mon, 18 Jul 2022 21:48:07 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4987ffc8bc6cbb769df4dd941574de6d0a30766e1d35d371c5ed45aeba785b`  
		Last Modified: Mon, 18 Jul 2022 21:48:10 GMT  
		Size: 4.7 MB (4692786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:564cd4be47c93fc2e03b800764ef11e1c27a4f37a56802df4197732fad9ae2e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17216500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf5779dbb8c59aa4f024dd254f360646e9a489a7ee967488d4de20260c03dc9`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:36:45 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 18 Jul 2022 23:36:45 GMT
ENV HOME=/home/user
# Mon, 18 Jul 2022 23:36:46 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 18 Jul 2022 23:36:47 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 23:36:48 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 23:37:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 18 Jul 2022 23:37:08 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 23:37:09 GMT
USER user
# Mon, 18 Jul 2022 23:37:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f97344484467e4c4ebb85aae724170073799295a3442c50ab532e249bd27b412`  
		Last Modified: Mon, 18 Jul 2022 19:08:29 GMT  
		Size: 2.7 MB (2694720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc9217fb4aa392f4d68e15e67a1738bdba81661d76ef27f98a859ca98fea7f4`  
		Last Modified: Mon, 18 Jul 2022 23:37:41 GMT  
		Size: 9.6 MB (9614190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c943cd07b898efc2d7524a805d91e8988448f4bfa1f9948493f1a885fd4e5e31`  
		Last Modified: Mon, 18 Jul 2022 23:37:39 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957ecc993dbe69ce704931a74e819999103ff7ed534556a71b5e62717f85f566`  
		Last Modified: Mon, 18 Jul 2022 23:37:40 GMT  
		Size: 4.9 MB (4906333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1-alpine` - linux; 386

```console
$ docker pull irssi@sha256:cb377bddeaa0f32f50bec41afb14efa635b8b275cd8dc27d29b9eb84278b07cd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16895156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89892b7d6a7e9cf4b9c20eaddfcfb4b60dfd2d3baf63e25ed682b85da30d9f9b`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 Jul 2022 20:38:19 GMT
ADD file:be69b7550bf861d8fb12bdbe1edf3a0d2519a6a4da61bd04858b6258ffbf48a7 in / 
# Mon, 18 Jul 2022 20:38:19 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 21:22:34 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 18 Jul 2022 21:22:34 GMT
ENV HOME=/home/user
# Mon, 18 Jul 2022 21:22:35 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 18 Jul 2022 21:22:36 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 21:22:37 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 21:22:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 18 Jul 2022 21:22:58 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 21:22:59 GMT
USER user
# Mon, 18 Jul 2022 21:23:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5d7f927419794ebb7496ac38b0659686317b2d2fac7252a4a0d40d43d5fdd662`  
		Last Modified: Mon, 18 Jul 2022 19:09:22 GMT  
		Size: 2.8 MB (2802334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2145e9491f9798ce6ba6a51e68ca96b186ad6ba788f3c69c1b1b154ad56a7e1a`  
		Last Modified: Mon, 18 Jul 2022 21:23:31 GMT  
		Size: 9.0 MB (8992480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d16a63cb4fb487e02f956e04140855533c28e2ee5e908cec5ea8a2468d6da3b`  
		Last Modified: Mon, 18 Jul 2022 21:23:29 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7d0ef11d7b29e8d2ec1207dc213657f05c112333cfe74b1e705a57a4df207e`  
		Last Modified: Mon, 18 Jul 2022 21:23:29 GMT  
		Size: 5.1 MB (5099084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:008615550f0709646e4fcc911584d2d8aa1b24e8bdd0a7672eae582e45216607
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17626048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8fd78e65c7b8aabcd0fb57760ca1a6a2c764f73a4bd95fa6940cff225cff5d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 Jul 2022 21:29:30 GMT
ADD file:69e4080f15f54e2d8f8aa25fdcba9c01dde149d43592edd5023106675e54a769 in / 
# Mon, 18 Jul 2022 21:29:31 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:23:27 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 18 Jul 2022 23:23:30 GMT
ENV HOME=/home/user
# Mon, 18 Jul 2022 23:23:37 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 18 Jul 2022 23:23:39 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 23:23:43 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 23:24:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 18 Jul 2022 23:24:22 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 23:24:27 GMT
USER user
# Mon, 18 Jul 2022 23:24:29 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:602896d442490cd3fbb6599f0f862d3673b7cd58eca3ac842b8e09bf8d012443`  
		Last Modified: Mon, 18 Jul 2022 19:09:09 GMT  
		Size: 2.8 MB (2789923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144d51d6462d104bc78871a12553ef8ecb02c24118323022315248cbccbae669`  
		Last Modified: Mon, 18 Jul 2022 23:25:09 GMT  
		Size: 9.7 MB (9719919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52753540298a409bae5d1a612e5db8239226d77a43e088361efcd4fc867ba3b7`  
		Last Modified: Mon, 18 Jul 2022 23:25:07 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1043e272f851236c4dc571cd7e98077d260326039dff8d24a2b0640dad98a15`  
		Last Modified: Mon, 18 Jul 2022 23:25:08 GMT  
		Size: 5.1 MB (5114922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:2f6ebdb305e5f2e8c4126dd0f9c56b6f10498a6782eaca868413a5181aed9820
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17667151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b91544b93d574c49f846ba8ca11d4857f02fb74183b9a821dcf03050801c6e8`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 Jul 2022 20:41:35 GMT
ADD file:deaa573cd61e07709846a5300fb627a8610e9754129c085ed483ff8897d0c002 in / 
# Mon, 18 Jul 2022 20:41:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 22:44:07 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 18 Jul 2022 22:44:10 GMT
ENV HOME=/home/user
# Mon, 18 Jul 2022 22:44:12 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 18 Jul 2022 22:44:13 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 22:44:14 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 22:45:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 18 Jul 2022 22:45:05 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 22:45:06 GMT
USER user
# Mon, 18 Jul 2022 22:45:06 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5f1840d5bacf4162a87f497e22d94bce946e660bdfce8eeefcbf7bd0beb193f3`  
		Last Modified: Mon, 18 Jul 2022 20:42:36 GMT  
		Size: 2.6 MB (2580798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df951ee246cfabbbcfb2dda7536db44d3a15ad885c57fb96e11b03ff3589094`  
		Last Modified: Mon, 18 Jul 2022 22:45:57 GMT  
		Size: 10.1 MB (10054683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d765c6e93fca15ebd173b5d15fd5fd709d4c8adc68967ced468eeb250bc472`  
		Last Modified: Mon, 18 Jul 2022 22:45:54 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a48b2916418ae80779b9c6f694ecce949d7d71adcddc0aa3f4bb2921a25a84`  
		Last Modified: Mon, 18 Jul 2022 22:45:56 GMT  
		Size: 5.0 MB (5030386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `irssi:1.4`

```console
$ docker pull irssi@sha256:6c1fac3ca2e9ecdabbc9187638b5106d56be577b5c60a5d3a1e2d1edb269c0f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `irssi:1.4` - linux; amd64

```console
$ docker pull irssi@sha256:4d0a57587f583ae57ba90633678591956501c95dbc1cd6703a8e8a4790577e2d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51343672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba512ed38aa173d1e69a89d5f49352ad0b61efaf7d3f7c542c627b03cdcfb0ef`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 04:33:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 04:33:52 GMT
ENV HOME=/home/user
# Tue, 12 Jul 2022 04:33:53 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 12 Jul 2022 04:33:53 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 19:31:00 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 19:31:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dirmngr 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Mon, 18 Jul 2022 19:31:39 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 19:31:39 GMT
USER user
# Mon, 18 Jul 2022 19:31:39 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:461246efe0a75316d99afdbf348f7063b57b0caeee8daab775f1f08152ea36f4`  
		Last Modified: Tue, 12 Jul 2022 01:24:34 GMT  
		Size: 31.4 MB (31366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e79e09cff439b97f521fe2a06f622f78563e7fa21992fac5121edd4d4cfdff7`  
		Last Modified: Tue, 12 Jul 2022 04:34:55 GMT  
		Size: 15.5 MB (15497990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de2a42942ce691111b16112e95781a9a4c0fad8e02d80fa30ad655226332107`  
		Last Modified: Tue, 12 Jul 2022 04:34:52 GMT  
		Size: 4.2 KB (4203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3a67937f3d44395a92dcfaabe40094a4d8fef1ba55683cdedea2d380c6d326`  
		Last Modified: Mon, 18 Jul 2022 19:32:29 GMT  
		Size: 4.5 MB (4474869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1.4` - linux; arm variant v5

```console
$ docker pull irssi@sha256:cbaecb7e5ce27a9f92f733f7d03bfc8b5a0a43ee3114f6bacafad16f03f8207a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47909536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ffc892412aa787e4af6555c04156ee5c4e13d354e8d87876b73144e97ea2954`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:10 GMT
ADD file:4cd2f95737fd3007912428eeac56036c9e67e989e66cec08a8be99da47f88494 in / 
# Tue, 02 Aug 2022 00:49:10 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:56:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:56:56 GMT
ENV HOME=/home/user
# Tue, 02 Aug 2022 01:56:57 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 02 Aug 2022 01:56:57 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 01:56:57 GMT
ENV IRSSI_VERSION=1.4.2
# Tue, 02 Aug 2022 01:57:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dirmngr 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Tue, 02 Aug 2022 01:57:52 GMT
WORKDIR /home/user
# Tue, 02 Aug 2022 01:57:52 GMT
USER user
# Tue, 02 Aug 2022 01:57:52 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5890b0ca6af5e8467a488e68716691950496a8f247d0495c2d595ddcb1893aff`  
		Last Modified: Tue, 02 Aug 2022 00:56:06 GMT  
		Size: 28.9 MB (28905515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b96885e167027fcb6391bfc0fda996e4c68280b656a669066fbca6ee32f57c`  
		Last Modified: Tue, 02 Aug 2022 01:58:20 GMT  
		Size: 14.7 MB (14674073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b78241a104470ed2f1128a082f2f65560bf86cf724fa5df219dbdf00d2faa0`  
		Last Modified: Tue, 02 Aug 2022 01:58:15 GMT  
		Size: 4.2 KB (4190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72eefd5a1fe1c338236141cea2f58baa3efd6d80e1d1c7043ed996e975a96ac`  
		Last Modified: Tue, 02 Aug 2022 01:58:16 GMT  
		Size: 4.3 MB (4325758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1.4` - linux; arm variant v7

```console
$ docker pull irssi@sha256:e921634c5488eab60d5f3bb71deaf4120a440291f0be93ee8379aba27b415e9f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45176825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f99154c23f142ad6e7a9f37ecd8062dceea9d74ff0edd51b490fc8e937b82ff`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Jul 2022 00:59:54 GMT
ADD file:ae890621b36ff6e27364bb7316b5bd4319a820ddf7e65565c6201eb11d70fde9 in / 
# Tue, 12 Jul 2022 00:59:55 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 06:34:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 06:34:28 GMT
ENV HOME=/home/user
# Tue, 12 Jul 2022 06:34:30 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 12 Jul 2022 06:34:30 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 20:17:40 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 20:18:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dirmngr 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Mon, 18 Jul 2022 20:18:49 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 20:18:49 GMT
USER user
# Mon, 18 Jul 2022 20:18:50 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:314cda9d0ef2282082d2bd0efd7659e0d9edb3ceae8e7919d990bcf95cbb3d2b`  
		Last Modified: Tue, 12 Jul 2022 01:12:37 GMT  
		Size: 26.6 MB (26560559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ca7959cb389c6a5178f433269da0b2c6c8474f8d44d9e40a3869ac96588d4d`  
		Last Modified: Tue, 12 Jul 2022 06:36:58 GMT  
		Size: 14.4 MB (14424292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976f86f89cadf992f0b4055818f123826998345af9b5f5940d0bc653a2427057`  
		Last Modified: Tue, 12 Jul 2022 06:36:43 GMT  
		Size: 4.2 KB (4188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419495c1f261eea969d0d2028dc1d47a5b2f7dd668f9f481a728a8b665085a0a`  
		Last Modified: Mon, 18 Jul 2022 20:20:19 GMT  
		Size: 4.2 MB (4187786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1.4` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:2d22ed2ec5237ace63ed06ac97c4d4a20e21c76708fadc56fc6c0a3962626605
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49603297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2913f649550379e0daaad94fb55a90e376e9be33556c8052e9d6460df2fad579`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:34 GMT
ADD file:f3a33075f4c3324c6a634ef37a1965ddd5606b4449c0f5909ce18eeb8268b612 in / 
# Tue, 12 Jul 2022 00:40:35 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 03:58:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 03:58:01 GMT
ENV HOME=/home/user
# Tue, 12 Jul 2022 03:58:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 12 Jul 2022 03:58:03 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 18:48:35 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 18:49:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dirmngr 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Mon, 18 Jul 2022 18:49:06 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 18:49:07 GMT
USER user
# Mon, 18 Jul 2022 18:49:08 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:60197a4c18d4b386d371cf39d01c48e98c357bba06da0b070a3c1f75006fd838`  
		Last Modified: Tue, 12 Jul 2022 00:46:13 GMT  
		Size: 30.1 MB (30054226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31d5df8c69c5980350d19a5ffb57504867950d6e5b8c3a6f11080af3e3a0c38`  
		Last Modified: Tue, 12 Jul 2022 03:59:16 GMT  
		Size: 15.4 MB (15377261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b76490db37eaebc94203a05f902096f75ed24cf7a086628cafc39dc7769bbf`  
		Last Modified: Tue, 12 Jul 2022 03:59:13 GMT  
		Size: 4.1 KB (4067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ccc8bb291efc3aa7242c0d8b4780541f2d9603daf68e756cdf6f635b29b4f4`  
		Last Modified: Mon, 18 Jul 2022 18:50:05 GMT  
		Size: 4.2 MB (4167743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1.4` - linux; 386

```console
$ docker pull irssi@sha256:6c4957ff125a55b1b7681b5dcff90a8b3038362e2a8e4153879db7a2be28b1c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51679954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50aea866fe6b1bbdd4191e840834c20db4a10eb7bd0c9578c2b83f18f0825eb0`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 02 Aug 2022 00:39:20 GMT
ADD file:f771e2286465694126158821089d801c7296376be2a56189e6041a15d2fe79f5 in / 
# Tue, 02 Aug 2022 00:39:21 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 03:10:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 03:10:20 GMT
ENV HOME=/home/user
# Tue, 02 Aug 2022 03:10:20 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 02 Aug 2022 03:10:21 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 03:10:22 GMT
ENV IRSSI_VERSION=1.4.2
# Tue, 02 Aug 2022 03:10:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dirmngr 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Tue, 02 Aug 2022 03:11:00 GMT
WORKDIR /home/user
# Tue, 02 Aug 2022 03:11:01 GMT
USER user
# Tue, 02 Aug 2022 03:11:02 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:90eb7f0ce9f33cf5dcd67d54c2fa606186dbaa5f95b6046f36145097267f9e53`  
		Last Modified: Tue, 02 Aug 2022 00:45:14 GMT  
		Size: 32.4 MB (32374054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e807876191c36c0343701cbf9f2866e857910c0bb70333fa34a0d8b7bc512b`  
		Last Modified: Tue, 02 Aug 2022 03:11:36 GMT  
		Size: 15.0 MB (15031673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e042e29265be416ef65d312aeebbf008b8a29b1ed9c1351486c336b91a11d4`  
		Last Modified: Tue, 02 Aug 2022 03:11:33 GMT  
		Size: 4.1 KB (4053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac3539df7150f2d647d38ae218b76d52ba34303d339bf960aa2fe6c5a8b441e`  
		Last Modified: Tue, 02 Aug 2022 03:11:33 GMT  
		Size: 4.3 MB (4270174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1.4` - linux; mips64le

```console
$ docker pull irssi@sha256:5e0bf0828437d767db40431686c24d975b9601b8360a8164074769d9d13c6acf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48617509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556eed7be91d94dbe25d160fa495d39f69c1add07bb664e33c473f458f9a3dd1`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 02 Aug 2022 01:10:34 GMT
ADD file:6dc22a1e5b5fcf23f2549406ddcc45c4e244f46e21eafa881de81fa87438e5d8 in / 
# Tue, 02 Aug 2022 01:10:38 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 03:17:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 03:17:38 GMT
ENV HOME=/home/user
# Tue, 02 Aug 2022 03:17:45 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 02 Aug 2022 03:17:48 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 03:17:51 GMT
ENV IRSSI_VERSION=1.4.2
# Tue, 02 Aug 2022 03:21:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dirmngr 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Tue, 02 Aug 2022 03:21:45 GMT
WORKDIR /home/user
# Tue, 02 Aug 2022 03:21:49 GMT
USER user
# Tue, 02 Aug 2022 03:21:52 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:88350749a27614c791450c256b051f023d81cdd256211274b1efac493779d2be`  
		Last Modified: Tue, 02 Aug 2022 01:21:02 GMT  
		Size: 29.6 MB (29628964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32415daee5708ee92f8f0d8cbb82cc3e0aba17931f1daa2fe19a06b38d6b4b3`  
		Last Modified: Tue, 02 Aug 2022 03:22:25 GMT  
		Size: 14.7 MB (14668257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31be73626d6aa213ab20d502e69c5545c4ef2147bcacdb751040c739cc9c28f`  
		Last Modified: Tue, 02 Aug 2022 03:22:11 GMT  
		Size: 4.1 KB (4066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848b6bffac840f3f64795049e1548ebc7769ce9475b3921d0cd85176dd664465`  
		Last Modified: Tue, 02 Aug 2022 03:22:15 GMT  
		Size: 4.3 MB (4316222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1.4` - linux; ppc64le

```console
$ docker pull irssi@sha256:a8e6205e8016bdc0cd109de6ed6e9d007b72c466be63523b492adeecc53f5433
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55758440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a96be9146d164ac0e9f7bfc663cc6e3e4d13b1d64bc9f0eef34643e6ac4eb72`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Jul 2022 01:25:28 GMT
ADD file:9e1afe48f40d94f879aefb12a7e68da2f0772d701e95b8219bd1f79a83e1933a in / 
# Tue, 12 Jul 2022 01:25:32 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 06:02:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 06:02:16 GMT
ENV HOME=/home/user
# Tue, 12 Jul 2022 06:02:24 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 12 Jul 2022 06:02:27 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 20:59:07 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 21:05:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dirmngr 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Mon, 18 Jul 2022 21:05:29 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 21:05:34 GMT
USER user
# Mon, 18 Jul 2022 21:05:39 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:bd3d68d1ce583727f6378a16916795b955cc0ad39e0ebe754a26007ef54744fa`  
		Last Modified: Tue, 12 Jul 2022 01:36:03 GMT  
		Size: 35.3 MB (35272500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39e75ba095c6987e0fca8686cbac241d72e4b34526b2312618405b4b0feba71`  
		Last Modified: Tue, 12 Jul 2022 06:07:46 GMT  
		Size: 15.8 MB (15797793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3029a04938ed8ac96ce82eea145146851d02beccd82d19f3af82573e0a00f41a`  
		Last Modified: Tue, 12 Jul 2022 06:07:41 GMT  
		Size: 4.2 KB (4216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3650334413d621df83d25ff4038e0c1ac603ce5ef7d064a444887e524b546e`  
		Last Modified: Mon, 18 Jul 2022 21:07:33 GMT  
		Size: 4.7 MB (4683931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1.4` - linux; s390x

```console
$ docker pull irssi@sha256:c664751349154e1ce063ab587bf63b9f363867f57ae9c1edb8da99dc42b3fe4a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50192142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2485b9e0e2067eb44ac6ef1a366099a1d3f9f29d553bfbe09dc44ef7dae829e`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 02 Aug 2022 00:42:27 GMT
ADD file:c2afc8990930846fbe7c99bfdfe9ea562c75feb6e3c9122431f7c9f8b5e51a7f in / 
# Tue, 02 Aug 2022 00:42:29 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 02:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 02:35:29 GMT
ENV HOME=/home/user
# Tue, 02 Aug 2022 02:35:30 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 02 Aug 2022 02:35:30 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 02:35:30 GMT
ENV IRSSI_VERSION=1.4.2
# Tue, 02 Aug 2022 02:35:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dirmngr 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Tue, 02 Aug 2022 02:35:57 GMT
WORKDIR /home/user
# Tue, 02 Aug 2022 02:35:57 GMT
USER user
# Tue, 02 Aug 2022 02:35:57 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:026d311d0716db60eba0572ea784c21031f420960510cebcc383dc53949b4db8`  
		Last Modified: Tue, 02 Aug 2022 00:48:01 GMT  
		Size: 29.6 MB (29640259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813471a33007d06aacc4cbaf7aff38415e1205c5fee4edd8e2c0f2bfebd0d8f2`  
		Last Modified: Tue, 02 Aug 2022 02:36:36 GMT  
		Size: 15.8 MB (15796925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecee3a36c2c868b4cf52323b6be62201a59b371d017e3336960cb20cb2ff679`  
		Last Modified: Tue, 02 Aug 2022 02:36:33 GMT  
		Size: 4.2 KB (4208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e622d653a1f908ca86a2ecd33d0381d0bcafee70c2badfa9733d02eca0a6901d`  
		Last Modified: Tue, 02 Aug 2022 02:36:33 GMT  
		Size: 4.8 MB (4750750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `irssi:1.4-alpine`

```console
$ docker pull irssi@sha256:854de1a51b99067ebb0100a67c6e13673d2fbdd5eb9a7b4b77484c65fc3cd0ad
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

### `irssi:1.4-alpine` - linux; amd64

```console
$ docker pull irssi@sha256:f3c10f861f7d988f12d99c084634ebbcaa0ee7554709b4cbeda8c0ffe5f7511e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17457462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f85f9670eee79491099fe67fa0e6ffc8d1f9222f94eac0129863c809506224`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 00:23:35 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Tue, 19 Jul 2022 00:23:35 GMT
ENV HOME=/home/user
# Tue, 19 Jul 2022 00:23:35 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 19 Jul 2022 00:23:36 GMT
ENV LANG=C.UTF-8
# Tue, 19 Jul 2022 00:23:36 GMT
ENV IRSSI_VERSION=1.4.2
# Tue, 19 Jul 2022 00:23:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Tue, 19 Jul 2022 00:23:58 GMT
WORKDIR /home/user
# Tue, 19 Jul 2022 00:23:58 GMT
USER user
# Tue, 19 Jul 2022 00:23:58 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b5bbd7de7a34116522b4918981e9d13d9f16810a588b74d764c886ca66f286`  
		Last Modified: Tue, 19 Jul 2022 00:24:16 GMT  
		Size: 9.6 MB (9635582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3125246c3b589cd814d841704f2635efc959d690c1baf7949f9bca0fdb5185a`  
		Last Modified: Tue, 19 Jul 2022 00:24:14 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912b4d23111a9384a40ebe73bb55898ab8cd45d79416b35411328fa809c814c0`  
		Last Modified: Tue, 19 Jul 2022 00:24:15 GMT  
		Size: 5.0 MB (5021792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1.4-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:3a494d4239afb464641516da33a1ac5641f0b315b22fa104eac28aa0a72f9c28
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16382978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb33fdc30a24d339ba9656ee8df90546bae6308ff1b070dcc65098a1ff78e4dc`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 Jul 2022 19:49:37 GMT
ADD file:7a20333469e71664904a0cb8f61613250f2bd092b4a27bfa7bbae1dc7e21b7ed in / 
# Mon, 18 Jul 2022 19:49:37 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 21:02:43 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 18 Jul 2022 21:02:44 GMT
ENV HOME=/home/user
# Mon, 18 Jul 2022 21:02:46 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 18 Jul 2022 21:02:46 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 21:02:46 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 21:03:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 18 Jul 2022 21:03:20 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 21:03:21 GMT
USER user
# Mon, 18 Jul 2022 21:03:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b7885075fcd06a866d12dfd56eb704045eaadbd22dc03a224cd98715be566677`  
		Last Modified: Mon, 18 Jul 2022 19:08:42 GMT  
		Size: 2.6 MB (2606431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead05fb861289a3112d85fde030e8569e9a7dc8dd23508fe65d82f88ee0b12a3`  
		Last Modified: Mon, 18 Jul 2022 21:04:05 GMT  
		Size: 8.9 MB (8861206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86cdcb4e11581d3551b521decf6e7d4a73ad09f615896b0723f46ed075ef77e2`  
		Last Modified: Mon, 18 Jul 2022 21:03:57 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5685ef9768727bd6b69beb5438e3f2f0dd1cc972b33dfe398ca9f2fc28a2e6c3`  
		Last Modified: Mon, 18 Jul 2022 21:04:01 GMT  
		Size: 4.9 MB (4914057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1.4-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:7726b670a7075eb493678469422e169667df6aab527e51cfaa879cda7f5062cc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15814593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64832f2b21baf5ec2006706a9cf25927c0a2a416d508ab5593ece2a7d00c258`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 Jul 2022 21:24:47 GMT
ADD file:68590e866bc6db27ad54d23de7dd275d0389cb86e4e6291a1243fcc234f2f7a1 in / 
# Mon, 18 Jul 2022 21:24:47 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 21:46:46 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 18 Jul 2022 21:46:47 GMT
ENV HOME=/home/user
# Mon, 18 Jul 2022 21:46:49 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 18 Jul 2022 21:46:49 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 21:46:50 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 21:47:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 18 Jul 2022 21:47:14 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 21:47:14 GMT
USER user
# Mon, 18 Jul 2022 21:47:14 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a6b45ace95f42a930d15c33679ab9c85d46019b7e73954cadc73bb9ba176509b`  
		Last Modified: Mon, 18 Jul 2022 19:08:56 GMT  
		Size: 2.4 MB (2412307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9e1dca7051a20a401a3d84f96da71dd867a9ee0e24f1a7f09677de75d53140`  
		Last Modified: Mon, 18 Jul 2022 21:48:15 GMT  
		Size: 8.7 MB (8708216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0f6db8c54d3924f3e78936c4066057027d8b3bd0a10af466cfc216a9ef6d2b`  
		Last Modified: Mon, 18 Jul 2022 21:48:07 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4987ffc8bc6cbb769df4dd941574de6d0a30766e1d35d371c5ed45aeba785b`  
		Last Modified: Mon, 18 Jul 2022 21:48:10 GMT  
		Size: 4.7 MB (4692786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1.4-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:564cd4be47c93fc2e03b800764ef11e1c27a4f37a56802df4197732fad9ae2e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17216500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf5779dbb8c59aa4f024dd254f360646e9a489a7ee967488d4de20260c03dc9`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:36:45 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 18 Jul 2022 23:36:45 GMT
ENV HOME=/home/user
# Mon, 18 Jul 2022 23:36:46 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 18 Jul 2022 23:36:47 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 23:36:48 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 23:37:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 18 Jul 2022 23:37:08 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 23:37:09 GMT
USER user
# Mon, 18 Jul 2022 23:37:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f97344484467e4c4ebb85aae724170073799295a3442c50ab532e249bd27b412`  
		Last Modified: Mon, 18 Jul 2022 19:08:29 GMT  
		Size: 2.7 MB (2694720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc9217fb4aa392f4d68e15e67a1738bdba81661d76ef27f98a859ca98fea7f4`  
		Last Modified: Mon, 18 Jul 2022 23:37:41 GMT  
		Size: 9.6 MB (9614190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c943cd07b898efc2d7524a805d91e8988448f4bfa1f9948493f1a885fd4e5e31`  
		Last Modified: Mon, 18 Jul 2022 23:37:39 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957ecc993dbe69ce704931a74e819999103ff7ed534556a71b5e62717f85f566`  
		Last Modified: Mon, 18 Jul 2022 23:37:40 GMT  
		Size: 4.9 MB (4906333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1.4-alpine` - linux; 386

```console
$ docker pull irssi@sha256:cb377bddeaa0f32f50bec41afb14efa635b8b275cd8dc27d29b9eb84278b07cd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16895156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89892b7d6a7e9cf4b9c20eaddfcfb4b60dfd2d3baf63e25ed682b85da30d9f9b`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 Jul 2022 20:38:19 GMT
ADD file:be69b7550bf861d8fb12bdbe1edf3a0d2519a6a4da61bd04858b6258ffbf48a7 in / 
# Mon, 18 Jul 2022 20:38:19 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 21:22:34 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 18 Jul 2022 21:22:34 GMT
ENV HOME=/home/user
# Mon, 18 Jul 2022 21:22:35 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 18 Jul 2022 21:22:36 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 21:22:37 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 21:22:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 18 Jul 2022 21:22:58 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 21:22:59 GMT
USER user
# Mon, 18 Jul 2022 21:23:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5d7f927419794ebb7496ac38b0659686317b2d2fac7252a4a0d40d43d5fdd662`  
		Last Modified: Mon, 18 Jul 2022 19:09:22 GMT  
		Size: 2.8 MB (2802334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2145e9491f9798ce6ba6a51e68ca96b186ad6ba788f3c69c1b1b154ad56a7e1a`  
		Last Modified: Mon, 18 Jul 2022 21:23:31 GMT  
		Size: 9.0 MB (8992480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d16a63cb4fb487e02f956e04140855533c28e2ee5e908cec5ea8a2468d6da3b`  
		Last Modified: Mon, 18 Jul 2022 21:23:29 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7d0ef11d7b29e8d2ec1207dc213657f05c112333cfe74b1e705a57a4df207e`  
		Last Modified: Mon, 18 Jul 2022 21:23:29 GMT  
		Size: 5.1 MB (5099084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1.4-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:008615550f0709646e4fcc911584d2d8aa1b24e8bdd0a7672eae582e45216607
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17626048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8fd78e65c7b8aabcd0fb57760ca1a6a2c764f73a4bd95fa6940cff225cff5d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 Jul 2022 21:29:30 GMT
ADD file:69e4080f15f54e2d8f8aa25fdcba9c01dde149d43592edd5023106675e54a769 in / 
# Mon, 18 Jul 2022 21:29:31 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:23:27 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 18 Jul 2022 23:23:30 GMT
ENV HOME=/home/user
# Mon, 18 Jul 2022 23:23:37 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 18 Jul 2022 23:23:39 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 23:23:43 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 23:24:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 18 Jul 2022 23:24:22 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 23:24:27 GMT
USER user
# Mon, 18 Jul 2022 23:24:29 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:602896d442490cd3fbb6599f0f862d3673b7cd58eca3ac842b8e09bf8d012443`  
		Last Modified: Mon, 18 Jul 2022 19:09:09 GMT  
		Size: 2.8 MB (2789923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144d51d6462d104bc78871a12553ef8ecb02c24118323022315248cbccbae669`  
		Last Modified: Mon, 18 Jul 2022 23:25:09 GMT  
		Size: 9.7 MB (9719919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52753540298a409bae5d1a612e5db8239226d77a43e088361efcd4fc867ba3b7`  
		Last Modified: Mon, 18 Jul 2022 23:25:07 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1043e272f851236c4dc571cd7e98077d260326039dff8d24a2b0640dad98a15`  
		Last Modified: Mon, 18 Jul 2022 23:25:08 GMT  
		Size: 5.1 MB (5114922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1.4-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:2f6ebdb305e5f2e8c4126dd0f9c56b6f10498a6782eaca868413a5181aed9820
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17667151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b91544b93d574c49f846ba8ca11d4857f02fb74183b9a821dcf03050801c6e8`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 Jul 2022 20:41:35 GMT
ADD file:deaa573cd61e07709846a5300fb627a8610e9754129c085ed483ff8897d0c002 in / 
# Mon, 18 Jul 2022 20:41:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 22:44:07 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 18 Jul 2022 22:44:10 GMT
ENV HOME=/home/user
# Mon, 18 Jul 2022 22:44:12 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 18 Jul 2022 22:44:13 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 22:44:14 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 22:45:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 18 Jul 2022 22:45:05 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 22:45:06 GMT
USER user
# Mon, 18 Jul 2022 22:45:06 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5f1840d5bacf4162a87f497e22d94bce946e660bdfce8eeefcbf7bd0beb193f3`  
		Last Modified: Mon, 18 Jul 2022 20:42:36 GMT  
		Size: 2.6 MB (2580798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df951ee246cfabbbcfb2dda7536db44d3a15ad885c57fb96e11b03ff3589094`  
		Last Modified: Mon, 18 Jul 2022 22:45:57 GMT  
		Size: 10.1 MB (10054683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d765c6e93fca15ebd173b5d15fd5fd709d4c8adc68967ced468eeb250bc472`  
		Last Modified: Mon, 18 Jul 2022 22:45:54 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a48b2916418ae80779b9c6f694ecce949d7d71adcddc0aa3f4bb2921a25a84`  
		Last Modified: Mon, 18 Jul 2022 22:45:56 GMT  
		Size: 5.0 MB (5030386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `irssi:1.4.2`

```console
$ docker pull irssi@sha256:6c1fac3ca2e9ecdabbc9187638b5106d56be577b5c60a5d3a1e2d1edb269c0f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `irssi:1.4.2` - linux; amd64

```console
$ docker pull irssi@sha256:4d0a57587f583ae57ba90633678591956501c95dbc1cd6703a8e8a4790577e2d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51343672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba512ed38aa173d1e69a89d5f49352ad0b61efaf7d3f7c542c627b03cdcfb0ef`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 04:33:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 04:33:52 GMT
ENV HOME=/home/user
# Tue, 12 Jul 2022 04:33:53 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 12 Jul 2022 04:33:53 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 19:31:00 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 19:31:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dirmngr 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Mon, 18 Jul 2022 19:31:39 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 19:31:39 GMT
USER user
# Mon, 18 Jul 2022 19:31:39 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:461246efe0a75316d99afdbf348f7063b57b0caeee8daab775f1f08152ea36f4`  
		Last Modified: Tue, 12 Jul 2022 01:24:34 GMT  
		Size: 31.4 MB (31366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e79e09cff439b97f521fe2a06f622f78563e7fa21992fac5121edd4d4cfdff7`  
		Last Modified: Tue, 12 Jul 2022 04:34:55 GMT  
		Size: 15.5 MB (15497990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de2a42942ce691111b16112e95781a9a4c0fad8e02d80fa30ad655226332107`  
		Last Modified: Tue, 12 Jul 2022 04:34:52 GMT  
		Size: 4.2 KB (4203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3a67937f3d44395a92dcfaabe40094a4d8fef1ba55683cdedea2d380c6d326`  
		Last Modified: Mon, 18 Jul 2022 19:32:29 GMT  
		Size: 4.5 MB (4474869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1.4.2` - linux; arm variant v5

```console
$ docker pull irssi@sha256:cbaecb7e5ce27a9f92f733f7d03bfc8b5a0a43ee3114f6bacafad16f03f8207a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47909536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ffc892412aa787e4af6555c04156ee5c4e13d354e8d87876b73144e97ea2954`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:10 GMT
ADD file:4cd2f95737fd3007912428eeac56036c9e67e989e66cec08a8be99da47f88494 in / 
# Tue, 02 Aug 2022 00:49:10 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:56:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:56:56 GMT
ENV HOME=/home/user
# Tue, 02 Aug 2022 01:56:57 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 02 Aug 2022 01:56:57 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 01:56:57 GMT
ENV IRSSI_VERSION=1.4.2
# Tue, 02 Aug 2022 01:57:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dirmngr 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Tue, 02 Aug 2022 01:57:52 GMT
WORKDIR /home/user
# Tue, 02 Aug 2022 01:57:52 GMT
USER user
# Tue, 02 Aug 2022 01:57:52 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5890b0ca6af5e8467a488e68716691950496a8f247d0495c2d595ddcb1893aff`  
		Last Modified: Tue, 02 Aug 2022 00:56:06 GMT  
		Size: 28.9 MB (28905515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b96885e167027fcb6391bfc0fda996e4c68280b656a669066fbca6ee32f57c`  
		Last Modified: Tue, 02 Aug 2022 01:58:20 GMT  
		Size: 14.7 MB (14674073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b78241a104470ed2f1128a082f2f65560bf86cf724fa5df219dbdf00d2faa0`  
		Last Modified: Tue, 02 Aug 2022 01:58:15 GMT  
		Size: 4.2 KB (4190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72eefd5a1fe1c338236141cea2f58baa3efd6d80e1d1c7043ed996e975a96ac`  
		Last Modified: Tue, 02 Aug 2022 01:58:16 GMT  
		Size: 4.3 MB (4325758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1.4.2` - linux; arm variant v7

```console
$ docker pull irssi@sha256:e921634c5488eab60d5f3bb71deaf4120a440291f0be93ee8379aba27b415e9f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45176825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f99154c23f142ad6e7a9f37ecd8062dceea9d74ff0edd51b490fc8e937b82ff`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Jul 2022 00:59:54 GMT
ADD file:ae890621b36ff6e27364bb7316b5bd4319a820ddf7e65565c6201eb11d70fde9 in / 
# Tue, 12 Jul 2022 00:59:55 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 06:34:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 06:34:28 GMT
ENV HOME=/home/user
# Tue, 12 Jul 2022 06:34:30 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 12 Jul 2022 06:34:30 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 20:17:40 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 20:18:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dirmngr 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Mon, 18 Jul 2022 20:18:49 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 20:18:49 GMT
USER user
# Mon, 18 Jul 2022 20:18:50 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:314cda9d0ef2282082d2bd0efd7659e0d9edb3ceae8e7919d990bcf95cbb3d2b`  
		Last Modified: Tue, 12 Jul 2022 01:12:37 GMT  
		Size: 26.6 MB (26560559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ca7959cb389c6a5178f433269da0b2c6c8474f8d44d9e40a3869ac96588d4d`  
		Last Modified: Tue, 12 Jul 2022 06:36:58 GMT  
		Size: 14.4 MB (14424292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976f86f89cadf992f0b4055818f123826998345af9b5f5940d0bc653a2427057`  
		Last Modified: Tue, 12 Jul 2022 06:36:43 GMT  
		Size: 4.2 KB (4188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419495c1f261eea969d0d2028dc1d47a5b2f7dd668f9f481a728a8b665085a0a`  
		Last Modified: Mon, 18 Jul 2022 20:20:19 GMT  
		Size: 4.2 MB (4187786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1.4.2` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:2d22ed2ec5237ace63ed06ac97c4d4a20e21c76708fadc56fc6c0a3962626605
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49603297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2913f649550379e0daaad94fb55a90e376e9be33556c8052e9d6460df2fad579`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:34 GMT
ADD file:f3a33075f4c3324c6a634ef37a1965ddd5606b4449c0f5909ce18eeb8268b612 in / 
# Tue, 12 Jul 2022 00:40:35 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 03:58:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 03:58:01 GMT
ENV HOME=/home/user
# Tue, 12 Jul 2022 03:58:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 12 Jul 2022 03:58:03 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 18:48:35 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 18:49:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dirmngr 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Mon, 18 Jul 2022 18:49:06 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 18:49:07 GMT
USER user
# Mon, 18 Jul 2022 18:49:08 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:60197a4c18d4b386d371cf39d01c48e98c357bba06da0b070a3c1f75006fd838`  
		Last Modified: Tue, 12 Jul 2022 00:46:13 GMT  
		Size: 30.1 MB (30054226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31d5df8c69c5980350d19a5ffb57504867950d6e5b8c3a6f11080af3e3a0c38`  
		Last Modified: Tue, 12 Jul 2022 03:59:16 GMT  
		Size: 15.4 MB (15377261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b76490db37eaebc94203a05f902096f75ed24cf7a086628cafc39dc7769bbf`  
		Last Modified: Tue, 12 Jul 2022 03:59:13 GMT  
		Size: 4.1 KB (4067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ccc8bb291efc3aa7242c0d8b4780541f2d9603daf68e756cdf6f635b29b4f4`  
		Last Modified: Mon, 18 Jul 2022 18:50:05 GMT  
		Size: 4.2 MB (4167743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1.4.2` - linux; 386

```console
$ docker pull irssi@sha256:6c4957ff125a55b1b7681b5dcff90a8b3038362e2a8e4153879db7a2be28b1c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51679954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50aea866fe6b1bbdd4191e840834c20db4a10eb7bd0c9578c2b83f18f0825eb0`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 02 Aug 2022 00:39:20 GMT
ADD file:f771e2286465694126158821089d801c7296376be2a56189e6041a15d2fe79f5 in / 
# Tue, 02 Aug 2022 00:39:21 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 03:10:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 03:10:20 GMT
ENV HOME=/home/user
# Tue, 02 Aug 2022 03:10:20 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 02 Aug 2022 03:10:21 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 03:10:22 GMT
ENV IRSSI_VERSION=1.4.2
# Tue, 02 Aug 2022 03:10:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dirmngr 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Tue, 02 Aug 2022 03:11:00 GMT
WORKDIR /home/user
# Tue, 02 Aug 2022 03:11:01 GMT
USER user
# Tue, 02 Aug 2022 03:11:02 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:90eb7f0ce9f33cf5dcd67d54c2fa606186dbaa5f95b6046f36145097267f9e53`  
		Last Modified: Tue, 02 Aug 2022 00:45:14 GMT  
		Size: 32.4 MB (32374054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e807876191c36c0343701cbf9f2866e857910c0bb70333fa34a0d8b7bc512b`  
		Last Modified: Tue, 02 Aug 2022 03:11:36 GMT  
		Size: 15.0 MB (15031673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e042e29265be416ef65d312aeebbf008b8a29b1ed9c1351486c336b91a11d4`  
		Last Modified: Tue, 02 Aug 2022 03:11:33 GMT  
		Size: 4.1 KB (4053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac3539df7150f2d647d38ae218b76d52ba34303d339bf960aa2fe6c5a8b441e`  
		Last Modified: Tue, 02 Aug 2022 03:11:33 GMT  
		Size: 4.3 MB (4270174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1.4.2` - linux; mips64le

```console
$ docker pull irssi@sha256:5e0bf0828437d767db40431686c24d975b9601b8360a8164074769d9d13c6acf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48617509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556eed7be91d94dbe25d160fa495d39f69c1add07bb664e33c473f458f9a3dd1`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 02 Aug 2022 01:10:34 GMT
ADD file:6dc22a1e5b5fcf23f2549406ddcc45c4e244f46e21eafa881de81fa87438e5d8 in / 
# Tue, 02 Aug 2022 01:10:38 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 03:17:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 03:17:38 GMT
ENV HOME=/home/user
# Tue, 02 Aug 2022 03:17:45 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 02 Aug 2022 03:17:48 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 03:17:51 GMT
ENV IRSSI_VERSION=1.4.2
# Tue, 02 Aug 2022 03:21:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dirmngr 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Tue, 02 Aug 2022 03:21:45 GMT
WORKDIR /home/user
# Tue, 02 Aug 2022 03:21:49 GMT
USER user
# Tue, 02 Aug 2022 03:21:52 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:88350749a27614c791450c256b051f023d81cdd256211274b1efac493779d2be`  
		Last Modified: Tue, 02 Aug 2022 01:21:02 GMT  
		Size: 29.6 MB (29628964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32415daee5708ee92f8f0d8cbb82cc3e0aba17931f1daa2fe19a06b38d6b4b3`  
		Last Modified: Tue, 02 Aug 2022 03:22:25 GMT  
		Size: 14.7 MB (14668257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31be73626d6aa213ab20d502e69c5545c4ef2147bcacdb751040c739cc9c28f`  
		Last Modified: Tue, 02 Aug 2022 03:22:11 GMT  
		Size: 4.1 KB (4066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848b6bffac840f3f64795049e1548ebc7769ce9475b3921d0cd85176dd664465`  
		Last Modified: Tue, 02 Aug 2022 03:22:15 GMT  
		Size: 4.3 MB (4316222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1.4.2` - linux; ppc64le

```console
$ docker pull irssi@sha256:a8e6205e8016bdc0cd109de6ed6e9d007b72c466be63523b492adeecc53f5433
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55758440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a96be9146d164ac0e9f7bfc663cc6e3e4d13b1d64bc9f0eef34643e6ac4eb72`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Jul 2022 01:25:28 GMT
ADD file:9e1afe48f40d94f879aefb12a7e68da2f0772d701e95b8219bd1f79a83e1933a in / 
# Tue, 12 Jul 2022 01:25:32 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 06:02:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 06:02:16 GMT
ENV HOME=/home/user
# Tue, 12 Jul 2022 06:02:24 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 12 Jul 2022 06:02:27 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 20:59:07 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 21:05:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dirmngr 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Mon, 18 Jul 2022 21:05:29 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 21:05:34 GMT
USER user
# Mon, 18 Jul 2022 21:05:39 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:bd3d68d1ce583727f6378a16916795b955cc0ad39e0ebe754a26007ef54744fa`  
		Last Modified: Tue, 12 Jul 2022 01:36:03 GMT  
		Size: 35.3 MB (35272500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39e75ba095c6987e0fca8686cbac241d72e4b34526b2312618405b4b0feba71`  
		Last Modified: Tue, 12 Jul 2022 06:07:46 GMT  
		Size: 15.8 MB (15797793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3029a04938ed8ac96ce82eea145146851d02beccd82d19f3af82573e0a00f41a`  
		Last Modified: Tue, 12 Jul 2022 06:07:41 GMT  
		Size: 4.2 KB (4216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3650334413d621df83d25ff4038e0c1ac603ce5ef7d064a444887e524b546e`  
		Last Modified: Mon, 18 Jul 2022 21:07:33 GMT  
		Size: 4.7 MB (4683931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1.4.2` - linux; s390x

```console
$ docker pull irssi@sha256:c664751349154e1ce063ab587bf63b9f363867f57ae9c1edb8da99dc42b3fe4a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50192142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2485b9e0e2067eb44ac6ef1a366099a1d3f9f29d553bfbe09dc44ef7dae829e`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 02 Aug 2022 00:42:27 GMT
ADD file:c2afc8990930846fbe7c99bfdfe9ea562c75feb6e3c9122431f7c9f8b5e51a7f in / 
# Tue, 02 Aug 2022 00:42:29 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 02:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 02:35:29 GMT
ENV HOME=/home/user
# Tue, 02 Aug 2022 02:35:30 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 02 Aug 2022 02:35:30 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 02:35:30 GMT
ENV IRSSI_VERSION=1.4.2
# Tue, 02 Aug 2022 02:35:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dirmngr 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Tue, 02 Aug 2022 02:35:57 GMT
WORKDIR /home/user
# Tue, 02 Aug 2022 02:35:57 GMT
USER user
# Tue, 02 Aug 2022 02:35:57 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:026d311d0716db60eba0572ea784c21031f420960510cebcc383dc53949b4db8`  
		Last Modified: Tue, 02 Aug 2022 00:48:01 GMT  
		Size: 29.6 MB (29640259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813471a33007d06aacc4cbaf7aff38415e1205c5fee4edd8e2c0f2bfebd0d8f2`  
		Last Modified: Tue, 02 Aug 2022 02:36:36 GMT  
		Size: 15.8 MB (15796925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecee3a36c2c868b4cf52323b6be62201a59b371d017e3336960cb20cb2ff679`  
		Last Modified: Tue, 02 Aug 2022 02:36:33 GMT  
		Size: 4.2 KB (4208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e622d653a1f908ca86a2ecd33d0381d0bcafee70c2badfa9733d02eca0a6901d`  
		Last Modified: Tue, 02 Aug 2022 02:36:33 GMT  
		Size: 4.8 MB (4750750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `irssi:1.4.2-alpine`

```console
$ docker pull irssi@sha256:854de1a51b99067ebb0100a67c6e13673d2fbdd5eb9a7b4b77484c65fc3cd0ad
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

### `irssi:1.4.2-alpine` - linux; amd64

```console
$ docker pull irssi@sha256:f3c10f861f7d988f12d99c084634ebbcaa0ee7554709b4cbeda8c0ffe5f7511e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17457462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f85f9670eee79491099fe67fa0e6ffc8d1f9222f94eac0129863c809506224`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 00:23:35 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Tue, 19 Jul 2022 00:23:35 GMT
ENV HOME=/home/user
# Tue, 19 Jul 2022 00:23:35 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 19 Jul 2022 00:23:36 GMT
ENV LANG=C.UTF-8
# Tue, 19 Jul 2022 00:23:36 GMT
ENV IRSSI_VERSION=1.4.2
# Tue, 19 Jul 2022 00:23:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Tue, 19 Jul 2022 00:23:58 GMT
WORKDIR /home/user
# Tue, 19 Jul 2022 00:23:58 GMT
USER user
# Tue, 19 Jul 2022 00:23:58 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b5bbd7de7a34116522b4918981e9d13d9f16810a588b74d764c886ca66f286`  
		Last Modified: Tue, 19 Jul 2022 00:24:16 GMT  
		Size: 9.6 MB (9635582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3125246c3b589cd814d841704f2635efc959d690c1baf7949f9bca0fdb5185a`  
		Last Modified: Tue, 19 Jul 2022 00:24:14 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912b4d23111a9384a40ebe73bb55898ab8cd45d79416b35411328fa809c814c0`  
		Last Modified: Tue, 19 Jul 2022 00:24:15 GMT  
		Size: 5.0 MB (5021792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1.4.2-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:3a494d4239afb464641516da33a1ac5641f0b315b22fa104eac28aa0a72f9c28
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16382978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb33fdc30a24d339ba9656ee8df90546bae6308ff1b070dcc65098a1ff78e4dc`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 Jul 2022 19:49:37 GMT
ADD file:7a20333469e71664904a0cb8f61613250f2bd092b4a27bfa7bbae1dc7e21b7ed in / 
# Mon, 18 Jul 2022 19:49:37 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 21:02:43 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 18 Jul 2022 21:02:44 GMT
ENV HOME=/home/user
# Mon, 18 Jul 2022 21:02:46 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 18 Jul 2022 21:02:46 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 21:02:46 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 21:03:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 18 Jul 2022 21:03:20 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 21:03:21 GMT
USER user
# Mon, 18 Jul 2022 21:03:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b7885075fcd06a866d12dfd56eb704045eaadbd22dc03a224cd98715be566677`  
		Last Modified: Mon, 18 Jul 2022 19:08:42 GMT  
		Size: 2.6 MB (2606431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead05fb861289a3112d85fde030e8569e9a7dc8dd23508fe65d82f88ee0b12a3`  
		Last Modified: Mon, 18 Jul 2022 21:04:05 GMT  
		Size: 8.9 MB (8861206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86cdcb4e11581d3551b521decf6e7d4a73ad09f615896b0723f46ed075ef77e2`  
		Last Modified: Mon, 18 Jul 2022 21:03:57 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5685ef9768727bd6b69beb5438e3f2f0dd1cc972b33dfe398ca9f2fc28a2e6c3`  
		Last Modified: Mon, 18 Jul 2022 21:04:01 GMT  
		Size: 4.9 MB (4914057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1.4.2-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:7726b670a7075eb493678469422e169667df6aab527e51cfaa879cda7f5062cc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15814593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64832f2b21baf5ec2006706a9cf25927c0a2a416d508ab5593ece2a7d00c258`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 Jul 2022 21:24:47 GMT
ADD file:68590e866bc6db27ad54d23de7dd275d0389cb86e4e6291a1243fcc234f2f7a1 in / 
# Mon, 18 Jul 2022 21:24:47 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 21:46:46 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 18 Jul 2022 21:46:47 GMT
ENV HOME=/home/user
# Mon, 18 Jul 2022 21:46:49 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 18 Jul 2022 21:46:49 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 21:46:50 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 21:47:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 18 Jul 2022 21:47:14 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 21:47:14 GMT
USER user
# Mon, 18 Jul 2022 21:47:14 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a6b45ace95f42a930d15c33679ab9c85d46019b7e73954cadc73bb9ba176509b`  
		Last Modified: Mon, 18 Jul 2022 19:08:56 GMT  
		Size: 2.4 MB (2412307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9e1dca7051a20a401a3d84f96da71dd867a9ee0e24f1a7f09677de75d53140`  
		Last Modified: Mon, 18 Jul 2022 21:48:15 GMT  
		Size: 8.7 MB (8708216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0f6db8c54d3924f3e78936c4066057027d8b3bd0a10af466cfc216a9ef6d2b`  
		Last Modified: Mon, 18 Jul 2022 21:48:07 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4987ffc8bc6cbb769df4dd941574de6d0a30766e1d35d371c5ed45aeba785b`  
		Last Modified: Mon, 18 Jul 2022 21:48:10 GMT  
		Size: 4.7 MB (4692786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1.4.2-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:564cd4be47c93fc2e03b800764ef11e1c27a4f37a56802df4197732fad9ae2e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17216500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf5779dbb8c59aa4f024dd254f360646e9a489a7ee967488d4de20260c03dc9`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:36:45 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 18 Jul 2022 23:36:45 GMT
ENV HOME=/home/user
# Mon, 18 Jul 2022 23:36:46 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 18 Jul 2022 23:36:47 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 23:36:48 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 23:37:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 18 Jul 2022 23:37:08 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 23:37:09 GMT
USER user
# Mon, 18 Jul 2022 23:37:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f97344484467e4c4ebb85aae724170073799295a3442c50ab532e249bd27b412`  
		Last Modified: Mon, 18 Jul 2022 19:08:29 GMT  
		Size: 2.7 MB (2694720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc9217fb4aa392f4d68e15e67a1738bdba81661d76ef27f98a859ca98fea7f4`  
		Last Modified: Mon, 18 Jul 2022 23:37:41 GMT  
		Size: 9.6 MB (9614190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c943cd07b898efc2d7524a805d91e8988448f4bfa1f9948493f1a885fd4e5e31`  
		Last Modified: Mon, 18 Jul 2022 23:37:39 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957ecc993dbe69ce704931a74e819999103ff7ed534556a71b5e62717f85f566`  
		Last Modified: Mon, 18 Jul 2022 23:37:40 GMT  
		Size: 4.9 MB (4906333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1.4.2-alpine` - linux; 386

```console
$ docker pull irssi@sha256:cb377bddeaa0f32f50bec41afb14efa635b8b275cd8dc27d29b9eb84278b07cd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16895156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89892b7d6a7e9cf4b9c20eaddfcfb4b60dfd2d3baf63e25ed682b85da30d9f9b`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 Jul 2022 20:38:19 GMT
ADD file:be69b7550bf861d8fb12bdbe1edf3a0d2519a6a4da61bd04858b6258ffbf48a7 in / 
# Mon, 18 Jul 2022 20:38:19 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 21:22:34 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 18 Jul 2022 21:22:34 GMT
ENV HOME=/home/user
# Mon, 18 Jul 2022 21:22:35 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 18 Jul 2022 21:22:36 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 21:22:37 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 21:22:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 18 Jul 2022 21:22:58 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 21:22:59 GMT
USER user
# Mon, 18 Jul 2022 21:23:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5d7f927419794ebb7496ac38b0659686317b2d2fac7252a4a0d40d43d5fdd662`  
		Last Modified: Mon, 18 Jul 2022 19:09:22 GMT  
		Size: 2.8 MB (2802334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2145e9491f9798ce6ba6a51e68ca96b186ad6ba788f3c69c1b1b154ad56a7e1a`  
		Last Modified: Mon, 18 Jul 2022 21:23:31 GMT  
		Size: 9.0 MB (8992480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d16a63cb4fb487e02f956e04140855533c28e2ee5e908cec5ea8a2468d6da3b`  
		Last Modified: Mon, 18 Jul 2022 21:23:29 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7d0ef11d7b29e8d2ec1207dc213657f05c112333cfe74b1e705a57a4df207e`  
		Last Modified: Mon, 18 Jul 2022 21:23:29 GMT  
		Size: 5.1 MB (5099084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1.4.2-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:008615550f0709646e4fcc911584d2d8aa1b24e8bdd0a7672eae582e45216607
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17626048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8fd78e65c7b8aabcd0fb57760ca1a6a2c764f73a4bd95fa6940cff225cff5d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 Jul 2022 21:29:30 GMT
ADD file:69e4080f15f54e2d8f8aa25fdcba9c01dde149d43592edd5023106675e54a769 in / 
# Mon, 18 Jul 2022 21:29:31 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:23:27 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 18 Jul 2022 23:23:30 GMT
ENV HOME=/home/user
# Mon, 18 Jul 2022 23:23:37 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 18 Jul 2022 23:23:39 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 23:23:43 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 23:24:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 18 Jul 2022 23:24:22 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 23:24:27 GMT
USER user
# Mon, 18 Jul 2022 23:24:29 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:602896d442490cd3fbb6599f0f862d3673b7cd58eca3ac842b8e09bf8d012443`  
		Last Modified: Mon, 18 Jul 2022 19:09:09 GMT  
		Size: 2.8 MB (2789923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144d51d6462d104bc78871a12553ef8ecb02c24118323022315248cbccbae669`  
		Last Modified: Mon, 18 Jul 2022 23:25:09 GMT  
		Size: 9.7 MB (9719919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52753540298a409bae5d1a612e5db8239226d77a43e088361efcd4fc867ba3b7`  
		Last Modified: Mon, 18 Jul 2022 23:25:07 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1043e272f851236c4dc571cd7e98077d260326039dff8d24a2b0640dad98a15`  
		Last Modified: Mon, 18 Jul 2022 23:25:08 GMT  
		Size: 5.1 MB (5114922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:1.4.2-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:2f6ebdb305e5f2e8c4126dd0f9c56b6f10498a6782eaca868413a5181aed9820
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17667151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b91544b93d574c49f846ba8ca11d4857f02fb74183b9a821dcf03050801c6e8`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 Jul 2022 20:41:35 GMT
ADD file:deaa573cd61e07709846a5300fb627a8610e9754129c085ed483ff8897d0c002 in / 
# Mon, 18 Jul 2022 20:41:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 22:44:07 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 18 Jul 2022 22:44:10 GMT
ENV HOME=/home/user
# Mon, 18 Jul 2022 22:44:12 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 18 Jul 2022 22:44:13 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 22:44:14 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 22:45:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 18 Jul 2022 22:45:05 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 22:45:06 GMT
USER user
# Mon, 18 Jul 2022 22:45:06 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5f1840d5bacf4162a87f497e22d94bce946e660bdfce8eeefcbf7bd0beb193f3`  
		Last Modified: Mon, 18 Jul 2022 20:42:36 GMT  
		Size: 2.6 MB (2580798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df951ee246cfabbbcfb2dda7536db44d3a15ad885c57fb96e11b03ff3589094`  
		Last Modified: Mon, 18 Jul 2022 22:45:57 GMT  
		Size: 10.1 MB (10054683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d765c6e93fca15ebd173b5d15fd5fd709d4c8adc68967ced468eeb250bc472`  
		Last Modified: Mon, 18 Jul 2022 22:45:54 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a48b2916418ae80779b9c6f694ecce949d7d71adcddc0aa3f4bb2921a25a84`  
		Last Modified: Mon, 18 Jul 2022 22:45:56 GMT  
		Size: 5.0 MB (5030386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `irssi:alpine`

```console
$ docker pull irssi@sha256:854de1a51b99067ebb0100a67c6e13673d2fbdd5eb9a7b4b77484c65fc3cd0ad
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
$ docker pull irssi@sha256:f3c10f861f7d988f12d99c084634ebbcaa0ee7554709b4cbeda8c0ffe5f7511e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17457462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f85f9670eee79491099fe67fa0e6ffc8d1f9222f94eac0129863c809506224`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 00:23:35 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Tue, 19 Jul 2022 00:23:35 GMT
ENV HOME=/home/user
# Tue, 19 Jul 2022 00:23:35 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 19 Jul 2022 00:23:36 GMT
ENV LANG=C.UTF-8
# Tue, 19 Jul 2022 00:23:36 GMT
ENV IRSSI_VERSION=1.4.2
# Tue, 19 Jul 2022 00:23:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Tue, 19 Jul 2022 00:23:58 GMT
WORKDIR /home/user
# Tue, 19 Jul 2022 00:23:58 GMT
USER user
# Tue, 19 Jul 2022 00:23:58 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b5bbd7de7a34116522b4918981e9d13d9f16810a588b74d764c886ca66f286`  
		Last Modified: Tue, 19 Jul 2022 00:24:16 GMT  
		Size: 9.6 MB (9635582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3125246c3b589cd814d841704f2635efc959d690c1baf7949f9bca0fdb5185a`  
		Last Modified: Tue, 19 Jul 2022 00:24:14 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912b4d23111a9384a40ebe73bb55898ab8cd45d79416b35411328fa809c814c0`  
		Last Modified: Tue, 19 Jul 2022 00:24:15 GMT  
		Size: 5.0 MB (5021792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:3a494d4239afb464641516da33a1ac5641f0b315b22fa104eac28aa0a72f9c28
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16382978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb33fdc30a24d339ba9656ee8df90546bae6308ff1b070dcc65098a1ff78e4dc`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 Jul 2022 19:49:37 GMT
ADD file:7a20333469e71664904a0cb8f61613250f2bd092b4a27bfa7bbae1dc7e21b7ed in / 
# Mon, 18 Jul 2022 19:49:37 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 21:02:43 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 18 Jul 2022 21:02:44 GMT
ENV HOME=/home/user
# Mon, 18 Jul 2022 21:02:46 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 18 Jul 2022 21:02:46 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 21:02:46 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 21:03:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 18 Jul 2022 21:03:20 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 21:03:21 GMT
USER user
# Mon, 18 Jul 2022 21:03:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b7885075fcd06a866d12dfd56eb704045eaadbd22dc03a224cd98715be566677`  
		Last Modified: Mon, 18 Jul 2022 19:08:42 GMT  
		Size: 2.6 MB (2606431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead05fb861289a3112d85fde030e8569e9a7dc8dd23508fe65d82f88ee0b12a3`  
		Last Modified: Mon, 18 Jul 2022 21:04:05 GMT  
		Size: 8.9 MB (8861206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86cdcb4e11581d3551b521decf6e7d4a73ad09f615896b0723f46ed075ef77e2`  
		Last Modified: Mon, 18 Jul 2022 21:03:57 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5685ef9768727bd6b69beb5438e3f2f0dd1cc972b33dfe398ca9f2fc28a2e6c3`  
		Last Modified: Mon, 18 Jul 2022 21:04:01 GMT  
		Size: 4.9 MB (4914057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:7726b670a7075eb493678469422e169667df6aab527e51cfaa879cda7f5062cc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15814593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64832f2b21baf5ec2006706a9cf25927c0a2a416d508ab5593ece2a7d00c258`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 Jul 2022 21:24:47 GMT
ADD file:68590e866bc6db27ad54d23de7dd275d0389cb86e4e6291a1243fcc234f2f7a1 in / 
# Mon, 18 Jul 2022 21:24:47 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 21:46:46 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 18 Jul 2022 21:46:47 GMT
ENV HOME=/home/user
# Mon, 18 Jul 2022 21:46:49 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 18 Jul 2022 21:46:49 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 21:46:50 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 21:47:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 18 Jul 2022 21:47:14 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 21:47:14 GMT
USER user
# Mon, 18 Jul 2022 21:47:14 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a6b45ace95f42a930d15c33679ab9c85d46019b7e73954cadc73bb9ba176509b`  
		Last Modified: Mon, 18 Jul 2022 19:08:56 GMT  
		Size: 2.4 MB (2412307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9e1dca7051a20a401a3d84f96da71dd867a9ee0e24f1a7f09677de75d53140`  
		Last Modified: Mon, 18 Jul 2022 21:48:15 GMT  
		Size: 8.7 MB (8708216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0f6db8c54d3924f3e78936c4066057027d8b3bd0a10af466cfc216a9ef6d2b`  
		Last Modified: Mon, 18 Jul 2022 21:48:07 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4987ffc8bc6cbb769df4dd941574de6d0a30766e1d35d371c5ed45aeba785b`  
		Last Modified: Mon, 18 Jul 2022 21:48:10 GMT  
		Size: 4.7 MB (4692786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:564cd4be47c93fc2e03b800764ef11e1c27a4f37a56802df4197732fad9ae2e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17216500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf5779dbb8c59aa4f024dd254f360646e9a489a7ee967488d4de20260c03dc9`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:36:45 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 18 Jul 2022 23:36:45 GMT
ENV HOME=/home/user
# Mon, 18 Jul 2022 23:36:46 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 18 Jul 2022 23:36:47 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 23:36:48 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 23:37:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 18 Jul 2022 23:37:08 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 23:37:09 GMT
USER user
# Mon, 18 Jul 2022 23:37:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f97344484467e4c4ebb85aae724170073799295a3442c50ab532e249bd27b412`  
		Last Modified: Mon, 18 Jul 2022 19:08:29 GMT  
		Size: 2.7 MB (2694720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc9217fb4aa392f4d68e15e67a1738bdba81661d76ef27f98a859ca98fea7f4`  
		Last Modified: Mon, 18 Jul 2022 23:37:41 GMT  
		Size: 9.6 MB (9614190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c943cd07b898efc2d7524a805d91e8988448f4bfa1f9948493f1a885fd4e5e31`  
		Last Modified: Mon, 18 Jul 2022 23:37:39 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957ecc993dbe69ce704931a74e819999103ff7ed534556a71b5e62717f85f566`  
		Last Modified: Mon, 18 Jul 2022 23:37:40 GMT  
		Size: 4.9 MB (4906333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; 386

```console
$ docker pull irssi@sha256:cb377bddeaa0f32f50bec41afb14efa635b8b275cd8dc27d29b9eb84278b07cd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16895156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89892b7d6a7e9cf4b9c20eaddfcfb4b60dfd2d3baf63e25ed682b85da30d9f9b`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 Jul 2022 20:38:19 GMT
ADD file:be69b7550bf861d8fb12bdbe1edf3a0d2519a6a4da61bd04858b6258ffbf48a7 in / 
# Mon, 18 Jul 2022 20:38:19 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 21:22:34 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 18 Jul 2022 21:22:34 GMT
ENV HOME=/home/user
# Mon, 18 Jul 2022 21:22:35 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 18 Jul 2022 21:22:36 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 21:22:37 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 21:22:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 18 Jul 2022 21:22:58 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 21:22:59 GMT
USER user
# Mon, 18 Jul 2022 21:23:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5d7f927419794ebb7496ac38b0659686317b2d2fac7252a4a0d40d43d5fdd662`  
		Last Modified: Mon, 18 Jul 2022 19:09:22 GMT  
		Size: 2.8 MB (2802334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2145e9491f9798ce6ba6a51e68ca96b186ad6ba788f3c69c1b1b154ad56a7e1a`  
		Last Modified: Mon, 18 Jul 2022 21:23:31 GMT  
		Size: 9.0 MB (8992480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d16a63cb4fb487e02f956e04140855533c28e2ee5e908cec5ea8a2468d6da3b`  
		Last Modified: Mon, 18 Jul 2022 21:23:29 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7d0ef11d7b29e8d2ec1207dc213657f05c112333cfe74b1e705a57a4df207e`  
		Last Modified: Mon, 18 Jul 2022 21:23:29 GMT  
		Size: 5.1 MB (5099084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:008615550f0709646e4fcc911584d2d8aa1b24e8bdd0a7672eae582e45216607
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17626048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8fd78e65c7b8aabcd0fb57760ca1a6a2c764f73a4bd95fa6940cff225cff5d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 Jul 2022 21:29:30 GMT
ADD file:69e4080f15f54e2d8f8aa25fdcba9c01dde149d43592edd5023106675e54a769 in / 
# Mon, 18 Jul 2022 21:29:31 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:23:27 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 18 Jul 2022 23:23:30 GMT
ENV HOME=/home/user
# Mon, 18 Jul 2022 23:23:37 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 18 Jul 2022 23:23:39 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 23:23:43 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 23:24:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 18 Jul 2022 23:24:22 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 23:24:27 GMT
USER user
# Mon, 18 Jul 2022 23:24:29 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:602896d442490cd3fbb6599f0f862d3673b7cd58eca3ac842b8e09bf8d012443`  
		Last Modified: Mon, 18 Jul 2022 19:09:09 GMT  
		Size: 2.8 MB (2789923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144d51d6462d104bc78871a12553ef8ecb02c24118323022315248cbccbae669`  
		Last Modified: Mon, 18 Jul 2022 23:25:09 GMT  
		Size: 9.7 MB (9719919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52753540298a409bae5d1a612e5db8239226d77a43e088361efcd4fc867ba3b7`  
		Last Modified: Mon, 18 Jul 2022 23:25:07 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1043e272f851236c4dc571cd7e98077d260326039dff8d24a2b0640dad98a15`  
		Last Modified: Mon, 18 Jul 2022 23:25:08 GMT  
		Size: 5.1 MB (5114922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:alpine` - linux; s390x

```console
$ docker pull irssi@sha256:2f6ebdb305e5f2e8c4126dd0f9c56b6f10498a6782eaca868413a5181aed9820
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17667151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b91544b93d574c49f846ba8ca11d4857f02fb74183b9a821dcf03050801c6e8`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 Jul 2022 20:41:35 GMT
ADD file:deaa573cd61e07709846a5300fb627a8610e9754129c085ed483ff8897d0c002 in / 
# Mon, 18 Jul 2022 20:41:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 22:44:07 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww
# Mon, 18 Jul 2022 22:44:10 GMT
ENV HOME=/home/user
# Mon, 18 Jul 2022 22:44:12 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Mon, 18 Jul 2022 22:44:13 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 22:44:14 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 22:45:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version
# Mon, 18 Jul 2022 22:45:05 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 22:45:06 GMT
USER user
# Mon, 18 Jul 2022 22:45:06 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5f1840d5bacf4162a87f497e22d94bce946e660bdfce8eeefcbf7bd0beb193f3`  
		Last Modified: Mon, 18 Jul 2022 20:42:36 GMT  
		Size: 2.6 MB (2580798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df951ee246cfabbbcfb2dda7536db44d3a15ad885c57fb96e11b03ff3589094`  
		Last Modified: Mon, 18 Jul 2022 22:45:57 GMT  
		Size: 10.1 MB (10054683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d765c6e93fca15ebd173b5d15fd5fd709d4c8adc68967ced468eeb250bc472`  
		Last Modified: Mon, 18 Jul 2022 22:45:54 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a48b2916418ae80779b9c6f694ecce949d7d71adcddc0aa3f4bb2921a25a84`  
		Last Modified: Mon, 18 Jul 2022 22:45:56 GMT  
		Size: 5.0 MB (5030386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `irssi:latest`

```console
$ docker pull irssi@sha256:6c1fac3ca2e9ecdabbc9187638b5106d56be577b5c60a5d3a1e2d1edb269c0f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `irssi:latest` - linux; amd64

```console
$ docker pull irssi@sha256:4d0a57587f583ae57ba90633678591956501c95dbc1cd6703a8e8a4790577e2d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51343672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba512ed38aa173d1e69a89d5f49352ad0b61efaf7d3f7c542c627b03cdcfb0ef`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 04:33:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 04:33:52 GMT
ENV HOME=/home/user
# Tue, 12 Jul 2022 04:33:53 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 12 Jul 2022 04:33:53 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 19:31:00 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 19:31:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dirmngr 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Mon, 18 Jul 2022 19:31:39 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 19:31:39 GMT
USER user
# Mon, 18 Jul 2022 19:31:39 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:461246efe0a75316d99afdbf348f7063b57b0caeee8daab775f1f08152ea36f4`  
		Last Modified: Tue, 12 Jul 2022 01:24:34 GMT  
		Size: 31.4 MB (31366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e79e09cff439b97f521fe2a06f622f78563e7fa21992fac5121edd4d4cfdff7`  
		Last Modified: Tue, 12 Jul 2022 04:34:55 GMT  
		Size: 15.5 MB (15497990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de2a42942ce691111b16112e95781a9a4c0fad8e02d80fa30ad655226332107`  
		Last Modified: Tue, 12 Jul 2022 04:34:52 GMT  
		Size: 4.2 KB (4203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3a67937f3d44395a92dcfaabe40094a4d8fef1ba55683cdedea2d380c6d326`  
		Last Modified: Mon, 18 Jul 2022 19:32:29 GMT  
		Size: 4.5 MB (4474869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:latest` - linux; arm variant v5

```console
$ docker pull irssi@sha256:cbaecb7e5ce27a9f92f733f7d03bfc8b5a0a43ee3114f6bacafad16f03f8207a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47909536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ffc892412aa787e4af6555c04156ee5c4e13d354e8d87876b73144e97ea2954`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 02 Aug 2022 00:49:10 GMT
ADD file:4cd2f95737fd3007912428eeac56036c9e67e989e66cec08a8be99da47f88494 in / 
# Tue, 02 Aug 2022 00:49:10 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:56:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:56:56 GMT
ENV HOME=/home/user
# Tue, 02 Aug 2022 01:56:57 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 02 Aug 2022 01:56:57 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 01:56:57 GMT
ENV IRSSI_VERSION=1.4.2
# Tue, 02 Aug 2022 01:57:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dirmngr 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Tue, 02 Aug 2022 01:57:52 GMT
WORKDIR /home/user
# Tue, 02 Aug 2022 01:57:52 GMT
USER user
# Tue, 02 Aug 2022 01:57:52 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5890b0ca6af5e8467a488e68716691950496a8f247d0495c2d595ddcb1893aff`  
		Last Modified: Tue, 02 Aug 2022 00:56:06 GMT  
		Size: 28.9 MB (28905515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b96885e167027fcb6391bfc0fda996e4c68280b656a669066fbca6ee32f57c`  
		Last Modified: Tue, 02 Aug 2022 01:58:20 GMT  
		Size: 14.7 MB (14674073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b78241a104470ed2f1128a082f2f65560bf86cf724fa5df219dbdf00d2faa0`  
		Last Modified: Tue, 02 Aug 2022 01:58:15 GMT  
		Size: 4.2 KB (4190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72eefd5a1fe1c338236141cea2f58baa3efd6d80e1d1c7043ed996e975a96ac`  
		Last Modified: Tue, 02 Aug 2022 01:58:16 GMT  
		Size: 4.3 MB (4325758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:latest` - linux; arm variant v7

```console
$ docker pull irssi@sha256:e921634c5488eab60d5f3bb71deaf4120a440291f0be93ee8379aba27b415e9f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45176825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f99154c23f142ad6e7a9f37ecd8062dceea9d74ff0edd51b490fc8e937b82ff`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Jul 2022 00:59:54 GMT
ADD file:ae890621b36ff6e27364bb7316b5bd4319a820ddf7e65565c6201eb11d70fde9 in / 
# Tue, 12 Jul 2022 00:59:55 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 06:34:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 06:34:28 GMT
ENV HOME=/home/user
# Tue, 12 Jul 2022 06:34:30 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 12 Jul 2022 06:34:30 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 20:17:40 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 20:18:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dirmngr 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Mon, 18 Jul 2022 20:18:49 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 20:18:49 GMT
USER user
# Mon, 18 Jul 2022 20:18:50 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:314cda9d0ef2282082d2bd0efd7659e0d9edb3ceae8e7919d990bcf95cbb3d2b`  
		Last Modified: Tue, 12 Jul 2022 01:12:37 GMT  
		Size: 26.6 MB (26560559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ca7959cb389c6a5178f433269da0b2c6c8474f8d44d9e40a3869ac96588d4d`  
		Last Modified: Tue, 12 Jul 2022 06:36:58 GMT  
		Size: 14.4 MB (14424292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976f86f89cadf992f0b4055818f123826998345af9b5f5940d0bc653a2427057`  
		Last Modified: Tue, 12 Jul 2022 06:36:43 GMT  
		Size: 4.2 KB (4188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419495c1f261eea969d0d2028dc1d47a5b2f7dd668f9f481a728a8b665085a0a`  
		Last Modified: Mon, 18 Jul 2022 20:20:19 GMT  
		Size: 4.2 MB (4187786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:latest` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:2d22ed2ec5237ace63ed06ac97c4d4a20e21c76708fadc56fc6c0a3962626605
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49603297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2913f649550379e0daaad94fb55a90e376e9be33556c8052e9d6460df2fad579`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:34 GMT
ADD file:f3a33075f4c3324c6a634ef37a1965ddd5606b4449c0f5909ce18eeb8268b612 in / 
# Tue, 12 Jul 2022 00:40:35 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 03:58:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 03:58:01 GMT
ENV HOME=/home/user
# Tue, 12 Jul 2022 03:58:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 12 Jul 2022 03:58:03 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 18:48:35 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 18:49:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dirmngr 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Mon, 18 Jul 2022 18:49:06 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 18:49:07 GMT
USER user
# Mon, 18 Jul 2022 18:49:08 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:60197a4c18d4b386d371cf39d01c48e98c357bba06da0b070a3c1f75006fd838`  
		Last Modified: Tue, 12 Jul 2022 00:46:13 GMT  
		Size: 30.1 MB (30054226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31d5df8c69c5980350d19a5ffb57504867950d6e5b8c3a6f11080af3e3a0c38`  
		Last Modified: Tue, 12 Jul 2022 03:59:16 GMT  
		Size: 15.4 MB (15377261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b76490db37eaebc94203a05f902096f75ed24cf7a086628cafc39dc7769bbf`  
		Last Modified: Tue, 12 Jul 2022 03:59:13 GMT  
		Size: 4.1 KB (4067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ccc8bb291efc3aa7242c0d8b4780541f2d9603daf68e756cdf6f635b29b4f4`  
		Last Modified: Mon, 18 Jul 2022 18:50:05 GMT  
		Size: 4.2 MB (4167743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:latest` - linux; 386

```console
$ docker pull irssi@sha256:6c4957ff125a55b1b7681b5dcff90a8b3038362e2a8e4153879db7a2be28b1c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51679954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50aea866fe6b1bbdd4191e840834c20db4a10eb7bd0c9578c2b83f18f0825eb0`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 02 Aug 2022 00:39:20 GMT
ADD file:f771e2286465694126158821089d801c7296376be2a56189e6041a15d2fe79f5 in / 
# Tue, 02 Aug 2022 00:39:21 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 03:10:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 03:10:20 GMT
ENV HOME=/home/user
# Tue, 02 Aug 2022 03:10:20 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 02 Aug 2022 03:10:21 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 03:10:22 GMT
ENV IRSSI_VERSION=1.4.2
# Tue, 02 Aug 2022 03:10:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dirmngr 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Tue, 02 Aug 2022 03:11:00 GMT
WORKDIR /home/user
# Tue, 02 Aug 2022 03:11:01 GMT
USER user
# Tue, 02 Aug 2022 03:11:02 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:90eb7f0ce9f33cf5dcd67d54c2fa606186dbaa5f95b6046f36145097267f9e53`  
		Last Modified: Tue, 02 Aug 2022 00:45:14 GMT  
		Size: 32.4 MB (32374054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e807876191c36c0343701cbf9f2866e857910c0bb70333fa34a0d8b7bc512b`  
		Last Modified: Tue, 02 Aug 2022 03:11:36 GMT  
		Size: 15.0 MB (15031673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e042e29265be416ef65d312aeebbf008b8a29b1ed9c1351486c336b91a11d4`  
		Last Modified: Tue, 02 Aug 2022 03:11:33 GMT  
		Size: 4.1 KB (4053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac3539df7150f2d647d38ae218b76d52ba34303d339bf960aa2fe6c5a8b441e`  
		Last Modified: Tue, 02 Aug 2022 03:11:33 GMT  
		Size: 4.3 MB (4270174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:latest` - linux; mips64le

```console
$ docker pull irssi@sha256:5e0bf0828437d767db40431686c24d975b9601b8360a8164074769d9d13c6acf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48617509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556eed7be91d94dbe25d160fa495d39f69c1add07bb664e33c473f458f9a3dd1`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 02 Aug 2022 01:10:34 GMT
ADD file:6dc22a1e5b5fcf23f2549406ddcc45c4e244f46e21eafa881de81fa87438e5d8 in / 
# Tue, 02 Aug 2022 01:10:38 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 03:17:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 03:17:38 GMT
ENV HOME=/home/user
# Tue, 02 Aug 2022 03:17:45 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 02 Aug 2022 03:17:48 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 03:17:51 GMT
ENV IRSSI_VERSION=1.4.2
# Tue, 02 Aug 2022 03:21:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dirmngr 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Tue, 02 Aug 2022 03:21:45 GMT
WORKDIR /home/user
# Tue, 02 Aug 2022 03:21:49 GMT
USER user
# Tue, 02 Aug 2022 03:21:52 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:88350749a27614c791450c256b051f023d81cdd256211274b1efac493779d2be`  
		Last Modified: Tue, 02 Aug 2022 01:21:02 GMT  
		Size: 29.6 MB (29628964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32415daee5708ee92f8f0d8cbb82cc3e0aba17931f1daa2fe19a06b38d6b4b3`  
		Last Modified: Tue, 02 Aug 2022 03:22:25 GMT  
		Size: 14.7 MB (14668257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31be73626d6aa213ab20d502e69c5545c4ef2147bcacdb751040c739cc9c28f`  
		Last Modified: Tue, 02 Aug 2022 03:22:11 GMT  
		Size: 4.1 KB (4066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848b6bffac840f3f64795049e1548ebc7769ce9475b3921d0cd85176dd664465`  
		Last Modified: Tue, 02 Aug 2022 03:22:15 GMT  
		Size: 4.3 MB (4316222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:latest` - linux; ppc64le

```console
$ docker pull irssi@sha256:a8e6205e8016bdc0cd109de6ed6e9d007b72c466be63523b492adeecc53f5433
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55758440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a96be9146d164ac0e9f7bfc663cc6e3e4d13b1d64bc9f0eef34643e6ac4eb72`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Jul 2022 01:25:28 GMT
ADD file:9e1afe48f40d94f879aefb12a7e68da2f0772d701e95b8219bd1f79a83e1933a in / 
# Tue, 12 Jul 2022 01:25:32 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 06:02:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 06:02:16 GMT
ENV HOME=/home/user
# Tue, 12 Jul 2022 06:02:24 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 12 Jul 2022 06:02:27 GMT
ENV LANG=C.UTF-8
# Mon, 18 Jul 2022 20:59:07 GMT
ENV IRSSI_VERSION=1.4.2
# Mon, 18 Jul 2022 21:05:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dirmngr 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Mon, 18 Jul 2022 21:05:29 GMT
WORKDIR /home/user
# Mon, 18 Jul 2022 21:05:34 GMT
USER user
# Mon, 18 Jul 2022 21:05:39 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:bd3d68d1ce583727f6378a16916795b955cc0ad39e0ebe754a26007ef54744fa`  
		Last Modified: Tue, 12 Jul 2022 01:36:03 GMT  
		Size: 35.3 MB (35272500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39e75ba095c6987e0fca8686cbac241d72e4b34526b2312618405b4b0feba71`  
		Last Modified: Tue, 12 Jul 2022 06:07:46 GMT  
		Size: 15.8 MB (15797793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3029a04938ed8ac96ce82eea145146851d02beccd82d19f3af82573e0a00f41a`  
		Last Modified: Tue, 12 Jul 2022 06:07:41 GMT  
		Size: 4.2 KB (4216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3650334413d621df83d25ff4038e0c1ac603ce5ef7d064a444887e524b546e`  
		Last Modified: Mon, 18 Jul 2022 21:07:33 GMT  
		Size: 4.7 MB (4683931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:latest` - linux; s390x

```console
$ docker pull irssi@sha256:c664751349154e1ce063ab587bf63b9f363867f57ae9c1edb8da99dc42b3fe4a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50192142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2485b9e0e2067eb44ac6ef1a366099a1d3f9f29d553bfbe09dc44ef7dae829e`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 02 Aug 2022 00:42:27 GMT
ADD file:c2afc8990930846fbe7c99bfdfe9ea562c75feb6e3c9122431f7c9f8b5e51a7f in / 
# Tue, 02 Aug 2022 00:42:29 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 02:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 02:35:29 GMT
ENV HOME=/home/user
# Tue, 02 Aug 2022 02:35:30 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 02 Aug 2022 02:35:30 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 02:35:30 GMT
ENV IRSSI_VERSION=1.4.2
# Tue, 02 Aug 2022 02:35:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dirmngr 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Tue, 02 Aug 2022 02:35:57 GMT
WORKDIR /home/user
# Tue, 02 Aug 2022 02:35:57 GMT
USER user
# Tue, 02 Aug 2022 02:35:57 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:026d311d0716db60eba0572ea784c21031f420960510cebcc383dc53949b4db8`  
		Last Modified: Tue, 02 Aug 2022 00:48:01 GMT  
		Size: 29.6 MB (29640259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813471a33007d06aacc4cbaf7aff38415e1205c5fee4edd8e2c0f2bfebd0d8f2`  
		Last Modified: Tue, 02 Aug 2022 02:36:36 GMT  
		Size: 15.8 MB (15796925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecee3a36c2c868b4cf52323b6be62201a59b371d017e3336960cb20cb2ff679`  
		Last Modified: Tue, 02 Aug 2022 02:36:33 GMT  
		Size: 4.2 KB (4208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e622d653a1f908ca86a2ecd33d0381d0bcafee70c2badfa9733d02eca0a6901d`  
		Last Modified: Tue, 02 Aug 2022 02:36:33 GMT  
		Size: 4.8 MB (4750750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
