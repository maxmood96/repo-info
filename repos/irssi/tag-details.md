<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `irssi`

-	[`irssi:1`](#irssi1)
-	[`irssi:1-alpine`](#irssi1-alpine)
-	[`irssi:1-alpine3.20`](#irssi1-alpine320)
-	[`irssi:1-bookworm`](#irssi1-bookworm)
-	[`irssi:1.4`](#irssi14)
-	[`irssi:1.4-alpine`](#irssi14-alpine)
-	[`irssi:1.4-alpine3.20`](#irssi14-alpine320)
-	[`irssi:1.4-bookworm`](#irssi14-bookworm)
-	[`irssi:1.4.5`](#irssi145)
-	[`irssi:1.4.5-alpine`](#irssi145-alpine)
-	[`irssi:1.4.5-alpine3.20`](#irssi145-alpine320)
-	[`irssi:1.4.5-bookworm`](#irssi145-bookworm)
-	[`irssi:alpine`](#irssialpine)
-	[`irssi:alpine3.20`](#irssialpine320)
-	[`irssi:bookworm`](#irssibookworm)
-	[`irssi:latest`](#irssilatest)

## `irssi:1`

```console
$ docker pull irssi@sha256:d843f5da94333b1e5b71252558cfc96bab350fe4b5ae651a74215574f5141d77
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `irssi:1` - linux; amd64

```console
$ docker pull irssi@sha256:8aa50d7d3ea8f42fd43067cfbb6f0de50482d7d8e3db5a50fe2598628eb02cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51991262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a6601170dc20fcf1c200d8db92a1f1b4cb70798a9bad21d6347fec54cedd7d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb24a21ee06ae2e696f315794f60683badb1fd6322bffc2a0319d2af71210d22`  
		Last Modified: Thu, 17 Oct 2024 01:21:30 GMT  
		Size: 18.3 MB (18268738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdfe65b078593a20f4d8a6a2e19a8bf4630a32c9a7de2f322b2844f2d93d438`  
		Last Modified: Thu, 17 Oct 2024 01:21:29 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5809862e7f3e9acbbd4cfdb6fa307742f16800ba62916d52f094603dda824867`  
		Last Modified: Thu, 17 Oct 2024 01:21:30 GMT  
		Size: 4.6 MB (4592881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:b14643a76798849fc221cdbff8e7ea9154d43b8eb786152f7b09914b50cb4457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bd8878fc0ba19f6256e48b5d5f656828755ecf598b5a6c70ff014b3ee3fc7c`

```dockerfile
```

-	Layers:
	-	`sha256:f8074bdb984a9cbee8b0939fbd785951f79e4c40ec6e2cabf14987ab7c996ed9`  
		Last Modified: Thu, 17 Oct 2024 01:21:30 GMT  
		Size: 5.4 MB (5365679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:944a60539d43dccd726aaed7cd2f3bd293bed84744b2dc7741271b82951374aa`  
		Last Modified: Thu, 17 Oct 2024 01:21:29 GMT  
		Size: 18.6 KB (18554 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v5

```console
$ docker pull irssi@sha256:e85a8d276df24059b698c6cc142a6506e446bfa77824eef8ce9bfa01e59a4de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48374514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8cf2dfca38be27dba04fd2515e55b60909c37be13165966482d40e007bdd01`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:c8ec8d65b2f61866a2c6085ed61e936733bc484abeeba1b91d12b9f6a97e456b in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e51d4479d9f15eaafec663087c05baede0a0724dc30787f7912ade3b686f46b1`  
		Last Modified: Thu, 17 Oct 2024 00:57:27 GMT  
		Size: 26.9 MB (26887306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df41522fb0d82bb74591eb0a6713b9bb3839d683778f8fab089fd229cbab932`  
		Last Modified: Thu, 17 Oct 2024 05:45:36 GMT  
		Size: 17.0 MB (17039325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fb9e3ff10a084e27b6bfc73e1c126d52dfb2770497d3af79313971c85d0e88`  
		Last Modified: Thu, 17 Oct 2024 05:45:35 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87475fcd2d3950e702cf8a915e34f0cc33b5d567947163f35f8b5ead687d17f`  
		Last Modified: Thu, 17 Oct 2024 05:45:35 GMT  
		Size: 4.4 MB (4444529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:d4fccfbe8c9851c23102ad85753a1eb2f86077bce99aef53d6de10c36ae00665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d43f272b6657e00c3e2aef48985598165862c59becd212cdcf2a6e41be557f1`

```dockerfile
```

-	Layers:
	-	`sha256:82a5e95b79e54c65b557fc48cafd3b3ad757a681ec457ab0dab4a03421e88b20`  
		Last Modified: Thu, 17 Oct 2024 05:45:35 GMT  
		Size: 5.4 MB (5367178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc81d93dc84be6d270a4b218df61a62925757a55ab8712283db916743c4d67ab`  
		Last Modified: Thu, 17 Oct 2024 05:45:35 GMT  
		Size: 18.7 KB (18682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v7

```console
$ docker pull irssi@sha256:12ad8e850827d74e28bde549e45ac6beaa8651c36f70afc08919d4cbc542961e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45654435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a7c45209aca883ac274fb51ef1c0c0e6d936a981a6518d42daa02f83a6a278`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f348c2f61d7048f13bbb2bf7c6015111e9341c1b2a57bb0f51c370ca45bd907`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 16.6 MB (16633805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8267612072f179f1f84c6a626ad7269f297796bd2a5cdfe38e2610ff43c9ba38`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980a4fb6213eb64092401fc4580bd066eb7536f435211170043953cb5d550b1a`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 4.3 MB (4299079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:9262df858faf119c78f44abe577174119e92d426eb5afed88413643ce45f3cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c68652ec81e35444cd943d16301610be8a1e00177afd6de2925c6813f9f4bba1`

```dockerfile
```

-	Layers:
	-	`sha256:672662f58b1c37e76367c167633e8ad8b24c5071cbe5c947ff3858f8eace60da`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 5.4 MB (5367033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf4fc54a2dd30f7fa8311901fa81effc94562db647873e07c968866f1d5b4a66`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 18.7 KB (18682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f0a0f670eae231f1274d0e9e5097240e841843799dd4bab65297e68836f003d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51720933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad0d0f0c746e27f7c110a3107d75d817c44d4de8ae6606706e33d6296c240d3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fa218b665e0696e6cbbb7e15f224e210265c26d0938799bf2cb4ba9ddb5ed7`  
		Last Modified: Thu, 17 Oct 2024 13:13:59 GMT  
		Size: 18.0 MB (18048181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830a882aa3c01ae181d1aff028e2fbdd695f7cad16cadb69acec9ad7c6404b09`  
		Last Modified: Thu, 17 Oct 2024 13:13:58 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e603ba669c49ad6e8006dc9fd6517daadb6e830ee90614880f222bb717b5359`  
		Last Modified: Thu, 17 Oct 2024 13:13:59 GMT  
		Size: 4.5 MB (4513057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:c90a647af8cbe3ce4e36bffff2ca2dfafe6905cc26bb80f77a68a6ef84a80cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5390891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227f292d79f3a8ec728ca0caa89f4bd85fda9ee2546c35bec4f4890158b19832`

```dockerfile
```

-	Layers:
	-	`sha256:1c3ef154ce409a963bb09794d072c2b1c34a7607ff31366904498b4bfd257aae`  
		Last Modified: Thu, 17 Oct 2024 13:13:59 GMT  
		Size: 5.4 MB (5372161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb2f7fe9f657bdaeb0daa90626317db717c17908e3e479b6e71a075ba1f6dfe0`  
		Last Modified: Thu, 17 Oct 2024 13:13:58 GMT  
		Size: 18.7 KB (18730 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; 386

```console
$ docker pull irssi@sha256:0456833f0dc5f5135063a36bcdfcad14dc427a41da7ff129bb03beca4950cc90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52561651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b622b093ac5b5bccce519dbcd83e5e38b1a80607e3fc8d044d24105bd88ad07f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108ff1f82b7d31627896ef9dfa4d55dd918dd899dc1d07d811f2a973ca493272`  
		Last Modified: Thu, 17 Oct 2024 01:21:25 GMT  
		Size: 17.8 MB (17807462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab24ea74320071af584210ffe42f29229a3c32d58f2fc6b39ce817b15e727ae`  
		Last Modified: Thu, 17 Oct 2024 01:21:24 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e92c1d542ec81f26c5c8944a9622b196df4a3c8a7130c9b8d03f6a1c1601e6`  
		Last Modified: Thu, 17 Oct 2024 01:21:24 GMT  
		Size: 4.6 MB (4606565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:3ec4be7da4181fdbeb6ab8972993b6a1b52b0f88152c7c6a3bee462bfbddce93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5380258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065781f2809ba4e58b52f7baf61a835fd97eebf699650f381a447202796234b7`

```dockerfile
```

-	Layers:
	-	`sha256:75eeb53340b15ef46774f8a563ed54455d45ba0e527466054dec23fddd1ea9d1`  
		Last Modified: Thu, 17 Oct 2024 01:21:24 GMT  
		Size: 5.4 MB (5361757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa627aa524b4d75732bb320f5907ea045cd6c3c40af27a99c07e097375bba8fc`  
		Last Modified: Thu, 17 Oct 2024 01:21:24 GMT  
		Size: 18.5 KB (18501 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; mips64le

```console
$ docker pull irssi@sha256:291d87011c5c636d069d6f74c6796c03d2208d050713b23db2a301c6a54bc9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50633180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e6aa70a891ce32f5488c0353e6f02facfb108db6ba13dfb255a05038802c24`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:673970f358f62b6b095139e9647b41b9af839d4e01f7698755b040f471ff80b2 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:75358c79454e0fed44aa25dd323536443b4a1230fc432aa226620e470d72cf5f`  
		Last Modified: Fri, 27 Sep 2024 09:11:36 GMT  
		Size: 29.1 MB (29124858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d53fbf788bd0e7b28f97c4dc927f8ab5bc32596e4d316d1e4107d63df122e3`  
		Last Modified: Fri, 27 Sep 2024 23:25:12 GMT  
		Size: 16.9 MB (16949902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2858574a09072d459734ac302f8784ee2119cd1028b5d0e81359d03e7693743`  
		Last Modified: Fri, 27 Sep 2024 23:25:10 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86aa9a6bf5e9b33a0ce592db709ac8916b028b333caa0bbdb8fba1bd2f6214cd`  
		Last Modified: Fri, 27 Sep 2024 23:25:11 GMT  
		Size: 4.6 MB (4555066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:7b17417d51f41d70cde36d9d968c36209ddd5246b2e9a87b8841b2c1aaee76fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bd0d67639923b725e3575a86ab49679b4125e46a54d6d4697146278f381a88`

```dockerfile
```

-	Layers:
	-	`sha256:55950ecb6cc8539508cfd44c53f5ad3fe2fb065c30a19cc098db41c8cf9a68da`  
		Last Modified: Fri, 27 Sep 2024 23:25:10 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; ppc64le

```console
$ docker pull irssi@sha256:9e802780529f1ac8dc9e2a4e005a33691d9392e00937ff96d0605832f9bebbd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56730477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802dbfec090fbf25a29b5a6497cf1b84626e3b8445a70448f5e978e66beb8135`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c9398d733e6504c746da92179ca87ad112a632322da102a80b7fcfb289570b`  
		Last Modified: Thu, 17 Oct 2024 08:39:47 GMT  
		Size: 18.8 MB (18776314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29a43ed635481a1588bff095c3612c8656bc784fe29d6e2775b4687f0754952`  
		Last Modified: Thu, 17 Oct 2024 08:39:46 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4012dfdba364ca794130d1dffd077292fcb38350f73fb6278877bd25d2d8c7fc`  
		Last Modified: Thu, 17 Oct 2024 08:39:47 GMT  
		Size: 4.8 MB (4828605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:1a5fd59e01471305d46ac075911b975e8aeb9c14be98e8c2e4441ce1de6d6bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80260c15ff6e7c8aadd796f8e69434fca49c016e38b7c433fb18d14cca2bd504`

```dockerfile
```

-	Layers:
	-	`sha256:25819b0bf172f91e1cd05bc76766c461bdf1e8521e7ae7c7a0a8bbc22ca147bf`  
		Last Modified: Thu, 17 Oct 2024 08:39:47 GMT  
		Size: 5.4 MB (5373373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:354ff742b1d00d43544704361eebfaace5714e6f96f4e66b0313e9d1267af98c`  
		Last Modified: Thu, 17 Oct 2024 08:39:46 GMT  
		Size: 18.6 KB (18620 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; s390x

```console
$ docker pull irssi@sha256:62d3dfafa7f8ea785b17fac4aeab1d35709c0631816835fa6904e57e336d1582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50307925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9113e290344eed8b5c9217ede2fd0b90f7b73c19455deaf66a2c37498fea6f3f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc28589ea18c5147d2150e6c305d805ff80ab242c5f64ebff3fa07cd244b1e20`  
		Last Modified: Thu, 17 Oct 2024 13:15:53 GMT  
		Size: 18.2 MB (18227811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e4c1d1c7203ba73e3baed860511382dcaba23fb316575e5b4a68aea09ad8ce`  
		Last Modified: Thu, 17 Oct 2024 13:15:52 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16802b2f05ed3d331e4ca172c0f5e0e78f969f531b192c9cab2b79fa17ca9320`  
		Last Modified: Thu, 17 Oct 2024 13:15:53 GMT  
		Size: 4.6 MB (4586676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:e5ddc58cf0baeb33e18378e5729dfafea51d5d9e6abf4ba9d3e48d5e8ea96eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5383534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548345c85d4ac645fd695bb4f1236c309665e73904bacdded8fab6976d751206`

```dockerfile
```

-	Layers:
	-	`sha256:bf5ab0e8e73932f8aba43d1f7ce78795c90e0123ee9735706a911813cc3d5fdb`  
		Last Modified: Thu, 17 Oct 2024 13:15:53 GMT  
		Size: 5.4 MB (5364980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6966e3fc81ec6a47d7dba5ee8184f4a0d792e39d59ee9ab2e594cb8c3dfe2f1a`  
		Last Modified: Thu, 17 Oct 2024 13:15:52 GMT  
		Size: 18.6 KB (18554 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine`

```console
$ docker pull irssi@sha256:8433cdf30e274988426352ad38712dc09f28c4c1768569d4588eea8dae437e60
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
$ docker pull irssi@sha256:225eeedb3d5df0d8342c28f28a67e14963a4a3f668754735ab50b36cf23849a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19723767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8718185e934cf00977ac16947769332a38a80ba94b1958d5134cc5096dddec`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c626f109cf0e2e5ee386344e1f4f1278bab9391d09e043d3f9afe609c04387`  
		Last Modified: Fri, 06 Sep 2024 23:21:57 GMT  
		Size: 10.2 MB (10191821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753e1b9dda433c6260ec07e1572c0120eeb2205ad32293eae47eaa0a81b43bfd`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fa96080be04b7162785b53e6197cf44a7906954d44de78eb0bbeb69eeac92e`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 5.9 MB (5907140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:187222cb890ac3b3f65f968a23c8375217deb65302025ca80d3bddd34aa6405a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1197741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ad74886f316acc6cfaebde6ff77de40ec17fd0107308bfb57973256f59e8d5`

```dockerfile
```

-	Layers:
	-	`sha256:f7ca62c1d6b0082fb2d26f943a081038469132453899545953a91012cd4e7375`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 1.2 MB (1180425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b77417a1071ef7e7085c110ce17cfa06c18b50cf1b1caf8ba006a14f926abb21`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 17.3 KB (17316 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:bc876fda49849676e70afc23dfc3e74c36da0c2a3745f5fd3c28a8aa9b8635b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18480137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf0c54c34c514e6637fbbdc3209d255343b87c65ed581f951673640306e1dac6`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4563366942775996dc7eff42d60df711ef73b0fbafbca9edb8d797024668c202`  
		Last Modified: Sat, 07 Sep 2024 02:40:26 GMT  
		Size: 9.4 MB (9362097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6b0c6e5c33e41b06fde0292dae092dc763b7e27b823ab7be705407c11384bd`  
		Last Modified: Sat, 07 Sep 2024 02:40:25 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcce1db33190250448077f9d4cd391b9ef2b6a67f7d2fa94f27bc0362e4894cd`  
		Last Modified: Sat, 07 Sep 2024 02:40:26 GMT  
		Size: 5.8 MB (5750537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:4d1617b7ab5430803bbd52362c57bb453d8dd4acaedf8bdde2447432a7ff9e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a999001bf9c39d625593692a3b737f6f3a0b814b3c4811047346af7fada502`

```dockerfile
```

-	Layers:
	-	`sha256:818f414539c29d70896c89b3932576101e8e18ce58a90487359afb4f38d44f5b`  
		Last Modified: Sat, 07 Sep 2024 02:40:25 GMT  
		Size: 17.2 KB (17221 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:1d02a8ed391c51bde9b27afde1ea4240cc487cf74dbf61e5d2efba692b2799f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17782449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053a71b3a279ad0e3a2e0d7dbbf4e54ad2278be015c7f288b5fd103a4d67c754`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0429f3169f57cf771d30f0b785f6c7a5ab02d43411f8d6f2344100a482351a48`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 9.2 MB (9183709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5dba3974eab46837cadb17dfa4a364e5da3b9bd43af9186c06744a8fd58a40`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f255b010ec76769301234a17a2d0bdd32e205d39407d7962c89e1a5c79b89851`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 5.5 MB (5502241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:14f64ac5066b5ca789c86b0625abe3210bf749b295085d8d92dd6af200205bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1200797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32f9747e49a5665b3336fd605ddcdacc76f8ada3a5d544863246fb41d31ad24`

```dockerfile
```

-	Layers:
	-	`sha256:35094785d6853a5f0461474df37f8127ad609827a2b89f696d94a63f97125283`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 1.2 MB (1183357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4d31524ff73face1950830eab2bd0ed7ec05e4012f74641a1b5a49010fc1998`  
		Last Modified: Sat, 07 Sep 2024 02:57:53 GMT  
		Size: 17.4 KB (17440 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:62e8dceafa5dcc45ea2419d86401fbf0824b7a4bae684d174ad74b52a78abf20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20053478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec1e645d1e32a1d6e4842461b9a9b6b03670618d7c7be7a3c59a8f9773ddd02`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad68fd7a6bae4d6a9f0791e9a8b0d89515ef68cc3b3bc2802082159c8f0b917`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 10.2 MB (10157951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1759a5bf2c0e097fe22b543d149e5fdcd014e7b5f039a9fdb8b9ba503d6be7f`  
		Last Modified: Sat, 07 Sep 2024 05:27:55 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0df7ac6458b3449bfc8746487857687df8de1d04144326f711d143f904e0da`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 5.8 MB (5806884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:964aec0691615b07c0f7cf64bd3c2aaf8e77f54ae96bd8ae41c132aa2d21c32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1198193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0846e8bd16a6800d33a45be72816781d99d14770119347a9b650981b6cf2073e`

```dockerfile
```

-	Layers:
	-	`sha256:fe65408852799879429a8939ccc5713fad8538db3615fa77035290c4b582c5ec`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 1.2 MB (1180529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d76afdd382391f2e7f0b7e5e52a8af475ce69ab9742ec727e6e0d04ed084114`  
		Last Modified: Sat, 07 Sep 2024 05:27:55 GMT  
		Size: 17.7 KB (17664 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; 386

```console
$ docker pull irssi@sha256:cec60383cb2114de36cc450b24a795c8b842ea3fe2b5d3ae261777966088981c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19101566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f9750cde5e598eddb25cb06de3196c475dfe940267f34c736aeebf2d606696`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fe8a84f82ad300ce90efce39dd06078babce03103f8b8fe54cdbafb1fbc1f5`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 9.6 MB (9637197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d066bbdeb2014769a48d8148c61e03de10dbfb7acd1ab85f2ded1e7fc00d4d`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52264d62ad1faa811627d0ed73c1b84f1ac7d0eb79bc1dfe11cf881039971566`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 6.0 MB (5994206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:8fa447d248e4470c90876cde43ba4113beae83308c1df0897cc7ef9aadc43c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1197639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e42131d18a25107b03a2c3896713f456d13455b6ae6538165e7722393cb301d`

```dockerfile
```

-	Layers:
	-	`sha256:9e6c0cce7fb0dd7e8aa2edbf38f26a85728a617a5dd3a52ad2b45f225e21aa48`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 1.2 MB (1180380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9529db747d4db3bf62950ed172f88b0bc2940614e0ca337601c634c09ba51f2`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 17.3 KB (17259 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:f4295c16c15be6d6b002444faf906a4376f6a034f0fb10e7804ca1a0eb5a5d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20117357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612e050904415a82d96b010cd7125b10f3b535d204678ca2a9de0dfdd94b5bab`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf7f01d0ac0592b557f92ad27859bdcd34b46bd87f3357c86c81131ba4c1ac3`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 10.4 MB (10379021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e046fbadf0eb3f861ca076d737a51e9d3f8f54cf0fe5a50fd781332a42914a3`  
		Last Modified: Sat, 07 Sep 2024 07:03:05 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e93d1891687db40bc621f9c7c4b32ada1170a9c98951f1fe4aa315a844c730`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 6.2 MB (6164918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:ec763bbab32c460ad03421366a5aebc14cf613d6d45bb177fd44d671e3bd6371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4e5a8fced4a91a234e459d3e86f70f0a875ef57ce7b3b2778200d6692f8cc1`

```dockerfile
```

-	Layers:
	-	`sha256:2121fb019fff014bbc612a435b5e0209feb68478ca72db18ce1d8ca584be271f`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 1.2 MB (1178529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a52d086952a00b69d128df0a14d1bdc11dfbe5c91859e833208040720b9d0efd`  
		Last Modified: Sat, 07 Sep 2024 07:03:05 GMT  
		Size: 17.4 KB (17382 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:856c91783f7d21012b38323b36991a4b415b148dcab362efe6d45ca221b9d692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18948633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882b8fdcf190add01c2dc00e479ba691543a23c72901c9b9581734e8ecbd4d80`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634141d08a7f2ae5a144da1847d931b4cc99514263aea51e764b222d536642bd`  
		Last Modified: Sat, 07 Sep 2024 20:33:42 GMT  
		Size: 9.6 MB (9645875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8a2a2ecd95ddd7ef0c9d83f432abab63b16ead3200fd2df5617cfd5b8f0e99`  
		Last Modified: Sat, 07 Sep 2024 20:33:40 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49e9fc5ff805842d79b092fb62541e430a9fdb5d1144f8a360cc2fc1171a61e`  
		Last Modified: Sat, 07 Sep 2024 20:33:41 GMT  
		Size: 5.9 MB (5930308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:3acf8b9addc44a281e26766672e6142aacb88117e08fb56734b09449033a5a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e863619e8a6d2f0955b1b8e1da7b02f294d705f526e5815a8d990aa430482ab2`

```dockerfile
```

-	Layers:
	-	`sha256:00b2eeaffa4b740f8aa8985162c83d7a26da17ff5e9c3bd70b0c62d8dc64788b`  
		Last Modified: Sat, 07 Sep 2024 20:33:41 GMT  
		Size: 1.2 MB (1178525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a3f803218dcbba5730579592f427070a871dd2311ce2e2ceb98ac94e033cdb3`  
		Last Modified: Sat, 07 Sep 2024 20:33:40 GMT  
		Size: 17.4 KB (17377 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:a9343811b921bf367edda23179c3a2567bc8c35339371a584986716c967d30fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20273410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386a4347853f194ac5a1aec08dc721a00fb5214f62aa6b5619bb97822cf8d8d7`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf007dfb739e6f45d5915a24bdaa5a2d439dd6e0b3b795852fdee75463ada95`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 10.8 MB (10753338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21af45072b07676ab768b93ba8bdbd6ea9039d1a189f72d756aef2f352d7f0af`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6f5d317148da6283d176e25e9078d039f9c168bb182f7d79b401a047fa5c44`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 6.1 MB (6057476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:c64fc2803cf39d52ca243caa6b69e23565bd37c6db576f2956d712bee758f118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e5d62029e06315a1f9d7c42efab99910196d2f0539c13839c2644d7722b7fc`

```dockerfile
```

-	Layers:
	-	`sha256:fa51fb87e83eeb4a26311a4273a680a426aad645be1a2b2166305da4793c83bc`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 1.2 MB (1178471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc9bd2b4610dbaf8c034897233371f6d76f0932f7276e254755a2a774162f786`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 17.3 KB (17316 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine3.20`

```console
$ docker pull irssi@sha256:8433cdf30e274988426352ad38712dc09f28c4c1768569d4588eea8dae437e60
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

### `irssi:1-alpine3.20` - linux; amd64

```console
$ docker pull irssi@sha256:225eeedb3d5df0d8342c28f28a67e14963a4a3f668754735ab50b36cf23849a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19723767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8718185e934cf00977ac16947769332a38a80ba94b1958d5134cc5096dddec`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c626f109cf0e2e5ee386344e1f4f1278bab9391d09e043d3f9afe609c04387`  
		Last Modified: Fri, 06 Sep 2024 23:21:57 GMT  
		Size: 10.2 MB (10191821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753e1b9dda433c6260ec07e1572c0120eeb2205ad32293eae47eaa0a81b43bfd`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fa96080be04b7162785b53e6197cf44a7906954d44de78eb0bbeb69eeac92e`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 5.9 MB (5907140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:187222cb890ac3b3f65f968a23c8375217deb65302025ca80d3bddd34aa6405a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1197741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ad74886f316acc6cfaebde6ff77de40ec17fd0107308bfb57973256f59e8d5`

```dockerfile
```

-	Layers:
	-	`sha256:f7ca62c1d6b0082fb2d26f943a081038469132453899545953a91012cd4e7375`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 1.2 MB (1180425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b77417a1071ef7e7085c110ce17cfa06c18b50cf1b1caf8ba006a14f926abb21`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 17.3 KB (17316 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.20` - linux; arm variant v6

```console
$ docker pull irssi@sha256:bc876fda49849676e70afc23dfc3e74c36da0c2a3745f5fd3c28a8aa9b8635b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18480137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf0c54c34c514e6637fbbdc3209d255343b87c65ed581f951673640306e1dac6`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4563366942775996dc7eff42d60df711ef73b0fbafbca9edb8d797024668c202`  
		Last Modified: Sat, 07 Sep 2024 02:40:26 GMT  
		Size: 9.4 MB (9362097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6b0c6e5c33e41b06fde0292dae092dc763b7e27b823ab7be705407c11384bd`  
		Last Modified: Sat, 07 Sep 2024 02:40:25 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcce1db33190250448077f9d4cd391b9ef2b6a67f7d2fa94f27bc0362e4894cd`  
		Last Modified: Sat, 07 Sep 2024 02:40:26 GMT  
		Size: 5.8 MB (5750537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:4d1617b7ab5430803bbd52362c57bb453d8dd4acaedf8bdde2447432a7ff9e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a999001bf9c39d625593692a3b737f6f3a0b814b3c4811047346af7fada502`

```dockerfile
```

-	Layers:
	-	`sha256:818f414539c29d70896c89b3932576101e8e18ce58a90487359afb4f38d44f5b`  
		Last Modified: Sat, 07 Sep 2024 02:40:25 GMT  
		Size: 17.2 KB (17221 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.20` - linux; arm variant v7

```console
$ docker pull irssi@sha256:1d02a8ed391c51bde9b27afde1ea4240cc487cf74dbf61e5d2efba692b2799f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17782449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053a71b3a279ad0e3a2e0d7dbbf4e54ad2278be015c7f288b5fd103a4d67c754`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0429f3169f57cf771d30f0b785f6c7a5ab02d43411f8d6f2344100a482351a48`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 9.2 MB (9183709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5dba3974eab46837cadb17dfa4a364e5da3b9bd43af9186c06744a8fd58a40`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f255b010ec76769301234a17a2d0bdd32e205d39407d7962c89e1a5c79b89851`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 5.5 MB (5502241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:14f64ac5066b5ca789c86b0625abe3210bf749b295085d8d92dd6af200205bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1200797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32f9747e49a5665b3336fd605ddcdacc76f8ada3a5d544863246fb41d31ad24`

```dockerfile
```

-	Layers:
	-	`sha256:35094785d6853a5f0461474df37f8127ad609827a2b89f696d94a63f97125283`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 1.2 MB (1183357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4d31524ff73face1950830eab2bd0ed7ec05e4012f74641a1b5a49010fc1998`  
		Last Modified: Sat, 07 Sep 2024 02:57:53 GMT  
		Size: 17.4 KB (17440 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:62e8dceafa5dcc45ea2419d86401fbf0824b7a4bae684d174ad74b52a78abf20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20053478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec1e645d1e32a1d6e4842461b9a9b6b03670618d7c7be7a3c59a8f9773ddd02`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad68fd7a6bae4d6a9f0791e9a8b0d89515ef68cc3b3bc2802082159c8f0b917`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 10.2 MB (10157951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1759a5bf2c0e097fe22b543d149e5fdcd014e7b5f039a9fdb8b9ba503d6be7f`  
		Last Modified: Sat, 07 Sep 2024 05:27:55 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0df7ac6458b3449bfc8746487857687df8de1d04144326f711d143f904e0da`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 5.8 MB (5806884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:964aec0691615b07c0f7cf64bd3c2aaf8e77f54ae96bd8ae41c132aa2d21c32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1198193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0846e8bd16a6800d33a45be72816781d99d14770119347a9b650981b6cf2073e`

```dockerfile
```

-	Layers:
	-	`sha256:fe65408852799879429a8939ccc5713fad8538db3615fa77035290c4b582c5ec`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 1.2 MB (1180529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d76afdd382391f2e7f0b7e5e52a8af475ce69ab9742ec727e6e0d04ed084114`  
		Last Modified: Sat, 07 Sep 2024 05:27:55 GMT  
		Size: 17.7 KB (17664 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.20` - linux; 386

```console
$ docker pull irssi@sha256:cec60383cb2114de36cc450b24a795c8b842ea3fe2b5d3ae261777966088981c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19101566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f9750cde5e598eddb25cb06de3196c475dfe940267f34c736aeebf2d606696`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fe8a84f82ad300ce90efce39dd06078babce03103f8b8fe54cdbafb1fbc1f5`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 9.6 MB (9637197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d066bbdeb2014769a48d8148c61e03de10dbfb7acd1ab85f2ded1e7fc00d4d`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52264d62ad1faa811627d0ed73c1b84f1ac7d0eb79bc1dfe11cf881039971566`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 6.0 MB (5994206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:8fa447d248e4470c90876cde43ba4113beae83308c1df0897cc7ef9aadc43c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1197639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e42131d18a25107b03a2c3896713f456d13455b6ae6538165e7722393cb301d`

```dockerfile
```

-	Layers:
	-	`sha256:9e6c0cce7fb0dd7e8aa2edbf38f26a85728a617a5dd3a52ad2b45f225e21aa48`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 1.2 MB (1180380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9529db747d4db3bf62950ed172f88b0bc2940614e0ca337601c634c09ba51f2`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 17.3 KB (17259 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.20` - linux; ppc64le

```console
$ docker pull irssi@sha256:f4295c16c15be6d6b002444faf906a4376f6a034f0fb10e7804ca1a0eb5a5d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20117357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612e050904415a82d96b010cd7125b10f3b535d204678ca2a9de0dfdd94b5bab`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf7f01d0ac0592b557f92ad27859bdcd34b46bd87f3357c86c81131ba4c1ac3`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 10.4 MB (10379021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e046fbadf0eb3f861ca076d737a51e9d3f8f54cf0fe5a50fd781332a42914a3`  
		Last Modified: Sat, 07 Sep 2024 07:03:05 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e93d1891687db40bc621f9c7c4b32ada1170a9c98951f1fe4aa315a844c730`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 6.2 MB (6164918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:ec763bbab32c460ad03421366a5aebc14cf613d6d45bb177fd44d671e3bd6371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4e5a8fced4a91a234e459d3e86f70f0a875ef57ce7b3b2778200d6692f8cc1`

```dockerfile
```

-	Layers:
	-	`sha256:2121fb019fff014bbc612a435b5e0209feb68478ca72db18ce1d8ca584be271f`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 1.2 MB (1178529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a52d086952a00b69d128df0a14d1bdc11dfbe5c91859e833208040720b9d0efd`  
		Last Modified: Sat, 07 Sep 2024 07:03:05 GMT  
		Size: 17.4 KB (17382 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.20` - linux; riscv64

```console
$ docker pull irssi@sha256:856c91783f7d21012b38323b36991a4b415b148dcab362efe6d45ca221b9d692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18948633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882b8fdcf190add01c2dc00e479ba691543a23c72901c9b9581734e8ecbd4d80`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634141d08a7f2ae5a144da1847d931b4cc99514263aea51e764b222d536642bd`  
		Last Modified: Sat, 07 Sep 2024 20:33:42 GMT  
		Size: 9.6 MB (9645875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8a2a2ecd95ddd7ef0c9d83f432abab63b16ead3200fd2df5617cfd5b8f0e99`  
		Last Modified: Sat, 07 Sep 2024 20:33:40 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49e9fc5ff805842d79b092fb62541e430a9fdb5d1144f8a360cc2fc1171a61e`  
		Last Modified: Sat, 07 Sep 2024 20:33:41 GMT  
		Size: 5.9 MB (5930308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:3acf8b9addc44a281e26766672e6142aacb88117e08fb56734b09449033a5a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e863619e8a6d2f0955b1b8e1da7b02f294d705f526e5815a8d990aa430482ab2`

```dockerfile
```

-	Layers:
	-	`sha256:00b2eeaffa4b740f8aa8985162c83d7a26da17ff5e9c3bd70b0c62d8dc64788b`  
		Last Modified: Sat, 07 Sep 2024 20:33:41 GMT  
		Size: 1.2 MB (1178525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a3f803218dcbba5730579592f427070a871dd2311ce2e2ceb98ac94e033cdb3`  
		Last Modified: Sat, 07 Sep 2024 20:33:40 GMT  
		Size: 17.4 KB (17377 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.20` - linux; s390x

```console
$ docker pull irssi@sha256:a9343811b921bf367edda23179c3a2567bc8c35339371a584986716c967d30fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20273410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386a4347853f194ac5a1aec08dc721a00fb5214f62aa6b5619bb97822cf8d8d7`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf007dfb739e6f45d5915a24bdaa5a2d439dd6e0b3b795852fdee75463ada95`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 10.8 MB (10753338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21af45072b07676ab768b93ba8bdbd6ea9039d1a189f72d756aef2f352d7f0af`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6f5d317148da6283d176e25e9078d039f9c168bb182f7d79b401a047fa5c44`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 6.1 MB (6057476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:c64fc2803cf39d52ca243caa6b69e23565bd37c6db576f2956d712bee758f118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e5d62029e06315a1f9d7c42efab99910196d2f0539c13839c2644d7722b7fc`

```dockerfile
```

-	Layers:
	-	`sha256:fa51fb87e83eeb4a26311a4273a680a426aad645be1a2b2166305da4793c83bc`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 1.2 MB (1178471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc9bd2b4610dbaf8c034897233371f6d76f0932f7276e254755a2a774162f786`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 17.3 KB (17316 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-bookworm`

```console
$ docker pull irssi@sha256:d843f5da94333b1e5b71252558cfc96bab350fe4b5ae651a74215574f5141d77
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `irssi:1-bookworm` - linux; amd64

```console
$ docker pull irssi@sha256:8aa50d7d3ea8f42fd43067cfbb6f0de50482d7d8e3db5a50fe2598628eb02cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51991262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a6601170dc20fcf1c200d8db92a1f1b4cb70798a9bad21d6347fec54cedd7d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb24a21ee06ae2e696f315794f60683badb1fd6322bffc2a0319d2af71210d22`  
		Last Modified: Thu, 17 Oct 2024 01:21:30 GMT  
		Size: 18.3 MB (18268738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdfe65b078593a20f4d8a6a2e19a8bf4630a32c9a7de2f322b2844f2d93d438`  
		Last Modified: Thu, 17 Oct 2024 01:21:29 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5809862e7f3e9acbbd4cfdb6fa307742f16800ba62916d52f094603dda824867`  
		Last Modified: Thu, 17 Oct 2024 01:21:30 GMT  
		Size: 4.6 MB (4592881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:b14643a76798849fc221cdbff8e7ea9154d43b8eb786152f7b09914b50cb4457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bd8878fc0ba19f6256e48b5d5f656828755ecf598b5a6c70ff014b3ee3fc7c`

```dockerfile
```

-	Layers:
	-	`sha256:f8074bdb984a9cbee8b0939fbd785951f79e4c40ec6e2cabf14987ab7c996ed9`  
		Last Modified: Thu, 17 Oct 2024 01:21:30 GMT  
		Size: 5.4 MB (5365679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:944a60539d43dccd726aaed7cd2f3bd293bed84744b2dc7741271b82951374aa`  
		Last Modified: Thu, 17 Oct 2024 01:21:29 GMT  
		Size: 18.6 KB (18554 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:e85a8d276df24059b698c6cc142a6506e446bfa77824eef8ce9bfa01e59a4de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48374514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8cf2dfca38be27dba04fd2515e55b60909c37be13165966482d40e007bdd01`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:c8ec8d65b2f61866a2c6085ed61e936733bc484abeeba1b91d12b9f6a97e456b in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e51d4479d9f15eaafec663087c05baede0a0724dc30787f7912ade3b686f46b1`  
		Last Modified: Thu, 17 Oct 2024 00:57:27 GMT  
		Size: 26.9 MB (26887306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df41522fb0d82bb74591eb0a6713b9bb3839d683778f8fab089fd229cbab932`  
		Last Modified: Thu, 17 Oct 2024 05:45:36 GMT  
		Size: 17.0 MB (17039325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fb9e3ff10a084e27b6bfc73e1c126d52dfb2770497d3af79313971c85d0e88`  
		Last Modified: Thu, 17 Oct 2024 05:45:35 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87475fcd2d3950e702cf8a915e34f0cc33b5d567947163f35f8b5ead687d17f`  
		Last Modified: Thu, 17 Oct 2024 05:45:35 GMT  
		Size: 4.4 MB (4444529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:d4fccfbe8c9851c23102ad85753a1eb2f86077bce99aef53d6de10c36ae00665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d43f272b6657e00c3e2aef48985598165862c59becd212cdcf2a6e41be557f1`

```dockerfile
```

-	Layers:
	-	`sha256:82a5e95b79e54c65b557fc48cafd3b3ad757a681ec457ab0dab4a03421e88b20`  
		Last Modified: Thu, 17 Oct 2024 05:45:35 GMT  
		Size: 5.4 MB (5367178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc81d93dc84be6d270a4b218df61a62925757a55ab8712283db916743c4d67ab`  
		Last Modified: Thu, 17 Oct 2024 05:45:35 GMT  
		Size: 18.7 KB (18682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:12ad8e850827d74e28bde549e45ac6beaa8651c36f70afc08919d4cbc542961e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45654435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a7c45209aca883ac274fb51ef1c0c0e6d936a981a6518d42daa02f83a6a278`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f348c2f61d7048f13bbb2bf7c6015111e9341c1b2a57bb0f51c370ca45bd907`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 16.6 MB (16633805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8267612072f179f1f84c6a626ad7269f297796bd2a5cdfe38e2610ff43c9ba38`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980a4fb6213eb64092401fc4580bd066eb7536f435211170043953cb5d550b1a`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 4.3 MB (4299079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:9262df858faf119c78f44abe577174119e92d426eb5afed88413643ce45f3cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c68652ec81e35444cd943d16301610be8a1e00177afd6de2925c6813f9f4bba1`

```dockerfile
```

-	Layers:
	-	`sha256:672662f58b1c37e76367c167633e8ad8b24c5071cbe5c947ff3858f8eace60da`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 5.4 MB (5367033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf4fc54a2dd30f7fa8311901fa81effc94562db647873e07c968866f1d5b4a66`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 18.7 KB (18682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f0a0f670eae231f1274d0e9e5097240e841843799dd4bab65297e68836f003d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51720933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad0d0f0c746e27f7c110a3107d75d817c44d4de8ae6606706e33d6296c240d3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fa218b665e0696e6cbbb7e15f224e210265c26d0938799bf2cb4ba9ddb5ed7`  
		Last Modified: Thu, 17 Oct 2024 13:13:59 GMT  
		Size: 18.0 MB (18048181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830a882aa3c01ae181d1aff028e2fbdd695f7cad16cadb69acec9ad7c6404b09`  
		Last Modified: Thu, 17 Oct 2024 13:13:58 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e603ba669c49ad6e8006dc9fd6517daadb6e830ee90614880f222bb717b5359`  
		Last Modified: Thu, 17 Oct 2024 13:13:59 GMT  
		Size: 4.5 MB (4513057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c90a647af8cbe3ce4e36bffff2ca2dfafe6905cc26bb80f77a68a6ef84a80cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5390891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227f292d79f3a8ec728ca0caa89f4bd85fda9ee2546c35bec4f4890158b19832`

```dockerfile
```

-	Layers:
	-	`sha256:1c3ef154ce409a963bb09794d072c2b1c34a7607ff31366904498b4bfd257aae`  
		Last Modified: Thu, 17 Oct 2024 13:13:59 GMT  
		Size: 5.4 MB (5372161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb2f7fe9f657bdaeb0daa90626317db717c17908e3e479b6e71a075ba1f6dfe0`  
		Last Modified: Thu, 17 Oct 2024 13:13:58 GMT  
		Size: 18.7 KB (18730 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:0456833f0dc5f5135063a36bcdfcad14dc427a41da7ff129bb03beca4950cc90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52561651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b622b093ac5b5bccce519dbcd83e5e38b1a80607e3fc8d044d24105bd88ad07f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108ff1f82b7d31627896ef9dfa4d55dd918dd899dc1d07d811f2a973ca493272`  
		Last Modified: Thu, 17 Oct 2024 01:21:25 GMT  
		Size: 17.8 MB (17807462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab24ea74320071af584210ffe42f29229a3c32d58f2fc6b39ce817b15e727ae`  
		Last Modified: Thu, 17 Oct 2024 01:21:24 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e92c1d542ec81f26c5c8944a9622b196df4a3c8a7130c9b8d03f6a1c1601e6`  
		Last Modified: Thu, 17 Oct 2024 01:21:24 GMT  
		Size: 4.6 MB (4606565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:3ec4be7da4181fdbeb6ab8972993b6a1b52b0f88152c7c6a3bee462bfbddce93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5380258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065781f2809ba4e58b52f7baf61a835fd97eebf699650f381a447202796234b7`

```dockerfile
```

-	Layers:
	-	`sha256:75eeb53340b15ef46774f8a563ed54455d45ba0e527466054dec23fddd1ea9d1`  
		Last Modified: Thu, 17 Oct 2024 01:21:24 GMT  
		Size: 5.4 MB (5361757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa627aa524b4d75732bb320f5907ea045cd6c3c40af27a99c07e097375bba8fc`  
		Last Modified: Thu, 17 Oct 2024 01:21:24 GMT  
		Size: 18.5 KB (18501 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:291d87011c5c636d069d6f74c6796c03d2208d050713b23db2a301c6a54bc9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50633180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e6aa70a891ce32f5488c0353e6f02facfb108db6ba13dfb255a05038802c24`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:673970f358f62b6b095139e9647b41b9af839d4e01f7698755b040f471ff80b2 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:75358c79454e0fed44aa25dd323536443b4a1230fc432aa226620e470d72cf5f`  
		Last Modified: Fri, 27 Sep 2024 09:11:36 GMT  
		Size: 29.1 MB (29124858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d53fbf788bd0e7b28f97c4dc927f8ab5bc32596e4d316d1e4107d63df122e3`  
		Last Modified: Fri, 27 Sep 2024 23:25:12 GMT  
		Size: 16.9 MB (16949902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2858574a09072d459734ac302f8784ee2119cd1028b5d0e81359d03e7693743`  
		Last Modified: Fri, 27 Sep 2024 23:25:10 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86aa9a6bf5e9b33a0ce592db709ac8916b028b333caa0bbdb8fba1bd2f6214cd`  
		Last Modified: Fri, 27 Sep 2024 23:25:11 GMT  
		Size: 4.6 MB (4555066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:7b17417d51f41d70cde36d9d968c36209ddd5246b2e9a87b8841b2c1aaee76fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bd0d67639923b725e3575a86ab49679b4125e46a54d6d4697146278f381a88`

```dockerfile
```

-	Layers:
	-	`sha256:55950ecb6cc8539508cfd44c53f5ad3fe2fb065c30a19cc098db41c8cf9a68da`  
		Last Modified: Fri, 27 Sep 2024 23:25:10 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:9e802780529f1ac8dc9e2a4e005a33691d9392e00937ff96d0605832f9bebbd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56730477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802dbfec090fbf25a29b5a6497cf1b84626e3b8445a70448f5e978e66beb8135`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c9398d733e6504c746da92179ca87ad112a632322da102a80b7fcfb289570b`  
		Last Modified: Thu, 17 Oct 2024 08:39:47 GMT  
		Size: 18.8 MB (18776314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29a43ed635481a1588bff095c3612c8656bc784fe29d6e2775b4687f0754952`  
		Last Modified: Thu, 17 Oct 2024 08:39:46 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4012dfdba364ca794130d1dffd077292fcb38350f73fb6278877bd25d2d8c7fc`  
		Last Modified: Thu, 17 Oct 2024 08:39:47 GMT  
		Size: 4.8 MB (4828605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:1a5fd59e01471305d46ac075911b975e8aeb9c14be98e8c2e4441ce1de6d6bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80260c15ff6e7c8aadd796f8e69434fca49c016e38b7c433fb18d14cca2bd504`

```dockerfile
```

-	Layers:
	-	`sha256:25819b0bf172f91e1cd05bc76766c461bdf1e8521e7ae7c7a0a8bbc22ca147bf`  
		Last Modified: Thu, 17 Oct 2024 08:39:47 GMT  
		Size: 5.4 MB (5373373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:354ff742b1d00d43544704361eebfaace5714e6f96f4e66b0313e9d1267af98c`  
		Last Modified: Thu, 17 Oct 2024 08:39:46 GMT  
		Size: 18.6 KB (18620 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:62d3dfafa7f8ea785b17fac4aeab1d35709c0631816835fa6904e57e336d1582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50307925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9113e290344eed8b5c9217ede2fd0b90f7b73c19455deaf66a2c37498fea6f3f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc28589ea18c5147d2150e6c305d805ff80ab242c5f64ebff3fa07cd244b1e20`  
		Last Modified: Thu, 17 Oct 2024 13:15:53 GMT  
		Size: 18.2 MB (18227811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e4c1d1c7203ba73e3baed860511382dcaba23fb316575e5b4a68aea09ad8ce`  
		Last Modified: Thu, 17 Oct 2024 13:15:52 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16802b2f05ed3d331e4ca172c0f5e0e78f969f531b192c9cab2b79fa17ca9320`  
		Last Modified: Thu, 17 Oct 2024 13:15:53 GMT  
		Size: 4.6 MB (4586676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:e5ddc58cf0baeb33e18378e5729dfafea51d5d9e6abf4ba9d3e48d5e8ea96eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5383534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548345c85d4ac645fd695bb4f1236c309665e73904bacdded8fab6976d751206`

```dockerfile
```

-	Layers:
	-	`sha256:bf5ab0e8e73932f8aba43d1f7ce78795c90e0123ee9735706a911813cc3d5fdb`  
		Last Modified: Thu, 17 Oct 2024 13:15:53 GMT  
		Size: 5.4 MB (5364980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6966e3fc81ec6a47d7dba5ee8184f4a0d792e39d59ee9ab2e594cb8c3dfe2f1a`  
		Last Modified: Thu, 17 Oct 2024 13:15:52 GMT  
		Size: 18.6 KB (18554 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4`

```console
$ docker pull irssi@sha256:d843f5da94333b1e5b71252558cfc96bab350fe4b5ae651a74215574f5141d77
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `irssi:1.4` - linux; amd64

```console
$ docker pull irssi@sha256:8aa50d7d3ea8f42fd43067cfbb6f0de50482d7d8e3db5a50fe2598628eb02cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51991262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a6601170dc20fcf1c200d8db92a1f1b4cb70798a9bad21d6347fec54cedd7d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb24a21ee06ae2e696f315794f60683badb1fd6322bffc2a0319d2af71210d22`  
		Last Modified: Thu, 17 Oct 2024 01:21:30 GMT  
		Size: 18.3 MB (18268738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdfe65b078593a20f4d8a6a2e19a8bf4630a32c9a7de2f322b2844f2d93d438`  
		Last Modified: Thu, 17 Oct 2024 01:21:29 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5809862e7f3e9acbbd4cfdb6fa307742f16800ba62916d52f094603dda824867`  
		Last Modified: Thu, 17 Oct 2024 01:21:30 GMT  
		Size: 4.6 MB (4592881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:b14643a76798849fc221cdbff8e7ea9154d43b8eb786152f7b09914b50cb4457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bd8878fc0ba19f6256e48b5d5f656828755ecf598b5a6c70ff014b3ee3fc7c`

```dockerfile
```

-	Layers:
	-	`sha256:f8074bdb984a9cbee8b0939fbd785951f79e4c40ec6e2cabf14987ab7c996ed9`  
		Last Modified: Thu, 17 Oct 2024 01:21:30 GMT  
		Size: 5.4 MB (5365679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:944a60539d43dccd726aaed7cd2f3bd293bed84744b2dc7741271b82951374aa`  
		Last Modified: Thu, 17 Oct 2024 01:21:29 GMT  
		Size: 18.6 KB (18554 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v5

```console
$ docker pull irssi@sha256:e85a8d276df24059b698c6cc142a6506e446bfa77824eef8ce9bfa01e59a4de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48374514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8cf2dfca38be27dba04fd2515e55b60909c37be13165966482d40e007bdd01`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:c8ec8d65b2f61866a2c6085ed61e936733bc484abeeba1b91d12b9f6a97e456b in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e51d4479d9f15eaafec663087c05baede0a0724dc30787f7912ade3b686f46b1`  
		Last Modified: Thu, 17 Oct 2024 00:57:27 GMT  
		Size: 26.9 MB (26887306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df41522fb0d82bb74591eb0a6713b9bb3839d683778f8fab089fd229cbab932`  
		Last Modified: Thu, 17 Oct 2024 05:45:36 GMT  
		Size: 17.0 MB (17039325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fb9e3ff10a084e27b6bfc73e1c126d52dfb2770497d3af79313971c85d0e88`  
		Last Modified: Thu, 17 Oct 2024 05:45:35 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87475fcd2d3950e702cf8a915e34f0cc33b5d567947163f35f8b5ead687d17f`  
		Last Modified: Thu, 17 Oct 2024 05:45:35 GMT  
		Size: 4.4 MB (4444529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:d4fccfbe8c9851c23102ad85753a1eb2f86077bce99aef53d6de10c36ae00665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d43f272b6657e00c3e2aef48985598165862c59becd212cdcf2a6e41be557f1`

```dockerfile
```

-	Layers:
	-	`sha256:82a5e95b79e54c65b557fc48cafd3b3ad757a681ec457ab0dab4a03421e88b20`  
		Last Modified: Thu, 17 Oct 2024 05:45:35 GMT  
		Size: 5.4 MB (5367178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc81d93dc84be6d270a4b218df61a62925757a55ab8712283db916743c4d67ab`  
		Last Modified: Thu, 17 Oct 2024 05:45:35 GMT  
		Size: 18.7 KB (18682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v7

```console
$ docker pull irssi@sha256:12ad8e850827d74e28bde549e45ac6beaa8651c36f70afc08919d4cbc542961e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45654435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a7c45209aca883ac274fb51ef1c0c0e6d936a981a6518d42daa02f83a6a278`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f348c2f61d7048f13bbb2bf7c6015111e9341c1b2a57bb0f51c370ca45bd907`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 16.6 MB (16633805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8267612072f179f1f84c6a626ad7269f297796bd2a5cdfe38e2610ff43c9ba38`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980a4fb6213eb64092401fc4580bd066eb7536f435211170043953cb5d550b1a`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 4.3 MB (4299079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:9262df858faf119c78f44abe577174119e92d426eb5afed88413643ce45f3cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c68652ec81e35444cd943d16301610be8a1e00177afd6de2925c6813f9f4bba1`

```dockerfile
```

-	Layers:
	-	`sha256:672662f58b1c37e76367c167633e8ad8b24c5071cbe5c947ff3858f8eace60da`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 5.4 MB (5367033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf4fc54a2dd30f7fa8311901fa81effc94562db647873e07c968866f1d5b4a66`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 18.7 KB (18682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f0a0f670eae231f1274d0e9e5097240e841843799dd4bab65297e68836f003d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51720933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad0d0f0c746e27f7c110a3107d75d817c44d4de8ae6606706e33d6296c240d3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fa218b665e0696e6cbbb7e15f224e210265c26d0938799bf2cb4ba9ddb5ed7`  
		Last Modified: Thu, 17 Oct 2024 13:13:59 GMT  
		Size: 18.0 MB (18048181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830a882aa3c01ae181d1aff028e2fbdd695f7cad16cadb69acec9ad7c6404b09`  
		Last Modified: Thu, 17 Oct 2024 13:13:58 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e603ba669c49ad6e8006dc9fd6517daadb6e830ee90614880f222bb717b5359`  
		Last Modified: Thu, 17 Oct 2024 13:13:59 GMT  
		Size: 4.5 MB (4513057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:c90a647af8cbe3ce4e36bffff2ca2dfafe6905cc26bb80f77a68a6ef84a80cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5390891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227f292d79f3a8ec728ca0caa89f4bd85fda9ee2546c35bec4f4890158b19832`

```dockerfile
```

-	Layers:
	-	`sha256:1c3ef154ce409a963bb09794d072c2b1c34a7607ff31366904498b4bfd257aae`  
		Last Modified: Thu, 17 Oct 2024 13:13:59 GMT  
		Size: 5.4 MB (5372161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb2f7fe9f657bdaeb0daa90626317db717c17908e3e479b6e71a075ba1f6dfe0`  
		Last Modified: Thu, 17 Oct 2024 13:13:58 GMT  
		Size: 18.7 KB (18730 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; 386

```console
$ docker pull irssi@sha256:0456833f0dc5f5135063a36bcdfcad14dc427a41da7ff129bb03beca4950cc90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52561651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b622b093ac5b5bccce519dbcd83e5e38b1a80607e3fc8d044d24105bd88ad07f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108ff1f82b7d31627896ef9dfa4d55dd918dd899dc1d07d811f2a973ca493272`  
		Last Modified: Thu, 17 Oct 2024 01:21:25 GMT  
		Size: 17.8 MB (17807462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab24ea74320071af584210ffe42f29229a3c32d58f2fc6b39ce817b15e727ae`  
		Last Modified: Thu, 17 Oct 2024 01:21:24 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e92c1d542ec81f26c5c8944a9622b196df4a3c8a7130c9b8d03f6a1c1601e6`  
		Last Modified: Thu, 17 Oct 2024 01:21:24 GMT  
		Size: 4.6 MB (4606565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:3ec4be7da4181fdbeb6ab8972993b6a1b52b0f88152c7c6a3bee462bfbddce93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5380258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065781f2809ba4e58b52f7baf61a835fd97eebf699650f381a447202796234b7`

```dockerfile
```

-	Layers:
	-	`sha256:75eeb53340b15ef46774f8a563ed54455d45ba0e527466054dec23fddd1ea9d1`  
		Last Modified: Thu, 17 Oct 2024 01:21:24 GMT  
		Size: 5.4 MB (5361757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa627aa524b4d75732bb320f5907ea045cd6c3c40af27a99c07e097375bba8fc`  
		Last Modified: Thu, 17 Oct 2024 01:21:24 GMT  
		Size: 18.5 KB (18501 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; mips64le

```console
$ docker pull irssi@sha256:291d87011c5c636d069d6f74c6796c03d2208d050713b23db2a301c6a54bc9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50633180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e6aa70a891ce32f5488c0353e6f02facfb108db6ba13dfb255a05038802c24`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:673970f358f62b6b095139e9647b41b9af839d4e01f7698755b040f471ff80b2 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:75358c79454e0fed44aa25dd323536443b4a1230fc432aa226620e470d72cf5f`  
		Last Modified: Fri, 27 Sep 2024 09:11:36 GMT  
		Size: 29.1 MB (29124858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d53fbf788bd0e7b28f97c4dc927f8ab5bc32596e4d316d1e4107d63df122e3`  
		Last Modified: Fri, 27 Sep 2024 23:25:12 GMT  
		Size: 16.9 MB (16949902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2858574a09072d459734ac302f8784ee2119cd1028b5d0e81359d03e7693743`  
		Last Modified: Fri, 27 Sep 2024 23:25:10 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86aa9a6bf5e9b33a0ce592db709ac8916b028b333caa0bbdb8fba1bd2f6214cd`  
		Last Modified: Fri, 27 Sep 2024 23:25:11 GMT  
		Size: 4.6 MB (4555066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:7b17417d51f41d70cde36d9d968c36209ddd5246b2e9a87b8841b2c1aaee76fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bd0d67639923b725e3575a86ab49679b4125e46a54d6d4697146278f381a88`

```dockerfile
```

-	Layers:
	-	`sha256:55950ecb6cc8539508cfd44c53f5ad3fe2fb065c30a19cc098db41c8cf9a68da`  
		Last Modified: Fri, 27 Sep 2024 23:25:10 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; ppc64le

```console
$ docker pull irssi@sha256:9e802780529f1ac8dc9e2a4e005a33691d9392e00937ff96d0605832f9bebbd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56730477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802dbfec090fbf25a29b5a6497cf1b84626e3b8445a70448f5e978e66beb8135`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c9398d733e6504c746da92179ca87ad112a632322da102a80b7fcfb289570b`  
		Last Modified: Thu, 17 Oct 2024 08:39:47 GMT  
		Size: 18.8 MB (18776314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29a43ed635481a1588bff095c3612c8656bc784fe29d6e2775b4687f0754952`  
		Last Modified: Thu, 17 Oct 2024 08:39:46 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4012dfdba364ca794130d1dffd077292fcb38350f73fb6278877bd25d2d8c7fc`  
		Last Modified: Thu, 17 Oct 2024 08:39:47 GMT  
		Size: 4.8 MB (4828605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:1a5fd59e01471305d46ac075911b975e8aeb9c14be98e8c2e4441ce1de6d6bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80260c15ff6e7c8aadd796f8e69434fca49c016e38b7c433fb18d14cca2bd504`

```dockerfile
```

-	Layers:
	-	`sha256:25819b0bf172f91e1cd05bc76766c461bdf1e8521e7ae7c7a0a8bbc22ca147bf`  
		Last Modified: Thu, 17 Oct 2024 08:39:47 GMT  
		Size: 5.4 MB (5373373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:354ff742b1d00d43544704361eebfaace5714e6f96f4e66b0313e9d1267af98c`  
		Last Modified: Thu, 17 Oct 2024 08:39:46 GMT  
		Size: 18.6 KB (18620 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; s390x

```console
$ docker pull irssi@sha256:62d3dfafa7f8ea785b17fac4aeab1d35709c0631816835fa6904e57e336d1582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50307925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9113e290344eed8b5c9217ede2fd0b90f7b73c19455deaf66a2c37498fea6f3f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc28589ea18c5147d2150e6c305d805ff80ab242c5f64ebff3fa07cd244b1e20`  
		Last Modified: Thu, 17 Oct 2024 13:15:53 GMT  
		Size: 18.2 MB (18227811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e4c1d1c7203ba73e3baed860511382dcaba23fb316575e5b4a68aea09ad8ce`  
		Last Modified: Thu, 17 Oct 2024 13:15:52 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16802b2f05ed3d331e4ca172c0f5e0e78f969f531b192c9cab2b79fa17ca9320`  
		Last Modified: Thu, 17 Oct 2024 13:15:53 GMT  
		Size: 4.6 MB (4586676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:e5ddc58cf0baeb33e18378e5729dfafea51d5d9e6abf4ba9d3e48d5e8ea96eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5383534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548345c85d4ac645fd695bb4f1236c309665e73904bacdded8fab6976d751206`

```dockerfile
```

-	Layers:
	-	`sha256:bf5ab0e8e73932f8aba43d1f7ce78795c90e0123ee9735706a911813cc3d5fdb`  
		Last Modified: Thu, 17 Oct 2024 13:15:53 GMT  
		Size: 5.4 MB (5364980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6966e3fc81ec6a47d7dba5ee8184f4a0d792e39d59ee9ab2e594cb8c3dfe2f1a`  
		Last Modified: Thu, 17 Oct 2024 13:15:52 GMT  
		Size: 18.6 KB (18554 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine`

```console
$ docker pull irssi@sha256:8433cdf30e274988426352ad38712dc09f28c4c1768569d4588eea8dae437e60
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
$ docker pull irssi@sha256:225eeedb3d5df0d8342c28f28a67e14963a4a3f668754735ab50b36cf23849a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19723767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8718185e934cf00977ac16947769332a38a80ba94b1958d5134cc5096dddec`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c626f109cf0e2e5ee386344e1f4f1278bab9391d09e043d3f9afe609c04387`  
		Last Modified: Fri, 06 Sep 2024 23:21:57 GMT  
		Size: 10.2 MB (10191821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753e1b9dda433c6260ec07e1572c0120eeb2205ad32293eae47eaa0a81b43bfd`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fa96080be04b7162785b53e6197cf44a7906954d44de78eb0bbeb69eeac92e`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 5.9 MB (5907140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:187222cb890ac3b3f65f968a23c8375217deb65302025ca80d3bddd34aa6405a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1197741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ad74886f316acc6cfaebde6ff77de40ec17fd0107308bfb57973256f59e8d5`

```dockerfile
```

-	Layers:
	-	`sha256:f7ca62c1d6b0082fb2d26f943a081038469132453899545953a91012cd4e7375`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 1.2 MB (1180425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b77417a1071ef7e7085c110ce17cfa06c18b50cf1b1caf8ba006a14f926abb21`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 17.3 KB (17316 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:bc876fda49849676e70afc23dfc3e74c36da0c2a3745f5fd3c28a8aa9b8635b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18480137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf0c54c34c514e6637fbbdc3209d255343b87c65ed581f951673640306e1dac6`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4563366942775996dc7eff42d60df711ef73b0fbafbca9edb8d797024668c202`  
		Last Modified: Sat, 07 Sep 2024 02:40:26 GMT  
		Size: 9.4 MB (9362097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6b0c6e5c33e41b06fde0292dae092dc763b7e27b823ab7be705407c11384bd`  
		Last Modified: Sat, 07 Sep 2024 02:40:25 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcce1db33190250448077f9d4cd391b9ef2b6a67f7d2fa94f27bc0362e4894cd`  
		Last Modified: Sat, 07 Sep 2024 02:40:26 GMT  
		Size: 5.8 MB (5750537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:4d1617b7ab5430803bbd52362c57bb453d8dd4acaedf8bdde2447432a7ff9e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a999001bf9c39d625593692a3b737f6f3a0b814b3c4811047346af7fada502`

```dockerfile
```

-	Layers:
	-	`sha256:818f414539c29d70896c89b3932576101e8e18ce58a90487359afb4f38d44f5b`  
		Last Modified: Sat, 07 Sep 2024 02:40:25 GMT  
		Size: 17.2 KB (17221 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:1d02a8ed391c51bde9b27afde1ea4240cc487cf74dbf61e5d2efba692b2799f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17782449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053a71b3a279ad0e3a2e0d7dbbf4e54ad2278be015c7f288b5fd103a4d67c754`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0429f3169f57cf771d30f0b785f6c7a5ab02d43411f8d6f2344100a482351a48`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 9.2 MB (9183709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5dba3974eab46837cadb17dfa4a364e5da3b9bd43af9186c06744a8fd58a40`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f255b010ec76769301234a17a2d0bdd32e205d39407d7962c89e1a5c79b89851`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 5.5 MB (5502241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:14f64ac5066b5ca789c86b0625abe3210bf749b295085d8d92dd6af200205bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1200797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32f9747e49a5665b3336fd605ddcdacc76f8ada3a5d544863246fb41d31ad24`

```dockerfile
```

-	Layers:
	-	`sha256:35094785d6853a5f0461474df37f8127ad609827a2b89f696d94a63f97125283`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 1.2 MB (1183357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4d31524ff73face1950830eab2bd0ed7ec05e4012f74641a1b5a49010fc1998`  
		Last Modified: Sat, 07 Sep 2024 02:57:53 GMT  
		Size: 17.4 KB (17440 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:62e8dceafa5dcc45ea2419d86401fbf0824b7a4bae684d174ad74b52a78abf20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20053478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec1e645d1e32a1d6e4842461b9a9b6b03670618d7c7be7a3c59a8f9773ddd02`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad68fd7a6bae4d6a9f0791e9a8b0d89515ef68cc3b3bc2802082159c8f0b917`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 10.2 MB (10157951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1759a5bf2c0e097fe22b543d149e5fdcd014e7b5f039a9fdb8b9ba503d6be7f`  
		Last Modified: Sat, 07 Sep 2024 05:27:55 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0df7ac6458b3449bfc8746487857687df8de1d04144326f711d143f904e0da`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 5.8 MB (5806884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:964aec0691615b07c0f7cf64bd3c2aaf8e77f54ae96bd8ae41c132aa2d21c32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1198193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0846e8bd16a6800d33a45be72816781d99d14770119347a9b650981b6cf2073e`

```dockerfile
```

-	Layers:
	-	`sha256:fe65408852799879429a8939ccc5713fad8538db3615fa77035290c4b582c5ec`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 1.2 MB (1180529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d76afdd382391f2e7f0b7e5e52a8af475ce69ab9742ec727e6e0d04ed084114`  
		Last Modified: Sat, 07 Sep 2024 05:27:55 GMT  
		Size: 17.7 KB (17664 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; 386

```console
$ docker pull irssi@sha256:cec60383cb2114de36cc450b24a795c8b842ea3fe2b5d3ae261777966088981c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19101566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f9750cde5e598eddb25cb06de3196c475dfe940267f34c736aeebf2d606696`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fe8a84f82ad300ce90efce39dd06078babce03103f8b8fe54cdbafb1fbc1f5`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 9.6 MB (9637197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d066bbdeb2014769a48d8148c61e03de10dbfb7acd1ab85f2ded1e7fc00d4d`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52264d62ad1faa811627d0ed73c1b84f1ac7d0eb79bc1dfe11cf881039971566`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 6.0 MB (5994206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:8fa447d248e4470c90876cde43ba4113beae83308c1df0897cc7ef9aadc43c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1197639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e42131d18a25107b03a2c3896713f456d13455b6ae6538165e7722393cb301d`

```dockerfile
```

-	Layers:
	-	`sha256:9e6c0cce7fb0dd7e8aa2edbf38f26a85728a617a5dd3a52ad2b45f225e21aa48`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 1.2 MB (1180380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9529db747d4db3bf62950ed172f88b0bc2940614e0ca337601c634c09ba51f2`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 17.3 KB (17259 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:f4295c16c15be6d6b002444faf906a4376f6a034f0fb10e7804ca1a0eb5a5d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20117357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612e050904415a82d96b010cd7125b10f3b535d204678ca2a9de0dfdd94b5bab`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf7f01d0ac0592b557f92ad27859bdcd34b46bd87f3357c86c81131ba4c1ac3`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 10.4 MB (10379021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e046fbadf0eb3f861ca076d737a51e9d3f8f54cf0fe5a50fd781332a42914a3`  
		Last Modified: Sat, 07 Sep 2024 07:03:05 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e93d1891687db40bc621f9c7c4b32ada1170a9c98951f1fe4aa315a844c730`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 6.2 MB (6164918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:ec763bbab32c460ad03421366a5aebc14cf613d6d45bb177fd44d671e3bd6371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4e5a8fced4a91a234e459d3e86f70f0a875ef57ce7b3b2778200d6692f8cc1`

```dockerfile
```

-	Layers:
	-	`sha256:2121fb019fff014bbc612a435b5e0209feb68478ca72db18ce1d8ca584be271f`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 1.2 MB (1178529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a52d086952a00b69d128df0a14d1bdc11dfbe5c91859e833208040720b9d0efd`  
		Last Modified: Sat, 07 Sep 2024 07:03:05 GMT  
		Size: 17.4 KB (17382 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:856c91783f7d21012b38323b36991a4b415b148dcab362efe6d45ca221b9d692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18948633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882b8fdcf190add01c2dc00e479ba691543a23c72901c9b9581734e8ecbd4d80`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634141d08a7f2ae5a144da1847d931b4cc99514263aea51e764b222d536642bd`  
		Last Modified: Sat, 07 Sep 2024 20:33:42 GMT  
		Size: 9.6 MB (9645875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8a2a2ecd95ddd7ef0c9d83f432abab63b16ead3200fd2df5617cfd5b8f0e99`  
		Last Modified: Sat, 07 Sep 2024 20:33:40 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49e9fc5ff805842d79b092fb62541e430a9fdb5d1144f8a360cc2fc1171a61e`  
		Last Modified: Sat, 07 Sep 2024 20:33:41 GMT  
		Size: 5.9 MB (5930308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:3acf8b9addc44a281e26766672e6142aacb88117e08fb56734b09449033a5a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e863619e8a6d2f0955b1b8e1da7b02f294d705f526e5815a8d990aa430482ab2`

```dockerfile
```

-	Layers:
	-	`sha256:00b2eeaffa4b740f8aa8985162c83d7a26da17ff5e9c3bd70b0c62d8dc64788b`  
		Last Modified: Sat, 07 Sep 2024 20:33:41 GMT  
		Size: 1.2 MB (1178525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a3f803218dcbba5730579592f427070a871dd2311ce2e2ceb98ac94e033cdb3`  
		Last Modified: Sat, 07 Sep 2024 20:33:40 GMT  
		Size: 17.4 KB (17377 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:a9343811b921bf367edda23179c3a2567bc8c35339371a584986716c967d30fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20273410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386a4347853f194ac5a1aec08dc721a00fb5214f62aa6b5619bb97822cf8d8d7`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf007dfb739e6f45d5915a24bdaa5a2d439dd6e0b3b795852fdee75463ada95`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 10.8 MB (10753338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21af45072b07676ab768b93ba8bdbd6ea9039d1a189f72d756aef2f352d7f0af`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6f5d317148da6283d176e25e9078d039f9c168bb182f7d79b401a047fa5c44`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 6.1 MB (6057476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:c64fc2803cf39d52ca243caa6b69e23565bd37c6db576f2956d712bee758f118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e5d62029e06315a1f9d7c42efab99910196d2f0539c13839c2644d7722b7fc`

```dockerfile
```

-	Layers:
	-	`sha256:fa51fb87e83eeb4a26311a4273a680a426aad645be1a2b2166305da4793c83bc`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 1.2 MB (1178471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc9bd2b4610dbaf8c034897233371f6d76f0932f7276e254755a2a774162f786`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 17.3 KB (17316 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine3.20`

```console
$ docker pull irssi@sha256:8433cdf30e274988426352ad38712dc09f28c4c1768569d4588eea8dae437e60
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

### `irssi:1.4-alpine3.20` - linux; amd64

```console
$ docker pull irssi@sha256:225eeedb3d5df0d8342c28f28a67e14963a4a3f668754735ab50b36cf23849a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19723767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8718185e934cf00977ac16947769332a38a80ba94b1958d5134cc5096dddec`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c626f109cf0e2e5ee386344e1f4f1278bab9391d09e043d3f9afe609c04387`  
		Last Modified: Fri, 06 Sep 2024 23:21:57 GMT  
		Size: 10.2 MB (10191821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753e1b9dda433c6260ec07e1572c0120eeb2205ad32293eae47eaa0a81b43bfd`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fa96080be04b7162785b53e6197cf44a7906954d44de78eb0bbeb69eeac92e`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 5.9 MB (5907140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:187222cb890ac3b3f65f968a23c8375217deb65302025ca80d3bddd34aa6405a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1197741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ad74886f316acc6cfaebde6ff77de40ec17fd0107308bfb57973256f59e8d5`

```dockerfile
```

-	Layers:
	-	`sha256:f7ca62c1d6b0082fb2d26f943a081038469132453899545953a91012cd4e7375`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 1.2 MB (1180425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b77417a1071ef7e7085c110ce17cfa06c18b50cf1b1caf8ba006a14f926abb21`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 17.3 KB (17316 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.20` - linux; arm variant v6

```console
$ docker pull irssi@sha256:bc876fda49849676e70afc23dfc3e74c36da0c2a3745f5fd3c28a8aa9b8635b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18480137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf0c54c34c514e6637fbbdc3209d255343b87c65ed581f951673640306e1dac6`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4563366942775996dc7eff42d60df711ef73b0fbafbca9edb8d797024668c202`  
		Last Modified: Sat, 07 Sep 2024 02:40:26 GMT  
		Size: 9.4 MB (9362097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6b0c6e5c33e41b06fde0292dae092dc763b7e27b823ab7be705407c11384bd`  
		Last Modified: Sat, 07 Sep 2024 02:40:25 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcce1db33190250448077f9d4cd391b9ef2b6a67f7d2fa94f27bc0362e4894cd`  
		Last Modified: Sat, 07 Sep 2024 02:40:26 GMT  
		Size: 5.8 MB (5750537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:4d1617b7ab5430803bbd52362c57bb453d8dd4acaedf8bdde2447432a7ff9e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a999001bf9c39d625593692a3b737f6f3a0b814b3c4811047346af7fada502`

```dockerfile
```

-	Layers:
	-	`sha256:818f414539c29d70896c89b3932576101e8e18ce58a90487359afb4f38d44f5b`  
		Last Modified: Sat, 07 Sep 2024 02:40:25 GMT  
		Size: 17.2 KB (17221 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.20` - linux; arm variant v7

```console
$ docker pull irssi@sha256:1d02a8ed391c51bde9b27afde1ea4240cc487cf74dbf61e5d2efba692b2799f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17782449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053a71b3a279ad0e3a2e0d7dbbf4e54ad2278be015c7f288b5fd103a4d67c754`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0429f3169f57cf771d30f0b785f6c7a5ab02d43411f8d6f2344100a482351a48`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 9.2 MB (9183709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5dba3974eab46837cadb17dfa4a364e5da3b9bd43af9186c06744a8fd58a40`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f255b010ec76769301234a17a2d0bdd32e205d39407d7962c89e1a5c79b89851`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 5.5 MB (5502241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:14f64ac5066b5ca789c86b0625abe3210bf749b295085d8d92dd6af200205bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1200797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32f9747e49a5665b3336fd605ddcdacc76f8ada3a5d544863246fb41d31ad24`

```dockerfile
```

-	Layers:
	-	`sha256:35094785d6853a5f0461474df37f8127ad609827a2b89f696d94a63f97125283`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 1.2 MB (1183357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4d31524ff73face1950830eab2bd0ed7ec05e4012f74641a1b5a49010fc1998`  
		Last Modified: Sat, 07 Sep 2024 02:57:53 GMT  
		Size: 17.4 KB (17440 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:62e8dceafa5dcc45ea2419d86401fbf0824b7a4bae684d174ad74b52a78abf20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20053478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec1e645d1e32a1d6e4842461b9a9b6b03670618d7c7be7a3c59a8f9773ddd02`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad68fd7a6bae4d6a9f0791e9a8b0d89515ef68cc3b3bc2802082159c8f0b917`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 10.2 MB (10157951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1759a5bf2c0e097fe22b543d149e5fdcd014e7b5f039a9fdb8b9ba503d6be7f`  
		Last Modified: Sat, 07 Sep 2024 05:27:55 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0df7ac6458b3449bfc8746487857687df8de1d04144326f711d143f904e0da`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 5.8 MB (5806884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:964aec0691615b07c0f7cf64bd3c2aaf8e77f54ae96bd8ae41c132aa2d21c32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1198193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0846e8bd16a6800d33a45be72816781d99d14770119347a9b650981b6cf2073e`

```dockerfile
```

-	Layers:
	-	`sha256:fe65408852799879429a8939ccc5713fad8538db3615fa77035290c4b582c5ec`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 1.2 MB (1180529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d76afdd382391f2e7f0b7e5e52a8af475ce69ab9742ec727e6e0d04ed084114`  
		Last Modified: Sat, 07 Sep 2024 05:27:55 GMT  
		Size: 17.7 KB (17664 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.20` - linux; 386

```console
$ docker pull irssi@sha256:cec60383cb2114de36cc450b24a795c8b842ea3fe2b5d3ae261777966088981c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19101566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f9750cde5e598eddb25cb06de3196c475dfe940267f34c736aeebf2d606696`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fe8a84f82ad300ce90efce39dd06078babce03103f8b8fe54cdbafb1fbc1f5`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 9.6 MB (9637197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d066bbdeb2014769a48d8148c61e03de10dbfb7acd1ab85f2ded1e7fc00d4d`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52264d62ad1faa811627d0ed73c1b84f1ac7d0eb79bc1dfe11cf881039971566`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 6.0 MB (5994206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:8fa447d248e4470c90876cde43ba4113beae83308c1df0897cc7ef9aadc43c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1197639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e42131d18a25107b03a2c3896713f456d13455b6ae6538165e7722393cb301d`

```dockerfile
```

-	Layers:
	-	`sha256:9e6c0cce7fb0dd7e8aa2edbf38f26a85728a617a5dd3a52ad2b45f225e21aa48`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 1.2 MB (1180380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9529db747d4db3bf62950ed172f88b0bc2940614e0ca337601c634c09ba51f2`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 17.3 KB (17259 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.20` - linux; ppc64le

```console
$ docker pull irssi@sha256:f4295c16c15be6d6b002444faf906a4376f6a034f0fb10e7804ca1a0eb5a5d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20117357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612e050904415a82d96b010cd7125b10f3b535d204678ca2a9de0dfdd94b5bab`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf7f01d0ac0592b557f92ad27859bdcd34b46bd87f3357c86c81131ba4c1ac3`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 10.4 MB (10379021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e046fbadf0eb3f861ca076d737a51e9d3f8f54cf0fe5a50fd781332a42914a3`  
		Last Modified: Sat, 07 Sep 2024 07:03:05 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e93d1891687db40bc621f9c7c4b32ada1170a9c98951f1fe4aa315a844c730`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 6.2 MB (6164918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:ec763bbab32c460ad03421366a5aebc14cf613d6d45bb177fd44d671e3bd6371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4e5a8fced4a91a234e459d3e86f70f0a875ef57ce7b3b2778200d6692f8cc1`

```dockerfile
```

-	Layers:
	-	`sha256:2121fb019fff014bbc612a435b5e0209feb68478ca72db18ce1d8ca584be271f`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 1.2 MB (1178529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a52d086952a00b69d128df0a14d1bdc11dfbe5c91859e833208040720b9d0efd`  
		Last Modified: Sat, 07 Sep 2024 07:03:05 GMT  
		Size: 17.4 KB (17382 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.20` - linux; riscv64

```console
$ docker pull irssi@sha256:856c91783f7d21012b38323b36991a4b415b148dcab362efe6d45ca221b9d692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18948633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882b8fdcf190add01c2dc00e479ba691543a23c72901c9b9581734e8ecbd4d80`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634141d08a7f2ae5a144da1847d931b4cc99514263aea51e764b222d536642bd`  
		Last Modified: Sat, 07 Sep 2024 20:33:42 GMT  
		Size: 9.6 MB (9645875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8a2a2ecd95ddd7ef0c9d83f432abab63b16ead3200fd2df5617cfd5b8f0e99`  
		Last Modified: Sat, 07 Sep 2024 20:33:40 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49e9fc5ff805842d79b092fb62541e430a9fdb5d1144f8a360cc2fc1171a61e`  
		Last Modified: Sat, 07 Sep 2024 20:33:41 GMT  
		Size: 5.9 MB (5930308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:3acf8b9addc44a281e26766672e6142aacb88117e08fb56734b09449033a5a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e863619e8a6d2f0955b1b8e1da7b02f294d705f526e5815a8d990aa430482ab2`

```dockerfile
```

-	Layers:
	-	`sha256:00b2eeaffa4b740f8aa8985162c83d7a26da17ff5e9c3bd70b0c62d8dc64788b`  
		Last Modified: Sat, 07 Sep 2024 20:33:41 GMT  
		Size: 1.2 MB (1178525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a3f803218dcbba5730579592f427070a871dd2311ce2e2ceb98ac94e033cdb3`  
		Last Modified: Sat, 07 Sep 2024 20:33:40 GMT  
		Size: 17.4 KB (17377 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.20` - linux; s390x

```console
$ docker pull irssi@sha256:a9343811b921bf367edda23179c3a2567bc8c35339371a584986716c967d30fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20273410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386a4347853f194ac5a1aec08dc721a00fb5214f62aa6b5619bb97822cf8d8d7`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf007dfb739e6f45d5915a24bdaa5a2d439dd6e0b3b795852fdee75463ada95`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 10.8 MB (10753338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21af45072b07676ab768b93ba8bdbd6ea9039d1a189f72d756aef2f352d7f0af`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6f5d317148da6283d176e25e9078d039f9c168bb182f7d79b401a047fa5c44`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 6.1 MB (6057476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:c64fc2803cf39d52ca243caa6b69e23565bd37c6db576f2956d712bee758f118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e5d62029e06315a1f9d7c42efab99910196d2f0539c13839c2644d7722b7fc`

```dockerfile
```

-	Layers:
	-	`sha256:fa51fb87e83eeb4a26311a4273a680a426aad645be1a2b2166305da4793c83bc`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 1.2 MB (1178471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc9bd2b4610dbaf8c034897233371f6d76f0932f7276e254755a2a774162f786`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 17.3 KB (17316 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-bookworm`

```console
$ docker pull irssi@sha256:d843f5da94333b1e5b71252558cfc96bab350fe4b5ae651a74215574f5141d77
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `irssi:1.4-bookworm` - linux; amd64

```console
$ docker pull irssi@sha256:8aa50d7d3ea8f42fd43067cfbb6f0de50482d7d8e3db5a50fe2598628eb02cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51991262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a6601170dc20fcf1c200d8db92a1f1b4cb70798a9bad21d6347fec54cedd7d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb24a21ee06ae2e696f315794f60683badb1fd6322bffc2a0319d2af71210d22`  
		Last Modified: Thu, 17 Oct 2024 01:21:30 GMT  
		Size: 18.3 MB (18268738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdfe65b078593a20f4d8a6a2e19a8bf4630a32c9a7de2f322b2844f2d93d438`  
		Last Modified: Thu, 17 Oct 2024 01:21:29 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5809862e7f3e9acbbd4cfdb6fa307742f16800ba62916d52f094603dda824867`  
		Last Modified: Thu, 17 Oct 2024 01:21:30 GMT  
		Size: 4.6 MB (4592881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:b14643a76798849fc221cdbff8e7ea9154d43b8eb786152f7b09914b50cb4457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bd8878fc0ba19f6256e48b5d5f656828755ecf598b5a6c70ff014b3ee3fc7c`

```dockerfile
```

-	Layers:
	-	`sha256:f8074bdb984a9cbee8b0939fbd785951f79e4c40ec6e2cabf14987ab7c996ed9`  
		Last Modified: Thu, 17 Oct 2024 01:21:30 GMT  
		Size: 5.4 MB (5365679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:944a60539d43dccd726aaed7cd2f3bd293bed84744b2dc7741271b82951374aa`  
		Last Modified: Thu, 17 Oct 2024 01:21:29 GMT  
		Size: 18.6 KB (18554 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:e85a8d276df24059b698c6cc142a6506e446bfa77824eef8ce9bfa01e59a4de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48374514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8cf2dfca38be27dba04fd2515e55b60909c37be13165966482d40e007bdd01`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:c8ec8d65b2f61866a2c6085ed61e936733bc484abeeba1b91d12b9f6a97e456b in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e51d4479d9f15eaafec663087c05baede0a0724dc30787f7912ade3b686f46b1`  
		Last Modified: Thu, 17 Oct 2024 00:57:27 GMT  
		Size: 26.9 MB (26887306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df41522fb0d82bb74591eb0a6713b9bb3839d683778f8fab089fd229cbab932`  
		Last Modified: Thu, 17 Oct 2024 05:45:36 GMT  
		Size: 17.0 MB (17039325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fb9e3ff10a084e27b6bfc73e1c126d52dfb2770497d3af79313971c85d0e88`  
		Last Modified: Thu, 17 Oct 2024 05:45:35 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87475fcd2d3950e702cf8a915e34f0cc33b5d567947163f35f8b5ead687d17f`  
		Last Modified: Thu, 17 Oct 2024 05:45:35 GMT  
		Size: 4.4 MB (4444529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:d4fccfbe8c9851c23102ad85753a1eb2f86077bce99aef53d6de10c36ae00665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d43f272b6657e00c3e2aef48985598165862c59becd212cdcf2a6e41be557f1`

```dockerfile
```

-	Layers:
	-	`sha256:82a5e95b79e54c65b557fc48cafd3b3ad757a681ec457ab0dab4a03421e88b20`  
		Last Modified: Thu, 17 Oct 2024 05:45:35 GMT  
		Size: 5.4 MB (5367178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc81d93dc84be6d270a4b218df61a62925757a55ab8712283db916743c4d67ab`  
		Last Modified: Thu, 17 Oct 2024 05:45:35 GMT  
		Size: 18.7 KB (18682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:12ad8e850827d74e28bde549e45ac6beaa8651c36f70afc08919d4cbc542961e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45654435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a7c45209aca883ac274fb51ef1c0c0e6d936a981a6518d42daa02f83a6a278`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f348c2f61d7048f13bbb2bf7c6015111e9341c1b2a57bb0f51c370ca45bd907`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 16.6 MB (16633805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8267612072f179f1f84c6a626ad7269f297796bd2a5cdfe38e2610ff43c9ba38`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980a4fb6213eb64092401fc4580bd066eb7536f435211170043953cb5d550b1a`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 4.3 MB (4299079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:9262df858faf119c78f44abe577174119e92d426eb5afed88413643ce45f3cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c68652ec81e35444cd943d16301610be8a1e00177afd6de2925c6813f9f4bba1`

```dockerfile
```

-	Layers:
	-	`sha256:672662f58b1c37e76367c167633e8ad8b24c5071cbe5c947ff3858f8eace60da`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 5.4 MB (5367033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf4fc54a2dd30f7fa8311901fa81effc94562db647873e07c968866f1d5b4a66`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 18.7 KB (18682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f0a0f670eae231f1274d0e9e5097240e841843799dd4bab65297e68836f003d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51720933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad0d0f0c746e27f7c110a3107d75d817c44d4de8ae6606706e33d6296c240d3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fa218b665e0696e6cbbb7e15f224e210265c26d0938799bf2cb4ba9ddb5ed7`  
		Last Modified: Thu, 17 Oct 2024 13:13:59 GMT  
		Size: 18.0 MB (18048181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830a882aa3c01ae181d1aff028e2fbdd695f7cad16cadb69acec9ad7c6404b09`  
		Last Modified: Thu, 17 Oct 2024 13:13:58 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e603ba669c49ad6e8006dc9fd6517daadb6e830ee90614880f222bb717b5359`  
		Last Modified: Thu, 17 Oct 2024 13:13:59 GMT  
		Size: 4.5 MB (4513057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c90a647af8cbe3ce4e36bffff2ca2dfafe6905cc26bb80f77a68a6ef84a80cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5390891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227f292d79f3a8ec728ca0caa89f4bd85fda9ee2546c35bec4f4890158b19832`

```dockerfile
```

-	Layers:
	-	`sha256:1c3ef154ce409a963bb09794d072c2b1c34a7607ff31366904498b4bfd257aae`  
		Last Modified: Thu, 17 Oct 2024 13:13:59 GMT  
		Size: 5.4 MB (5372161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb2f7fe9f657bdaeb0daa90626317db717c17908e3e479b6e71a075ba1f6dfe0`  
		Last Modified: Thu, 17 Oct 2024 13:13:58 GMT  
		Size: 18.7 KB (18730 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:0456833f0dc5f5135063a36bcdfcad14dc427a41da7ff129bb03beca4950cc90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52561651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b622b093ac5b5bccce519dbcd83e5e38b1a80607e3fc8d044d24105bd88ad07f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108ff1f82b7d31627896ef9dfa4d55dd918dd899dc1d07d811f2a973ca493272`  
		Last Modified: Thu, 17 Oct 2024 01:21:25 GMT  
		Size: 17.8 MB (17807462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab24ea74320071af584210ffe42f29229a3c32d58f2fc6b39ce817b15e727ae`  
		Last Modified: Thu, 17 Oct 2024 01:21:24 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e92c1d542ec81f26c5c8944a9622b196df4a3c8a7130c9b8d03f6a1c1601e6`  
		Last Modified: Thu, 17 Oct 2024 01:21:24 GMT  
		Size: 4.6 MB (4606565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:3ec4be7da4181fdbeb6ab8972993b6a1b52b0f88152c7c6a3bee462bfbddce93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5380258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065781f2809ba4e58b52f7baf61a835fd97eebf699650f381a447202796234b7`

```dockerfile
```

-	Layers:
	-	`sha256:75eeb53340b15ef46774f8a563ed54455d45ba0e527466054dec23fddd1ea9d1`  
		Last Modified: Thu, 17 Oct 2024 01:21:24 GMT  
		Size: 5.4 MB (5361757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa627aa524b4d75732bb320f5907ea045cd6c3c40af27a99c07e097375bba8fc`  
		Last Modified: Thu, 17 Oct 2024 01:21:24 GMT  
		Size: 18.5 KB (18501 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:291d87011c5c636d069d6f74c6796c03d2208d050713b23db2a301c6a54bc9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50633180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e6aa70a891ce32f5488c0353e6f02facfb108db6ba13dfb255a05038802c24`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:673970f358f62b6b095139e9647b41b9af839d4e01f7698755b040f471ff80b2 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:75358c79454e0fed44aa25dd323536443b4a1230fc432aa226620e470d72cf5f`  
		Last Modified: Fri, 27 Sep 2024 09:11:36 GMT  
		Size: 29.1 MB (29124858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d53fbf788bd0e7b28f97c4dc927f8ab5bc32596e4d316d1e4107d63df122e3`  
		Last Modified: Fri, 27 Sep 2024 23:25:12 GMT  
		Size: 16.9 MB (16949902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2858574a09072d459734ac302f8784ee2119cd1028b5d0e81359d03e7693743`  
		Last Modified: Fri, 27 Sep 2024 23:25:10 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86aa9a6bf5e9b33a0ce592db709ac8916b028b333caa0bbdb8fba1bd2f6214cd`  
		Last Modified: Fri, 27 Sep 2024 23:25:11 GMT  
		Size: 4.6 MB (4555066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:7b17417d51f41d70cde36d9d968c36209ddd5246b2e9a87b8841b2c1aaee76fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bd0d67639923b725e3575a86ab49679b4125e46a54d6d4697146278f381a88`

```dockerfile
```

-	Layers:
	-	`sha256:55950ecb6cc8539508cfd44c53f5ad3fe2fb065c30a19cc098db41c8cf9a68da`  
		Last Modified: Fri, 27 Sep 2024 23:25:10 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:9e802780529f1ac8dc9e2a4e005a33691d9392e00937ff96d0605832f9bebbd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56730477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802dbfec090fbf25a29b5a6497cf1b84626e3b8445a70448f5e978e66beb8135`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c9398d733e6504c746da92179ca87ad112a632322da102a80b7fcfb289570b`  
		Last Modified: Thu, 17 Oct 2024 08:39:47 GMT  
		Size: 18.8 MB (18776314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29a43ed635481a1588bff095c3612c8656bc784fe29d6e2775b4687f0754952`  
		Last Modified: Thu, 17 Oct 2024 08:39:46 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4012dfdba364ca794130d1dffd077292fcb38350f73fb6278877bd25d2d8c7fc`  
		Last Modified: Thu, 17 Oct 2024 08:39:47 GMT  
		Size: 4.8 MB (4828605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:1a5fd59e01471305d46ac075911b975e8aeb9c14be98e8c2e4441ce1de6d6bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80260c15ff6e7c8aadd796f8e69434fca49c016e38b7c433fb18d14cca2bd504`

```dockerfile
```

-	Layers:
	-	`sha256:25819b0bf172f91e1cd05bc76766c461bdf1e8521e7ae7c7a0a8bbc22ca147bf`  
		Last Modified: Thu, 17 Oct 2024 08:39:47 GMT  
		Size: 5.4 MB (5373373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:354ff742b1d00d43544704361eebfaace5714e6f96f4e66b0313e9d1267af98c`  
		Last Modified: Thu, 17 Oct 2024 08:39:46 GMT  
		Size: 18.6 KB (18620 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:62d3dfafa7f8ea785b17fac4aeab1d35709c0631816835fa6904e57e336d1582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50307925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9113e290344eed8b5c9217ede2fd0b90f7b73c19455deaf66a2c37498fea6f3f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc28589ea18c5147d2150e6c305d805ff80ab242c5f64ebff3fa07cd244b1e20`  
		Last Modified: Thu, 17 Oct 2024 13:15:53 GMT  
		Size: 18.2 MB (18227811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e4c1d1c7203ba73e3baed860511382dcaba23fb316575e5b4a68aea09ad8ce`  
		Last Modified: Thu, 17 Oct 2024 13:15:52 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16802b2f05ed3d331e4ca172c0f5e0e78f969f531b192c9cab2b79fa17ca9320`  
		Last Modified: Thu, 17 Oct 2024 13:15:53 GMT  
		Size: 4.6 MB (4586676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:e5ddc58cf0baeb33e18378e5729dfafea51d5d9e6abf4ba9d3e48d5e8ea96eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5383534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548345c85d4ac645fd695bb4f1236c309665e73904bacdded8fab6976d751206`

```dockerfile
```

-	Layers:
	-	`sha256:bf5ab0e8e73932f8aba43d1f7ce78795c90e0123ee9735706a911813cc3d5fdb`  
		Last Modified: Thu, 17 Oct 2024 13:15:53 GMT  
		Size: 5.4 MB (5364980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6966e3fc81ec6a47d7dba5ee8184f4a0d792e39d59ee9ab2e594cb8c3dfe2f1a`  
		Last Modified: Thu, 17 Oct 2024 13:15:52 GMT  
		Size: 18.6 KB (18554 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5`

```console
$ docker pull irssi@sha256:d843f5da94333b1e5b71252558cfc96bab350fe4b5ae651a74215574f5141d77
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `irssi:1.4.5` - linux; amd64

```console
$ docker pull irssi@sha256:8aa50d7d3ea8f42fd43067cfbb6f0de50482d7d8e3db5a50fe2598628eb02cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51991262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a6601170dc20fcf1c200d8db92a1f1b4cb70798a9bad21d6347fec54cedd7d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb24a21ee06ae2e696f315794f60683badb1fd6322bffc2a0319d2af71210d22`  
		Last Modified: Thu, 17 Oct 2024 01:21:30 GMT  
		Size: 18.3 MB (18268738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdfe65b078593a20f4d8a6a2e19a8bf4630a32c9a7de2f322b2844f2d93d438`  
		Last Modified: Thu, 17 Oct 2024 01:21:29 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5809862e7f3e9acbbd4cfdb6fa307742f16800ba62916d52f094603dda824867`  
		Last Modified: Thu, 17 Oct 2024 01:21:30 GMT  
		Size: 4.6 MB (4592881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:b14643a76798849fc221cdbff8e7ea9154d43b8eb786152f7b09914b50cb4457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bd8878fc0ba19f6256e48b5d5f656828755ecf598b5a6c70ff014b3ee3fc7c`

```dockerfile
```

-	Layers:
	-	`sha256:f8074bdb984a9cbee8b0939fbd785951f79e4c40ec6e2cabf14987ab7c996ed9`  
		Last Modified: Thu, 17 Oct 2024 01:21:30 GMT  
		Size: 5.4 MB (5365679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:944a60539d43dccd726aaed7cd2f3bd293bed84744b2dc7741271b82951374aa`  
		Last Modified: Thu, 17 Oct 2024 01:21:29 GMT  
		Size: 18.6 KB (18554 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v5

```console
$ docker pull irssi@sha256:e85a8d276df24059b698c6cc142a6506e446bfa77824eef8ce9bfa01e59a4de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48374514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8cf2dfca38be27dba04fd2515e55b60909c37be13165966482d40e007bdd01`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:c8ec8d65b2f61866a2c6085ed61e936733bc484abeeba1b91d12b9f6a97e456b in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e51d4479d9f15eaafec663087c05baede0a0724dc30787f7912ade3b686f46b1`  
		Last Modified: Thu, 17 Oct 2024 00:57:27 GMT  
		Size: 26.9 MB (26887306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df41522fb0d82bb74591eb0a6713b9bb3839d683778f8fab089fd229cbab932`  
		Last Modified: Thu, 17 Oct 2024 05:45:36 GMT  
		Size: 17.0 MB (17039325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fb9e3ff10a084e27b6bfc73e1c126d52dfb2770497d3af79313971c85d0e88`  
		Last Modified: Thu, 17 Oct 2024 05:45:35 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87475fcd2d3950e702cf8a915e34f0cc33b5d567947163f35f8b5ead687d17f`  
		Last Modified: Thu, 17 Oct 2024 05:45:35 GMT  
		Size: 4.4 MB (4444529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:d4fccfbe8c9851c23102ad85753a1eb2f86077bce99aef53d6de10c36ae00665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d43f272b6657e00c3e2aef48985598165862c59becd212cdcf2a6e41be557f1`

```dockerfile
```

-	Layers:
	-	`sha256:82a5e95b79e54c65b557fc48cafd3b3ad757a681ec457ab0dab4a03421e88b20`  
		Last Modified: Thu, 17 Oct 2024 05:45:35 GMT  
		Size: 5.4 MB (5367178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc81d93dc84be6d270a4b218df61a62925757a55ab8712283db916743c4d67ab`  
		Last Modified: Thu, 17 Oct 2024 05:45:35 GMT  
		Size: 18.7 KB (18682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v7

```console
$ docker pull irssi@sha256:12ad8e850827d74e28bde549e45ac6beaa8651c36f70afc08919d4cbc542961e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45654435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a7c45209aca883ac274fb51ef1c0c0e6d936a981a6518d42daa02f83a6a278`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f348c2f61d7048f13bbb2bf7c6015111e9341c1b2a57bb0f51c370ca45bd907`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 16.6 MB (16633805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8267612072f179f1f84c6a626ad7269f297796bd2a5cdfe38e2610ff43c9ba38`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980a4fb6213eb64092401fc4580bd066eb7536f435211170043953cb5d550b1a`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 4.3 MB (4299079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:9262df858faf119c78f44abe577174119e92d426eb5afed88413643ce45f3cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c68652ec81e35444cd943d16301610be8a1e00177afd6de2925c6813f9f4bba1`

```dockerfile
```

-	Layers:
	-	`sha256:672662f58b1c37e76367c167633e8ad8b24c5071cbe5c947ff3858f8eace60da`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 5.4 MB (5367033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf4fc54a2dd30f7fa8311901fa81effc94562db647873e07c968866f1d5b4a66`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 18.7 KB (18682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f0a0f670eae231f1274d0e9e5097240e841843799dd4bab65297e68836f003d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51720933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad0d0f0c746e27f7c110a3107d75d817c44d4de8ae6606706e33d6296c240d3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fa218b665e0696e6cbbb7e15f224e210265c26d0938799bf2cb4ba9ddb5ed7`  
		Last Modified: Thu, 17 Oct 2024 13:13:59 GMT  
		Size: 18.0 MB (18048181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830a882aa3c01ae181d1aff028e2fbdd695f7cad16cadb69acec9ad7c6404b09`  
		Last Modified: Thu, 17 Oct 2024 13:13:58 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e603ba669c49ad6e8006dc9fd6517daadb6e830ee90614880f222bb717b5359`  
		Last Modified: Thu, 17 Oct 2024 13:13:59 GMT  
		Size: 4.5 MB (4513057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:c90a647af8cbe3ce4e36bffff2ca2dfafe6905cc26bb80f77a68a6ef84a80cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5390891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227f292d79f3a8ec728ca0caa89f4bd85fda9ee2546c35bec4f4890158b19832`

```dockerfile
```

-	Layers:
	-	`sha256:1c3ef154ce409a963bb09794d072c2b1c34a7607ff31366904498b4bfd257aae`  
		Last Modified: Thu, 17 Oct 2024 13:13:59 GMT  
		Size: 5.4 MB (5372161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb2f7fe9f657bdaeb0daa90626317db717c17908e3e479b6e71a075ba1f6dfe0`  
		Last Modified: Thu, 17 Oct 2024 13:13:58 GMT  
		Size: 18.7 KB (18730 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; 386

```console
$ docker pull irssi@sha256:0456833f0dc5f5135063a36bcdfcad14dc427a41da7ff129bb03beca4950cc90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52561651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b622b093ac5b5bccce519dbcd83e5e38b1a80607e3fc8d044d24105bd88ad07f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108ff1f82b7d31627896ef9dfa4d55dd918dd899dc1d07d811f2a973ca493272`  
		Last Modified: Thu, 17 Oct 2024 01:21:25 GMT  
		Size: 17.8 MB (17807462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab24ea74320071af584210ffe42f29229a3c32d58f2fc6b39ce817b15e727ae`  
		Last Modified: Thu, 17 Oct 2024 01:21:24 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e92c1d542ec81f26c5c8944a9622b196df4a3c8a7130c9b8d03f6a1c1601e6`  
		Last Modified: Thu, 17 Oct 2024 01:21:24 GMT  
		Size: 4.6 MB (4606565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:3ec4be7da4181fdbeb6ab8972993b6a1b52b0f88152c7c6a3bee462bfbddce93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5380258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065781f2809ba4e58b52f7baf61a835fd97eebf699650f381a447202796234b7`

```dockerfile
```

-	Layers:
	-	`sha256:75eeb53340b15ef46774f8a563ed54455d45ba0e527466054dec23fddd1ea9d1`  
		Last Modified: Thu, 17 Oct 2024 01:21:24 GMT  
		Size: 5.4 MB (5361757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa627aa524b4d75732bb320f5907ea045cd6c3c40af27a99c07e097375bba8fc`  
		Last Modified: Thu, 17 Oct 2024 01:21:24 GMT  
		Size: 18.5 KB (18501 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; mips64le

```console
$ docker pull irssi@sha256:291d87011c5c636d069d6f74c6796c03d2208d050713b23db2a301c6a54bc9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50633180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e6aa70a891ce32f5488c0353e6f02facfb108db6ba13dfb255a05038802c24`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:673970f358f62b6b095139e9647b41b9af839d4e01f7698755b040f471ff80b2 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:75358c79454e0fed44aa25dd323536443b4a1230fc432aa226620e470d72cf5f`  
		Last Modified: Fri, 27 Sep 2024 09:11:36 GMT  
		Size: 29.1 MB (29124858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d53fbf788bd0e7b28f97c4dc927f8ab5bc32596e4d316d1e4107d63df122e3`  
		Last Modified: Fri, 27 Sep 2024 23:25:12 GMT  
		Size: 16.9 MB (16949902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2858574a09072d459734ac302f8784ee2119cd1028b5d0e81359d03e7693743`  
		Last Modified: Fri, 27 Sep 2024 23:25:10 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86aa9a6bf5e9b33a0ce592db709ac8916b028b333caa0bbdb8fba1bd2f6214cd`  
		Last Modified: Fri, 27 Sep 2024 23:25:11 GMT  
		Size: 4.6 MB (4555066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:7b17417d51f41d70cde36d9d968c36209ddd5246b2e9a87b8841b2c1aaee76fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bd0d67639923b725e3575a86ab49679b4125e46a54d6d4697146278f381a88`

```dockerfile
```

-	Layers:
	-	`sha256:55950ecb6cc8539508cfd44c53f5ad3fe2fb065c30a19cc098db41c8cf9a68da`  
		Last Modified: Fri, 27 Sep 2024 23:25:10 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; ppc64le

```console
$ docker pull irssi@sha256:9e802780529f1ac8dc9e2a4e005a33691d9392e00937ff96d0605832f9bebbd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56730477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802dbfec090fbf25a29b5a6497cf1b84626e3b8445a70448f5e978e66beb8135`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c9398d733e6504c746da92179ca87ad112a632322da102a80b7fcfb289570b`  
		Last Modified: Thu, 17 Oct 2024 08:39:47 GMT  
		Size: 18.8 MB (18776314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29a43ed635481a1588bff095c3612c8656bc784fe29d6e2775b4687f0754952`  
		Last Modified: Thu, 17 Oct 2024 08:39:46 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4012dfdba364ca794130d1dffd077292fcb38350f73fb6278877bd25d2d8c7fc`  
		Last Modified: Thu, 17 Oct 2024 08:39:47 GMT  
		Size: 4.8 MB (4828605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:1a5fd59e01471305d46ac075911b975e8aeb9c14be98e8c2e4441ce1de6d6bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80260c15ff6e7c8aadd796f8e69434fca49c016e38b7c433fb18d14cca2bd504`

```dockerfile
```

-	Layers:
	-	`sha256:25819b0bf172f91e1cd05bc76766c461bdf1e8521e7ae7c7a0a8bbc22ca147bf`  
		Last Modified: Thu, 17 Oct 2024 08:39:47 GMT  
		Size: 5.4 MB (5373373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:354ff742b1d00d43544704361eebfaace5714e6f96f4e66b0313e9d1267af98c`  
		Last Modified: Thu, 17 Oct 2024 08:39:46 GMT  
		Size: 18.6 KB (18620 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; s390x

```console
$ docker pull irssi@sha256:62d3dfafa7f8ea785b17fac4aeab1d35709c0631816835fa6904e57e336d1582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50307925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9113e290344eed8b5c9217ede2fd0b90f7b73c19455deaf66a2c37498fea6f3f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc28589ea18c5147d2150e6c305d805ff80ab242c5f64ebff3fa07cd244b1e20`  
		Last Modified: Thu, 17 Oct 2024 13:15:53 GMT  
		Size: 18.2 MB (18227811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e4c1d1c7203ba73e3baed860511382dcaba23fb316575e5b4a68aea09ad8ce`  
		Last Modified: Thu, 17 Oct 2024 13:15:52 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16802b2f05ed3d331e4ca172c0f5e0e78f969f531b192c9cab2b79fa17ca9320`  
		Last Modified: Thu, 17 Oct 2024 13:15:53 GMT  
		Size: 4.6 MB (4586676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:e5ddc58cf0baeb33e18378e5729dfafea51d5d9e6abf4ba9d3e48d5e8ea96eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5383534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548345c85d4ac645fd695bb4f1236c309665e73904bacdded8fab6976d751206`

```dockerfile
```

-	Layers:
	-	`sha256:bf5ab0e8e73932f8aba43d1f7ce78795c90e0123ee9735706a911813cc3d5fdb`  
		Last Modified: Thu, 17 Oct 2024 13:15:53 GMT  
		Size: 5.4 MB (5364980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6966e3fc81ec6a47d7dba5ee8184f4a0d792e39d59ee9ab2e594cb8c3dfe2f1a`  
		Last Modified: Thu, 17 Oct 2024 13:15:52 GMT  
		Size: 18.6 KB (18554 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine`

```console
$ docker pull irssi@sha256:8433cdf30e274988426352ad38712dc09f28c4c1768569d4588eea8dae437e60
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
$ docker pull irssi@sha256:225eeedb3d5df0d8342c28f28a67e14963a4a3f668754735ab50b36cf23849a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19723767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8718185e934cf00977ac16947769332a38a80ba94b1958d5134cc5096dddec`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c626f109cf0e2e5ee386344e1f4f1278bab9391d09e043d3f9afe609c04387`  
		Last Modified: Fri, 06 Sep 2024 23:21:57 GMT  
		Size: 10.2 MB (10191821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753e1b9dda433c6260ec07e1572c0120eeb2205ad32293eae47eaa0a81b43bfd`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fa96080be04b7162785b53e6197cf44a7906954d44de78eb0bbeb69eeac92e`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 5.9 MB (5907140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:187222cb890ac3b3f65f968a23c8375217deb65302025ca80d3bddd34aa6405a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1197741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ad74886f316acc6cfaebde6ff77de40ec17fd0107308bfb57973256f59e8d5`

```dockerfile
```

-	Layers:
	-	`sha256:f7ca62c1d6b0082fb2d26f943a081038469132453899545953a91012cd4e7375`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 1.2 MB (1180425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b77417a1071ef7e7085c110ce17cfa06c18b50cf1b1caf8ba006a14f926abb21`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 17.3 KB (17316 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:bc876fda49849676e70afc23dfc3e74c36da0c2a3745f5fd3c28a8aa9b8635b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18480137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf0c54c34c514e6637fbbdc3209d255343b87c65ed581f951673640306e1dac6`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4563366942775996dc7eff42d60df711ef73b0fbafbca9edb8d797024668c202`  
		Last Modified: Sat, 07 Sep 2024 02:40:26 GMT  
		Size: 9.4 MB (9362097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6b0c6e5c33e41b06fde0292dae092dc763b7e27b823ab7be705407c11384bd`  
		Last Modified: Sat, 07 Sep 2024 02:40:25 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcce1db33190250448077f9d4cd391b9ef2b6a67f7d2fa94f27bc0362e4894cd`  
		Last Modified: Sat, 07 Sep 2024 02:40:26 GMT  
		Size: 5.8 MB (5750537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:4d1617b7ab5430803bbd52362c57bb453d8dd4acaedf8bdde2447432a7ff9e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a999001bf9c39d625593692a3b737f6f3a0b814b3c4811047346af7fada502`

```dockerfile
```

-	Layers:
	-	`sha256:818f414539c29d70896c89b3932576101e8e18ce58a90487359afb4f38d44f5b`  
		Last Modified: Sat, 07 Sep 2024 02:40:25 GMT  
		Size: 17.2 KB (17221 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:1d02a8ed391c51bde9b27afde1ea4240cc487cf74dbf61e5d2efba692b2799f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17782449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053a71b3a279ad0e3a2e0d7dbbf4e54ad2278be015c7f288b5fd103a4d67c754`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0429f3169f57cf771d30f0b785f6c7a5ab02d43411f8d6f2344100a482351a48`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 9.2 MB (9183709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5dba3974eab46837cadb17dfa4a364e5da3b9bd43af9186c06744a8fd58a40`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f255b010ec76769301234a17a2d0bdd32e205d39407d7962c89e1a5c79b89851`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 5.5 MB (5502241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:14f64ac5066b5ca789c86b0625abe3210bf749b295085d8d92dd6af200205bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1200797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32f9747e49a5665b3336fd605ddcdacc76f8ada3a5d544863246fb41d31ad24`

```dockerfile
```

-	Layers:
	-	`sha256:35094785d6853a5f0461474df37f8127ad609827a2b89f696d94a63f97125283`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 1.2 MB (1183357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4d31524ff73face1950830eab2bd0ed7ec05e4012f74641a1b5a49010fc1998`  
		Last Modified: Sat, 07 Sep 2024 02:57:53 GMT  
		Size: 17.4 KB (17440 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:62e8dceafa5dcc45ea2419d86401fbf0824b7a4bae684d174ad74b52a78abf20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20053478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec1e645d1e32a1d6e4842461b9a9b6b03670618d7c7be7a3c59a8f9773ddd02`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad68fd7a6bae4d6a9f0791e9a8b0d89515ef68cc3b3bc2802082159c8f0b917`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 10.2 MB (10157951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1759a5bf2c0e097fe22b543d149e5fdcd014e7b5f039a9fdb8b9ba503d6be7f`  
		Last Modified: Sat, 07 Sep 2024 05:27:55 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0df7ac6458b3449bfc8746487857687df8de1d04144326f711d143f904e0da`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 5.8 MB (5806884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:964aec0691615b07c0f7cf64bd3c2aaf8e77f54ae96bd8ae41c132aa2d21c32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1198193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0846e8bd16a6800d33a45be72816781d99d14770119347a9b650981b6cf2073e`

```dockerfile
```

-	Layers:
	-	`sha256:fe65408852799879429a8939ccc5713fad8538db3615fa77035290c4b582c5ec`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 1.2 MB (1180529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d76afdd382391f2e7f0b7e5e52a8af475ce69ab9742ec727e6e0d04ed084114`  
		Last Modified: Sat, 07 Sep 2024 05:27:55 GMT  
		Size: 17.7 KB (17664 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; 386

```console
$ docker pull irssi@sha256:cec60383cb2114de36cc450b24a795c8b842ea3fe2b5d3ae261777966088981c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19101566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f9750cde5e598eddb25cb06de3196c475dfe940267f34c736aeebf2d606696`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fe8a84f82ad300ce90efce39dd06078babce03103f8b8fe54cdbafb1fbc1f5`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 9.6 MB (9637197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d066bbdeb2014769a48d8148c61e03de10dbfb7acd1ab85f2ded1e7fc00d4d`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52264d62ad1faa811627d0ed73c1b84f1ac7d0eb79bc1dfe11cf881039971566`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 6.0 MB (5994206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:8fa447d248e4470c90876cde43ba4113beae83308c1df0897cc7ef9aadc43c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1197639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e42131d18a25107b03a2c3896713f456d13455b6ae6538165e7722393cb301d`

```dockerfile
```

-	Layers:
	-	`sha256:9e6c0cce7fb0dd7e8aa2edbf38f26a85728a617a5dd3a52ad2b45f225e21aa48`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 1.2 MB (1180380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9529db747d4db3bf62950ed172f88b0bc2940614e0ca337601c634c09ba51f2`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 17.3 KB (17259 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:f4295c16c15be6d6b002444faf906a4376f6a034f0fb10e7804ca1a0eb5a5d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20117357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612e050904415a82d96b010cd7125b10f3b535d204678ca2a9de0dfdd94b5bab`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf7f01d0ac0592b557f92ad27859bdcd34b46bd87f3357c86c81131ba4c1ac3`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 10.4 MB (10379021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e046fbadf0eb3f861ca076d737a51e9d3f8f54cf0fe5a50fd781332a42914a3`  
		Last Modified: Sat, 07 Sep 2024 07:03:05 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e93d1891687db40bc621f9c7c4b32ada1170a9c98951f1fe4aa315a844c730`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 6.2 MB (6164918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:ec763bbab32c460ad03421366a5aebc14cf613d6d45bb177fd44d671e3bd6371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4e5a8fced4a91a234e459d3e86f70f0a875ef57ce7b3b2778200d6692f8cc1`

```dockerfile
```

-	Layers:
	-	`sha256:2121fb019fff014bbc612a435b5e0209feb68478ca72db18ce1d8ca584be271f`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 1.2 MB (1178529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a52d086952a00b69d128df0a14d1bdc11dfbe5c91859e833208040720b9d0efd`  
		Last Modified: Sat, 07 Sep 2024 07:03:05 GMT  
		Size: 17.4 KB (17382 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:856c91783f7d21012b38323b36991a4b415b148dcab362efe6d45ca221b9d692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18948633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882b8fdcf190add01c2dc00e479ba691543a23c72901c9b9581734e8ecbd4d80`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634141d08a7f2ae5a144da1847d931b4cc99514263aea51e764b222d536642bd`  
		Last Modified: Sat, 07 Sep 2024 20:33:42 GMT  
		Size: 9.6 MB (9645875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8a2a2ecd95ddd7ef0c9d83f432abab63b16ead3200fd2df5617cfd5b8f0e99`  
		Last Modified: Sat, 07 Sep 2024 20:33:40 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49e9fc5ff805842d79b092fb62541e430a9fdb5d1144f8a360cc2fc1171a61e`  
		Last Modified: Sat, 07 Sep 2024 20:33:41 GMT  
		Size: 5.9 MB (5930308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:3acf8b9addc44a281e26766672e6142aacb88117e08fb56734b09449033a5a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e863619e8a6d2f0955b1b8e1da7b02f294d705f526e5815a8d990aa430482ab2`

```dockerfile
```

-	Layers:
	-	`sha256:00b2eeaffa4b740f8aa8985162c83d7a26da17ff5e9c3bd70b0c62d8dc64788b`  
		Last Modified: Sat, 07 Sep 2024 20:33:41 GMT  
		Size: 1.2 MB (1178525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a3f803218dcbba5730579592f427070a871dd2311ce2e2ceb98ac94e033cdb3`  
		Last Modified: Sat, 07 Sep 2024 20:33:40 GMT  
		Size: 17.4 KB (17377 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:a9343811b921bf367edda23179c3a2567bc8c35339371a584986716c967d30fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20273410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386a4347853f194ac5a1aec08dc721a00fb5214f62aa6b5619bb97822cf8d8d7`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf007dfb739e6f45d5915a24bdaa5a2d439dd6e0b3b795852fdee75463ada95`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 10.8 MB (10753338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21af45072b07676ab768b93ba8bdbd6ea9039d1a189f72d756aef2f352d7f0af`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6f5d317148da6283d176e25e9078d039f9c168bb182f7d79b401a047fa5c44`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 6.1 MB (6057476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:c64fc2803cf39d52ca243caa6b69e23565bd37c6db576f2956d712bee758f118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e5d62029e06315a1f9d7c42efab99910196d2f0539c13839c2644d7722b7fc`

```dockerfile
```

-	Layers:
	-	`sha256:fa51fb87e83eeb4a26311a4273a680a426aad645be1a2b2166305da4793c83bc`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 1.2 MB (1178471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc9bd2b4610dbaf8c034897233371f6d76f0932f7276e254755a2a774162f786`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 17.3 KB (17316 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine3.20`

```console
$ docker pull irssi@sha256:8433cdf30e274988426352ad38712dc09f28c4c1768569d4588eea8dae437e60
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

### `irssi:1.4.5-alpine3.20` - linux; amd64

```console
$ docker pull irssi@sha256:225eeedb3d5df0d8342c28f28a67e14963a4a3f668754735ab50b36cf23849a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19723767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8718185e934cf00977ac16947769332a38a80ba94b1958d5134cc5096dddec`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c626f109cf0e2e5ee386344e1f4f1278bab9391d09e043d3f9afe609c04387`  
		Last Modified: Fri, 06 Sep 2024 23:21:57 GMT  
		Size: 10.2 MB (10191821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753e1b9dda433c6260ec07e1572c0120eeb2205ad32293eae47eaa0a81b43bfd`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fa96080be04b7162785b53e6197cf44a7906954d44de78eb0bbeb69eeac92e`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 5.9 MB (5907140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:187222cb890ac3b3f65f968a23c8375217deb65302025ca80d3bddd34aa6405a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1197741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ad74886f316acc6cfaebde6ff77de40ec17fd0107308bfb57973256f59e8d5`

```dockerfile
```

-	Layers:
	-	`sha256:f7ca62c1d6b0082fb2d26f943a081038469132453899545953a91012cd4e7375`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 1.2 MB (1180425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b77417a1071ef7e7085c110ce17cfa06c18b50cf1b1caf8ba006a14f926abb21`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 17.3 KB (17316 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.20` - linux; arm variant v6

```console
$ docker pull irssi@sha256:bc876fda49849676e70afc23dfc3e74c36da0c2a3745f5fd3c28a8aa9b8635b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18480137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf0c54c34c514e6637fbbdc3209d255343b87c65ed581f951673640306e1dac6`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4563366942775996dc7eff42d60df711ef73b0fbafbca9edb8d797024668c202`  
		Last Modified: Sat, 07 Sep 2024 02:40:26 GMT  
		Size: 9.4 MB (9362097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6b0c6e5c33e41b06fde0292dae092dc763b7e27b823ab7be705407c11384bd`  
		Last Modified: Sat, 07 Sep 2024 02:40:25 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcce1db33190250448077f9d4cd391b9ef2b6a67f7d2fa94f27bc0362e4894cd`  
		Last Modified: Sat, 07 Sep 2024 02:40:26 GMT  
		Size: 5.8 MB (5750537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:4d1617b7ab5430803bbd52362c57bb453d8dd4acaedf8bdde2447432a7ff9e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a999001bf9c39d625593692a3b737f6f3a0b814b3c4811047346af7fada502`

```dockerfile
```

-	Layers:
	-	`sha256:818f414539c29d70896c89b3932576101e8e18ce58a90487359afb4f38d44f5b`  
		Last Modified: Sat, 07 Sep 2024 02:40:25 GMT  
		Size: 17.2 KB (17221 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.20` - linux; arm variant v7

```console
$ docker pull irssi@sha256:1d02a8ed391c51bde9b27afde1ea4240cc487cf74dbf61e5d2efba692b2799f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17782449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053a71b3a279ad0e3a2e0d7dbbf4e54ad2278be015c7f288b5fd103a4d67c754`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0429f3169f57cf771d30f0b785f6c7a5ab02d43411f8d6f2344100a482351a48`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 9.2 MB (9183709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5dba3974eab46837cadb17dfa4a364e5da3b9bd43af9186c06744a8fd58a40`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f255b010ec76769301234a17a2d0bdd32e205d39407d7962c89e1a5c79b89851`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 5.5 MB (5502241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:14f64ac5066b5ca789c86b0625abe3210bf749b295085d8d92dd6af200205bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1200797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32f9747e49a5665b3336fd605ddcdacc76f8ada3a5d544863246fb41d31ad24`

```dockerfile
```

-	Layers:
	-	`sha256:35094785d6853a5f0461474df37f8127ad609827a2b89f696d94a63f97125283`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 1.2 MB (1183357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4d31524ff73face1950830eab2bd0ed7ec05e4012f74641a1b5a49010fc1998`  
		Last Modified: Sat, 07 Sep 2024 02:57:53 GMT  
		Size: 17.4 KB (17440 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:62e8dceafa5dcc45ea2419d86401fbf0824b7a4bae684d174ad74b52a78abf20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20053478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec1e645d1e32a1d6e4842461b9a9b6b03670618d7c7be7a3c59a8f9773ddd02`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad68fd7a6bae4d6a9f0791e9a8b0d89515ef68cc3b3bc2802082159c8f0b917`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 10.2 MB (10157951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1759a5bf2c0e097fe22b543d149e5fdcd014e7b5f039a9fdb8b9ba503d6be7f`  
		Last Modified: Sat, 07 Sep 2024 05:27:55 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0df7ac6458b3449bfc8746487857687df8de1d04144326f711d143f904e0da`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 5.8 MB (5806884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:964aec0691615b07c0f7cf64bd3c2aaf8e77f54ae96bd8ae41c132aa2d21c32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1198193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0846e8bd16a6800d33a45be72816781d99d14770119347a9b650981b6cf2073e`

```dockerfile
```

-	Layers:
	-	`sha256:fe65408852799879429a8939ccc5713fad8538db3615fa77035290c4b582c5ec`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 1.2 MB (1180529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d76afdd382391f2e7f0b7e5e52a8af475ce69ab9742ec727e6e0d04ed084114`  
		Last Modified: Sat, 07 Sep 2024 05:27:55 GMT  
		Size: 17.7 KB (17664 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.20` - linux; 386

```console
$ docker pull irssi@sha256:cec60383cb2114de36cc450b24a795c8b842ea3fe2b5d3ae261777966088981c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19101566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f9750cde5e598eddb25cb06de3196c475dfe940267f34c736aeebf2d606696`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fe8a84f82ad300ce90efce39dd06078babce03103f8b8fe54cdbafb1fbc1f5`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 9.6 MB (9637197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d066bbdeb2014769a48d8148c61e03de10dbfb7acd1ab85f2ded1e7fc00d4d`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52264d62ad1faa811627d0ed73c1b84f1ac7d0eb79bc1dfe11cf881039971566`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 6.0 MB (5994206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:8fa447d248e4470c90876cde43ba4113beae83308c1df0897cc7ef9aadc43c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1197639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e42131d18a25107b03a2c3896713f456d13455b6ae6538165e7722393cb301d`

```dockerfile
```

-	Layers:
	-	`sha256:9e6c0cce7fb0dd7e8aa2edbf38f26a85728a617a5dd3a52ad2b45f225e21aa48`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 1.2 MB (1180380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9529db747d4db3bf62950ed172f88b0bc2940614e0ca337601c634c09ba51f2`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 17.3 KB (17259 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.20` - linux; ppc64le

```console
$ docker pull irssi@sha256:f4295c16c15be6d6b002444faf906a4376f6a034f0fb10e7804ca1a0eb5a5d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20117357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612e050904415a82d96b010cd7125b10f3b535d204678ca2a9de0dfdd94b5bab`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf7f01d0ac0592b557f92ad27859bdcd34b46bd87f3357c86c81131ba4c1ac3`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 10.4 MB (10379021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e046fbadf0eb3f861ca076d737a51e9d3f8f54cf0fe5a50fd781332a42914a3`  
		Last Modified: Sat, 07 Sep 2024 07:03:05 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e93d1891687db40bc621f9c7c4b32ada1170a9c98951f1fe4aa315a844c730`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 6.2 MB (6164918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:ec763bbab32c460ad03421366a5aebc14cf613d6d45bb177fd44d671e3bd6371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4e5a8fced4a91a234e459d3e86f70f0a875ef57ce7b3b2778200d6692f8cc1`

```dockerfile
```

-	Layers:
	-	`sha256:2121fb019fff014bbc612a435b5e0209feb68478ca72db18ce1d8ca584be271f`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 1.2 MB (1178529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a52d086952a00b69d128df0a14d1bdc11dfbe5c91859e833208040720b9d0efd`  
		Last Modified: Sat, 07 Sep 2024 07:03:05 GMT  
		Size: 17.4 KB (17382 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.20` - linux; riscv64

```console
$ docker pull irssi@sha256:856c91783f7d21012b38323b36991a4b415b148dcab362efe6d45ca221b9d692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18948633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882b8fdcf190add01c2dc00e479ba691543a23c72901c9b9581734e8ecbd4d80`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634141d08a7f2ae5a144da1847d931b4cc99514263aea51e764b222d536642bd`  
		Last Modified: Sat, 07 Sep 2024 20:33:42 GMT  
		Size: 9.6 MB (9645875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8a2a2ecd95ddd7ef0c9d83f432abab63b16ead3200fd2df5617cfd5b8f0e99`  
		Last Modified: Sat, 07 Sep 2024 20:33:40 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49e9fc5ff805842d79b092fb62541e430a9fdb5d1144f8a360cc2fc1171a61e`  
		Last Modified: Sat, 07 Sep 2024 20:33:41 GMT  
		Size: 5.9 MB (5930308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:3acf8b9addc44a281e26766672e6142aacb88117e08fb56734b09449033a5a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e863619e8a6d2f0955b1b8e1da7b02f294d705f526e5815a8d990aa430482ab2`

```dockerfile
```

-	Layers:
	-	`sha256:00b2eeaffa4b740f8aa8985162c83d7a26da17ff5e9c3bd70b0c62d8dc64788b`  
		Last Modified: Sat, 07 Sep 2024 20:33:41 GMT  
		Size: 1.2 MB (1178525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a3f803218dcbba5730579592f427070a871dd2311ce2e2ceb98ac94e033cdb3`  
		Last Modified: Sat, 07 Sep 2024 20:33:40 GMT  
		Size: 17.4 KB (17377 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.20` - linux; s390x

```console
$ docker pull irssi@sha256:a9343811b921bf367edda23179c3a2567bc8c35339371a584986716c967d30fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20273410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386a4347853f194ac5a1aec08dc721a00fb5214f62aa6b5619bb97822cf8d8d7`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf007dfb739e6f45d5915a24bdaa5a2d439dd6e0b3b795852fdee75463ada95`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 10.8 MB (10753338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21af45072b07676ab768b93ba8bdbd6ea9039d1a189f72d756aef2f352d7f0af`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6f5d317148da6283d176e25e9078d039f9c168bb182f7d79b401a047fa5c44`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 6.1 MB (6057476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:c64fc2803cf39d52ca243caa6b69e23565bd37c6db576f2956d712bee758f118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e5d62029e06315a1f9d7c42efab99910196d2f0539c13839c2644d7722b7fc`

```dockerfile
```

-	Layers:
	-	`sha256:fa51fb87e83eeb4a26311a4273a680a426aad645be1a2b2166305da4793c83bc`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 1.2 MB (1178471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc9bd2b4610dbaf8c034897233371f6d76f0932f7276e254755a2a774162f786`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 17.3 KB (17316 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-bookworm`

```console
$ docker pull irssi@sha256:d843f5da94333b1e5b71252558cfc96bab350fe4b5ae651a74215574f5141d77
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `irssi:1.4.5-bookworm` - linux; amd64

```console
$ docker pull irssi@sha256:8aa50d7d3ea8f42fd43067cfbb6f0de50482d7d8e3db5a50fe2598628eb02cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51991262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a6601170dc20fcf1c200d8db92a1f1b4cb70798a9bad21d6347fec54cedd7d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb24a21ee06ae2e696f315794f60683badb1fd6322bffc2a0319d2af71210d22`  
		Last Modified: Thu, 17 Oct 2024 01:21:30 GMT  
		Size: 18.3 MB (18268738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdfe65b078593a20f4d8a6a2e19a8bf4630a32c9a7de2f322b2844f2d93d438`  
		Last Modified: Thu, 17 Oct 2024 01:21:29 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5809862e7f3e9acbbd4cfdb6fa307742f16800ba62916d52f094603dda824867`  
		Last Modified: Thu, 17 Oct 2024 01:21:30 GMT  
		Size: 4.6 MB (4592881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:b14643a76798849fc221cdbff8e7ea9154d43b8eb786152f7b09914b50cb4457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bd8878fc0ba19f6256e48b5d5f656828755ecf598b5a6c70ff014b3ee3fc7c`

```dockerfile
```

-	Layers:
	-	`sha256:f8074bdb984a9cbee8b0939fbd785951f79e4c40ec6e2cabf14987ab7c996ed9`  
		Last Modified: Thu, 17 Oct 2024 01:21:30 GMT  
		Size: 5.4 MB (5365679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:944a60539d43dccd726aaed7cd2f3bd293bed84744b2dc7741271b82951374aa`  
		Last Modified: Thu, 17 Oct 2024 01:21:29 GMT  
		Size: 18.6 KB (18554 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:e85a8d276df24059b698c6cc142a6506e446bfa77824eef8ce9bfa01e59a4de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48374514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8cf2dfca38be27dba04fd2515e55b60909c37be13165966482d40e007bdd01`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:c8ec8d65b2f61866a2c6085ed61e936733bc484abeeba1b91d12b9f6a97e456b in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e51d4479d9f15eaafec663087c05baede0a0724dc30787f7912ade3b686f46b1`  
		Last Modified: Thu, 17 Oct 2024 00:57:27 GMT  
		Size: 26.9 MB (26887306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df41522fb0d82bb74591eb0a6713b9bb3839d683778f8fab089fd229cbab932`  
		Last Modified: Thu, 17 Oct 2024 05:45:36 GMT  
		Size: 17.0 MB (17039325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fb9e3ff10a084e27b6bfc73e1c126d52dfb2770497d3af79313971c85d0e88`  
		Last Modified: Thu, 17 Oct 2024 05:45:35 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87475fcd2d3950e702cf8a915e34f0cc33b5d567947163f35f8b5ead687d17f`  
		Last Modified: Thu, 17 Oct 2024 05:45:35 GMT  
		Size: 4.4 MB (4444529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:d4fccfbe8c9851c23102ad85753a1eb2f86077bce99aef53d6de10c36ae00665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d43f272b6657e00c3e2aef48985598165862c59becd212cdcf2a6e41be557f1`

```dockerfile
```

-	Layers:
	-	`sha256:82a5e95b79e54c65b557fc48cafd3b3ad757a681ec457ab0dab4a03421e88b20`  
		Last Modified: Thu, 17 Oct 2024 05:45:35 GMT  
		Size: 5.4 MB (5367178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc81d93dc84be6d270a4b218df61a62925757a55ab8712283db916743c4d67ab`  
		Last Modified: Thu, 17 Oct 2024 05:45:35 GMT  
		Size: 18.7 KB (18682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:12ad8e850827d74e28bde549e45ac6beaa8651c36f70afc08919d4cbc542961e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45654435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a7c45209aca883ac274fb51ef1c0c0e6d936a981a6518d42daa02f83a6a278`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f348c2f61d7048f13bbb2bf7c6015111e9341c1b2a57bb0f51c370ca45bd907`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 16.6 MB (16633805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8267612072f179f1f84c6a626ad7269f297796bd2a5cdfe38e2610ff43c9ba38`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980a4fb6213eb64092401fc4580bd066eb7536f435211170043953cb5d550b1a`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 4.3 MB (4299079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:9262df858faf119c78f44abe577174119e92d426eb5afed88413643ce45f3cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c68652ec81e35444cd943d16301610be8a1e00177afd6de2925c6813f9f4bba1`

```dockerfile
```

-	Layers:
	-	`sha256:672662f58b1c37e76367c167633e8ad8b24c5071cbe5c947ff3858f8eace60da`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 5.4 MB (5367033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf4fc54a2dd30f7fa8311901fa81effc94562db647873e07c968866f1d5b4a66`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 18.7 KB (18682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f0a0f670eae231f1274d0e9e5097240e841843799dd4bab65297e68836f003d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51720933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad0d0f0c746e27f7c110a3107d75d817c44d4de8ae6606706e33d6296c240d3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fa218b665e0696e6cbbb7e15f224e210265c26d0938799bf2cb4ba9ddb5ed7`  
		Last Modified: Thu, 17 Oct 2024 13:13:59 GMT  
		Size: 18.0 MB (18048181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830a882aa3c01ae181d1aff028e2fbdd695f7cad16cadb69acec9ad7c6404b09`  
		Last Modified: Thu, 17 Oct 2024 13:13:58 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e603ba669c49ad6e8006dc9fd6517daadb6e830ee90614880f222bb717b5359`  
		Last Modified: Thu, 17 Oct 2024 13:13:59 GMT  
		Size: 4.5 MB (4513057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c90a647af8cbe3ce4e36bffff2ca2dfafe6905cc26bb80f77a68a6ef84a80cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5390891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227f292d79f3a8ec728ca0caa89f4bd85fda9ee2546c35bec4f4890158b19832`

```dockerfile
```

-	Layers:
	-	`sha256:1c3ef154ce409a963bb09794d072c2b1c34a7607ff31366904498b4bfd257aae`  
		Last Modified: Thu, 17 Oct 2024 13:13:59 GMT  
		Size: 5.4 MB (5372161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb2f7fe9f657bdaeb0daa90626317db717c17908e3e479b6e71a075ba1f6dfe0`  
		Last Modified: Thu, 17 Oct 2024 13:13:58 GMT  
		Size: 18.7 KB (18730 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:0456833f0dc5f5135063a36bcdfcad14dc427a41da7ff129bb03beca4950cc90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52561651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b622b093ac5b5bccce519dbcd83e5e38b1a80607e3fc8d044d24105bd88ad07f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108ff1f82b7d31627896ef9dfa4d55dd918dd899dc1d07d811f2a973ca493272`  
		Last Modified: Thu, 17 Oct 2024 01:21:25 GMT  
		Size: 17.8 MB (17807462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab24ea74320071af584210ffe42f29229a3c32d58f2fc6b39ce817b15e727ae`  
		Last Modified: Thu, 17 Oct 2024 01:21:24 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e92c1d542ec81f26c5c8944a9622b196df4a3c8a7130c9b8d03f6a1c1601e6`  
		Last Modified: Thu, 17 Oct 2024 01:21:24 GMT  
		Size: 4.6 MB (4606565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:3ec4be7da4181fdbeb6ab8972993b6a1b52b0f88152c7c6a3bee462bfbddce93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5380258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065781f2809ba4e58b52f7baf61a835fd97eebf699650f381a447202796234b7`

```dockerfile
```

-	Layers:
	-	`sha256:75eeb53340b15ef46774f8a563ed54455d45ba0e527466054dec23fddd1ea9d1`  
		Last Modified: Thu, 17 Oct 2024 01:21:24 GMT  
		Size: 5.4 MB (5361757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa627aa524b4d75732bb320f5907ea045cd6c3c40af27a99c07e097375bba8fc`  
		Last Modified: Thu, 17 Oct 2024 01:21:24 GMT  
		Size: 18.5 KB (18501 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:291d87011c5c636d069d6f74c6796c03d2208d050713b23db2a301c6a54bc9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50633180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e6aa70a891ce32f5488c0353e6f02facfb108db6ba13dfb255a05038802c24`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:673970f358f62b6b095139e9647b41b9af839d4e01f7698755b040f471ff80b2 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:75358c79454e0fed44aa25dd323536443b4a1230fc432aa226620e470d72cf5f`  
		Last Modified: Fri, 27 Sep 2024 09:11:36 GMT  
		Size: 29.1 MB (29124858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d53fbf788bd0e7b28f97c4dc927f8ab5bc32596e4d316d1e4107d63df122e3`  
		Last Modified: Fri, 27 Sep 2024 23:25:12 GMT  
		Size: 16.9 MB (16949902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2858574a09072d459734ac302f8784ee2119cd1028b5d0e81359d03e7693743`  
		Last Modified: Fri, 27 Sep 2024 23:25:10 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86aa9a6bf5e9b33a0ce592db709ac8916b028b333caa0bbdb8fba1bd2f6214cd`  
		Last Modified: Fri, 27 Sep 2024 23:25:11 GMT  
		Size: 4.6 MB (4555066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:7b17417d51f41d70cde36d9d968c36209ddd5246b2e9a87b8841b2c1aaee76fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bd0d67639923b725e3575a86ab49679b4125e46a54d6d4697146278f381a88`

```dockerfile
```

-	Layers:
	-	`sha256:55950ecb6cc8539508cfd44c53f5ad3fe2fb065c30a19cc098db41c8cf9a68da`  
		Last Modified: Fri, 27 Sep 2024 23:25:10 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:9e802780529f1ac8dc9e2a4e005a33691d9392e00937ff96d0605832f9bebbd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56730477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802dbfec090fbf25a29b5a6497cf1b84626e3b8445a70448f5e978e66beb8135`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c9398d733e6504c746da92179ca87ad112a632322da102a80b7fcfb289570b`  
		Last Modified: Thu, 17 Oct 2024 08:39:47 GMT  
		Size: 18.8 MB (18776314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29a43ed635481a1588bff095c3612c8656bc784fe29d6e2775b4687f0754952`  
		Last Modified: Thu, 17 Oct 2024 08:39:46 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4012dfdba364ca794130d1dffd077292fcb38350f73fb6278877bd25d2d8c7fc`  
		Last Modified: Thu, 17 Oct 2024 08:39:47 GMT  
		Size: 4.8 MB (4828605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:1a5fd59e01471305d46ac075911b975e8aeb9c14be98e8c2e4441ce1de6d6bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80260c15ff6e7c8aadd796f8e69434fca49c016e38b7c433fb18d14cca2bd504`

```dockerfile
```

-	Layers:
	-	`sha256:25819b0bf172f91e1cd05bc76766c461bdf1e8521e7ae7c7a0a8bbc22ca147bf`  
		Last Modified: Thu, 17 Oct 2024 08:39:47 GMT  
		Size: 5.4 MB (5373373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:354ff742b1d00d43544704361eebfaace5714e6f96f4e66b0313e9d1267af98c`  
		Last Modified: Thu, 17 Oct 2024 08:39:46 GMT  
		Size: 18.6 KB (18620 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:62d3dfafa7f8ea785b17fac4aeab1d35709c0631816835fa6904e57e336d1582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50307925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9113e290344eed8b5c9217ede2fd0b90f7b73c19455deaf66a2c37498fea6f3f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc28589ea18c5147d2150e6c305d805ff80ab242c5f64ebff3fa07cd244b1e20`  
		Last Modified: Thu, 17 Oct 2024 13:15:53 GMT  
		Size: 18.2 MB (18227811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e4c1d1c7203ba73e3baed860511382dcaba23fb316575e5b4a68aea09ad8ce`  
		Last Modified: Thu, 17 Oct 2024 13:15:52 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16802b2f05ed3d331e4ca172c0f5e0e78f969f531b192c9cab2b79fa17ca9320`  
		Last Modified: Thu, 17 Oct 2024 13:15:53 GMT  
		Size: 4.6 MB (4586676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:e5ddc58cf0baeb33e18378e5729dfafea51d5d9e6abf4ba9d3e48d5e8ea96eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5383534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548345c85d4ac645fd695bb4f1236c309665e73904bacdded8fab6976d751206`

```dockerfile
```

-	Layers:
	-	`sha256:bf5ab0e8e73932f8aba43d1f7ce78795c90e0123ee9735706a911813cc3d5fdb`  
		Last Modified: Thu, 17 Oct 2024 13:15:53 GMT  
		Size: 5.4 MB (5364980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6966e3fc81ec6a47d7dba5ee8184f4a0d792e39d59ee9ab2e594cb8c3dfe2f1a`  
		Last Modified: Thu, 17 Oct 2024 13:15:52 GMT  
		Size: 18.6 KB (18554 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine`

```console
$ docker pull irssi@sha256:8433cdf30e274988426352ad38712dc09f28c4c1768569d4588eea8dae437e60
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
$ docker pull irssi@sha256:225eeedb3d5df0d8342c28f28a67e14963a4a3f668754735ab50b36cf23849a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19723767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8718185e934cf00977ac16947769332a38a80ba94b1958d5134cc5096dddec`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c626f109cf0e2e5ee386344e1f4f1278bab9391d09e043d3f9afe609c04387`  
		Last Modified: Fri, 06 Sep 2024 23:21:57 GMT  
		Size: 10.2 MB (10191821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753e1b9dda433c6260ec07e1572c0120eeb2205ad32293eae47eaa0a81b43bfd`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fa96080be04b7162785b53e6197cf44a7906954d44de78eb0bbeb69eeac92e`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 5.9 MB (5907140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:187222cb890ac3b3f65f968a23c8375217deb65302025ca80d3bddd34aa6405a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1197741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ad74886f316acc6cfaebde6ff77de40ec17fd0107308bfb57973256f59e8d5`

```dockerfile
```

-	Layers:
	-	`sha256:f7ca62c1d6b0082fb2d26f943a081038469132453899545953a91012cd4e7375`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 1.2 MB (1180425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b77417a1071ef7e7085c110ce17cfa06c18b50cf1b1caf8ba006a14f926abb21`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 17.3 KB (17316 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:bc876fda49849676e70afc23dfc3e74c36da0c2a3745f5fd3c28a8aa9b8635b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18480137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf0c54c34c514e6637fbbdc3209d255343b87c65ed581f951673640306e1dac6`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4563366942775996dc7eff42d60df711ef73b0fbafbca9edb8d797024668c202`  
		Last Modified: Sat, 07 Sep 2024 02:40:26 GMT  
		Size: 9.4 MB (9362097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6b0c6e5c33e41b06fde0292dae092dc763b7e27b823ab7be705407c11384bd`  
		Last Modified: Sat, 07 Sep 2024 02:40:25 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcce1db33190250448077f9d4cd391b9ef2b6a67f7d2fa94f27bc0362e4894cd`  
		Last Modified: Sat, 07 Sep 2024 02:40:26 GMT  
		Size: 5.8 MB (5750537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:4d1617b7ab5430803bbd52362c57bb453d8dd4acaedf8bdde2447432a7ff9e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a999001bf9c39d625593692a3b737f6f3a0b814b3c4811047346af7fada502`

```dockerfile
```

-	Layers:
	-	`sha256:818f414539c29d70896c89b3932576101e8e18ce58a90487359afb4f38d44f5b`  
		Last Modified: Sat, 07 Sep 2024 02:40:25 GMT  
		Size: 17.2 KB (17221 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:1d02a8ed391c51bde9b27afde1ea4240cc487cf74dbf61e5d2efba692b2799f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17782449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053a71b3a279ad0e3a2e0d7dbbf4e54ad2278be015c7f288b5fd103a4d67c754`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0429f3169f57cf771d30f0b785f6c7a5ab02d43411f8d6f2344100a482351a48`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 9.2 MB (9183709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5dba3974eab46837cadb17dfa4a364e5da3b9bd43af9186c06744a8fd58a40`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f255b010ec76769301234a17a2d0bdd32e205d39407d7962c89e1a5c79b89851`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 5.5 MB (5502241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:14f64ac5066b5ca789c86b0625abe3210bf749b295085d8d92dd6af200205bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1200797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32f9747e49a5665b3336fd605ddcdacc76f8ada3a5d544863246fb41d31ad24`

```dockerfile
```

-	Layers:
	-	`sha256:35094785d6853a5f0461474df37f8127ad609827a2b89f696d94a63f97125283`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 1.2 MB (1183357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4d31524ff73face1950830eab2bd0ed7ec05e4012f74641a1b5a49010fc1998`  
		Last Modified: Sat, 07 Sep 2024 02:57:53 GMT  
		Size: 17.4 KB (17440 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:62e8dceafa5dcc45ea2419d86401fbf0824b7a4bae684d174ad74b52a78abf20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20053478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec1e645d1e32a1d6e4842461b9a9b6b03670618d7c7be7a3c59a8f9773ddd02`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad68fd7a6bae4d6a9f0791e9a8b0d89515ef68cc3b3bc2802082159c8f0b917`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 10.2 MB (10157951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1759a5bf2c0e097fe22b543d149e5fdcd014e7b5f039a9fdb8b9ba503d6be7f`  
		Last Modified: Sat, 07 Sep 2024 05:27:55 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0df7ac6458b3449bfc8746487857687df8de1d04144326f711d143f904e0da`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 5.8 MB (5806884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:964aec0691615b07c0f7cf64bd3c2aaf8e77f54ae96bd8ae41c132aa2d21c32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1198193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0846e8bd16a6800d33a45be72816781d99d14770119347a9b650981b6cf2073e`

```dockerfile
```

-	Layers:
	-	`sha256:fe65408852799879429a8939ccc5713fad8538db3615fa77035290c4b582c5ec`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 1.2 MB (1180529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d76afdd382391f2e7f0b7e5e52a8af475ce69ab9742ec727e6e0d04ed084114`  
		Last Modified: Sat, 07 Sep 2024 05:27:55 GMT  
		Size: 17.7 KB (17664 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; 386

```console
$ docker pull irssi@sha256:cec60383cb2114de36cc450b24a795c8b842ea3fe2b5d3ae261777966088981c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19101566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f9750cde5e598eddb25cb06de3196c475dfe940267f34c736aeebf2d606696`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fe8a84f82ad300ce90efce39dd06078babce03103f8b8fe54cdbafb1fbc1f5`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 9.6 MB (9637197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d066bbdeb2014769a48d8148c61e03de10dbfb7acd1ab85f2ded1e7fc00d4d`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52264d62ad1faa811627d0ed73c1b84f1ac7d0eb79bc1dfe11cf881039971566`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 6.0 MB (5994206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:8fa447d248e4470c90876cde43ba4113beae83308c1df0897cc7ef9aadc43c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1197639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e42131d18a25107b03a2c3896713f456d13455b6ae6538165e7722393cb301d`

```dockerfile
```

-	Layers:
	-	`sha256:9e6c0cce7fb0dd7e8aa2edbf38f26a85728a617a5dd3a52ad2b45f225e21aa48`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 1.2 MB (1180380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9529db747d4db3bf62950ed172f88b0bc2940614e0ca337601c634c09ba51f2`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 17.3 KB (17259 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:f4295c16c15be6d6b002444faf906a4376f6a034f0fb10e7804ca1a0eb5a5d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20117357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612e050904415a82d96b010cd7125b10f3b535d204678ca2a9de0dfdd94b5bab`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf7f01d0ac0592b557f92ad27859bdcd34b46bd87f3357c86c81131ba4c1ac3`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 10.4 MB (10379021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e046fbadf0eb3f861ca076d737a51e9d3f8f54cf0fe5a50fd781332a42914a3`  
		Last Modified: Sat, 07 Sep 2024 07:03:05 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e93d1891687db40bc621f9c7c4b32ada1170a9c98951f1fe4aa315a844c730`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 6.2 MB (6164918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:ec763bbab32c460ad03421366a5aebc14cf613d6d45bb177fd44d671e3bd6371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4e5a8fced4a91a234e459d3e86f70f0a875ef57ce7b3b2778200d6692f8cc1`

```dockerfile
```

-	Layers:
	-	`sha256:2121fb019fff014bbc612a435b5e0209feb68478ca72db18ce1d8ca584be271f`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 1.2 MB (1178529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a52d086952a00b69d128df0a14d1bdc11dfbe5c91859e833208040720b9d0efd`  
		Last Modified: Sat, 07 Sep 2024 07:03:05 GMT  
		Size: 17.4 KB (17382 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:856c91783f7d21012b38323b36991a4b415b148dcab362efe6d45ca221b9d692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18948633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882b8fdcf190add01c2dc00e479ba691543a23c72901c9b9581734e8ecbd4d80`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634141d08a7f2ae5a144da1847d931b4cc99514263aea51e764b222d536642bd`  
		Last Modified: Sat, 07 Sep 2024 20:33:42 GMT  
		Size: 9.6 MB (9645875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8a2a2ecd95ddd7ef0c9d83f432abab63b16ead3200fd2df5617cfd5b8f0e99`  
		Last Modified: Sat, 07 Sep 2024 20:33:40 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49e9fc5ff805842d79b092fb62541e430a9fdb5d1144f8a360cc2fc1171a61e`  
		Last Modified: Sat, 07 Sep 2024 20:33:41 GMT  
		Size: 5.9 MB (5930308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:3acf8b9addc44a281e26766672e6142aacb88117e08fb56734b09449033a5a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e863619e8a6d2f0955b1b8e1da7b02f294d705f526e5815a8d990aa430482ab2`

```dockerfile
```

-	Layers:
	-	`sha256:00b2eeaffa4b740f8aa8985162c83d7a26da17ff5e9c3bd70b0c62d8dc64788b`  
		Last Modified: Sat, 07 Sep 2024 20:33:41 GMT  
		Size: 1.2 MB (1178525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a3f803218dcbba5730579592f427070a871dd2311ce2e2ceb98ac94e033cdb3`  
		Last Modified: Sat, 07 Sep 2024 20:33:40 GMT  
		Size: 17.4 KB (17377 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; s390x

```console
$ docker pull irssi@sha256:a9343811b921bf367edda23179c3a2567bc8c35339371a584986716c967d30fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20273410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386a4347853f194ac5a1aec08dc721a00fb5214f62aa6b5619bb97822cf8d8d7`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf007dfb739e6f45d5915a24bdaa5a2d439dd6e0b3b795852fdee75463ada95`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 10.8 MB (10753338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21af45072b07676ab768b93ba8bdbd6ea9039d1a189f72d756aef2f352d7f0af`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6f5d317148da6283d176e25e9078d039f9c168bb182f7d79b401a047fa5c44`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 6.1 MB (6057476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:c64fc2803cf39d52ca243caa6b69e23565bd37c6db576f2956d712bee758f118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e5d62029e06315a1f9d7c42efab99910196d2f0539c13839c2644d7722b7fc`

```dockerfile
```

-	Layers:
	-	`sha256:fa51fb87e83eeb4a26311a4273a680a426aad645be1a2b2166305da4793c83bc`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 1.2 MB (1178471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc9bd2b4610dbaf8c034897233371f6d76f0932f7276e254755a2a774162f786`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 17.3 KB (17316 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine3.20`

```console
$ docker pull irssi@sha256:8433cdf30e274988426352ad38712dc09f28c4c1768569d4588eea8dae437e60
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

### `irssi:alpine3.20` - linux; amd64

```console
$ docker pull irssi@sha256:225eeedb3d5df0d8342c28f28a67e14963a4a3f668754735ab50b36cf23849a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19723767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8718185e934cf00977ac16947769332a38a80ba94b1958d5134cc5096dddec`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c626f109cf0e2e5ee386344e1f4f1278bab9391d09e043d3f9afe609c04387`  
		Last Modified: Fri, 06 Sep 2024 23:21:57 GMT  
		Size: 10.2 MB (10191821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753e1b9dda433c6260ec07e1572c0120eeb2205ad32293eae47eaa0a81b43bfd`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fa96080be04b7162785b53e6197cf44a7906954d44de78eb0bbeb69eeac92e`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 5.9 MB (5907140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:187222cb890ac3b3f65f968a23c8375217deb65302025ca80d3bddd34aa6405a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1197741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ad74886f316acc6cfaebde6ff77de40ec17fd0107308bfb57973256f59e8d5`

```dockerfile
```

-	Layers:
	-	`sha256:f7ca62c1d6b0082fb2d26f943a081038469132453899545953a91012cd4e7375`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 1.2 MB (1180425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b77417a1071ef7e7085c110ce17cfa06c18b50cf1b1caf8ba006a14f926abb21`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 17.3 KB (17316 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.20` - linux; arm variant v6

```console
$ docker pull irssi@sha256:bc876fda49849676e70afc23dfc3e74c36da0c2a3745f5fd3c28a8aa9b8635b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18480137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf0c54c34c514e6637fbbdc3209d255343b87c65ed581f951673640306e1dac6`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4563366942775996dc7eff42d60df711ef73b0fbafbca9edb8d797024668c202`  
		Last Modified: Sat, 07 Sep 2024 02:40:26 GMT  
		Size: 9.4 MB (9362097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6b0c6e5c33e41b06fde0292dae092dc763b7e27b823ab7be705407c11384bd`  
		Last Modified: Sat, 07 Sep 2024 02:40:25 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcce1db33190250448077f9d4cd391b9ef2b6a67f7d2fa94f27bc0362e4894cd`  
		Last Modified: Sat, 07 Sep 2024 02:40:26 GMT  
		Size: 5.8 MB (5750537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:4d1617b7ab5430803bbd52362c57bb453d8dd4acaedf8bdde2447432a7ff9e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a999001bf9c39d625593692a3b737f6f3a0b814b3c4811047346af7fada502`

```dockerfile
```

-	Layers:
	-	`sha256:818f414539c29d70896c89b3932576101e8e18ce58a90487359afb4f38d44f5b`  
		Last Modified: Sat, 07 Sep 2024 02:40:25 GMT  
		Size: 17.2 KB (17221 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.20` - linux; arm variant v7

```console
$ docker pull irssi@sha256:1d02a8ed391c51bde9b27afde1ea4240cc487cf74dbf61e5d2efba692b2799f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17782449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053a71b3a279ad0e3a2e0d7dbbf4e54ad2278be015c7f288b5fd103a4d67c754`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0429f3169f57cf771d30f0b785f6c7a5ab02d43411f8d6f2344100a482351a48`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 9.2 MB (9183709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5dba3974eab46837cadb17dfa4a364e5da3b9bd43af9186c06744a8fd58a40`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f255b010ec76769301234a17a2d0bdd32e205d39407d7962c89e1a5c79b89851`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 5.5 MB (5502241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:14f64ac5066b5ca789c86b0625abe3210bf749b295085d8d92dd6af200205bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1200797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32f9747e49a5665b3336fd605ddcdacc76f8ada3a5d544863246fb41d31ad24`

```dockerfile
```

-	Layers:
	-	`sha256:35094785d6853a5f0461474df37f8127ad609827a2b89f696d94a63f97125283`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 1.2 MB (1183357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4d31524ff73face1950830eab2bd0ed7ec05e4012f74641a1b5a49010fc1998`  
		Last Modified: Sat, 07 Sep 2024 02:57:53 GMT  
		Size: 17.4 KB (17440 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:62e8dceafa5dcc45ea2419d86401fbf0824b7a4bae684d174ad74b52a78abf20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20053478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec1e645d1e32a1d6e4842461b9a9b6b03670618d7c7be7a3c59a8f9773ddd02`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad68fd7a6bae4d6a9f0791e9a8b0d89515ef68cc3b3bc2802082159c8f0b917`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 10.2 MB (10157951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1759a5bf2c0e097fe22b543d149e5fdcd014e7b5f039a9fdb8b9ba503d6be7f`  
		Last Modified: Sat, 07 Sep 2024 05:27:55 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0df7ac6458b3449bfc8746487857687df8de1d04144326f711d143f904e0da`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 5.8 MB (5806884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:964aec0691615b07c0f7cf64bd3c2aaf8e77f54ae96bd8ae41c132aa2d21c32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1198193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0846e8bd16a6800d33a45be72816781d99d14770119347a9b650981b6cf2073e`

```dockerfile
```

-	Layers:
	-	`sha256:fe65408852799879429a8939ccc5713fad8538db3615fa77035290c4b582c5ec`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 1.2 MB (1180529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d76afdd382391f2e7f0b7e5e52a8af475ce69ab9742ec727e6e0d04ed084114`  
		Last Modified: Sat, 07 Sep 2024 05:27:55 GMT  
		Size: 17.7 KB (17664 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.20` - linux; 386

```console
$ docker pull irssi@sha256:cec60383cb2114de36cc450b24a795c8b842ea3fe2b5d3ae261777966088981c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19101566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f9750cde5e598eddb25cb06de3196c475dfe940267f34c736aeebf2d606696`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fe8a84f82ad300ce90efce39dd06078babce03103f8b8fe54cdbafb1fbc1f5`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 9.6 MB (9637197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d066bbdeb2014769a48d8148c61e03de10dbfb7acd1ab85f2ded1e7fc00d4d`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52264d62ad1faa811627d0ed73c1b84f1ac7d0eb79bc1dfe11cf881039971566`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 6.0 MB (5994206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:8fa447d248e4470c90876cde43ba4113beae83308c1df0897cc7ef9aadc43c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1197639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e42131d18a25107b03a2c3896713f456d13455b6ae6538165e7722393cb301d`

```dockerfile
```

-	Layers:
	-	`sha256:9e6c0cce7fb0dd7e8aa2edbf38f26a85728a617a5dd3a52ad2b45f225e21aa48`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 1.2 MB (1180380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9529db747d4db3bf62950ed172f88b0bc2940614e0ca337601c634c09ba51f2`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 17.3 KB (17259 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.20` - linux; ppc64le

```console
$ docker pull irssi@sha256:f4295c16c15be6d6b002444faf906a4376f6a034f0fb10e7804ca1a0eb5a5d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20117357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612e050904415a82d96b010cd7125b10f3b535d204678ca2a9de0dfdd94b5bab`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf7f01d0ac0592b557f92ad27859bdcd34b46bd87f3357c86c81131ba4c1ac3`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 10.4 MB (10379021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e046fbadf0eb3f861ca076d737a51e9d3f8f54cf0fe5a50fd781332a42914a3`  
		Last Modified: Sat, 07 Sep 2024 07:03:05 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e93d1891687db40bc621f9c7c4b32ada1170a9c98951f1fe4aa315a844c730`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 6.2 MB (6164918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:ec763bbab32c460ad03421366a5aebc14cf613d6d45bb177fd44d671e3bd6371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4e5a8fced4a91a234e459d3e86f70f0a875ef57ce7b3b2778200d6692f8cc1`

```dockerfile
```

-	Layers:
	-	`sha256:2121fb019fff014bbc612a435b5e0209feb68478ca72db18ce1d8ca584be271f`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 1.2 MB (1178529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a52d086952a00b69d128df0a14d1bdc11dfbe5c91859e833208040720b9d0efd`  
		Last Modified: Sat, 07 Sep 2024 07:03:05 GMT  
		Size: 17.4 KB (17382 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.20` - linux; riscv64

```console
$ docker pull irssi@sha256:856c91783f7d21012b38323b36991a4b415b148dcab362efe6d45ca221b9d692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18948633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882b8fdcf190add01c2dc00e479ba691543a23c72901c9b9581734e8ecbd4d80`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634141d08a7f2ae5a144da1847d931b4cc99514263aea51e764b222d536642bd`  
		Last Modified: Sat, 07 Sep 2024 20:33:42 GMT  
		Size: 9.6 MB (9645875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8a2a2ecd95ddd7ef0c9d83f432abab63b16ead3200fd2df5617cfd5b8f0e99`  
		Last Modified: Sat, 07 Sep 2024 20:33:40 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49e9fc5ff805842d79b092fb62541e430a9fdb5d1144f8a360cc2fc1171a61e`  
		Last Modified: Sat, 07 Sep 2024 20:33:41 GMT  
		Size: 5.9 MB (5930308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:3acf8b9addc44a281e26766672e6142aacb88117e08fb56734b09449033a5a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e863619e8a6d2f0955b1b8e1da7b02f294d705f526e5815a8d990aa430482ab2`

```dockerfile
```

-	Layers:
	-	`sha256:00b2eeaffa4b740f8aa8985162c83d7a26da17ff5e9c3bd70b0c62d8dc64788b`  
		Last Modified: Sat, 07 Sep 2024 20:33:41 GMT  
		Size: 1.2 MB (1178525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a3f803218dcbba5730579592f427070a871dd2311ce2e2ceb98ac94e033cdb3`  
		Last Modified: Sat, 07 Sep 2024 20:33:40 GMT  
		Size: 17.4 KB (17377 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.20` - linux; s390x

```console
$ docker pull irssi@sha256:a9343811b921bf367edda23179c3a2567bc8c35339371a584986716c967d30fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20273410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386a4347853f194ac5a1aec08dc721a00fb5214f62aa6b5619bb97822cf8d8d7`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Wed, 22 May 2024 22:40:32 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf007dfb739e6f45d5915a24bdaa5a2d439dd6e0b3b795852fdee75463ada95`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 10.8 MB (10753338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21af45072b07676ab768b93ba8bdbd6ea9039d1a189f72d756aef2f352d7f0af`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6f5d317148da6283d176e25e9078d039f9c168bb182f7d79b401a047fa5c44`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 6.1 MB (6057476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:c64fc2803cf39d52ca243caa6b69e23565bd37c6db576f2956d712bee758f118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e5d62029e06315a1f9d7c42efab99910196d2f0539c13839c2644d7722b7fc`

```dockerfile
```

-	Layers:
	-	`sha256:fa51fb87e83eeb4a26311a4273a680a426aad645be1a2b2166305da4793c83bc`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 1.2 MB (1178471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc9bd2b4610dbaf8c034897233371f6d76f0932f7276e254755a2a774162f786`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 17.3 KB (17316 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:bookworm`

```console
$ docker pull irssi@sha256:d843f5da94333b1e5b71252558cfc96bab350fe4b5ae651a74215574f5141d77
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `irssi:bookworm` - linux; amd64

```console
$ docker pull irssi@sha256:8aa50d7d3ea8f42fd43067cfbb6f0de50482d7d8e3db5a50fe2598628eb02cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51991262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a6601170dc20fcf1c200d8db92a1f1b4cb70798a9bad21d6347fec54cedd7d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb24a21ee06ae2e696f315794f60683badb1fd6322bffc2a0319d2af71210d22`  
		Last Modified: Thu, 17 Oct 2024 01:21:30 GMT  
		Size: 18.3 MB (18268738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdfe65b078593a20f4d8a6a2e19a8bf4630a32c9a7de2f322b2844f2d93d438`  
		Last Modified: Thu, 17 Oct 2024 01:21:29 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5809862e7f3e9acbbd4cfdb6fa307742f16800ba62916d52f094603dda824867`  
		Last Modified: Thu, 17 Oct 2024 01:21:30 GMT  
		Size: 4.6 MB (4592881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:b14643a76798849fc221cdbff8e7ea9154d43b8eb786152f7b09914b50cb4457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bd8878fc0ba19f6256e48b5d5f656828755ecf598b5a6c70ff014b3ee3fc7c`

```dockerfile
```

-	Layers:
	-	`sha256:f8074bdb984a9cbee8b0939fbd785951f79e4c40ec6e2cabf14987ab7c996ed9`  
		Last Modified: Thu, 17 Oct 2024 01:21:30 GMT  
		Size: 5.4 MB (5365679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:944a60539d43dccd726aaed7cd2f3bd293bed84744b2dc7741271b82951374aa`  
		Last Modified: Thu, 17 Oct 2024 01:21:29 GMT  
		Size: 18.6 KB (18554 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:e85a8d276df24059b698c6cc142a6506e446bfa77824eef8ce9bfa01e59a4de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48374514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8cf2dfca38be27dba04fd2515e55b60909c37be13165966482d40e007bdd01`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:c8ec8d65b2f61866a2c6085ed61e936733bc484abeeba1b91d12b9f6a97e456b in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e51d4479d9f15eaafec663087c05baede0a0724dc30787f7912ade3b686f46b1`  
		Last Modified: Thu, 17 Oct 2024 00:57:27 GMT  
		Size: 26.9 MB (26887306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df41522fb0d82bb74591eb0a6713b9bb3839d683778f8fab089fd229cbab932`  
		Last Modified: Thu, 17 Oct 2024 05:45:36 GMT  
		Size: 17.0 MB (17039325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fb9e3ff10a084e27b6bfc73e1c126d52dfb2770497d3af79313971c85d0e88`  
		Last Modified: Thu, 17 Oct 2024 05:45:35 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87475fcd2d3950e702cf8a915e34f0cc33b5d567947163f35f8b5ead687d17f`  
		Last Modified: Thu, 17 Oct 2024 05:45:35 GMT  
		Size: 4.4 MB (4444529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:d4fccfbe8c9851c23102ad85753a1eb2f86077bce99aef53d6de10c36ae00665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d43f272b6657e00c3e2aef48985598165862c59becd212cdcf2a6e41be557f1`

```dockerfile
```

-	Layers:
	-	`sha256:82a5e95b79e54c65b557fc48cafd3b3ad757a681ec457ab0dab4a03421e88b20`  
		Last Modified: Thu, 17 Oct 2024 05:45:35 GMT  
		Size: 5.4 MB (5367178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc81d93dc84be6d270a4b218df61a62925757a55ab8712283db916743c4d67ab`  
		Last Modified: Thu, 17 Oct 2024 05:45:35 GMT  
		Size: 18.7 KB (18682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:12ad8e850827d74e28bde549e45ac6beaa8651c36f70afc08919d4cbc542961e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45654435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a7c45209aca883ac274fb51ef1c0c0e6d936a981a6518d42daa02f83a6a278`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f348c2f61d7048f13bbb2bf7c6015111e9341c1b2a57bb0f51c370ca45bd907`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 16.6 MB (16633805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8267612072f179f1f84c6a626ad7269f297796bd2a5cdfe38e2610ff43c9ba38`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980a4fb6213eb64092401fc4580bd066eb7536f435211170043953cb5d550b1a`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 4.3 MB (4299079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:9262df858faf119c78f44abe577174119e92d426eb5afed88413643ce45f3cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c68652ec81e35444cd943d16301610be8a1e00177afd6de2925c6813f9f4bba1`

```dockerfile
```

-	Layers:
	-	`sha256:672662f58b1c37e76367c167633e8ad8b24c5071cbe5c947ff3858f8eace60da`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 5.4 MB (5367033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf4fc54a2dd30f7fa8311901fa81effc94562db647873e07c968866f1d5b4a66`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 18.7 KB (18682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f0a0f670eae231f1274d0e9e5097240e841843799dd4bab65297e68836f003d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51720933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad0d0f0c746e27f7c110a3107d75d817c44d4de8ae6606706e33d6296c240d3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fa218b665e0696e6cbbb7e15f224e210265c26d0938799bf2cb4ba9ddb5ed7`  
		Last Modified: Thu, 17 Oct 2024 13:13:59 GMT  
		Size: 18.0 MB (18048181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830a882aa3c01ae181d1aff028e2fbdd695f7cad16cadb69acec9ad7c6404b09`  
		Last Modified: Thu, 17 Oct 2024 13:13:58 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e603ba669c49ad6e8006dc9fd6517daadb6e830ee90614880f222bb717b5359`  
		Last Modified: Thu, 17 Oct 2024 13:13:59 GMT  
		Size: 4.5 MB (4513057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c90a647af8cbe3ce4e36bffff2ca2dfafe6905cc26bb80f77a68a6ef84a80cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5390891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227f292d79f3a8ec728ca0caa89f4bd85fda9ee2546c35bec4f4890158b19832`

```dockerfile
```

-	Layers:
	-	`sha256:1c3ef154ce409a963bb09794d072c2b1c34a7607ff31366904498b4bfd257aae`  
		Last Modified: Thu, 17 Oct 2024 13:13:59 GMT  
		Size: 5.4 MB (5372161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb2f7fe9f657bdaeb0daa90626317db717c17908e3e479b6e71a075ba1f6dfe0`  
		Last Modified: Thu, 17 Oct 2024 13:13:58 GMT  
		Size: 18.7 KB (18730 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; 386

```console
$ docker pull irssi@sha256:0456833f0dc5f5135063a36bcdfcad14dc427a41da7ff129bb03beca4950cc90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52561651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b622b093ac5b5bccce519dbcd83e5e38b1a80607e3fc8d044d24105bd88ad07f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108ff1f82b7d31627896ef9dfa4d55dd918dd899dc1d07d811f2a973ca493272`  
		Last Modified: Thu, 17 Oct 2024 01:21:25 GMT  
		Size: 17.8 MB (17807462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab24ea74320071af584210ffe42f29229a3c32d58f2fc6b39ce817b15e727ae`  
		Last Modified: Thu, 17 Oct 2024 01:21:24 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e92c1d542ec81f26c5c8944a9622b196df4a3c8a7130c9b8d03f6a1c1601e6`  
		Last Modified: Thu, 17 Oct 2024 01:21:24 GMT  
		Size: 4.6 MB (4606565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:3ec4be7da4181fdbeb6ab8972993b6a1b52b0f88152c7c6a3bee462bfbddce93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5380258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065781f2809ba4e58b52f7baf61a835fd97eebf699650f381a447202796234b7`

```dockerfile
```

-	Layers:
	-	`sha256:75eeb53340b15ef46774f8a563ed54455d45ba0e527466054dec23fddd1ea9d1`  
		Last Modified: Thu, 17 Oct 2024 01:21:24 GMT  
		Size: 5.4 MB (5361757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa627aa524b4d75732bb320f5907ea045cd6c3c40af27a99c07e097375bba8fc`  
		Last Modified: Thu, 17 Oct 2024 01:21:24 GMT  
		Size: 18.5 KB (18501 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:291d87011c5c636d069d6f74c6796c03d2208d050713b23db2a301c6a54bc9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50633180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e6aa70a891ce32f5488c0353e6f02facfb108db6ba13dfb255a05038802c24`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:673970f358f62b6b095139e9647b41b9af839d4e01f7698755b040f471ff80b2 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:75358c79454e0fed44aa25dd323536443b4a1230fc432aa226620e470d72cf5f`  
		Last Modified: Fri, 27 Sep 2024 09:11:36 GMT  
		Size: 29.1 MB (29124858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d53fbf788bd0e7b28f97c4dc927f8ab5bc32596e4d316d1e4107d63df122e3`  
		Last Modified: Fri, 27 Sep 2024 23:25:12 GMT  
		Size: 16.9 MB (16949902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2858574a09072d459734ac302f8784ee2119cd1028b5d0e81359d03e7693743`  
		Last Modified: Fri, 27 Sep 2024 23:25:10 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86aa9a6bf5e9b33a0ce592db709ac8916b028b333caa0bbdb8fba1bd2f6214cd`  
		Last Modified: Fri, 27 Sep 2024 23:25:11 GMT  
		Size: 4.6 MB (4555066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:7b17417d51f41d70cde36d9d968c36209ddd5246b2e9a87b8841b2c1aaee76fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bd0d67639923b725e3575a86ab49679b4125e46a54d6d4697146278f381a88`

```dockerfile
```

-	Layers:
	-	`sha256:55950ecb6cc8539508cfd44c53f5ad3fe2fb065c30a19cc098db41c8cf9a68da`  
		Last Modified: Fri, 27 Sep 2024 23:25:10 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:9e802780529f1ac8dc9e2a4e005a33691d9392e00937ff96d0605832f9bebbd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56730477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802dbfec090fbf25a29b5a6497cf1b84626e3b8445a70448f5e978e66beb8135`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c9398d733e6504c746da92179ca87ad112a632322da102a80b7fcfb289570b`  
		Last Modified: Thu, 17 Oct 2024 08:39:47 GMT  
		Size: 18.8 MB (18776314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29a43ed635481a1588bff095c3612c8656bc784fe29d6e2775b4687f0754952`  
		Last Modified: Thu, 17 Oct 2024 08:39:46 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4012dfdba364ca794130d1dffd077292fcb38350f73fb6278877bd25d2d8c7fc`  
		Last Modified: Thu, 17 Oct 2024 08:39:47 GMT  
		Size: 4.8 MB (4828605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:1a5fd59e01471305d46ac075911b975e8aeb9c14be98e8c2e4441ce1de6d6bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80260c15ff6e7c8aadd796f8e69434fca49c016e38b7c433fb18d14cca2bd504`

```dockerfile
```

-	Layers:
	-	`sha256:25819b0bf172f91e1cd05bc76766c461bdf1e8521e7ae7c7a0a8bbc22ca147bf`  
		Last Modified: Thu, 17 Oct 2024 08:39:47 GMT  
		Size: 5.4 MB (5373373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:354ff742b1d00d43544704361eebfaace5714e6f96f4e66b0313e9d1267af98c`  
		Last Modified: Thu, 17 Oct 2024 08:39:46 GMT  
		Size: 18.6 KB (18620 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:62d3dfafa7f8ea785b17fac4aeab1d35709c0631816835fa6904e57e336d1582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50307925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9113e290344eed8b5c9217ede2fd0b90f7b73c19455deaf66a2c37498fea6f3f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc28589ea18c5147d2150e6c305d805ff80ab242c5f64ebff3fa07cd244b1e20`  
		Last Modified: Thu, 17 Oct 2024 13:15:53 GMT  
		Size: 18.2 MB (18227811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e4c1d1c7203ba73e3baed860511382dcaba23fb316575e5b4a68aea09ad8ce`  
		Last Modified: Thu, 17 Oct 2024 13:15:52 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16802b2f05ed3d331e4ca172c0f5e0e78f969f531b192c9cab2b79fa17ca9320`  
		Last Modified: Thu, 17 Oct 2024 13:15:53 GMT  
		Size: 4.6 MB (4586676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:e5ddc58cf0baeb33e18378e5729dfafea51d5d9e6abf4ba9d3e48d5e8ea96eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5383534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548345c85d4ac645fd695bb4f1236c309665e73904bacdded8fab6976d751206`

```dockerfile
```

-	Layers:
	-	`sha256:bf5ab0e8e73932f8aba43d1f7ce78795c90e0123ee9735706a911813cc3d5fdb`  
		Last Modified: Thu, 17 Oct 2024 13:15:53 GMT  
		Size: 5.4 MB (5364980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6966e3fc81ec6a47d7dba5ee8184f4a0d792e39d59ee9ab2e594cb8c3dfe2f1a`  
		Last Modified: Thu, 17 Oct 2024 13:15:52 GMT  
		Size: 18.6 KB (18554 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:latest`

```console
$ docker pull irssi@sha256:d843f5da94333b1e5b71252558cfc96bab350fe4b5ae651a74215574f5141d77
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `irssi:latest` - linux; amd64

```console
$ docker pull irssi@sha256:8aa50d7d3ea8f42fd43067cfbb6f0de50482d7d8e3db5a50fe2598628eb02cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51991262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a6601170dc20fcf1c200d8db92a1f1b4cb70798a9bad21d6347fec54cedd7d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb24a21ee06ae2e696f315794f60683badb1fd6322bffc2a0319d2af71210d22`  
		Last Modified: Thu, 17 Oct 2024 01:21:30 GMT  
		Size: 18.3 MB (18268738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdfe65b078593a20f4d8a6a2e19a8bf4630a32c9a7de2f322b2844f2d93d438`  
		Last Modified: Thu, 17 Oct 2024 01:21:29 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5809862e7f3e9acbbd4cfdb6fa307742f16800ba62916d52f094603dda824867`  
		Last Modified: Thu, 17 Oct 2024 01:21:30 GMT  
		Size: 4.6 MB (4592881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:b14643a76798849fc221cdbff8e7ea9154d43b8eb786152f7b09914b50cb4457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bd8878fc0ba19f6256e48b5d5f656828755ecf598b5a6c70ff014b3ee3fc7c`

```dockerfile
```

-	Layers:
	-	`sha256:f8074bdb984a9cbee8b0939fbd785951f79e4c40ec6e2cabf14987ab7c996ed9`  
		Last Modified: Thu, 17 Oct 2024 01:21:30 GMT  
		Size: 5.4 MB (5365679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:944a60539d43dccd726aaed7cd2f3bd293bed84744b2dc7741271b82951374aa`  
		Last Modified: Thu, 17 Oct 2024 01:21:29 GMT  
		Size: 18.6 KB (18554 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v5

```console
$ docker pull irssi@sha256:e85a8d276df24059b698c6cc142a6506e446bfa77824eef8ce9bfa01e59a4de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48374514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8cf2dfca38be27dba04fd2515e55b60909c37be13165966482d40e007bdd01`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:c8ec8d65b2f61866a2c6085ed61e936733bc484abeeba1b91d12b9f6a97e456b in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e51d4479d9f15eaafec663087c05baede0a0724dc30787f7912ade3b686f46b1`  
		Last Modified: Thu, 17 Oct 2024 00:57:27 GMT  
		Size: 26.9 MB (26887306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df41522fb0d82bb74591eb0a6713b9bb3839d683778f8fab089fd229cbab932`  
		Last Modified: Thu, 17 Oct 2024 05:45:36 GMT  
		Size: 17.0 MB (17039325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fb9e3ff10a084e27b6bfc73e1c126d52dfb2770497d3af79313971c85d0e88`  
		Last Modified: Thu, 17 Oct 2024 05:45:35 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87475fcd2d3950e702cf8a915e34f0cc33b5d567947163f35f8b5ead687d17f`  
		Last Modified: Thu, 17 Oct 2024 05:45:35 GMT  
		Size: 4.4 MB (4444529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:d4fccfbe8c9851c23102ad85753a1eb2f86077bce99aef53d6de10c36ae00665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d43f272b6657e00c3e2aef48985598165862c59becd212cdcf2a6e41be557f1`

```dockerfile
```

-	Layers:
	-	`sha256:82a5e95b79e54c65b557fc48cafd3b3ad757a681ec457ab0dab4a03421e88b20`  
		Last Modified: Thu, 17 Oct 2024 05:45:35 GMT  
		Size: 5.4 MB (5367178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc81d93dc84be6d270a4b218df61a62925757a55ab8712283db916743c4d67ab`  
		Last Modified: Thu, 17 Oct 2024 05:45:35 GMT  
		Size: 18.7 KB (18682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v7

```console
$ docker pull irssi@sha256:12ad8e850827d74e28bde549e45ac6beaa8651c36f70afc08919d4cbc542961e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45654435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a7c45209aca883ac274fb51ef1c0c0e6d936a981a6518d42daa02f83a6a278`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f348c2f61d7048f13bbb2bf7c6015111e9341c1b2a57bb0f51c370ca45bd907`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 16.6 MB (16633805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8267612072f179f1f84c6a626ad7269f297796bd2a5cdfe38e2610ff43c9ba38`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980a4fb6213eb64092401fc4580bd066eb7536f435211170043953cb5d550b1a`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 4.3 MB (4299079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:9262df858faf119c78f44abe577174119e92d426eb5afed88413643ce45f3cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c68652ec81e35444cd943d16301610be8a1e00177afd6de2925c6813f9f4bba1`

```dockerfile
```

-	Layers:
	-	`sha256:672662f58b1c37e76367c167633e8ad8b24c5071cbe5c947ff3858f8eace60da`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 5.4 MB (5367033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf4fc54a2dd30f7fa8311901fa81effc94562db647873e07c968866f1d5b4a66`  
		Last Modified: Thu, 17 Oct 2024 14:16:34 GMT  
		Size: 18.7 KB (18682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f0a0f670eae231f1274d0e9e5097240e841843799dd4bab65297e68836f003d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51720933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad0d0f0c746e27f7c110a3107d75d817c44d4de8ae6606706e33d6296c240d3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fa218b665e0696e6cbbb7e15f224e210265c26d0938799bf2cb4ba9ddb5ed7`  
		Last Modified: Thu, 17 Oct 2024 13:13:59 GMT  
		Size: 18.0 MB (18048181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830a882aa3c01ae181d1aff028e2fbdd695f7cad16cadb69acec9ad7c6404b09`  
		Last Modified: Thu, 17 Oct 2024 13:13:58 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e603ba669c49ad6e8006dc9fd6517daadb6e830ee90614880f222bb717b5359`  
		Last Modified: Thu, 17 Oct 2024 13:13:59 GMT  
		Size: 4.5 MB (4513057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:c90a647af8cbe3ce4e36bffff2ca2dfafe6905cc26bb80f77a68a6ef84a80cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5390891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227f292d79f3a8ec728ca0caa89f4bd85fda9ee2546c35bec4f4890158b19832`

```dockerfile
```

-	Layers:
	-	`sha256:1c3ef154ce409a963bb09794d072c2b1c34a7607ff31366904498b4bfd257aae`  
		Last Modified: Thu, 17 Oct 2024 13:13:59 GMT  
		Size: 5.4 MB (5372161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb2f7fe9f657bdaeb0daa90626317db717c17908e3e479b6e71a075ba1f6dfe0`  
		Last Modified: Thu, 17 Oct 2024 13:13:58 GMT  
		Size: 18.7 KB (18730 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; 386

```console
$ docker pull irssi@sha256:0456833f0dc5f5135063a36bcdfcad14dc427a41da7ff129bb03beca4950cc90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52561651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b622b093ac5b5bccce519dbcd83e5e38b1a80607e3fc8d044d24105bd88ad07f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108ff1f82b7d31627896ef9dfa4d55dd918dd899dc1d07d811f2a973ca493272`  
		Last Modified: Thu, 17 Oct 2024 01:21:25 GMT  
		Size: 17.8 MB (17807462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab24ea74320071af584210ffe42f29229a3c32d58f2fc6b39ce817b15e727ae`  
		Last Modified: Thu, 17 Oct 2024 01:21:24 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e92c1d542ec81f26c5c8944a9622b196df4a3c8a7130c9b8d03f6a1c1601e6`  
		Last Modified: Thu, 17 Oct 2024 01:21:24 GMT  
		Size: 4.6 MB (4606565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:3ec4be7da4181fdbeb6ab8972993b6a1b52b0f88152c7c6a3bee462bfbddce93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5380258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065781f2809ba4e58b52f7baf61a835fd97eebf699650f381a447202796234b7`

```dockerfile
```

-	Layers:
	-	`sha256:75eeb53340b15ef46774f8a563ed54455d45ba0e527466054dec23fddd1ea9d1`  
		Last Modified: Thu, 17 Oct 2024 01:21:24 GMT  
		Size: 5.4 MB (5361757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa627aa524b4d75732bb320f5907ea045cd6c3c40af27a99c07e097375bba8fc`  
		Last Modified: Thu, 17 Oct 2024 01:21:24 GMT  
		Size: 18.5 KB (18501 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; mips64le

```console
$ docker pull irssi@sha256:291d87011c5c636d069d6f74c6796c03d2208d050713b23db2a301c6a54bc9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50633180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e6aa70a891ce32f5488c0353e6f02facfb108db6ba13dfb255a05038802c24`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:673970f358f62b6b095139e9647b41b9af839d4e01f7698755b040f471ff80b2 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:75358c79454e0fed44aa25dd323536443b4a1230fc432aa226620e470d72cf5f`  
		Last Modified: Fri, 27 Sep 2024 09:11:36 GMT  
		Size: 29.1 MB (29124858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d53fbf788bd0e7b28f97c4dc927f8ab5bc32596e4d316d1e4107d63df122e3`  
		Last Modified: Fri, 27 Sep 2024 23:25:12 GMT  
		Size: 16.9 MB (16949902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2858574a09072d459734ac302f8784ee2119cd1028b5d0e81359d03e7693743`  
		Last Modified: Fri, 27 Sep 2024 23:25:10 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86aa9a6bf5e9b33a0ce592db709ac8916b028b333caa0bbdb8fba1bd2f6214cd`  
		Last Modified: Fri, 27 Sep 2024 23:25:11 GMT  
		Size: 4.6 MB (4555066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:7b17417d51f41d70cde36d9d968c36209ddd5246b2e9a87b8841b2c1aaee76fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bd0d67639923b725e3575a86ab49679b4125e46a54d6d4697146278f381a88`

```dockerfile
```

-	Layers:
	-	`sha256:55950ecb6cc8539508cfd44c53f5ad3fe2fb065c30a19cc098db41c8cf9a68da`  
		Last Modified: Fri, 27 Sep 2024 23:25:10 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; ppc64le

```console
$ docker pull irssi@sha256:9e802780529f1ac8dc9e2a4e005a33691d9392e00937ff96d0605832f9bebbd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56730477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802dbfec090fbf25a29b5a6497cf1b84626e3b8445a70448f5e978e66beb8135`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c9398d733e6504c746da92179ca87ad112a632322da102a80b7fcfb289570b`  
		Last Modified: Thu, 17 Oct 2024 08:39:47 GMT  
		Size: 18.8 MB (18776314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29a43ed635481a1588bff095c3612c8656bc784fe29d6e2775b4687f0754952`  
		Last Modified: Thu, 17 Oct 2024 08:39:46 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4012dfdba364ca794130d1dffd077292fcb38350f73fb6278877bd25d2d8c7fc`  
		Last Modified: Thu, 17 Oct 2024 08:39:47 GMT  
		Size: 4.8 MB (4828605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:1a5fd59e01471305d46ac075911b975e8aeb9c14be98e8c2e4441ce1de6d6bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80260c15ff6e7c8aadd796f8e69434fca49c016e38b7c433fb18d14cca2bd504`

```dockerfile
```

-	Layers:
	-	`sha256:25819b0bf172f91e1cd05bc76766c461bdf1e8521e7ae7c7a0a8bbc22ca147bf`  
		Last Modified: Thu, 17 Oct 2024 08:39:47 GMT  
		Size: 5.4 MB (5373373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:354ff742b1d00d43544704361eebfaace5714e6f96f4e66b0313e9d1267af98c`  
		Last Modified: Thu, 17 Oct 2024 08:39:46 GMT  
		Size: 18.6 KB (18620 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; s390x

```console
$ docker pull irssi@sha256:62d3dfafa7f8ea785b17fac4aeab1d35709c0631816835fa6904e57e336d1582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50307925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9113e290344eed8b5c9217ede2fd0b90f7b73c19455deaf66a2c37498fea6f3f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc28589ea18c5147d2150e6c305d805ff80ab242c5f64ebff3fa07cd244b1e20`  
		Last Modified: Thu, 17 Oct 2024 13:15:53 GMT  
		Size: 18.2 MB (18227811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e4c1d1c7203ba73e3baed860511382dcaba23fb316575e5b4a68aea09ad8ce`  
		Last Modified: Thu, 17 Oct 2024 13:15:52 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16802b2f05ed3d331e4ca172c0f5e0e78f969f531b192c9cab2b79fa17ca9320`  
		Last Modified: Thu, 17 Oct 2024 13:15:53 GMT  
		Size: 4.6 MB (4586676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:e5ddc58cf0baeb33e18378e5729dfafea51d5d9e6abf4ba9d3e48d5e8ea96eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5383534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548345c85d4ac645fd695bb4f1236c309665e73904bacdded8fab6976d751206`

```dockerfile
```

-	Layers:
	-	`sha256:bf5ab0e8e73932f8aba43d1f7ce78795c90e0123ee9735706a911813cc3d5fdb`  
		Last Modified: Thu, 17 Oct 2024 13:15:53 GMT  
		Size: 5.4 MB (5364980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6966e3fc81ec6a47d7dba5ee8184f4a0d792e39d59ee9ab2e594cb8c3dfe2f1a`  
		Last Modified: Thu, 17 Oct 2024 13:15:52 GMT  
		Size: 18.6 KB (18554 bytes)  
		MIME: application/vnd.in-toto+json
