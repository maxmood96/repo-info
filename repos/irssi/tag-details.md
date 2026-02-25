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
$ docker pull irssi@sha256:6f18ede25b4d4593ab99544ab52277a4e1254f2fbe6a64def5eb7de58074fffc
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
$ docker pull irssi@sha256:49c3737149b22851a93ba69ac22cebd9abf8c8a5d5994e2ca286860caf15353a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53871168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f752e1dfe12c027448c72cd5e3229ea7002dea38239febe081da26b8f7b27ed3`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:03:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:03:00 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:03:00 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:03:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:03:41 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:03:41 GMT
USER user
# Tue, 24 Feb 2026 19:03:41 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7ad25661c3266880a3c864c64ca6faa3b88c0ddb4a998a667e1f1d4b99a22d`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 19.2 MB (19222246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc80a3f9407efa5dcf0dc0ba37f425c82a6ecff60485ff89dd844390ff01a53`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d808574b07af61087631c143ffb9e4be37c1313e4d6fb331c97d17da0f436b32`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 4.9 MB (4866927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:abd6aeef322973ea82182a219b2ba14441f100be5d532e6f7b52e6062bc15a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979b803961d56ac53e2960a4847046894c3f5095836cf0aa2fd343e0288e1e0e`

```dockerfile
```

-	Layers:
	-	`sha256:3557d7d8d5e4df3d7ade5b19b149d56205ce87989a1066808f14bcf3f4321be4`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 5.6 MB (5588475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94196f7468e34a70daa83619d0cf5061ae5adf7711aca144d3d43fc9475a48da`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v5

```console
$ docker pull irssi@sha256:6887b2daf7a8e04420d9f8019955beefca4b05d2370737f5085f12f8bb863c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50955082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82db261419aa9d562d5751330a1b61cd4d76e7c5028123921b370b072d4e9c19`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:59:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 18:59:28 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 18:59:28 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 18:59:28 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 18:59:28 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:00:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:00:20 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:00:20 GMT
USER user
# Tue, 24 Feb 2026 19:00:20 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7364bcc76ebade3ad468fc97fcab1317a1b01976383c65ec8f166e9828038c67`  
		Last Modified: Tue, 24 Feb 2026 19:00:34 GMT  
		Size: 18.3 MB (18294280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d702d54a8b971c044db6fb77d45b0c781dbb99062e9faf1a81743c47fc56bf`  
		Last Modified: Tue, 24 Feb 2026 19:00:31 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b41ba1be7d2ca3c964a8be01ccc30e64cc8a0ca03702c32d5870d2d3d769bb`  
		Last Modified: Tue, 24 Feb 2026 19:00:35 GMT  
		Size: 4.7 MB (4709832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:9ec580a8a2c10e1b7ac74c5a41f66009751caa3a8d2b0dc76ce73021e5457329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3590dbb7640207ebd9aa49bf6c514655778ebcc0dea1bf38fe7da73c02990d03`

```dockerfile
```

-	Layers:
	-	`sha256:93ef4bd1a5d0d962b395d82efceb8f97a7d23f4cd0a74978d0edd9456835b58f`  
		Last Modified: Tue, 24 Feb 2026 19:00:31 GMT  
		Size: 5.6 MB (5586024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:025639689d36438751d0440bf57caefab23fbf1a4e77b9cc3febff3196f2a2b9`  
		Last Modified: Tue, 24 Feb 2026 19:00:31 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v7

```console
$ docker pull irssi@sha256:e65224016b946c4d99129fad9314bdbdc0bf0296df171d4ce13bc5aa24cb6cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48688484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9c173ed818b8888f5cbf8f2e9258855675b8dd27c9cb7908c704a1d3069397`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:03:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:03:16 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:03:16 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:03:16 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:03:16 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:03:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:03:58 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:03:58 GMT
USER user
# Tue, 24 Feb 2026 19:03:58 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6afde1291a25c0cc231ccde29bbe0ad9ff81c712d4e11e050becb6d4ba8ce0d`  
		Last Modified: Tue, 24 Feb 2026 19:04:08 GMT  
		Size: 17.9 MB (17913151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b8f6d599a61d91e34fb4362460af69da8f684fd2226c0a12c37f1fee9652b8`  
		Last Modified: Tue, 24 Feb 2026 19:04:07 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4575a9012f56ba332b5c7534e48f48a25065b112fa4613e17f2d061261eb8e13`  
		Last Modified: Tue, 24 Feb 2026 19:04:08 GMT  
		Size: 4.6 MB (4558224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:578b6038b34fa00900a70d96abebf8df03f41cbef32e270af68c766ed6703f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9176d67dd016c9ba37147b21f657ef2ae76348260f1f72189b8dc548007b5a73`

```dockerfile
```

-	Layers:
	-	`sha256:cca03ae28695eb959e228e35c2e861a53e15134500b965d0f79e67be15a1cf50`  
		Last Modified: Tue, 24 Feb 2026 19:04:08 GMT  
		Size: 5.6 MB (5589046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dade344df2087c2cbe360a19c02237de12027a28b597247bd6d4844a90a5dad`  
		Last Modified: Tue, 24 Feb 2026 19:04:07 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:b5705a932a1071d49bc33cb793e6492a17f0c13a09af00c00847132826a5399d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53975047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95271ad57b650f4906bebb73ced93170cb93cdc9485991098fde0de3c6ac7f3b`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:06:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:06:10 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:06:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:06:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:06:46 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:06:46 GMT
USER user
# Tue, 24 Feb 2026 19:06:46 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bde18e6576dd26665639dfee2e2c29ab72d5a490303fa301ad8b6d16d01032`  
		Last Modified: Tue, 24 Feb 2026 19:06:58 GMT  
		Size: 19.1 MB (19050073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb0f26017633de6d20b077a7d5fbc6cc2e5ca7a1231309bb6d18d9c6914a55b`  
		Last Modified: Tue, 24 Feb 2026 19:06:57 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5666611ba24e987a94791ca84b6bb380525795696e072f0d60ba9d17ade814ef`  
		Last Modified: Tue, 24 Feb 2026 19:06:57 GMT  
		Size: 4.8 MB (4781514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:900b2ed2e203d81d8f8d6a5cd524d2db8b91bd6962cbb74ffcb0d2a396647107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136a2b4c868d58cd89f9de10c7f831de5ff64687d2b3f76d4e7c01b8ffa16584`

```dockerfile
```

-	Layers:
	-	`sha256:2fef361a887b7785b6efd16d1c15d0262f2f2c6d45edab1f8a975ba81b6f1fdd`  
		Last Modified: Tue, 24 Feb 2026 19:06:57 GMT  
		Size: 5.6 MB (5594959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb64f6057abd305766916ed63546cbd132d825a2da5422247487175382c5f5b9`  
		Last Modified: Tue, 24 Feb 2026 19:06:57 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; 386

```console
$ docker pull irssi@sha256:47a406a29379abd6ed06b0d20217433e973e2870d780ff30823782f31e5c6b33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54908577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91e586aa3e8ce17d01aee6359c922ffe41daa80e277df7ae8ed8d1889e1bb0b`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:58:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 18:58:30 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 18:58:30 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 18:58:30 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 18:58:30 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 18:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 18:59:11 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 18:59:11 GMT
USER user
# Tue, 24 Feb 2026 18:59:11 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ae61c08fa4b2cc99f86dc6a1fe4823c3e0ac9a711287f64cac6485a6238ac8`  
		Last Modified: Tue, 24 Feb 2026 18:59:21 GMT  
		Size: 18.7 MB (18742816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf3f98a9e73f8a6e5b1989e717a2286e372230bcaff62941bae689905197df8`  
		Last Modified: Tue, 24 Feb 2026 18:59:20 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a297182723d0165449b463b3d8873cf3e889a114d50096866c842a8e640504`  
		Last Modified: Tue, 24 Feb 2026 18:59:21 GMT  
		Size: 4.9 MB (4868483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:6c462d49b091009b00485bef9ea87abfab3cb1639844d8c0ed87db6e3e81f5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ff00c0c6b361160a520647c72a3cf1d9322aed6a3382745d35d0d05d128d4e`

```dockerfile
```

-	Layers:
	-	`sha256:b4fd1d01133f85b3efcc51e3d12301590bbb5fb57101916a792336a8d1dea592`  
		Last Modified: Tue, 24 Feb 2026 18:59:21 GMT  
		Size: 5.6 MB (5584598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00eea56a9297862479d3e58a1bd8c833d2a522ff54655c30af9634f5c984d84d`  
		Last Modified: Tue, 24 Feb 2026 18:59:20 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; ppc64le

```console
$ docker pull irssi@sha256:91b49338a181c6d7b1ae5689c2a610af4dcb438d1eb567f96160219d271063f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58240333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4fc70f04320b975862b6d37425c6f5766d3f6c2e97e62049747274abf47acc`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:07:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:07:22 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:07:22 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:07:22 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:07:22 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:09:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:09:16 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:09:16 GMT
USER user
# Tue, 24 Feb 2026 19:09:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5beebebe5029aabb929ae44c4537e3b21fd8d65921a409bb2df1b7c9b634b6d`  
		Last Modified: Tue, 24 Feb 2026 19:09:44 GMT  
		Size: 19.5 MB (19538939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed570b0aeb97d8cb44da9c8850814c6aa7e1b43fe3d9f4058d9d5a52f0eb6224`  
		Last Modified: Tue, 24 Feb 2026 19:09:43 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ecef354c37ad21cbe5f6e442c1f3c79f858cd86e1ece389542887cae1cff44d`  
		Last Modified: Tue, 24 Feb 2026 19:09:43 GMT  
		Size: 5.1 MB (5097820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:38354f39cc3e23ea94d1feaca94d6602908c74c9dbd5beddfeeb5bd33866538a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904a8b4a8a183068c5d6db74160bbb18d87a4c74f95375cf320b45143257753e`

```dockerfile
```

-	Layers:
	-	`sha256:4c2d2dc5bef56d23df0cb5b905d48dc667fb78e0a3c3a168e9e8a3a4f7f1b318`  
		Last Modified: Tue, 24 Feb 2026 19:09:43 GMT  
		Size: 5.6 MB (5595506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:373385b6bc18ef5a4933f2dfe5147cd4368d7f2730b1f214cd1abe2372ffb0d2`  
		Last Modified: Tue, 24 Feb 2026 19:09:43 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; riscv64

```console
$ docker pull irssi@sha256:3a7d38a48cd82c9bd2d5741f468dcdfbf92e333ecc06c2d12dbfe8b938ab0307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51693147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0a99e5b7cd8d4f262722aed889c863e4c892a0f23fe9749d929e8dec75cf662`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 03:03:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 03:03:38 GMT
ENV HOME=/home/user
# Wed, 25 Feb 2026 03:03:38 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 25 Feb 2026 03:03:38 GMT
ENV LANG=C.UTF-8
# Wed, 25 Feb 2026 03:03:38 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 25 Feb 2026 03:10:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 25 Feb 2026 03:10:25 GMT
WORKDIR /home/user
# Wed, 25 Feb 2026 03:10:25 GMT
USER user
# Wed, 25 Feb 2026 03:10:25 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6508c3cdfc31f498c772515ee0821b13440e08ba735c32d3cba318269a3f687`  
		Last Modified: Wed, 25 Feb 2026 03:12:21 GMT  
		Size: 18.6 MB (18552692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ef556a8959335b7e794bf6752b54a81934178688ef1e7d4dbdb197aa0eb326`  
		Last Modified: Wed, 25 Feb 2026 03:12:16 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2794c755bfc5dceb9c6a1eb2ff258465b48801c3bd877b5cde6f46d9920a5c`  
		Last Modified: Wed, 25 Feb 2026 03:12:18 GMT  
		Size: 4.9 MB (4860678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:5ad91e36e6745d334569f2aede71764aa6ab0c8d2ed12405c01d1a981287b5ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ebcaf2e72424c63e04d825e7d04bbe5589f3f805c573faf9c8484afea2b540f`

```dockerfile
```

-	Layers:
	-	`sha256:5c3be456f6ce9090fac8cee71f4291c1aaef1a9ac164f8e2bd0de699367a6334`  
		Last Modified: Wed, 25 Feb 2026 03:12:18 GMT  
		Size: 5.6 MB (5579778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9be1a19638d1af3b7539195ea9d207d142146b312fe552361ffde9b48f90de25`  
		Last Modified: Wed, 25 Feb 2026 03:12:16 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; s390x

```console
$ docker pull irssi@sha256:9d2c67d051b5f92f329619102e0e2bc0df643ef026d1f553c93d501eb54b0049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54516690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf87075c86e270be08f7350f9904070bb3c572934e47a6d6aa9e70fefbff3812`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:01:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:01:50 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:01:50 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:01:50 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:01:50 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:03:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:03:57 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:03:57 GMT
USER user
# Tue, 24 Feb 2026 19:03:57 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb8e7c85a43a84dc9bfa10f335db4cb6dbd00571742698dd7d26077875d9a48`  
		Last Modified: Tue, 24 Feb 2026 19:04:25 GMT  
		Size: 19.8 MB (19768672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e12ffbdb3791dcf1981e8eefcf126275f55fe052fac3a8fafc881aac17c34d8`  
		Last Modified: Tue, 24 Feb 2026 19:04:24 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149d77b47e1605f5cda1129f653ed9adbc0c8c0c2286fd9e81c91c6c44d32956`  
		Last Modified: Tue, 24 Feb 2026 19:04:25 GMT  
		Size: 4.9 MB (4906478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:d10e5a37df33b885dd47403b1e8b7a310eb535821e3b44695a144c5fb72da92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b0fb8133b9ed0bb88f527230ee5b7eefff618321781bea5b846e5b8d1ea2a2`

```dockerfile
```

-	Layers:
	-	`sha256:9ab81d1d85995cb9010ed56d4fdb909af0e66dc54953575d97300c5e3eb22dbe`  
		Last Modified: Tue, 24 Feb 2026 19:04:24 GMT  
		Size: 5.6 MB (5589380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5cb68be6babc8fbd8fc9be84183610c6d3f88b4fb466e15ef8526dfead89283`  
		Last Modified: Tue, 24 Feb 2026 19:04:24 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine`

```console
$ docker pull irssi@sha256:bc9744c4e1f3c9e4401ee35e73ff4f7c97683f5c784c5cce21910e488a4ee219
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
$ docker pull irssi@sha256:84665fb63540b0ca94547800ed0093cb97d41e1cbc0d2aa823a67e6af91fe8ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20784026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6645503b9d588217c1fb06c9a2d7e278a4360e4aa22e92d8ff0af44ac2c6c10`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:47 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:17:47 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:17:47 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:17:47 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:17:47 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:18:00 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:18:00 GMT
USER user
# Wed, 28 Jan 2026 02:18:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d65c05b32f228b7007340211a175e100ca3ddb33a7e2c44b15d11799a9a84ad`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 10.9 MB (10857996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082c32a8914140e457d67603de3b04ccc66e688baed84d8d500f40dc885ef27a`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93abf1ed0403fdbc85fa021598a1202b3d9b55bd9d785457b554af6b86fc7d`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 6.1 MB (6063223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:7bd9c1f9350891fb6e79ac3dc4d7686c1c714bb2c12147cb089864d19ef3bc9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e29e513927a47425fe64b68ba4eeb03593581de0692a732211bc7b11537936`

```dockerfile
```

-	Layers:
	-	`sha256:5d4ee629f31bfb597346562d7da53858808c502ca6820fb40a7c347520afebad`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 1.3 MB (1308739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b9c1c09e72415a3ca7367aec0652ca69a856b8c6a57ef69ba919d208498b76`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:9a8babd75444eea65ebe3a06627eceb16f4d50aec2da2998fd3a611d75ed5b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19539552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04e50bc1d87804658a7d29a7ebb00b20d1a22d6d21cd19f5eff93f84035eb0b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:23:56 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:23:57 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:23:57 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:23:57 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:23:57 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:24:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:24:17 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:24:17 GMT
USER user
# Wed, 28 Jan 2026 02:24:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d5c4e6a80a684ff34083f2ded6ae6a1b0f08ded4c8c5b0967f8b209ee2cd80`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 10.1 MB (10075626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93db171eca68243a4f689b5400ef3c2ac2a1074f1eae1f9f0d049506c8756fe`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23c8c890839d95ebaf447485d8492d089fc8fa23d1ca65c6349a41ac95bc961`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 5.9 MB (5893116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:424e17d1ca73b3f1d92e5d0c0b7272bbaeee943cc673a2249f0bf7ca99eeedde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e7bd514eeda8663e46d4eeed484d7df02209f60112393607269af3e2c0430c`

```dockerfile
```

-	Layers:
	-	`sha256:8fbda3c9e4c0ad20ecba339d117fab2e86108fcfe33cbba7f8ddc3053d6bc89a`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:42ff91c7e5cb5046e91c18adce476ce64e5d772ab658a70c9df46e592b10ce82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18828366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ac84c98bbbaf189bedd8109f71397874c887df2e4eb32123f05470b88358b5`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:21 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:22:22 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:22:22 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:22:22 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:22:22 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:22:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:22:37 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:22:37 GMT
USER user
# Wed, 28 Jan 2026 02:22:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132ae8f3941338d2191aad9429d0bd185ceeb7aeedb8fddf43adad6b57e3273e`  
		Last Modified: Wed, 28 Jan 2026 02:22:45 GMT  
		Size: 9.9 MB (9902405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770acb73451dc424aeb5afcad4a4882f5d765fcbcc8b659b8841bf77d8166afe`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda40971fe170d5e56e81f398ba01d1904a08b07386da11fe56b125109dd60b9`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 5.6 MB (5643252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:fcebcd556b705ae5c410e6b569b01096b561714c5c2fc1d7c8c746decaeef0bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1328781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d61d96801a2a79a245717287e0380350d8e1b0c44936b6dcaf8429b0e2074bab`

```dockerfile
```

-	Layers:
	-	`sha256:e0caf0a4bbae914fea3e8ffab5d1f1752e3fc858d38e993806dd2b78f6919657`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 1.3 MB (1311147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fda69d589c766de3e44adc56d464708c1c2090577cfe6fdd9a50f95229a2c4fa`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:c53ef5cb4c4fb78d4ffdaad1b902adc24327fb49d4ad5c6d719dcf26f8e1ceba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20927195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7538037fb15131e4b2540ac0e275393593929c95a1ca622c94e6c70d99874f28`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:48 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:17:48 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:17:48 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:17:48 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:17:48 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:18:00 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:18:00 GMT
USER user
# Wed, 28 Jan 2026 02:18:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628108c2cc8068dbd74588362d3734d7b6b306883916eb33cb53af667c096440`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 10.8 MB (10792790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9361ffc4206f8e272dc8adc782da4ab39f3b1fe287c6dfb23c57814cf1e94439`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7efe759a9de929b3a25440ff73ac10595ac218ae5d0a087f34fa385d7db181f`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 5.9 MB (5936327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:ac959328037122478f2c09228cf4478f1c099d3257efec2dae9823db1d16b2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db6c23ab4cfc36c7b70e7f4325b9bfa25d1a31a205c632f8e25757cb01f7cef`

```dockerfile
```

-	Layers:
	-	`sha256:3b09e8c286f81074ecdbaaeccccef453ddf9951ff459e4c086e01b8968fe3b0e`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 1.3 MB (1308193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57974d8beacb812f7bb8f7b52301ddd6a66eb7f4c851dcc2ee58f100ec0208b1`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 17.7 KB (17682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; 386

```console
$ docker pull irssi@sha256:a32c16d5607a49617e8d077ec1f9ba5b53b0001a5d70805f183e27ac8f377955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20225669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7946f5f999880045f35ea6c3b7115f7cc7ca872f2653f90c5b0a114ea701599b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:14 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:16:14 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:16:14 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:16:14 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:16:14 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:16:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:16:34 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:16:34 GMT
USER user
# Wed, 28 Jan 2026 02:16:34 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50882b3c493b99635b6de6cd7279fc00a7df160e84cd53399664993828611810`  
		Last Modified: Wed, 28 Jan 2026 02:16:41 GMT  
		Size: 10.4 MB (10393535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7588c02c444f10953a0f0aac9fa979fe4a835bbefde822557708fbd3d21750de`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7dcb0c68d5a17e86130988d6ddf97978ae4c3d866b099962426d869a1c1fc3`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 6.1 MB (6144150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:b77b6da6595a9c4ebfe003d3192b1a97bd9a14f1fe19417ad4a8d7068acc0505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16f268d469cb9fcc79cb87b83fdcbadb9fa6818bf4d9c56a441df0e015c2ec6`

```dockerfile
```

-	Layers:
	-	`sha256:1ddc13011deb856a736a8c90df7acab1227398d8a2ae9e4586daa141365096b4`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 1.3 MB (1308694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47e26778e3f506818fa4ed452e58334a8e15701f1d896ec8ed2ff3288ca7ecef`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:b40803da860e141ec3ab2320cf224c304aa870a9a884cb362b69e74b6fd82b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21272396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a2c6a98e5b7978e9d4671908d2864a8d58c1b872e5ec279f9a7a67312f3e2b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:32:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:32:11 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:32:11 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:32:11 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:32:11 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:32:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:32:31 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:32:31 GMT
USER user
# Wed, 28 Jan 2026 02:32:31 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc81a5350f307da5c9651178208c0aa789db44da9179ac834ac469d70ce42cc`  
		Last Modified: Wed, 28 Jan 2026 02:32:51 GMT  
		Size: 11.1 MB (11079608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e505a6cbf58cbc8474040a9d448a79cab0812b78e3b1c6db13e87987f8e4d9a0`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3296179391416e1833f722cc60f06d3ee4df4255177c36a2f41a35a6ab2661b`  
		Last Modified: Wed, 28 Jan 2026 02:32:51 GMT  
		Size: 6.4 MB (6362158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:e2ead2561551ba2a279d799d266e484e986d5370478af7155036333e682a1a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551e8fca5526f8aa868ce90e80d554f73ff2800bcf6fb3b0fb1b9013223228b5`

```dockerfile
```

-	Layers:
	-	`sha256:890481868cc7de496dcdc1f70cc0d6026227efccdd40466a57aa43304c3e345f`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 1.3 MB (1308146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9fac81ff985d048567933403c842b1d477306de718e7d5226612b3cb1eb068`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:a29b54bd9ab139f5c60185ee85db0a602092a6821866cad82df0fb45368c398c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19942208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9176875f86f8abf3bc20c65b42847d911af0be7e5863f4d6dcbd526719132c`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 08:24:33 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 08:24:34 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 08:24:34 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 08:24:34 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 08:24:34 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 08:28:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 08:28:23 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 08:28:23 GMT
USER user
# Wed, 28 Jan 2026 08:28:23 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b6c4248bc749950275ce15b2dff82393f4351ced2e20c7b5e2ffef3c0848ce`  
		Last Modified: Wed, 28 Jan 2026 08:29:26 GMT  
		Size: 10.3 MB (10291898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e176dad2b23e06165e59400a1ff2260014ec93b0fb3b8c7628a64e1adaf49f`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3131351fcf8ddb074fb73d582b50e94aa55e099ca06fc128b310489675e69c97`  
		Last Modified: Wed, 28 Jan 2026 08:29:26 GMT  
		Size: 6.1 MB (6064037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:165ef1cc15b3aeae45d6479f80369f8078869b953af00ad6ddb3765a55356e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7192140d2d48650b459b2a9acdce6a086c4bf08877b907f3c6bc37ce9799d3e7`

```dockerfile
```

-	Layers:
	-	`sha256:a59cb060f285e8659782eab321b072ac7afdce9472b5395d10144bca9d127b79`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 1.3 MB (1308142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e90caa10ad17b6e48ce9a44b3d010cc7b20e200cbb6ec1067441e247ce555fc`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:e55dc3c7ee83af6ee968373464f0b874c0d9149e01ce32f4680a83b5791d2ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21334391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a042dac64e240c543befef410a12767f4051b627b63028b597010c108714083`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:52 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:19:52 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:19:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:19:52 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:19:52 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:20:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:20:14 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:20:14 GMT
USER user
# Wed, 28 Jan 2026 02:20:14 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e174cb7156ade2e31408909452271b26ae4f143ef276276f0f448b1bad2165`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 11.4 MB (11405107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2a6b19294dd14e5551b394d76102c59c84eae810434dca5ae909a1e58da672`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faba483b2b5362b1905ca82789be9c963c7fde3135033f6aac9183937e5d9161`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 6.2 MB (6202965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:05475f6695b9e4e1863216bdc5de6a1a24bfec2a5baecd06f9a7bc6cd0d17408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3183ed0bc53cc736e214c57eaef2cb864de7e9dbaccf5fe0a5530c72247ac1ab`

```dockerfile
```

-	Layers:
	-	`sha256:c63a0479be024622dc272c05215babf54e4fc3b5c5ab3d053c0dcf2de80483cb`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 1.3 MB (1308088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5037cc7aa93ea1e1f234114cc48a82216f93fe0b9ee46a01ee9a03609cbe19e`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 17.5 KB (17499 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine3.23`

```console
$ docker pull irssi@sha256:bc9744c4e1f3c9e4401ee35e73ff4f7c97683f5c784c5cce21910e488a4ee219
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
$ docker pull irssi@sha256:84665fb63540b0ca94547800ed0093cb97d41e1cbc0d2aa823a67e6af91fe8ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20784026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6645503b9d588217c1fb06c9a2d7e278a4360e4aa22e92d8ff0af44ac2c6c10`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:47 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:17:47 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:17:47 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:17:47 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:17:47 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:18:00 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:18:00 GMT
USER user
# Wed, 28 Jan 2026 02:18:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d65c05b32f228b7007340211a175e100ca3ddb33a7e2c44b15d11799a9a84ad`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 10.9 MB (10857996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082c32a8914140e457d67603de3b04ccc66e688baed84d8d500f40dc885ef27a`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93abf1ed0403fdbc85fa021598a1202b3d9b55bd9d785457b554af6b86fc7d`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 6.1 MB (6063223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:7bd9c1f9350891fb6e79ac3dc4d7686c1c714bb2c12147cb089864d19ef3bc9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e29e513927a47425fe64b68ba4eeb03593581de0692a732211bc7b11537936`

```dockerfile
```

-	Layers:
	-	`sha256:5d4ee629f31bfb597346562d7da53858808c502ca6820fb40a7c347520afebad`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 1.3 MB (1308739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b9c1c09e72415a3ca7367aec0652ca69a856b8c6a57ef69ba919d208498b76`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; arm variant v6

```console
$ docker pull irssi@sha256:9a8babd75444eea65ebe3a06627eceb16f4d50aec2da2998fd3a611d75ed5b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19539552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04e50bc1d87804658a7d29a7ebb00b20d1a22d6d21cd19f5eff93f84035eb0b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:23:56 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:23:57 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:23:57 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:23:57 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:23:57 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:24:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:24:17 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:24:17 GMT
USER user
# Wed, 28 Jan 2026 02:24:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d5c4e6a80a684ff34083f2ded6ae6a1b0f08ded4c8c5b0967f8b209ee2cd80`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 10.1 MB (10075626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93db171eca68243a4f689b5400ef3c2ac2a1074f1eae1f9f0d049506c8756fe`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23c8c890839d95ebaf447485d8492d089fc8fa23d1ca65c6349a41ac95bc961`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 5.9 MB (5893116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:424e17d1ca73b3f1d92e5d0c0b7272bbaeee943cc673a2249f0bf7ca99eeedde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e7bd514eeda8663e46d4eeed484d7df02209f60112393607269af3e2c0430c`

```dockerfile
```

-	Layers:
	-	`sha256:8fbda3c9e4c0ad20ecba339d117fab2e86108fcfe33cbba7f8ddc3053d6bc89a`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; arm variant v7

```console
$ docker pull irssi@sha256:42ff91c7e5cb5046e91c18adce476ce64e5d772ab658a70c9df46e592b10ce82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18828366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ac84c98bbbaf189bedd8109f71397874c887df2e4eb32123f05470b88358b5`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:21 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:22:22 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:22:22 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:22:22 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:22:22 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:22:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:22:37 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:22:37 GMT
USER user
# Wed, 28 Jan 2026 02:22:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132ae8f3941338d2191aad9429d0bd185ceeb7aeedb8fddf43adad6b57e3273e`  
		Last Modified: Wed, 28 Jan 2026 02:22:45 GMT  
		Size: 9.9 MB (9902405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770acb73451dc424aeb5afcad4a4882f5d765fcbcc8b659b8841bf77d8166afe`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda40971fe170d5e56e81f398ba01d1904a08b07386da11fe56b125109dd60b9`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 5.6 MB (5643252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:fcebcd556b705ae5c410e6b569b01096b561714c5c2fc1d7c8c746decaeef0bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1328781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d61d96801a2a79a245717287e0380350d8e1b0c44936b6dcaf8429b0e2074bab`

```dockerfile
```

-	Layers:
	-	`sha256:e0caf0a4bbae914fea3e8ffab5d1f1752e3fc858d38e993806dd2b78f6919657`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 1.3 MB (1311147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fda69d589c766de3e44adc56d464708c1c2090577cfe6fdd9a50f95229a2c4fa`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:c53ef5cb4c4fb78d4ffdaad1b902adc24327fb49d4ad5c6d719dcf26f8e1ceba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20927195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7538037fb15131e4b2540ac0e275393593929c95a1ca622c94e6c70d99874f28`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:48 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:17:48 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:17:48 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:17:48 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:17:48 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:18:00 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:18:00 GMT
USER user
# Wed, 28 Jan 2026 02:18:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628108c2cc8068dbd74588362d3734d7b6b306883916eb33cb53af667c096440`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 10.8 MB (10792790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9361ffc4206f8e272dc8adc782da4ab39f3b1fe287c6dfb23c57814cf1e94439`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7efe759a9de929b3a25440ff73ac10595ac218ae5d0a087f34fa385d7db181f`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 5.9 MB (5936327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:ac959328037122478f2c09228cf4478f1c099d3257efec2dae9823db1d16b2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db6c23ab4cfc36c7b70e7f4325b9bfa25d1a31a205c632f8e25757cb01f7cef`

```dockerfile
```

-	Layers:
	-	`sha256:3b09e8c286f81074ecdbaaeccccef453ddf9951ff459e4c086e01b8968fe3b0e`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 1.3 MB (1308193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57974d8beacb812f7bb8f7b52301ddd6a66eb7f4c851dcc2ee58f100ec0208b1`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 17.7 KB (17682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; 386

```console
$ docker pull irssi@sha256:a32c16d5607a49617e8d077ec1f9ba5b53b0001a5d70805f183e27ac8f377955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20225669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7946f5f999880045f35ea6c3b7115f7cc7ca872f2653f90c5b0a114ea701599b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:14 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:16:14 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:16:14 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:16:14 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:16:14 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:16:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:16:34 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:16:34 GMT
USER user
# Wed, 28 Jan 2026 02:16:34 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50882b3c493b99635b6de6cd7279fc00a7df160e84cd53399664993828611810`  
		Last Modified: Wed, 28 Jan 2026 02:16:41 GMT  
		Size: 10.4 MB (10393535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7588c02c444f10953a0f0aac9fa979fe4a835bbefde822557708fbd3d21750de`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7dcb0c68d5a17e86130988d6ddf97978ae4c3d866b099962426d869a1c1fc3`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 6.1 MB (6144150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:b77b6da6595a9c4ebfe003d3192b1a97bd9a14f1fe19417ad4a8d7068acc0505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16f268d469cb9fcc79cb87b83fdcbadb9fa6818bf4d9c56a441df0e015c2ec6`

```dockerfile
```

-	Layers:
	-	`sha256:1ddc13011deb856a736a8c90df7acab1227398d8a2ae9e4586daa141365096b4`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 1.3 MB (1308694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47e26778e3f506818fa4ed452e58334a8e15701f1d896ec8ed2ff3288ca7ecef`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; ppc64le

```console
$ docker pull irssi@sha256:b40803da860e141ec3ab2320cf224c304aa870a9a884cb362b69e74b6fd82b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21272396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a2c6a98e5b7978e9d4671908d2864a8d58c1b872e5ec279f9a7a67312f3e2b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:32:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:32:11 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:32:11 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:32:11 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:32:11 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:32:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:32:31 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:32:31 GMT
USER user
# Wed, 28 Jan 2026 02:32:31 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc81a5350f307da5c9651178208c0aa789db44da9179ac834ac469d70ce42cc`  
		Last Modified: Wed, 28 Jan 2026 02:32:51 GMT  
		Size: 11.1 MB (11079608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e505a6cbf58cbc8474040a9d448a79cab0812b78e3b1c6db13e87987f8e4d9a0`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3296179391416e1833f722cc60f06d3ee4df4255177c36a2f41a35a6ab2661b`  
		Last Modified: Wed, 28 Jan 2026 02:32:51 GMT  
		Size: 6.4 MB (6362158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:e2ead2561551ba2a279d799d266e484e986d5370478af7155036333e682a1a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551e8fca5526f8aa868ce90e80d554f73ff2800bcf6fb3b0fb1b9013223228b5`

```dockerfile
```

-	Layers:
	-	`sha256:890481868cc7de496dcdc1f70cc0d6026227efccdd40466a57aa43304c3e345f`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 1.3 MB (1308146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9fac81ff985d048567933403c842b1d477306de718e7d5226612b3cb1eb068`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; riscv64

```console
$ docker pull irssi@sha256:a29b54bd9ab139f5c60185ee85db0a602092a6821866cad82df0fb45368c398c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19942208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9176875f86f8abf3bc20c65b42847d911af0be7e5863f4d6dcbd526719132c`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 08:24:33 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 08:24:34 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 08:24:34 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 08:24:34 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 08:24:34 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 08:28:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 08:28:23 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 08:28:23 GMT
USER user
# Wed, 28 Jan 2026 08:28:23 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b6c4248bc749950275ce15b2dff82393f4351ced2e20c7b5e2ffef3c0848ce`  
		Last Modified: Wed, 28 Jan 2026 08:29:26 GMT  
		Size: 10.3 MB (10291898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e176dad2b23e06165e59400a1ff2260014ec93b0fb3b8c7628a64e1adaf49f`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3131351fcf8ddb074fb73d582b50e94aa55e099ca06fc128b310489675e69c97`  
		Last Modified: Wed, 28 Jan 2026 08:29:26 GMT  
		Size: 6.1 MB (6064037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:165ef1cc15b3aeae45d6479f80369f8078869b953af00ad6ddb3765a55356e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7192140d2d48650b459b2a9acdce6a086c4bf08877b907f3c6bc37ce9799d3e7`

```dockerfile
```

-	Layers:
	-	`sha256:a59cb060f285e8659782eab321b072ac7afdce9472b5395d10144bca9d127b79`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 1.3 MB (1308142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e90caa10ad17b6e48ce9a44b3d010cc7b20e200cbb6ec1067441e247ce555fc`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; s390x

```console
$ docker pull irssi@sha256:e55dc3c7ee83af6ee968373464f0b874c0d9149e01ce32f4680a83b5791d2ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21334391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a042dac64e240c543befef410a12767f4051b627b63028b597010c108714083`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:52 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:19:52 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:19:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:19:52 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:19:52 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:20:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:20:14 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:20:14 GMT
USER user
# Wed, 28 Jan 2026 02:20:14 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e174cb7156ade2e31408909452271b26ae4f143ef276276f0f448b1bad2165`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 11.4 MB (11405107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2a6b19294dd14e5551b394d76102c59c84eae810434dca5ae909a1e58da672`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faba483b2b5362b1905ca82789be9c963c7fde3135033f6aac9183937e5d9161`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 6.2 MB (6202965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:05475f6695b9e4e1863216bdc5de6a1a24bfec2a5baecd06f9a7bc6cd0d17408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3183ed0bc53cc736e214c57eaef2cb864de7e9dbaccf5fe0a5530c72247ac1ab`

```dockerfile
```

-	Layers:
	-	`sha256:c63a0479be024622dc272c05215babf54e4fc3b5c5ab3d053c0dcf2de80483cb`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 1.3 MB (1308088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5037cc7aa93ea1e1f234114cc48a82216f93fe0b9ee46a01ee9a03609cbe19e`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 17.5 KB (17499 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-trixie`

```console
$ docker pull irssi@sha256:6f18ede25b4d4593ab99544ab52277a4e1254f2fbe6a64def5eb7de58074fffc
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
$ docker pull irssi@sha256:49c3737149b22851a93ba69ac22cebd9abf8c8a5d5994e2ca286860caf15353a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53871168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f752e1dfe12c027448c72cd5e3229ea7002dea38239febe081da26b8f7b27ed3`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:03:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:03:00 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:03:00 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:03:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:03:41 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:03:41 GMT
USER user
# Tue, 24 Feb 2026 19:03:41 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7ad25661c3266880a3c864c64ca6faa3b88c0ddb4a998a667e1f1d4b99a22d`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 19.2 MB (19222246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc80a3f9407efa5dcf0dc0ba37f425c82a6ecff60485ff89dd844390ff01a53`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d808574b07af61087631c143ffb9e4be37c1313e4d6fb331c97d17da0f436b32`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 4.9 MB (4866927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:abd6aeef322973ea82182a219b2ba14441f100be5d532e6f7b52e6062bc15a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979b803961d56ac53e2960a4847046894c3f5095836cf0aa2fd343e0288e1e0e`

```dockerfile
```

-	Layers:
	-	`sha256:3557d7d8d5e4df3d7ade5b19b149d56205ce87989a1066808f14bcf3f4321be4`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 5.6 MB (5588475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94196f7468e34a70daa83619d0cf5061ae5adf7711aca144d3d43fc9475a48da`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:6887b2daf7a8e04420d9f8019955beefca4b05d2370737f5085f12f8bb863c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50955082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82db261419aa9d562d5751330a1b61cd4d76e7c5028123921b370b072d4e9c19`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:59:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 18:59:28 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 18:59:28 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 18:59:28 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 18:59:28 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:00:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:00:20 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:00:20 GMT
USER user
# Tue, 24 Feb 2026 19:00:20 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7364bcc76ebade3ad468fc97fcab1317a1b01976383c65ec8f166e9828038c67`  
		Last Modified: Tue, 24 Feb 2026 19:00:34 GMT  
		Size: 18.3 MB (18294280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d702d54a8b971c044db6fb77d45b0c781dbb99062e9faf1a81743c47fc56bf`  
		Last Modified: Tue, 24 Feb 2026 19:00:31 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b41ba1be7d2ca3c964a8be01ccc30e64cc8a0ca03702c32d5870d2d3d769bb`  
		Last Modified: Tue, 24 Feb 2026 19:00:35 GMT  
		Size: 4.7 MB (4709832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:9ec580a8a2c10e1b7ac74c5a41f66009751caa3a8d2b0dc76ce73021e5457329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3590dbb7640207ebd9aa49bf6c514655778ebcc0dea1bf38fe7da73c02990d03`

```dockerfile
```

-	Layers:
	-	`sha256:93ef4bd1a5d0d962b395d82efceb8f97a7d23f4cd0a74978d0edd9456835b58f`  
		Last Modified: Tue, 24 Feb 2026 19:00:31 GMT  
		Size: 5.6 MB (5586024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:025639689d36438751d0440bf57caefab23fbf1a4e77b9cc3febff3196f2a2b9`  
		Last Modified: Tue, 24 Feb 2026 19:00:31 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:e65224016b946c4d99129fad9314bdbdc0bf0296df171d4ce13bc5aa24cb6cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48688484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9c173ed818b8888f5cbf8f2e9258855675b8dd27c9cb7908c704a1d3069397`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:03:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:03:16 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:03:16 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:03:16 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:03:16 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:03:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:03:58 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:03:58 GMT
USER user
# Tue, 24 Feb 2026 19:03:58 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6afde1291a25c0cc231ccde29bbe0ad9ff81c712d4e11e050becb6d4ba8ce0d`  
		Last Modified: Tue, 24 Feb 2026 19:04:08 GMT  
		Size: 17.9 MB (17913151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b8f6d599a61d91e34fb4362460af69da8f684fd2226c0a12c37f1fee9652b8`  
		Last Modified: Tue, 24 Feb 2026 19:04:07 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4575a9012f56ba332b5c7534e48f48a25065b112fa4613e17f2d061261eb8e13`  
		Last Modified: Tue, 24 Feb 2026 19:04:08 GMT  
		Size: 4.6 MB (4558224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:578b6038b34fa00900a70d96abebf8df03f41cbef32e270af68c766ed6703f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9176d67dd016c9ba37147b21f657ef2ae76348260f1f72189b8dc548007b5a73`

```dockerfile
```

-	Layers:
	-	`sha256:cca03ae28695eb959e228e35c2e861a53e15134500b965d0f79e67be15a1cf50`  
		Last Modified: Tue, 24 Feb 2026 19:04:08 GMT  
		Size: 5.6 MB (5589046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dade344df2087c2cbe360a19c02237de12027a28b597247bd6d4844a90a5dad`  
		Last Modified: Tue, 24 Feb 2026 19:04:07 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:b5705a932a1071d49bc33cb793e6492a17f0c13a09af00c00847132826a5399d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53975047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95271ad57b650f4906bebb73ced93170cb93cdc9485991098fde0de3c6ac7f3b`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:06:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:06:10 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:06:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:06:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:06:46 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:06:46 GMT
USER user
# Tue, 24 Feb 2026 19:06:46 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bde18e6576dd26665639dfee2e2c29ab72d5a490303fa301ad8b6d16d01032`  
		Last Modified: Tue, 24 Feb 2026 19:06:58 GMT  
		Size: 19.1 MB (19050073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb0f26017633de6d20b077a7d5fbc6cc2e5ca7a1231309bb6d18d9c6914a55b`  
		Last Modified: Tue, 24 Feb 2026 19:06:57 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5666611ba24e987a94791ca84b6bb380525795696e072f0d60ba9d17ade814ef`  
		Last Modified: Tue, 24 Feb 2026 19:06:57 GMT  
		Size: 4.8 MB (4781514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:900b2ed2e203d81d8f8d6a5cd524d2db8b91bd6962cbb74ffcb0d2a396647107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136a2b4c868d58cd89f9de10c7f831de5ff64687d2b3f76d4e7c01b8ffa16584`

```dockerfile
```

-	Layers:
	-	`sha256:2fef361a887b7785b6efd16d1c15d0262f2f2c6d45edab1f8a975ba81b6f1fdd`  
		Last Modified: Tue, 24 Feb 2026 19:06:57 GMT  
		Size: 5.6 MB (5594959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb64f6057abd305766916ed63546cbd132d825a2da5422247487175382c5f5b9`  
		Last Modified: Tue, 24 Feb 2026 19:06:57 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; 386

```console
$ docker pull irssi@sha256:47a406a29379abd6ed06b0d20217433e973e2870d780ff30823782f31e5c6b33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54908577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91e586aa3e8ce17d01aee6359c922ffe41daa80e277df7ae8ed8d1889e1bb0b`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:58:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 18:58:30 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 18:58:30 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 18:58:30 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 18:58:30 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 18:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 18:59:11 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 18:59:11 GMT
USER user
# Tue, 24 Feb 2026 18:59:11 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ae61c08fa4b2cc99f86dc6a1fe4823c3e0ac9a711287f64cac6485a6238ac8`  
		Last Modified: Tue, 24 Feb 2026 18:59:21 GMT  
		Size: 18.7 MB (18742816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf3f98a9e73f8a6e5b1989e717a2286e372230bcaff62941bae689905197df8`  
		Last Modified: Tue, 24 Feb 2026 18:59:20 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a297182723d0165449b463b3d8873cf3e889a114d50096866c842a8e640504`  
		Last Modified: Tue, 24 Feb 2026 18:59:21 GMT  
		Size: 4.9 MB (4868483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:6c462d49b091009b00485bef9ea87abfab3cb1639844d8c0ed87db6e3e81f5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ff00c0c6b361160a520647c72a3cf1d9322aed6a3382745d35d0d05d128d4e`

```dockerfile
```

-	Layers:
	-	`sha256:b4fd1d01133f85b3efcc51e3d12301590bbb5fb57101916a792336a8d1dea592`  
		Last Modified: Tue, 24 Feb 2026 18:59:21 GMT  
		Size: 5.6 MB (5584598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00eea56a9297862479d3e58a1bd8c833d2a522ff54655c30af9634f5c984d84d`  
		Last Modified: Tue, 24 Feb 2026 18:59:20 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:91b49338a181c6d7b1ae5689c2a610af4dcb438d1eb567f96160219d271063f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58240333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4fc70f04320b975862b6d37425c6f5766d3f6c2e97e62049747274abf47acc`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:07:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:07:22 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:07:22 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:07:22 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:07:22 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:09:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:09:16 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:09:16 GMT
USER user
# Tue, 24 Feb 2026 19:09:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5beebebe5029aabb929ae44c4537e3b21fd8d65921a409bb2df1b7c9b634b6d`  
		Last Modified: Tue, 24 Feb 2026 19:09:44 GMT  
		Size: 19.5 MB (19538939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed570b0aeb97d8cb44da9c8850814c6aa7e1b43fe3d9f4058d9d5a52f0eb6224`  
		Last Modified: Tue, 24 Feb 2026 19:09:43 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ecef354c37ad21cbe5f6e442c1f3c79f858cd86e1ece389542887cae1cff44d`  
		Last Modified: Tue, 24 Feb 2026 19:09:43 GMT  
		Size: 5.1 MB (5097820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:38354f39cc3e23ea94d1feaca94d6602908c74c9dbd5beddfeeb5bd33866538a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904a8b4a8a183068c5d6db74160bbb18d87a4c74f95375cf320b45143257753e`

```dockerfile
```

-	Layers:
	-	`sha256:4c2d2dc5bef56d23df0cb5b905d48dc667fb78e0a3c3a168e9e8a3a4f7f1b318`  
		Last Modified: Tue, 24 Feb 2026 19:09:43 GMT  
		Size: 5.6 MB (5595506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:373385b6bc18ef5a4933f2dfe5147cd4368d7f2730b1f214cd1abe2372ffb0d2`  
		Last Modified: Tue, 24 Feb 2026 19:09:43 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:3a7d38a48cd82c9bd2d5741f468dcdfbf92e333ecc06c2d12dbfe8b938ab0307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51693147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0a99e5b7cd8d4f262722aed889c863e4c892a0f23fe9749d929e8dec75cf662`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 03:03:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 03:03:38 GMT
ENV HOME=/home/user
# Wed, 25 Feb 2026 03:03:38 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 25 Feb 2026 03:03:38 GMT
ENV LANG=C.UTF-8
# Wed, 25 Feb 2026 03:03:38 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 25 Feb 2026 03:10:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 25 Feb 2026 03:10:25 GMT
WORKDIR /home/user
# Wed, 25 Feb 2026 03:10:25 GMT
USER user
# Wed, 25 Feb 2026 03:10:25 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6508c3cdfc31f498c772515ee0821b13440e08ba735c32d3cba318269a3f687`  
		Last Modified: Wed, 25 Feb 2026 03:12:21 GMT  
		Size: 18.6 MB (18552692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ef556a8959335b7e794bf6752b54a81934178688ef1e7d4dbdb197aa0eb326`  
		Last Modified: Wed, 25 Feb 2026 03:12:16 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2794c755bfc5dceb9c6a1eb2ff258465b48801c3bd877b5cde6f46d9920a5c`  
		Last Modified: Wed, 25 Feb 2026 03:12:18 GMT  
		Size: 4.9 MB (4860678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:5ad91e36e6745d334569f2aede71764aa6ab0c8d2ed12405c01d1a981287b5ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ebcaf2e72424c63e04d825e7d04bbe5589f3f805c573faf9c8484afea2b540f`

```dockerfile
```

-	Layers:
	-	`sha256:5c3be456f6ce9090fac8cee71f4291c1aaef1a9ac164f8e2bd0de699367a6334`  
		Last Modified: Wed, 25 Feb 2026 03:12:18 GMT  
		Size: 5.6 MB (5579778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9be1a19638d1af3b7539195ea9d207d142146b312fe552361ffde9b48f90de25`  
		Last Modified: Wed, 25 Feb 2026 03:12:16 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; s390x

```console
$ docker pull irssi@sha256:9d2c67d051b5f92f329619102e0e2bc0df643ef026d1f553c93d501eb54b0049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54516690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf87075c86e270be08f7350f9904070bb3c572934e47a6d6aa9e70fefbff3812`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:01:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:01:50 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:01:50 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:01:50 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:01:50 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:03:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:03:57 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:03:57 GMT
USER user
# Tue, 24 Feb 2026 19:03:57 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb8e7c85a43a84dc9bfa10f335db4cb6dbd00571742698dd7d26077875d9a48`  
		Last Modified: Tue, 24 Feb 2026 19:04:25 GMT  
		Size: 19.8 MB (19768672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e12ffbdb3791dcf1981e8eefcf126275f55fe052fac3a8fafc881aac17c34d8`  
		Last Modified: Tue, 24 Feb 2026 19:04:24 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149d77b47e1605f5cda1129f653ed9adbc0c8c0c2286fd9e81c91c6c44d32956`  
		Last Modified: Tue, 24 Feb 2026 19:04:25 GMT  
		Size: 4.9 MB (4906478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:d10e5a37df33b885dd47403b1e8b7a310eb535821e3b44695a144c5fb72da92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b0fb8133b9ed0bb88f527230ee5b7eefff618321781bea5b846e5b8d1ea2a2`

```dockerfile
```

-	Layers:
	-	`sha256:9ab81d1d85995cb9010ed56d4fdb909af0e66dc54953575d97300c5e3eb22dbe`  
		Last Modified: Tue, 24 Feb 2026 19:04:24 GMT  
		Size: 5.6 MB (5589380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5cb68be6babc8fbd8fc9be84183610c6d3f88b4fb466e15ef8526dfead89283`  
		Last Modified: Tue, 24 Feb 2026 19:04:24 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4`

```console
$ docker pull irssi@sha256:6f18ede25b4d4593ab99544ab52277a4e1254f2fbe6a64def5eb7de58074fffc
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
$ docker pull irssi@sha256:49c3737149b22851a93ba69ac22cebd9abf8c8a5d5994e2ca286860caf15353a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53871168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f752e1dfe12c027448c72cd5e3229ea7002dea38239febe081da26b8f7b27ed3`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:03:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:03:00 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:03:00 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:03:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:03:41 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:03:41 GMT
USER user
# Tue, 24 Feb 2026 19:03:41 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7ad25661c3266880a3c864c64ca6faa3b88c0ddb4a998a667e1f1d4b99a22d`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 19.2 MB (19222246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc80a3f9407efa5dcf0dc0ba37f425c82a6ecff60485ff89dd844390ff01a53`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d808574b07af61087631c143ffb9e4be37c1313e4d6fb331c97d17da0f436b32`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 4.9 MB (4866927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:abd6aeef322973ea82182a219b2ba14441f100be5d532e6f7b52e6062bc15a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979b803961d56ac53e2960a4847046894c3f5095836cf0aa2fd343e0288e1e0e`

```dockerfile
```

-	Layers:
	-	`sha256:3557d7d8d5e4df3d7ade5b19b149d56205ce87989a1066808f14bcf3f4321be4`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 5.6 MB (5588475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94196f7468e34a70daa83619d0cf5061ae5adf7711aca144d3d43fc9475a48da`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v5

```console
$ docker pull irssi@sha256:6887b2daf7a8e04420d9f8019955beefca4b05d2370737f5085f12f8bb863c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50955082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82db261419aa9d562d5751330a1b61cd4d76e7c5028123921b370b072d4e9c19`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:59:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 18:59:28 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 18:59:28 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 18:59:28 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 18:59:28 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:00:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:00:20 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:00:20 GMT
USER user
# Tue, 24 Feb 2026 19:00:20 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7364bcc76ebade3ad468fc97fcab1317a1b01976383c65ec8f166e9828038c67`  
		Last Modified: Tue, 24 Feb 2026 19:00:34 GMT  
		Size: 18.3 MB (18294280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d702d54a8b971c044db6fb77d45b0c781dbb99062e9faf1a81743c47fc56bf`  
		Last Modified: Tue, 24 Feb 2026 19:00:31 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b41ba1be7d2ca3c964a8be01ccc30e64cc8a0ca03702c32d5870d2d3d769bb`  
		Last Modified: Tue, 24 Feb 2026 19:00:35 GMT  
		Size: 4.7 MB (4709832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:9ec580a8a2c10e1b7ac74c5a41f66009751caa3a8d2b0dc76ce73021e5457329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3590dbb7640207ebd9aa49bf6c514655778ebcc0dea1bf38fe7da73c02990d03`

```dockerfile
```

-	Layers:
	-	`sha256:93ef4bd1a5d0d962b395d82efceb8f97a7d23f4cd0a74978d0edd9456835b58f`  
		Last Modified: Tue, 24 Feb 2026 19:00:31 GMT  
		Size: 5.6 MB (5586024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:025639689d36438751d0440bf57caefab23fbf1a4e77b9cc3febff3196f2a2b9`  
		Last Modified: Tue, 24 Feb 2026 19:00:31 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v7

```console
$ docker pull irssi@sha256:e65224016b946c4d99129fad9314bdbdc0bf0296df171d4ce13bc5aa24cb6cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48688484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9c173ed818b8888f5cbf8f2e9258855675b8dd27c9cb7908c704a1d3069397`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:03:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:03:16 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:03:16 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:03:16 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:03:16 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:03:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:03:58 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:03:58 GMT
USER user
# Tue, 24 Feb 2026 19:03:58 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6afde1291a25c0cc231ccde29bbe0ad9ff81c712d4e11e050becb6d4ba8ce0d`  
		Last Modified: Tue, 24 Feb 2026 19:04:08 GMT  
		Size: 17.9 MB (17913151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b8f6d599a61d91e34fb4362460af69da8f684fd2226c0a12c37f1fee9652b8`  
		Last Modified: Tue, 24 Feb 2026 19:04:07 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4575a9012f56ba332b5c7534e48f48a25065b112fa4613e17f2d061261eb8e13`  
		Last Modified: Tue, 24 Feb 2026 19:04:08 GMT  
		Size: 4.6 MB (4558224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:578b6038b34fa00900a70d96abebf8df03f41cbef32e270af68c766ed6703f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9176d67dd016c9ba37147b21f657ef2ae76348260f1f72189b8dc548007b5a73`

```dockerfile
```

-	Layers:
	-	`sha256:cca03ae28695eb959e228e35c2e861a53e15134500b965d0f79e67be15a1cf50`  
		Last Modified: Tue, 24 Feb 2026 19:04:08 GMT  
		Size: 5.6 MB (5589046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dade344df2087c2cbe360a19c02237de12027a28b597247bd6d4844a90a5dad`  
		Last Modified: Tue, 24 Feb 2026 19:04:07 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:b5705a932a1071d49bc33cb793e6492a17f0c13a09af00c00847132826a5399d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53975047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95271ad57b650f4906bebb73ced93170cb93cdc9485991098fde0de3c6ac7f3b`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:06:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:06:10 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:06:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:06:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:06:46 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:06:46 GMT
USER user
# Tue, 24 Feb 2026 19:06:46 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bde18e6576dd26665639dfee2e2c29ab72d5a490303fa301ad8b6d16d01032`  
		Last Modified: Tue, 24 Feb 2026 19:06:58 GMT  
		Size: 19.1 MB (19050073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb0f26017633de6d20b077a7d5fbc6cc2e5ca7a1231309bb6d18d9c6914a55b`  
		Last Modified: Tue, 24 Feb 2026 19:06:57 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5666611ba24e987a94791ca84b6bb380525795696e072f0d60ba9d17ade814ef`  
		Last Modified: Tue, 24 Feb 2026 19:06:57 GMT  
		Size: 4.8 MB (4781514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:900b2ed2e203d81d8f8d6a5cd524d2db8b91bd6962cbb74ffcb0d2a396647107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136a2b4c868d58cd89f9de10c7f831de5ff64687d2b3f76d4e7c01b8ffa16584`

```dockerfile
```

-	Layers:
	-	`sha256:2fef361a887b7785b6efd16d1c15d0262f2f2c6d45edab1f8a975ba81b6f1fdd`  
		Last Modified: Tue, 24 Feb 2026 19:06:57 GMT  
		Size: 5.6 MB (5594959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb64f6057abd305766916ed63546cbd132d825a2da5422247487175382c5f5b9`  
		Last Modified: Tue, 24 Feb 2026 19:06:57 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; 386

```console
$ docker pull irssi@sha256:47a406a29379abd6ed06b0d20217433e973e2870d780ff30823782f31e5c6b33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54908577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91e586aa3e8ce17d01aee6359c922ffe41daa80e277df7ae8ed8d1889e1bb0b`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:58:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 18:58:30 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 18:58:30 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 18:58:30 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 18:58:30 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 18:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 18:59:11 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 18:59:11 GMT
USER user
# Tue, 24 Feb 2026 18:59:11 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ae61c08fa4b2cc99f86dc6a1fe4823c3e0ac9a711287f64cac6485a6238ac8`  
		Last Modified: Tue, 24 Feb 2026 18:59:21 GMT  
		Size: 18.7 MB (18742816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf3f98a9e73f8a6e5b1989e717a2286e372230bcaff62941bae689905197df8`  
		Last Modified: Tue, 24 Feb 2026 18:59:20 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a297182723d0165449b463b3d8873cf3e889a114d50096866c842a8e640504`  
		Last Modified: Tue, 24 Feb 2026 18:59:21 GMT  
		Size: 4.9 MB (4868483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:6c462d49b091009b00485bef9ea87abfab3cb1639844d8c0ed87db6e3e81f5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ff00c0c6b361160a520647c72a3cf1d9322aed6a3382745d35d0d05d128d4e`

```dockerfile
```

-	Layers:
	-	`sha256:b4fd1d01133f85b3efcc51e3d12301590bbb5fb57101916a792336a8d1dea592`  
		Last Modified: Tue, 24 Feb 2026 18:59:21 GMT  
		Size: 5.6 MB (5584598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00eea56a9297862479d3e58a1bd8c833d2a522ff54655c30af9634f5c984d84d`  
		Last Modified: Tue, 24 Feb 2026 18:59:20 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; ppc64le

```console
$ docker pull irssi@sha256:91b49338a181c6d7b1ae5689c2a610af4dcb438d1eb567f96160219d271063f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58240333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4fc70f04320b975862b6d37425c6f5766d3f6c2e97e62049747274abf47acc`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:07:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:07:22 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:07:22 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:07:22 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:07:22 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:09:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:09:16 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:09:16 GMT
USER user
# Tue, 24 Feb 2026 19:09:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5beebebe5029aabb929ae44c4537e3b21fd8d65921a409bb2df1b7c9b634b6d`  
		Last Modified: Tue, 24 Feb 2026 19:09:44 GMT  
		Size: 19.5 MB (19538939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed570b0aeb97d8cb44da9c8850814c6aa7e1b43fe3d9f4058d9d5a52f0eb6224`  
		Last Modified: Tue, 24 Feb 2026 19:09:43 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ecef354c37ad21cbe5f6e442c1f3c79f858cd86e1ece389542887cae1cff44d`  
		Last Modified: Tue, 24 Feb 2026 19:09:43 GMT  
		Size: 5.1 MB (5097820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:38354f39cc3e23ea94d1feaca94d6602908c74c9dbd5beddfeeb5bd33866538a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904a8b4a8a183068c5d6db74160bbb18d87a4c74f95375cf320b45143257753e`

```dockerfile
```

-	Layers:
	-	`sha256:4c2d2dc5bef56d23df0cb5b905d48dc667fb78e0a3c3a168e9e8a3a4f7f1b318`  
		Last Modified: Tue, 24 Feb 2026 19:09:43 GMT  
		Size: 5.6 MB (5595506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:373385b6bc18ef5a4933f2dfe5147cd4368d7f2730b1f214cd1abe2372ffb0d2`  
		Last Modified: Tue, 24 Feb 2026 19:09:43 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; riscv64

```console
$ docker pull irssi@sha256:3a7d38a48cd82c9bd2d5741f468dcdfbf92e333ecc06c2d12dbfe8b938ab0307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51693147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0a99e5b7cd8d4f262722aed889c863e4c892a0f23fe9749d929e8dec75cf662`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 03:03:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 03:03:38 GMT
ENV HOME=/home/user
# Wed, 25 Feb 2026 03:03:38 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 25 Feb 2026 03:03:38 GMT
ENV LANG=C.UTF-8
# Wed, 25 Feb 2026 03:03:38 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 25 Feb 2026 03:10:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 25 Feb 2026 03:10:25 GMT
WORKDIR /home/user
# Wed, 25 Feb 2026 03:10:25 GMT
USER user
# Wed, 25 Feb 2026 03:10:25 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6508c3cdfc31f498c772515ee0821b13440e08ba735c32d3cba318269a3f687`  
		Last Modified: Wed, 25 Feb 2026 03:12:21 GMT  
		Size: 18.6 MB (18552692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ef556a8959335b7e794bf6752b54a81934178688ef1e7d4dbdb197aa0eb326`  
		Last Modified: Wed, 25 Feb 2026 03:12:16 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2794c755bfc5dceb9c6a1eb2ff258465b48801c3bd877b5cde6f46d9920a5c`  
		Last Modified: Wed, 25 Feb 2026 03:12:18 GMT  
		Size: 4.9 MB (4860678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:5ad91e36e6745d334569f2aede71764aa6ab0c8d2ed12405c01d1a981287b5ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ebcaf2e72424c63e04d825e7d04bbe5589f3f805c573faf9c8484afea2b540f`

```dockerfile
```

-	Layers:
	-	`sha256:5c3be456f6ce9090fac8cee71f4291c1aaef1a9ac164f8e2bd0de699367a6334`  
		Last Modified: Wed, 25 Feb 2026 03:12:18 GMT  
		Size: 5.6 MB (5579778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9be1a19638d1af3b7539195ea9d207d142146b312fe552361ffde9b48f90de25`  
		Last Modified: Wed, 25 Feb 2026 03:12:16 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; s390x

```console
$ docker pull irssi@sha256:9d2c67d051b5f92f329619102e0e2bc0df643ef026d1f553c93d501eb54b0049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54516690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf87075c86e270be08f7350f9904070bb3c572934e47a6d6aa9e70fefbff3812`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:01:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:01:50 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:01:50 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:01:50 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:01:50 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:03:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:03:57 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:03:57 GMT
USER user
# Tue, 24 Feb 2026 19:03:57 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb8e7c85a43a84dc9bfa10f335db4cb6dbd00571742698dd7d26077875d9a48`  
		Last Modified: Tue, 24 Feb 2026 19:04:25 GMT  
		Size: 19.8 MB (19768672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e12ffbdb3791dcf1981e8eefcf126275f55fe052fac3a8fafc881aac17c34d8`  
		Last Modified: Tue, 24 Feb 2026 19:04:24 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149d77b47e1605f5cda1129f653ed9adbc0c8c0c2286fd9e81c91c6c44d32956`  
		Last Modified: Tue, 24 Feb 2026 19:04:25 GMT  
		Size: 4.9 MB (4906478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:d10e5a37df33b885dd47403b1e8b7a310eb535821e3b44695a144c5fb72da92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b0fb8133b9ed0bb88f527230ee5b7eefff618321781bea5b846e5b8d1ea2a2`

```dockerfile
```

-	Layers:
	-	`sha256:9ab81d1d85995cb9010ed56d4fdb909af0e66dc54953575d97300c5e3eb22dbe`  
		Last Modified: Tue, 24 Feb 2026 19:04:24 GMT  
		Size: 5.6 MB (5589380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5cb68be6babc8fbd8fc9be84183610c6d3f88b4fb466e15ef8526dfead89283`  
		Last Modified: Tue, 24 Feb 2026 19:04:24 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine`

```console
$ docker pull irssi@sha256:bc9744c4e1f3c9e4401ee35e73ff4f7c97683f5c784c5cce21910e488a4ee219
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
$ docker pull irssi@sha256:84665fb63540b0ca94547800ed0093cb97d41e1cbc0d2aa823a67e6af91fe8ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20784026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6645503b9d588217c1fb06c9a2d7e278a4360e4aa22e92d8ff0af44ac2c6c10`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:47 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:17:47 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:17:47 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:17:47 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:17:47 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:18:00 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:18:00 GMT
USER user
# Wed, 28 Jan 2026 02:18:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d65c05b32f228b7007340211a175e100ca3ddb33a7e2c44b15d11799a9a84ad`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 10.9 MB (10857996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082c32a8914140e457d67603de3b04ccc66e688baed84d8d500f40dc885ef27a`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93abf1ed0403fdbc85fa021598a1202b3d9b55bd9d785457b554af6b86fc7d`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 6.1 MB (6063223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:7bd9c1f9350891fb6e79ac3dc4d7686c1c714bb2c12147cb089864d19ef3bc9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e29e513927a47425fe64b68ba4eeb03593581de0692a732211bc7b11537936`

```dockerfile
```

-	Layers:
	-	`sha256:5d4ee629f31bfb597346562d7da53858808c502ca6820fb40a7c347520afebad`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 1.3 MB (1308739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b9c1c09e72415a3ca7367aec0652ca69a856b8c6a57ef69ba919d208498b76`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:9a8babd75444eea65ebe3a06627eceb16f4d50aec2da2998fd3a611d75ed5b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19539552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04e50bc1d87804658a7d29a7ebb00b20d1a22d6d21cd19f5eff93f84035eb0b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:23:56 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:23:57 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:23:57 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:23:57 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:23:57 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:24:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:24:17 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:24:17 GMT
USER user
# Wed, 28 Jan 2026 02:24:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d5c4e6a80a684ff34083f2ded6ae6a1b0f08ded4c8c5b0967f8b209ee2cd80`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 10.1 MB (10075626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93db171eca68243a4f689b5400ef3c2ac2a1074f1eae1f9f0d049506c8756fe`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23c8c890839d95ebaf447485d8492d089fc8fa23d1ca65c6349a41ac95bc961`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 5.9 MB (5893116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:424e17d1ca73b3f1d92e5d0c0b7272bbaeee943cc673a2249f0bf7ca99eeedde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e7bd514eeda8663e46d4eeed484d7df02209f60112393607269af3e2c0430c`

```dockerfile
```

-	Layers:
	-	`sha256:8fbda3c9e4c0ad20ecba339d117fab2e86108fcfe33cbba7f8ddc3053d6bc89a`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:42ff91c7e5cb5046e91c18adce476ce64e5d772ab658a70c9df46e592b10ce82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18828366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ac84c98bbbaf189bedd8109f71397874c887df2e4eb32123f05470b88358b5`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:21 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:22:22 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:22:22 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:22:22 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:22:22 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:22:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:22:37 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:22:37 GMT
USER user
# Wed, 28 Jan 2026 02:22:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132ae8f3941338d2191aad9429d0bd185ceeb7aeedb8fddf43adad6b57e3273e`  
		Last Modified: Wed, 28 Jan 2026 02:22:45 GMT  
		Size: 9.9 MB (9902405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770acb73451dc424aeb5afcad4a4882f5d765fcbcc8b659b8841bf77d8166afe`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda40971fe170d5e56e81f398ba01d1904a08b07386da11fe56b125109dd60b9`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 5.6 MB (5643252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:fcebcd556b705ae5c410e6b569b01096b561714c5c2fc1d7c8c746decaeef0bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1328781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d61d96801a2a79a245717287e0380350d8e1b0c44936b6dcaf8429b0e2074bab`

```dockerfile
```

-	Layers:
	-	`sha256:e0caf0a4bbae914fea3e8ffab5d1f1752e3fc858d38e993806dd2b78f6919657`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 1.3 MB (1311147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fda69d589c766de3e44adc56d464708c1c2090577cfe6fdd9a50f95229a2c4fa`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:c53ef5cb4c4fb78d4ffdaad1b902adc24327fb49d4ad5c6d719dcf26f8e1ceba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20927195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7538037fb15131e4b2540ac0e275393593929c95a1ca622c94e6c70d99874f28`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:48 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:17:48 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:17:48 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:17:48 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:17:48 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:18:00 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:18:00 GMT
USER user
# Wed, 28 Jan 2026 02:18:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628108c2cc8068dbd74588362d3734d7b6b306883916eb33cb53af667c096440`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 10.8 MB (10792790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9361ffc4206f8e272dc8adc782da4ab39f3b1fe287c6dfb23c57814cf1e94439`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7efe759a9de929b3a25440ff73ac10595ac218ae5d0a087f34fa385d7db181f`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 5.9 MB (5936327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:ac959328037122478f2c09228cf4478f1c099d3257efec2dae9823db1d16b2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db6c23ab4cfc36c7b70e7f4325b9bfa25d1a31a205c632f8e25757cb01f7cef`

```dockerfile
```

-	Layers:
	-	`sha256:3b09e8c286f81074ecdbaaeccccef453ddf9951ff459e4c086e01b8968fe3b0e`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 1.3 MB (1308193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57974d8beacb812f7bb8f7b52301ddd6a66eb7f4c851dcc2ee58f100ec0208b1`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 17.7 KB (17682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; 386

```console
$ docker pull irssi@sha256:a32c16d5607a49617e8d077ec1f9ba5b53b0001a5d70805f183e27ac8f377955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20225669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7946f5f999880045f35ea6c3b7115f7cc7ca872f2653f90c5b0a114ea701599b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:14 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:16:14 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:16:14 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:16:14 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:16:14 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:16:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:16:34 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:16:34 GMT
USER user
# Wed, 28 Jan 2026 02:16:34 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50882b3c493b99635b6de6cd7279fc00a7df160e84cd53399664993828611810`  
		Last Modified: Wed, 28 Jan 2026 02:16:41 GMT  
		Size: 10.4 MB (10393535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7588c02c444f10953a0f0aac9fa979fe4a835bbefde822557708fbd3d21750de`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7dcb0c68d5a17e86130988d6ddf97978ae4c3d866b099962426d869a1c1fc3`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 6.1 MB (6144150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:b77b6da6595a9c4ebfe003d3192b1a97bd9a14f1fe19417ad4a8d7068acc0505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16f268d469cb9fcc79cb87b83fdcbadb9fa6818bf4d9c56a441df0e015c2ec6`

```dockerfile
```

-	Layers:
	-	`sha256:1ddc13011deb856a736a8c90df7acab1227398d8a2ae9e4586daa141365096b4`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 1.3 MB (1308694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47e26778e3f506818fa4ed452e58334a8e15701f1d896ec8ed2ff3288ca7ecef`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:b40803da860e141ec3ab2320cf224c304aa870a9a884cb362b69e74b6fd82b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21272396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a2c6a98e5b7978e9d4671908d2864a8d58c1b872e5ec279f9a7a67312f3e2b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:32:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:32:11 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:32:11 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:32:11 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:32:11 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:32:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:32:31 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:32:31 GMT
USER user
# Wed, 28 Jan 2026 02:32:31 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc81a5350f307da5c9651178208c0aa789db44da9179ac834ac469d70ce42cc`  
		Last Modified: Wed, 28 Jan 2026 02:32:51 GMT  
		Size: 11.1 MB (11079608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e505a6cbf58cbc8474040a9d448a79cab0812b78e3b1c6db13e87987f8e4d9a0`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3296179391416e1833f722cc60f06d3ee4df4255177c36a2f41a35a6ab2661b`  
		Last Modified: Wed, 28 Jan 2026 02:32:51 GMT  
		Size: 6.4 MB (6362158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:e2ead2561551ba2a279d799d266e484e986d5370478af7155036333e682a1a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551e8fca5526f8aa868ce90e80d554f73ff2800bcf6fb3b0fb1b9013223228b5`

```dockerfile
```

-	Layers:
	-	`sha256:890481868cc7de496dcdc1f70cc0d6026227efccdd40466a57aa43304c3e345f`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 1.3 MB (1308146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9fac81ff985d048567933403c842b1d477306de718e7d5226612b3cb1eb068`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:a29b54bd9ab139f5c60185ee85db0a602092a6821866cad82df0fb45368c398c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19942208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9176875f86f8abf3bc20c65b42847d911af0be7e5863f4d6dcbd526719132c`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 08:24:33 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 08:24:34 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 08:24:34 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 08:24:34 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 08:24:34 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 08:28:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 08:28:23 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 08:28:23 GMT
USER user
# Wed, 28 Jan 2026 08:28:23 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b6c4248bc749950275ce15b2dff82393f4351ced2e20c7b5e2ffef3c0848ce`  
		Last Modified: Wed, 28 Jan 2026 08:29:26 GMT  
		Size: 10.3 MB (10291898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e176dad2b23e06165e59400a1ff2260014ec93b0fb3b8c7628a64e1adaf49f`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3131351fcf8ddb074fb73d582b50e94aa55e099ca06fc128b310489675e69c97`  
		Last Modified: Wed, 28 Jan 2026 08:29:26 GMT  
		Size: 6.1 MB (6064037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:165ef1cc15b3aeae45d6479f80369f8078869b953af00ad6ddb3765a55356e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7192140d2d48650b459b2a9acdce6a086c4bf08877b907f3c6bc37ce9799d3e7`

```dockerfile
```

-	Layers:
	-	`sha256:a59cb060f285e8659782eab321b072ac7afdce9472b5395d10144bca9d127b79`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 1.3 MB (1308142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e90caa10ad17b6e48ce9a44b3d010cc7b20e200cbb6ec1067441e247ce555fc`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:e55dc3c7ee83af6ee968373464f0b874c0d9149e01ce32f4680a83b5791d2ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21334391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a042dac64e240c543befef410a12767f4051b627b63028b597010c108714083`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:52 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:19:52 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:19:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:19:52 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:19:52 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:20:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:20:14 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:20:14 GMT
USER user
# Wed, 28 Jan 2026 02:20:14 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e174cb7156ade2e31408909452271b26ae4f143ef276276f0f448b1bad2165`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 11.4 MB (11405107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2a6b19294dd14e5551b394d76102c59c84eae810434dca5ae909a1e58da672`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faba483b2b5362b1905ca82789be9c963c7fde3135033f6aac9183937e5d9161`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 6.2 MB (6202965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:05475f6695b9e4e1863216bdc5de6a1a24bfec2a5baecd06f9a7bc6cd0d17408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3183ed0bc53cc736e214c57eaef2cb864de7e9dbaccf5fe0a5530c72247ac1ab`

```dockerfile
```

-	Layers:
	-	`sha256:c63a0479be024622dc272c05215babf54e4fc3b5c5ab3d053c0dcf2de80483cb`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 1.3 MB (1308088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5037cc7aa93ea1e1f234114cc48a82216f93fe0b9ee46a01ee9a03609cbe19e`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 17.5 KB (17499 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine3.23`

```console
$ docker pull irssi@sha256:bc9744c4e1f3c9e4401ee35e73ff4f7c97683f5c784c5cce21910e488a4ee219
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
$ docker pull irssi@sha256:84665fb63540b0ca94547800ed0093cb97d41e1cbc0d2aa823a67e6af91fe8ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20784026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6645503b9d588217c1fb06c9a2d7e278a4360e4aa22e92d8ff0af44ac2c6c10`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:47 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:17:47 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:17:47 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:17:47 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:17:47 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:18:00 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:18:00 GMT
USER user
# Wed, 28 Jan 2026 02:18:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d65c05b32f228b7007340211a175e100ca3ddb33a7e2c44b15d11799a9a84ad`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 10.9 MB (10857996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082c32a8914140e457d67603de3b04ccc66e688baed84d8d500f40dc885ef27a`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93abf1ed0403fdbc85fa021598a1202b3d9b55bd9d785457b554af6b86fc7d`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 6.1 MB (6063223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:7bd9c1f9350891fb6e79ac3dc4d7686c1c714bb2c12147cb089864d19ef3bc9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e29e513927a47425fe64b68ba4eeb03593581de0692a732211bc7b11537936`

```dockerfile
```

-	Layers:
	-	`sha256:5d4ee629f31bfb597346562d7da53858808c502ca6820fb40a7c347520afebad`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 1.3 MB (1308739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b9c1c09e72415a3ca7367aec0652ca69a856b8c6a57ef69ba919d208498b76`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; arm variant v6

```console
$ docker pull irssi@sha256:9a8babd75444eea65ebe3a06627eceb16f4d50aec2da2998fd3a611d75ed5b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19539552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04e50bc1d87804658a7d29a7ebb00b20d1a22d6d21cd19f5eff93f84035eb0b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:23:56 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:23:57 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:23:57 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:23:57 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:23:57 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:24:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:24:17 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:24:17 GMT
USER user
# Wed, 28 Jan 2026 02:24:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d5c4e6a80a684ff34083f2ded6ae6a1b0f08ded4c8c5b0967f8b209ee2cd80`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 10.1 MB (10075626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93db171eca68243a4f689b5400ef3c2ac2a1074f1eae1f9f0d049506c8756fe`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23c8c890839d95ebaf447485d8492d089fc8fa23d1ca65c6349a41ac95bc961`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 5.9 MB (5893116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:424e17d1ca73b3f1d92e5d0c0b7272bbaeee943cc673a2249f0bf7ca99eeedde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e7bd514eeda8663e46d4eeed484d7df02209f60112393607269af3e2c0430c`

```dockerfile
```

-	Layers:
	-	`sha256:8fbda3c9e4c0ad20ecba339d117fab2e86108fcfe33cbba7f8ddc3053d6bc89a`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; arm variant v7

```console
$ docker pull irssi@sha256:42ff91c7e5cb5046e91c18adce476ce64e5d772ab658a70c9df46e592b10ce82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18828366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ac84c98bbbaf189bedd8109f71397874c887df2e4eb32123f05470b88358b5`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:21 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:22:22 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:22:22 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:22:22 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:22:22 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:22:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:22:37 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:22:37 GMT
USER user
# Wed, 28 Jan 2026 02:22:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132ae8f3941338d2191aad9429d0bd185ceeb7aeedb8fddf43adad6b57e3273e`  
		Last Modified: Wed, 28 Jan 2026 02:22:45 GMT  
		Size: 9.9 MB (9902405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770acb73451dc424aeb5afcad4a4882f5d765fcbcc8b659b8841bf77d8166afe`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda40971fe170d5e56e81f398ba01d1904a08b07386da11fe56b125109dd60b9`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 5.6 MB (5643252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:fcebcd556b705ae5c410e6b569b01096b561714c5c2fc1d7c8c746decaeef0bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1328781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d61d96801a2a79a245717287e0380350d8e1b0c44936b6dcaf8429b0e2074bab`

```dockerfile
```

-	Layers:
	-	`sha256:e0caf0a4bbae914fea3e8ffab5d1f1752e3fc858d38e993806dd2b78f6919657`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 1.3 MB (1311147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fda69d589c766de3e44adc56d464708c1c2090577cfe6fdd9a50f95229a2c4fa`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:c53ef5cb4c4fb78d4ffdaad1b902adc24327fb49d4ad5c6d719dcf26f8e1ceba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20927195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7538037fb15131e4b2540ac0e275393593929c95a1ca622c94e6c70d99874f28`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:48 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:17:48 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:17:48 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:17:48 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:17:48 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:18:00 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:18:00 GMT
USER user
# Wed, 28 Jan 2026 02:18:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628108c2cc8068dbd74588362d3734d7b6b306883916eb33cb53af667c096440`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 10.8 MB (10792790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9361ffc4206f8e272dc8adc782da4ab39f3b1fe287c6dfb23c57814cf1e94439`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7efe759a9de929b3a25440ff73ac10595ac218ae5d0a087f34fa385d7db181f`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 5.9 MB (5936327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:ac959328037122478f2c09228cf4478f1c099d3257efec2dae9823db1d16b2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db6c23ab4cfc36c7b70e7f4325b9bfa25d1a31a205c632f8e25757cb01f7cef`

```dockerfile
```

-	Layers:
	-	`sha256:3b09e8c286f81074ecdbaaeccccef453ddf9951ff459e4c086e01b8968fe3b0e`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 1.3 MB (1308193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57974d8beacb812f7bb8f7b52301ddd6a66eb7f4c851dcc2ee58f100ec0208b1`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 17.7 KB (17682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; 386

```console
$ docker pull irssi@sha256:a32c16d5607a49617e8d077ec1f9ba5b53b0001a5d70805f183e27ac8f377955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20225669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7946f5f999880045f35ea6c3b7115f7cc7ca872f2653f90c5b0a114ea701599b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:14 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:16:14 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:16:14 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:16:14 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:16:14 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:16:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:16:34 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:16:34 GMT
USER user
# Wed, 28 Jan 2026 02:16:34 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50882b3c493b99635b6de6cd7279fc00a7df160e84cd53399664993828611810`  
		Last Modified: Wed, 28 Jan 2026 02:16:41 GMT  
		Size: 10.4 MB (10393535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7588c02c444f10953a0f0aac9fa979fe4a835bbefde822557708fbd3d21750de`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7dcb0c68d5a17e86130988d6ddf97978ae4c3d866b099962426d869a1c1fc3`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 6.1 MB (6144150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:b77b6da6595a9c4ebfe003d3192b1a97bd9a14f1fe19417ad4a8d7068acc0505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16f268d469cb9fcc79cb87b83fdcbadb9fa6818bf4d9c56a441df0e015c2ec6`

```dockerfile
```

-	Layers:
	-	`sha256:1ddc13011deb856a736a8c90df7acab1227398d8a2ae9e4586daa141365096b4`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 1.3 MB (1308694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47e26778e3f506818fa4ed452e58334a8e15701f1d896ec8ed2ff3288ca7ecef`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; ppc64le

```console
$ docker pull irssi@sha256:b40803da860e141ec3ab2320cf224c304aa870a9a884cb362b69e74b6fd82b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21272396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a2c6a98e5b7978e9d4671908d2864a8d58c1b872e5ec279f9a7a67312f3e2b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:32:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:32:11 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:32:11 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:32:11 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:32:11 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:32:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:32:31 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:32:31 GMT
USER user
# Wed, 28 Jan 2026 02:32:31 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc81a5350f307da5c9651178208c0aa789db44da9179ac834ac469d70ce42cc`  
		Last Modified: Wed, 28 Jan 2026 02:32:51 GMT  
		Size: 11.1 MB (11079608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e505a6cbf58cbc8474040a9d448a79cab0812b78e3b1c6db13e87987f8e4d9a0`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3296179391416e1833f722cc60f06d3ee4df4255177c36a2f41a35a6ab2661b`  
		Last Modified: Wed, 28 Jan 2026 02:32:51 GMT  
		Size: 6.4 MB (6362158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:e2ead2561551ba2a279d799d266e484e986d5370478af7155036333e682a1a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551e8fca5526f8aa868ce90e80d554f73ff2800bcf6fb3b0fb1b9013223228b5`

```dockerfile
```

-	Layers:
	-	`sha256:890481868cc7de496dcdc1f70cc0d6026227efccdd40466a57aa43304c3e345f`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 1.3 MB (1308146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9fac81ff985d048567933403c842b1d477306de718e7d5226612b3cb1eb068`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; riscv64

```console
$ docker pull irssi@sha256:a29b54bd9ab139f5c60185ee85db0a602092a6821866cad82df0fb45368c398c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19942208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9176875f86f8abf3bc20c65b42847d911af0be7e5863f4d6dcbd526719132c`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 08:24:33 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 08:24:34 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 08:24:34 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 08:24:34 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 08:24:34 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 08:28:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 08:28:23 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 08:28:23 GMT
USER user
# Wed, 28 Jan 2026 08:28:23 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b6c4248bc749950275ce15b2dff82393f4351ced2e20c7b5e2ffef3c0848ce`  
		Last Modified: Wed, 28 Jan 2026 08:29:26 GMT  
		Size: 10.3 MB (10291898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e176dad2b23e06165e59400a1ff2260014ec93b0fb3b8c7628a64e1adaf49f`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3131351fcf8ddb074fb73d582b50e94aa55e099ca06fc128b310489675e69c97`  
		Last Modified: Wed, 28 Jan 2026 08:29:26 GMT  
		Size: 6.1 MB (6064037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:165ef1cc15b3aeae45d6479f80369f8078869b953af00ad6ddb3765a55356e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7192140d2d48650b459b2a9acdce6a086c4bf08877b907f3c6bc37ce9799d3e7`

```dockerfile
```

-	Layers:
	-	`sha256:a59cb060f285e8659782eab321b072ac7afdce9472b5395d10144bca9d127b79`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 1.3 MB (1308142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e90caa10ad17b6e48ce9a44b3d010cc7b20e200cbb6ec1067441e247ce555fc`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; s390x

```console
$ docker pull irssi@sha256:e55dc3c7ee83af6ee968373464f0b874c0d9149e01ce32f4680a83b5791d2ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21334391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a042dac64e240c543befef410a12767f4051b627b63028b597010c108714083`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:52 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:19:52 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:19:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:19:52 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:19:52 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:20:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:20:14 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:20:14 GMT
USER user
# Wed, 28 Jan 2026 02:20:14 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e174cb7156ade2e31408909452271b26ae4f143ef276276f0f448b1bad2165`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 11.4 MB (11405107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2a6b19294dd14e5551b394d76102c59c84eae810434dca5ae909a1e58da672`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faba483b2b5362b1905ca82789be9c963c7fde3135033f6aac9183937e5d9161`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 6.2 MB (6202965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:05475f6695b9e4e1863216bdc5de6a1a24bfec2a5baecd06f9a7bc6cd0d17408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3183ed0bc53cc736e214c57eaef2cb864de7e9dbaccf5fe0a5530c72247ac1ab`

```dockerfile
```

-	Layers:
	-	`sha256:c63a0479be024622dc272c05215babf54e4fc3b5c5ab3d053c0dcf2de80483cb`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 1.3 MB (1308088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5037cc7aa93ea1e1f234114cc48a82216f93fe0b9ee46a01ee9a03609cbe19e`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 17.5 KB (17499 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-trixie`

```console
$ docker pull irssi@sha256:6f18ede25b4d4593ab99544ab52277a4e1254f2fbe6a64def5eb7de58074fffc
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
$ docker pull irssi@sha256:49c3737149b22851a93ba69ac22cebd9abf8c8a5d5994e2ca286860caf15353a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53871168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f752e1dfe12c027448c72cd5e3229ea7002dea38239febe081da26b8f7b27ed3`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:03:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:03:00 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:03:00 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:03:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:03:41 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:03:41 GMT
USER user
# Tue, 24 Feb 2026 19:03:41 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7ad25661c3266880a3c864c64ca6faa3b88c0ddb4a998a667e1f1d4b99a22d`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 19.2 MB (19222246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc80a3f9407efa5dcf0dc0ba37f425c82a6ecff60485ff89dd844390ff01a53`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d808574b07af61087631c143ffb9e4be37c1313e4d6fb331c97d17da0f436b32`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 4.9 MB (4866927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:abd6aeef322973ea82182a219b2ba14441f100be5d532e6f7b52e6062bc15a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979b803961d56ac53e2960a4847046894c3f5095836cf0aa2fd343e0288e1e0e`

```dockerfile
```

-	Layers:
	-	`sha256:3557d7d8d5e4df3d7ade5b19b149d56205ce87989a1066808f14bcf3f4321be4`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 5.6 MB (5588475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94196f7468e34a70daa83619d0cf5061ae5adf7711aca144d3d43fc9475a48da`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:6887b2daf7a8e04420d9f8019955beefca4b05d2370737f5085f12f8bb863c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50955082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82db261419aa9d562d5751330a1b61cd4d76e7c5028123921b370b072d4e9c19`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:59:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 18:59:28 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 18:59:28 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 18:59:28 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 18:59:28 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:00:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:00:20 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:00:20 GMT
USER user
# Tue, 24 Feb 2026 19:00:20 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7364bcc76ebade3ad468fc97fcab1317a1b01976383c65ec8f166e9828038c67`  
		Last Modified: Tue, 24 Feb 2026 19:00:34 GMT  
		Size: 18.3 MB (18294280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d702d54a8b971c044db6fb77d45b0c781dbb99062e9faf1a81743c47fc56bf`  
		Last Modified: Tue, 24 Feb 2026 19:00:31 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b41ba1be7d2ca3c964a8be01ccc30e64cc8a0ca03702c32d5870d2d3d769bb`  
		Last Modified: Tue, 24 Feb 2026 19:00:35 GMT  
		Size: 4.7 MB (4709832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:9ec580a8a2c10e1b7ac74c5a41f66009751caa3a8d2b0dc76ce73021e5457329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3590dbb7640207ebd9aa49bf6c514655778ebcc0dea1bf38fe7da73c02990d03`

```dockerfile
```

-	Layers:
	-	`sha256:93ef4bd1a5d0d962b395d82efceb8f97a7d23f4cd0a74978d0edd9456835b58f`  
		Last Modified: Tue, 24 Feb 2026 19:00:31 GMT  
		Size: 5.6 MB (5586024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:025639689d36438751d0440bf57caefab23fbf1a4e77b9cc3febff3196f2a2b9`  
		Last Modified: Tue, 24 Feb 2026 19:00:31 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:e65224016b946c4d99129fad9314bdbdc0bf0296df171d4ce13bc5aa24cb6cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48688484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9c173ed818b8888f5cbf8f2e9258855675b8dd27c9cb7908c704a1d3069397`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:03:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:03:16 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:03:16 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:03:16 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:03:16 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:03:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:03:58 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:03:58 GMT
USER user
# Tue, 24 Feb 2026 19:03:58 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6afde1291a25c0cc231ccde29bbe0ad9ff81c712d4e11e050becb6d4ba8ce0d`  
		Last Modified: Tue, 24 Feb 2026 19:04:08 GMT  
		Size: 17.9 MB (17913151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b8f6d599a61d91e34fb4362460af69da8f684fd2226c0a12c37f1fee9652b8`  
		Last Modified: Tue, 24 Feb 2026 19:04:07 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4575a9012f56ba332b5c7534e48f48a25065b112fa4613e17f2d061261eb8e13`  
		Last Modified: Tue, 24 Feb 2026 19:04:08 GMT  
		Size: 4.6 MB (4558224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:578b6038b34fa00900a70d96abebf8df03f41cbef32e270af68c766ed6703f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9176d67dd016c9ba37147b21f657ef2ae76348260f1f72189b8dc548007b5a73`

```dockerfile
```

-	Layers:
	-	`sha256:cca03ae28695eb959e228e35c2e861a53e15134500b965d0f79e67be15a1cf50`  
		Last Modified: Tue, 24 Feb 2026 19:04:08 GMT  
		Size: 5.6 MB (5589046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dade344df2087c2cbe360a19c02237de12027a28b597247bd6d4844a90a5dad`  
		Last Modified: Tue, 24 Feb 2026 19:04:07 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:b5705a932a1071d49bc33cb793e6492a17f0c13a09af00c00847132826a5399d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53975047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95271ad57b650f4906bebb73ced93170cb93cdc9485991098fde0de3c6ac7f3b`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:06:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:06:10 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:06:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:06:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:06:46 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:06:46 GMT
USER user
# Tue, 24 Feb 2026 19:06:46 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bde18e6576dd26665639dfee2e2c29ab72d5a490303fa301ad8b6d16d01032`  
		Last Modified: Tue, 24 Feb 2026 19:06:58 GMT  
		Size: 19.1 MB (19050073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb0f26017633de6d20b077a7d5fbc6cc2e5ca7a1231309bb6d18d9c6914a55b`  
		Last Modified: Tue, 24 Feb 2026 19:06:57 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5666611ba24e987a94791ca84b6bb380525795696e072f0d60ba9d17ade814ef`  
		Last Modified: Tue, 24 Feb 2026 19:06:57 GMT  
		Size: 4.8 MB (4781514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:900b2ed2e203d81d8f8d6a5cd524d2db8b91bd6962cbb74ffcb0d2a396647107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136a2b4c868d58cd89f9de10c7f831de5ff64687d2b3f76d4e7c01b8ffa16584`

```dockerfile
```

-	Layers:
	-	`sha256:2fef361a887b7785b6efd16d1c15d0262f2f2c6d45edab1f8a975ba81b6f1fdd`  
		Last Modified: Tue, 24 Feb 2026 19:06:57 GMT  
		Size: 5.6 MB (5594959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb64f6057abd305766916ed63546cbd132d825a2da5422247487175382c5f5b9`  
		Last Modified: Tue, 24 Feb 2026 19:06:57 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; 386

```console
$ docker pull irssi@sha256:47a406a29379abd6ed06b0d20217433e973e2870d780ff30823782f31e5c6b33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54908577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91e586aa3e8ce17d01aee6359c922ffe41daa80e277df7ae8ed8d1889e1bb0b`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:58:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 18:58:30 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 18:58:30 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 18:58:30 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 18:58:30 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 18:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 18:59:11 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 18:59:11 GMT
USER user
# Tue, 24 Feb 2026 18:59:11 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ae61c08fa4b2cc99f86dc6a1fe4823c3e0ac9a711287f64cac6485a6238ac8`  
		Last Modified: Tue, 24 Feb 2026 18:59:21 GMT  
		Size: 18.7 MB (18742816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf3f98a9e73f8a6e5b1989e717a2286e372230bcaff62941bae689905197df8`  
		Last Modified: Tue, 24 Feb 2026 18:59:20 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a297182723d0165449b463b3d8873cf3e889a114d50096866c842a8e640504`  
		Last Modified: Tue, 24 Feb 2026 18:59:21 GMT  
		Size: 4.9 MB (4868483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:6c462d49b091009b00485bef9ea87abfab3cb1639844d8c0ed87db6e3e81f5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ff00c0c6b361160a520647c72a3cf1d9322aed6a3382745d35d0d05d128d4e`

```dockerfile
```

-	Layers:
	-	`sha256:b4fd1d01133f85b3efcc51e3d12301590bbb5fb57101916a792336a8d1dea592`  
		Last Modified: Tue, 24 Feb 2026 18:59:21 GMT  
		Size: 5.6 MB (5584598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00eea56a9297862479d3e58a1bd8c833d2a522ff54655c30af9634f5c984d84d`  
		Last Modified: Tue, 24 Feb 2026 18:59:20 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:91b49338a181c6d7b1ae5689c2a610af4dcb438d1eb567f96160219d271063f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58240333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4fc70f04320b975862b6d37425c6f5766d3f6c2e97e62049747274abf47acc`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:07:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:07:22 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:07:22 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:07:22 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:07:22 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:09:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:09:16 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:09:16 GMT
USER user
# Tue, 24 Feb 2026 19:09:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5beebebe5029aabb929ae44c4537e3b21fd8d65921a409bb2df1b7c9b634b6d`  
		Last Modified: Tue, 24 Feb 2026 19:09:44 GMT  
		Size: 19.5 MB (19538939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed570b0aeb97d8cb44da9c8850814c6aa7e1b43fe3d9f4058d9d5a52f0eb6224`  
		Last Modified: Tue, 24 Feb 2026 19:09:43 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ecef354c37ad21cbe5f6e442c1f3c79f858cd86e1ece389542887cae1cff44d`  
		Last Modified: Tue, 24 Feb 2026 19:09:43 GMT  
		Size: 5.1 MB (5097820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:38354f39cc3e23ea94d1feaca94d6602908c74c9dbd5beddfeeb5bd33866538a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904a8b4a8a183068c5d6db74160bbb18d87a4c74f95375cf320b45143257753e`

```dockerfile
```

-	Layers:
	-	`sha256:4c2d2dc5bef56d23df0cb5b905d48dc667fb78e0a3c3a168e9e8a3a4f7f1b318`  
		Last Modified: Tue, 24 Feb 2026 19:09:43 GMT  
		Size: 5.6 MB (5595506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:373385b6bc18ef5a4933f2dfe5147cd4368d7f2730b1f214cd1abe2372ffb0d2`  
		Last Modified: Tue, 24 Feb 2026 19:09:43 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:3a7d38a48cd82c9bd2d5741f468dcdfbf92e333ecc06c2d12dbfe8b938ab0307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51693147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0a99e5b7cd8d4f262722aed889c863e4c892a0f23fe9749d929e8dec75cf662`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 03:03:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 03:03:38 GMT
ENV HOME=/home/user
# Wed, 25 Feb 2026 03:03:38 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 25 Feb 2026 03:03:38 GMT
ENV LANG=C.UTF-8
# Wed, 25 Feb 2026 03:03:38 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 25 Feb 2026 03:10:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 25 Feb 2026 03:10:25 GMT
WORKDIR /home/user
# Wed, 25 Feb 2026 03:10:25 GMT
USER user
# Wed, 25 Feb 2026 03:10:25 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6508c3cdfc31f498c772515ee0821b13440e08ba735c32d3cba318269a3f687`  
		Last Modified: Wed, 25 Feb 2026 03:12:21 GMT  
		Size: 18.6 MB (18552692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ef556a8959335b7e794bf6752b54a81934178688ef1e7d4dbdb197aa0eb326`  
		Last Modified: Wed, 25 Feb 2026 03:12:16 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2794c755bfc5dceb9c6a1eb2ff258465b48801c3bd877b5cde6f46d9920a5c`  
		Last Modified: Wed, 25 Feb 2026 03:12:18 GMT  
		Size: 4.9 MB (4860678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:5ad91e36e6745d334569f2aede71764aa6ab0c8d2ed12405c01d1a981287b5ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ebcaf2e72424c63e04d825e7d04bbe5589f3f805c573faf9c8484afea2b540f`

```dockerfile
```

-	Layers:
	-	`sha256:5c3be456f6ce9090fac8cee71f4291c1aaef1a9ac164f8e2bd0de699367a6334`  
		Last Modified: Wed, 25 Feb 2026 03:12:18 GMT  
		Size: 5.6 MB (5579778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9be1a19638d1af3b7539195ea9d207d142146b312fe552361ffde9b48f90de25`  
		Last Modified: Wed, 25 Feb 2026 03:12:16 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; s390x

```console
$ docker pull irssi@sha256:9d2c67d051b5f92f329619102e0e2bc0df643ef026d1f553c93d501eb54b0049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54516690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf87075c86e270be08f7350f9904070bb3c572934e47a6d6aa9e70fefbff3812`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:01:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:01:50 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:01:50 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:01:50 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:01:50 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:03:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:03:57 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:03:57 GMT
USER user
# Tue, 24 Feb 2026 19:03:57 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb8e7c85a43a84dc9bfa10f335db4cb6dbd00571742698dd7d26077875d9a48`  
		Last Modified: Tue, 24 Feb 2026 19:04:25 GMT  
		Size: 19.8 MB (19768672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e12ffbdb3791dcf1981e8eefcf126275f55fe052fac3a8fafc881aac17c34d8`  
		Last Modified: Tue, 24 Feb 2026 19:04:24 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149d77b47e1605f5cda1129f653ed9adbc0c8c0c2286fd9e81c91c6c44d32956`  
		Last Modified: Tue, 24 Feb 2026 19:04:25 GMT  
		Size: 4.9 MB (4906478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:d10e5a37df33b885dd47403b1e8b7a310eb535821e3b44695a144c5fb72da92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b0fb8133b9ed0bb88f527230ee5b7eefff618321781bea5b846e5b8d1ea2a2`

```dockerfile
```

-	Layers:
	-	`sha256:9ab81d1d85995cb9010ed56d4fdb909af0e66dc54953575d97300c5e3eb22dbe`  
		Last Modified: Tue, 24 Feb 2026 19:04:24 GMT  
		Size: 5.6 MB (5589380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5cb68be6babc8fbd8fc9be84183610c6d3f88b4fb466e15ef8526dfead89283`  
		Last Modified: Tue, 24 Feb 2026 19:04:24 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5`

```console
$ docker pull irssi@sha256:6f18ede25b4d4593ab99544ab52277a4e1254f2fbe6a64def5eb7de58074fffc
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
$ docker pull irssi@sha256:49c3737149b22851a93ba69ac22cebd9abf8c8a5d5994e2ca286860caf15353a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53871168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f752e1dfe12c027448c72cd5e3229ea7002dea38239febe081da26b8f7b27ed3`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:03:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:03:00 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:03:00 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:03:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:03:41 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:03:41 GMT
USER user
# Tue, 24 Feb 2026 19:03:41 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7ad25661c3266880a3c864c64ca6faa3b88c0ddb4a998a667e1f1d4b99a22d`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 19.2 MB (19222246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc80a3f9407efa5dcf0dc0ba37f425c82a6ecff60485ff89dd844390ff01a53`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d808574b07af61087631c143ffb9e4be37c1313e4d6fb331c97d17da0f436b32`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 4.9 MB (4866927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:abd6aeef322973ea82182a219b2ba14441f100be5d532e6f7b52e6062bc15a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979b803961d56ac53e2960a4847046894c3f5095836cf0aa2fd343e0288e1e0e`

```dockerfile
```

-	Layers:
	-	`sha256:3557d7d8d5e4df3d7ade5b19b149d56205ce87989a1066808f14bcf3f4321be4`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 5.6 MB (5588475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94196f7468e34a70daa83619d0cf5061ae5adf7711aca144d3d43fc9475a48da`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v5

```console
$ docker pull irssi@sha256:6887b2daf7a8e04420d9f8019955beefca4b05d2370737f5085f12f8bb863c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50955082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82db261419aa9d562d5751330a1b61cd4d76e7c5028123921b370b072d4e9c19`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:59:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 18:59:28 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 18:59:28 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 18:59:28 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 18:59:28 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:00:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:00:20 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:00:20 GMT
USER user
# Tue, 24 Feb 2026 19:00:20 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7364bcc76ebade3ad468fc97fcab1317a1b01976383c65ec8f166e9828038c67`  
		Last Modified: Tue, 24 Feb 2026 19:00:34 GMT  
		Size: 18.3 MB (18294280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d702d54a8b971c044db6fb77d45b0c781dbb99062e9faf1a81743c47fc56bf`  
		Last Modified: Tue, 24 Feb 2026 19:00:31 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b41ba1be7d2ca3c964a8be01ccc30e64cc8a0ca03702c32d5870d2d3d769bb`  
		Last Modified: Tue, 24 Feb 2026 19:00:35 GMT  
		Size: 4.7 MB (4709832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:9ec580a8a2c10e1b7ac74c5a41f66009751caa3a8d2b0dc76ce73021e5457329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3590dbb7640207ebd9aa49bf6c514655778ebcc0dea1bf38fe7da73c02990d03`

```dockerfile
```

-	Layers:
	-	`sha256:93ef4bd1a5d0d962b395d82efceb8f97a7d23f4cd0a74978d0edd9456835b58f`  
		Last Modified: Tue, 24 Feb 2026 19:00:31 GMT  
		Size: 5.6 MB (5586024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:025639689d36438751d0440bf57caefab23fbf1a4e77b9cc3febff3196f2a2b9`  
		Last Modified: Tue, 24 Feb 2026 19:00:31 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v7

```console
$ docker pull irssi@sha256:e65224016b946c4d99129fad9314bdbdc0bf0296df171d4ce13bc5aa24cb6cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48688484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9c173ed818b8888f5cbf8f2e9258855675b8dd27c9cb7908c704a1d3069397`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:03:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:03:16 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:03:16 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:03:16 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:03:16 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:03:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:03:58 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:03:58 GMT
USER user
# Tue, 24 Feb 2026 19:03:58 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6afde1291a25c0cc231ccde29bbe0ad9ff81c712d4e11e050becb6d4ba8ce0d`  
		Last Modified: Tue, 24 Feb 2026 19:04:08 GMT  
		Size: 17.9 MB (17913151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b8f6d599a61d91e34fb4362460af69da8f684fd2226c0a12c37f1fee9652b8`  
		Last Modified: Tue, 24 Feb 2026 19:04:07 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4575a9012f56ba332b5c7534e48f48a25065b112fa4613e17f2d061261eb8e13`  
		Last Modified: Tue, 24 Feb 2026 19:04:08 GMT  
		Size: 4.6 MB (4558224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:578b6038b34fa00900a70d96abebf8df03f41cbef32e270af68c766ed6703f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9176d67dd016c9ba37147b21f657ef2ae76348260f1f72189b8dc548007b5a73`

```dockerfile
```

-	Layers:
	-	`sha256:cca03ae28695eb959e228e35c2e861a53e15134500b965d0f79e67be15a1cf50`  
		Last Modified: Tue, 24 Feb 2026 19:04:08 GMT  
		Size: 5.6 MB (5589046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dade344df2087c2cbe360a19c02237de12027a28b597247bd6d4844a90a5dad`  
		Last Modified: Tue, 24 Feb 2026 19:04:07 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:b5705a932a1071d49bc33cb793e6492a17f0c13a09af00c00847132826a5399d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53975047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95271ad57b650f4906bebb73ced93170cb93cdc9485991098fde0de3c6ac7f3b`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:06:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:06:10 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:06:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:06:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:06:46 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:06:46 GMT
USER user
# Tue, 24 Feb 2026 19:06:46 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bde18e6576dd26665639dfee2e2c29ab72d5a490303fa301ad8b6d16d01032`  
		Last Modified: Tue, 24 Feb 2026 19:06:58 GMT  
		Size: 19.1 MB (19050073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb0f26017633de6d20b077a7d5fbc6cc2e5ca7a1231309bb6d18d9c6914a55b`  
		Last Modified: Tue, 24 Feb 2026 19:06:57 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5666611ba24e987a94791ca84b6bb380525795696e072f0d60ba9d17ade814ef`  
		Last Modified: Tue, 24 Feb 2026 19:06:57 GMT  
		Size: 4.8 MB (4781514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:900b2ed2e203d81d8f8d6a5cd524d2db8b91bd6962cbb74ffcb0d2a396647107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136a2b4c868d58cd89f9de10c7f831de5ff64687d2b3f76d4e7c01b8ffa16584`

```dockerfile
```

-	Layers:
	-	`sha256:2fef361a887b7785b6efd16d1c15d0262f2f2c6d45edab1f8a975ba81b6f1fdd`  
		Last Modified: Tue, 24 Feb 2026 19:06:57 GMT  
		Size: 5.6 MB (5594959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb64f6057abd305766916ed63546cbd132d825a2da5422247487175382c5f5b9`  
		Last Modified: Tue, 24 Feb 2026 19:06:57 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; 386

```console
$ docker pull irssi@sha256:47a406a29379abd6ed06b0d20217433e973e2870d780ff30823782f31e5c6b33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54908577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91e586aa3e8ce17d01aee6359c922ffe41daa80e277df7ae8ed8d1889e1bb0b`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:58:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 18:58:30 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 18:58:30 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 18:58:30 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 18:58:30 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 18:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 18:59:11 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 18:59:11 GMT
USER user
# Tue, 24 Feb 2026 18:59:11 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ae61c08fa4b2cc99f86dc6a1fe4823c3e0ac9a711287f64cac6485a6238ac8`  
		Last Modified: Tue, 24 Feb 2026 18:59:21 GMT  
		Size: 18.7 MB (18742816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf3f98a9e73f8a6e5b1989e717a2286e372230bcaff62941bae689905197df8`  
		Last Modified: Tue, 24 Feb 2026 18:59:20 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a297182723d0165449b463b3d8873cf3e889a114d50096866c842a8e640504`  
		Last Modified: Tue, 24 Feb 2026 18:59:21 GMT  
		Size: 4.9 MB (4868483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:6c462d49b091009b00485bef9ea87abfab3cb1639844d8c0ed87db6e3e81f5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ff00c0c6b361160a520647c72a3cf1d9322aed6a3382745d35d0d05d128d4e`

```dockerfile
```

-	Layers:
	-	`sha256:b4fd1d01133f85b3efcc51e3d12301590bbb5fb57101916a792336a8d1dea592`  
		Last Modified: Tue, 24 Feb 2026 18:59:21 GMT  
		Size: 5.6 MB (5584598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00eea56a9297862479d3e58a1bd8c833d2a522ff54655c30af9634f5c984d84d`  
		Last Modified: Tue, 24 Feb 2026 18:59:20 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; ppc64le

```console
$ docker pull irssi@sha256:91b49338a181c6d7b1ae5689c2a610af4dcb438d1eb567f96160219d271063f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58240333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4fc70f04320b975862b6d37425c6f5766d3f6c2e97e62049747274abf47acc`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:07:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:07:22 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:07:22 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:07:22 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:07:22 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:09:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:09:16 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:09:16 GMT
USER user
# Tue, 24 Feb 2026 19:09:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5beebebe5029aabb929ae44c4537e3b21fd8d65921a409bb2df1b7c9b634b6d`  
		Last Modified: Tue, 24 Feb 2026 19:09:44 GMT  
		Size: 19.5 MB (19538939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed570b0aeb97d8cb44da9c8850814c6aa7e1b43fe3d9f4058d9d5a52f0eb6224`  
		Last Modified: Tue, 24 Feb 2026 19:09:43 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ecef354c37ad21cbe5f6e442c1f3c79f858cd86e1ece389542887cae1cff44d`  
		Last Modified: Tue, 24 Feb 2026 19:09:43 GMT  
		Size: 5.1 MB (5097820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:38354f39cc3e23ea94d1feaca94d6602908c74c9dbd5beddfeeb5bd33866538a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904a8b4a8a183068c5d6db74160bbb18d87a4c74f95375cf320b45143257753e`

```dockerfile
```

-	Layers:
	-	`sha256:4c2d2dc5bef56d23df0cb5b905d48dc667fb78e0a3c3a168e9e8a3a4f7f1b318`  
		Last Modified: Tue, 24 Feb 2026 19:09:43 GMT  
		Size: 5.6 MB (5595506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:373385b6bc18ef5a4933f2dfe5147cd4368d7f2730b1f214cd1abe2372ffb0d2`  
		Last Modified: Tue, 24 Feb 2026 19:09:43 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; riscv64

```console
$ docker pull irssi@sha256:3a7d38a48cd82c9bd2d5741f468dcdfbf92e333ecc06c2d12dbfe8b938ab0307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51693147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0a99e5b7cd8d4f262722aed889c863e4c892a0f23fe9749d929e8dec75cf662`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 03:03:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 03:03:38 GMT
ENV HOME=/home/user
# Wed, 25 Feb 2026 03:03:38 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 25 Feb 2026 03:03:38 GMT
ENV LANG=C.UTF-8
# Wed, 25 Feb 2026 03:03:38 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 25 Feb 2026 03:10:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 25 Feb 2026 03:10:25 GMT
WORKDIR /home/user
# Wed, 25 Feb 2026 03:10:25 GMT
USER user
# Wed, 25 Feb 2026 03:10:25 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6508c3cdfc31f498c772515ee0821b13440e08ba735c32d3cba318269a3f687`  
		Last Modified: Wed, 25 Feb 2026 03:12:21 GMT  
		Size: 18.6 MB (18552692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ef556a8959335b7e794bf6752b54a81934178688ef1e7d4dbdb197aa0eb326`  
		Last Modified: Wed, 25 Feb 2026 03:12:16 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2794c755bfc5dceb9c6a1eb2ff258465b48801c3bd877b5cde6f46d9920a5c`  
		Last Modified: Wed, 25 Feb 2026 03:12:18 GMT  
		Size: 4.9 MB (4860678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:5ad91e36e6745d334569f2aede71764aa6ab0c8d2ed12405c01d1a981287b5ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ebcaf2e72424c63e04d825e7d04bbe5589f3f805c573faf9c8484afea2b540f`

```dockerfile
```

-	Layers:
	-	`sha256:5c3be456f6ce9090fac8cee71f4291c1aaef1a9ac164f8e2bd0de699367a6334`  
		Last Modified: Wed, 25 Feb 2026 03:12:18 GMT  
		Size: 5.6 MB (5579778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9be1a19638d1af3b7539195ea9d207d142146b312fe552361ffde9b48f90de25`  
		Last Modified: Wed, 25 Feb 2026 03:12:16 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; s390x

```console
$ docker pull irssi@sha256:9d2c67d051b5f92f329619102e0e2bc0df643ef026d1f553c93d501eb54b0049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54516690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf87075c86e270be08f7350f9904070bb3c572934e47a6d6aa9e70fefbff3812`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:01:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:01:50 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:01:50 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:01:50 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:01:50 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:03:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:03:57 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:03:57 GMT
USER user
# Tue, 24 Feb 2026 19:03:57 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb8e7c85a43a84dc9bfa10f335db4cb6dbd00571742698dd7d26077875d9a48`  
		Last Modified: Tue, 24 Feb 2026 19:04:25 GMT  
		Size: 19.8 MB (19768672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e12ffbdb3791dcf1981e8eefcf126275f55fe052fac3a8fafc881aac17c34d8`  
		Last Modified: Tue, 24 Feb 2026 19:04:24 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149d77b47e1605f5cda1129f653ed9adbc0c8c0c2286fd9e81c91c6c44d32956`  
		Last Modified: Tue, 24 Feb 2026 19:04:25 GMT  
		Size: 4.9 MB (4906478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:d10e5a37df33b885dd47403b1e8b7a310eb535821e3b44695a144c5fb72da92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b0fb8133b9ed0bb88f527230ee5b7eefff618321781bea5b846e5b8d1ea2a2`

```dockerfile
```

-	Layers:
	-	`sha256:9ab81d1d85995cb9010ed56d4fdb909af0e66dc54953575d97300c5e3eb22dbe`  
		Last Modified: Tue, 24 Feb 2026 19:04:24 GMT  
		Size: 5.6 MB (5589380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5cb68be6babc8fbd8fc9be84183610c6d3f88b4fb466e15ef8526dfead89283`  
		Last Modified: Tue, 24 Feb 2026 19:04:24 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine`

```console
$ docker pull irssi@sha256:bc9744c4e1f3c9e4401ee35e73ff4f7c97683f5c784c5cce21910e488a4ee219
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
$ docker pull irssi@sha256:84665fb63540b0ca94547800ed0093cb97d41e1cbc0d2aa823a67e6af91fe8ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20784026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6645503b9d588217c1fb06c9a2d7e278a4360e4aa22e92d8ff0af44ac2c6c10`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:47 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:17:47 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:17:47 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:17:47 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:17:47 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:18:00 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:18:00 GMT
USER user
# Wed, 28 Jan 2026 02:18:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d65c05b32f228b7007340211a175e100ca3ddb33a7e2c44b15d11799a9a84ad`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 10.9 MB (10857996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082c32a8914140e457d67603de3b04ccc66e688baed84d8d500f40dc885ef27a`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93abf1ed0403fdbc85fa021598a1202b3d9b55bd9d785457b554af6b86fc7d`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 6.1 MB (6063223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:7bd9c1f9350891fb6e79ac3dc4d7686c1c714bb2c12147cb089864d19ef3bc9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e29e513927a47425fe64b68ba4eeb03593581de0692a732211bc7b11537936`

```dockerfile
```

-	Layers:
	-	`sha256:5d4ee629f31bfb597346562d7da53858808c502ca6820fb40a7c347520afebad`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 1.3 MB (1308739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b9c1c09e72415a3ca7367aec0652ca69a856b8c6a57ef69ba919d208498b76`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:9a8babd75444eea65ebe3a06627eceb16f4d50aec2da2998fd3a611d75ed5b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19539552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04e50bc1d87804658a7d29a7ebb00b20d1a22d6d21cd19f5eff93f84035eb0b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:23:56 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:23:57 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:23:57 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:23:57 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:23:57 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:24:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:24:17 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:24:17 GMT
USER user
# Wed, 28 Jan 2026 02:24:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d5c4e6a80a684ff34083f2ded6ae6a1b0f08ded4c8c5b0967f8b209ee2cd80`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 10.1 MB (10075626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93db171eca68243a4f689b5400ef3c2ac2a1074f1eae1f9f0d049506c8756fe`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23c8c890839d95ebaf447485d8492d089fc8fa23d1ca65c6349a41ac95bc961`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 5.9 MB (5893116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:424e17d1ca73b3f1d92e5d0c0b7272bbaeee943cc673a2249f0bf7ca99eeedde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e7bd514eeda8663e46d4eeed484d7df02209f60112393607269af3e2c0430c`

```dockerfile
```

-	Layers:
	-	`sha256:8fbda3c9e4c0ad20ecba339d117fab2e86108fcfe33cbba7f8ddc3053d6bc89a`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:42ff91c7e5cb5046e91c18adce476ce64e5d772ab658a70c9df46e592b10ce82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18828366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ac84c98bbbaf189bedd8109f71397874c887df2e4eb32123f05470b88358b5`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:21 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:22:22 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:22:22 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:22:22 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:22:22 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:22:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:22:37 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:22:37 GMT
USER user
# Wed, 28 Jan 2026 02:22:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132ae8f3941338d2191aad9429d0bd185ceeb7aeedb8fddf43adad6b57e3273e`  
		Last Modified: Wed, 28 Jan 2026 02:22:45 GMT  
		Size: 9.9 MB (9902405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770acb73451dc424aeb5afcad4a4882f5d765fcbcc8b659b8841bf77d8166afe`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda40971fe170d5e56e81f398ba01d1904a08b07386da11fe56b125109dd60b9`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 5.6 MB (5643252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:fcebcd556b705ae5c410e6b569b01096b561714c5c2fc1d7c8c746decaeef0bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1328781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d61d96801a2a79a245717287e0380350d8e1b0c44936b6dcaf8429b0e2074bab`

```dockerfile
```

-	Layers:
	-	`sha256:e0caf0a4bbae914fea3e8ffab5d1f1752e3fc858d38e993806dd2b78f6919657`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 1.3 MB (1311147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fda69d589c766de3e44adc56d464708c1c2090577cfe6fdd9a50f95229a2c4fa`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:c53ef5cb4c4fb78d4ffdaad1b902adc24327fb49d4ad5c6d719dcf26f8e1ceba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20927195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7538037fb15131e4b2540ac0e275393593929c95a1ca622c94e6c70d99874f28`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:48 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:17:48 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:17:48 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:17:48 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:17:48 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:18:00 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:18:00 GMT
USER user
# Wed, 28 Jan 2026 02:18:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628108c2cc8068dbd74588362d3734d7b6b306883916eb33cb53af667c096440`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 10.8 MB (10792790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9361ffc4206f8e272dc8adc782da4ab39f3b1fe287c6dfb23c57814cf1e94439`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7efe759a9de929b3a25440ff73ac10595ac218ae5d0a087f34fa385d7db181f`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 5.9 MB (5936327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:ac959328037122478f2c09228cf4478f1c099d3257efec2dae9823db1d16b2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db6c23ab4cfc36c7b70e7f4325b9bfa25d1a31a205c632f8e25757cb01f7cef`

```dockerfile
```

-	Layers:
	-	`sha256:3b09e8c286f81074ecdbaaeccccef453ddf9951ff459e4c086e01b8968fe3b0e`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 1.3 MB (1308193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57974d8beacb812f7bb8f7b52301ddd6a66eb7f4c851dcc2ee58f100ec0208b1`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 17.7 KB (17682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; 386

```console
$ docker pull irssi@sha256:a32c16d5607a49617e8d077ec1f9ba5b53b0001a5d70805f183e27ac8f377955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20225669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7946f5f999880045f35ea6c3b7115f7cc7ca872f2653f90c5b0a114ea701599b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:14 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:16:14 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:16:14 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:16:14 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:16:14 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:16:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:16:34 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:16:34 GMT
USER user
# Wed, 28 Jan 2026 02:16:34 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50882b3c493b99635b6de6cd7279fc00a7df160e84cd53399664993828611810`  
		Last Modified: Wed, 28 Jan 2026 02:16:41 GMT  
		Size: 10.4 MB (10393535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7588c02c444f10953a0f0aac9fa979fe4a835bbefde822557708fbd3d21750de`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7dcb0c68d5a17e86130988d6ddf97978ae4c3d866b099962426d869a1c1fc3`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 6.1 MB (6144150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:b77b6da6595a9c4ebfe003d3192b1a97bd9a14f1fe19417ad4a8d7068acc0505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16f268d469cb9fcc79cb87b83fdcbadb9fa6818bf4d9c56a441df0e015c2ec6`

```dockerfile
```

-	Layers:
	-	`sha256:1ddc13011deb856a736a8c90df7acab1227398d8a2ae9e4586daa141365096b4`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 1.3 MB (1308694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47e26778e3f506818fa4ed452e58334a8e15701f1d896ec8ed2ff3288ca7ecef`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:b40803da860e141ec3ab2320cf224c304aa870a9a884cb362b69e74b6fd82b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21272396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a2c6a98e5b7978e9d4671908d2864a8d58c1b872e5ec279f9a7a67312f3e2b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:32:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:32:11 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:32:11 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:32:11 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:32:11 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:32:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:32:31 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:32:31 GMT
USER user
# Wed, 28 Jan 2026 02:32:31 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc81a5350f307da5c9651178208c0aa789db44da9179ac834ac469d70ce42cc`  
		Last Modified: Wed, 28 Jan 2026 02:32:51 GMT  
		Size: 11.1 MB (11079608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e505a6cbf58cbc8474040a9d448a79cab0812b78e3b1c6db13e87987f8e4d9a0`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3296179391416e1833f722cc60f06d3ee4df4255177c36a2f41a35a6ab2661b`  
		Last Modified: Wed, 28 Jan 2026 02:32:51 GMT  
		Size: 6.4 MB (6362158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:e2ead2561551ba2a279d799d266e484e986d5370478af7155036333e682a1a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551e8fca5526f8aa868ce90e80d554f73ff2800bcf6fb3b0fb1b9013223228b5`

```dockerfile
```

-	Layers:
	-	`sha256:890481868cc7de496dcdc1f70cc0d6026227efccdd40466a57aa43304c3e345f`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 1.3 MB (1308146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9fac81ff985d048567933403c842b1d477306de718e7d5226612b3cb1eb068`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:a29b54bd9ab139f5c60185ee85db0a602092a6821866cad82df0fb45368c398c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19942208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9176875f86f8abf3bc20c65b42847d911af0be7e5863f4d6dcbd526719132c`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 08:24:33 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 08:24:34 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 08:24:34 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 08:24:34 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 08:24:34 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 08:28:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 08:28:23 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 08:28:23 GMT
USER user
# Wed, 28 Jan 2026 08:28:23 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b6c4248bc749950275ce15b2dff82393f4351ced2e20c7b5e2ffef3c0848ce`  
		Last Modified: Wed, 28 Jan 2026 08:29:26 GMT  
		Size: 10.3 MB (10291898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e176dad2b23e06165e59400a1ff2260014ec93b0fb3b8c7628a64e1adaf49f`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3131351fcf8ddb074fb73d582b50e94aa55e099ca06fc128b310489675e69c97`  
		Last Modified: Wed, 28 Jan 2026 08:29:26 GMT  
		Size: 6.1 MB (6064037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:165ef1cc15b3aeae45d6479f80369f8078869b953af00ad6ddb3765a55356e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7192140d2d48650b459b2a9acdce6a086c4bf08877b907f3c6bc37ce9799d3e7`

```dockerfile
```

-	Layers:
	-	`sha256:a59cb060f285e8659782eab321b072ac7afdce9472b5395d10144bca9d127b79`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 1.3 MB (1308142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e90caa10ad17b6e48ce9a44b3d010cc7b20e200cbb6ec1067441e247ce555fc`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:e55dc3c7ee83af6ee968373464f0b874c0d9149e01ce32f4680a83b5791d2ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21334391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a042dac64e240c543befef410a12767f4051b627b63028b597010c108714083`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:52 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:19:52 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:19:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:19:52 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:19:52 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:20:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:20:14 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:20:14 GMT
USER user
# Wed, 28 Jan 2026 02:20:14 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e174cb7156ade2e31408909452271b26ae4f143ef276276f0f448b1bad2165`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 11.4 MB (11405107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2a6b19294dd14e5551b394d76102c59c84eae810434dca5ae909a1e58da672`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faba483b2b5362b1905ca82789be9c963c7fde3135033f6aac9183937e5d9161`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 6.2 MB (6202965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:05475f6695b9e4e1863216bdc5de6a1a24bfec2a5baecd06f9a7bc6cd0d17408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3183ed0bc53cc736e214c57eaef2cb864de7e9dbaccf5fe0a5530c72247ac1ab`

```dockerfile
```

-	Layers:
	-	`sha256:c63a0479be024622dc272c05215babf54e4fc3b5c5ab3d053c0dcf2de80483cb`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 1.3 MB (1308088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5037cc7aa93ea1e1f234114cc48a82216f93fe0b9ee46a01ee9a03609cbe19e`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 17.5 KB (17499 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine3.23`

```console
$ docker pull irssi@sha256:bc9744c4e1f3c9e4401ee35e73ff4f7c97683f5c784c5cce21910e488a4ee219
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
$ docker pull irssi@sha256:84665fb63540b0ca94547800ed0093cb97d41e1cbc0d2aa823a67e6af91fe8ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20784026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6645503b9d588217c1fb06c9a2d7e278a4360e4aa22e92d8ff0af44ac2c6c10`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:47 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:17:47 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:17:47 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:17:47 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:17:47 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:18:00 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:18:00 GMT
USER user
# Wed, 28 Jan 2026 02:18:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d65c05b32f228b7007340211a175e100ca3ddb33a7e2c44b15d11799a9a84ad`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 10.9 MB (10857996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082c32a8914140e457d67603de3b04ccc66e688baed84d8d500f40dc885ef27a`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93abf1ed0403fdbc85fa021598a1202b3d9b55bd9d785457b554af6b86fc7d`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 6.1 MB (6063223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:7bd9c1f9350891fb6e79ac3dc4d7686c1c714bb2c12147cb089864d19ef3bc9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e29e513927a47425fe64b68ba4eeb03593581de0692a732211bc7b11537936`

```dockerfile
```

-	Layers:
	-	`sha256:5d4ee629f31bfb597346562d7da53858808c502ca6820fb40a7c347520afebad`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 1.3 MB (1308739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b9c1c09e72415a3ca7367aec0652ca69a856b8c6a57ef69ba919d208498b76`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; arm variant v6

```console
$ docker pull irssi@sha256:9a8babd75444eea65ebe3a06627eceb16f4d50aec2da2998fd3a611d75ed5b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19539552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04e50bc1d87804658a7d29a7ebb00b20d1a22d6d21cd19f5eff93f84035eb0b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:23:56 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:23:57 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:23:57 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:23:57 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:23:57 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:24:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:24:17 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:24:17 GMT
USER user
# Wed, 28 Jan 2026 02:24:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d5c4e6a80a684ff34083f2ded6ae6a1b0f08ded4c8c5b0967f8b209ee2cd80`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 10.1 MB (10075626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93db171eca68243a4f689b5400ef3c2ac2a1074f1eae1f9f0d049506c8756fe`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23c8c890839d95ebaf447485d8492d089fc8fa23d1ca65c6349a41ac95bc961`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 5.9 MB (5893116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:424e17d1ca73b3f1d92e5d0c0b7272bbaeee943cc673a2249f0bf7ca99eeedde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e7bd514eeda8663e46d4eeed484d7df02209f60112393607269af3e2c0430c`

```dockerfile
```

-	Layers:
	-	`sha256:8fbda3c9e4c0ad20ecba339d117fab2e86108fcfe33cbba7f8ddc3053d6bc89a`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; arm variant v7

```console
$ docker pull irssi@sha256:42ff91c7e5cb5046e91c18adce476ce64e5d772ab658a70c9df46e592b10ce82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18828366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ac84c98bbbaf189bedd8109f71397874c887df2e4eb32123f05470b88358b5`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:21 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:22:22 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:22:22 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:22:22 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:22:22 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:22:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:22:37 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:22:37 GMT
USER user
# Wed, 28 Jan 2026 02:22:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132ae8f3941338d2191aad9429d0bd185ceeb7aeedb8fddf43adad6b57e3273e`  
		Last Modified: Wed, 28 Jan 2026 02:22:45 GMT  
		Size: 9.9 MB (9902405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770acb73451dc424aeb5afcad4a4882f5d765fcbcc8b659b8841bf77d8166afe`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda40971fe170d5e56e81f398ba01d1904a08b07386da11fe56b125109dd60b9`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 5.6 MB (5643252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:fcebcd556b705ae5c410e6b569b01096b561714c5c2fc1d7c8c746decaeef0bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1328781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d61d96801a2a79a245717287e0380350d8e1b0c44936b6dcaf8429b0e2074bab`

```dockerfile
```

-	Layers:
	-	`sha256:e0caf0a4bbae914fea3e8ffab5d1f1752e3fc858d38e993806dd2b78f6919657`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 1.3 MB (1311147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fda69d589c766de3e44adc56d464708c1c2090577cfe6fdd9a50f95229a2c4fa`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:c53ef5cb4c4fb78d4ffdaad1b902adc24327fb49d4ad5c6d719dcf26f8e1ceba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20927195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7538037fb15131e4b2540ac0e275393593929c95a1ca622c94e6c70d99874f28`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:48 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:17:48 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:17:48 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:17:48 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:17:48 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:18:00 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:18:00 GMT
USER user
# Wed, 28 Jan 2026 02:18:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628108c2cc8068dbd74588362d3734d7b6b306883916eb33cb53af667c096440`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 10.8 MB (10792790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9361ffc4206f8e272dc8adc782da4ab39f3b1fe287c6dfb23c57814cf1e94439`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7efe759a9de929b3a25440ff73ac10595ac218ae5d0a087f34fa385d7db181f`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 5.9 MB (5936327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:ac959328037122478f2c09228cf4478f1c099d3257efec2dae9823db1d16b2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db6c23ab4cfc36c7b70e7f4325b9bfa25d1a31a205c632f8e25757cb01f7cef`

```dockerfile
```

-	Layers:
	-	`sha256:3b09e8c286f81074ecdbaaeccccef453ddf9951ff459e4c086e01b8968fe3b0e`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 1.3 MB (1308193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57974d8beacb812f7bb8f7b52301ddd6a66eb7f4c851dcc2ee58f100ec0208b1`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 17.7 KB (17682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; 386

```console
$ docker pull irssi@sha256:a32c16d5607a49617e8d077ec1f9ba5b53b0001a5d70805f183e27ac8f377955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20225669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7946f5f999880045f35ea6c3b7115f7cc7ca872f2653f90c5b0a114ea701599b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:14 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:16:14 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:16:14 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:16:14 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:16:14 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:16:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:16:34 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:16:34 GMT
USER user
# Wed, 28 Jan 2026 02:16:34 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50882b3c493b99635b6de6cd7279fc00a7df160e84cd53399664993828611810`  
		Last Modified: Wed, 28 Jan 2026 02:16:41 GMT  
		Size: 10.4 MB (10393535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7588c02c444f10953a0f0aac9fa979fe4a835bbefde822557708fbd3d21750de`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7dcb0c68d5a17e86130988d6ddf97978ae4c3d866b099962426d869a1c1fc3`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 6.1 MB (6144150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:b77b6da6595a9c4ebfe003d3192b1a97bd9a14f1fe19417ad4a8d7068acc0505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16f268d469cb9fcc79cb87b83fdcbadb9fa6818bf4d9c56a441df0e015c2ec6`

```dockerfile
```

-	Layers:
	-	`sha256:1ddc13011deb856a736a8c90df7acab1227398d8a2ae9e4586daa141365096b4`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 1.3 MB (1308694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47e26778e3f506818fa4ed452e58334a8e15701f1d896ec8ed2ff3288ca7ecef`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; ppc64le

```console
$ docker pull irssi@sha256:b40803da860e141ec3ab2320cf224c304aa870a9a884cb362b69e74b6fd82b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21272396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a2c6a98e5b7978e9d4671908d2864a8d58c1b872e5ec279f9a7a67312f3e2b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:32:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:32:11 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:32:11 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:32:11 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:32:11 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:32:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:32:31 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:32:31 GMT
USER user
# Wed, 28 Jan 2026 02:32:31 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc81a5350f307da5c9651178208c0aa789db44da9179ac834ac469d70ce42cc`  
		Last Modified: Wed, 28 Jan 2026 02:32:51 GMT  
		Size: 11.1 MB (11079608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e505a6cbf58cbc8474040a9d448a79cab0812b78e3b1c6db13e87987f8e4d9a0`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3296179391416e1833f722cc60f06d3ee4df4255177c36a2f41a35a6ab2661b`  
		Last Modified: Wed, 28 Jan 2026 02:32:51 GMT  
		Size: 6.4 MB (6362158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:e2ead2561551ba2a279d799d266e484e986d5370478af7155036333e682a1a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551e8fca5526f8aa868ce90e80d554f73ff2800bcf6fb3b0fb1b9013223228b5`

```dockerfile
```

-	Layers:
	-	`sha256:890481868cc7de496dcdc1f70cc0d6026227efccdd40466a57aa43304c3e345f`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 1.3 MB (1308146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9fac81ff985d048567933403c842b1d477306de718e7d5226612b3cb1eb068`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; riscv64

```console
$ docker pull irssi@sha256:a29b54bd9ab139f5c60185ee85db0a602092a6821866cad82df0fb45368c398c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19942208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9176875f86f8abf3bc20c65b42847d911af0be7e5863f4d6dcbd526719132c`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 08:24:33 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 08:24:34 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 08:24:34 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 08:24:34 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 08:24:34 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 08:28:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 08:28:23 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 08:28:23 GMT
USER user
# Wed, 28 Jan 2026 08:28:23 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b6c4248bc749950275ce15b2dff82393f4351ced2e20c7b5e2ffef3c0848ce`  
		Last Modified: Wed, 28 Jan 2026 08:29:26 GMT  
		Size: 10.3 MB (10291898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e176dad2b23e06165e59400a1ff2260014ec93b0fb3b8c7628a64e1adaf49f`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3131351fcf8ddb074fb73d582b50e94aa55e099ca06fc128b310489675e69c97`  
		Last Modified: Wed, 28 Jan 2026 08:29:26 GMT  
		Size: 6.1 MB (6064037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:165ef1cc15b3aeae45d6479f80369f8078869b953af00ad6ddb3765a55356e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7192140d2d48650b459b2a9acdce6a086c4bf08877b907f3c6bc37ce9799d3e7`

```dockerfile
```

-	Layers:
	-	`sha256:a59cb060f285e8659782eab321b072ac7afdce9472b5395d10144bca9d127b79`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 1.3 MB (1308142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e90caa10ad17b6e48ce9a44b3d010cc7b20e200cbb6ec1067441e247ce555fc`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; s390x

```console
$ docker pull irssi@sha256:e55dc3c7ee83af6ee968373464f0b874c0d9149e01ce32f4680a83b5791d2ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21334391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a042dac64e240c543befef410a12767f4051b627b63028b597010c108714083`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:52 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:19:52 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:19:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:19:52 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:19:52 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:20:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:20:14 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:20:14 GMT
USER user
# Wed, 28 Jan 2026 02:20:14 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e174cb7156ade2e31408909452271b26ae4f143ef276276f0f448b1bad2165`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 11.4 MB (11405107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2a6b19294dd14e5551b394d76102c59c84eae810434dca5ae909a1e58da672`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faba483b2b5362b1905ca82789be9c963c7fde3135033f6aac9183937e5d9161`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 6.2 MB (6202965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:05475f6695b9e4e1863216bdc5de6a1a24bfec2a5baecd06f9a7bc6cd0d17408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3183ed0bc53cc736e214c57eaef2cb864de7e9dbaccf5fe0a5530c72247ac1ab`

```dockerfile
```

-	Layers:
	-	`sha256:c63a0479be024622dc272c05215babf54e4fc3b5c5ab3d053c0dcf2de80483cb`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 1.3 MB (1308088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5037cc7aa93ea1e1f234114cc48a82216f93fe0b9ee46a01ee9a03609cbe19e`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 17.5 KB (17499 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-trixie`

```console
$ docker pull irssi@sha256:6f18ede25b4d4593ab99544ab52277a4e1254f2fbe6a64def5eb7de58074fffc
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
$ docker pull irssi@sha256:49c3737149b22851a93ba69ac22cebd9abf8c8a5d5994e2ca286860caf15353a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53871168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f752e1dfe12c027448c72cd5e3229ea7002dea38239febe081da26b8f7b27ed3`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:03:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:03:00 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:03:00 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:03:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:03:41 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:03:41 GMT
USER user
# Tue, 24 Feb 2026 19:03:41 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7ad25661c3266880a3c864c64ca6faa3b88c0ddb4a998a667e1f1d4b99a22d`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 19.2 MB (19222246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc80a3f9407efa5dcf0dc0ba37f425c82a6ecff60485ff89dd844390ff01a53`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d808574b07af61087631c143ffb9e4be37c1313e4d6fb331c97d17da0f436b32`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 4.9 MB (4866927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:abd6aeef322973ea82182a219b2ba14441f100be5d532e6f7b52e6062bc15a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979b803961d56ac53e2960a4847046894c3f5095836cf0aa2fd343e0288e1e0e`

```dockerfile
```

-	Layers:
	-	`sha256:3557d7d8d5e4df3d7ade5b19b149d56205ce87989a1066808f14bcf3f4321be4`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 5.6 MB (5588475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94196f7468e34a70daa83619d0cf5061ae5adf7711aca144d3d43fc9475a48da`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:6887b2daf7a8e04420d9f8019955beefca4b05d2370737f5085f12f8bb863c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50955082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82db261419aa9d562d5751330a1b61cd4d76e7c5028123921b370b072d4e9c19`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:59:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 18:59:28 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 18:59:28 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 18:59:28 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 18:59:28 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:00:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:00:20 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:00:20 GMT
USER user
# Tue, 24 Feb 2026 19:00:20 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7364bcc76ebade3ad468fc97fcab1317a1b01976383c65ec8f166e9828038c67`  
		Last Modified: Tue, 24 Feb 2026 19:00:34 GMT  
		Size: 18.3 MB (18294280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d702d54a8b971c044db6fb77d45b0c781dbb99062e9faf1a81743c47fc56bf`  
		Last Modified: Tue, 24 Feb 2026 19:00:31 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b41ba1be7d2ca3c964a8be01ccc30e64cc8a0ca03702c32d5870d2d3d769bb`  
		Last Modified: Tue, 24 Feb 2026 19:00:35 GMT  
		Size: 4.7 MB (4709832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:9ec580a8a2c10e1b7ac74c5a41f66009751caa3a8d2b0dc76ce73021e5457329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3590dbb7640207ebd9aa49bf6c514655778ebcc0dea1bf38fe7da73c02990d03`

```dockerfile
```

-	Layers:
	-	`sha256:93ef4bd1a5d0d962b395d82efceb8f97a7d23f4cd0a74978d0edd9456835b58f`  
		Last Modified: Tue, 24 Feb 2026 19:00:31 GMT  
		Size: 5.6 MB (5586024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:025639689d36438751d0440bf57caefab23fbf1a4e77b9cc3febff3196f2a2b9`  
		Last Modified: Tue, 24 Feb 2026 19:00:31 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:e65224016b946c4d99129fad9314bdbdc0bf0296df171d4ce13bc5aa24cb6cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48688484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9c173ed818b8888f5cbf8f2e9258855675b8dd27c9cb7908c704a1d3069397`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:03:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:03:16 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:03:16 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:03:16 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:03:16 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:03:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:03:58 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:03:58 GMT
USER user
# Tue, 24 Feb 2026 19:03:58 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6afde1291a25c0cc231ccde29bbe0ad9ff81c712d4e11e050becb6d4ba8ce0d`  
		Last Modified: Tue, 24 Feb 2026 19:04:08 GMT  
		Size: 17.9 MB (17913151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b8f6d599a61d91e34fb4362460af69da8f684fd2226c0a12c37f1fee9652b8`  
		Last Modified: Tue, 24 Feb 2026 19:04:07 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4575a9012f56ba332b5c7534e48f48a25065b112fa4613e17f2d061261eb8e13`  
		Last Modified: Tue, 24 Feb 2026 19:04:08 GMT  
		Size: 4.6 MB (4558224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:578b6038b34fa00900a70d96abebf8df03f41cbef32e270af68c766ed6703f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9176d67dd016c9ba37147b21f657ef2ae76348260f1f72189b8dc548007b5a73`

```dockerfile
```

-	Layers:
	-	`sha256:cca03ae28695eb959e228e35c2e861a53e15134500b965d0f79e67be15a1cf50`  
		Last Modified: Tue, 24 Feb 2026 19:04:08 GMT  
		Size: 5.6 MB (5589046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dade344df2087c2cbe360a19c02237de12027a28b597247bd6d4844a90a5dad`  
		Last Modified: Tue, 24 Feb 2026 19:04:07 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:b5705a932a1071d49bc33cb793e6492a17f0c13a09af00c00847132826a5399d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53975047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95271ad57b650f4906bebb73ced93170cb93cdc9485991098fde0de3c6ac7f3b`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:06:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:06:10 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:06:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:06:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:06:46 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:06:46 GMT
USER user
# Tue, 24 Feb 2026 19:06:46 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bde18e6576dd26665639dfee2e2c29ab72d5a490303fa301ad8b6d16d01032`  
		Last Modified: Tue, 24 Feb 2026 19:06:58 GMT  
		Size: 19.1 MB (19050073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb0f26017633de6d20b077a7d5fbc6cc2e5ca7a1231309bb6d18d9c6914a55b`  
		Last Modified: Tue, 24 Feb 2026 19:06:57 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5666611ba24e987a94791ca84b6bb380525795696e072f0d60ba9d17ade814ef`  
		Last Modified: Tue, 24 Feb 2026 19:06:57 GMT  
		Size: 4.8 MB (4781514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:900b2ed2e203d81d8f8d6a5cd524d2db8b91bd6962cbb74ffcb0d2a396647107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136a2b4c868d58cd89f9de10c7f831de5ff64687d2b3f76d4e7c01b8ffa16584`

```dockerfile
```

-	Layers:
	-	`sha256:2fef361a887b7785b6efd16d1c15d0262f2f2c6d45edab1f8a975ba81b6f1fdd`  
		Last Modified: Tue, 24 Feb 2026 19:06:57 GMT  
		Size: 5.6 MB (5594959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb64f6057abd305766916ed63546cbd132d825a2da5422247487175382c5f5b9`  
		Last Modified: Tue, 24 Feb 2026 19:06:57 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; 386

```console
$ docker pull irssi@sha256:47a406a29379abd6ed06b0d20217433e973e2870d780ff30823782f31e5c6b33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54908577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91e586aa3e8ce17d01aee6359c922ffe41daa80e277df7ae8ed8d1889e1bb0b`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:58:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 18:58:30 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 18:58:30 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 18:58:30 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 18:58:30 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 18:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 18:59:11 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 18:59:11 GMT
USER user
# Tue, 24 Feb 2026 18:59:11 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ae61c08fa4b2cc99f86dc6a1fe4823c3e0ac9a711287f64cac6485a6238ac8`  
		Last Modified: Tue, 24 Feb 2026 18:59:21 GMT  
		Size: 18.7 MB (18742816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf3f98a9e73f8a6e5b1989e717a2286e372230bcaff62941bae689905197df8`  
		Last Modified: Tue, 24 Feb 2026 18:59:20 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a297182723d0165449b463b3d8873cf3e889a114d50096866c842a8e640504`  
		Last Modified: Tue, 24 Feb 2026 18:59:21 GMT  
		Size: 4.9 MB (4868483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:6c462d49b091009b00485bef9ea87abfab3cb1639844d8c0ed87db6e3e81f5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ff00c0c6b361160a520647c72a3cf1d9322aed6a3382745d35d0d05d128d4e`

```dockerfile
```

-	Layers:
	-	`sha256:b4fd1d01133f85b3efcc51e3d12301590bbb5fb57101916a792336a8d1dea592`  
		Last Modified: Tue, 24 Feb 2026 18:59:21 GMT  
		Size: 5.6 MB (5584598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00eea56a9297862479d3e58a1bd8c833d2a522ff54655c30af9634f5c984d84d`  
		Last Modified: Tue, 24 Feb 2026 18:59:20 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:91b49338a181c6d7b1ae5689c2a610af4dcb438d1eb567f96160219d271063f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58240333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4fc70f04320b975862b6d37425c6f5766d3f6c2e97e62049747274abf47acc`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:07:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:07:22 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:07:22 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:07:22 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:07:22 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:09:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:09:16 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:09:16 GMT
USER user
# Tue, 24 Feb 2026 19:09:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5beebebe5029aabb929ae44c4537e3b21fd8d65921a409bb2df1b7c9b634b6d`  
		Last Modified: Tue, 24 Feb 2026 19:09:44 GMT  
		Size: 19.5 MB (19538939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed570b0aeb97d8cb44da9c8850814c6aa7e1b43fe3d9f4058d9d5a52f0eb6224`  
		Last Modified: Tue, 24 Feb 2026 19:09:43 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ecef354c37ad21cbe5f6e442c1f3c79f858cd86e1ece389542887cae1cff44d`  
		Last Modified: Tue, 24 Feb 2026 19:09:43 GMT  
		Size: 5.1 MB (5097820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:38354f39cc3e23ea94d1feaca94d6602908c74c9dbd5beddfeeb5bd33866538a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904a8b4a8a183068c5d6db74160bbb18d87a4c74f95375cf320b45143257753e`

```dockerfile
```

-	Layers:
	-	`sha256:4c2d2dc5bef56d23df0cb5b905d48dc667fb78e0a3c3a168e9e8a3a4f7f1b318`  
		Last Modified: Tue, 24 Feb 2026 19:09:43 GMT  
		Size: 5.6 MB (5595506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:373385b6bc18ef5a4933f2dfe5147cd4368d7f2730b1f214cd1abe2372ffb0d2`  
		Last Modified: Tue, 24 Feb 2026 19:09:43 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:3a7d38a48cd82c9bd2d5741f468dcdfbf92e333ecc06c2d12dbfe8b938ab0307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51693147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0a99e5b7cd8d4f262722aed889c863e4c892a0f23fe9749d929e8dec75cf662`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 03:03:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 03:03:38 GMT
ENV HOME=/home/user
# Wed, 25 Feb 2026 03:03:38 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 25 Feb 2026 03:03:38 GMT
ENV LANG=C.UTF-8
# Wed, 25 Feb 2026 03:03:38 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 25 Feb 2026 03:10:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 25 Feb 2026 03:10:25 GMT
WORKDIR /home/user
# Wed, 25 Feb 2026 03:10:25 GMT
USER user
# Wed, 25 Feb 2026 03:10:25 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6508c3cdfc31f498c772515ee0821b13440e08ba735c32d3cba318269a3f687`  
		Last Modified: Wed, 25 Feb 2026 03:12:21 GMT  
		Size: 18.6 MB (18552692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ef556a8959335b7e794bf6752b54a81934178688ef1e7d4dbdb197aa0eb326`  
		Last Modified: Wed, 25 Feb 2026 03:12:16 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2794c755bfc5dceb9c6a1eb2ff258465b48801c3bd877b5cde6f46d9920a5c`  
		Last Modified: Wed, 25 Feb 2026 03:12:18 GMT  
		Size: 4.9 MB (4860678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:5ad91e36e6745d334569f2aede71764aa6ab0c8d2ed12405c01d1a981287b5ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ebcaf2e72424c63e04d825e7d04bbe5589f3f805c573faf9c8484afea2b540f`

```dockerfile
```

-	Layers:
	-	`sha256:5c3be456f6ce9090fac8cee71f4291c1aaef1a9ac164f8e2bd0de699367a6334`  
		Last Modified: Wed, 25 Feb 2026 03:12:18 GMT  
		Size: 5.6 MB (5579778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9be1a19638d1af3b7539195ea9d207d142146b312fe552361ffde9b48f90de25`  
		Last Modified: Wed, 25 Feb 2026 03:12:16 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; s390x

```console
$ docker pull irssi@sha256:9d2c67d051b5f92f329619102e0e2bc0df643ef026d1f553c93d501eb54b0049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54516690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf87075c86e270be08f7350f9904070bb3c572934e47a6d6aa9e70fefbff3812`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:01:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:01:50 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:01:50 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:01:50 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:01:50 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:03:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:03:57 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:03:57 GMT
USER user
# Tue, 24 Feb 2026 19:03:57 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb8e7c85a43a84dc9bfa10f335db4cb6dbd00571742698dd7d26077875d9a48`  
		Last Modified: Tue, 24 Feb 2026 19:04:25 GMT  
		Size: 19.8 MB (19768672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e12ffbdb3791dcf1981e8eefcf126275f55fe052fac3a8fafc881aac17c34d8`  
		Last Modified: Tue, 24 Feb 2026 19:04:24 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149d77b47e1605f5cda1129f653ed9adbc0c8c0c2286fd9e81c91c6c44d32956`  
		Last Modified: Tue, 24 Feb 2026 19:04:25 GMT  
		Size: 4.9 MB (4906478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:d10e5a37df33b885dd47403b1e8b7a310eb535821e3b44695a144c5fb72da92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b0fb8133b9ed0bb88f527230ee5b7eefff618321781bea5b846e5b8d1ea2a2`

```dockerfile
```

-	Layers:
	-	`sha256:9ab81d1d85995cb9010ed56d4fdb909af0e66dc54953575d97300c5e3eb22dbe`  
		Last Modified: Tue, 24 Feb 2026 19:04:24 GMT  
		Size: 5.6 MB (5589380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5cb68be6babc8fbd8fc9be84183610c6d3f88b4fb466e15ef8526dfead89283`  
		Last Modified: Tue, 24 Feb 2026 19:04:24 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine`

```console
$ docker pull irssi@sha256:bc9744c4e1f3c9e4401ee35e73ff4f7c97683f5c784c5cce21910e488a4ee219
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
$ docker pull irssi@sha256:84665fb63540b0ca94547800ed0093cb97d41e1cbc0d2aa823a67e6af91fe8ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20784026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6645503b9d588217c1fb06c9a2d7e278a4360e4aa22e92d8ff0af44ac2c6c10`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:47 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:17:47 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:17:47 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:17:47 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:17:47 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:18:00 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:18:00 GMT
USER user
# Wed, 28 Jan 2026 02:18:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d65c05b32f228b7007340211a175e100ca3ddb33a7e2c44b15d11799a9a84ad`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 10.9 MB (10857996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082c32a8914140e457d67603de3b04ccc66e688baed84d8d500f40dc885ef27a`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93abf1ed0403fdbc85fa021598a1202b3d9b55bd9d785457b554af6b86fc7d`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 6.1 MB (6063223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:7bd9c1f9350891fb6e79ac3dc4d7686c1c714bb2c12147cb089864d19ef3bc9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e29e513927a47425fe64b68ba4eeb03593581de0692a732211bc7b11537936`

```dockerfile
```

-	Layers:
	-	`sha256:5d4ee629f31bfb597346562d7da53858808c502ca6820fb40a7c347520afebad`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 1.3 MB (1308739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b9c1c09e72415a3ca7367aec0652ca69a856b8c6a57ef69ba919d208498b76`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:9a8babd75444eea65ebe3a06627eceb16f4d50aec2da2998fd3a611d75ed5b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19539552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04e50bc1d87804658a7d29a7ebb00b20d1a22d6d21cd19f5eff93f84035eb0b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:23:56 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:23:57 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:23:57 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:23:57 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:23:57 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:24:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:24:17 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:24:17 GMT
USER user
# Wed, 28 Jan 2026 02:24:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d5c4e6a80a684ff34083f2ded6ae6a1b0f08ded4c8c5b0967f8b209ee2cd80`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 10.1 MB (10075626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93db171eca68243a4f689b5400ef3c2ac2a1074f1eae1f9f0d049506c8756fe`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23c8c890839d95ebaf447485d8492d089fc8fa23d1ca65c6349a41ac95bc961`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 5.9 MB (5893116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:424e17d1ca73b3f1d92e5d0c0b7272bbaeee943cc673a2249f0bf7ca99eeedde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e7bd514eeda8663e46d4eeed484d7df02209f60112393607269af3e2c0430c`

```dockerfile
```

-	Layers:
	-	`sha256:8fbda3c9e4c0ad20ecba339d117fab2e86108fcfe33cbba7f8ddc3053d6bc89a`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:42ff91c7e5cb5046e91c18adce476ce64e5d772ab658a70c9df46e592b10ce82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18828366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ac84c98bbbaf189bedd8109f71397874c887df2e4eb32123f05470b88358b5`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:21 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:22:22 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:22:22 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:22:22 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:22:22 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:22:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:22:37 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:22:37 GMT
USER user
# Wed, 28 Jan 2026 02:22:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132ae8f3941338d2191aad9429d0bd185ceeb7aeedb8fddf43adad6b57e3273e`  
		Last Modified: Wed, 28 Jan 2026 02:22:45 GMT  
		Size: 9.9 MB (9902405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770acb73451dc424aeb5afcad4a4882f5d765fcbcc8b659b8841bf77d8166afe`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda40971fe170d5e56e81f398ba01d1904a08b07386da11fe56b125109dd60b9`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 5.6 MB (5643252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:fcebcd556b705ae5c410e6b569b01096b561714c5c2fc1d7c8c746decaeef0bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1328781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d61d96801a2a79a245717287e0380350d8e1b0c44936b6dcaf8429b0e2074bab`

```dockerfile
```

-	Layers:
	-	`sha256:e0caf0a4bbae914fea3e8ffab5d1f1752e3fc858d38e993806dd2b78f6919657`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 1.3 MB (1311147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fda69d589c766de3e44adc56d464708c1c2090577cfe6fdd9a50f95229a2c4fa`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:c53ef5cb4c4fb78d4ffdaad1b902adc24327fb49d4ad5c6d719dcf26f8e1ceba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20927195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7538037fb15131e4b2540ac0e275393593929c95a1ca622c94e6c70d99874f28`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:48 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:17:48 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:17:48 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:17:48 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:17:48 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:18:00 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:18:00 GMT
USER user
# Wed, 28 Jan 2026 02:18:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628108c2cc8068dbd74588362d3734d7b6b306883916eb33cb53af667c096440`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 10.8 MB (10792790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9361ffc4206f8e272dc8adc782da4ab39f3b1fe287c6dfb23c57814cf1e94439`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7efe759a9de929b3a25440ff73ac10595ac218ae5d0a087f34fa385d7db181f`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 5.9 MB (5936327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:ac959328037122478f2c09228cf4478f1c099d3257efec2dae9823db1d16b2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db6c23ab4cfc36c7b70e7f4325b9bfa25d1a31a205c632f8e25757cb01f7cef`

```dockerfile
```

-	Layers:
	-	`sha256:3b09e8c286f81074ecdbaaeccccef453ddf9951ff459e4c086e01b8968fe3b0e`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 1.3 MB (1308193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57974d8beacb812f7bb8f7b52301ddd6a66eb7f4c851dcc2ee58f100ec0208b1`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 17.7 KB (17682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; 386

```console
$ docker pull irssi@sha256:a32c16d5607a49617e8d077ec1f9ba5b53b0001a5d70805f183e27ac8f377955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20225669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7946f5f999880045f35ea6c3b7115f7cc7ca872f2653f90c5b0a114ea701599b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:14 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:16:14 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:16:14 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:16:14 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:16:14 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:16:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:16:34 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:16:34 GMT
USER user
# Wed, 28 Jan 2026 02:16:34 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50882b3c493b99635b6de6cd7279fc00a7df160e84cd53399664993828611810`  
		Last Modified: Wed, 28 Jan 2026 02:16:41 GMT  
		Size: 10.4 MB (10393535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7588c02c444f10953a0f0aac9fa979fe4a835bbefde822557708fbd3d21750de`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7dcb0c68d5a17e86130988d6ddf97978ae4c3d866b099962426d869a1c1fc3`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 6.1 MB (6144150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:b77b6da6595a9c4ebfe003d3192b1a97bd9a14f1fe19417ad4a8d7068acc0505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16f268d469cb9fcc79cb87b83fdcbadb9fa6818bf4d9c56a441df0e015c2ec6`

```dockerfile
```

-	Layers:
	-	`sha256:1ddc13011deb856a736a8c90df7acab1227398d8a2ae9e4586daa141365096b4`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 1.3 MB (1308694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47e26778e3f506818fa4ed452e58334a8e15701f1d896ec8ed2ff3288ca7ecef`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:b40803da860e141ec3ab2320cf224c304aa870a9a884cb362b69e74b6fd82b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21272396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a2c6a98e5b7978e9d4671908d2864a8d58c1b872e5ec279f9a7a67312f3e2b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:32:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:32:11 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:32:11 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:32:11 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:32:11 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:32:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:32:31 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:32:31 GMT
USER user
# Wed, 28 Jan 2026 02:32:31 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc81a5350f307da5c9651178208c0aa789db44da9179ac834ac469d70ce42cc`  
		Last Modified: Wed, 28 Jan 2026 02:32:51 GMT  
		Size: 11.1 MB (11079608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e505a6cbf58cbc8474040a9d448a79cab0812b78e3b1c6db13e87987f8e4d9a0`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3296179391416e1833f722cc60f06d3ee4df4255177c36a2f41a35a6ab2661b`  
		Last Modified: Wed, 28 Jan 2026 02:32:51 GMT  
		Size: 6.4 MB (6362158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:e2ead2561551ba2a279d799d266e484e986d5370478af7155036333e682a1a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551e8fca5526f8aa868ce90e80d554f73ff2800bcf6fb3b0fb1b9013223228b5`

```dockerfile
```

-	Layers:
	-	`sha256:890481868cc7de496dcdc1f70cc0d6026227efccdd40466a57aa43304c3e345f`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 1.3 MB (1308146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9fac81ff985d048567933403c842b1d477306de718e7d5226612b3cb1eb068`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:a29b54bd9ab139f5c60185ee85db0a602092a6821866cad82df0fb45368c398c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19942208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9176875f86f8abf3bc20c65b42847d911af0be7e5863f4d6dcbd526719132c`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 08:24:33 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 08:24:34 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 08:24:34 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 08:24:34 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 08:24:34 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 08:28:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 08:28:23 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 08:28:23 GMT
USER user
# Wed, 28 Jan 2026 08:28:23 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b6c4248bc749950275ce15b2dff82393f4351ced2e20c7b5e2ffef3c0848ce`  
		Last Modified: Wed, 28 Jan 2026 08:29:26 GMT  
		Size: 10.3 MB (10291898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e176dad2b23e06165e59400a1ff2260014ec93b0fb3b8c7628a64e1adaf49f`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3131351fcf8ddb074fb73d582b50e94aa55e099ca06fc128b310489675e69c97`  
		Last Modified: Wed, 28 Jan 2026 08:29:26 GMT  
		Size: 6.1 MB (6064037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:165ef1cc15b3aeae45d6479f80369f8078869b953af00ad6ddb3765a55356e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7192140d2d48650b459b2a9acdce6a086c4bf08877b907f3c6bc37ce9799d3e7`

```dockerfile
```

-	Layers:
	-	`sha256:a59cb060f285e8659782eab321b072ac7afdce9472b5395d10144bca9d127b79`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 1.3 MB (1308142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e90caa10ad17b6e48ce9a44b3d010cc7b20e200cbb6ec1067441e247ce555fc`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; s390x

```console
$ docker pull irssi@sha256:e55dc3c7ee83af6ee968373464f0b874c0d9149e01ce32f4680a83b5791d2ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21334391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a042dac64e240c543befef410a12767f4051b627b63028b597010c108714083`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:52 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:19:52 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:19:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:19:52 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:19:52 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:20:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:20:14 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:20:14 GMT
USER user
# Wed, 28 Jan 2026 02:20:14 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e174cb7156ade2e31408909452271b26ae4f143ef276276f0f448b1bad2165`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 11.4 MB (11405107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2a6b19294dd14e5551b394d76102c59c84eae810434dca5ae909a1e58da672`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faba483b2b5362b1905ca82789be9c963c7fde3135033f6aac9183937e5d9161`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 6.2 MB (6202965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:05475f6695b9e4e1863216bdc5de6a1a24bfec2a5baecd06f9a7bc6cd0d17408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3183ed0bc53cc736e214c57eaef2cb864de7e9dbaccf5fe0a5530c72247ac1ab`

```dockerfile
```

-	Layers:
	-	`sha256:c63a0479be024622dc272c05215babf54e4fc3b5c5ab3d053c0dcf2de80483cb`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 1.3 MB (1308088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5037cc7aa93ea1e1f234114cc48a82216f93fe0b9ee46a01ee9a03609cbe19e`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 17.5 KB (17499 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine3.23`

```console
$ docker pull irssi@sha256:bc9744c4e1f3c9e4401ee35e73ff4f7c97683f5c784c5cce21910e488a4ee219
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
$ docker pull irssi@sha256:84665fb63540b0ca94547800ed0093cb97d41e1cbc0d2aa823a67e6af91fe8ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20784026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6645503b9d588217c1fb06c9a2d7e278a4360e4aa22e92d8ff0af44ac2c6c10`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:47 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:17:47 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:17:47 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:17:47 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:17:47 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:18:00 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:18:00 GMT
USER user
# Wed, 28 Jan 2026 02:18:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d65c05b32f228b7007340211a175e100ca3ddb33a7e2c44b15d11799a9a84ad`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 10.9 MB (10857996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082c32a8914140e457d67603de3b04ccc66e688baed84d8d500f40dc885ef27a`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93abf1ed0403fdbc85fa021598a1202b3d9b55bd9d785457b554af6b86fc7d`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 6.1 MB (6063223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:7bd9c1f9350891fb6e79ac3dc4d7686c1c714bb2c12147cb089864d19ef3bc9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e29e513927a47425fe64b68ba4eeb03593581de0692a732211bc7b11537936`

```dockerfile
```

-	Layers:
	-	`sha256:5d4ee629f31bfb597346562d7da53858808c502ca6820fb40a7c347520afebad`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 1.3 MB (1308739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b9c1c09e72415a3ca7367aec0652ca69a856b8c6a57ef69ba919d208498b76`  
		Last Modified: Wed, 28 Jan 2026 02:18:06 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; arm variant v6

```console
$ docker pull irssi@sha256:9a8babd75444eea65ebe3a06627eceb16f4d50aec2da2998fd3a611d75ed5b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19539552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04e50bc1d87804658a7d29a7ebb00b20d1a22d6d21cd19f5eff93f84035eb0b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:23:56 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:23:57 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:23:57 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:23:57 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:23:57 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:24:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:24:17 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:24:17 GMT
USER user
# Wed, 28 Jan 2026 02:24:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d5c4e6a80a684ff34083f2ded6ae6a1b0f08ded4c8c5b0967f8b209ee2cd80`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 10.1 MB (10075626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93db171eca68243a4f689b5400ef3c2ac2a1074f1eae1f9f0d049506c8756fe`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23c8c890839d95ebaf447485d8492d089fc8fa23d1ca65c6349a41ac95bc961`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 5.9 MB (5893116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:424e17d1ca73b3f1d92e5d0c0b7272bbaeee943cc673a2249f0bf7ca99eeedde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e7bd514eeda8663e46d4eeed484d7df02209f60112393607269af3e2c0430c`

```dockerfile
```

-	Layers:
	-	`sha256:8fbda3c9e4c0ad20ecba339d117fab2e86108fcfe33cbba7f8ddc3053d6bc89a`  
		Last Modified: Wed, 28 Jan 2026 02:24:22 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; arm variant v7

```console
$ docker pull irssi@sha256:42ff91c7e5cb5046e91c18adce476ce64e5d772ab658a70c9df46e592b10ce82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18828366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ac84c98bbbaf189bedd8109f71397874c887df2e4eb32123f05470b88358b5`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:22:21 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:22:22 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:22:22 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:22:22 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:22:22 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:22:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:22:37 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:22:37 GMT
USER user
# Wed, 28 Jan 2026 02:22:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132ae8f3941338d2191aad9429d0bd185ceeb7aeedb8fddf43adad6b57e3273e`  
		Last Modified: Wed, 28 Jan 2026 02:22:45 GMT  
		Size: 9.9 MB (9902405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770acb73451dc424aeb5afcad4a4882f5d765fcbcc8b659b8841bf77d8166afe`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda40971fe170d5e56e81f398ba01d1904a08b07386da11fe56b125109dd60b9`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 5.6 MB (5643252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:fcebcd556b705ae5c410e6b569b01096b561714c5c2fc1d7c8c746decaeef0bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1328781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d61d96801a2a79a245717287e0380350d8e1b0c44936b6dcaf8429b0e2074bab`

```dockerfile
```

-	Layers:
	-	`sha256:e0caf0a4bbae914fea3e8ffab5d1f1752e3fc858d38e993806dd2b78f6919657`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 1.3 MB (1311147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fda69d589c766de3e44adc56d464708c1c2090577cfe6fdd9a50f95229a2c4fa`  
		Last Modified: Wed, 28 Jan 2026 02:22:44 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:c53ef5cb4c4fb78d4ffdaad1b902adc24327fb49d4ad5c6d719dcf26f8e1ceba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20927195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7538037fb15131e4b2540ac0e275393593929c95a1ca622c94e6c70d99874f28`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:17:48 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:17:48 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:17:48 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:17:48 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:17:48 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:18:00 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:18:00 GMT
USER user
# Wed, 28 Jan 2026 02:18:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628108c2cc8068dbd74588362d3734d7b6b306883916eb33cb53af667c096440`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 10.8 MB (10792790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9361ffc4206f8e272dc8adc782da4ab39f3b1fe287c6dfb23c57814cf1e94439`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7efe759a9de929b3a25440ff73ac10595ac218ae5d0a087f34fa385d7db181f`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 5.9 MB (5936327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:ac959328037122478f2c09228cf4478f1c099d3257efec2dae9823db1d16b2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db6c23ab4cfc36c7b70e7f4325b9bfa25d1a31a205c632f8e25757cb01f7cef`

```dockerfile
```

-	Layers:
	-	`sha256:3b09e8c286f81074ecdbaaeccccef453ddf9951ff459e4c086e01b8968fe3b0e`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 1.3 MB (1308193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57974d8beacb812f7bb8f7b52301ddd6a66eb7f4c851dcc2ee58f100ec0208b1`  
		Last Modified: Wed, 28 Jan 2026 02:18:08 GMT  
		Size: 17.7 KB (17682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; 386

```console
$ docker pull irssi@sha256:a32c16d5607a49617e8d077ec1f9ba5b53b0001a5d70805f183e27ac8f377955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20225669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7946f5f999880045f35ea6c3b7115f7cc7ca872f2653f90c5b0a114ea701599b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:16:14 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:16:14 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:16:14 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:16:14 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:16:14 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:16:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:16:34 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:16:34 GMT
USER user
# Wed, 28 Jan 2026 02:16:34 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50882b3c493b99635b6de6cd7279fc00a7df160e84cd53399664993828611810`  
		Last Modified: Wed, 28 Jan 2026 02:16:41 GMT  
		Size: 10.4 MB (10393535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7588c02c444f10953a0f0aac9fa979fe4a835bbefde822557708fbd3d21750de`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7dcb0c68d5a17e86130988d6ddf97978ae4c3d866b099962426d869a1c1fc3`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 6.1 MB (6144150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:b77b6da6595a9c4ebfe003d3192b1a97bd9a14f1fe19417ad4a8d7068acc0505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16f268d469cb9fcc79cb87b83fdcbadb9fa6818bf4d9c56a441df0e015c2ec6`

```dockerfile
```

-	Layers:
	-	`sha256:1ddc13011deb856a736a8c90df7acab1227398d8a2ae9e4586daa141365096b4`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 1.3 MB (1308694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47e26778e3f506818fa4ed452e58334a8e15701f1d896ec8ed2ff3288ca7ecef`  
		Last Modified: Wed, 28 Jan 2026 02:16:40 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; ppc64le

```console
$ docker pull irssi@sha256:b40803da860e141ec3ab2320cf224c304aa870a9a884cb362b69e74b6fd82b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21272396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a2c6a98e5b7978e9d4671908d2864a8d58c1b872e5ec279f9a7a67312f3e2b`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:32:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:32:11 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:32:11 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:32:11 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:32:11 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:32:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:32:31 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:32:31 GMT
USER user
# Wed, 28 Jan 2026 02:32:31 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc81a5350f307da5c9651178208c0aa789db44da9179ac834ac469d70ce42cc`  
		Last Modified: Wed, 28 Jan 2026 02:32:51 GMT  
		Size: 11.1 MB (11079608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e505a6cbf58cbc8474040a9d448a79cab0812b78e3b1c6db13e87987f8e4d9a0`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3296179391416e1833f722cc60f06d3ee4df4255177c36a2f41a35a6ab2661b`  
		Last Modified: Wed, 28 Jan 2026 02:32:51 GMT  
		Size: 6.4 MB (6362158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:e2ead2561551ba2a279d799d266e484e986d5370478af7155036333e682a1a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551e8fca5526f8aa868ce90e80d554f73ff2800bcf6fb3b0fb1b9013223228b5`

```dockerfile
```

-	Layers:
	-	`sha256:890481868cc7de496dcdc1f70cc0d6026227efccdd40466a57aa43304c3e345f`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 1.3 MB (1308146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9fac81ff985d048567933403c842b1d477306de718e7d5226612b3cb1eb068`  
		Last Modified: Wed, 28 Jan 2026 02:32:50 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; riscv64

```console
$ docker pull irssi@sha256:a29b54bd9ab139f5c60185ee85db0a602092a6821866cad82df0fb45368c398c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19942208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9176875f86f8abf3bc20c65b42847d911af0be7e5863f4d6dcbd526719132c`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 08:24:33 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 08:24:34 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 08:24:34 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 08:24:34 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 08:24:34 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 08:28:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 08:28:23 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 08:28:23 GMT
USER user
# Wed, 28 Jan 2026 08:28:23 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b6c4248bc749950275ce15b2dff82393f4351ced2e20c7b5e2ffef3c0848ce`  
		Last Modified: Wed, 28 Jan 2026 08:29:26 GMT  
		Size: 10.3 MB (10291898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e176dad2b23e06165e59400a1ff2260014ec93b0fb3b8c7628a64e1adaf49f`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3131351fcf8ddb074fb73d582b50e94aa55e099ca06fc128b310489675e69c97`  
		Last Modified: Wed, 28 Jan 2026 08:29:26 GMT  
		Size: 6.1 MB (6064037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:165ef1cc15b3aeae45d6479f80369f8078869b953af00ad6ddb3765a55356e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7192140d2d48650b459b2a9acdce6a086c4bf08877b907f3c6bc37ce9799d3e7`

```dockerfile
```

-	Layers:
	-	`sha256:a59cb060f285e8659782eab321b072ac7afdce9472b5395d10144bca9d127b79`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 1.3 MB (1308142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e90caa10ad17b6e48ce9a44b3d010cc7b20e200cbb6ec1067441e247ce555fc`  
		Last Modified: Wed, 28 Jan 2026 08:29:24 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; s390x

```console
$ docker pull irssi@sha256:e55dc3c7ee83af6ee968373464f0b874c0d9149e01ce32f4680a83b5791d2ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21334391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a042dac64e240c543befef410a12767f4051b627b63028b597010c108714083`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:19:52 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 28 Jan 2026 02:19:52 GMT
ENV HOME=/home/user
# Wed, 28 Jan 2026 02:19:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 28 Jan 2026 02:19:52 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:19:52 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 28 Jan 2026 02:20:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 28 Jan 2026 02:20:14 GMT
WORKDIR /home/user
# Wed, 28 Jan 2026 02:20:14 GMT
USER user
# Wed, 28 Jan 2026 02:20:14 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e174cb7156ade2e31408909452271b26ae4f143ef276276f0f448b1bad2165`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 11.4 MB (11405107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2a6b19294dd14e5551b394d76102c59c84eae810434dca5ae909a1e58da672`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faba483b2b5362b1905ca82789be9c963c7fde3135033f6aac9183937e5d9161`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 6.2 MB (6202965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:05475f6695b9e4e1863216bdc5de6a1a24bfec2a5baecd06f9a7bc6cd0d17408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3183ed0bc53cc736e214c57eaef2cb864de7e9dbaccf5fe0a5530c72247ac1ab`

```dockerfile
```

-	Layers:
	-	`sha256:c63a0479be024622dc272c05215babf54e4fc3b5c5ab3d053c0dcf2de80483cb`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 1.3 MB (1308088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5037cc7aa93ea1e1f234114cc48a82216f93fe0b9ee46a01ee9a03609cbe19e`  
		Last Modified: Wed, 28 Jan 2026 02:20:24 GMT  
		Size: 17.5 KB (17499 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:latest`

```console
$ docker pull irssi@sha256:6f18ede25b4d4593ab99544ab52277a4e1254f2fbe6a64def5eb7de58074fffc
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
$ docker pull irssi@sha256:49c3737149b22851a93ba69ac22cebd9abf8c8a5d5994e2ca286860caf15353a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53871168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f752e1dfe12c027448c72cd5e3229ea7002dea38239febe081da26b8f7b27ed3`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:03:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:03:00 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:03:00 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:03:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:03:41 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:03:41 GMT
USER user
# Tue, 24 Feb 2026 19:03:41 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7ad25661c3266880a3c864c64ca6faa3b88c0ddb4a998a667e1f1d4b99a22d`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 19.2 MB (19222246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc80a3f9407efa5dcf0dc0ba37f425c82a6ecff60485ff89dd844390ff01a53`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d808574b07af61087631c143ffb9e4be37c1313e4d6fb331c97d17da0f436b32`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 4.9 MB (4866927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:abd6aeef322973ea82182a219b2ba14441f100be5d532e6f7b52e6062bc15a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979b803961d56ac53e2960a4847046894c3f5095836cf0aa2fd343e0288e1e0e`

```dockerfile
```

-	Layers:
	-	`sha256:3557d7d8d5e4df3d7ade5b19b149d56205ce87989a1066808f14bcf3f4321be4`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 5.6 MB (5588475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94196f7468e34a70daa83619d0cf5061ae5adf7711aca144d3d43fc9475a48da`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v5

```console
$ docker pull irssi@sha256:6887b2daf7a8e04420d9f8019955beefca4b05d2370737f5085f12f8bb863c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50955082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82db261419aa9d562d5751330a1b61cd4d76e7c5028123921b370b072d4e9c19`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:59:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 18:59:28 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 18:59:28 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 18:59:28 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 18:59:28 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:00:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:00:20 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:00:20 GMT
USER user
# Tue, 24 Feb 2026 19:00:20 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7364bcc76ebade3ad468fc97fcab1317a1b01976383c65ec8f166e9828038c67`  
		Last Modified: Tue, 24 Feb 2026 19:00:34 GMT  
		Size: 18.3 MB (18294280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d702d54a8b971c044db6fb77d45b0c781dbb99062e9faf1a81743c47fc56bf`  
		Last Modified: Tue, 24 Feb 2026 19:00:31 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b41ba1be7d2ca3c964a8be01ccc30e64cc8a0ca03702c32d5870d2d3d769bb`  
		Last Modified: Tue, 24 Feb 2026 19:00:35 GMT  
		Size: 4.7 MB (4709832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:9ec580a8a2c10e1b7ac74c5a41f66009751caa3a8d2b0dc76ce73021e5457329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3590dbb7640207ebd9aa49bf6c514655778ebcc0dea1bf38fe7da73c02990d03`

```dockerfile
```

-	Layers:
	-	`sha256:93ef4bd1a5d0d962b395d82efceb8f97a7d23f4cd0a74978d0edd9456835b58f`  
		Last Modified: Tue, 24 Feb 2026 19:00:31 GMT  
		Size: 5.6 MB (5586024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:025639689d36438751d0440bf57caefab23fbf1a4e77b9cc3febff3196f2a2b9`  
		Last Modified: Tue, 24 Feb 2026 19:00:31 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v7

```console
$ docker pull irssi@sha256:e65224016b946c4d99129fad9314bdbdc0bf0296df171d4ce13bc5aa24cb6cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48688484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9c173ed818b8888f5cbf8f2e9258855675b8dd27c9cb7908c704a1d3069397`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:03:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:03:16 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:03:16 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:03:16 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:03:16 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:03:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:03:58 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:03:58 GMT
USER user
# Tue, 24 Feb 2026 19:03:58 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6afde1291a25c0cc231ccde29bbe0ad9ff81c712d4e11e050becb6d4ba8ce0d`  
		Last Modified: Tue, 24 Feb 2026 19:04:08 GMT  
		Size: 17.9 MB (17913151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b8f6d599a61d91e34fb4362460af69da8f684fd2226c0a12c37f1fee9652b8`  
		Last Modified: Tue, 24 Feb 2026 19:04:07 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4575a9012f56ba332b5c7534e48f48a25065b112fa4613e17f2d061261eb8e13`  
		Last Modified: Tue, 24 Feb 2026 19:04:08 GMT  
		Size: 4.6 MB (4558224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:578b6038b34fa00900a70d96abebf8df03f41cbef32e270af68c766ed6703f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9176d67dd016c9ba37147b21f657ef2ae76348260f1f72189b8dc548007b5a73`

```dockerfile
```

-	Layers:
	-	`sha256:cca03ae28695eb959e228e35c2e861a53e15134500b965d0f79e67be15a1cf50`  
		Last Modified: Tue, 24 Feb 2026 19:04:08 GMT  
		Size: 5.6 MB (5589046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dade344df2087c2cbe360a19c02237de12027a28b597247bd6d4844a90a5dad`  
		Last Modified: Tue, 24 Feb 2026 19:04:07 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:b5705a932a1071d49bc33cb793e6492a17f0c13a09af00c00847132826a5399d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53975047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95271ad57b650f4906bebb73ced93170cb93cdc9485991098fde0de3c6ac7f3b`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:06:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:06:10 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:06:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:06:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:06:46 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:06:46 GMT
USER user
# Tue, 24 Feb 2026 19:06:46 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bde18e6576dd26665639dfee2e2c29ab72d5a490303fa301ad8b6d16d01032`  
		Last Modified: Tue, 24 Feb 2026 19:06:58 GMT  
		Size: 19.1 MB (19050073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb0f26017633de6d20b077a7d5fbc6cc2e5ca7a1231309bb6d18d9c6914a55b`  
		Last Modified: Tue, 24 Feb 2026 19:06:57 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5666611ba24e987a94791ca84b6bb380525795696e072f0d60ba9d17ade814ef`  
		Last Modified: Tue, 24 Feb 2026 19:06:57 GMT  
		Size: 4.8 MB (4781514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:900b2ed2e203d81d8f8d6a5cd524d2db8b91bd6962cbb74ffcb0d2a396647107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136a2b4c868d58cd89f9de10c7f831de5ff64687d2b3f76d4e7c01b8ffa16584`

```dockerfile
```

-	Layers:
	-	`sha256:2fef361a887b7785b6efd16d1c15d0262f2f2c6d45edab1f8a975ba81b6f1fdd`  
		Last Modified: Tue, 24 Feb 2026 19:06:57 GMT  
		Size: 5.6 MB (5594959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb64f6057abd305766916ed63546cbd132d825a2da5422247487175382c5f5b9`  
		Last Modified: Tue, 24 Feb 2026 19:06:57 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; 386

```console
$ docker pull irssi@sha256:47a406a29379abd6ed06b0d20217433e973e2870d780ff30823782f31e5c6b33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54908577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91e586aa3e8ce17d01aee6359c922ffe41daa80e277df7ae8ed8d1889e1bb0b`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:58:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 18:58:30 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 18:58:30 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 18:58:30 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 18:58:30 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 18:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 18:59:11 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 18:59:11 GMT
USER user
# Tue, 24 Feb 2026 18:59:11 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ae61c08fa4b2cc99f86dc6a1fe4823c3e0ac9a711287f64cac6485a6238ac8`  
		Last Modified: Tue, 24 Feb 2026 18:59:21 GMT  
		Size: 18.7 MB (18742816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf3f98a9e73f8a6e5b1989e717a2286e372230bcaff62941bae689905197df8`  
		Last Modified: Tue, 24 Feb 2026 18:59:20 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a297182723d0165449b463b3d8873cf3e889a114d50096866c842a8e640504`  
		Last Modified: Tue, 24 Feb 2026 18:59:21 GMT  
		Size: 4.9 MB (4868483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:6c462d49b091009b00485bef9ea87abfab3cb1639844d8c0ed87db6e3e81f5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ff00c0c6b361160a520647c72a3cf1d9322aed6a3382745d35d0d05d128d4e`

```dockerfile
```

-	Layers:
	-	`sha256:b4fd1d01133f85b3efcc51e3d12301590bbb5fb57101916a792336a8d1dea592`  
		Last Modified: Tue, 24 Feb 2026 18:59:21 GMT  
		Size: 5.6 MB (5584598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00eea56a9297862479d3e58a1bd8c833d2a522ff54655c30af9634f5c984d84d`  
		Last Modified: Tue, 24 Feb 2026 18:59:20 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; ppc64le

```console
$ docker pull irssi@sha256:91b49338a181c6d7b1ae5689c2a610af4dcb438d1eb567f96160219d271063f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58240333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4fc70f04320b975862b6d37425c6f5766d3f6c2e97e62049747274abf47acc`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:07:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:07:22 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:07:22 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:07:22 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:07:22 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:09:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:09:16 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:09:16 GMT
USER user
# Tue, 24 Feb 2026 19:09:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5beebebe5029aabb929ae44c4537e3b21fd8d65921a409bb2df1b7c9b634b6d`  
		Last Modified: Tue, 24 Feb 2026 19:09:44 GMT  
		Size: 19.5 MB (19538939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed570b0aeb97d8cb44da9c8850814c6aa7e1b43fe3d9f4058d9d5a52f0eb6224`  
		Last Modified: Tue, 24 Feb 2026 19:09:43 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ecef354c37ad21cbe5f6e442c1f3c79f858cd86e1ece389542887cae1cff44d`  
		Last Modified: Tue, 24 Feb 2026 19:09:43 GMT  
		Size: 5.1 MB (5097820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:38354f39cc3e23ea94d1feaca94d6602908c74c9dbd5beddfeeb5bd33866538a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904a8b4a8a183068c5d6db74160bbb18d87a4c74f95375cf320b45143257753e`

```dockerfile
```

-	Layers:
	-	`sha256:4c2d2dc5bef56d23df0cb5b905d48dc667fb78e0a3c3a168e9e8a3a4f7f1b318`  
		Last Modified: Tue, 24 Feb 2026 19:09:43 GMT  
		Size: 5.6 MB (5595506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:373385b6bc18ef5a4933f2dfe5147cd4368d7f2730b1f214cd1abe2372ffb0d2`  
		Last Modified: Tue, 24 Feb 2026 19:09:43 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; riscv64

```console
$ docker pull irssi@sha256:3a7d38a48cd82c9bd2d5741f468dcdfbf92e333ecc06c2d12dbfe8b938ab0307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51693147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0a99e5b7cd8d4f262722aed889c863e4c892a0f23fe9749d929e8dec75cf662`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 03:03:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 03:03:38 GMT
ENV HOME=/home/user
# Wed, 25 Feb 2026 03:03:38 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 25 Feb 2026 03:03:38 GMT
ENV LANG=C.UTF-8
# Wed, 25 Feb 2026 03:03:38 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 25 Feb 2026 03:10:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 25 Feb 2026 03:10:25 GMT
WORKDIR /home/user
# Wed, 25 Feb 2026 03:10:25 GMT
USER user
# Wed, 25 Feb 2026 03:10:25 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6508c3cdfc31f498c772515ee0821b13440e08ba735c32d3cba318269a3f687`  
		Last Modified: Wed, 25 Feb 2026 03:12:21 GMT  
		Size: 18.6 MB (18552692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ef556a8959335b7e794bf6752b54a81934178688ef1e7d4dbdb197aa0eb326`  
		Last Modified: Wed, 25 Feb 2026 03:12:16 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2794c755bfc5dceb9c6a1eb2ff258465b48801c3bd877b5cde6f46d9920a5c`  
		Last Modified: Wed, 25 Feb 2026 03:12:18 GMT  
		Size: 4.9 MB (4860678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:5ad91e36e6745d334569f2aede71764aa6ab0c8d2ed12405c01d1a981287b5ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ebcaf2e72424c63e04d825e7d04bbe5589f3f805c573faf9c8484afea2b540f`

```dockerfile
```

-	Layers:
	-	`sha256:5c3be456f6ce9090fac8cee71f4291c1aaef1a9ac164f8e2bd0de699367a6334`  
		Last Modified: Wed, 25 Feb 2026 03:12:18 GMT  
		Size: 5.6 MB (5579778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9be1a19638d1af3b7539195ea9d207d142146b312fe552361ffde9b48f90de25`  
		Last Modified: Wed, 25 Feb 2026 03:12:16 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; s390x

```console
$ docker pull irssi@sha256:9d2c67d051b5f92f329619102e0e2bc0df643ef026d1f553c93d501eb54b0049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54516690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf87075c86e270be08f7350f9904070bb3c572934e47a6d6aa9e70fefbff3812`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:01:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:01:50 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:01:50 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:01:50 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:01:50 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:03:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:03:57 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:03:57 GMT
USER user
# Tue, 24 Feb 2026 19:03:57 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb8e7c85a43a84dc9bfa10f335db4cb6dbd00571742698dd7d26077875d9a48`  
		Last Modified: Tue, 24 Feb 2026 19:04:25 GMT  
		Size: 19.8 MB (19768672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e12ffbdb3791dcf1981e8eefcf126275f55fe052fac3a8fafc881aac17c34d8`  
		Last Modified: Tue, 24 Feb 2026 19:04:24 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149d77b47e1605f5cda1129f653ed9adbc0c8c0c2286fd9e81c91c6c44d32956`  
		Last Modified: Tue, 24 Feb 2026 19:04:25 GMT  
		Size: 4.9 MB (4906478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:d10e5a37df33b885dd47403b1e8b7a310eb535821e3b44695a144c5fb72da92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b0fb8133b9ed0bb88f527230ee5b7eefff618321781bea5b846e5b8d1ea2a2`

```dockerfile
```

-	Layers:
	-	`sha256:9ab81d1d85995cb9010ed56d4fdb909af0e66dc54953575d97300c5e3eb22dbe`  
		Last Modified: Tue, 24 Feb 2026 19:04:24 GMT  
		Size: 5.6 MB (5589380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5cb68be6babc8fbd8fc9be84183610c6d3f88b4fb466e15ef8526dfead89283`  
		Last Modified: Tue, 24 Feb 2026 19:04:24 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:trixie`

```console
$ docker pull irssi@sha256:6f18ede25b4d4593ab99544ab52277a4e1254f2fbe6a64def5eb7de58074fffc
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
$ docker pull irssi@sha256:49c3737149b22851a93ba69ac22cebd9abf8c8a5d5994e2ca286860caf15353a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53871168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f752e1dfe12c027448c72cd5e3229ea7002dea38239febe081da26b8f7b27ed3`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:03:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:03:00 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:03:00 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:03:00 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:03:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:03:41 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:03:41 GMT
USER user
# Tue, 24 Feb 2026 19:03:41 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7ad25661c3266880a3c864c64ca6faa3b88c0ddb4a998a667e1f1d4b99a22d`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 19.2 MB (19222246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc80a3f9407efa5dcf0dc0ba37f425c82a6ecff60485ff89dd844390ff01a53`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d808574b07af61087631c143ffb9e4be37c1313e4d6fb331c97d17da0f436b32`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 4.9 MB (4866927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:abd6aeef322973ea82182a219b2ba14441f100be5d532e6f7b52e6062bc15a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979b803961d56ac53e2960a4847046894c3f5095836cf0aa2fd343e0288e1e0e`

```dockerfile
```

-	Layers:
	-	`sha256:3557d7d8d5e4df3d7ade5b19b149d56205ce87989a1066808f14bcf3f4321be4`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 5.6 MB (5588475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94196f7468e34a70daa83619d0cf5061ae5adf7711aca144d3d43fc9475a48da`  
		Last Modified: Tue, 24 Feb 2026 19:03:51 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:6887b2daf7a8e04420d9f8019955beefca4b05d2370737f5085f12f8bb863c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50955082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82db261419aa9d562d5751330a1b61cd4d76e7c5028123921b370b072d4e9c19`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:59:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 18:59:28 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 18:59:28 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 18:59:28 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 18:59:28 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:00:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:00:20 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:00:20 GMT
USER user
# Tue, 24 Feb 2026 19:00:20 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7364bcc76ebade3ad468fc97fcab1317a1b01976383c65ec8f166e9828038c67`  
		Last Modified: Tue, 24 Feb 2026 19:00:34 GMT  
		Size: 18.3 MB (18294280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d702d54a8b971c044db6fb77d45b0c781dbb99062e9faf1a81743c47fc56bf`  
		Last Modified: Tue, 24 Feb 2026 19:00:31 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b41ba1be7d2ca3c964a8be01ccc30e64cc8a0ca03702c32d5870d2d3d769bb`  
		Last Modified: Tue, 24 Feb 2026 19:00:35 GMT  
		Size: 4.7 MB (4709832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:9ec580a8a2c10e1b7ac74c5a41f66009751caa3a8d2b0dc76ce73021e5457329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3590dbb7640207ebd9aa49bf6c514655778ebcc0dea1bf38fe7da73c02990d03`

```dockerfile
```

-	Layers:
	-	`sha256:93ef4bd1a5d0d962b395d82efceb8f97a7d23f4cd0a74978d0edd9456835b58f`  
		Last Modified: Tue, 24 Feb 2026 19:00:31 GMT  
		Size: 5.6 MB (5586024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:025639689d36438751d0440bf57caefab23fbf1a4e77b9cc3febff3196f2a2b9`  
		Last Modified: Tue, 24 Feb 2026 19:00:31 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:e65224016b946c4d99129fad9314bdbdc0bf0296df171d4ce13bc5aa24cb6cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48688484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9c173ed818b8888f5cbf8f2e9258855675b8dd27c9cb7908c704a1d3069397`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:03:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:03:16 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:03:16 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:03:16 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:03:16 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:03:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:03:58 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:03:58 GMT
USER user
# Tue, 24 Feb 2026 19:03:58 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6afde1291a25c0cc231ccde29bbe0ad9ff81c712d4e11e050becb6d4ba8ce0d`  
		Last Modified: Tue, 24 Feb 2026 19:04:08 GMT  
		Size: 17.9 MB (17913151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b8f6d599a61d91e34fb4362460af69da8f684fd2226c0a12c37f1fee9652b8`  
		Last Modified: Tue, 24 Feb 2026 19:04:07 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4575a9012f56ba332b5c7534e48f48a25065b112fa4613e17f2d061261eb8e13`  
		Last Modified: Tue, 24 Feb 2026 19:04:08 GMT  
		Size: 4.6 MB (4558224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:578b6038b34fa00900a70d96abebf8df03f41cbef32e270af68c766ed6703f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9176d67dd016c9ba37147b21f657ef2ae76348260f1f72189b8dc548007b5a73`

```dockerfile
```

-	Layers:
	-	`sha256:cca03ae28695eb959e228e35c2e861a53e15134500b965d0f79e67be15a1cf50`  
		Last Modified: Tue, 24 Feb 2026 19:04:08 GMT  
		Size: 5.6 MB (5589046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dade344df2087c2cbe360a19c02237de12027a28b597247bd6d4844a90a5dad`  
		Last Modified: Tue, 24 Feb 2026 19:04:07 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:b5705a932a1071d49bc33cb793e6492a17f0c13a09af00c00847132826a5399d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53975047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95271ad57b650f4906bebb73ced93170cb93cdc9485991098fde0de3c6ac7f3b`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:06:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:06:10 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:06:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:06:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:06:46 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:06:46 GMT
USER user
# Tue, 24 Feb 2026 19:06:46 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bde18e6576dd26665639dfee2e2c29ab72d5a490303fa301ad8b6d16d01032`  
		Last Modified: Tue, 24 Feb 2026 19:06:58 GMT  
		Size: 19.1 MB (19050073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb0f26017633de6d20b077a7d5fbc6cc2e5ca7a1231309bb6d18d9c6914a55b`  
		Last Modified: Tue, 24 Feb 2026 19:06:57 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5666611ba24e987a94791ca84b6bb380525795696e072f0d60ba9d17ade814ef`  
		Last Modified: Tue, 24 Feb 2026 19:06:57 GMT  
		Size: 4.8 MB (4781514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:900b2ed2e203d81d8f8d6a5cd524d2db8b91bd6962cbb74ffcb0d2a396647107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136a2b4c868d58cd89f9de10c7f831de5ff64687d2b3f76d4e7c01b8ffa16584`

```dockerfile
```

-	Layers:
	-	`sha256:2fef361a887b7785b6efd16d1c15d0262f2f2c6d45edab1f8a975ba81b6f1fdd`  
		Last Modified: Tue, 24 Feb 2026 19:06:57 GMT  
		Size: 5.6 MB (5594959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb64f6057abd305766916ed63546cbd132d825a2da5422247487175382c5f5b9`  
		Last Modified: Tue, 24 Feb 2026 19:06:57 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; 386

```console
$ docker pull irssi@sha256:47a406a29379abd6ed06b0d20217433e973e2870d780ff30823782f31e5c6b33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54908577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91e586aa3e8ce17d01aee6359c922ffe41daa80e277df7ae8ed8d1889e1bb0b`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:58:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 18:58:30 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 18:58:30 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 18:58:30 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 18:58:30 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 18:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 18:59:11 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 18:59:11 GMT
USER user
# Tue, 24 Feb 2026 18:59:11 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ae61c08fa4b2cc99f86dc6a1fe4823c3e0ac9a711287f64cac6485a6238ac8`  
		Last Modified: Tue, 24 Feb 2026 18:59:21 GMT  
		Size: 18.7 MB (18742816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf3f98a9e73f8a6e5b1989e717a2286e372230bcaff62941bae689905197df8`  
		Last Modified: Tue, 24 Feb 2026 18:59:20 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a297182723d0165449b463b3d8873cf3e889a114d50096866c842a8e640504`  
		Last Modified: Tue, 24 Feb 2026 18:59:21 GMT  
		Size: 4.9 MB (4868483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:6c462d49b091009b00485bef9ea87abfab3cb1639844d8c0ed87db6e3e81f5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ff00c0c6b361160a520647c72a3cf1d9322aed6a3382745d35d0d05d128d4e`

```dockerfile
```

-	Layers:
	-	`sha256:b4fd1d01133f85b3efcc51e3d12301590bbb5fb57101916a792336a8d1dea592`  
		Last Modified: Tue, 24 Feb 2026 18:59:21 GMT  
		Size: 5.6 MB (5584598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00eea56a9297862479d3e58a1bd8c833d2a522ff54655c30af9634f5c984d84d`  
		Last Modified: Tue, 24 Feb 2026 18:59:20 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:91b49338a181c6d7b1ae5689c2a610af4dcb438d1eb567f96160219d271063f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58240333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4fc70f04320b975862b6d37425c6f5766d3f6c2e97e62049747274abf47acc`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:07:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:07:22 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:07:22 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:07:22 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:07:22 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:09:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:09:16 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:09:16 GMT
USER user
# Tue, 24 Feb 2026 19:09:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5beebebe5029aabb929ae44c4537e3b21fd8d65921a409bb2df1b7c9b634b6d`  
		Last Modified: Tue, 24 Feb 2026 19:09:44 GMT  
		Size: 19.5 MB (19538939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed570b0aeb97d8cb44da9c8850814c6aa7e1b43fe3d9f4058d9d5a52f0eb6224`  
		Last Modified: Tue, 24 Feb 2026 19:09:43 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ecef354c37ad21cbe5f6e442c1f3c79f858cd86e1ece389542887cae1cff44d`  
		Last Modified: Tue, 24 Feb 2026 19:09:43 GMT  
		Size: 5.1 MB (5097820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:38354f39cc3e23ea94d1feaca94d6602908c74c9dbd5beddfeeb5bd33866538a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904a8b4a8a183068c5d6db74160bbb18d87a4c74f95375cf320b45143257753e`

```dockerfile
```

-	Layers:
	-	`sha256:4c2d2dc5bef56d23df0cb5b905d48dc667fb78e0a3c3a168e9e8a3a4f7f1b318`  
		Last Modified: Tue, 24 Feb 2026 19:09:43 GMT  
		Size: 5.6 MB (5595506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:373385b6bc18ef5a4933f2dfe5147cd4368d7f2730b1f214cd1abe2372ffb0d2`  
		Last Modified: Tue, 24 Feb 2026 19:09:43 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:3a7d38a48cd82c9bd2d5741f468dcdfbf92e333ecc06c2d12dbfe8b938ab0307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51693147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0a99e5b7cd8d4f262722aed889c863e4c892a0f23fe9749d929e8dec75cf662`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 03:03:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 03:03:38 GMT
ENV HOME=/home/user
# Wed, 25 Feb 2026 03:03:38 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 25 Feb 2026 03:03:38 GMT
ENV LANG=C.UTF-8
# Wed, 25 Feb 2026 03:03:38 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 25 Feb 2026 03:10:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 25 Feb 2026 03:10:25 GMT
WORKDIR /home/user
# Wed, 25 Feb 2026 03:10:25 GMT
USER user
# Wed, 25 Feb 2026 03:10:25 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6508c3cdfc31f498c772515ee0821b13440e08ba735c32d3cba318269a3f687`  
		Last Modified: Wed, 25 Feb 2026 03:12:21 GMT  
		Size: 18.6 MB (18552692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ef556a8959335b7e794bf6752b54a81934178688ef1e7d4dbdb197aa0eb326`  
		Last Modified: Wed, 25 Feb 2026 03:12:16 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2794c755bfc5dceb9c6a1eb2ff258465b48801c3bd877b5cde6f46d9920a5c`  
		Last Modified: Wed, 25 Feb 2026 03:12:18 GMT  
		Size: 4.9 MB (4860678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:5ad91e36e6745d334569f2aede71764aa6ab0c8d2ed12405c01d1a981287b5ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ebcaf2e72424c63e04d825e7d04bbe5589f3f805c573faf9c8484afea2b540f`

```dockerfile
```

-	Layers:
	-	`sha256:5c3be456f6ce9090fac8cee71f4291c1aaef1a9ac164f8e2bd0de699367a6334`  
		Last Modified: Wed, 25 Feb 2026 03:12:18 GMT  
		Size: 5.6 MB (5579778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9be1a19638d1af3b7539195ea9d207d142146b312fe552361ffde9b48f90de25`  
		Last Modified: Wed, 25 Feb 2026 03:12:16 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; s390x

```console
$ docker pull irssi@sha256:9d2c67d051b5f92f329619102e0e2bc0df643ef026d1f553c93d501eb54b0049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54516690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf87075c86e270be08f7350f9904070bb3c572934e47a6d6aa9e70fefbff3812`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:01:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:01:50 GMT
ENV HOME=/home/user
# Tue, 24 Feb 2026 19:01:50 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 24 Feb 2026 19:01:50 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:01:50 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 24 Feb 2026 19:03:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 24 Feb 2026 19:03:57 GMT
WORKDIR /home/user
# Tue, 24 Feb 2026 19:03:57 GMT
USER user
# Tue, 24 Feb 2026 19:03:57 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb8e7c85a43a84dc9bfa10f335db4cb6dbd00571742698dd7d26077875d9a48`  
		Last Modified: Tue, 24 Feb 2026 19:04:25 GMT  
		Size: 19.8 MB (19768672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e12ffbdb3791dcf1981e8eefcf126275f55fe052fac3a8fafc881aac17c34d8`  
		Last Modified: Tue, 24 Feb 2026 19:04:24 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149d77b47e1605f5cda1129f653ed9adbc0c8c0c2286fd9e81c91c6c44d32956`  
		Last Modified: Tue, 24 Feb 2026 19:04:25 GMT  
		Size: 4.9 MB (4906478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:d10e5a37df33b885dd47403b1e8b7a310eb535821e3b44695a144c5fb72da92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b0fb8133b9ed0bb88f527230ee5b7eefff618321781bea5b846e5b8d1ea2a2`

```dockerfile
```

-	Layers:
	-	`sha256:9ab81d1d85995cb9010ed56d4fdb909af0e66dc54953575d97300c5e3eb22dbe`  
		Last Modified: Tue, 24 Feb 2026 19:04:24 GMT  
		Size: 5.6 MB (5589380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5cb68be6babc8fbd8fc9be84183610c6d3f88b4fb466e15ef8526dfead89283`  
		Last Modified: Tue, 24 Feb 2026 19:04:24 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json
