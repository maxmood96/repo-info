<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `irssi`

-	[`irssi:1`](#irssi1)
-	[`irssi:1-alpine`](#irssi1-alpine)
-	[`irssi:1-alpine3.22`](#irssi1-alpine322)
-	[`irssi:1-trixie`](#irssi1-trixie)
-	[`irssi:1.4`](#irssi14)
-	[`irssi:1.4-alpine`](#irssi14-alpine)
-	[`irssi:1.4-alpine3.22`](#irssi14-alpine322)
-	[`irssi:1.4-trixie`](#irssi14-trixie)
-	[`irssi:1.4.5`](#irssi145)
-	[`irssi:1.4.5-alpine`](#irssi145-alpine)
-	[`irssi:1.4.5-alpine3.22`](#irssi145-alpine322)
-	[`irssi:1.4.5-trixie`](#irssi145-trixie)
-	[`irssi:alpine`](#irssialpine)
-	[`irssi:alpine3.22`](#irssialpine322)
-	[`irssi:latest`](#irssilatest)
-	[`irssi:trixie`](#irssitrixie)

## `irssi:1`

```console
$ docker pull irssi@sha256:5cf9ab8c791c26cf2aa97983f1cc4debbebc4fb203bae59694fc0398575102d2
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
$ docker pull irssi@sha256:f62560d766eab4534167883aef43fa8fad47d829ff5c18467b86628e024bd9c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53870137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769552443b8c0b77660078238cebe5d212969cc1cef60189b3e988284170f129`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
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
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50e33926f10233e1cefedd2afc470ffdca1d03aae27f61804a5308859157ecd`  
		Last Modified: Tue, 21 Oct 2025 01:18:57 GMT  
		Size: 19.2 MB (19222452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5172862d08ce0c808ae6bd8643e68f924682e5145be1e8111d0b52f49a6fe9bc`  
		Last Modified: Tue, 21 Oct 2025 01:18:55 GMT  
		Size: 3.3 KB (3335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160b0c22ddb061ea4cd17f1ed3ca11aec9c1535fa615b47a6577d131dafc4ba3`  
		Last Modified: Tue, 21 Oct 2025 01:18:56 GMT  
		Size: 4.9 MB (4866394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:6eff9cda53aa1fce62b753cb7e75d79fbe1450f9fec0a77f0972a0a5c20df8d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4a3535c6261e33feac4e249dfb231f9d22a1d643b2b4a9b3d8f0a1ed8ff4dc`

```dockerfile
```

-	Layers:
	-	`sha256:984b3275ff964e7bbd701d8b5ca39a1b1abcd3f1bcf095ff7fea54585adab0a5`  
		Last Modified: Tue, 21 Oct 2025 10:59:26 GMT  
		Size: 5.6 MB (5588383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80576291496298d1465daebae79c9c7e21c694e8d2ab8ac5425ebf50e8de2192`  
		Last Modified: Tue, 21 Oct 2025 10:59:27 GMT  
		Size: 18.7 KB (18694 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v5

```console
$ docker pull irssi@sha256:53bc4bdfbee3e6398af8cf776254a80b7ed67e7da2fe11c32d32d7abbe566dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50946604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea2d9d131f13dbc0476fa90cf34ad8697fe5db46e9a4c3807db7c7805165ed1`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 00:24:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:24:18 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 00:24:18 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 00:24:18 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 00:24:18 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 00:25:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 00:25:08 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 00:25:08 GMT
USER user
# Tue, 04 Nov 2025 00:25:08 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:453afc2258d7bc5729fed5672fb95bafa092e30a933b4377a12034be940a671b`  
		Last Modified: Tue, 04 Nov 2025 00:13:12 GMT  
		Size: 27.9 MB (27946438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56437b5f3c4f729d31fe7638873251d16b28c1c3d692a9956f5b69136d43e930`  
		Last Modified: Tue, 04 Nov 2025 00:25:28 GMT  
		Size: 18.3 MB (18287214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13428abf70cc1a9fb886bcdae90cfbe2d84d6f55745ed019971ee5ffd12cbc36`  
		Last Modified: Tue, 04 Nov 2025 00:25:27 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa255570f57e9797d70ef3d709d8bc0234a1d6314252033f6b60cde7930d539`  
		Last Modified: Tue, 04 Nov 2025 00:25:27 GMT  
		Size: 4.7 MB (4709590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:2cab70366a5eefad158f1357e7fbb0b830669bd73781291fc8f2f7c487e14ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe26f64be2cf34a6f1dbb907289e3ceedcd6e667a219c0df9ad5cccdd52607e1`

```dockerfile
```

-	Layers:
	-	`sha256:d6ab272cfb896c643aefbdbff6cc4a0edfb3a6ef0aff0c6564cc88a358010e7c`  
		Last Modified: Tue, 04 Nov 2025 08:59:27 GMT  
		Size: 5.6 MB (5585932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c8664e85e0ed44674cf84da06545a8bad6ddb201e7c9bdeffa2d711dc060c4`  
		Last Modified: Tue, 04 Nov 2025 08:59:28 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v7

```console
$ docker pull irssi@sha256:ec7216e01ceba6748f58241dd44ef50c704fd9d0cbf6131634fd49a15f702256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48683586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb33d7b4c257421d912466ff540a8eab48db1957b1513f08e045342c3e09f7e`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
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
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec21711d4a258965a72caed76918b337c0aa5de6b91e590c06fc5e4745646f55`  
		Last Modified: Tue, 21 Oct 2025 01:21:40 GMT  
		Size: 17.9 MB (17908849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b844f9ec9159fe5dc1bceb0c829cf8fed6b324e19975cd9a3e797da3b9e7f32`  
		Last Modified: Tue, 21 Oct 2025 01:21:39 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8319989dae0a45f302eefb7eacf795675adb09faf457ef920f5f154d9e8fd6a`  
		Last Modified: Tue, 21 Oct 2025 01:21:40 GMT  
		Size: 4.6 MB (4558483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:1caf5b32a9cc375fdb8989c5e37fd5701d48a4ee13f33a1efb1c643b6656b614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1644fbc65e3d69b2d3bdd0d9e16c452b7d1c7156e981d44b810e54fb21f72726`

```dockerfile
```

-	Layers:
	-	`sha256:ef4ef36a4fd0ce15ccfe9d8c5c18fc16fafd0038ee0a805f0e2fbd3884993613`  
		Last Modified: Tue, 21 Oct 2025 07:59:30 GMT  
		Size: 5.6 MB (5588954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a879647ba458c48533bd9bc58dc4e49735e56b2b2509ed8842988ba5b86312e0`  
		Last Modified: Tue, 21 Oct 2025 07:59:31 GMT  
		Size: 18.8 KB (18832 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:77dfd1a59d7b77b123cca1beadf2971d1ba2ab34fdeeefeadce1a24e0f13126c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53976450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03efcec3d095c3aea650cc38e8beac272725967f1d9705561a88cc2cfabd06c7`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
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
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b408dc86163fc3064303c3d87a6f050d94d7e50026af6fec8d474bde261f9b`  
		Last Modified: Tue, 21 Oct 2025 01:19:20 GMT  
		Size: 19.0 MB (19049325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec261c2c31268433efbe285382be2e8e472bc1069f6f4703a8c3225b10ce0192`  
		Last Modified: Tue, 21 Oct 2025 01:19:18 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1acd4e881dacb1490ed68208dd4440fca46f3dc100f2a812bf12c1f676495e5`  
		Last Modified: Tue, 21 Oct 2025 01:19:19 GMT  
		Size: 4.8 MB (4781638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:2835026ba33a88cc6dd9fad1db6db1ec4ac24c190ed8d34348d3c797171fcabb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6636c1128d2fa3dcbaaa075ffd279fcdb2e092e8cd8f4acd4b4056e29c38c764`

```dockerfile
```

-	Layers:
	-	`sha256:71b8d4b308985e51f1304ef1f8d2a4365932f656bec2d21685a2b0333d5e3ccb`  
		Last Modified: Tue, 21 Oct 2025 07:59:54 GMT  
		Size: 5.6 MB (5594867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cda273518a593b1fdc06763d67c1ec3babffc7218cf0dfde047a1d3545ed65a0`  
		Last Modified: Tue, 21 Oct 2025 07:59:55 GMT  
		Size: 18.9 KB (18876 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; 386

```console
$ docker pull irssi@sha256:906a0c6f51c0b1f3b4ecb3f2e1c968d3704a25c07977646ef27d94b4b52f843b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54906871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f15a626e6515729d1e92c4029f7fd5ad811e6b1fa57491b31c1375bfd151edd`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
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
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a10221caffdcbfa0e53f49b1c8340c488768b10a5ea331304fe42934a151e92`  
		Last Modified: Tue, 21 Oct 2025 01:19:19 GMT  
		Size: 18.7 MB (18740674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99453861535e7430a13e074b1001d31ea1b6113f5f26cbd98c4898b8f5248b1`  
		Last Modified: Tue, 21 Oct 2025 01:19:17 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2532aeb1762cf3e40be739eca77e4a75e1fe38161883765d09f93de9e8e2da0e`  
		Last Modified: Tue, 21 Oct 2025 01:19:17 GMT  
		Size: 4.9 MB (4868206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:7da87f53975d8a9812601bfebe2d8b85bb1ddace02345349599eb31d26603b89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b166c953777c8cc44a6f84ea8cf0efae3b040be490d0e4cf0af5fc12b2fffe`

```dockerfile
```

-	Layers:
	-	`sha256:0d1c17737f2969710a690596ea60539faa8669ce29c2cdb5aea0ab822518a718`  
		Last Modified: Tue, 21 Oct 2025 10:59:42 GMT  
		Size: 5.6 MB (5584506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cf1c8a6fed6cbd711442dee178708058badce283771d0b8d81faae2d7964c89`  
		Last Modified: Tue, 21 Oct 2025 10:59:43 GMT  
		Size: 18.6 KB (18638 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; ppc64le

```console
$ docker pull irssi@sha256:a084063aa561239245a691754b6dc2d671df6ef0560db4211c54b612f3e7ea15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58241580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f34336095685fcdececa53b502c6d01e505509b56e53158c6db1a854159927`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:40:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:40:10 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 01:40:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 01:40:10 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 01:40:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 01:41:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 01:41:53 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 01:41:53 GMT
USER user
# Tue, 04 Nov 2025 01:41:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87028ebfcd452692a3fb8d88c28f9dcaefbb732091f6921899481be54ff4c14a`  
		Last Modified: Tue, 04 Nov 2025 01:42:34 GMT  
		Size: 19.5 MB (19542341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4394dbe86dcc81b464d6e1d783cd35d455809fc85f44e42d150f96559d485a41`  
		Last Modified: Tue, 04 Nov 2025 01:42:28 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf7c6c4c0df971675464c86be67bdab3c2c25b38b37e01da482c5cb66037d0d`  
		Last Modified: Tue, 04 Nov 2025 01:42:30 GMT  
		Size: 5.1 MB (5097230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:f4763863a1b427e12438c44a011d6f057521086ff7d6d3089a8b1548112e00dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5919bc5740e214ee4b9780aee2c1ad773d2cb3193a47296199d9dd43b538349`

```dockerfile
```

-	Layers:
	-	`sha256:3c8efade8711469af7719f447e79a6a55a49965364fecba525c872e2c2c39f54`  
		Last Modified: Tue, 04 Nov 2025 08:59:43 GMT  
		Size: 5.6 MB (5595414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73fb47554826c5ea1fd080726318e56e507fb096dbdab60c4c068e35d1748a83`  
		Last Modified: Tue, 04 Nov 2025 08:59:43 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; riscv64

```console
$ docker pull irssi@sha256:ad6bd3a5205e24902df7636515066e77cd40386afc556802ffb26f1c77e0e0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51688796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af58c0755eac6d8da52a1a1e0818d9a970afed3f79411b1e29c974e03693f77c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 03:21:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:21:31 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 03:21:31 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 03:21:31 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 03:21:31 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 03:28:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 03:28:16 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 03:28:16 GMT
USER user
# Tue, 04 Nov 2025 03:28:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd582df31684b74a9fa351a3f7a398aaac1fcbdf5dbaa85b5372c8462d7c2f4`  
		Last Modified: Tue, 04 Nov 2025 03:30:29 GMT  
		Size: 18.5 MB (18549071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbc8e452a4bcbb01a4646ec80e76632da072b403d910c0cb470f33071b26713`  
		Last Modified: Tue, 04 Nov 2025 03:30:26 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339fd9308e80cf2bb6fbb2002e6caf32c46d806077d562abd9e9697cb185d246`  
		Last Modified: Tue, 04 Nov 2025 03:30:27 GMT  
		Size: 4.9 MB (4860578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:386968c0f2cc63a525d899d89b5efea2a6c8fb70db205e6fa72353d875d5a0ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6597a75bc6701428d03667f7d6c7f70c99d7b60e95a8d1fdb08d4b3ad6afec`

```dockerfile
```

-	Layers:
	-	`sha256:dc7fd9c40909a5578f92745efde764baa371271f42768e30f606d02bd12b7e43`  
		Last Modified: Tue, 04 Nov 2025 05:59:53 GMT  
		Size: 5.6 MB (5579686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2613fe6d4ed13c302d41cf48b4f8409a1d5bbf2c78e18ebcfa865a7ff55fc8a9`  
		Last Modified: Tue, 04 Nov 2025 05:59:54 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; s390x

```console
$ docker pull irssi@sha256:3a50bacd0aeaff8b8bb33a64478b835190ffccaa1513205554f7ee1f6a184193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54506755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a48d7420330e0856941ae3d5e153f27daff93349a4fa18e370e1742cb7f711`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 06:57:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 06:57:24 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 06:57:24 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 06:57:24 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 06:57:24 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 06:57:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 06:57:59 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 06:57:59 GMT
USER user
# Tue, 04 Nov 2025 06:57:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033854155955c69f5e80286c0220fcbce49683f27ff99d1e3003af7fcaf6c877`  
		Last Modified: Tue, 04 Nov 2025 06:58:21 GMT  
		Size: 19.8 MB (19760115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c247a95f4cb0054a4d91356e28a34cd9e78b4cd6a91641cb206c20a4432358`  
		Last Modified: Tue, 04 Nov 2025 06:58:20 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c870c8580f75359f105944243814e2056231525934f2762d516037ba84460b`  
		Last Modified: Tue, 04 Nov 2025 06:58:21 GMT  
		Size: 4.9 MB (4905887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:67067471ee97249a779cc6457e15b62dcd86599b15c73cb35fe07d4ee9d9bc15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb77a7d993b8fd0d0709a3f5d273dca60cf5a00b2a1843faf52e53880c2147e9`

```dockerfile
```

-	Layers:
	-	`sha256:6fabbd9421ca04d0605ccb6b593319d76d9eeb706da0f60a92f293e472d49d62`  
		Last Modified: Tue, 04 Nov 2025 09:00:17 GMT  
		Size: 5.6 MB (5589288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcd0465106c749fc617ea8887ce197ef6acc786e35587fff1f92baafdcc874fc`  
		Last Modified: Tue, 04 Nov 2025 09:00:18 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine`

```console
$ docker pull irssi@sha256:1e663ae10149c0b4d9df663b9da7bb650a58deea6cb49343c8191884eb0ec8ab
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
$ docker pull irssi@sha256:faf9e4f6be7260cc0682ec1445c6826e0bdcdc63f4a064eb8a981701bb709594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20173425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8798df3f4b34c7e6f52a3727072b2c410704453c6794f69663ce299680c47d3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e11827177f1c189b726b09341a9159227f1bfd85f6bfa5e738af089ccd47cc`  
		Last Modified: Wed, 08 Oct 2025 22:39:07 GMT  
		Size: 10.4 MB (10396003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6644b44e4c465f7087dbb97380180e75f01380c552303d8a2486f385aad34f35`  
		Last Modified: Wed, 08 Oct 2025 22:39:04 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b031546d04685e49a4d43b8482a34aaa0e6a3a6d75e947a09671aaf238e1ffc`  
		Last Modified: Wed, 08 Oct 2025 22:39:05 GMT  
		Size: 6.0 MB (5973981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:60dc002a8263e274525a471186038e9a631be6a5c61c1fd9e0ec2accade632f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be809ef2f20f547ecb812fc7251645454e581cc3d872627c003659069a74285e`

```dockerfile
```

-	Layers:
	-	`sha256:7def044fb5b5a27bb8a83fe2e1f6903b88c7090d91d03cc25c2be92d2b115084`  
		Last Modified: Thu, 09 Oct 2025 01:59:25 GMT  
		Size: 1.3 MB (1270668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09d745c2ae7ce01c7631e58d7cf581615e9c45ca2b8d31cccaa988c9e5257205`  
		Last Modified: Thu, 09 Oct 2025 01:59:26 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:8dfb08ad7779ab00246287f396771e855c5271e8e67f8fcb68229714505701e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18926923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e4ac8e569bab3223b4cbc8f2ffb5137d951b2efa8fbca448cdef1d3e4925de`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
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
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733b352b3151cd505887f05e68a9791f679acceebf79736c8050c72db1b5191a`  
		Last Modified: Wed, 08 Oct 2025 21:42:07 GMT  
		Size: 9.6 MB (9619615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8386f23106fb9eeab59f6f1e82d6fda32cd5130f7e9240952ab361424133835`  
		Last Modified: Wed, 08 Oct 2025 21:42:06 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5176e22c73a447407c118250d8b7084c947461ad88e0f8ffba848633ef457d1`  
		Last Modified: Wed, 08 Oct 2025 21:42:08 GMT  
		Size: 5.8 MB (5802239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:3529f2221a487a696afdfab5dd8793069c4e5153fdd0bbc77b1a10ed59976e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c402305c7b183a88a4427e0caf1314f408323bb659aab78e52073f5d4946a814`

```dockerfile
```

-	Layers:
	-	`sha256:40cb74de7dde3071930d2507974b11b96e2a2fcf0dd4cc4063ea7658469d44d0`  
		Last Modified: Wed, 08 Oct 2025 22:59:36 GMT  
		Size: 17.5 KB (17462 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:1c77198ac74e17d59093ac465b9d5cb18f5cf9b495d394dc7fe1757c6cd43c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18234853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81e381f20e12f748a613e6b9d046d4f23726de50b2d6209ee706e26cdc81cd9`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
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
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d355e9f8d23dd7df754d0fc9b69cb593d77843421e4fdc90e0999ac63d910671`  
		Last Modified: Wed, 08 Oct 2025 21:42:22 GMT  
		Size: 9.4 MB (9449582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d327d03f3716120871e15d8a53213e2201fb4c543cff4cfda89d44a362924f5b`  
		Last Modified: Wed, 08 Oct 2025 21:42:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a7bac72cbbe13e0d2ca93a7e2045c3cee7af4a9a99e4f4a137d438a669963e`  
		Last Modified: Wed, 08 Oct 2025 21:42:21 GMT  
		Size: 5.6 MB (5562729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:a538097b3d9e95fd66c681e163119ee4fda34648e1138be1471be07765e086b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1291403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121bd05d16ceb8c11139b6c2e140bdd3f2ff4d48d4eeae0c78b36653e7f2cb0a`

```dockerfile
```

-	Layers:
	-	`sha256:66532285c363d95627518c5ee59b11b1d8179d0e9a5459c633c0d02618fed06d`  
		Last Modified: Wed, 08 Oct 2025 22:59:39 GMT  
		Size: 1.3 MB (1273726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81f81d5bd314d48e57ad6439aa665accb301d8fa90cf9cfbc734e80cc3932d07`  
		Last Modified: Wed, 08 Oct 2025 22:59:40 GMT  
		Size: 17.7 KB (17677 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:6312b888a6893a7c5bcbfa3b983ab38749f99778b44a99530ef47a5fa8afe92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20344949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6748a647916da83e7b32a7fc1af7248d48c18b28e2c35d2403a1aeaba48783`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
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
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60d53dd86b6f70255a46f81ded3715200f2293ef56b5b5e4a9bd208fe73a5a4`  
		Last Modified: Wed, 08 Oct 2025 21:28:34 GMT  
		Size: 10.4 MB (10358145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f35b8acbeb2e8727c286447b6769cf3d016bb4864c5ad35e2e295e2f173749a`  
		Last Modified: Wed, 08 Oct 2025 21:28:33 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb455678cd1949819acffee4a71aa2ae7f91c1aae58a696c6666455cd9924e53`  
		Last Modified: Wed, 08 Oct 2025 21:28:35 GMT  
		Size: 5.8 MB (5847748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:816e238d7fee6ac073eb8bd4ed99e37a650f1d462c391ae4ae546450436b6e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f33b353f49dad9739f03717967b6ed81661089b4a5f7503a731715f3f4e1f5`

```dockerfile
```

-	Layers:
	-	`sha256:d1eb3ee699a52f4b20f4604d2e59b51c391ac02eb535317009268ef8a4fc45df`  
		Last Modified: Wed, 08 Oct 2025 22:59:44 GMT  
		Size: 1.3 MB (1270772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:309170da33d1e1e4b4a1a75c21c0120ff197fc0e4fb56a433d3097dd47cdb44b`  
		Last Modified: Wed, 08 Oct 2025 22:59:44 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; 386

```console
$ docker pull irssi@sha256:e66bdc96a17047cd31d803681e0c481fef6963c4d0120511222702e892610149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19616013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9546217ea8e23f6143afa741cd4e2050c708ad5ad67102826bac0bd4e68e070`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
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
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9ef0d9eddfed06ea09466e4f959f424bd4487ea48914b239e32d9a01ae664b`  
		Last Modified: Wed, 08 Oct 2025 21:14:07 GMT  
		Size: 9.9 MB (9940223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1546130b809d653b7ffb8056fabb7cde5c59816ee611d191515f665953378af9`  
		Last Modified: Wed, 08 Oct 2025 21:14:06 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05246638c115aace0ae244236cec9016bac4501e4699e0b5761e13d518f3aa7`  
		Last Modified: Wed, 08 Oct 2025 21:14:07 GMT  
		Size: 6.1 MB (6055871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:b12b29108acc7caee0ab23ab7c1191d2861b6bf4761b820569a0bb5519120cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a3cccb44b653f9d355429131978d3190d1b78b70f94e13b2cc06e9f7997a5e`

```dockerfile
```

-	Layers:
	-	`sha256:3ae7b6184d4abc32aca3718238c88832fa852fc8a1b082f050f7d291dfde1737`  
		Last Modified: Wed, 08 Oct 2025 22:59:48 GMT  
		Size: 1.3 MB (1270623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7720d5b50178fd0c79f8f0d50307c9837e7c9413280ecc69217fdc55705d6b3f`  
		Last Modified: Wed, 08 Oct 2025 22:59:49 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:11ec21937e624e10112a9366a2e39f63804c250cd288519f31d38458aa0c9d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20560595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41dfe8eb30ae660e9f6b618bd8acba1eb372978247dff8685fcdb0393231e246`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
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
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48c17d61a4d1554d280ba28d7252c2f305090eeac61b357dd6b76bd73c43c63`  
		Last Modified: Thu, 09 Oct 2025 00:45:13 GMT  
		Size: 10.6 MB (10595397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26efea3de5b42df966c34855cef32948787b76acb851a4084e3e3ad212766f3`  
		Last Modified: Thu, 09 Oct 2025 00:45:11 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa99ddfbbb8375b453f006a945c8fa07c1ce170fda8448f7b653f0ac29d72c7b`  
		Last Modified: Thu, 09 Oct 2025 00:45:07 GMT  
		Size: 6.2 MB (6231972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:9c4cef9155fe22476444ceb17f379012b0c8b3e5e05a7c96919fa63eff2fdfe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179a2005edd691213f7786f101a4bd63364292c1882766e726e961190a7a7a47`

```dockerfile
```

-	Layers:
	-	`sha256:33a5c683cc42bda4a70c31f9d11afeffee44599ee508e945b64f8f0f007364b0`  
		Last Modified: Thu, 09 Oct 2025 01:59:38 GMT  
		Size: 1.3 MB (1268775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921ee5b46b5c6c2bdcc6f69f3de81a1779cddf19f1c547cb5807d97cd7e0429e`  
		Last Modified: Thu, 09 Oct 2025 01:59:39 GMT  
		Size: 17.6 KB (17615 bytes)  
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
$ docker pull irssi@sha256:f3623b26ebb6e5ca70e89646c7b5dc3cc4923efff13fcf40e13603205b1d2c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20728269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4dc9af67d43ea3efb18b38b4dd936194a56cde8d7cedf49529c2085f844b996`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
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
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a35a93027b47a44ea544d9fee84d01ab7be35185d9c512211141ce9d358b9c`  
		Last Modified: Thu, 09 Oct 2025 00:42:42 GMT  
		Size: 11.0 MB (10953642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054cb0439f6b75b07dcf89d2ae109ef474c8c1ca0e6748b16768e98125bfadd4`  
		Last Modified: Thu, 09 Oct 2025 00:42:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1439f567e83e96d3eb1406d4ffb34da86c733b3fc27798542727ad6be641a537`  
		Last Modified: Thu, 09 Oct 2025 00:42:36 GMT  
		Size: 6.1 MB (6124398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:033679be33af045692166464cde309c06c55d1e3c2f0f70ff8f5a32a40c138cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3b68e4209308a841644a418b0f59ac60f7f2626e13c308ee01fa66528b5f4b`

```dockerfile
```

-	Layers:
	-	`sha256:874c4b424a680cfa6457999c0ce435d96b02cffc5203fa3f92b393d5811628a1`  
		Last Modified: Thu, 09 Oct 2025 01:59:58 GMT  
		Size: 1.3 MB (1268717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:586c45ea22dc49613e4d853a8c98ede4e76cc44653d06cf317710f979f305a99`  
		Last Modified: Thu, 09 Oct 2025 01:59:59 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine3.22`

```console
$ docker pull irssi@sha256:1e663ae10149c0b4d9df663b9da7bb650a58deea6cb49343c8191884eb0ec8ab
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

### `irssi:1-alpine3.22` - linux; amd64

```console
$ docker pull irssi@sha256:faf9e4f6be7260cc0682ec1445c6826e0bdcdc63f4a064eb8a981701bb709594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20173425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8798df3f4b34c7e6f52a3727072b2c410704453c6794f69663ce299680c47d3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e11827177f1c189b726b09341a9159227f1bfd85f6bfa5e738af089ccd47cc`  
		Last Modified: Wed, 08 Oct 2025 22:39:07 GMT  
		Size: 10.4 MB (10396003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6644b44e4c465f7087dbb97380180e75f01380c552303d8a2486f385aad34f35`  
		Last Modified: Wed, 08 Oct 2025 22:39:04 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b031546d04685e49a4d43b8482a34aaa0e6a3a6d75e947a09671aaf238e1ffc`  
		Last Modified: Wed, 08 Oct 2025 22:39:05 GMT  
		Size: 6.0 MB (5973981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:60dc002a8263e274525a471186038e9a631be6a5c61c1fd9e0ec2accade632f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be809ef2f20f547ecb812fc7251645454e581cc3d872627c003659069a74285e`

```dockerfile
```

-	Layers:
	-	`sha256:7def044fb5b5a27bb8a83fe2e1f6903b88c7090d91d03cc25c2be92d2b115084`  
		Last Modified: Thu, 09 Oct 2025 01:59:25 GMT  
		Size: 1.3 MB (1270668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09d745c2ae7ce01c7631e58d7cf581615e9c45ca2b8d31cccaa988c9e5257205`  
		Last Modified: Thu, 09 Oct 2025 01:59:26 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.22` - linux; arm variant v6

```console
$ docker pull irssi@sha256:8dfb08ad7779ab00246287f396771e855c5271e8e67f8fcb68229714505701e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18926923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e4ac8e569bab3223b4cbc8f2ffb5137d951b2efa8fbca448cdef1d3e4925de`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
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
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733b352b3151cd505887f05e68a9791f679acceebf79736c8050c72db1b5191a`  
		Last Modified: Wed, 08 Oct 2025 21:42:07 GMT  
		Size: 9.6 MB (9619615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8386f23106fb9eeab59f6f1e82d6fda32cd5130f7e9240952ab361424133835`  
		Last Modified: Wed, 08 Oct 2025 21:42:06 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5176e22c73a447407c118250d8b7084c947461ad88e0f8ffba848633ef457d1`  
		Last Modified: Wed, 08 Oct 2025 21:42:08 GMT  
		Size: 5.8 MB (5802239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:3529f2221a487a696afdfab5dd8793069c4e5153fdd0bbc77b1a10ed59976e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c402305c7b183a88a4427e0caf1314f408323bb659aab78e52073f5d4946a814`

```dockerfile
```

-	Layers:
	-	`sha256:40cb74de7dde3071930d2507974b11b96e2a2fcf0dd4cc4063ea7658469d44d0`  
		Last Modified: Wed, 08 Oct 2025 22:59:36 GMT  
		Size: 17.5 KB (17462 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.22` - linux; arm variant v7

```console
$ docker pull irssi@sha256:1c77198ac74e17d59093ac465b9d5cb18f5cf9b495d394dc7fe1757c6cd43c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18234853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81e381f20e12f748a613e6b9d046d4f23726de50b2d6209ee706e26cdc81cd9`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
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
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d355e9f8d23dd7df754d0fc9b69cb593d77843421e4fdc90e0999ac63d910671`  
		Last Modified: Wed, 08 Oct 2025 21:42:22 GMT  
		Size: 9.4 MB (9449582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d327d03f3716120871e15d8a53213e2201fb4c543cff4cfda89d44a362924f5b`  
		Last Modified: Wed, 08 Oct 2025 21:42:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a7bac72cbbe13e0d2ca93a7e2045c3cee7af4a9a99e4f4a137d438a669963e`  
		Last Modified: Wed, 08 Oct 2025 21:42:21 GMT  
		Size: 5.6 MB (5562729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:a538097b3d9e95fd66c681e163119ee4fda34648e1138be1471be07765e086b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1291403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121bd05d16ceb8c11139b6c2e140bdd3f2ff4d48d4eeae0c78b36653e7f2cb0a`

```dockerfile
```

-	Layers:
	-	`sha256:66532285c363d95627518c5ee59b11b1d8179d0e9a5459c633c0d02618fed06d`  
		Last Modified: Wed, 08 Oct 2025 22:59:39 GMT  
		Size: 1.3 MB (1273726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81f81d5bd314d48e57ad6439aa665accb301d8fa90cf9cfbc734e80cc3932d07`  
		Last Modified: Wed, 08 Oct 2025 22:59:40 GMT  
		Size: 17.7 KB (17677 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:6312b888a6893a7c5bcbfa3b983ab38749f99778b44a99530ef47a5fa8afe92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20344949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6748a647916da83e7b32a7fc1af7248d48c18b28e2c35d2403a1aeaba48783`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
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
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60d53dd86b6f70255a46f81ded3715200f2293ef56b5b5e4a9bd208fe73a5a4`  
		Last Modified: Wed, 08 Oct 2025 21:28:34 GMT  
		Size: 10.4 MB (10358145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f35b8acbeb2e8727c286447b6769cf3d016bb4864c5ad35e2e295e2f173749a`  
		Last Modified: Wed, 08 Oct 2025 21:28:33 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb455678cd1949819acffee4a71aa2ae7f91c1aae58a696c6666455cd9924e53`  
		Last Modified: Wed, 08 Oct 2025 21:28:35 GMT  
		Size: 5.8 MB (5847748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:816e238d7fee6ac073eb8bd4ed99e37a650f1d462c391ae4ae546450436b6e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f33b353f49dad9739f03717967b6ed81661089b4a5f7503a731715f3f4e1f5`

```dockerfile
```

-	Layers:
	-	`sha256:d1eb3ee699a52f4b20f4604d2e59b51c391ac02eb535317009268ef8a4fc45df`  
		Last Modified: Wed, 08 Oct 2025 22:59:44 GMT  
		Size: 1.3 MB (1270772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:309170da33d1e1e4b4a1a75c21c0120ff197fc0e4fb56a433d3097dd47cdb44b`  
		Last Modified: Wed, 08 Oct 2025 22:59:44 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.22` - linux; 386

```console
$ docker pull irssi@sha256:e66bdc96a17047cd31d803681e0c481fef6963c4d0120511222702e892610149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19616013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9546217ea8e23f6143afa741cd4e2050c708ad5ad67102826bac0bd4e68e070`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
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
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9ef0d9eddfed06ea09466e4f959f424bd4487ea48914b239e32d9a01ae664b`  
		Last Modified: Wed, 08 Oct 2025 21:14:07 GMT  
		Size: 9.9 MB (9940223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1546130b809d653b7ffb8056fabb7cde5c59816ee611d191515f665953378af9`  
		Last Modified: Wed, 08 Oct 2025 21:14:06 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05246638c115aace0ae244236cec9016bac4501e4699e0b5761e13d518f3aa7`  
		Last Modified: Wed, 08 Oct 2025 21:14:07 GMT  
		Size: 6.1 MB (6055871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:b12b29108acc7caee0ab23ab7c1191d2861b6bf4761b820569a0bb5519120cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a3cccb44b653f9d355429131978d3190d1b78b70f94e13b2cc06e9f7997a5e`

```dockerfile
```

-	Layers:
	-	`sha256:3ae7b6184d4abc32aca3718238c88832fa852fc8a1b082f050f7d291dfde1737`  
		Last Modified: Wed, 08 Oct 2025 22:59:48 GMT  
		Size: 1.3 MB (1270623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7720d5b50178fd0c79f8f0d50307c9837e7c9413280ecc69217fdc55705d6b3f`  
		Last Modified: Wed, 08 Oct 2025 22:59:49 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.22` - linux; ppc64le

```console
$ docker pull irssi@sha256:11ec21937e624e10112a9366a2e39f63804c250cd288519f31d38458aa0c9d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20560595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41dfe8eb30ae660e9f6b618bd8acba1eb372978247dff8685fcdb0393231e246`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
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
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48c17d61a4d1554d280ba28d7252c2f305090eeac61b357dd6b76bd73c43c63`  
		Last Modified: Thu, 09 Oct 2025 00:45:13 GMT  
		Size: 10.6 MB (10595397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26efea3de5b42df966c34855cef32948787b76acb851a4084e3e3ad212766f3`  
		Last Modified: Thu, 09 Oct 2025 00:45:11 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa99ddfbbb8375b453f006a945c8fa07c1ce170fda8448f7b653f0ac29d72c7b`  
		Last Modified: Thu, 09 Oct 2025 00:45:07 GMT  
		Size: 6.2 MB (6231972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:9c4cef9155fe22476444ceb17f379012b0c8b3e5e05a7c96919fa63eff2fdfe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179a2005edd691213f7786f101a4bd63364292c1882766e726e961190a7a7a47`

```dockerfile
```

-	Layers:
	-	`sha256:33a5c683cc42bda4a70c31f9d11afeffee44599ee508e945b64f8f0f007364b0`  
		Last Modified: Thu, 09 Oct 2025 01:59:38 GMT  
		Size: 1.3 MB (1268775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921ee5b46b5c6c2bdcc6f69f3de81a1779cddf19f1c547cb5807d97cd7e0429e`  
		Last Modified: Thu, 09 Oct 2025 01:59:39 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.22` - linux; riscv64

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

### `irssi:1-alpine3.22` - unknown; unknown

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

### `irssi:1-alpine3.22` - linux; s390x

```console
$ docker pull irssi@sha256:f3623b26ebb6e5ca70e89646c7b5dc3cc4923efff13fcf40e13603205b1d2c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20728269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4dc9af67d43ea3efb18b38b4dd936194a56cde8d7cedf49529c2085f844b996`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
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
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a35a93027b47a44ea544d9fee84d01ab7be35185d9c512211141ce9d358b9c`  
		Last Modified: Thu, 09 Oct 2025 00:42:42 GMT  
		Size: 11.0 MB (10953642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054cb0439f6b75b07dcf89d2ae109ef474c8c1ca0e6748b16768e98125bfadd4`  
		Last Modified: Thu, 09 Oct 2025 00:42:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1439f567e83e96d3eb1406d4ffb34da86c733b3fc27798542727ad6be641a537`  
		Last Modified: Thu, 09 Oct 2025 00:42:36 GMT  
		Size: 6.1 MB (6124398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:033679be33af045692166464cde309c06c55d1e3c2f0f70ff8f5a32a40c138cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3b68e4209308a841644a418b0f59ac60f7f2626e13c308ee01fa66528b5f4b`

```dockerfile
```

-	Layers:
	-	`sha256:874c4b424a680cfa6457999c0ce435d96b02cffc5203fa3f92b393d5811628a1`  
		Last Modified: Thu, 09 Oct 2025 01:59:58 GMT  
		Size: 1.3 MB (1268717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:586c45ea22dc49613e4d853a8c98ede4e76cc44653d06cf317710f979f305a99`  
		Last Modified: Thu, 09 Oct 2025 01:59:59 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-trixie`

```console
$ docker pull irssi@sha256:5cf9ab8c791c26cf2aa97983f1cc4debbebc4fb203bae59694fc0398575102d2
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
$ docker pull irssi@sha256:f62560d766eab4534167883aef43fa8fad47d829ff5c18467b86628e024bd9c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53870137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769552443b8c0b77660078238cebe5d212969cc1cef60189b3e988284170f129`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
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
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50e33926f10233e1cefedd2afc470ffdca1d03aae27f61804a5308859157ecd`  
		Last Modified: Tue, 21 Oct 2025 01:18:57 GMT  
		Size: 19.2 MB (19222452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5172862d08ce0c808ae6bd8643e68f924682e5145be1e8111d0b52f49a6fe9bc`  
		Last Modified: Tue, 21 Oct 2025 01:18:55 GMT  
		Size: 3.3 KB (3335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160b0c22ddb061ea4cd17f1ed3ca11aec9c1535fa615b47a6577d131dafc4ba3`  
		Last Modified: Tue, 21 Oct 2025 01:18:56 GMT  
		Size: 4.9 MB (4866394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:6eff9cda53aa1fce62b753cb7e75d79fbe1450f9fec0a77f0972a0a5c20df8d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4a3535c6261e33feac4e249dfb231f9d22a1d643b2b4a9b3d8f0a1ed8ff4dc`

```dockerfile
```

-	Layers:
	-	`sha256:984b3275ff964e7bbd701d8b5ca39a1b1abcd3f1bcf095ff7fea54585adab0a5`  
		Last Modified: Tue, 21 Oct 2025 10:59:26 GMT  
		Size: 5.6 MB (5588383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80576291496298d1465daebae79c9c7e21c694e8d2ab8ac5425ebf50e8de2192`  
		Last Modified: Tue, 21 Oct 2025 10:59:27 GMT  
		Size: 18.7 KB (18694 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:53bc4bdfbee3e6398af8cf776254a80b7ed67e7da2fe11c32d32d7abbe566dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50946604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea2d9d131f13dbc0476fa90cf34ad8697fe5db46e9a4c3807db7c7805165ed1`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 00:24:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:24:18 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 00:24:18 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 00:24:18 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 00:24:18 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 00:25:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 00:25:08 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 00:25:08 GMT
USER user
# Tue, 04 Nov 2025 00:25:08 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:453afc2258d7bc5729fed5672fb95bafa092e30a933b4377a12034be940a671b`  
		Last Modified: Tue, 04 Nov 2025 00:13:12 GMT  
		Size: 27.9 MB (27946438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56437b5f3c4f729d31fe7638873251d16b28c1c3d692a9956f5b69136d43e930`  
		Last Modified: Tue, 04 Nov 2025 00:25:28 GMT  
		Size: 18.3 MB (18287214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13428abf70cc1a9fb886bcdae90cfbe2d84d6f55745ed019971ee5ffd12cbc36`  
		Last Modified: Tue, 04 Nov 2025 00:25:27 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa255570f57e9797d70ef3d709d8bc0234a1d6314252033f6b60cde7930d539`  
		Last Modified: Tue, 04 Nov 2025 00:25:27 GMT  
		Size: 4.7 MB (4709590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:2cab70366a5eefad158f1357e7fbb0b830669bd73781291fc8f2f7c487e14ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe26f64be2cf34a6f1dbb907289e3ceedcd6e667a219c0df9ad5cccdd52607e1`

```dockerfile
```

-	Layers:
	-	`sha256:d6ab272cfb896c643aefbdbff6cc4a0edfb3a6ef0aff0c6564cc88a358010e7c`  
		Last Modified: Tue, 04 Nov 2025 08:59:27 GMT  
		Size: 5.6 MB (5585932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c8664e85e0ed44674cf84da06545a8bad6ddb201e7c9bdeffa2d711dc060c4`  
		Last Modified: Tue, 04 Nov 2025 08:59:28 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:ec7216e01ceba6748f58241dd44ef50c704fd9d0cbf6131634fd49a15f702256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48683586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb33d7b4c257421d912466ff540a8eab48db1957b1513f08e045342c3e09f7e`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
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
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec21711d4a258965a72caed76918b337c0aa5de6b91e590c06fc5e4745646f55`  
		Last Modified: Tue, 21 Oct 2025 01:21:40 GMT  
		Size: 17.9 MB (17908849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b844f9ec9159fe5dc1bceb0c829cf8fed6b324e19975cd9a3e797da3b9e7f32`  
		Last Modified: Tue, 21 Oct 2025 01:21:39 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8319989dae0a45f302eefb7eacf795675adb09faf457ef920f5f154d9e8fd6a`  
		Last Modified: Tue, 21 Oct 2025 01:21:40 GMT  
		Size: 4.6 MB (4558483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:1caf5b32a9cc375fdb8989c5e37fd5701d48a4ee13f33a1efb1c643b6656b614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1644fbc65e3d69b2d3bdd0d9e16c452b7d1c7156e981d44b810e54fb21f72726`

```dockerfile
```

-	Layers:
	-	`sha256:ef4ef36a4fd0ce15ccfe9d8c5c18fc16fafd0038ee0a805f0e2fbd3884993613`  
		Last Modified: Tue, 21 Oct 2025 07:59:30 GMT  
		Size: 5.6 MB (5588954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a879647ba458c48533bd9bc58dc4e49735e56b2b2509ed8842988ba5b86312e0`  
		Last Modified: Tue, 21 Oct 2025 07:59:31 GMT  
		Size: 18.8 KB (18832 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:77dfd1a59d7b77b123cca1beadf2971d1ba2ab34fdeeefeadce1a24e0f13126c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53976450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03efcec3d095c3aea650cc38e8beac272725967f1d9705561a88cc2cfabd06c7`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
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
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b408dc86163fc3064303c3d87a6f050d94d7e50026af6fec8d474bde261f9b`  
		Last Modified: Tue, 21 Oct 2025 01:19:20 GMT  
		Size: 19.0 MB (19049325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec261c2c31268433efbe285382be2e8e472bc1069f6f4703a8c3225b10ce0192`  
		Last Modified: Tue, 21 Oct 2025 01:19:18 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1acd4e881dacb1490ed68208dd4440fca46f3dc100f2a812bf12c1f676495e5`  
		Last Modified: Tue, 21 Oct 2025 01:19:19 GMT  
		Size: 4.8 MB (4781638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:2835026ba33a88cc6dd9fad1db6db1ec4ac24c190ed8d34348d3c797171fcabb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6636c1128d2fa3dcbaaa075ffd279fcdb2e092e8cd8f4acd4b4056e29c38c764`

```dockerfile
```

-	Layers:
	-	`sha256:71b8d4b308985e51f1304ef1f8d2a4365932f656bec2d21685a2b0333d5e3ccb`  
		Last Modified: Tue, 21 Oct 2025 07:59:54 GMT  
		Size: 5.6 MB (5594867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cda273518a593b1fdc06763d67c1ec3babffc7218cf0dfde047a1d3545ed65a0`  
		Last Modified: Tue, 21 Oct 2025 07:59:55 GMT  
		Size: 18.9 KB (18876 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; 386

```console
$ docker pull irssi@sha256:906a0c6f51c0b1f3b4ecb3f2e1c968d3704a25c07977646ef27d94b4b52f843b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54906871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f15a626e6515729d1e92c4029f7fd5ad811e6b1fa57491b31c1375bfd151edd`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
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
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a10221caffdcbfa0e53f49b1c8340c488768b10a5ea331304fe42934a151e92`  
		Last Modified: Tue, 21 Oct 2025 01:19:19 GMT  
		Size: 18.7 MB (18740674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99453861535e7430a13e074b1001d31ea1b6113f5f26cbd98c4898b8f5248b1`  
		Last Modified: Tue, 21 Oct 2025 01:19:17 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2532aeb1762cf3e40be739eca77e4a75e1fe38161883765d09f93de9e8e2da0e`  
		Last Modified: Tue, 21 Oct 2025 01:19:17 GMT  
		Size: 4.9 MB (4868206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:7da87f53975d8a9812601bfebe2d8b85bb1ddace02345349599eb31d26603b89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b166c953777c8cc44a6f84ea8cf0efae3b040be490d0e4cf0af5fc12b2fffe`

```dockerfile
```

-	Layers:
	-	`sha256:0d1c17737f2969710a690596ea60539faa8669ce29c2cdb5aea0ab822518a718`  
		Last Modified: Tue, 21 Oct 2025 10:59:42 GMT  
		Size: 5.6 MB (5584506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cf1c8a6fed6cbd711442dee178708058badce283771d0b8d81faae2d7964c89`  
		Last Modified: Tue, 21 Oct 2025 10:59:43 GMT  
		Size: 18.6 KB (18638 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:a084063aa561239245a691754b6dc2d671df6ef0560db4211c54b612f3e7ea15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58241580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f34336095685fcdececa53b502c6d01e505509b56e53158c6db1a854159927`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:40:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:40:10 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 01:40:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 01:40:10 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 01:40:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 01:41:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 01:41:53 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 01:41:53 GMT
USER user
# Tue, 04 Nov 2025 01:41:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87028ebfcd452692a3fb8d88c28f9dcaefbb732091f6921899481be54ff4c14a`  
		Last Modified: Tue, 04 Nov 2025 01:42:34 GMT  
		Size: 19.5 MB (19542341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4394dbe86dcc81b464d6e1d783cd35d455809fc85f44e42d150f96559d485a41`  
		Last Modified: Tue, 04 Nov 2025 01:42:28 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf7c6c4c0df971675464c86be67bdab3c2c25b38b37e01da482c5cb66037d0d`  
		Last Modified: Tue, 04 Nov 2025 01:42:30 GMT  
		Size: 5.1 MB (5097230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:f4763863a1b427e12438c44a011d6f057521086ff7d6d3089a8b1548112e00dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5919bc5740e214ee4b9780aee2c1ad773d2cb3193a47296199d9dd43b538349`

```dockerfile
```

-	Layers:
	-	`sha256:3c8efade8711469af7719f447e79a6a55a49965364fecba525c872e2c2c39f54`  
		Last Modified: Tue, 04 Nov 2025 08:59:43 GMT  
		Size: 5.6 MB (5595414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73fb47554826c5ea1fd080726318e56e507fb096dbdab60c4c068e35d1748a83`  
		Last Modified: Tue, 04 Nov 2025 08:59:43 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:ad6bd3a5205e24902df7636515066e77cd40386afc556802ffb26f1c77e0e0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51688796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af58c0755eac6d8da52a1a1e0818d9a970afed3f79411b1e29c974e03693f77c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 03:21:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:21:31 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 03:21:31 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 03:21:31 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 03:21:31 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 03:28:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 03:28:16 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 03:28:16 GMT
USER user
# Tue, 04 Nov 2025 03:28:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd582df31684b74a9fa351a3f7a398aaac1fcbdf5dbaa85b5372c8462d7c2f4`  
		Last Modified: Tue, 04 Nov 2025 03:30:29 GMT  
		Size: 18.5 MB (18549071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbc8e452a4bcbb01a4646ec80e76632da072b403d910c0cb470f33071b26713`  
		Last Modified: Tue, 04 Nov 2025 03:30:26 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339fd9308e80cf2bb6fbb2002e6caf32c46d806077d562abd9e9697cb185d246`  
		Last Modified: Tue, 04 Nov 2025 03:30:27 GMT  
		Size: 4.9 MB (4860578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:386968c0f2cc63a525d899d89b5efea2a6c8fb70db205e6fa72353d875d5a0ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6597a75bc6701428d03667f7d6c7f70c99d7b60e95a8d1fdb08d4b3ad6afec`

```dockerfile
```

-	Layers:
	-	`sha256:dc7fd9c40909a5578f92745efde764baa371271f42768e30f606d02bd12b7e43`  
		Last Modified: Tue, 04 Nov 2025 05:59:53 GMT  
		Size: 5.6 MB (5579686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2613fe6d4ed13c302d41cf48b4f8409a1d5bbf2c78e18ebcfa865a7ff55fc8a9`  
		Last Modified: Tue, 04 Nov 2025 05:59:54 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; s390x

```console
$ docker pull irssi@sha256:3a50bacd0aeaff8b8bb33a64478b835190ffccaa1513205554f7ee1f6a184193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54506755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a48d7420330e0856941ae3d5e153f27daff93349a4fa18e370e1742cb7f711`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 06:57:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 06:57:24 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 06:57:24 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 06:57:24 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 06:57:24 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 06:57:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 06:57:59 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 06:57:59 GMT
USER user
# Tue, 04 Nov 2025 06:57:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033854155955c69f5e80286c0220fcbce49683f27ff99d1e3003af7fcaf6c877`  
		Last Modified: Tue, 04 Nov 2025 06:58:21 GMT  
		Size: 19.8 MB (19760115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c247a95f4cb0054a4d91356e28a34cd9e78b4cd6a91641cb206c20a4432358`  
		Last Modified: Tue, 04 Nov 2025 06:58:20 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c870c8580f75359f105944243814e2056231525934f2762d516037ba84460b`  
		Last Modified: Tue, 04 Nov 2025 06:58:21 GMT  
		Size: 4.9 MB (4905887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:67067471ee97249a779cc6457e15b62dcd86599b15c73cb35fe07d4ee9d9bc15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb77a7d993b8fd0d0709a3f5d273dca60cf5a00b2a1843faf52e53880c2147e9`

```dockerfile
```

-	Layers:
	-	`sha256:6fabbd9421ca04d0605ccb6b593319d76d9eeb706da0f60a92f293e472d49d62`  
		Last Modified: Tue, 04 Nov 2025 09:00:17 GMT  
		Size: 5.6 MB (5589288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcd0465106c749fc617ea8887ce197ef6acc786e35587fff1f92baafdcc874fc`  
		Last Modified: Tue, 04 Nov 2025 09:00:18 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4`

```console
$ docker pull irssi@sha256:5cf9ab8c791c26cf2aa97983f1cc4debbebc4fb203bae59694fc0398575102d2
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
$ docker pull irssi@sha256:f62560d766eab4534167883aef43fa8fad47d829ff5c18467b86628e024bd9c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53870137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769552443b8c0b77660078238cebe5d212969cc1cef60189b3e988284170f129`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
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
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50e33926f10233e1cefedd2afc470ffdca1d03aae27f61804a5308859157ecd`  
		Last Modified: Tue, 21 Oct 2025 01:18:57 GMT  
		Size: 19.2 MB (19222452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5172862d08ce0c808ae6bd8643e68f924682e5145be1e8111d0b52f49a6fe9bc`  
		Last Modified: Tue, 21 Oct 2025 01:18:55 GMT  
		Size: 3.3 KB (3335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160b0c22ddb061ea4cd17f1ed3ca11aec9c1535fa615b47a6577d131dafc4ba3`  
		Last Modified: Tue, 21 Oct 2025 01:18:56 GMT  
		Size: 4.9 MB (4866394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:6eff9cda53aa1fce62b753cb7e75d79fbe1450f9fec0a77f0972a0a5c20df8d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4a3535c6261e33feac4e249dfb231f9d22a1d643b2b4a9b3d8f0a1ed8ff4dc`

```dockerfile
```

-	Layers:
	-	`sha256:984b3275ff964e7bbd701d8b5ca39a1b1abcd3f1bcf095ff7fea54585adab0a5`  
		Last Modified: Tue, 21 Oct 2025 10:59:26 GMT  
		Size: 5.6 MB (5588383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80576291496298d1465daebae79c9c7e21c694e8d2ab8ac5425ebf50e8de2192`  
		Last Modified: Tue, 21 Oct 2025 10:59:27 GMT  
		Size: 18.7 KB (18694 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v5

```console
$ docker pull irssi@sha256:53bc4bdfbee3e6398af8cf776254a80b7ed67e7da2fe11c32d32d7abbe566dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50946604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea2d9d131f13dbc0476fa90cf34ad8697fe5db46e9a4c3807db7c7805165ed1`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 00:24:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:24:18 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 00:24:18 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 00:24:18 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 00:24:18 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 00:25:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 00:25:08 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 00:25:08 GMT
USER user
# Tue, 04 Nov 2025 00:25:08 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:453afc2258d7bc5729fed5672fb95bafa092e30a933b4377a12034be940a671b`  
		Last Modified: Tue, 04 Nov 2025 00:13:12 GMT  
		Size: 27.9 MB (27946438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56437b5f3c4f729d31fe7638873251d16b28c1c3d692a9956f5b69136d43e930`  
		Last Modified: Tue, 04 Nov 2025 00:25:28 GMT  
		Size: 18.3 MB (18287214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13428abf70cc1a9fb886bcdae90cfbe2d84d6f55745ed019971ee5ffd12cbc36`  
		Last Modified: Tue, 04 Nov 2025 00:25:27 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa255570f57e9797d70ef3d709d8bc0234a1d6314252033f6b60cde7930d539`  
		Last Modified: Tue, 04 Nov 2025 00:25:27 GMT  
		Size: 4.7 MB (4709590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:2cab70366a5eefad158f1357e7fbb0b830669bd73781291fc8f2f7c487e14ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe26f64be2cf34a6f1dbb907289e3ceedcd6e667a219c0df9ad5cccdd52607e1`

```dockerfile
```

-	Layers:
	-	`sha256:d6ab272cfb896c643aefbdbff6cc4a0edfb3a6ef0aff0c6564cc88a358010e7c`  
		Last Modified: Tue, 04 Nov 2025 08:59:27 GMT  
		Size: 5.6 MB (5585932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c8664e85e0ed44674cf84da06545a8bad6ddb201e7c9bdeffa2d711dc060c4`  
		Last Modified: Tue, 04 Nov 2025 08:59:28 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v7

```console
$ docker pull irssi@sha256:ec7216e01ceba6748f58241dd44ef50c704fd9d0cbf6131634fd49a15f702256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48683586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb33d7b4c257421d912466ff540a8eab48db1957b1513f08e045342c3e09f7e`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
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
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec21711d4a258965a72caed76918b337c0aa5de6b91e590c06fc5e4745646f55`  
		Last Modified: Tue, 21 Oct 2025 01:21:40 GMT  
		Size: 17.9 MB (17908849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b844f9ec9159fe5dc1bceb0c829cf8fed6b324e19975cd9a3e797da3b9e7f32`  
		Last Modified: Tue, 21 Oct 2025 01:21:39 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8319989dae0a45f302eefb7eacf795675adb09faf457ef920f5f154d9e8fd6a`  
		Last Modified: Tue, 21 Oct 2025 01:21:40 GMT  
		Size: 4.6 MB (4558483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:1caf5b32a9cc375fdb8989c5e37fd5701d48a4ee13f33a1efb1c643b6656b614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1644fbc65e3d69b2d3bdd0d9e16c452b7d1c7156e981d44b810e54fb21f72726`

```dockerfile
```

-	Layers:
	-	`sha256:ef4ef36a4fd0ce15ccfe9d8c5c18fc16fafd0038ee0a805f0e2fbd3884993613`  
		Last Modified: Tue, 21 Oct 2025 07:59:30 GMT  
		Size: 5.6 MB (5588954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a879647ba458c48533bd9bc58dc4e49735e56b2b2509ed8842988ba5b86312e0`  
		Last Modified: Tue, 21 Oct 2025 07:59:31 GMT  
		Size: 18.8 KB (18832 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:77dfd1a59d7b77b123cca1beadf2971d1ba2ab34fdeeefeadce1a24e0f13126c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53976450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03efcec3d095c3aea650cc38e8beac272725967f1d9705561a88cc2cfabd06c7`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
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
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b408dc86163fc3064303c3d87a6f050d94d7e50026af6fec8d474bde261f9b`  
		Last Modified: Tue, 21 Oct 2025 01:19:20 GMT  
		Size: 19.0 MB (19049325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec261c2c31268433efbe285382be2e8e472bc1069f6f4703a8c3225b10ce0192`  
		Last Modified: Tue, 21 Oct 2025 01:19:18 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1acd4e881dacb1490ed68208dd4440fca46f3dc100f2a812bf12c1f676495e5`  
		Last Modified: Tue, 21 Oct 2025 01:19:19 GMT  
		Size: 4.8 MB (4781638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:2835026ba33a88cc6dd9fad1db6db1ec4ac24c190ed8d34348d3c797171fcabb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6636c1128d2fa3dcbaaa075ffd279fcdb2e092e8cd8f4acd4b4056e29c38c764`

```dockerfile
```

-	Layers:
	-	`sha256:71b8d4b308985e51f1304ef1f8d2a4365932f656bec2d21685a2b0333d5e3ccb`  
		Last Modified: Tue, 21 Oct 2025 07:59:54 GMT  
		Size: 5.6 MB (5594867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cda273518a593b1fdc06763d67c1ec3babffc7218cf0dfde047a1d3545ed65a0`  
		Last Modified: Tue, 21 Oct 2025 07:59:55 GMT  
		Size: 18.9 KB (18876 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; 386

```console
$ docker pull irssi@sha256:906a0c6f51c0b1f3b4ecb3f2e1c968d3704a25c07977646ef27d94b4b52f843b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54906871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f15a626e6515729d1e92c4029f7fd5ad811e6b1fa57491b31c1375bfd151edd`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
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
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a10221caffdcbfa0e53f49b1c8340c488768b10a5ea331304fe42934a151e92`  
		Last Modified: Tue, 21 Oct 2025 01:19:19 GMT  
		Size: 18.7 MB (18740674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99453861535e7430a13e074b1001d31ea1b6113f5f26cbd98c4898b8f5248b1`  
		Last Modified: Tue, 21 Oct 2025 01:19:17 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2532aeb1762cf3e40be739eca77e4a75e1fe38161883765d09f93de9e8e2da0e`  
		Last Modified: Tue, 21 Oct 2025 01:19:17 GMT  
		Size: 4.9 MB (4868206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:7da87f53975d8a9812601bfebe2d8b85bb1ddace02345349599eb31d26603b89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b166c953777c8cc44a6f84ea8cf0efae3b040be490d0e4cf0af5fc12b2fffe`

```dockerfile
```

-	Layers:
	-	`sha256:0d1c17737f2969710a690596ea60539faa8669ce29c2cdb5aea0ab822518a718`  
		Last Modified: Tue, 21 Oct 2025 10:59:42 GMT  
		Size: 5.6 MB (5584506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cf1c8a6fed6cbd711442dee178708058badce283771d0b8d81faae2d7964c89`  
		Last Modified: Tue, 21 Oct 2025 10:59:43 GMT  
		Size: 18.6 KB (18638 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; ppc64le

```console
$ docker pull irssi@sha256:a084063aa561239245a691754b6dc2d671df6ef0560db4211c54b612f3e7ea15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58241580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f34336095685fcdececa53b502c6d01e505509b56e53158c6db1a854159927`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:40:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:40:10 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 01:40:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 01:40:10 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 01:40:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 01:41:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 01:41:53 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 01:41:53 GMT
USER user
# Tue, 04 Nov 2025 01:41:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87028ebfcd452692a3fb8d88c28f9dcaefbb732091f6921899481be54ff4c14a`  
		Last Modified: Tue, 04 Nov 2025 01:42:34 GMT  
		Size: 19.5 MB (19542341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4394dbe86dcc81b464d6e1d783cd35d455809fc85f44e42d150f96559d485a41`  
		Last Modified: Tue, 04 Nov 2025 01:42:28 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf7c6c4c0df971675464c86be67bdab3c2c25b38b37e01da482c5cb66037d0d`  
		Last Modified: Tue, 04 Nov 2025 01:42:30 GMT  
		Size: 5.1 MB (5097230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:f4763863a1b427e12438c44a011d6f057521086ff7d6d3089a8b1548112e00dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5919bc5740e214ee4b9780aee2c1ad773d2cb3193a47296199d9dd43b538349`

```dockerfile
```

-	Layers:
	-	`sha256:3c8efade8711469af7719f447e79a6a55a49965364fecba525c872e2c2c39f54`  
		Last Modified: Tue, 04 Nov 2025 08:59:43 GMT  
		Size: 5.6 MB (5595414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73fb47554826c5ea1fd080726318e56e507fb096dbdab60c4c068e35d1748a83`  
		Last Modified: Tue, 04 Nov 2025 08:59:43 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; riscv64

```console
$ docker pull irssi@sha256:ad6bd3a5205e24902df7636515066e77cd40386afc556802ffb26f1c77e0e0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51688796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af58c0755eac6d8da52a1a1e0818d9a970afed3f79411b1e29c974e03693f77c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 03:21:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:21:31 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 03:21:31 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 03:21:31 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 03:21:31 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 03:28:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 03:28:16 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 03:28:16 GMT
USER user
# Tue, 04 Nov 2025 03:28:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd582df31684b74a9fa351a3f7a398aaac1fcbdf5dbaa85b5372c8462d7c2f4`  
		Last Modified: Tue, 04 Nov 2025 03:30:29 GMT  
		Size: 18.5 MB (18549071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbc8e452a4bcbb01a4646ec80e76632da072b403d910c0cb470f33071b26713`  
		Last Modified: Tue, 04 Nov 2025 03:30:26 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339fd9308e80cf2bb6fbb2002e6caf32c46d806077d562abd9e9697cb185d246`  
		Last Modified: Tue, 04 Nov 2025 03:30:27 GMT  
		Size: 4.9 MB (4860578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:386968c0f2cc63a525d899d89b5efea2a6c8fb70db205e6fa72353d875d5a0ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6597a75bc6701428d03667f7d6c7f70c99d7b60e95a8d1fdb08d4b3ad6afec`

```dockerfile
```

-	Layers:
	-	`sha256:dc7fd9c40909a5578f92745efde764baa371271f42768e30f606d02bd12b7e43`  
		Last Modified: Tue, 04 Nov 2025 05:59:53 GMT  
		Size: 5.6 MB (5579686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2613fe6d4ed13c302d41cf48b4f8409a1d5bbf2c78e18ebcfa865a7ff55fc8a9`  
		Last Modified: Tue, 04 Nov 2025 05:59:54 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; s390x

```console
$ docker pull irssi@sha256:3a50bacd0aeaff8b8bb33a64478b835190ffccaa1513205554f7ee1f6a184193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54506755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a48d7420330e0856941ae3d5e153f27daff93349a4fa18e370e1742cb7f711`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 06:57:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 06:57:24 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 06:57:24 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 06:57:24 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 06:57:24 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 06:57:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 06:57:59 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 06:57:59 GMT
USER user
# Tue, 04 Nov 2025 06:57:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033854155955c69f5e80286c0220fcbce49683f27ff99d1e3003af7fcaf6c877`  
		Last Modified: Tue, 04 Nov 2025 06:58:21 GMT  
		Size: 19.8 MB (19760115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c247a95f4cb0054a4d91356e28a34cd9e78b4cd6a91641cb206c20a4432358`  
		Last Modified: Tue, 04 Nov 2025 06:58:20 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c870c8580f75359f105944243814e2056231525934f2762d516037ba84460b`  
		Last Modified: Tue, 04 Nov 2025 06:58:21 GMT  
		Size: 4.9 MB (4905887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:67067471ee97249a779cc6457e15b62dcd86599b15c73cb35fe07d4ee9d9bc15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb77a7d993b8fd0d0709a3f5d273dca60cf5a00b2a1843faf52e53880c2147e9`

```dockerfile
```

-	Layers:
	-	`sha256:6fabbd9421ca04d0605ccb6b593319d76d9eeb706da0f60a92f293e472d49d62`  
		Last Modified: Tue, 04 Nov 2025 09:00:17 GMT  
		Size: 5.6 MB (5589288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcd0465106c749fc617ea8887ce197ef6acc786e35587fff1f92baafdcc874fc`  
		Last Modified: Tue, 04 Nov 2025 09:00:18 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine`

```console
$ docker pull irssi@sha256:1e663ae10149c0b4d9df663b9da7bb650a58deea6cb49343c8191884eb0ec8ab
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
$ docker pull irssi@sha256:faf9e4f6be7260cc0682ec1445c6826e0bdcdc63f4a064eb8a981701bb709594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20173425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8798df3f4b34c7e6f52a3727072b2c410704453c6794f69663ce299680c47d3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e11827177f1c189b726b09341a9159227f1bfd85f6bfa5e738af089ccd47cc`  
		Last Modified: Wed, 08 Oct 2025 22:39:07 GMT  
		Size: 10.4 MB (10396003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6644b44e4c465f7087dbb97380180e75f01380c552303d8a2486f385aad34f35`  
		Last Modified: Wed, 08 Oct 2025 22:39:04 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b031546d04685e49a4d43b8482a34aaa0e6a3a6d75e947a09671aaf238e1ffc`  
		Last Modified: Wed, 08 Oct 2025 22:39:05 GMT  
		Size: 6.0 MB (5973981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:60dc002a8263e274525a471186038e9a631be6a5c61c1fd9e0ec2accade632f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be809ef2f20f547ecb812fc7251645454e581cc3d872627c003659069a74285e`

```dockerfile
```

-	Layers:
	-	`sha256:7def044fb5b5a27bb8a83fe2e1f6903b88c7090d91d03cc25c2be92d2b115084`  
		Last Modified: Thu, 09 Oct 2025 01:59:25 GMT  
		Size: 1.3 MB (1270668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09d745c2ae7ce01c7631e58d7cf581615e9c45ca2b8d31cccaa988c9e5257205`  
		Last Modified: Thu, 09 Oct 2025 01:59:26 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:8dfb08ad7779ab00246287f396771e855c5271e8e67f8fcb68229714505701e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18926923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e4ac8e569bab3223b4cbc8f2ffb5137d951b2efa8fbca448cdef1d3e4925de`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
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
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733b352b3151cd505887f05e68a9791f679acceebf79736c8050c72db1b5191a`  
		Last Modified: Wed, 08 Oct 2025 21:42:07 GMT  
		Size: 9.6 MB (9619615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8386f23106fb9eeab59f6f1e82d6fda32cd5130f7e9240952ab361424133835`  
		Last Modified: Wed, 08 Oct 2025 21:42:06 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5176e22c73a447407c118250d8b7084c947461ad88e0f8ffba848633ef457d1`  
		Last Modified: Wed, 08 Oct 2025 21:42:08 GMT  
		Size: 5.8 MB (5802239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:3529f2221a487a696afdfab5dd8793069c4e5153fdd0bbc77b1a10ed59976e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c402305c7b183a88a4427e0caf1314f408323bb659aab78e52073f5d4946a814`

```dockerfile
```

-	Layers:
	-	`sha256:40cb74de7dde3071930d2507974b11b96e2a2fcf0dd4cc4063ea7658469d44d0`  
		Last Modified: Wed, 08 Oct 2025 22:59:36 GMT  
		Size: 17.5 KB (17462 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:1c77198ac74e17d59093ac465b9d5cb18f5cf9b495d394dc7fe1757c6cd43c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18234853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81e381f20e12f748a613e6b9d046d4f23726de50b2d6209ee706e26cdc81cd9`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
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
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d355e9f8d23dd7df754d0fc9b69cb593d77843421e4fdc90e0999ac63d910671`  
		Last Modified: Wed, 08 Oct 2025 21:42:22 GMT  
		Size: 9.4 MB (9449582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d327d03f3716120871e15d8a53213e2201fb4c543cff4cfda89d44a362924f5b`  
		Last Modified: Wed, 08 Oct 2025 21:42:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a7bac72cbbe13e0d2ca93a7e2045c3cee7af4a9a99e4f4a137d438a669963e`  
		Last Modified: Wed, 08 Oct 2025 21:42:21 GMT  
		Size: 5.6 MB (5562729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:a538097b3d9e95fd66c681e163119ee4fda34648e1138be1471be07765e086b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1291403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121bd05d16ceb8c11139b6c2e140bdd3f2ff4d48d4eeae0c78b36653e7f2cb0a`

```dockerfile
```

-	Layers:
	-	`sha256:66532285c363d95627518c5ee59b11b1d8179d0e9a5459c633c0d02618fed06d`  
		Last Modified: Wed, 08 Oct 2025 22:59:39 GMT  
		Size: 1.3 MB (1273726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81f81d5bd314d48e57ad6439aa665accb301d8fa90cf9cfbc734e80cc3932d07`  
		Last Modified: Wed, 08 Oct 2025 22:59:40 GMT  
		Size: 17.7 KB (17677 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:6312b888a6893a7c5bcbfa3b983ab38749f99778b44a99530ef47a5fa8afe92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20344949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6748a647916da83e7b32a7fc1af7248d48c18b28e2c35d2403a1aeaba48783`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
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
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60d53dd86b6f70255a46f81ded3715200f2293ef56b5b5e4a9bd208fe73a5a4`  
		Last Modified: Wed, 08 Oct 2025 21:28:34 GMT  
		Size: 10.4 MB (10358145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f35b8acbeb2e8727c286447b6769cf3d016bb4864c5ad35e2e295e2f173749a`  
		Last Modified: Wed, 08 Oct 2025 21:28:33 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb455678cd1949819acffee4a71aa2ae7f91c1aae58a696c6666455cd9924e53`  
		Last Modified: Wed, 08 Oct 2025 21:28:35 GMT  
		Size: 5.8 MB (5847748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:816e238d7fee6ac073eb8bd4ed99e37a650f1d462c391ae4ae546450436b6e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f33b353f49dad9739f03717967b6ed81661089b4a5f7503a731715f3f4e1f5`

```dockerfile
```

-	Layers:
	-	`sha256:d1eb3ee699a52f4b20f4604d2e59b51c391ac02eb535317009268ef8a4fc45df`  
		Last Modified: Wed, 08 Oct 2025 22:59:44 GMT  
		Size: 1.3 MB (1270772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:309170da33d1e1e4b4a1a75c21c0120ff197fc0e4fb56a433d3097dd47cdb44b`  
		Last Modified: Wed, 08 Oct 2025 22:59:44 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; 386

```console
$ docker pull irssi@sha256:e66bdc96a17047cd31d803681e0c481fef6963c4d0120511222702e892610149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19616013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9546217ea8e23f6143afa741cd4e2050c708ad5ad67102826bac0bd4e68e070`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
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
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9ef0d9eddfed06ea09466e4f959f424bd4487ea48914b239e32d9a01ae664b`  
		Last Modified: Wed, 08 Oct 2025 21:14:07 GMT  
		Size: 9.9 MB (9940223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1546130b809d653b7ffb8056fabb7cde5c59816ee611d191515f665953378af9`  
		Last Modified: Wed, 08 Oct 2025 21:14:06 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05246638c115aace0ae244236cec9016bac4501e4699e0b5761e13d518f3aa7`  
		Last Modified: Wed, 08 Oct 2025 21:14:07 GMT  
		Size: 6.1 MB (6055871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:b12b29108acc7caee0ab23ab7c1191d2861b6bf4761b820569a0bb5519120cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a3cccb44b653f9d355429131978d3190d1b78b70f94e13b2cc06e9f7997a5e`

```dockerfile
```

-	Layers:
	-	`sha256:3ae7b6184d4abc32aca3718238c88832fa852fc8a1b082f050f7d291dfde1737`  
		Last Modified: Wed, 08 Oct 2025 22:59:48 GMT  
		Size: 1.3 MB (1270623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7720d5b50178fd0c79f8f0d50307c9837e7c9413280ecc69217fdc55705d6b3f`  
		Last Modified: Wed, 08 Oct 2025 22:59:49 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:11ec21937e624e10112a9366a2e39f63804c250cd288519f31d38458aa0c9d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20560595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41dfe8eb30ae660e9f6b618bd8acba1eb372978247dff8685fcdb0393231e246`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
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
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48c17d61a4d1554d280ba28d7252c2f305090eeac61b357dd6b76bd73c43c63`  
		Last Modified: Thu, 09 Oct 2025 00:45:13 GMT  
		Size: 10.6 MB (10595397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26efea3de5b42df966c34855cef32948787b76acb851a4084e3e3ad212766f3`  
		Last Modified: Thu, 09 Oct 2025 00:45:11 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa99ddfbbb8375b453f006a945c8fa07c1ce170fda8448f7b653f0ac29d72c7b`  
		Last Modified: Thu, 09 Oct 2025 00:45:07 GMT  
		Size: 6.2 MB (6231972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:9c4cef9155fe22476444ceb17f379012b0c8b3e5e05a7c96919fa63eff2fdfe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179a2005edd691213f7786f101a4bd63364292c1882766e726e961190a7a7a47`

```dockerfile
```

-	Layers:
	-	`sha256:33a5c683cc42bda4a70c31f9d11afeffee44599ee508e945b64f8f0f007364b0`  
		Last Modified: Thu, 09 Oct 2025 01:59:38 GMT  
		Size: 1.3 MB (1268775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921ee5b46b5c6c2bdcc6f69f3de81a1779cddf19f1c547cb5807d97cd7e0429e`  
		Last Modified: Thu, 09 Oct 2025 01:59:39 GMT  
		Size: 17.6 KB (17615 bytes)  
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
$ docker pull irssi@sha256:f3623b26ebb6e5ca70e89646c7b5dc3cc4923efff13fcf40e13603205b1d2c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20728269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4dc9af67d43ea3efb18b38b4dd936194a56cde8d7cedf49529c2085f844b996`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
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
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a35a93027b47a44ea544d9fee84d01ab7be35185d9c512211141ce9d358b9c`  
		Last Modified: Thu, 09 Oct 2025 00:42:42 GMT  
		Size: 11.0 MB (10953642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054cb0439f6b75b07dcf89d2ae109ef474c8c1ca0e6748b16768e98125bfadd4`  
		Last Modified: Thu, 09 Oct 2025 00:42:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1439f567e83e96d3eb1406d4ffb34da86c733b3fc27798542727ad6be641a537`  
		Last Modified: Thu, 09 Oct 2025 00:42:36 GMT  
		Size: 6.1 MB (6124398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:033679be33af045692166464cde309c06c55d1e3c2f0f70ff8f5a32a40c138cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3b68e4209308a841644a418b0f59ac60f7f2626e13c308ee01fa66528b5f4b`

```dockerfile
```

-	Layers:
	-	`sha256:874c4b424a680cfa6457999c0ce435d96b02cffc5203fa3f92b393d5811628a1`  
		Last Modified: Thu, 09 Oct 2025 01:59:58 GMT  
		Size: 1.3 MB (1268717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:586c45ea22dc49613e4d853a8c98ede4e76cc44653d06cf317710f979f305a99`  
		Last Modified: Thu, 09 Oct 2025 01:59:59 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine3.22`

```console
$ docker pull irssi@sha256:1e663ae10149c0b4d9df663b9da7bb650a58deea6cb49343c8191884eb0ec8ab
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

### `irssi:1.4-alpine3.22` - linux; amd64

```console
$ docker pull irssi@sha256:faf9e4f6be7260cc0682ec1445c6826e0bdcdc63f4a064eb8a981701bb709594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20173425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8798df3f4b34c7e6f52a3727072b2c410704453c6794f69663ce299680c47d3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e11827177f1c189b726b09341a9159227f1bfd85f6bfa5e738af089ccd47cc`  
		Last Modified: Wed, 08 Oct 2025 22:39:07 GMT  
		Size: 10.4 MB (10396003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6644b44e4c465f7087dbb97380180e75f01380c552303d8a2486f385aad34f35`  
		Last Modified: Wed, 08 Oct 2025 22:39:04 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b031546d04685e49a4d43b8482a34aaa0e6a3a6d75e947a09671aaf238e1ffc`  
		Last Modified: Wed, 08 Oct 2025 22:39:05 GMT  
		Size: 6.0 MB (5973981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:60dc002a8263e274525a471186038e9a631be6a5c61c1fd9e0ec2accade632f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be809ef2f20f547ecb812fc7251645454e581cc3d872627c003659069a74285e`

```dockerfile
```

-	Layers:
	-	`sha256:7def044fb5b5a27bb8a83fe2e1f6903b88c7090d91d03cc25c2be92d2b115084`  
		Last Modified: Thu, 09 Oct 2025 01:59:25 GMT  
		Size: 1.3 MB (1270668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09d745c2ae7ce01c7631e58d7cf581615e9c45ca2b8d31cccaa988c9e5257205`  
		Last Modified: Thu, 09 Oct 2025 01:59:26 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.22` - linux; arm variant v6

```console
$ docker pull irssi@sha256:8dfb08ad7779ab00246287f396771e855c5271e8e67f8fcb68229714505701e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18926923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e4ac8e569bab3223b4cbc8f2ffb5137d951b2efa8fbca448cdef1d3e4925de`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
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
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733b352b3151cd505887f05e68a9791f679acceebf79736c8050c72db1b5191a`  
		Last Modified: Wed, 08 Oct 2025 21:42:07 GMT  
		Size: 9.6 MB (9619615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8386f23106fb9eeab59f6f1e82d6fda32cd5130f7e9240952ab361424133835`  
		Last Modified: Wed, 08 Oct 2025 21:42:06 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5176e22c73a447407c118250d8b7084c947461ad88e0f8ffba848633ef457d1`  
		Last Modified: Wed, 08 Oct 2025 21:42:08 GMT  
		Size: 5.8 MB (5802239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:3529f2221a487a696afdfab5dd8793069c4e5153fdd0bbc77b1a10ed59976e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c402305c7b183a88a4427e0caf1314f408323bb659aab78e52073f5d4946a814`

```dockerfile
```

-	Layers:
	-	`sha256:40cb74de7dde3071930d2507974b11b96e2a2fcf0dd4cc4063ea7658469d44d0`  
		Last Modified: Wed, 08 Oct 2025 22:59:36 GMT  
		Size: 17.5 KB (17462 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.22` - linux; arm variant v7

```console
$ docker pull irssi@sha256:1c77198ac74e17d59093ac465b9d5cb18f5cf9b495d394dc7fe1757c6cd43c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18234853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81e381f20e12f748a613e6b9d046d4f23726de50b2d6209ee706e26cdc81cd9`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
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
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d355e9f8d23dd7df754d0fc9b69cb593d77843421e4fdc90e0999ac63d910671`  
		Last Modified: Wed, 08 Oct 2025 21:42:22 GMT  
		Size: 9.4 MB (9449582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d327d03f3716120871e15d8a53213e2201fb4c543cff4cfda89d44a362924f5b`  
		Last Modified: Wed, 08 Oct 2025 21:42:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a7bac72cbbe13e0d2ca93a7e2045c3cee7af4a9a99e4f4a137d438a669963e`  
		Last Modified: Wed, 08 Oct 2025 21:42:21 GMT  
		Size: 5.6 MB (5562729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:a538097b3d9e95fd66c681e163119ee4fda34648e1138be1471be07765e086b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1291403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121bd05d16ceb8c11139b6c2e140bdd3f2ff4d48d4eeae0c78b36653e7f2cb0a`

```dockerfile
```

-	Layers:
	-	`sha256:66532285c363d95627518c5ee59b11b1d8179d0e9a5459c633c0d02618fed06d`  
		Last Modified: Wed, 08 Oct 2025 22:59:39 GMT  
		Size: 1.3 MB (1273726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81f81d5bd314d48e57ad6439aa665accb301d8fa90cf9cfbc734e80cc3932d07`  
		Last Modified: Wed, 08 Oct 2025 22:59:40 GMT  
		Size: 17.7 KB (17677 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:6312b888a6893a7c5bcbfa3b983ab38749f99778b44a99530ef47a5fa8afe92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20344949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6748a647916da83e7b32a7fc1af7248d48c18b28e2c35d2403a1aeaba48783`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
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
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60d53dd86b6f70255a46f81ded3715200f2293ef56b5b5e4a9bd208fe73a5a4`  
		Last Modified: Wed, 08 Oct 2025 21:28:34 GMT  
		Size: 10.4 MB (10358145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f35b8acbeb2e8727c286447b6769cf3d016bb4864c5ad35e2e295e2f173749a`  
		Last Modified: Wed, 08 Oct 2025 21:28:33 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb455678cd1949819acffee4a71aa2ae7f91c1aae58a696c6666455cd9924e53`  
		Last Modified: Wed, 08 Oct 2025 21:28:35 GMT  
		Size: 5.8 MB (5847748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:816e238d7fee6ac073eb8bd4ed99e37a650f1d462c391ae4ae546450436b6e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f33b353f49dad9739f03717967b6ed81661089b4a5f7503a731715f3f4e1f5`

```dockerfile
```

-	Layers:
	-	`sha256:d1eb3ee699a52f4b20f4604d2e59b51c391ac02eb535317009268ef8a4fc45df`  
		Last Modified: Wed, 08 Oct 2025 22:59:44 GMT  
		Size: 1.3 MB (1270772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:309170da33d1e1e4b4a1a75c21c0120ff197fc0e4fb56a433d3097dd47cdb44b`  
		Last Modified: Wed, 08 Oct 2025 22:59:44 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.22` - linux; 386

```console
$ docker pull irssi@sha256:e66bdc96a17047cd31d803681e0c481fef6963c4d0120511222702e892610149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19616013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9546217ea8e23f6143afa741cd4e2050c708ad5ad67102826bac0bd4e68e070`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
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
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9ef0d9eddfed06ea09466e4f959f424bd4487ea48914b239e32d9a01ae664b`  
		Last Modified: Wed, 08 Oct 2025 21:14:07 GMT  
		Size: 9.9 MB (9940223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1546130b809d653b7ffb8056fabb7cde5c59816ee611d191515f665953378af9`  
		Last Modified: Wed, 08 Oct 2025 21:14:06 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05246638c115aace0ae244236cec9016bac4501e4699e0b5761e13d518f3aa7`  
		Last Modified: Wed, 08 Oct 2025 21:14:07 GMT  
		Size: 6.1 MB (6055871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:b12b29108acc7caee0ab23ab7c1191d2861b6bf4761b820569a0bb5519120cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a3cccb44b653f9d355429131978d3190d1b78b70f94e13b2cc06e9f7997a5e`

```dockerfile
```

-	Layers:
	-	`sha256:3ae7b6184d4abc32aca3718238c88832fa852fc8a1b082f050f7d291dfde1737`  
		Last Modified: Wed, 08 Oct 2025 22:59:48 GMT  
		Size: 1.3 MB (1270623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7720d5b50178fd0c79f8f0d50307c9837e7c9413280ecc69217fdc55705d6b3f`  
		Last Modified: Wed, 08 Oct 2025 22:59:49 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.22` - linux; ppc64le

```console
$ docker pull irssi@sha256:11ec21937e624e10112a9366a2e39f63804c250cd288519f31d38458aa0c9d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20560595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41dfe8eb30ae660e9f6b618bd8acba1eb372978247dff8685fcdb0393231e246`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
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
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48c17d61a4d1554d280ba28d7252c2f305090eeac61b357dd6b76bd73c43c63`  
		Last Modified: Thu, 09 Oct 2025 00:45:13 GMT  
		Size: 10.6 MB (10595397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26efea3de5b42df966c34855cef32948787b76acb851a4084e3e3ad212766f3`  
		Last Modified: Thu, 09 Oct 2025 00:45:11 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa99ddfbbb8375b453f006a945c8fa07c1ce170fda8448f7b653f0ac29d72c7b`  
		Last Modified: Thu, 09 Oct 2025 00:45:07 GMT  
		Size: 6.2 MB (6231972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:9c4cef9155fe22476444ceb17f379012b0c8b3e5e05a7c96919fa63eff2fdfe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179a2005edd691213f7786f101a4bd63364292c1882766e726e961190a7a7a47`

```dockerfile
```

-	Layers:
	-	`sha256:33a5c683cc42bda4a70c31f9d11afeffee44599ee508e945b64f8f0f007364b0`  
		Last Modified: Thu, 09 Oct 2025 01:59:38 GMT  
		Size: 1.3 MB (1268775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921ee5b46b5c6c2bdcc6f69f3de81a1779cddf19f1c547cb5807d97cd7e0429e`  
		Last Modified: Thu, 09 Oct 2025 01:59:39 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.22` - linux; riscv64

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

### `irssi:1.4-alpine3.22` - unknown; unknown

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

### `irssi:1.4-alpine3.22` - linux; s390x

```console
$ docker pull irssi@sha256:f3623b26ebb6e5ca70e89646c7b5dc3cc4923efff13fcf40e13603205b1d2c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20728269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4dc9af67d43ea3efb18b38b4dd936194a56cde8d7cedf49529c2085f844b996`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
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
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a35a93027b47a44ea544d9fee84d01ab7be35185d9c512211141ce9d358b9c`  
		Last Modified: Thu, 09 Oct 2025 00:42:42 GMT  
		Size: 11.0 MB (10953642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054cb0439f6b75b07dcf89d2ae109ef474c8c1ca0e6748b16768e98125bfadd4`  
		Last Modified: Thu, 09 Oct 2025 00:42:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1439f567e83e96d3eb1406d4ffb34da86c733b3fc27798542727ad6be641a537`  
		Last Modified: Thu, 09 Oct 2025 00:42:36 GMT  
		Size: 6.1 MB (6124398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:033679be33af045692166464cde309c06c55d1e3c2f0f70ff8f5a32a40c138cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3b68e4209308a841644a418b0f59ac60f7f2626e13c308ee01fa66528b5f4b`

```dockerfile
```

-	Layers:
	-	`sha256:874c4b424a680cfa6457999c0ce435d96b02cffc5203fa3f92b393d5811628a1`  
		Last Modified: Thu, 09 Oct 2025 01:59:58 GMT  
		Size: 1.3 MB (1268717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:586c45ea22dc49613e4d853a8c98ede4e76cc44653d06cf317710f979f305a99`  
		Last Modified: Thu, 09 Oct 2025 01:59:59 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-trixie`

```console
$ docker pull irssi@sha256:5cf9ab8c791c26cf2aa97983f1cc4debbebc4fb203bae59694fc0398575102d2
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
$ docker pull irssi@sha256:f62560d766eab4534167883aef43fa8fad47d829ff5c18467b86628e024bd9c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53870137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769552443b8c0b77660078238cebe5d212969cc1cef60189b3e988284170f129`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
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
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50e33926f10233e1cefedd2afc470ffdca1d03aae27f61804a5308859157ecd`  
		Last Modified: Tue, 21 Oct 2025 01:18:57 GMT  
		Size: 19.2 MB (19222452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5172862d08ce0c808ae6bd8643e68f924682e5145be1e8111d0b52f49a6fe9bc`  
		Last Modified: Tue, 21 Oct 2025 01:18:55 GMT  
		Size: 3.3 KB (3335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160b0c22ddb061ea4cd17f1ed3ca11aec9c1535fa615b47a6577d131dafc4ba3`  
		Last Modified: Tue, 21 Oct 2025 01:18:56 GMT  
		Size: 4.9 MB (4866394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:6eff9cda53aa1fce62b753cb7e75d79fbe1450f9fec0a77f0972a0a5c20df8d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4a3535c6261e33feac4e249dfb231f9d22a1d643b2b4a9b3d8f0a1ed8ff4dc`

```dockerfile
```

-	Layers:
	-	`sha256:984b3275ff964e7bbd701d8b5ca39a1b1abcd3f1bcf095ff7fea54585adab0a5`  
		Last Modified: Tue, 21 Oct 2025 10:59:26 GMT  
		Size: 5.6 MB (5588383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80576291496298d1465daebae79c9c7e21c694e8d2ab8ac5425ebf50e8de2192`  
		Last Modified: Tue, 21 Oct 2025 10:59:27 GMT  
		Size: 18.7 KB (18694 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:53bc4bdfbee3e6398af8cf776254a80b7ed67e7da2fe11c32d32d7abbe566dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50946604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea2d9d131f13dbc0476fa90cf34ad8697fe5db46e9a4c3807db7c7805165ed1`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 00:24:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:24:18 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 00:24:18 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 00:24:18 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 00:24:18 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 00:25:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 00:25:08 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 00:25:08 GMT
USER user
# Tue, 04 Nov 2025 00:25:08 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:453afc2258d7bc5729fed5672fb95bafa092e30a933b4377a12034be940a671b`  
		Last Modified: Tue, 04 Nov 2025 00:13:12 GMT  
		Size: 27.9 MB (27946438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56437b5f3c4f729d31fe7638873251d16b28c1c3d692a9956f5b69136d43e930`  
		Last Modified: Tue, 04 Nov 2025 00:25:28 GMT  
		Size: 18.3 MB (18287214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13428abf70cc1a9fb886bcdae90cfbe2d84d6f55745ed019971ee5ffd12cbc36`  
		Last Modified: Tue, 04 Nov 2025 00:25:27 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa255570f57e9797d70ef3d709d8bc0234a1d6314252033f6b60cde7930d539`  
		Last Modified: Tue, 04 Nov 2025 00:25:27 GMT  
		Size: 4.7 MB (4709590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:2cab70366a5eefad158f1357e7fbb0b830669bd73781291fc8f2f7c487e14ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe26f64be2cf34a6f1dbb907289e3ceedcd6e667a219c0df9ad5cccdd52607e1`

```dockerfile
```

-	Layers:
	-	`sha256:d6ab272cfb896c643aefbdbff6cc4a0edfb3a6ef0aff0c6564cc88a358010e7c`  
		Last Modified: Tue, 04 Nov 2025 08:59:27 GMT  
		Size: 5.6 MB (5585932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c8664e85e0ed44674cf84da06545a8bad6ddb201e7c9bdeffa2d711dc060c4`  
		Last Modified: Tue, 04 Nov 2025 08:59:28 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:ec7216e01ceba6748f58241dd44ef50c704fd9d0cbf6131634fd49a15f702256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48683586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb33d7b4c257421d912466ff540a8eab48db1957b1513f08e045342c3e09f7e`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
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
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec21711d4a258965a72caed76918b337c0aa5de6b91e590c06fc5e4745646f55`  
		Last Modified: Tue, 21 Oct 2025 01:21:40 GMT  
		Size: 17.9 MB (17908849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b844f9ec9159fe5dc1bceb0c829cf8fed6b324e19975cd9a3e797da3b9e7f32`  
		Last Modified: Tue, 21 Oct 2025 01:21:39 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8319989dae0a45f302eefb7eacf795675adb09faf457ef920f5f154d9e8fd6a`  
		Last Modified: Tue, 21 Oct 2025 01:21:40 GMT  
		Size: 4.6 MB (4558483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:1caf5b32a9cc375fdb8989c5e37fd5701d48a4ee13f33a1efb1c643b6656b614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1644fbc65e3d69b2d3bdd0d9e16c452b7d1c7156e981d44b810e54fb21f72726`

```dockerfile
```

-	Layers:
	-	`sha256:ef4ef36a4fd0ce15ccfe9d8c5c18fc16fafd0038ee0a805f0e2fbd3884993613`  
		Last Modified: Tue, 21 Oct 2025 07:59:30 GMT  
		Size: 5.6 MB (5588954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a879647ba458c48533bd9bc58dc4e49735e56b2b2509ed8842988ba5b86312e0`  
		Last Modified: Tue, 21 Oct 2025 07:59:31 GMT  
		Size: 18.8 KB (18832 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:77dfd1a59d7b77b123cca1beadf2971d1ba2ab34fdeeefeadce1a24e0f13126c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53976450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03efcec3d095c3aea650cc38e8beac272725967f1d9705561a88cc2cfabd06c7`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
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
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b408dc86163fc3064303c3d87a6f050d94d7e50026af6fec8d474bde261f9b`  
		Last Modified: Tue, 21 Oct 2025 01:19:20 GMT  
		Size: 19.0 MB (19049325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec261c2c31268433efbe285382be2e8e472bc1069f6f4703a8c3225b10ce0192`  
		Last Modified: Tue, 21 Oct 2025 01:19:18 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1acd4e881dacb1490ed68208dd4440fca46f3dc100f2a812bf12c1f676495e5`  
		Last Modified: Tue, 21 Oct 2025 01:19:19 GMT  
		Size: 4.8 MB (4781638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:2835026ba33a88cc6dd9fad1db6db1ec4ac24c190ed8d34348d3c797171fcabb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6636c1128d2fa3dcbaaa075ffd279fcdb2e092e8cd8f4acd4b4056e29c38c764`

```dockerfile
```

-	Layers:
	-	`sha256:71b8d4b308985e51f1304ef1f8d2a4365932f656bec2d21685a2b0333d5e3ccb`  
		Last Modified: Tue, 21 Oct 2025 07:59:54 GMT  
		Size: 5.6 MB (5594867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cda273518a593b1fdc06763d67c1ec3babffc7218cf0dfde047a1d3545ed65a0`  
		Last Modified: Tue, 21 Oct 2025 07:59:55 GMT  
		Size: 18.9 KB (18876 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; 386

```console
$ docker pull irssi@sha256:906a0c6f51c0b1f3b4ecb3f2e1c968d3704a25c07977646ef27d94b4b52f843b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54906871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f15a626e6515729d1e92c4029f7fd5ad811e6b1fa57491b31c1375bfd151edd`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
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
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a10221caffdcbfa0e53f49b1c8340c488768b10a5ea331304fe42934a151e92`  
		Last Modified: Tue, 21 Oct 2025 01:19:19 GMT  
		Size: 18.7 MB (18740674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99453861535e7430a13e074b1001d31ea1b6113f5f26cbd98c4898b8f5248b1`  
		Last Modified: Tue, 21 Oct 2025 01:19:17 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2532aeb1762cf3e40be739eca77e4a75e1fe38161883765d09f93de9e8e2da0e`  
		Last Modified: Tue, 21 Oct 2025 01:19:17 GMT  
		Size: 4.9 MB (4868206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:7da87f53975d8a9812601bfebe2d8b85bb1ddace02345349599eb31d26603b89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b166c953777c8cc44a6f84ea8cf0efae3b040be490d0e4cf0af5fc12b2fffe`

```dockerfile
```

-	Layers:
	-	`sha256:0d1c17737f2969710a690596ea60539faa8669ce29c2cdb5aea0ab822518a718`  
		Last Modified: Tue, 21 Oct 2025 10:59:42 GMT  
		Size: 5.6 MB (5584506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cf1c8a6fed6cbd711442dee178708058badce283771d0b8d81faae2d7964c89`  
		Last Modified: Tue, 21 Oct 2025 10:59:43 GMT  
		Size: 18.6 KB (18638 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:a084063aa561239245a691754b6dc2d671df6ef0560db4211c54b612f3e7ea15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58241580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f34336095685fcdececa53b502c6d01e505509b56e53158c6db1a854159927`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:40:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:40:10 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 01:40:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 01:40:10 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 01:40:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 01:41:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 01:41:53 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 01:41:53 GMT
USER user
# Tue, 04 Nov 2025 01:41:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87028ebfcd452692a3fb8d88c28f9dcaefbb732091f6921899481be54ff4c14a`  
		Last Modified: Tue, 04 Nov 2025 01:42:34 GMT  
		Size: 19.5 MB (19542341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4394dbe86dcc81b464d6e1d783cd35d455809fc85f44e42d150f96559d485a41`  
		Last Modified: Tue, 04 Nov 2025 01:42:28 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf7c6c4c0df971675464c86be67bdab3c2c25b38b37e01da482c5cb66037d0d`  
		Last Modified: Tue, 04 Nov 2025 01:42:30 GMT  
		Size: 5.1 MB (5097230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:f4763863a1b427e12438c44a011d6f057521086ff7d6d3089a8b1548112e00dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5919bc5740e214ee4b9780aee2c1ad773d2cb3193a47296199d9dd43b538349`

```dockerfile
```

-	Layers:
	-	`sha256:3c8efade8711469af7719f447e79a6a55a49965364fecba525c872e2c2c39f54`  
		Last Modified: Tue, 04 Nov 2025 08:59:43 GMT  
		Size: 5.6 MB (5595414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73fb47554826c5ea1fd080726318e56e507fb096dbdab60c4c068e35d1748a83`  
		Last Modified: Tue, 04 Nov 2025 08:59:43 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:ad6bd3a5205e24902df7636515066e77cd40386afc556802ffb26f1c77e0e0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51688796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af58c0755eac6d8da52a1a1e0818d9a970afed3f79411b1e29c974e03693f77c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 03:21:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:21:31 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 03:21:31 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 03:21:31 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 03:21:31 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 03:28:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 03:28:16 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 03:28:16 GMT
USER user
# Tue, 04 Nov 2025 03:28:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd582df31684b74a9fa351a3f7a398aaac1fcbdf5dbaa85b5372c8462d7c2f4`  
		Last Modified: Tue, 04 Nov 2025 03:30:29 GMT  
		Size: 18.5 MB (18549071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbc8e452a4bcbb01a4646ec80e76632da072b403d910c0cb470f33071b26713`  
		Last Modified: Tue, 04 Nov 2025 03:30:26 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339fd9308e80cf2bb6fbb2002e6caf32c46d806077d562abd9e9697cb185d246`  
		Last Modified: Tue, 04 Nov 2025 03:30:27 GMT  
		Size: 4.9 MB (4860578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:386968c0f2cc63a525d899d89b5efea2a6c8fb70db205e6fa72353d875d5a0ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6597a75bc6701428d03667f7d6c7f70c99d7b60e95a8d1fdb08d4b3ad6afec`

```dockerfile
```

-	Layers:
	-	`sha256:dc7fd9c40909a5578f92745efde764baa371271f42768e30f606d02bd12b7e43`  
		Last Modified: Tue, 04 Nov 2025 05:59:53 GMT  
		Size: 5.6 MB (5579686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2613fe6d4ed13c302d41cf48b4f8409a1d5bbf2c78e18ebcfa865a7ff55fc8a9`  
		Last Modified: Tue, 04 Nov 2025 05:59:54 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; s390x

```console
$ docker pull irssi@sha256:3a50bacd0aeaff8b8bb33a64478b835190ffccaa1513205554f7ee1f6a184193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54506755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a48d7420330e0856941ae3d5e153f27daff93349a4fa18e370e1742cb7f711`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 06:57:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 06:57:24 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 06:57:24 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 06:57:24 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 06:57:24 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 06:57:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 06:57:59 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 06:57:59 GMT
USER user
# Tue, 04 Nov 2025 06:57:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033854155955c69f5e80286c0220fcbce49683f27ff99d1e3003af7fcaf6c877`  
		Last Modified: Tue, 04 Nov 2025 06:58:21 GMT  
		Size: 19.8 MB (19760115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c247a95f4cb0054a4d91356e28a34cd9e78b4cd6a91641cb206c20a4432358`  
		Last Modified: Tue, 04 Nov 2025 06:58:20 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c870c8580f75359f105944243814e2056231525934f2762d516037ba84460b`  
		Last Modified: Tue, 04 Nov 2025 06:58:21 GMT  
		Size: 4.9 MB (4905887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:67067471ee97249a779cc6457e15b62dcd86599b15c73cb35fe07d4ee9d9bc15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb77a7d993b8fd0d0709a3f5d273dca60cf5a00b2a1843faf52e53880c2147e9`

```dockerfile
```

-	Layers:
	-	`sha256:6fabbd9421ca04d0605ccb6b593319d76d9eeb706da0f60a92f293e472d49d62`  
		Last Modified: Tue, 04 Nov 2025 09:00:17 GMT  
		Size: 5.6 MB (5589288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcd0465106c749fc617ea8887ce197ef6acc786e35587fff1f92baafdcc874fc`  
		Last Modified: Tue, 04 Nov 2025 09:00:18 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5`

```console
$ docker pull irssi@sha256:b59a4c12644a0027378d6b7fc6fdb8933cc3eb9cf106e0952aee8798d91b182e
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
$ docker pull irssi@sha256:f553b587fa2fcc5d841159dae68ae5bf4fa4d3c004d4d41242dc5313d4846fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53869909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6b3f77c651ad0f798e6d156e86951a9c95ee5d69267226def79404119d3ddc`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:05:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:05:17 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 04:05:17 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 04:05:17 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 04:05:17 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 04:05:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 04:05:53 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 04:05:53 GMT
USER user
# Tue, 04 Nov 2025 04:05:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b0149746e47a3ae7dee7e39c040588240de613548f17fe0a058de2c1fc9261`  
		Last Modified: Tue, 04 Nov 2025 04:06:12 GMT  
		Size: 19.2 MB (19221929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e10c64e7837e1354d0490b74de7c2c3e98fc0c725da960fbded84b74970342`  
		Last Modified: Tue, 04 Nov 2025 04:06:09 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119f0b70c0bf9309cf82be23770dfc5801e9ef27c65481131ca9363d15c89931`  
		Last Modified: Tue, 04 Nov 2025 04:06:09 GMT  
		Size: 4.9 MB (4866514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:6b140b015d97f19b567cc8a1a2761d84a722bee7b30026905ae95f53561b9dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc93d52e86204f02c704594c0e6e1fad2032358d3d0ba201fc97399b5e3b1c18`

```dockerfile
```

-	Layers:
	-	`sha256:8dd46d6af558746cf8ebd456f3223832a8b27e755e65d95b16b4e1a65c31339b`  
		Last Modified: Tue, 04 Nov 2025 08:59:45 GMT  
		Size: 5.6 MB (5588383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abee79486a69ff2a04d7a50f938463a4fc51734d6565f7e6b1812dbaa04897a5`  
		Last Modified: Tue, 04 Nov 2025 08:59:46 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v5

```console
$ docker pull irssi@sha256:53bc4bdfbee3e6398af8cf776254a80b7ed67e7da2fe11c32d32d7abbe566dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50946604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea2d9d131f13dbc0476fa90cf34ad8697fe5db46e9a4c3807db7c7805165ed1`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 00:24:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:24:18 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 00:24:18 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 00:24:18 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 00:24:18 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 00:25:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 00:25:08 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 00:25:08 GMT
USER user
# Tue, 04 Nov 2025 00:25:08 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:453afc2258d7bc5729fed5672fb95bafa092e30a933b4377a12034be940a671b`  
		Last Modified: Tue, 04 Nov 2025 00:13:12 GMT  
		Size: 27.9 MB (27946438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56437b5f3c4f729d31fe7638873251d16b28c1c3d692a9956f5b69136d43e930`  
		Last Modified: Tue, 04 Nov 2025 00:25:28 GMT  
		Size: 18.3 MB (18287214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13428abf70cc1a9fb886bcdae90cfbe2d84d6f55745ed019971ee5ffd12cbc36`  
		Last Modified: Tue, 04 Nov 2025 00:25:27 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa255570f57e9797d70ef3d709d8bc0234a1d6314252033f6b60cde7930d539`  
		Last Modified: Tue, 04 Nov 2025 00:25:27 GMT  
		Size: 4.7 MB (4709590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:2cab70366a5eefad158f1357e7fbb0b830669bd73781291fc8f2f7c487e14ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe26f64be2cf34a6f1dbb907289e3ceedcd6e667a219c0df9ad5cccdd52607e1`

```dockerfile
```

-	Layers:
	-	`sha256:d6ab272cfb896c643aefbdbff6cc4a0edfb3a6ef0aff0c6564cc88a358010e7c`  
		Last Modified: Tue, 04 Nov 2025 08:59:27 GMT  
		Size: 5.6 MB (5585932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c8664e85e0ed44674cf84da06545a8bad6ddb201e7c9bdeffa2d711dc060c4`  
		Last Modified: Tue, 04 Nov 2025 08:59:28 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v7

```console
$ docker pull irssi@sha256:ec7216e01ceba6748f58241dd44ef50c704fd9d0cbf6131634fd49a15f702256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48683586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb33d7b4c257421d912466ff540a8eab48db1957b1513f08e045342c3e09f7e`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
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
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec21711d4a258965a72caed76918b337c0aa5de6b91e590c06fc5e4745646f55`  
		Last Modified: Tue, 21 Oct 2025 01:21:40 GMT  
		Size: 17.9 MB (17908849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b844f9ec9159fe5dc1bceb0c829cf8fed6b324e19975cd9a3e797da3b9e7f32`  
		Last Modified: Tue, 21 Oct 2025 01:21:39 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8319989dae0a45f302eefb7eacf795675adb09faf457ef920f5f154d9e8fd6a`  
		Last Modified: Tue, 21 Oct 2025 01:21:40 GMT  
		Size: 4.6 MB (4558483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:1caf5b32a9cc375fdb8989c5e37fd5701d48a4ee13f33a1efb1c643b6656b614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1644fbc65e3d69b2d3bdd0d9e16c452b7d1c7156e981d44b810e54fb21f72726`

```dockerfile
```

-	Layers:
	-	`sha256:ef4ef36a4fd0ce15ccfe9d8c5c18fc16fafd0038ee0a805f0e2fbd3884993613`  
		Last Modified: Tue, 21 Oct 2025 07:59:30 GMT  
		Size: 5.6 MB (5588954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a879647ba458c48533bd9bc58dc4e49735e56b2b2509ed8842988ba5b86312e0`  
		Last Modified: Tue, 21 Oct 2025 07:59:31 GMT  
		Size: 18.8 KB (18832 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:77dfd1a59d7b77b123cca1beadf2971d1ba2ab34fdeeefeadce1a24e0f13126c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53976450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03efcec3d095c3aea650cc38e8beac272725967f1d9705561a88cc2cfabd06c7`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
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
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b408dc86163fc3064303c3d87a6f050d94d7e50026af6fec8d474bde261f9b`  
		Last Modified: Tue, 21 Oct 2025 01:19:20 GMT  
		Size: 19.0 MB (19049325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec261c2c31268433efbe285382be2e8e472bc1069f6f4703a8c3225b10ce0192`  
		Last Modified: Tue, 21 Oct 2025 01:19:18 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1acd4e881dacb1490ed68208dd4440fca46f3dc100f2a812bf12c1f676495e5`  
		Last Modified: Tue, 21 Oct 2025 01:19:19 GMT  
		Size: 4.8 MB (4781638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:2835026ba33a88cc6dd9fad1db6db1ec4ac24c190ed8d34348d3c797171fcabb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6636c1128d2fa3dcbaaa075ffd279fcdb2e092e8cd8f4acd4b4056e29c38c764`

```dockerfile
```

-	Layers:
	-	`sha256:71b8d4b308985e51f1304ef1f8d2a4365932f656bec2d21685a2b0333d5e3ccb`  
		Last Modified: Tue, 21 Oct 2025 07:59:54 GMT  
		Size: 5.6 MB (5594867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cda273518a593b1fdc06763d67c1ec3babffc7218cf0dfde047a1d3545ed65a0`  
		Last Modified: Tue, 21 Oct 2025 07:59:55 GMT  
		Size: 18.9 KB (18876 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; 386

```console
$ docker pull irssi@sha256:906a0c6f51c0b1f3b4ecb3f2e1c968d3704a25c07977646ef27d94b4b52f843b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54906871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f15a626e6515729d1e92c4029f7fd5ad811e6b1fa57491b31c1375bfd151edd`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
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
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a10221caffdcbfa0e53f49b1c8340c488768b10a5ea331304fe42934a151e92`  
		Last Modified: Tue, 21 Oct 2025 01:19:19 GMT  
		Size: 18.7 MB (18740674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99453861535e7430a13e074b1001d31ea1b6113f5f26cbd98c4898b8f5248b1`  
		Last Modified: Tue, 21 Oct 2025 01:19:17 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2532aeb1762cf3e40be739eca77e4a75e1fe38161883765d09f93de9e8e2da0e`  
		Last Modified: Tue, 21 Oct 2025 01:19:17 GMT  
		Size: 4.9 MB (4868206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:7da87f53975d8a9812601bfebe2d8b85bb1ddace02345349599eb31d26603b89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b166c953777c8cc44a6f84ea8cf0efae3b040be490d0e4cf0af5fc12b2fffe`

```dockerfile
```

-	Layers:
	-	`sha256:0d1c17737f2969710a690596ea60539faa8669ce29c2cdb5aea0ab822518a718`  
		Last Modified: Tue, 21 Oct 2025 10:59:42 GMT  
		Size: 5.6 MB (5584506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cf1c8a6fed6cbd711442dee178708058badce283771d0b8d81faae2d7964c89`  
		Last Modified: Tue, 21 Oct 2025 10:59:43 GMT  
		Size: 18.6 KB (18638 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; ppc64le

```console
$ docker pull irssi@sha256:a084063aa561239245a691754b6dc2d671df6ef0560db4211c54b612f3e7ea15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58241580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f34336095685fcdececa53b502c6d01e505509b56e53158c6db1a854159927`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:40:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:40:10 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 01:40:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 01:40:10 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 01:40:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 01:41:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 01:41:53 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 01:41:53 GMT
USER user
# Tue, 04 Nov 2025 01:41:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87028ebfcd452692a3fb8d88c28f9dcaefbb732091f6921899481be54ff4c14a`  
		Last Modified: Tue, 04 Nov 2025 01:42:34 GMT  
		Size: 19.5 MB (19542341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4394dbe86dcc81b464d6e1d783cd35d455809fc85f44e42d150f96559d485a41`  
		Last Modified: Tue, 04 Nov 2025 01:42:28 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf7c6c4c0df971675464c86be67bdab3c2c25b38b37e01da482c5cb66037d0d`  
		Last Modified: Tue, 04 Nov 2025 01:42:30 GMT  
		Size: 5.1 MB (5097230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:f4763863a1b427e12438c44a011d6f057521086ff7d6d3089a8b1548112e00dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5919bc5740e214ee4b9780aee2c1ad773d2cb3193a47296199d9dd43b538349`

```dockerfile
```

-	Layers:
	-	`sha256:3c8efade8711469af7719f447e79a6a55a49965364fecba525c872e2c2c39f54`  
		Last Modified: Tue, 04 Nov 2025 08:59:43 GMT  
		Size: 5.6 MB (5595414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73fb47554826c5ea1fd080726318e56e507fb096dbdab60c4c068e35d1748a83`  
		Last Modified: Tue, 04 Nov 2025 08:59:43 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; riscv64

```console
$ docker pull irssi@sha256:ad6bd3a5205e24902df7636515066e77cd40386afc556802ffb26f1c77e0e0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51688796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af58c0755eac6d8da52a1a1e0818d9a970afed3f79411b1e29c974e03693f77c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 03:21:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:21:31 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 03:21:31 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 03:21:31 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 03:21:31 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 03:28:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 03:28:16 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 03:28:16 GMT
USER user
# Tue, 04 Nov 2025 03:28:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd582df31684b74a9fa351a3f7a398aaac1fcbdf5dbaa85b5372c8462d7c2f4`  
		Last Modified: Tue, 04 Nov 2025 03:30:29 GMT  
		Size: 18.5 MB (18549071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbc8e452a4bcbb01a4646ec80e76632da072b403d910c0cb470f33071b26713`  
		Last Modified: Tue, 04 Nov 2025 03:30:26 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339fd9308e80cf2bb6fbb2002e6caf32c46d806077d562abd9e9697cb185d246`  
		Last Modified: Tue, 04 Nov 2025 03:30:27 GMT  
		Size: 4.9 MB (4860578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:386968c0f2cc63a525d899d89b5efea2a6c8fb70db205e6fa72353d875d5a0ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6597a75bc6701428d03667f7d6c7f70c99d7b60e95a8d1fdb08d4b3ad6afec`

```dockerfile
```

-	Layers:
	-	`sha256:dc7fd9c40909a5578f92745efde764baa371271f42768e30f606d02bd12b7e43`  
		Last Modified: Tue, 04 Nov 2025 05:59:53 GMT  
		Size: 5.6 MB (5579686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2613fe6d4ed13c302d41cf48b4f8409a1d5bbf2c78e18ebcfa865a7ff55fc8a9`  
		Last Modified: Tue, 04 Nov 2025 05:59:54 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; s390x

```console
$ docker pull irssi@sha256:3a50bacd0aeaff8b8bb33a64478b835190ffccaa1513205554f7ee1f6a184193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54506755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a48d7420330e0856941ae3d5e153f27daff93349a4fa18e370e1742cb7f711`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 06:57:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 06:57:24 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 06:57:24 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 06:57:24 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 06:57:24 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 06:57:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 06:57:59 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 06:57:59 GMT
USER user
# Tue, 04 Nov 2025 06:57:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033854155955c69f5e80286c0220fcbce49683f27ff99d1e3003af7fcaf6c877`  
		Last Modified: Tue, 04 Nov 2025 06:58:21 GMT  
		Size: 19.8 MB (19760115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c247a95f4cb0054a4d91356e28a34cd9e78b4cd6a91641cb206c20a4432358`  
		Last Modified: Tue, 04 Nov 2025 06:58:20 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c870c8580f75359f105944243814e2056231525934f2762d516037ba84460b`  
		Last Modified: Tue, 04 Nov 2025 06:58:21 GMT  
		Size: 4.9 MB (4905887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:67067471ee97249a779cc6457e15b62dcd86599b15c73cb35fe07d4ee9d9bc15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb77a7d993b8fd0d0709a3f5d273dca60cf5a00b2a1843faf52e53880c2147e9`

```dockerfile
```

-	Layers:
	-	`sha256:6fabbd9421ca04d0605ccb6b593319d76d9eeb706da0f60a92f293e472d49d62`  
		Last Modified: Tue, 04 Nov 2025 09:00:17 GMT  
		Size: 5.6 MB (5589288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcd0465106c749fc617ea8887ce197ef6acc786e35587fff1f92baafdcc874fc`  
		Last Modified: Tue, 04 Nov 2025 09:00:18 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine`

```console
$ docker pull irssi@sha256:1e663ae10149c0b4d9df663b9da7bb650a58deea6cb49343c8191884eb0ec8ab
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
$ docker pull irssi@sha256:faf9e4f6be7260cc0682ec1445c6826e0bdcdc63f4a064eb8a981701bb709594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20173425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8798df3f4b34c7e6f52a3727072b2c410704453c6794f69663ce299680c47d3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e11827177f1c189b726b09341a9159227f1bfd85f6bfa5e738af089ccd47cc`  
		Last Modified: Wed, 08 Oct 2025 22:39:07 GMT  
		Size: 10.4 MB (10396003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6644b44e4c465f7087dbb97380180e75f01380c552303d8a2486f385aad34f35`  
		Last Modified: Wed, 08 Oct 2025 22:39:04 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b031546d04685e49a4d43b8482a34aaa0e6a3a6d75e947a09671aaf238e1ffc`  
		Last Modified: Wed, 08 Oct 2025 22:39:05 GMT  
		Size: 6.0 MB (5973981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:60dc002a8263e274525a471186038e9a631be6a5c61c1fd9e0ec2accade632f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be809ef2f20f547ecb812fc7251645454e581cc3d872627c003659069a74285e`

```dockerfile
```

-	Layers:
	-	`sha256:7def044fb5b5a27bb8a83fe2e1f6903b88c7090d91d03cc25c2be92d2b115084`  
		Last Modified: Thu, 09 Oct 2025 01:59:25 GMT  
		Size: 1.3 MB (1270668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09d745c2ae7ce01c7631e58d7cf581615e9c45ca2b8d31cccaa988c9e5257205`  
		Last Modified: Thu, 09 Oct 2025 01:59:26 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:8dfb08ad7779ab00246287f396771e855c5271e8e67f8fcb68229714505701e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18926923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e4ac8e569bab3223b4cbc8f2ffb5137d951b2efa8fbca448cdef1d3e4925de`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
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
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733b352b3151cd505887f05e68a9791f679acceebf79736c8050c72db1b5191a`  
		Last Modified: Wed, 08 Oct 2025 21:42:07 GMT  
		Size: 9.6 MB (9619615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8386f23106fb9eeab59f6f1e82d6fda32cd5130f7e9240952ab361424133835`  
		Last Modified: Wed, 08 Oct 2025 21:42:06 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5176e22c73a447407c118250d8b7084c947461ad88e0f8ffba848633ef457d1`  
		Last Modified: Wed, 08 Oct 2025 21:42:08 GMT  
		Size: 5.8 MB (5802239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:3529f2221a487a696afdfab5dd8793069c4e5153fdd0bbc77b1a10ed59976e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c402305c7b183a88a4427e0caf1314f408323bb659aab78e52073f5d4946a814`

```dockerfile
```

-	Layers:
	-	`sha256:40cb74de7dde3071930d2507974b11b96e2a2fcf0dd4cc4063ea7658469d44d0`  
		Last Modified: Wed, 08 Oct 2025 22:59:36 GMT  
		Size: 17.5 KB (17462 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:1c77198ac74e17d59093ac465b9d5cb18f5cf9b495d394dc7fe1757c6cd43c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18234853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81e381f20e12f748a613e6b9d046d4f23726de50b2d6209ee706e26cdc81cd9`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
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
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d355e9f8d23dd7df754d0fc9b69cb593d77843421e4fdc90e0999ac63d910671`  
		Last Modified: Wed, 08 Oct 2025 21:42:22 GMT  
		Size: 9.4 MB (9449582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d327d03f3716120871e15d8a53213e2201fb4c543cff4cfda89d44a362924f5b`  
		Last Modified: Wed, 08 Oct 2025 21:42:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a7bac72cbbe13e0d2ca93a7e2045c3cee7af4a9a99e4f4a137d438a669963e`  
		Last Modified: Wed, 08 Oct 2025 21:42:21 GMT  
		Size: 5.6 MB (5562729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:a538097b3d9e95fd66c681e163119ee4fda34648e1138be1471be07765e086b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1291403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121bd05d16ceb8c11139b6c2e140bdd3f2ff4d48d4eeae0c78b36653e7f2cb0a`

```dockerfile
```

-	Layers:
	-	`sha256:66532285c363d95627518c5ee59b11b1d8179d0e9a5459c633c0d02618fed06d`  
		Last Modified: Wed, 08 Oct 2025 22:59:39 GMT  
		Size: 1.3 MB (1273726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81f81d5bd314d48e57ad6439aa665accb301d8fa90cf9cfbc734e80cc3932d07`  
		Last Modified: Wed, 08 Oct 2025 22:59:40 GMT  
		Size: 17.7 KB (17677 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:6312b888a6893a7c5bcbfa3b983ab38749f99778b44a99530ef47a5fa8afe92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20344949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6748a647916da83e7b32a7fc1af7248d48c18b28e2c35d2403a1aeaba48783`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
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
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60d53dd86b6f70255a46f81ded3715200f2293ef56b5b5e4a9bd208fe73a5a4`  
		Last Modified: Wed, 08 Oct 2025 21:28:34 GMT  
		Size: 10.4 MB (10358145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f35b8acbeb2e8727c286447b6769cf3d016bb4864c5ad35e2e295e2f173749a`  
		Last Modified: Wed, 08 Oct 2025 21:28:33 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb455678cd1949819acffee4a71aa2ae7f91c1aae58a696c6666455cd9924e53`  
		Last Modified: Wed, 08 Oct 2025 21:28:35 GMT  
		Size: 5.8 MB (5847748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:816e238d7fee6ac073eb8bd4ed99e37a650f1d462c391ae4ae546450436b6e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f33b353f49dad9739f03717967b6ed81661089b4a5f7503a731715f3f4e1f5`

```dockerfile
```

-	Layers:
	-	`sha256:d1eb3ee699a52f4b20f4604d2e59b51c391ac02eb535317009268ef8a4fc45df`  
		Last Modified: Wed, 08 Oct 2025 22:59:44 GMT  
		Size: 1.3 MB (1270772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:309170da33d1e1e4b4a1a75c21c0120ff197fc0e4fb56a433d3097dd47cdb44b`  
		Last Modified: Wed, 08 Oct 2025 22:59:44 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; 386

```console
$ docker pull irssi@sha256:e66bdc96a17047cd31d803681e0c481fef6963c4d0120511222702e892610149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19616013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9546217ea8e23f6143afa741cd4e2050c708ad5ad67102826bac0bd4e68e070`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
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
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9ef0d9eddfed06ea09466e4f959f424bd4487ea48914b239e32d9a01ae664b`  
		Last Modified: Wed, 08 Oct 2025 21:14:07 GMT  
		Size: 9.9 MB (9940223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1546130b809d653b7ffb8056fabb7cde5c59816ee611d191515f665953378af9`  
		Last Modified: Wed, 08 Oct 2025 21:14:06 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05246638c115aace0ae244236cec9016bac4501e4699e0b5761e13d518f3aa7`  
		Last Modified: Wed, 08 Oct 2025 21:14:07 GMT  
		Size: 6.1 MB (6055871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:b12b29108acc7caee0ab23ab7c1191d2861b6bf4761b820569a0bb5519120cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a3cccb44b653f9d355429131978d3190d1b78b70f94e13b2cc06e9f7997a5e`

```dockerfile
```

-	Layers:
	-	`sha256:3ae7b6184d4abc32aca3718238c88832fa852fc8a1b082f050f7d291dfde1737`  
		Last Modified: Wed, 08 Oct 2025 22:59:48 GMT  
		Size: 1.3 MB (1270623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7720d5b50178fd0c79f8f0d50307c9837e7c9413280ecc69217fdc55705d6b3f`  
		Last Modified: Wed, 08 Oct 2025 22:59:49 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:11ec21937e624e10112a9366a2e39f63804c250cd288519f31d38458aa0c9d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20560595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41dfe8eb30ae660e9f6b618bd8acba1eb372978247dff8685fcdb0393231e246`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
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
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48c17d61a4d1554d280ba28d7252c2f305090eeac61b357dd6b76bd73c43c63`  
		Last Modified: Thu, 09 Oct 2025 00:45:13 GMT  
		Size: 10.6 MB (10595397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26efea3de5b42df966c34855cef32948787b76acb851a4084e3e3ad212766f3`  
		Last Modified: Thu, 09 Oct 2025 00:45:11 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa99ddfbbb8375b453f006a945c8fa07c1ce170fda8448f7b653f0ac29d72c7b`  
		Last Modified: Thu, 09 Oct 2025 00:45:07 GMT  
		Size: 6.2 MB (6231972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:9c4cef9155fe22476444ceb17f379012b0c8b3e5e05a7c96919fa63eff2fdfe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179a2005edd691213f7786f101a4bd63364292c1882766e726e961190a7a7a47`

```dockerfile
```

-	Layers:
	-	`sha256:33a5c683cc42bda4a70c31f9d11afeffee44599ee508e945b64f8f0f007364b0`  
		Last Modified: Thu, 09 Oct 2025 01:59:38 GMT  
		Size: 1.3 MB (1268775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921ee5b46b5c6c2bdcc6f69f3de81a1779cddf19f1c547cb5807d97cd7e0429e`  
		Last Modified: Thu, 09 Oct 2025 01:59:39 GMT  
		Size: 17.6 KB (17615 bytes)  
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
$ docker pull irssi@sha256:f3623b26ebb6e5ca70e89646c7b5dc3cc4923efff13fcf40e13603205b1d2c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20728269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4dc9af67d43ea3efb18b38b4dd936194a56cde8d7cedf49529c2085f844b996`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
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
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a35a93027b47a44ea544d9fee84d01ab7be35185d9c512211141ce9d358b9c`  
		Last Modified: Thu, 09 Oct 2025 00:42:42 GMT  
		Size: 11.0 MB (10953642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054cb0439f6b75b07dcf89d2ae109ef474c8c1ca0e6748b16768e98125bfadd4`  
		Last Modified: Thu, 09 Oct 2025 00:42:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1439f567e83e96d3eb1406d4ffb34da86c733b3fc27798542727ad6be641a537`  
		Last Modified: Thu, 09 Oct 2025 00:42:36 GMT  
		Size: 6.1 MB (6124398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:033679be33af045692166464cde309c06c55d1e3c2f0f70ff8f5a32a40c138cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3b68e4209308a841644a418b0f59ac60f7f2626e13c308ee01fa66528b5f4b`

```dockerfile
```

-	Layers:
	-	`sha256:874c4b424a680cfa6457999c0ce435d96b02cffc5203fa3f92b393d5811628a1`  
		Last Modified: Thu, 09 Oct 2025 01:59:58 GMT  
		Size: 1.3 MB (1268717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:586c45ea22dc49613e4d853a8c98ede4e76cc44653d06cf317710f979f305a99`  
		Last Modified: Thu, 09 Oct 2025 01:59:59 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine3.22`

```console
$ docker pull irssi@sha256:1e663ae10149c0b4d9df663b9da7bb650a58deea6cb49343c8191884eb0ec8ab
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

### `irssi:1.4.5-alpine3.22` - linux; amd64

```console
$ docker pull irssi@sha256:faf9e4f6be7260cc0682ec1445c6826e0bdcdc63f4a064eb8a981701bb709594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20173425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8798df3f4b34c7e6f52a3727072b2c410704453c6794f69663ce299680c47d3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e11827177f1c189b726b09341a9159227f1bfd85f6bfa5e738af089ccd47cc`  
		Last Modified: Wed, 08 Oct 2025 22:39:07 GMT  
		Size: 10.4 MB (10396003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6644b44e4c465f7087dbb97380180e75f01380c552303d8a2486f385aad34f35`  
		Last Modified: Wed, 08 Oct 2025 22:39:04 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b031546d04685e49a4d43b8482a34aaa0e6a3a6d75e947a09671aaf238e1ffc`  
		Last Modified: Wed, 08 Oct 2025 22:39:05 GMT  
		Size: 6.0 MB (5973981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:60dc002a8263e274525a471186038e9a631be6a5c61c1fd9e0ec2accade632f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be809ef2f20f547ecb812fc7251645454e581cc3d872627c003659069a74285e`

```dockerfile
```

-	Layers:
	-	`sha256:7def044fb5b5a27bb8a83fe2e1f6903b88c7090d91d03cc25c2be92d2b115084`  
		Last Modified: Thu, 09 Oct 2025 01:59:25 GMT  
		Size: 1.3 MB (1270668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09d745c2ae7ce01c7631e58d7cf581615e9c45ca2b8d31cccaa988c9e5257205`  
		Last Modified: Thu, 09 Oct 2025 01:59:26 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.22` - linux; arm variant v6

```console
$ docker pull irssi@sha256:8dfb08ad7779ab00246287f396771e855c5271e8e67f8fcb68229714505701e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18926923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e4ac8e569bab3223b4cbc8f2ffb5137d951b2efa8fbca448cdef1d3e4925de`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
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
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733b352b3151cd505887f05e68a9791f679acceebf79736c8050c72db1b5191a`  
		Last Modified: Wed, 08 Oct 2025 21:42:07 GMT  
		Size: 9.6 MB (9619615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8386f23106fb9eeab59f6f1e82d6fda32cd5130f7e9240952ab361424133835`  
		Last Modified: Wed, 08 Oct 2025 21:42:06 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5176e22c73a447407c118250d8b7084c947461ad88e0f8ffba848633ef457d1`  
		Last Modified: Wed, 08 Oct 2025 21:42:08 GMT  
		Size: 5.8 MB (5802239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:3529f2221a487a696afdfab5dd8793069c4e5153fdd0bbc77b1a10ed59976e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c402305c7b183a88a4427e0caf1314f408323bb659aab78e52073f5d4946a814`

```dockerfile
```

-	Layers:
	-	`sha256:40cb74de7dde3071930d2507974b11b96e2a2fcf0dd4cc4063ea7658469d44d0`  
		Last Modified: Wed, 08 Oct 2025 22:59:36 GMT  
		Size: 17.5 KB (17462 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.22` - linux; arm variant v7

```console
$ docker pull irssi@sha256:1c77198ac74e17d59093ac465b9d5cb18f5cf9b495d394dc7fe1757c6cd43c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18234853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81e381f20e12f748a613e6b9d046d4f23726de50b2d6209ee706e26cdc81cd9`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
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
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d355e9f8d23dd7df754d0fc9b69cb593d77843421e4fdc90e0999ac63d910671`  
		Last Modified: Wed, 08 Oct 2025 21:42:22 GMT  
		Size: 9.4 MB (9449582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d327d03f3716120871e15d8a53213e2201fb4c543cff4cfda89d44a362924f5b`  
		Last Modified: Wed, 08 Oct 2025 21:42:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a7bac72cbbe13e0d2ca93a7e2045c3cee7af4a9a99e4f4a137d438a669963e`  
		Last Modified: Wed, 08 Oct 2025 21:42:21 GMT  
		Size: 5.6 MB (5562729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:a538097b3d9e95fd66c681e163119ee4fda34648e1138be1471be07765e086b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1291403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121bd05d16ceb8c11139b6c2e140bdd3f2ff4d48d4eeae0c78b36653e7f2cb0a`

```dockerfile
```

-	Layers:
	-	`sha256:66532285c363d95627518c5ee59b11b1d8179d0e9a5459c633c0d02618fed06d`  
		Last Modified: Wed, 08 Oct 2025 22:59:39 GMT  
		Size: 1.3 MB (1273726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81f81d5bd314d48e57ad6439aa665accb301d8fa90cf9cfbc734e80cc3932d07`  
		Last Modified: Wed, 08 Oct 2025 22:59:40 GMT  
		Size: 17.7 KB (17677 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:6312b888a6893a7c5bcbfa3b983ab38749f99778b44a99530ef47a5fa8afe92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20344949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6748a647916da83e7b32a7fc1af7248d48c18b28e2c35d2403a1aeaba48783`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
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
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60d53dd86b6f70255a46f81ded3715200f2293ef56b5b5e4a9bd208fe73a5a4`  
		Last Modified: Wed, 08 Oct 2025 21:28:34 GMT  
		Size: 10.4 MB (10358145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f35b8acbeb2e8727c286447b6769cf3d016bb4864c5ad35e2e295e2f173749a`  
		Last Modified: Wed, 08 Oct 2025 21:28:33 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb455678cd1949819acffee4a71aa2ae7f91c1aae58a696c6666455cd9924e53`  
		Last Modified: Wed, 08 Oct 2025 21:28:35 GMT  
		Size: 5.8 MB (5847748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:816e238d7fee6ac073eb8bd4ed99e37a650f1d462c391ae4ae546450436b6e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f33b353f49dad9739f03717967b6ed81661089b4a5f7503a731715f3f4e1f5`

```dockerfile
```

-	Layers:
	-	`sha256:d1eb3ee699a52f4b20f4604d2e59b51c391ac02eb535317009268ef8a4fc45df`  
		Last Modified: Wed, 08 Oct 2025 22:59:44 GMT  
		Size: 1.3 MB (1270772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:309170da33d1e1e4b4a1a75c21c0120ff197fc0e4fb56a433d3097dd47cdb44b`  
		Last Modified: Wed, 08 Oct 2025 22:59:44 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.22` - linux; 386

```console
$ docker pull irssi@sha256:e66bdc96a17047cd31d803681e0c481fef6963c4d0120511222702e892610149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19616013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9546217ea8e23f6143afa741cd4e2050c708ad5ad67102826bac0bd4e68e070`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
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
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9ef0d9eddfed06ea09466e4f959f424bd4487ea48914b239e32d9a01ae664b`  
		Last Modified: Wed, 08 Oct 2025 21:14:07 GMT  
		Size: 9.9 MB (9940223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1546130b809d653b7ffb8056fabb7cde5c59816ee611d191515f665953378af9`  
		Last Modified: Wed, 08 Oct 2025 21:14:06 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05246638c115aace0ae244236cec9016bac4501e4699e0b5761e13d518f3aa7`  
		Last Modified: Wed, 08 Oct 2025 21:14:07 GMT  
		Size: 6.1 MB (6055871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:b12b29108acc7caee0ab23ab7c1191d2861b6bf4761b820569a0bb5519120cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a3cccb44b653f9d355429131978d3190d1b78b70f94e13b2cc06e9f7997a5e`

```dockerfile
```

-	Layers:
	-	`sha256:3ae7b6184d4abc32aca3718238c88832fa852fc8a1b082f050f7d291dfde1737`  
		Last Modified: Wed, 08 Oct 2025 22:59:48 GMT  
		Size: 1.3 MB (1270623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7720d5b50178fd0c79f8f0d50307c9837e7c9413280ecc69217fdc55705d6b3f`  
		Last Modified: Wed, 08 Oct 2025 22:59:49 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.22` - linux; ppc64le

```console
$ docker pull irssi@sha256:11ec21937e624e10112a9366a2e39f63804c250cd288519f31d38458aa0c9d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20560595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41dfe8eb30ae660e9f6b618bd8acba1eb372978247dff8685fcdb0393231e246`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
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
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48c17d61a4d1554d280ba28d7252c2f305090eeac61b357dd6b76bd73c43c63`  
		Last Modified: Thu, 09 Oct 2025 00:45:13 GMT  
		Size: 10.6 MB (10595397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26efea3de5b42df966c34855cef32948787b76acb851a4084e3e3ad212766f3`  
		Last Modified: Thu, 09 Oct 2025 00:45:11 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa99ddfbbb8375b453f006a945c8fa07c1ce170fda8448f7b653f0ac29d72c7b`  
		Last Modified: Thu, 09 Oct 2025 00:45:07 GMT  
		Size: 6.2 MB (6231972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:9c4cef9155fe22476444ceb17f379012b0c8b3e5e05a7c96919fa63eff2fdfe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179a2005edd691213f7786f101a4bd63364292c1882766e726e961190a7a7a47`

```dockerfile
```

-	Layers:
	-	`sha256:33a5c683cc42bda4a70c31f9d11afeffee44599ee508e945b64f8f0f007364b0`  
		Last Modified: Thu, 09 Oct 2025 01:59:38 GMT  
		Size: 1.3 MB (1268775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921ee5b46b5c6c2bdcc6f69f3de81a1779cddf19f1c547cb5807d97cd7e0429e`  
		Last Modified: Thu, 09 Oct 2025 01:59:39 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.22` - linux; riscv64

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

### `irssi:1.4.5-alpine3.22` - unknown; unknown

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

### `irssi:1.4.5-alpine3.22` - linux; s390x

```console
$ docker pull irssi@sha256:f3623b26ebb6e5ca70e89646c7b5dc3cc4923efff13fcf40e13603205b1d2c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20728269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4dc9af67d43ea3efb18b38b4dd936194a56cde8d7cedf49529c2085f844b996`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
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
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a35a93027b47a44ea544d9fee84d01ab7be35185d9c512211141ce9d358b9c`  
		Last Modified: Thu, 09 Oct 2025 00:42:42 GMT  
		Size: 11.0 MB (10953642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054cb0439f6b75b07dcf89d2ae109ef474c8c1ca0e6748b16768e98125bfadd4`  
		Last Modified: Thu, 09 Oct 2025 00:42:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1439f567e83e96d3eb1406d4ffb34da86c733b3fc27798542727ad6be641a537`  
		Last Modified: Thu, 09 Oct 2025 00:42:36 GMT  
		Size: 6.1 MB (6124398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:033679be33af045692166464cde309c06c55d1e3c2f0f70ff8f5a32a40c138cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3b68e4209308a841644a418b0f59ac60f7f2626e13c308ee01fa66528b5f4b`

```dockerfile
```

-	Layers:
	-	`sha256:874c4b424a680cfa6457999c0ce435d96b02cffc5203fa3f92b393d5811628a1`  
		Last Modified: Thu, 09 Oct 2025 01:59:58 GMT  
		Size: 1.3 MB (1268717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:586c45ea22dc49613e4d853a8c98ede4e76cc44653d06cf317710f979f305a99`  
		Last Modified: Thu, 09 Oct 2025 01:59:59 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-trixie`

```console
$ docker pull irssi@sha256:5cf9ab8c791c26cf2aa97983f1cc4debbebc4fb203bae59694fc0398575102d2
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
$ docker pull irssi@sha256:f62560d766eab4534167883aef43fa8fad47d829ff5c18467b86628e024bd9c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53870137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769552443b8c0b77660078238cebe5d212969cc1cef60189b3e988284170f129`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
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
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50e33926f10233e1cefedd2afc470ffdca1d03aae27f61804a5308859157ecd`  
		Last Modified: Tue, 21 Oct 2025 01:18:57 GMT  
		Size: 19.2 MB (19222452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5172862d08ce0c808ae6bd8643e68f924682e5145be1e8111d0b52f49a6fe9bc`  
		Last Modified: Tue, 21 Oct 2025 01:18:55 GMT  
		Size: 3.3 KB (3335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160b0c22ddb061ea4cd17f1ed3ca11aec9c1535fa615b47a6577d131dafc4ba3`  
		Last Modified: Tue, 21 Oct 2025 01:18:56 GMT  
		Size: 4.9 MB (4866394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:6eff9cda53aa1fce62b753cb7e75d79fbe1450f9fec0a77f0972a0a5c20df8d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4a3535c6261e33feac4e249dfb231f9d22a1d643b2b4a9b3d8f0a1ed8ff4dc`

```dockerfile
```

-	Layers:
	-	`sha256:984b3275ff964e7bbd701d8b5ca39a1b1abcd3f1bcf095ff7fea54585adab0a5`  
		Last Modified: Tue, 21 Oct 2025 10:59:26 GMT  
		Size: 5.6 MB (5588383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80576291496298d1465daebae79c9c7e21c694e8d2ab8ac5425ebf50e8de2192`  
		Last Modified: Tue, 21 Oct 2025 10:59:27 GMT  
		Size: 18.7 KB (18694 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:53bc4bdfbee3e6398af8cf776254a80b7ed67e7da2fe11c32d32d7abbe566dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50946604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea2d9d131f13dbc0476fa90cf34ad8697fe5db46e9a4c3807db7c7805165ed1`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 00:24:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:24:18 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 00:24:18 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 00:24:18 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 00:24:18 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 00:25:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 00:25:08 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 00:25:08 GMT
USER user
# Tue, 04 Nov 2025 00:25:08 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:453afc2258d7bc5729fed5672fb95bafa092e30a933b4377a12034be940a671b`  
		Last Modified: Tue, 04 Nov 2025 00:13:12 GMT  
		Size: 27.9 MB (27946438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56437b5f3c4f729d31fe7638873251d16b28c1c3d692a9956f5b69136d43e930`  
		Last Modified: Tue, 04 Nov 2025 00:25:28 GMT  
		Size: 18.3 MB (18287214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13428abf70cc1a9fb886bcdae90cfbe2d84d6f55745ed019971ee5ffd12cbc36`  
		Last Modified: Tue, 04 Nov 2025 00:25:27 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa255570f57e9797d70ef3d709d8bc0234a1d6314252033f6b60cde7930d539`  
		Last Modified: Tue, 04 Nov 2025 00:25:27 GMT  
		Size: 4.7 MB (4709590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:2cab70366a5eefad158f1357e7fbb0b830669bd73781291fc8f2f7c487e14ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe26f64be2cf34a6f1dbb907289e3ceedcd6e667a219c0df9ad5cccdd52607e1`

```dockerfile
```

-	Layers:
	-	`sha256:d6ab272cfb896c643aefbdbff6cc4a0edfb3a6ef0aff0c6564cc88a358010e7c`  
		Last Modified: Tue, 04 Nov 2025 08:59:27 GMT  
		Size: 5.6 MB (5585932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c8664e85e0ed44674cf84da06545a8bad6ddb201e7c9bdeffa2d711dc060c4`  
		Last Modified: Tue, 04 Nov 2025 08:59:28 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:ec7216e01ceba6748f58241dd44ef50c704fd9d0cbf6131634fd49a15f702256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48683586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb33d7b4c257421d912466ff540a8eab48db1957b1513f08e045342c3e09f7e`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
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
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec21711d4a258965a72caed76918b337c0aa5de6b91e590c06fc5e4745646f55`  
		Last Modified: Tue, 21 Oct 2025 01:21:40 GMT  
		Size: 17.9 MB (17908849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b844f9ec9159fe5dc1bceb0c829cf8fed6b324e19975cd9a3e797da3b9e7f32`  
		Last Modified: Tue, 21 Oct 2025 01:21:39 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8319989dae0a45f302eefb7eacf795675adb09faf457ef920f5f154d9e8fd6a`  
		Last Modified: Tue, 21 Oct 2025 01:21:40 GMT  
		Size: 4.6 MB (4558483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:1caf5b32a9cc375fdb8989c5e37fd5701d48a4ee13f33a1efb1c643b6656b614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1644fbc65e3d69b2d3bdd0d9e16c452b7d1c7156e981d44b810e54fb21f72726`

```dockerfile
```

-	Layers:
	-	`sha256:ef4ef36a4fd0ce15ccfe9d8c5c18fc16fafd0038ee0a805f0e2fbd3884993613`  
		Last Modified: Tue, 21 Oct 2025 07:59:30 GMT  
		Size: 5.6 MB (5588954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a879647ba458c48533bd9bc58dc4e49735e56b2b2509ed8842988ba5b86312e0`  
		Last Modified: Tue, 21 Oct 2025 07:59:31 GMT  
		Size: 18.8 KB (18832 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:77dfd1a59d7b77b123cca1beadf2971d1ba2ab34fdeeefeadce1a24e0f13126c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53976450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03efcec3d095c3aea650cc38e8beac272725967f1d9705561a88cc2cfabd06c7`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
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
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b408dc86163fc3064303c3d87a6f050d94d7e50026af6fec8d474bde261f9b`  
		Last Modified: Tue, 21 Oct 2025 01:19:20 GMT  
		Size: 19.0 MB (19049325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec261c2c31268433efbe285382be2e8e472bc1069f6f4703a8c3225b10ce0192`  
		Last Modified: Tue, 21 Oct 2025 01:19:18 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1acd4e881dacb1490ed68208dd4440fca46f3dc100f2a812bf12c1f676495e5`  
		Last Modified: Tue, 21 Oct 2025 01:19:19 GMT  
		Size: 4.8 MB (4781638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:2835026ba33a88cc6dd9fad1db6db1ec4ac24c190ed8d34348d3c797171fcabb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6636c1128d2fa3dcbaaa075ffd279fcdb2e092e8cd8f4acd4b4056e29c38c764`

```dockerfile
```

-	Layers:
	-	`sha256:71b8d4b308985e51f1304ef1f8d2a4365932f656bec2d21685a2b0333d5e3ccb`  
		Last Modified: Tue, 21 Oct 2025 07:59:54 GMT  
		Size: 5.6 MB (5594867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cda273518a593b1fdc06763d67c1ec3babffc7218cf0dfde047a1d3545ed65a0`  
		Last Modified: Tue, 21 Oct 2025 07:59:55 GMT  
		Size: 18.9 KB (18876 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; 386

```console
$ docker pull irssi@sha256:906a0c6f51c0b1f3b4ecb3f2e1c968d3704a25c07977646ef27d94b4b52f843b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54906871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f15a626e6515729d1e92c4029f7fd5ad811e6b1fa57491b31c1375bfd151edd`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
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
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a10221caffdcbfa0e53f49b1c8340c488768b10a5ea331304fe42934a151e92`  
		Last Modified: Tue, 21 Oct 2025 01:19:19 GMT  
		Size: 18.7 MB (18740674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99453861535e7430a13e074b1001d31ea1b6113f5f26cbd98c4898b8f5248b1`  
		Last Modified: Tue, 21 Oct 2025 01:19:17 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2532aeb1762cf3e40be739eca77e4a75e1fe38161883765d09f93de9e8e2da0e`  
		Last Modified: Tue, 21 Oct 2025 01:19:17 GMT  
		Size: 4.9 MB (4868206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:7da87f53975d8a9812601bfebe2d8b85bb1ddace02345349599eb31d26603b89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b166c953777c8cc44a6f84ea8cf0efae3b040be490d0e4cf0af5fc12b2fffe`

```dockerfile
```

-	Layers:
	-	`sha256:0d1c17737f2969710a690596ea60539faa8669ce29c2cdb5aea0ab822518a718`  
		Last Modified: Tue, 21 Oct 2025 10:59:42 GMT  
		Size: 5.6 MB (5584506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cf1c8a6fed6cbd711442dee178708058badce283771d0b8d81faae2d7964c89`  
		Last Modified: Tue, 21 Oct 2025 10:59:43 GMT  
		Size: 18.6 KB (18638 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:a084063aa561239245a691754b6dc2d671df6ef0560db4211c54b612f3e7ea15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58241580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f34336095685fcdececa53b502c6d01e505509b56e53158c6db1a854159927`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:40:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:40:10 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 01:40:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 01:40:10 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 01:40:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 01:41:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 01:41:53 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 01:41:53 GMT
USER user
# Tue, 04 Nov 2025 01:41:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87028ebfcd452692a3fb8d88c28f9dcaefbb732091f6921899481be54ff4c14a`  
		Last Modified: Tue, 04 Nov 2025 01:42:34 GMT  
		Size: 19.5 MB (19542341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4394dbe86dcc81b464d6e1d783cd35d455809fc85f44e42d150f96559d485a41`  
		Last Modified: Tue, 04 Nov 2025 01:42:28 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf7c6c4c0df971675464c86be67bdab3c2c25b38b37e01da482c5cb66037d0d`  
		Last Modified: Tue, 04 Nov 2025 01:42:30 GMT  
		Size: 5.1 MB (5097230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:f4763863a1b427e12438c44a011d6f057521086ff7d6d3089a8b1548112e00dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5919bc5740e214ee4b9780aee2c1ad773d2cb3193a47296199d9dd43b538349`

```dockerfile
```

-	Layers:
	-	`sha256:3c8efade8711469af7719f447e79a6a55a49965364fecba525c872e2c2c39f54`  
		Last Modified: Tue, 04 Nov 2025 08:59:43 GMT  
		Size: 5.6 MB (5595414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73fb47554826c5ea1fd080726318e56e507fb096dbdab60c4c068e35d1748a83`  
		Last Modified: Tue, 04 Nov 2025 08:59:43 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:ad6bd3a5205e24902df7636515066e77cd40386afc556802ffb26f1c77e0e0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51688796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af58c0755eac6d8da52a1a1e0818d9a970afed3f79411b1e29c974e03693f77c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 03:21:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:21:31 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 03:21:31 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 03:21:31 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 03:21:31 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 03:28:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 03:28:16 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 03:28:16 GMT
USER user
# Tue, 04 Nov 2025 03:28:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd582df31684b74a9fa351a3f7a398aaac1fcbdf5dbaa85b5372c8462d7c2f4`  
		Last Modified: Tue, 04 Nov 2025 03:30:29 GMT  
		Size: 18.5 MB (18549071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbc8e452a4bcbb01a4646ec80e76632da072b403d910c0cb470f33071b26713`  
		Last Modified: Tue, 04 Nov 2025 03:30:26 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339fd9308e80cf2bb6fbb2002e6caf32c46d806077d562abd9e9697cb185d246`  
		Last Modified: Tue, 04 Nov 2025 03:30:27 GMT  
		Size: 4.9 MB (4860578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:386968c0f2cc63a525d899d89b5efea2a6c8fb70db205e6fa72353d875d5a0ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6597a75bc6701428d03667f7d6c7f70c99d7b60e95a8d1fdb08d4b3ad6afec`

```dockerfile
```

-	Layers:
	-	`sha256:dc7fd9c40909a5578f92745efde764baa371271f42768e30f606d02bd12b7e43`  
		Last Modified: Tue, 04 Nov 2025 05:59:53 GMT  
		Size: 5.6 MB (5579686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2613fe6d4ed13c302d41cf48b4f8409a1d5bbf2c78e18ebcfa865a7ff55fc8a9`  
		Last Modified: Tue, 04 Nov 2025 05:59:54 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; s390x

```console
$ docker pull irssi@sha256:3a50bacd0aeaff8b8bb33a64478b835190ffccaa1513205554f7ee1f6a184193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54506755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a48d7420330e0856941ae3d5e153f27daff93349a4fa18e370e1742cb7f711`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 06:57:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 06:57:24 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 06:57:24 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 06:57:24 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 06:57:24 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 06:57:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 06:57:59 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 06:57:59 GMT
USER user
# Tue, 04 Nov 2025 06:57:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033854155955c69f5e80286c0220fcbce49683f27ff99d1e3003af7fcaf6c877`  
		Last Modified: Tue, 04 Nov 2025 06:58:21 GMT  
		Size: 19.8 MB (19760115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c247a95f4cb0054a4d91356e28a34cd9e78b4cd6a91641cb206c20a4432358`  
		Last Modified: Tue, 04 Nov 2025 06:58:20 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c870c8580f75359f105944243814e2056231525934f2762d516037ba84460b`  
		Last Modified: Tue, 04 Nov 2025 06:58:21 GMT  
		Size: 4.9 MB (4905887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:67067471ee97249a779cc6457e15b62dcd86599b15c73cb35fe07d4ee9d9bc15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb77a7d993b8fd0d0709a3f5d273dca60cf5a00b2a1843faf52e53880c2147e9`

```dockerfile
```

-	Layers:
	-	`sha256:6fabbd9421ca04d0605ccb6b593319d76d9eeb706da0f60a92f293e472d49d62`  
		Last Modified: Tue, 04 Nov 2025 09:00:17 GMT  
		Size: 5.6 MB (5589288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcd0465106c749fc617ea8887ce197ef6acc786e35587fff1f92baafdcc874fc`  
		Last Modified: Tue, 04 Nov 2025 09:00:18 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine`

```console
$ docker pull irssi@sha256:1e663ae10149c0b4d9df663b9da7bb650a58deea6cb49343c8191884eb0ec8ab
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
$ docker pull irssi@sha256:faf9e4f6be7260cc0682ec1445c6826e0bdcdc63f4a064eb8a981701bb709594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20173425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8798df3f4b34c7e6f52a3727072b2c410704453c6794f69663ce299680c47d3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e11827177f1c189b726b09341a9159227f1bfd85f6bfa5e738af089ccd47cc`  
		Last Modified: Wed, 08 Oct 2025 22:39:07 GMT  
		Size: 10.4 MB (10396003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6644b44e4c465f7087dbb97380180e75f01380c552303d8a2486f385aad34f35`  
		Last Modified: Wed, 08 Oct 2025 22:39:04 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b031546d04685e49a4d43b8482a34aaa0e6a3a6d75e947a09671aaf238e1ffc`  
		Last Modified: Wed, 08 Oct 2025 22:39:05 GMT  
		Size: 6.0 MB (5973981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:60dc002a8263e274525a471186038e9a631be6a5c61c1fd9e0ec2accade632f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be809ef2f20f547ecb812fc7251645454e581cc3d872627c003659069a74285e`

```dockerfile
```

-	Layers:
	-	`sha256:7def044fb5b5a27bb8a83fe2e1f6903b88c7090d91d03cc25c2be92d2b115084`  
		Last Modified: Thu, 09 Oct 2025 01:59:25 GMT  
		Size: 1.3 MB (1270668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09d745c2ae7ce01c7631e58d7cf581615e9c45ca2b8d31cccaa988c9e5257205`  
		Last Modified: Thu, 09 Oct 2025 01:59:26 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:8dfb08ad7779ab00246287f396771e855c5271e8e67f8fcb68229714505701e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18926923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e4ac8e569bab3223b4cbc8f2ffb5137d951b2efa8fbca448cdef1d3e4925de`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
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
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733b352b3151cd505887f05e68a9791f679acceebf79736c8050c72db1b5191a`  
		Last Modified: Wed, 08 Oct 2025 21:42:07 GMT  
		Size: 9.6 MB (9619615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8386f23106fb9eeab59f6f1e82d6fda32cd5130f7e9240952ab361424133835`  
		Last Modified: Wed, 08 Oct 2025 21:42:06 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5176e22c73a447407c118250d8b7084c947461ad88e0f8ffba848633ef457d1`  
		Last Modified: Wed, 08 Oct 2025 21:42:08 GMT  
		Size: 5.8 MB (5802239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:3529f2221a487a696afdfab5dd8793069c4e5153fdd0bbc77b1a10ed59976e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c402305c7b183a88a4427e0caf1314f408323bb659aab78e52073f5d4946a814`

```dockerfile
```

-	Layers:
	-	`sha256:40cb74de7dde3071930d2507974b11b96e2a2fcf0dd4cc4063ea7658469d44d0`  
		Last Modified: Wed, 08 Oct 2025 22:59:36 GMT  
		Size: 17.5 KB (17462 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:1c77198ac74e17d59093ac465b9d5cb18f5cf9b495d394dc7fe1757c6cd43c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18234853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81e381f20e12f748a613e6b9d046d4f23726de50b2d6209ee706e26cdc81cd9`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
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
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d355e9f8d23dd7df754d0fc9b69cb593d77843421e4fdc90e0999ac63d910671`  
		Last Modified: Wed, 08 Oct 2025 21:42:22 GMT  
		Size: 9.4 MB (9449582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d327d03f3716120871e15d8a53213e2201fb4c543cff4cfda89d44a362924f5b`  
		Last Modified: Wed, 08 Oct 2025 21:42:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a7bac72cbbe13e0d2ca93a7e2045c3cee7af4a9a99e4f4a137d438a669963e`  
		Last Modified: Wed, 08 Oct 2025 21:42:21 GMT  
		Size: 5.6 MB (5562729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:a538097b3d9e95fd66c681e163119ee4fda34648e1138be1471be07765e086b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1291403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121bd05d16ceb8c11139b6c2e140bdd3f2ff4d48d4eeae0c78b36653e7f2cb0a`

```dockerfile
```

-	Layers:
	-	`sha256:66532285c363d95627518c5ee59b11b1d8179d0e9a5459c633c0d02618fed06d`  
		Last Modified: Wed, 08 Oct 2025 22:59:39 GMT  
		Size: 1.3 MB (1273726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81f81d5bd314d48e57ad6439aa665accb301d8fa90cf9cfbc734e80cc3932d07`  
		Last Modified: Wed, 08 Oct 2025 22:59:40 GMT  
		Size: 17.7 KB (17677 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:6312b888a6893a7c5bcbfa3b983ab38749f99778b44a99530ef47a5fa8afe92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20344949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6748a647916da83e7b32a7fc1af7248d48c18b28e2c35d2403a1aeaba48783`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
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
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60d53dd86b6f70255a46f81ded3715200f2293ef56b5b5e4a9bd208fe73a5a4`  
		Last Modified: Wed, 08 Oct 2025 21:28:34 GMT  
		Size: 10.4 MB (10358145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f35b8acbeb2e8727c286447b6769cf3d016bb4864c5ad35e2e295e2f173749a`  
		Last Modified: Wed, 08 Oct 2025 21:28:33 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb455678cd1949819acffee4a71aa2ae7f91c1aae58a696c6666455cd9924e53`  
		Last Modified: Wed, 08 Oct 2025 21:28:35 GMT  
		Size: 5.8 MB (5847748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:816e238d7fee6ac073eb8bd4ed99e37a650f1d462c391ae4ae546450436b6e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f33b353f49dad9739f03717967b6ed81661089b4a5f7503a731715f3f4e1f5`

```dockerfile
```

-	Layers:
	-	`sha256:d1eb3ee699a52f4b20f4604d2e59b51c391ac02eb535317009268ef8a4fc45df`  
		Last Modified: Wed, 08 Oct 2025 22:59:44 GMT  
		Size: 1.3 MB (1270772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:309170da33d1e1e4b4a1a75c21c0120ff197fc0e4fb56a433d3097dd47cdb44b`  
		Last Modified: Wed, 08 Oct 2025 22:59:44 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; 386

```console
$ docker pull irssi@sha256:e66bdc96a17047cd31d803681e0c481fef6963c4d0120511222702e892610149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19616013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9546217ea8e23f6143afa741cd4e2050c708ad5ad67102826bac0bd4e68e070`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
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
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9ef0d9eddfed06ea09466e4f959f424bd4487ea48914b239e32d9a01ae664b`  
		Last Modified: Wed, 08 Oct 2025 21:14:07 GMT  
		Size: 9.9 MB (9940223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1546130b809d653b7ffb8056fabb7cde5c59816ee611d191515f665953378af9`  
		Last Modified: Wed, 08 Oct 2025 21:14:06 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05246638c115aace0ae244236cec9016bac4501e4699e0b5761e13d518f3aa7`  
		Last Modified: Wed, 08 Oct 2025 21:14:07 GMT  
		Size: 6.1 MB (6055871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:b12b29108acc7caee0ab23ab7c1191d2861b6bf4761b820569a0bb5519120cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a3cccb44b653f9d355429131978d3190d1b78b70f94e13b2cc06e9f7997a5e`

```dockerfile
```

-	Layers:
	-	`sha256:3ae7b6184d4abc32aca3718238c88832fa852fc8a1b082f050f7d291dfde1737`  
		Last Modified: Wed, 08 Oct 2025 22:59:48 GMT  
		Size: 1.3 MB (1270623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7720d5b50178fd0c79f8f0d50307c9837e7c9413280ecc69217fdc55705d6b3f`  
		Last Modified: Wed, 08 Oct 2025 22:59:49 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:11ec21937e624e10112a9366a2e39f63804c250cd288519f31d38458aa0c9d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20560595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41dfe8eb30ae660e9f6b618bd8acba1eb372978247dff8685fcdb0393231e246`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
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
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48c17d61a4d1554d280ba28d7252c2f305090eeac61b357dd6b76bd73c43c63`  
		Last Modified: Thu, 09 Oct 2025 00:45:13 GMT  
		Size: 10.6 MB (10595397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26efea3de5b42df966c34855cef32948787b76acb851a4084e3e3ad212766f3`  
		Last Modified: Thu, 09 Oct 2025 00:45:11 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa99ddfbbb8375b453f006a945c8fa07c1ce170fda8448f7b653f0ac29d72c7b`  
		Last Modified: Thu, 09 Oct 2025 00:45:07 GMT  
		Size: 6.2 MB (6231972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:9c4cef9155fe22476444ceb17f379012b0c8b3e5e05a7c96919fa63eff2fdfe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179a2005edd691213f7786f101a4bd63364292c1882766e726e961190a7a7a47`

```dockerfile
```

-	Layers:
	-	`sha256:33a5c683cc42bda4a70c31f9d11afeffee44599ee508e945b64f8f0f007364b0`  
		Last Modified: Thu, 09 Oct 2025 01:59:38 GMT  
		Size: 1.3 MB (1268775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921ee5b46b5c6c2bdcc6f69f3de81a1779cddf19f1c547cb5807d97cd7e0429e`  
		Last Modified: Thu, 09 Oct 2025 01:59:39 GMT  
		Size: 17.6 KB (17615 bytes)  
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
$ docker pull irssi@sha256:f3623b26ebb6e5ca70e89646c7b5dc3cc4923efff13fcf40e13603205b1d2c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20728269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4dc9af67d43ea3efb18b38b4dd936194a56cde8d7cedf49529c2085f844b996`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
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
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a35a93027b47a44ea544d9fee84d01ab7be35185d9c512211141ce9d358b9c`  
		Last Modified: Thu, 09 Oct 2025 00:42:42 GMT  
		Size: 11.0 MB (10953642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054cb0439f6b75b07dcf89d2ae109ef474c8c1ca0e6748b16768e98125bfadd4`  
		Last Modified: Thu, 09 Oct 2025 00:42:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1439f567e83e96d3eb1406d4ffb34da86c733b3fc27798542727ad6be641a537`  
		Last Modified: Thu, 09 Oct 2025 00:42:36 GMT  
		Size: 6.1 MB (6124398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:033679be33af045692166464cde309c06c55d1e3c2f0f70ff8f5a32a40c138cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3b68e4209308a841644a418b0f59ac60f7f2626e13c308ee01fa66528b5f4b`

```dockerfile
```

-	Layers:
	-	`sha256:874c4b424a680cfa6457999c0ce435d96b02cffc5203fa3f92b393d5811628a1`  
		Last Modified: Thu, 09 Oct 2025 01:59:58 GMT  
		Size: 1.3 MB (1268717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:586c45ea22dc49613e4d853a8c98ede4e76cc44653d06cf317710f979f305a99`  
		Last Modified: Thu, 09 Oct 2025 01:59:59 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine3.22`

```console
$ docker pull irssi@sha256:1e663ae10149c0b4d9df663b9da7bb650a58deea6cb49343c8191884eb0ec8ab
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

### `irssi:alpine3.22` - linux; amd64

```console
$ docker pull irssi@sha256:faf9e4f6be7260cc0682ec1445c6826e0bdcdc63f4a064eb8a981701bb709594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20173425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8798df3f4b34c7e6f52a3727072b2c410704453c6794f69663ce299680c47d3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e11827177f1c189b726b09341a9159227f1bfd85f6bfa5e738af089ccd47cc`  
		Last Modified: Wed, 08 Oct 2025 22:39:07 GMT  
		Size: 10.4 MB (10396003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6644b44e4c465f7087dbb97380180e75f01380c552303d8a2486f385aad34f35`  
		Last Modified: Wed, 08 Oct 2025 22:39:04 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b031546d04685e49a4d43b8482a34aaa0e6a3a6d75e947a09671aaf238e1ffc`  
		Last Modified: Wed, 08 Oct 2025 22:39:05 GMT  
		Size: 6.0 MB (5973981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:60dc002a8263e274525a471186038e9a631be6a5c61c1fd9e0ec2accade632f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be809ef2f20f547ecb812fc7251645454e581cc3d872627c003659069a74285e`

```dockerfile
```

-	Layers:
	-	`sha256:7def044fb5b5a27bb8a83fe2e1f6903b88c7090d91d03cc25c2be92d2b115084`  
		Last Modified: Thu, 09 Oct 2025 01:59:25 GMT  
		Size: 1.3 MB (1270668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09d745c2ae7ce01c7631e58d7cf581615e9c45ca2b8d31cccaa988c9e5257205`  
		Last Modified: Thu, 09 Oct 2025 01:59:26 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.22` - linux; arm variant v6

```console
$ docker pull irssi@sha256:8dfb08ad7779ab00246287f396771e855c5271e8e67f8fcb68229714505701e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18926923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e4ac8e569bab3223b4cbc8f2ffb5137d951b2efa8fbca448cdef1d3e4925de`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
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
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733b352b3151cd505887f05e68a9791f679acceebf79736c8050c72db1b5191a`  
		Last Modified: Wed, 08 Oct 2025 21:42:07 GMT  
		Size: 9.6 MB (9619615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8386f23106fb9eeab59f6f1e82d6fda32cd5130f7e9240952ab361424133835`  
		Last Modified: Wed, 08 Oct 2025 21:42:06 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5176e22c73a447407c118250d8b7084c947461ad88e0f8ffba848633ef457d1`  
		Last Modified: Wed, 08 Oct 2025 21:42:08 GMT  
		Size: 5.8 MB (5802239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:3529f2221a487a696afdfab5dd8793069c4e5153fdd0bbc77b1a10ed59976e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c402305c7b183a88a4427e0caf1314f408323bb659aab78e52073f5d4946a814`

```dockerfile
```

-	Layers:
	-	`sha256:40cb74de7dde3071930d2507974b11b96e2a2fcf0dd4cc4063ea7658469d44d0`  
		Last Modified: Wed, 08 Oct 2025 22:59:36 GMT  
		Size: 17.5 KB (17462 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.22` - linux; arm variant v7

```console
$ docker pull irssi@sha256:1c77198ac74e17d59093ac465b9d5cb18f5cf9b495d394dc7fe1757c6cd43c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18234853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81e381f20e12f748a613e6b9d046d4f23726de50b2d6209ee706e26cdc81cd9`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
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
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d355e9f8d23dd7df754d0fc9b69cb593d77843421e4fdc90e0999ac63d910671`  
		Last Modified: Wed, 08 Oct 2025 21:42:22 GMT  
		Size: 9.4 MB (9449582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d327d03f3716120871e15d8a53213e2201fb4c543cff4cfda89d44a362924f5b`  
		Last Modified: Wed, 08 Oct 2025 21:42:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a7bac72cbbe13e0d2ca93a7e2045c3cee7af4a9a99e4f4a137d438a669963e`  
		Last Modified: Wed, 08 Oct 2025 21:42:21 GMT  
		Size: 5.6 MB (5562729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:a538097b3d9e95fd66c681e163119ee4fda34648e1138be1471be07765e086b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1291403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121bd05d16ceb8c11139b6c2e140bdd3f2ff4d48d4eeae0c78b36653e7f2cb0a`

```dockerfile
```

-	Layers:
	-	`sha256:66532285c363d95627518c5ee59b11b1d8179d0e9a5459c633c0d02618fed06d`  
		Last Modified: Wed, 08 Oct 2025 22:59:39 GMT  
		Size: 1.3 MB (1273726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81f81d5bd314d48e57ad6439aa665accb301d8fa90cf9cfbc734e80cc3932d07`  
		Last Modified: Wed, 08 Oct 2025 22:59:40 GMT  
		Size: 17.7 KB (17677 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:6312b888a6893a7c5bcbfa3b983ab38749f99778b44a99530ef47a5fa8afe92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20344949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6748a647916da83e7b32a7fc1af7248d48c18b28e2c35d2403a1aeaba48783`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
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
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60d53dd86b6f70255a46f81ded3715200f2293ef56b5b5e4a9bd208fe73a5a4`  
		Last Modified: Wed, 08 Oct 2025 21:28:34 GMT  
		Size: 10.4 MB (10358145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f35b8acbeb2e8727c286447b6769cf3d016bb4864c5ad35e2e295e2f173749a`  
		Last Modified: Wed, 08 Oct 2025 21:28:33 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb455678cd1949819acffee4a71aa2ae7f91c1aae58a696c6666455cd9924e53`  
		Last Modified: Wed, 08 Oct 2025 21:28:35 GMT  
		Size: 5.8 MB (5847748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:816e238d7fee6ac073eb8bd4ed99e37a650f1d462c391ae4ae546450436b6e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f33b353f49dad9739f03717967b6ed81661089b4a5f7503a731715f3f4e1f5`

```dockerfile
```

-	Layers:
	-	`sha256:d1eb3ee699a52f4b20f4604d2e59b51c391ac02eb535317009268ef8a4fc45df`  
		Last Modified: Wed, 08 Oct 2025 22:59:44 GMT  
		Size: 1.3 MB (1270772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:309170da33d1e1e4b4a1a75c21c0120ff197fc0e4fb56a433d3097dd47cdb44b`  
		Last Modified: Wed, 08 Oct 2025 22:59:44 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.22` - linux; 386

```console
$ docker pull irssi@sha256:e66bdc96a17047cd31d803681e0c481fef6963c4d0120511222702e892610149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19616013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9546217ea8e23f6143afa741cd4e2050c708ad5ad67102826bac0bd4e68e070`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
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
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9ef0d9eddfed06ea09466e4f959f424bd4487ea48914b239e32d9a01ae664b`  
		Last Modified: Wed, 08 Oct 2025 21:14:07 GMT  
		Size: 9.9 MB (9940223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1546130b809d653b7ffb8056fabb7cde5c59816ee611d191515f665953378af9`  
		Last Modified: Wed, 08 Oct 2025 21:14:06 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05246638c115aace0ae244236cec9016bac4501e4699e0b5761e13d518f3aa7`  
		Last Modified: Wed, 08 Oct 2025 21:14:07 GMT  
		Size: 6.1 MB (6055871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:b12b29108acc7caee0ab23ab7c1191d2861b6bf4761b820569a0bb5519120cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a3cccb44b653f9d355429131978d3190d1b78b70f94e13b2cc06e9f7997a5e`

```dockerfile
```

-	Layers:
	-	`sha256:3ae7b6184d4abc32aca3718238c88832fa852fc8a1b082f050f7d291dfde1737`  
		Last Modified: Wed, 08 Oct 2025 22:59:48 GMT  
		Size: 1.3 MB (1270623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7720d5b50178fd0c79f8f0d50307c9837e7c9413280ecc69217fdc55705d6b3f`  
		Last Modified: Wed, 08 Oct 2025 22:59:49 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.22` - linux; ppc64le

```console
$ docker pull irssi@sha256:11ec21937e624e10112a9366a2e39f63804c250cd288519f31d38458aa0c9d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20560595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41dfe8eb30ae660e9f6b618bd8acba1eb372978247dff8685fcdb0393231e246`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
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
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48c17d61a4d1554d280ba28d7252c2f305090eeac61b357dd6b76bd73c43c63`  
		Last Modified: Thu, 09 Oct 2025 00:45:13 GMT  
		Size: 10.6 MB (10595397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26efea3de5b42df966c34855cef32948787b76acb851a4084e3e3ad212766f3`  
		Last Modified: Thu, 09 Oct 2025 00:45:11 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa99ddfbbb8375b453f006a945c8fa07c1ce170fda8448f7b653f0ac29d72c7b`  
		Last Modified: Thu, 09 Oct 2025 00:45:07 GMT  
		Size: 6.2 MB (6231972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:9c4cef9155fe22476444ceb17f379012b0c8b3e5e05a7c96919fa63eff2fdfe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179a2005edd691213f7786f101a4bd63364292c1882766e726e961190a7a7a47`

```dockerfile
```

-	Layers:
	-	`sha256:33a5c683cc42bda4a70c31f9d11afeffee44599ee508e945b64f8f0f007364b0`  
		Last Modified: Thu, 09 Oct 2025 01:59:38 GMT  
		Size: 1.3 MB (1268775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921ee5b46b5c6c2bdcc6f69f3de81a1779cddf19f1c547cb5807d97cd7e0429e`  
		Last Modified: Thu, 09 Oct 2025 01:59:39 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.22` - linux; riscv64

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

### `irssi:alpine3.22` - unknown; unknown

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

### `irssi:alpine3.22` - linux; s390x

```console
$ docker pull irssi@sha256:f3623b26ebb6e5ca70e89646c7b5dc3cc4923efff13fcf40e13603205b1d2c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20728269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4dc9af67d43ea3efb18b38b4dd936194a56cde8d7cedf49529c2085f844b996`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 21:14:55 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
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
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a35a93027b47a44ea544d9fee84d01ab7be35185d9c512211141ce9d358b9c`  
		Last Modified: Thu, 09 Oct 2025 00:42:42 GMT  
		Size: 11.0 MB (10953642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054cb0439f6b75b07dcf89d2ae109ef474c8c1ca0e6748b16768e98125bfadd4`  
		Last Modified: Thu, 09 Oct 2025 00:42:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1439f567e83e96d3eb1406d4ffb34da86c733b3fc27798542727ad6be641a537`  
		Last Modified: Thu, 09 Oct 2025 00:42:36 GMT  
		Size: 6.1 MB (6124398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:033679be33af045692166464cde309c06c55d1e3c2f0f70ff8f5a32a40c138cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3b68e4209308a841644a418b0f59ac60f7f2626e13c308ee01fa66528b5f4b`

```dockerfile
```

-	Layers:
	-	`sha256:874c4b424a680cfa6457999c0ce435d96b02cffc5203fa3f92b393d5811628a1`  
		Last Modified: Thu, 09 Oct 2025 01:59:58 GMT  
		Size: 1.3 MB (1268717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:586c45ea22dc49613e4d853a8c98ede4e76cc44653d06cf317710f979f305a99`  
		Last Modified: Thu, 09 Oct 2025 01:59:59 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:latest`

```console
$ docker pull irssi@sha256:b59a4c12644a0027378d6b7fc6fdb8933cc3eb9cf106e0952aee8798d91b182e
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
$ docker pull irssi@sha256:f553b587fa2fcc5d841159dae68ae5bf4fa4d3c004d4d41242dc5313d4846fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53869909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6b3f77c651ad0f798e6d156e86951a9c95ee5d69267226def79404119d3ddc`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:05:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:05:17 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 04:05:17 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 04:05:17 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 04:05:17 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 04:05:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 04:05:53 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 04:05:53 GMT
USER user
# Tue, 04 Nov 2025 04:05:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b0149746e47a3ae7dee7e39c040588240de613548f17fe0a058de2c1fc9261`  
		Last Modified: Tue, 04 Nov 2025 04:06:12 GMT  
		Size: 19.2 MB (19221929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e10c64e7837e1354d0490b74de7c2c3e98fc0c725da960fbded84b74970342`  
		Last Modified: Tue, 04 Nov 2025 04:06:09 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119f0b70c0bf9309cf82be23770dfc5801e9ef27c65481131ca9363d15c89931`  
		Last Modified: Tue, 04 Nov 2025 04:06:09 GMT  
		Size: 4.9 MB (4866514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:6b140b015d97f19b567cc8a1a2761d84a722bee7b30026905ae95f53561b9dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc93d52e86204f02c704594c0e6e1fad2032358d3d0ba201fc97399b5e3b1c18`

```dockerfile
```

-	Layers:
	-	`sha256:8dd46d6af558746cf8ebd456f3223832a8b27e755e65d95b16b4e1a65c31339b`  
		Last Modified: Tue, 04 Nov 2025 08:59:45 GMT  
		Size: 5.6 MB (5588383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abee79486a69ff2a04d7a50f938463a4fc51734d6565f7e6b1812dbaa04897a5`  
		Last Modified: Tue, 04 Nov 2025 08:59:46 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v5

```console
$ docker pull irssi@sha256:53bc4bdfbee3e6398af8cf776254a80b7ed67e7da2fe11c32d32d7abbe566dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50946604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea2d9d131f13dbc0476fa90cf34ad8697fe5db46e9a4c3807db7c7805165ed1`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 00:24:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:24:18 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 00:24:18 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 00:24:18 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 00:24:18 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 00:25:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 00:25:08 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 00:25:08 GMT
USER user
# Tue, 04 Nov 2025 00:25:08 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:453afc2258d7bc5729fed5672fb95bafa092e30a933b4377a12034be940a671b`  
		Last Modified: Tue, 04 Nov 2025 00:13:12 GMT  
		Size: 27.9 MB (27946438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56437b5f3c4f729d31fe7638873251d16b28c1c3d692a9956f5b69136d43e930`  
		Last Modified: Tue, 04 Nov 2025 00:25:28 GMT  
		Size: 18.3 MB (18287214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13428abf70cc1a9fb886bcdae90cfbe2d84d6f55745ed019971ee5ffd12cbc36`  
		Last Modified: Tue, 04 Nov 2025 00:25:27 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa255570f57e9797d70ef3d709d8bc0234a1d6314252033f6b60cde7930d539`  
		Last Modified: Tue, 04 Nov 2025 00:25:27 GMT  
		Size: 4.7 MB (4709590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:2cab70366a5eefad158f1357e7fbb0b830669bd73781291fc8f2f7c487e14ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe26f64be2cf34a6f1dbb907289e3ceedcd6e667a219c0df9ad5cccdd52607e1`

```dockerfile
```

-	Layers:
	-	`sha256:d6ab272cfb896c643aefbdbff6cc4a0edfb3a6ef0aff0c6564cc88a358010e7c`  
		Last Modified: Tue, 04 Nov 2025 08:59:27 GMT  
		Size: 5.6 MB (5585932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c8664e85e0ed44674cf84da06545a8bad6ddb201e7c9bdeffa2d711dc060c4`  
		Last Modified: Tue, 04 Nov 2025 08:59:28 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v7

```console
$ docker pull irssi@sha256:ec7216e01ceba6748f58241dd44ef50c704fd9d0cbf6131634fd49a15f702256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48683586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb33d7b4c257421d912466ff540a8eab48db1957b1513f08e045342c3e09f7e`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
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
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec21711d4a258965a72caed76918b337c0aa5de6b91e590c06fc5e4745646f55`  
		Last Modified: Tue, 21 Oct 2025 01:21:40 GMT  
		Size: 17.9 MB (17908849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b844f9ec9159fe5dc1bceb0c829cf8fed6b324e19975cd9a3e797da3b9e7f32`  
		Last Modified: Tue, 21 Oct 2025 01:21:39 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8319989dae0a45f302eefb7eacf795675adb09faf457ef920f5f154d9e8fd6a`  
		Last Modified: Tue, 21 Oct 2025 01:21:40 GMT  
		Size: 4.6 MB (4558483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:1caf5b32a9cc375fdb8989c5e37fd5701d48a4ee13f33a1efb1c643b6656b614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1644fbc65e3d69b2d3bdd0d9e16c452b7d1c7156e981d44b810e54fb21f72726`

```dockerfile
```

-	Layers:
	-	`sha256:ef4ef36a4fd0ce15ccfe9d8c5c18fc16fafd0038ee0a805f0e2fbd3884993613`  
		Last Modified: Tue, 21 Oct 2025 07:59:30 GMT  
		Size: 5.6 MB (5588954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a879647ba458c48533bd9bc58dc4e49735e56b2b2509ed8842988ba5b86312e0`  
		Last Modified: Tue, 21 Oct 2025 07:59:31 GMT  
		Size: 18.8 KB (18832 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:77dfd1a59d7b77b123cca1beadf2971d1ba2ab34fdeeefeadce1a24e0f13126c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53976450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03efcec3d095c3aea650cc38e8beac272725967f1d9705561a88cc2cfabd06c7`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
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
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b408dc86163fc3064303c3d87a6f050d94d7e50026af6fec8d474bde261f9b`  
		Last Modified: Tue, 21 Oct 2025 01:19:20 GMT  
		Size: 19.0 MB (19049325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec261c2c31268433efbe285382be2e8e472bc1069f6f4703a8c3225b10ce0192`  
		Last Modified: Tue, 21 Oct 2025 01:19:18 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1acd4e881dacb1490ed68208dd4440fca46f3dc100f2a812bf12c1f676495e5`  
		Last Modified: Tue, 21 Oct 2025 01:19:19 GMT  
		Size: 4.8 MB (4781638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:2835026ba33a88cc6dd9fad1db6db1ec4ac24c190ed8d34348d3c797171fcabb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6636c1128d2fa3dcbaaa075ffd279fcdb2e092e8cd8f4acd4b4056e29c38c764`

```dockerfile
```

-	Layers:
	-	`sha256:71b8d4b308985e51f1304ef1f8d2a4365932f656bec2d21685a2b0333d5e3ccb`  
		Last Modified: Tue, 21 Oct 2025 07:59:54 GMT  
		Size: 5.6 MB (5594867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cda273518a593b1fdc06763d67c1ec3babffc7218cf0dfde047a1d3545ed65a0`  
		Last Modified: Tue, 21 Oct 2025 07:59:55 GMT  
		Size: 18.9 KB (18876 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; 386

```console
$ docker pull irssi@sha256:906a0c6f51c0b1f3b4ecb3f2e1c968d3704a25c07977646ef27d94b4b52f843b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54906871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f15a626e6515729d1e92c4029f7fd5ad811e6b1fa57491b31c1375bfd151edd`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
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
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a10221caffdcbfa0e53f49b1c8340c488768b10a5ea331304fe42934a151e92`  
		Last Modified: Tue, 21 Oct 2025 01:19:19 GMT  
		Size: 18.7 MB (18740674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99453861535e7430a13e074b1001d31ea1b6113f5f26cbd98c4898b8f5248b1`  
		Last Modified: Tue, 21 Oct 2025 01:19:17 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2532aeb1762cf3e40be739eca77e4a75e1fe38161883765d09f93de9e8e2da0e`  
		Last Modified: Tue, 21 Oct 2025 01:19:17 GMT  
		Size: 4.9 MB (4868206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:7da87f53975d8a9812601bfebe2d8b85bb1ddace02345349599eb31d26603b89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b166c953777c8cc44a6f84ea8cf0efae3b040be490d0e4cf0af5fc12b2fffe`

```dockerfile
```

-	Layers:
	-	`sha256:0d1c17737f2969710a690596ea60539faa8669ce29c2cdb5aea0ab822518a718`  
		Last Modified: Tue, 21 Oct 2025 10:59:42 GMT  
		Size: 5.6 MB (5584506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cf1c8a6fed6cbd711442dee178708058badce283771d0b8d81faae2d7964c89`  
		Last Modified: Tue, 21 Oct 2025 10:59:43 GMT  
		Size: 18.6 KB (18638 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; ppc64le

```console
$ docker pull irssi@sha256:a084063aa561239245a691754b6dc2d671df6ef0560db4211c54b612f3e7ea15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58241580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f34336095685fcdececa53b502c6d01e505509b56e53158c6db1a854159927`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:40:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:40:10 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 01:40:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 01:40:10 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 01:40:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 01:41:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 01:41:53 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 01:41:53 GMT
USER user
# Tue, 04 Nov 2025 01:41:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87028ebfcd452692a3fb8d88c28f9dcaefbb732091f6921899481be54ff4c14a`  
		Last Modified: Tue, 04 Nov 2025 01:42:34 GMT  
		Size: 19.5 MB (19542341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4394dbe86dcc81b464d6e1d783cd35d455809fc85f44e42d150f96559d485a41`  
		Last Modified: Tue, 04 Nov 2025 01:42:28 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf7c6c4c0df971675464c86be67bdab3c2c25b38b37e01da482c5cb66037d0d`  
		Last Modified: Tue, 04 Nov 2025 01:42:30 GMT  
		Size: 5.1 MB (5097230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:f4763863a1b427e12438c44a011d6f057521086ff7d6d3089a8b1548112e00dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5919bc5740e214ee4b9780aee2c1ad773d2cb3193a47296199d9dd43b538349`

```dockerfile
```

-	Layers:
	-	`sha256:3c8efade8711469af7719f447e79a6a55a49965364fecba525c872e2c2c39f54`  
		Last Modified: Tue, 04 Nov 2025 08:59:43 GMT  
		Size: 5.6 MB (5595414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73fb47554826c5ea1fd080726318e56e507fb096dbdab60c4c068e35d1748a83`  
		Last Modified: Tue, 04 Nov 2025 08:59:43 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; riscv64

```console
$ docker pull irssi@sha256:ad6bd3a5205e24902df7636515066e77cd40386afc556802ffb26f1c77e0e0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51688796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af58c0755eac6d8da52a1a1e0818d9a970afed3f79411b1e29c974e03693f77c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 03:21:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:21:31 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 03:21:31 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 03:21:31 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 03:21:31 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 03:28:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 03:28:16 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 03:28:16 GMT
USER user
# Tue, 04 Nov 2025 03:28:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd582df31684b74a9fa351a3f7a398aaac1fcbdf5dbaa85b5372c8462d7c2f4`  
		Last Modified: Tue, 04 Nov 2025 03:30:29 GMT  
		Size: 18.5 MB (18549071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbc8e452a4bcbb01a4646ec80e76632da072b403d910c0cb470f33071b26713`  
		Last Modified: Tue, 04 Nov 2025 03:30:26 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339fd9308e80cf2bb6fbb2002e6caf32c46d806077d562abd9e9697cb185d246`  
		Last Modified: Tue, 04 Nov 2025 03:30:27 GMT  
		Size: 4.9 MB (4860578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:386968c0f2cc63a525d899d89b5efea2a6c8fb70db205e6fa72353d875d5a0ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6597a75bc6701428d03667f7d6c7f70c99d7b60e95a8d1fdb08d4b3ad6afec`

```dockerfile
```

-	Layers:
	-	`sha256:dc7fd9c40909a5578f92745efde764baa371271f42768e30f606d02bd12b7e43`  
		Last Modified: Tue, 04 Nov 2025 05:59:53 GMT  
		Size: 5.6 MB (5579686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2613fe6d4ed13c302d41cf48b4f8409a1d5bbf2c78e18ebcfa865a7ff55fc8a9`  
		Last Modified: Tue, 04 Nov 2025 05:59:54 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; s390x

```console
$ docker pull irssi@sha256:3a50bacd0aeaff8b8bb33a64478b835190ffccaa1513205554f7ee1f6a184193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54506755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a48d7420330e0856941ae3d5e153f27daff93349a4fa18e370e1742cb7f711`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 06:57:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 06:57:24 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 06:57:24 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 06:57:24 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 06:57:24 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 06:57:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 06:57:59 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 06:57:59 GMT
USER user
# Tue, 04 Nov 2025 06:57:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033854155955c69f5e80286c0220fcbce49683f27ff99d1e3003af7fcaf6c877`  
		Last Modified: Tue, 04 Nov 2025 06:58:21 GMT  
		Size: 19.8 MB (19760115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c247a95f4cb0054a4d91356e28a34cd9e78b4cd6a91641cb206c20a4432358`  
		Last Modified: Tue, 04 Nov 2025 06:58:20 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c870c8580f75359f105944243814e2056231525934f2762d516037ba84460b`  
		Last Modified: Tue, 04 Nov 2025 06:58:21 GMT  
		Size: 4.9 MB (4905887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:67067471ee97249a779cc6457e15b62dcd86599b15c73cb35fe07d4ee9d9bc15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb77a7d993b8fd0d0709a3f5d273dca60cf5a00b2a1843faf52e53880c2147e9`

```dockerfile
```

-	Layers:
	-	`sha256:6fabbd9421ca04d0605ccb6b593319d76d9eeb706da0f60a92f293e472d49d62`  
		Last Modified: Tue, 04 Nov 2025 09:00:17 GMT  
		Size: 5.6 MB (5589288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcd0465106c749fc617ea8887ce197ef6acc786e35587fff1f92baafdcc874fc`  
		Last Modified: Tue, 04 Nov 2025 09:00:18 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:trixie`

```console
$ docker pull irssi@sha256:b59a4c12644a0027378d6b7fc6fdb8933cc3eb9cf106e0952aee8798d91b182e
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
$ docker pull irssi@sha256:f553b587fa2fcc5d841159dae68ae5bf4fa4d3c004d4d41242dc5313d4846fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53869909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6b3f77c651ad0f798e6d156e86951a9c95ee5d69267226def79404119d3ddc`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:05:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:05:17 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 04:05:17 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 04:05:17 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 04:05:17 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 04:05:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 04:05:53 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 04:05:53 GMT
USER user
# Tue, 04 Nov 2025 04:05:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b0149746e47a3ae7dee7e39c040588240de613548f17fe0a058de2c1fc9261`  
		Last Modified: Tue, 04 Nov 2025 04:06:12 GMT  
		Size: 19.2 MB (19221929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e10c64e7837e1354d0490b74de7c2c3e98fc0c725da960fbded84b74970342`  
		Last Modified: Tue, 04 Nov 2025 04:06:09 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119f0b70c0bf9309cf82be23770dfc5801e9ef27c65481131ca9363d15c89931`  
		Last Modified: Tue, 04 Nov 2025 04:06:09 GMT  
		Size: 4.9 MB (4866514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:6b140b015d97f19b567cc8a1a2761d84a722bee7b30026905ae95f53561b9dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc93d52e86204f02c704594c0e6e1fad2032358d3d0ba201fc97399b5e3b1c18`

```dockerfile
```

-	Layers:
	-	`sha256:8dd46d6af558746cf8ebd456f3223832a8b27e755e65d95b16b4e1a65c31339b`  
		Last Modified: Tue, 04 Nov 2025 08:59:45 GMT  
		Size: 5.6 MB (5588383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abee79486a69ff2a04d7a50f938463a4fc51734d6565f7e6b1812dbaa04897a5`  
		Last Modified: Tue, 04 Nov 2025 08:59:46 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:53bc4bdfbee3e6398af8cf776254a80b7ed67e7da2fe11c32d32d7abbe566dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50946604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea2d9d131f13dbc0476fa90cf34ad8697fe5db46e9a4c3807db7c7805165ed1`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 00:24:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:24:18 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 00:24:18 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 00:24:18 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 00:24:18 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 00:25:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 00:25:08 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 00:25:08 GMT
USER user
# Tue, 04 Nov 2025 00:25:08 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:453afc2258d7bc5729fed5672fb95bafa092e30a933b4377a12034be940a671b`  
		Last Modified: Tue, 04 Nov 2025 00:13:12 GMT  
		Size: 27.9 MB (27946438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56437b5f3c4f729d31fe7638873251d16b28c1c3d692a9956f5b69136d43e930`  
		Last Modified: Tue, 04 Nov 2025 00:25:28 GMT  
		Size: 18.3 MB (18287214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13428abf70cc1a9fb886bcdae90cfbe2d84d6f55745ed019971ee5ffd12cbc36`  
		Last Modified: Tue, 04 Nov 2025 00:25:27 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa255570f57e9797d70ef3d709d8bc0234a1d6314252033f6b60cde7930d539`  
		Last Modified: Tue, 04 Nov 2025 00:25:27 GMT  
		Size: 4.7 MB (4709590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:2cab70366a5eefad158f1357e7fbb0b830669bd73781291fc8f2f7c487e14ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe26f64be2cf34a6f1dbb907289e3ceedcd6e667a219c0df9ad5cccdd52607e1`

```dockerfile
```

-	Layers:
	-	`sha256:d6ab272cfb896c643aefbdbff6cc4a0edfb3a6ef0aff0c6564cc88a358010e7c`  
		Last Modified: Tue, 04 Nov 2025 08:59:27 GMT  
		Size: 5.6 MB (5585932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c8664e85e0ed44674cf84da06545a8bad6ddb201e7c9bdeffa2d711dc060c4`  
		Last Modified: Tue, 04 Nov 2025 08:59:28 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:ec7216e01ceba6748f58241dd44ef50c704fd9d0cbf6131634fd49a15f702256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48683586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb33d7b4c257421d912466ff540a8eab48db1957b1513f08e045342c3e09f7e`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
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
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec21711d4a258965a72caed76918b337c0aa5de6b91e590c06fc5e4745646f55`  
		Last Modified: Tue, 21 Oct 2025 01:21:40 GMT  
		Size: 17.9 MB (17908849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b844f9ec9159fe5dc1bceb0c829cf8fed6b324e19975cd9a3e797da3b9e7f32`  
		Last Modified: Tue, 21 Oct 2025 01:21:39 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8319989dae0a45f302eefb7eacf795675adb09faf457ef920f5f154d9e8fd6a`  
		Last Modified: Tue, 21 Oct 2025 01:21:40 GMT  
		Size: 4.6 MB (4558483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:1caf5b32a9cc375fdb8989c5e37fd5701d48a4ee13f33a1efb1c643b6656b614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1644fbc65e3d69b2d3bdd0d9e16c452b7d1c7156e981d44b810e54fb21f72726`

```dockerfile
```

-	Layers:
	-	`sha256:ef4ef36a4fd0ce15ccfe9d8c5c18fc16fafd0038ee0a805f0e2fbd3884993613`  
		Last Modified: Tue, 21 Oct 2025 07:59:30 GMT  
		Size: 5.6 MB (5588954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a879647ba458c48533bd9bc58dc4e49735e56b2b2509ed8842988ba5b86312e0`  
		Last Modified: Tue, 21 Oct 2025 07:59:31 GMT  
		Size: 18.8 KB (18832 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:77dfd1a59d7b77b123cca1beadf2971d1ba2ab34fdeeefeadce1a24e0f13126c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53976450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03efcec3d095c3aea650cc38e8beac272725967f1d9705561a88cc2cfabd06c7`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
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
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b408dc86163fc3064303c3d87a6f050d94d7e50026af6fec8d474bde261f9b`  
		Last Modified: Tue, 21 Oct 2025 01:19:20 GMT  
		Size: 19.0 MB (19049325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec261c2c31268433efbe285382be2e8e472bc1069f6f4703a8c3225b10ce0192`  
		Last Modified: Tue, 21 Oct 2025 01:19:18 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1acd4e881dacb1490ed68208dd4440fca46f3dc100f2a812bf12c1f676495e5`  
		Last Modified: Tue, 21 Oct 2025 01:19:19 GMT  
		Size: 4.8 MB (4781638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:2835026ba33a88cc6dd9fad1db6db1ec4ac24c190ed8d34348d3c797171fcabb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6636c1128d2fa3dcbaaa075ffd279fcdb2e092e8cd8f4acd4b4056e29c38c764`

```dockerfile
```

-	Layers:
	-	`sha256:71b8d4b308985e51f1304ef1f8d2a4365932f656bec2d21685a2b0333d5e3ccb`  
		Last Modified: Tue, 21 Oct 2025 07:59:54 GMT  
		Size: 5.6 MB (5594867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cda273518a593b1fdc06763d67c1ec3babffc7218cf0dfde047a1d3545ed65a0`  
		Last Modified: Tue, 21 Oct 2025 07:59:55 GMT  
		Size: 18.9 KB (18876 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; 386

```console
$ docker pull irssi@sha256:906a0c6f51c0b1f3b4ecb3f2e1c968d3704a25c07977646ef27d94b4b52f843b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54906871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f15a626e6515729d1e92c4029f7fd5ad811e6b1fa57491b31c1375bfd151edd`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
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
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a10221caffdcbfa0e53f49b1c8340c488768b10a5ea331304fe42934a151e92`  
		Last Modified: Tue, 21 Oct 2025 01:19:19 GMT  
		Size: 18.7 MB (18740674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99453861535e7430a13e074b1001d31ea1b6113f5f26cbd98c4898b8f5248b1`  
		Last Modified: Tue, 21 Oct 2025 01:19:17 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2532aeb1762cf3e40be739eca77e4a75e1fe38161883765d09f93de9e8e2da0e`  
		Last Modified: Tue, 21 Oct 2025 01:19:17 GMT  
		Size: 4.9 MB (4868206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:7da87f53975d8a9812601bfebe2d8b85bb1ddace02345349599eb31d26603b89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b166c953777c8cc44a6f84ea8cf0efae3b040be490d0e4cf0af5fc12b2fffe`

```dockerfile
```

-	Layers:
	-	`sha256:0d1c17737f2969710a690596ea60539faa8669ce29c2cdb5aea0ab822518a718`  
		Last Modified: Tue, 21 Oct 2025 10:59:42 GMT  
		Size: 5.6 MB (5584506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cf1c8a6fed6cbd711442dee178708058badce283771d0b8d81faae2d7964c89`  
		Last Modified: Tue, 21 Oct 2025 10:59:43 GMT  
		Size: 18.6 KB (18638 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:a084063aa561239245a691754b6dc2d671df6ef0560db4211c54b612f3e7ea15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58241580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f34336095685fcdececa53b502c6d01e505509b56e53158c6db1a854159927`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:40:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:40:10 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 01:40:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 01:40:10 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 01:40:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 01:41:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 01:41:53 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 01:41:53 GMT
USER user
# Tue, 04 Nov 2025 01:41:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87028ebfcd452692a3fb8d88c28f9dcaefbb732091f6921899481be54ff4c14a`  
		Last Modified: Tue, 04 Nov 2025 01:42:34 GMT  
		Size: 19.5 MB (19542341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4394dbe86dcc81b464d6e1d783cd35d455809fc85f44e42d150f96559d485a41`  
		Last Modified: Tue, 04 Nov 2025 01:42:28 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf7c6c4c0df971675464c86be67bdab3c2c25b38b37e01da482c5cb66037d0d`  
		Last Modified: Tue, 04 Nov 2025 01:42:30 GMT  
		Size: 5.1 MB (5097230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:f4763863a1b427e12438c44a011d6f057521086ff7d6d3089a8b1548112e00dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5919bc5740e214ee4b9780aee2c1ad773d2cb3193a47296199d9dd43b538349`

```dockerfile
```

-	Layers:
	-	`sha256:3c8efade8711469af7719f447e79a6a55a49965364fecba525c872e2c2c39f54`  
		Last Modified: Tue, 04 Nov 2025 08:59:43 GMT  
		Size: 5.6 MB (5595414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73fb47554826c5ea1fd080726318e56e507fb096dbdab60c4c068e35d1748a83`  
		Last Modified: Tue, 04 Nov 2025 08:59:43 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:ad6bd3a5205e24902df7636515066e77cd40386afc556802ffb26f1c77e0e0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51688796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af58c0755eac6d8da52a1a1e0818d9a970afed3f79411b1e29c974e03693f77c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 03:21:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:21:31 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 03:21:31 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 03:21:31 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 03:21:31 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 03:28:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 03:28:16 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 03:28:16 GMT
USER user
# Tue, 04 Nov 2025 03:28:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd582df31684b74a9fa351a3f7a398aaac1fcbdf5dbaa85b5372c8462d7c2f4`  
		Last Modified: Tue, 04 Nov 2025 03:30:29 GMT  
		Size: 18.5 MB (18549071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbc8e452a4bcbb01a4646ec80e76632da072b403d910c0cb470f33071b26713`  
		Last Modified: Tue, 04 Nov 2025 03:30:26 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339fd9308e80cf2bb6fbb2002e6caf32c46d806077d562abd9e9697cb185d246`  
		Last Modified: Tue, 04 Nov 2025 03:30:27 GMT  
		Size: 4.9 MB (4860578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:386968c0f2cc63a525d899d89b5efea2a6c8fb70db205e6fa72353d875d5a0ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6597a75bc6701428d03667f7d6c7f70c99d7b60e95a8d1fdb08d4b3ad6afec`

```dockerfile
```

-	Layers:
	-	`sha256:dc7fd9c40909a5578f92745efde764baa371271f42768e30f606d02bd12b7e43`  
		Last Modified: Tue, 04 Nov 2025 05:59:53 GMT  
		Size: 5.6 MB (5579686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2613fe6d4ed13c302d41cf48b4f8409a1d5bbf2c78e18ebcfa865a7ff55fc8a9`  
		Last Modified: Tue, 04 Nov 2025 05:59:54 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; s390x

```console
$ docker pull irssi@sha256:3a50bacd0aeaff8b8bb33a64478b835190ffccaa1513205554f7ee1f6a184193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54506755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a48d7420330e0856941ae3d5e153f27daff93349a4fa18e370e1742cb7f711`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 06:57:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 06:57:24 GMT
ENV HOME=/home/user
# Tue, 04 Nov 2025 06:57:24 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 04 Nov 2025 06:57:24 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 06:57:24 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 04 Nov 2025 06:57:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 04 Nov 2025 06:57:59 GMT
WORKDIR /home/user
# Tue, 04 Nov 2025 06:57:59 GMT
USER user
# Tue, 04 Nov 2025 06:57:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033854155955c69f5e80286c0220fcbce49683f27ff99d1e3003af7fcaf6c877`  
		Last Modified: Tue, 04 Nov 2025 06:58:21 GMT  
		Size: 19.8 MB (19760115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c247a95f4cb0054a4d91356e28a34cd9e78b4cd6a91641cb206c20a4432358`  
		Last Modified: Tue, 04 Nov 2025 06:58:20 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c870c8580f75359f105944243814e2056231525934f2762d516037ba84460b`  
		Last Modified: Tue, 04 Nov 2025 06:58:21 GMT  
		Size: 4.9 MB (4905887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:67067471ee97249a779cc6457e15b62dcd86599b15c73cb35fe07d4ee9d9bc15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb77a7d993b8fd0d0709a3f5d273dca60cf5a00b2a1843faf52e53880c2147e9`

```dockerfile
```

-	Layers:
	-	`sha256:6fabbd9421ca04d0605ccb6b593319d76d9eeb706da0f60a92f293e472d49d62`  
		Last Modified: Tue, 04 Nov 2025 09:00:17 GMT  
		Size: 5.6 MB (5589288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcd0465106c749fc617ea8887ce197ef6acc786e35587fff1f92baafdcc874fc`  
		Last Modified: Tue, 04 Nov 2025 09:00:18 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json
