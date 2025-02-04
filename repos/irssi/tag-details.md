<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `irssi`

-	[`irssi:1`](#irssi1)
-	[`irssi:1-alpine`](#irssi1-alpine)
-	[`irssi:1-alpine3.21`](#irssi1-alpine321)
-	[`irssi:1-bookworm`](#irssi1-bookworm)
-	[`irssi:1.4`](#irssi14)
-	[`irssi:1.4-alpine`](#irssi14-alpine)
-	[`irssi:1.4-alpine3.21`](#irssi14-alpine321)
-	[`irssi:1.4-bookworm`](#irssi14-bookworm)
-	[`irssi:1.4.5`](#irssi145)
-	[`irssi:1.4.5-alpine`](#irssi145-alpine)
-	[`irssi:1.4.5-alpine3.21`](#irssi145-alpine321)
-	[`irssi:1.4.5-bookworm`](#irssi145-bookworm)
-	[`irssi:alpine`](#irssialpine)
-	[`irssi:alpine3.21`](#irssialpine321)
-	[`irssi:bookworm`](#irssibookworm)
-	[`irssi:latest`](#irssilatest)

## `irssi:1`

```console
$ docker pull irssi@sha256:b8d2cd8a4049dbd6a5e516a27fad3786893254901b0cbe96cf7b8886bf7c4942
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
$ docker pull irssi@sha256:03912cf04635b54b85fd210ee261a305fcd0b75d5094bce04c064eb81e05b367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51077295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ccc0d8fbc3c33f0820f01b1a454060587f8daa35c9df96d6c833fa6328086c`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d511daa4d1415f6ad1cb79745c81943a9f61f01896306f729191b612aa6da385`  
		Last Modified: Tue, 04 Feb 2025 04:22:43 GMT  
		Size: 18.3 MB (18268701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7da886d618548bbc8edd2f3505b119ff05b10ea29bfa77dec0d0db9005fcc6`  
		Last Modified: Tue, 04 Feb 2025 04:22:43 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93083499d680e9cddc0233998007046abd698e15757c31742eb433dff3a5011`  
		Last Modified: Tue, 04 Feb 2025 04:22:43 GMT  
		Size: 4.6 MB (4592934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:174243e31561a4202e6b08708e99fa9dae865a38dbddb9b0869032f782eeacae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6c362f77e9fa8569a125ec3242f05088c7129ef65f5475015dab41cec25abd`

```dockerfile
```

-	Layers:
	-	`sha256:9395cad4b9b7e2104529e3e860a2500276bb55ae3eebb114000689df0dd0e91b`  
		Last Modified: Tue, 04 Feb 2025 04:22:43 GMT  
		Size: 5.4 MB (5378443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a50dddc4319682a8ba3c43b88ee87250da64d004b77224eba699f4d40ce7d359`  
		Last Modified: Tue, 04 Feb 2025 04:22:42 GMT  
		Size: 18.7 KB (18715 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v5

```console
$ docker pull irssi@sha256:dd944eacc299fca9043f3a00584234312850041958c75a0a6d12352765957d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47224246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912ff2cc1544806cafd6236219b0efb454d1e9c7acb0a12ddb4031ba709c1652`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
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
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1258e5d59e85019768cf23e6152f950437776cfa96a36330f19be08d5e5ba1`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 17.0 MB (17039747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85eefa10fde4b95b381c673baaa58bc7a769df56f26012a5eab676834fb8b23`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa075f5f9593a4a003f660804bb8ade9b6b2da4f6dd19460fa34dde1e3fb656`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 4.4 MB (4444590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:c84f8f903292b8d9782d59a46d6a0b289f5a71bc089bde0dfa5e04a2e07f4332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f3e72502240ef6d69ad6368e81442928a515ea384405d55a4fefe0aef6904d0`

```dockerfile
```

-	Layers:
	-	`sha256:c0b21ea472520d859ac86769bdf0c5cf41720c142217ed9228036522e82e8a37`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 5.4 MB (5380052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d64f287313b7a31f8ae5875a679eb78d8b7b763891544779f5fcaecdc43322cc`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 18.8 KB (18849 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v7

```console
$ docker pull irssi@sha256:ba7c89a907137df9fc57af330fcb8d4634bb3ddde13c463b28a3aeb7959925cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44851709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66388d5089eadb184158f401a4f8b5b389ba7aae6c565e710d389eb6665ac2ec`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
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
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932cf98d70207b070896ceab0de9e238d520df78d567a209aec71355a30916aa`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 16.6 MB (16634724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84820068b052b7cae2187bf56b2d33211c396539ee172714f142dd2f0b9c948d`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898ec6f2b57f7fd8b176a35fa5a1334504aa332e8affe55eeb9ff25d73621cf8`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 4.3 MB (4299093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:8c38fbd99e47af292068fa29397214c2b4534bbe7598f0c06c61be30213c4f9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b975de2e8d2c83833261c1e8c3e8cacea19547242f5e577f3cd43b12cd99e009`

```dockerfile
```

-	Layers:
	-	`sha256:6e72488613f8e15e5a42b6366f3525135910f79b1e1c7a0f373b376dd5a0b207`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 5.4 MB (5379801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c25e19b3808062c3d6d7031500eca2c4f5f19abb6b96ec225d3a428f06dbeb9`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:0bff7107c5be3fa8a25980ae315db1b9da57e49cc94334465a6e1c07abbcddc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50606136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3c20928b6ab78915d2427093df0e4985772217b37dc3034a5b4ef3dfd8184b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5ac57f9db7aba2c602974068cfd0990b4a237e2084ee4464dca4528f2f88a2`  
		Last Modified: Tue, 04 Feb 2025 05:04:18 GMT  
		Size: 18.0 MB (18048813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768cb18511de259fecfb8830cdd7b4b39cefffd5c24fd03a2a7484a7e39e410a`  
		Last Modified: Tue, 04 Feb 2025 05:04:17 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41d11b3d9e0b41e7923110a53e52bd3c8ebc03797cd43d93d04519eea4bcf3b`  
		Last Modified: Tue, 04 Feb 2025 05:04:18 GMT  
		Size: 4.5 MB (4513086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:f3402365e17e758646f38363037821b30d5cec7a2039ca536bf0577c564273bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5403817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606d87a50640b89f893f51a5ff46677d0fd16006c373e63ac4c9ff52133a2e99`

```dockerfile
```

-	Layers:
	-	`sha256:6a18f84d3ff9162ef107a22bf2419d0e91df8f95be917a59b94c3d7405a865ad`  
		Last Modified: Tue, 04 Feb 2025 05:04:18 GMT  
		Size: 5.4 MB (5384919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97e11e03e9217e9050435b22329e4fe651256e1b9db095df49cf2d714e57ee20`  
		Last Modified: Tue, 04 Feb 2025 05:04:17 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; 386

```console
$ docker pull irssi@sha256:901c6cdf7b9d9fdc66c2e7dd015ffab8a6081181f9664809445a60c1c38f57cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51604819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9418e89975585854f86de94d18855e65e9e330eb60bb7f870487523b913eb6`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
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
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0543364fb9178760678fa313c25e29a93474ec565b26a98f7d221f081cfa6a9c`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 17.8 MB (17807283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4f54cfc888447a00950a8bed260bf83c0756e22074ac6e517d7545b44f061f`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64e4d38d8a9c3397670d282869aa68fbfdb19555a3fd1d34f7ae25f68fdb868`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 4.6 MB (4606722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:6d2c12ab302908181af339e8eb030381601052e9aa017c7f804873ff65920a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab4cc8392cf9691f665c1370a68c7c145ff1fad836c7a24e37e8d41b5ab26a9`

```dockerfile
```

-	Layers:
	-	`sha256:965d9da101532415d68a74753d9924a1e85cf63a2e8f60e7b6b137f37ff1a692`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 5.4 MB (5374522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09777d51eae80232a9001b5c2558d0d5e289cf425ee47ff2b7db36cda95c4bbe`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; mips64le

```console
$ docker pull irssi@sha256:d28818c42163119adcad0b1dcc26dd7ee850621c4356cbdcc32052b06b2f44cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49995182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d601077f4b52e3127d33d93c3fd09c9a701af11c206f79265cf5ff8a7e42466a`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
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
	-	`sha256:b08d7e697b04bda8cef97763765ebbbc16790e22945b5ab31d97d448a15c8650`  
		Last Modified: Tue, 14 Jan 2025 01:38:32 GMT  
		Size: 28.5 MB (28486647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28f67779f78f00b80585aca7c46133aac31e7a256cf0b1f9b3e60566fad8eed`  
		Last Modified: Tue, 14 Jan 2025 03:13:01 GMT  
		Size: 17.0 MB (16950218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc98bb01c2f2bf9d8d7512a480781548fb3c35c00f1f8fff06e9e26a41b1cba0`  
		Last Modified: Tue, 14 Jan 2025 03:13:00 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a398bade67980c1a0c2fcfa9e505b9f4821bdd51c3350ac55e34cf3f7e4f2aac`  
		Last Modified: Tue, 14 Jan 2025 03:13:00 GMT  
		Size: 4.6 MB (4554954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:665f345ac934ad25efb96e98503d18f9b95162467b661516823bc4ceeb08085f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:428042208a2bac18955a943d20fa3571bfa1ea754f23553c377de300f9aca094`

```dockerfile
```

-	Layers:
	-	`sha256:338f5611412cfef6ba26d4eac7ff605a2cd384cf876ff5e3d51edce260c45bb2`  
		Last Modified: Tue, 14 Jan 2025 03:13:00 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; ppc64le

```console
$ docker pull irssi@sha256:db1436694e6c5ad22d0afd0ba2487379f11b7dc537e6501ba566158fe8105fe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55654162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624e127e90e41e644939a244ce8d62bb74a540c288c2c0535b1307f1afc90102`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca063b7f943193c22ab40e7a8e97b0e148f087a20fe6419289c97b7d0ef5e29`  
		Last Modified: Tue, 04 Feb 2025 04:41:05 GMT  
		Size: 18.8 MB (18777294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5c622dc9d0af77577cf31f9d90344b8ab556071dd841eb65a65041dabe9c36`  
		Last Modified: Tue, 04 Feb 2025 04:41:04 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfcc7bc84e38fd9dceea4a35a8d5af6dff5263311cbb4059040c5c8d368ebb6c`  
		Last Modified: Tue, 04 Feb 2025 04:41:05 GMT  
		Size: 4.8 MB (4828728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:c21a2202c7b4c4f878928156b12375c7647a7362dda59b47fae6546152e32cef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c600601ba93309811b816a5fbc2cfbd876725e686dca5266591d2ecdc7d63078`

```dockerfile
```

-	Layers:
	-	`sha256:237ae9c8b196f0c7bd7c1c0add9e83abb0b11c4629c88f3329059a541b89f726`  
		Last Modified: Tue, 04 Feb 2025 04:41:05 GMT  
		Size: 5.4 MB (5386137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:967827e2da291c538712da27aa99c36482ec1592d412f1fa4635aa2517dfb2d1`  
		Last Modified: Tue, 04 Feb 2025 04:41:04 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; s390x

```console
$ docker pull irssi@sha256:118557ad5cdd352ec957387289121525cc9c6d7c237dedb0059f51973bba9393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49677205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a90444e62f0a7ecd2943f88d9460a14b97af595211a1ffd5cce125a8a52fad2`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
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
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89da8dc0f15330b25d2b981b51d661f0b4a1a93b4a88830c02b98f46631dcd0e`  
		Last Modified: Tue, 04 Feb 2025 04:50:15 GMT  
		Size: 18.2 MB (18228328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701509cd8027b019559956e107cce23e31704234e0261871b6ecae13613de4d2`  
		Last Modified: Tue, 04 Feb 2025 04:50:14 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47c46a9d50c61988c85d1cce9566c2df29abc1065542d4a3ae247d7699c4f0e`  
		Last Modified: Tue, 04 Feb 2025 04:50:14 GMT  
		Size: 4.6 MB (4586893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:8463cfba482b17372e31908c83f933c9f580c2bce5f2a8dd85834a35b925d5eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc57343be8f1aa8eb99773aa94db903bb11309cca10478dc61d9f772f975e48`

```dockerfile
```

-	Layers:
	-	`sha256:02b334568b4b4bf4bbc2080ac7d38143a78ca5cc83de2f55aa27bfb79d053bff`  
		Last Modified: Tue, 04 Feb 2025 04:50:14 GMT  
		Size: 5.4 MB (5377637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03285e941ada1088ba347bf3577bda3f4315e3964da59a1e4a022b260138852b`  
		Last Modified: Tue, 04 Feb 2025 04:50:14 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine`

```console
$ docker pull irssi@sha256:f1cdedacf033ae45b37671d63aefae07033b2a0fa3507085aa0a16255adb1d73
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
$ docker pull irssi@sha256:4193e61a40c9328c1b94ce51e9031ba03dcd3181e5d39b0c9351593d9d3df809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19987543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4186d7ecf686de55a532210964caea9788cd858e2e57e629cc98bfce33904c`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4504f7d1d5480733759d05ffb799048947251956dc083fb64f2c6180fd71bbe6`  
		Last Modified: Wed, 08 Jan 2025 18:00:08 GMT  
		Size: 10.4 MB (10401239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f16860e1b787f03fd5b37bb710d5b50605e28da9b2c3348cfd157d768c820d8`  
		Last Modified: Wed, 08 Jan 2025 18:00:07 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5436031ccb3a5ef03c713d64220269098f86f750cacef5fe3d656838ada41134`  
		Last Modified: Wed, 08 Jan 2025 18:00:08 GMT  
		Size: 5.9 MB (5943594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:ed0fd16fa5dfc1ebb8e540279c3d56f06461c47c0b4eaa56f7213d59f3b8e5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa28e6ca713aae5e0760abe87a8c1701e24b4315e06305f8e06361ee6822f5b`

```dockerfile
```

-	Layers:
	-	`sha256:94fc1e0bcc3ff5ed5a5b810abeb8277b9ec7f0b855de0306d071b5c9da2d7f02`  
		Last Modified: Wed, 08 Jan 2025 18:00:08 GMT  
		Size: 1.3 MB (1268412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:916523bbffc94549b1ff2ea0578c76d54649b18cfd72b2568821dd66668f3dad`  
		Last Modified: Wed, 08 Jan 2025 18:00:07 GMT  
		Size: 17.5 KB (17542 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:2c444becc8f59a3051899f1b7b18e61f5ac1976b48abb242ac94743d6786a431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18765986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a046672ba023e89b9eb473b361bd77e1c1014a2533ea78f24fc82d3369cba24`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd9ce7987b867c5af93522ef0a0dca7f861cb1456c6eb767e86ce82fe63cce7`  
		Last Modified: Wed, 08 Jan 2025 18:43:20 GMT  
		Size: 9.6 MB (9623095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d674e7a159f0f639e7a5021bff9aa181d8cae6336d7ff23bbd66596842a959b3`  
		Last Modified: Wed, 08 Jan 2025 18:43:20 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142129b2b5659fa1422811fe59177a83490781fb5b4a86d8275c5bd9b7ab4f21`  
		Last Modified: Wed, 08 Jan 2025 18:43:20 GMT  
		Size: 5.8 MB (5778018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:6d6fece555bab7727c0c848ecfb996f863aa6813c9814ce2fa861e93e8b01b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:069a3134f379df2190cd7556f65b5847c3f1951876aa1888e978eed8d260eb18`

```dockerfile
```

-	Layers:
	-	`sha256:d5fb6e0a557bb302e68efc005e3a5ecb0446078bb337c0a0c4f057ae96221bf8`  
		Last Modified: Wed, 08 Jan 2025 18:43:20 GMT  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:17e89e906bd000045a476506e7e9f7dd5d9035c70cc48090cad4010281aa7532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18087011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2dde65e0d23b2f156349a8a42d6c3bc1f5051b08494987065eb4a248ba5fc37`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a09db915c011952a96d8c7ca2b871e8fe1825206fe7759a30ab888cc91bb92`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 9.4 MB (9448825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acde75a6180a2de97da5d1ce62f0a9c5c4cc0b1bd19a6fcc2902647b1d54477b`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfc084ccf7459c766e83460c6a97fca525bc73643aa2723bae27ceb01142a7b`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 5.5 MB (5540079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:43913a2144b298d81f3267cf9a6f55f0c7e045815fac0a2b89f83005f1b97711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e2e5e1e7ba6c2ff85b85c46dd0ecaa5cba30daaa969a436d84eb64419d7c83`

```dockerfile
```

-	Layers:
	-	`sha256:4b8a927505163cf9f81c70e70e7c0ad65876827c5facba8fa6c05b0e2bc84b77`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 1.3 MB (1271293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b93f06e549d3f10c217b728a96ba8a80c217724b1d06f9ec3363b151fe34376`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:6e9881525ef20752b9832c3149eb0774888ae031e0c43131c707f2f21cee9eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20175650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef2f09837c399298898d414af25542ad0956de47c8d2d6894701b5865ecaa874`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df099fddd890ebfe7f630edd22f1ba8a8c64e9a9e9ded3e7624da394b887eaea`  
		Last Modified: Wed, 08 Jan 2025 18:40:12 GMT  
		Size: 10.4 MB (10360970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d169feda846a3364940c249513e4fa35fecd78cbed0ca18935dae6b0dc2066be`  
		Last Modified: Wed, 08 Jan 2025 18:40:11 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea10c87b59dafc64feccc55905a62f7d7bf66a87c13d5a061155457b6eadfc24`  
		Last Modified: Wed, 08 Jan 2025 18:40:12 GMT  
		Size: 5.8 MB (5821325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:dc724abcb64978abb5f013ad3a6632bcc41723d5b8d12a2223b8c2bd882b4f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d63fbf85996e7700610efcd716ce493e55a5867cc779533976748e6a4d60d8`

```dockerfile
```

-	Layers:
	-	`sha256:9a2585646a2f2f594aa08ff0feed38cb4df2b7371ebddd3d25f9946040742c76`  
		Last Modified: Wed, 08 Jan 2025 18:40:11 GMT  
		Size: 1.3 MB (1268516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33a53d9019370f622feed69cdf3f4b775b86e3874d014caf34d0fa72310bfb1f`  
		Last Modified: Wed, 08 Jan 2025 18:40:11 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; 386

```console
$ docker pull irssi@sha256:66bdc2d923e986725903011611db090dab933811ba58bb9a4f7449b4345e3ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19451510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9c1a6434c24f1223cf7d759e2f2f0d4ed74b6b0f5c6dc83e9921aab3bd3b0d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e695bb54ed6dd62b384f4243e489a53cfa6bf81159ac8a2d5331fa54f9bb5b93`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 10.0 MB (9955036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bff2a0e42946a090bf9cd1a1ade056259fa04da87b496116efb91a05538994`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17796159e6bf6eb0fbbd1eb96ab993de0fad5f98892f1e645d429f47333c576d`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 6.0 MB (6032353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:da09e3dde96fca610afc57dd87913c5c26769281b2e38d7990e66f7e0eb5c88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d9d648950f50f00f0452683fc547bb3a513bed5b9a83f07b7a67a7ab7c8124`

```dockerfile
```

-	Layers:
	-	`sha256:29e4298aceb4adb527f2fd00a54634db1d6c562ead9fb9576ae2c06fcff73a88`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 1.3 MB (1268367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6efc04ea8f8ec2cf101dfe86667d9e9e33a4e3623cb32cd0486036d93fc2bf47`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:77b18e9b102c70aca2fd173d672a6387d5d4e7b8d9fb2838aefe6462856daf9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20370271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714e229372660ec3a04811680ccf779431ccd182ebb90b090ddd62a4095f94bc`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3dade292c0d99d49bd8bccb4f5301fa9e6416d2ff0cab1ed87da5930f97288`  
		Last Modified: Thu, 09 Jan 2025 01:04:03 GMT  
		Size: 10.6 MB (10589990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d39712a74a770b38e3014eee3a7239d780aef10c9c024898ff964ca34f8fe3`  
		Last Modified: Thu, 09 Jan 2025 01:04:02 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bff666ec900fd764acb66933a40ed991d1ac6f8f7174503cd405e4e4b1f944`  
		Last Modified: Thu, 09 Jan 2025 01:04:03 GMT  
		Size: 6.2 MB (6205685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:1d2e5fa0de35ec1a259eb7308f3ec149d06faeda79f3fa42040fe690c244af16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6bae0bb93a6e119362f8cd6a7c5929a0c97666b020728ca1e82eebda1facdfe`

```dockerfile
```

-	Layers:
	-	`sha256:df0e9f5c297036747026956cad41a6c76e04e34e9fd890a313e013a1811aad63`  
		Last Modified: Thu, 09 Jan 2025 01:04:02 GMT  
		Size: 1.3 MB (1266519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fede1e415e2cff757a4c91851125029ac6bd4aaf5dcab8dc8adaf1b7bfcbfe21`  
		Last Modified: Thu, 09 Jan 2025 01:04:02 GMT  
		Size: 17.6 KB (17614 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:b4f5c740627fb94a821a9dbf08157f8eacc8f5a3aed7553ba47db1d9499c8f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19154010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3777b973a4d24c8082c913587f0399482c732316803c9e6a292f1961cc40d4c7`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd7ec6e781516c496daae1d6401e6540db7529619d89bbd48ce9cf60c0195e1`  
		Last Modified: Wed, 08 Jan 2025 21:22:30 GMT  
		Size: 9.8 MB (9845278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11088be527f2981fb0b5303fbc64e717db2f0647ca5771c159a30a0909c3e623`  
		Last Modified: Wed, 08 Jan 2025 21:22:28 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cfd13ced3df5fde280cc947ff2d63a6942e46ddc9f37e3475cdc61fd0bc6eb`  
		Last Modified: Wed, 08 Jan 2025 21:22:29 GMT  
		Size: 6.0 MB (5957479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:dcedd9fb51d467f4e3eaea6a0d5571c92e71eadded71c976c2221716768d9f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155919124ec5ecc222daef344381c74dce8e92e12fa1374f63ff93f93b299fba`

```dockerfile
```

-	Layers:
	-	`sha256:dafb523c6256c24d8d65125905c555948e373014d598c71c17ec2f3ccac4a89e`  
		Last Modified: Wed, 08 Jan 2025 21:22:28 GMT  
		Size: 1.3 MB (1266515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bebeba2510bf5a835d265f324e66347bd510f3ea5193d47ba886310e45981376`  
		Last Modified: Wed, 08 Jan 2025 21:22:28 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:eaca14a1db62c3011646ff5b9a0c126ffdf822d6247ca522dea4296981ff76cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20534645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9620684b7e00cbb2560ff59e10b70d42408d78441905c69e0288ca1a7ad2c120`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bc6ed4a265dfbf7241885f2a24ffd881c938d097a20d3ca7d370aa99474561`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 11.0 MB (10967495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d80f56cffc7118476df73396dc7a6e7919b6c45194ba9483ae6e18dff40a38`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c276b72ae3cd0f4f7b7e0b065f065ffb7fc942aef396f68d729eb51f65d74a`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 6.1 MB (6099288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:5f079783853eb1a971d632f0d85a17e4a1a409a1beef81c2d97faea7c670ab7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c09fbadb09c6c97be762da3c9f62a50392ab031fb8395ab730af3cdd052192b`

```dockerfile
```

-	Layers:
	-	`sha256:2d6b96935b072f35f8b3b648e02079dfa529258931ef5325a8b3a890be3bce17`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 1.3 MB (1266461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36c38183b124c53300e18138d172e1f82b2131f348c608ee58bf35e0bb207d00`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine3.21`

```console
$ docker pull irssi@sha256:f1cdedacf033ae45b37671d63aefae07033b2a0fa3507085aa0a16255adb1d73
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

### `irssi:1-alpine3.21` - linux; amd64

```console
$ docker pull irssi@sha256:4193e61a40c9328c1b94ce51e9031ba03dcd3181e5d39b0c9351593d9d3df809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19987543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4186d7ecf686de55a532210964caea9788cd858e2e57e629cc98bfce33904c`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4504f7d1d5480733759d05ffb799048947251956dc083fb64f2c6180fd71bbe6`  
		Last Modified: Wed, 08 Jan 2025 18:00:08 GMT  
		Size: 10.4 MB (10401239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f16860e1b787f03fd5b37bb710d5b50605e28da9b2c3348cfd157d768c820d8`  
		Last Modified: Wed, 08 Jan 2025 18:00:07 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5436031ccb3a5ef03c713d64220269098f86f750cacef5fe3d656838ada41134`  
		Last Modified: Wed, 08 Jan 2025 18:00:08 GMT  
		Size: 5.9 MB (5943594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:ed0fd16fa5dfc1ebb8e540279c3d56f06461c47c0b4eaa56f7213d59f3b8e5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa28e6ca713aae5e0760abe87a8c1701e24b4315e06305f8e06361ee6822f5b`

```dockerfile
```

-	Layers:
	-	`sha256:94fc1e0bcc3ff5ed5a5b810abeb8277b9ec7f0b855de0306d071b5c9da2d7f02`  
		Last Modified: Wed, 08 Jan 2025 18:00:08 GMT  
		Size: 1.3 MB (1268412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:916523bbffc94549b1ff2ea0578c76d54649b18cfd72b2568821dd66668f3dad`  
		Last Modified: Wed, 08 Jan 2025 18:00:07 GMT  
		Size: 17.5 KB (17542 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.21` - linux; arm variant v6

```console
$ docker pull irssi@sha256:2c444becc8f59a3051899f1b7b18e61f5ac1976b48abb242ac94743d6786a431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18765986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a046672ba023e89b9eb473b361bd77e1c1014a2533ea78f24fc82d3369cba24`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd9ce7987b867c5af93522ef0a0dca7f861cb1456c6eb767e86ce82fe63cce7`  
		Last Modified: Wed, 08 Jan 2025 18:43:20 GMT  
		Size: 9.6 MB (9623095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d674e7a159f0f639e7a5021bff9aa181d8cae6336d7ff23bbd66596842a959b3`  
		Last Modified: Wed, 08 Jan 2025 18:43:20 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142129b2b5659fa1422811fe59177a83490781fb5b4a86d8275c5bd9b7ab4f21`  
		Last Modified: Wed, 08 Jan 2025 18:43:20 GMT  
		Size: 5.8 MB (5778018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:6d6fece555bab7727c0c848ecfb996f863aa6813c9814ce2fa861e93e8b01b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:069a3134f379df2190cd7556f65b5847c3f1951876aa1888e978eed8d260eb18`

```dockerfile
```

-	Layers:
	-	`sha256:d5fb6e0a557bb302e68efc005e3a5ecb0446078bb337c0a0c4f057ae96221bf8`  
		Last Modified: Wed, 08 Jan 2025 18:43:20 GMT  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.21` - linux; arm variant v7

```console
$ docker pull irssi@sha256:17e89e906bd000045a476506e7e9f7dd5d9035c70cc48090cad4010281aa7532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18087011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2dde65e0d23b2f156349a8a42d6c3bc1f5051b08494987065eb4a248ba5fc37`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a09db915c011952a96d8c7ca2b871e8fe1825206fe7759a30ab888cc91bb92`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 9.4 MB (9448825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acde75a6180a2de97da5d1ce62f0a9c5c4cc0b1bd19a6fcc2902647b1d54477b`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfc084ccf7459c766e83460c6a97fca525bc73643aa2723bae27ceb01142a7b`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 5.5 MB (5540079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:43913a2144b298d81f3267cf9a6f55f0c7e045815fac0a2b89f83005f1b97711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e2e5e1e7ba6c2ff85b85c46dd0ecaa5cba30daaa969a436d84eb64419d7c83`

```dockerfile
```

-	Layers:
	-	`sha256:4b8a927505163cf9f81c70e70e7c0ad65876827c5facba8fa6c05b0e2bc84b77`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 1.3 MB (1271293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b93f06e549d3f10c217b728a96ba8a80c217724b1d06f9ec3363b151fe34376`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:6e9881525ef20752b9832c3149eb0774888ae031e0c43131c707f2f21cee9eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20175650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef2f09837c399298898d414af25542ad0956de47c8d2d6894701b5865ecaa874`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df099fddd890ebfe7f630edd22f1ba8a8c64e9a9e9ded3e7624da394b887eaea`  
		Last Modified: Wed, 08 Jan 2025 18:40:12 GMT  
		Size: 10.4 MB (10360970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d169feda846a3364940c249513e4fa35fecd78cbed0ca18935dae6b0dc2066be`  
		Last Modified: Wed, 08 Jan 2025 18:40:11 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea10c87b59dafc64feccc55905a62f7d7bf66a87c13d5a061155457b6eadfc24`  
		Last Modified: Wed, 08 Jan 2025 18:40:12 GMT  
		Size: 5.8 MB (5821325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:dc724abcb64978abb5f013ad3a6632bcc41723d5b8d12a2223b8c2bd882b4f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d63fbf85996e7700610efcd716ce493e55a5867cc779533976748e6a4d60d8`

```dockerfile
```

-	Layers:
	-	`sha256:9a2585646a2f2f594aa08ff0feed38cb4df2b7371ebddd3d25f9946040742c76`  
		Last Modified: Wed, 08 Jan 2025 18:40:11 GMT  
		Size: 1.3 MB (1268516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33a53d9019370f622feed69cdf3f4b775b86e3874d014caf34d0fa72310bfb1f`  
		Last Modified: Wed, 08 Jan 2025 18:40:11 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.21` - linux; 386

```console
$ docker pull irssi@sha256:66bdc2d923e986725903011611db090dab933811ba58bb9a4f7449b4345e3ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19451510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9c1a6434c24f1223cf7d759e2f2f0d4ed74b6b0f5c6dc83e9921aab3bd3b0d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e695bb54ed6dd62b384f4243e489a53cfa6bf81159ac8a2d5331fa54f9bb5b93`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 10.0 MB (9955036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bff2a0e42946a090bf9cd1a1ade056259fa04da87b496116efb91a05538994`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17796159e6bf6eb0fbbd1eb96ab993de0fad5f98892f1e645d429f47333c576d`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 6.0 MB (6032353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:da09e3dde96fca610afc57dd87913c5c26769281b2e38d7990e66f7e0eb5c88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d9d648950f50f00f0452683fc547bb3a513bed5b9a83f07b7a67a7ab7c8124`

```dockerfile
```

-	Layers:
	-	`sha256:29e4298aceb4adb527f2fd00a54634db1d6c562ead9fb9576ae2c06fcff73a88`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 1.3 MB (1268367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6efc04ea8f8ec2cf101dfe86667d9e9e33a4e3623cb32cd0486036d93fc2bf47`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.21` - linux; ppc64le

```console
$ docker pull irssi@sha256:77b18e9b102c70aca2fd173d672a6387d5d4e7b8d9fb2838aefe6462856daf9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20370271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714e229372660ec3a04811680ccf779431ccd182ebb90b090ddd62a4095f94bc`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3dade292c0d99d49bd8bccb4f5301fa9e6416d2ff0cab1ed87da5930f97288`  
		Last Modified: Thu, 09 Jan 2025 01:04:03 GMT  
		Size: 10.6 MB (10589990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d39712a74a770b38e3014eee3a7239d780aef10c9c024898ff964ca34f8fe3`  
		Last Modified: Thu, 09 Jan 2025 01:04:02 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bff666ec900fd764acb66933a40ed991d1ac6f8f7174503cd405e4e4b1f944`  
		Last Modified: Thu, 09 Jan 2025 01:04:03 GMT  
		Size: 6.2 MB (6205685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:1d2e5fa0de35ec1a259eb7308f3ec149d06faeda79f3fa42040fe690c244af16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6bae0bb93a6e119362f8cd6a7c5929a0c97666b020728ca1e82eebda1facdfe`

```dockerfile
```

-	Layers:
	-	`sha256:df0e9f5c297036747026956cad41a6c76e04e34e9fd890a313e013a1811aad63`  
		Last Modified: Thu, 09 Jan 2025 01:04:02 GMT  
		Size: 1.3 MB (1266519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fede1e415e2cff757a4c91851125029ac6bd4aaf5dcab8dc8adaf1b7bfcbfe21`  
		Last Modified: Thu, 09 Jan 2025 01:04:02 GMT  
		Size: 17.6 KB (17614 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.21` - linux; riscv64

```console
$ docker pull irssi@sha256:b4f5c740627fb94a821a9dbf08157f8eacc8f5a3aed7553ba47db1d9499c8f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19154010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3777b973a4d24c8082c913587f0399482c732316803c9e6a292f1961cc40d4c7`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd7ec6e781516c496daae1d6401e6540db7529619d89bbd48ce9cf60c0195e1`  
		Last Modified: Wed, 08 Jan 2025 21:22:30 GMT  
		Size: 9.8 MB (9845278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11088be527f2981fb0b5303fbc64e717db2f0647ca5771c159a30a0909c3e623`  
		Last Modified: Wed, 08 Jan 2025 21:22:28 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cfd13ced3df5fde280cc947ff2d63a6942e46ddc9f37e3475cdc61fd0bc6eb`  
		Last Modified: Wed, 08 Jan 2025 21:22:29 GMT  
		Size: 6.0 MB (5957479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:dcedd9fb51d467f4e3eaea6a0d5571c92e71eadded71c976c2221716768d9f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155919124ec5ecc222daef344381c74dce8e92e12fa1374f63ff93f93b299fba`

```dockerfile
```

-	Layers:
	-	`sha256:dafb523c6256c24d8d65125905c555948e373014d598c71c17ec2f3ccac4a89e`  
		Last Modified: Wed, 08 Jan 2025 21:22:28 GMT  
		Size: 1.3 MB (1266515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bebeba2510bf5a835d265f324e66347bd510f3ea5193d47ba886310e45981376`  
		Last Modified: Wed, 08 Jan 2025 21:22:28 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.21` - linux; s390x

```console
$ docker pull irssi@sha256:eaca14a1db62c3011646ff5b9a0c126ffdf822d6247ca522dea4296981ff76cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20534645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9620684b7e00cbb2560ff59e10b70d42408d78441905c69e0288ca1a7ad2c120`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bc6ed4a265dfbf7241885f2a24ffd881c938d097a20d3ca7d370aa99474561`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 11.0 MB (10967495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d80f56cffc7118476df73396dc7a6e7919b6c45194ba9483ae6e18dff40a38`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c276b72ae3cd0f4f7b7e0b065f065ffb7fc942aef396f68d729eb51f65d74a`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 6.1 MB (6099288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:5f079783853eb1a971d632f0d85a17e4a1a409a1beef81c2d97faea7c670ab7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c09fbadb09c6c97be762da3c9f62a50392ab031fb8395ab730af3cdd052192b`

```dockerfile
```

-	Layers:
	-	`sha256:2d6b96935b072f35f8b3b648e02079dfa529258931ef5325a8b3a890be3bce17`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 1.3 MB (1266461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36c38183b124c53300e18138d172e1f82b2131f348c608ee58bf35e0bb207d00`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-bookworm`

```console
$ docker pull irssi@sha256:b8d2cd8a4049dbd6a5e516a27fad3786893254901b0cbe96cf7b8886bf7c4942
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
$ docker pull irssi@sha256:03912cf04635b54b85fd210ee261a305fcd0b75d5094bce04c064eb81e05b367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51077295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ccc0d8fbc3c33f0820f01b1a454060587f8daa35c9df96d6c833fa6328086c`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d511daa4d1415f6ad1cb79745c81943a9f61f01896306f729191b612aa6da385`  
		Last Modified: Tue, 04 Feb 2025 04:22:43 GMT  
		Size: 18.3 MB (18268701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7da886d618548bbc8edd2f3505b119ff05b10ea29bfa77dec0d0db9005fcc6`  
		Last Modified: Tue, 04 Feb 2025 04:22:43 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93083499d680e9cddc0233998007046abd698e15757c31742eb433dff3a5011`  
		Last Modified: Tue, 04 Feb 2025 04:22:43 GMT  
		Size: 4.6 MB (4592934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:174243e31561a4202e6b08708e99fa9dae865a38dbddb9b0869032f782eeacae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6c362f77e9fa8569a125ec3242f05088c7129ef65f5475015dab41cec25abd`

```dockerfile
```

-	Layers:
	-	`sha256:9395cad4b9b7e2104529e3e860a2500276bb55ae3eebb114000689df0dd0e91b`  
		Last Modified: Tue, 04 Feb 2025 04:22:43 GMT  
		Size: 5.4 MB (5378443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a50dddc4319682a8ba3c43b88ee87250da64d004b77224eba699f4d40ce7d359`  
		Last Modified: Tue, 04 Feb 2025 04:22:42 GMT  
		Size: 18.7 KB (18715 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:dd944eacc299fca9043f3a00584234312850041958c75a0a6d12352765957d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47224246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912ff2cc1544806cafd6236219b0efb454d1e9c7acb0a12ddb4031ba709c1652`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
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
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1258e5d59e85019768cf23e6152f950437776cfa96a36330f19be08d5e5ba1`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 17.0 MB (17039747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85eefa10fde4b95b381c673baaa58bc7a769df56f26012a5eab676834fb8b23`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa075f5f9593a4a003f660804bb8ade9b6b2da4f6dd19460fa34dde1e3fb656`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 4.4 MB (4444590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c84f8f903292b8d9782d59a46d6a0b289f5a71bc089bde0dfa5e04a2e07f4332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f3e72502240ef6d69ad6368e81442928a515ea384405d55a4fefe0aef6904d0`

```dockerfile
```

-	Layers:
	-	`sha256:c0b21ea472520d859ac86769bdf0c5cf41720c142217ed9228036522e82e8a37`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 5.4 MB (5380052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d64f287313b7a31f8ae5875a679eb78d8b7b763891544779f5fcaecdc43322cc`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 18.8 KB (18849 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:ba7c89a907137df9fc57af330fcb8d4634bb3ddde13c463b28a3aeb7959925cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44851709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66388d5089eadb184158f401a4f8b5b389ba7aae6c565e710d389eb6665ac2ec`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
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
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932cf98d70207b070896ceab0de9e238d520df78d567a209aec71355a30916aa`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 16.6 MB (16634724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84820068b052b7cae2187bf56b2d33211c396539ee172714f142dd2f0b9c948d`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898ec6f2b57f7fd8b176a35fa5a1334504aa332e8affe55eeb9ff25d73621cf8`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 4.3 MB (4299093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:8c38fbd99e47af292068fa29397214c2b4534bbe7598f0c06c61be30213c4f9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b975de2e8d2c83833261c1e8c3e8cacea19547242f5e577f3cd43b12cd99e009`

```dockerfile
```

-	Layers:
	-	`sha256:6e72488613f8e15e5a42b6366f3525135910f79b1e1c7a0f373b376dd5a0b207`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 5.4 MB (5379801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c25e19b3808062c3d6d7031500eca2c4f5f19abb6b96ec225d3a428f06dbeb9`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:0bff7107c5be3fa8a25980ae315db1b9da57e49cc94334465a6e1c07abbcddc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50606136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3c20928b6ab78915d2427093df0e4985772217b37dc3034a5b4ef3dfd8184b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5ac57f9db7aba2c602974068cfd0990b4a237e2084ee4464dca4528f2f88a2`  
		Last Modified: Tue, 04 Feb 2025 05:04:18 GMT  
		Size: 18.0 MB (18048813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768cb18511de259fecfb8830cdd7b4b39cefffd5c24fd03a2a7484a7e39e410a`  
		Last Modified: Tue, 04 Feb 2025 05:04:17 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41d11b3d9e0b41e7923110a53e52bd3c8ebc03797cd43d93d04519eea4bcf3b`  
		Last Modified: Tue, 04 Feb 2025 05:04:18 GMT  
		Size: 4.5 MB (4513086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:f3402365e17e758646f38363037821b30d5cec7a2039ca536bf0577c564273bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5403817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606d87a50640b89f893f51a5ff46677d0fd16006c373e63ac4c9ff52133a2e99`

```dockerfile
```

-	Layers:
	-	`sha256:6a18f84d3ff9162ef107a22bf2419d0e91df8f95be917a59b94c3d7405a865ad`  
		Last Modified: Tue, 04 Feb 2025 05:04:18 GMT  
		Size: 5.4 MB (5384919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97e11e03e9217e9050435b22329e4fe651256e1b9db095df49cf2d714e57ee20`  
		Last Modified: Tue, 04 Feb 2025 05:04:17 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:901c6cdf7b9d9fdc66c2e7dd015ffab8a6081181f9664809445a60c1c38f57cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51604819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9418e89975585854f86de94d18855e65e9e330eb60bb7f870487523b913eb6`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
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
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0543364fb9178760678fa313c25e29a93474ec565b26a98f7d221f081cfa6a9c`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 17.8 MB (17807283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4f54cfc888447a00950a8bed260bf83c0756e22074ac6e517d7545b44f061f`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64e4d38d8a9c3397670d282869aa68fbfdb19555a3fd1d34f7ae25f68fdb868`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 4.6 MB (4606722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:6d2c12ab302908181af339e8eb030381601052e9aa017c7f804873ff65920a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab4cc8392cf9691f665c1370a68c7c145ff1fad836c7a24e37e8d41b5ab26a9`

```dockerfile
```

-	Layers:
	-	`sha256:965d9da101532415d68a74753d9924a1e85cf63a2e8f60e7b6b137f37ff1a692`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 5.4 MB (5374522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09777d51eae80232a9001b5c2558d0d5e289cf425ee47ff2b7db36cda95c4bbe`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:d28818c42163119adcad0b1dcc26dd7ee850621c4356cbdcc32052b06b2f44cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49995182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d601077f4b52e3127d33d93c3fd09c9a701af11c206f79265cf5ff8a7e42466a`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
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
	-	`sha256:b08d7e697b04bda8cef97763765ebbbc16790e22945b5ab31d97d448a15c8650`  
		Last Modified: Tue, 14 Jan 2025 01:38:32 GMT  
		Size: 28.5 MB (28486647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28f67779f78f00b80585aca7c46133aac31e7a256cf0b1f9b3e60566fad8eed`  
		Last Modified: Tue, 14 Jan 2025 03:13:01 GMT  
		Size: 17.0 MB (16950218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc98bb01c2f2bf9d8d7512a480781548fb3c35c00f1f8fff06e9e26a41b1cba0`  
		Last Modified: Tue, 14 Jan 2025 03:13:00 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a398bade67980c1a0c2fcfa9e505b9f4821bdd51c3350ac55e34cf3f7e4f2aac`  
		Last Modified: Tue, 14 Jan 2025 03:13:00 GMT  
		Size: 4.6 MB (4554954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:665f345ac934ad25efb96e98503d18f9b95162467b661516823bc4ceeb08085f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:428042208a2bac18955a943d20fa3571bfa1ea754f23553c377de300f9aca094`

```dockerfile
```

-	Layers:
	-	`sha256:338f5611412cfef6ba26d4eac7ff605a2cd384cf876ff5e3d51edce260c45bb2`  
		Last Modified: Tue, 14 Jan 2025 03:13:00 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:db1436694e6c5ad22d0afd0ba2487379f11b7dc537e6501ba566158fe8105fe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55654162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624e127e90e41e644939a244ce8d62bb74a540c288c2c0535b1307f1afc90102`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca063b7f943193c22ab40e7a8e97b0e148f087a20fe6419289c97b7d0ef5e29`  
		Last Modified: Tue, 04 Feb 2025 04:41:05 GMT  
		Size: 18.8 MB (18777294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5c622dc9d0af77577cf31f9d90344b8ab556071dd841eb65a65041dabe9c36`  
		Last Modified: Tue, 04 Feb 2025 04:41:04 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfcc7bc84e38fd9dceea4a35a8d5af6dff5263311cbb4059040c5c8d368ebb6c`  
		Last Modified: Tue, 04 Feb 2025 04:41:05 GMT  
		Size: 4.8 MB (4828728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c21a2202c7b4c4f878928156b12375c7647a7362dda59b47fae6546152e32cef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c600601ba93309811b816a5fbc2cfbd876725e686dca5266591d2ecdc7d63078`

```dockerfile
```

-	Layers:
	-	`sha256:237ae9c8b196f0c7bd7c1c0add9e83abb0b11c4629c88f3329059a541b89f726`  
		Last Modified: Tue, 04 Feb 2025 04:41:05 GMT  
		Size: 5.4 MB (5386137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:967827e2da291c538712da27aa99c36482ec1592d412f1fa4635aa2517dfb2d1`  
		Last Modified: Tue, 04 Feb 2025 04:41:04 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:118557ad5cdd352ec957387289121525cc9c6d7c237dedb0059f51973bba9393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49677205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a90444e62f0a7ecd2943f88d9460a14b97af595211a1ffd5cce125a8a52fad2`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
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
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89da8dc0f15330b25d2b981b51d661f0b4a1a93b4a88830c02b98f46631dcd0e`  
		Last Modified: Tue, 04 Feb 2025 04:50:15 GMT  
		Size: 18.2 MB (18228328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701509cd8027b019559956e107cce23e31704234e0261871b6ecae13613de4d2`  
		Last Modified: Tue, 04 Feb 2025 04:50:14 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47c46a9d50c61988c85d1cce9566c2df29abc1065542d4a3ae247d7699c4f0e`  
		Last Modified: Tue, 04 Feb 2025 04:50:14 GMT  
		Size: 4.6 MB (4586893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:8463cfba482b17372e31908c83f933c9f580c2bce5f2a8dd85834a35b925d5eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc57343be8f1aa8eb99773aa94db903bb11309cca10478dc61d9f772f975e48`

```dockerfile
```

-	Layers:
	-	`sha256:02b334568b4b4bf4bbc2080ac7d38143a78ca5cc83de2f55aa27bfb79d053bff`  
		Last Modified: Tue, 04 Feb 2025 04:50:14 GMT  
		Size: 5.4 MB (5377637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03285e941ada1088ba347bf3577bda3f4315e3964da59a1e4a022b260138852b`  
		Last Modified: Tue, 04 Feb 2025 04:50:14 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4`

```console
$ docker pull irssi@sha256:b8d2cd8a4049dbd6a5e516a27fad3786893254901b0cbe96cf7b8886bf7c4942
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
$ docker pull irssi@sha256:03912cf04635b54b85fd210ee261a305fcd0b75d5094bce04c064eb81e05b367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51077295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ccc0d8fbc3c33f0820f01b1a454060587f8daa35c9df96d6c833fa6328086c`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d511daa4d1415f6ad1cb79745c81943a9f61f01896306f729191b612aa6da385`  
		Last Modified: Tue, 04 Feb 2025 04:22:43 GMT  
		Size: 18.3 MB (18268701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7da886d618548bbc8edd2f3505b119ff05b10ea29bfa77dec0d0db9005fcc6`  
		Last Modified: Tue, 04 Feb 2025 04:22:43 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93083499d680e9cddc0233998007046abd698e15757c31742eb433dff3a5011`  
		Last Modified: Tue, 04 Feb 2025 04:22:43 GMT  
		Size: 4.6 MB (4592934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:174243e31561a4202e6b08708e99fa9dae865a38dbddb9b0869032f782eeacae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6c362f77e9fa8569a125ec3242f05088c7129ef65f5475015dab41cec25abd`

```dockerfile
```

-	Layers:
	-	`sha256:9395cad4b9b7e2104529e3e860a2500276bb55ae3eebb114000689df0dd0e91b`  
		Last Modified: Tue, 04 Feb 2025 04:22:43 GMT  
		Size: 5.4 MB (5378443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a50dddc4319682a8ba3c43b88ee87250da64d004b77224eba699f4d40ce7d359`  
		Last Modified: Tue, 04 Feb 2025 04:22:42 GMT  
		Size: 18.7 KB (18715 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v5

```console
$ docker pull irssi@sha256:dd944eacc299fca9043f3a00584234312850041958c75a0a6d12352765957d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47224246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912ff2cc1544806cafd6236219b0efb454d1e9c7acb0a12ddb4031ba709c1652`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
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
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1258e5d59e85019768cf23e6152f950437776cfa96a36330f19be08d5e5ba1`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 17.0 MB (17039747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85eefa10fde4b95b381c673baaa58bc7a769df56f26012a5eab676834fb8b23`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa075f5f9593a4a003f660804bb8ade9b6b2da4f6dd19460fa34dde1e3fb656`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 4.4 MB (4444590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:c84f8f903292b8d9782d59a46d6a0b289f5a71bc089bde0dfa5e04a2e07f4332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f3e72502240ef6d69ad6368e81442928a515ea384405d55a4fefe0aef6904d0`

```dockerfile
```

-	Layers:
	-	`sha256:c0b21ea472520d859ac86769bdf0c5cf41720c142217ed9228036522e82e8a37`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 5.4 MB (5380052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d64f287313b7a31f8ae5875a679eb78d8b7b763891544779f5fcaecdc43322cc`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 18.8 KB (18849 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v7

```console
$ docker pull irssi@sha256:ba7c89a907137df9fc57af330fcb8d4634bb3ddde13c463b28a3aeb7959925cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44851709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66388d5089eadb184158f401a4f8b5b389ba7aae6c565e710d389eb6665ac2ec`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
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
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932cf98d70207b070896ceab0de9e238d520df78d567a209aec71355a30916aa`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 16.6 MB (16634724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84820068b052b7cae2187bf56b2d33211c396539ee172714f142dd2f0b9c948d`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898ec6f2b57f7fd8b176a35fa5a1334504aa332e8affe55eeb9ff25d73621cf8`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 4.3 MB (4299093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:8c38fbd99e47af292068fa29397214c2b4534bbe7598f0c06c61be30213c4f9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b975de2e8d2c83833261c1e8c3e8cacea19547242f5e577f3cd43b12cd99e009`

```dockerfile
```

-	Layers:
	-	`sha256:6e72488613f8e15e5a42b6366f3525135910f79b1e1c7a0f373b376dd5a0b207`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 5.4 MB (5379801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c25e19b3808062c3d6d7031500eca2c4f5f19abb6b96ec225d3a428f06dbeb9`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:0bff7107c5be3fa8a25980ae315db1b9da57e49cc94334465a6e1c07abbcddc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50606136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3c20928b6ab78915d2427093df0e4985772217b37dc3034a5b4ef3dfd8184b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5ac57f9db7aba2c602974068cfd0990b4a237e2084ee4464dca4528f2f88a2`  
		Last Modified: Tue, 04 Feb 2025 05:04:18 GMT  
		Size: 18.0 MB (18048813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768cb18511de259fecfb8830cdd7b4b39cefffd5c24fd03a2a7484a7e39e410a`  
		Last Modified: Tue, 04 Feb 2025 05:04:17 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41d11b3d9e0b41e7923110a53e52bd3c8ebc03797cd43d93d04519eea4bcf3b`  
		Last Modified: Tue, 04 Feb 2025 05:04:18 GMT  
		Size: 4.5 MB (4513086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:f3402365e17e758646f38363037821b30d5cec7a2039ca536bf0577c564273bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5403817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606d87a50640b89f893f51a5ff46677d0fd16006c373e63ac4c9ff52133a2e99`

```dockerfile
```

-	Layers:
	-	`sha256:6a18f84d3ff9162ef107a22bf2419d0e91df8f95be917a59b94c3d7405a865ad`  
		Last Modified: Tue, 04 Feb 2025 05:04:18 GMT  
		Size: 5.4 MB (5384919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97e11e03e9217e9050435b22329e4fe651256e1b9db095df49cf2d714e57ee20`  
		Last Modified: Tue, 04 Feb 2025 05:04:17 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; 386

```console
$ docker pull irssi@sha256:901c6cdf7b9d9fdc66c2e7dd015ffab8a6081181f9664809445a60c1c38f57cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51604819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9418e89975585854f86de94d18855e65e9e330eb60bb7f870487523b913eb6`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
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
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0543364fb9178760678fa313c25e29a93474ec565b26a98f7d221f081cfa6a9c`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 17.8 MB (17807283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4f54cfc888447a00950a8bed260bf83c0756e22074ac6e517d7545b44f061f`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64e4d38d8a9c3397670d282869aa68fbfdb19555a3fd1d34f7ae25f68fdb868`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 4.6 MB (4606722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:6d2c12ab302908181af339e8eb030381601052e9aa017c7f804873ff65920a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab4cc8392cf9691f665c1370a68c7c145ff1fad836c7a24e37e8d41b5ab26a9`

```dockerfile
```

-	Layers:
	-	`sha256:965d9da101532415d68a74753d9924a1e85cf63a2e8f60e7b6b137f37ff1a692`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 5.4 MB (5374522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09777d51eae80232a9001b5c2558d0d5e289cf425ee47ff2b7db36cda95c4bbe`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; mips64le

```console
$ docker pull irssi@sha256:d28818c42163119adcad0b1dcc26dd7ee850621c4356cbdcc32052b06b2f44cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49995182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d601077f4b52e3127d33d93c3fd09c9a701af11c206f79265cf5ff8a7e42466a`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
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
	-	`sha256:b08d7e697b04bda8cef97763765ebbbc16790e22945b5ab31d97d448a15c8650`  
		Last Modified: Tue, 14 Jan 2025 01:38:32 GMT  
		Size: 28.5 MB (28486647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28f67779f78f00b80585aca7c46133aac31e7a256cf0b1f9b3e60566fad8eed`  
		Last Modified: Tue, 14 Jan 2025 03:13:01 GMT  
		Size: 17.0 MB (16950218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc98bb01c2f2bf9d8d7512a480781548fb3c35c00f1f8fff06e9e26a41b1cba0`  
		Last Modified: Tue, 14 Jan 2025 03:13:00 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a398bade67980c1a0c2fcfa9e505b9f4821bdd51c3350ac55e34cf3f7e4f2aac`  
		Last Modified: Tue, 14 Jan 2025 03:13:00 GMT  
		Size: 4.6 MB (4554954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:665f345ac934ad25efb96e98503d18f9b95162467b661516823bc4ceeb08085f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:428042208a2bac18955a943d20fa3571bfa1ea754f23553c377de300f9aca094`

```dockerfile
```

-	Layers:
	-	`sha256:338f5611412cfef6ba26d4eac7ff605a2cd384cf876ff5e3d51edce260c45bb2`  
		Last Modified: Tue, 14 Jan 2025 03:13:00 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; ppc64le

```console
$ docker pull irssi@sha256:db1436694e6c5ad22d0afd0ba2487379f11b7dc537e6501ba566158fe8105fe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55654162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624e127e90e41e644939a244ce8d62bb74a540c288c2c0535b1307f1afc90102`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca063b7f943193c22ab40e7a8e97b0e148f087a20fe6419289c97b7d0ef5e29`  
		Last Modified: Tue, 04 Feb 2025 04:41:05 GMT  
		Size: 18.8 MB (18777294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5c622dc9d0af77577cf31f9d90344b8ab556071dd841eb65a65041dabe9c36`  
		Last Modified: Tue, 04 Feb 2025 04:41:04 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfcc7bc84e38fd9dceea4a35a8d5af6dff5263311cbb4059040c5c8d368ebb6c`  
		Last Modified: Tue, 04 Feb 2025 04:41:05 GMT  
		Size: 4.8 MB (4828728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:c21a2202c7b4c4f878928156b12375c7647a7362dda59b47fae6546152e32cef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c600601ba93309811b816a5fbc2cfbd876725e686dca5266591d2ecdc7d63078`

```dockerfile
```

-	Layers:
	-	`sha256:237ae9c8b196f0c7bd7c1c0add9e83abb0b11c4629c88f3329059a541b89f726`  
		Last Modified: Tue, 04 Feb 2025 04:41:05 GMT  
		Size: 5.4 MB (5386137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:967827e2da291c538712da27aa99c36482ec1592d412f1fa4635aa2517dfb2d1`  
		Last Modified: Tue, 04 Feb 2025 04:41:04 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; s390x

```console
$ docker pull irssi@sha256:118557ad5cdd352ec957387289121525cc9c6d7c237dedb0059f51973bba9393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49677205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a90444e62f0a7ecd2943f88d9460a14b97af595211a1ffd5cce125a8a52fad2`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
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
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89da8dc0f15330b25d2b981b51d661f0b4a1a93b4a88830c02b98f46631dcd0e`  
		Last Modified: Tue, 04 Feb 2025 04:50:15 GMT  
		Size: 18.2 MB (18228328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701509cd8027b019559956e107cce23e31704234e0261871b6ecae13613de4d2`  
		Last Modified: Tue, 04 Feb 2025 04:50:14 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47c46a9d50c61988c85d1cce9566c2df29abc1065542d4a3ae247d7699c4f0e`  
		Last Modified: Tue, 04 Feb 2025 04:50:14 GMT  
		Size: 4.6 MB (4586893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:8463cfba482b17372e31908c83f933c9f580c2bce5f2a8dd85834a35b925d5eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc57343be8f1aa8eb99773aa94db903bb11309cca10478dc61d9f772f975e48`

```dockerfile
```

-	Layers:
	-	`sha256:02b334568b4b4bf4bbc2080ac7d38143a78ca5cc83de2f55aa27bfb79d053bff`  
		Last Modified: Tue, 04 Feb 2025 04:50:14 GMT  
		Size: 5.4 MB (5377637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03285e941ada1088ba347bf3577bda3f4315e3964da59a1e4a022b260138852b`  
		Last Modified: Tue, 04 Feb 2025 04:50:14 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine`

```console
$ docker pull irssi@sha256:f1cdedacf033ae45b37671d63aefae07033b2a0fa3507085aa0a16255adb1d73
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
$ docker pull irssi@sha256:4193e61a40c9328c1b94ce51e9031ba03dcd3181e5d39b0c9351593d9d3df809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19987543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4186d7ecf686de55a532210964caea9788cd858e2e57e629cc98bfce33904c`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4504f7d1d5480733759d05ffb799048947251956dc083fb64f2c6180fd71bbe6`  
		Last Modified: Wed, 08 Jan 2025 18:00:08 GMT  
		Size: 10.4 MB (10401239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f16860e1b787f03fd5b37bb710d5b50605e28da9b2c3348cfd157d768c820d8`  
		Last Modified: Wed, 08 Jan 2025 18:00:07 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5436031ccb3a5ef03c713d64220269098f86f750cacef5fe3d656838ada41134`  
		Last Modified: Wed, 08 Jan 2025 18:00:08 GMT  
		Size: 5.9 MB (5943594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:ed0fd16fa5dfc1ebb8e540279c3d56f06461c47c0b4eaa56f7213d59f3b8e5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa28e6ca713aae5e0760abe87a8c1701e24b4315e06305f8e06361ee6822f5b`

```dockerfile
```

-	Layers:
	-	`sha256:94fc1e0bcc3ff5ed5a5b810abeb8277b9ec7f0b855de0306d071b5c9da2d7f02`  
		Last Modified: Wed, 08 Jan 2025 18:00:08 GMT  
		Size: 1.3 MB (1268412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:916523bbffc94549b1ff2ea0578c76d54649b18cfd72b2568821dd66668f3dad`  
		Last Modified: Wed, 08 Jan 2025 18:00:07 GMT  
		Size: 17.5 KB (17542 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:2c444becc8f59a3051899f1b7b18e61f5ac1976b48abb242ac94743d6786a431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18765986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a046672ba023e89b9eb473b361bd77e1c1014a2533ea78f24fc82d3369cba24`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd9ce7987b867c5af93522ef0a0dca7f861cb1456c6eb767e86ce82fe63cce7`  
		Last Modified: Wed, 08 Jan 2025 18:43:20 GMT  
		Size: 9.6 MB (9623095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d674e7a159f0f639e7a5021bff9aa181d8cae6336d7ff23bbd66596842a959b3`  
		Last Modified: Wed, 08 Jan 2025 18:43:20 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142129b2b5659fa1422811fe59177a83490781fb5b4a86d8275c5bd9b7ab4f21`  
		Last Modified: Wed, 08 Jan 2025 18:43:20 GMT  
		Size: 5.8 MB (5778018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:6d6fece555bab7727c0c848ecfb996f863aa6813c9814ce2fa861e93e8b01b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:069a3134f379df2190cd7556f65b5847c3f1951876aa1888e978eed8d260eb18`

```dockerfile
```

-	Layers:
	-	`sha256:d5fb6e0a557bb302e68efc005e3a5ecb0446078bb337c0a0c4f057ae96221bf8`  
		Last Modified: Wed, 08 Jan 2025 18:43:20 GMT  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:17e89e906bd000045a476506e7e9f7dd5d9035c70cc48090cad4010281aa7532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18087011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2dde65e0d23b2f156349a8a42d6c3bc1f5051b08494987065eb4a248ba5fc37`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a09db915c011952a96d8c7ca2b871e8fe1825206fe7759a30ab888cc91bb92`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 9.4 MB (9448825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acde75a6180a2de97da5d1ce62f0a9c5c4cc0b1bd19a6fcc2902647b1d54477b`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfc084ccf7459c766e83460c6a97fca525bc73643aa2723bae27ceb01142a7b`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 5.5 MB (5540079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:43913a2144b298d81f3267cf9a6f55f0c7e045815fac0a2b89f83005f1b97711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e2e5e1e7ba6c2ff85b85c46dd0ecaa5cba30daaa969a436d84eb64419d7c83`

```dockerfile
```

-	Layers:
	-	`sha256:4b8a927505163cf9f81c70e70e7c0ad65876827c5facba8fa6c05b0e2bc84b77`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 1.3 MB (1271293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b93f06e549d3f10c217b728a96ba8a80c217724b1d06f9ec3363b151fe34376`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:6e9881525ef20752b9832c3149eb0774888ae031e0c43131c707f2f21cee9eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20175650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef2f09837c399298898d414af25542ad0956de47c8d2d6894701b5865ecaa874`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df099fddd890ebfe7f630edd22f1ba8a8c64e9a9e9ded3e7624da394b887eaea`  
		Last Modified: Wed, 08 Jan 2025 18:40:12 GMT  
		Size: 10.4 MB (10360970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d169feda846a3364940c249513e4fa35fecd78cbed0ca18935dae6b0dc2066be`  
		Last Modified: Wed, 08 Jan 2025 18:40:11 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea10c87b59dafc64feccc55905a62f7d7bf66a87c13d5a061155457b6eadfc24`  
		Last Modified: Wed, 08 Jan 2025 18:40:12 GMT  
		Size: 5.8 MB (5821325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:dc724abcb64978abb5f013ad3a6632bcc41723d5b8d12a2223b8c2bd882b4f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d63fbf85996e7700610efcd716ce493e55a5867cc779533976748e6a4d60d8`

```dockerfile
```

-	Layers:
	-	`sha256:9a2585646a2f2f594aa08ff0feed38cb4df2b7371ebddd3d25f9946040742c76`  
		Last Modified: Wed, 08 Jan 2025 18:40:11 GMT  
		Size: 1.3 MB (1268516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33a53d9019370f622feed69cdf3f4b775b86e3874d014caf34d0fa72310bfb1f`  
		Last Modified: Wed, 08 Jan 2025 18:40:11 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; 386

```console
$ docker pull irssi@sha256:66bdc2d923e986725903011611db090dab933811ba58bb9a4f7449b4345e3ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19451510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9c1a6434c24f1223cf7d759e2f2f0d4ed74b6b0f5c6dc83e9921aab3bd3b0d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e695bb54ed6dd62b384f4243e489a53cfa6bf81159ac8a2d5331fa54f9bb5b93`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 10.0 MB (9955036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bff2a0e42946a090bf9cd1a1ade056259fa04da87b496116efb91a05538994`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17796159e6bf6eb0fbbd1eb96ab993de0fad5f98892f1e645d429f47333c576d`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 6.0 MB (6032353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:da09e3dde96fca610afc57dd87913c5c26769281b2e38d7990e66f7e0eb5c88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d9d648950f50f00f0452683fc547bb3a513bed5b9a83f07b7a67a7ab7c8124`

```dockerfile
```

-	Layers:
	-	`sha256:29e4298aceb4adb527f2fd00a54634db1d6c562ead9fb9576ae2c06fcff73a88`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 1.3 MB (1268367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6efc04ea8f8ec2cf101dfe86667d9e9e33a4e3623cb32cd0486036d93fc2bf47`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:77b18e9b102c70aca2fd173d672a6387d5d4e7b8d9fb2838aefe6462856daf9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20370271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714e229372660ec3a04811680ccf779431ccd182ebb90b090ddd62a4095f94bc`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3dade292c0d99d49bd8bccb4f5301fa9e6416d2ff0cab1ed87da5930f97288`  
		Last Modified: Thu, 09 Jan 2025 01:04:03 GMT  
		Size: 10.6 MB (10589990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d39712a74a770b38e3014eee3a7239d780aef10c9c024898ff964ca34f8fe3`  
		Last Modified: Thu, 09 Jan 2025 01:04:02 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bff666ec900fd764acb66933a40ed991d1ac6f8f7174503cd405e4e4b1f944`  
		Last Modified: Thu, 09 Jan 2025 01:04:03 GMT  
		Size: 6.2 MB (6205685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:1d2e5fa0de35ec1a259eb7308f3ec149d06faeda79f3fa42040fe690c244af16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6bae0bb93a6e119362f8cd6a7c5929a0c97666b020728ca1e82eebda1facdfe`

```dockerfile
```

-	Layers:
	-	`sha256:df0e9f5c297036747026956cad41a6c76e04e34e9fd890a313e013a1811aad63`  
		Last Modified: Thu, 09 Jan 2025 01:04:02 GMT  
		Size: 1.3 MB (1266519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fede1e415e2cff757a4c91851125029ac6bd4aaf5dcab8dc8adaf1b7bfcbfe21`  
		Last Modified: Thu, 09 Jan 2025 01:04:02 GMT  
		Size: 17.6 KB (17614 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:b4f5c740627fb94a821a9dbf08157f8eacc8f5a3aed7553ba47db1d9499c8f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19154010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3777b973a4d24c8082c913587f0399482c732316803c9e6a292f1961cc40d4c7`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd7ec6e781516c496daae1d6401e6540db7529619d89bbd48ce9cf60c0195e1`  
		Last Modified: Wed, 08 Jan 2025 21:22:30 GMT  
		Size: 9.8 MB (9845278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11088be527f2981fb0b5303fbc64e717db2f0647ca5771c159a30a0909c3e623`  
		Last Modified: Wed, 08 Jan 2025 21:22:28 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cfd13ced3df5fde280cc947ff2d63a6942e46ddc9f37e3475cdc61fd0bc6eb`  
		Last Modified: Wed, 08 Jan 2025 21:22:29 GMT  
		Size: 6.0 MB (5957479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:dcedd9fb51d467f4e3eaea6a0d5571c92e71eadded71c976c2221716768d9f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155919124ec5ecc222daef344381c74dce8e92e12fa1374f63ff93f93b299fba`

```dockerfile
```

-	Layers:
	-	`sha256:dafb523c6256c24d8d65125905c555948e373014d598c71c17ec2f3ccac4a89e`  
		Last Modified: Wed, 08 Jan 2025 21:22:28 GMT  
		Size: 1.3 MB (1266515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bebeba2510bf5a835d265f324e66347bd510f3ea5193d47ba886310e45981376`  
		Last Modified: Wed, 08 Jan 2025 21:22:28 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:eaca14a1db62c3011646ff5b9a0c126ffdf822d6247ca522dea4296981ff76cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20534645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9620684b7e00cbb2560ff59e10b70d42408d78441905c69e0288ca1a7ad2c120`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bc6ed4a265dfbf7241885f2a24ffd881c938d097a20d3ca7d370aa99474561`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 11.0 MB (10967495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d80f56cffc7118476df73396dc7a6e7919b6c45194ba9483ae6e18dff40a38`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c276b72ae3cd0f4f7b7e0b065f065ffb7fc942aef396f68d729eb51f65d74a`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 6.1 MB (6099288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:5f079783853eb1a971d632f0d85a17e4a1a409a1beef81c2d97faea7c670ab7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c09fbadb09c6c97be762da3c9f62a50392ab031fb8395ab730af3cdd052192b`

```dockerfile
```

-	Layers:
	-	`sha256:2d6b96935b072f35f8b3b648e02079dfa529258931ef5325a8b3a890be3bce17`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 1.3 MB (1266461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36c38183b124c53300e18138d172e1f82b2131f348c608ee58bf35e0bb207d00`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine3.21`

```console
$ docker pull irssi@sha256:f1cdedacf033ae45b37671d63aefae07033b2a0fa3507085aa0a16255adb1d73
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

### `irssi:1.4-alpine3.21` - linux; amd64

```console
$ docker pull irssi@sha256:4193e61a40c9328c1b94ce51e9031ba03dcd3181e5d39b0c9351593d9d3df809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19987543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4186d7ecf686de55a532210964caea9788cd858e2e57e629cc98bfce33904c`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4504f7d1d5480733759d05ffb799048947251956dc083fb64f2c6180fd71bbe6`  
		Last Modified: Wed, 08 Jan 2025 18:00:08 GMT  
		Size: 10.4 MB (10401239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f16860e1b787f03fd5b37bb710d5b50605e28da9b2c3348cfd157d768c820d8`  
		Last Modified: Wed, 08 Jan 2025 18:00:07 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5436031ccb3a5ef03c713d64220269098f86f750cacef5fe3d656838ada41134`  
		Last Modified: Wed, 08 Jan 2025 18:00:08 GMT  
		Size: 5.9 MB (5943594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:ed0fd16fa5dfc1ebb8e540279c3d56f06461c47c0b4eaa56f7213d59f3b8e5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa28e6ca713aae5e0760abe87a8c1701e24b4315e06305f8e06361ee6822f5b`

```dockerfile
```

-	Layers:
	-	`sha256:94fc1e0bcc3ff5ed5a5b810abeb8277b9ec7f0b855de0306d071b5c9da2d7f02`  
		Last Modified: Wed, 08 Jan 2025 18:00:08 GMT  
		Size: 1.3 MB (1268412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:916523bbffc94549b1ff2ea0578c76d54649b18cfd72b2568821dd66668f3dad`  
		Last Modified: Wed, 08 Jan 2025 18:00:07 GMT  
		Size: 17.5 KB (17542 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.21` - linux; arm variant v6

```console
$ docker pull irssi@sha256:2c444becc8f59a3051899f1b7b18e61f5ac1976b48abb242ac94743d6786a431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18765986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a046672ba023e89b9eb473b361bd77e1c1014a2533ea78f24fc82d3369cba24`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd9ce7987b867c5af93522ef0a0dca7f861cb1456c6eb767e86ce82fe63cce7`  
		Last Modified: Wed, 08 Jan 2025 18:43:20 GMT  
		Size: 9.6 MB (9623095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d674e7a159f0f639e7a5021bff9aa181d8cae6336d7ff23bbd66596842a959b3`  
		Last Modified: Wed, 08 Jan 2025 18:43:20 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142129b2b5659fa1422811fe59177a83490781fb5b4a86d8275c5bd9b7ab4f21`  
		Last Modified: Wed, 08 Jan 2025 18:43:20 GMT  
		Size: 5.8 MB (5778018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:6d6fece555bab7727c0c848ecfb996f863aa6813c9814ce2fa861e93e8b01b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:069a3134f379df2190cd7556f65b5847c3f1951876aa1888e978eed8d260eb18`

```dockerfile
```

-	Layers:
	-	`sha256:d5fb6e0a557bb302e68efc005e3a5ecb0446078bb337c0a0c4f057ae96221bf8`  
		Last Modified: Wed, 08 Jan 2025 18:43:20 GMT  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.21` - linux; arm variant v7

```console
$ docker pull irssi@sha256:17e89e906bd000045a476506e7e9f7dd5d9035c70cc48090cad4010281aa7532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18087011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2dde65e0d23b2f156349a8a42d6c3bc1f5051b08494987065eb4a248ba5fc37`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a09db915c011952a96d8c7ca2b871e8fe1825206fe7759a30ab888cc91bb92`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 9.4 MB (9448825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acde75a6180a2de97da5d1ce62f0a9c5c4cc0b1bd19a6fcc2902647b1d54477b`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfc084ccf7459c766e83460c6a97fca525bc73643aa2723bae27ceb01142a7b`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 5.5 MB (5540079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:43913a2144b298d81f3267cf9a6f55f0c7e045815fac0a2b89f83005f1b97711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e2e5e1e7ba6c2ff85b85c46dd0ecaa5cba30daaa969a436d84eb64419d7c83`

```dockerfile
```

-	Layers:
	-	`sha256:4b8a927505163cf9f81c70e70e7c0ad65876827c5facba8fa6c05b0e2bc84b77`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 1.3 MB (1271293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b93f06e549d3f10c217b728a96ba8a80c217724b1d06f9ec3363b151fe34376`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:6e9881525ef20752b9832c3149eb0774888ae031e0c43131c707f2f21cee9eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20175650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef2f09837c399298898d414af25542ad0956de47c8d2d6894701b5865ecaa874`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df099fddd890ebfe7f630edd22f1ba8a8c64e9a9e9ded3e7624da394b887eaea`  
		Last Modified: Wed, 08 Jan 2025 18:40:12 GMT  
		Size: 10.4 MB (10360970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d169feda846a3364940c249513e4fa35fecd78cbed0ca18935dae6b0dc2066be`  
		Last Modified: Wed, 08 Jan 2025 18:40:11 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea10c87b59dafc64feccc55905a62f7d7bf66a87c13d5a061155457b6eadfc24`  
		Last Modified: Wed, 08 Jan 2025 18:40:12 GMT  
		Size: 5.8 MB (5821325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:dc724abcb64978abb5f013ad3a6632bcc41723d5b8d12a2223b8c2bd882b4f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d63fbf85996e7700610efcd716ce493e55a5867cc779533976748e6a4d60d8`

```dockerfile
```

-	Layers:
	-	`sha256:9a2585646a2f2f594aa08ff0feed38cb4df2b7371ebddd3d25f9946040742c76`  
		Last Modified: Wed, 08 Jan 2025 18:40:11 GMT  
		Size: 1.3 MB (1268516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33a53d9019370f622feed69cdf3f4b775b86e3874d014caf34d0fa72310bfb1f`  
		Last Modified: Wed, 08 Jan 2025 18:40:11 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.21` - linux; 386

```console
$ docker pull irssi@sha256:66bdc2d923e986725903011611db090dab933811ba58bb9a4f7449b4345e3ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19451510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9c1a6434c24f1223cf7d759e2f2f0d4ed74b6b0f5c6dc83e9921aab3bd3b0d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e695bb54ed6dd62b384f4243e489a53cfa6bf81159ac8a2d5331fa54f9bb5b93`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 10.0 MB (9955036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bff2a0e42946a090bf9cd1a1ade056259fa04da87b496116efb91a05538994`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17796159e6bf6eb0fbbd1eb96ab993de0fad5f98892f1e645d429f47333c576d`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 6.0 MB (6032353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:da09e3dde96fca610afc57dd87913c5c26769281b2e38d7990e66f7e0eb5c88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d9d648950f50f00f0452683fc547bb3a513bed5b9a83f07b7a67a7ab7c8124`

```dockerfile
```

-	Layers:
	-	`sha256:29e4298aceb4adb527f2fd00a54634db1d6c562ead9fb9576ae2c06fcff73a88`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 1.3 MB (1268367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6efc04ea8f8ec2cf101dfe86667d9e9e33a4e3623cb32cd0486036d93fc2bf47`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.21` - linux; ppc64le

```console
$ docker pull irssi@sha256:77b18e9b102c70aca2fd173d672a6387d5d4e7b8d9fb2838aefe6462856daf9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20370271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714e229372660ec3a04811680ccf779431ccd182ebb90b090ddd62a4095f94bc`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3dade292c0d99d49bd8bccb4f5301fa9e6416d2ff0cab1ed87da5930f97288`  
		Last Modified: Thu, 09 Jan 2025 01:04:03 GMT  
		Size: 10.6 MB (10589990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d39712a74a770b38e3014eee3a7239d780aef10c9c024898ff964ca34f8fe3`  
		Last Modified: Thu, 09 Jan 2025 01:04:02 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bff666ec900fd764acb66933a40ed991d1ac6f8f7174503cd405e4e4b1f944`  
		Last Modified: Thu, 09 Jan 2025 01:04:03 GMT  
		Size: 6.2 MB (6205685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:1d2e5fa0de35ec1a259eb7308f3ec149d06faeda79f3fa42040fe690c244af16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6bae0bb93a6e119362f8cd6a7c5929a0c97666b020728ca1e82eebda1facdfe`

```dockerfile
```

-	Layers:
	-	`sha256:df0e9f5c297036747026956cad41a6c76e04e34e9fd890a313e013a1811aad63`  
		Last Modified: Thu, 09 Jan 2025 01:04:02 GMT  
		Size: 1.3 MB (1266519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fede1e415e2cff757a4c91851125029ac6bd4aaf5dcab8dc8adaf1b7bfcbfe21`  
		Last Modified: Thu, 09 Jan 2025 01:04:02 GMT  
		Size: 17.6 KB (17614 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.21` - linux; riscv64

```console
$ docker pull irssi@sha256:b4f5c740627fb94a821a9dbf08157f8eacc8f5a3aed7553ba47db1d9499c8f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19154010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3777b973a4d24c8082c913587f0399482c732316803c9e6a292f1961cc40d4c7`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd7ec6e781516c496daae1d6401e6540db7529619d89bbd48ce9cf60c0195e1`  
		Last Modified: Wed, 08 Jan 2025 21:22:30 GMT  
		Size: 9.8 MB (9845278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11088be527f2981fb0b5303fbc64e717db2f0647ca5771c159a30a0909c3e623`  
		Last Modified: Wed, 08 Jan 2025 21:22:28 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cfd13ced3df5fde280cc947ff2d63a6942e46ddc9f37e3475cdc61fd0bc6eb`  
		Last Modified: Wed, 08 Jan 2025 21:22:29 GMT  
		Size: 6.0 MB (5957479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:dcedd9fb51d467f4e3eaea6a0d5571c92e71eadded71c976c2221716768d9f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155919124ec5ecc222daef344381c74dce8e92e12fa1374f63ff93f93b299fba`

```dockerfile
```

-	Layers:
	-	`sha256:dafb523c6256c24d8d65125905c555948e373014d598c71c17ec2f3ccac4a89e`  
		Last Modified: Wed, 08 Jan 2025 21:22:28 GMT  
		Size: 1.3 MB (1266515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bebeba2510bf5a835d265f324e66347bd510f3ea5193d47ba886310e45981376`  
		Last Modified: Wed, 08 Jan 2025 21:22:28 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.21` - linux; s390x

```console
$ docker pull irssi@sha256:eaca14a1db62c3011646ff5b9a0c126ffdf822d6247ca522dea4296981ff76cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20534645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9620684b7e00cbb2560ff59e10b70d42408d78441905c69e0288ca1a7ad2c120`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bc6ed4a265dfbf7241885f2a24ffd881c938d097a20d3ca7d370aa99474561`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 11.0 MB (10967495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d80f56cffc7118476df73396dc7a6e7919b6c45194ba9483ae6e18dff40a38`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c276b72ae3cd0f4f7b7e0b065f065ffb7fc942aef396f68d729eb51f65d74a`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 6.1 MB (6099288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:5f079783853eb1a971d632f0d85a17e4a1a409a1beef81c2d97faea7c670ab7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c09fbadb09c6c97be762da3c9f62a50392ab031fb8395ab730af3cdd052192b`

```dockerfile
```

-	Layers:
	-	`sha256:2d6b96935b072f35f8b3b648e02079dfa529258931ef5325a8b3a890be3bce17`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 1.3 MB (1266461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36c38183b124c53300e18138d172e1f82b2131f348c608ee58bf35e0bb207d00`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-bookworm`

```console
$ docker pull irssi@sha256:b8d2cd8a4049dbd6a5e516a27fad3786893254901b0cbe96cf7b8886bf7c4942
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
$ docker pull irssi@sha256:03912cf04635b54b85fd210ee261a305fcd0b75d5094bce04c064eb81e05b367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51077295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ccc0d8fbc3c33f0820f01b1a454060587f8daa35c9df96d6c833fa6328086c`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d511daa4d1415f6ad1cb79745c81943a9f61f01896306f729191b612aa6da385`  
		Last Modified: Tue, 04 Feb 2025 04:22:43 GMT  
		Size: 18.3 MB (18268701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7da886d618548bbc8edd2f3505b119ff05b10ea29bfa77dec0d0db9005fcc6`  
		Last Modified: Tue, 04 Feb 2025 04:22:43 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93083499d680e9cddc0233998007046abd698e15757c31742eb433dff3a5011`  
		Last Modified: Tue, 04 Feb 2025 04:22:43 GMT  
		Size: 4.6 MB (4592934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:174243e31561a4202e6b08708e99fa9dae865a38dbddb9b0869032f782eeacae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6c362f77e9fa8569a125ec3242f05088c7129ef65f5475015dab41cec25abd`

```dockerfile
```

-	Layers:
	-	`sha256:9395cad4b9b7e2104529e3e860a2500276bb55ae3eebb114000689df0dd0e91b`  
		Last Modified: Tue, 04 Feb 2025 04:22:43 GMT  
		Size: 5.4 MB (5378443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a50dddc4319682a8ba3c43b88ee87250da64d004b77224eba699f4d40ce7d359`  
		Last Modified: Tue, 04 Feb 2025 04:22:42 GMT  
		Size: 18.7 KB (18715 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:dd944eacc299fca9043f3a00584234312850041958c75a0a6d12352765957d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47224246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912ff2cc1544806cafd6236219b0efb454d1e9c7acb0a12ddb4031ba709c1652`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
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
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1258e5d59e85019768cf23e6152f950437776cfa96a36330f19be08d5e5ba1`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 17.0 MB (17039747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85eefa10fde4b95b381c673baaa58bc7a769df56f26012a5eab676834fb8b23`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa075f5f9593a4a003f660804bb8ade9b6b2da4f6dd19460fa34dde1e3fb656`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 4.4 MB (4444590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c84f8f903292b8d9782d59a46d6a0b289f5a71bc089bde0dfa5e04a2e07f4332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f3e72502240ef6d69ad6368e81442928a515ea384405d55a4fefe0aef6904d0`

```dockerfile
```

-	Layers:
	-	`sha256:c0b21ea472520d859ac86769bdf0c5cf41720c142217ed9228036522e82e8a37`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 5.4 MB (5380052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d64f287313b7a31f8ae5875a679eb78d8b7b763891544779f5fcaecdc43322cc`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 18.8 KB (18849 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:ba7c89a907137df9fc57af330fcb8d4634bb3ddde13c463b28a3aeb7959925cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44851709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66388d5089eadb184158f401a4f8b5b389ba7aae6c565e710d389eb6665ac2ec`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
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
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932cf98d70207b070896ceab0de9e238d520df78d567a209aec71355a30916aa`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 16.6 MB (16634724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84820068b052b7cae2187bf56b2d33211c396539ee172714f142dd2f0b9c948d`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898ec6f2b57f7fd8b176a35fa5a1334504aa332e8affe55eeb9ff25d73621cf8`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 4.3 MB (4299093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:8c38fbd99e47af292068fa29397214c2b4534bbe7598f0c06c61be30213c4f9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b975de2e8d2c83833261c1e8c3e8cacea19547242f5e577f3cd43b12cd99e009`

```dockerfile
```

-	Layers:
	-	`sha256:6e72488613f8e15e5a42b6366f3525135910f79b1e1c7a0f373b376dd5a0b207`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 5.4 MB (5379801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c25e19b3808062c3d6d7031500eca2c4f5f19abb6b96ec225d3a428f06dbeb9`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:0bff7107c5be3fa8a25980ae315db1b9da57e49cc94334465a6e1c07abbcddc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50606136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3c20928b6ab78915d2427093df0e4985772217b37dc3034a5b4ef3dfd8184b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5ac57f9db7aba2c602974068cfd0990b4a237e2084ee4464dca4528f2f88a2`  
		Last Modified: Tue, 04 Feb 2025 05:04:18 GMT  
		Size: 18.0 MB (18048813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768cb18511de259fecfb8830cdd7b4b39cefffd5c24fd03a2a7484a7e39e410a`  
		Last Modified: Tue, 04 Feb 2025 05:04:17 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41d11b3d9e0b41e7923110a53e52bd3c8ebc03797cd43d93d04519eea4bcf3b`  
		Last Modified: Tue, 04 Feb 2025 05:04:18 GMT  
		Size: 4.5 MB (4513086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:f3402365e17e758646f38363037821b30d5cec7a2039ca536bf0577c564273bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5403817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606d87a50640b89f893f51a5ff46677d0fd16006c373e63ac4c9ff52133a2e99`

```dockerfile
```

-	Layers:
	-	`sha256:6a18f84d3ff9162ef107a22bf2419d0e91df8f95be917a59b94c3d7405a865ad`  
		Last Modified: Tue, 04 Feb 2025 05:04:18 GMT  
		Size: 5.4 MB (5384919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97e11e03e9217e9050435b22329e4fe651256e1b9db095df49cf2d714e57ee20`  
		Last Modified: Tue, 04 Feb 2025 05:04:17 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:901c6cdf7b9d9fdc66c2e7dd015ffab8a6081181f9664809445a60c1c38f57cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51604819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9418e89975585854f86de94d18855e65e9e330eb60bb7f870487523b913eb6`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
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
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0543364fb9178760678fa313c25e29a93474ec565b26a98f7d221f081cfa6a9c`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 17.8 MB (17807283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4f54cfc888447a00950a8bed260bf83c0756e22074ac6e517d7545b44f061f`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64e4d38d8a9c3397670d282869aa68fbfdb19555a3fd1d34f7ae25f68fdb868`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 4.6 MB (4606722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:6d2c12ab302908181af339e8eb030381601052e9aa017c7f804873ff65920a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab4cc8392cf9691f665c1370a68c7c145ff1fad836c7a24e37e8d41b5ab26a9`

```dockerfile
```

-	Layers:
	-	`sha256:965d9da101532415d68a74753d9924a1e85cf63a2e8f60e7b6b137f37ff1a692`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 5.4 MB (5374522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09777d51eae80232a9001b5c2558d0d5e289cf425ee47ff2b7db36cda95c4bbe`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:d28818c42163119adcad0b1dcc26dd7ee850621c4356cbdcc32052b06b2f44cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49995182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d601077f4b52e3127d33d93c3fd09c9a701af11c206f79265cf5ff8a7e42466a`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
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
	-	`sha256:b08d7e697b04bda8cef97763765ebbbc16790e22945b5ab31d97d448a15c8650`  
		Last Modified: Tue, 14 Jan 2025 01:38:32 GMT  
		Size: 28.5 MB (28486647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28f67779f78f00b80585aca7c46133aac31e7a256cf0b1f9b3e60566fad8eed`  
		Last Modified: Tue, 14 Jan 2025 03:13:01 GMT  
		Size: 17.0 MB (16950218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc98bb01c2f2bf9d8d7512a480781548fb3c35c00f1f8fff06e9e26a41b1cba0`  
		Last Modified: Tue, 14 Jan 2025 03:13:00 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a398bade67980c1a0c2fcfa9e505b9f4821bdd51c3350ac55e34cf3f7e4f2aac`  
		Last Modified: Tue, 14 Jan 2025 03:13:00 GMT  
		Size: 4.6 MB (4554954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:665f345ac934ad25efb96e98503d18f9b95162467b661516823bc4ceeb08085f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:428042208a2bac18955a943d20fa3571bfa1ea754f23553c377de300f9aca094`

```dockerfile
```

-	Layers:
	-	`sha256:338f5611412cfef6ba26d4eac7ff605a2cd384cf876ff5e3d51edce260c45bb2`  
		Last Modified: Tue, 14 Jan 2025 03:13:00 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:db1436694e6c5ad22d0afd0ba2487379f11b7dc537e6501ba566158fe8105fe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55654162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624e127e90e41e644939a244ce8d62bb74a540c288c2c0535b1307f1afc90102`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca063b7f943193c22ab40e7a8e97b0e148f087a20fe6419289c97b7d0ef5e29`  
		Last Modified: Tue, 04 Feb 2025 04:41:05 GMT  
		Size: 18.8 MB (18777294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5c622dc9d0af77577cf31f9d90344b8ab556071dd841eb65a65041dabe9c36`  
		Last Modified: Tue, 04 Feb 2025 04:41:04 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfcc7bc84e38fd9dceea4a35a8d5af6dff5263311cbb4059040c5c8d368ebb6c`  
		Last Modified: Tue, 04 Feb 2025 04:41:05 GMT  
		Size: 4.8 MB (4828728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c21a2202c7b4c4f878928156b12375c7647a7362dda59b47fae6546152e32cef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c600601ba93309811b816a5fbc2cfbd876725e686dca5266591d2ecdc7d63078`

```dockerfile
```

-	Layers:
	-	`sha256:237ae9c8b196f0c7bd7c1c0add9e83abb0b11c4629c88f3329059a541b89f726`  
		Last Modified: Tue, 04 Feb 2025 04:41:05 GMT  
		Size: 5.4 MB (5386137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:967827e2da291c538712da27aa99c36482ec1592d412f1fa4635aa2517dfb2d1`  
		Last Modified: Tue, 04 Feb 2025 04:41:04 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:118557ad5cdd352ec957387289121525cc9c6d7c237dedb0059f51973bba9393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49677205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a90444e62f0a7ecd2943f88d9460a14b97af595211a1ffd5cce125a8a52fad2`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
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
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89da8dc0f15330b25d2b981b51d661f0b4a1a93b4a88830c02b98f46631dcd0e`  
		Last Modified: Tue, 04 Feb 2025 04:50:15 GMT  
		Size: 18.2 MB (18228328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701509cd8027b019559956e107cce23e31704234e0261871b6ecae13613de4d2`  
		Last Modified: Tue, 04 Feb 2025 04:50:14 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47c46a9d50c61988c85d1cce9566c2df29abc1065542d4a3ae247d7699c4f0e`  
		Last Modified: Tue, 04 Feb 2025 04:50:14 GMT  
		Size: 4.6 MB (4586893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:8463cfba482b17372e31908c83f933c9f580c2bce5f2a8dd85834a35b925d5eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc57343be8f1aa8eb99773aa94db903bb11309cca10478dc61d9f772f975e48`

```dockerfile
```

-	Layers:
	-	`sha256:02b334568b4b4bf4bbc2080ac7d38143a78ca5cc83de2f55aa27bfb79d053bff`  
		Last Modified: Tue, 04 Feb 2025 04:50:14 GMT  
		Size: 5.4 MB (5377637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03285e941ada1088ba347bf3577bda3f4315e3964da59a1e4a022b260138852b`  
		Last Modified: Tue, 04 Feb 2025 04:50:14 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5`

```console
$ docker pull irssi@sha256:b8d2cd8a4049dbd6a5e516a27fad3786893254901b0cbe96cf7b8886bf7c4942
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
$ docker pull irssi@sha256:03912cf04635b54b85fd210ee261a305fcd0b75d5094bce04c064eb81e05b367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51077295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ccc0d8fbc3c33f0820f01b1a454060587f8daa35c9df96d6c833fa6328086c`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d511daa4d1415f6ad1cb79745c81943a9f61f01896306f729191b612aa6da385`  
		Last Modified: Tue, 04 Feb 2025 04:22:43 GMT  
		Size: 18.3 MB (18268701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7da886d618548bbc8edd2f3505b119ff05b10ea29bfa77dec0d0db9005fcc6`  
		Last Modified: Tue, 04 Feb 2025 04:22:43 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93083499d680e9cddc0233998007046abd698e15757c31742eb433dff3a5011`  
		Last Modified: Tue, 04 Feb 2025 04:22:43 GMT  
		Size: 4.6 MB (4592934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:174243e31561a4202e6b08708e99fa9dae865a38dbddb9b0869032f782eeacae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6c362f77e9fa8569a125ec3242f05088c7129ef65f5475015dab41cec25abd`

```dockerfile
```

-	Layers:
	-	`sha256:9395cad4b9b7e2104529e3e860a2500276bb55ae3eebb114000689df0dd0e91b`  
		Last Modified: Tue, 04 Feb 2025 04:22:43 GMT  
		Size: 5.4 MB (5378443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a50dddc4319682a8ba3c43b88ee87250da64d004b77224eba699f4d40ce7d359`  
		Last Modified: Tue, 04 Feb 2025 04:22:42 GMT  
		Size: 18.7 KB (18715 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v5

```console
$ docker pull irssi@sha256:dd944eacc299fca9043f3a00584234312850041958c75a0a6d12352765957d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47224246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912ff2cc1544806cafd6236219b0efb454d1e9c7acb0a12ddb4031ba709c1652`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
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
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1258e5d59e85019768cf23e6152f950437776cfa96a36330f19be08d5e5ba1`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 17.0 MB (17039747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85eefa10fde4b95b381c673baaa58bc7a769df56f26012a5eab676834fb8b23`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa075f5f9593a4a003f660804bb8ade9b6b2da4f6dd19460fa34dde1e3fb656`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 4.4 MB (4444590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:c84f8f903292b8d9782d59a46d6a0b289f5a71bc089bde0dfa5e04a2e07f4332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f3e72502240ef6d69ad6368e81442928a515ea384405d55a4fefe0aef6904d0`

```dockerfile
```

-	Layers:
	-	`sha256:c0b21ea472520d859ac86769bdf0c5cf41720c142217ed9228036522e82e8a37`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 5.4 MB (5380052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d64f287313b7a31f8ae5875a679eb78d8b7b763891544779f5fcaecdc43322cc`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 18.8 KB (18849 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v7

```console
$ docker pull irssi@sha256:ba7c89a907137df9fc57af330fcb8d4634bb3ddde13c463b28a3aeb7959925cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44851709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66388d5089eadb184158f401a4f8b5b389ba7aae6c565e710d389eb6665ac2ec`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
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
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932cf98d70207b070896ceab0de9e238d520df78d567a209aec71355a30916aa`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 16.6 MB (16634724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84820068b052b7cae2187bf56b2d33211c396539ee172714f142dd2f0b9c948d`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898ec6f2b57f7fd8b176a35fa5a1334504aa332e8affe55eeb9ff25d73621cf8`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 4.3 MB (4299093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:8c38fbd99e47af292068fa29397214c2b4534bbe7598f0c06c61be30213c4f9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b975de2e8d2c83833261c1e8c3e8cacea19547242f5e577f3cd43b12cd99e009`

```dockerfile
```

-	Layers:
	-	`sha256:6e72488613f8e15e5a42b6366f3525135910f79b1e1c7a0f373b376dd5a0b207`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 5.4 MB (5379801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c25e19b3808062c3d6d7031500eca2c4f5f19abb6b96ec225d3a428f06dbeb9`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:0bff7107c5be3fa8a25980ae315db1b9da57e49cc94334465a6e1c07abbcddc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50606136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3c20928b6ab78915d2427093df0e4985772217b37dc3034a5b4ef3dfd8184b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5ac57f9db7aba2c602974068cfd0990b4a237e2084ee4464dca4528f2f88a2`  
		Last Modified: Tue, 04 Feb 2025 05:04:18 GMT  
		Size: 18.0 MB (18048813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768cb18511de259fecfb8830cdd7b4b39cefffd5c24fd03a2a7484a7e39e410a`  
		Last Modified: Tue, 04 Feb 2025 05:04:17 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41d11b3d9e0b41e7923110a53e52bd3c8ebc03797cd43d93d04519eea4bcf3b`  
		Last Modified: Tue, 04 Feb 2025 05:04:18 GMT  
		Size: 4.5 MB (4513086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:f3402365e17e758646f38363037821b30d5cec7a2039ca536bf0577c564273bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5403817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606d87a50640b89f893f51a5ff46677d0fd16006c373e63ac4c9ff52133a2e99`

```dockerfile
```

-	Layers:
	-	`sha256:6a18f84d3ff9162ef107a22bf2419d0e91df8f95be917a59b94c3d7405a865ad`  
		Last Modified: Tue, 04 Feb 2025 05:04:18 GMT  
		Size: 5.4 MB (5384919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97e11e03e9217e9050435b22329e4fe651256e1b9db095df49cf2d714e57ee20`  
		Last Modified: Tue, 04 Feb 2025 05:04:17 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; 386

```console
$ docker pull irssi@sha256:901c6cdf7b9d9fdc66c2e7dd015ffab8a6081181f9664809445a60c1c38f57cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51604819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9418e89975585854f86de94d18855e65e9e330eb60bb7f870487523b913eb6`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
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
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0543364fb9178760678fa313c25e29a93474ec565b26a98f7d221f081cfa6a9c`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 17.8 MB (17807283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4f54cfc888447a00950a8bed260bf83c0756e22074ac6e517d7545b44f061f`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64e4d38d8a9c3397670d282869aa68fbfdb19555a3fd1d34f7ae25f68fdb868`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 4.6 MB (4606722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:6d2c12ab302908181af339e8eb030381601052e9aa017c7f804873ff65920a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab4cc8392cf9691f665c1370a68c7c145ff1fad836c7a24e37e8d41b5ab26a9`

```dockerfile
```

-	Layers:
	-	`sha256:965d9da101532415d68a74753d9924a1e85cf63a2e8f60e7b6b137f37ff1a692`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 5.4 MB (5374522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09777d51eae80232a9001b5c2558d0d5e289cf425ee47ff2b7db36cda95c4bbe`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; mips64le

```console
$ docker pull irssi@sha256:d28818c42163119adcad0b1dcc26dd7ee850621c4356cbdcc32052b06b2f44cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49995182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d601077f4b52e3127d33d93c3fd09c9a701af11c206f79265cf5ff8a7e42466a`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
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
	-	`sha256:b08d7e697b04bda8cef97763765ebbbc16790e22945b5ab31d97d448a15c8650`  
		Last Modified: Tue, 14 Jan 2025 01:38:32 GMT  
		Size: 28.5 MB (28486647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28f67779f78f00b80585aca7c46133aac31e7a256cf0b1f9b3e60566fad8eed`  
		Last Modified: Tue, 14 Jan 2025 03:13:01 GMT  
		Size: 17.0 MB (16950218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc98bb01c2f2bf9d8d7512a480781548fb3c35c00f1f8fff06e9e26a41b1cba0`  
		Last Modified: Tue, 14 Jan 2025 03:13:00 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a398bade67980c1a0c2fcfa9e505b9f4821bdd51c3350ac55e34cf3f7e4f2aac`  
		Last Modified: Tue, 14 Jan 2025 03:13:00 GMT  
		Size: 4.6 MB (4554954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:665f345ac934ad25efb96e98503d18f9b95162467b661516823bc4ceeb08085f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:428042208a2bac18955a943d20fa3571bfa1ea754f23553c377de300f9aca094`

```dockerfile
```

-	Layers:
	-	`sha256:338f5611412cfef6ba26d4eac7ff605a2cd384cf876ff5e3d51edce260c45bb2`  
		Last Modified: Tue, 14 Jan 2025 03:13:00 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; ppc64le

```console
$ docker pull irssi@sha256:db1436694e6c5ad22d0afd0ba2487379f11b7dc537e6501ba566158fe8105fe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55654162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624e127e90e41e644939a244ce8d62bb74a540c288c2c0535b1307f1afc90102`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca063b7f943193c22ab40e7a8e97b0e148f087a20fe6419289c97b7d0ef5e29`  
		Last Modified: Tue, 04 Feb 2025 04:41:05 GMT  
		Size: 18.8 MB (18777294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5c622dc9d0af77577cf31f9d90344b8ab556071dd841eb65a65041dabe9c36`  
		Last Modified: Tue, 04 Feb 2025 04:41:04 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfcc7bc84e38fd9dceea4a35a8d5af6dff5263311cbb4059040c5c8d368ebb6c`  
		Last Modified: Tue, 04 Feb 2025 04:41:05 GMT  
		Size: 4.8 MB (4828728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:c21a2202c7b4c4f878928156b12375c7647a7362dda59b47fae6546152e32cef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c600601ba93309811b816a5fbc2cfbd876725e686dca5266591d2ecdc7d63078`

```dockerfile
```

-	Layers:
	-	`sha256:237ae9c8b196f0c7bd7c1c0add9e83abb0b11c4629c88f3329059a541b89f726`  
		Last Modified: Tue, 04 Feb 2025 04:41:05 GMT  
		Size: 5.4 MB (5386137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:967827e2da291c538712da27aa99c36482ec1592d412f1fa4635aa2517dfb2d1`  
		Last Modified: Tue, 04 Feb 2025 04:41:04 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; s390x

```console
$ docker pull irssi@sha256:118557ad5cdd352ec957387289121525cc9c6d7c237dedb0059f51973bba9393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49677205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a90444e62f0a7ecd2943f88d9460a14b97af595211a1ffd5cce125a8a52fad2`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
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
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89da8dc0f15330b25d2b981b51d661f0b4a1a93b4a88830c02b98f46631dcd0e`  
		Last Modified: Tue, 04 Feb 2025 04:50:15 GMT  
		Size: 18.2 MB (18228328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701509cd8027b019559956e107cce23e31704234e0261871b6ecae13613de4d2`  
		Last Modified: Tue, 04 Feb 2025 04:50:14 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47c46a9d50c61988c85d1cce9566c2df29abc1065542d4a3ae247d7699c4f0e`  
		Last Modified: Tue, 04 Feb 2025 04:50:14 GMT  
		Size: 4.6 MB (4586893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:8463cfba482b17372e31908c83f933c9f580c2bce5f2a8dd85834a35b925d5eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc57343be8f1aa8eb99773aa94db903bb11309cca10478dc61d9f772f975e48`

```dockerfile
```

-	Layers:
	-	`sha256:02b334568b4b4bf4bbc2080ac7d38143a78ca5cc83de2f55aa27bfb79d053bff`  
		Last Modified: Tue, 04 Feb 2025 04:50:14 GMT  
		Size: 5.4 MB (5377637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03285e941ada1088ba347bf3577bda3f4315e3964da59a1e4a022b260138852b`  
		Last Modified: Tue, 04 Feb 2025 04:50:14 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine`

```console
$ docker pull irssi@sha256:f1cdedacf033ae45b37671d63aefae07033b2a0fa3507085aa0a16255adb1d73
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
$ docker pull irssi@sha256:4193e61a40c9328c1b94ce51e9031ba03dcd3181e5d39b0c9351593d9d3df809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19987543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4186d7ecf686de55a532210964caea9788cd858e2e57e629cc98bfce33904c`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4504f7d1d5480733759d05ffb799048947251956dc083fb64f2c6180fd71bbe6`  
		Last Modified: Wed, 08 Jan 2025 18:00:08 GMT  
		Size: 10.4 MB (10401239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f16860e1b787f03fd5b37bb710d5b50605e28da9b2c3348cfd157d768c820d8`  
		Last Modified: Wed, 08 Jan 2025 18:00:07 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5436031ccb3a5ef03c713d64220269098f86f750cacef5fe3d656838ada41134`  
		Last Modified: Wed, 08 Jan 2025 18:00:08 GMT  
		Size: 5.9 MB (5943594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:ed0fd16fa5dfc1ebb8e540279c3d56f06461c47c0b4eaa56f7213d59f3b8e5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa28e6ca713aae5e0760abe87a8c1701e24b4315e06305f8e06361ee6822f5b`

```dockerfile
```

-	Layers:
	-	`sha256:94fc1e0bcc3ff5ed5a5b810abeb8277b9ec7f0b855de0306d071b5c9da2d7f02`  
		Last Modified: Wed, 08 Jan 2025 18:00:08 GMT  
		Size: 1.3 MB (1268412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:916523bbffc94549b1ff2ea0578c76d54649b18cfd72b2568821dd66668f3dad`  
		Last Modified: Wed, 08 Jan 2025 18:00:07 GMT  
		Size: 17.5 KB (17542 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:2c444becc8f59a3051899f1b7b18e61f5ac1976b48abb242ac94743d6786a431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18765986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a046672ba023e89b9eb473b361bd77e1c1014a2533ea78f24fc82d3369cba24`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd9ce7987b867c5af93522ef0a0dca7f861cb1456c6eb767e86ce82fe63cce7`  
		Last Modified: Wed, 08 Jan 2025 18:43:20 GMT  
		Size: 9.6 MB (9623095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d674e7a159f0f639e7a5021bff9aa181d8cae6336d7ff23bbd66596842a959b3`  
		Last Modified: Wed, 08 Jan 2025 18:43:20 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142129b2b5659fa1422811fe59177a83490781fb5b4a86d8275c5bd9b7ab4f21`  
		Last Modified: Wed, 08 Jan 2025 18:43:20 GMT  
		Size: 5.8 MB (5778018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:6d6fece555bab7727c0c848ecfb996f863aa6813c9814ce2fa861e93e8b01b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:069a3134f379df2190cd7556f65b5847c3f1951876aa1888e978eed8d260eb18`

```dockerfile
```

-	Layers:
	-	`sha256:d5fb6e0a557bb302e68efc005e3a5ecb0446078bb337c0a0c4f057ae96221bf8`  
		Last Modified: Wed, 08 Jan 2025 18:43:20 GMT  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:17e89e906bd000045a476506e7e9f7dd5d9035c70cc48090cad4010281aa7532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18087011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2dde65e0d23b2f156349a8a42d6c3bc1f5051b08494987065eb4a248ba5fc37`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a09db915c011952a96d8c7ca2b871e8fe1825206fe7759a30ab888cc91bb92`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 9.4 MB (9448825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acde75a6180a2de97da5d1ce62f0a9c5c4cc0b1bd19a6fcc2902647b1d54477b`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfc084ccf7459c766e83460c6a97fca525bc73643aa2723bae27ceb01142a7b`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 5.5 MB (5540079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:43913a2144b298d81f3267cf9a6f55f0c7e045815fac0a2b89f83005f1b97711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e2e5e1e7ba6c2ff85b85c46dd0ecaa5cba30daaa969a436d84eb64419d7c83`

```dockerfile
```

-	Layers:
	-	`sha256:4b8a927505163cf9f81c70e70e7c0ad65876827c5facba8fa6c05b0e2bc84b77`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 1.3 MB (1271293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b93f06e549d3f10c217b728a96ba8a80c217724b1d06f9ec3363b151fe34376`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:6e9881525ef20752b9832c3149eb0774888ae031e0c43131c707f2f21cee9eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20175650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef2f09837c399298898d414af25542ad0956de47c8d2d6894701b5865ecaa874`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df099fddd890ebfe7f630edd22f1ba8a8c64e9a9e9ded3e7624da394b887eaea`  
		Last Modified: Wed, 08 Jan 2025 18:40:12 GMT  
		Size: 10.4 MB (10360970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d169feda846a3364940c249513e4fa35fecd78cbed0ca18935dae6b0dc2066be`  
		Last Modified: Wed, 08 Jan 2025 18:40:11 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea10c87b59dafc64feccc55905a62f7d7bf66a87c13d5a061155457b6eadfc24`  
		Last Modified: Wed, 08 Jan 2025 18:40:12 GMT  
		Size: 5.8 MB (5821325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:dc724abcb64978abb5f013ad3a6632bcc41723d5b8d12a2223b8c2bd882b4f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d63fbf85996e7700610efcd716ce493e55a5867cc779533976748e6a4d60d8`

```dockerfile
```

-	Layers:
	-	`sha256:9a2585646a2f2f594aa08ff0feed38cb4df2b7371ebddd3d25f9946040742c76`  
		Last Modified: Wed, 08 Jan 2025 18:40:11 GMT  
		Size: 1.3 MB (1268516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33a53d9019370f622feed69cdf3f4b775b86e3874d014caf34d0fa72310bfb1f`  
		Last Modified: Wed, 08 Jan 2025 18:40:11 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; 386

```console
$ docker pull irssi@sha256:66bdc2d923e986725903011611db090dab933811ba58bb9a4f7449b4345e3ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19451510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9c1a6434c24f1223cf7d759e2f2f0d4ed74b6b0f5c6dc83e9921aab3bd3b0d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e695bb54ed6dd62b384f4243e489a53cfa6bf81159ac8a2d5331fa54f9bb5b93`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 10.0 MB (9955036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bff2a0e42946a090bf9cd1a1ade056259fa04da87b496116efb91a05538994`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17796159e6bf6eb0fbbd1eb96ab993de0fad5f98892f1e645d429f47333c576d`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 6.0 MB (6032353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:da09e3dde96fca610afc57dd87913c5c26769281b2e38d7990e66f7e0eb5c88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d9d648950f50f00f0452683fc547bb3a513bed5b9a83f07b7a67a7ab7c8124`

```dockerfile
```

-	Layers:
	-	`sha256:29e4298aceb4adb527f2fd00a54634db1d6c562ead9fb9576ae2c06fcff73a88`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 1.3 MB (1268367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6efc04ea8f8ec2cf101dfe86667d9e9e33a4e3623cb32cd0486036d93fc2bf47`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:77b18e9b102c70aca2fd173d672a6387d5d4e7b8d9fb2838aefe6462856daf9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20370271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714e229372660ec3a04811680ccf779431ccd182ebb90b090ddd62a4095f94bc`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3dade292c0d99d49bd8bccb4f5301fa9e6416d2ff0cab1ed87da5930f97288`  
		Last Modified: Thu, 09 Jan 2025 01:04:03 GMT  
		Size: 10.6 MB (10589990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d39712a74a770b38e3014eee3a7239d780aef10c9c024898ff964ca34f8fe3`  
		Last Modified: Thu, 09 Jan 2025 01:04:02 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bff666ec900fd764acb66933a40ed991d1ac6f8f7174503cd405e4e4b1f944`  
		Last Modified: Thu, 09 Jan 2025 01:04:03 GMT  
		Size: 6.2 MB (6205685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:1d2e5fa0de35ec1a259eb7308f3ec149d06faeda79f3fa42040fe690c244af16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6bae0bb93a6e119362f8cd6a7c5929a0c97666b020728ca1e82eebda1facdfe`

```dockerfile
```

-	Layers:
	-	`sha256:df0e9f5c297036747026956cad41a6c76e04e34e9fd890a313e013a1811aad63`  
		Last Modified: Thu, 09 Jan 2025 01:04:02 GMT  
		Size: 1.3 MB (1266519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fede1e415e2cff757a4c91851125029ac6bd4aaf5dcab8dc8adaf1b7bfcbfe21`  
		Last Modified: Thu, 09 Jan 2025 01:04:02 GMT  
		Size: 17.6 KB (17614 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:b4f5c740627fb94a821a9dbf08157f8eacc8f5a3aed7553ba47db1d9499c8f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19154010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3777b973a4d24c8082c913587f0399482c732316803c9e6a292f1961cc40d4c7`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd7ec6e781516c496daae1d6401e6540db7529619d89bbd48ce9cf60c0195e1`  
		Last Modified: Wed, 08 Jan 2025 21:22:30 GMT  
		Size: 9.8 MB (9845278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11088be527f2981fb0b5303fbc64e717db2f0647ca5771c159a30a0909c3e623`  
		Last Modified: Wed, 08 Jan 2025 21:22:28 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cfd13ced3df5fde280cc947ff2d63a6942e46ddc9f37e3475cdc61fd0bc6eb`  
		Last Modified: Wed, 08 Jan 2025 21:22:29 GMT  
		Size: 6.0 MB (5957479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:dcedd9fb51d467f4e3eaea6a0d5571c92e71eadded71c976c2221716768d9f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155919124ec5ecc222daef344381c74dce8e92e12fa1374f63ff93f93b299fba`

```dockerfile
```

-	Layers:
	-	`sha256:dafb523c6256c24d8d65125905c555948e373014d598c71c17ec2f3ccac4a89e`  
		Last Modified: Wed, 08 Jan 2025 21:22:28 GMT  
		Size: 1.3 MB (1266515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bebeba2510bf5a835d265f324e66347bd510f3ea5193d47ba886310e45981376`  
		Last Modified: Wed, 08 Jan 2025 21:22:28 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:eaca14a1db62c3011646ff5b9a0c126ffdf822d6247ca522dea4296981ff76cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20534645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9620684b7e00cbb2560ff59e10b70d42408d78441905c69e0288ca1a7ad2c120`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bc6ed4a265dfbf7241885f2a24ffd881c938d097a20d3ca7d370aa99474561`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 11.0 MB (10967495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d80f56cffc7118476df73396dc7a6e7919b6c45194ba9483ae6e18dff40a38`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c276b72ae3cd0f4f7b7e0b065f065ffb7fc942aef396f68d729eb51f65d74a`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 6.1 MB (6099288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:5f079783853eb1a971d632f0d85a17e4a1a409a1beef81c2d97faea7c670ab7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c09fbadb09c6c97be762da3c9f62a50392ab031fb8395ab730af3cdd052192b`

```dockerfile
```

-	Layers:
	-	`sha256:2d6b96935b072f35f8b3b648e02079dfa529258931ef5325a8b3a890be3bce17`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 1.3 MB (1266461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36c38183b124c53300e18138d172e1f82b2131f348c608ee58bf35e0bb207d00`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine3.21`

```console
$ docker pull irssi@sha256:f1cdedacf033ae45b37671d63aefae07033b2a0fa3507085aa0a16255adb1d73
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

### `irssi:1.4.5-alpine3.21` - linux; amd64

```console
$ docker pull irssi@sha256:4193e61a40c9328c1b94ce51e9031ba03dcd3181e5d39b0c9351593d9d3df809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19987543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4186d7ecf686de55a532210964caea9788cd858e2e57e629cc98bfce33904c`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4504f7d1d5480733759d05ffb799048947251956dc083fb64f2c6180fd71bbe6`  
		Last Modified: Wed, 08 Jan 2025 18:00:08 GMT  
		Size: 10.4 MB (10401239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f16860e1b787f03fd5b37bb710d5b50605e28da9b2c3348cfd157d768c820d8`  
		Last Modified: Wed, 08 Jan 2025 18:00:07 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5436031ccb3a5ef03c713d64220269098f86f750cacef5fe3d656838ada41134`  
		Last Modified: Wed, 08 Jan 2025 18:00:08 GMT  
		Size: 5.9 MB (5943594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:ed0fd16fa5dfc1ebb8e540279c3d56f06461c47c0b4eaa56f7213d59f3b8e5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa28e6ca713aae5e0760abe87a8c1701e24b4315e06305f8e06361ee6822f5b`

```dockerfile
```

-	Layers:
	-	`sha256:94fc1e0bcc3ff5ed5a5b810abeb8277b9ec7f0b855de0306d071b5c9da2d7f02`  
		Last Modified: Wed, 08 Jan 2025 18:00:08 GMT  
		Size: 1.3 MB (1268412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:916523bbffc94549b1ff2ea0578c76d54649b18cfd72b2568821dd66668f3dad`  
		Last Modified: Wed, 08 Jan 2025 18:00:07 GMT  
		Size: 17.5 KB (17542 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.21` - linux; arm variant v6

```console
$ docker pull irssi@sha256:2c444becc8f59a3051899f1b7b18e61f5ac1976b48abb242ac94743d6786a431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18765986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a046672ba023e89b9eb473b361bd77e1c1014a2533ea78f24fc82d3369cba24`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd9ce7987b867c5af93522ef0a0dca7f861cb1456c6eb767e86ce82fe63cce7`  
		Last Modified: Wed, 08 Jan 2025 18:43:20 GMT  
		Size: 9.6 MB (9623095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d674e7a159f0f639e7a5021bff9aa181d8cae6336d7ff23bbd66596842a959b3`  
		Last Modified: Wed, 08 Jan 2025 18:43:20 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142129b2b5659fa1422811fe59177a83490781fb5b4a86d8275c5bd9b7ab4f21`  
		Last Modified: Wed, 08 Jan 2025 18:43:20 GMT  
		Size: 5.8 MB (5778018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:6d6fece555bab7727c0c848ecfb996f863aa6813c9814ce2fa861e93e8b01b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:069a3134f379df2190cd7556f65b5847c3f1951876aa1888e978eed8d260eb18`

```dockerfile
```

-	Layers:
	-	`sha256:d5fb6e0a557bb302e68efc005e3a5ecb0446078bb337c0a0c4f057ae96221bf8`  
		Last Modified: Wed, 08 Jan 2025 18:43:20 GMT  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.21` - linux; arm variant v7

```console
$ docker pull irssi@sha256:17e89e906bd000045a476506e7e9f7dd5d9035c70cc48090cad4010281aa7532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18087011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2dde65e0d23b2f156349a8a42d6c3bc1f5051b08494987065eb4a248ba5fc37`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a09db915c011952a96d8c7ca2b871e8fe1825206fe7759a30ab888cc91bb92`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 9.4 MB (9448825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acde75a6180a2de97da5d1ce62f0a9c5c4cc0b1bd19a6fcc2902647b1d54477b`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfc084ccf7459c766e83460c6a97fca525bc73643aa2723bae27ceb01142a7b`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 5.5 MB (5540079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:43913a2144b298d81f3267cf9a6f55f0c7e045815fac0a2b89f83005f1b97711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e2e5e1e7ba6c2ff85b85c46dd0ecaa5cba30daaa969a436d84eb64419d7c83`

```dockerfile
```

-	Layers:
	-	`sha256:4b8a927505163cf9f81c70e70e7c0ad65876827c5facba8fa6c05b0e2bc84b77`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 1.3 MB (1271293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b93f06e549d3f10c217b728a96ba8a80c217724b1d06f9ec3363b151fe34376`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:6e9881525ef20752b9832c3149eb0774888ae031e0c43131c707f2f21cee9eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20175650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef2f09837c399298898d414af25542ad0956de47c8d2d6894701b5865ecaa874`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df099fddd890ebfe7f630edd22f1ba8a8c64e9a9e9ded3e7624da394b887eaea`  
		Last Modified: Wed, 08 Jan 2025 18:40:12 GMT  
		Size: 10.4 MB (10360970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d169feda846a3364940c249513e4fa35fecd78cbed0ca18935dae6b0dc2066be`  
		Last Modified: Wed, 08 Jan 2025 18:40:11 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea10c87b59dafc64feccc55905a62f7d7bf66a87c13d5a061155457b6eadfc24`  
		Last Modified: Wed, 08 Jan 2025 18:40:12 GMT  
		Size: 5.8 MB (5821325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:dc724abcb64978abb5f013ad3a6632bcc41723d5b8d12a2223b8c2bd882b4f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d63fbf85996e7700610efcd716ce493e55a5867cc779533976748e6a4d60d8`

```dockerfile
```

-	Layers:
	-	`sha256:9a2585646a2f2f594aa08ff0feed38cb4df2b7371ebddd3d25f9946040742c76`  
		Last Modified: Wed, 08 Jan 2025 18:40:11 GMT  
		Size: 1.3 MB (1268516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33a53d9019370f622feed69cdf3f4b775b86e3874d014caf34d0fa72310bfb1f`  
		Last Modified: Wed, 08 Jan 2025 18:40:11 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.21` - linux; 386

```console
$ docker pull irssi@sha256:66bdc2d923e986725903011611db090dab933811ba58bb9a4f7449b4345e3ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19451510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9c1a6434c24f1223cf7d759e2f2f0d4ed74b6b0f5c6dc83e9921aab3bd3b0d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e695bb54ed6dd62b384f4243e489a53cfa6bf81159ac8a2d5331fa54f9bb5b93`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 10.0 MB (9955036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bff2a0e42946a090bf9cd1a1ade056259fa04da87b496116efb91a05538994`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17796159e6bf6eb0fbbd1eb96ab993de0fad5f98892f1e645d429f47333c576d`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 6.0 MB (6032353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:da09e3dde96fca610afc57dd87913c5c26769281b2e38d7990e66f7e0eb5c88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d9d648950f50f00f0452683fc547bb3a513bed5b9a83f07b7a67a7ab7c8124`

```dockerfile
```

-	Layers:
	-	`sha256:29e4298aceb4adb527f2fd00a54634db1d6c562ead9fb9576ae2c06fcff73a88`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 1.3 MB (1268367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6efc04ea8f8ec2cf101dfe86667d9e9e33a4e3623cb32cd0486036d93fc2bf47`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.21` - linux; ppc64le

```console
$ docker pull irssi@sha256:77b18e9b102c70aca2fd173d672a6387d5d4e7b8d9fb2838aefe6462856daf9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20370271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714e229372660ec3a04811680ccf779431ccd182ebb90b090ddd62a4095f94bc`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3dade292c0d99d49bd8bccb4f5301fa9e6416d2ff0cab1ed87da5930f97288`  
		Last Modified: Thu, 09 Jan 2025 01:04:03 GMT  
		Size: 10.6 MB (10589990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d39712a74a770b38e3014eee3a7239d780aef10c9c024898ff964ca34f8fe3`  
		Last Modified: Thu, 09 Jan 2025 01:04:02 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bff666ec900fd764acb66933a40ed991d1ac6f8f7174503cd405e4e4b1f944`  
		Last Modified: Thu, 09 Jan 2025 01:04:03 GMT  
		Size: 6.2 MB (6205685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:1d2e5fa0de35ec1a259eb7308f3ec149d06faeda79f3fa42040fe690c244af16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6bae0bb93a6e119362f8cd6a7c5929a0c97666b020728ca1e82eebda1facdfe`

```dockerfile
```

-	Layers:
	-	`sha256:df0e9f5c297036747026956cad41a6c76e04e34e9fd890a313e013a1811aad63`  
		Last Modified: Thu, 09 Jan 2025 01:04:02 GMT  
		Size: 1.3 MB (1266519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fede1e415e2cff757a4c91851125029ac6bd4aaf5dcab8dc8adaf1b7bfcbfe21`  
		Last Modified: Thu, 09 Jan 2025 01:04:02 GMT  
		Size: 17.6 KB (17614 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.21` - linux; riscv64

```console
$ docker pull irssi@sha256:b4f5c740627fb94a821a9dbf08157f8eacc8f5a3aed7553ba47db1d9499c8f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19154010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3777b973a4d24c8082c913587f0399482c732316803c9e6a292f1961cc40d4c7`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd7ec6e781516c496daae1d6401e6540db7529619d89bbd48ce9cf60c0195e1`  
		Last Modified: Wed, 08 Jan 2025 21:22:30 GMT  
		Size: 9.8 MB (9845278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11088be527f2981fb0b5303fbc64e717db2f0647ca5771c159a30a0909c3e623`  
		Last Modified: Wed, 08 Jan 2025 21:22:28 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cfd13ced3df5fde280cc947ff2d63a6942e46ddc9f37e3475cdc61fd0bc6eb`  
		Last Modified: Wed, 08 Jan 2025 21:22:29 GMT  
		Size: 6.0 MB (5957479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:dcedd9fb51d467f4e3eaea6a0d5571c92e71eadded71c976c2221716768d9f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155919124ec5ecc222daef344381c74dce8e92e12fa1374f63ff93f93b299fba`

```dockerfile
```

-	Layers:
	-	`sha256:dafb523c6256c24d8d65125905c555948e373014d598c71c17ec2f3ccac4a89e`  
		Last Modified: Wed, 08 Jan 2025 21:22:28 GMT  
		Size: 1.3 MB (1266515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bebeba2510bf5a835d265f324e66347bd510f3ea5193d47ba886310e45981376`  
		Last Modified: Wed, 08 Jan 2025 21:22:28 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.21` - linux; s390x

```console
$ docker pull irssi@sha256:eaca14a1db62c3011646ff5b9a0c126ffdf822d6247ca522dea4296981ff76cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20534645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9620684b7e00cbb2560ff59e10b70d42408d78441905c69e0288ca1a7ad2c120`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bc6ed4a265dfbf7241885f2a24ffd881c938d097a20d3ca7d370aa99474561`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 11.0 MB (10967495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d80f56cffc7118476df73396dc7a6e7919b6c45194ba9483ae6e18dff40a38`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c276b72ae3cd0f4f7b7e0b065f065ffb7fc942aef396f68d729eb51f65d74a`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 6.1 MB (6099288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:5f079783853eb1a971d632f0d85a17e4a1a409a1beef81c2d97faea7c670ab7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c09fbadb09c6c97be762da3c9f62a50392ab031fb8395ab730af3cdd052192b`

```dockerfile
```

-	Layers:
	-	`sha256:2d6b96935b072f35f8b3b648e02079dfa529258931ef5325a8b3a890be3bce17`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 1.3 MB (1266461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36c38183b124c53300e18138d172e1f82b2131f348c608ee58bf35e0bb207d00`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-bookworm`

```console
$ docker pull irssi@sha256:b8d2cd8a4049dbd6a5e516a27fad3786893254901b0cbe96cf7b8886bf7c4942
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
$ docker pull irssi@sha256:03912cf04635b54b85fd210ee261a305fcd0b75d5094bce04c064eb81e05b367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51077295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ccc0d8fbc3c33f0820f01b1a454060587f8daa35c9df96d6c833fa6328086c`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d511daa4d1415f6ad1cb79745c81943a9f61f01896306f729191b612aa6da385`  
		Last Modified: Tue, 04 Feb 2025 04:22:43 GMT  
		Size: 18.3 MB (18268701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7da886d618548bbc8edd2f3505b119ff05b10ea29bfa77dec0d0db9005fcc6`  
		Last Modified: Tue, 04 Feb 2025 04:22:43 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93083499d680e9cddc0233998007046abd698e15757c31742eb433dff3a5011`  
		Last Modified: Tue, 04 Feb 2025 04:22:43 GMT  
		Size: 4.6 MB (4592934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:174243e31561a4202e6b08708e99fa9dae865a38dbddb9b0869032f782eeacae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6c362f77e9fa8569a125ec3242f05088c7129ef65f5475015dab41cec25abd`

```dockerfile
```

-	Layers:
	-	`sha256:9395cad4b9b7e2104529e3e860a2500276bb55ae3eebb114000689df0dd0e91b`  
		Last Modified: Tue, 04 Feb 2025 04:22:43 GMT  
		Size: 5.4 MB (5378443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a50dddc4319682a8ba3c43b88ee87250da64d004b77224eba699f4d40ce7d359`  
		Last Modified: Tue, 04 Feb 2025 04:22:42 GMT  
		Size: 18.7 KB (18715 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:dd944eacc299fca9043f3a00584234312850041958c75a0a6d12352765957d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47224246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912ff2cc1544806cafd6236219b0efb454d1e9c7acb0a12ddb4031ba709c1652`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
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
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1258e5d59e85019768cf23e6152f950437776cfa96a36330f19be08d5e5ba1`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 17.0 MB (17039747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85eefa10fde4b95b381c673baaa58bc7a769df56f26012a5eab676834fb8b23`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa075f5f9593a4a003f660804bb8ade9b6b2da4f6dd19460fa34dde1e3fb656`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 4.4 MB (4444590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c84f8f903292b8d9782d59a46d6a0b289f5a71bc089bde0dfa5e04a2e07f4332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f3e72502240ef6d69ad6368e81442928a515ea384405d55a4fefe0aef6904d0`

```dockerfile
```

-	Layers:
	-	`sha256:c0b21ea472520d859ac86769bdf0c5cf41720c142217ed9228036522e82e8a37`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 5.4 MB (5380052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d64f287313b7a31f8ae5875a679eb78d8b7b763891544779f5fcaecdc43322cc`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 18.8 KB (18849 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:ba7c89a907137df9fc57af330fcb8d4634bb3ddde13c463b28a3aeb7959925cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44851709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66388d5089eadb184158f401a4f8b5b389ba7aae6c565e710d389eb6665ac2ec`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
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
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932cf98d70207b070896ceab0de9e238d520df78d567a209aec71355a30916aa`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 16.6 MB (16634724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84820068b052b7cae2187bf56b2d33211c396539ee172714f142dd2f0b9c948d`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898ec6f2b57f7fd8b176a35fa5a1334504aa332e8affe55eeb9ff25d73621cf8`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 4.3 MB (4299093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:8c38fbd99e47af292068fa29397214c2b4534bbe7598f0c06c61be30213c4f9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b975de2e8d2c83833261c1e8c3e8cacea19547242f5e577f3cd43b12cd99e009`

```dockerfile
```

-	Layers:
	-	`sha256:6e72488613f8e15e5a42b6366f3525135910f79b1e1c7a0f373b376dd5a0b207`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 5.4 MB (5379801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c25e19b3808062c3d6d7031500eca2c4f5f19abb6b96ec225d3a428f06dbeb9`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:0bff7107c5be3fa8a25980ae315db1b9da57e49cc94334465a6e1c07abbcddc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50606136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3c20928b6ab78915d2427093df0e4985772217b37dc3034a5b4ef3dfd8184b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5ac57f9db7aba2c602974068cfd0990b4a237e2084ee4464dca4528f2f88a2`  
		Last Modified: Tue, 04 Feb 2025 05:04:18 GMT  
		Size: 18.0 MB (18048813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768cb18511de259fecfb8830cdd7b4b39cefffd5c24fd03a2a7484a7e39e410a`  
		Last Modified: Tue, 04 Feb 2025 05:04:17 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41d11b3d9e0b41e7923110a53e52bd3c8ebc03797cd43d93d04519eea4bcf3b`  
		Last Modified: Tue, 04 Feb 2025 05:04:18 GMT  
		Size: 4.5 MB (4513086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:f3402365e17e758646f38363037821b30d5cec7a2039ca536bf0577c564273bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5403817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606d87a50640b89f893f51a5ff46677d0fd16006c373e63ac4c9ff52133a2e99`

```dockerfile
```

-	Layers:
	-	`sha256:6a18f84d3ff9162ef107a22bf2419d0e91df8f95be917a59b94c3d7405a865ad`  
		Last Modified: Tue, 04 Feb 2025 05:04:18 GMT  
		Size: 5.4 MB (5384919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97e11e03e9217e9050435b22329e4fe651256e1b9db095df49cf2d714e57ee20`  
		Last Modified: Tue, 04 Feb 2025 05:04:17 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:901c6cdf7b9d9fdc66c2e7dd015ffab8a6081181f9664809445a60c1c38f57cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51604819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9418e89975585854f86de94d18855e65e9e330eb60bb7f870487523b913eb6`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
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
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0543364fb9178760678fa313c25e29a93474ec565b26a98f7d221f081cfa6a9c`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 17.8 MB (17807283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4f54cfc888447a00950a8bed260bf83c0756e22074ac6e517d7545b44f061f`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64e4d38d8a9c3397670d282869aa68fbfdb19555a3fd1d34f7ae25f68fdb868`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 4.6 MB (4606722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:6d2c12ab302908181af339e8eb030381601052e9aa017c7f804873ff65920a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab4cc8392cf9691f665c1370a68c7c145ff1fad836c7a24e37e8d41b5ab26a9`

```dockerfile
```

-	Layers:
	-	`sha256:965d9da101532415d68a74753d9924a1e85cf63a2e8f60e7b6b137f37ff1a692`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 5.4 MB (5374522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09777d51eae80232a9001b5c2558d0d5e289cf425ee47ff2b7db36cda95c4bbe`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:d28818c42163119adcad0b1dcc26dd7ee850621c4356cbdcc32052b06b2f44cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49995182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d601077f4b52e3127d33d93c3fd09c9a701af11c206f79265cf5ff8a7e42466a`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
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
	-	`sha256:b08d7e697b04bda8cef97763765ebbbc16790e22945b5ab31d97d448a15c8650`  
		Last Modified: Tue, 14 Jan 2025 01:38:32 GMT  
		Size: 28.5 MB (28486647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28f67779f78f00b80585aca7c46133aac31e7a256cf0b1f9b3e60566fad8eed`  
		Last Modified: Tue, 14 Jan 2025 03:13:01 GMT  
		Size: 17.0 MB (16950218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc98bb01c2f2bf9d8d7512a480781548fb3c35c00f1f8fff06e9e26a41b1cba0`  
		Last Modified: Tue, 14 Jan 2025 03:13:00 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a398bade67980c1a0c2fcfa9e505b9f4821bdd51c3350ac55e34cf3f7e4f2aac`  
		Last Modified: Tue, 14 Jan 2025 03:13:00 GMT  
		Size: 4.6 MB (4554954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:665f345ac934ad25efb96e98503d18f9b95162467b661516823bc4ceeb08085f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:428042208a2bac18955a943d20fa3571bfa1ea754f23553c377de300f9aca094`

```dockerfile
```

-	Layers:
	-	`sha256:338f5611412cfef6ba26d4eac7ff605a2cd384cf876ff5e3d51edce260c45bb2`  
		Last Modified: Tue, 14 Jan 2025 03:13:00 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:db1436694e6c5ad22d0afd0ba2487379f11b7dc537e6501ba566158fe8105fe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55654162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624e127e90e41e644939a244ce8d62bb74a540c288c2c0535b1307f1afc90102`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca063b7f943193c22ab40e7a8e97b0e148f087a20fe6419289c97b7d0ef5e29`  
		Last Modified: Tue, 04 Feb 2025 04:41:05 GMT  
		Size: 18.8 MB (18777294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5c622dc9d0af77577cf31f9d90344b8ab556071dd841eb65a65041dabe9c36`  
		Last Modified: Tue, 04 Feb 2025 04:41:04 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfcc7bc84e38fd9dceea4a35a8d5af6dff5263311cbb4059040c5c8d368ebb6c`  
		Last Modified: Tue, 04 Feb 2025 04:41:05 GMT  
		Size: 4.8 MB (4828728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c21a2202c7b4c4f878928156b12375c7647a7362dda59b47fae6546152e32cef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c600601ba93309811b816a5fbc2cfbd876725e686dca5266591d2ecdc7d63078`

```dockerfile
```

-	Layers:
	-	`sha256:237ae9c8b196f0c7bd7c1c0add9e83abb0b11c4629c88f3329059a541b89f726`  
		Last Modified: Tue, 04 Feb 2025 04:41:05 GMT  
		Size: 5.4 MB (5386137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:967827e2da291c538712da27aa99c36482ec1592d412f1fa4635aa2517dfb2d1`  
		Last Modified: Tue, 04 Feb 2025 04:41:04 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:118557ad5cdd352ec957387289121525cc9c6d7c237dedb0059f51973bba9393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49677205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a90444e62f0a7ecd2943f88d9460a14b97af595211a1ffd5cce125a8a52fad2`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
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
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89da8dc0f15330b25d2b981b51d661f0b4a1a93b4a88830c02b98f46631dcd0e`  
		Last Modified: Tue, 04 Feb 2025 04:50:15 GMT  
		Size: 18.2 MB (18228328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701509cd8027b019559956e107cce23e31704234e0261871b6ecae13613de4d2`  
		Last Modified: Tue, 04 Feb 2025 04:50:14 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47c46a9d50c61988c85d1cce9566c2df29abc1065542d4a3ae247d7699c4f0e`  
		Last Modified: Tue, 04 Feb 2025 04:50:14 GMT  
		Size: 4.6 MB (4586893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:8463cfba482b17372e31908c83f933c9f580c2bce5f2a8dd85834a35b925d5eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc57343be8f1aa8eb99773aa94db903bb11309cca10478dc61d9f772f975e48`

```dockerfile
```

-	Layers:
	-	`sha256:02b334568b4b4bf4bbc2080ac7d38143a78ca5cc83de2f55aa27bfb79d053bff`  
		Last Modified: Tue, 04 Feb 2025 04:50:14 GMT  
		Size: 5.4 MB (5377637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03285e941ada1088ba347bf3577bda3f4315e3964da59a1e4a022b260138852b`  
		Last Modified: Tue, 04 Feb 2025 04:50:14 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine`

```console
$ docker pull irssi@sha256:f1cdedacf033ae45b37671d63aefae07033b2a0fa3507085aa0a16255adb1d73
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
$ docker pull irssi@sha256:4193e61a40c9328c1b94ce51e9031ba03dcd3181e5d39b0c9351593d9d3df809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19987543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4186d7ecf686de55a532210964caea9788cd858e2e57e629cc98bfce33904c`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4504f7d1d5480733759d05ffb799048947251956dc083fb64f2c6180fd71bbe6`  
		Last Modified: Wed, 08 Jan 2025 18:00:08 GMT  
		Size: 10.4 MB (10401239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f16860e1b787f03fd5b37bb710d5b50605e28da9b2c3348cfd157d768c820d8`  
		Last Modified: Wed, 08 Jan 2025 18:00:07 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5436031ccb3a5ef03c713d64220269098f86f750cacef5fe3d656838ada41134`  
		Last Modified: Wed, 08 Jan 2025 18:00:08 GMT  
		Size: 5.9 MB (5943594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:ed0fd16fa5dfc1ebb8e540279c3d56f06461c47c0b4eaa56f7213d59f3b8e5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa28e6ca713aae5e0760abe87a8c1701e24b4315e06305f8e06361ee6822f5b`

```dockerfile
```

-	Layers:
	-	`sha256:94fc1e0bcc3ff5ed5a5b810abeb8277b9ec7f0b855de0306d071b5c9da2d7f02`  
		Last Modified: Wed, 08 Jan 2025 18:00:08 GMT  
		Size: 1.3 MB (1268412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:916523bbffc94549b1ff2ea0578c76d54649b18cfd72b2568821dd66668f3dad`  
		Last Modified: Wed, 08 Jan 2025 18:00:07 GMT  
		Size: 17.5 KB (17542 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:2c444becc8f59a3051899f1b7b18e61f5ac1976b48abb242ac94743d6786a431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18765986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a046672ba023e89b9eb473b361bd77e1c1014a2533ea78f24fc82d3369cba24`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd9ce7987b867c5af93522ef0a0dca7f861cb1456c6eb767e86ce82fe63cce7`  
		Last Modified: Wed, 08 Jan 2025 18:43:20 GMT  
		Size: 9.6 MB (9623095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d674e7a159f0f639e7a5021bff9aa181d8cae6336d7ff23bbd66596842a959b3`  
		Last Modified: Wed, 08 Jan 2025 18:43:20 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142129b2b5659fa1422811fe59177a83490781fb5b4a86d8275c5bd9b7ab4f21`  
		Last Modified: Wed, 08 Jan 2025 18:43:20 GMT  
		Size: 5.8 MB (5778018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:6d6fece555bab7727c0c848ecfb996f863aa6813c9814ce2fa861e93e8b01b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:069a3134f379df2190cd7556f65b5847c3f1951876aa1888e978eed8d260eb18`

```dockerfile
```

-	Layers:
	-	`sha256:d5fb6e0a557bb302e68efc005e3a5ecb0446078bb337c0a0c4f057ae96221bf8`  
		Last Modified: Wed, 08 Jan 2025 18:43:20 GMT  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:17e89e906bd000045a476506e7e9f7dd5d9035c70cc48090cad4010281aa7532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18087011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2dde65e0d23b2f156349a8a42d6c3bc1f5051b08494987065eb4a248ba5fc37`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a09db915c011952a96d8c7ca2b871e8fe1825206fe7759a30ab888cc91bb92`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 9.4 MB (9448825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acde75a6180a2de97da5d1ce62f0a9c5c4cc0b1bd19a6fcc2902647b1d54477b`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfc084ccf7459c766e83460c6a97fca525bc73643aa2723bae27ceb01142a7b`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 5.5 MB (5540079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:43913a2144b298d81f3267cf9a6f55f0c7e045815fac0a2b89f83005f1b97711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e2e5e1e7ba6c2ff85b85c46dd0ecaa5cba30daaa969a436d84eb64419d7c83`

```dockerfile
```

-	Layers:
	-	`sha256:4b8a927505163cf9f81c70e70e7c0ad65876827c5facba8fa6c05b0e2bc84b77`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 1.3 MB (1271293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b93f06e549d3f10c217b728a96ba8a80c217724b1d06f9ec3363b151fe34376`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:6e9881525ef20752b9832c3149eb0774888ae031e0c43131c707f2f21cee9eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20175650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef2f09837c399298898d414af25542ad0956de47c8d2d6894701b5865ecaa874`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df099fddd890ebfe7f630edd22f1ba8a8c64e9a9e9ded3e7624da394b887eaea`  
		Last Modified: Wed, 08 Jan 2025 18:40:12 GMT  
		Size: 10.4 MB (10360970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d169feda846a3364940c249513e4fa35fecd78cbed0ca18935dae6b0dc2066be`  
		Last Modified: Wed, 08 Jan 2025 18:40:11 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea10c87b59dafc64feccc55905a62f7d7bf66a87c13d5a061155457b6eadfc24`  
		Last Modified: Wed, 08 Jan 2025 18:40:12 GMT  
		Size: 5.8 MB (5821325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:dc724abcb64978abb5f013ad3a6632bcc41723d5b8d12a2223b8c2bd882b4f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d63fbf85996e7700610efcd716ce493e55a5867cc779533976748e6a4d60d8`

```dockerfile
```

-	Layers:
	-	`sha256:9a2585646a2f2f594aa08ff0feed38cb4df2b7371ebddd3d25f9946040742c76`  
		Last Modified: Wed, 08 Jan 2025 18:40:11 GMT  
		Size: 1.3 MB (1268516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33a53d9019370f622feed69cdf3f4b775b86e3874d014caf34d0fa72310bfb1f`  
		Last Modified: Wed, 08 Jan 2025 18:40:11 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; 386

```console
$ docker pull irssi@sha256:66bdc2d923e986725903011611db090dab933811ba58bb9a4f7449b4345e3ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19451510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9c1a6434c24f1223cf7d759e2f2f0d4ed74b6b0f5c6dc83e9921aab3bd3b0d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e695bb54ed6dd62b384f4243e489a53cfa6bf81159ac8a2d5331fa54f9bb5b93`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 10.0 MB (9955036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bff2a0e42946a090bf9cd1a1ade056259fa04da87b496116efb91a05538994`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17796159e6bf6eb0fbbd1eb96ab993de0fad5f98892f1e645d429f47333c576d`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 6.0 MB (6032353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:da09e3dde96fca610afc57dd87913c5c26769281b2e38d7990e66f7e0eb5c88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d9d648950f50f00f0452683fc547bb3a513bed5b9a83f07b7a67a7ab7c8124`

```dockerfile
```

-	Layers:
	-	`sha256:29e4298aceb4adb527f2fd00a54634db1d6c562ead9fb9576ae2c06fcff73a88`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 1.3 MB (1268367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6efc04ea8f8ec2cf101dfe86667d9e9e33a4e3623cb32cd0486036d93fc2bf47`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:77b18e9b102c70aca2fd173d672a6387d5d4e7b8d9fb2838aefe6462856daf9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20370271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714e229372660ec3a04811680ccf779431ccd182ebb90b090ddd62a4095f94bc`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3dade292c0d99d49bd8bccb4f5301fa9e6416d2ff0cab1ed87da5930f97288`  
		Last Modified: Thu, 09 Jan 2025 01:04:03 GMT  
		Size: 10.6 MB (10589990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d39712a74a770b38e3014eee3a7239d780aef10c9c024898ff964ca34f8fe3`  
		Last Modified: Thu, 09 Jan 2025 01:04:02 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bff666ec900fd764acb66933a40ed991d1ac6f8f7174503cd405e4e4b1f944`  
		Last Modified: Thu, 09 Jan 2025 01:04:03 GMT  
		Size: 6.2 MB (6205685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:1d2e5fa0de35ec1a259eb7308f3ec149d06faeda79f3fa42040fe690c244af16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6bae0bb93a6e119362f8cd6a7c5929a0c97666b020728ca1e82eebda1facdfe`

```dockerfile
```

-	Layers:
	-	`sha256:df0e9f5c297036747026956cad41a6c76e04e34e9fd890a313e013a1811aad63`  
		Last Modified: Thu, 09 Jan 2025 01:04:02 GMT  
		Size: 1.3 MB (1266519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fede1e415e2cff757a4c91851125029ac6bd4aaf5dcab8dc8adaf1b7bfcbfe21`  
		Last Modified: Thu, 09 Jan 2025 01:04:02 GMT  
		Size: 17.6 KB (17614 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:b4f5c740627fb94a821a9dbf08157f8eacc8f5a3aed7553ba47db1d9499c8f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19154010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3777b973a4d24c8082c913587f0399482c732316803c9e6a292f1961cc40d4c7`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd7ec6e781516c496daae1d6401e6540db7529619d89bbd48ce9cf60c0195e1`  
		Last Modified: Wed, 08 Jan 2025 21:22:30 GMT  
		Size: 9.8 MB (9845278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11088be527f2981fb0b5303fbc64e717db2f0647ca5771c159a30a0909c3e623`  
		Last Modified: Wed, 08 Jan 2025 21:22:28 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cfd13ced3df5fde280cc947ff2d63a6942e46ddc9f37e3475cdc61fd0bc6eb`  
		Last Modified: Wed, 08 Jan 2025 21:22:29 GMT  
		Size: 6.0 MB (5957479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:dcedd9fb51d467f4e3eaea6a0d5571c92e71eadded71c976c2221716768d9f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155919124ec5ecc222daef344381c74dce8e92e12fa1374f63ff93f93b299fba`

```dockerfile
```

-	Layers:
	-	`sha256:dafb523c6256c24d8d65125905c555948e373014d598c71c17ec2f3ccac4a89e`  
		Last Modified: Wed, 08 Jan 2025 21:22:28 GMT  
		Size: 1.3 MB (1266515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bebeba2510bf5a835d265f324e66347bd510f3ea5193d47ba886310e45981376`  
		Last Modified: Wed, 08 Jan 2025 21:22:28 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; s390x

```console
$ docker pull irssi@sha256:eaca14a1db62c3011646ff5b9a0c126ffdf822d6247ca522dea4296981ff76cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20534645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9620684b7e00cbb2560ff59e10b70d42408d78441905c69e0288ca1a7ad2c120`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bc6ed4a265dfbf7241885f2a24ffd881c938d097a20d3ca7d370aa99474561`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 11.0 MB (10967495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d80f56cffc7118476df73396dc7a6e7919b6c45194ba9483ae6e18dff40a38`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c276b72ae3cd0f4f7b7e0b065f065ffb7fc942aef396f68d729eb51f65d74a`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 6.1 MB (6099288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:5f079783853eb1a971d632f0d85a17e4a1a409a1beef81c2d97faea7c670ab7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c09fbadb09c6c97be762da3c9f62a50392ab031fb8395ab730af3cdd052192b`

```dockerfile
```

-	Layers:
	-	`sha256:2d6b96935b072f35f8b3b648e02079dfa529258931ef5325a8b3a890be3bce17`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 1.3 MB (1266461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36c38183b124c53300e18138d172e1f82b2131f348c608ee58bf35e0bb207d00`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine3.21`

```console
$ docker pull irssi@sha256:f1cdedacf033ae45b37671d63aefae07033b2a0fa3507085aa0a16255adb1d73
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
$ docker pull irssi@sha256:4193e61a40c9328c1b94ce51e9031ba03dcd3181e5d39b0c9351593d9d3df809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19987543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4186d7ecf686de55a532210964caea9788cd858e2e57e629cc98bfce33904c`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4504f7d1d5480733759d05ffb799048947251956dc083fb64f2c6180fd71bbe6`  
		Last Modified: Wed, 08 Jan 2025 18:00:08 GMT  
		Size: 10.4 MB (10401239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f16860e1b787f03fd5b37bb710d5b50605e28da9b2c3348cfd157d768c820d8`  
		Last Modified: Wed, 08 Jan 2025 18:00:07 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5436031ccb3a5ef03c713d64220269098f86f750cacef5fe3d656838ada41134`  
		Last Modified: Wed, 08 Jan 2025 18:00:08 GMT  
		Size: 5.9 MB (5943594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:ed0fd16fa5dfc1ebb8e540279c3d56f06461c47c0b4eaa56f7213d59f3b8e5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa28e6ca713aae5e0760abe87a8c1701e24b4315e06305f8e06361ee6822f5b`

```dockerfile
```

-	Layers:
	-	`sha256:94fc1e0bcc3ff5ed5a5b810abeb8277b9ec7f0b855de0306d071b5c9da2d7f02`  
		Last Modified: Wed, 08 Jan 2025 18:00:08 GMT  
		Size: 1.3 MB (1268412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:916523bbffc94549b1ff2ea0578c76d54649b18cfd72b2568821dd66668f3dad`  
		Last Modified: Wed, 08 Jan 2025 18:00:07 GMT  
		Size: 17.5 KB (17542 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; arm variant v6

```console
$ docker pull irssi@sha256:2c444becc8f59a3051899f1b7b18e61f5ac1976b48abb242ac94743d6786a431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18765986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a046672ba023e89b9eb473b361bd77e1c1014a2533ea78f24fc82d3369cba24`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd9ce7987b867c5af93522ef0a0dca7f861cb1456c6eb767e86ce82fe63cce7`  
		Last Modified: Wed, 08 Jan 2025 18:43:20 GMT  
		Size: 9.6 MB (9623095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d674e7a159f0f639e7a5021bff9aa181d8cae6336d7ff23bbd66596842a959b3`  
		Last Modified: Wed, 08 Jan 2025 18:43:20 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142129b2b5659fa1422811fe59177a83490781fb5b4a86d8275c5bd9b7ab4f21`  
		Last Modified: Wed, 08 Jan 2025 18:43:20 GMT  
		Size: 5.8 MB (5778018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:6d6fece555bab7727c0c848ecfb996f863aa6813c9814ce2fa861e93e8b01b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:069a3134f379df2190cd7556f65b5847c3f1951876aa1888e978eed8d260eb18`

```dockerfile
```

-	Layers:
	-	`sha256:d5fb6e0a557bb302e68efc005e3a5ecb0446078bb337c0a0c4f057ae96221bf8`  
		Last Modified: Wed, 08 Jan 2025 18:43:20 GMT  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; arm variant v7

```console
$ docker pull irssi@sha256:17e89e906bd000045a476506e7e9f7dd5d9035c70cc48090cad4010281aa7532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18087011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2dde65e0d23b2f156349a8a42d6c3bc1f5051b08494987065eb4a248ba5fc37`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a09db915c011952a96d8c7ca2b871e8fe1825206fe7759a30ab888cc91bb92`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 9.4 MB (9448825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acde75a6180a2de97da5d1ce62f0a9c5c4cc0b1bd19a6fcc2902647b1d54477b`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfc084ccf7459c766e83460c6a97fca525bc73643aa2723bae27ceb01142a7b`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 5.5 MB (5540079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:43913a2144b298d81f3267cf9a6f55f0c7e045815fac0a2b89f83005f1b97711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e2e5e1e7ba6c2ff85b85c46dd0ecaa5cba30daaa969a436d84eb64419d7c83`

```dockerfile
```

-	Layers:
	-	`sha256:4b8a927505163cf9f81c70e70e7c0ad65876827c5facba8fa6c05b0e2bc84b77`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 1.3 MB (1271293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b93f06e549d3f10c217b728a96ba8a80c217724b1d06f9ec3363b151fe34376`  
		Last Modified: Wed, 08 Jan 2025 18:44:41 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:6e9881525ef20752b9832c3149eb0774888ae031e0c43131c707f2f21cee9eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20175650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef2f09837c399298898d414af25542ad0956de47c8d2d6894701b5865ecaa874`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df099fddd890ebfe7f630edd22f1ba8a8c64e9a9e9ded3e7624da394b887eaea`  
		Last Modified: Wed, 08 Jan 2025 18:40:12 GMT  
		Size: 10.4 MB (10360970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d169feda846a3364940c249513e4fa35fecd78cbed0ca18935dae6b0dc2066be`  
		Last Modified: Wed, 08 Jan 2025 18:40:11 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea10c87b59dafc64feccc55905a62f7d7bf66a87c13d5a061155457b6eadfc24`  
		Last Modified: Wed, 08 Jan 2025 18:40:12 GMT  
		Size: 5.8 MB (5821325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:dc724abcb64978abb5f013ad3a6632bcc41723d5b8d12a2223b8c2bd882b4f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d63fbf85996e7700610efcd716ce493e55a5867cc779533976748e6a4d60d8`

```dockerfile
```

-	Layers:
	-	`sha256:9a2585646a2f2f594aa08ff0feed38cb4df2b7371ebddd3d25f9946040742c76`  
		Last Modified: Wed, 08 Jan 2025 18:40:11 GMT  
		Size: 1.3 MB (1268516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33a53d9019370f622feed69cdf3f4b775b86e3874d014caf34d0fa72310bfb1f`  
		Last Modified: Wed, 08 Jan 2025 18:40:11 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; 386

```console
$ docker pull irssi@sha256:66bdc2d923e986725903011611db090dab933811ba58bb9a4f7449b4345e3ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19451510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9c1a6434c24f1223cf7d759e2f2f0d4ed74b6b0f5c6dc83e9921aab3bd3b0d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e695bb54ed6dd62b384f4243e489a53cfa6bf81159ac8a2d5331fa54f9bb5b93`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 10.0 MB (9955036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bff2a0e42946a090bf9cd1a1ade056259fa04da87b496116efb91a05538994`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17796159e6bf6eb0fbbd1eb96ab993de0fad5f98892f1e645d429f47333c576d`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 6.0 MB (6032353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:da09e3dde96fca610afc57dd87913c5c26769281b2e38d7990e66f7e0eb5c88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d9d648950f50f00f0452683fc547bb3a513bed5b9a83f07b7a67a7ab7c8124`

```dockerfile
```

-	Layers:
	-	`sha256:29e4298aceb4adb527f2fd00a54634db1d6c562ead9fb9576ae2c06fcff73a88`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 1.3 MB (1268367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6efc04ea8f8ec2cf101dfe86667d9e9e33a4e3623cb32cd0486036d93fc2bf47`  
		Last Modified: Wed, 08 Jan 2025 17:59:53 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; ppc64le

```console
$ docker pull irssi@sha256:77b18e9b102c70aca2fd173d672a6387d5d4e7b8d9fb2838aefe6462856daf9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20370271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714e229372660ec3a04811680ccf779431ccd182ebb90b090ddd62a4095f94bc`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3dade292c0d99d49bd8bccb4f5301fa9e6416d2ff0cab1ed87da5930f97288`  
		Last Modified: Thu, 09 Jan 2025 01:04:03 GMT  
		Size: 10.6 MB (10589990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d39712a74a770b38e3014eee3a7239d780aef10c9c024898ff964ca34f8fe3`  
		Last Modified: Thu, 09 Jan 2025 01:04:02 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bff666ec900fd764acb66933a40ed991d1ac6f8f7174503cd405e4e4b1f944`  
		Last Modified: Thu, 09 Jan 2025 01:04:03 GMT  
		Size: 6.2 MB (6205685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:1d2e5fa0de35ec1a259eb7308f3ec149d06faeda79f3fa42040fe690c244af16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6bae0bb93a6e119362f8cd6a7c5929a0c97666b020728ca1e82eebda1facdfe`

```dockerfile
```

-	Layers:
	-	`sha256:df0e9f5c297036747026956cad41a6c76e04e34e9fd890a313e013a1811aad63`  
		Last Modified: Thu, 09 Jan 2025 01:04:02 GMT  
		Size: 1.3 MB (1266519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fede1e415e2cff757a4c91851125029ac6bd4aaf5dcab8dc8adaf1b7bfcbfe21`  
		Last Modified: Thu, 09 Jan 2025 01:04:02 GMT  
		Size: 17.6 KB (17614 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; riscv64

```console
$ docker pull irssi@sha256:b4f5c740627fb94a821a9dbf08157f8eacc8f5a3aed7553ba47db1d9499c8f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19154010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3777b973a4d24c8082c913587f0399482c732316803c9e6a292f1961cc40d4c7`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd7ec6e781516c496daae1d6401e6540db7529619d89bbd48ce9cf60c0195e1`  
		Last Modified: Wed, 08 Jan 2025 21:22:30 GMT  
		Size: 9.8 MB (9845278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11088be527f2981fb0b5303fbc64e717db2f0647ca5771c159a30a0909c3e623`  
		Last Modified: Wed, 08 Jan 2025 21:22:28 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cfd13ced3df5fde280cc947ff2d63a6942e46ddc9f37e3475cdc61fd0bc6eb`  
		Last Modified: Wed, 08 Jan 2025 21:22:29 GMT  
		Size: 6.0 MB (5957479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:dcedd9fb51d467f4e3eaea6a0d5571c92e71eadded71c976c2221716768d9f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155919124ec5ecc222daef344381c74dce8e92e12fa1374f63ff93f93b299fba`

```dockerfile
```

-	Layers:
	-	`sha256:dafb523c6256c24d8d65125905c555948e373014d598c71c17ec2f3ccac4a89e`  
		Last Modified: Wed, 08 Jan 2025 21:22:28 GMT  
		Size: 1.3 MB (1266515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bebeba2510bf5a835d265f324e66347bd510f3ea5193d47ba886310e45981376`  
		Last Modified: Wed, 08 Jan 2025 21:22:28 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; s390x

```console
$ docker pull irssi@sha256:eaca14a1db62c3011646ff5b9a0c126ffdf822d6247ca522dea4296981ff76cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20534645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9620684b7e00cbb2560ff59e10b70d42408d78441905c69e0288ca1a7ad2c120`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:52:22 GMT
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
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bc6ed4a265dfbf7241885f2a24ffd881c938d097a20d3ca7d370aa99474561`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 11.0 MB (10967495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d80f56cffc7118476df73396dc7a6e7919b6c45194ba9483ae6e18dff40a38`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c276b72ae3cd0f4f7b7e0b065f065ffb7fc942aef396f68d729eb51f65d74a`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 6.1 MB (6099288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:5f079783853eb1a971d632f0d85a17e4a1a409a1beef81c2d97faea7c670ab7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c09fbadb09c6c97be762da3c9f62a50392ab031fb8395ab730af3cdd052192b`

```dockerfile
```

-	Layers:
	-	`sha256:2d6b96935b072f35f8b3b648e02079dfa529258931ef5325a8b3a890be3bce17`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 1.3 MB (1266461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36c38183b124c53300e18138d172e1f82b2131f348c608ee58bf35e0bb207d00`  
		Last Modified: Wed, 08 Jan 2025 18:26:51 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:bookworm`

```console
$ docker pull irssi@sha256:b8d2cd8a4049dbd6a5e516a27fad3786893254901b0cbe96cf7b8886bf7c4942
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
$ docker pull irssi@sha256:03912cf04635b54b85fd210ee261a305fcd0b75d5094bce04c064eb81e05b367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51077295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ccc0d8fbc3c33f0820f01b1a454060587f8daa35c9df96d6c833fa6328086c`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d511daa4d1415f6ad1cb79745c81943a9f61f01896306f729191b612aa6da385`  
		Last Modified: Tue, 04 Feb 2025 04:22:43 GMT  
		Size: 18.3 MB (18268701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7da886d618548bbc8edd2f3505b119ff05b10ea29bfa77dec0d0db9005fcc6`  
		Last Modified: Tue, 04 Feb 2025 04:22:43 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93083499d680e9cddc0233998007046abd698e15757c31742eb433dff3a5011`  
		Last Modified: Tue, 04 Feb 2025 04:22:43 GMT  
		Size: 4.6 MB (4592934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:174243e31561a4202e6b08708e99fa9dae865a38dbddb9b0869032f782eeacae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6c362f77e9fa8569a125ec3242f05088c7129ef65f5475015dab41cec25abd`

```dockerfile
```

-	Layers:
	-	`sha256:9395cad4b9b7e2104529e3e860a2500276bb55ae3eebb114000689df0dd0e91b`  
		Last Modified: Tue, 04 Feb 2025 04:22:43 GMT  
		Size: 5.4 MB (5378443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a50dddc4319682a8ba3c43b88ee87250da64d004b77224eba699f4d40ce7d359`  
		Last Modified: Tue, 04 Feb 2025 04:22:42 GMT  
		Size: 18.7 KB (18715 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:dd944eacc299fca9043f3a00584234312850041958c75a0a6d12352765957d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47224246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912ff2cc1544806cafd6236219b0efb454d1e9c7acb0a12ddb4031ba709c1652`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
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
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1258e5d59e85019768cf23e6152f950437776cfa96a36330f19be08d5e5ba1`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 17.0 MB (17039747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85eefa10fde4b95b381c673baaa58bc7a769df56f26012a5eab676834fb8b23`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa075f5f9593a4a003f660804bb8ade9b6b2da4f6dd19460fa34dde1e3fb656`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 4.4 MB (4444590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c84f8f903292b8d9782d59a46d6a0b289f5a71bc089bde0dfa5e04a2e07f4332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f3e72502240ef6d69ad6368e81442928a515ea384405d55a4fefe0aef6904d0`

```dockerfile
```

-	Layers:
	-	`sha256:c0b21ea472520d859ac86769bdf0c5cf41720c142217ed9228036522e82e8a37`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 5.4 MB (5380052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d64f287313b7a31f8ae5875a679eb78d8b7b763891544779f5fcaecdc43322cc`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 18.8 KB (18849 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:ba7c89a907137df9fc57af330fcb8d4634bb3ddde13c463b28a3aeb7959925cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44851709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66388d5089eadb184158f401a4f8b5b389ba7aae6c565e710d389eb6665ac2ec`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
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
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932cf98d70207b070896ceab0de9e238d520df78d567a209aec71355a30916aa`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 16.6 MB (16634724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84820068b052b7cae2187bf56b2d33211c396539ee172714f142dd2f0b9c948d`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898ec6f2b57f7fd8b176a35fa5a1334504aa332e8affe55eeb9ff25d73621cf8`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 4.3 MB (4299093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:8c38fbd99e47af292068fa29397214c2b4534bbe7598f0c06c61be30213c4f9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b975de2e8d2c83833261c1e8c3e8cacea19547242f5e577f3cd43b12cd99e009`

```dockerfile
```

-	Layers:
	-	`sha256:6e72488613f8e15e5a42b6366f3525135910f79b1e1c7a0f373b376dd5a0b207`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 5.4 MB (5379801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c25e19b3808062c3d6d7031500eca2c4f5f19abb6b96ec225d3a428f06dbeb9`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:0bff7107c5be3fa8a25980ae315db1b9da57e49cc94334465a6e1c07abbcddc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50606136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3c20928b6ab78915d2427093df0e4985772217b37dc3034a5b4ef3dfd8184b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5ac57f9db7aba2c602974068cfd0990b4a237e2084ee4464dca4528f2f88a2`  
		Last Modified: Tue, 04 Feb 2025 05:04:18 GMT  
		Size: 18.0 MB (18048813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768cb18511de259fecfb8830cdd7b4b39cefffd5c24fd03a2a7484a7e39e410a`  
		Last Modified: Tue, 04 Feb 2025 05:04:17 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41d11b3d9e0b41e7923110a53e52bd3c8ebc03797cd43d93d04519eea4bcf3b`  
		Last Modified: Tue, 04 Feb 2025 05:04:18 GMT  
		Size: 4.5 MB (4513086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:f3402365e17e758646f38363037821b30d5cec7a2039ca536bf0577c564273bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5403817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606d87a50640b89f893f51a5ff46677d0fd16006c373e63ac4c9ff52133a2e99`

```dockerfile
```

-	Layers:
	-	`sha256:6a18f84d3ff9162ef107a22bf2419d0e91df8f95be917a59b94c3d7405a865ad`  
		Last Modified: Tue, 04 Feb 2025 05:04:18 GMT  
		Size: 5.4 MB (5384919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97e11e03e9217e9050435b22329e4fe651256e1b9db095df49cf2d714e57ee20`  
		Last Modified: Tue, 04 Feb 2025 05:04:17 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; 386

```console
$ docker pull irssi@sha256:901c6cdf7b9d9fdc66c2e7dd015ffab8a6081181f9664809445a60c1c38f57cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51604819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9418e89975585854f86de94d18855e65e9e330eb60bb7f870487523b913eb6`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
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
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0543364fb9178760678fa313c25e29a93474ec565b26a98f7d221f081cfa6a9c`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 17.8 MB (17807283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4f54cfc888447a00950a8bed260bf83c0756e22074ac6e517d7545b44f061f`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64e4d38d8a9c3397670d282869aa68fbfdb19555a3fd1d34f7ae25f68fdb868`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 4.6 MB (4606722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:6d2c12ab302908181af339e8eb030381601052e9aa017c7f804873ff65920a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab4cc8392cf9691f665c1370a68c7c145ff1fad836c7a24e37e8d41b5ab26a9`

```dockerfile
```

-	Layers:
	-	`sha256:965d9da101532415d68a74753d9924a1e85cf63a2e8f60e7b6b137f37ff1a692`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 5.4 MB (5374522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09777d51eae80232a9001b5c2558d0d5e289cf425ee47ff2b7db36cda95c4bbe`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:d28818c42163119adcad0b1dcc26dd7ee850621c4356cbdcc32052b06b2f44cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49995182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d601077f4b52e3127d33d93c3fd09c9a701af11c206f79265cf5ff8a7e42466a`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
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
	-	`sha256:b08d7e697b04bda8cef97763765ebbbc16790e22945b5ab31d97d448a15c8650`  
		Last Modified: Tue, 14 Jan 2025 01:38:32 GMT  
		Size: 28.5 MB (28486647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28f67779f78f00b80585aca7c46133aac31e7a256cf0b1f9b3e60566fad8eed`  
		Last Modified: Tue, 14 Jan 2025 03:13:01 GMT  
		Size: 17.0 MB (16950218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc98bb01c2f2bf9d8d7512a480781548fb3c35c00f1f8fff06e9e26a41b1cba0`  
		Last Modified: Tue, 14 Jan 2025 03:13:00 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a398bade67980c1a0c2fcfa9e505b9f4821bdd51c3350ac55e34cf3f7e4f2aac`  
		Last Modified: Tue, 14 Jan 2025 03:13:00 GMT  
		Size: 4.6 MB (4554954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:665f345ac934ad25efb96e98503d18f9b95162467b661516823bc4ceeb08085f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:428042208a2bac18955a943d20fa3571bfa1ea754f23553c377de300f9aca094`

```dockerfile
```

-	Layers:
	-	`sha256:338f5611412cfef6ba26d4eac7ff605a2cd384cf876ff5e3d51edce260c45bb2`  
		Last Modified: Tue, 14 Jan 2025 03:13:00 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:db1436694e6c5ad22d0afd0ba2487379f11b7dc537e6501ba566158fe8105fe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55654162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624e127e90e41e644939a244ce8d62bb74a540c288c2c0535b1307f1afc90102`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca063b7f943193c22ab40e7a8e97b0e148f087a20fe6419289c97b7d0ef5e29`  
		Last Modified: Tue, 04 Feb 2025 04:41:05 GMT  
		Size: 18.8 MB (18777294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5c622dc9d0af77577cf31f9d90344b8ab556071dd841eb65a65041dabe9c36`  
		Last Modified: Tue, 04 Feb 2025 04:41:04 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfcc7bc84e38fd9dceea4a35a8d5af6dff5263311cbb4059040c5c8d368ebb6c`  
		Last Modified: Tue, 04 Feb 2025 04:41:05 GMT  
		Size: 4.8 MB (4828728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c21a2202c7b4c4f878928156b12375c7647a7362dda59b47fae6546152e32cef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c600601ba93309811b816a5fbc2cfbd876725e686dca5266591d2ecdc7d63078`

```dockerfile
```

-	Layers:
	-	`sha256:237ae9c8b196f0c7bd7c1c0add9e83abb0b11c4629c88f3329059a541b89f726`  
		Last Modified: Tue, 04 Feb 2025 04:41:05 GMT  
		Size: 5.4 MB (5386137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:967827e2da291c538712da27aa99c36482ec1592d412f1fa4635aa2517dfb2d1`  
		Last Modified: Tue, 04 Feb 2025 04:41:04 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:118557ad5cdd352ec957387289121525cc9c6d7c237dedb0059f51973bba9393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49677205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a90444e62f0a7ecd2943f88d9460a14b97af595211a1ffd5cce125a8a52fad2`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
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
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89da8dc0f15330b25d2b981b51d661f0b4a1a93b4a88830c02b98f46631dcd0e`  
		Last Modified: Tue, 04 Feb 2025 04:50:15 GMT  
		Size: 18.2 MB (18228328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701509cd8027b019559956e107cce23e31704234e0261871b6ecae13613de4d2`  
		Last Modified: Tue, 04 Feb 2025 04:50:14 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47c46a9d50c61988c85d1cce9566c2df29abc1065542d4a3ae247d7699c4f0e`  
		Last Modified: Tue, 04 Feb 2025 04:50:14 GMT  
		Size: 4.6 MB (4586893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:8463cfba482b17372e31908c83f933c9f580c2bce5f2a8dd85834a35b925d5eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc57343be8f1aa8eb99773aa94db903bb11309cca10478dc61d9f772f975e48`

```dockerfile
```

-	Layers:
	-	`sha256:02b334568b4b4bf4bbc2080ac7d38143a78ca5cc83de2f55aa27bfb79d053bff`  
		Last Modified: Tue, 04 Feb 2025 04:50:14 GMT  
		Size: 5.4 MB (5377637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03285e941ada1088ba347bf3577bda3f4315e3964da59a1e4a022b260138852b`  
		Last Modified: Tue, 04 Feb 2025 04:50:14 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:latest`

```console
$ docker pull irssi@sha256:b8d2cd8a4049dbd6a5e516a27fad3786893254901b0cbe96cf7b8886bf7c4942
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
$ docker pull irssi@sha256:03912cf04635b54b85fd210ee261a305fcd0b75d5094bce04c064eb81e05b367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51077295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ccc0d8fbc3c33f0820f01b1a454060587f8daa35c9df96d6c833fa6328086c`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d511daa4d1415f6ad1cb79745c81943a9f61f01896306f729191b612aa6da385`  
		Last Modified: Tue, 04 Feb 2025 04:22:43 GMT  
		Size: 18.3 MB (18268701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7da886d618548bbc8edd2f3505b119ff05b10ea29bfa77dec0d0db9005fcc6`  
		Last Modified: Tue, 04 Feb 2025 04:22:43 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93083499d680e9cddc0233998007046abd698e15757c31742eb433dff3a5011`  
		Last Modified: Tue, 04 Feb 2025 04:22:43 GMT  
		Size: 4.6 MB (4592934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:174243e31561a4202e6b08708e99fa9dae865a38dbddb9b0869032f782eeacae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6c362f77e9fa8569a125ec3242f05088c7129ef65f5475015dab41cec25abd`

```dockerfile
```

-	Layers:
	-	`sha256:9395cad4b9b7e2104529e3e860a2500276bb55ae3eebb114000689df0dd0e91b`  
		Last Modified: Tue, 04 Feb 2025 04:22:43 GMT  
		Size: 5.4 MB (5378443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a50dddc4319682a8ba3c43b88ee87250da64d004b77224eba699f4d40ce7d359`  
		Last Modified: Tue, 04 Feb 2025 04:22:42 GMT  
		Size: 18.7 KB (18715 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v5

```console
$ docker pull irssi@sha256:dd944eacc299fca9043f3a00584234312850041958c75a0a6d12352765957d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47224246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912ff2cc1544806cafd6236219b0efb454d1e9c7acb0a12ddb4031ba709c1652`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
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
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1258e5d59e85019768cf23e6152f950437776cfa96a36330f19be08d5e5ba1`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 17.0 MB (17039747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85eefa10fde4b95b381c673baaa58bc7a769df56f26012a5eab676834fb8b23`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa075f5f9593a4a003f660804bb8ade9b6b2da4f6dd19460fa34dde1e3fb656`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 4.4 MB (4444590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:c84f8f903292b8d9782d59a46d6a0b289f5a71bc089bde0dfa5e04a2e07f4332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f3e72502240ef6d69ad6368e81442928a515ea384405d55a4fefe0aef6904d0`

```dockerfile
```

-	Layers:
	-	`sha256:c0b21ea472520d859ac86769bdf0c5cf41720c142217ed9228036522e82e8a37`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 5.4 MB (5380052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d64f287313b7a31f8ae5875a679eb78d8b7b763891544779f5fcaecdc43322cc`  
		Last Modified: Tue, 04 Feb 2025 04:55:10 GMT  
		Size: 18.8 KB (18849 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v7

```console
$ docker pull irssi@sha256:ba7c89a907137df9fc57af330fcb8d4634bb3ddde13c463b28a3aeb7959925cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44851709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66388d5089eadb184158f401a4f8b5b389ba7aae6c565e710d389eb6665ac2ec`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
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
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932cf98d70207b070896ceab0de9e238d520df78d567a209aec71355a30916aa`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 16.6 MB (16634724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84820068b052b7cae2187bf56b2d33211c396539ee172714f142dd2f0b9c948d`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898ec6f2b57f7fd8b176a35fa5a1334504aa332e8affe55eeb9ff25d73621cf8`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 4.3 MB (4299093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:8c38fbd99e47af292068fa29397214c2b4534bbe7598f0c06c61be30213c4f9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b975de2e8d2c83833261c1e8c3e8cacea19547242f5e577f3cd43b12cd99e009`

```dockerfile
```

-	Layers:
	-	`sha256:6e72488613f8e15e5a42b6366f3525135910f79b1e1c7a0f373b376dd5a0b207`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 5.4 MB (5379801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c25e19b3808062c3d6d7031500eca2c4f5f19abb6b96ec225d3a428f06dbeb9`  
		Last Modified: Tue, 04 Feb 2025 04:55:24 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:0bff7107c5be3fa8a25980ae315db1b9da57e49cc94334465a6e1c07abbcddc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50606136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3c20928b6ab78915d2427093df0e4985772217b37dc3034a5b4ef3dfd8184b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5ac57f9db7aba2c602974068cfd0990b4a237e2084ee4464dca4528f2f88a2`  
		Last Modified: Tue, 04 Feb 2025 05:04:18 GMT  
		Size: 18.0 MB (18048813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768cb18511de259fecfb8830cdd7b4b39cefffd5c24fd03a2a7484a7e39e410a`  
		Last Modified: Tue, 04 Feb 2025 05:04:17 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41d11b3d9e0b41e7923110a53e52bd3c8ebc03797cd43d93d04519eea4bcf3b`  
		Last Modified: Tue, 04 Feb 2025 05:04:18 GMT  
		Size: 4.5 MB (4513086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:f3402365e17e758646f38363037821b30d5cec7a2039ca536bf0577c564273bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5403817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606d87a50640b89f893f51a5ff46677d0fd16006c373e63ac4c9ff52133a2e99`

```dockerfile
```

-	Layers:
	-	`sha256:6a18f84d3ff9162ef107a22bf2419d0e91df8f95be917a59b94c3d7405a865ad`  
		Last Modified: Tue, 04 Feb 2025 05:04:18 GMT  
		Size: 5.4 MB (5384919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97e11e03e9217e9050435b22329e4fe651256e1b9db095df49cf2d714e57ee20`  
		Last Modified: Tue, 04 Feb 2025 05:04:17 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; 386

```console
$ docker pull irssi@sha256:901c6cdf7b9d9fdc66c2e7dd015ffab8a6081181f9664809445a60c1c38f57cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51604819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9418e89975585854f86de94d18855e65e9e330eb60bb7f870487523b913eb6`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
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
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0543364fb9178760678fa313c25e29a93474ec565b26a98f7d221f081cfa6a9c`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 17.8 MB (17807283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4f54cfc888447a00950a8bed260bf83c0756e22074ac6e517d7545b44f061f`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64e4d38d8a9c3397670d282869aa68fbfdb19555a3fd1d34f7ae25f68fdb868`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 4.6 MB (4606722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:6d2c12ab302908181af339e8eb030381601052e9aa017c7f804873ff65920a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab4cc8392cf9691f665c1370a68c7c145ff1fad836c7a24e37e8d41b5ab26a9`

```dockerfile
```

-	Layers:
	-	`sha256:965d9da101532415d68a74753d9924a1e85cf63a2e8f60e7b6b137f37ff1a692`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 5.4 MB (5374522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09777d51eae80232a9001b5c2558d0d5e289cf425ee47ff2b7db36cda95c4bbe`  
		Last Modified: Tue, 04 Feb 2025 04:22:50 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; mips64le

```console
$ docker pull irssi@sha256:d28818c42163119adcad0b1dcc26dd7ee850621c4356cbdcc32052b06b2f44cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49995182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d601077f4b52e3127d33d93c3fd09c9a701af11c206f79265cf5ff8a7e42466a`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
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
	-	`sha256:b08d7e697b04bda8cef97763765ebbbc16790e22945b5ab31d97d448a15c8650`  
		Last Modified: Tue, 14 Jan 2025 01:38:32 GMT  
		Size: 28.5 MB (28486647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28f67779f78f00b80585aca7c46133aac31e7a256cf0b1f9b3e60566fad8eed`  
		Last Modified: Tue, 14 Jan 2025 03:13:01 GMT  
		Size: 17.0 MB (16950218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc98bb01c2f2bf9d8d7512a480781548fb3c35c00f1f8fff06e9e26a41b1cba0`  
		Last Modified: Tue, 14 Jan 2025 03:13:00 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a398bade67980c1a0c2fcfa9e505b9f4821bdd51c3350ac55e34cf3f7e4f2aac`  
		Last Modified: Tue, 14 Jan 2025 03:13:00 GMT  
		Size: 4.6 MB (4554954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:665f345ac934ad25efb96e98503d18f9b95162467b661516823bc4ceeb08085f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:428042208a2bac18955a943d20fa3571bfa1ea754f23553c377de300f9aca094`

```dockerfile
```

-	Layers:
	-	`sha256:338f5611412cfef6ba26d4eac7ff605a2cd384cf876ff5e3d51edce260c45bb2`  
		Last Modified: Tue, 14 Jan 2025 03:13:00 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; ppc64le

```console
$ docker pull irssi@sha256:db1436694e6c5ad22d0afd0ba2487379f11b7dc537e6501ba566158fe8105fe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55654162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624e127e90e41e644939a244ce8d62bb74a540c288c2c0535b1307f1afc90102`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca063b7f943193c22ab40e7a8e97b0e148f087a20fe6419289c97b7d0ef5e29`  
		Last Modified: Tue, 04 Feb 2025 04:41:05 GMT  
		Size: 18.8 MB (18777294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5c622dc9d0af77577cf31f9d90344b8ab556071dd841eb65a65041dabe9c36`  
		Last Modified: Tue, 04 Feb 2025 04:41:04 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfcc7bc84e38fd9dceea4a35a8d5af6dff5263311cbb4059040c5c8d368ebb6c`  
		Last Modified: Tue, 04 Feb 2025 04:41:05 GMT  
		Size: 4.8 MB (4828728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:c21a2202c7b4c4f878928156b12375c7647a7362dda59b47fae6546152e32cef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c600601ba93309811b816a5fbc2cfbd876725e686dca5266591d2ecdc7d63078`

```dockerfile
```

-	Layers:
	-	`sha256:237ae9c8b196f0c7bd7c1c0add9e83abb0b11c4629c88f3329059a541b89f726`  
		Last Modified: Tue, 04 Feb 2025 04:41:05 GMT  
		Size: 5.4 MB (5386137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:967827e2da291c538712da27aa99c36482ec1592d412f1fa4635aa2517dfb2d1`  
		Last Modified: Tue, 04 Feb 2025 04:41:04 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; s390x

```console
$ docker pull irssi@sha256:118557ad5cdd352ec957387289121525cc9c6d7c237dedb0059f51973bba9393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49677205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a90444e62f0a7ecd2943f88d9460a14b97af595211a1ffd5cce125a8a52fad2`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
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
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89da8dc0f15330b25d2b981b51d661f0b4a1a93b4a88830c02b98f46631dcd0e`  
		Last Modified: Tue, 04 Feb 2025 04:50:15 GMT  
		Size: 18.2 MB (18228328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701509cd8027b019559956e107cce23e31704234e0261871b6ecae13613de4d2`  
		Last Modified: Tue, 04 Feb 2025 04:50:14 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47c46a9d50c61988c85d1cce9566c2df29abc1065542d4a3ae247d7699c4f0e`  
		Last Modified: Tue, 04 Feb 2025 04:50:14 GMT  
		Size: 4.6 MB (4586893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:8463cfba482b17372e31908c83f933c9f580c2bce5f2a8dd85834a35b925d5eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc57343be8f1aa8eb99773aa94db903bb11309cca10478dc61d9f772f975e48`

```dockerfile
```

-	Layers:
	-	`sha256:02b334568b4b4bf4bbc2080ac7d38143a78ca5cc83de2f55aa27bfb79d053bff`  
		Last Modified: Tue, 04 Feb 2025 04:50:14 GMT  
		Size: 5.4 MB (5377637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03285e941ada1088ba347bf3577bda3f4315e3964da59a1e4a022b260138852b`  
		Last Modified: Tue, 04 Feb 2025 04:50:14 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json
